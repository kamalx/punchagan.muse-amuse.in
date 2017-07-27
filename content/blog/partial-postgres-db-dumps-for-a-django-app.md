+++
title = "Partial postgres db dumps for a Django app"
date = "2016-01-10T00:00:00+05:30"
tags = ["blag", "django", "postgres", "sql"]
draft = false
+++

Off late, I have been working with a large `postgres` database that is used by
an app built in `Django`.  I wanted a partial dump of the database to try out
some experimental clean up scripts.  I haven't really used databases before,
and the last time I had to do this I did it in a pretty ad-hoc fashion.  This
time around, I tried to do it more methodically and to document it.


## The Django Route {#the-django-route}

I looked around for tools that let you do this, and found [django-fixture-magic](https://github.com/davedash/django-fixture-magic).
I first tried it out on my older partial dump (10% as large as the original db)
and it turned out to be reasonably fast and worked well, after making a [few
changes](https://github.com/davedash/django-fixture-magic/pull/35) to get it working with Python 3.x.  Its `kitchensink` flag to the
`dump_object` seemed like a promising option, but **didn't** really seem to get all
the required tables for ManyToManyFields.  I worked around it, by getting a
dump of all the models which were related using Django's `dumpdata`.


### Get a dump with objects of interest {#get-a-dump-with-objects-of-interest}

The `dump_object` command lets you run commands to select the objects that you
want to have in the dump, and that is quite a useful thing.

```sh
python manage.py dump_object dataset.Product -k --query '{"subcategory_id__in": [1886, ...]}' > products.json
```

Also, get a dump of related tables.

```sh
# Dump of related fields
python manage.py dumpdata dataset.Attribute > attributes.json
```


### Create the new empty db {#create-the-new-empty-db}

Next, create a new database where this fixture can be loaded!

```sh
# Create the db
sudo su - postgres
createdb mydb

# Create a user, if required
createuser -P

```


#### Grant access to the user {#grant-access-to-the-user}

In the `psql` prompt type the following to grant the user permissions for the
database.

```sql
GRANT ALL PRIVILEGES ON DATABASE mydb TO myuser;
```


### Fix settings.py and create tables for the models. {#fix-settings-dot-py-and-create-tables-for-the-models-dot}

Make changes to `settings.py` to use the newly created database, and then
create the tables used by the app, and then load the data.

```sh
python manage.py syncdb
python manage.py loaddata products.json
```


### Too slow! {#too-slow}

This method worked and was reasonably fast when I was trying to get 20k rows
from a table with about 200k rows, with all the dependencies.

But, when I tried to get a dump of about 200k rows from a table with 2M rows,
it was way too slow to be of any use.  There could've been a couple of reasons
for this, which I didn't have the time to look into, and debug.

-   The web-server where the `Django` app was running, and the `db` server with
    the `postgres` database were on different machines in separate datacenters,
    which could've been adding a significant amount of latency.

-   Just the size of the database being much larger could be making it slower?

These are things I should be looking into and learning about, when I have more
time at hand.  For now, I needed a quicker way to get a dump.  Even though the
raw SQL route was more manual, it turned out to be much quicker.


## Raw SQL dump route {#raw-sql-dump-route}


### Get a dump of the interesting tables {#get-a-dump-of-the-interesting-tables}

First, I had to get a dump of all the tables with the data I was interested in,
one-by-one.

```sql
COPY (SELECT * FROM "dataset_product" WHERE ("dataset_product"."subcategory_id" IN (319557, 94589, 332, 406, 626, 1886) AND "dataset_product"."gender_id" = 1)) TO '/tmp/products.tsv'

COPY (SELECT * FROM "dataset_photo" WHERE "dataset_photo"."product_id" IN (SELECT U0."id" FROM "dataset_product" U0 WHERE (U0."subcategory_id" IN (319557, 94589, 332, 406, 626, 1886) AND U0."gender_id" = 1))) TO '/tmp/photos.tsv'

-- Copy a bunch of other tables!
```


### Load the data from the dumps {#load-the-data-from-the-dumps}

```sql
-- syncdb
COPY dataset_product FROM '/tmp/products.tsv' ENCODING 'UTF8';
COPY dataset_photo FROM '/tmp/photos.tsv' ENCODING 'UTF8';
-- Copy a bunch of other tables!
```


### Make tables writable {#make-tables-writable}

Some of the tables did not let me write anything to them, until I [altered the
sequence](http://centoshowtos.org/web-services/django-and-postgres-duplicate-key/) for these tables.


### Automating {#automating}

It would be pretty nice if all of this was automated -- allow a user to enter
exactly the same kind of a query that `django-fixture-magic` lets you run, and
figure out the SQL copies that need to be done to get the requested dump. Its
something that currently would qualify as yak-shaving, but may be a handy thing
to have. Someone somewhere possibly already has something that does this.

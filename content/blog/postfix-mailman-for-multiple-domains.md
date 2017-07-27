+++
title = "Postfix + Mailman for Multiple Domains."
date = "2009-08-05T00:00:00+05:30"
tags = ["ology"]
draft = false
+++

Well, there are a hazaar tutorials on setting up Postfix and
Mailman for Debian for a single domain. There were a few for doing
that for multiple domains also, but nothing comprehensive, if I
could say so. This link is pretty comprehensive and details all
the steps for setting up Postfix for a single domain.  Here is all
you'll want to know about setting up Virtual domains in Postfix.

You only need to make a few changes for adding a second (or more)
domain. You just need to add the `virtual_alias_domains` and add
`virtual_alias_maps`. Here is a glimpse of how my `main.cf` looks:

```text
myhostname = mail.abc.in
mydomain = abc.in
mydestination = $myhostname, $mydomain, localhost.$mydomain
myorigin = /etc/mailname
virtual_alias_maps =
                hash:/etc/postfix/virtual-xyz,
                hash:/etc/postfix/virtual-abc,
                hash:/var/lib/mailman/data/virtual-mailman
virtual_alias_domains = xyz.in, mail.xyz.in
```

`virtual-xyz` and `virtual-abc` contain the virtual aliases for
each domain. Note that Postfix expects hash files and hence you
need to run `postmap /etc/postfix/virtual-abc` each
time the file is changed, to keep the hash file in sync with the
text file that you edit. Also, you need to run `postfix reload`,
each time you make changes to `main.cf` or `master.cf`

Fairly straight forward, right? But it took me quite sometime to
get it all right, since this was the first time I was doing
anything with Mail Transfer Agents or the like.

Now, onto Mailman. Well the Installation Manual of Mailman,
literally has it all. Here is a look at how my
`mm_cfg.py` looks:

```text
DEFAULT_EMAIL_HOST = 'abc.in'
DEFAULT_URL_HOST   = 'mail.abc.in'
add_virtualhost(DEFAULT_URL_HOST, DEFAULT_EMAIL_HOST)
POSTFIX_STYLE_VIRTUAL_DOMAINS=['xyz.in']
add_virtualhost('mail.xyz.in', 'xyz.in')
MTA='Postfix'
```

The only trouble was to get mailing lists with same names on both
the domains (which I couldn't get working). I experimented with
multiple mailman instances but that won't work because the MTA
can't differentiate between the two instances of mailman. The
alternative is probably to have two instances of postfix running
too. But that I felt was like going too far, and gave up. [What if
we wanted to add another domain to the list?!]

Also, I had to make a few alterations to the Apache file to allow
access to the mailman pages without breaking the Zope redirection
that was already set-up.

[Thanks to Shantanu and Vattam (and all the hazaar people using
Postfix and Mailman and cared to document things for the sake of
others, and of course Google)]

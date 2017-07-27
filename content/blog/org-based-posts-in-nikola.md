+++
title = "Org based posts in Nikola"
date = "2014-04-20T00:00:00+05:30"
tags = ["blog", "emacs", "nikola", "orgmode"]
draft = false
+++

[Chen Bin](http://binchen.org/) asked me to share my Nikola+Org work-flow, and share an
example post.

The org source for any post can be found by changing the URL of a post
from `.html` to `.org`.

I don't have much of a work-flow, because I don't post too often, but
here is what I typically do, to make a new post.

I start off by creating a new post using

```sh
$ nikola new_post
```

and then give the post a title and start editing the post in Emacs.

I have a simple snippet that lets me insert tags, based on existing
tags.

<script src="https://gist.github.com/6629020.js"></script>

Once I'm happy with the content of a post, I run `nikola auto` to
build the source and serve it locally, and see if the post "looks"
reasonable, after being rendered.

Once, I'm happy with it, I commit the post and deploy it using `nikola
deploy`.

I also have a plugin, that posts captured bookmarks and quotes onto
the blog, with a single command. I should probably make the sources of
my blog open, and push it onto GitHub.

**Update <span class="timestamp-wrapper"><span class="timestamp">[2015-05-13 Wed]</span></span>**

-   I use my own [plugin](https://plugins.getnikola.com/#orgmode) for Nikola which lets me write posts in org-mode.  There
    is a similar [plugin](https://github.com/redguardtoo/org2nikola) by Chen Bin, that exports posts to intermediate html,
    that is then used by Nikola.

-   The source for my blog is now on [GitHub](https://github.com/punchagan/punchagan.muse-amuse.in)

-   I also have [custom elisp](https://github.com/punchagan/dot-emacs/blob/master/punchagan.org#nikola-stuff) to be able to make a new post, and deploy the site
    from within Emacs.

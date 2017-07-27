+++
title = "Pandoc can now do Org"
date = "2010-12-06T00:00:00+05:30"
tags = ["emacs", "haskell", "orgmode"]
draft = false
+++

Pandoc is a haskell library and a command line tool, that can
convert markup from one to another and it does it pretty well.
Until now it supported quite a few markups, but not orgmode.  But
now, Orgmode support has been added! Yay!

But, it can only read from other formats and write to org-mode
format.  The other way around, is not possible, but you can do
that straight from org-mode, right?

I've often felt the need for an org-importer and hence decided to
do something about it.  I stumbled upon Pandoc, when I was moving
my blog, and found it pretty neat.  After, yet another request for
an importer, on the org-mode mailing list, I decided to look at
Pandoc.  I was somehow under the impression that it was written in
Python.  But it turned out, I had to learn Haskell!  A good excuse
to learn a new language, eh?  I brushed through a tutorial for a
couple of days (and was blown off by the paradigm of the language)
and was able to port the RST writer in Pandoc, to an Org
writer.  :)

You can get the latest version from here

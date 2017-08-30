---
title : "Recurse Center, 2014-06-23"
date : 2014-06-23T04:38:29-04:00
tags : ["conference", "git", "principle"]
categories : ["recursecenter"]
draft : false
---

-   The Apprenticeship patterns book is very interesting!  I shall
    continue to read it and start create daily/weekly rituals from the
    actions prescribed in the book!
-   I was reading [this post](http://blogs.collab.net/git/protect-git-history#.U6fixh-caV4) on `git gc`, `reflog`, etc. and wanted to
    see what the default values were for some of the configurable
    variables.  But, the git config command didn't help.  Developer/code
    defaults are also a part of the "config" system, and any tools to
    inspect config variables should display them, if no other values
    have been set explicitly!
-   "If experience is built upon failure as much as success, then you
    need a more or less private space where you can seek out failure."
    -- Apprenticeship Patterns.
-   Our check-in groups changed, but 3 of us from our last check-in
    group are together again!
-   Most of the day was spent with Git.  In the morning, I learned that
    setting `push.default` to `nothing` will prevent pushing any
    branches without specifying explicitly which branch I want to push.
-   Also, later in the day, Alan gave a presentation mapping the
    internals of git to the commands, trying to give everyone a better
    mental model of Git.
-   I spent some time trying to get `jedi` integration for `emacs`. It
    should've worked out of the box, but I'm not sure the ELPA
    repositories have proper dependency/version management.  Seems to be
    the problem, everywhere!  Dependencies of a package get updated, and
    the package starts acting up...
-   Chaitu sent me a link about solving mazes using Finite Automata, and
    I spent some time trying to write a simple solver, and compare it
    with Nava's breadth first search.  But, it looks like we broke her
    code during the refactor.  I may get back to this, at some point.
-   I also spent a few minutes talking to Kyle, while he was trying to
    implement a simple version of the NTP protocol.  The algorithm it
    turns out, is pretty simple.
-   I started reading a little bit on crypt-analysis for Simple
    Substitution ciphers, and I'll try implementing one of the
    algorithms today.
-   The day ended with yummy pizza and video watching!  We watched --
    -   Bret Victor, [Inventing on Principle](http://vimeo.com/36579366) (54 min)
    -   Gary Bernhardt, [WAT](https://www.destroyallsoftware.com/talks/wat) (4 min)
    -   Guy Steele, [Growing a Language](https://www.youtube.com/watch?v=_ahvzDzKdB0) (53 min)

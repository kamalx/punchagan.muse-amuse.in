---
title : "Recurse Center, 2014-08-11"
date : 2014-08-11T11:16:08-04:00
tags : ["django", "python", "twitter"]
categories : ["recursecenter"]
draft : false
---

-   I spent about an hour in the morning testing out the staging blaggregator
    instance, and things seemed to work as expected.  Side note, I got added as a
    collaborator on the blaggregator repo!
-   We worked through the first chapter on getting video working, but we mostly
    ended up just copying code rather than actually understanding/carefully
    studying it.  I'm not sure how I feel about it, but we got to display fancy
    stuff.
-   I wasn't feeling like working on any of my 'old'/'ongoing' projects, and
    since Mondays don't feel very productive, I worked on writing a couple of
    simple scripts to create twitter lists of HSers, batch wise.

    For the HS API, I just reused some old code I had lying around from my
    experiments with the OAuth2 API, though I had to tweak it a little bit to be
    able to actually login, using requests. Something about CSRF tokens seems to
    have changed.

    In the process, I found that twitter's API isn't very pleasant to use.  Or
    may be it's the fact that I was using python twitter client without getting
    my own client id/key, but the whole experience of dealing with the twitter
    API wasn't a pleasant one at all!
-   Amber, Daria and I also spent about an hour white-boarding some problems from
    the Cracking the Code Interview book.
-   I ended up fixing some minor issues with blaggregator and am hoping that the
    long pending PR will be merged today.

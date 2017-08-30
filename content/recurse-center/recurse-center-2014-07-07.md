---
title : "Recurse Center, 2014-07-07"
date : 2014-07-08T10:07:20-04:00
tags : ["programming", "python", "thought", "writing"]
categories : ["recursecenter"]
draft : false
---

-   As preparation for a one-on-one this week with one of the facilitators, I was
    wondering if I was really getting better as a programmer, by doing what I am
    doing.
-   I have heard at numerous places that reading and reflection are keys to
    getting better. I feel like I haven't been giving these things much attention
    in the past couple of weeks. I don't catch up on reading all the awesome
    reading material shared on Zulip and I switched from writing this blog post
    first thing in the morning, to any-time-after-lunch. I don't think this
    worked out very well. Writing the post worked as a way to reflect on what I
    had done yesterday, and what I should be doing today. So, I am back to
    writing the blog post, first thing in the morning!
-   Yesterday, I worked on indexing the Python sources in a way that the
    inspection code can look up, later.  During this process, I found that my
    code to use libclang's AST wasn't generic enough, and I had to clean it up to
    be able to extract useful information from any file in the `cpython` sources.
-   We also got to attend a super-awesome talk by [Steve Labnik](http://words.steveklabnik.com/)! He talked about
    his progression from being an application developer, to writing libraries, to
    working on languages (as a professional developer). He made a lot of
    interesting and inspiring points during his talk.  Some of those that stuck
    with me are:

    -   None of these is particularly harder than any of the other. Depending on
        each person's personality, or the way their brain works, they are good at
        doing one or the other.
    -   Getting good at programming is a matter of showing up, more than about the
        "genes".  He repeated quite a few times that he disliked the idea of "baby
        hacker", and left out the story of his childhood and college programming
        days! I'm totally stealing his idea of meeting every saturday at 1pm, with
        a bunch of friends and working until it was 10pm or so, when they could get
        cheap beer and food!  And he did this all through his college!  It is
        interesting that this idea is so similar to Hacker School!

    It was a very enjoyable and inspiring talk on the whole.
-   The plan for today is to actually have the parsed information dumped into
    some persistent format, and modify the inspect code to actually use it.
-   I will also be pairing with Kyle for a few hours on working through some of
    <http://mitpress.mit.edu/books/audio-programming-book>

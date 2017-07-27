+++
title = "Recurse Center, 2014-07-22"
date = 2014-07-22T10:46:36-04:00
tags = ["learning", "python", "raspberry_pi"]
categories = ["recursecenter"]
draft = false
+++

## Mel's talks {#mel-s-talks}

-   Mel's talk in the morning was brilliant!  I wonder why it's not a part of
    recommended reading for Hacker Schoolers, or referred to, in the manual.
-   Logically, it makes sense that Mel came now, so that she didn't have to come
    twice to talk to the firsts and seconds, but it would have been great to have
    had this talk in the first week of Hacker School!
-   Mel gave us a lot of new information and insights into education and learning
    styles. I also like the fact that she gave us all a good vocabulary to think
    about and discuss stuff related to learning. I will try to think, and apply
    as much of this as I can, for the rest of my time here.
-   She talked about [test driven learning](http://blog.melchua.com/2014/02/10/test-driven-learning-setting-learning-goals-for-yourself-software-engineering-edition/) which seemed very interesting. Instead
    of just saying, "wow that would be an interesting thing to do", stop for a
    moment, think about what you are trying to learn, and how you will assess if
    you have learnt what you wanted to, and then dive into the project.
-   The [learning styles](http://www.engr.ncsu.edu/learningstyles/ilsweb.html) workshop was pretty good too, though I feel like I don't
    know myself well enough, and I unable to properly "bucket" myself.  Later, I
    took a [quiz](http://www.engr.ncsu.edu/learningstyles/ilsweb.html), and ended up fairly close to the middle, in all the dimensions.
-   Mel introduced us to the idea of [cognitive apprenticeship](http://www.scribd.com/doc/201816780/A-Cognitive-Apprenticeship-Primer), and encouraged us
    to try out the different modes when pairing. I really liked the idea of [Zone
    of proximal development](http://en.wikipedia.org/wiki/Zone_of_proximal_development) and I will try to take the advice of spending most of
    the rest of my time here in this zone.
-   Do I (really) care?  Motivation and mindset, ...
-   Be courageous!


## Airplay and Raspberry Pi {#airplay-and-raspberry-pi}

-   I was trying to wrap libshairport and use it on the RPi to be able to listen
    to songs being streamed on Airplay, and use that data to drive the LEDs.
-   Shairport, a tool written in C seemed to work.  My attempts to wrap
    `libshairport`, which is a fork of `shairport` converting it into a library,
    failed miserably.
-   The trouble was essentially getting Airplay to discover my service.  I tried
    a bunch of things with `pybonjour` and `avahi`, but wasn't able to get it
    right.
-   Finally, I tried just announcing the service with `shairport`, and actually
    running a python script that wraps `libshairport` to listen to the data.
    But, this didn't work and iTunes complained that this Airplay device is not
    compatible. Before going much further with this, I found `shairplay` which is
    a tool similar to `shairport`, but came with a library, and also Python
    bindings!  I happily used this to get stuff working!
-   I'm interested to see today, what exactly I was missing yesterday!


## Emacs club {#emacs-club}

-   I demoed org-mode to a bunch of people for about half an hour, and it was
    good to see people being blown away by what it can do, exactly the way I
    was, when I first came across it.


## Today {#today}

-   Work on RPi to clean up a few things for the party.
-   Compare `libshairplay` and `libshairport` to see what I was doing wrong,
    yesterday.
-   May be write up the whole thing, and make the code available.
-   Learn a little bit about Parsers from rntz.

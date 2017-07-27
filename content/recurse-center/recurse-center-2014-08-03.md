+++
title = "Recurse Center, 2014-08-03"
date = 2014-08-04T16:10:41-04:00
tags = ["C", "python", "raspberry_pi"]
categories = ["recursecenter"]
draft = false
+++

## Friday {#friday}

-   On Friday, I didn't do the exercises that everyone else doing job prep were
    doing.  I wanted to continue writing C code, and continued to work on the
    `bencode` parser in C.  I barely was able to finish adding support for lists.
-   I got comfortable using Valgrind, in the process of debugging a stupidity of
    not using `realloc` correctly.
-   What I was able to write with Python in an hour or so, I have been writing
    for about a day, in C, and haven't yet finished it!  It definitely doesn't
    help that my C is very rusty...


## Saturday & Sunday {#saturday-and-sunday}

-   I didn't work much, and went around New York with Madhu.  We went to quite
    a few places around here, the highlight being, the view of Manhattan's
    skyline from the Staten Island Ferry.
-   NYC's library also had an interesting exhibhition on the history of
    America, just before and during WW-I.
-   On Sunday, I tried out Mary TTS on the raspberry pi, and it is simply
    unusable.
-   I then, started writing a simple wrapper around Google's tts that is used
    by Google translate.
-   The TTS part is more or less working right now, the next step would be to
    deploy it on the RaspberryPi and start using it as a radio, to see what my
    needs are like. Hooking it up to [Jasper client](https://github.com/jasperproject/jasper-client) seems like a good idea,
    right now... though I'm not sure if it would work very well, with the pi's
    audio output drowning out the voice commands.

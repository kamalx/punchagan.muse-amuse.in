---
title : "Recurse Center, 2014-08-27"
date : 2014-08-28T09:51:30-04:00
tags : ["PIL", "python"]
categories : ["recursecenter"]
draft : false
---

-   I spent the whole of yesterday just working on the LED-bot.
-   Spent some time cleaning up meta-stuff about the project, making it a real
    package, adding a setup.py, added LICENSE & AUTHOR files, etc.
-   I found it really frustrating that there's no good/standard way to remove
    duplication of information between pip's `requirements.txt` and
    `install_requires`
-   We got the bot running on the Beagle Bone, but it turned out to be too slow.
    After some playing around with trying to get rid of Python for-loops, I was
    able to use PIL's `image.tobytes` and some image cropping to get the data to
    be sent to the LEDs, and it sped up the display quite a bit.

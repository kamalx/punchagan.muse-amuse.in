---
title : "Recurse Center, 2014-07-14"
date : 2014-07-15T18:25:15-04:00
tags : ["numpy", "python"]
categories : ["recursecenter"]
draft : false
---

-   Monday morning checkins for our group had only two people. That was strange!
    Very strange!


## Work on cinspect {#work-on-cinspect}

-   I wrote up a README since David (an alum at Hacker School) showed interest in
    the project.  But, he probably isn't that interested anymore since the code
    base is Python2.x only.
-   I got rid of assumptions that method names would start with the module name
    or the type name, and actually look up references to the names in the
    definitions of types or objects.
-   I also improved the test-suite to actually download sources of CPython and
    index them.  They take very very long!!
-   I tried to get it working with Numpy, but getting all the headers to include
    wasn't as easy as I assumed it would be!

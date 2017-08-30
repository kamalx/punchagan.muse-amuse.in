---
title : "Bookmarks [2013/12/05]"
date : "2013-12-05T00:00:00+05:30"
categories : ["bookmarks"]
draft : false
---

-   [Raspberry Pi Python Adventures: IEEE 754/854, when it is needed](http://raspberry-python.blogspot.in/2013/10/ieee-754854-when-it-is-needed.html)

    If you want IEEE 754/854 decimal behaviour, what you want to use is
    the decimal module

-   [Experiments in public: Rethinking my excuses about hiring for Test Automation](http://alecmunro.blogspot.in/2013/10/rethinking-my-excuses-about-hiring-for.html)

    Be an Automator, spend your days debugging everyone else's software,
    drive the art forward, and enjoy (in the long run) incredible job
    security!

-   [Ned Batchelder: Range overlap in two compares](http://nedbatchelder.com/blog/201310/range_overlap_in_two_compares.html)

    His code used eight comparisons to check whether the endpoint of one of the ranges was contained within the other range. In Python it would look like this:

    ```python
    def overlap(start1, end1, start2, end2):
        """Does the range (start1, end1) overlap with (start2, end2)?"""

        return (
            start1 <= start2 <= end1 or
            start1 <= end2 <= end1 or
            start2 <= start1 <= end2 or
            start2 <= end1 <= end2
        )

    ```

    I said you could do it in two comparisons rather than eight, but
    could never remember the trick.

-   [Cubr | Keep on Coding](http://cbarker.net/blog/projects/applications/cubr)

    Cubr is a project I completed in three weeks at the end of my
    introductory computer science class at CMU. The idea is simple: you
    mix up a Rubik’s cube. You show the cube to your computer’s
    webcam. Some magic happens, and your cube appears onscreen. Then,
    the cube begins to solve itself, and all you have to do is follow
    along and you will have solved your cube!

-   [Corey Goldberg: deadsnakes - Using Old Versions of Python on Ubuntu](http://coreygoldberg.blogspot.in/2013/10/deadsnakes-using-old-versions-of-python.html)

    The Python packages in the official Ubuntu archives generally don't
    go back all that far, but people might still need to develop and
    test against these old Python interpreters. Felix Krull maintains a
    PPA (package archive) of older Python versions that are easy to
    install on Ubuntu.

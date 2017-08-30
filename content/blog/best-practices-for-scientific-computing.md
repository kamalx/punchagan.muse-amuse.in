---
title : "Best Practices for Scientific Computing"
date : "2012-12-24T00:00:00+05:30"
tags : ["advice", "programming", "science", "software"]
draft : false
---

Shantanu and I gave a short talk titled "Software Carpentry for
Scientists" for the graduate students of Chemical Engineering
department, IISc, this Friday.  We gave a short introduction to
Git, TDD, Numpy/Scipy, etc and mentioned a few things from Greg
Wilson et al's paper.

I promised to revert to them with links to a few resources.  I
figured it would be more beneficial, if I just put it in a
publicly available place.

A summary of the paper by Greg Wilson et. al., is below.


## Useful resources {#useful-resources}


### Software Carpentry {#software-carpentry}

-   Paper by Greg Wilson et. al.
-   Software Carpentry


### Git & version control {#git-and-version-control}

-   <http://bit.ly/VfbOww>
-   <http://karlagius.com/2009/01/09/version-control-for-the-masses/>
-   <http://try.github.com>
-   <http://betterexplained.com/articles/a-visual-guide-to-version-control/>
-   <http://betterexplained.com/articles/intro-to-distributed-version-control-illustrated/>


### TDD {#tdd}

-   <http://software-carpentry.org/4_0/test/index.html>
-   <https://www.google.co.in/?q=TDD+matlab>


### SciPy {#scipy}

-   <http://scipy-lectures.github.com>


### Python {#python}

-   <http://docs.python.org/tutorial>


### GUI tools in Python {#gui-tools-in-python}

-   <http://code.enthought.com/projects/traits/docs/html/tutorials/traits_ui_scientific_app.html>
-   <http://docs.enthought.com/traits>
-   <http://docs.enthought.com/traitsui>
-   <http://docs.enthought.com/enaml>


## Summary of paper by Greg Wilson et. al. {#summary-of-paper-by-greg-wilson-et-dot-al-dot}

1.  Write programs for people, not computers
    -   a program should not require its readers to hold more than a
        handful of facts in memory at once.
    -   names should be consistent, distinctive and meaningful.
    -   code style and formatting should be consistent.
    -   all aspects of software development should be broken down
        into tasks roughly an hour long
2.  Automate repetitive tasks
    -   rely on the computer to repeat tasks
    -   save recent commands in a file for re-use
    -   use a build to automate scientific work-flows
3.  Use the computer to record history
    -   software tools should be used to track computational work
        automatically.
4.  Make incremental changes
    -   work in small steps with frequent feedback and course
        correction
5.  Use version control
    -   use a version control system
    -   everything that has been created manually should be put in
        version control
6.  Don't repeat yourself (or others)
    -   every piece of data must have a single authoritative
        representation in the system
    -   code should be modularized rather than copied and pasted
    -   re-use code instead of rewriting it
7.  Plan for mistakes
    -   add assertions to programs to check their operation
    -   use an off-the-shelf unit testing library
    -   use all available oracles when testing programs
    -   turn bugs into test cases
    -   use a symbolic debugger
8.  Optimize software only after it works correctly
    -   use a profiler to identify bottlenecks
    -   write code in the highest-level language possible
9.  Document design and purpose, not mechanics
    -   document interfaces and reasons, not implementations
    -   refactor code instead of explaining how it works
    -   embed the documentation for a piece of software in that software
10. Collaborate
    -   use pre-merge code reviews
    -   use pair programming when bringing someone new up to speed
        and when tackling particularly tricky problems
    -   use an issue tracking tool

+++
title = "I love FOSS.  How do I start contributing (code)?"
date = "2011-03-28T00:00:00+05:30"
tags = ["contribute", "foss", "howto", "newbie"]
draft = false
best = true
+++

## Why this article? {#why-this-article}

I teach (Science and Engineering) students and teachers to use Python for
their computational tasks.  I'm occasionally asked this question or something
similar.  I remember, it was not too long ago, that I asked this question
very often.  I asked anybody who was more experienced than me, "How do I
start contributing (code) to FOSS?" and all the answers I got, were very
similar.  Also, my answer is not going to be radically different.  But, I
would still like to answer this question, because -

1.  All the answers I got, were from big-time, experienced contributors.  I
    suspect, they only vaguely remember how it feels to be just starting off.
    But, I am just starting off and I think my answer brings a slightly
    different perspective that would help others[^fn:1].
2.  This piece of writing is meant to be one comprehensive compilation of
    things I want to share, if and when I'm asked this question in the
    future[^fn:2].
3.  More than anything else, a reminder and reference for myself.  I still
    have a long way to go.  I only have a handful of contributions against my
    name (none of them earth shattering).  I haven't (yet) done my 10,000
    hours of programming nor have I learned anything like half a dozen
    programming languages.[^fn:3]

Thanks to baali, Ringo and Voodoo for reading drafts of this article and
giving some very valuable feedback to improve it.


## What should I do? {#what-should-i-do}

I know how exciting the FOSS world seems, the first time we discover it.  You
are dying to contribute.  You want to contribute, Right Now!  But you've no
clue, what, where and how.  Relax.  Give yourself time.  You've a lifetime
ahead of you.  Explore.  Explore, even more.  Play with things, Try out
stuff, Break stuff, Spill things all over the place.  Have fun![^fn:4]

Given that you are reading this, I presume that, you do have access to the
Internet.  But, if you don't, it could turn an impediment to your goal.  Easy
access to a decent internet connection is a prerequisite.

Learn a programming language, well[^fn:3].  By learning, I don't mean
getting familiar with the syntax or passing a bunch of exams.  Get familiar
with the paradigms of the language.  Learn to think in that language.  Write
code that does something **real**, instead of doing toy examples.[^fn:5] Also,
it helps know bits and pieces about the history and evolution of the
language.  This will give you a sense of why some features are present (or
absent) and will help you program better, in that language[^fn:6].

Some projects will definitely catch your eye, while you are exploring.  Start
using the ones that you need.  Follow them!

Start with using the bleeding edge [^fn:7] software.  Bleeding edge refers
to the latest sources of the project, where the active development is going
on.  Given the continuous nature of software development, using the latest
source,

1.  prevents you from wasting time on fixing bugs that have already been fixed
    and
2.  lets you look at the latest changes being made and contribute effectively
    and easily

Also, start following the project's mailing lists -- both the dev and the
user lists, if they are separate.  The user-list discussions will help you
discover functionality and possibly give you some chance to peek at the
source code, too.  Don't be surprised or worried if you don't follow most of
what goes on, in the dev-list.  Be patient and keep at it.  You will learn a
lot about the _what, why and how_ of the project.  Also don't be afraid to
look foolish there!  There wouldn't be one developer who doesn't have some
embarrassing logs of stuff she said in public, in her initial days.

Slowly you'll start to learn the dynamics of the community -- how things
function, the DOs and DON'Ts, etc [^fn:8].  Also, there's a good chance
that the project has an active IRC channel.  If it does, hanging out there
will give you more insights.  Contributing to the documentation, is often a
useful step before contributing code.  Cleaning up the documentation or
writing documentation, often requires you to read the code and helps you
understand it better.

Next, start **acting** on Bug reports (or tiny feature requests).  Start with
trying to reproduce the bugs and sending confirmations.  Gradually, start
looking at the source and trying to figure out where the problem is.  Be
patient, with this [^fn:9] .  Once you get comfortable with the code
and the coding style, start sending code snippets and comments, explaining
what you think might be the problem.  One fine day, you will be able to send
a full working patch!  But, before that don't hesitate to send partial fixes.
You can learn a lot from the comments of the devs and looking at how they
finally fixed it.  Also, IRC could be a good place to ask for help, if you
are stuck and are looking for some quick help, so you can move further.

In all of this, it helps if you have one (or a bunch of) favorite _area(s)_
or _module(s)_ of the project, specially in a big project.  You should pounce
upon any issues in your favorite area.

Participate in sprints.  It's not uncommon for projects to have regular
sprints.  Make it there [^fn:10]!  Also, a couple of developers may decide
to meet up on a weekend and hack.  If it's happening in your neighborhood,
ask if you can join.  Don't be surprised, if they shout out a big YES!  You
will definitely learn a lot, when there is help so close-by.

A _shortcut_ would be to start your own project!  It is easier (in some ways)
to release your own code under a FOSS license, than contribute to some of the
existing projects.  You don't have to have your code approved by the project
leads, you don't need to mould your code to fit the standards of the project,
you don't have to read and understand all the (relevant parts of the)
existing code, etc.  But all of this, definitely teaches you a lot.

As a beginner, I think it is important to solve your **own** problems, problems
that you care about (at least at that point in time).  Most of the projects,
started off with their developers wanting to solve their own problems.  Only,
incidentally, they solved some of the World's problems, too!

Start small, though.  Don't start off with a project that aims to replace
Chrome or Firefox as the best browser, or an editor to replace Vim or Emacs.
Writing extensions to your favorite software could be a good place to start,
for instance an Emacs minor/major mode[^fn:11], a Chrome
extension[^fn:12], etc.  Stand on the shoulders of giants!

Also, take this as an opportunity to gain some of the skills that would be
useful, when you want to start contributing to others projects.

1.  Learn to use Version Control (Git + GitHub is awesome!)
2.  Learn to use build and setup tools.
3.  Learn about packaging and distributing your software.
4.  Learn how to license your code.
5.  Learn to Collaborate!

All of this, I hope, would suffice to get your first contribution in.  But,
there are a few things that will help you in the long run.

Good English. Specially written communication, since that is how you would be
communicating, more often than not.  Fair or not, hackers are known to be
very particular about good communication.  I'm not exaggerating when I say,
what you say may be ignored even if it makes perfect sense, if you said it in
sloppy English.

Using a \*nix would put you in some great company.  At the very least, you
save time when looking for solutions to known problems.  Using a good editor
and learning to type quickly can be big productivity gains.  You only get 24
hours a day!

An understanding of licensing issues, can come in handy, many a times.

For more, read How to Become a Hacker by Eric Raymond.

Happy Hacking!

[^fn:1]: I'm writing in the Indian context.
[^fn:2]: All of this is generic advice, but students applying to programs like
GSoC, may find it useful.
[^fn:3]: Teach Yourself Programming in Ten Years by Peter Norvig.
[^fn:4]: Getting yourself a GitHub account and _socializing_ there is a lot
of fun and helps quite a bit.  GitHub is my Facebook!
[^fn:5]: I started learning Python from _the Python tutorial_ and some other
sources and doing the examples in them.  It was good, but I think I started
learning more, and better, when I started solving problems from Project Euler.
And writing an IRC bot in Python, taught me a lot more than all of this.
[^fn:6]: I recommend Python, but I am definitely biased.  Any language that
is generic enough would do, really.

1.  It gets you off the blocks, very quickly.
2.  It is easy to learn.
3.  It is batteries included. Read as, comes bundled with a huge bunch of
    libraries.
4.  It is general purpose enough. Read as, it has libraries that let you do
    anything, you'd possibly want to do.
5.  There's a lot of Python code around, that you can read andlearn from.
[^fn:7]: You may have to learn to use a version control system; at the very
least cloning and pulling updates.
[^fn:8]: Org-mode is the only project that I really contribute to, actively.
I **really** liked the way the community gels together and the kind of people on
the list.  There are some really knowledgeable, friendly and helpful people.
It feels great to be a part of the community.
[^fn:9]: There have been instances, where it took me half a day to fix
something, that would've been fixed in about an hour by someone more
comfortable with the code.  But, I think everybody goes through this stage.
This is how you learn.
[^fn:10]: A few months ago, I was part of a sprint on the numpy-scipy
eco-system.  We had somewhere around 50 patches (a lot of them were
documentation fixes) submitted to all the projects!  Most of the people were
submitting their first patch and I think it was a great opportunity for them to
start.  [I should try and get back to them.]
[^fn:11]: Org-mode is really awesome, and I use it for everything I write.  Blog
posts are a big part of what I write, and so, I wanted to write them in
orgmode.  And so, org2blog was born.
[^fn:12]: I recently wrote a Chrome extension, thanks to a friend's idea.
Inspired by Gmail notifications, a GitHub addict wanted notifications for
activity in GitHub.

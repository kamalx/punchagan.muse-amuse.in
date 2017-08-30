---
title : "Not so Floppix..."
date : "2007-12-11T00:00:00+05:30"
tags : ["emacs", "lafootgiri", "ology"]
draft : false
---

**Disambiguation:** The original Linux on 2 Floppies is here.

I, post this from a remastered version of Knoppix that we named
Floppix!

It all actually began, with me deciding to do a bit of Emacs-ing
at home during the winter hols but I don't have a Linux box at
home. Live-CD is the way to go! But then Emacs doesn't \\\*usually\\\*
go with Live-CDs. So I decided to get around making my own. :)
[Dunnet "Dunnet Game"),
an Adventure game in Emacs, played a crucial role in motivating me
to go ahead!] The rest as they say is history....

Actually, I tried a debootstrap from my Debian etch but I couldn't
manage to get the initrd working. [[<http://avudem.blogspot.com>
"Voodoo"][I ain't this geekish, its only that I am incapable of
putting these terms in a simpler language.] After numerous futile
attempt, I gave up for the time being and that's when the genius
of [Voodoo]] came in, he took a different route. Remastering
Knoppix.[Modifying an existing Live-CD of Knoppix]

I won't get into the exact details of how we got about it. There's
a lot of online help available for that.

A few highlights, for the curious reader...

-   got rid of the default KDE and replaced it with
    Fluxbox. [actually Floppix = Fluxbox + Knoppix :P]
-   added emacs, cmucl, slime, octave, linuxdcpp, vlc and others.
-   got rid of other packages which we weren't going to use.
-   changed the boot message
-   changed the default background image.
-   removed the default boot image [ couldn't change it as the image
    we chose wasn't being properly converted to lss16 format ]
-   tested the CD with Qemu [size of the iso got more than 700MB]
-   removed a few other not so regularly used packages [including
    wine!]
-   burnt the CD
-   Logged in!

Now, that I've logged in, I realize we managed to quite a decent
job. Obviously we weren't perfect. It was the first time and done
in quite a hurry. [btw, we have our end-sems going on; I've no
exam tomorrow though] I was able to listen to music, connect to
the DC, play a game of dunnet and make a blogpost! We also missed
a few packages, for instance a screen shot capture program! But it
ain't too bad, still a long way to go though!

Just hoping we manage to make it better, as we get better at it!
;)

Here comes FloppixV0.1!

---

Update [3/1/08]: I never knew that GIMP could capture screenshots!
ImageMagick can do that too. I had two programs at hand and
thought I had none! Here's a Screenshot of the Floppix Desktop.

{{<figure src="../images/floppix_desktop.jpg">}}

Picture Source [for the Background Image] : 9

---

Update 2 [4/1/08]: There is already a floppy distro of Linux
called Floppix. I knew about this only when some one searching for
it reached my blog. Guess I should do something about this. [I'll
be able to do it only after getting back to campus,though]

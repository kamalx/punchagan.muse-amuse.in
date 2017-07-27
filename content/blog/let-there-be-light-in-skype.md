+++
title = "Let there be light, in skype!"
date = "2014-03-29T00:00:00+05:30"
tags = ["hack", "linux"]
draft = false
+++

At home, my video would always show a silhouette in G+ and Skype, and
I always thought that this was because the lighting at home was not
sufficient.  At office, the video was decent.  But, moving to sit
right under the light also didn't help much.

Struggling with a bunch of tools like `v4lctl`, `guvcview` didn't
help. But, during these struggles I noticed that `cheese` would show
me bright and cheerful, while all the other programs showed my
silhouette.

I set out to "fake" the output of `cheese` as a video device that
skype and other programs could use. But, I didn't have to go all the
way.  I ended up using [v4l2loopback](https://github.com/umlaeute/v4l2loopback/) to create a loopback video device,
and just using `gst-launch` to redirect video to that device, did the
trick!  Thanks gstreamer!  Thanks v4l2loopback! :)

Here's a convenient [script](https://gist.github.com/punchagan/9859210) to use it every time I need it.

<script src="https://gist.github.com/9859210.js"></script>

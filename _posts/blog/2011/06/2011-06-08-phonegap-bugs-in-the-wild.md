---
title: PhoneGap Android bugs in the wild
date: 2011-06-08 23:43:25 Z
categories:
- app
author: Joe Bowser
status: publish
type: post
format: html
---

Android was the first platform that we ported PhoneGap to after we wrote the initial iPhone implementation, and PhoneGap Android is just as old as the T-Mobile G1\.  One thing that makes Android a different platform to develop for compared to the other platforms is the fact that Android until recently was relatively Open Source.  This means that they maintain their own bug tracker on Google Code and we can check there and see what our users are reporting, and whether they're experiencing the same pains that we are.

With the most recent release of Honeycomb, there is this notoriously bad issue with the Android browser that we currently work around by disabling 3D Acceleration.  It appears that we're not the only people that noticed this, and that people have been filing issues with the Android project.  However, the issue with the tickets is that it's easy for there to be duplicates.  It'd be great if we could get more attention to this issue so that it could get resolved, so if people could be sure to favourite both of these issues, that would be awesome.

* [http://code.google.com/p/android/issues/detail?id=17458](http://code.google.com/p/android/issues/detail?id=17458)
* [http://code.google.com/p/android/issues/detail?id=17352](http://code.google.com/p/android/issues/detail?id=17352)

Hopefully with the additional attention, we can get this issue fixed for Honeycomb and not have to live with it when 3D CSS Animations and the other changes come into later versions of Android.  Also, if you find issues with Android PhoneGap, and they turn out to be something in the Android OS, please search for the bug in the project, file it if it doesn't exist and let us know.  If we know about it, and we can reproduce it on our end, we'll spend time promoting it, and maybe even trying to fix it or working around it like we did with the addJavascriptInterface issue.  Finding these issues and making sure that Open Source projects like the Android project know about them is one way that we can make the mobile web better for everyone.

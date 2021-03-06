---
title: 'EDGE UPDATE: Android 1.x Database Storage'
date: 2009-12-09 00:15:00 Z
categories:
- app
author: Joe Bowser
link: http://blogs.nitobi.com/joe/2009/12/08/edge-update-android-1-x-database-storage/
status: publish
type: post
format: html
---

I just finished the basic version of Android 1.6 Database Storage for PhoneGap. Unlike Android 2.0, which has a proper implementation of this, Android 1.6 does not. There are definitely numerous bugs that can happen with this implementation of Database Storage, such as mis-formatted numbers being passed into Javascript due to what SQLite sends back to the browser, however I've tried to mimic the HTML 5 spec the best I could with Java and JavaScript.

Now, the code being passed is VERY primitive, and it's not well documented. Android is notorious for having this weird API in the providers that gets in the way of you and your SQLite Database. Providing a mapping from Javascript to the rawQuery seems to have made the most sense. We have yet to add a fail condition to this yet, so when it fails, it will fail silently. That's somewhat annoying when it comes to errors in SQL syntax, and we'll try to hammer out that bug later this week.

[› Visit the original post](http://blogs.nitobi.com/joe/2009/12/08/edge-update-android-1-x-database-storage/)

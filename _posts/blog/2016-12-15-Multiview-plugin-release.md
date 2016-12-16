---
author: Sterling Gerritz
title: Release of PhoneGap Multiview Plugin!
date: 2016-12-14
tags:
- Announcement
- Android
- iOS
- Plugin
- Release
- PhoneGap Blog
---

We're happy to announce the release of the new PhoneGap MultiView plugin with support for iOS and Android!

The MultiView plugin empowers developers with the ability to launch multiple Cordova Webviews within
one PhoneGap application! Each webview is fully independent, is able to communicate with local storage, and has its own set of plugins.

Please check out a demo video which illustrates the passing of data between webviews:

[Youtube - Demo (Android) Project](https://youtu.be/_ZzBA28QO4s)

[Youtube - Demo (iOS) Project](https://youtu.be/WVbxFIGBh0Y)

Source code to our Demo Project is included in the repo, to run it in iOS/Android:

```bash
$ cd demo
$ cordova platform add ios (or) cordova platform add android
$ cordova plugin add --link .. (Android does not link)
$ cordova run ios (or) cordova run android
```
## Installation Instructions
After you have built your project, install the plugin in your current working directory of your project location:
```bash
$ phonegap plugin add phonegap-plugin-multiview (or) cordova plugin add phonegap-plugin-multiview

## Quickstart Guide to Using the MultiView Plugin

The plugin and documentation are available for download [here in the PhoneGap Repo](https://github.com/phonegap/phonegap-plugin-multiview).

To utilize both views you must create *two* separate JavaScript files which correspond repectively to the native portion of the plugin (PGMultiview.java and PGMultiviewActivity.java).

To *launch* a new webview make this call in your application's JavaScript:

```bash
$ PGMultiView.loadView(url, strPayload, success, error);
```

To *dismiss* a webview make this call in your application's JS:

```bash
$ PGMultiView.dismissView(data);
```

## Stay Tuned!

This is the first version of the API.  We currently only support two views in a stack but are continually adding functionality and in process of providing support for multiple views.

## Issues

- Currently data is stored to memory (not disc).  Under most operating conditions this should not be an issue. However, in an extreme low memory state you do risk losing data between views if either PGMultiView.java or or PGMultiViewActivity crash before reaching onStop() in the activity lifecycle.

- This bug should be resolved in the near future, the next release of this plugin bindsEvents() and writes the saved view state to local storage so that it can be retrieved at OnPause() in the Cordova Activities' lifecycle.

## Contact Us

Your feedback is graciously accepted and appreciated!

[Please submit your pull requests and issues here](https://github.com/phonegap/phonegap-plugin-multiview/).
---
author: Franziskus Domig
categories:
- Programming
date: 2011-09-16T10:42:32+00:00
flattrss_autosubmited:
- "true"
tags:
- Android
- Java
title: Start an Android Intent without pushing on the history stack
type: post
url: /2011/09/16/start-an-android-intent-without-pushing-on-the-history-stack/
---

I was wondering how to create an Intent with the Android SDK which will not be pushed on top of the history stack. Which means, if another Intent will be started, the back button pressed event will not move back to the specific Intent. Actually this is done pretty easy with setting a [FLAG\_ACTIVITY\_NO_HISTORY][1]. An example the is given with the following code snipped.
  
<!--more-->

<div class="oembed-gist">
  <noscript>
    View the code on <a href="https://gist.github.com/fdomig/5531562">Gist</a>.
  </noscript>
</div>

 [1]: http://developer.android.com/reference/android/content/Intent.html#FLAG_ACTIVITY_NO_HISTORY "Intent Description in the Android Developer Documentation"

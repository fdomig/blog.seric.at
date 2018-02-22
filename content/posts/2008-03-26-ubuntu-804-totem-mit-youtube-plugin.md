---
author: Franziskus Domig
categories:
- Linux
date: 2008-03-26T06:31:11+00:00
tags:
- Beta
- Hardy
- Totem
- Ubuntu
- Youtube
title: 'Ubuntu 8.04: Totem mit Youtube Plugin'
type: post
url: /2008/03/26/ubuntu-804-totem-mit-youtube-plugin/
---

<img class="alignleft size-thumbnail wp-image-42" title="Totem Youtube" src="/uploads/2008/03/totem_plugins_youtube.png" alt="Totem Youtube" width="392" height="221" />[Ubuntu 8.04 Hardy Heron][1] kommt mit einem frischen Totem Videoplayer mit [Youtube][2] Plugin welches allerdings in der aktuellen Hardy Beta noch etwas angeschubst werden muss. Das Plugin lässt sich bei einigen Installationen nicht so einfach aktivieren und bricht mit der (nicht sehr aussagekräftigen) Fehlermeldung: **Plugin Fehler &#8220;Plugin »YouTube-Browser« konnte nicht aktiviert werden&#8221;** ab.
  
Abhilfe schafft die Installation des Pakets **python-gdata** welches für das Plugin benötigt wird, dieses kann man mittels: **`sudo apt-get install python-gdata`** aus den Paketquellen installieren.

So sollte man nun zumindest Youtube Videos suchen können, kann man diese noch nicht abspielen, fehlt sehr wahrscheindlich noch Gnash und/oder GStreamer &#8220;bad&#8221;-Plugins welche man mit: **`sudo apt-get install gnash gstreamer0.10-plugins-bad`** installieren kann.

[<img class="aligncenter size-medium attachment wp-att-46" title="Youtube Totem" src="/uploads/2008/03/totem_youtube_2.png" alt="" width="500" />][3]

Nun sollte man einen funktionierenden Totem Videoplayer mit Youtube haben.

 [1]: http://www.ubuntu.com/testing/hardy/beta "Ubuntu 8.04 Hardy Beta Release"
 [2]: http://www.youtube.com
 [3]: /uploads/2008/03/totem_youtube_2.png

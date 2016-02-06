---
title:  "Remote Control App"
subtitle: "Using the lockscreen to control a receiver"
author: ""
avatar: "img/authors/me.png"
image: "img/remote.JPG"
date:   2016-02-02 12:12:12
---

Ever felt that your remote control is clumsy? Why not create a remote control that shows exactly the buttons you need, when you need them.

##Remotes are inefficient

I am not a fan of remote controls. They have way to many buttons that I never use and always get lost.
That's why I created a way for me to control my receiver via an app.

##Hardware

Sadly my receiver does not have a way to connect it to my LAN. So I had to find another way to send commands to it. I used a raspberry pi with an infrared led. On it runs a java server that receives commands via the network.

Remote controls flash the ir-led in patterns to send commands. Because I was not able to find the commands for my receiver online I had to read them. I used an LED-Transistor that I connected to the Raspberry and two batteries. Then I read the values with the [LIRC library](http://www.lirc.org/html/index.html).

![Reading IR Values]({{ site.github..url }}/img/reading.jpg){: style="width:100%"}

##App

The app replaces the default lockscreen. If the phone is connected to my wifi it enables the command buttons. The volume is turned up and down via swipe commands around the clock.

![Lockscreen]({{ site.github.url }}/img/lockscreen.png){: style="width:50%; margin-left:auto; margin-right:auto; display:block"}

If you are interessted in the source code, send me a pm over at github.

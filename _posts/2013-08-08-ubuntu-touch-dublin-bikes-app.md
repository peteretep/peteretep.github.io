---
layout: post
title: Ubuntu Touch Dublin Bikes App
category: Technology
excerpt: A while ago I started working on an Ubuntu Touch app for the DublinBikes bicycle sharing scheme. I'm a big fan of the bike sharing scheme and use them whenever I am out and about in the centre of Dublin.
---
A while ago I started working on an Ubuntu Touch app for the [DublinBikes](http://DublinBikes.ie) bicycle sharing scheme. I'm a big fan of the bike sharing scheme and use them whenever I am out and about in the centre of Dublin.

I use a Dublin Bikes app on my android phone, so I decided to try and write one for the Ubuntu Touch platform. I've been following Ubuntu Touch developments and like what I see so far.

The development has been made much easier because all the data is available. A project called [CityBik.es](http://citybik.es) provide a public API with data about bike sharing schemes worldwide.

This is the first time I've used QML and I haven't had a chance to do anything with this since my operation, so the code is not pretty. It's basically an evenings worth of playing around. So far, I'm just retrieving the list of bike stations and displaying them in a ListView, along with the number of free bikes and stands.

I'm following this tutorial on [Building an Ubuntu SDK app](http://mhall119.com/2013/04/building-an-ubuntu-sdk-app-rev-1/).

I'd like to have the list automatically sort by nearest station, and then of course add in a map.

Hopefully I'll get back to playing with this when things quiet down a bit.

https://github.com/peteretep/ubuntu-dublinbikes


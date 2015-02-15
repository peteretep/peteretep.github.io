---
layout: post
title: A Visit To The Clouds
category: Technology
excerpt: We have recently come up against some infrastructure capcacity issues at my workplace. After some investigation, we realised that our servers are not running as efficiently as they could be. We needed to update the OS on the servers, and this meant a visit to the data centre.
---

We have recently come up against some infrastructure capcacity issues at my workplace. After some investigation, we realised that our servers are not running as efficiently as they could be. We are running an older operating system (Centos 5). Although the servers all contain 64bit hardware, the 32bit version of Centos was running on them. This meant or applications couldn't use the full power and RAM available on the servers.

<div class="row">
  <div class="col-md-6">
    <div class="thumbnail">
      <img src="http://www.visualid.com/wp-content/uploads/2013/10/serverss.jpg" alt="...">
      <div class="caption">
        <em>Me with the rest of the Muppets - Animal, Fozzy and Gonzo</em>
      </div>
    </div>
  </div>
  <div class="col-md-6">
    <div class="thumbnail">
      <img src="http://www.visualid.com/wp-content/uploads/2013/10/neighbourservers.jpg" alt="...">
      <div class="caption">
        <em>We call our servers after characters in the Muppets Show and it was nice to see we aren’t the only ones to do something like this – our neighbouring servers are called Shaggy and Scooby!</em>
      </div>
    </div>
  </div>
</div>

When looking at these issues, I knew things weren't right. The plan was to “virtualise” our servers using [Xen](http://xenproject.org "Xen Project") and manage them using [Cloudmin](http://www.webmin.com/cloudmin.html "Cloudmin"). This would mean that we can use the hardware to it’s full capacity and easily expand as necessary in the future.
The first step was to install an up to date operating system on one of the servers. We usually access our servers remotely, but a reinstall meant actually accessing the server itself. I put in some overtime and headed out to the data centre. It was around 9pm and the place was deserted, only one guy there keeping the internet running all night. It was my first time to visit the data centre and it was great to finally meet our servers in person.

I managed to update the OS and after verifying that I could remotely access “Gonzo”, I logged out and hit the road. As I left, I was warned to “mind the rabbits”. I had no idea what he meant until a colony of rabbits ran out in front of the car!

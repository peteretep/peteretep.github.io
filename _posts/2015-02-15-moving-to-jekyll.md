---
layout: post
title: Moving from Wordpress to Jekyll
category: technology
excerpt: I haven't blogged on here for a while - I haven't been able to think of anything to write about. To kickstart things again, I'm moving this blog from Wordpress to Github pages and Jekyll.
---

I haven't blogged on my personal blog in a long time.
I have been doing some writing for the [OnePageCRM Developer Blog][1], but haven't been able to think of anything to write about here.

We host the site on [Github Pages][3], which I think is pretty appropriate for a developer blog!
I really like this workflow, each blog is basically a git repository. I can write posts with my usual text editor and use my usual development tools. When you commit html files to the master branch of the repository, they are automatically hosted at a personal url.
You can make the workflow even more powerful by using [Jekyll][2], a static site generator built in ruby. It basically gives you a powerful templating system, translating markdown files to static html files. Each blog post is a file named with a particular convention.

I decided to move my personal site from Wordpress to Jekyll and change the design a bit using [Bootstrap][3]. I like using Bootstrap - some people call it lazy, but I don't care. I can quickly add nice stlyes and icons simply by adding a few CDN's. I know I'm adding CSS bloat, but who cares, it's a simple static site, that nobody reads anyway!

I exported my Wordpress site, but some images and layouts have become a bit messed up. I'll clean them up eventually.

I'm planning to blog a bit more - and also cross post some of my posts from my posts on the OnePageCRM blog. I'll also plan to play around with the styling of the site a bit more.

  [1]: http://developer.onepagecrm.com/blog
  [2]: http://jekyll.rb
  [3]: http://getbootstrap.com
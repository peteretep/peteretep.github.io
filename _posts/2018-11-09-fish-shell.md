---
published: true
layout: post
slug: "fish-shell"
category: software
author: peter
---

I first wrote about [Fish Shell](https://fishshell.com/) a couple of years ago when I was writing for the [OnePageCRM Developer Blog](https://developer.onepagecrm.com/blog/2014/08/11/fish-shell/).

Fish Shell is a replacement for the standard linux bash shell and I really like it.

Each time I setup a new laptop or reinstall my operating system, I find myself going back my original blog bost to remember how to do it.

This time, I've decided to update my instructions and write a new post.

So, here's how I installed Fish Shell on my new install of Ubuntu 18.10:

```
sudo apt install fish
```

Next I want to set it as the default shell:

```
chsh -s /usr/bin/fish
```
Then logout and log back in.

## Plugins
The plugins scene for fish shell seems to have changed a bit since my original post.
There seems to be a few competing package managers, but I'm going to stick with [Oh-My-Fish](https://github.com/oh-my-fish/oh-my-fish) as it has the most stars on Github.

Install the default setup with:

```
sudo apt install curl # Why no curl installed!?
curl -L https://get.oh-my.fish | fish
```

The minimal install pretty much gives me what I want - colours, git information, neatened file paths, and I can then install any other packages I might like.



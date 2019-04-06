---
published: true
layout: post
slug: "django-development-environment"
category: software
author: peter
---

I'll shortly be starting a new job, and it's back to the web development world for me.
The last time I was actively working as a web developer, it was mainly in a Ruby on Rails environment. I love Rails and it's convention over configuration approach. I'm more than happy to go with the design choices made by people much more experienced than I am! My new job seems to be mostly in the Django world. Django is the Python equivalent of Rails - a full web framework "with batteries included".

I like this approach as the work I mostly interested in at the moment doesn't need javascript based single page application kind of things.
Python has always been on the edges of my programming work - I haven't done a huge amount of core work in Python, but I've spent plenty of time working through tutorials and  using and editing other people's Python work.
I'm really happy to be moving over to Python - it's extensive use in the engineering and data science world makes me feel like it is a solid career move. I'll miss the "poetry" of Ruby, but Python is pretty too!

Over the last few years I have helped a few people set up Python environments - mostly for data science sort of reasons. It always seems to be a hurdle - different versions of Python and various libraries. There are great tools available to get through it clearly, but inevitably I forget the best practices each time I set up a new machine.

This post is to document for myself how I setup my development environment, so I can easily replicate it again.

In general, I use Ubuntu - usually the most recent version, or sometimes the latest LTS.

I have been using Fish Shell for a few years. Usually the advantages of it outweigh any difficulties of replacing bash for me, but sometimes I find it adds an extra layer of confusion if I am not fully confident of my setup. I'll be setting up bash for Python development as well as Fish, so can fall back if I get confused.

For text editing I used to use Sublime Text, but recently started using VisualStudio Code. I think I'll go hole hog on the move to VS Code and include whatever plugins I install here too. On the other hand there's noting wrong with Sublime, so maybe I'll also set that up.

This post will be something I update and tweak over time.

# Usual things needed to add to a fresh Ubuntu install
```
sudo apt install git
sudo apt install vim
sudo apt install curl
```

## Fish
Install fish:
```
sudo apt install fish
```
Make it default if you like, with:
```
chsh -s /usr/bin/fish
```
Install OMF:
```
curl -L https://get.oh-my.fish | fish
```

# Installing Python and Virtual Environments
Ubuntu 18.04 comes with Python3 installed as default, at `python3`.

## Bash

```
sudo pip3 install virtualenvwrapper

```
Edit your `.bashrc` file:
```
vim ~/.bashrc

# Add the lines:
export WORKON_HOME=$HOME/.virtualenvs
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
export VIRTUALENVWRAPPER_VIRTUALENV_ARGS=' -p /usr/bin/python3 '
export PROJECT_HOME=$HOME/Devel
source /usr/local/bin/virtualenvwrapper.sh
```
Apply the updated `bashrc` file:
```
source ~/.bashrc
```

Now virtualenvwrapper is installed and can be used like this:

```
mkvirtualenv name_for_environment

deactivate — Exit out of the current Python virtual environment
workon — List available virtual environments
workon name_of_environment — Activate the specified Python virtual environment
rmvirtualenv name_of_environment — Remove the specified environment.

```

## Fish
Virtualenvwrapper doesn't work with Fish shell, but there is a similar project, [VirtualFish](https://virtualfish.readthedocs.io/en/latest/).

Install VirtualFish:
```
pip3 install virtualfish
```

Add the following lines to your `~/.config/fish/config.fish`. The first line sets python3 as the default python to make new virtual environments with virtualfish.

```
set -Ux VIRTUALFISH_DEFAULT_PYTHON python3
eval (python -m virtualfish compat_aliases auto_activation)
```


Create a new environment with:

```
vf new name_of_env
vf workon name_of_env
```

# Starting a new Django project
First, make a new virtual environment for the project.
```
vf new djangos_band_aye
```
The new virtual environment should be activated, but if not just run `vf activate djangos_band_aye`.

Install Django in the new virtual environment:
```
pip install Django
```
Start a new Django project:

```
django-admin startproject djangos_band_aye
cd djangos_band_aye
```
Now connect the virtual environment to the project folder, so you don't have to remember to activate it next time:

```
vf connect
```




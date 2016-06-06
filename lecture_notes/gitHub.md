---
title:  Intro to GitHub
layout: notes
---

## Introduction
Throughout this course, we will be using [GitHub](http://github.com/) to manage our projects.  [GitHub](http://github.com/) allows us to have a centralized location to store and manage the projects that we will create in this class.  It also allows you to manage your own individual copy of that project, modify it as needed, and build a history of those modifications. When you are done with your work, you'll submit your project and get feedback using a *pull request*.  Understanding how to work with Git (the underlying version control system behind [GitHub](http://github.com/)) and [GitHub](http://github.com/) are very important first steps in this course.

## Get a GitHub Account
Get yourself setup with a GitHub account.  I recommend that you add your name to the account so that others can search for and find your account and repositories. The free account is fine, though if you checkout the [GitHub Student Pack](https://education.github.com/pack) you can get a micro account for free while you are a student. (To get the student stuff you'll need GitHub to know your student email. You can add more than one email to your account under Settings.)

<iframe width="560" height="315" src="https://www.youtube.com/embed/ezxRcdJ8glM?list=PLg7s6cbtAD17rhrz2BJWAPJMjR71B3IDx" frameborder="0" allowfullscreen></iframe>

Once you are registered, make sure to get me your GitHub user name so I can add you to our GitHub organization.  This will get you access to any non-public material I post for the duration of the course.

## What is GitHub and why do we use it?

<iframe src="https://player.vimeo.com/video/89542305" width="560" height="315" frameborder="0" allowfullscreen></iframe>


## Workflow
Most assignments will begin with a starter repository that you will *fork*.  This gives you a general layout for the project and any starter code that you should have to begin.  You'll then *clone* the repository to your computer, make changes and *commit* them to your local repository.  It's a good habit to commit code locally often.  This allows you to make specific notes on what you've done in the commit messages, and gives you a point to go back to if you want to undo something.  When you're done with a chunk of work, or just need to save it *in the cloud* to go home for the night, you *push* your changes up to GitHub.  To get those changes on another computer, you *fetch* or *pull* them.  When you are done with the assingment and are ready to submit it for grading, you make a *pull request*.  This allows me to get you awesome in-code feedback as I  grade.  

We will walk through this process in more detail in the Student Directory assignment. But before we can do that, we need to install and configure GitHub and/or git.


## Installing Git at Home
In the classroom, git will be installed for you, but you will also want to have this installed on the computer you will be working on at home.  Git is fairly easy to install;  follow the instructions below for your operating system.


### Install on Windows
On Windows, the simplest option is to install [GitHub for Windows](http://windows.github.com).  This includes a command line version of Git as well as the GitHub GUI. We will be working with git from the command line, so you'll want convenient access to the *Git Shell*.  You may want to add this as a shortcut on your desktop or pin it to the start menu or taskbar.

We will focus on using git from the command line, as this is a more portable and marketable skill. The GitHub UI is nice, but on the job, it is unlikely your repository will be on GitHub, so you don't want to become dependent on this interface.


### Install on Mac
If you are using a Mac, open up a [Terminal]({{ "/documents/mac-terminal.html" | prepend:site.baseurl }}) window and type git.  You may find that it is already installed, or if not that it will prompt you to install the XCode Command Line Developer Tools.  If it does not, you likely have an older version of the Mac OS and should download and install the tools from the [Apple Developer Site](https://developer.apple.com/downloads/index.action).  You can also install the full XCode suite from the Apple App Store, but this will take additional space.  

GitHub Desktop is not required, we only need the underlying git command, and actually I encourage you not to use the application itself, but there is also now a [GitHub Desktop for Mac](https://desktop.github.com/) 


### Install on Linux
If you are on a Linux system, I'm going to assume that you know how to use your package manager - on a Debian system this would be apt-get.  Using the package manager for your system, install git.
{% highlight bash %}
$ sudo apt-get install git
{% endhighlight %}


## Configure Git
Before you dive in, you'll want to configure git with your user information. In the commands below, fill in your name and the email you used with your GitHub account.  This email is what will tie your activity to your account.  **Make sure that you are using the same email and check for typos.**
{% highlight bash %}
$ git config --global user.name "User Name"
$ git config --global user.email "user@email"
{% endhighlight %}


## Using a portable Drive
Since our classroom computers are wiped on reboot, it's a good idea to work off a portable drive while in class. If you choose to do this, you can configure git locally for each repository, then that configuration can be carried over into the classroom.  You can't do this now, since you don't have a repository yet, but keep this in mind for later.
{% highlight bash %}
$ git config --local user.name "User Name"
$ git config --local user.email "user@email"
{% endhighlight %}

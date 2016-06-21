---
title:  More GitHub
layout: notes
---

## GitHub
Throughout this course, we will be using [GitHub](http://github.com/) to manage our projects.  [GitHub](http://github.com/) allows us to have a centralized location to store and manage the projects that we will create in this class. Understanding how to work with Git (the underlying version control system behind [GitHub](http://github.com/)) and [GitHub](http://github.com/) are very important topics in this course.

## GitHub Workflow
As part of the Student Directory assignment, you learned the basic workflow process that we will use for nearly all the assignments in this course.  It is very important that you understand and follow this process to get your assignments and have them graded correctly.

Submitting your pull request signals that the assignment is ready to be graded, so it is important that you complete this final step.  If there is no pull request submitted, the assignment will not be graded and you will not receive any credit for your work.

## Pull-request feedback
When your work is graded, all of the comments are added to the pull request in GitHub. This allows the comments to be tied directly to the lines of code that you have written.  You should be notified of the comments by email, depending on your GitHub settings, but it is generally more meaningful to look at those comments on the pull-request in GitHub as that gives you the context in which the comment was made.

The video below walks you through how to find and view this feedback.

<iframe width="420" height="315" src="https://www.youtube.com/embed/diyiRMGUsaQ" frameborder="0" allowfullscreen></iframe>


## Creating a new repository
Most assignments for this class will begin with a starter repository that you will *fork* from our course GitHub page.  This gives you a general layout for the project and any starter code that you should have to begin.  You'll then *clone* the repository to your computer.   

But what do you do if you don't have a repository to fork and clone?  You can create a new repository on the GitHub website and either add starter files to it on the web so that you can clone it to your computer OR you can start with code in a directory on your computer and turn that directory into a git repository that you link to GitHub.  This is the process that I usually follow, as I typically start the project before I think about making a spot for it on GitHub.

The process for creating a new GitHub repository is the same.  On the GitHub website, you go to your profile, then your list of repositories, then click the green "New" button.

  <img src="{{ "/assets/images/shell-github-cmds/github-new-repo.png" | prepend: site.baseurl }}" alt="Screen capture showing new button." />

On the next page, you need to name the repository, decide if it will be public or private, and whether or not you will initialize it on GitHub then clone or do that on your computer. If you already have files on your computer, it is easiest to leave the "initialize" box unchecked, and generally I just always take this approach anyway.

  <img src="{{ "/assets/images/shell-github-cmds/github-new-repo-init.png" | prepend: site.baseurl }}" alt="Screen capture showing create repository page." />

Click the green "Create Repository" button.

If you chose to initialize on GitHub, you can now clone the repository and follow the same steps you would normally to add files, commit and push them to GitHub.

If you did not check the box to initialize on GitHub, the next screen gives you the commands to initialize the repository on your computer.  

  <img src="{{ "/assets/images/shell-github-cmds/github-new-repo-cmds.png" | prepend: site.baseurl }}" alt="Screen capture showing commands to initialize locally." />

Go to the GitShell (or terminal) and go into the directory that contains your files.  

If you already have a readme file, you can skip the echo command and begin with `git init`.  The `git init` command is used to initialize a new git repository.  

Once you have initialized the repository all of the other git commands that you have learned such as `git status`, `git add`, `git commit`, etc. will work in this directory.  However before you can push, you need to tell it where to push to.  That is what the `git remote add origin` command does.  Just copy that one from GitHub.

---
title: "Creating Your Development Environment"
teaching: 30
exercises: 0
questions:
- How does a contributing co-author set up their development environment?
objectives:  
- Creating a GitHub Account.
- Installing GitHub Desktop on your local computer.
- Cloning the project repository.
- Installing Ruby/Jekyll software.
- Editing and creating files locally.
- Pulling and pushing files from/to the main GitHub repository.
keypoints:
- Developing and editing files, when rendered locally, ensure error free files populate the main repository.
---

## Introduction

Creating a development environment on your local computer ensures source code is error free in advance of pushing to the GitHub repository.

With the approriate credentials, the GitHub site for this project can be used to create and edit files, with no other requirements for the developer.  
This technique works, but new renders are often delayed by a minute or two, and can be cumbersome to manage. 
Instead, building a local editing environment is preferred.

Here we provide guidance on creating your development environment.

## Local Setup

MacOS is not FreeBSD, but is related. Built in terminal emulation provides a mechanism for command line instructions. 
Bash can be used as the shell.
Windows users often use Putty as the interface.
WYSIWYG systems such as Finder can be used for file managment.

First up, creating a GitHub working directory in your home directory where your GitHub repository can be cloned, for example: 
~~~
$ mkdir Work/
$ pwd
/Users/demuth/Work
~~~
{: .language-bash}

- (Follow this link to Install GitHub Desktop)[https://github.com/apps/desktop]
- (Follow this link to inspect the GitHub site for this project)[https://github.com/demuth/cyberphysics] and select the green Code button and snag (copy to your buffer) from the URL https://github.com/DUNE/computing-basics.git which will be used to clone locally the repo using GitHub Desktop.
- Launch GitHub Desktop, select File and Clone Repository... from the menu bar.
  - in the Clone a Repository popup window, select the URL tab, and paste from your buffer https://github.com/DUNE/computing-basics.git
  - select a Local Path, for example, type /Users/demuth/Work or use the Choose button in the GitHub Desktop interface.
  - select the blue Clone button to initiate the cloning.
- Return to your terminal window and inspect the directory that is created. You might also open a Finder window to inspect the new files.
- Primary to contributing authors are the two subdirectories, `_episodes`, possibly `_extras', and `figs`.
- While commandline git commands are possible for your local repository, GitHub Desktop frees you from the burdens of learning new commands.




{% include links.md %}

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

Installing GitHub Desktop follows.

{% include links.md %}

---
title: "Build from Styles Notes"
teaching: 0
exercises: 0
questions:
- What is a Software Carpentry lesson template?
- Which lesson template should we use for source?
- How to import lesson template as a GitHub repo?
objectives:  
- Identify Software Carpentry lesson template source.
- Build DUNE repo and corresponding .io site.
keypoints:
- Build from styles template is straightforward but requires a few steps for GitHub Pages to render correctly.
---

## Introduction

In this lesson we will build a github.io site for the upcoming training of the DUNE Computing HWDB which has learning materials presented using the Software Carpentry (SC) templates. 

Identify SC lesson template source:
Work from the latest version of the lesson template, to verify versioning, visit [https://github.com/swcarpentry](https://github.com/swcarpentry),  and check out the meta-repository to help navigate the lessons and repos of the SC Community: [https://github.com/swcarpentry/swcarpentry](https://github.com/swcarpentry/swcarpentry).
>## Build Note
>Observing file dates at  https://github.com/carpentries/styles indicates no commits to the styles repo have been made in the last 2 years, with latest release: styles v9.5.3 Latest on Aug 21, 2018. All styles development work has shifted to their Workbench project, still in a beta stage.
{: .callout}
### Steps in a Nutshell
* Copy styles .git URL to buffer
* Create DUNE GitHub instance 
* Import styles (not fork, not clone)
* GitHub settings, set default branch to gh-pages, then delete the main branch.
* Locally, clone your github instance using GitHub Desktop
* In a terminal window whle in top level of your repo, and using $python bin/lesson_initialize.py
* Run $make serve to enable Jekyll/Ruby/Bundler based editing for localhost viewing
* Make edits, when ready push updates to the master repo on Github
### User Setup Expectations
* Versed at building GitHub repo.
* Capable of using GitHub Desktop.
* Has an editing environment such as emacs configured on their development computer.
* Has installed Ruby/Jekyll development framework for localhost editing.
* Markdown as a program language is understood.
### Step by Step Instructions

Start by going to the Software Carpentries site at https://github.com/carpentries/styles 

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image6.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image6.png" alt="Image 6" />
</a>

and snag the URL by select the green <> Code button:

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image9.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image9.png" alt="Image 9" />
</a>

and select the HTTPS link and copy it to your buffer (command C on Mac), that is https://github.com/carpentries/styles.git

Next, go to https://github.com/DUNE/ 

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image2.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image2.png" alt="Image 2" />
</a>

follow the green New Repository tab in the top menu and select the green New repository link (https://github.com/organizations/DUNE/repositories/new)

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image7.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image7.png" alt="Image 7" width="200px" height="auto" />
</a>

except follow the Import a repository text link (https://github.com/new/import) 

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image12.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image12.png" alt="Image 12" width="745" height="183" />
</a>

to set up a new DUNE repository, here named computing-HWDB:

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image8.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image8.png" alt="Image 8" />
</a>

As Your old repository's clone URL use https://github.com/carpentries/styles.git and Your new repository details DUNE/computing-HWDB ensuring that Repository name is available. Set access to the repository as Public, then select the green Begin import button:

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image10.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image10.png" alt="Image 10" />
</a>

Once prepared, a link to your repo will be provided. Go to https://github.com/DUNE/computing-HWDB to verify the base installation. 

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image14.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image14.png" alt="Image 14" />
</a>

The styles configuration requires that the default branch be the gh-pages branch, when built it is main, view this under the Settings tab, which opens in General

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image11.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image11.png" alt="Image 11" />
</a>

The Default branch is changes from main to gh-pages using the dual direction button

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image5.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image5.png" alt="Image 5" />
</a>

the result

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image13.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image13.png" alt="Image 13" />
</a>


Notice missing from the repository in the collection are both the configuration file _config.yml, and the index.md file. Also missing are setup.md, README.md. To generate the necessary configuratoin files it is best to retreat to your local development environment.

Using the GitHub Desktop application (see install notes), build a local repository of the https://github.com/DUNE/computing-HWDB Under GitHub's File menu, select Clone Repository... 

Assuming you are logged in to GitHub within the GitHub Desktop, in the popup window filter from GitHub.com the DUNE repository you just built, namely DUNE/computing-HWD and set the appropriate local working directory to park the repo. Select the blue Clone button.

Once built, from a Terminal window, go to that directory to verify contents, and the existance of the file bin/lesson_initialize.py then run it using the python command $ python bin/lesson_initialize.py  where the _config.yml, index.md, setup.md, and README.md files will be generated.

Most important is configuring the _config.yml file, checking that file the #FixME prompts. There are only a few.

Before editing the other new files, use GitHub Desktop to commit your update, providing a Summary and optionally a Description of the changes, Commit to gh-pages using the blue button, then select the Push origin (blue button), then check for those on the GitHub site.

GitHub can now auto-generate your .io.

Go to About (upper right) and edit (select the gear), and select the URL checkbox, which will link your GitHub code page to the .io file for easy access.

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image16.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image16.png" alt="Image 16" />
</a>

Edit index.md, setup.md, and README.md accordingly.

Add _episodes as needed._





#### Image Archive

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image1.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image1.png" alt="Image 1" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image3.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image3.png" alt="Image 3" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image4.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image4.png" alt="Image 4" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image5.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image5.png" alt="Image 5" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image6.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image6.png" alt="Image 6" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image7.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image7.png" alt="Image 7" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image8.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image8.png" alt="Image 8" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image9.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image9.png" alt="Image 9" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image10.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image10.png" alt="Image 10" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image11.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image11.png" alt="Image 11" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image12.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image12.png" alt="Image 12" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image13.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image13.png" alt="Image 13" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image14.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image14.png" alt="Image 14" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image15.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image15.png" alt="Image 15" />
</a>

<a href="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image16.png">
  <img src="{{ page.root }}/fig/Build-for-May-2024-DUNE-computing-HWDB-training-on-github/images/image16.png" alt="Image 16" />
</a>



{% include links.md %}

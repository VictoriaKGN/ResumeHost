---
layout: page
title: README
permalink: /README/
---

# How to host and format a resume using Markdown, Markdown editor, Github Pages and Jekyll in Windows

## Purpose
* Host and format a resume using Markdown, editor of choice, Github Pages, and Jekyll.
* Understand and incorporate tools from Andrew Etter's book Modern Technical Writing

## Prerequisites
* [Github](https://github.com/) account
* [Git installed](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and connected to your account
* Resume formatted in [Markdown](https://www.markdownguide.org/)

## Instructions
#### Install Ruby and Jekyll
> _Format a document with a static site generator_
> Static sites are incredible dependable, quick, and easy to use. They dont require any additional installs or complecated dependencies. In this case we are using Jekyll to host the local static site.

**1. Install Ruby**
* Head over to [RubyInstaller](https://rubyinstaller.org/downloads/) and install the latest version under WITH DEVKIT (this is important as it will help us later on)
* Navigate to the folder in which the download happened (most likely in downloads), right click on the rubyinstaller and choose `Run as administrator`.
* Follow the installation process with default options selected.
* Once RubyInstaller window popped up, select option `MSYS2 and MINGW development toolchain`

**2. Install Jekyll**
* Open command promped by searching `cmd` in the search bar on your computer.
* To make sure Ruby was correctly installed, run `ruby -v`. A version printed indicates it was correctly installed.
* Do the same with `gem -v`
* Run `gem install jekyll bundler`
* To make sure Type `jekyll -v` and hit enter to make sure it was correctly installed.

#### Host a resume on a local site using Jekyll
> _Use a lightweight markup language_
> Lightweight markup languages make it easier than ever to display text. They are easy and fast to learn and can be used to make websites quick. In this case we are using Markdown.

**1. Host local site**
* Open command promped or terminal in the text editor of your choice and make sure you are at the right directory
* Run `jekyll new <website_name>` where \<website_name\> is the name of your choice for the website
* Navigate into the new directory by running `cd \<website_name\>`
* To proceed, run `bundle install` to make sure all the correct gems been installed
* Run `bundle exec jekyll serve`
* Open any browser of choice and go to `localhost:4000`

**2. View your resume on the site**
* Open the folder of the site in a markdown editor of your choice
* Head over to `index.markdown`
* Remove all the code after the second `---` line
* Copy and paste there your resume that is written in Markdown
* Remove the file in `_posts` folder
* Change the info in `_config.yml` to match your info
* Refresh the local site and you are done!

#### Get the resume on GitHub Pages
> _Host documents on a distributed version control system_
> Version control makes it easier to keep track of changes and enable multiple people to work on the same files without making a mess. Any sort of changes are recorded and its super easy to revert them. In this case we are using GitHub.

**1. Push the static website into GitHub**
* Open Git CMD and make sure you are at the Jekyll project folder
* Run `git init` to initialize the git repository inside the Jekyll project
* To checkout GitHub Pages branch, run `git checkout -b gh-pages`
* Run `git add .` to add stage the new files 
* Run `git commit -m "initial commit"` to commit the changes
* Create a repository in Github called `<user_name>.github.io` where \<user_name\> is your GitHub username
* Run `git remote add origin <remote_repository_URL>` where \<remote_repository_URL\> is the URL of your GitHub repository
* To push all files into that repository, run `git push origin gh-pages`
* Refresh the GitHub repository and you should be able to see the files

**2. Open the resume's GitHub Pages website**
* Head to the settings of the GitHub repository
* Go to `Pages` on the left menu
* Look for a message that says `Your site is live at <URL>` and click the \<URL\>
* Your resume is now live!

#### More resources
* [Markdown tutorial](https://www.youtube.com/watch?v=HUBNt18RFbo)
* [Modern Technical Writing by Andrew Etter](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS/ref=sr_1_1?keywords=modern+technical+writing+by+andrew+etter&qid=1667328753&qu=eyJxc2MiOiIwLjAwIiwicXNhIjoiMC4wMCIsInFzcCI6IjAuMDAifQ%3D%3D&sprefix=Andrew+etter+%2Caps%2C108&sr=8-1)
* [Jekyll tutorials](https://www.youtube.com/watch?v=T1itpPvFWHI&list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB)

## Authors and Acknoledgments
#### Reviewers:
* Aqil Mukhi
* Ryan Dotzlaw
* Mostafa Hamed

## FAQ
* Why is Markdown better than a word processor?
> The main reasons why Markdown is better than a word processor is because Markdown supports Version Control, can be eddited on any editor of choice, is simple, and can be written using keyboard only.

* Why are my changes not showing on the local static site?
> The first thing is to make sure that the server is runnint - you can check that by looking at the message that been printed after running `bundle exec jekyll serve`. In case everything is running and no errors or warnings are displayed, make sure to save the changes on the editor and refresh the local site.

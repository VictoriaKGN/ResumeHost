---
layout: page
title: README
permalink: /README/
---

# How to host and format a resume using Markdown, Markdown editor, Github Pages and Jekyll in Windows

## Purpose
* Host and format a resume using Markdown, Markdown editor, Github Pages, and Jekyll.
* Understand and incorporate tools from Andrew Etter's book Modern Technical Writing

## Prerequisites
* Github account
* Git installed and connected to your account
* Resume formatted in Markdown

## Instructions
#### Install Ruby and Jekyll
1. Install Ruby
* Head over to [RubyInstaller](https://rubyinstaller.org/downloads/) and install the latest version under WITH DEVKIT (this is important as it will help us later on)
* Head over to the folder in which the download happened (most likely in downloads), right click on the rubyinstaller and choose `Run as administrator`.
* Follow the installation process with default options selected.
* Once RubyInstaller window popped up, select option `MSYS2 and MINGW development toolchain`

2. Install Jekyll
* Open command promped by searching `cmd` in the search bar on your computer.
* To make sure Ruby was correctly installed, run `ruby -v`. A version printed indicates it was correctly installed.
* Do the same with `gem -v`
* Run `gem install jekyll bundler`
* To make sure Type `jekyll -v` and hit enter to make sure it was correctly installed.

#### Host a resume on a local site using Jekyll
1. Host local site
* Open command promped or terminal in the text editor of your choice and make sure you are at the right directory.
* Run `jekyll new <website_name>` where \<website_name\> is the name of your choice for the website.
* Navigate into the new directory by running `cd \<website_name\>`
* To proceed, run `bundle install` to make sure all the correct gems been installed
* Run `bundle exec jekyll serve`
* Open any browser of choice and go to `localhost:4000`

2. View your resume on the site
* Open the folder of the site in a markdown editor of your choice
* Head over to `index.markdown`
* Remove all the code after the second `---` line
* Copy and paste there your resume that is written in Markdown
* Refresh the local site and you are done!

#### Get the resume on GitHub Pages
1. Set a GitHub repository inside the Jekyll project folder
* Open the commend promped or terminal in the text editor and make sure you are at the Jekyll project folder
* Run `git init` to initialize the git repository
* To checkout GitHub Pages branch, run `git checkout -b gh-pages`
* Run `git add .` to add stage the new files 
* Run `git commit -m "initial commit"` to commit the changes

2. Push the repository to GitHub
* Create a repository in Github called `<user_name>.github.io` where \<user_name\> is your GitHub username
* Run `git remote add origin <remote_repository_URL>` where \<remote_repository_URL\> is the URL of your GitHub repository.
* To push all files into that repository, run `git push origin gh-pages`
* Refresh the GitHub repository and you should be able to see the files.

3. Open the resume's GitHub Pages website
* Head to the settings of the GitHub repository
* Go to `Pages` on the left menu
* Look for a message that says `Your side is live at <URL>` and click the URL
* Your resume is now live!


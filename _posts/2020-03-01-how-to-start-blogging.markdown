---
layout: post
title:  "Start personal blog with GitHub pages"
date:   2020-03-01 14:43:30 +0100
categories: GitHub, GitHub Pages, Jekyll
---

# Is blogging something for me?
Do you have a lot of interesting things to share? Do you want to help others with problems you have overcome? Do you want to show your expertise online? 
Then starting a personal blob would be a great idea.

There are a lot of different platforms to start writing a blog like [wordpress.org](https://wordpress.org), [blogger](https://blogger.com), [wordpress.com](https://wordpress.com), [wix](https://wix.com),... You can find a lot of information and comparisons between these different platforms. 

This guide will show you how to start a personal blog on GitHub Pages with Jekyll.

# Why GitHub Pages?
[GitHub Pages](https://pages.github.com/) is an easy and free way to start your fist personal blob. It is a static site hosting service that takes HTML, CSS, and JavaScript files straight from a repository on GitHub. 

[GitHub](https://github.com) is a web and cloud-based service that helps developers store and manage their code, as well as track and control changes to their code.

Benefits of using GitHub pages:

* Hosting your site on GitHub Pages will be completely free. You can choose between a subdomain on GitHub (</username/>.github.io) or assign you own custom domain name.
* Real time updates: you can easily update your site by committing your changes to GitHub repository. GitHub automatically pushes the update out live.
* Jekyll support: Jekyll is a ruby based site generator which creates HTMl pages for you.

# Setup GitHub Pages with Jekyll
>note: this tutorial is based on windows installation.

## Prerequisites
To start with GitHub pages your should install some Prerequisites.

1. Install Ruby: 
   
   Ruby is an open source object-oriented programming language mainly used in web programming. 
   
   [Download Ruby](https://rubyinstaller.org/downloads/) and install.

   Check Ruby installation in cmd line.
   ```cmd 
   ruby -v
   ```

2. Install Bundler
   
   [Bundler](https://bundler.io/) provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed.

    ```cmd
    gem install jekyll bundler
    ```

    See if Jekyll installed properly
    ```
    jekyll -v
    ```

3. Install Git or GitHub desktop
    
    Download and install GitHub desktop from [here](https://desktop.github.com/)

    Or if you like CLI more you can [Install Git](https://git-scm.com/downloads)

## Create repository
Go to your repositories on GitHub.

1. Create new repository
![create new repo]({{ site.url }}/assets/new-repo.png)

2. Name repository in format: 
    </user/>.github.io
    ![new repo]({{ site.url }}/assets/create-repo.png)

    Make repository public.

## Create Jekyll folder structure

1. Connect to repository in GitHub desktop

    ![github desktop]({{ site.url }}/assets/connect-to-repo.png)

    Clone your newly created repository.

    ![github clone]({{ site.url }}/assets/clone-repo.png)


2. Open cmd window and navigate to local folder
    
     ```cmd
    Cd <path to local folder>
    ```

3. Initialize bundle. This will create bundle Gemfile
    ```cmd
    bundle init
    ```
4. Add Jekyll gem to the Gemfile 
    ```cmd
    bundle add jekyll
    ```
5. Create new Jekyll site
    ```cmd
    bundle exec jekyll new . --force
    ```
6. Install the dependencies specified in your Gemfile
    ```cmd
    bundle install
    ```
7. Your folder structure should look like this.
    ![folder structure]({{ site.url }}/assets/folder-structure.png)

8. Open Gemfile that was created and comment out gem "jekyll", "~> 3.8.5"
   
   Uncomment gem "github-pages", "~> 204", group: :jekyll_plugins

    ![update gemfile]({{ site.url }}/assets/update-gem-file.png)

9. Test your site locally.    
    ```cmd
    bundle exec jekyll serve
    ```
    ![local]({{ site.url }}/assets/local.png)

10. Commit changes locally
    
    Go back to GitHub desktop and identify you local changes.
    ![changes]({{ site.url }}/assets/changes.png)

    Enter description and commit your changes

    ![commit]({{ site.url }}/assets/commit.png)
11. Push changes
    ![push]({{ site.url }}/assets/push.png)

## View your site on GitHub
Go to settings from your GitHub repository.
    ![settings]({{ site.url }}/assets/settings.png)

Go to your personal blog site.
    ![site]({{ site.url }}/assets/site.png)
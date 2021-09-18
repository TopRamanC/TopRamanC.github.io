---
layout: post
title:  "Blog 0 - Getting Started with GitHub"
date:   2021-09-17 18:34:20 -0700
categories: jekyll update
---

# **What is GitHub?**
#### GitHub is used for software development using verison control and Git for internet hosting. GitHub is essentialy a repository hosting database used for project collaborations by many companies and people around the world.

# **Important commands for GitHub:**
### **Git add**
#### Git add is used to add files to the staging area before it can be commit to a repository.
##### **Command in usage:**
{% highlight ruby %}
$ git add <file or directory name>
{% endhighlight %}


### **Git Commit**
#### Git Commit is used to commit the changes to your local repository before the changes can be pushed to your Git Repository. Each commit is associated with a "commit message" to help understand the changes made.
##### **Command in usage:**
{% highlight ruby %}
$ git commit -m "Commit message"
{% endhighlight %}

### **Git Push**
#### Git Push is used to push your commits from your local respository into the Git repository.
##### **Command in usage:**
{% highlight ruby %}
$ git push <>
{% endhighlight %}

### **Git Status**
#### Git Status shows any files in the staging area that are not commited.
##### **Command in usage:**
{% highlight ruby %}
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)

  	index.html
{% endhighlight %}

### **Git Pull**
#### Git Push is used to get the latest version of a respository from the Git repository into your local respository.
##### **Command in usage:**
{% highlight ruby %}
$ git pull <respository>
{% endhighlight %}

### **Git Fetch**
#### Git Fetch is used to download any commits or files from your Git repository into your local repository.
##### **Command in usage:**
{% highlight ruby %}
$ git fetch <repository>
{% endhighlight %}

### **Git Checkout**
#### Git Checkout is used to switch between branches.
##### **Command in usage:**
{% highlight ruby %}
$ git checkout <branch name>
{% endhighlight %}

### **Git Merge**
#### Git Merge is used to merge two branches together. In many situations you may have a "staging branch" where you make all your changes and later can be used to combine with your main branch.
##### **Command in usage:**
{% highlight ruby %}
$ git merge <branch name>
{% endhighlight %}

# **Visual explanation for Git commands:**
<img src="https://topramanc.github.io/Images/git.png">
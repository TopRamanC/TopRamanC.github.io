---
layout: post
title:  "Blog 1 - Docker"
date:   2021-09-24 18:21:20 -0700
categories: jekyll update
---

# **What is Docker?**
#### Docker is an application development tool that helps DevOps and developers as it allows you to use virtualization to build and run applications in containers. 

# **What is a Container?**
#### A Container is a run-time environment where you can build and deploy software. Each container is independent and do not affect other running containers. Containers run at the app layer which allows them to virtualize the operating systemm to run isolated processes.

# **What is a Docker Container Image?**
####  Docker Container Image is a file that conatins instructions for deplying containers. Docker Image consists of all the files necesarry to deploy a functional environment such as source code, libraries, and dependencies. 

# **Important commands for Docker:**
### **docker ps**
#### Usage: Displays a list of all running containers.
##### **Example**
{% highlight ruby %}
root@ubuntu:~# docker ps
CONTAINER ID   IMAGE          COMMAND       CREATED      STATUS         PORTS                                       NAMES
861e02fa00ad   ubuntu:18.04   "/bin/bash"   2 days ago   Up 8 seconds   0.0.0.0:9090->9090/tcp, :::9090->9090/tcp   simple-prometheus
{% endhighlight %}

![Commands Image](https://topramanc.github.io/Images/ps.png)



### **docker ps -a**
#### Usage: Displays all running and stopped containers.
##### **Example**
{% highlight ruby %}

{% endhighlight %}

### **docker run**
#### Usage: Create a container from an image.
##### **Example**
{% highlight ruby %}

{% endhighlight %}

### **docker exec**
#### Usage: Access a running container.
##### **Example**
{% highlight ruby %}

{% endhighlight %}

### **docker stop**
#### Usage: Stop a running container.
##### **Example**
{% highlight ruby %}

{% endhighlight %}

### **docker rm**
#### Usage: Remove a stopped container.
##### **Example**
{% highlight ruby %}

{% endhighlight %}

### **docker rmi**
#### Usage: Remove an image.
##### **Example**
{% highlight ruby %}

{% endhighlight %}
---
layout: post
title:  "Blog 2 - Ansible"
date:   2021-10-01 18:43:20 -0700
categories: jekyll update
---

# **What is Docker?**
#### Docker is an application development tool that helps DevOps and developers as it allows you to use virtualization to build and run applications in containers. 

# **What is a Container?**
#### A Container is a run-time environment where you can build and deploy software. Each container is independent and do not affect other running containers. Containers run at the app layer which allows them to virtualize the operating systemm to run isolated processes.

# **What is a Docker Container Image?**
####  Docker Container Image is a file that conatins instructions for deploying containers. Docker Image consists of all the files necesarry to deploy a functional environment such as source code, libraries, and dependencies. 

# **Important commands for Docker:**
### **docker ps**
#### Usage: Displays a list of all running containers.
##### **Example:**
{% highlight ruby %}
root@ubuntu:~# docker ps
CONTAINER ID   IMAGE          COMMAND       CREATED      STATUS         PORTS                                       NAMES
861e02fa00ad   ubuntu:18.04   "/bin/bash"   2 days ago   Up 8 seconds   0.0.0.0:9090->9090/tcp, :::9090->9090/tcp   simple-prometheus
{% endhighlight %}

### **docker ps -a**
#### Usage: Displays all running and stopped containers.
##### **Example:**
{% highlight ruby %}
root@ubuntu:~# docker ps -a
CONTAINER ID   IMAGE           COMMAND       CREATED        STATUS                    PORTS                                       NAMES
3e29936bb794   node-exporter   "/bin/bash"   34 hours ago   Exited (0) 34 hours ago                                               elegant_kare
861e02fa00ad   ubuntu:18.04    "/bin/bash"   2 days ago     Up 13 minutes             0.0.0.0:9090->9090/tcp, :::9090->9090/tcp   simple-prometheus
{% endhighlight %}

### **docker run**
#### Usage: Create a container from an image.
##### **Example:**
{% highlight ruby %}
root@ubuntu:~# docker run -it ubuntu:18.04
root@9729fafc8737:/#
{% endhighlight %}

### **docker exec**
#### Usage: Access a running container.
##### **Example:**
{% highlight ruby %}
root@ubuntu:~# docker exec -it simple-prometheus /bin/bash
root@861e02fa00ad:/#
{% endhighlight %}

### **docker stop**
#### Usage: Stop a running container.
##### **Example:**
{% highlight ruby %}
root@ubuntu:~# docker stop simple-prometheus
simple-prometheus
root@ubuntu:~# 
{% endhighlight %}

### **docker rm**
#### Usage: Remove a stopped container.
##### **Example:**
{% highlight ruby %}
root@ubuntu:~# docker rm practical_dijkstra
practical_dijkstra
root@ubuntu:~# docker ps -a
CONTAINER ID   IMAGE           COMMAND       CREATED        STATUS                     PORTS     NAMES
3e29936bb794   node-exporter   "/bin/bash"   34 hours ago   Exited (0) 34 hours ago              elegant_kare
861e02fa00ad   ubuntu:18.04    "/bin/bash"   2 days ago     Exited (0) 2 minutes ago             simple-prometheus
root@ubuntu:~# 
{% endhighlight %}

### **docker rmi**
#### Usage: Remove an image.
##### **Example:**
{% highlight ruby %}
root@ubuntu:~# docker rmi ubuntu:latest
Untagged: ubuntu:latest
Untagged: ubuntu@sha256:9d6a8699fb5c9c39cf08a0871bd6219f0400981c570894cd8cbea30d3424a31f
Deleted: sha256:fb52e22af1b01869e23e75089c368a1130fa538946d0411d47f964f8b1076180
Deleted: sha256:4942a1abcbfa1c325b1d7ed93d3cf6020f555be706672308a4a4a6b6d631d2e7
root@ubuntu:~# 
{% endhighlight %}
---
layout: post
title:  "Blog 2 - Ansible"
date:   2021-10-01 18:43:20 -0700
categories: jekyll update
---

# **What is Ansible?**
#### Ansible is a configuration management tool that enables infrastructure as code. It can deploy software, configure systems, and also provides continuous deployments.

# **What is Infrastructure as Code (IaC)?**
#### Infrastructe as Code (IaC) is the process of provisioning and managing networking and computing infrastructure through code files rather than physical hardware configuration.

# **Why should you use Ansible?**
####  *Ansible can do multiple jobs sucsh as Configuration Management and Deployments.
####  *Ansible is agentless, cloud native, and SSH based which allows the user to push changes from one source to multiple sites.
####  *Ansible is extensible has it has a large community with many pre-built modules and you can build your own custom modules.
####  *Ansuble is easy to setup and uses syntax based on YAML.

# *


# **Important commands for Docker:**
### **docker ps**
#### Usage: Displays a list of all running containers.
##### **Example:**
{% highlight ruby %}
root@ubuntu:~# docker ps
CONTAINER ID   IMAGE          COMMAND       CREATED      STATUS         PORTS                                       NAMES
861e02fa00ad   ubuntu:18.04   "/bin/bash"   2 days ago   Up 8 seconds   0.0.0.0:9090->9090/tcp, :::9090->9090/tcp   simple-prometheus
{% endhighlight %}
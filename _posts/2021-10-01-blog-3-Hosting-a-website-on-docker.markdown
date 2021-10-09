---
layout: post
title:  "Blog 3 - Hosting a website on Docker"
date:   2021-10-07 18:0:20 -0700
categories: jekyll update
---

# **What do you need to host a website on Docker?**
* Docker installed.
* A Dockerfile
* Your html file

# **What is a dockerfile?**
#### A Dockerfile consists of commands and istructions that are used to built a docker image. Dockerfile helps automate the process of builidng an image by executing numerous commands at once.

# **What should your Dockerfile contain?**
* Your Dockerfile must contain the Apache httpd server along with your html file to be hosted.

# **Below is a Dockerfile to host an static webpage on a apache server:**
{% highlight ruby %}
FROM httpd

WORKDIR /usr/local/apache2/htdocs

COPY index.html .
{% endhighlight %}

# **Docker commands needed to host your website:**
* Docker build -t <name of the tag of the image being built> .
* Docker run -dit --name my_website -p 8080:80 my_image

#### 
---
layout: post
title:  "Blog 6 - Virtual Hosts on Apache"
date:   2021-10-29 15:0:37 -0700
categories: jekyll update
---

# **What are Virutal Hosts on Apache?**
#### Virtual hosts are used to run more than one domain on a single IP address. It allows you to have multiple websites running on a single server.

# **There are two types of Virtual Hosts:**
#### IP based Virtual Hosts - your apache server will run two or more IP addresses.
#### Domain based Virtual Hosts - your spache server will have one IP address but with multiple domains.

# **How do I make Virtual Hosts:**
#### Step 1: Create a new Virtual Host File in sites-available directory.
{% highlight ruby %}
sudo vi /etc/apache2/sites-available/virtualhost.conf
{% endhighlight %}

#### Step 2: Add your Virtual Host block to your file.
#### The two Virtual Host block below are domain based Virtual Hosts where you can access your website using both of the domains listed below in the Virtual Host blocks:
{% highlight ruby %}
<VirtualHost *:8080 *:80>

  ServerName www.batteryyard88.com 

	ServerAdmin webmaster@localhost
	DocumentRoot /var/www/html
        
  ErrorDocument 404 /forbidden.html
  ErrorDocument 403 /not-found.html

  Alias /user1 /home/user1/public_html
  Alias /user2 /home/user2/public_html
  Alias /user3 /home/user3/public_html
  Alias /user4 /home/user4/public_html
  Alias /user5 /home/user5/public_html

  Alias /promotions /home/marketing/public_html 

  ErrorLog ${APACHE_LOG_DIR}/error.log
	CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>

<VirtualHost *:8080 *:80>
       
  ServerName www.batterymarket88.com 

	ServerAdmin webmaster@localhost
	DocumentRoot /var/www/html
        
  ErrorDocument 404 /forbidden.html
  ErrorDocument 403 /not-found.html

  Alias /user1 /home/user1/public_html
  Alias /user2 /home/user2/public_html
  Alias /user3 /home/user3/public_html
  Alias /user4 /home/user4/public_html
  Alias /user5 /home/user5/public_html

  Alias /promotions /home/marketing/public_html 
       
	ErrorLog ${APACHE_LOG_DIR}/error.log
	CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
{% endhighlight %}

#### Step 3: You need to activate your Virtual Host file.
{% highlight ruby %}
sudo a2ensite virtualhost.conf
{% endhighlight %}

#### Step 4: Restart Apache to apply your changes.
{% highlight ruby %}
sudo service apache2 restart
{% endhighlight %}
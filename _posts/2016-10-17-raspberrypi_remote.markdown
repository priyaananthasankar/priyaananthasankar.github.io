---
layout: post
title:  "Raspberry PI Remote Connection using Weaved"
date:   2016-Oct-17 10:00:43 +0530
categories: jekyll update
author: "Priya Ananthasankar"
---
Setup a Remote connection to Raspberry Pi like this:

1. Connect your Raspberry Pi to a HDMI monitor. Make sure you have a keyboard and a mouse. Make sure it is able to connect to the internet using a Wifi.
2. Install Weaved for Raspberry Pi. Weaved is a service software freely downloadable for Pi. https://www.weaved.com. Create a user id and password with Weaved.
3. Open a terminal and type these:

{% highlight ruby %}
sudo apt-get install weavedconnectd
sudo weavedinstaller
{% endhighlight %}

4. It will ask you stuff like this:
{% highlight ruby %}
1) Sign in to your existing remot3.it account
2) Request a code for a new remot3.it account
3) Enter a verification code received in e-mail
4) Exit
{% endhighlight %}

5. Select 1 and sign in to your account. It will prompt for user name and password.
6. Once you login it will ask you options to install SSH,VNC or the Web interface.
7. Here is an SSH example:
{% highlight ruby %}
1) Attach/reinstall remot3.it to a Service
{% endhighlight %}

8. It will throw a Protocol Selection Menu like this

{% highlight ruby %}
1) SSH on port 22
{% endhighlight %}

9. It will configure SSH on port 22. You can select another port if you want to. You can select a name say "eagles"

10. Now check if your SSH service is up

{% highlight ruby %}
sudo netstat -apn | grep -w tcp | grep LISTEN
{% endhighlight %}

11. Now open a terminal in *another laptop or desktop* and login to your weaved account over the web. Weaved will show you the SSH connection named "eagles" in their web interface. Just click on it.

12. Here is an image of how it shows up. 
<div>
<img display="block" margin="auto" src="/assets/eagles.jpg" height="250" width="400">
</div>

13. Connect from your laptop through SSH into the pi. When prompted give the pi password:
<br>
{% highlight ruby %}
$ ssh -l pi proxy13.yoics.net -p 37955
pi@proxy13.yoics.net's password: 

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Sun Oct 16 23:59:57 2016 from localhost
pi@raspberrypi:~ $ 
{% endhighlight %}




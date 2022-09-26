---
author: '@ramonsuarez'
categories:
- Uncategorized
date: "2011-05-20T07:21:00Z"
excerpt: I've been running Ubuntu 11.4 Natty Narwhal for a few days already on a brand
  new Samsung 900x3a and I have to say that I'm quite happy with it. First of all,
  Ubuntu Linux is the best operating system in this galaxy. Then, the machine is great,
  an...
guid: http://ramonsuarez.com/how-to-install-ubuntu-in-a-samsung-900x3a-ult
id: 62
tags:
- howto
- install
- linux
- nattynarwhal
- samsung900x3a
- ubuntu
title: How To Install Ubuntu in a Samsung 900x3a ultraportable laptop
url: /how-to-install-ubuntu-in-a-samsung-900x3a-ult/
---

I’ve been running Ubuntu 11.4 Natty Narwhal for a few days already on a brand new Samsung 900x3a and I have to say that I’m quite happy with it. First of all, Ubuntu Linux is the best operating system in this galaxy. Then, the machine is great, and not only for the looks.

Here’s a simplified How-To:

1. [Download Ubuntu](http://www.ubuntu.com/sites/all/themes/ubuntu10/logo.png), make sure that in the dropdown box you choose the 64bit version.
2. Luckily, the Samsung 9 series laptop does not have a CD/DVD so you have to [install Ubuntu with a USB stick](https://help.ubuntu.com/community/Installation/FromUSBStick). You need a disk with at least 1 gigabyte. All information in the disk will be erased when preparing the install disk.
3. Plug the disk in the right-side USB port. It will not work in the left side.
4. Start your computer and follow the [installation steps](http://blog.sudobits.com/2011/04/23/how-to-install-ubuntu-11-04-from-usb-or-cd/). This is a good source of information to [learn about partitioning](http://ubuntuforums.org/showthread.php?t=282018). Here’s an excellent [Ubuntu guide to do manual partitions](http://www.linuxbsdos.com/2011/05/04/manual-disk-partitioning-guide-for-ubuntu-11-04/).
5. Once the install is done, remove the USB key and reboot your computer.
6. OPTIONAL: you may want to go over this article on the [top 10 things to do after you install Ubuntu Natty Narwhal](http://www.unixmen.com/linux-tutorials/linux-distributions/linux-distributions4-ubuntu/1540-top-things-to-do-after-installing-ubuntu-1104-natty-narwhal).

The mouse trackpad/touchpad is over sensitive and does not allow click and drag. The solution is in the [Ubuntu Samsung 9 Series](http://ubuntuforums.org/showthread.php?t=1737086) page:

> **<span class="highlight">Trackpad</span>**  
> \*If you have a problem you can use the following method to enable right clicking:
> 
> <div style="margin:20px;margin-top:5px;"><div class="smallfont" style="margin-bottom:2px;">Code:</div><div class="CodeRay"><div class="code"><div class="CodeRay"><div class="code">```
> sudo suecho options psmouse proto=exps > /etc/modprobe.d/psmouse.modprobereboot
> ```
> 
> </div></div></div></div></div>**-OR-**
> 
> Go to System&gt;Preferences&gt;Mouse and select “TouchPad” Tab and select 2 finger scrolling and 2 finger right click.

<span style="font-size:13px;font-weight:normal;">\* Remember that to copy or paste text in the terminal you have to use CTRL+Shift+C and </span>CTRL+Shift+V.

I used the code solution and **lost the trackpad scrolling**.

If you are running more than one operating system, this [Natty Narwhal grub guide](http://ubuntuguide.org/wiki/Ubuntu:Natty#Installing_multiple_OS_on_a_single_computer) can be very useful. I did have an issue with the Grub boot-loader with my install, here’s a guide on [how to re-install Grub2](<https://help.ubuntu.com/community/Grub2#Reinstalling from LiveCD>).

And last, If you have any doubts or want to learn more about how to use it, check the [Ubuntu user documentation](https://help.ubuntu.com/community). They can even help you [switch to Ubuntu from Windows or Mac](<https://help.ubuntu.com/community#Switching From Another Operating System>).
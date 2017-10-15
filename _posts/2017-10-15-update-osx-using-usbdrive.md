---
title: update OSX using a usb drive
layout: post
img: update-to-sierra-using-usbdrive.jpg
---

# History :
2 years ago i installed OSX(el capitan) on my friend production machine(after i picked the hardware myself, i choose an asus motherboard because where i live sellers does not sell gigabyte), after 2 days (yes 2 days, i finally succeded on make it work, problem was caused mainly by me trying to use binary file of another build ), to resume after that thing went flawlessly, system work as expected, even after updates, sometimes i just need to fix graphic driver and audio, just an install of a new drivers and copy paste of a kext, until 2 week ago after uninstalling Teamviewer and rebooting, kernel panic, missing kext.


![kernel panic screenshot]({{ "/images/kernel-panic.png" | absolute_url }})


i searched everywhere, this kext does not exist,
a production machine, many project, tried everything, i cant access data.



# Preinstall step and upgrade

i didn't figure until my friend told me why not upgrade using a usb drive.

after searching on the net, except one post that say it's possible to update to yosemite using a usb drive, nothing on the net, which made spectacle about the whole idea, the solution was to backup all what my friend needed than to give it a shoot, i booted up using a ubuntu bootable usb drive, i was able to access all my file but when i tried to copy them, i had a lot of problem with permissions, at the end i removed the ssd(a 120GB ssd) than i putted as a second drive on my own hackintosh ( using a sata drive connected to the motherboard), finally i copied all the needed file (using carbon clone, this software is speedy).

after that i created a usb drive with sierra on it, than i booted on it, you will come to a screen where it request you to choose the drive on which to install sierra, i tell you **osx will be installed on** and it give you hard drive to choose from( this is the confusing part, nothing about upgrade ), when it come to this screen just choose the hard drive on which osx is installed (the one you want to upgrade), than hit install, it may take a while, progress bar may seem to be stuck, but it is installing, after it finish your system should restart, with your system running sierra, with all your data (and kernel panic gone), for my case with my suprise, i didn't need to update neither the graphic drive (nvidia one) and the ethernet drive, they work after update.

# Resume
to make thing short, yes you can upgrade to sierra using a usb drive, even if the installer say nothing about upgrade(it only say install), if you select a partition that contain osx (like in my case el capitan), "install" will upgrade it ( it does not a clean install ), finally sometimes running an older osx version can have it's benefits

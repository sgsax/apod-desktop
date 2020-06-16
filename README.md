# apod-desktop
Script to set your Linux desktop wallpaper to the Astronomy Picture of the Day.

## Usage
Invoke the script on login using a method appropriate to your desktop manager
```
Usage: apod gnome1|gnome22|gnome24|gnome3|kde|fvwm|fvwm-xv|xfce|xfce4|hsetroot|i3
```

## How it works
This script scrapes the current [Astronomy Picture of the Day page](https://apod.nasa.gov/apod/astropix.html) for the image linked there, downloads the image, and sets it as your desktop wallpaper for a variety of Linux desktop managers.

## Supported desktop managers
The current supported list is as follows:

* Gnome 1.x, 2.2, 2.4, 3.x
* KDE
* FVWM (alternatively using xv)
* XFCE
* Enlightenment
* i3
* Generic X11 using hsetroot

## Temporary transition image
I found that for some desktops, resetting the wallpaper to a new file with the same name did not always refresh. For those desktop managers, I switch to a default temporary image first, then back to the new APOD image. I have provided a sample image with this repository which is a copy of the classic RCA "Indian Head" TV test pattern [Source](https://en.wikipedia.org/wiki/File:RCA_Indian_Head_test_pattern.JPG). This is of course highly insensitive, so feel free to change it to something else you prefer.

## Customization
There are two tunable settings you will need to adjust for your own environment:
1. The location of your downloaded APOD image
2. The aforementioned temporary image used to facilitate refreshing the desktop

## Caveats
* All downloaded images are named `apod.jpg`, actual filetype is ignored. Most DMs seem to be able to cope with this and display the iamge anyway.
* Occasionally the APOD image is a video. In this case, either the system default wallpaper or black screen is displayed, depending on your distro and DM.

### History
I've been curating this for personal use for nearly 15 years, updating for new versions of DMs as I have switched back and forth over the years. I've always enjoyed it and decided to upload it for the public good.

# My_Dwm
dwm - dynamic window manager
============================
dwm is an extremely fast, small, and dynamic window manager for X.

What's in this fork?
--------------------
This is what you get:
![Screenshot](screenshot.png?raw=true "Bussy")
![Screenshot](screenshot_1.png?raw=true "Clear")

My config contains these features:
- based on version 6.1(20151109)
- MOD key is alt key
- Bottomstack patch applied
- Mod+F1 keys   launch power menagment with dmenu (poweroff, reboot, lock the screen etc.)
- Mod+F2 keys   launch dmenu_media (MPC controller menu)
- Mod+F3 keys   launch dmenu_home which browses through home folder and opens files
- Mod+F4 keys   take screenshot
- Mod+F5 keys   take sreenshot of selected area
- Mod+F6 keys   launch dmenu which browses through applications menu and launches apps
- Mod+F7 keys   launch ranger fm
- Mod+p keys    launches dmenu_all
- bstack        can be selected with [Alt]+[u]
- bstackhoriz   can be selected with [Alt]+[o]


Requirements
------------
In order to build dwm you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install

If you are going to use the default bluegray color scheme it is highly
recommended to also install the bluegray files shipped in the dextra package.


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.




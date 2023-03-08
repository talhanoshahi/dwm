dwm - dynamic window manager
============================
dwm is an extremely fast, small, and dynamic window manager for X.


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

Patches Applied
---------------
1. [aspectresize-6.2](https://dwm.suckless.org/patches/aspectresize/)
2. [functionalgaps-6.2](https://dwm.suckless.org/patches/functionalgaps/)
3. [attachaside-6.3](https://dwm.suckless.org/patches/attachaside/)
4. [swallow-6.3](https://dwm.suckless.org/patches/swallow/)
5. [actual-fullscreen-20191112-cb3ff58a](https://dwm.suckless.org/patches/actualfullscreen/)
4. [bar height-6.3](https://dwm.suckless.org/patches/bar_height/)

Synaptics touchpad driver for X.Org
===================================

This is a fork from git://anongit.freedesktop.org/xorg/driver/xf86-input-synaptics

ABOUT
-----

This is a bit of an "eclectic" Synaptic driver. Includes SynapticsSHM 
driver--which is actually removed in the newer versions of synaptics, but is 
required for multitouch programs like xSwipe.

Than PalmRejection using PalmMinZ is included from somewhere.

And finally included is three finger dragging from: quadpixels/three-finger-dragging
I am not sure if there is a setting to turn this on/off. So you might want to 
checkout an earlier commit if don't like to use it.

HOW TO COMPILE AND INSTALL
--------------------------

**First run**

```
./autogen.sh
```

And the script will tell you all the dependencies you'll have to install in order to make.
Run the command again and again until you've resolved all the dependencies and can run ./autogen.sh without errors.

**Uninstall current installed synaptics driver from the system**

```
sudo apt-get remove xserver-xorg-input-synaptics
```

**The compile and install**

```
./configure --exec_prefix=/usr 
make
sudo make install
```

Reboot and you're done!

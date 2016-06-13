Intel Graphics
==============

To avoid tearing, put the following in `/etc/X11/xorg.conf.d/20-intel.conf`:

    Section "Device"
      Identifier "Intel Graphics"
      Driver     "intel"
      Option     "AccelMethod" "sna"
      Option     "TearFree"    "true"
    EndSection

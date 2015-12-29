Transmission Icon
=================

By default the scalable icon is selected for Transmission.
To get size-optimised bitmaps:

    $ sudo rm /usr/share/icons/hicolor/apps/transmission.svg
    $ sudo gtk-update-icon-cache -f /usr/share/icons/hicolor

Now the scalable icon will not be considered.

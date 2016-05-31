Avahi Icons
===========

Avahi is a dependency of samba and gnome-shell, so it cannot be removed, but its
hideous and useless icons can be removed from the application menu:

    $ cd /usr/share/applications
    $ sudo rm avahi-discover.desktop bssh.desktop bvnc.desktop

Enjoy a clean application menu.

Guix
====

If Guix fails with the following message on an Ubuntu host in a container:

    the group `guixbuild' specified in `build-users-group' does not exist

Resolve as follows

    apt install nscd
    /etc/init.d/nscd start

After this Guix should work.

More info: https://debbugs.gnu.org/cgi/bugreport.cgi?bug=30298

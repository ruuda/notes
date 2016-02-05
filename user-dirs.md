User Directories
================

By default the Gnome user directories are capitalized. To use lowercase instead:

    $ cd
    $ mv Desktop desktop
    $ mv Downloads download
    $ mv Documents documents
    $ mv Music music
    $ mv Pictures pictures
    $ mv Videos videos
    $ xdg-user-dirs-update --set DESKTOP ~/desktop
    $ xdg-user-dirs-update --set DOWNLOAD ~/downloads
    $ xdg-user-dirs-update --set DOCUMENTS ~/documents
    $ xdg-user-dirs-update --set MUSIC ~/music
    $ xdg-user-dirs-update --set PICTURES ~/pictures
    $ xdg-user-dirs-update --set VIDEOS ~/videos

Also remove useless directories:

    $ rmdir Templates
    $ rmdir Public

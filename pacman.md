Pacman
======

To list explicitly installed leaf packages from the repositories:

    $ pacman -Qnettq

To list installed foreign packages (e.g. from the AUR):

    $ pacman -Qmeq

Flags:

 * `-Q`: query
 * `-d`: list only packages installed as dependency
 * `-e`: list only explicitly installed packages
 * `-m`: list only foreign packages
 * `-n`: list only packages from the repositories
 * `-t`: list only packages not (optionally) depended on by other packages
 * `-tt`: list only packages that are not required by other packages
 * `-q`: print package names only, not formatted name and version

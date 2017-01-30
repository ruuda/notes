Python Shebangs
===============

To replace all `python` shebangs with `python2` shebangs (for example to use
Chromium’s depot_tools on Arch):

    git ls-files | grep '.py$' | xargs sed -i -e '1s:#!/usr/bin/env python:#!/usr/bin/env python2:'

Sed options used:

 * `-i`: update files in-place.
 * `-e`: apply the following script.

Sed syntax used:

 * `1`: match only the first line.
 * `s`: substitute like `s/REGEXP/REPLACEMENT/FLAGS`. An other single character
   can be used in stead of `/`. In this case `:` is used.

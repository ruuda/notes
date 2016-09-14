Scaling Governor
================

Set the scaling governor to "performance" (always max frequency):

    $ echo performance | sudo tee /sys/devices/system/cpu/cpu*/cpufreq/scaling_governor > /dev/null

The "powersave" governor minimizes the frequency instead.

To lock a program to a certain core:

    $ taskset -c 6 ./some-program

This will lock the program to core 6.

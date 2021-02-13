Udev
====

To run `hdparm` when a given disk connects, to set the power management to allow
spindown, drop the following in `/etc/udev/rules.d/01-hdparm.rules`:

    # Set power management to 64/256 (the -B flag), where values from 0-127 allow spindown.
    # Set inactivity timeout for spindown to 24*5 = 120 seconds (-S).
    ACTION=="add", SUBSYSTEM=="block", KERNEL=="sda", RUN+="/usr/bin/hdparm -B 64 -S 24 /dev/sda"

To set the IO queue size when a disk connects, drop the following in
`/etc/udev/rules.d/02-queue.rules`:

    # Set the IO queue depth to 2048.
    ACTION=="add", SUBSYSTEM=="block", KERNEL=="sda", ATTR{queue/nr_requests}="2048"

To confirm that power management works:

    hdparm -C /dev/sda

To confirm that the queue size is set:

    cat /sys/block/sda/queue/nr_requests

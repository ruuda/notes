Listening on Port
=================

To figure out which process is listening on port 5037:

    fuser 5037/tcp

Add `--kill` to also kill that process.

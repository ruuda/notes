Fingerprints
================

To obtain the fingerprints of the server ssh keys:

    $ ssh-keygen -lf /etc/ssh/ssh_host_ecdsa_key.pub
    $ ssh-keygen -lf /etc/ssh/ssh_host_ed25519_key.pub

Options:

 * `-l`: Print fingerprint.
 * `-f`: Filename.

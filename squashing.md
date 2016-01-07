Squashing
=========

To squash all the commits after `onto` up to and including head,
without using an interactive rebase:

    $ git reset --soft onto
    $ git commit

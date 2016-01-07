Rebasing
========

To rebase branch feature2 that was tracking feature1, when feature1 has
been rebased:

    $ git rebase --onto feature1 feature1@{1} feature2

To edit or reorder the first commit in an interactive rebase:

    $ git rebase -i --root

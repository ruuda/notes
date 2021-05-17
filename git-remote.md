Git Remote
==========

To pull over https but push with ssh, edit the Git config (`git config -e`):

    [remote "github"]
      url = https://github.com/ruuda/notes
      pushurl = git@github.com:ruuda/notes

To check out pull requests locally:

    [remote "github"]
      fetch = +refs/pull/*/head:refs/remotes/origin/pull/*

Git Remote
==========

To pull over https but push with ssh, edit the Git config (`git config -e`):

    [remote "github"]
      url = https://github.com/ruud-v-a/notes
      pushurl = git@github.com:ruud-v-a/notes

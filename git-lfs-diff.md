Git LFS Diff
============

Diff files tracked by Git LFS, after they have been committed:

    git difftool --no-prompt --extcmd='/usr/bin/git diff --no-index' c1 c2

This diffs commits `c1` and `c2`. Pass `-- file` to diff only the given file.

Last touched files
==================

To list the files in a Git repository including their last touched time:

    $ git ls-files -z dir | xargs -0n1 -I{} git log -1 --format='%ai {}' {}

Flags:

 * `-z`: make ls-files separate filenames by a null character.
 * `-0`: make xargs read null-separated filenames.
 * `-n1`: make xargs pass at most one filename per process.
 * `I{}`: make xargs replace `{}` with the filename in the command template.

Git log format:

 * `%ai`: author date in pseudo ISO 8601 format.
 * `%aI`: author date in strict ISO 8601 format.
 * `%ci`: committer date in pseudo ISO 8601 format.
 * `%cI`: committer date in strict ISO 8601 format.

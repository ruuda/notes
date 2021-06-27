Nix inodes
==========

Check if your file system ran out of inodes:

    df --inodes

When Nix is using too many, clear up the biggest consumers:

    du --inodes --max-depth 1 /nix/store | \
      awk '{ if ($1 > 2000) { print $2; fflush(stdout); } }' | \
      xargs -n 5 nix-store --delete

Pipeline explained:

 * `du` lists number of inodes and full path for directories under `/nix/store`.
 * With `awk` we filter the ones using more than 2000 inodes, and print only
   the path. Be sure to flush, so deleting can start quickly. `du` can take a
   long time to fully traverse `/nix/store`, and if we need to wait for a buffer
   of output, it takes a long time befoer `xargs` receives anything.
 * Call `nix-store --delete` in batches of 5, because it seems to be somewhat
   slow if we delete many paths at once.

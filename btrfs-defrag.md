Btrfs deframentation
====================

Defragmentation creates new extents, so it destroys sharing through reflinks.
To preserve sharing, only defragment files where none of the extents are shared.

    expr='{
      if ($1 == $2 && $2 > 0 && $3 == "-") {
        fname = "";
        for (i = 4; i < NF; i++) fname = fname $i " ";
        printf "%s%s\0",fname,$NF
      }
    }'
    btrfs filesystem du --raw * | awk "$expr" | xargs -0 btrfs filesystem defragment -vr

Breakdown:

 * List "total", "exclusive", "set shared", "filename" for everything in the
   current directory and below.
 * If total equals exclusive, the file or directory is safe to defragment. In
   that case, output the filename, terminated by a null instead of a newline.
 * Run `btrfs defragment` on every file or directory.

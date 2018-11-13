PDF Splitting
=============

To extract all pages from `in.pdf` into separate pdfs:

    $ pdfseparate in.pdf in-%d.pdf

To extract pages 2 to 4, inclusive:

    $ pdfseparate -f 2 -l 4 in.pdf out.pdf

Flags:

 * `-f`: First page
 * `-l`: Last page

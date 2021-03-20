PDF to PNG
==========

To render a PDF to PNG:

    gs -sDEVICE=png16m -sOutputFile=out%d.png in.pdf

Flags:

 * `-h`: List available devices.
 * `-r`: Set resolution in pixels per inch.

Remarks:

 * Any `%d` in the file name will be substituted by a page number.

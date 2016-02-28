Resizing
========

To resize an image in a linear color space:

    $ convert src.png
        -colorspace LAB
        -filter Lanczos2
        -distort Resize 32x32!
        -colorspace sRGB out.png

Specifying the size:

 * Do not specify height to keep aspect ratio.
 * Specify height to fit into desired size.
 * Add exclamation mark to stretch to desired size.

A few available filters:

 * Triangle: for bilinear interpolation.
 * Cubic: approximates a Gaussian filter with a cubic polynomial.
 * Lanczos, Lanczos2: produce good results in general.
 * Cosine: a single cosine lobe, good for sharp downsampling.

The `-distort` option uses an elliptical weighted averaging function that
samples both dimensions at once, and it does not clamp intermediate values.
The `-resize` option resizes images in two passes (horizontal and vertical),
and it does clamp intermediate values.

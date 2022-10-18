Memes
=====

To create a meme with Imagemagick:

    $ convert officespace.jpg
        -font Impact
        -pointsize 30
        -fill white
        -stroke black
        -strokewidth 2
        -grativy south
        -annotate +0+0 'SO WE "FIXED" THE GLITCH'
        fixedtheglitch.jpg

To obtain the Impact font on Ubuntu, one can install the
`ttf-mscorefonts-installer` package.

To overlay on an animated gif, add `-coalesce` after the loading, before
`-font`, and `-layers optimize` as the final stage. Without this, the text
may drift.

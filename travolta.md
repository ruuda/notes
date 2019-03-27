Travolta Meme
=============

Suppose you had an animated gif of John Travolta with backroung color #fcfefc.
Overlay it on top of a different image as follows:

    $ convert background.png
        -coalesce null: travolta.gif
        -transparent '#fcfefc'
        -gravity center
        -layers composite
        output.gif

The `-transparent` option allows making one particular color transparent.
The `-gravity` option centers Travolta on the background.

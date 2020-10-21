Travolta Meme
=============

Suppose you had an animated gif of John Travolta with backround color #fcfefc.
Overlay it on top of a different image as follows:

    $ convert background.png
        -coalesce null: travolta.gif
        -transparent '#fcfefc'
        -gravity center
        -layers composite
        output.gif

The `-transparent` option allows making one particular color transparent.
The `-gravity` option centers Travolta on the background.

Suppose you wanted to stack 680x400 `anim.gif` below 1360x400 `static.png`:

    $ convert anim.gif
      -coalesce
      -gravity south
      -extent 0x600
      -gravity north
      null: \( static.png -distort Resize 680x \)
      -layers composite
      stacked.gif

Flags:

 * `-gravity`: Put the first image below, the second one on top.
 * `-coalesce`: Merge gif delta frames into full frames.
 * `-extent`: Set the canvas size, 0 to keep the current width.
 * `null:`: Needed to mark the end of the animation.
 * `()`: Apply the distort inside only to this image.
 * `-layers composite`: Compose the animation and static image frame by frame.

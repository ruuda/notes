Video to Gif
============

To convert `video.webm` to `video.gif`:

    $ ffmpeg -i video.webm -vf "fps=15,palettegen" -y palette.png 
    $ ffmpeg -i video.webm -i palette.png -lavfi "fps=15 [x]; [x][1:v] paletteuse" -y video.gif


Film volume compression
=======================

When the dialogue is inaudible, but the action scenes are defening:

    celluloid --mpv-options=--af="acompressor=ratio=4,loudnorm"

For audio filter documentation, see `mpv --af=help`. Other interesting filters
(I haven't tested all of them at this point):

 * `acompressor`: Compressor.
 * `acontrast`:   Dynamic range compressor or expander.
 * `alimiter`:    Look-ahead limiter.
 * `compand`:     Another dynamic range compressor.
 * `dynaudnorm`:  Dynamic audio normalizer.
 * `loudnorm`:    EBU R128 loudness normalization.

List the parameters of specific filters with `mpv --af=filter=help`, although
documentation is needed to clarify their meaning.

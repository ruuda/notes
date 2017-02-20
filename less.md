Less
====

To make less pass through ansi colors, instead of printing escapes:

    $ less -R file

Flags:

 * `-r`, `--raw-control-chars`: display control characters without escaping
 * `-R`, `--RAW-CONTROL-CHARS`: same as `-r`, but only for ansi color escapes

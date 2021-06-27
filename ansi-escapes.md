ANSI Escape Sequences
=====================

Escape sequences:

 * `0x1b, 0x5b` (`ESC, [`) introduces escape sequence.

Color and text style:

 * `m` ends an escape sequence.
 * Reset all: `0`.
 * Bold: `1`, off: `21`.
 * Italic: `3`, off: `23`.
 * Underline: `4`, off: `24`.
 * Foreground color:
   * `30`: Black
   * `31`: Red
   * `32`: Green
   * `33`: Yellow
   * `34`: Blue
   * `35`: Magenta
   * `36`: Cyan
   * `37`: White
   * `39`: Default
   * Any of the above followed by `;1` to make it bright.
 * Background color: foreground color + 10.

Navigation (no closing `m`):

 * Clear line: `K`.
 * Move cursor up `x` lines: `xF`, e.g. `2F`. Shorten to just `F` for one line.

Examples:

 * Turn text red: `\x1b[31m`. Turn off: `\x1b[0m`.
 * Clear the line above: `\x1b[F\x1b[K`.

Ripping CDs
===========

To set up Whipper, a ripper with AccurateRip verification:

    $ whipper drive analyze
    $ whipper drive list

Search for the listed model at http://www.accuraterip.com/driveoffsets.htm.
Suppose that the offset is +102, then insert a popular disc that is likely to
be on AccurateRip, and then:

    $ whipper offset find -o 102

Now rip the disc:

    $ whipper cd rip

Alternatively, rip with Cdparanoia directly (does not verify AccurateRip):

    $ cdparanoia --output-wav --batch

Flags:

 * `--output-wav`: Write files as wav (not raw PCM, not aiff, etc.)
 * `--batch`: Rip all tracks.

This is a collection of console fonts that can be loaded using the OpenBSD
`wsfontload` command. They are common monospace fonts that you may be familiar
with.

Fonts available here:

* Adobe Source Code Pro
* DejaVu Sans Mono
* Fira Code
* Go Mono

Note: these are TTF fonts that have been converted into bitmap format, with
no antialiasing. They can look rather rough around the edges as a result.

## Why?

The default OpenBSD font is a font called "Spleen". All respect given to its
creator Frederic Cambus, I just don't like it.

## Procedure

If you want to do the same thing for your own favorite font:

1. Open TTF font in FontForge.
1. From "Element->Bitmap Strikes Available", add bitmap versions of all font
   characters.
1. "File->Generate Fonts..." and save a set of `.fnt` files containing the
   bitmap strikes.
1. Use Simon Tatham's `dewinfont` to convert the `.fnt` files
   [into .txt format](txt/).
1. Go back to (2) above and fiddle with the pixel heights until characters of
   the actual desired size are generated ("pixel height" in FontForge is not
   the same thing).
1. The `mkfont` script will convert the `.txt` files into the binary format
   expected by `wsfontload`.

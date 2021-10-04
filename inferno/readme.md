This directory does not require actual translations. It contains a pool of
all fonts used by programs that run on top of the Inferno Game Engine.

Inferno based programs select a _best fitting_ font based on language,
requested size and type. Finally, falling back on English versions when no
suitable font is found.

For example, ImgEdit uses 2 fonts at present 10x12 and 8x8. So, if the language
is set to TR, the 1012N-TR.FNT will be used for 10x12 characters. However,
since no smaller size is provided that fits in the 8x8 requirement, the
0808N-EN.FNT will get loaded for that size.

On a side note, ImgEdit uses two font file formats. 08x?? is always saved in
a flat font bitmap file compatible with most programs that can load fonts (like
VFONT and other utilities). For fonts more than 8-bits wide, it uses a new
font file format which will only work in programs that support that format.

If you desire creating/updating fonts, I currently suggest the following order
of importance...

10x12
08x08
08x16

Of much less importance at present. However, when additional higher resolution
video drivers are added, that may change.

12x14
08x20
08x18
08x12
08x14
08x10

Additional sizes can be provided as well. :-)

The N stands for Normal font. I & B would be bold and italic. The - is kinda
a reserved for future use typeface stuff.
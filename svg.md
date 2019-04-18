
# OP-1 SVG

The OP-1 can parse SVG files but its very strict regarding the format. It can
understand most graphics primitives, but they need to be formatted properly.
The limitations make it a challenge to modify the graphics with tools such as
Inkscape. Lots of SVG features are entirely unsupported.


## Supported Elements (non exhaustive list)

 - line

 - polyline
 
 - rect

 - ellipse

 - circle

 - path
 > Only supports a specific formatting of the `d` attribute.
 
 
## Colos

The OP-1 uses the colors in colors.svg for dynamic parts of the graphics.
Static parts of the graphics use the same colors, but they're separately
specified in the individual SVG files.

 
## Fonts

The OP-1 uses the characters in opfont.svg for drawing dynamic texts in the
graphics. Similarly as the colors static texts are written directly into
the SVG files.


## Desiging custom graphics

If and when designing custom GFX for the OP-1 you should use the default colors and 
line widths. Please keep to the original TE OP-1 vibe if you know what I mean.




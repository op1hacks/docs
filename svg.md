
# OP-1 SVG

The OP-1 can parse SVG files but its very strict regarding the format. It can
understand most graphics primitives, but they need to be formatted properly.
The limitations make it a challenge to modify the graphics with tools such as
Inkscape. Lots of SVG features are entirely unsupported.


## Supported Elements (non exhaustive list)

 - svg

 - rect

 - g

 - line

 - path

   - Only supports a specific formatting of the `d` attribute.

   - It seems that line commands only supports a single coordinate pair. That means that `L 10,10 20,20` doesn't work and should instead be written as `L 10,10 L 20,20`. The same logic might apply to other commands too but I haven't verified that yet.

 - polyline

 - circle

 - polygon

 - ellipse

 - defs (?)

 - clipPath (?)

 - use (?)


## Supported attributes

    xmlns, xmlns:xlink,
    version, id, x, y, width, height, viewBox,
    enable-background, space, fill, stroke, d, stroke-width,
    cx, cy, r, x1, y1, x2, y2, stroke-dasharray, display,
    stroke-linecap, points, rx, ry, stroke-linejoin, transform,
    stroke-miterlimit, href, overflow, clip-path, opacity,


## Transformations

Transforms seem to be mostly unsupported, except for the matrix transform
that seems to be used in a few of the graphics. Transforms on groups of
elements don't seem to work at all.


## Decimal precision

The OP-1 crashes if numeric values in SVG files have more than 4 decimals
of precision.


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




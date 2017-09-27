# Renderers

See [Render Techniques](https://processing.org/tutorials/rendering/)

* `JAVA2D` (default)
* `P2D` - OPENGL, can do texture and lighting, unlike `JAVA2D`, and is faster but lower quality
* `P3D` - OPENGL
* `PDF`
* `FX2D` new in version 3 and set to become the new default

The `P2D` renderer is faster than Default but not as high quality. May be slower with stroked shapes (is this just on andriod? but P3D not a problem due to faster stroke tesselation https://github.com/processing/processing-android/issues/203).

> The P3D renderer doesn't support strokeCap() or strokeJoin(), which can lead to ugly results when using strokeWeight().

### Smoothing

Note: The P2D and P3D renderers default to `smooth(2)` (so says the [smooth()](https://processing.org/reference/smooth_.html) docs, but )

In Processing 3 `smooth()` and `noSmooth()` can only be called within setup(), and only called once. Note `smooth()` has been the default since Processing 2. Offscreen surfaces (createGraphics()) inherit from parent sketch but can override before first call to beginDraw().

See https://github.com/processing/processing/issues/3357
and
https://github.com/processing/processing-docs/issues/251
for some confusing things.
It might be worth looking at the code to know for sure.

Smooth can be set to:

* 0: no smoothing
* 1: default for renderer
* 2+:

Java2D:

* 2 = bilinear (a lower mode)
* 3 = bicubic (default)

For OpenGL:

* 2 = 2x anti-aliasing (default)
* 4 = 4x (4 and 8 may now work with all harware) 

Note smooth() == smooth(1)


## OpenGL

Adjust OpenGL renderers using `stroke()` (doesn't this work for default also?) and `hint()`.

### Hints

https://github.com/processing/processing/wiki/Advanced-OpenGL

http://processingjs.org/reference/hint_/

See the section on hint in https://processing.github.io/processing-javadocs/core/processing/core/PGraphics.html

`hint(DISABLE_DEPTH_MASK)`


# Renderers

See [Render Techniques](https://processing.org/tutorials/rendering/)

* `JAVA2D` (default)
* `P2D` - OPENGL, can do texture and lighting, unlike `JAVA2D`, and is faster but lower quality
* `P3D` - OPENGL
* `PDF`
* `FX2D` new in version 3 and set to become the new default


The `P2D` renderer is faster than Default but not as high quality.

> The P3D renderer doesn't support strokeCap() or strokeJoin(), which can lead to ugly results when using strokeWeight().


## OpenGL

Adjust OpenGL renderers using `stroke()` (doesn't this work for default also?) and `hint()`.

### Hints

https://github.com/processing/processing/wiki/Advanced-OpenGL

http://processingjs.org/reference/hint_/

    



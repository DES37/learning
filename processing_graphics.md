Processing Graphics
===================



OPENGL




[smooth(), noSmooth() behavior](https://github.com/processing/processing/issues/3357) Processing Issue.




See public accessors `sketchWidth()`, `sketchSmooth()`, etc.


Rendering Performance

https://www.youtube.com/watch?v=NZG3g0NRR4I


PGraphics
---------

```
PGraphics canvas = createGraphics(200, 200);
canvas.beginDraw();
canvas.rect(0, 0, 100, 100);
canvas.endDraw();
image(canvas, 0, 0);
```

---

### Smooth

Specify smooth levels can be 2, 3, 4, 8. The the default renderer uses _bicubic smoothing_ `smooth(3)` unless otherwise specified. The P2D and P3D renderes default to _2x anti-aliasing_ (`smooth(2)`). The others correspond to 4x and 8x anti-aliasing (double check). Can also choose `noSmooth()`.

When using PGraphics smoothing must be set before call to `beginDraw()`.

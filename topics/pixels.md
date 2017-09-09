# Processing Topics: Pixels

The individual pixels of a PImage can be accessed through its `pixels[]` array, however `loadPixels()` must be called first to populate it. After manipulating it `updatePixels()` must be called. Pixel `x, y` is accessed as `pixels[y*width+x]` (i.e. row-major order, left to right starting at top row) Instead of using the pixels array `get(x, y)` and `set(x, y)` may also be used, but they are slower.

`PApplet` also provides these methods as a means to access the pixels of the display window `PGraphics`.

---

PGraphics? buffer?

images





# Images in Processing

What is the proper strategy for converting from one file format to another, e.g. stripping alpha?

##### Ref

* [PImage (reference)](https://processing.org/reference/PImage.html)
* [PImage (javadoc)](https://processing.github.io/processing-javadocs/core/processing/core/PImage.html)
* [Images and Pixels (tutorial)](https://processing.org/tutorials/pixels/) by Dan Shiffman

## The `PImage` Class

`loadImage()`

`createImage()`
: specify width, height, and format. Use this instead of constructor.

`imageMode()`

`requestImage()`


### `PImage` Fields

`pixels`

`width`

`height`

`format`
: RGB (1), ARGB (2), ALPHA (4)

## `PImage` Methods

An entire image may be manipulated through the images `pixels[]` field, but first the array must be populated using `loadPixels()` and then pushed back to the image with `updatePixels()`.

The color of individual pixels or sections of an image may be read/changed using `get()`/`set()`.

`mask()`

`filter()`

`blend()`

`copy()`

`save()`

Note: `PApplet` also has versions of all of these methods, which would appear to relate to the `PGraphics` object `PApplet.g` (note `PGraphics` is a subclass of `PImage`). Note: `mask()` can't be used on the main drawing surface, while `filter()` and `blend()` can. Not sure about the others.

Also, compare `blend()` with `blendMode()`!



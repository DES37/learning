# Processing Graphics

See [PGraphics javadoc](http://processing.github.io/processing-javadocs/core/processing/core/PGraphics.html)


OPENGL


[smooth(), noSmooth() behavior #3357](https://github.com/processing/processing/issues/3357) Processing Issue.


See public accessors `sketchWidth()`, `sketchSmooth()`, etc.

## `PGraphics` Class

extends PImage!

    PGraphics canvas = createGraphics(200, 200);
    canvas.beginDraw();
    canvas.rect(0, 0, 100, 100);
    canvas.endDraw();
    image(canvas, 0, 0);

#### PGraphics fields of note

    int backgroundColor  // Last background color that was set, zero if an image
    
    int colorMode  // The current colorMode
    float colorModeA  // Max value for alpha set by colorMode
    float colorModeX  // Max value for red (or hue) set by colorMode
    float colorModeY  // Max value for green (or saturation) set by colorMode
    float colorModeZ  // Max value for blue (or value) set by colorMode
    
    int ellipseMode  // The current ellipse mode (read-only)
    
    boolean fill  // true if fill() is enabled, (read-only)
    int fillColor  // fill that was last set (read-only)
    
    int imageMode  // The current image alignment (read-only)
    
    int pixelCount
    
    int rectMode  // The current rect mode (read-only)
    int shapeMode  // The current shape alignment mode (read-only)
    
    int smooth
    
    boolean stroke  // true if stroke() is enabled, (read-only)
    int strokeCap  // Set by strokeCap() (read-only).
    int strokeColor  // stroke that was last set (read-only)
    int strokeJoin  // Set by strokeJoin() (read-only).
    float strokeWeight  // Last value set by strokeWeight() (read-only).
    
    int textAlign  // The current text align (read-only)
    int textAlignY  // The current vertical text alignment (read-only)
    PFont textFont  // The current text font (read-only)
    float textLeading  // The current text leading (read-only)
    int textMode  // The current text mode (read-only)
    float textSize  // The current text size (read-only)
    
    PImage textureImage  // Current image being used as a texture
    int textureMode  // Sets whether texture coordinates passed to vertex() calls will be based on coordinates that are based on the IMAGE or NORMALIZED.
    float textureU  // Current horizontal coordinate for texture, will always be between 0 and 1, even if using textureMode(IMAGE).
    float textureV  // Current vertical coordinate for texture, see above.
    
    boolean tint  // True if tint() is enabled (read-only).
    int tintColor  // tint that was last set (read-only)

Note:

* colorMode: RGB=1, HSB=3

#### PGraphics methods of note

    boolean is2D()  // Return true if this renderer supports 2D drawing.
    boolean is3D()  // Return true if this renderer supports 3D drawing.
    boolean isGL()  // Return true if this renderer does rendering through OpenGL.

PGraphics also has some methods that I came across while working with P3D. But what are they!?

method              | ? 
--------------------|------
`printCamera()`     | ~camera
`printMatrix()`     | ~push/pop/reset/applyMatrix
`printProjection()` | ~camera

---

### Smooth

Specify smooth levels can be 2, 3, 4, 8. The the default renderer uses _bicubic smoothing_ `smooth(3)` unless otherwise specified. The P2D and P3D renderes default to _2x anti-aliasing_ (`smooth(2)`). The others correspond to 4x and 8x anti-aliasing (double check). Can also choose `noSmooth()`.

When using PGraphics smoothing must be set before call to `beginDraw()`.

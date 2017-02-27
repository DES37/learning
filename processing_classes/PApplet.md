# Processing Internals

Nuts and bolts and abstractions and Java interface.

#### Links

- [Processing Javadocs: Core](https://processing.github.io/processing-javadocs/core/)
- [Processing Javadocs: Libraries](https://processing.github.io/processing-javadocs/libraries/)

---

Use processing's `core.jar` to code directly in Java.

Processing sketches are `PApplet` objects.

## PApplet Class

See [PApplet javadoc](http://processing.github.io/processing-javadocs/core/processing/core/PApplet.html)

#### PApplet fields of note

    PGraphics g  // The PGraphics renderer associated with this PApplet
    
    int width
    int height
    int displayWidth
    int displayHeight
    
    float frameRate
    
    int mouseX
    int mouseY
    int pmouseX
    int pmouseY
    
    boolean mousePressed
    int mouseButton
    
    boolean keyPressed
    char key
    int keyCode
    
    int[] pixels  // color datatype
    static int platform



## `PApplet` Class

* [PApplet (javadoc)](https://processing.github.io/processing-javadocs/core/processing/core/PApplet.html)

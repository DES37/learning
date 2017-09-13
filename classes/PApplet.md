# Processing Internals

Nuts and bolts and abstractions and Java interface.

#### Links

- [Processing Javadocs: Core](https://processing.github.io/processing-javadocs/core/)
- [Processing Javadocs: Libraries](https://processing.github.io/processing-javadocs/libraries/)

---

Use processing's `core.jar` to code directly in Java.

Processing sketches are `PApplet` objects.

## `PApplet` Class

* [PApplet (javadoc)](https://processing.github.io/processing-javadocs/core/processing/core/PApplet.html)

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

## PApplet Methods

### PApplet Paths

See [PApplet.java](https://github.com/processing/processing/blob/master/core/src/processing/core/PApplet.java) for more details. Some for internal use only, and many undocumented!

Simply put `sketchPath()` and `savePath()` to get paths, using the latter when there are intermediate paths involved. To create the files use the `sketchFile()` and `saveFile()`.

`sketchPath()` 
: Gets path of sketch and initializes private `sketchPath` field using `calcSketchPath()`. With an argument "Prepend the sketch folder path to the filename (or path) that is passed in. External libraries should use this function to save to the sketch folder." Actually create a File at that path using `sketchFile()`

`savePath()`
: "Like `sketchPath()`, but creates any in-between folders (using `createPath()`) so that things save properly." Actually create a File at that path using `saveFile()`.

`createPath()`
: "Takes a path and creates any in-between folders if they don't already exist." Has String and File versions.

`dataPath()`
: for internal use. Unreliable cross platorm quirks but might return path to data dir. Prefer `sketchPath()`.

`dataFile()`
: "Return a full path to an item in the data folder as a File object."

`sketchOutputPath()` returnes `outputPath` field, so?



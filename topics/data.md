# Data

Usually assets are read from `data` directory, or you can provide an absolute path (what about relative?) or url.

## Listing Paths and Directories

These are new and undocumented and return arrays of the contained files either as String or File. Paths args are given as String or alternatively, in the case of `listFiles()`, as an existing File object.

These functions assume that non-absolute paths are relative to the sketch folder. The `relative` option to `listPaths()` will return an array of relative paths instead of absolute paths.

* `listPaths()`
* `listFiles()`

Params:

    // "relative" -> no effect with the Files version, but important for listPaths
    // "recursive"
    // "extension=js" or "extensions=js|csv|txt" (no dot)
    // "directories" -> only directories
    // "files" -> only files
    // "hidden" -> include hidden files (prefixed with .) disabled by default
    public String[] listPaths(String path, String... options)
    public File[] listFiles(String path, String... options)
    static public File[] listFiles(File base, String... options)

[processing/processing-docs/#460](https://github.com/processing/processing-docs/issues/460) and [processing/processing-docs/#4622](https://github.com/processing/processing/issues/4622)

[directorylist example](https://processing.org/examples/directorylist.html), note not linked from examples page, and this may do things the old way

https://processing.org/discourse/beta/num_1247100666.html
: example may be old

## Etc

Recall methods of Java's File class:

File
 .getAbsolutePath()/.getAbsoluteFile
 .getParent()/.getParentFile()
 .getParent/.getParentFile

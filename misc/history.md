Processing History and Changes
==============================

? IntList, Table?


Processing Version 3
--------------------

`settings()`


https://github.com/processing/processing/wiki/Changes-in-3.0
https://github.com/processing/processing/blob/master/core/README.md


#### No variables in size()

It's no longer possible to use variables in `size()`. Instead set it to anything, then: 

surface.setResizable(true);
surface.setSize(round(random(200, 500)), round(random(200, 500)));

### settings()

The precompiler implicitly moves `size()`, `fullScreen()`, `pixelDensity()`, and `smooth()`
 to `settings()`. If you are using Processing outside of the IDE (e.g. Eclipse) or another IDE then you use a `settings()` function for calling these.



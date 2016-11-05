Shapes in Processing
====================







### `PShape`

> Datatype for storing shapes. Before a shape is used, it must be loaded with the `loadShape()` or created with the `createShape()`. The `shape()` function is used to draw the shape to the display window. Processing can currently load and display SVG (Scalable Vector Graphics) and OBJ shapes. OBJ files can only be opened using the `P3D` renderer. The `loadShape()` function supports SVG files created with Inkscape and Adobe Illustrator. It is not a full SVG implementation, but offers some straightforward support for handling vector data. 

[`Pshape`](https://processing.org/reference/PShape.html) object also has many methods.

##### Loading/Creating shapes

`loadShape`

`createShape`

##### Rendering shapes

`shape`

##### Shape behavior

`shapeMode`


### Shape functions

It's possible and common to create shapes without explicitely createing a `PShape` object, but it's rather pedestrian.

Many (most? all?) of the general shape functions are also available as methods of `PShape`.





### 2D Shapes


### 3D Shapes

### ?

`beginShape`/`endShape`
`vertex` / `curverVertex` / `bezierVertex`


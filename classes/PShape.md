# Processing Shapes

*immediate mode* vs *retained mode*

## `PShape` Class

> Datatype for storing shapes. Before a shape is used, it must be loaded with the `loadShape()` or created with the `createShape()`. The `shape()` function is used to draw the shape to the display window. Processing can currently load and display SVG (Scalable Vector Graphics) and OBJ shapes. OBJ files can only be opened using the `P3D` renderer. The `loadShape()` function supports SVG files created with Inkscape and Adobe Illustrator. It is not a full SVG implementation, but offers some straightforward support for handling vector data. 

[`PShape`](https://processing.org/reference/PShape.html) object also has many methods.

See also [PShape Tutorial](https://processing.org/tutorials/pshape/)

#### Loading/Creating shapes

##### createShape()

1. Create primitive shapes with `createShape()` by giving the kind of shape as the first parameter, followed by the appropriate parameters for that shape.

    `createShape()` parameter  | corresponding primitive function
    ---------------------------|---------------------------------
    `ELLIPSE`                  | `ellipse()`
    `RECT`                     | `rect()`
    `ARC`                      | `arc()`
    `TRIANGLE`                 | `triangle()`
    `SPHERE`                   | `sphere()`
    `BOX`                      | `box()`
    `QUAD`                     | `quad()`
    `LINE`                     | `line()`

2. Create custom PShapes by calling `createShape()` without parameters, then enclose vertices between `beginShape()` and `endShape()`.
    1. Create any irregular polygon by specifying vertices with `vertex()` (call `beginShape()` with no parameters).
    2. Create curves using`curveVertex()` and `bezierVertex()` (call `beginShape()` with no parameters).
    3. Create complex shapes by specifying a parameter to `beginShape()` and specifying coordinates with `vertex()`.
    
    beginShape()   ||
    ---------------|---
    default        | irregular polygon
    POINTS         |
    LINES          |
    TRIANGLES      |
    TRIANGLE_FAN   |
    TRIANGLE_STRIP |
    QUADS          |
    QUAD_STRIP     |
    
    * Can also create negative shapes with `beginContour()/endContour()`.
    * Note: review using texture() here and maybe? elsewhere
    * Note: Per-vertex stroke and fill are supported by the `P2D` and `P3D` renderers. Remember to use `setStroke()` and `setFill()` for PShape objects.

3. Group PShape objects together by using `createShape(GROUP)` and adding shapes with `addChild()`.

Ref: [`createShape()`](https://processing.org/reference/createShape_.html)

##### loadShape()

Loads SVG and OBJ files

Ref: [`loadShape()`](https://processing.org/reference/loadShape_.html)

#### Rendering shapes

`shape()`

#### Shape behavior

`shapeMode()`

## Shape functions

It's possible and common to create shapes without explicitly creating a `PShape` object, but it's rather pedestrian.

Many (most? all?) of the general shape functions are also available as methods of `PShape`.

## 2D Shapes

## 3D Shapes

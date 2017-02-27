Coordinate Systems
==================


Processing's coordinate system positions the origin in the upper-left corner, the *x* axis increases to the right, the *y* axis increases downward (Processing's 3D coordinate system is *left-handed*, with the *z* axis pointing outward toward the viewer.

Note: To test handedness the thumb is x, index finger is y, and middle/rest are z.


## Transformation and Pixels

Unless the coordinate system is scaled, any coordinates specified in non-integer values are effectively the same as  if the `floor()` were taken. Note: `floor()` calculates the nearest int less than or equal, vs `int()` which chops the decimal value and results in the near nearest int closest to zero. There is thus no advantage to drawing fractional pixels.

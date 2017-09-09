# Error Handling

## Try Blocks

In catch block it might be useful to:

    e.printStackTrace();  // the only useful output from a Java Throwable
    exit();  // cause sketch to exit after draw() completes
    return;  // may be useful to return from a function

Note `Exception` is the generic catchall name.


### Refs

* https://processing.org/reference/try.html
* https://processing.org/reference/catch.html
* https://docs.oracle.com/javase/tutorial/essential/exceptions/try.html
* https://docs.oracle.com/javase/tutorial/essential/exceptions/catch.html


## Etc

testing ==null is a valid way to test for uninitialized objects.

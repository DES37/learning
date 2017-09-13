# Error Handling

## Try Blocks

try
[processing](https://processing.org/reference/try.html)
[java](https://docs.oracle.com/javase/tutorial/essential/exceptions/try.html)

catch
[processing](https://processing.org/reference/catch.html)
[java](https://docs.oracle.com/javase/tutorial/essential/exceptions/catch.html)

In catch block it might be useful to:

    e.printStackTrace();  // the only useful output from a Java Throwable
    exit();  // cause sketch to exit after draw() completes
    return;  // may be useful to return from a function

Note `Exception` is the generic catchall name.


### Refs

* [Lesson: Exceptions](https://docs.oracle.com/javase/tutorial/essential/exceptions/index.html)


## Etc

testing ==null is a valid way to test for uninitialized objects.

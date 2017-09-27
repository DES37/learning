# Threads in Processing

[`thread()`](https://processing.org/reference/thread_.html)

* [Lesson: Concurrency](https://docs.oracle.com/javase/tutorial/essential/concurrency/)

## Java Threads

1. Implement [`Runnable`](https://docs.oracle.com/javase/8/docs/api/java/lang/Runnable.html) interface, namely a `run()` method (more general)
2. Subclass [`Thread`](https://docs.oracle.com/javase/8/docs/api/java/lang/Thread.html), which itself implements `Runnable` (easier to use)

In both cases you implement a `run()` method.

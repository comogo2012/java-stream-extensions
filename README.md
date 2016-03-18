# Java Stream Extensions

One of the best features coming out of [Java 1.8](http://docs.oracle.com/javase/8/docs/api/) has to be its new Streaming framework coupled with the lamda expressions. These go a long way toward making Java a more functional language, although it's still
not [Scala](http://www.scala-lang.org).

Streams allow the developer to chain together operations affecting the entire bulk of elements from some collection or other source without having to include the procedural steps of iterating through each item. This is a key feature as it allows the Java compiler and JVM to determine the best strategy for iterating through items and takes it out of the hands of the developer.  Plus the code is prettier and cleaner.

An example taken from the [Stream JavaDocs](http://docs.oracle.com/javase/8/docs/api/java/util/stream/package-summary.html), you will be confronted with certain limitations. 

```

int sum = widgets.stream()
                      .filter(b -> b.getColor() == RED)
                      .mapToInt(b -> b.getWeight())
                      .sum();

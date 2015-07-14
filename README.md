# SimpleLanguage

A simple language built using Truffle for the GraalVM.

This repository is licensed under the permissive UPL licence. Fork it to begin
your own Truffle language.

There are two branches - `master` which is compatible with the latest release of
GraalVM, and `latest` which is compatible with the development version of
GraalVM, which you will have to build yourself.

## Compiling

    mvn package

## Testing

    mvn test

## Running

    bin/sl HelloWorld.sl

## Running With Graal

Build GraalVM https://wiki.openjdk.java.net/display/Graal/Instructions.

Then run:

    JAVACMD=../basic-graal/jdk1.8.0_31/product/bin/java bin/sl HelloWorld.sl

You may have to adjust the path `../basic-graal/jdk1.8.0_31/product/bin/java`
for your system.

## Options

To pass options to the JVM, prefix with `-J`. For example, `-J-Xmx1G`.

## Documentation

SimpleLanguage is heavily documented to explain the how and why of writing a
Truffle language. A good way to read this documentation is to generate HTML of
the JavaDoc comments and read that, and then read the source alongside the
comments.

    mvn javadoc:javadoc

Note that this may appear to fail with Java 8, but the files are still
accessible at `target/site/apidocs/index.html`.

Start with the `SLLanguage` class.

You should also have access to the [Truffle documentation
itself](http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/all/index.html).

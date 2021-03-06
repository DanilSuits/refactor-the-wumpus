# Refactor the Wumpus

## Goal

Transform the provided implementation of _Hunt the Wumpus_ into a healthy,
maintainable code base.

## Overview

Legacy code is hard.

In this particular example, I've taken the original BASIC implementation
of Hunt the Wumpus, and transcribed it as accurately as I was able to
Java.

There's nothing deliberately tricky about the translation -- the code is
not particularly well structured, and the naming conventions do not
prioritize communicating intent.  So it goes.

On the other hand, the implementation is small; it is single threaded,
with no external dependencies.

## Maven Notes

The regression tests were segregated into a special profile, which in
this stack is `disabled` by default.  They can be run during the
test cycle by enabling the `guru-checks-output` profile.

```bash
mvn -P guru-checks-output clean test
```

To run the program from the command line:

```bash
mvn compile exec:java
```
 

## Links

[Original Source Code][1]

[1]: https://github.com/mad4j/Hunt-the-Wumpus/blob/master/references/Best%20of%20Creative%20Computing%20Vol%201/wumpus.bas

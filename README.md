# Lab 1.9-1.11 — Method Signatures, Class Methods, and the Math Class

Eight short methods in `MathLab.java`, most of them one line. The instructions
for each one are in the comment block directly above the method, so read them
there — this page is just the map.

Plan on 30 to 45 minutes.

## What you will practice

- Reading a header and writing the signature: the method name plus the ordered
  list of parameter types, and nothing else.
- Telling a parameter from an argument, and matching arguments by position.
- Calling a `void` method as a statement, and a non-void one as part of an
  expression.
- Writing two overloaded methods: one name, two different parameter lists.
- Calling a class method as `ClassName.methodName(arguments)`, and knowing when
  the class name may be left off.
- Using `Math.abs`, `Math.sqrt`, `Math.pow` and `Math.random`, and knowing what
  type each one hands back.

## Getting started

1. Open this folder in your editor.
1. Open `src/main/java/MathLab.java`. That is the only file you change.
1. Work down the file. Each part is marked with a comment that starts with
   `TODO`; replace the placeholder line under it with your own code.

To run your program and see your output:

```sh
mvn -q compile exec:java
```

Your teacher will run a separate set of tests on your work when you turn it in.

## The parts

| Part | Method | What it is about |
| --- | --- | --- |
| 1 | `totalMinutes(int, int)` | parameters and argument order |
| 2 | `totalSeconds(int, int)` | calling a method you wrote |
| 3 | `printLabel(String, int)` | a `void` method prints, it does not return |
| 4a | `distanceFromZero(int)` | `Math.abs` on an `int` |
| 4b | `distanceFromZero(double)` | the same name, a `double` parameter |
| 5 | `hypotenuse(double, double)` | `Math.sqrt` with a nested expression |
| 6 | `powerOf(int, int)` | `Math.pow` returns a `double` |
| 7 | `rollInRange(int, int)` | `Math.random` scaled into a range |

## Before you turn it in

- [ ] Every `TODO` comment has been replaced with real code.
- [ ] `mvn -q compile exec:java` runs without errors.
- [ ] Part 3 prints exactly one line, in the form `"Pencils: 12"`, and no other
      part prints anything.
- [ ] Both `distanceFromZero` methods are still in the file. They share a name
      on purpose, and deleting either one counts as renaming it.
- [ ] Part 7 includes both ends of the range. Substitute `0.0` for
      `Math.random()` and check the smallest value, then a value just under
      `1.0` and check the largest.
- [ ] You did not rename any method, change any parameter list, or change any
      return type. The grader compiles against those exact signatures, so a
      rename means a zero even if your logic is perfect.
- [ ] You may change `main` however you like. It is not graded.

## Optional extension, not graded

Add this to `main` and run the program half a dozen times:

```java
System.out.println((int) Math.random() * 6 + 1);
System.out.println((int) (Math.random() * 6) + 1);
```

One of those two lines prints the same number every single time. Write one
sentence saying which one and why.

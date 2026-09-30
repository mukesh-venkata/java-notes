<a name="top"></a>

# ▶️ 3. Running a Program from the Command Line

> **Core idea:** Arguments are written after the class name when launching the Java program.

## Basic Command

~~~text
java ClassName argument1 argument2 ...
~~~

For example:

~~~text
java HelloWorld Java
~~~

Here:
- HelloWorld → class name
- Java → first command-line argument

## Multiple Arguments

~~~text
java HelloWorld Java 27 Developer
~~~

The values are mapped by position:

~~~text
args[0] → "Java"
args[1] → "27"
args[2] → "Developer"
~~~

## Execution Flow

~~~text
Command line
     ↓
java ClassName arg1 arg2 arg3
     ↓
JVM starts the program
     ↓
main(String[] args)
     ↓
args[0], args[1], args[2]...
~~~

## Program Name Is Not an Argument

In:

~~~text
java HelloWorld Java 27
~~~

HelloWorld is the class name used to launch the program.

The command-line arguments are Java and 27.

Therefore:

~~~text
args[0] = "Java"
args[1] = "27"
~~~

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. Where are command-line arguments written?</summary>
<br>

After the class name in the Java launch command.

</details>

<details>
<summary>Q2. Is the class name stored in args[0]?</summary>
<br>

No. args[0] contains the first supplied argument after the class name.

</details>

<details>
<summary>Q3. How are multiple arguments distinguished?</summary>
<br>

They are separated according to the command-line parsing rules of the environment; commonly whitespace separates arguments unless quoting/escaping rules group text.

</details>
## Related Notes

- [Basics →](01-command-line-arguments-basics.md)
- [args Array →](02-args-array-and-accessing-arguments.md)
- [Converting Arguments →](04-converting-command-line-arguments.md)
- [Quick Revision →](05-command-line-arguments-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

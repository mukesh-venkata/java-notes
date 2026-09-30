<a name="top"></a>

# 🖥️ 1. Command-Line Arguments — Basics

> **Core idea:** Command-line arguments are values supplied when a Java program is started from the command line.

## What Are Command-Line Arguments?

Command-line arguments are values passed to a Java program when the program starts.

The main method receives them through:

~~~java
public static void main(String[] args) {
}
~~~

Here, args is a String array.

## Basic Example

~~~java
public static void main(String[] args) {
    if (args.length > 0) {
        System.out.println(args[0]);
    } else {
        System.out.println("No arguments provided");
    }
}
~~~

The values supplied after the class name are placed into args.

## Why Use Command-Line Arguments?

They allow input to be supplied without changing the source code.

For example:

~~~text
java HelloWorld Java
java HelloWorld Python
java HelloWorld Kotlin
~~~

## Key Points

- args is a String array.
- Command-line arguments are received as Strings.
- args.length gives the number of supplied arguments.
- args[0] represents the first argument.
- If no arguments are supplied, args.length is 0.

## Interview Questions

### Q1. What are command-line arguments?
Values supplied to a Java program when it is started from the command line.

### Q2. Where are command-line arguments received?
In the String[] args parameter of main().

### Q3. What is the type of args?
String[].

### Q4. What does args.length represent?
The number of command-line arguments supplied.

## Related Notes

- [args Array & Accessing Arguments →](02-args-array-and-accessing-arguments.md)
- [Running from Command Line →](03-running-from-command-line.md)
- [Converting Arguments →](04-converting-command-line-arguments.md)
- [Quick Revision →](05-command-line-arguments-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

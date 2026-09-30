<a name="top"></a>

# 🧩 2. args Array & Accessing Arguments

> **Core idea:** args is a String array, so each command-line argument can be accessed using an index.

## args Is a String Array

In:

~~~java
public static void main(String[] args) {
}
~~~

args is a reference to a String[].

## First Argument

~~~java
System.out.println(args[0]);
~~~

args[0] is the first command-line argument.

## Multiple Arguments

Suppose the program is started with:

~~~text
java HelloWorld Java 27 Developer
~~~

| Index | Value |
|---:|---|
| args[0] | "Java" |
| args[1] | "27" |
| args[2] | "Developer" |

Notice that "27" is still a String at this stage.

## args.length

Use args.length to determine how many arguments were supplied.

For the example above, the result is 3.

## Avoid Invalid Index Access

If no arguments are supplied:

~~~text
java HelloWorld
~~~

then args.length is 0.

So this is unsafe:

~~~java
System.out.println(args[0]); // ❌ if no argument was supplied
~~~

Check first:

~~~java
if (args.length > 0) {
    System.out.println(args[0]);
}
~~~

## Index Pattern

~~~text
Arguments:
Java   27   Developer
 ↓      ↓       ↓
 0      1       2

args[0] → first
args[1] → second
args[2] → third
~~~

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What is args?</summary>
<br>

A String array containing the command-line arguments passed to the program.

</details>

<details>
<summary>2. How do you access the first argument?</summary>
<br>

args[0].

</details>

<details>
<summary>3. How do you count arguments?</summary>
<br>

args.length.

</details>

<details>
<summary>4. What happens if args[0] is accessed when there are no arguments?</summary>
<br>

ArrayIndexOutOfBoundsException occurs.

</details>
## Related Notes

- [Basics →](01-command-line-arguments-basics.md)
- [Running from Command Line →](03-running-from-command-line.md)
- [Converting Arguments →](04-converting-command-line-arguments.md)
- [Quick Revision →](05-command-line-arguments-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

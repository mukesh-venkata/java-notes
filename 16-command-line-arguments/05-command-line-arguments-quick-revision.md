<a name="top"></a>

# ⚡ 5. Command-Line Arguments — Quick Revision

> **30-second revision:** Values supplied when starting a Java program are received by main() through the String[] args parameter.

## Core Rules

| Concept | Remember |
|---|---|
| Received in | String[] args |
| First argument | args[0] |
| Second argument | args[1] |
| Number of arguments | args.length |
| Argument type | String |
| Numeric conversion | Use parsing methods |
| No arguments | args.length == 0 |

## Example

~~~text
java HelloWorld Java 27
~~~

Result:

~~~text
args[0] → "Java"
args[1] → "27"
args.length → 2
~~~

"27" is a String until converted.

## Conversion

~~~java
int value = Integer.parseInt(args[1]);
~~~

## Safety Check

Before accessing an index, make sure that the required argument exists:

~~~java
if (args.length > 0) {
    System.out.println(args[0]);
}
~~~

## Memory Trick

> **args = String[]**  
> **index = argument**  
> **length = count**  
> **parse = convert**

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What is args?</summary>
<br>

A String array containing command-line arguments.

</details>

<details>
<summary>2. Where is the first argument stored?</summary>
<br>

args[0].

</details>

<details>
<summary>3. How many arguments were supplied?</summary>
<br>

args.length.

</details>

<details>
<summary>4. Are numeric arguments automatically integers?</summary>
<br>

No. They arrive as Strings.

</details>

<details>
<summary>5. How do you convert 27 to an int?</summary>
<br>

Use Integer.parseInt("27").

</details>

<details>
<summary>6. What happens when an invalid index is accessed?</summary>
<br>

ArrayIndexOutOfBoundsException.

</details>

<details>
<summary>7. What happens when invalid numeric text is parsed as an integer?</summary>
<br>

NumberFormatException.

</details>
## Related Notes

- [Basics →](01-command-line-arguments-basics.md)
- [args Array →](02-args-array-and-accessing-arguments.md)
- [Running from Command Line →](03-running-from-command-line.md)
- [Converting Arguments →](04-converting-command-line-arguments.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

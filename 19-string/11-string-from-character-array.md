<a name="top"></a>

# 🔤 11. Creating a String from a Character Array

> **Core idea:** A `char[]` can be converted into a String using a String constructor.

## 🧠 Basic Example

```java
char[] chars = {'J', 'a', 'v', 'a'};

String s = new String(chars);

System.out.println(s);
```

Output:

```text
Java
```

The constructor creates a String whose characters come from the array.

## 🔄 Flow

```text
char[]
  ↓
{'J','a','v','a'}
  ↓
new String(chars)
  ↓
"Java"
```

## 📌 Why Is This Useful?

It is useful when text is already available as characters and a String value is required.

## 🔎 Other String-Producing Operations

Strings can also be produced by operations that return String values, for example:

- `substring()`
- `concat()`
- `toString()`

These are not separate fundamental object-creation mechanisms in the same sense as the String constructor, but they can produce new String results.

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. Can a char array be converted to String?</summary>
<br>

Yes, for example by using new String(char[]).

</details>

<details>
<summary>Q2. What does new String(chars) produce?</summary>
<br>

It produces a String containing the characters represented by the array.

</details>

<details>
<summary>Q3. Are substring() and concat() constructors?</summary>
<br>

No. They are String methods that can return String results; they are not constructors.

</details>
## 🔗 Related Notes

- [Creating String Objects Overview →](08-creating-string-objects-overview.md)
- [new Operator →](10-string-using-new-operator.md)
- [Memory & Storage →](12-string-memory-and-storage.md)
- [Quick Revision →](14-string-object-creation-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

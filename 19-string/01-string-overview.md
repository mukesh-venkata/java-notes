<a name="top"></a>

# 🔤 1. String — Overview

> **Core idea:** **String** is a final class in **java.lang** whose objects are immutable.

## 🧠 String Class

The Java **String** class is declared as:

~~~java
public final class String
~~~

It belongs to:

~~~text
java.lang.String
~~~

Because **java.lang** is automatically available, an explicit import is normally unnecessary.

## 📌 Important Characteristics

- String is a class.
- It is declared final.
- It belongs to java.lang.
- String objects are immutable.
- String provides many methods for text processing.

## 🔒 Why Is String final?

Making String final prevents subclasses from changing its behavior. This helps keep the behavior of this fundamental Java type consistent.

## 🧩 String Objects

~~~java
String name = "Java";
~~~

Here:

- name is a reference variable.
- "Java" is a String value/object.
- The reference points to that String.

## 🎯 Interview Questions & Answers

> **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Is String a class?</summary>
<br>

Yes.

</details>

<details>
<summary>Is String final?</summary>
<br>

Yes.

</details>

<details>
<summary>Which package contains String?</summary>
<br>

java.lang.

</details>

<details>
<summary>Is String mutable?</summary>
<br>

No. String objects are immutable.

</details>

## 🔗 Related Notes

- [String Immutability →](02-string-immutability.md)
- [String References & Garbage Collection →](03-string-reference-and-garbage-collection.md)
- [StringBuffer →](04-stringbuffer.md)
- [StringBuilder →](05-stringbuilder.md)
- [String vs StringBuffer vs StringBuilder →](06-string-vs-stringbuffer-vs-stringbuilder.md)
- [Quick Revision →](07-string-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

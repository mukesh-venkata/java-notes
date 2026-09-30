<a name="top"></a>

# 🔒 2. String Immutability

> **Core idea:** Once a String object is created, its contents cannot be changed.

## 🧠 What Does Immutable Mean?

An immutable object cannot have its state changed after creation.

~~~java
String s = "Java";
~~~

The contents of the existing String object cannot be modified.

## 🔍 concat() Example

~~~java
String s = "Java";

s.concat(" Programming");

System.out.println(s);
~~~

Output:

~~~text
Java
~~~

Why? **concat()** creates a new String containing the combined text. It does not modify the original String object.

Conceptually:

~~~text
Before:
s ─────→ "Java"

After s.concat(" Programming"):
s ─────→ "Java"
          "Java Programming" ← new object, result not assigned
~~~

## ✅ Correct Way

~~~java
String s = "Java";

s = s.concat(" Programming");

System.out.println(s);
~~~

Output:

~~~text
Java Programming
~~~

## 📌 General Rule

Many String operations return a new String instead of modifying the existing object.

~~~java
String s = "java";

String upper = s.toUpperCase();

System.out.println(s);     // java
System.out.println(upper); // JAVA
~~~

## 🧠 Memory Trick

> **String cannot change itself; operations create a new String.**

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. Why is String immutable?</summary>
<br>

Because String objects cannot change after creation; this supports safe sharing, String Pool reuse, and predictable behavior.

</details>

<details>
<summary>2. Does concat() modify the original String?</summary>
<br>

No. concat() returns a new String containing the combined content.

</details>

<details>
<summary>3. How do you keep the concatenated result?</summary>
<br>

Assign the returned String to a reference, for example s = s.concat("Java").

</details>
## 🔗 Related Notes

- [String Overview →](01-string-overview.md)
- [References & Garbage Collection →](03-string-reference-and-garbage-collection.md)
- [StringBuffer →](04-stringbuffer.md)
- [StringBuilder →](05-stringbuilder.md)
- [Quick Revision →](07-string-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

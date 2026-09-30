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

## 🎯 Interview Questions

1. Why is String immutable?
2. Does concat() modify the original String?
3. How do you keep the concatenated result?

## 🔗 Related Notes

- [String Overview →](01-string-overview.md)
- [References & Garbage Collection →](03-string-reference-and-garbage-collection.md)
- [StringBuffer →](04-stringbuffer.md)
- [StringBuilder →](05-stringbuilder.md)
- [Quick Revision →](07-string-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

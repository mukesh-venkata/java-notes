<a name="top"></a>

# 🧵 4. StringBuffer

> **Core idea:** StringBuffer is a mutable character sequence whose methods are synchronized.

## 🧠 What Is StringBuffer?

StringBuffer is mutable, so its character sequence can be changed.

~~~java
StringBuffer buffer = new StringBuffer("Java");

buffer.append(" Programming");

System.out.println(buffer);
~~~

Output:

~~~text
Java Programming
~~~

## 🔒 Thread Safety

StringBuffer's methods are synchronized. This provides thread-safety characteristics when the same StringBuffer is accessed concurrently through its synchronized methods.

## 📌 Characteristics

- Mutable
- Synchronized methods
- Useful when synchronized mutable text operations are relevant
- Typically less performant than StringBuilder for ordinary single-threaded use because of synchronization overhead

## 🔄 Modification Model

~~~text
String
  ↓
Immutable
  ↓
Modification → new String

StringBuffer
  ↓
Mutable + synchronized
  ↓
Modification → same buffer
~~~

## 🎯 Interview Questions & Answers

> **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Is StringBuffer mutable?</summary>
<br>

Yes

</details>

<details>
<summary>Is StringBuffer synchronized?</summary>
<br>

Yes

</details>

<details>
<summary>StringBuffer vs StringBuilder?</summary>
<br>

StringBuffer is synchronized; StringBuilder is not.

</details>

## 🔗 Related Notes

- [String Overview →](01-string-overview.md)
- [String Immutability →](02-string-immutability.md)
- [StringBuilder →](05-stringbuilder.md)
- [Comparison →](06-string-vs-stringbuffer-vs-stringbuilder.md)
- [Quick Revision →](07-string-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

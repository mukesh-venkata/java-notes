<a name="top"></a>

# ⚡ 7. String — Quick Revision

> **30-second revision:** String is immutable; StringBuffer and StringBuilder are mutable alternatives with different synchronization characteristics.

## 🧠 Master Table

| Class | Mutable? | Synchronization | Typical use |
|---|---|---|---|
| String | ❌ | Not applicable | Immutable text |
| StringBuffer | ✅ | Synchronized | Mutable text when synchronized methods are relevant |
| StringBuilder | ✅ | Not synchronized | Mutable text in typical single-threaded use |

## 🔑 Key Rules

- String is public final class String.
- String belongs to java.lang.
- java.lang is automatically available.
- String objects are immutable.
- String operations such as concat() return a new String when a changed value is needed.
- Reassignment changes which object a reference points to; it does not mutate the original String.
- An object is eligible for GC when it is no longer reachable.
- StringBuffer is mutable and synchronized.
- StringBuilder is mutable and not synchronized.
- StringBuilder is commonly preferred for ordinary single-threaded string building.

## 🧠 Memory Trick

~~~text
String       → Immutable
StringBuffer → Mutable + Synchronized
StringBuilder→ Mutable + No synchronization
~~~

## 🎯 Interview Questions & Answers

> **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Why is String immutable?</summary>
<br>

`String` objects cannot be changed after creation. This supports safe sharing, String Pool reuse, and predictable behavior.

</details>

<details>
<summary>Is String final?</summary>
<br>

Yes. `String` is a `final` class.

</details>

<details>
<summary>Which package contains String?</summary>
<br>

`java.lang`.

</details>

<details>
<summary>What happens when concat() is called without assigning its result?</summary>
<br>

A new String is returned, but the original reference is unchanged if the result is not stored.

</details>

<details>
<summary>When does an old String become eligible for garbage collection?</summary>
<br>

When no live reference can reach that String object. Eligibility does not mean collection happens immediately.

</details>

<details>
<summary>What is the difference between StringBuffer and StringBuilder?</summary>
<br>

`StringBuffer` is mutable and synchronized; `StringBuilder` is mutable and not synchronized.

</details>

<details>
<summary>Which one is synchronized?</summary>
<br>

`StringBuffer`.

</details>

<details>
<summary>Why is StringBuilder commonly used in single-threaded code?</summary>
<br>

`StringBuilder` avoids synchronization overhead and is commonly used when thread-safe mutation is not required.

</details>

## 🔗 Related Notes

- [String Overview →](01-string-overview.md)
- [String Immutability →](02-string-immutability.md)
- [String References & Garbage Collection →](03-string-reference-and-garbage-collection.md)
- [StringBuffer →](04-stringbuffer.md)
- [StringBuilder →](05-stringbuilder.md)
- [Comparison →](06-string-vs-stringbuffer-vs-stringbuilder.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

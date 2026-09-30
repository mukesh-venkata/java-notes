<a name="top"></a>

# ♻️ 3. String References & Garbage Collection

> **Core idea:** An object becomes eligible for garbage collection when it is no longer reachable.

## 🔗 Reference Reassignment

~~~java
String s = "Java";
s = s.concat(" Programming");
~~~

Conceptually:

~~~text
Before:
s ─────→ "Java"

After reassignment:
s ─────→ "Java Programming"
~~~

The old String object may become eligible for garbage collection **if no other reachable reference points to it**.

## 🧠 Reachability Matters

~~~java
String first = "Java";
String second = first;

first = "Python";
~~~

The original String is still reachable through second:

~~~text
second ─────→ "Java"
first  ─────→ "Python"
~~~

So the old object is not eligible merely because first changed.

## 📌 Important Rule

> **Garbage-collection eligibility depends on reachability, not simply on reassignment.**

## ⚠️ GC Timing

Eligible for garbage collection does **not** mean the object is immediately collected. The JVM determines when garbage collection occurs.

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. When does a String object become eligible for GC?</summary>
<br>

When no live reference can reach that String object. A pooled literal can remain reachable through the String Pool.

</details>

<details>
<summary>2. Does reassignment always make the old String eligible?</summary>
<br>

No. It makes the old object eligible only if no other live reference can reach it.

</details>

<details>
<summary>3. Does eligible for GC mean immediately collected?</summary>
<br>

No. It only means the object is available for collection; the JVM decides when or whether to perform garbage collection.

</details>
## 🔗 Related Notes

- [String Overview →](01-string-overview.md)
- [String Immutability →](02-string-immutability.md)
- [StringBuffer →](04-stringbuffer.md)
- [StringBuilder →](05-stringbuilder.md)
- [Quick Revision →](07-string-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

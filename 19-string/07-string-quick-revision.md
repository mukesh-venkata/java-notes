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

## 🎯 Interview Questions

1. Why is String immutable?
2. Is String final?
3. Which package contains String?
4. What happens when concat() is called without assigning its result?
5. When does an old String become eligible for garbage collection?
6. What is the difference between StringBuffer and StringBuilder?
7. Which one is synchronized?
8. Why is StringBuilder commonly used in single-threaded code?

## 🔗 Related Notes

- [String Overview →](01-string-overview.md)
- [String Immutability →](02-string-immutability.md)
- [String References & Garbage Collection →](03-string-reference-and-garbage-collection.md)
- [StringBuffer →](04-stringbuffer.md)
- [StringBuilder →](05-stringbuilder.md)
- [Comparison →](06-string-vs-stringbuffer-vs-stringbuilder.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

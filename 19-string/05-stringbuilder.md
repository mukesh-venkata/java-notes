<a name="top"></a>

# 🛠️ 5. StringBuilder

> **Core idea:** StringBuilder is a mutable character sequence that does not provide synchronization.

## 🧠 What Is StringBuilder?

~~~java
StringBuilder builder = new StringBuilder("Java");

builder.append(" Programming");

System.out.println(builder);
~~~

Output:

~~~text
Java Programming
~~~

## 🚀 Performance

StringBuilder is not synchronized. Because it avoids synchronization overhead, it is generally preferred over StringBuffer for typical single-threaded string-building tasks.

## 📌 Characteristics

- Mutable
- Not synchronized
- Not intended as a thread-safe replacement for StringBuffer
- Typically faster than StringBuffer in ordinary single-threaded use

## 🔄 Modification Model

~~~text
StringBuilder
  ↓
Mutable + not synchronized
  ↓
Modification → same builder
~~~

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. Is StringBuilder mutable?</summary>
<br>

**Yes.** Its character sequence can be modified.

</details>

<details>
<summary>2. Is StringBuilder synchronized?</summary>
<br>

**No.** StringBuilder does not provide synchronization for its operations.

</details>

<details>
<summary>3. Why is it commonly faster than StringBuffer?</summary>
<br>

It normally avoids synchronization overhead, making it suitable when thread-safe mutation is not required.

</details>
## 🔗 Related Notes

- [String Overview →](01-string-overview.md)
- [String Immutability →](02-string-immutability.md)
- [StringBuffer →](04-stringbuffer.md)
- [Comparison →](06-string-vs-stringbuffer-vs-stringbuilder.md)
- [Quick Revision →](07-string-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

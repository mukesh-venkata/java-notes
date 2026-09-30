<a name="top"></a>

# ⚡ 14. Creating String Objects — Quick Revision

> **30-second revision:** String literals use the String Pool; `new String(...)` creates an additional String object; `intern()` returns the canonical pooled String.

## 🧠 Master Table

| Approach | Example | Main result |
|---|---|---|
| Literal | `String s = "Java";` | Interned String |
| new | `new String("Java")` | New String object |
| char[] | `new String(chars)` | New String from characters |
| intern() | `s.intern()` | Canonical pooled String |

## 🔑 Key Rules

- Identical String literals can share the same pooled String.
- `==` compares references.
- `equals()` compares String contents.
- `new String(...)` creates a distinct String object.
- A literal used as an argument to `new String(...)` is still an interned literal.
- `new String(char[])` creates a String from character data.
- `intern()` returns the canonical pooled String.
- `intern()` does not simply move a heap String object into the pool.
- String Pool management is JVM-implementation detail; use the conceptual pooled/canonical model for learning.

## 🧠 Memory Trick

```text
Literal → Pool
new     → New object
char[]   → String
intern() → Pool reference
```

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. Where are String literals interned?</summary>
<br>

In the String Pool.

</details>

<details>
<summary>2. Why can two identical literals have the same reference?</summary>
<br>

The same canonical pooled String can be reused.

</details>

<details>
<summary>3. What does <code>new String("Java")</code> create?</summary>
<br>

A new String object.

</details>

<details>
<summary>4. Why can two new String() objects have == false?</summary>
<br>

Each new expression creates a distinct String object, so the references are different.

</details>

<details>
<summary>5. What is the difference between == and equals()?</summary>
<br>

For String objects, == checks reference identity while equals() checks content equality.

</details>

<details>
<summary>6. What does intern() return?</summary>
<br>

The canonical pooled String for the same contents.

</details>

<details>
<summary>7. Does intern() move a heap object into the pool?</summary>
<br>

No. It returns the canonical pooled reference.

</details>

<details>
<summary>8. How can a char[] be converted to String?</summary>
<br>

For example, by using new String(charArray).

</details>
## 🔗 Related Notes

- [Creating String Objects Overview →](08-creating-string-objects-overview.md)
- [String Literals & String Pool →](09-string-literals-and-string-pool.md)
- [String Using new →](10-string-using-new-operator.md)
- [String from Character Array →](11-string-from-character-array.md)
- [String Memory & Storage →](12-string-memory-and-storage.md)
- [intern() →](13-string-intern.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

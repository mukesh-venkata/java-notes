<a name="top"></a>

# 🆕 10. Creating Strings Using the new Operator

> **Core idea:** `new String(...)` explicitly creates a new String object.

## 🧠 Example

```java
String s1 = new String("Java");
String s2 = new String("Java");

System.out.println(s1 == s2);
```

Output:

```text
false
```

Each `new String("Java")` expression creates a distinct String object.

## 🔍 What About the Literal?

The literal `"Java"` is itself an interned String value.

So this expression:

```java
new String("Java")
```

involves:

1. The literal `"Java"` is obtained from the String Pool.
2. `new String(...)` creates another String object.

Conceptually:

```text
String Pool                 Heap
┌──────────┐              ┌──────────┐
│  "Java"  │ ←─────────── │ String   │
└──────────┘              │ "Java"   │
                          └──────────┘
                               ↑
                              s1
```

## 📌 Reference Comparison

```java
String a = new String("Java");
String b = new String("Java");

a == b       // false
a.equals(b)  // true
```

Why?

- `a` and `b` refer to different objects.
- Their contents are equal.

## ⚠️ Important

Using `new String("Java")` is usually unnecessary when a literal is sufficient, because it deliberately creates another String object.

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. Does <code>new String("Java")</code> create a new object?</summary>
<br>

Yes. The new expression creates a new String object.

</details>

<details>
<summary>2. Can the literal inside it be pooled?</summary>
<br>

Yes. The literal can be present in the String Pool while new String("Java") creates another String object.

</details>

<details>
<summary>3. Why is <code>a == b</code> false for two separate <code>new String()</code> calls?</summary>
<br>

Each new String() call creates a distinct String object, so the references point to different objects.

</details>

<details>
<summary>4. Why can <code>a.equals(b)</code> be true?</summary>
<br>

String.equals() compares String contents rather than object identity.

</details>
## 🔗 Related Notes

- [String Literals & String Pool →](09-string-literals-and-string-pool.md)
- [Memory & Storage →](12-string-memory-and-storage.md)
- [intern() →](13-string-intern.md)
- [Quick Revision →](14-string-object-creation-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

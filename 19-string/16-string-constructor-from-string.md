<a name="top"></a>

# 🆕 16. String Constructor from Another String

> **Core idea:** `new String(String)` creates a String object whose contents are the same as the supplied String.

## 🧠 Syntax

```java
String str = new String("Hello Java");
```

## 🔍 Example

```java
String str1 = new String("Hello Java");

System.out.println(str1);
```

Output:

```text
Hello Java
```

## 🧠 Memory Concept

Consider:

```java
String str1 = new String("Java");
```

The literal `"Java"` is an interned String, while `new String("Java")` creates an additional String object.

Conceptually:

```text
String Pool                 Heap
┌──────────┐              ┌──────────────┐
│  "Java"  │              │ String "Java"│
└──────────┘              └──────┬───────┘
                                 ↑
                                str1
```

## 🔍 Reference Comparison

```java
String a = new String("Java");
String b = new String("Java");

System.out.println(a == b);      // false
System.out.println(a.equals(b)); // true
```

- `==` compares references.
- `equals()` compares String contents.

## ⚠️ Practical Note

When you simply need the String value, a literal is normally preferable:

```java
String s = "Java";
```

Using `new String("Java")` is mainly useful when you specifically need a distinct String object.

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. Does <code>new String("Java")</code> create a new object?</summary>
<br>

Yes.

</details>

<details>
<summary>2. Is the literal <code>"Java"</code> also an interned String?</summary>
<br>

Yes. String literals are interned in the String Pool.

</details>

<details>
<summary>3. Why can two <code>new String()</code> references be different?</summary>
<br>

They refer to different String objects created by separate new expressions.

</details>

<details>
<summary>4. Why can <code>equals()</code> still return true?</summary>
<br>

String.equals() compares contents, which can be equal even when the objects are different.

</details>
## 🔗 Related Notes

- [Constructors Overview →](15-string-constructors-overview.md)
- [String Pool & Literals →](09-string-literals-and-string-pool.md)
- [String Memory & Storage →](12-string-memory-and-storage.md)
- [Quick Revision →](19-string-constructors-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

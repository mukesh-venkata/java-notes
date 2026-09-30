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

## 🎯 Interview Questions

1. Does `new String("Java")` create a new object? **Yes.**
2. Is the literal `"Java"` also an interned String? **Yes.**
3. Why can two `new String()` references be different? **They refer to different objects.**
4. Why can `equals()` still return true? **Their contents are equal.**

## 🔗 Related Notes

- [Constructors Overview →](15-string-constructors-overview.md)
- [String Pool & Literals →](09-string-literals-and-string-pool.md)
- [String Memory & Storage →](12-string-memory-and-storage.md)
- [Quick Revision →](19-string-constructors-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

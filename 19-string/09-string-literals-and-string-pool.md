<a name="top"></a>

# 🔤 9. String Literals & the String Pool

> **Core idea:** String literals are interned strings and can be reused from the String Pool.

## 🧠 String Literal

Example:

```java
String s1 = "Java";
String s2 = "Java";

System.out.println(s1 == s2);
```

Output:

```text
true
```

When the same literal is reused, the references can point to the same pooled String.

## 🏊 String Pool

Conceptually:

```text
String Pool
┌─────────────┐
│   "Java"    │
└──────┬──────┘
       ↑
   ┌───┴───┐
  s1      s2
```

The pool allows identical literal strings to be shared rather than requiring a separate pooled String for every occurrence.

## 🔍 == vs equals()

`==` compares references for objects.

`equals()` compares String contents.

```java
String a = "Java";
String b = "Java";

System.out.println(a == b);       // true
System.out.println(a.equals(b));  // true
```

## 📌 Important

The String Pool is commonly discussed as part of Java's string interning mechanism. Modern JVMs manage pooled strings in the heap, but the important programming concept is **canonical reuse of interned String values**.

## 🎯 Interview Questions

### Q1. Where are String literals interned?
In the String Pool.

### Q2. Why can two identical literals have the same reference?
The same pooled String can be reused.

### Q3. Does == compare String content?
No. It compares references.

### Q4. Which method compares String content?
`equals()`.

## 🔗 Related Notes

- [Creating String Objects Overview →](08-creating-string-objects-overview.md)
- [new Operator →](10-string-using-new-operator.md)
- [Memory & Storage →](12-string-memory-and-storage.md)
- [intern() →](13-string-intern.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

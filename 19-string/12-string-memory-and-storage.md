<a name="top"></a>

# 🧠 12. How Strings Are Stored in Java Memory

> **Core idea:** String literals are interned for reuse, while `new String(...)` creates an additional String object.

## 1️⃣ String Literal

```java
String s = "Java";
```

Conceptually:

```text
String Pool
┌──────────┐
│  "Java"  │
└────┬─────┘
     ↑
     s
```

## 2️⃣ Using new

```java
String s1 = new String("Java");
```

Conceptually:

```text
String Pool                 Heap
┌──────────┐              ┌──────────────┐
│  "Java"  │              │ String "Java"│
└─────┬────┘              └──────┬───────┘
      ↑                          ↑
  literal                    s1 reference
```

The literal can refer to the pooled String while `new String()` creates a separate String object.

## 📌 Important Memory Rules

- String literals are interned.
- Identical interned literals can be reused.
- `new String(...)` creates a distinct String object.
- Multiple references can point to the same String object.
- `==` compares references; `equals()` compares content for String.

## 🧠 JVM Nuance

Avoid memorizing an old simplified rule that says “the String Pool is always in a separate special memory area.” Modern JVM implementations manage interned Strings in the heap.

For interviews, the most useful model is:

```text
String literal → interned String Pool
new String(...) → additional String object
```

## 🎯 Interview Questions

1. What happens with a String literal?
2. What does new String() add?
3. Can multiple references share a pooled String?
4. Does the String Pool have to be treated as a separate memory region from the heap?
5. What is the difference between reference equality and content equality?

## 🔗 Related Notes

- [String Literals & String Pool →](09-string-literals-and-string-pool.md)
- [new Operator →](10-string-using-new-operator.md)
- [intern() →](13-string-intern.md)
- [Quick Revision →](14-string-object-creation-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

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

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What happens with a String literal?</summary>
<br>

A String literal is interned in the String Pool, and references to that literal can share the canonical pooled String.

</details>

<details>
<summary>2. What does new String() add?</summary>
<br>

new String(...) creates a new String object even when the same text is already available as a pooled literal.

</details>

<details>
<summary>3. Can multiple references share a pooled String?</summary>
<br>

Yes. Multiple references can point to the same canonical pooled String.

</details>

<details>
<summary>4. Does the String Pool have to be treated as a separate memory region from the heap?</summary>
<br>

No. Modern JVMs manage interned Strings in the heap; the important concept is canonical reuse through the String Pool.

</details>

<details>
<summary>5. What is the difference between reference equality and content equality?</summary>
<br>

== checks reference identity for objects, while equals() checks String content.

</details>
## 🔗 Related Notes

- [String Literals & String Pool →](09-string-literals-and-string-pool.md)
- [new Operator →](10-string-using-new-operator.md)
- [intern() →](13-string-intern.md)
- [Quick Revision →](14-string-object-creation-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

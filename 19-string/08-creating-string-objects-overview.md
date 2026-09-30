<a name="top"></a>

# 🧱 8. Creating String Objects — Overview

> **Core idea:** Java Strings can commonly be created through literals, constructors, and character-array conversion.

## 🧠 Three Common Ways

| # | Approach | Main idea |
|---:|---|---|
| 1 | String literal | Uses the String Pool |
| 2 | `new String(...)` | Creates a new String object |
| 3 | Character array | Creates a String from `char[]` |

## 🔄 Big Picture

```text
Creating String objects
        │
        ├── "Java"
        │      ↓
        │   String Pool
        │
        ├── new String("Java")
        │      ↓
        │   New String object
        │
        └── new String(char[])
               ↓
          New String object
```

## 🔗 Related Concept

`intern()` is not another normal constructor. It returns the canonical pooled String for the same contents.

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What are common ways to create a String?</summary>
<br>

Common forms include String literals, the String constructors, and methods such as valueOf() that create or return String values.

</details>

<details>
<summary>2. Where is a String literal stored?</summary>
<br>

A String literal is interned in the String Pool.

</details>

<details>
<summary>3. What does <code>new String()</code> do?</summary>
<br>

It creates a new String object using the selected constructor.

</details>

<details>
<summary>4. What does <code>intern()</code> return?</summary>
<br>

The canonical pooled String for the same contents.

</details>
## 🔗 Related Notes

- [String Literals & String Pool →](09-string-literals-and-string-pool.md)
- [String Using new →](10-string-using-new-operator.md)
- [String from Character Array →](11-string-from-character-array.md)
- [String Memory & Storage →](12-string-memory-and-storage.md)
- [intern() →](13-string-intern.md)
- [Quick Revision →](14-string-object-creation-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

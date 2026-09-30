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

## 🎯 Interview Questions

1. What are common ways to create a String?
2. Where is a String literal stored?
3. What does `new String()` do?
4. What does `intern()` return?

## 🔗 Related Notes

- [String Literals & String Pool →](09-string-literals-and-string-pool.md)
- [String Using new →](10-string-using-new-operator.md)
- [String from Character Array →](11-string-from-character-array.md)
- [String Memory & Storage →](12-string-memory-and-storage.md)
- [intern() →](13-string-intern.md)
- [Quick Revision →](14-string-object-creation-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

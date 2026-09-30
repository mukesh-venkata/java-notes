<a name="top"></a>

# ⚡ 7. Ways to Create an Object — Quick Revision

> **30-second revision:** Java supports normal constructor-based creation, copying, runtime reflection, and reconstruction from serialized data.

## 🧠 Five Approaches

| # | Way | Remember |
|---:|---|---|
| 1 | `new` | Normal creation + constructor |
| 2 | `clone()` | Shallow copy |
| 3 | Reflection | Runtime-driven creation |
| 4 | Constructor Reflection | `Constructor.newInstance()` |
| 5 | Deserialization | `ObjectInputStream.readObject()` |

## 🔑 High-Value Rules

- `new` invokes the selected constructor.
- `clone()` creates a shallow copy when supported.
- `Cloneable` is a marker interface.
- `Class.newInstance()` is deprecated since Java 9.
- `Constructor.newInstance()` is the modern constructor-reflection API.
- Deserialization reconstructs serialized state.
- The serializable class's constructor is not invoked in the usual way during normal deserialization.

## 🧠 Memory Trick

```text
NEW    → Normal
CLONE  → Copy
REFLECT→ Runtime
CTOR   → Specific constructor
READ   → Reconstruct
```

## 🎯 Interview Questions

1. What is the most common way to create an object?
2. What type of copy does `clone()` provide?
3. What is `Cloneable`?
4. Why is `Class.newInstance()` avoided?
5. What replaces the old reflection approach?
6. How does constructor reflection create an object?
7. What does `readObject()` do?
8. Is the serializable class's constructor invoked normally during deserialization?

## 🔗 Related Notes

- [Overview →](01-object-creation-overview.md)
- [new Operator →](02-new-operator.md)
- [clone() & Shallow Copy →](03-clone-and-shallow-copy.md)
- [Reflection →](04-reflection-object-creation.md)
- [Deserialization →](05-deserialization-object-creation.md)
- [Comparison →](06-object-creation-comparison.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

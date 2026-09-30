<a name="top"></a>

# 🧱 1. Object Creation in Java — Overview

> **Core idea:** Java objects can be created or reconstructed in several ways, depending on the situation.

## 🧠 Five Common Approaches

| # | Approach | Main idea |
|---:|---|---|
| 1 | `new` operator | Creates an object and invokes a constructor |
| 2 | `clone()` | Creates a shallow copy of an existing object |
| 3 | Reflection | Creates an object dynamically at runtime |
| 4 | Constructor Reflection | Obtains a `Constructor` and invokes it |
| 5 | Deserialization | Reconstructs an object from serialized data |

## 🔄 Big Picture

```text
Ways to create / reconstruct an object
              ↓
 ┌────────────┼─────────────┐
 ↓            ↓             ↓
new         clone()      Reflection
                            ↓
                    Constructor.newInstance()
                            ↓
                     Deserialization
```

## 📌 Important Distinction

These approaches do not all work in exactly the same way.

- `new` → normal constructor-based creation.
- `clone()` → copy-based creation.
- Reflection → runtime-driven creation.
- Constructor reflection → explicitly invokes a selected constructor.
- Deserialization → reconstructs an object's serialized state.

## 🎯 When Are They Useful?

### `new`
The normal choice when the class and constructor are known at compile time.

### `clone()`
Useful when a supported cloning mechanism is intentionally used to copy an existing object.

### Reflection
Useful when the class or constructor needs to be discovered dynamically at runtime.

### Deserialization
Used when serialized object data needs to be reconstructed.

## 🔗 Related Notes

- [new Operator →](02-new-operator.md)
- [clone() & Shallow Copy →](03-clone-and-shallow-copy.md)
- [Reflection Object Creation →](04-reflection-object-creation.md)
- [Deserialization Object Creation →](05-deserialization-object-creation.md)
- [Object Creation Comparison →](06-object-creation-comparison.md)
- [Quick Revision →](07-object-creation-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

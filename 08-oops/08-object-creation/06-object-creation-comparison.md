<a name="top"></a>

# 📊 6. Object Creation — Comparison

> **Core idea:** Different object-creation techniques solve different problems.

## 📋 Comparison Table

| # | Approach | Key API / syntax | Constructor behavior | Main idea |
|---:|---|---|---|---|
| 1 | `new` | `new Student()` | Invoked | Normal creation |
| 2 | `clone()` | `obj.clone()` | Not a normal new-object constructor call | Shallow copy |
| 3 | Reflection | `Constructor.newInstance()` | Selected constructor invoked | Runtime-driven creation |
| 4 | Constructor Reflection | `constructor.newInstance()` | Selected constructor invoked | Specific constructor |
| 5 | Deserialization | `readObject()` | Serializable class constructor not invoked normally | Reconstruct serialized state |

## 🔍 Important Terminology

The handwritten topic separates “Reflection” and “Constructor via Reflection.” The practical distinction is:

- Reflection can refer broadly to runtime inspection and dynamic creation.
- `Constructor.newInstance()` is the modern constructor-based reflection mechanism.

The older `Class.newInstance()` approach is deprecated.

## 🧠 Quick Decision Guide

```text
Known class + normal creation
        ↓
       new

Existing object + supported copy mechanism
        ↓
     clone()

Need runtime class/constructor discovery
        ↓
 Constructor.newInstance()

Have serialized object data
        ↓
   readObject()
```

## 🎯 Interview Points

- `new` is the standard constructor-based approach.
- `clone()` creates a shallow copy when supported.
- `Class.newInstance()` is deprecated since Java 9.
- `Constructor.newInstance()` is the modern reflection mechanism.
- Deserialization reconstructs serialized object state.
- Normal deserialization does not invoke the serializable class's constructor in the usual way.

## 🔗 Related Notes

- [Overview →](01-object-creation-overview.md)
- [new Operator →](02-new-operator.md)
- [clone() →](03-clone-and-shallow-copy.md)
- [Reflection →](04-reflection-object-creation.md)
- [Deserialization →](05-deserialization-object-creation.md)
- [Quick Revision →](07-object-creation-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

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

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What is the most common way to create an object?</summary>
<br>

Using the new operator with a constructor.

</details>

<details>
<summary>2. What type of copy does clone() provide?</summary>
<br>

Object.clone() provides a shallow copy by default.

</details>

<details>
<summary>3. What is Cloneable?</summary>
<br>

A marker interface used to indicate support for the Object cloning mechanism.

</details>

<details>
<summary>4. Why is Class.newInstance() avoided?</summary>
<br>

It has been deprecated since Java 9 and has less precise exception behavior than the modern constructor reflection API.

</details>

<details>
<summary>5. What replaces the old reflection approach?</summary>
<br>

Constructor.newInstance() is the modern reflection API for invoking a constructor.

</details>

<details>
<summary>6. How does constructor reflection create an object?</summary>
<br>

A Constructor object is obtained and its newInstance() method is invoked with the required arguments.

</details>

<details>
<summary>7. What does readObject() do?</summary>
<br>

It participates in Java deserialization by reading serialized data and reconstructing object state according to the serialization mechanism.

</details>

<details>
<summary>8. Is the serializable class's constructor invoked normally during deserialization?</summary>
<br>

For a Serializable class, its normal constructors are not invoked during default deserialization; initialization of the serializable object follows the serialization mechanism.

</details>
## 🔗 Related Notes

- [Overview →](01-object-creation-overview.md)
- [new Operator →](02-new-operator.md)
- [clone() & Shallow Copy →](03-clone-and-shallow-copy.md)
- [Reflection →](04-reflection-object-creation.md)
- [Deserialization →](05-deserialization-object-creation.md)
- [Comparison →](06-object-creation-comparison.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

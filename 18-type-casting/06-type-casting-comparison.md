<a name="top"></a>

# 📊 6. Type Casting — Comparison

## 🔢 Primitive Casting

| Type | Direction | Automatic? | Example |
|---|---|---|---|
| Widening | Narrower → wider | Usually yes | `int x = 'A';` |
| Narrowing | Wider → narrower | No | `char c = (char) 65;` |

## 🧬 Reference Casting

| Type | Direction | Automatic? | Example |
|---|---|---|---|
| Upcasting | Child → Parent | Yes | `Parent p = new Child();` |
| Downcasting | Parent → Child | No | `Child c = (Child) p;` |

## 🧠 Side-by-Side

```text
Primitive
  Widening   → automatic
  Narrowing  → explicit

Reference
  Upcasting  → automatic
  Downcasting → explicit
```

## ⚠️ Main Risk

### Narrowing
May lose information because the target type has a smaller representable range or precision.

### Downcasting
May fail at runtime if the actual object is not an instance of the target type.

## 🔍 Safe Reference Downcasting

```java
if (p instanceof Child) {
    Child c = (Child) p;
}
```

## 📌 Literal Rules

| Literal | Default / indicated type |
|---|---|
| `10` | `int` |
| `10L` | `long` |
| `10.20` | `double` |
| `10.20f` | `float` |

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What is the difference between widening and narrowing?</summary>
<br>

Widening converts to a broader compatible primitive type and is usually implicit; narrowing converts to a smaller type and generally requires an explicit cast.

</details>

<details>
<summary>2. What is the difference between upcasting and downcasting?</summary>
<br>

Upcasting treats a child object through a parent reference and is generally implicit. Downcasting converts a parent reference to a more specific child reference and requires an explicit cast.

</details>

<details>
<summary>3. Which conversions are normally implicit?</summary>
<br>

Primitive widening and compatible reference upcasting are normally implicit.

</details>

<details>
<summary>4. Why can narrowing lose information?</summary>
<br>

A smaller target type may not be able to represent every value of the source type, so precision or magnitude can be lost.

</details>

<details>
<summary>5. Why can downcasting throw ClassCastException?</summary>
<br>

The runtime object may not actually be an instance of the target child type, so the cast is invalid.

</details>

<details>
<summary>6. What is the role of instanceof?</summary>
<br>

It tests whether a reference is compatible with a specified type before performing a reference cast or using type-specific behavior.

</details>
## 🔗 Related Notes

- [Overview →](01-type-casting-overview.md)
- [Primitive Casting →](02-primitive-widening-and-narrowing.md)
- [Numeric Literals →](03-numeric-literals-and-casting.md)
- [Reference Casting →](04-reference-upcasting-and-downcasting.md)
- [instanceof →](05-instanceof-and-classcastexception.md)
- [Quick Revision →](07-type-casting-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

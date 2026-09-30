<a name="top"></a>

# ⚡ 7. Type Casting — Quick Revision

> **30-second revision:** Primitive casting changes primitive values; reference casting changes compatible object references.

## 🧠 Master Table

| Category | Type | Direction | Cast |
|---|---|---|---|
| Primitive | Widening | Narrower → wider | Usually implicit |
| Primitive | Narrowing | Wider → narrower | Explicit |
| Reference | Upcasting | Child → Parent | Usually implicit |
| Reference | Downcasting | Parent → Child | Explicit |

## 🔑 Key Rules

- Widening primitive conversion is generally automatic.
- Narrowing primitive conversion normally requires an explicit cast.
- Upcasting a child reference to a parent reference is automatic.
- Downcasting requires an explicit cast.
- Downcasting is safe only when the runtime object is compatible with the target type.
- Invalid runtime downcasts can cause `ClassCastException`.
- Use `instanceof` when a runtime type check is needed.
- Decimal floating-point literals are `double` by default.
- Use `f` or `F` for a `float` literal.
- Integer literals are normally `int`; use `L`/ `l` for `long`.

## 🧠 Memory Trick

```text
Primitive:
W → Wide → automatic
N → Narrow → explicit

Reference:
U → Up → Child → Parent
D → Down → Parent → Child
```

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What is type casting?</summary>
<br>

Converting a value or reference from one compatible type to another.

</details>

<details>
<summary>2. What are the two broad categories of type casting?</summary>
<br>

Primitive casting and reference casting.

</details>

<details>
<summary>3. What is widening?</summary>
<br>

Converting a narrower primitive type to a wider compatible type, usually automatically.

</details>

<details>
<summary>4. What is narrowing?</summary>
<br>

Converting a wider primitive type to a narrower type, generally using an explicit cast.

</details>

<details>
<summary>5. What is upcasting?</summary>
<br>

Treating a child object through a parent reference.

</details>

<details>
<summary>6. What is downcasting?</summary>
<br>

Explicitly converting a parent reference to a more specific child reference when the runtime object is actually compatible.

</details>

<details>
<summary>7. Why can downcasting throw ClassCastException?</summary>
<br>

Because the runtime object may not be an instance of the target child type.

</details>

<details>
<summary>8. How does instanceof help?</summary>
<br>

It checks reference compatibility with a type before performing a cast.

</details>

<details>
<summary>9. What is the default type of 10.20?</summary>
<br>

double.

</details>

<details>
<summary>10. How do you write a float literal?</summary>
<br>

Use f or F, for example 10.20f.

</details>

<details>
<summary>11. How do you write a long literal?</summary>
<br>

Use L or l, for example 100L. Uppercase L is generally clearer.

</details>
## 🔗 Related Notes

- [Overview →](01-type-casting-overview.md)
- [Primitive Widening & Narrowing →](02-primitive-widening-and-narrowing.md)
- [Numeric Literals →](03-numeric-literals-and-casting.md)
- [Reference Upcasting & Downcasting →](04-reference-upcasting-and-downcasting.md)
- [instanceof & ClassCastException →](05-instanceof-and-classcastexception.md)
- [Comparison →](06-type-casting-comparison.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

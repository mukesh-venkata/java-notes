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

## 🎯 Interview Questions

1. What is type casting?
2. What are the two broad categories of type casting?
3. What is widening?
4. What is narrowing?
5. What is upcasting?
6. What is downcasting?
7. Why can downcasting throw ClassCastException?
8. How does instanceof help?
9. What is the default type of 10.20?
10. How do you write a float literal?
11. How do you write a long literal?

## 🔗 Related Notes

- [Overview →](01-type-casting-overview.md)
- [Primitive Widening & Narrowing →](02-primitive-widening-and-narrowing.md)
- [Numeric Literals →](03-numeric-literals-and-casting.md)
- [Reference Upcasting & Downcasting →](04-reference-upcasting-and-downcasting.md)
- [instanceof & ClassCastException →](05-instanceof-and-classcastexception.md)
- [Comparison →](06-type-casting-comparison.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

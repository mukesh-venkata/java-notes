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

## 🎯 Interview Questions

1. What is the difference between widening and narrowing?
2. What is the difference between upcasting and downcasting?
3. Which conversions are normally implicit?
4. Why can narrowing lose information?
5. Why can downcasting throw ClassCastException?
6. What is the role of instanceof?

## 🔗 Related Notes

- [Overview →](01-type-casting-overview.md)
- [Primitive Casting →](02-primitive-widening-and-narrowing.md)
- [Numeric Literals →](03-numeric-literals-and-casting.md)
- [Reference Casting →](04-reference-upcasting-and-downcasting.md)
- [instanceof →](05-instanceof-and-classcastexception.md)
- [Quick Revision →](07-type-casting-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

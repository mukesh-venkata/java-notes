<a name="top"></a>

# 🔄 1. Type Casting — Overview

> **Core idea:** Type casting converts a value from one data type to another compatible data type.

## 🧠 Two Main Categories

```text
Type Casting
│
├── Primitive Type Casting
│   ├── Widening → implicit
│   └── Narrowing → explicit
│
└── Reference Type Casting
    ├── Upcasting → Child → Parent
    └── Downcasting → Parent → Child
```

## 1️⃣ Primitive Type Casting

Primitive casting converts one primitive value to another compatible primitive type.

### Widening

A narrower primitive type is converted to a wider compatible type.

- Usually automatic.
- No explicit cast is required.

```java
char ch = 'A';
int value = ch;

System.out.println(value); // 65
```

### Narrowing

A wider type is converted to a narrower type.

- Must normally be explicit.
- A cast is required.

```java
int value = 65;
char ch = (char) value;

System.out.println(ch); // A
```

## 2️⃣ Reference Type Casting

Reference casting converts a reference from one compatible reference type to another.

It normally requires an inheritance or interface relationship.

### Upcasting

```java
Parent p = new Child();
```

Child reference → Parent reference.

Usually automatic.

### Downcasting

```java
Child c = (Child) p;
```

Parent reference → Child reference.

Requires an explicit cast and is safe only when the runtime object is compatible with `Child`.

## 📌 Key Difference

| Primitive | Reference |
|---|---|
| Works with primitive values | Works with object references |
| Widening / narrowing | Upcasting / downcasting |
| Numeric/character conversion rules | Type hierarchy compatibility |
| No `instanceof` for primitive values | `instanceof` can check reference compatibility |

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What is type casting?</summary>
<br>

Converting a value or reference from one compatible type to another.

</details>

<details>
<summary>Q2. What are the two broad categories?</summary>
<br>

Primitive casting and reference casting.

</details>

<details>
<summary>Q3. What is widening?</summary>
<br>

Converting a narrower primitive type to a wider compatible type, usually automatically.

</details>

<details>
<summary>Q4. What is upcasting?</summary>
<br>

Converting a child reference to a parent reference. It is generally implicit when the types are compatible.

</details>
## 🔗 Related Notes

- [Primitive Widening & Narrowing →](02-primitive-widening-and-narrowing.md)
- [Numeric Literals & Casting →](03-numeric-literals-and-casting.md)
- [Reference Upcasting & Downcasting →](04-reference-upcasting-and-downcasting.md)
- [instanceof & ClassCastException →](05-instanceof-and-classcastexception.md)
- [Comparison →](06-type-casting-comparison.md)
- [Quick Revision →](07-type-casting-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

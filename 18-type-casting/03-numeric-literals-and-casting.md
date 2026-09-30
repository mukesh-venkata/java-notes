<a name="top"></a>

# 🔣 3. Numeric Literals & Casting

> **Core idea:** Literal types matter when Java decides whether an assignment or conversion is valid.

## 🔢 Decimal / Floating-Point Literals

A decimal floating-point literal is a `double` by default.

```java
double d = 10.20;   // OK
```

Assigning the same literal directly to a `float` is not allowed without indicating that it is a float literal:

```java
float f = 10.20;   // Compilation error
```

Use `f` or `F`:

```java
float f1 = 10.20f;
float f2 = 10.20F;
```

## 🔢 Integer Literals

An integer literal is normally of type `int` when its value can be represented as an `int`.

To make it a `long` literal, use `L` or `l`.

```java
long x = 21727L;
```

### Why Prefer Uppercase L?

```java
long x = 21727L;
```

Uppercase `L` is easier to distinguish from the digit `1`.

## 🔗 Connection to Casting

Literal type can affect assignment:

```java
int a = 10;        // int literal
long b = 10;       // widening conversion
float c = 10.20f;  // float literal
double d = 10.20;  // double literal
```

## 🧠 Remember

```text
10       → int
10L      → long
10.20    → double
10.20f   → float
```

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What is the default type of an integer literal?</summary>
<br>

int, subject to the literal's representable range.

</details>

<details>
<summary>Q2. What is the default type of a decimal floating-point literal?</summary>
<br>

double.

</details>

<details>
<summary>Q3. How do you write a float literal?</summary>
<br>

Use f or F, for example 10.20f.

</details>

<details>
<summary>Q4. How do you write a long literal?</summary>
<br>

Use L or l; uppercase L is generally clearer.

</details>
## 🔗 Related Notes

- [Type Casting Overview →](01-type-casting-overview.md)
- [Widening & Narrowing →](02-primitive-widening-and-narrowing.md)
- [Reference Casting →](04-reference-upcasting-and-downcasting.md)
- [Quick Revision →](07-type-casting-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

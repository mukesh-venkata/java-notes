<a name="top"></a>

# ➕ Java Arithmetic & Assignment Operators

> **Topic 11 • Java Fundamentals**

## 1️⃣ Arithmetic Operators

Arithmetic operators perform mathematical operations.

| Operator | Operation | Example |
|---|---|---|
| `+` | Addition | `a + b` |
| `-` | Subtraction | `a - b` |
| `*` | Multiplication | `a * b` |
| `/` | Division | `a / b` |
| `%` | Modulus / remainder | `a % b` |

### Example

```java
int a = 10;
int b = 3;

System.out.println(a + b); // 13
System.out.println(a - b); // 7
System.out.println(a * b); // 30
System.out.println(a / b); // 3
System.out.println(a % b); // 1
```

### ⚠️ Integer Division

When both operands are integers, Java performs integer division:

```java
10 / 3   // 3
```

The fractional part is discarded.

With a floating-point operand:

```java
10.0 / 3   // approximately 3.333...
```

---

## 2️⃣ Assignment Operators

Assignment operators store or update a value in a variable.

| Operator | Meaning | Equivalent |
|---|---|---|
| `=` | Assign | `a = 5` |
| `+=` | Add and assign | `a = a + 5` |
| `-=` | Subtract and assign | `a = a - 5` |
| `*=` | Multiply and assign | `a = a * 2` |
| `/=` | Divide and assign | `a = a / 2` |
| `%=` | Modulus and assign | `a = a % 3` |

### Example

```java
int a = 10;

a += 5;  // 15
a -= 5;  // 10
a *= 2;  // 20
a /= 2;  // 10
a %= 3;  // 1
```

---

## 🧠 Quick Memory

**Arithmetic → Calculate**

```text
+  -  *  /  %
```

**Assignment → Store / Update**

```text
=  +=  -=  *=  /=  %=
```

---

## 🎤 Interview Quick Check

**Q1. What does `%` return?**  
A: The remainder after division.

**Q2. What is `10 / 3` when both are `int`?**  
A: `3`.

**Q3. What does `a += 5` mean?**  
A: `a = a + 5`.

---

## 🔗 Navigation

⬅️ [Operators Overview](./01-operators-overview.md)

➡️ [Increment, Decrement & Unary](./03-increment-decrement-unary.md)

➡️ [Quick Revision](./07-operators-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

# 🔢 Java Increment, Decrement & Unary Operators

> **Topic 11 • Java Fundamentals**

## 1️⃣ Increment & Decrement

| Operator | Meaning |
|---|---|
| `++` | Increment by 1 |
| `--` | Decrement by 1 |

### Prefix vs Postfix

The position of the operator affects when the updated value is used in an expression.

| Form | Name | Value used in expression |
|---|---|---|
| `++a` | Prefix increment | Updated value |
| `a++` | Postfix increment | Original value |
| `--a` | Prefix decrement | Updated value |
| `a--` | Postfix decrement | Original value |

### Example

```java
int a = 10;

int x = ++a; // a = 11, x = 11

int b = 10;

int y = b++; // y = 10, b = 11
```

> **Memory trick:** Prefix = **change first, use later**. Postfix = **use first, change later**.

---

## 2️⃣ Unary Operators

A unary operator works with **one operand**.

| Operator | Meaning |
|---|---|
| `+` | Unary plus |
| `-` | Unary minus |
| `++` | Increment |
| `--` | Decrement |
| `!` | Logical NOT |
| `~` | Bitwise complement |

### Examples

```java
int a = 10;

int b = -a;       // -10
boolean c = !true; // false
int d = ~a;       // -11
```

For an integer, bitwise complement follows:

```text
~n = -(n + 1)
```

So:

```text
~10 = -11
```

---

## 🧠 Important Distinction

`++` and `--` are:

- Increment/decrement operators
- Unary operators

This shows that Java's operator categories can overlap.

---

## 🎤 Interview Quick Check

**Q1. What is the difference between `++a` and `a++`?**  
A: Prefix updates before the value is used in the expression; postfix uses the original value before updating.

**Q2. How many operands does a unary operator use?**  
A: One.

**Q3. What is `~10`?**  
A: `-11` for an integer value.

---

## 🔗 Navigation

⬅️ [Operators Overview](./01-operators-overview.md)

➡️ [Relational, Logical & Ternary](./04-relational-logical-ternary.md)

➡️ [Bitwise Operators](./05-bitwise-operators.md)

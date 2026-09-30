# 🔀 Java Relational, Logical & Ternary Operators

> **Topic 11 • Java Fundamentals**

## 1️⃣ Relational Operators

Relational operators compare values.

| Operator | Meaning |
|---|---|
| `==` | Equal to |
| `!=` | Not equal to |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |

The result is a boolean:

```text
true / false
```

### Example

```java
int a = 10;
int b = 20;

a == b; // false
a != b; // true
a > b;  // false
a < b;  // true
a >= b; // false
a <= b; // true
```

> **Important:** For objects, `==` checks reference identity, while `.equals()` is commonly used to compare logical/content equality when the class provides the appropriate implementation.

---

## 2️⃣ Logical Operators

Logical operators combine or negate boolean expressions.

| Operator | Meaning |
|---|---|
| `&&` | Logical AND |
| `||` | Logical OR |
| `!` | Logical NOT |

### Example

```java
int age = 25;

if (age > 18 && age < 60) {
    System.out.println("Valid");
}
```

### Truth Table

| A | B | A && B | A || B |
|---|---|---|---|
| false | false | false | false |
| false | true | false | true |
| true | false | false | true |
| true | true | true | true |

For NOT:

| A | !A |
|---|---|
| false | true |
| true | false |

### ⚡ Short-Circuiting

With `&&` and `||`, Java can skip evaluating the right-hand expression when the result is already known.

```java
if (obj != null && obj.isValid()) {
    // Safe short-circuit pattern
}
```

---

## 3️⃣ Ternary Operator

The conditional operator `?:` is Java's ternary operator.

### Syntax

```text
condition ? valueIfTrue : valueIfFalse
```

### Example

```java
int age = 20;

String result = age >= 18 ? "Adult" : "Minor";
```

If the condition is true:

```text
result = "Adult"
```

Otherwise:

```text
result = "Minor"
```

> **Memory trick:** Ternary = **one condition, two choices**.

---

## 🎤 Interview Quick Check

**Q1. What is the result type of a relational expression?**  
A: `boolean`.

**Q2. What is the difference between `&&` and `&`?**  
A: `&&` is logical AND with short-circuit evaluation; `&` is bitwise AND for integral operands and also a non-short-circuit boolean AND when used with booleans.

**Q3. What is the ternary operator?**  
A: The conditional operator `?:`, which selects one of two expressions based on a condition.

---

## 🔗 Navigation

⬅️ [Operators Overview](./01-operators-overview.md)

➡️ [Bitwise Operators](./05-bitwise-operators.md)

➡️ [Quick Revision](./07-operators-quick-revision.md)

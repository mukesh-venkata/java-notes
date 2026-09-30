# ⚙️ Java Operators — Overview

> **Topic 11 • Java Fundamentals**

An **operator** is a symbol or keyword that tells Java to perform an operation on one or more operands.

---

## 🎯 What Is an Operator?

In:

```java
int result = a + b;
```

- `+` is the **operator**
- `a` and `b` are **operands**
- `result` stores the result

Operators are used for calculations, comparisons, assignments, logical decisions, object creation and more.

---

## 🧩 Java Operator Map

A useful memory aid from the notes is:

### **IND-AAB-LURT**

| Letter | Category | Examples |
|---|---|---|
| **I** | Increment / Decrement | `++`, `--` |
| **N** | `new` | `new Student()` |
| **D** | Dot / member access | `student.name` |
| **A** | Arithmetic | `+`, `-`, `*`, `/`, `%` |
| **A** | Assignment | `=`, `+=`, `-=`, `*=` |
| **B** | Bitwise / shift | `&`, `|`, `^`, `~`, `<<`, `>>`, `>>>` |
| **L** | Logical | `&&`, `||`, `!` |
| **U** | Unary | `+`, `-`, `++`, `--`, `!`, `~` |
| **R** | Relational | `==`, `!=`, `>`, `<`, `>=`, `<=` |
| **T** | Ternary | `?:` |

> **Important:** These categories overlap. For example, `++` is both an increment/decrement operator and a unary operator.

---

## 🔢 Unary, Binary and Ternary

Operators can also be classified by the number of operands they work with.

### Unary → 1 operand

```java
++a;
-a;
!flag;
```

### Binary → 2 operands

```java
a + b;
a > b;
a && b;
```

### Ternary → 3 operands

```java
condition ? value1 : value2;
```

---

## 🧠 Operator vs Operand

```text
        a + b
        │ │ │
     operand │ operand
             │
          operator
```

Think:

**Operator = performs the operation**  
**Operand = value the operation works on**

---

## 🎤 Interview Quick Check

**Q1. What is an operator?**  
A: A symbol or keyword used to perform an operation on one or more operands.

**Q2. What is an operand?**  
A: A value or expression on which an operator acts.

**Q3. How many operands does a ternary operator use?**  
A: Three.

**Q4. Can an operator belong to more than one category?**  
A: Yes. For example, `++` is both increment/decrement and unary.

---

## 🔗 Navigation

➡️ [Arithmetic & Assignment](./02-arithmetic-assignment.md)

➡️ [Increment, Decrement & Unary](./03-increment-decrement-unary.md)

➡️ [Relational, Logical & Ternary](./04-relational-logical-ternary.md)

➡️ [Bitwise Operators](./05-bitwise-operators.md)

➡️ [new & Dot Operators](./06-new-and-dot-operators.md)

➡️ [Quick Revision](./07-operators-quick-revision.md)

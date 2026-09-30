# 🪜 Java `if-else-if` Ladder

> **Topic 12 • Java Fundamentals**

An `if-else-if` ladder is used when there are **multiple conditions** to evaluate.

---

## 📌 Syntax

```java
if (condition1) {
    // block 1
} else if (condition2) {
    // block 2
} else {
    // default block
}
```

Java evaluates conditions **from top to bottom**.

The first condition that is true gets its block executed, and the remaining conditions in that chain are skipped.

---

## 💻 Example

```java
int marks = 80;

if (marks >= 90) {
    System.out.println("A");
} else if (marks >= 75) {
    System.out.println("B");
} else {
    System.out.println("C");
}
```

Output:

```text
B
```

---

## 🔀 Flow

```text
Condition 1?
   │
 ┌─┴─┐
Yes  No
 │    │
Block  Condition 2?
       │
     ┌─┴─┐
    Yes  No
     │    │
   Block  Condition 3? ...
```

---

## ⚠️ Order Matters

Put more specific or higher-priority conditions first when the ranges overlap.

Example:

```java
if (marks >= 90) {
    System.out.println("A");
} else if (marks >= 75) {
    System.out.println("B");
}
```

If `marks = 95`, the first condition matches, so `A` is printed.

---

## 🎤 Interview Quick Check

**Q1. How are conditions evaluated?**  
A: From top to bottom.

**Q2. Can multiple branches of the same `if-else-if` chain execute?**  
A: No. Once a condition matches, the rest of that chain is skipped.

---

## 🔗 Navigation

⬅️ [if-else](./03-if-else-statement.md)

➡️ [Nested if](./05-nested-if.md)

➡️ [switch](./06-switch-statement.md)

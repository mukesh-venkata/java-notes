# 🔵 Java `if` Statement

> **Topic 12 • Java Fundamentals**

The `if` statement executes a block of code **only when its condition is true**.

---

## 📌 Syntax

```java
if (condition) {
    // statements
}
```

The condition must evaluate to a `boolean`.

---

## 💻 Example

```java
int age = 18;

if (age >= 18) {
    System.out.println("Adult");
}
```

Because `age >= 18` is true, the block executes.

If the condition is false, the block is skipped.

---

## 🔀 Flow

```text
        Condition
           │
      ┌────┴────┐
     true      false
       │          │
    Execute     Skip
     block      block
       │          │
       └────┬─────┘
            ↓
         Continue
```

---

## 🧠 Key Point

An `if` statement has **one explicit decision path**:

```text
true  → execute
false → skip
```

If you need an alternative action for the false case, use `if-else`.

---

## 🎤 Interview Quick Check

**Q1. What does an `if` statement do?**  
A: It executes a block when its boolean condition is true.

**Q2. Can Java's `if` condition be an integer like C/C++?**  
A: No. Java requires a boolean expression.

---

## 🔗 Navigation

⬅️ [Conditional Statements Overview](./01-conditional-statements-overview.md)

➡️ [if-else](./03-if-else-statement.md)

➡️ [Quick Revision](./07-conditional-statements-quick-revision.md)

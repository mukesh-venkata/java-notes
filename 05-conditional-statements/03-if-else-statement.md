# 🔵 Java `if-else` Statement

> **Topic 12 • Java Fundamentals**

The `if-else` statement provides two possible execution paths.

---

## 📌 Syntax

```java
if (condition) {
    // executes when true
} else {
    // executes when false
}
```

---

## 💻 Example

```java
int age = 18;

if (age >= 18) {
    System.out.println("Adult");
} else {
    System.out.println("Minor");
}
```

### Flow

```text
          Condition
             │
       ┌─────┴─────┐
      true        false
       │             │
   if block       else block
       │             │
       └──────┬──────┘
              ↓
           Continue
```

Exactly one of the two branches executes.

---

## 🧠 When to Use It

Use `if-else` when there are two mutually exclusive paths.

Examples:

- Adult / Minor
- Pass / Fail
- Valid / Invalid
- Available / Unavailable

---

## 🎤 Interview Quick Check

**Q1. How many branches does `if-else` provide?**  
A: Two.

**Q2. Can both the `if` and `else` blocks execute for one evaluation?**  
A: No. One branch is selected.

---

## 🔗 Navigation

⬅️ [if Statement](./02-if-statement.md)

➡️ [if-else-if Ladder](./04-if-else-if-ladder.md)

➡️ [Quick Revision](./07-conditional-statements-quick-revision.md)

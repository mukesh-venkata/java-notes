# 🪆 Java Nested `if`

> **Topic 12 • Java Fundamentals**

A **nested `if`** is an `if` statement placed inside another `if` statement.

---

## 📌 Example

```java
int age = 18;
boolean hasLicense = true;

if (age >= 18) {
    if (hasLicense) {
        System.out.println("Can drive");
    }
}
```

The inner condition is checked only after the outer condition is true.

---

## 🔀 Execution Flow

```text
Age >= 18?
    │
  ┌─┴─┐
 No  Yes
 │     │
Stop  Has license?
        │
      ┌─┴─┐
     No  Yes
     │     │
   Stop  Can drive
```

---

## 🧠 When Is It Useful?

Nested conditions can represent dependent decisions:

```text
First decision
     ↓
Second decision
     ↓
Action
```

For example:

- User is logged in → check authorization
- Product is available → check stock
- Age is eligible → check license

> Deep nesting can make code harder to read. When appropriate, simpler conditions or early returns can improve readability.

---

## 🎤 Interview Quick Check

**Q1. What is nested `if`?**  
A: An `if` statement inside another `if` statement.

**Q2. When is the inner condition evaluated?**  
A: Only when execution reaches the inner `if`, typically after the outer condition is true.

---

## 🔗 Navigation

⬅️ [if-else-if Ladder](./04-if-else-if-ladder.md)

➡️ [switch Statement](./06-switch-statement.md)

➡️ [Quick Revision](./07-conditional-statements-quick-revision.md)

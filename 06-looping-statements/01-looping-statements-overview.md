<a name="top"></a>

# 🔁 Java Looping Statements — Overview

> **Topic 13 • Java Fundamentals**

A **loop** repeatedly executes a block of code while a condition or iteration rule allows it to continue.

---

## 🎯 Why Use Loops?

Without a loop:

```java
System.out.println(1);
System.out.println(2);
System.out.println(3);
System.out.println(4);
System.out.println(5);
```

With a loop:

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

Loops reduce repetition and make repetitive logic easier to maintain.

---

## 🧠 Master Mnemonic

### **N-E-F-D-W**

| Letter | Loop |
|---|---|
| **N** | Nested loop |
| **E** | Enhanced `for` |
| **F** | `for` |
| **D** | `do-while` |
| **W** | `while` |

---

## 🧩 Main Loop Types

```text
                    LOOPS
                      │
        ┌─────────────┼─────────────┐
        │             │             │
     Entry-check   Exit-check    Element-based
        │             │             │
     for/while      do-while    enhanced for
        │
     Nested loops can
     contain other loops
```

---

## 📊 Quick Comparison

| Loop | Condition timing | Typical use |
|---|---|---|
| `for` | Before body | Structured/known iteration pattern |
| `while` | Before body | Condition-driven repetition |
| `do-while` | After body | Body must execute at least once |
| Enhanced `for` | Element iteration | Arrays and `Iterable` data |
| Nested loop | Depends on contained loops | Multi-level repetition |

---

## 🧠 Key Memory Line

**Same logic → Different loops → Choose the right one.**

---

## 🎤 Interview Quick Check

**Q1. What is a loop?**  
A: A control-flow construct used to repeatedly execute a block of code.

**Q2. Which loop guarantees at least one execution of its body?**  
A: `do-while`.

**Q3. Which loop is designed for iterating over elements without explicitly managing an index?**  
A: Enhanced `for`.

---

## 🔗 Navigation

➡️ [for Loop](./02-for-loop.md)

➡️ [while Loop](./03-while-loop.md)

➡️ [do-while Loop](./04-do-while-loop.md)

➡️ [Enhanced for Loop](./05-enhanced-for-loop.md)

➡️ [Nested Loops](./06-nested-loops.md)

➡️ [Quick Revision](./07-looping-statements-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

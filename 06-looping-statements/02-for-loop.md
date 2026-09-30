# 🔄 Java `for` Loop

> **Topic 13 • Java Fundamentals**

The `for` loop is useful when initialization, a continuation condition and an update step form a structured iteration pattern.

---

## 📌 Syntax

```java
for (initialization; condition; update) {
    // loop body
}
```

### Execution Order

```text
Initialization
      ↓
   Condition
      ↓
   ┌──┴──┐
  true  false
   │      │
 Body    Exit
   │
 Update
   │
   └──────→ Condition
```

The initialization runs once. The condition is checked before each iteration, and the update runs after the body.

---

## 💻 Example

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

Output:

```text
1
2
3
4
5
```

---

## 🧩 The Three Parts

| Part | Purpose |
|---|---|
| Initialization | Establishes the starting state |
| Condition | Decides whether another iteration should run |
| Update | Changes the loop state |

---

## 🧠 When to Use

A `for` loop is a natural choice when the iteration pattern is easy to express in one place.

Examples:

- Count from 1 to 100
- Iterate using an index
- Repeat a known number of times

> A `for` loop does not require a known number of iterations; its condition can depend on runtime state.

---

## 🎤 Interview Quick Check

**Q1. How many times does the initialization run?**  
A: Once, when the loop starts.

**Q2. When is the condition checked?**  
A: Before each iteration.

**Q3. When is the update executed?**  
A: After the loop body of each completed iteration.

---

## 🔗 Navigation

⬅️ [Looping Overview](./01-looping-statements-overview.md)

➡️ [while Loop](./03-while-loop.md)

➡️ [Quick Revision](./07-looping-statements-quick-revision.md)

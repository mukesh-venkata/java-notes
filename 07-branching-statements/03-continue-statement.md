<a name="top"></a>

# ⏭️ Java `continue` Statement

> **Topic 14 • Java Fundamentals**

The `continue` statement skips the remaining statements in the **current iteration** of a loop and proceeds with the next iteration.

---

## 💻 Example

```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        continue;
    }

    System.out.println(i);
}
```

Output:

```text
1
2
4
5
```

When `i == 3`, the print statement is skipped.

---

## 🔀 Execution Flow

```text
Loop iteration
      │
    continue?
    ├── No → remaining body → next iteration
    └── Yes
         ↓
   skip remaining body
         ↓
     next iteration
```

---

## 📌 Where Can It Be Used?

`continue` applies to loops:

- `for`
- `while`
- `do-while`

It is **not** a standalone statement for traditional `switch` control.

---

## 🔄 Important Difference in Loops

In a `for` loop, after `continue`, the update expression is still performed.

```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        continue;
    }
    System.out.println(i);
}
```

After `continue` at `i == 3`, Java proceeds to the `i++` update and then checks the condition again.

In a `while` or `do-while` loop, make sure the loop-control state is updated appropriately; otherwise, `continue` can accidentally create an infinite loop.

---

## 🪆 Labeled continue

Java also supports labeled `continue` for continuing an enclosing labeled loop.

```java
outer:
for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 3; j++) {
        if (j == 2) {
            continue outer;
        }
        System.out.println(i + " " + j);
    }
}
```

This skips to the next iteration of the loop labeled `outer`.

---

## 🧠 Memory Trick

```text
continue → SKIP
```

---

## 🎤 Interview Quick Check

**Q1. What does `continue` do?**  
A: It skips the remaining statements of the current loop iteration.

**Q2. Does `continue` terminate the loop?**  
A: No. The loop proceeds to its next iteration.

**Q3. What is important about `continue` in a `for` loop?**  
A: The update expression still runs after `continue`.

---

## 🔗 Navigation

⬅️ [break](./02-break-statement.md)

➡️ [return](./04-return-statement.md)

➡️ [Quick Revision](./05-branching-statements-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

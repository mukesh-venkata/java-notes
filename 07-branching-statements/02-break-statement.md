<a name="top"></a>

# 🛑 Java `break` Statement

> **Topic 14 • Java Fundamentals**

The `break` statement immediately terminates the nearest applicable **loop or switch statement**.

---

## 💻 Example

```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        break;
    }

    System.out.println(i);
}
```

Output:

```text
1
2
```

When `i == 3`, `break` exits the loop immediately.

---

## 🔀 Execution Flow

```text
Loop
 │
 ├── condition true
 │      ↓
 │    body
 │      ↓
 │   break?
 │    ├─ No → next iteration
 │    └─ Yes → EXIT LOOP
 │
 └── condition false → EXIT
```

---

## 📌 Where Can It Be Used?

### Loops

`break` can be used in:

- `for`
- `while`
- `do-while`

### switch

`break` can terminate a traditional `switch` statement.

---

## 🪆 Nested Loops

An unlabeled `break` exits the **nearest enclosing loop or switch**.

```java
for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 3; j++) {
        if (j == 2) {
            break;
        }
        System.out.println(i + " " + j);
    }
}
```

Here, `break` exits the inner loop, not the outer loop.

---

## 🏷️ Labeled break

Java also supports labeled `break` for exiting an enclosing labeled statement.

```java
outer:
for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 3; j++) {
        if (i == 2 && j == 2) {
            break outer;
        }
    }
}
```

This exits the loop labeled `outer`.

---

## 🧠 Memory Trick

```text
break → STOP
```

---

## 🎤 Interview Quick Check

**Q1. What does `break` do?**  
A: It terminates the nearest applicable loop or switch.

**Q2. What happens to an unlabeled `break` in nested loops?**  
A: It exits the nearest enclosing loop or switch.

**Q3. Can `break` be used outside a loop or switch?**  
A: Only as part of an applicable labeled statement; an ordinary unlabeled `break` outside a loop or switch is a compile-time error.

---

## 🔗 Navigation

⬅️ [Branching Overview](./01-branching-statements-overview.md)

➡️ [continue](./03-continue-statement.md)

➡️ [return](./04-return-statement.md)

➡️ [Quick Revision](./05-branching-statements-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

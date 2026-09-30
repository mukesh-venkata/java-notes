# 🔂 Java `do-while` Loop

> **Topic 13 • Java Fundamentals**

A `do-while` loop executes its body first and checks the condition **afterward**.

---

## 📌 Syntax

```java
do {
    // loop body
} while (condition);
```

> Notice the semicolon after the `while (condition)`.

---

## 💻 Example

```java
int i = 1;

do {
    System.out.println(i);
    i++;
} while (i <= 5);
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

## ⭐ Key Property

The body executes **at least once**, even if the condition is initially false.

```java
int i = 10;

do {
    System.out.println("Runs once");
} while (i < 5);
```

Output:

```text
Runs once
```

---

## 🔀 Flow

```text
      Body
       ↓
   Condition
       │
    ┌──┴──┐
   true  false
    │      │
    └──→ Body
           │
          Exit
```

---

## 🆚 while vs do-while

| Feature | `while` | `do-while` |
|---|---|---|
| Condition checked | Before body | After body |
| Minimum executions | 0 | 1 |
| Best remembered as | Check → Execute | Execute → Check |

---

## 🎤 Interview Quick Check

**Q1. Which loop executes at least once?**  
A: `do-while`.

**Q2. Why?**  
A: Its condition is evaluated after the body.

**Q3. What punctuation follows the condition?**  
A: A semicolon.

---

## 🔗 Navigation

⬅️ [while Loop](./03-while-loop.md)

➡️ [Enhanced for Loop](./05-enhanced-for-loop.md)

➡️ [Quick Revision](./07-looping-statements-quick-revision.md)

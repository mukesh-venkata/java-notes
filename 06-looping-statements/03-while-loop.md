<a name="top"></a>

# 🔁 Java `while` Loop

> **Topic 13 • Java Fundamentals**

A `while` loop repeatedly executes its body **while its condition is true**.

---

## 📌 Syntax

```java
while (condition) {
    // loop body
}
```

The condition is checked **before** each iteration.

---

## 💻 Example

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
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

## 🔀 Flow

```text
       Condition
          │
      ┌───┴───┐
     true    false
      │         │
    Body       Exit
      │
    Update
      │
      └────→ Condition
```

---

## ⚠️ Important

Because the condition is checked first, a `while` loop can execute **zero times**.

```java
int i = 10;

while (i < 5) {
    System.out.println(i);
}
```

The body never executes.

---

## ♾️ Infinite Loop Example

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    // missing update
}
```

If the condition never becomes false, the loop continues indefinitely.

---

## 🎤 Interview Quick Check

**Q1. When is the condition checked?**  
A: Before each iteration.

**Q2. Can a `while` loop execute zero times?**  
A: Yes.

**Q3. What commonly causes an unintended infinite loop?**  
A: The loop state is not changed so that the condition can eventually become false.

---

## 🔗 Navigation

⬅️ [for Loop](./02-for-loop.md)

➡️ [do-while Loop](./04-do-while-loop.md)

➡️ [Quick Revision](./07-looping-statements-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

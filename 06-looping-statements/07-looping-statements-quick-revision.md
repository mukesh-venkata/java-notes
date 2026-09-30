<a name="top"></a>

# ⚡ Java Looping Statements — Quick Revision

> **Topic 13 • 30-Second Revision**

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

## 📌 Syntax Cheat Sheet

### `for`

```java
for (initialization; condition; update) {
    // body
}
```

### `while`

```java
while (condition) {
    // body
}
```

### `do-while`

```java
do {
    // body
} while (condition);
```

### Enhanced `for`

```java
for (Type item : collectionOrArray) {
    // body
}
```

### Nested Loop

```java
for (...) {
    for (...) {
        // body
    }
}
```

---

## 🔥 Most Important Comparison

| Loop | Condition check | Minimum body executions |
|---|---|---:|
| `for` | Before | 0 |
| `while` | Before | 0 |
| `do-while` | After | 1 |
| Enhanced `for` | Iterates elements | Depends on source size |
| Nested loop | Depends on contained loops | Depends on bounds |

---

## 🧠 Choose the Loop

```text
Structured iteration?
       │
      Yes → for

Condition-driven repetition?
       │
      Yes → while

Must execute once first?
       │
      Yes → do-while

Just visit each element?
       │
      Yes → enhanced for

Multiple levels of repetition?
       │
      Yes → nested loop
```

---

## 🎤 Interview Questions & Answers

> **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Which loop checks before execution?</summary>
<br>

`for` and `while`.

</details>

<details>
<summary>Which loop checks after execution?</summary>
<br>

`do-while`.

</details>

<details>
<summary>Which loop runs at least once?</summary>
<br>

`do-while`.

</details>

<details>
<summary>Enhanced `for`?</summary>
<br>

Iterates over array elements or `Iterable` elements without explicit index management.

</details>

<details>
<summary>Nested loop?</summary>
<br>

A loop inside another loop.

</details>

<details>
<summary>Common two-level nested complexity?</summary>
<br>

O(n²), when both loops independently run n times.

</details>

## 🗺️ Final Memory Map

```text
                    JAVA LOOPS
                       │
       ┌───────────────┼────────────────┐
       │               │                │
    Entry-check     Exit-check      Element-based
       │               │                │
    for / while     do-while        enhanced for
       │
    Nested loops can
    combine any loops
```

---

## 🔗 Navigation

⬅️ [Looping Overview](./01-looping-statements-overview.md)

⬅️ [for Loop](./02-for-loop.md)

⬅️ [while Loop](./03-while-loop.md)

⬅️ [do-while Loop](./04-do-while-loop.md)

⬅️ [Enhanced for](./05-enhanced-for-loop.md)

⬅️ [Nested Loops](./06-nested-loops.md)

🏠 [Java Notes Home](../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

<a name="top"></a>

# ⚡ Java Conditional Statements — Quick Revision

> **Topic 12 • 30-Second Revision**

## 🧠 Master Mnemonic

### **N-I-E-I-S**

| Letter | Remember |
|---|---|
| **N** | Nested `if` |
| **I** | `if` |
| **E** | `if-else` |
| **I** | `if-else-if` |
| **S** | `switch` |

---

## 📌 Syntax Cheat Sheet

### `if`

```java
if (condition) {
    // action
}
```

### `if-else`

```java
if (condition) {
    // true
} else {
    // false
}
```

### `if-else-if`

```java
if (condition1) {
} else if (condition2) {
} else {
}
```

### Nested `if`

```java
if (condition1) {
    if (condition2) {
    }
}
```

### `switch`

```java
switch (value) {
    case 1:
        // action
        break;
    default:
        // fallback
}
```

---

## 🔀 Quick Comparison

| Construct | Best remembered as |
|---|---|
| `if` | One condition |
| `if-else` | Two paths |
| `if-else-if` | Multiple conditions |
| Nested `if` | Decision inside decision |
| `switch` | Multiple discrete cases |

---

## 🧠 SWITCH — FD-BD

```text
F → Fall-through
D → Default
B → Break
D → Decimal types not supported as traditional selectors
```

Traditional switch does not support `float` or `double` selectors.

---

## 🎤 Interview Questions & Answers

> **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Condition type?</summary>
<br>

Java `if` conditions must be boolean expressions.

</details>

<details>
<summary>`if-else`?</summary>
<br>

Provides two execution paths.

</details>

<details>
<summary>`if-else-if`?</summary>
<br>

Checks conditions from top to bottom.

</details>

<details>
<summary>Nested `if`?</summary>
<br>

An `if` inside another `if`.

</details>

<details>
<summary>Fall-through?</summary>
<br>

Traditional switch execution continues into later cases when not terminated.

</details>

<details>
<summary>`default`?</summary>
<br>

Executes when no case matches.

</details>

<details>
<summary>`break`?</summary>
<br>

Terminates the traditional switch.

</details>

<details>
<summary>Decimal selector?</summary>
<br>

`float` and `double` aren't supported as traditional switch selectors.

</details>

## 🗺️ Final Memory Map

```text
              CONDITIONAL STATEMENTS
                       │
          ┌────────────┴────────────┐
          │                         │
        if-family                switch
          │                         │
   ┌──────┼─────────┐        case / break
   │      │         │             │
  if    if-else   if-else-if    default
   │
 nested if
```

---

## 🔗 Navigation

⬅️ [Conditional Statements Overview](./01-conditional-statements-overview.md)

⬅️ [if](./02-if-statement.md)

⬅️ [if-else](./03-if-else-statement.md)

⬅️ [if-else-if](./04-if-else-if-ladder.md)

⬅️ [Nested if](./05-nested-if.md)

⬅️ [switch](./06-switch-statement.md)

🏠 [Java Notes Home](../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

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

## 🎤 Interview One-Liners

**Condition type?** → Java `if` conditions must be boolean expressions.

**`if-else`?** → Provides two execution paths.

**`if-else-if`?** → Checks conditions from top to bottom.

**Nested `if`?** → An `if` inside another `if`.

**Fall-through?** → Traditional switch execution continues into later cases when not terminated.

**`default`?** → Executes when no case matches.

**`break`?** → Terminates the traditional switch.

**Decimal selector?** → `float` and `double` aren't supported as traditional switch selectors.

---

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

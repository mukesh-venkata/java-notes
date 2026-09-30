<a name="top"></a>

# 🔤 Java Scanner — `next()` vs `nextLine()`

> **Topic 17 • Scanner**

The difference between `next()` and `nextLine()` is one of the most important Scanner concepts for beginners.

---

## 1️⃣ `next()`

`next()` returns the next token, typically stopping at whitespace.

```java
String name = sc.next();
```

Input:

```text
Mukesh Pilla
```

Result:

```text
Mukesh
```

---

## 2️⃣ `nextLine()`

`nextLine()` advances past the current line and returns the input that was skipped, excluding the line separator.

```java
String name = sc.nextLine();
```

Input:

```text
Mukesh Pilla
```

Result:

```text
Mukesh Pilla
```

---

## 🆚 Comparison

| Method | Reads |
|---|---|
| `next()` | Next token |
| `nextLine()` | Remaining input on the current line |

---

## 🔀 Visual

```text
Input:
Mukesh Pilla
      ↑
    space

next()
  ↓
Mukesh

nextLine()
  ↓
Mukesh Pilla
```

---

## ⚠️ Important Nuance

The behavior of `nextLine()` depends on where the Scanner's cursor currently is.

For example, after a token-based method such as `next()`, the line separator remains unread. Calling `nextLine()` may therefore return the remaining text on that line, which can be an empty string if only the line separator remains.

This is the reason the common `nextInt()` + `nextLine()` issue occurs.

---

## 🎤 Interview Quick Check

**Q1. What does `next()` read?**  
A: The next token.

**Q2. What does `nextLine()` read?**  
A: The remaining input on the current line, excluding the line separator.

**Q3. Which should you use for a full name containing spaces?**  
A: Usually `nextLine()`.

---

## 🔗 Navigation

⬅️ [Scanner Overview](./01-scanner-overview.md)

➡️ [Numeric Input](./03-scanner-numeric-input.md)

➡️ [nextInt() + nextLine() Problem](./05-nextint-nextline-problem.md)

➡️ [Quick Revision](./06-scanner-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

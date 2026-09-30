# 🧩 Java Scanner — Other Input Methods

> **Topic 17 • Scanner**

Besides text and numeric methods, Scanner provides methods for reading other primitive types and checking available input.

---

## 🔘 Boolean Input

Use:

```java
boolean active = sc.nextBoolean();
```

The next token must be recognizable as a boolean value according to Scanner's boolean parsing rules; otherwise an input mismatch can occur.

---

## 🔎 Checking Input Before Reading

Useful methods include:

```java
sc.hasNext()
sc.hasNextLine()
sc.hasNextInt()
sc.hasNextLong()
sc.hasNextDouble()
```

Example:

```java
if (sc.hasNextInt()) {
    int age = sc.nextInt();
}
```

This can help avoid attempting a numeric read when the next token is not an integer.

---

## 📊 Quick Table

| Method | Purpose |
|---|---|
| `nextBoolean()` | Reads a boolean |
| `hasNext()` | Checks whether another token is available |
| `hasNextLine()` | Checks whether another line is available |
| `hasNextInt()` | Checks whether the next token can be read as an int |
| `hasNextLong()` | Checks for a long-compatible token |
| `hasNextDouble()` | Checks for a double-compatible token |

---

## 🎤 Interview Quick Check

**Q1. Which method reads a boolean?**  
A: `nextBoolean()`.

**Q2. Why use `hasNextInt()`?**  
A: To check whether the next token can be interpreted as an integer before calling `nextInt()`.

**Q3. What does `hasNextLine()` check?**  
A: Whether another line is available in the input.

---

## 🔗 Navigation

⬅️ [Numeric Input](./03-scanner-numeric-input.md)

➡️ [nextInt() + nextLine() Problem](./05-nextint-nextline-problem.md)

➡️ [Quick Revision](./06-scanner-quick-revision.md)

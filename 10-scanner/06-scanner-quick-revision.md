<a name="top"></a>

# ⚡ Java Scanner — Quick Revision

> **Topic 17 • 30-Second Revision**

## 🛠️ Setup

```java
import java.util.Scanner;

Scanner sc = new Scanner(System.in);
```

---

## 🧠 Method Memory Map

```text
Scanner
   │
   ├── next()        → next token
   ├── nextLine()    → remaining current line
   ├── nextInt()     → int
   ├── nextLong()    → long
   ├── nextFloat()   → float
   ├── nextDouble()  → double
   ├── nextShort()   → short
   ├── nextByte()    → byte
   └── nextBoolean() → boolean
```

---

## 📊 Quick Table

| Method | Reads |
|---|---|
| `next()` | Next token |
| `nextLine()` | Remaining current line |
| `nextInt()` | `int` |
| `nextLong()` | `long` |
| `nextFloat()` | `float` |
| `nextDouble()` | `double` |
| `nextShort()` | `short` |
| `nextByte()` | `byte` |
| `nextBoolean()` | `boolean` |

---

## 🚨 Golden Rule

```text
nextInt()
   ↓
newline may remain
   ↓
nextLine()
   ↓
may consume remaining newline
```

Common fix:

```java
int age = sc.nextInt();
sc.nextLine();
String name = sc.nextLine();
```

---

## 🧠 Three Things to Remember

**1. Scanner package** → `java.util.Scanner`

**2. Keyboard input source** → commonly `System.in`

**3. Full line** → `nextLine()`

---

## 🎤 Interview Questions & Answers

> **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Scanner?</summary>
<br>

A utility class commonly used to parse input from sources such as standard input.

</details>

<details>
<summary>`next()`?</summary>
<br>

Reads the next token.

</details>

<details>
<summary>`nextLine()`?</summary>
<br>

Reads the remaining input on the current line.

</details>

<details>
<summary>`nextInt()`?</summary>
<br>

Reads the next integer token.

</details>

<details>
<summary>Why does `nextInt()` + `nextLine()` cause trouble?</summary>
<br>

The line separator after the integer may remain, so `nextLine()` can consume the rest of that line immediately.

</details>

<details>
<summary>Does Scanner only read keyboard input?</summary>
<br>

No. It can parse other input sources such as strings, files and streams.

</details>

## 🔗 Navigation

⬅️ [Scanner Overview](./01-scanner-overview.md)

⬅️ [next() vs nextLine()](./02-scanner-next-and-nextline.md)

⬅️ [Numeric Input](./03-scanner-numeric-input.md)

⬅️ [Other Input Methods](./04-scanner-other-input-methods.md)

⬅️ [nextInt() + nextLine()](./05-nextint-nextline-problem.md)

🏠 [Java Notes Home](../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

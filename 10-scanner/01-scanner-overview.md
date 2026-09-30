<a name="top"></a>

# ⌨️ Java Scanner — Overview

> **Topic 17 • User Input**

The Java **Scanner** class is commonly used to read input from sources such as the keyboard.

---

## 📌 Import Scanner

```java
import java.util.Scanner;
```

Scanner belongs to the `java.util` package.

---

## 🛠️ Create a Scanner Object

```java
Scanner sc = new Scanner(System.in);
```

Here:

| Part | Meaning |
|---|---|
| `Scanner` | Scanner class |
| `sc` | Reference variable |
| `new Scanner(...)` | Creates a Scanner object |
| `System.in` | Standard input stream |

---

## 🔀 Input Flow

```text
Keyboard
   ↓
System.in
   ↓
Scanner
   ↓
Java Program
```

### What is `System.in`?

`System.in` represents Java's **standard input stream**.

When running a console program, it is commonly connected to keyboard/console input.

Scanner reads from that input source.

---

## 💻 Simple Example

```java
import java.util.Scanner;

class UserInput {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your name: ");
        String name = sc.nextLine();

        System.out.println("Hello, " + name);
    }
}
```

---

## 🧹 Closing Scanner

When a Scanner is created over `System.in`, closing the Scanner also closes the underlying input stream.

For short console programs this may be fine at program termination. In larger applications, avoid closing a shared `System.in` prematurely if more input is still required.

---

## 🎤 Interview Quick Check

**Q1. Which package contains Scanner?**  
A: `java.util`.

**Q2. What does `System.in` represent?**  
A: The standard input stream.

**Q3. What does `new Scanner(System.in)` do?**  
A: Creates a Scanner that reads from the standard input stream.

---

## 🔗 Navigation

➡️ [next() vs nextLine()](./02-scanner-next-and-nextline.md)

➡️ [Numeric Input](./03-scanner-numeric-input.md)

➡️ [Other Input Methods](./04-scanner-other-input-methods.md)

➡️ [nextInt() + nextLine() Problem](./05-nextint-nextline-problem.md)

➡️ [Quick Revision](./06-scanner-quick-revision.md)

🏠 [Java Notes Home](../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

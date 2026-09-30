# ⚠️ Java Scanner — `nextInt()` + `nextLine()` Problem

> **Topic 17 • Scanner**

One of the most common Scanner mistakes happens when a token-reading method such as `nextInt()` is followed immediately by `nextLine()`.

---

## ❌ Common Problem

```java
int age = sc.nextInt();
String name = sc.nextLine();
```

Suppose the input is:

```text
25
Mukesh Pilla
```

After `nextInt()` reads `25`, the line separator after the number remains unread.

Then `nextLine()` consumes that remaining line separator and can return an empty string.

---

## 🔀 What Actually Happens?

```text
Input buffer
┌──────────────────────┐
│ 25 \n Mukesh Pilla   │
└──────────────────────┘
      ↑
  nextInt()
      ↓
reads 25
      ↓
newline remains
      ↓
  nextLine()
      ↓
consumes newline
      ↓
returns ""
```

The issue is about the Scanner's current position in the input, not about `nextInt()` being "broken".

---

## ✅ Common Fix

Consume the rest of the current line first:

```java
int age = sc.nextInt();
sc.nextLine();

String name = sc.nextLine();

System.out.println(age);
System.out.println(name);
```

---

## 💻 Full Example

```java
import java.util.Scanner;

class UserDetails {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter age: ");
        int age = sc.nextInt();
        sc.nextLine();

        System.out.print("Enter full name: ");
        String name = sc.nextLine();

        System.out.println("Age: " + age);
        System.out.println("Name: " + name);
    }
}
```

---

## 🔑 Memory Rule

> **Token read → newline may remain → nextLine() consumes the rest of the current line.**

This is why you will often see:

```java
sc.nextInt();
sc.nextLine();
```

before reading a full line.

---

## 🧠 Alternative Approach

If your input design is line-oriented, another approach is to read everything with `nextLine()` and convert the text:

```java
int age = Integer.parseInt(sc.nextLine());
```

This can make cursor behavior easier to reason about in some console programs.

---

## 🎤 Interview Quick Check

**Q1. Why can `nextLine()` return an empty string after `nextInt()`?**  
A: Because the line separator remains after the integer token, and `nextLine()` consumes the rest of that line.

**Q2. What is the common fix?**  
A: Call `nextLine()` once to consume the remainder of the current line before reading the next full line.

**Q3. Is this a Scanner bug?**  
A: No. It follows the different token/line-reading semantics of the methods.

---

## 🔗 Navigation

⬅️ [Numeric Input](./03-scanner-numeric-input.md)

⬅️ [next() vs nextLine()](./02-scanner-next-and-nextline.md)

➡️ [Quick Revision](./06-scanner-quick-revision.md)

🏠 [Java Notes Home](../README.md)

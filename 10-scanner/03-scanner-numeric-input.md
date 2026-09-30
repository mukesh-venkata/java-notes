# 🔢 Java Scanner — Numeric Input

> **Topic 17 • Scanner**

Scanner provides methods for reading primitive numeric values directly.

---

## 📊 Common Numeric Methods

| Method | Return type | Reads |
|---|---|---|
| `nextByte()` | `byte` | Byte value |
| `nextShort()` | `short` | Short value |
| `nextInt()` | `int` | Integer value |
| `nextLong()` | `long` | Long value |
| `nextFloat()` | `float` | Floating-point value |
| `nextDouble()` | `double` | Double value |

---

## 💻 Examples

```java
int age = sc.nextInt();

long population = sc.nextLong();

float price = sc.nextFloat();

double salary = sc.nextDouble();

short marks = sc.nextShort();

byte value = sc.nextByte();
```

---

## 🧩 Complete Example

```java
Scanner sc = new Scanner(System.in);

System.out.print("Enter age: ");
int age = sc.nextInt();

System.out.print("Enter salary: ");
double salary = sc.nextDouble();

System.out.println(age);
System.out.println(salary);
```

---

## ⚠️ Invalid Input

The input must be compatible with the expected type.

For example:

```java
int age = sc.nextInt();
```

If the next input token cannot be interpreted as an integer, Scanner can throw an `InputMismatchException`.

We will study exception handling separately.

---

## 🧠 Memory Trick

```text
next + Type
     ↓
nextInt    → int
nextLong   → long
nextFloat  → float
nextDouble → double
```

---

## 🎤 Interview Quick Check

**Q1. Which method reads an `int`?**  
A: `nextInt()`.

**Q2. Which method reads a `double`?**  
A: `nextDouble()`.

**Q3. What can happen when input does not match the requested numeric type?**  
A: Scanner can throw `InputMismatchException`.

---

## 🔗 Navigation

⬅️ [next() vs nextLine()](./02-scanner-next-and-nextline.md)

➡️ [Other Input Methods](./04-scanner-other-input-methods.md)

➡️ [nextInt() + nextLine() Problem](./05-nextint-nextline-problem.md)

➡️ [Quick Revision](./06-scanner-quick-revision.md)

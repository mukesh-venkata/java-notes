<a name="top"></a>

# 🔒 1. `final` Keyword & Final Variables

> **Core idea:** `final` adds a restriction so something cannot be changed in a particular way after it is finalized.

---

## 🧠 What is `final`?

The `final` keyword is used to restrict:

- 🔒 **Modification** of variables
- 🚫 **Overriding** of methods
- 🧬 **Inheritance/extension** of classes

Think:

> **final = “This cannot be changed in this way.”**

Java applies a different restriction depending on where `final` is used.

| Usage | Restriction |
|---|---|
| `final` variable | Cannot be reassigned |
| `final` method | Cannot be overridden |
| `final` class | Cannot be extended |

---

## 1️⃣ Final Variable

A **final variable cannot be reassigned after it has been initialized**.

### Example

```java
final int age = 27;

age = 30;   // ❌ Compilation error
```

### What happens?

1. `age` is declared as `final`.
2. It receives the value `27`.
3. A second assignment is attempted.
4. Java rejects the reassignment.

```text
final int age = 27;
        ↓
   value assigned
        ↓
   🔒 locked from reassignment
        ↓
age = 30  ❌
```

---

## 2️⃣ Final Variables Must Be Initialized

A final variable must receive a value before it is used.

### Valid

```java
final int age;
age = 27;

System.out.println(age);
```

The important rule is:

> A final variable must be definitely assigned exactly once before it is read.

### Invalid

```java
final int age;

System.out.println(age);  // ❌ Not initialized
```

---

## 3️⃣ Final Variables and Constants

Final variables are commonly used to represent values that should not be reassigned.

For constants, Java commonly uses:

```java
static final double PI = 3.14159;
static final int MAX_USERS = 100;
```

By convention, constant names are written in **UPPER_SNAKE_CASE**.

### Example

```java
class MathConfig {
    static final double PI = 3.14159;
    static final int MAX_USERS = 100;
}
```

---

## ⚠️ Important: Final Reference vs Object Mutation

For a reference variable, `final` prevents the **reference from being reassigned**. It does not automatically make the referenced object immutable.

```java
final StringBuilder builder = new StringBuilder("Java");

builder.append(" Notes");   // ✅ Allowed

builder = new StringBuilder("New");  // ❌ Reassignment
```

So:

```text
final reference
     │
     ├── reference cannot point to another object ❌
     │
     └── referenced object may still be mutable ✅
```

This distinction is important in interviews.

---

## 🧠 Memory Trick

> **Final Variable → Value/reference cannot be reassigned**

For a reference:

> **final locks the reference, not necessarily the object.**

---

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. Can a final variable be reassigned?</summary>
<br>

No. Once definitely assigned, it cannot be assigned again.

</details>

<details>
<summary>Q2. Can a final variable be initialized later?</summary>
<br>

Yes, provided it is definitely assigned before it is read and is assigned only once.

</details>

<details>
<summary>Q3. Does a final reference make an object immutable?</summary>
<br>

No. final prevents reassignment of the reference; the object's own mutability depends on its class and state.

</details>

<details>
<summary>Q4. How are constants commonly declared?</summary>
<br>

Using static final, for example static final int MAX_SIZE = 100.

</details>
## ⚡ Quick Revision

| Rule | Remember |
|---|---|
| Final variable | Cannot be reassigned |
| Initialization | Must happen before use |
| Constant | Commonly `static final` |
| Final reference | Reference cannot be reassigned |
| Object behind final reference | May still be mutable |

---

## 🔗 Related Notes

- [Final Method →](02-final-method.md)
- [Final Class →](03-final-class.md)
- [Final Keyword Quick Revision →](04-final-keyword-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

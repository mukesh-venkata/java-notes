<a name="top"></a>

# 🧩 Types of Constructors in Java

> **Topic 21 • Constructors**

Java constructor discussions commonly use four terms:

1. Compiler-provided default constructor
2. User-defined constructor
3. No-argument constructor
4. Parameterized constructor

The most important distinction is between a **compiler-provided default constructor** and a **user-defined no-argument constructor**.

---

# 1️⃣ Compiler-Provided Default Constructor

If you declare **no constructor at all** in a class, the Java compiler implicitly provides a default constructor, subject to the Java Language Specification's rules.

Example:

```java
class Student {
    int age;
}
```

You did not write a constructor.

Conceptually, the class gets a no-argument constructor equivalent in effect to:

```java
Student() {
    super();
}
```

Its accessibility is based on the class's accessibility.

You can therefore write:

```java
Student s = new Student();
```

### ⚠️ Important

The compiler-provided default constructor is available **only when you do not declare any constructor**.

If you write even one constructor:

```java
class Student {

    Student(int age) {
        this.age = age;
    }

    int age;
}
```

the compiler does **not** also provide a no-argument default constructor.

So this will fail:

```java
new Student();
```

unless you explicitly provide a no-argument constructor.

---

# 2️⃣ User-Defined Constructor

A **user-defined constructor** is explicitly written by the programmer.

```java
class Student {

    Student() {
        System.out.println("Student created");
    }
}
```

Here, the constructor is written by the programmer.

It can contain initialization logic:

```java
class Student {

    int age;

    Student() {
        age = 18;
    }
}
```

This is a **user-defined no-argument constructor**.

> It is not the same thing as the compiler-provided default constructor.

---

# 3️⃣ No-Argument Constructor

A no-argument constructor has **zero parameters**.

```java
class Student {

    Student() {
        System.out.println("No-argument constructor");
    }
}
```

A no-argument constructor may be:

- Compiler-provided, if you declare no constructor.
- User-defined, if you explicitly write one.

### 🧠 Key Point

```text
No-argument = zero parameters

Default = compiler-provided when no constructor is declared
```

Therefore:

> Every compiler-provided default constructor is a no-argument constructor, but not every no-argument constructor is compiler-provided.

---

# 4️⃣ Parameterized Constructor

A parameterized constructor accepts one or more parameters.

```java
class Student {

    int age;

    Student(int age) {
        this.age = age;
    }
}
```

Creating the object:

```java
Student s = new Student(27);
```

The value `27` is passed to the constructor and used to initialize the object's state.

Another example:

```java
class Student {

    int age;
    String name;

    Student(int age, String name) {
        this.age = age;
        this.name = name;
    }
}
```

---

# 5️⃣ Constructor Types — Comparison

| Type | Parameters | Written by | Key Point |
|---|---:|---|---|
| Compiler-provided default | 0 | Compiler implicitly | Exists when no constructor is declared |
| User-defined no-arg | 0 | Programmer | Explicitly written |
| Parameterized | 1+ | Programmer | Accepts initialization values |

## 6️⃣ Common Confusion

### ❌ Incorrect

> “If I don't write a no-argument constructor, Java always gives me one.”

### ✅ Correct

Java provides the default constructor only when **no constructor declaration exists**.

### Example

```java
class Student {

    Student(int age) {
    }
}
```

There is no compiler-provided `Student()`.

To support:

```java
new Student();
```

you must explicitly define:

```java
Student() {
}
```

---

# 7️⃣ Quick Mental Model

```text
No constructor declared
        ↓
Compiler-provided default constructor

Constructor explicitly declared
        ↓
No automatic default constructor
        ↓
Define no-arg constructor yourself if needed
```

## 🎤 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. When does Java provide a default constructor?</summary>
<br>

When the class declares no constructor, the compiler provides a default no-argument constructor, subject to the class's access context.

</details>

<details>
<summary>Q2. Is a user-defined no-argument constructor a default constructor?</summary>
<br>

It is a no-argument constructor, but it is not the compiler-provided default constructor.

</details>

<details>
<summary>Q3. What happens when you declare only a parameterized constructor?</summary>
<br>

No compiler-provided no-argument constructor is added.

</details>

<details>
<summary>Q4. What is a parameterized constructor?</summary>
<br>

A constructor that accepts one or more parameters.

</details>
## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

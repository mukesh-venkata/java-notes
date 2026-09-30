<a name="top"></a>

# 🆕 2. Object Creation Using the new Operator

> **Core idea:** The `new` operator is the normal way to create an object when the class and constructor are known.

## 🧠 Basic Syntax

```java
Student student = new Student();
```

Here:

- `Student` → reference type
- `student` → reference variable
- `new Student()` → creates the object and invokes the constructor

Conceptually:

```text
Student student = new Student();
       ↓              ↓
 reference        object creation
                    +
                 constructor
```

## 🔄 What Happens?

When an object is created using `new`, Java performs object initialization and constructor invocation as part of the creation process.

A simplified view is:

```text
new Student()
     ↓
Object creation
     ↓
Constructor invocation
     ↓
Initialized object
     ↓
Reference stored in student
```

## 📌 Example

```java
class Student {
    Student() {
        System.out.println("Constructor called");
    }
}

Student student = new Student();
```

Output:

```text
Constructor called
```

## 🎯 Why Is new Common?

- Easy to read.
- Type-safe at compile time.
- Uses the constructor explicitly written for the class.
- Supports normal constructor overloading.

For example:

```java
Student s1 = new Student();
Student s2 = new Student("Alex", 27);
```

assuming matching constructors exist.

## ⚠️ Important

The `new` operator is not itself a method call. The constructor is invoked as part of the object creation expression.

Also, a reference variable and the object are different concepts:

```text
student  ─────────→  Student object
reference             object
```

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What is the most common way to create an object?</summary>
<br>

Using the new operator with a class constructor.

</details>

<details>
<summary>Q2. Does new invoke a constructor?</summary>
<br>

Yes. A class instance creation expression selects and invokes a constructor.

</details>

<details>
<summary>Q3. Is the reference variable the object?</summary>
<br>

No. The reference variable stores a reference to an object; it is not the object itself.

</details>
## 🔗 Related Notes

- [Overview →](01-object-creation-overview.md)
- [clone() & Shallow Copy →](03-clone-and-shallow-copy.md)
- [Reflection →](04-reflection-object-creation.md)
- [Comparison →](06-object-creation-comparison.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

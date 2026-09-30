<a name="top"></a>

# 🏗️ Java Class vs Object

> **Topic 15 • OOP Introduction**

Class and object are related, but they are not the same thing.

---

## 📘 Class

A **class** defines a type.

It can contain:

- Fields
- Methods
- Constructors
- Initializers
- Nested types

Example:

```java
class Student {
    String name;
    int age;

    void display() {
        System.out.println(name + " " + age);
    }
}
```

Think:

> **Class = blueprint/type definition**

---

## 🧩 Object

An **object** is an instance of a class.

```java
Student s = new Student();
```

Here:

- `Student` → class/type
- `s` → reference variable
- `new Student()` → object creation expression
- The resulting object → instance of `Student`

---

## 🔀 Class → Object

```text
             Student
               │
          class definition
               │
        ┌──────┴──────┐
        ↓             ↓
     Object 1       Object 2
      name=A          name=B
      age=20          age=25
```

Multiple objects can be created from the same class.

---

## 📊 Comparison

| Class | Object |
|---|---|
| Defines a type | Instance of a type |
| Describes possible state/behavior | Has actual state |
| Used as a template/type definition | Created from a class |
| Example: `Student` | Example: `new Student()` |

---

## ⚠️ Important Terminology

Do not confuse:

```java
Student s = new Student();
```

with the statement:

> "s is the object."

More precisely:

- `s` is a **reference variable**
- `new Student()` creates the **object**
- `s` refers to that object

---

## 🎤 Interview Quick Check

**Q1. What is a class?**  
A: A type definition that describes state and behavior.

**Q2. What is an object?**  
A: An instance of a class.

**Q3. What is the difference between a reference and an object?**  
A: A reference variable holds a reference to an object; the object is the runtime instance itself.

---

## 🔗 Navigation

⬅️ [Four Pillars](./02-four-pillars.md)

➡️ [Object Basics](./04-object-basics.md)

➡️ [Quick Revision](./05-oops-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

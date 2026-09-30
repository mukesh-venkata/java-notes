# ☕ Java OOP — Introduction

> **Topic 15 • Object-Oriented Programming**

## 🎯 What Is OOP?

**Object-Oriented Programming (OOP)** is a programming approach that organizes software around **objects**, which combine state (data) and behavior (methods).

Java is a strongly object-oriented language with primitive types as a notable exception.

---

## 💡 Why OOP?

OOP helps organize larger programs around meaningful entities and responsibilities.

Common goals include:

- 🧩 Modularity
- ♻️ Reusability
- 🔒 Controlled access to data
- 🛠️ Maintainability
- 📈 Extensibility

Think:

```text
Real-world entity
      ↓
    Object
      ↓
 State + Behavior
      ↓
 Organized program
```

---

## 🧠 The Four Pillars

### Memory Trick: **A-E-I-P**

| Letter | Pillar | Core idea |
|---|---|---|
| **A** | Abstraction | Hide unnecessary implementation details |
| **E** | Encapsulation | Bundle data + behavior and control access |
| **I** | Inheritance | Derive a class from another class |
| **P** | Polymorphism | One interface/reference, different behaviors |

```text
                 OOP
                  │
       ┌──────────┼──────────┐
       │          │          │
 Abstraction Encapsulation Inheritance
       │          │          │
       └──────────┼──────────┘
                  │
            Polymorphism
```

These are **foundational ideas**, not the entire OOP syllabus.

---

## 🏗️ Class → Object

A **class** defines a type and describes its possible state and behavior.

An **object** is an instance of a class.

```text
        Class
   ┌──────────────┐
   │ Student      │
   │ name          │
   │ age           │
   │ study()       │
   └──────┬───────┘
          │
       creates
          ↓
       Object
   ┌──────────────┐
   │ Student      │
   │ Mukesh       │
   │ 27            │
   └──────────────┘
```

---

## 💻 Simple Example

```java
class Student {
    String name;

    void study() {
        System.out.println(name + " is studying");
    }
}

Student student = new Student();
student.name = "Mukesh";
student.study();
```

Here:

- `Student` → class
- `student` → reference variable
- `new Student()` → creates an object
- `name` → instance field
- `study()` → instance method

---

## 🧠 OOP Learning Path

This introduction gives the map. We will study each area deeply later:

```text
OOP Introduction
       ↓
Classes & Objects
       ↓
Encapsulation
       ↓
Inheritance
       ↓
Polymorphism
       ↓
Abstraction
       ↓
Constructors / this / super
       ↓
Object class / equals / hashCode
       ↓
Composition / Advanced OOP
```

---

## 🎤 Interview Quick Check

**Q1. What is OOP?**  
A: A programming approach that organizes software around objects containing state and behavior.

**Q2. What are the four commonly taught pillars of OOP?**  
A: Abstraction, Encapsulation, Inheritance and Polymorphism.

**Q3. Is a class the same as an object?**  
A: No. A class defines a type; an object is an instance of that class.

---

## 🔗 Navigation

➡️ [Four Pillars](./02-four-pillars.md)

➡️ [Class vs Object](./03-class-vs-object.md)

➡️ [Object Basics](./04-object-basics.md)

➡️ [Quick Revision](./05-oops-quick-revision.md)

🏠 [Java Notes Home](../../README.md)

# 🧩 Java Object Basics

> **Topic 15 • OOP Introduction**

An object is a runtime instance of a class.

Objects allow programs to work with the state and behavior defined by their class.

---

## 🛠️ Creating an Object

```java
Student s = new Student();
```

Conceptually:

```text
Student
   │
   ├── type
   │
   └── new Student()
          ↓
       Object
          ↑
          │
          s
     reference variable
```

---

## 📌 Accessing Members

If `s` refers to a `Student` object:

```java
s.age = 20;
s.display();
```

The dot operator accesses accessible members through the reference.

---

## 🧠 Object State vs Behavior

```java
class Student {
    String name;      // state

    void study() {    // behavior
        System.out.println("Studying");
    }
}
```

Think:

```text
Object
 ├── State      → fields/data
 └── Behavior   → methods
```

---

## 🗄️ Memory Note

In common JVM implementations, objects are generally allocated in the **heap**.

The exact runtime representation and memory layout are implementation details of the JVM.

Do not reduce Java memory management to the oversimplified rule:

> "Reference = stack, object = heap."

Local variables and references can be optimized or represented differently by the JVM, while the Java language specification does not mandate a simple stack/heap mapping for every variable.

---

## 🔢 hashCode() — First Introduction

Every Java object inherits methods from `Object`, including:

```java
hashCode()
```

Example:

```java
Student s = new Student();
System.out.println(s.hashCode());
```

### Important

A hash code is **not guaranteed to be unique**.

Different objects can have the same hash code.

For objects that are considered equal according to `equals()`, Java's contract requires them to return the same hash code.

We will study:

- `Object`
- `equals()`
- `hashCode()`
- Their contracts and practical use

in a dedicated advanced section later.

---

## 🎤 Interview Quick Check

**Q1. What is an object?**  
A: A runtime instance of a class.

**Q2. Where are objects generally allocated in common JVM implementations?**  
A: The heap.

**Q3. Is `hashCode()` guaranteed to be unique for every object?**  
A: No.

---

## 🔗 Navigation

⬅️ [Class vs Object](./03-class-vs-object.md)

➡️ [Quick Revision](./05-oops-quick-revision.md)

🏠 [Java Notes Home](../../README.md)

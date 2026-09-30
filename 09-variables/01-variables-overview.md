<a name="top"></a>

# 📦 Java Variables — Overview

> **Topic 16 • Java Fundamentals**

A **variable** is a named storage location used by a program to hold a value.

---

## 🎯 What Do We Need to Understand About a Variable?

When studying a variable, remember these six ideas:

```text
Declaration
    ↓
Initialization
    ↓
Default Value
    ↓
Access
    ↓
Memory
    ↓
Scope
```

---

## 🧩 Three Main Variable Categories

```text
                    VARIABLES
                        │
          ┌─────────────┼─────────────┐
          ↓             ↓             ↓
       STATIC        INSTANCE        LOCAL
       (Class)       (Object)       (Scope)
          │             │             │
       shared        per object    per execution
```

### 1. Class / Static Variable

Declared with `static`.

```java
class Counter {
    static int count;
}
```

Associated with the class rather than a particular object.

### 2. Instance Variable

A field declared inside a class but outside methods, constructors and initializer blocks.

```java
class Student {
    int age;
}
```

Each object has its own instance state.

### 3. Local Variable

Declared inside a method, constructor, or block.

```java
void display() {
    int age = 20;
}
```

Its scope is limited to the relevant method/constructor/block.

---

## 🧠 Default Values

Fields receive default values when they are not explicitly initialized.

Common examples:

| Type | Default |
|---|---|
| Integer types | `0` |
| `float` / `double` | `0.0` / `0.0d` |
| `boolean` | `false` |
| `char` | `'\\u0000'` |
| Reference types | `null` |

### ⚠️ Local Variables

Local variables **do not receive automatic default values**.

They must be definitely assigned before they are read.

---

## 🧠 Memory Note

Avoid memorizing an overly rigid rule such as:

> "Every static variable is in the Method Area and every local variable is on the stack."

The Java language specification does not prescribe one universal memory layout.

For learning:

- Instance fields are part of object state.
- Static fields are associated with the class.
- Local variables are associated with a method/block execution.
- Exact storage and optimization are JVM implementation details.

---

## 🎤 Interview Quick Check

**Q1. What is a variable?**  
A: A named storage location used to hold a value.

**Q2. What are the three common categories of Java variables?**  
A: Static/class variables, instance variables and local variables.

**Q3. Which variables receive default values automatically?**  
A: Fields, including static and instance fields. Local variables must be definitely assigned before use.

---

## 🔗 Navigation

➡️ [Static Variables](./02-class-static-variables.md)

➡️ [Instance Variables](./03-instance-variables.md)

➡️ [Local Variables](./04-local-variables.md)

➡️ [Comparison & Quick Revision](./05-variables-comparison-quick-revision.md)

🏠 [Java Notes Home](../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

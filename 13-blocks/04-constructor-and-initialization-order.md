# 🏗️ Java Constructor & Initialization Order

> **Topic 20 • Blocks**

Constructors, static initialization and instance initialization work together during class initialization and object construction.

## 1️⃣ Class Initialization

When a class is initialized, its static initialization occurs.

```text
Class initialization
      ↓
Static field initializers / static blocks
      ↓
Class initialization completes
```

Static initialization occurs once for a given class initialization.

## 2️⃣ Object Construction

When an object is created, instance initialization occurs before the constructor body.

```text
Object creation
      ↓
Instance field initializers / instance initialization blocks
      ↓
Constructor body
```

Instance field initializers and instance initialization blocks execute in their textual order.

## 💻 Example

```java
class Student {
    static {
        System.out.println("Static");
    }

    int age = 20;

    {
        System.out.println("Instance Block");
    }

    Student() {
        System.out.println("Constructor");
    }
}
```

After class initialization has occurred, conceptually:

```text
new Student()
      ↓
instance field initialization
      ↓
instance initialization block
      ↓
constructor body
```

## 🧬 Inheritance

A useful simplified mental model is:

```text
Class initialization
    ↓
Superclass initialization
    ↓
Subclass initialization

Object construction
    ↓
Superclass instance initialization
    ↓
Superclass constructor
    ↓
Subclass instance initialization
    ↓
Subclass constructor
```

The full Java Language Specification rules are more detailed, especially around explicit constructor invocation and field initializers.

## ⚠️ Important

Do not memorize static initialization and object construction as one uninterrupted sequence.

**Static initialization belongs to class initialization.**  
**Instance initialization and constructors belong to object construction.**

## 🎤 Interview Quick Check

**When does static initialization happen?** During class initialization.

**When does an instance initialization block run?** During object construction, before the constructor body for that class.

**What runs before the constructor body?** Instance field initializers and instance initialization blocks for that class.

## 🔗 Navigation

⬅️ [Blocks Overview](./01-blocks-overview.md)  
⬅️ [Static Block](./02-static-block.md)  
⬅️ [Instance Initialization Block](./03-instance-initialization-block.md)  
➡️ [Quick Revision](./05-blocks-quick-revision.md)

🏠 [Java Notes Home](../README.md)

<a name="top"></a>

# 🧱 Java Blocks

> **Topic 13 • Blocks**

A **block** is a group of Java statements enclosed inside curly braces `{ }`. Blocks help group statements and are important when learning Java initialization.

## 1️⃣ Main Concepts

This topic focuses on:
- Static block
- Instance initialization block
- Constructor

A constructor is not technically a block, but its body is a block and its execution is closely connected with object initialization.

---

# ⚡ Java Static Block

> **Topic 20 • Blocks**

## 1️⃣ Static Block

A static block is written using the static keyword.

~~~java
static {
    System.out.println("Static Block");
}
~~~

It executes during **class initialization**.

### Important Points

- It belongs to class initialization, not to an individual object.
- Static initialization happens once for a given class initialization.
- If a class has multiple static blocks, their initialization actions follow source order.

~~~java
class Demo {
    static {
        System.out.println("First");
    }

    static {
        System.out.println("Second");
    }
}
~~~

Output during that initialization:

~~~text
First
Second
~~~

### 🧠 Remember

**Static → Class → Once**


➡️ [Instance Initialization Block](./03-instance-initialization-block.md)
➡️ [Static vs Instance](./05-static-vs-instance-block.md)

🏠 [Java Notes Home](../README.md)

---

# 🟢 Java Instance Initialization Block

> **Topic 20 • Blocks**

## 2️⃣ Instance Initialization Block

An instance initialization block is a block without the static keyword.

~~~java
class Student {
    {
        System.out.println("Instance Block");
    }

    Student() {
        System.out.println("Constructor");
    }
}
~~~

It runs as part of **object construction**, before the constructor body for that class.

If you create two objects, the instance initialization runs for each object construction.

Multiple instance initialization blocks are allowed. Their initialization actions follow their source order together with instance field initializers.

### 🧠 Remember

**Instance → Object → Every construction**


➡️ [Constructor](./04-constructor.md)
➡️ [Initialization Order](./06-initialization-order.md)

🏠 [Java Notes Home](../README.md)

---

# 🏗️ Java Constructor

> **Topic 20 • Blocks**

## 3️⃣ Constructor

A constructor has the same name as its class and is used when an object is created.

~~~java
class Student {
    Student() {
        System.out.println("Constructor");
    }
}
~~~

A constructor is **not technically a block**. Its body is a block. We study it here because it is closely connected with object initialization.

### 🧠 Remember

**Constructor → Initialize Object**


## 🧠 Remember

**new object → constructor → initialize object**

➡️ [Initialization Order](./06-initialization-order.md)

🏠 [Java Notes Home](../README.md)

---

# ⚖️ Static Block vs Instance Block

> **Topic 20 • Blocks**

## 📊 Quick Comparison

| | Static Block | Instance Block | Constructor |
|---|---|---|---|
| Keyword | static | No static | Class name |
| Belongs to | Class initialization | Object construction | Object construction |
| Runs | During class initialization | During object construction | During constructor invocation |
| Frequency | Once per class initialization | Each object construction | Each constructor invocation |
| Main purpose | Class-level setup | Instance-level setup | Object initialization |


## 🧠 Memory Trick

**Static = Class**

**Instance = Object**

➡️ [Initialization Order](./06-initialization-order.md)

🏠 [Java Notes Home](../README.md)

## 🧠 Master Memory Trick

```text
CLASS  → STATIC
OBJECT → INSTANCE → CONSTRUCTOR
```

## 🎤 Interview Questions

**What is a block?** A group of statements enclosed in curly braces.

**What is a static block?** A block used during class initialization.

**What is an instance initialization block?** A non-static block whose initialization actions run during object construction before the constructor body for that class.

**Is a constructor a block?** No. A constructor is a class member; its body is a block.

➡️ [Initialization Order](./02-initialization-order.md)
➡️ [Blocks Quick Revision](./03-blocks-quick-revision.md)

🏠 [Java Notes Home](../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

# 🧱 Java Blocks

> **Topic 20 • Blocks**

A **block** is a group of Java statements enclosed in curly braces { }.

~~~java
{
    // statements
}
~~~

Blocks are used to group statements and are also important in Java initialization.

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

## 📊 Quick Comparison

| | Static Block | Instance Block | Constructor |
|---|---|---|---|
| Keyword | static | No static | Class name |
| Belongs to | Class initialization | Object construction | Object construction |
| Runs | During class initialization | During object construction | During constructor invocation |
| Frequency | Once per class initialization | Each object construction | Each constructor invocation |
| Main purpose | Class-level setup | Instance-level setup | Object initialization |

## 🎤 Interview Questions

**Does a static block run for every object?** No.

**Does an instance block use static?** No.

**Does an instance block run before the constructor body?** Yes.

**Is a constructor itself a block?** No. Its body is a block.

➡️ [Initialization Order](./02-initialization-order.md)  
➡️ [Quick Revision](./03-blocks-quick-revision.md)

🏠 [Java Notes Home](../README.md)
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
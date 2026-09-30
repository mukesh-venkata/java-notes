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
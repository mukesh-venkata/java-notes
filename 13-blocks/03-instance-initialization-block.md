# 🟢 Java Instance Initialization Block

> **Topic 20 • Blocks**

An **instance initialization block** is a block inside a class that does not use `static`.

```java
{
    System.out.println("Instance Block");
}
```

## 🔹 When Does It Run?

It runs as part of **each object construction**, before the constructor body of that class.

```java
class Student {
    {
        System.out.println("Instance Block");
    }

    Student() {
        System.out.println("Constructor");
    }
}
```

Conceptually:

```text
new Student()
    ↓
Instance initialization
    ↓
Constructor body
```

## 🔹 Multiple Instance Blocks

Multiple instance initialization blocks execute in source order, interleaved with instance field initializers according to their textual order.

```java
class Demo {
    int x = 10;

    {
        System.out.println("Block 1");
    }

    int y = 20;

    {
        System.out.println("Block 2");
    }
}
```

## 🧠 Key Difference

```text
STATIC BLOCK
→ class initialization

INSTANCE BLOCK
→ object construction
```

## 🎤 Interview Quick Check

**Does an instance block use `static`?** No.

**How often can it execute?** For each object construction.

**Does it execute before the constructor body?** Yes.

**Can there be multiple instance blocks?** Yes; their initialization actions follow source order.

## 🔗 Navigation

⬅️ [Blocks Overview](./01-blocks-overview.md)  
➡️ [Static Block](./02-static-block.md)  
➡️ [Constructor & Initialization Order](./04-constructor-and-initialization-order.md)  
➡️ [Quick Revision](./05-blocks-quick-revision.md)

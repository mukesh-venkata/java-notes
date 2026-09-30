# ⚡ Java Static Block

> **Topic 20 • Blocks**

A **static block** is a block declared with the `static` keyword.

```java
static {
    System.out.println("Static Block");
}
```

## 🔹 When Does It Run?

A static block executes during **class initialization**.

For the usual application entry-point class, class initialization happens before `main()` is invoked. More generally, remember that static initialization happens when the JVM initializes the class.

## 🔹 How Often?

Static initialization occurs once for a given class initialization. Multiple static blocks execute in textual order.

```java
class Demo {
    static {
        System.out.println("Static 1");
    }
    static {
        System.out.println("Static 2");
    }
}
```

Conceptually:

```text
Class initialization
       ↓
Static 1
       ↓
Static 2
       ↓
Initialization completes
```

## 💻 Example

```java
class Demo {
    static {
        System.out.println("Static block");
    }

    public static void main(String[] args) {
        System.out.println("main");
    }
}
```

Typical output:

```text
Static block
main
```

## 🎯 Common Use

Static blocks can perform class-level initialization that requires statements rather than a simple field initializer.

## 🎤 Interview Quick Check

**What identifies a static block?** `static`.

**When does it execute?** During class initialization.

**Can a class have multiple static blocks?** Yes; they execute in textual order.

## 🔗 Navigation

⬅️ [Blocks Overview](./01-blocks-overview.md)  
➡️ [Instance Initialization Block](./03-instance-initialization-block.md)  
➡️ [Constructor & Initialization Order](./04-constructor-and-initialization-order.md)  
➡️ [Quick Revision](./05-blocks-quick-revision.md)

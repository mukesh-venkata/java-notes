# 🕶️ Java Method Hiding

> **Topic 18 • Methods**

When a subclass declares a **static method** with the same signature as a static method in its superclass, the child method **hides** the parent method.

Static methods are not overridden.

## 💻 Example

```java
class Parent {
    static void display() {
        System.out.println("Parent");
    }
}

class Child extends Parent {
    static void display() {
        System.out.println("Child");
    }
}

Parent p = new Child();
p.display(); // Parent
```

The selected static method depends on the compile-time reference/class context, not runtime overriding dispatch.

## 🆚 Hiding vs Overriding

```text
Static method
     ↓
Method hiding
     ↓
Class/reference context

Instance method
     ↓
Method overriding
     ↓
Runtime object
```

Prefer class-qualified access:

```java
Parent.display();
Child.display();
```

## 🎤 Interview Quick Check

**Can static methods be overridden?**  
No. Static methods are hidden.

**What determines a hidden static method call?**  
The compile-time type/class context.

## 🔗 Navigation

⬅️ [Recursion](./10-recursion.md)

➡️ [Quick Revision](./12-methods-quick-revision.md)

🏠 [Java Notes Home](../README.md)

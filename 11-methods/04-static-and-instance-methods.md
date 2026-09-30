# ⚙️ Java Static & Instance Methods

> **Topic 18 • Methods**

Java methods are commonly encountered as **static methods** and **instance methods**.

## 1️⃣ Static Method

A static method is declared with `static` and is associated with the class.

```java
class Test {
    static void display() {
        System.out.println("Hello");
    }
}

Test.display();
```

## 2️⃣ Instance Method

An instance method is not declared `static` and is associated with an object.

```java
class Test {
    void display() {
        System.out.println("Hello");
    }
}

Test t = new Test();
t.display();
```

## 🆚 Comparison

| Feature | Static | Instance |
|---|---|---|
| Associated with | Class | Object |
| Typical call | `Class.method()` | `object.method()` |
| Requires object for normal invocation? | No | Yes |
| Can directly use instance state? | No, not without an object/reference | Yes |

A static method has no implicit `this` reference. An instance method executes with a current-object context.

## 🧠 Memory Trick

```text
STATIC   → CLASS
INSTANCE → OBJECT
```

## 🎤 Interview Quick Check

**Can a static method directly access an instance field?**  
No. It needs an object/reference.

**Does an instance method have a current-object context?**  
Yes.

## 🔗 Navigation

⬅️ [Method Signature](./03-method-signature.md)

➡️ [Method Binding](./05-method-binding.md)

➡️ [Method Hiding](./11-method-hiding.md)

➡️ [Quick Revision](./12-methods-quick-revision.md)

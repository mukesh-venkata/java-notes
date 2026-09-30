<a name="top"></a>

# 🔗 Java Method Binding

> **Topic 18 • Methods**

**Method binding** describes how a method call is associated with the method implementation that will execute.

```text
Binding
├── Static / Early / Compile-time
└── Dynamic / Late / Runtime
```

## 🟦 Static / Early Binding

Common examples include static, private and final methods, along with overloaded method selection.

## 🟥 Dynamic / Runtime Binding

For an overridable instance method, Java can select the implementation based on the **runtime class of the object**.

```java
class Animal {
    void sound() {
        System.out.println("Animal");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog");
    }
}

Animal a = new Dog();
a.sound(); // Dog
```

```text
Reference type → available members
Runtime object → overridden implementation
```

## 🎤 Interview Quick Check

**What is runtime binding?**  
Selection of an overridden instance method based on the runtime class of the object.

**Which methods participate in overriding-based dynamic dispatch?**  
Overridable instance methods.

## 🔗 Navigation

⬅️ [Static & Instance Methods](./04-static-and-instance-methods.md)

➡️ [Overriding](./07-method-overriding.md)

➡️ [Overloading](./06-method-overloading.md)

➡️ [Quick Revision](./12-methods-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

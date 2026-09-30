<a name="top"></a>

# 🧬 Java Method Overriding

> **Topic 18 • Methods**

**Method overriding** occurs when a subclass provides its own implementation of an inherited, overridable instance method with the same signature.

## 💻 Example

```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Bark");
    }
}

Animal animal = new Dog();
animal.sound(); // Bark
```

## 📌 Basic Rules

An overriding method:

- Must have a compatible signature.
- Cannot reduce access visibility.
- May provide a covariant return type for reference returns.
- Cannot override a `final` method.
- Does not override a `static` method; static methods are hidden.
- Does not override a `private` method in the ordinary overriding sense.

## 🧠 `@Override`

```java
@Override
void sound() {
    System.out.println("Bark");
}
```

The annotation asks the compiler to verify that the method is actually overriding a superclass/interface method.

## 🎤 Interview Quick Check

**Overriding?**  
A subclass provides a new implementation for an inherited overridable instance method.

**Can static methods be overridden?**  
No. They are hidden.

**Can private methods be overridden?**  
No, not in the normal overriding sense.

**Can a final method be overridden?**  
No.

## 🔗 Navigation

⬅️ [Overloading](./06-method-overloading.md)

➡️ [Overriding vs Overloading](./08-overriding-vs-overloading.md)

➡️ [Access & Overriding Rules](./09-method-access-and-overriding-rules.md)

➡️ [Method Binding](./05-method-binding.md)

➡️ [Quick Revision](./12-methods-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

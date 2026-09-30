<a name="top"></a>

# 🔐 Java Method Access & Overriding Rules

> **Topic 18 • Methods**

Some methods cannot participate in normal overriding, and an overriding method must respect Java's access rules.

## 🧠 SPF Memory Trick

```text
S → Static
P → Private
F → Final
```

### Static

A static method is **hidden**, not overridden.

### Private

A private method is not inherited by a subclass in the ordinary sense, so a same-named child method is not an override of that private method.

### Final

A final instance method cannot be overridden.

## 🔒 Access Cannot Be Reduced

The overriding method cannot make the inherited accessible contract more restrictive.

```text
public    → public
protected → protected / public
package   → package / protected / public
```

The exact package-access case depends on the package relationship.

## 🔄 Covariant Return Type

An overriding method may return a subtype of the original reference return type.

```java
class Animal { }
class Dog extends Animal { }

class Parent {
    Animal getAnimal() {
        return new Animal();
    }
}

class Child extends Parent {
    @Override
    Dog getAnimal() {
        return new Dog();
    }
}
```

## 🧩 `@Override`

Use `@Override` so the compiler can verify the intended override.

## 🎤 Interview Quick Check

**SPF?**  
Static → hidden, Private → not overridden, Final → cannot override.

**Can access be reduced?**  
No.

**Can an overriding return type change?**  
A compatible covariant reference return type is allowed.

## 🔗 Navigation

⬅️ [Overriding](./07-method-overriding.md)

➡️ [Recursion](./10-recursion.md)

➡️ [Method Hiding](./11-method-hiding.md)

➡️ [Quick Revision](./12-methods-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

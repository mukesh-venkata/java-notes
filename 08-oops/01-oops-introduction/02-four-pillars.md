<a name="top"></a>

# 🧱 Java OOP — Four Pillars

> **Topic 15 • OOP Introduction**

The four commonly taught pillars of OOP are:

### **A-E-I-P**

```text
A → Abstraction
E → Encapsulation
I → Inheritance
P → Polymorphism
```

---

## 1️⃣ Abstraction

**Show essential behavior while hiding unnecessary implementation details.**

Java commonly uses:

- Abstract classes
- Interfaces

Example idea:

```text
User
 ↓
calls start()
 ↓
doesn't need to know every internal implementation step
```

> We will study abstraction in depth later.

---

## 2️⃣ Encapsulation

Encapsulation combines data and related behavior and controls how that data is accessed.

A common Java design uses:

```java
class Student {
    private int age;

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}
```

The `private` field is not directly accessible from outside the class.

> Encapsulation is broader than simply writing getters and setters.

---

## 3️⃣ Inheritance

Inheritance allows a class to derive from another class.

```java
class Animal {
    void eat() {
        System.out.println("Eating");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Barking");
    }
}
```

A `Dog` object can use the inherited `eat()` method.

> Java class inheritance is single-parent at the class level. Multiple inheritance of classes is not supported; interfaces provide another mechanism for combining contracts.

---

## 4️⃣ Polymorphism

Polymorphism means that the same interface or reference can represent different concrete behavior.

Two important forms in Java are:

| Form | Common mechanism |
|---|---|
| Compile-time polymorphism | Method overloading |
| Runtime polymorphism | Method overriding |

Example:

```java
Animal animal = new Dog();
animal.sound();
```

If `Dog` overrides `sound()`, the overridden implementation can be selected at runtime.

---

## 🧠 One-Line Memory

```text
A → Hide details
E → Control access
I → Reuse/derive behavior
P → Different behavior through a common type
```

---

## 🎤 Interview Quick Check

**Abstraction?** → Hide unnecessary implementation details.

**Encapsulation?** → Bundle state/behavior and control access.

**Inheritance?** → Derive one class from another.

**Polymorphism?** → Same type/interface can lead to different implementations.

---

## 🔗 Navigation

⬅️ [OOP Overview](./01-oops-overview.md)

➡️ [Class vs Object](./03-class-vs-object.md)

➡️ [Quick Revision](./05-oops-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

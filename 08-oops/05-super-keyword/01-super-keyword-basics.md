<a name="top"></a>

# 🧬 Java `super` Keyword

> **Topic 24 • `super` Keyword**

The `super` keyword is used in a child class to refer to the **immediate parent-class context**.

It is especially useful when a child needs to access a parent constructor, parent method, or parent field.

## 1️⃣ What Does `super` Mean?

Consider:

~~~java
class Animal {
    String name = "Animal";
}

class Dog extends Animal {
    String name = "Dog";

    void show() {
        System.out.println(super.name);
    }
}
~~~

Here:

~~~text
Dog
 ↓
super
 ↓
Animal
~~~

So `super.name` refers to the parent-class field.

> **Important:** `super` refers to the **immediate superclass**, not an arbitrary grandparent class.

## 2️⃣ Three Main Uses

| # | Usage | Meaning |
|---:|---|---|
| 1 | `super()` | Calls a parent constructor |
| 2 | `super.method()` | Calls an accessible parent method |
| 3 | `super.field` | Accesses an accessible parent field |

These three forms cover the core use of `super`.

## 3️⃣ `super` vs `this`

| `this` | `super` |
|---|---|
| Current object/class context | Immediate parent-class context |
| `this.field` | `super.field` |
| `this.method()` | `super.method()` |
| `this()` → same-class constructor | `super()` → parent constructor |

Memory:

~~~text
this  → CURRENT
super → PARENT
~~~

## 4️⃣ Important Rules

- `super` is used in an instance context.
- `super()`, when explicitly used, must be the first statement in a constructor.
- `super(...)` invokes an applicable constructor of the immediate superclass.
- `super.method()` accesses an inherited parent implementation when permitted.
- `super.field` accesses an accessible parent field.
- `super` does not directly jump to an arbitrary grandparent.

## 5️⃣ Basic Inheritance Diagram

~~~text
Parent Class
   Animal
      ↑
    super
      ↑
Child Class
    Dog
~~~

Inside `Dog`, `super` provides access to the immediate `Animal` context.

## 🎤 Interview Questions

**Q1. What is `super`?**  
A keyword used by a subclass to refer to its immediate superclass context.

**Q2. What are the three major uses of `super`?**  
Calling a parent constructor, calling a parent method, and accessing a parent field.

**Q3. Does `super` refer to the grandparent?**  
No. It refers to the immediate parent.

➡️ [`super()` — Parent Constructor](./02-super-constructor.md)
➡️ [`super` Method & Field](./03-super-method-and-field.md)

🏠 [Java Notes Home](../../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

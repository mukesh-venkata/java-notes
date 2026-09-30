<a name="top"></a>

# 🎯 Java `this` Keyword

> **Topic 22 • `this` Keyword**

The `this` keyword refers to the **current object** — the object whose instance method or constructor is currently being executed.

## 1️⃣ What Does `this` Mean?

~~~java
class Student {
    String name;

    void display() {
        System.out.println(this.name);
    }
}
~~~

If `s.display()` is invoked, then inside `display()`, `this` refers to `s`.

~~~text
this → current object
~~~

## 2️⃣ Instance Context

`this` is associated with an object, so it is available in an **instance context**.

It cannot be used directly inside a static method:

~~~java
class Student {
    static void show() {
        // this;  // compile-time error
    }
}
~~~

A static method belongs to the class and has no implicit current object.

## 3️⃣ Five Important Uses

| # | Use | Example |
|---:|---|---|
| 1 | Current object's instance variable | `this.name` |
| 2 | Another constructor in same class | `this()` |
| 3 | Current object's instance method | `this.show()` |
| 4 | Pass current object as argument | `show(this)` |
| 5 | Return current object | `return this;` |

## 🧠 Memory Trick

**REFER → CALL → PASS → RETURN**

~~~text
this.variable
this()
this.method()
method(this)
return this
~~~

## 🎤 Interview Questions

**Q1. What does `this` refer to?**  
The current object whose instance method or constructor is executing.

**Q2. Can `this` be used directly in a static method?**  
No.

**Q3. Is `this` a normal variable?**  
No. It is a Java keyword representing the current object reference in an instance context.

➡️ [Instance Members](./02-this-for-instance-members.md)
➡️ [Constructor & Method Calls](./03-this-constructor-and-method-calls.md)

🏠 [Java Notes Home](../../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

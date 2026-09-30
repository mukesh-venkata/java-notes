<a name="top"></a>

# 🔗 `super` & Constructor Chaining in Inheritance

> **Topic 23 • Inheritance**

When inheritance is involved, `super` provides a way to refer to the immediate parent class and to invoke its constructor.

## 1️⃣ `super()` — Parent Constructor

~~~java
class Parent {
    Parent() {
        System.out.println("Parent");
    }
}

class Child extends Parent {
    Child() {
        super();
        System.out.println("Child");
    }
}
~~~

Flow:

~~~text
new Child()
    ↓
Child constructor
    ↓
super()
    ↓
Parent constructor
    ↓
Child constructor body
~~~

If a child constructor does not explicitly begin with a constructor invocation, Java inserts an implicit `super()` when applicable.

## 2️⃣ Parent Without a No-Argument Constructor

Consider:

~~~java
class Parent {
    Parent(int value) {
    }
}

class Child extends Parent {
    Child() {
        super(10);
    }
}
~~~

The child must invoke an applicable parent constructor because `Parent()` does not exist.

## 3️⃣ `super.field`

A child can use `super.field` to refer to an accessible field declared in the immediate parent.

~~~java
class Parent {
    int value = 10;
}

class Child extends Parent {
    int value = 20;

    void show() {
        System.out.println(value);
        System.out.println(super.value);
    }
}
~~~

Output:

~~~text
20
10
~~~

Here `value` refers to the child field, while `super.value` refers to the parent field.

## 4️⃣ `super.method()`

A child can invoke an accessible parent implementation using `super.method()`.

~~~java
class Parent {
    void show() {
        System.out.println("Parent");
    }
}

class Child extends Parent {
    @Override
    void show() {
        System.out.println("Child");
        super.show();
    }
}
~~~

Flow:

~~~text
Child.show()
    ↓
prints Child
    ↓
super.show()
    ↓
Parent.show()
~~~

This is especially useful when overriding a method but still wanting to execute the parent's implementation.

## 5️⃣ `super` vs `this`

| Keyword | Refers to |
|---|---|
| `this` | Current object/current class context |
| `super` | Immediate parent class part/context |

Common forms:

~~~text
this.field
this.method()
this()

super.field
super.method()
super()
~~~

## 6️⃣ First-Statement Rule

In a constructor:

- Explicit `this(...)` must be first.
- Explicit `super(...)` must be first.
- A constructor cannot explicitly use both as its first constructor-invocation statement.

## 7️⃣ Constructor Chain With Inheritance

~~~java
class Parent {
    Parent() {
        System.out.println("Parent constructor");
    }
}

class Child extends Parent {
    Child() {
        super();
        System.out.println("Child constructor");
    }
}
~~~

The parent constructor completes before the child constructor body continues.

## 🧠 Memory Trick

**this → current class/object**

**super → immediate parent**

**super() → parent constructor**

## 🎤 Interview Questions

**Q1. What does `super()` do?**  
Invokes a constructor of the immediate parent class.

**Q2. What does `super.method()` do?**  
Invokes an accessible method implementation from the immediate parent.

**Q3. What does `super.field` do?**  
Accesses an accessible field declared in the immediate parent.

**Q4. Why might a child need explicit `super(args)`?**  
When the parent has no applicable no-argument constructor.

➡️ [Access & Inheritance](./03-access-and-inheritance.md)
➡️ [Method Overriding](./05-inheritance-and-method-overriding.md)

🏠 [Java Notes Home](../../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

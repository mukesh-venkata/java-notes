<a name="top"></a>

# 🎯 `super.method()` & `super.field`

> **Topic 24 • `super` Keyword**

Two important uses of `super` are accessing members of the immediate parent:

- `super.method()`
- `super.field`

## 1️⃣ `super.method()`

Suppose the child overrides a parent method:

~~~java
class Animal {

    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Dog sound");
        super.sound();
    }
}
~~~

When:

~~~java
Dog d = new Dog();
d.sound();
~~~

the child method executes first, then:

~~~java
super.sound();
~~~

invokes the parent implementation.

Flow:

~~~text
Dog.sound()
    ↓
super.sound()
    ↓
Animal.sound()
~~~

## 2️⃣ Why Use `super.method()`?

It is useful when the child wants to **extend** parent behavior instead of completely replacing it.

Example:

~~~java
class Dog extends Animal {

    @Override
    void sound() {
        super.sound();
        System.out.println("Dog-specific sound");
    }
}
~~~

This lets the child reuse the parent's implementation.

## 3️⃣ `super.field`

If parent and child have fields with the same name:

~~~java
class Animal {
    String name = "Animal";
}

class Dog extends Animal {
    String name = "Dog";

    void display() {
        System.out.println(name);
        System.out.println(this.name);
        System.out.println(super.name);
    }
}
~~~

Output:

~~~text
Dog
Dog
Animal
~~~

Meaning:

~~~text
name       → child field in this context
this.name  → current object's child field
super.name → parent field
~~~

## 4️⃣ Field Hiding

Fields are not dynamically overridden like instance methods.

When a child declares a field with the same name as a parent field, the fields are **hidden**, not overridden.

`super.field` can explicitly select the parent field.

## 5️⃣ `super` and Private Members

A child cannot use `super.privateField` to bypass the parent's private access restriction.

~~~java
class Animal {
    private String name = "Animal";
}

class Dog extends Animal {
    void show() {
        // System.out.println(super.name); // compile-time error
    }
}
~~~

The parent can expose controlled access through an accessible method.

## 6️⃣ `super.method()` vs `this.method()`

| Syntax | Meaning |
|---|---|
| `this.method()` | Invoke method on current object |
| `super.method()` | Invoke parent-class implementation |

Example:

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
        this.show();   // would recursively call Child.show()
        // super.show(); // calls Parent.show()
    }
}
~~~

> **Important:** Do not use `this.show()` inside this overriding example when you intend to call the parent; it would call the child method again.

Correct parent call:

~~~java
super.show();
~~~

## 7️⃣ Immediate Parent Only

If:

~~~text
Grandparent
     ↓
   Parent
     ↓
   Child
~~~

inside `Child`, `super` refers to `Parent`, not directly to `Grandparent`.

A child cannot write something like `super.super.method()`.

## 🧠 Memory Trick

**this → CURRENT**

**super → PARENT**

## 🎤 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What does <code>super.method()</code> do?</summary>
<br>

It calls an accessible implementation of the method from the immediate parent class.

</details>

<details>
<summary>Q2. What does <code>super.field</code> do?</summary>
<br>

It accesses an accessible parent-class field.

</details>

<details>
<summary>Q3. Can <code>super</code> access a private parent field?</summary>
<br>

No. Private members are not directly accessible from the subclass.

</details>

<details>
<summary>Q4. Can <code>super</code> directly access a grandparent?</summary>
<br>

No. super refers to the immediate parent class context.

</details>
## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

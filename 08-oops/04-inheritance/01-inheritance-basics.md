<a name="top"></a>

# 🧬 Java Inheritance Basics

> **Topic 23 • Inheritance**

**Inheritance** is an OOP mechanism in which a child class acquires accessible members from a parent class.

It establishes a **parent → child** relationship and helps with code reuse.

## 1️⃣ Basic Idea

~~~text
Parent Class
   ↓ extends
Child Class
~~~

Example:

~~~java
class Animal {
    String name;

    void eat() {
        System.out.println("Eating");
    }
}

class Dog extends Animal {

    void bark() {
        System.out.println("Barking");
    }
}
~~~

Now:

~~~java
Dog d = new Dog();

d.name;     // inherited accessible field
d.eat();    // inherited accessible method
d.bark();   // Dog's own method
~~~

The child class can use accessible members of its parent.

## 2️⃣ Important Terms

| Term | Meaning |
|---|---|
| Parent / Superclass | Class being inherited from |
| Child / Subclass | Class that extends another class |
| `extends` | Keyword used for class inheritance |
| IS-A | Parent-child relationship represented by inheritance |

For:

~~~java
class Dog extends Animal
~~~

we can say:

> A Dog **IS-A** Animal.

## 3️⃣ What Does a Child Acquire?

A child can use accessible fields and methods of the parent.

~~~text
Animal
 ├── name
 └── eat()

     ↓ extends

Dog
 ├── name       ← inherited accessible member
 ├── eat()      ← inherited accessible member
 └── bark()     ← child member
~~~

Inheritance does **not** mean that every parent member becomes directly accessible in every situation. Access modifiers still apply.

## 4️⃣ Why Use Inheritance?

Inheritance can provide:

- Code reuse
- Common behavior in a parent class
- Specialized behavior in child classes
- A natural IS-A relationship
- A foundation for method overriding and runtime polymorphism

Example:

~~~java
class Vehicle {
    void start() {
        System.out.println("Vehicle starts");
    }
}

class Car extends Vehicle {
    void drive() {
        System.out.println("Car drives");
    }
}
~~~

The common `start()` behavior can be placed in `Vehicle`, while `Car` adds specialized behavior.

## 5️⃣ Constructors Are Not Inherited

This is an important rule.

~~~java
class Parent {
    Parent() {
    }
}

class Child extends Parent {
}
~~~

The `Parent` constructor is **not inherited** by `Child`.

However, constructing a child object involves parent-constructor invocation as part of constructor chaining.

This distinction becomes important when learning `super()`.

## 6️⃣ Private Members

A `private` field or method of the parent is not directly accessible from the child class.

~~~java
class Parent {
    private int value;
}

class Child extends Parent {
    void show() {
        // System.out.println(value); // compile-time error
    }
}
~~~

The parent can expose controlled access through methods such as getters when appropriate.

## 7️⃣ Simple Execution Picture

~~~text
class Animal
     ↑
   extends
     ↑
class Dog

new Dog()
   ↓
Dog object
   ↓
Can use accessible inherited behavior
   +
Can use Dog's own behavior
~~~

Inheritance describes the class relationship; object construction still follows Java's initialization and constructor rules.

## 🧠 Memory Trick

**PARENT → COMMON MEMBERS**

**CHILD → INHERITED + SPECIALIZED MEMBERS**

## 🎤 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What is inheritance?</summary>
<br>

A mechanism through which a child class can acquire and use accessible members of a parent class.

</details>

<details>
<summary>Q2. Which keyword is used for class inheritance?</summary>
<br>

extends.

</details>

<details>
<summary>Q3. What is an IS-A relationship?</summary>
<br>

A relationship where a child is a specialized form of the parent, such as Dog IS-A Animal.

</details>

<details>
<summary>Q4. Are constructors inherited?</summary>
<br>

No. Constructors are not inherited.

</details>

<details>
<summary>Q5. Are private members directly accessible in a child class?</summary>
<br>

No. Private members are directly accessible only within the class that declares them.

</details>
## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

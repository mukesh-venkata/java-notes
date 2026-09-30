<a name="top"></a>

# 🔄 Inheritance & Method Overriding

> **Topic 23 • Inheritance**

Inheritance becomes especially powerful when a child class provides its own implementation of an inherited instance method.

This is **method overriding**.

## 1️⃣ Basic Example

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
    }
}
~~~

The child provides a new implementation of the inherited instance method.

## 2️⃣ Parent Reference, Child Object

~~~java
Animal a = new Dog();
a.sound();
~~~

The reference type is `Animal`, but the object is a `Dog`.

For an overridable instance method, Java selects the implementation based on the actual object at runtime.

~~~text
Animal reference
      ↓
   Dog object
      ↓
   sound()
      ↓
Dog.sound()
~~~

This is the foundation of **runtime polymorphism**.

## 3️⃣ `@Override`

Use:

~~~java
@Override
void sound() {
}
~~~

The annotation tells the compiler that you intend to override an inherited method.

It helps catch mistakes such as an incorrect parameter list.

## 4️⃣ Important Overriding Rules

An overriding method generally must:

- Have the same method signature as the inherited instance method.
- Not reduce access visibility.
- Follow return-type compatibility rules.
- Not override a `final` instance method.
- Not override a `private` method because private methods are not inherited by the subclass.
- Respect checked-exception rules for overriding methods.

A `static` method is not overridden; it is **hidden** when a child declares a compatible static method.

## 5️⃣ Access Level

A child cannot reduce the visibility of an overridden method.

For example:

~~~java
class Parent {
    public void show() {
    }
}

class Child extends Parent {
    // private void show() { } // invalid
}
~~~

The child method cannot be more restrictive than the inherited method.

## 6️⃣ Covariant Return Type

An overriding method may return a subtype of the original method's return type.

~~~java
class Parent {
    Parent get() {
        return this;
    }
}

class Child extends Parent {
    @Override
    Child get() {
        return this;
    }
}
~~~

`Child` is a subtype of `Parent`, so the return type is covariant.

## 7️⃣ `final` Methods

A final instance method cannot be overridden.

~~~java
class Parent {
    final void show() {
    }
}

class Child extends Parent {
    // void show() { } // invalid
}
~~~

Use `final` when an implementation should not be overridden by subclasses.

## 8️⃣ Private Methods

A private method belongs only to its declaring class and is not inherited by the subclass.

Therefore, a child method with the same signature is not an override of the parent's private method.

## 9️⃣ Static Method Hiding

Static methods belong to the class context.

If a child declares a compatible static method with the same signature, this is **method hiding**, not overriding.

~~~java
class Parent {
    static void show() {
        System.out.println("Parent");
    }
}

class Child extends Parent {
    static void show() {
        System.out.println("Child");
    }
}
~~~

This distinction becomes important when comparing static binding with runtime dispatch.

## 🔟 Inheritance → Overriding → Runtime Polymorphism

~~~text
Inheritance
    ↓
Child receives accessible behavior
    ↓
Child overrides an instance method
    ↓
Parent reference can refer to Child object
    ↓
Runtime method dispatch
    ↓
Overridden Child implementation executes
~~~

## 🧠 Memory Trick

**INHERIT → OVERRIDE → RUNTIME DISPATCH**

## 🎤 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What is method overriding?</summary>
<br>

A subclass provides a compatible implementation of an inherited instance method.

</details>

<details>
<summary>Q2. Is static method overriding?</summary>
<br>

No. Static methods are hidden, not overridden.

</details>

<details>
<summary>Q3. Can a private method be overridden?</summary>
<br>

No. Private methods are not inherited by subclasses and therefore cannot be overridden.

</details>

<details>
<summary>Q4. Can a final method be overridden?</summary>
<br>

No.

</details>

<details>
<summary>Q5. Why is <code>Animal a = new Dog()</code> important?</summary>
<br>

It demonstrates a parent reference referring to a child object and forms the basis for runtime polymorphism.

</details>
## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

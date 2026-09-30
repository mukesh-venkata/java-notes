<a name="top"></a>

# 🔗 `super()` — Parent Constructor

> **Topic 24 • `super` Keyword**

`super()` is used to invoke an applicable constructor of the **immediate parent class**.

Constructor chaining ensures that the parent part of a child object is initialized before the child constructor body completes.

## 1️⃣ Basic `super()`

~~~java
class Animal {

    Animal() {
        System.out.println("Animal constructor");
    }
}

class Dog extends Animal {

    Dog() {
        super();
        System.out.println("Dog constructor");
    }
}
~~~

Creating:

~~~java
Dog d = new Dog();
~~~

Conceptual flow:

~~~text
new Dog()
   ↓
Dog()
   ↓
super()
   ↓
Animal()
   ↓
Dog constructor body
~~~

## 2️⃣ Parameterized `super(...)`

A child can pass arguments to a parent constructor.

~~~java
class Animal {

    Animal(String name) {
        System.out.println(name);
    }
}

class Dog extends Animal {

    Dog() {
        super("Dog");
    }
}
~~~

Here:

~~~java
super("Dog");
~~~

selects the applicable `Animal(String)` constructor.

## 3️⃣ `super()` Must Be First

If explicitly written, the constructor invocation must be the first statement.

✅ Correct:

~~~java
Dog() {
    super("Dog");
    System.out.println("Dog");
}
~~~

❌ Incorrect:

~~~java
Dog() {
    System.out.println("Before");
    super("Dog");
}
~~~

The second example does not compile.

## 4️⃣ Implicit `super()`

If a constructor does not explicitly begin with `this(...)` or `super(...)`, Java inserts an implicit `super()` when an accessible no-argument constructor of the parent is available.

Example:

~~~java
class Animal {
    Animal() {
    }
}

class Dog extends Animal {
    Dog() {
        // implicit super();
    }
}
~~~

Conceptually:

~~~java
Dog() {
    super();
}
~~~

## 5️⃣ What If Parent Has Only a Parameterized Constructor?

Consider:

~~~java
class Animal {

    Animal(String name) {
    }
}

class Dog extends Animal {

    Dog() {
        super("Dog");
    }
}
~~~

A child cannot rely on an implicit no-argument `super()` because the parent does not provide an accessible no-argument constructor.

The child must invoke an applicable parent constructor explicitly.

## 6️⃣ `this()` vs `super()`

| Syntax | Calls |
|---|---|
| `this()` | Another constructor in the same class |
| `super()` | Constructor in the immediate parent |

A constructor can explicitly begin with one constructor-invocation statement, not both.

For example:

~~~java
class Dog extends Animal {

    Dog() {
        this(10);
    }

    Dog(int age) {
        super("Dog");
    }
}
~~~

Flow:

~~~text
Dog()
 ↓
this(10)
 ↓
Dog(int)
 ↓
super("Dog")
 ↓
Animal(String)
~~~

## 7️⃣ Constructor Chaining Is Not Constructor Inheritance

Parent constructors are not inherited by the child.

Instead, a parent constructor participates in child-object construction through `super(...)`.

Think:

~~~text
One Dog object
┌────────────────────┐
│ Animal state       │
├────────────────────┤
│ Dog state          │
└────────────────────┘
~~~

## 🧠 Memory Trick

**super() → PARENT CONSTRUCTOR**

**FIRST STATEMENT → IMPORTANT**

## 🎤 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What does <code>super()</code> do?</summary>
<br>

It invokes an applicable constructor of the immediate parent class.

</details>

<details>
<summary>Q2. Must <code>super()</code> be first?</summary>
<br>

Yes, when explicitly used as a constructor invocation, it must be the first statement in the constructor.

</details>

<details>
<summary>Q3. What happens if the parent has no accessible no-argument constructor?</summary>
<br>

The child must explicitly invoke an accessible parent constructor with matching arguments.

</details>

<details>
<summary>Q4. Are parent constructors inherited?</summary>
<br>

No. Constructors are not inherited.

</details>
## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

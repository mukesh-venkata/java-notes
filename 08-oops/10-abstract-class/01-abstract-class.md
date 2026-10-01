<a name="top"></a>

# 🧩 Abstract Class

> **Core idea:** An abstract class is declared with the abstract keyword. It cannot be instantiated directly, but it can provide shared state and behavior for subclasses.

## What is an Abstract Class?

An **abstract class** is a class declared using the abstract keyword.

~~~java
abstract class Animal {
}
~~~

An abstract class is commonly used when a parent class should define common behavior or state while leaving some behavior for subclasses to provide.

### Simple definition

> **Abstract class = A class that cannot be instantiated directly and may define abstract behavior for subclasses.**

---

## Why Do We Need an Abstract Class?

Suppose every Animal should have a sound operation, but different animals produce different sounds.

We can define the common contract in an abstract class:

~~~java
abstract class Animal {

    abstract void sound();
}
~~~

Concrete subclasses provide their own implementation:

~~~java
class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Bark");
    }
}

class Cat extends Animal {

    @Override
    void sound() {
        System.out.println("Meow");
    }
}
~~~

The parent defines **what must be done**, while the child defines **how it is done**.

---

## Syntax

~~~java
abstract class ClassName {

    // instance variables
    // static members
    // constructors
    // concrete methods
    // abstract methods
}
~~~

---

## 1. Cannot Create an Object Directly

An abstract class cannot be instantiated directly.

~~~java
abstract class Animal {
}

Animal a = new Animal(); // Compilation error
~~~

A reference of the abstract type is allowed, but the actual object must be a concrete subclass.

~~~java
abstract class Animal {
}

class Dog extends Animal {
}

Animal a = new Dog(); // Allowed
~~~

### Important distinction

~~~text
Animal a = new Animal();  ❌
        ↓
Abstract class cannot be instantiated

Animal a = new Dog();    ✅
        ↓
Dog is concrete
~~~

The second form uses polymorphic reference assignment: the reference is of the abstract parent type, while the actual object is a concrete child object.

---

## 2. Abstract Class Can Have Constructors

An abstract class **can have constructors**.

~~~java
abstract class Animal {

    Animal() {
        System.out.println("Animal constructor");
    }
}

class Dog extends Animal {

    Dog() {
        System.out.println("Dog constructor");
    }
}

public class Main {

    public static void main(String[] args) {
        Dog d = new Dog();
    }
}
~~~

### Output

~~~text
Animal constructor
Dog constructor
~~~

### Why does the abstract-class constructor execute?

The abstract class itself is not instantiated, but its constructor runs as part of constructing a concrete subclass object.

~~~text
new Dog()
   ↓
Animal constructor
   ↓
Dog constructor
   ↓
Dog object ready
~~~

> **Remember:** No direct abstract-class object is created, but its constructor can participate in subclass construction.

---

## 3. Abstract Class Can Have Abstract Methods

An **abstract method** is declared without a method body.

~~~java
abstract class Animal {

    abstract void sound();
}
~~~

A concrete subclass provides the implementation:

~~~java
class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Bark");
    }
}
~~~

### Flow

~~~text
Abstract class
      ↓
abstract method
      ↓
Concrete subclass
      ↓
method implementation
~~~

---

## 4. Abstract Class Can Have Concrete Methods

An abstract class is **not limited to abstract methods**.

It can contain normal/concrete methods with implementations.

~~~java
abstract class Animal {

    abstract void sound();

    void eat() {
        System.out.println("Eating");
    }
}
~~~

The subclass can use the inherited concrete method:

~~~java
class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Bark");
    }
}
~~~

Usage:

~~~java
Dog d = new Dog();

d.sound();
d.eat();
~~~

So an abstract class can combine:

~~~text
Abstract Class
      │
      ├── Abstract methods
      │      → subclass provides implementation
      │
      └── Concrete methods
             → implementation already provided
~~~

---

## 5. Abstract Class Can Have Instance Variables

An abstract class can contain instance variables.

~~~java
abstract class Animal {

    String name = "Animal";
}
~~~

A concrete subclass object contains the inherited instance state.

~~~java
class Dog extends Animal {
}

Dog d = new Dog();

System.out.println(d.name);
~~~

Output:

~~~text
Animal
~~~

---

## 6. Abstract Class Can Have Static Members

An abstract class can also contain static members.

~~~java
abstract class Animal {

    static int count = 10;

    static void displayCount() {
        System.out.println(count);
    }
}
~~~

A static member belongs to the class, not to an individual object.

~~~java
Animal.displayCount();
~~~

The fact that the class is abstract does not prevent it from having static members.

---

## 7. Abstract Methods — Important Restrictions

An abstract method cannot be:

- ❌ private
- ❌ static
- ❌ final

### Why?

#### private + abstract ❌

A private method is not available to subclasses for overriding. An abstract method exists specifically to require subclass implementation.

~~~java
abstract class Animal {

    private abstract void sound(); // Compilation error
}
~~~

#### static + abstract ❌

Static methods are class-level methods. They are hidden rather than overridden as instance methods.

~~~java
abstract class Animal {

    static abstract void sound(); // Compilation error
}
~~~

#### final + abstract ❌

A final method cannot be overridden, while an abstract method requires a subclass implementation.

~~~java
abstract class Animal {

    final abstract void sound(); // Compilation error
}
~~~

### Memory trick

> **Abstract needs Override.**

~~~text
private → cannot be overridden
static  → class-level method, not instance overriding
final   → overriding prohibited
~~~

---

## 8. The Contract of an Abstract Class

An abstract class can define a contract that concrete subclasses must fulfill.

~~~java
abstract class Animal {

    abstract void sound();
    abstract void eat();
}
~~~

A concrete subclass must implement all inherited abstract methods:

~~~java
class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Bark");
    }

    @Override
    void eat() {
        System.out.println("Eating");
    }
}
~~~

Now Dog is concrete and can be instantiated:

~~~java
Dog d = new Dog();
~~~

### Contract flow

~~~text
Abstract Parent
      ↓
Declares required behavior
      ↓
Concrete Child
      ↓
Implements all required abstract methods
      ↓
Concrete class
      ↓
Object can be created
~~~

---

## 9. What If the Child Does Not Implement All Abstract Methods?

Suppose the parent declares two abstract methods:

~~~java
abstract class Animal {

    abstract void sound();
    abstract void eat();
}
~~~

If the child implements only one:

~~~java
class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Bark");
    }
}
~~~

Dog cannot be concrete because eat() is still abstract.

The child must either:

1. Implement the remaining abstract methods, **or**
2. Also be declared abstract.

~~~java
abstract class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Bark");
    }
}
~~~

> **Rule:** A concrete subclass must implement all inherited abstract methods.

An abstract subclass can leave some abstract methods unimplemented.

---

## 10. Complete Example

~~~java
abstract class Animal {

    String name = "Animal";

    Animal() {
        System.out.println("Animal constructor");
    }

    abstract void sound();

    void eat() {
        System.out.println("Eating");
    }

    static void category() {
        System.out.println("Living organism");
    }
}

class Dog extends Animal {

    Dog() {
        System.out.println("Dog constructor");
    }

    @Override
    void sound() {
        System.out.println("Bark");
    }
}

public class Main {

    public static void main(String[] args) {

        Animal a = new Dog();

        System.out.println(a.name);
        a.sound();
        a.eat();

        Animal.category();
    }
}
~~~

### Output

~~~text
Animal constructor
Dog constructor
Animal
Bark
Eating
Living organism
~~~

This example demonstrates:

- Abstract class
- Constructor
- Instance variable
- Abstract method
- Concrete method
- Static method
- Concrete subclass
- Method overriding
- Parent-type reference
- Child object

---

## Concrete Class vs Abstract Class

| Feature | Concrete Class | Abstract Class |
|---|---|---|
| abstract keyword | ❌ No | ✅ Yes |
| Direct object creation | ✅ Yes | ❌ No |
| Concrete methods | ✅ Yes | ✅ Yes |
| Abstract methods | ❌ No | ✅ Can have |
| Constructors | ✅ Yes | ✅ Yes |
| Instance variables | ✅ Yes | ✅ Yes |
| Static members | ✅ Yes | ✅ Yes |

> **Key point:** The abstract keyword determines whether the class itself can be instantiated directly. An abstract class may still contain fully implemented methods and state.

---

## Abstract Class Mental Model

~~~text
                 ABSTRACT CLASS
                        │
          ┌─────────────┼─────────────┐
          ↓             ↓             ↓
       State         Behavior      Contract
    instance/static  concrete      abstract
      members         methods       methods
                        │             │
                        └──────┬──────┘
                               ↓
                         Concrete Child
                               ↓
                     Implements contract
                               ↓
                         Object created
~~~

---

## Memory Trick

> **Abstract = No direct object + possible contract for subclasses.**

~~~text
ABSTRACT
   ↓
No direct object
   +
Can define abstract behavior
   +
Can contain concrete behavior
~~~

---

## Interview Questions

<details>
<summary>1. What is an abstract class?</summary>

A class declared with the abstract keyword. It cannot be instantiated directly and can contain abstract as well as concrete members.

</details>

<details>
<summary>2. Can we create an object of an abstract class?</summary>

No. Direct instantiation of an abstract class is not allowed.

</details>

<details>
<summary>3. Can an abstract class have a constructor?</summary>

Yes. Its constructor executes as part of constructing a concrete subclass object.

</details>

<details>
<summary>4. Can an abstract class contain concrete methods?</summary>

Yes. An abstract class can contain both abstract methods and concrete methods.

</details>

<details>
<summary>5. Can an abstract class have instance variables?</summary>

Yes. It can contain instance variables like a normal class.

</details>

<details>
<summary>6. Can an abstract class have static methods?</summary>

Yes. An abstract class can contain static members, including static methods.

</details>

<details>
<summary>7. Can an abstract method be private?</summary>

No. A private method cannot be overridden by a subclass, while an abstract method requires subclass implementation.

</details>

<details>
<summary>8. Can an abstract method be static?</summary>

No. Static methods are class-level methods and are hidden rather than overridden.

</details>

<details>
<summary>9. Can an abstract method be final?</summary>

No. A final method cannot be overridden, while an abstract method requires implementation by a concrete subclass.

</details>

<details>
<summary>10. What happens if a subclass does not implement every inherited abstract method?</summary>

The subclass must itself be declared abstract; otherwise, the compiler reports an error.

</details>

<details>
<summary>11. Can an abstract class have no abstract methods?</summary>

Yes. A class may be declared abstract even if it does not declare any abstract methods. It still cannot be instantiated directly.

</details>

---

## Quick Revision

- An abstract class is declared using the abstract keyword.
- It **cannot be instantiated directly**.
- It can have abstract methods.
- It can have concrete methods.
- It can have constructors.
- It can have instance variables.
- It can have static members.
- An abstract method cannot be private, static, or final.
- A concrete child must implement all inherited abstract methods.
- An abstract child may leave some abstract methods unimplemented.
- An abstract-class constructor executes while constructing a concrete subclass object.
- An abstract class can have **zero abstract methods**.
- **Abstract = no direct object + possible contract for subclasses.**

---

## Related Notes

- [OOP Overview](../01-oops-introduction/01-oops-overview.md)
- [Inheritance Basics](../04-inheritance/01-inheritance-basics.md)
- [super & Constructor Chaining](../04-inheritance/04-super-and-constructor-chaining.md)
- [Method Overriding](../04-inheritance/05-inheritance-and-method-overriding.md)
- [Concrete Class](../09-concrete-class/01-concrete-class.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [OOP Home](../)

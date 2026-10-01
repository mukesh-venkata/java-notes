<a name="top"></a>

# 🔌 Interface

> **Core idea:** An interface defines a contract that specifies what an implementing class must provide.

## What is an Interface?

An **interface** is a reference type in Java used to define a contract for classes.

A class uses the `implements` keyword to implement an interface.

~~~java
interface Animal {

    void sound();
}

class Dog implements Animal {

    @Override
    public void sound() {
        System.out.println("Bark");
    }
}
~~~

The interface says **what operation is required**. The implementing class provides the implementation.

### Simple mental model

~~~text
Interface
   ↓
Contract
   ↓
Class implements it
   ↓
Required behavior is provided
~~~

---

## Why Use an Interface?

Interfaces are useful for:

- Defining a common contract
- Supporting multiple inheritance of type
- Reducing coupling between code components
- Allowing different classes to provide different implementations
- Designing flexible APIs

Interfaces were traditionally used to achieve **complete abstraction**, but modern Java interfaces can also contain implemented methods such as `default`, `static`, and private methods.

---

# 1. Interface Cannot Be Instantiated Directly

You cannot directly create an object of an interface.

~~~java
interface Animal {
}

Animal a = new Animal(); // ❌ Compilation error
~~~

However, an interface can be used as a reference type:

~~~java
interface Animal {
}

class Dog implements Animal {
}

Animal a = new Dog(); // ✅
~~~

Here:

- `Animal` is the declared reference type.
- `Dog` is the concrete class.
- The actual object is a `Dog`.

~~~text
Animal reference
      ↓
    Dog object
      ↓
Concrete implementation
~~~

This is an important use of interfaces in polymorphism.

---

# 2. Interfaces Do Not Have Constructors

Interfaces do not declare constructors.

~~~java
interface Animal {

    Animal() { } // ❌ Not allowed
}
~~~

A constructor initializes an object of a class, while an interface itself cannot be instantiated.

A class that implements the interface can have its own constructor:

~~~java
interface Animal {
    void sound();
}

class Dog implements Animal {

    Dog() {
        System.out.println("Dog constructor");
    }

    @Override
    public void sound() {
        System.out.println("Bark");
    }
}
~~~

---

# 3. Interface Variables

Fields declared in an interface are implicitly:

~~~text
public static final
~~~

Example:

~~~java
interface Test {

    int MAX = 100;
}
~~~

This is equivalent to:

~~~java
interface Test {

    public static final int MAX = 100;
}
~~~

Therefore, interface fields are **constants**.

~~~java
System.out.println(Test.MAX);
~~~

You cannot reassign them:

~~~java
Test.MAX = 200; // ❌ Compilation error
~~~

### Important

Interface fields are:

- `public`
- `static`
- `final`

They are **not instance variables**.

~~~text
Interface field
      ↓
public static final
      ↓
Constant
~~~

---

# 4. Interface Methods

Interface method rules have evolved across Java versions.

## Before Java 8

A normal interface method was implicitly:

~~~java
public abstract
~~~

Example:

~~~java
interface Test {

    void display();
}
~~~

Equivalent form:

~~~java
interface Test {

    public abstract void display();
}
~~~

The method has no implementation body.

---

## Java 8: Default and Static Methods

Java 8 introduced implemented methods in interfaces.

### Default method

A `default` method has an implementation:

~~~java
interface Test {

    default void show() {
        System.out.println("Hello");
    }
}
~~~

A class implementing the interface inherits the default implementation unless it overrides it.

### Static method

An interface can also contain static methods:

~~~java
interface Test {

    static void test() {
        System.out.println("Static");
    }
}
~~~

A static interface method is called using the interface name:

~~~java
Test.test();
~~~

It is not inherited as an instance method by implementing classes.

---

## Java 9+: Private Interface Methods

Java 9 introduced private methods in interfaces.

~~~java
interface Test {

    default void show() {
        helper();
    }

    private void helper() {
        System.out.println("Helper");
    }
}
~~~

Private interface methods are used internally by the interface's implemented methods. They are not inherited or directly accessible by implementing classes.

### Interface method timeline

~~~text
Before Java 8
      ↓
public abstract methods

Java 8
      ↓
public abstract
public default
public static

Java 9+
      ↓
private interface methods
~~~

> **Interview point:** Do not say that all interface methods are always abstract. That is true for the traditional interface model, but not for modern Java.

---

# 5. Interface Methods and Overriding

An interface abstract method is implicitly `public`.

Therefore, when a class implements it, the implementation must also be `public`.

~~~java
interface Animal {

    void sound();
}

class Dog implements Animal {

    @Override
    public void sound() {
        System.out.println("Bark");
    }
}
~~~

### Why must it be public?

The interface method is public. An implementing method cannot reduce the visibility of an inherited public contract.

This is invalid:

~~~java
class Dog implements Animal {

    @Override
    void sound() { // ❌ Not public
        System.out.println("Bark");
    }
}
~~~

The compiler reports an error because the implementation attempts to reduce visibility.

~~~text
Interface method
public
   ↓
Implementing method
public
   ↓
Visibility preserved
~~~

---

# 6. Interface Relationships

Java provides three important interface/class relationships.

## 1. Class → implements → Interface

~~~java
interface Animal {
}

class Dog implements Animal {
}
~~~

A class implements an interface.

---

## 2. Interface → extends → Interface

An interface can extend another interface.

~~~java
interface Animal {
}

interface Pet extends Animal {
}
~~~

An interface uses `extends`, not `implements`, when inheriting from another interface.

---

## 3. Class → implements → Multiple Interfaces

A class can implement multiple interfaces.

~~~java
interface Animal {
}

interface Pet {
}

class Dog implements Animal, Pet {
}
~~~

This is one of the ways Java supports **multiple inheritance of type**.

---

# 7. Multiple Inheritance

Java does **not** allow a class to extend multiple classes.

This is invalid:

~~~java
class A {
}

class B {
}

class C extends A, B { // ❌ Not allowed
}
~~~

However, a class can implement multiple interfaces:

~~~java
interface A {
    void show();
}

interface B {
    void display();
}

class C implements A, B {

    @Override
    public void show() {
        System.out.println("Show");
    }

    @Override
    public void display() {
        System.out.println("Display");
    }
}
~~~

### Relationship

~~~text
             Interface A
                  │
                  │
                  ├──────┐
                  │      │
             Interface B  │
                  │      │
                  └──┬───┘
                     ↓
                Class C
             implements A, B
~~~

### Important terminology

It is more precise to say:

> Java does not support multiple inheritance of classes, but a class can implement multiple interfaces and therefore inherit multiple types/contracts.

---

# 8. Class Implementing an Interface

Suppose an interface declares two abstract methods:

~~~java
interface Animal {

    void sound();
    void eat();
}
~~~

A concrete class implementing it must implement both:

~~~java
class Dog implements Animal {

    @Override
    public void sound() {
        System.out.println("Bark");
    }

    @Override
    public void eat() {
        System.out.println("Eating");
    }
}
~~~

If a class does not implement all required abstract methods, it must itself be declared abstract.

### Incorrect

~~~java
class Dog implements Animal {

    @Override
    public void sound() {
        System.out.println("Bark");
    }

    // eat() is not implemented
    // ❌ Dog must be abstract
}
~~~

### Correct

~~~java
abstract class Dog implements Animal {

    @Override
    public void sound() {
        System.out.println("Bark");
    }

    // eat() remains abstract
}
~~~

### Rule

~~~text
Class implements interface
          ↓
Implement all inherited abstract methods
          ↓
Concrete class
          ↓
Object can be created

OR

Do not implement all
          ↓
Declare class abstract
~~~

---

# 9. Interface Inheritance

An interface can extend one or more interfaces.

~~~java
interface Animal {
    void sound();
}

interface Pet {
    void play();
}

interface Dog extends Animal, Pet {
}
~~~

Now a class implementing `Dog` must provide the required methods from both parent interfaces.

~~~java
class Labrador implements Dog {

    @Override
    public void sound() {
        System.out.println("Bark");
    }

    @Override
    public void play() {
        System.out.println("Playing");
    }
}
~~~

This is another example of multiple inheritance of type.

---

# 10. Why Use an Interface Instead of an Abstract Class?

Interfaces and abstract classes overlap in some capabilities, but they solve different design problems.

## Interface

Useful when the focus is a **contract/capability**:

- Multiple inheritance of type
- Loose coupling
- Contract-based design
- Multiple unrelated classes can implement the same capability
- Interface fields are constants
- No per-object instance state defined by interface fields

Example:

~~~java
interface Printable {
    void print();
}
~~~

Different classes can implement the same contract:

~~~java
class Report implements Printable {

    @Override
    public void print() {
        System.out.println("Printing report");
    }
}

class Invoice implements Printable {

    @Override
    public void print() {
        System.out.println("Printing invoice");
    }
}
~~~

---

## Abstract Class

Useful when related classes need a **shared base implementation or state**:

- Code reuse
- Partial implementation
- Instance variables
- Constructors
- Concrete methods
- Abstract methods

Example:

~~~java
abstract class Animal {

    String name;

    Animal(String name) {
        this.name = name;
    }

    void eat() {
        System.out.println(name + " is eating");
    }

    abstract void sound();
}
~~~

### Mental model

~~~text
Interface
   ↓
"What must you provide?"
   ↓
Contract / capability

Abstract class
   ↓
"What do related classes share?"
   ↓
State + implementation + contract
~~~

---

# 11. Interface vs Abstract Class

| Feature | Interface | Abstract Class |
|---|---|---|
| Direct object creation | ❌ No | ❌ No |
| Interface fields | ✅ public static final | Can have instance/static fields |
| Instance variables | ❌ No instance fields | ✅ Yes |
| Traditional abstract methods | ✅ Yes | ✅ Yes |
| Default methods | ✅ Yes | N/A as a language feature |
| Static methods | ✅ Yes | ✅ Yes |
| Private methods | ✅ Yes (Java 9+) | ✅ Yes |
| Constructors | ❌ No | ✅ Yes |
| Multiple inheritance of type | ✅ Supported | Limited to one superclass |
| Concrete methods | ✅ Default/static/private methods can have bodies | ✅ Yes |
| Code reuse through instance state | Limited | Strong |
| Loose coupling | Common use | Also possible |

> **Important:** Interface vs abstract class is not simply "interface = abstraction" and "abstract class = code reuse". Both can provide abstraction and implementations; the appropriate choice depends on the relationship and design requirement.

---

# 12. Complete Example

~~~java
interface Printable {

    int MAX_COPIES = 10;

    void print();

    default void preview() {
        System.out.println("Preview");
    }

    static void info() {
        System.out.println("Printable interface");
    }

    private void helper() {
        System.out.println("Helper");
    }
}

class Report implements Printable {

    @Override
    public void print() {
        System.out.println("Printing report");
    }

    @Override
    public void preview() {
        System.out.println("Report preview");
    }
}

public class Main {

    public static void main(String[] args) {

        Printable p = new Report();

        p.print();
        p.preview();

        System.out.println(Printable.MAX_COPIES);
        Printable.info();
    }
}
~~~

### Output

~~~text
Printing report
Report preview
10
Printable interface
~~~

This example demonstrates:

- Interface contract
- Interface constant
- Abstract interface method
- Default method
- Static method
- Private interface method
- Implementation
- Overriding
- Interface reference
- Concrete object

---

# 13. Common Interview Traps

### Trap 1: "All interface methods are abstract."

❌ Not in modern Java.

Interfaces can contain:

- Abstract methods
- Default methods
- Static methods
- Private methods

---

### Trap 2: "Interface variables are instance variables."

❌ No.

Interface fields are implicitly:

~~~text
public static final
~~~

They are constants.

---

### Trap 3: "A class can extend multiple interfaces."

❌ The terminology is incorrect.

A class **implements** multiple interfaces.

~~~java
class Dog implements Animal, Pet {
}
~~~

An interface **extends** one or more interfaces.

~~~java
interface Dog extends Animal, Pet {
}
~~~

---

### Trap 4: "Implementing method can be package-private."

❌ Not when implementing a public interface method.

~~~java
public void sound() { }
~~~

must preserve public visibility.

---

## Memory Tricks

### Interface keywords

~~~text
CLASS      → implements → INTERFACE

INTERFACE  → extends   → INTERFACE
~~~

### Interface fields

~~~text
Interface field
      ↓
public + static + final
      ↓
Constant
~~~

### Interface implementation

~~~text
implements
    ↓
All required abstract methods
    ↓
Concrete class
~~~

### Multiple inheritance

~~~text
Multiple classes
      ❌

Multiple interfaces
      ✅
~~~

---

## Interview Questions

<details>
<summary>1. What is an interface?</summary>

An interface defines a contract that implementing classes must fulfill. Modern Java interfaces can also contain default, static, and private methods with implementations.

</details>

<details>
<summary>2. Can we create an object of an interface?</summary>

No. An interface cannot be instantiated directly, but an interface reference can refer to an object of a concrete implementing class.

</details>

<details>
<summary>3. Can an interface have constructors?</summary>

No. Interfaces cannot have constructors.

</details>

<details>
<summary>4. What is the default nature of interface variables?</summary>

Interface fields are implicitly public, static, and final.

</details>

<details>
<summary>5. What is the default nature of an interface abstract method?</summary>

A traditional interface abstract method is implicitly public and abstract.

</details>

<details>
<summary>6. Can an interface have a method with a body?</summary>

Yes. Modern Java interfaces can contain default, static, and private methods with implementations.

</details>

<details>
<summary>7. Can a class implement multiple interfaces?</summary>

Yes.

~~~java
class C implements A, B {
}
~~~

</details>

<details>
<summary>8. Can an interface extend another interface?</summary>

Yes. An interface can extend one or more interfaces.

~~~java
interface C extends A, B {
}
~~~

</details>

<details>
<summary>9. Why must an implementing method be public?</summary>

Because an interface abstract method is public, and an overriding/implementing method cannot reduce visibility.

</details>

<details>
<summary>10. What happens if a class does not implement all inherited abstract interface methods?</summary>

The class must be declared abstract; otherwise, compilation fails.

</details>

<details>
<summary>11. Does Java support multiple inheritance?</summary>

Java does not support multiple inheritance of classes. It supports implementing multiple interfaces, which provides multiple inheritance of type.

</details>

<details>
<summary>12. Can an interface have private methods?</summary>

Yes. Private interface methods were introduced in Java 9 and can be used internally by interface methods.

</details>

<details>
<summary>13. Can an interface have static methods?</summary>

Yes. Static interface methods are called using the interface name.

~~~java
MyInterface.method();
~~~

</details>

---

## Quick Revision

- **Interface → Contract**
- Cannot be instantiated directly.
- Interfaces do not have constructors.
- Interface fields are implicitly **public static final**.
- Traditional interface abstract methods are implicitly **public abstract**.
- Java 8 introduced **default** and **static** interface methods.
- Java 9 introduced **private interface methods**.
- Class → **implements** → interface.
- Interface → **extends** → interface.
- A class can implement multiple interfaces.
- An interface can extend multiple interfaces.
- Implementing methods must preserve public visibility for public interface methods.
- A concrete implementing class must implement all required abstract methods.
- Otherwise, the implementing class must be abstract.
- Java does not support multiple inheritance of classes.
- Interfaces support **multiple inheritance of type**.
- Interface fields are constants, not per-object instance variables.
- **Interface = contract + flexibility + multiple inheritance of type.**

---

## Related Notes

- [OOP Overview](../01-oops-introduction/01-oops-overview.md)
- [Inheritance Basics](../04-inheritance/01-inheritance-basics.md)
- [Method Overriding](../04-inheritance/05-inheritance-and-method-overriding.md)
- [Concrete Class](../09-concrete-class/01-concrete-class.md)
- [Abstract Class](../10-abstract-class/01-abstract-class.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [OOP Home](../)

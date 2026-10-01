<a name="top"></a>

# 🧱 Concrete Class

> **Core idea:** A concrete class is a non-abstract class that can be instantiated directly.

## What is a Concrete Class?

A **concrete class** is a regular Java class that is not declared with the abstract keyword. It can be used directly to create objects.

### Simple definition

> **Concrete class = A class whose object can be created directly.**

~~~java
class Student {

    void display() {
        System.out.println("Hello");
    }
}

Student s = new Student();
s.display();
~~~

Here:

- Student is a concrete class.
- display() is a concrete method.
- new Student() creates an object.
- The object can be used directly.

---

## Why is it called "Concrete"?

Concrete means complete or definite.

In Java, a concrete class provides a usable implementation rather than being declared abstract.

~~~text
Concrete Class
      ↓
Usable class
      ↓
Object can be created
~~~

---

## Basic Syntax

~~~java
class ClassName {

    // fields
    // constructors
    // concrete methods
}
~~~

Object creation:

~~~java
ClassName object = new ClassName();
~~~

---

## Example

~~~java
class Student {

    String name;

    void display() {
        System.out.println("Student: " + name);
    }
}

public class Main {

    public static void main(String[] args) {

        Student s = new Student();

        s.name = "Ravi";
        s.display();
    }
}
~~~

### Output

~~~text
Student: Ravi
~~~

### Step-by-step

~~~text
class Student
      ↓
Concrete class
      ↓
new Student()
      ↓
Student object created
      ↓
s.display()
      ↓
Method executes
~~~

---

## Key Characteristics

### 1. It is a regular class

A concrete class is not declared using the abstract keyword.

~~~java
class Student {
}
~~~

### 2. An object can be created

~~~java
Student s = new Student();
~~~

This is the most important distinction from an abstract class.

### 3. It can contain concrete methods

A concrete method has an implementation/body.

~~~java
void display() {
    System.out.println("Hello");
}
~~~

A concrete class can also contain constructors, instance variables, static members, and other normal class members.

### 4. It can be used directly by client code

Because an instance can be created, the class can directly represent an object required by the program.

---

## Concrete Class and Constructors

A concrete class can have constructors.

~~~java
class Student {

    Student() {
        System.out.println("Constructor called");
    }
}
~~~

Object creation:

~~~java
Student s = new Student();
~~~

Output:

~~~text
Constructor called
~~~

If no constructor is explicitly declared, Java may provide a default constructor when the normal default-constructor rules apply.

---

## Concrete Class vs Abstract Class

| Feature | Concrete Class | Abstract Class |
|---|---|---|
| Declared with abstract? | No | Yes |
| Direct object creation | ✅ Allowed | ❌ Not allowed |
| Concrete methods | ✅ Yes | ✅ Yes |
| Abstract methods | ❌ No | ✅ Can have |
| Constructor | ✅ Yes | ✅ Yes |
| Instance variables | ✅ Yes | ✅ Yes |
| Static members | ✅ Yes | ✅ Yes |

> **Important:** An abstract class can contain concrete methods, and it can even contain no abstract methods. The defining restriction is that the abstract class itself cannot be instantiated directly.

---

## Relationship with Inheritance

A concrete class can extend another class.

It can also extend an abstract class when it implements all inherited abstract methods.

~~~java
abstract class Animal {

    abstract void sound();
}

class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Bark");
    }
}
~~~

Dog is concrete because it provides the required implementation.

~~~text
Abstract Parent
      ↓
abstract method
      ↓
Concrete Child
      ↓
implements required method
      ↓
Object can be created
~~~

---

## Memory Trick

> **Concrete = Complete enough to Create an object.**

~~~text
CONCRETE
    ↓
CAN CREATE
    ↓
OBJECT
~~~

---

## Interview Questions

<details>
<summary>1. What is a concrete class?</summary>

A concrete class is a non-abstract class that can be instantiated directly to create objects.

</details>

<details>
<summary>2. Can we create an object of a concrete class?</summary>

Yes. A concrete class can be instantiated using the new operator, subject to constructor accessibility.

</details>

<details>
<summary>3. Can a concrete class contain constructors?</summary>

Yes. A concrete class can have one or more constructors.

</details>

<details>
<summary>4. Can a concrete class extend an abstract class?</summary>

Yes. A concrete subclass must provide implementations for all inherited abstract methods that it is required to implement.

</details>

<details>
<summary>5. Does Java have a concrete keyword?</summary>

No. Java has no concrete keyword. The term concrete class describes a non-abstract class that can be instantiated.

</details>

---

## Quick Revision

- A **concrete class** is a non-abstract class.
- Its object can be created directly.
- It can contain concrete methods.
- It can have constructors.
- It can have instance variables and static members.
- Java does **not** have a concrete keyword.
- A concrete subclass of an abstract class must implement the required inherited abstract methods.
- **Concrete → Can create an object.**

---

## Related Notes

- [OOP Overview](../01-oops-introduction/01-oops-overview.md)
- [Inheritance Basics](../04-inheritance/01-inheritance-basics.md)
- [Object Creation Overview](../08-object-creation/01-object-creation-overview.md)
- [Abstract Class](../10-abstract-class/01-abstract-class.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [OOP Home](../)

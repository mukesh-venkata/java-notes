<a name="top"></a>

# 🏗️ Java Constructor Basics

> **Topic 21 • Constructors**

A **constructor** is a special class member used to initialize a newly created object.

## 1️⃣ What Is a Constructor?

A constructor:

- Has the **same name as the class**.
- Has **no return type**, not even `void`.
- Runs as part of object creation or constructor chaining.
- Is commonly used to initialize an object's instance state.

Example:

```java
class Student {

    Student() {
        System.out.println("Student object created");
    }
}
```

Creating the object:

```java
Student s = new Student();
```

Conceptually:

```text
new Student()
      ↓
Object is created
      ↓
Constructor executes
      ↓
Object is initialized
```

> **Important:** Saying a constructor is “called automatically” is a beginner-friendly description of what happens during `new Student()`. Constructors can also be invoked through constructor chaining using `this()` or `super()`.

## 2️⃣ Constructor vs Method

Do not confuse a constructor with a method.

| Constructor | Method |
|---|---|
| Same name as class | Can have any valid method name |
| No return type | Has a return type or `void` |
| Used during object construction | Performs an operation |
| Cannot be called like an ordinary method | Can be invoked explicitly |
| Can be overloaded | Can be overloaded |

Example:

```java
class Student {

    Student() {                 // constructor
        System.out.println("Constructor");
    }

    void display() {            // method
        System.out.println("Method");
    }
}
```

This is **not** a constructor:

```java
void Student() {
}
```

Because it has a return type, it is a method named `Student`.

## 3️⃣ Initialization vs Instantiation

These two terms are important.

### 🔹 Instantiation

**Instantiation** means creating an object from a class.

```java
Student s = new Student();
```

The `new Student()` expression creates an instance.

### 🔹 Initialization

**Initialization** means assigning the initial state/values required for the object.

For example:

```java
class Student {

    int age;

    Student(int age) {
        this.age = age;
    }
}
```

Here the constructor initializes the object's `age`.

### 🧠 Easy Difference

```text
Instantiation → Create the object

Initialization → Give the object its initial state
```

## 4️⃣ Why Do We Need Constructors?

Without a constructor, an object can still be created, but you may need separate statements to establish its state.

Example:

```java
class Student {
    String name;
    int age;
}

Student s = new Student();
s.name = "Mukesh";
s.age = 27;
```

A constructor can combine the required initialization:

```java
class Student {

    String name;
    int age;

    Student(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

Student s = new Student("Mukesh", 27);
```

This makes object creation and initialization more structured.

## 5️⃣ Constructor Execution

Consider:

```java
class Student {

    int age = 20;

    Student(int age) {
        this.age = age;
    }
}
```

When:

```java
Student s = new Student(27);
```

the object-construction process includes allocating the object and performing the class's initialization steps before the constructor body completes.

For a simple class, think:

```text
new Student(27)
      ↓
Object creation
      ↓
Instance initialization
      ↓
Constructor body
      ↓
Reference receives object
```

The complete initialization rules become especially important when fields, initializer blocks, inheritance, and `super()` are involved.

## 6️⃣ Constructor Syntax

General form:

```java
class ClassName {

    ClassName(parameters) {
        // initialization
    }
}
```

Example:

```java
class Employee {

    int id;
    String name;

    Employee(int id, String name) {
        this.id = id;
        this.name = name;
    }
}
```

## 7️⃣ Important Rules

- Constructor name must match the class name.
- Constructors cannot have a return type.
- Constructors can be overloaded.
- Constructors are not inherited.
- A constructor can call another constructor using `this()`.
- A constructor can invoke a parent constructor using `super()`.
- `this()` or `super()`, when explicitly used, must be the first statement in the constructor.
- A constructor cannot directly invoke both `this()` and `super()` in the same constructor because only one constructor-invocation statement can appear first.

## 🧠 Memory Trick

**SAME NAME + NO RETURN TYPE + INITIALIZE OBJECT**

## 🎤 Interview Questions

**Q1. What is a constructor?**  
A class member used during object construction to initialize the newly created object.

**Q2. Can a constructor have a return type?**  
No. Not even `void`.

**Q3. Can constructors be overloaded?**  
Yes, by using different parameter lists.

**Q4. Are constructors inherited?**  
No.

**Q5. What is the difference between instantiation and initialization?**  
Instantiation creates an object; initialization establishes its initial state.

➡️ [Constructor Types](./02-constructor-types.md)  
➡️ [Constructor Overloading](./03-constructor-overloading.md)  
➡️ [Constructor Chaining](./04-constructor-chaining.md)

🏠 [Java Notes Home](../../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

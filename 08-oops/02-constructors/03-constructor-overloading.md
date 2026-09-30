# 🔀 Constructor Overloading

> **Topic 21 • Constructors**

**Constructor overloading** means defining multiple constructors in the same class with different parameter lists.

It allows objects of the same class to be initialized in different ways.

## 1️⃣ Basic Example

```java
class Student {

    Student() {
        System.out.println("No-arg constructor");
    }

    Student(int age) {
        System.out.println("Age: " + age);
    }

    Student(int age, String name) {
        System.out.println(age + " " + name);
    }
}
```

Different constructors can have different:

- Number of parameters
- Types of parameters
- Order of parameter types

## 2️⃣ Different Number of Parameters

```java
class Student {

    Student() {
    }

    Student(int age) {
    }

    Student(int age, String name) {
    }
}
```

The compiler selects the constructor whose parameter list matches the invocation.

```java
new Student();
new Student(27);
new Student(27, "Mukesh");
```

## 3️⃣ Different Parameter Types

```java
class Demo {

    Demo(int value) {
    }

    Demo(String value) {
    }
}
```

Both constructors are valid because their parameter types differ.

## 4️⃣ Different Parameter Order

```java
class Demo {

    Demo(int id, String name) {
    }

    Demo(String name, int id) {
    }
}
```

The parameter type sequence is different, so the constructors are overloaded.

## 5️⃣ What Is Not Overloading?

Changing only parameter names does not create an overload.

❌ Invalid:

```java
Student(int age) {
}

Student(int marks) {
}
```

Both have the same parameter type list: `(int)`.

Also, a return type is not part of a constructor signature because constructors do not have return types.

## 6️⃣ Constructor Selection

When you write:

```java
Student s = new Student(27);
```

the compiler looks for a matching constructor.

```text
new Student(27)
      ↓
Available constructors
      ↓
(int) matches
      ↓
Student(int) selected
```

If no applicable constructor exists, compilation fails.

## 7️⃣ Constructor Overloading and Compile-Time Polymorphism

Constructor overloading is commonly described as **compile-time polymorphism** because the applicable constructor is determined during compilation based on the argument list.

Example:

```java
Student s1 = new Student();
Student s2 = new Student(27);
Student s3 = new Student(27, "Mukesh");
```

Different constructor signatures support different initialization paths.

## 8️⃣ Why Use Constructor Overloading?

It gives callers multiple ways to create a valid object.

For example:

```java
class Employee {

    int id;
    String name;
    String department;

    Employee(int id) {
        this.id = id;
    }

    Employee(int id, String name) {
        this.id = id;
        this.name = name;
    }

    Employee(int id, String name, String department) {
        this.id = id;
        this.name = name;
        this.department = department;
    }
}
```

The caller can provide only the information available at creation time.

## 9️⃣ Overloading Rules

Remember:

- Same class
- Same constructor name — naturally the class name
- Different parameter list
- Number, type, or order can differ
- Parameter names alone cannot distinguish constructors
- Return type is not involved
- Constructor overloading is resolved at compile time

## 🧠 Memory Trick

**NUMBER / TYPE / ORDER → OVERLOAD**

## 🎤 Interview Questions

**Q1. Can constructors be overloaded?**  
Yes.

**Q2. Can constructors differ only by parameter names?**  
No.

**Q3. Does return type participate in constructor overloading?**  
No.

**Q4. Is constructor overloading compile-time polymorphism?**  
It is commonly described as compile-time polymorphism because the applicable overloaded constructor is selected during compilation.

**Q5. What happens if no matching constructor exists?**  
The code fails to compile.

➡️ [Constructor Types](./02-constructor-types.md)  
➡️ [Constructor Chaining](./04-constructor-chaining.md)

🏠 [Java Notes Home](../../README.md)

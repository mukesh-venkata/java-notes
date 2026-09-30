# 03. Non-Primitive / Reference Data Types

<div align="center">

![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Topic](https://img.shields.io/badge/Topic-Reference%20Types-2DD4BF?style=for-the-badge)

</div>

---

> Reference types describe variables that can refer to objects, arrays, or other reference-type values.

## 🧠 Mnemonic: SAIC

~~~mermaid
flowchart LR
    A[Reference Types] --> B[String]
    A --> C[Array]
    A --> D[Interface]
    A --> E[Class]
~~~

| Letter | Type | Description |
|---|---|---|
| **S** | **String** | Sequence of characters |
| **A** | **Array** | Stores multiple values of the same type |
| **I** | **Interface** | Defines a contract that classes can implement |
| **C** | **Class** | Blueprint used for creating objects |

> **SAIC = String → Array → Interface → Class**

## 1️⃣ String

String represents a sequence of characters.

~~~java
String name = "Java";
~~~

String is a **class**, not a primitive data type.

## 2️⃣ Array

An array stores multiple values under one variable name.

~~~java
int[] numbers = {10, 20, 30};
~~~

Arrays are objects in Java, so an array variable is a reference variable.

~~~text
numbers
   │
   └────────► [10, 20, 30]
~~~

## 3️⃣ Interface

An interface defines a contract that implementing classes agree to follow.

~~~java
interface Animal {
    void sound();
}

class Dog implements Animal {

    public void sound() {
        System.out.println("Bark");
    }
}

Animal animal = new Dog();
~~~

## 4️⃣ Class

A class is a blueprint from which objects can be created.

~~~java
class Car {
    String model;
}

Car car = new Car();
~~~

Here:

- **Car** → class type
- **car** → reference variable
- **new Car()** → object creation expression

## 🧠 Reference Variable vs Object

~~~text
String name = "Java";

Reference Variable
      name
       │
       │ refers to
       ▼
    String Object
    ┌─────────────┐
    │   "Java"    │
    └─────────────┘
~~~

Another example:

~~~text
Car car = new Car();

car
 │
 └──────────────► Car object
                  ┌───────────┐
                  │  model    │
                  └───────────┘
~~~

> **Important:** The simplified statement "references are on stack and objects are on heap" is not a universal Java language rule. Common JVM implementations generally allocate objects on the heap, but exact implementation details are JVM-dependent.

## 🔄 Primitive vs Reference

| Feature | Primitive | Reference |
|---|---|---|
| Examples | int, double, char | String, arrays, classes |
| Built-in primitive types | 8 | Many reference types |
| Variable represents | A primitive value | A reference to an object/array or null |
| Methods | No methods on the primitive value itself | Objects can provide methods |
| Example | int age = 27 | String name = "Java" |

## ⚠️ null

Reference variables can hold null:

~~~java
String name = null;
~~~

Primitive variables cannot:

~~~java
int age = null;    // Compile-time error
~~~

## ⚡ 30-Second Revision

~~~text
Reference Types
      ↓
    SAIC
      ↓
S → String
A → Array
I → Interface
C → Class
~~~

**Reference variable → refers to an object, array, or another reference value.**

<details>
<summary>🎯 Interview Quick Check</summary>

**Q: Is String primitive or reference type?**  
A: Reference type; String is a class.

**Q: Are arrays primitive?**  
A: No. Arrays are objects, so array variables are reference types.

**Q: Can a primitive variable contain null?**  
A: No.

**Q: Can a reference variable contain null?**  
A: Yes.

</details>

---

## 🧭 Navigation

⬅️ [Data Types Overview](01-data-types-overview.md) • 📚 Data Types

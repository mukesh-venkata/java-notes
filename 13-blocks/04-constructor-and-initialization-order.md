# 🏗️ Constructor & Initialization Order

> **Topic 20 • Blocks**

The easiest way to understand this is to separate **class initialization** from **object creation**.

## 🟣 Class Initialization

~~~text
Class initialized
      ↓
Static fields / static blocks
~~~

Static initialization happens once for the class.

## 🟢 Object Creation

For a simple class:

~~~text
new Student()
      ↓
Instance fields
      ↓
Instance block
      ↓
Constructor
~~~

## Example

~~~java
class Student {
    static {
        System.out.println("Static");
    }

    int age = 20;

    {
        System.out.println("Instance Block");
    }

    Student() {
        System.out.println("Constructor");
    }
}
~~~

### 🧠 Easy Trick

**Class → Static**  
**Object → Instance → Constructor**

Inheritance has additional constructor-chaining rules. We will learn those properly in the **Inheritance** section instead of mixing them into this basic topic.

🏠 [Java Notes Home](../README.md)
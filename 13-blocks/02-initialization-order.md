<a name="top"></a>

# 🔄 Java Initialization Order

> **Topic 13 • Blocks**

The easiest way to understand initialization is to separate **class initialization** from **object creation**.

## 🟣 Part 1 — Class Initialization

When a class is initialized, its static initialization is performed.

~~~text
Class initialization
       ↓
Static field initialization / static blocks
~~~

For the normal application class, static initialization occurs before that class's main method is invoked when the class is initialized as the entry point.

## 🟢 Part 2 — Object Creation

When an object is created, instance initialization happens before the constructor body.

For a simple class:

~~~text
new Student()
      ↓
Instance field initialization
      ↓
Instance initialization block
      ↓
Constructor body
~~~

## 💻 Complete Example

~~~java
class Student {

    static {
        System.out.println("Static Block");
    }

    int age = 20;

    {
        System.out.println("Instance Block");
    }

    Student() {
        System.out.println("Constructor");
    }

    public static void main(String[] args) {
        System.out.println("main");
        new Student();
    }
}
~~~

A simple way to think about the output is:

~~~text
Static Block
main
Instance Block
Constructor
~~~

The broader Java initialization rules become more detailed with inheritance, explicit constructor calls and other language features.

## 🧬 Inheritance Preview

When inheritance is introduced, initialization involves the parent class before the child class, and object construction initializes the parent part before the child part.

~~~text
Parent class initialization
        ↓
Child class initialization
        ↓
Object construction
        ↓
Parent instance initialization
        ↓
Parent constructor
        ↓
Child instance initialization
        ↓
Child constructor
~~~

This is only a preview. The detailed constructor-chaining rules will be covered later in **Inheritance**, rather than making this basic Blocks topic unnecessarily difficult.

## 🧠 Easy Memory Trick

**CLASS → STATIC**

**OBJECT → INSTANCE → CONSTRUCTOR**

## 🎤 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>When does a static block run?</summary>
<br>

During class initialization.

</details>

<details>
<summary>When does an instance block run?</summary>
<br>

During object construction, after instance field initializers and before the constructor body for that class.

</details>

<details>
<summary>What happens before the constructor body?</summary>
<br>

Instance field initialization and instance initialization blocks for that class execute before the constructor body.

</details>
## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

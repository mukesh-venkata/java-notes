<a name="top"></a>

# 🎯 `this` for Instance Variables

> **Topic 22 • `this` Keyword**

The most common use of `this` is distinguishing an **instance variable** from a constructor or method parameter with the same name.

## 1️⃣ The Name-Shadowing Problem

~~~java
class Student {
    String name;

    Student(String name) {
        name = name;
    }
}
~~~

Both `name` references inside the constructor refer to the parameter. The instance variable is not selected automatically.

## 2️⃣ Use `this.name`

~~~java
class Student {
    String name;

    Student(String name) {
        this.name = name;
    }
}
~~~

Meaning:

~~~text
this.name → current object's instance variable
name      → constructor parameter
~~~

So:

`this.name = name;`

means:

> Assign the parameter `name` to the current object's `name` field.

## 3️⃣ Example

~~~java
class Student {
    String name;
    int age;

    Student(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
~~~

For `new Student("Mukesh", 27)`:

~~~text
Current object
name = "Mukesh"
age  = 27

Constructor parameters
name = "Mukesh"
age  = 27
~~~

## 4️⃣ Multiple Objects

If:

~~~java
Student s1 = new Student("A", 20);
Student s2 = new Student("B", 25);
~~~

then during construction:

~~~text
this → s1
~~~

and later:

~~~text
this → s2
~~~

So `this` represents whichever object is the current receiver of the instance invocation.

## 5️⃣ Can `this` Be Omitted?

Often yes, when there is no ambiguity.

~~~java
class Student {
    int age;

    void show() {
        System.out.println(age);
    }
}
~~~

This can be written explicitly as:

~~~java
void show() {
    System.out.println(this.age);
}
~~~

But when a parameter has the same name, `this` makes the distinction explicit:

~~~java
Student(int age) {
    this.age = age;
}
~~~

## 🧠 Memory Trick

**`this.field` = current object's field**

## 🎤 Interview Questions

**Q1. Why use `this` in constructors?**  
To distinguish an instance variable from a parameter with the same name.

**Q2. What does `this.name = name` mean?**  
Assign the parameter to the current object's instance variable.

**Q3. Can `this` be omitted when there is no name conflict?**  
Often yes.

➡️ [`this` Basics](./01-this-keyword-basics.md)
➡️ [Constructor & Method Calls](./03-this-constructor-and-method-calls.md)

🏠 [Java Notes Home](../../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

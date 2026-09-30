<a name="top"></a>

# ⚡ `this` Keyword — Quick Revision

> **Topic 22 • 30-Second Revision**

## 🧠 Master Idea

~~~text
this
 ↓
CURRENT OBJECT
~~~

## 5 Important Uses

| # | Use | Example |
|---:|---|---|
| 1 | Current object's instance variable | `this.name` |
| 2 | Another constructor in same class | `this()` |
| 3 | Current object's instance method | `this.show()` |
| 4 | Pass current object as argument | `show(this)` |
| 5 | Return current object | `return this` |

## 🔥 Memory Map

~~~text
this.variable → instance variable
this()        → same-class constructor
this.method() → current object's method
method(this)  → pass current object
return this   → return current object
~~~

## ⚠️ Important Rules

- `this` refers to the current object.
- It is used in an instance context.
- It cannot be directly used inside a static method.
- Explicit `this()` must be the first statement in a constructor.
- `this()` calls another constructor in the same class.
- `this.method()` calls an instance method on the current object.
- Passing or returning `this` does not create a new object.

## 🎯 Common Example

~~~java
class Student {
    String name;

    Student(String name) {
        this.name = name;
    }

    void display() {
        this.show();
    }

    void show() {
        System.out.println(this.name);
    }
}
~~~

## 🎤 Interview Questions & Answers

> **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>What is `this`?</summary>
<br>

Current object reference in an instance context.

</details>

<details>
<summary>Why use `this.name = name`?</summary>
<br>

To distinguish the instance field from the parameter.

</details>

<details>
<summary>What does `this()` do?</summary>
<br>

Calls another constructor in the same class.

</details>

<details>
<summary>What does `this.show()` do?</summary>
<br>

Calls `show()` on the current object.

</details>

<details>
<summary>What does `return this` do?</summary>
<br>

Returns the current object reference.

</details>

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

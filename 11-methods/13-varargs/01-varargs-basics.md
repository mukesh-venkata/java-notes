<a name="top"></a>
# 🔢 1. Varargs — Basics
> **Core idea:** Varargs allows a method to accept a variable number of arguments of the same type.
## 🧠 What Is Varargs?
**Varargs** means **variable-length arguments**. It allows a method to accept zero, one, or multiple arguments.
### Syntax
```java
public void add(int... values) {
}
```
The three dots indicate a **varargs parameter**.
## 📌 Basic Example
```java
public void add(int... values) {
    for (int value : values) {
        System.out.println(value);
    }
}
```
Valid calls:
```java
add();
add(10);
add(10, 20);
add(10, 20, 30);
```
## 🔍 Why Use Varargs?
Instead of separate methods for one, two, three, or more inputs, one method can handle a flexible number of inputs.
## 🧠 Memory Trick
> **Varargs = variable number of arguments**
## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What is varargs?</summary>
<br>

A Java feature that allows a method to accept a variable number of arguments of a compatible type.

</details>

<details>
<summary>Q2. What symbol represents varargs?</summary>
<br>

Three dots: ...

</details>

<details>
<summary>Q3. Can a varargs method be called with zero arguments?</summary>
<br>

Yes. The varargs parameter receives an empty array for that invocation.

</details>

<details>
<summary>Q4. What type of values can one varargs parameter accept?</summary>
<br>

Values compatible with the declared element type of the varargs parameter.

</details>
## 🔗 Related Notes
- [Varargs Rules & Parameters →](02-varargs-rules-and-parameters.md)
- [Varargs as Array & Method Calls →](03-varargs-as-array-and-method-calls.md)
- [Varargs Quick Revision →](04-varargs-quick-revision.md)
- [Methods Overview →](../01-methods-overview.md)
## 🧭 Navigation
⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

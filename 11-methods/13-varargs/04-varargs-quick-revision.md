<a name="top"></a>
# ⚡ 4. Varargs — Quick Revision
> **30-second revision:** Varargs lets a method accept a variable number of arguments of a declared type.
## 🧠 Core Rules
| Rule | Remember |
|---|---|
| Syntax | type... name |
| Number of varargs parameters | Only one |
| Position | Must be last |
| Normal parameters | Can appear before varargs |
| Inside method | Treated as an array |
| Arguments | Zero, one, or many |
## Example
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
## With Normal Parameters
```java
public void printNumbers(String name, int... numbers) {
    System.out.println(name);
    for (int number : numbers) {
        System.out.println(number);
    }
}
```
Remember:
```text
normal parameters → varargs → LAST
```
## 🔄 Array Connection
```text
int... values
     ↓
treated as int[] inside method
     ↓
values.length
values[index]
for-each
```
A compatible array can also be passed directly.
## 🧠 Memory Trick
> **One varargs + always last + internally array**
## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What is varargs?</summary>
<br>

A Java feature that allows a method to accept a variable number of arguments of a compatible type.

</details>

<details>
<summary>2. What syntax represents varargs?</summary>
<br>

Three dots: ...

</details>

<details>
<summary>3. Can a method have two varargs parameters?</summary>
<br>

No. A method can have at most one variable-arity parameter.

</details>

<details>
<summary>4. Can normal parameters come before varargs?</summary>
<br>

Yes. The varargs parameter must be the last parameter.

</details>

<details>
<summary>5. Can a parameter come after varargs?</summary>
<br>

No. The variable-arity parameter must be last.

</details>

<details>
<summary>6. What is varargs treated as inside the method?</summary>
<br>

An array of the declared element type.

</details>

<details>
<summary>7. Can a varargs method be called with zero arguments?</summary>
<br>

Yes. The varargs parameter receives an empty array for that invocation.

</details>

<details>
<summary>8. Can a compatible array be passed directly?</summary>
<br>

Yes. A compatible array can be passed directly to a varargs parameter.

</details>
## 🔗 Related Notes
- [Varargs Basics →](01-varargs-basics.md)
- [Varargs Rules & Parameters →](02-varargs-rules-and-parameters.md)
- [Varargs as Array & Method Calls →](03-varargs-as-array-and-method-calls.md)
## 🧭 Navigation
⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

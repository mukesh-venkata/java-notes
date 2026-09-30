<a name="top"></a>
# 📋 2. Varargs — Rules & Parameters
> **Core idea:** Varargs has a few important declaration rules.
## 1️⃣ Only One Varargs Parameter
A method can have **only one varargs parameter**.
### Valid
```java
void add(int... values) {
}
```
### Invalid
```java
void add(int... values, int... more) {  // ❌
}
```
## 2️⃣ Varargs Must Be the Last Parameter
### Valid
```java
void add(String name, int... numbers) {
}
```
### Invalid
```java
void add(int... numbers, String name) {  // ❌
}
```
The compiler needs to know which arguments belong to the variable-length parameter.
## 3️⃣ Normal Parameters Can Come Before Varargs
```java
void printNumbers(String label, int... numbers) {
    System.out.println(label);
    for (int number : numbers) {
        System.out.println(number);
    }
}
```
Calls:
```java
printNumbers("Numbers");
printNumbers("Numbers", 10);
printNumbers("Numbers", 10, 20, 30);
```
## 🧠 Declaration Pattern
```text
normal parameter(s) → varargs parameter
                           ↑
                         LAST
```
## 🎯 Interview Questions
1. How many varargs parameters can a method have? **Only one.**
2. Where must the varargs parameter appear? **Last.**
3. Can normal parameters appear before varargs? **Yes.**
4. Can a parameter appear after varargs? **No.**
## 🔗 Related Notes
- [Varargs Basics →](01-varargs-basics.md)
- [Varargs as Array & Method Calls →](03-varargs-as-array-and-method-calls.md)
- [Varargs Quick Revision →](04-varargs-quick-revision.md)
## 🧭 Navigation
⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

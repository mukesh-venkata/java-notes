<a name="top"></a>
# 🔄 3. Varargs as Array & Method Calls
> **Core idea:** Inside the method body, a varargs parameter is treated as an array.
## 🧠 Internally Treated as an Array
```java
public void add(int... values) {
    for (int value : values) {
        System.out.println(value);
    }
}
```
Conceptually:
```text
add(10, 20, 30)
       ↓
int[] values
       ↓
[10, 20, 30]
```
## 1️⃣ Zero Arguments
```java
add();
```
The varargs parameter receives an **empty array**.
## 2️⃣ One Argument
```java
add(10);
```
Conceptually: [10]
## 3️⃣ Multiple Arguments
```java
add(10, 20, 30);
```
Conceptually:
```text
index:   0    1    2
values: [10] [20] [30]
```
## 4️⃣ Array Operations
Because the varargs parameter is an array, normal array operations can be used.
```java
public void add(int... values) {
    System.out.println(values.length);
    if (values.length > 0) {
        System.out.println(values[0]);
    }
}
```
You can also use an enhanced for loop.
## 🔍 Passing an Array Directly
A compatible array can be passed directly:
```java
int[] numbers = {10, 20, 30};
add(numbers);
```
## ⚠️ Varargs Is Not “Any Type”
The supplied arguments must be compatible with the declared element type.
```java
void add(int... values)
void print(String... values)
```
## 🎯 Interview Questions
1. What is a varargs parameter treated as inside the method? **An array.**
2. What happens with zero arguments? **An empty array is received.**
3. Can a compatible array be passed directly? **Yes.**
4. Can unrelated types be passed? **No.**
## 🔗 Related Notes
- [Varargs Basics →](01-varargs-basics.md)
- [Varargs Rules & Parameters →](02-varargs-rules-and-parameters.md)
- [Varargs Quick Revision →](04-varargs-quick-revision.md)
## 🧭 Navigation
⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

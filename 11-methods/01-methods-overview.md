<a name="top"></a>

# 🧩 Java Methods — Overview

> **Topic 18 • Methods**

A **method** is a named block of code that performs a specific task.

Methods help make programs reusable, modular, readable and easier to maintain.

## 🏗️ Basic Structure

```java
public int add(int a, int b) {
    return a + b;
}
```

Think:

```text
Access modifier
      ↓
Return type
      ↓
Method name
      ↓
Parameters
      ↓
Method body
```

## 🎯 Why Use Methods?

Instead of repeating the same logic, put it in one method and call it wherever needed.

```text
             Method
                ↓
       ┌────────┼────────┐
       ↓        ↓        ↓
      Call     Call     Call
```

## 🧠 Method Building Blocks

A method can involve:

- Access modifier
- Return type
- Method name
- Parameter list
- Method body
- `return` statement when a value must be returned

## 💻 Example

```java
public int multiply(int a, int b) {
    return a * b;
}

int result = multiply(4, 5);
System.out.println(result); // 20
```

## 🎤 Interview Quick Check

**What is a method?**  
A named block of code that performs a task.

**Why use methods?**  
For reuse, modularity, readability and maintainability.

**Can a method return no value?**  
Yes. A `void` method does not return a value.

## 🔗 Navigation

➡️ [Declaration & Definition](./02-method-declaration-and-definition.md)

➡️ [Method Signature](./03-method-signature.md)

➡️ [Static & Instance Methods](./04-static-and-instance-methods.md)

➡️ [Method Binding](./05-method-binding.md)

➡️ [Overloading](./06-method-overloading.md)

➡️ [Overriding](./07-method-overriding.md)

➡️ [Overriding vs Overloading](./08-overriding-vs-overloading.md)

➡️ [Access & Overriding Rules](./09-method-access-and-overriding-rules.md)

➡️ [Recursion](./10-recursion.md)

➡️ [Method Hiding](./11-method-hiding.md)

➡️ [Quick Revision](./12-methods-quick-revision.md)

🏠 [Java Notes Home](../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

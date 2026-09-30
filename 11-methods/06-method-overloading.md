# 🔀 Java Method Overloading

> **Topic 18 • Methods**

**Method overloading** means defining methods with the same name but different parameter lists.

It is commonly described as **compile-time polymorphism**.

## 💻 Examples

### Different Number of Parameters

```java
int add(int a, int b)
int add(int a, int b, int c)
```

### Different Parameter Types

```java
int add(int a, int b)
double add(double a, double b)
```

### Different Parameter Order / Types

```java
void display(int a, double b)
void display(double a, int b)
```

## ❌ Return Type Alone Is Not Enough

```java
int add(int a, int b)
double add(int a, int b)
```

Not a valid overload pair because return type is not part of the method signature.

## 🧠 What About `main()`?

Java permits overloading a method named `main`. The Java launcher still looks for the recognized application entry-point form.

## 🎤 Interview Quick Check

**What changes in overloading?**  
The parameter list.

**Can methods be overloaded only by changing return type?**  
No.

**Is overloading compile-time or runtime polymorphism?**  
It is commonly classified as compile-time polymorphism.

## 🔗 Navigation

⬅️ [Method Binding](./05-method-binding.md)

➡️ [Overriding](./07-method-overriding.md)

➡️ [Overriding vs Overloading](./08-overriding-vs-overloading.md)

➡️ [Quick Revision](./12-methods-quick-revision.md)

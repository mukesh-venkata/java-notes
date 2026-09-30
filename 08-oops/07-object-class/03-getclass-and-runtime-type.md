<a name="top"></a>

# 🏷️ 3. getClass() & Runtime Type

> **Core idea:** `getClass()` returns the runtime class of the object.

## 🧠 What Does getClass() Do?

The `getClass()` method returns a `Class<?>` object representing the runtime class of the object.

Example:

```java
Student student = new Student();

System.out.println(student.getClass());
```

A possible output is:

```text
class Student
```

The exact printed form depends on the class and package.

## 🔄 Runtime Type

Consider:

```java
Animal animal = new Dog();
```

The reference type is `Animal`, but the actual runtime object is a `Dog`.

Therefore:

```java
animal.getClass()
```

represents `Dog.class`.

```text
Reference type  → Animal
Runtime object  → Dog
                      ↓
                 getClass()
                      ↓
                  Dog.class
```

## 📌 Why Is This Useful?

It can be used when runtime type information is needed.

For example:

```java
if (animal.getClass() == Dog.class) {
    System.out.println("Runtime object is Dog");
}
```

Use this carefully; normal polymorphism and `instanceof` are often more appropriate when the goal is checking type compatibility.

## ⚠️ getClass() and static Type

`getClass()` describes the actual object at runtime, not merely the declared reference type.

```java
Animal animal = new Dog();

System.out.println(animal.getClass() == Dog.class); // true
```

## 🎯 Interview Questions

### Q1. What does getClass() return?
A `Class<?>` object representing the object's runtime class.

### Q2. Is getClass() based on the reference type?
No. It reports the runtime class of the actual object.

### Q3. What happens if the reference is null?
Calling an instance method through a null reference causes `NullPointerException`.

## 🔗 Related Notes

- [Object Class Overview →](01-object-class-overview.md)
- [toString(), hashCode() & equals() →](02-tostring-hashcode-equals.md)
- [clone() & Shallow Copy →](04-clone-and-shallow-copy.md)
- [Quick Revision →](07-object-class-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

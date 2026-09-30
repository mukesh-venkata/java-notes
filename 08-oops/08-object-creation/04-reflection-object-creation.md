<a name="top"></a>

# 🔬 4. Object Creation Using Reflection

> **Core idea:** Reflection can create objects dynamically when the class and constructor are discovered at runtime.

## 🕰️ Older Approach: Class.newInstance()

An older reflection approach was:

```java
Class<?> clazz = Class.forName("Student");
Student student = (Student) clazz.newInstance();
```

However, `Class.newInstance()` has been **deprecated since Java 9**.

## ✅ Modern Approach

The preferred reflection mechanism is to obtain a `Constructor` and invoke `newInstance()`.

For a no-argument constructor:

```java
Class<?> clazz = Class.forName("Student");

Student student = (Student)
        clazz.getDeclaredConstructor().newInstance();
```

This is runtime-driven object creation.

## 🔍 How It Works

```text
Class.forName(...)
       ↓
Class object
       ↓
getDeclaredConstructor()
       ↓
Constructor object
       ↓
newInstance()
       ↓
New object
```

## ⚙️ Parameterized Constructor

Suppose:

```java
class Student {
    Student(String name, int age) {
    }
}
```

Reflection can select that constructor:

```java
Constructor<Student> constructor =
        Student.class.getDeclaredConstructor(String.class, int.class);

Student student = constructor.newInstance("Alex", 27);
```

## 📌 Why Use Reflection?

Reflection can be useful when:

- The class is selected dynamically.
- Constructor information is discovered at runtime.
- Frameworks or tools need runtime type information.

## ⚠️ Important

Reflection can involve checked exceptions and access restrictions. Modern code should prefer the appropriate `Constructor.newInstance()` API instead of the deprecated `Class.newInstance()`.

## 🎯 Interview Questions

### Q1. Is Class.newInstance() the modern approach?
No. It has been deprecated since Java 9.

### Q2. What is the modern reflection approach?
Obtain a `Constructor` and call `Constructor.newInstance()`.

### Q3. Why is reflection useful?
It enables runtime-driven discovery and creation of objects.

## 🔗 Related Notes

- [Overview →](01-object-creation-overview.md)
- [clone() & Shallow Copy →](03-clone-and-shallow-copy.md)
- [Deserialization →](05-deserialization-object-creation.md)
- [Comparison →](06-object-creation-comparison.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

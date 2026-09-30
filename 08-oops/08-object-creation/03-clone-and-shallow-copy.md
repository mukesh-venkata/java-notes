<a name="top"></a>

# 🧬 3. Object Creation Using clone()

> **Core idea:** `clone()` can create a new object by making a shallow copy of an existing object.

## 🧠 Basic Idea

Suppose:

```java
Student s1 = new Student();
Student s2 = s1.clone();
```

If cloning is supported, `s2` refers to a different outer object whose field values are copied from `s1`.

## 📌 Cloneable

The traditional Java cloning mechanism commonly uses the marker interface `Cloneable`.

```java
class Student implements Cloneable {
    int age;

    @Override
    public Student clone() throws CloneNotSupportedException {
        return (Student) super.clone();
    }
}
```

Usage:

```java
Student s1 = new Student();
Student s2 = s1.clone();
```

## 🔍 Shallow Copy

`Object.clone()` performs a field-for-field shallow copy.

```text
Original                         Copy

Student                          Student
 age = 27                        age = 27
 address ───────┐               address ───────┐
                ↓                               ↓
          Address object  ←──────────────  same Address object
```

For a shallow copy:

- Primitive field values are copied.
- Reference values are copied.
- Referenced objects are not automatically duplicated.

Therefore, mutable referenced objects can be shared.

## ⚠️ CloneNotSupportedException

If the object does not support the expected cloning mechanism, `Object.clone()` can throw `CloneNotSupportedException`.

Also remember:

> `Cloneable` is a marker interface; it does not declare the `clone()` method.

## 🔗 Connection to Object Class

`clone()` comes from `java.lang.Object`, so this topic builds directly on the Object Class topic.

## 🎯 Interview Questions

### Q1. What type of copy does Object.clone() provide?
A shallow copy.

### Q2. Does cloning automatically duplicate nested referenced objects?
No.

### Q3. What is Cloneable?
A marker interface indicating support for the Object cloning mechanism.

### Q4. Can clone() throw an exception?
Yes, `CloneNotSupportedException`.

## 🔗 Related Notes

- [Object Class →](../07-object-class/04-clone-and-shallow-copy.md)
- [Overview →](01-object-creation-overview.md)
- [Reflection →](04-reflection-object-creation.md)
- [Comparison →](06-object-creation-comparison.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

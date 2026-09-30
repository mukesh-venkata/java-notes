<a name="top"></a>

# 🧬 4. clone() & Shallow Copy

> **Core idea:** `clone()` can create a shallow copy of an object when the class supports cloning.

## 🧠 What Does clone() Do?

The `Object.clone()` method creates and returns a shallow copy of the object.

Its declaration is:

```java
protected Object clone() throws CloneNotSupportedException
```

A class commonly implements the marker interface `Cloneable` to indicate that cloning is supported.

## 📌 Example

```java
class Student implements Cloneable {
    int age;

    Student(int age) {
        this.age = age;
    }

    @Override
    public Student clone() throws CloneNotSupportedException {
        return (Student) super.clone();
    }
}
```

Usage:

```java
Student original = new Student(20);
Student copy = original.clone();
```

## 🔍 What Is a Shallow Copy?

A shallow copy creates a new outer object, but references inside the object are copied as references.

```text
Original object
    age ───────→ 20
    address ───→ Address object
                       ↑
                       │
Copy object
    age ───────→ 20
    address ───→ same Address object
```

So:

- The outer objects are different.
- Primitive fields are copied by value.
- Reference fields contain copied references.
- Referenced mutable objects may therefore be shared.

## 🧠 Shallow vs Deep Copy

```text
Shallow copy → new outer object + shared referenced objects
Deep copy    → new outer object + independently copied nested objects
```

## ⚠️ CloneNotSupportedException

If an object does not support the cloning mechanism expected by `Object.clone()`, calling the protected method can result in `CloneNotSupportedException`.

Also note that `Cloneable` is a marker interface: it declares no `clone()` method.

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What kind of copy does Object.clone() perform?</summary>
<br>

A shallow copy.

</details>

<details>
<summary>Q2. Does clone() automatically deep-copy referenced objects?</summary>
<br>

No. Referenced objects are not recursively cloned by the default Object.clone() behavior.

</details>

<details>
<summary>Q3. What is Cloneable?</summary>
<br>

A marker interface used to indicate support for the Object cloning mechanism.

</details>

<details>
<summary>Q4. Can clone() throw an exception?</summary>
<br>

Yes. CloneNotSupportedException can be thrown when the object's class does not support cloning through the mechanism.

</details>
## 🔗 Related Notes

- [Object Class Overview →](01-object-class-overview.md)
- [toString(), hashCode() & equals() →](02-tostring-hashcode-equals.md)
- [finalize() & Resource Cleanup →](05-finalize-and-resource-cleanup.md)
- [Quick Revision →](07-object-class-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

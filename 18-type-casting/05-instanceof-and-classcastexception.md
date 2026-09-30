<a name="top"></a>

# 🛡️ 5. instanceof & ClassCastException

## 🔎 instanceof

The `instanceof` operator checks whether an object reference is compatible with a specified reference type.

### Syntax

```java
objectReference instanceof ClassName
```

### Example

```java
Parent p = new Child();

if (p instanceof Child) {
    Child c = (Child) p;
    c.childMethod();
}
```

The check helps make a downcast safer.

## ❌ ClassCastException

A `ClassCastException` occurs when a reference is cast to an incompatible type at runtime.

Example:

```java
class Parent {
}

class Child extends Parent {
}

Parent p = new Parent();
Child c = (Child) p; // ClassCastException
```

The reference type `Parent` alone does not guarantee that the object is a `Child`.

## 🔄 Safe Downcasting Pattern

```java
Parent p = new Child();

if (p instanceof Child) {
    Child c = (Child) p;
    // use c
}
```

## 🧠 Runtime Object Matters

```text
Declared reference type
        ↓
      Parent
        │
        └──────→ actual object
                    ↓
                  Child
```

A cast is checked against the actual runtime object.

## 📌 instanceof and null

For a null reference:

```java
Parent p = null;

System.out.println(p instanceof Child); // false
```

The operator does not throw `NullPointerException` merely because the reference is null.

## 🎯 Interview Questions

### Q1. What does instanceof do?
It checks reference compatibility with a type.

### Q2. Why use instanceof before downcasting?
To check the runtime type before performing the cast.

### Q3. What happens when an incompatible cast is attempted?
A `ClassCastException` can occur at runtime.

### Q4. What does null instanceof SomeType return?
`false`.

## 🔗 Related Notes

- [Reference Upcasting & Downcasting →](04-reference-upcasting-and-downcasting.md)
- [Comparison →](06-type-casting-comparison.md)
- [Quick Revision →](07-type-casting-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

<a name="top"></a>

# 🧩 1. Object Class — Overview

> **Core idea:** `java.lang.Object` is the root class of the Java class hierarchy.

## 🧠 What Is Object?

`Object` is a class in the `java.lang` package.

For ordinary Java classes, `Object` is the ultimate superclass. A class can inherit from `Object` directly or indirectly.

```text
Object
   ↑
Parent
   ↑
Child
```

If you write:

```java
class Student {
}
```

the class still inherits the members of `Object` through implicit inheritance.

### Important Exception

Interfaces do not extend the `Object` class. However, objects of implementing classes still inherit `Object` methods through their class hierarchy.

## 📚 Common Object Methods

The commonly studied `Object` methods include:

| Method | Main purpose |
|---|---|
| `toString()` | String representation |
| `hashCode()` | Hash code |
| `equals(Object)` | Equality comparison |
| `getClass()` | Runtime class information |
| `clone()` | Shallow copy |
| `finalize()` | Legacy finalization mechanism |
| `wait()` | Make current thread wait |
| `wait(long)` | Timed wait |
| `wait(long, int)` | Timed wait with nanoseconds |
| `notify()` | Wake one waiting thread |
| `notifyAll()` | Wake all waiting threads |

## 🔗 How to Think About the API

```text
Object
  ├── Object identity & representation
  │     ├── toString()
  │     ├── equals()
  │     └── hashCode()
  │
  ├── Runtime type
  │     └── getClass()
  │
  ├── Copying
  │     └── clone()
  │
  ├── Legacy finalization
  │     └── finalize()
  │
  └── Thread coordination
        ├── wait()
        ├── notify()
        └── notifyAll()
```

## 🎯 Interview Questions

### Q1. Which class is the root of the Java class hierarchy?
`java.lang.Object` for classes.

### Q2. Is Object automatically available?
Yes. `java.lang` is automatically imported.

### Q3. Do interfaces extend Object?
No. Interfaces have their own inheritance model.

### Q4. Why is Object important?
It provides common behavior available through the class hierarchy, such as equality, hashing, string representation, runtime type information, and thread coordination methods.

## 🔗 Related Notes

- [toString(), hashCode() & equals() →](02-tostring-hashcode-equals.md)
- [getClass() →](03-getclass-and-runtime-type.md)
- [clone() & Shallow Copy →](04-clone-and-shallow-copy.md)
- [finalize() & Resource Cleanup →](05-finalize-and-resource-cleanup.md)
- [wait(), notify() & notifyAll() →](06-wait-notify-notifyall.md)
- [Quick Revision →](07-object-class-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

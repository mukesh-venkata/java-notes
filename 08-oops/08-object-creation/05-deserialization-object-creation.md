<a name="top"></a>

# 📦 5. Object Reconstruction Using Deserialization

> **Core idea:** Deserialization reconstructs an object from serialized data.

## 🧠 What Is Deserialization?

Deserialization is the process of reading serialized object data and reconstructing the object.

A typical Java example uses `ObjectInputStream`:

```java
try (ObjectInputStream ois =
         new ObjectInputStream(new FileInputStream("student.ser"))) {

    Student student = (Student) ois.readObject();
}
```

The class being serialized normally implements `Serializable`:

```java
class Student implements Serializable {
}
```

## 🔄 Flow

```text
Serialized data
      ↓
ObjectInputStream
      ↓
readObject()
      ↓
Reconstructed object
```

## ⚠️ Constructor Behavior

For normal Java deserialization of a serializable class, the serializable class's constructors are not invoked in the usual way to reconstruct its state.

The first non-serializable superclass's no-argument constructor is involved in the deserialization process.

This is different from normal `new` creation.

## 🧠 new vs Deserialization

| `new` | Deserialization |
|---|---|
| Constructor is invoked | Serializable class constructor is not invoked in the usual way |
| Starts normal initialization | Reconstructs serialized state |
| Object is created from class + constructor | Object is reconstructed from serialized data |

## 📌 Important Requirements

- The object graph being serialized must satisfy Java serialization rules.
- The class normally implements `Serializable`.
- `readObject()` can throw `ClassNotFoundException` and `IOException`.

## 🎯 Interview Questions

### Q1. What is deserialization?
Reconstructing an object from serialized data.

### Q2. Which class is commonly used to read serialized objects?
`ObjectInputStream`.

### Q3. Which method reads the object?
`readObject()`.

### Q4. Is the serializable class's constructor invoked normally?
No.

### Q5. What interface is commonly implemented for Java serialization?
`Serializable`.

## 🔗 Related Notes

- [Overview →](01-object-creation-overview.md)
- [Reflection →](04-reflection-object-creation.md)
- [Comparison →](06-object-creation-comparison.md)
- [Quick Revision →](07-object-creation-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

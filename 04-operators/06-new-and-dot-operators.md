<a name="top"></a>

# 🆕 Java `new` & Dot `.` — Object Creation and Member Access

> **Topic 11 • Java Fundamentals**

## 1️⃣ `new` Keyword

The `new` keyword is used to create a new object or array and obtain a reference to it.

### Example

```java
Student student = new Student();
```

Conceptually:

```text
new Student()
     ↓
object created
     ↓
reference returned
     ↓
student
```

> **Important:** `new` is a **keyword**, not a conventional operator like `+` or `==`. It is included in the handwritten mnemonic as the "New Operator" for easy memorization.

---

## 2️⃣ Dot `.` — Member Access

The dot is used to access members through a qualifying expression, such as an object reference.

```java
student.name;
student.display();
```

Here:

- `student` identifies the object/reference being used.
- `name` is a field.
- `display()` is a method.
- `.` provides member access.

> **Important:** The dot is commonly taught as the "dot operator," but technically it is better understood as a **member-access/separator token** in Java syntax.

---

## 🧠 Memory Trick

```text
new → create
.   → access
```

---

## 🎤 Interview Quick Check

**Q1. What does `new` do?**  
A: It creates a new object or array and returns a reference to it.

**Q2. What is `.` used for?**  
A: It provides member access, such as accessing an object's field or method.

**Q3. Is `new` technically an operator?**  
A: No. It is a Java keyword used in object/array creation expressions.

---

## 🔗 Navigation

⬅️ [Bitwise Operators](./05-bitwise-operators.md)

➡️ [Quick Revision](./07-operators-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

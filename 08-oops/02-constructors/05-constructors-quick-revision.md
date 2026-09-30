<a name="top"></a>

# ⚡ Constructors — Quick Revision

> **Topic 21 • 30-Second Revision**

## 🧠 Master Idea

```text
Constructor
    ↓
Initialize Object
    ↓
Types
    ↓
Overloading
    ↓
Chaining
```

## 1️⃣ Constructor

- Same name as class
- No return type
- Used during object construction
- Can initialize instance state
- Can be overloaded
- Not inherited

## 2️⃣ Types

| Type | Key Point |
|---|---|
| Compiler-provided default | Added when no constructor is declared |
| User-defined no-arg | Explicitly written with zero parameters |
| Parameterized | Accepts one or more parameters |

### ⚠️ Remember

**Default ≠ every no-argument constructor**

A user-defined no-arg constructor is not the compiler-provided default constructor.

## 3️⃣ Overloading

```text
Different NUMBER
      OR
Different TYPE
      OR
Different ORDER
          ↓
Constructor Overloading
```

Parameter names alone are not enough.

## 4️⃣ Chaining

```text
this()  → SAME CLASS
super() → PARENT CLASS
```

Both must be the first statement when explicitly used.

A constructor cannot explicitly use both in the same constructor.

## 5️⃣ Instantiation vs Initialization

**Instantiation → Create object**

**Initialization → Establish initial state**

## 🎯 Quick Example

```java
class Student {

    int age;

    Student() {
        this(18);
    }

    Student(int age) {
        this.age = age;
    }
}
```

Flow:

```text
new Student()
     ↓
this(18)
     ↓
Student(int)
     ↓
age initialized
```

## 🎤 Interview One-Liners

**Constructor:** Special class member used during object construction.

**Default constructor:** Compiler-provided constructor when no constructor declaration exists.

**Overloading:** Multiple constructors with different parameter lists.

**this():** Calls another constructor in the same class.

**super():** Calls a parent-class constructor.

🏠 [Java Notes Home](../../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

<a name="top"></a>

# 🔍 2. toString(), hashCode() & equals()

> **Core idea:** These three methods are central to object representation, equality, and hash-based collections.

## 1️⃣ toString()

`toString()` returns a String representation of an object.

Example:

```java
Student student = new Student();
System.out.println(student.toString());
```

The default implementation from `Object` produces a representation containing the runtime class name and a hexadecimal form of the object's hash code.

A class can override `toString()` to provide meaningful content:

```java
class Student {
    String name = "Alex";

    @Override
    public String toString() {
        return "Student{name='" + name + "'}";
    }
}
```

Then printing the object can display useful information instead of the default representation.

---

## 2️⃣ hashCode()

`hashCode()` returns an integer hash code for the object.

Important:

- A hash code is **not necessarily a memory address**.
- Different objects can have the same hash code.
- Equal objects must have the same hash code.

```java
int hash = student.hashCode();
```

### 🔗 Relationship with equals()

The important contract is:

```text
a.equals(b) == true
        ↓
a.hashCode() == b.hashCode()
```

The reverse is not guaranteed:

```text
same hash code
      ≠
definitely equal
```

This relationship matters especially for hash-based collections such as `HashMap` and `HashSet`.

---

## 3️⃣ equals(Object obj)

The `equals()` method is used to compare objects for equality.

The default implementation inherited from `Object` behaves like an identity comparison: two references are equal only when they refer to the same object.

```java
Student s1 = new Student();
Student s2 = new Student();

System.out.println(s1.equals(s2)); // false
System.out.println(s1.equals(s1)); // true
```

A class can override `equals()` to define logical equality.

### Example

```java
class Student {
    String name;

    Student(String name) {
        this.name = name;
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (!(obj instanceof Student other)) return false;
        return java.util.Objects.equals(name, other.name);
    }

    @Override
    public int hashCode() {
        return java.util.Objects.hash(name);
    }
}
```

Now two different Student objects with the same name can be considered logically equal.

## ⚠️ equals() vs ==

```text
==       → reference identity for objects
equals() → equality defined by the class
```

For a class that does not override `equals()`, the inherited Object behavior is identity-based.

## 🧠 Memory Trick

> **toString → describe**  
> **equals → compare**  
> **hashCode → hash**

## 🎯 Interview Questions

### Q1. What does toString() return?
A String representation of the object.

### Q2. Is hashCode() a memory address?
No. It returns an integer hash code.

### Q3. If equals() returns true, what must be true?
The two objects must have the same hash code.

### Q4. Does the default Object.equals() perform logical field comparison?
No. It is identity-based.

### Q5. Why override equals() and hashCode() together?
Because the hashCode contract requires equal objects to have equal hash codes.

## 🔗 Related Notes

- [Object Class Overview →](01-object-class-overview.md)
- [getClass() →](03-getclass-and-runtime-type.md)
- [clone() & Shallow Copy →](04-clone-and-shallow-copy.md)
- [Quick Revision →](07-object-class-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

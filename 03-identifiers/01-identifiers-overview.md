<a name="top"></a>

# 🔤 Java Identifiers — Overview

> **Topic 10 • Java Fundamentals**

An **identifier** is the name given to a program element so that it can be referred to in Java code.

---

## 🎯 What Is an Identifier?

An identifier is a programmer-defined name for elements such as:

- Class
- Interface
- Method
- Variable
- Package

### Example

```java
class Student {

    String studentName;

    void calculateSalary() {
    }
}
```

Here:

| Identifier | Represents |
|---|---|
| `Student` | Class |
| `studentName` | Variable |
| `calculateSalary` | Method |

---

## 🔠 Java Identifiers Are Case-Sensitive

Java treats uppercase and lowercase letters as different characters.

```text
mukeshPilla ≠ MukeshPilla
```

So these can represent different identifiers:

```java
int studentCount;
int StudentCount;
```

> **Remember:** Java is **case-sensitive**.

---

## 📏 Basic Identifier Rules

A valid identifier:

1. Can contain letters, digits, underscore (`_`) and dollar sign (`$`).
2. Must not start with a digit.
3. Must not contain spaces.
4. Must not be a Java keyword.
5. Is case-sensitive.
6. Can be of any length, subject to compiler/tooling limits.

### Examples

| Valid | Invalid | Reason |
|---|---|---|
| `studentName` | `2students` | Starts with a digit |
| `_count` | `student name` | Contains a space |
| `$value` | `class` | Keyword |
| `student2` | `total-marks` | `-` is not allowed |

> **Good practice:** Although `_` and `$` can be legal in some positions, normal application code should prefer descriptive names using standard Java naming conventions.

---

## 🚫 Keywords Cannot Be Identifiers

Java keywords have predefined meaning and cannot be used as programmer-defined identifiers.

Examples:

```text
class
int
public
static
if
return
new
```

❌ Invalid:

```java
int class = 10;
```

✅ Valid:

```java
int classCount = 10;
```

---

## 🧠 Memory Trick

### **Identifier = "Name of a Program Element"**

Think:

```text
Class     → Name
Method    → Name
Variable  → Name
Interface → Name
Package   → Name
```

---

## 🎤 Interview Quick Check

**Q1. What is an identifier in Java?**  
A: A name given to a program element such as a class, method, variable, interface or package.

**Q2. Are Java identifiers case-sensitive?**  
A: Yes.

**Q3. Can a Java keyword be used as an identifier?**  
A: No.

**Q4. Can an identifier start with a digit?**  
A: No.

---

## 🔗 Next

➡️ [Java Naming Conventions](./02-java-naming-conventions.md)

➡️ [Quick Revision](./03-identifiers-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

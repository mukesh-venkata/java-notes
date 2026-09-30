<a name="top"></a>

# ⚡ Java Identifiers — Quick Revision

> **Topic 10 • 30-Second Revision**

## 🔤 Identifier

An **identifier** is the name given to a Java program element.

```text
Class • Interface • Method • Variable • Package
```

---

## 📌 Core Rules

- Java identifiers are **case-sensitive**.
- An identifier cannot start with a digit.
- Spaces are not allowed.
- Java keywords cannot be used as identifiers.
- Letters, digits, `_` and `$` are permitted according to Java's identifier rules.

### Example

```text
mukeshPilla ≠ MukeshPilla
```

---

## 🏷️ Naming Conventions

| Element | Convention | Example |
|---|---|---|
| Class / Interface | PascalCase | `PaymentService` |
| Method / Variable | camelCase | `studentName` |
| Constant | UPPER_SNAKE_CASE | `MAX_VALUE` |
| Package | lowercase | `com.company.project` |

---

## 🧠 Memory Trick

### **P → C → U → L**

```text
PascalCase       → Class / Interface
camelCase        → Method / Variable
UPPER_SNAKE_CASE → Constant
lowercase        → Package
```

---

## 🔎 Example

```java
package com.company.project;

class PaymentService {

    static final int MAX_VALUE = 100;

    String studentName;

    void calculateSalary() {
    }
}
```

| Name | Type | Convention |
|---|---|---|
| `com.company.project` | Package | lowercase |
| `PaymentService` | Class | PascalCase |
| `MAX_VALUE` | Constant | UPPER_SNAKE_CASE |
| `studentName` | Variable | camelCase |
| `calculateSalary()` | Method | camelCase |

---

## 🎤 Interview One-Liners

**Identifier?** → Name given to a program element.

**Case-sensitive?** → Yes.

**Keyword as identifier?** → Not allowed.

**Class convention?** → PascalCase.

**Variable/method convention?** → camelCase.

**Constant convention?** → UPPER_SNAKE_CASE.

**Package convention?** → lowercase.

---

## 🔗 Navigation

⬅️ [Identifiers Overview](./01-identifiers-overview.md)

⬅️ [Naming Conventions](./02-java-naming-conventions.md)

🏠 [Java Notes Home](../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

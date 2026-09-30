# ✍️ Java Naming Conventions

> **Topic 10 • Java Fundamentals**

Naming conventions are standard practices used to make Java code **consistent, readable and easier to maintain**.

---

## 🧩 The 4 Main Conventions

| Program Element | Convention | Example |
|---|---|---|
| Class / Interface | **PascalCase** | `PaymentService` |
| Method / Variable | **camelCase** | `studentName` |
| Constant | **UPPER_SNAKE_CASE** | `MAX_VALUE` |
| Package | **lowercase** | `com.company.project` |

---

## 1️⃣ Class / Interface → PascalCase

Start each word with an uppercase letter.

### Examples

```text
MukeshPilla
Student
PaymentService
StudentDetails
```

### Example

```java
class PaymentService {
}

interface PaymentProcessor {
}
```

---

## 2️⃣ Methods / Variables → camelCase

Start with a lowercase letter and capitalize the first letter of each following word.

### Variables

```text
mukeshPilla
studentName
totalAmount
employeeCount
```

### Methods

```text
calculateSalary()
getStudentDetails()
saveEmployee()
```

### Example

```java
String studentName;
int employeeCount;

void calculateSalary() {
}
```

---

## 3️⃣ Constants → UPPER_SNAKE_CASE

Constants are commonly written using uppercase letters, with words separated by underscores.

### Examples

```text
MUKESH_PILLA
MAX_VALUE
MIN_AMOUNT
MAX_RETRY_COUNT
```

### Example

```java
static final int MAX_VALUE = 100;
static final int MIN_AMOUNT = 10;
```

> **Convention:** Constants are typically declared with `static final`.

---

## 4️⃣ Packages → lowercase

Package names are conventionally written in lowercase.

For organization and uniqueness, reverse-domain naming is commonly used.

### Examples

```text
mukesh.pilla
com.company.project
com.example.payment
```

### Example

```java
package com.company.project;
```

---

## 🗺️ Naming Map

```text
                  Java Naming
                       │
        ┌──────────────┼──────────────┐
        │              │              │
     Type names     Members       Constants
        │              │              │
    PascalCase      camelCase    UPPER_SNAKE_CASE
        │              │              │
 PaymentService   studentName    MAX_VALUE

                  Package
                     │
                  lowercase
                     │
              com.company.project
```

---

## 💡 Why Naming Conventions Matter

Good names help developers:

- Understand code faster
- Identify the purpose of an element
- Maintain large codebases
- Follow team standards
- Review code more easily

> **Simple rule:** A good identifier should make the code easier to understand without needing extra explanation.

---

## 🎤 Interview Quick Check

**Q1. What naming convention is used for Java classes?**  
A: PascalCase.

**Q2. What naming convention is commonly used for variables and methods?**  
A: camelCase.

**Q3. How are constants conventionally named?**  
A: UPPER_SNAKE_CASE.

**Q4. How are package names conventionally written?**  
A: Lowercase, commonly following reverse-domain naming.

---

## 🧠 10-Second Memory Trick

**P → C → U → L**

```text
P → PascalCase       → Class / Interface
C → camelCase        → Method / Variable
U → UPPER_SNAKE_CASE → Constant
L → lowercase        → Package
```

---

## 🔗 Navigation

⬅️ [Identifiers Overview](./01-identifiers-overview.md)

➡️ [Quick Revision](./03-identifiers-quick-revision.md)

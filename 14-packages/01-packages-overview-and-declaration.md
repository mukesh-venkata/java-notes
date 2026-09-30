<a name="top"></a>

# 📦 1. Packages — Overview & Declaration

> **Core idea:** A package groups related Java types and helps organize an application.

---

## 🧠 What is a Package?

A **package** is a namespace used to group related Java types such as:

- Classes
- Interfaces
- Exceptions
- Enums
- Other types

For example, a project might organize incident-management code under:

`com.example.application`

Think of a package as a **folder-like namespace for Java types**.

---

## Why Do We Use Packages?

Packages help us:

- 📁 Organize related code
- 🔍 Find classes more easily
- 🏷️ Avoid naming conflicts
- 🔐 Control access using package-related access rules
- 🏗️ Structure large applications

### Simple View

`text
Application
   │
   ├── com.example.application
   ├── com.example.admin
   └── com.example.user
`

---

## 1️⃣ Package Declaration

A Java source file can declare its package using the `package` keyword.

### Syntax

`java
package packageName;
`

### Example

`java
package com.example.application;
`

This tells Java that the types declared in that source file belong to that package.

---

## 📌 Where Does the Package Declaration Go?

The package declaration appears at the beginning of the Java source file, after any permitted comments or package annotations.

### Example

`java
// This is a comment

package com.example.application;

public class IncidentService {
}
`

The package declaration comes before normal type declarations such as classes and interfaces.

---

## 2️⃣ Only One Package Declaration

A Java source file can have **only one package declaration**.

### Correct

`java
package com.example.application;

public class IncidentService {
}
`

### Incorrect

`java
package com.example.application;
package com.example.admin;   // ❌ Not allowed
`

One source file belongs to one declared package.

---

## 🔗 Package Declaration vs Import

These keywords have different jobs:

| Keyword | Purpose |
|---|---|
| `package` | Declares which package the current source file belongs to |
| `import` | Makes types from another package available by simple name |

Example:

`java
package com.example.application;

import java.util.List;
`

Here:

- `package` identifies the current package.
- `import` brings `List` into simple-name scope.

---

## 🎯 Interview Questions

### Q1. What is a package in Java?
A namespace used to group related Java types and organize applications.

### Q2. How many package declarations can a source file contain?
Only **one** package declaration.

### Q3. Where is the package declaration placed?
At the beginning of the source file, after permitted comments and package annotations.

### Q4. What is the difference between package and import?
`package` declares the current package; `import` allows types from another package to be referred to by simple name.

---

## ⚡ Quick Revision

`text
package
   ↓
declares the current package
   ↓
groups related Java types
   ↓
only one package declaration per source file
`

---

## 🔗 Related Notes

- [java.lang Package →](02-java-lang-package.md)
- [Import & Wildcard →](03-import-statement-and-wildcard.md)
- [Package Naming & Structure →](04-package-naming-and-structure.md)
- [Packages Quick Revision →](05-packages-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

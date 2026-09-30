<a name="top"></a>

# 🏗️ 4. Package Naming & Structure

> **Core idea:** Meaningful package names make large Java applications easier to organize and understand.

---

## 🏷️ Package Naming Convention

Java package names are conventionally written in **lowercase**.

A common approach is to start with the organization's **reversed domain name**.

### Example

For an organization using the domain `example.com`, a package might begin with:

`text
com.example...
`

A project-specific package could be:

`java
com.example.application
`

---

## Why Reverse the Domain?

The reversed-domain convention helps organizations create package names that are less likely to collide with package names created by other organizations.

Think:

`text
Original domain
      ↓
    example.com
      ↓ reverse domain
    com.example
      ↓
 application/module
    com.example
      ↓
 feature/module
    com.example.application
`

---

## 📦 Breaking Down a Package Name

Example:

`text
com.example.application
`

| Part | Meaning |
|---|---|
| `com` | Domain-level prefix |
| `example` | Organization/company |
| `ghd` | Application/project |
| `incidentmanagement` | Module or feature area |

So:

**com → example → application**

---

## 🏢 Enterprise Package Structure

A large application may organize code into meaningful modules.

For example:

`text
com
└── example
    └── ghd
        ├── incidentmanagement
        ├── admin
        └── user
`

Inside a module, packages can be organized further by responsibility.

For example:

`text
com.example.application
├── controller
├── service
├── repository
├── dto
└── entity
`

This type of organization is common in layered Java applications.

---

## 📌 Package Names Are Not Necessarily the Same as Folders

In normal Java project layouts, package names correspond to directory paths.

For:

`java
package com.example.application;
`

the source path is typically organized like:

`text
src/
└── ...
    └── com/
        └── example/
            └── ghd/
                └── incidentmanagement/
                    └── IncidentService.java
`

Build tools and IDEs manage these conventions for us, but the package declaration remains the Java namespace declaration.

---

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What naming convention is commonly used for Java packages?</summary>
<br>

Lowercase names, commonly starting with the organization's reversed domain name.

</details>

<details>
<summary>Q2. Why use a reversed domain name?</summary>
<br>

To reduce the chance of package-name collisions between organizations.

</details>

<details>
<summary>Q3. What does <code>com.example.application</code> represent?</summary>
<br>

A hierarchical package namespace representing an organization, application, and module or feature area.

</details>

<details>
<summary>Q4. Can package names contain uppercase letters?</summary>
<br>

Java permits valid identifiers according to its lexical rules, but package names are conventionally written in lowercase.

</details>
## ⚡ Quick Revision

> **Package naming → lowercase + reversed domain + meaningful modules**

`text
com → tcs → ghd → incidentmanagement
│      │      │        │
domain company  app    module
`

---

## 🔗 Related Notes

- [Packages Overview →](01-packages-overview-and-declaration.md)
- [java.lang →](02-java-lang-package.md)
- [Import & Wildcard →](03-import-statement-and-wildcard.md)
- [Packages Quick Revision →](05-packages-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

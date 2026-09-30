<a name="top"></a>

# 🏗️ 4. Package Naming & Structure

> **Core idea:** Meaningful package names make large Java applications easier to organize and understand.

---

## 🏷️ Package Naming Convention

Java package names are conventionally written in **lowercase**.

A common approach is to start with the organization's **reversed domain name**.

### Example

For an organization using the domain `tcs.com`, a package might begin with:

`text
com.tcs...
`

A project-specific package could be:

`java
com.tcs.ghd.incidentmanagement
`

---

## Why Reverse the Domain?

The reversed-domain convention helps organizations create package names that are less likely to collide with package names created by other organizations.

Think:

`text
Original domain
      ↓
    tcs.com
      ↓ reverse domain
    com.tcs
      ↓
 application/module
    com.tcs.ghd
      ↓
 feature/module
    com.tcs.ghd.incidentmanagement
`

---

## 📦 Breaking Down a Package Name

Example:

`text
com.tcs.ghd.incidentmanagement
`

| Part | Meaning |
|---|---|
| `com` | Domain-level prefix |
| `tcs` | Organization/company |
| `ghd` | Application/project |
| `incidentmanagement` | Module or feature area |

So:

**com → tcs → ghd → incidentmanagement**

---

## 🏢 Enterprise Package Structure

A large application may organize code into meaningful modules.

For example:

`text
com
└── tcs
    └── ghd
        ├── incidentmanagement
        ├── admin
        └── user
`

Inside a module, packages can be organized further by responsibility.

For example:

`text
com.tcs.ghd.incidentmanagement
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
package com.tcs.ghd.incidentmanagement;
`

the source path is typically organized like:

`text
src/
└── ...
    └── com/
        └── tcs/
            └── ghd/
                └── incidentmanagement/
                    └── IncidentService.java
`

Build tools and IDEs manage these conventions for us, but the package declaration remains the Java namespace declaration.

---

## 🎯 Interview Questions

### Q1. What naming convention is commonly used for Java packages?
Lowercase names, commonly starting with the organization's reversed domain name.

### Q2. Why use a reversed domain name?
To reduce the chance of package-name collisions between organizations.

### Q3. What does `com.tcs.ghd.incidentmanagement` represent?
A hierarchical package namespace representing an organization, application, and module/feature area.

### Q4. Can package names contain uppercase letters?
Java permits identifiers according to its naming rules, but package names are conventionally written in lowercase.

---

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

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

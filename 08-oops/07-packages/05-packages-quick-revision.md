<a name="top"></a>

# ⚡ 5. Packages — Quick Revision

> **30-second revision:** Package = organize related Java types; `import` = use accessible types from another package by simple name.

---

## 🧠 Core Rules

| Concept | Key Rule |
|---|---|
| Package | Groups related Java types |
| `package` declaration | Declares the current package |
| Package declarations | Only one per source file |
| `java.lang` | Automatically imported |
| `import` | Makes imported types available by simple name |
| `import package.*` | Covers types directly in that package |
| Wildcard `*` | Does **not** import subpackages |
| Package naming | Commonly lowercase + reversed domain |

---

## 1️⃣ Package Declaration

`java
package com.tcs.ghd.incidentmanagement;
`

Remember:

> **One source file → one package declaration.**

---

## 2️⃣ java.lang

Automatically available:

- `String`
- `System`
- `Math`
- `Object`
- `Integer`

Normally no need for:

`java
import java.lang.String;
`

---

## 3️⃣ Wildcard Import

`java
import java.io.*;
`

Means:

> Make accessible types directly in `java.io` available by simple name.

It does **not** mean:

> “Import all subpackages.”

---

## 4️⃣ Package Structure

`text
com
 ↓
tcs
 ↓
ghd
 ↓
incidentmanagement
`

A common enterprise structure can continue into responsibility-based packages:

`text
controller
service
repository
dto
entity
`

---

## 🔥 Package vs Import

| `package` | `import` |
|---|---|
| Declares current package | Refers to types from another package |
| Usually at beginning of source file | Appears after package declaration |
| One package declaration | Multiple imports are allowed |
| Defines namespace | Enables simple-name usage |

---

## 🎯 Interview Questions

1. **What is a package?**  
   A namespace used to group related Java types and organize code.

2. **How many package declarations can one source file have?**  
   One.

3. **Which package is automatically imported?**  
   `java.lang`.

4. **Does `import java.util.*` import `java.util.concurrent`?**  
   No. Subpackages are not imported by a wildcard.

5. **Can we use a class without importing it?**  
   Yes, if it is in the same package, in `java.lang`, or referenced by its fully qualified name (subject to accessibility).

6. **What is a common package naming convention?**  
   Lowercase names using a reversed domain prefix, followed by meaningful application/module names.

---

## 🧠 Memory Trick

> **Package = where the class belongs**  
> **Import = how another type is referred to**

---

## ⚡ 30-Second Recall

`text
PACKAGE
  ↓
organize + namespace

java.lang
  ↓
automatic

IMPORT
  ↓
use accessible types by simple name

*
  ↓
direct package types only
  ↓
❌ no subpackages
`

---

## 🔗 Related Notes

- [Packages Overview →](01-packages-overview-and-declaration.md)
- [java.lang Package →](02-java-lang-package.md)
- [Import & Wildcard →](03-import-statement-and-wildcard.md)
- [Package Naming & Structure →](04-package-naming-and-structure.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

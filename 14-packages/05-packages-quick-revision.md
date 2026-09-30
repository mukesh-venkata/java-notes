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
package com.example.application;
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
example
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

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What is a package?</summary>
<br>

A namespace used to group related Java types and organize code.

</details>

<details>
<summary>2. How many package declarations can one source file have?</summary>
<br>

One package declaration can appear in a Java source file.

</details>

<details>
<summary>3. Which package is automatically imported?</summary>
<br>

java.lang.

</details>

<details>
<summary>4. Does import java.util.* import java.util.concurrent?</summary>
<br>

No. A wildcard import covers types directly in the specified package; it does not import subpackages.

</details>

<details>
<summary>5. Can we use a class without importing it?</summary>
<br>

Yes, if it is in the same package, in java.lang, or referenced by its fully qualified name, subject to accessibility.

</details>

<details>
<summary>6. What is a common package naming convention?</summary>
<br>

Use lowercase names, commonly beginning with a reversed domain name, followed by meaningful application or module names.

</details>
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

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

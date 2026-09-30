<a name="top"></a>

# 📥 3. import Statement & Wildcard

> **Core idea:** `import` lets you use accessible types from another package by their simple names.

---

## 🧠 Why Do We Use `import`?

Suppose we want to use `File` from `java.io`.

Without an import, we can use its fully qualified name:

`java
java.io.File file = new java.io.File("data.txt");
`

With an import:

`java
import java.io.File;

File file = new File("data.txt");
`

The import makes the simple name `File` available in the source file.

---

## 1️⃣ Importing One Type

### Syntax

`java
import packageName.TypeName;
`

### Example

`java
import java.io.File;
`

Now `File` can be referred to by its simple name.

---

## 2️⃣ Importing Multiple Types

You can import individual types separately.

`java
import java.io.File;
import java.io.FileReader;
import java.io.BufferedReader;
import java.io.IOException;
`

These types are all directly inside the `java.io` package.

---

## 3️⃣ Importing Using `*`

Java also supports a wildcard import:

`java
import java.io.*;
`

This makes accessible types declared directly in `java.io` available by simple name.

Examples include:

- `File`
- `FileReader`
- `BufferedReader`
- `IOException`

---

## ⚠️ `*` Does NOT Import Subpackages

This is a very important rule.

`java
import java.io.*;
`

does **not** import types from a subpackage such as:

`java
java.io.somepackage.SomeClass
`

Think:

`text
java.io.*
    │
    ├── File              ✅
    ├── FileReader        ✅
    └── somepackage       ❌ not imported
             │
             └── SomeClass
`

A wildcard import covers the specified package's types; it does not recursively include subpackages.

---

## 4️⃣ Import Does Not Mean “Import Everything”

The wildcard does not mean every type under the entire package hierarchy.

For:

`java
import java.io.*;
`

the `*` applies to types directly in `java.io`, not nested packages.

---

## 🔍 Import vs Fully Qualified Name

| Approach | Example |
|---|---|
| Import | `File` |
| Fully qualified name | `java.io.File` |

Both can refer to the same type.

### Example

`java
import java.io.File;

class Demo {
    File file;
}
`

Without import:

`java
class Demo {
    java.io.File file;
}
`

---

## 🎯 Interview Questions

### Q1. What does `import` do?
It allows an accessible type from another package to be referred to by its simple name.

### Q2. What does `import java.io.*` import?
It imports accessible types directly declared in `java.io` for simple-name use.

### Q3. Does `import java.io.*` import subpackages?
**No.**

### Q4. Can we use a fully qualified class name without import?
**Yes.**

---

## ⚡ Quick Revision

`text
import java.io.*;
       │
       ↓
types directly in java.io
       │
       ├── File          ✅
       ├── FileReader    ✅
       └── subpackages   ❌
`

---

## 🔗 Related Notes

- [Packages Overview →](01-packages-overview-and-declaration.md)
- [java.lang →](02-java-lang-package.md)
- [Package Naming & Structure →](04-package-naming-and-structure.md)
- [Packages Quick Revision →](05-packages-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

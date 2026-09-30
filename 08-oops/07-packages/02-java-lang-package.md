<a name="top"></a>

# ☕ 2. java.lang Package

> **Core idea:** `java.lang` is automatically imported into every Java source file.

---

## 🧠 What is `java.lang`?

`java.lang` is a standard Java package containing fundamental classes used throughout Java programs.

Examples include:

- `String`
- `System`
- `Math`
- `Object`
- `Integer`

---

## 🚀 Automatic Import

Java automatically makes the types in `java.lang` available.

That is why we can write:

`java
String name = "Mukesh";
System.out.println(name);

Integer number = 10;
`

without writing:

`java
import java.lang.String;
import java.lang.System;
import java.lang.Integer;
`

---

## What Does “Automatically Imported” Mean?

Conceptually:

`text
Every Java source file
        │
        ↓
java.lang types available
        │
        ├── String
        ├── System
        ├── Object
        ├── Math
        └── Integer
`

You normally do not need to write explicit imports for these types.

---

## 📌 Examples

### String

`java
String message = "Hello Java";
`

### System

`java
System.out.println("Hello");
`

### Math

`java
double result = Math.sqrt(25);
`

### Object

Every class ultimately has `Object` as its root superclass, directly or indirectly.

`java
Object value = "Java";
`

---

## Do We Need This?

Normally, no:

`java
import java.lang.String;
`

Because `java.lang` is automatically imported.

Explicitly importing a `java.lang` type is generally unnecessary.

---

## ⚠️ Important Distinction

Only `java.lang` is automatically imported.

Other packages are **not** automatically imported just because they are part of the Java platform.

For example, for `ArrayList` we normally write:

`java
import java.util.ArrayList;
`

---

## 🎯 Interview Questions

### Q1. Which package is automatically imported in every Java program?
`java.lang`.

### Q2. Name some classes from `java.lang`.
`String`, `System`, `Math`, `Object`, and wrapper classes such as `Integer`.

### Q3. Do we need to explicitly import `java.lang.String`?
No. `java.lang` is automatically imported.

### Q4. Is `java.util` automatically imported?
No.

---

## ⚡ Quick Revision

> **java.lang → automatically available**

`text
java.lang
   ↓
automatic import
   ↓
String, System, Math, Object, Integer...
`

---

## 🔗 Related Notes

- [Packages Overview →](01-packages-overview-and-declaration.md)
- [Import & Wildcard →](03-import-statement-and-wildcard.md)
- [Package Naming & Structure →](04-package-naming-and-structure.md)
- [Packages Quick Revision →](05-packages-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

<a name="top"></a>

# 🧰 4. Commonly Used Java Standard Packages

> **Core idea:** Different standard packages provide APIs for different programming needs.

## 📦 Package Overview

| Package | Purpose | Example types |
|---|---|---|
| `java.lang` | Core language functionality | `String`, `System`, `Math`, `Object` |
| `java.util` | Collections and utilities | `Scanner`, `ArrayList`, `HashMap` |
| `java.io` | Traditional input/output | `File`, `FileReader`, `FileWriter` |
| `java.time` | Date and time API | `LocalDate`, `LocalTime`, `LocalDateTime` |
| `java.net` | Networking APIs | `URI`, `URL`, `Socket` |

## 🔹 java.util

Used for collections and many utility classes.

Examples:

~~~java
import java.util.ArrayList;
import java.util.HashMap;
import java.util.Scanner;
~~~

Common types include:

- `ArrayList`
- `HashMap`
- `Scanner`

## 🔹 java.io

Provides APIs for traditional input/output and file-related operations.

Examples:

- `File`
- `FileReader`
- `FileWriter`

## 🔹 java.time

Provides the modern date and time API.

Examples:

- `LocalDate`
- `LocalTime`
- `LocalDateTime`

## 🔹 java.net

Provides networking-related APIs.

Examples include:

- `URI`
- `URL`
- `Socket`

## ⚠️ Package Imports

Unlike `java.lang`, these packages are not automatically imported.

For example:

~~~java
import java.util.ArrayList;
~~~

is normally needed before directly using `ArrayList` by its simple name.

## 🎯 Interview Questions

### Q1. Which package contains ArrayList?
`java.util`.

### Q2. Which package provides LocalDate?
`java.time`.

### Q3. Which package is commonly used for traditional file I/O?
`java.io`.

### Q4. Is java.util automatically imported?
No.

## 🔗 Related Notes

- [Library Overview →](01-java-standard-library-overview.md)
- [java.lang & Automatic Import →](02-java-lang-and-automatic-import.md)
- [String & length() →](03-string-and-length.md)
- [Quick Revision →](05-java-standard-library-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

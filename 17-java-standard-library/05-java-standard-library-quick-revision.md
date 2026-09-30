<a name="top"></a>

# ⚡ 5. Java Standard Library — Quick Revision

> **30-second revision:** The Java Standard Library provides predefined reusable APIs through packages, classes, interfaces, and methods.

## 🧠 Core Concepts

| Concept | Remember |
|---|---|
| Java Standard Library / API | Predefined reusable functionality |
| `java.lang` | Automatically imported |
| `String` | `java.lang.String` |
| `String.length()` | Number of characters |
| `java.util` | Collections & utilities |
| `java.io` | Traditional I/O |
| `java.time` | Date & time |
| `java.net` | Networking |

## 🔄 Package → Class → Method

~~~text
java.lang
    ↓
String
    ↓
length()
~~~

## 📌 Important Rules

- `java.lang` is automatically available.
- `java.util`, `java.io`, `java.time`, and `java.net` are not automatically imported.
- `String.length()` is a method.
- Array `length` is a field.
- Command-line examples and other API usage should use the appropriate package/import.

## 🧠 Memory Trick

> **lang → language core**  
> **util → utilities**  
> **io → input/output**  
> **time → date/time**  
> **net → networking**

## 🎯 Interview Questions

1. What is the Java Standard Library?
2. Which package is automatically imported? **java.lang**
3. Where is String located? **java.lang.String**
4. What does String.length() return? **Number of characters**
5. Where is ArrayList located? **java.util**
6. Where is LocalDate located? **java.time**
7. Is java.io automatically imported? **No**
8. What is the difference between String.length() and array.length? **String uses a method; arrays use a field.**

## 🔗 Related Notes

- [Library Overview →](01-java-standard-library-overview.md)
- [java.lang & Automatic Import →](02-java-lang-and-automatic-import.md)
- [String & length() →](03-string-and-length.md)
- [Commonly Used Packages →](04-commonly-used-java-packages.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

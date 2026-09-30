<a name="top"></a>

# 🔤 3. String & length()

> **Core idea:** `String` is a class in `java.lang`, and `length()` returns the number of characters in a string.

## 🧩 String

`String` belongs to the `java.lang` package.

Example:

~~~java
String name = "Java";
~~~

No explicit `java.lang.String` import is normally required.

## 📏 length()

The `length()` method returns the number of characters in a `String`.

Example:

~~~java
String name = "Java";

System.out.println(name.length());
~~~

Output:

~~~text
4
~~~

### Another Example

~~~java
String name = "Hello";

System.out.println(name.length());
~~~

Output:

~~~text
5
~~~

## 🔍 Package → Class → Method

~~~text
java.lang  →  String  →  length()
 package      class       method
~~~

This is a useful way to understand where a Java API method comes from.

## ⚠️ Important

For a `String`, `length()` is a **method**, so parentheses are used:

~~~java
name.length()
~~~

This differs from an array, where `length` is a field:

~~~java
int[] numbers = {10, 20, 30};

System.out.println(numbers.length);
~~~

## 🎯 Interview Questions

### Q1. Which package contains String?
`java.lang`.

### Q2. What does String.length() return?
The number of characters in the string.

### Q3. Is length() a method or a field?
For `String`, `length()` is a method.

### Q4. Is array length accessed the same way?
No. Arrays use the `length` field, without parentheses.

## 🔗 Related Notes

- [Library Overview →](01-java-standard-library-overview.md)
- [java.lang & Automatic Import →](02-java-lang-and-automatic-import.md)
- [Commonly Used Packages →](04-commonly-used-java-packages.md)
- [Quick Revision →](05-java-standard-library-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

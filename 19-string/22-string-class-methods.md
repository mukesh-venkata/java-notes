<a name="top"></a>

# 🔤 22. String Class Methods

> **30-second revision:** `String` provides many methods for character access, length, modification, searching, extraction, conversion, checking, joining, comparison, and String Pool operations.

## 📌 Overview

`String` provides many useful methods to perform operations on Strings.

Because `String` is **immutable**, methods that appear to modify a String return a new String instead of changing the original String.

```java
String s = "Java";
String upper = s.toUpperCase();

System.out.println(s);
System.out.println(upper);
```

### Output

```text
Java
JAVA
```

The original `s` remains unchanged.

---

## 1️⃣ `charAt(int index)`

Returns the character at the specified index.

```java
String s = "Java";
System.out.println(s.charAt(0));
```

### Output

```text
J
```

> Indexing is zero-based.

---

## 2️⃣ `length()`

Returns the number of characters in the String.

```java
String s = "Java";
System.out.println(s.length());
```

### Output

```text
4
```

---

## 3️⃣ `concat(String str)`

Concatenates the specified String to the end of the current String and returns a new String.

```java
String s1 = "Java";
String s2 = "Programming";

System.out.println(s2.concat(s1));
```

### Output

```text
ProgrammingJava
```

> `concat()` does not modify the original Strings.

---

## 4️⃣ `replace()`

Replaces characters or matching character sequences and returns a new String.

### Character replacement

```java
String s = "Java";
System.out.println(s.replace('a', 'b'));
```

### Output

```text
Jbvb
```

### Common forms

```java
s.replace('a', 'b');       // char → char
s.replace("Java", "Python"); // String → String
```

---

## 5️⃣ `toUpperCase()`

Converts the String to uppercase and returns a new String.

```java
String s = "Java";
System.out.println(s.toUpperCase());
```

### Output

```text
JAVA
```

---

## 6️⃣ `toLowerCase()`

Converts the String to lowercase and returns a new String.

```java
String s = "JAVA";
System.out.println(s.toLowerCase());
```

### Output

```text
java
```

---

## 7️⃣ `indexOf()`

Returns the index of the **first occurrence** of the specified character or substring.

```java
String s = "banana";
System.out.println(s.indexOf('a'));
```

### Output

```text
1
```

> Returns `-1` when the search value is not found.

---

## 8️⃣ `lastIndexOf()`

Returns the index of the **last occurrence** of the specified character or substring.

```java
String s = "banana";
System.out.println(s.lastIndexOf('a'));
```

### Output

```text
5
```

> Returns `-1` when the search value is not found.

---

## 9️⃣ `substring()`

Extracts a portion of a String.

### `substring(int beginIndex)`

Returns the substring from `beginIndex` to the end.

### `substring(int beginIndex, int endIndex)`

Returns the substring from `beginIndex` inclusive to `endIndex` exclusive.

```java
String s = "Java";
System.out.println(s.substring(1, 3));
```

### Output

```text
av
```

---

## 🔟 `split()`

Splits a String using a regular-expression delimiter and returns a `String[]`.

```java
String s = "a@b@c";
String[] arr = s.split("@");

System.out.println(java.util.Arrays.toString(arr));
```

### Output

```text
[a, b, c]
```

---

## 1️⃣1️⃣ `String.valueOf()`

`valueOf()` is a **static method** that converts values into their String representation.

```java
System.out.println(String.valueOf(10));
System.out.println(String.valueOf(10.5));
System.out.println(String.valueOf(true));
```

### Output

```text
10
10.5
true
```

It is overloaded for different data types and also has an overload for objects.

---

## 1️⃣2️⃣ `startsWith(String prefix, int offset)`

Checks whether the String starts with the specified prefix at the given zero-based offset.

```java
String s = "HelloJava";
System.out.println(s.startsWith("Java", 5));
```

### Output

```text
true
```

### Related overload

```java
s.startsWith("Hello");
```

checks whether the entire String starts with the specified prefix.

---

## 1️⃣3️⃣ `endsWith(String suffix)`

Checks whether the String ends with the specified suffix.

```java
String s = "HelloJava";
System.out.println(s.endsWith("Java"));
```

### Output

```text
true
```

> `endsWith()` does not have an offset parameter.

---

## 1️⃣4️⃣ `trim()`

Removes leading and trailing characters with code points less than or equal to `U+0020` (space and other basic control/whitespace characters).

```java
String s = "  Java  ";
System.out.println(s.trim());
```

### Output

```text
Java
```

> `trim()` does not remove all Unicode whitespace. For broader Unicode-aware whitespace handling, `strip()` and related methods are available in modern Java.

---

## 1️⃣5️⃣ `toCharArray()`

Converts the String into a new character array.

```java
String s = "abc";
char[] arr = s.toCharArray();

System.out.println(java.util.Arrays.toString(arr));
```

### Output

```text
[a, b, c]
```

---

## 1️⃣6️⃣ `String.copyValueOf()`

Creates a String from a character array.

```java
char[] arr = {'a', 'b', 'c'};
String s = String.copyValueOf(arr);

System.out.println(s);
```

### Output

```text
abc
```

> `String.copyValueOf(char[])` is a static method.

---

## 1️⃣7️⃣ `matches(String regex)`

Checks whether the **entire String** matches the specified regular expression.

```java
String s = "12345";
System.out.println(s.matches("\\d+"));
```

### Output

```text
true
```

> `matches()` checks the complete String, not just a substring.

---

## 1️⃣8️⃣ `String.join()`

`join()` is a static method that joins multiple character sequences using a delimiter.

```java
String result = String.join("-", "2025", "11", "24");
System.out.println(result);
```

### Output

```text
2025-11-24
```

---

## 1️⃣9️⃣ `isEmpty()`

Returns `true` when the String has length `0`.

```java
String s = "";
System.out.println(s.isEmpty());
```

### Output

```text
true
```

> A String containing a space is **not** empty because its length is `1`.

---

## 2️⃣0️⃣ `intern()`

Returns the canonical representation of the String from the String Pool.

```java
String s = new String("abc").intern();
```

After `intern()`, the reference returned points to the canonical pooled String for that content.

> `intern()` returns the pooled reference; it does not simply "move" the existing object into the String Pool.

---

## 2️⃣1️⃣ `equals()`

Compares the **content** of two Strings.

```java
System.out.println("abc".equals("abc"));
```

### Output

```text
true
```

> Use `equals()` when you want content equality between Strings.

---

## 2️⃣2️⃣ `compareTo()`

Compares Strings lexicographically and returns an integer indicating their natural ordering.

```java
System.out.println("abc".compareTo("abd"));
```

### Result Meaning

```text
0  → equal in natural ordering
< 0 → first String comes before second
> 0 → first String comes after second
```

> Do not depend on the exact negative or positive value; depend on its sign.

---

## 2️⃣3️⃣ `toString()`

`String` overrides `Object.toString()` and returns the String's own content.

```java
String s = "Java";
System.out.println(s.toString());
```

### Output

```text
Java
```

---

## 📊 Quick Revision — Method Categories

| Category | Methods |
|---|---|
| Character | `charAt()`, `toCharArray()` |
| Length | `length()`, `isEmpty()` |
| Modification / Transformation | `concat()`, `replace()`, `toUpperCase()`, `toLowerCase()`, `trim()` |
| Searching | `indexOf()`, `lastIndexOf()` |
| Extraction | `substring()` |
| Splitting | `split()` |
| Conversion | `String.valueOf()`, `toCharArray()`, `String.copyValueOf()` |
| Checking | `startsWith()`, `endsWith()`, `matches()` |
| Joining | `String.join()` |
| Comparison | `equals()`, `compareTo()` |
| Object / Pool | `toString()`, `intern()` |

## 🧠 Remember

```text
CHARACTER → charAt(), toCharArray()
LENGTH    → length(), isEmpty()
CHANGE    → concat(), replace(), case conversion, trim()
SEARCH    → indexOf(), lastIndexOf()
EXTRACT   → substring()
SPLIT     → split()
CONVERT   → valueOf(), copyValueOf()
CHECK     → startsWith(), endsWith(), matches()
JOIN      → String.join()
COMPARE   → equals(), compareTo()
POOL      → intern()
```

> **Small methods, many possibilities — String provides a rich API for working with text.**

## 🎯 Interview Questions

1. Why does `String` return a new object from methods such as `concat()` and `replace()`?
2. What is the difference between `length()` and `isEmpty()`?
3. What is the difference between `indexOf()` and `lastIndexOf()`?
4. What is the difference between `substring()` and `subSequence()`?
5. What does `split()` return?
6. Why is `String.valueOf()` static?
7. What does `startsWith(String, int)` do?
8. What does `trim()` remove, and how is it different from `strip()`?
9. What does `matches()` check?
10. What is the purpose of `intern()`?
11. What is the difference between `equals()` and `compareTo()`?
12. What does `String.join()` do?

## 🔗 Related Notes

- [String Overview →](01-string-overview.md)
- [String Immutability →](02-string-immutability.md)
- [Interfaces Implemented by String →](21-interfaces-implemented-by-string.md)
- [Overridden Methods in String →](20-overridden-methods-in-string.md)
- [String `intern()` →](13-string-intern.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)
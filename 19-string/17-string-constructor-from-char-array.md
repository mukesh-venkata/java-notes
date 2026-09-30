<a name="top"></a>

# 🔤 17. String Constructor from char[]

> **Core idea:** `new String(char[])` creates a String from the characters contained in an array.

## 🧠 Syntax

```java
String str = new String(charArray);
```

## 🔍 Example

```java
char[] chars = {'J', 'A', 'V', 'A'};

String str = new String(chars);

System.out.println(str);
```

Output:

```text
JAVA
```

## 🔄 Conversion Flow

```text
char[]
  │
  ├── 'J'
  ├── 'A'
  ├── 'V'
  └── 'A'
        ↓
new String(chars)
        ↓
      "JAVA"
```

## 🧠 Memory Concept

The constructor uses the character data to create a String object.

This is different from simply assigning a character array to a String reference; the types are different.

## 📌 Example with a Range

Java also provides constructors that can create a String from part of a character array:

```java
char[] chars = {'J', 'A', 'V', 'A'};

String str = new String(chars, 1, 2);

System.out.println(str);
```

Output:

```text
AV
```

Here:

- `1` is the starting index.
- `2` is the number of characters.

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. Can a char array be converted into String?</summary>
<br>

Yes.

</details>

<details>
<summary>2. Which constructor is commonly used?</summary>
<br>

new String(char[]).

</details>

<details>
<summary>3. Can a String be created from only part of a char array?</summary>
<br>

Yes. The String constructor has an overload that accepts an offset and count.

</details>
## 🔗 Related Notes

- [Constructors Overview →](15-string-constructors-overview.md)
- [Creating String from Character Array →](11-string-from-character-array.md)
- [Byte Array Constructor →](18-string-constructor-from-byte-array.md)
- [Quick Revision →](19-string-constructors-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

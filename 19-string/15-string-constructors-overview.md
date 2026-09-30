<a name="top"></a>

# 🧱 15. String Constructors — Overview

> **Core idea:** String constructors create String objects from different kinds of input data.

## 🧠 What Are String Constructors?

The String class provides constructors that can create String objects from inputs such as:

- Another String
- A character array
- A byte array

Constructors are used with the `new` keyword.

## 📚 Constructor Overview

| Constructor | Purpose |
|---|---|
| `String(String value)` | Creates a String from another String |
| `String(char[] value)` | Creates a String from characters |
| `String(byte[] value)` | Creates a String by decoding bytes using the platform default charset |
| `String(byte[] value, Charset charset)` | Creates a String using the specified charset |

## 🔄 Learning Flow

```text
String Constructors
       │
       ├── String
       │     ↓
       │  new String("Java")
       │
       ├── char[]
       │     ↓
       │  new String(chars)
       │
       └── byte[]
             ↓
       new String(bytes, charset)
```

## 📌 Important

A String literal such as:

```java
String s = "Java";
```

does not require the `new` keyword.

Using:

```java
String s = new String("Java");
```

explicitly creates a new String object.

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What are String constructors?</summary>
<br>

Constructors of String that create String objects from sources such as another String, a character array, or a byte array.

</details>

<details>
<summary>2. Can String be created from a char array?</summary>
<br>

Yes. For example, new String(charArray).

</details>

<details>
<summary>3. Can String be created from a byte array?</summary>
<br>

Yes. The bytes are decoded using a charset.

</details>

<details>
<summary>4. Why should an explicit charset be used when decoding bytes?</summary>
<br>

To make the byte-to-text conversion predictable and independent of the platform's default charset.

</details>
## 🔗 Related Notes

- [String Constructor from String →](16-string-constructor-from-string.md)
- [String Constructor from char[] →](17-string-constructor-from-char-array.md)
- [String Constructor from byte[] →](18-string-constructor-from-byte-array.md)
- [Quick Revision →](19-string-constructors-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

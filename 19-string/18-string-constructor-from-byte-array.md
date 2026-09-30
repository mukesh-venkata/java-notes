<a name="top"></a>

# 🧩 18. String Constructor from byte[]

> **Core idea:** A byte array must be decoded into characters using a charset to create a String.

## 🧠 Basic Syntax

```java
String str = new String(byteArray);
```

This constructor decodes the bytes using the platform's default charset.

## 🔍 Example

```java
byte[] bytes = {72, 101, 108, 108, 111};

String str = new String(bytes);

System.out.println(str);
```

The intended output for an ASCII-compatible charset is:

```text
Hello
```

The byte values correspond to the characters:

| Byte | Character |
|---:|:---:|
| 72 | H |
| 101 | e |
| 108 | l |
| 108 | l |
| 111 | o |

## ⚠️ Charset Matters

For predictable decoding, specify the charset explicitly.

```java
import java.nio.charset.StandardCharsets;

byte[] bytes = {72, 101, 108, 108, 111};

String str = new String(bytes, StandardCharsets.UTF_8);
```

This makes the encoding choice explicit.

## 🔄 Conversion Flow

```text
byte[]
  ↓
decode using charset
  ↓
String
```

## 📌 Why Explicit Charset Is Better

A byte sequence has no universal text meaning by itself. The charset defines how those bytes map to characters.

Therefore, when the encoding is known, prefer:

```java
new String(bytes, StandardCharsets.UTF_8)
```

over relying on the platform default charset.

## 🎯 Interview Questions

1. Can String be created from byte[]? **Yes.**
2. What does byte[] → String involve? **Decoding bytes using a charset.**
3. What does `new String(byte[])` use? **The platform default charset.**
4. How can you make decoding predictable? **Specify an explicit Charset.**

## 🔗 Related Notes

- [Constructors Overview →](15-string-constructors-overview.md)
- [String from Character Array →](17-string-constructor-from-char-array.md)
- [String Memory & Storage →](12-string-memory-and-storage.md)
- [Quick Revision →](19-string-constructors-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

<a name="top"></a>

# ⚡ 19. String Constructors — Quick Revision

> **30-second revision:** String constructors can build Strings from another String, character arrays, and byte arrays.

## 📊 Constructor Comparison

| Constructor | Input | Result |
|---|---|---|
| `String(String s)` | String | String with the same contents |
| `String(char[] value)` | char array | String from characters |
| `String(byte[] value)` | byte array | String decoded with platform default charset |
| `String(byte[] value, Charset charset)` | byte array + charset | String decoded using specified charset |

## 🔑 Key Points

- `new String("Java")` creates a new String object.
- The literal `"Java"` is an interned String.
- `new String(char[])` creates a String from character data.
- `new String(byte[])` decodes bytes using the platform default charset.
- Prefer an explicit charset when decoding known byte data.
- `StandardCharsets.UTF_8` is a common explicit choice when the data is UTF-8.
- `==` compares references.
- `equals()` compares String contents.

## 🧠 Memory Trick

```text
String  → same text
char[]  → characters → String
byte[]  → decode → String
Charset → tells Java how bytes become characters
```

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What are common String constructors?</summary>
<br>

Constructors can create Strings from another String, char arrays, byte arrays, and other supported input forms.

</details>

<details>
<summary>2. What does <code>new String(String)</code> do?</summary>
<br>

It creates a new String object whose contents are copied from the supplied String.

</details>

<details>
<summary>3. How is a char[] converted to String?</summary>
<br>

Use a String constructor such as new String(charArray).

</details>

<details>
<summary>4. How is a byte[] converted to String?</summary>
<br>

Decode the bytes using a charset, preferably by specifying an explicit Charset.

</details>

<details>
<summary>5. Why should a charset be specified when decoding bytes?</summary>
<br>

To make the result predictable across platforms and environments.

</details>

<details>
<summary>6. What is the difference between == and equals() for Strings?</summary>
<br>

== compares object references, while equals() compares String contents.

</details>
## 🔗 Related Notes

- [Constructors Overview →](15-string-constructors-overview.md)
- [String Constructor from String →](16-string-constructor-from-string.md)
- [String Constructor from char[] →](17-string-constructor-from-char-array.md)
- [String Constructor from byte[] →](18-string-constructor-from-byte-array.md)
- [Topic 35 — String Object Creation →](14-string-object-creation-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

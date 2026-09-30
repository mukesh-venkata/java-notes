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

## 🎯 Interview Questions

1. What are common String constructors?
2. What does `new String(String)` do?
3. How is a char[] converted to String?
4. How is a byte[] converted to String?
5. Why should a charset be specified when decoding bytes?
6. What is the difference between `==` and `equals()` for Strings?

## 🔗 Related Notes

- [Constructors Overview →](15-string-constructors-overview.md)
- [String Constructor from String →](16-string-constructor-from-string.md)
- [String Constructor from char[] →](17-string-constructor-from-char-array.md)
- [String Constructor from byte[] →](18-string-constructor-from-byte-array.md)
- [Topic 35 — String Object Creation →](14-string-object-creation-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

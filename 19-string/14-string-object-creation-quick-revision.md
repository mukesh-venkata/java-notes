<a name="top"></a>

# ⚡ 14. Creating String Objects — Quick Revision

> **30-second revision:** String literals use the String Pool; `new String(...)` creates an additional String object; `intern()` returns the canonical pooled String.

## 🧠 Master Table

| Approach | Example | Main result |
|---|---|---|
| Literal | `String s = "Java";` | Interned String |
| new | `new String("Java")` | New String object |
| char[] | `new String(chars)` | New String from characters |
| intern() | `s.intern()` | Canonical pooled String |

## 🔑 Key Rules

- Identical String literals can share the same pooled String.
- `==` compares references.
- `equals()` compares String contents.
- `new String(...)` creates a distinct String object.
- A literal used as an argument to `new String(...)` is still an interned literal.
- `new String(char[])` creates a String from character data.
- `intern()` returns the canonical pooled String.
- `intern()` does not simply move a heap String object into the pool.
- String Pool management is JVM-implementation detail; use the conceptual pooled/canonical model for learning.

## 🧠 Memory Trick

```text
Literal → Pool
new     → New object
char[]   → String
intern() → Pool reference
```

## 🎯 Interview Questions

1. Where are String literals interned?
2. Why can two identical literals have the same reference?
3. What does new String("Java") create?
4. Why can two new String() objects have == false?
5. What is the difference between == and equals()?
6. What does intern() return?
7. Does intern() move a heap object into the pool?
8. How can a char[] be converted to String?

## 🔗 Related Notes

- [Creating String Objects Overview →](08-creating-string-objects-overview.md)
- [String Literals & String Pool →](09-string-literals-and-string-pool.md)
- [String Using new →](10-string-using-new-operator.md)
- [String from Character Array →](11-string-from-character-array.md)
- [String Memory & Storage →](12-string-memory-and-storage.md)
- [intern() →](13-string-intern.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

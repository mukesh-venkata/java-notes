<a name="top"></a>

# 📊 6. String vs StringBuffer vs StringBuilder

## 🧠 Comparison Table

| Feature | String | StringBuffer | StringBuilder |
|---|---|---|---|
| Mutability | Immutable | Mutable | Mutable |
| Synchronization | Not applicable to immutable state | Synchronized methods | Not synchronized |
| Typical use | Fixed/unchanging text | Mutable text where synchronized methods are relevant | Mutable text in typical single-threaded use |
| Modification | Produces new String objects | Modifies the same buffer | Modifies the same builder |
| Typical performance | Repeated modification can create more objects | Synchronization adds overhead | Typically faster than StringBuffer in single-threaded use |

## 🔒 Thread-Safety Clarification

- String is immutable, so its state cannot be changed after construction.
- StringBuffer provides synchronized methods.
- StringBuilder does not provide synchronization.
- Immutability and synchronization are different mechanisms.

## 🔄 Modification Model

~~~text
String
  ↓
immutable
  ↓
operation → new String

StringBuffer
  ↓
mutable + synchronized
  ↓
operation → same buffer

StringBuilder
  ↓
mutable + not synchronized
  ↓
operation → same builder
~~~

## 🎯 Choosing a Class

### String
Use when the text value should not change.

### StringBuffer
Use when a mutable character sequence is needed and synchronized methods are appropriate.

### StringBuilder
Use when a mutable character sequence is needed and synchronization is not required.

## ⚠️ Performance Note

“StringBuilder is faster” is context-dependent. The usual distinction is that StringBuilder avoids the synchronization overhead present in StringBuffer, making it generally preferable for ordinary single-threaded use.

## 🎯 Interview Questions

1. Is String immutable?
2. Is StringBuffer mutable?
3. Is StringBuilder mutable?
4. Which one is synchronized?
5. Why is StringBuilder commonly preferred in single-threaded code?
6. What is the difference between immutability and synchronization?
7. What happens when a String is modified?

## 🔗 Related Notes

- [String Overview →](01-string-overview.md)
- [String Immutability →](02-string-immutability.md)
- [StringBuffer →](04-stringbuffer.md)
- [StringBuilder →](05-stringbuilder.md)
- [Quick Revision →](07-string-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

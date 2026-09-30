<a name="top"></a>

# 🏊 13. String intern()

> **Core idea:** `intern()` returns the canonical pooled String for the same character sequence.

## 🧠 Basic Example

```java
String s1 = new String("Java");
String s2 = s1.intern();
String s3 = "Java";

System.out.println(s2 == s3);
```

Output:

```text
true
```

Why?

- `s1` refers to a separately created String object.
- `s1.intern()` returns the canonical pooled String for the contents.
- `s3` refers to the same pooled String.

## 🔄 Flow

```text
s1
 ↓
Heap String "Java"

s1.intern()
 ↓
Canonical pooled "Java"
 ↑
s2 and s3
```

## 📌 If the String Is Already in the Pool

If an equal String is already interned, `intern()` returns the existing canonical pooled reference.

## 📌 If It Is Not Already in the Pool

The String is added to the pool and the canonical pooled reference is returned.

## ⚠️ Important Correction

`intern()` does **not** simply move the existing heap object into the String Pool.

It returns the canonical pooled representation for the String's contents.

## 🔍 Reference vs Content

```java
String s1 = new String("Java");

System.out.println(s1 == "Java");          // false
System.out.println(s1.intern() == "Java"); // true
```

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What does <code>intern()</code> return?</summary>
<br>

The canonical pooled String for the same contents.

</details>

<details>
<summary>Q2. Does <code>intern()</code> modify the original String?</summary>
<br>

No. String is immutable. intern() returns a pooled reference; it does not modify the original String.

</details>

<details>
<summary>Q3. Does <code>intern()</code> move the heap object into the pool?</summary>
<br>

No. It returns the canonical pooled reference for the String's contents.

</details>

<details>
<summary>Q4. Why can <code>intern()</code> make <code>==</code> true?</summary>
<br>

Because two references can point to the same canonical pooled String after interning.

</details>
## 🔗 Related Notes

- [String Literals & String Pool →](09-string-literals-and-string-pool.md)
- [new Operator →](10-string-using-new-operator.md)
- [Memory & Storage →](12-string-memory-and-storage.md)
- [Quick Revision →](14-string-object-creation-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

<a name="top"></a>

# 🔤 21. Interfaces Implemented by String

> **30-second revision:** `String` implements `CharSequence`, `Comparable<String>`, and `Serializable` — giving it standard character-sequence operations, natural ordering, and serialization support.

## 📌 Overview

`String` is a `final` class that implements three important interfaces:

1. `CharSequence`
2. `Comparable<String>`
3. `Serializable`

A simplified declaration is:

```java
public final class String
        implements CharSequence, Comparable<String>, Serializable {
    // ...
}
```

### Why does `String` implement these interfaces?

| Interface | Purpose |
|---|---|
| `CharSequence` | Provides a common way to work with sequences of characters |
| `Comparable<String>` | Provides natural lexicographical ordering |
| `Serializable` | Allows String objects to participate in Java serialization |

---

## 1️⃣ `CharSequence`

`CharSequence` provides a standard way to access and work with a sequence of characters.

It is implemented by classes such as:

- `String`
- `StringBuilder`
- `StringBuffer`

### Important methods

| Method | Purpose |
|---|---|
| `charAt(int index)` | Returns the character at the specified index |
| `length()` | Returns the number of characters |
| `subSequence(int start, int end)` | Returns a portion of the sequence |
| `toString()` | Returns a String representation of the sequence |

### Example

```java
String s = "Java";

System.out.println(s.charAt(0));
System.out.println(s.length());
System.out.println(s.subSequence(1, 3));
```

### Output

```text
J
4
av
```

### 🔑 Key Point

Because `String` implements `CharSequence`, a String can be used wherever a `CharSequence` is expected.

```java
CharSequence sequence = "Java";

System.out.println(sequence.length());
System.out.println(sequence.charAt(0));
```

---

## 2️⃣ `Comparable<String>`

`String` implements `Comparable<String>` to provide its natural ordering.

The interface defines:

```java
public interface Comparable<T> {
    int compareTo(T o);
}
```

For Strings, `compareTo()` performs a **lexicographical comparison**.

### Example

```java
String s1 = "Apple";
String s2 = "Banana";

int result = s1.compareTo(s2);
System.out.println(result);
```

### Result

The result is negative because `"Apple"` comes before `"Banana"` in natural lexicographical ordering.

The exact negative number should not be relied upon.

### Return Value Meaning

| Result | Meaning |
|---|---|
| `0` | Both Strings are equal in their natural ordering |
| Negative | First String comes before the second |
| Positive | First String comes after the second |

### 🔑 Key Point

```text
compareTo() < 0  → first comes before second
compareTo() == 0 → strings are equal in natural ordering
compareTo() > 0  → first comes after second
```

This natural ordering is useful with sorting APIs and ordered collections such as `TreeSet` and `TreeMap`.

---

## 3️⃣ `Serializable`

`String` implements `Serializable`, which allows String objects to participate in Java object serialization.

Serialization converts an object's state into a byte stream that can be stored or transmitted.

`Serializable` is a **marker interface**, meaning it does not declare methods that implementing classes must implement.

A simplified declaration is:

```java
public interface Serializable {
    // no methods
}
```

### Example Use Cases

- Storing String-containing object state in a file
- Sending serializable object state over a network
- Caching serialized object state

### 🔑 Key Point

```text
Serializable → object state → byte stream
```

---

## 🧠 One Class — Three Interfaces

```text
                       String
                         │
          ┌──────────────┼──────────────┐
          ↓              ↓              ↓
   CharSequence     Comparable       Serializable
          │          <String>             │
          ↓              ↓                ↓
   Character       Natural order      Serialization
    sequence       / comparison       support
```

### Easy Memory Trick

```text
CHAR → CharSequence
COMPARE → Comparable<String>
SAVE / SEND → Serializable
```

---

## 📊 Quick Comparison

| Interface | Purpose | Key Methods / Points |
|---|---|---|
| `CharSequence` | Common abstraction for character sequences | `charAt()`, `length()`, `subSequence()`, `toString()` |
| `Comparable<String>` | Natural ordering of Strings | `compareTo(String)` |
| `Serializable` | Enables Java serialization | Marker interface; no methods |

---

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. Which interfaces does String implement?</summary>
<br>

CharSequence, Comparable<String>, and Serializable.

</details>

<details>
<summary>2. Why does String implement CharSequence?</summary>
<br>

To provide the standard CharSequence abstraction for working with a sequence of characters.

</details>

<details>
<summary>3. What are the important methods in CharSequence?</summary>
<br>

charAt(), length(), subSequence(), and toString().

</details>

<details>
<summary>4. What does String.compareTo() do?</summary>
<br>

It performs a lexicographical comparison and returns a negative, zero, or positive integer according to natural ordering.

</details>

<details>
<summary>5. What do negative, zero, and positive values from compareTo() mean?</summary>
<br>

Negative means the first String comes before the second; zero means equal in natural ordering; positive means the first comes after the second.

</details>

<details>
<summary>6. Why should you not depend on the exact negative or positive value returned by compareTo()?</summary>
<br>

The contract specifies the sign and ordering relationship, not one particular numeric value for all comparisons.

</details>

<details>
<summary>7. Why does String implement Serializable?</summary>
<br>

So String objects can participate in Java serialization.

</details>

<details>
<summary>8. What is a marker interface?</summary>
<br>

An interface used to mark a class as having a particular capability or property without requiring implementation of interface methods.

</details>

<details>
<summary>9. Can a String be assigned to a CharSequence reference?</summary>
<br>

Yes. String implements CharSequence.

</details>

<details>
<summary>10. How does Comparable<String> help when Strings are sorted?</summary>
<br>

It provides String's natural ordering through compareTo(), which sorting APIs can use.

</details>
## ⚡ Quick Revision

| Interface | String's Role | Remember |
|---|---|---|
| `CharSequence` | Works as a character sequence | `charAt`, `length`, `subSequence` |
| `Comparable<String>` | Provides natural String ordering | `compareTo()` |
| `Serializable` | Supports Java serialization | Marker interface |

### 🧠 Remember

```text
String
  ↓
CHAR     → CharSequence
COMPARE  → Comparable<String>
SAVE     → Serializable
```

> **One String class → three useful capabilities: character sequence, natural ordering, and serialization support.**

## 🔗 Related Notes

- [String Overview →](01-string-overview.md)
- [StringBuffer →](04-stringbuffer.md)
- [StringBuilder →](05-stringbuilder.md)
- [Overridden Methods in String →](20-overridden-methods-in-string.md)
- [String Constructors Quick Revision →](19-string-constructors-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)
<a name="top"></a>

# 🔤 20. Overridden Methods in String

> **30-second revision:** `String` overrides `toString()`, `hashCode()` and `equals()` from `Object` so their behavior is based on String content.

## 📌 Overview

`String` is a class, and like every Java class, it inherits methods from `Object`.

For meaningful String behavior, `String` overrides important methods such as:

- `toString()`
- `hashCode()`
- `equals()`

> **Same method name → different behavior in the `String` class.**

---

## 1️⃣ `toString()`

`String` overrides `toString()` so that it returns the String's own content.

```java
String s = "Java";

System.out.println(s.toString());
```

### Output

```text
Java
```

The default `Object.toString()` implementation produces a value based on the class name and hash code, but `String` provides meaningful content instead.

### 🔑 Key Point

```text
String.toString() → returns the String content
```

Since printing an object uses `toString()` internally, this is why:

```java
System.out.println(s);
```

also prints:

```text
Java
```

---

## 2️⃣ `hashCode()`

`String` overrides `hashCode()`.

The hash code is calculated from the characters/content of the String.

```java
String s1 = "Java";
String s2 = "Java";

System.out.println(s1.hashCode());
System.out.println(s2.hashCode());
```

### Output

```text
2301506
2301506
```

The exact numeric value is determined by Java's String hash-code algorithm.

### 🔑 Important Rule

If two Strings are equal according to `equals()`, they must have the same hash code.

```text
s1.equals(s2) → true
        ↓
s1.hashCode() == s2.hashCode()
```

However, the reverse is not guaranteed:

```text
same hash code ≠ necessarily equal objects
```

---

## 3️⃣ `equals()`

`String` overrides `equals()` to compare the **content** of two Strings.

```java
String s1 = new String("Java");
String s2 = new String("Java");

System.out.println(s1.equals(s2));
```

### Output

```text
true
```

Even though `s1` and `s2` are different String objects, their contents are the same.

### 🔑 Key Point

```text
String.equals() → compares String content
```

So:

```java
String s1 = new String("Java");
String s2 = new String("Java");

s1.equals(s2);   // true
s1 == s2;        // false
```

---

## 4️⃣ `==` Operator

`==` behaves differently for primitives and object references.

### Primitive Types

For primitives, `==` compares **values**.

```java
int a = 10;
int b = 10;

System.out.println(a == b);
```

### Output

```text
true
```

### Object / Reference Types

For objects, `==` compares **references** — whether both references point to the same object.

```java
String s1 = new String("Java");
String s2 = new String("Java");

System.out.println(s1 == s2);
```

### Output

```text
false
```

Both objects contain `"Java"`, but they are separate objects.

### String Literals

String literals are stored in the String Pool.

```java
String s1 = "Java";
String s2 = "Java";

System.out.println(s1 == s2);
```

### Output

```text
true
```

Both references point to the same pooled String object.

---

## 🧠 Memory Representation

### String Literal

```text
String Pool
┌──────────────┐
│    "Java"    │
└──────────────┘
     ↑      ↑
    s1      s2

s1 == s2 → true
```

### Using `new String("Java")`

```text
String Pool              Heap
┌──────────────┐        ┌──────────────┐
│    "Java"    │        │ String "Java"│
└──────────────┘        └──────────────┘
                           ↑
                          s2

s1 → pooled "Java"
```

With:

```java
String s1 = "Java";
String s2 = new String("Java");

System.out.println(s1 == s2);
```

the result is:

```text
false
```

because the references point to different objects.

> **Note:** `new String("Java")` creates a new String object even though the literal `"Java"` is already available in the String Pool.

---

## 📊 Method / Operator Comparison

| Method / Operator | Overridden in `String`? | Behavior |
|---|:---:|---|
| `toString()` | Yes | Returns String content |
| `hashCode()` | Yes | Calculated from String content |
| `equals()` | Yes | Compares String content |
| `==` (primitives) | No | Compares primitive values |
| `==` (objects) | No | Compares object references |

---

## 🎯 Interview Questions

1. Which `Object` methods are commonly overridden by `String`?
2. What does `String.toString()` return?
3. How is a String's `hashCode()` calculated?
4. Why do equal Strings have the same hash code?
5. What does `String.equals()` compare?
6. What is the difference between `==` and `equals()` for Strings?
7. Why can two String literals make `==` return `true`?
8. Why does `new String("Java") == new String("Java")` return `false`?
9. Can two unequal Strings have the same hash code?
10. Why is `equals()` important when Strings are used as keys in a `HashMap`?

---

## ⚡ Quick Revision

| Method / Operator | String Behavior | Example |
|---|---|---|
| `toString()` | Returns String's content | `"Java".toString()` → `"Java"` |
| `hashCode()` | Calculated from content | Equal Strings → same hash code |
| `equals()` | Compares content | `new String("Java").equals(new String("Java"))` → `true` |
| `==` (primitives) | Compares values | `10 == 10` → `true` |
| `==` (objects) | Compares references | `new String("Java") == new String("Java")` → `false` |
| `==` (literals) | Same pooled object may be referenced | `"Java" == "Java"` → `true` |

### 🧠 Remember

```text
equals() → CONTENT
==       → REFERENCE (objects)
hashCode → CONTENT-BASED HASH
toString → STRING CONTENT
```

> **Content matters in `equals()` and `hashCode()`. Reference identity matters in `==` for objects.**

## 🔗 Related Notes

- [String Overview →](01-string-overview.md)
- [String Literals & String Pool →](09-string-literals-and-string-pool.md)
- [String Using `new` Operator →](10-string-using-new-operator.md)
- [String `intern()` →](13-string-intern.md)
- [String Constructors Quick Revision →](19-string-constructors-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)
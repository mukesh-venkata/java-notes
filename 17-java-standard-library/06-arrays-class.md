<a name="top"></a>

# 🔢 06. Arrays Class

> **30-second revision:** `java.util.Arrays` is a `final` utility class with static methods for common array operations such as printing, sorting, searching, comparing, filling, and copying arrays.

## 📌 Overview

`java.util.Arrays` is a utility class provided for common operations on arrays.

- It belongs to the `java.util` package.
- It is a `final` utility class.
- Its commonly used operations are provided through `static` methods.
- Like every Java class, it ultimately extends `Object`.

A simplified declaration is:

```java
public final class Arrays extends Object {
    // static utility methods
}
```

Import:

```java
import java.util.Arrays;
```

---

## 1️⃣ `toString()`

`Arrays.toString()` converts a one-dimensional array into a readable String representation.

```java
int[] a = {3, 6, 9};
System.out.println(Arrays.toString(a));
```

### Output

```text
[3, 6, 9]
```

---

## 2️⃣ `deepToString()`

`Arrays.deepToString()` is useful for displaying multidimensional or nested arrays.

```java
int[][] arr = {
    {1, 2},
    {3, 4}
};

System.out.println(Arrays.deepToString(arr));
```

### Output

```text
[[1, 2], [3, 4]]
```

### 🔑 Remember

```text
1D array         → Arrays.toString()
Nested arrays    → Arrays.deepToString()
```

---

## 3️⃣ `sort()`

`Arrays.sort()` sorts an array according to the ordering defined by the applicable overload. For primitive arrays, this results in ascending numerical order.

```java
int[] a = {5, 2, 9, 1};
Arrays.sort(a);
System.out.println(Arrays.toString(a));
```

### Output

```text
[1, 2, 5, 9]
```

> `sort()` modifies the supplied array.

---

## 4️⃣ `binarySearch()`

`Arrays.binarySearch()` searches a sorted array using binary search.

```java
int[] a = {10, 20, 30, 40};
int index = Arrays.binarySearch(a, 30);
System.out.println(index);
```

### Output

```text
2
```

### 🔑 Important

Treat the array as sorted according to the ordering used by the search before calling the method.

If the element is not found, the method returns a negative value. For the standard sorted-array overload, the result is `-(insertion point) - 1`.

---

## 5️⃣ `equals()`

`Arrays.equals()` compares two one-dimensional arrays element-by-element.

```java
int[] a = {1, 2, 3};
int[] b = {1, 2, 3};

System.out.println(Arrays.equals(a, b));
```

### Output

```text
true
```

### `array.equals()` vs `Arrays.equals()`

```java
a.equals(b);
```

uses the inherited `Object.equals()` behavior for arrays and therefore compares references.

Whereas:

```java
Arrays.equals(a, b);
```

compares the elements of the arrays.

> For multidimensional or nested arrays, use `Arrays.deepEquals()` for deep content comparison.

---

## 6️⃣ `fill()`

`Arrays.fill()` fills array elements with the specified value.

```java
int[] a = new int[5];
Arrays.fill(a, 7);

System.out.println(Arrays.toString(a));
```

### Output

```text
[7, 7, 7, 7, 7]
```

Range-based overloads can fill only a selected portion of an array.

---

## 7️⃣ `copyOf()`

`Arrays.copyOf()` creates a new array containing elements copied from the original array.

```java
int[] a = {1, 2, 3};
int[] b = Arrays.copyOf(a, 5);

System.out.println(Arrays.toString(b));
```

### Output

```text
[1, 2, 3, 0, 0]
```

When the requested length is larger than the original, the additional elements receive their type's default value.

> `copyOf()` creates a different array object.

---

## 8️⃣ Final Array Reference

`final` can be applied to an array reference.

```java
final int[] a = {1, 2, 3};
```

The reference cannot be reassigned:

```java
a = new int[]{4, 5, 6}; // ❌ Compilation error
```

But the elements can still be changed:

```java
a[0] = 100; // ✅ Allowed
System.out.println(Arrays.toString(a));
```

### Output

```text
[100, 2, 3]
```

### 🔑 Key Point

```text
final array reference → reference cannot change
                       array elements can change
```

---

## 🧠 Method Selection

```text
Display 1D array       → toString()
Display nested arrays  → deepToString()
Sort                   → sort()
Search                 → binarySearch()
Compare 1D arrays      → equals()
Compare nested arrays  → deepEquals()
Fill                   → fill()
Copy                   → copyOf()
```

---

## 📊 Quick Revision

| Method / Concept | Purpose |
|---|---|
| `toString()` | 1D array → readable String representation |
| `deepToString()` | Multidimensional/nested array → String representation |
| `sort()` | Sorts array elements |
| `binarySearch()` | Searches a sorted array |
| `equals()` | Compares 1D array contents |
| `fill()` | Fills array elements with a value |
| `copyOf()` | Creates a new copied array |
| `final` array reference | Reference cannot be reassigned, but elements can change |

## 🧠 Remember

```text
PRINT   → toString() / deepToString()
SORT    → sort()
SEARCH  → binarySearch()
COMPARE → equals() / deepEquals()
FILL    → fill()
COPY    → copyOf()
FINAL   → reference fixed, elements mutable
```

> **`Arrays` provides ready-made utilities for common array operations.**

## 🎯 Interview Questions & Answers

> **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What is <code>java.util.Arrays</code>?</summary>

`java.util.Arrays` is a `final` utility class in the `java.util` package that provides static methods for performing common operations on arrays.

</details>

<details>
<summary>2. What is the difference between <code>Arrays.toString()</code> and <code>Arrays.deepToString()</code>?</summary>

`Arrays.toString()` is used for one-dimensional arrays, while `Arrays.deepToString()` is designed for multidimensional or nested arrays.

</details>

<details>
<summary>3. Does <code>Arrays.sort()</code> modify the original array?</summary>

Yes. `Arrays.sort()` sorts the supplied array in place, so the original array is modified.

</details>

<details>
<summary>4. What condition should be satisfied before using <code>Arrays.binarySearch()</code>?</summary>

The array must be sorted according to the ordering used by the search. Otherwise, the result is not reliable.

</details>

<details>
<summary>5. What does <code>binarySearch()</code> return when an element is not found?</summary>

It returns a negative value. For the standard sorted-array overload, the result is `-(insertion point) - 1`.

</details>

<details>
<summary>6. What is the difference between <code>array.equals()</code> and <code>Arrays.equals()</code>?</summary>

An array inherits `equals()` from `Object`, so `array.equals(other)` compares references. `Arrays.equals()` compares corresponding elements of one-dimensional arrays.

</details>

<details>
<summary>7. When should <code>Arrays.deepEquals()</code> be used?</summary>

Use `Arrays.deepEquals()` when you need content-based comparison of multidimensional or nested arrays.

</details>

<details>
<summary>8. What does <code>Arrays.fill()</code> do?</summary>

It assigns the specified value to the elements of an array. Range-based overloads can fill only a selected portion.

</details>

<details>
<summary>9. What happens when <code>Arrays.copyOf()</code> creates a larger array?</summary>

A new array is created. Existing elements are copied, and the additional positions receive the default value of the array's component type.

</details>

<details>
<summary>10. Does <code>final int[] a</code> make the array elements immutable?</summary>

No. `final` prevents the array reference from being reassigned, but the elements of the referenced array can still be changed.

</details>

## 🔗 Related Notes

- [Java Standard Library Overview →](01-java-standard-library-overview.md)
- [Commonly Used Java Packages →](04-commonly-used-java-packages.md)
- [String Class Methods →](../19-string/22-string-class-methods.md)
- [Data Types →](../02-data-types/03-reference-data-types.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)
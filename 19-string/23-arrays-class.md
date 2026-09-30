<a name="top"></a>

# 🔢 23. Arrays Class

> **30-second revision:** `java.util.Arrays` is a `final` utility class that provides static methods for common array operations such as printing, sorting, searching, comparing, filling, and copying arrays.

## 📌 Overview

`java.util.Arrays` is a utility class containing static methods for working with arrays.

- It belongs to the `java.util` package.
- It is a `final` class.
- Its methods are primarily `static` utility methods.
- Like every Java class, it ultimately extends `Object`.

A simplified declaration is:

```java
public final class Arrays extends Object {
    // static utility methods
}
```

Import it with:

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

> For a one-dimensional array, use `Arrays.toString()` instead of printing the array reference directly.

---

## 2️⃣ `deepToString()`

`Arrays.deepToString()` is useful for displaying multidimensional arrays and nested arrays.

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
1D array          → Arrays.toString()
Nested arrays     → Arrays.deepToString()
```

---

## 3️⃣ `sort()`

`Arrays.sort()` sorts array elements in ascending order for the standard primitive-array overloads.

```java
int[] a = {5, 2, 9, 1};
Arrays.sort(a);
System.out.println(Arrays.toString(a));
```

### Output

```text
[1, 2, 5, 9]
```

> `sort()` modifies the supplied array; it does not create a sorted copy by default.

---

## 4️⃣ `binarySearch()`

`Arrays.binarySearch()` searches for an element using binary search.

The array must already be sorted according to the ordering used for the search.

```java
int[] a = {10, 20, 30, 40};
int index = Arrays.binarySearch(a, 30);
System.out.println(index);
```

### Output

```text
2
```

### If the element is not found

The method returns a negative value. More precisely, for the relevant sorted-array overload, the result is `-(insertion point) - 1`.

---

## 5️⃣ `equals()`

`Arrays.equals()` compares two arrays element-by-element for one-dimensional arrays.

```java
int[] a = {1, 2, 3};
int[] b = {1, 2, 3};

System.out.println(Arrays.equals(a, b));
```

### Output

```text
true
```

### `Arrays.equals()` vs array `equals()`

```java
a.equals(b);
```

compares object identity because arrays inherit `equals()` from `Object`.

Whereas:

```java
Arrays.equals(a, b);
```

compares the array elements.

> For multidimensional or nested arrays, use `Arrays.deepEquals()` when content-based deep comparison is required.

---

## 6️⃣ `fill()`

`Arrays.fill()` fills all elements of an array with the specified value.

```java
int[] a = new int[5];
Arrays.fill(a, 7);

System.out.println(Arrays.toString(a));
```

### Output

```text
[7, 7, 7, 7, 7]
```

There are also range-based overloads for filling a selected portion of an array.

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

> `copyOf()` creates a different array object; it does not make the two array references point to the same array.

---

## 8️⃣ Final Array Reference

`final` can be applied to an array reference.

```java
final int[] a = {1, 2, 3};
```

The reference cannot be reassigned to another array:

```java
a = new int[]{4, 5, 6}; // ❌ Compilation error
```

But the elements of the referenced array can still be changed:

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
| `deepToString()` | Nested/multidimensional array → String representation |
| `sort()` | Sorts array elements |
| `binarySearch()` | Searches a sorted array |
| `equals()` | Compares 1D array contents |
| `fill()` | Fills array elements with a value |
| `copyOf()` | Creates a copied array |
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

> **`Arrays` gives you ready-made utility methods so common array operations do not need to be implemented manually.**

## 🎯 Interview Questions

1. What is `java.util.Arrays`?
2. What is the difference between `Arrays.toString()` and `Arrays.deepToString()`?
3. Does `Arrays.sort()` modify the original array?
4. What condition must be satisfied before using `Arrays.binarySearch()`?
5. What does `binarySearch()` return when an element is not found?
6. What is the difference between `array.equals()` and `Arrays.equals()`?
7. When should `Arrays.deepEquals()` be used?
8. What does `Arrays.fill()` do?
9. What happens when `Arrays.copyOf()` creates a larger array?
10. Does `final int[] a` make the array elements immutable?

## 🔗 Related Notes

- [Arrays Overview →](../09-variables/01-variables-overview.md)
- [String Class Methods →](22-string-class-methods.md)
- [Type Casting →](../18-type-casting/01-type-casting-overview.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)
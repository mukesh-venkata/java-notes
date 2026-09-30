# 🔁 Java Enhanced `for` Loop — for-each

> **Topic 13 • Java Fundamentals**

The **enhanced `for` loop**, commonly called the **for-each loop**, iterates over the elements of an array or an object implementing `Iterable`.

---

## 📌 Syntax

```java
for (dataType variable : arrayOrIterable) {
    // loop body
}
```

---

## 💻 Array Example

```java
int[] numbers = {10, 20, 30};

for (int number : numbers) {
    System.out.println(number);
}
```

Output:

```text
10
20
30
```

No explicit index variable is required.

---

## 🧩 How to Read It

```text
for (int number : numbers)
     │       │
     │       └── source elements
     └────────── current element
```

Think:

> **For each number in numbers...**

---

## 🆚 Traditional for vs Enhanced for

### Traditional

```java
for (int i = 0; i < numbers.length; i++) {
    System.out.println(numbers[i]);
}
```

### Enhanced

```java
for (int number : numbers) {
    System.out.println(number);
}
```

The enhanced form is often cleaner when you only need each element.

---

## ⚠️ Important Limitations

Enhanced `for` is not the best choice when you need:

- The current index
- Custom index jumps
- Direct control over iteration order
- Certain structural modifications during collection traversal

For those cases, a traditional `for` loop or another iterator-based approach may be more appropriate.

---

## 🎤 Interview Quick Check

**Q1. What is another name for enhanced `for`?**  
A: For-each loop.

**Q2. Can it iterate over arrays?**  
A: Yes.

**Q3. Can it iterate over collections?**  
A: Yes, for collections that implement `Iterable`.

**Q4. Does it directly expose the array/collection index?**  
A: No.

---

## 🔗 Navigation

⬅️ [do-while Loop](./04-do-while-loop.md)

➡️ [Nested Loops](./06-nested-loops.md)

➡️ [Quick Revision](./07-looping-statements-quick-revision.md)

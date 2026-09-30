# 🪆 Java Nested Loops

> **Topic 13 • Java Fundamentals**

A **nested loop** is a loop placed inside another loop.

The inner loop completes its iterations for each iteration of the outer loop.

---

## 💻 Example

```java
for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 3; j++) {
        System.out.println(i + " " + j);
    }
}
```

Output:

```text
1 1
1 2
1 3
2 1
2 2
2 3
3 1
3 2
3 3
```

---

## 🔀 Execution Pattern

```text
Outer i = 1
 ├── Inner j = 1
 ├── Inner j = 2
 └── Inner j = 3

Outer i = 2
 ├── Inner j = 1
 ├── Inner j = 2
 └── Inner j = 3

Outer i = 3
 ├── Inner j = 1
 ├── Inner j = 2
 └── Inner j = 3
```

For this example:

```text
Outer iterations × Inner iterations
       3 × 3 = 9
```

---

## 📊 Iteration Table

| Outer `i` | Inner `j` values |
|---:|---|
| 1 | 1, 2, 3 |
| 2 | 1, 2, 3 |
| 3 | 1, 2, 3 |

---

## 🎯 Common Uses

Nested loops are useful for:

- Matrix processing
- Two-dimensional arrays
- Tables
- Pattern generation
- Comparing pairs of values

---

## ⚠️ Performance Note

If both loops run `n` times independently, the total number of inner-body executions is approximately:

```text
n × n = n²
```

So nested loops can lead to **O(n²)** time complexity in common cases.

The actual complexity depends on the loop bounds and work performed inside the loops.

---

## 🎤 Interview Quick Check

**Q1. What is a nested loop?**  
A: A loop inside another loop.

**Q2. In a 3 × 3 nested loop, how many times does the inner body execute if both loops run fully?**  
A: 9 times.

**Q3. What is a common complexity of two independent n-sized nested loops?**  
A: O(n²).

---

## 🔗 Navigation

⬅️ [Enhanced for Loop](./05-enhanced-for-loop.md)

➡️ [Quick Revision](./07-looping-statements-quick-revision.md)

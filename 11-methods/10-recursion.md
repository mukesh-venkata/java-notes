<a name="top"></a>

# 🔁 Java Recursion

> **Topic 18 • Methods**

**Recursion** occurs when a method directly or indirectly calls itself.

## 🧩 Two Essential Parts

1. **Base case** — stops recursion.
2. **Recursive case** — moves toward the base case.

```text
Method
  ↓
Recursive call
  ↓
Recursive call
  ↓
Base case
  ↓
Return
```

## 💻 Factorial Example

```java
static int factorial(int n) {
    if (n <= 1) {
        return 1;
    }

    return n * factorial(n - 1);
}
```

For `factorial(4)`, calls build downward and then return upward.

## 🧠 Call Stack

Each active recursive invocation requires execution state.

```text
factorial(4)
factorial(3)
factorial(2)
factorial(1)
──────────────
     Stack
```

Recursion without proper termination can eventually cause `StackOverflowError`.

## 🔄 Recursion vs Iteration

| Recursion | Iteration |
|---|---|
| Method calls itself | Loop repeats |
| Active calls consume call-stack resources | Usually avoids recursive call growth |
| Natural for trees/divide-and-conquer | Often simpler for straightforward repetition |

## 🎤 Interview Quick Check

**What is recursion?**  
A method calling itself directly or indirectly.

**What prevents infinite recursion?**  
A correct base case and progress toward it.

**What can excessive recursion cause?**  
`StackOverflowError`.

## 🔗 Navigation

⬅️ [Access & Overriding Rules](./09-method-access-and-overriding-rules.md)

➡️ [Method Hiding](./11-method-hiding.md)

➡️ [Quick Revision](./12-methods-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

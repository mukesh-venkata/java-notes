<a name="top"></a>

# 🧹 5. finalize() & Resource Cleanup

> **Core idea:** `finalize()` is a legacy finalization mechanism and should not be used for resource cleanup.

## 🕰️ Historical Purpose

The `finalize()` method was historically intended to give an object an opportunity to perform cleanup before the object was reclaimed by garbage collection.

Its historical declaration was:

```java
protected void finalize() throws Throwable
```

## ⚠️ Modern Java

`finalize()` has been **deprecated since Java 9** and was subsequently **removed from the modern Java API in Java 18**.

Therefore, new Java code should not rely on finalization.

Finalization is unsuitable for reliable resource management because its execution timing is not deterministic.

## 🚫 Do Not Use finalize() for Resource Cleanup

Resources such as files, streams, sockets, and database connections should be closed explicitly or through APIs designed for deterministic cleanup.

### Prefer try-with-resources

```java
try (java.io.BufferedReader reader =
         new java.io.BufferedReader(new java.io.FileReader("data.txt"))) {

    System.out.println(reader.readLine());

}
```

The resource is closed automatically when the try block completes.

## 🔄 Old Idea vs Modern Approach

| Historical approach | Modern approach |
|---|---|
| `finalize()` | `try-with-resources` |
| Cleanup timing not deterministic | Deterministic resource management |
| Legacy mechanism | Recommended for `AutoCloseable` resources |

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What was finalize() historically intended for?</summary>
<br>

Cleanup work before garbage collection reclaimed an object.

</details>

<details>
<summary>Q2. Should finalize() be used for resource cleanup?</summary>
<br>

No. Resource cleanup should be explicit and deterministic, such as with try-with-resources for AutoCloseable resources.

</details>

<details>
<summary>Q3. When was finalize() deprecated?</summary>
<br>

Java 9.

</details>

<details>
<summary>Q4. When was finalization removed from the modern Java API?</summary>
<br>

Java 18 deprecated and disabled finalization by default? Actually, Java 18 deprecated finalization for removal; it was not simply removed from the API in Java 18.

</details>

<details>
<summary>Q5. What should be preferred for AutoCloseable resources?</summary>
<br>

Try-with-resources or explicit close() management where appropriate.

</details>
## 🔗 Related Notes

- [Object Class Overview →](01-object-class-overview.md)
- [clone() & Shallow Copy →](04-clone-and-shallow-copy.md)
- [wait(), notify() & notifyAll() →](06-wait-notify-notifyall.md)
- [Quick Revision →](07-object-class-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

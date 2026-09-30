# ↩️ Java `return` Statement

> **Topic 14 • Java Fundamentals**

The `return` statement terminates the execution of the **current method**.

It can either return a value or return without a value.

---

## 1️⃣ Return Without a Value

A `void` method can use:

```java
return;
```

Example:

```java
static void checkAge(int age) {
    if (age < 18) {
        return;
    }

    System.out.println("Eligible");
}
```

When the condition is true, the method ends immediately.

---

## 2️⃣ Return With a Value

A non-void method can return a value compatible with its declared return type.

```java
static int getNumber() {
    return 10;
}
```

The caller can use the returned value:

```java
int value = getNumber();
```

---

## 🔀 Execution Flow

```text
Method starts
     │
     ↓
  statements
     │
  return?
     │
    Yes
     ↓
Method exits
     │
     ↓
Caller continues
```

Any statements after an executed `return` in that method are not executed.

---

## 🧩 Return Type

The declared return type must match the method's return behavior.

```java
static int add(int a, int b) {
    return a + b;
}
```

For a `void` method:

```java
static void printMessage() {
    System.out.println("Hello");
    return;
}
```

The explicit `return;` is optional at the end of a `void` method.

---

## 🆚 break vs continue vs return

| Statement | Effect |
|---|---|
| `break` | Exits nearest applicable loop or switch |
| `continue` | Skips current loop iteration |
| `return` | Exits current method |

Example mental model:

```text
break     → STOP THE LOOP/SWITCH
continue  → SKIP THIS ITERATION
return    → LEAVE THE METHOD
```

---

## 🎤 Interview Quick Check

**Q1. Can `return` return a value?**  
A: Yes, from a non-void method.

**Q2. Can a `void` method use `return`?**  
A: Yes, using `return;` without a value.

**Q3. What happens to code after an executed `return`?**  
A: It is not executed because the current method has already ended.

---

## 🔗 Navigation

⬅️ [continue](./03-continue-statement.md)

➡️ [Branching Overview](./01-branching-statements-overview.md)

➡️ [Quick Revision](./05-branching-statements-quick-revision.md)

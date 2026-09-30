# 🔀 Java `switch` Statement

> **Topic 12 • Java Fundamentals**

The `switch` statement selects among multiple possible execution paths based on a selector value.

---

## 📌 Basic Syntax

```java
switch (day) {
    case 1:
        System.out.println("Monday");
        break;

    case 2:
        System.out.println("Tuesday");
        break;

    default:
        System.out.println("Invalid day");
}
```

---

## 🧩 Main Parts

| Part | Purpose |
|---|---|
| `switch` | Starts the selection |
| `case` | Defines a possible matching value |
| `break` | Exits the traditional switch statement |
| `default` | Runs when no case matches |

---

## ⚡ Fall-Through

If a traditional `case` does not end with `break`, execution can continue into the next case.

```java
int day = 1;

switch (day) {
    case 1:
        System.out.println("Monday");
    case 2:
        System.out.println("Tuesday");
        break;
}
```

Output:

```text
Monday
Tuesday
```

This behavior is called **fall-through**.

---

## 🧠 FD-BD Memory Trick

| Letter | Meaning |
|---|---|
| **F** | Fall-through |
| **D** | Default |
| **B** | Break |
| **D** | Decimal |

The final **D** reminds you that traditional `switch` does not support `float` or `double` selector types.

---

## 🔢 Traditional Switch Selector Types

Traditional Java `switch` supports:

- `byte`
- `short`
- `char`
- `int`
- Corresponding wrapper types
- `String`
- `enum`

It does **not** support `float` or `double` as selector types.

### Example

❌ Not valid:

```java
double value = 1.5;

switch (value) {
    // compile-time error
}
```

---

## 🆕 Modern Java Note

Modern Java also provides enhanced `switch` forms, including arrow labels and switch expressions.

Example:

```java
String result = switch (day) {
    case 1 -> "Monday";
    case 2 -> "Tuesday";
    default -> "Invalid day";
};
```

Arrow labels avoid the traditional fall-through behavior between cases.

> The traditional `case ... break` form is still important for understanding existing Java code and interviews.

---

## 🎤 Interview Quick Check

**Q1. What is fall-through?**  
A: In a traditional switch, execution continues into subsequent cases when a matching case does not terminate with `break` or another control-flow statement.

**Q2. What is `default`?**  
A: The branch selected when no case matches.

**Q3. Can `double` be used as a traditional switch selector?**  
A: No.

**Q4. What does `break` do in a traditional switch?**  
A: It terminates the switch statement.

---

## 🔗 Navigation

⬅️ [Nested if](./05-nested-if.md)

➡️ [Quick Revision](./07-conditional-statements-quick-revision.md)

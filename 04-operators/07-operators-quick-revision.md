<a name="top"></a>

# ⚡ Java Operators — Quick Revision

> **Topic 11 • 30-Second Revision**

## 🧠 Master Mnemonic

### **IND-AAB-LURT**

| Letter | Remember |
|---|---|
| **I** | Increment / Decrement |
| **N** | `new` |
| **D** | Dot / member access |
| **A** | Arithmetic |
| **A** | Assignment |
| **B** | Bitwise |
| **L** | Logical |
| **U** | Unary |
| **R** | Relational |
| **T** | Ternary |

> Categories can overlap. For example, `++` is both increment/decrement and unary.

---

## 📌 Operator Cheat Sheet

| Category | Operators |
|---|---|
| Arithmetic | `+ - * / %` |
| Assignment | `= += -= *= /= %=` |
| Increment / Decrement | `++ --` |
| Unary | `+ - ++ -- ! ~` |
| Relational | `== != > < >= <=` |
| Logical | `&& || !` |
| Bitwise | `& | ^ ~` |
| Shift | `<< >> >>>` |
| Ternary | `?:` |
| Object creation | `new` keyword |
| Member access | `.` |

---

## 🔢 Prefix vs Postfix

```text
++a → update first, then use
a++ → use first, then update

--a → update first, then use
a-- → use first, then update
```

---

## 🔀 Logical Operators

```text
&& → AND → both conditions must be true
|| → OR  → at least one condition must be true
!  → NOT → reverses boolean value
```

`&&` and `||` use short-circuit evaluation.

---

## 🧮 Bitwise Operators

```text
&   → AND
|   → OR
^   → XOR
~   → complement
<<  → left shift
>>  → signed right shift
>>> → unsigned right shift
```

### Fast Examples

```text
5 & 3  = 1
5 | 3  = 7
5 ^ 3  = 6
~10    = -11
```

---

## 🔀 Ternary

```text
condition ? valueIfTrue : valueIfFalse
```

Example:

```java
String result = age >= 18 ? "Adult" : "Minor";
```

---

## 🎤 Interview Questions & Answers

> **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Operator?</summary>
<br>

Performs an operation on one or more operands.

</details>

<details>
<summary>Operand?</summary>
<br>

Value/expression acted upon by an operator.

</details>

<details>
<summary>`10 / 3` with ints?</summary>
<br>

`3`.

</details>

<details>
<summary>`++a` vs `a++`?</summary>
<br>

Prefix uses updated value; postfix uses original value in the expression.

</details>

<details>
<summary>`==` vs `.equals()` for objects?</summary>
<br>

`==` compares references; `.equals()` is commonly used for logical/content equality.

</details>

<details>
<summary>`>>` vs `>>>`?</summary>
<br>

Signed right shift vs zero-fill right shift.

</details>

<details>
<summary>Ternary syntax?</summary>
<br>

`condition ? trueValue : falseValue`.

</details>

## 🗺️ Final Memory Map

```text
                    JAVA OPERATORS
                         │
       ┌─────────────────┼─────────────────┐
       │                 │                 │
    Calculate          Compare          Decide
       │                 │                 │
   + - * / %       == != > < >= <=      && || !
       │                 │                 │
    Assign            Bitwise           Ternary
       │                 │                 │
  = += -= *=       & | ^ ~ << >> >>>       ?:
      /= %=
```

---

## 🔗 Navigation

⬅️ [Operators Overview](./01-operators-overview.md)

⬅️ [Arithmetic & Assignment](./02-arithmetic-assignment.md)

⬅️ [Increment, Decrement & Unary](./03-increment-decrement-unary.md)

⬅️ [Relational, Logical & Ternary](./04-relational-logical-ternary.md)

⬅️ [Bitwise Operators](./05-bitwise-operators.md)

⬅️ [new & Dot Operators](./06-new-and-dot-operators.md)

🏠 [Java Notes Home](../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

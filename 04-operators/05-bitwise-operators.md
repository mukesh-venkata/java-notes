<a name="top"></a>

# 🧮 Java Bitwise & Shift Operators

> **Topic 11 • Java Fundamentals**

Bitwise operators work at the level of individual bits. For integer types, they are useful for flags, masks, low-level calculations and performance-sensitive operations.

---

## 🔢 Main Operators

| Operator | Meaning |
|---|---|
| `&` | Bitwise AND |
| `|` | Bitwise OR |
| `^` | Bitwise XOR |
| `~` | Bitwise complement |
| `<<` | Left shift |
| `>>` | Signed right shift |
| `>>>` | Unsigned right shift |

---

## 1️⃣ AND — `&`

A bit is `1` only when both corresponding bits are `1`.

```text
  0101   (5)
& 0011   (3)
------
  0001   (1)
```

```java
5 & 3   // 1
```

---

## 2️⃣ OR — `|`

A bit is `1` when at least one corresponding bit is `1`.

```text
  0101   (5)
| 0011   (3)
------
  0111   (7)
```

```java
5 | 3   // 7
```

---

## 3️⃣ XOR — `^`

A bit is `1` when the corresponding bits are different.

```text
  0101
^ 0011
------
  0110   (6)
```

```java
5 ^ 3   // 6
```

### XOR Memory

```text
Same → 0
Different → 1
```

---

## 4️⃣ NOT / Complement — `~`

Flips every bit.

For signed two's-complement integers:

```text
~n = -(n + 1)
```

Therefore:

```text
~5  = -6
~10 = -11
```

---

## 5️⃣ Left Shift — `<<`

Moves bits to the left and fills the rightmost positions with zeros.

For values where no significant bits are lost:

```text
n << k ≈ n × 2ᵏ
```

Example:

```text
5 << 1 = 10
5 << 2 = 20
```

---

## 6️⃣ Signed Right Shift — `>>`

Shifts bits right while preserving the sign by filling the left side with the sign bit.

For positive values:

```text
20 >> 2 = 5
```

---

## 7️⃣ Unsigned Right Shift — `>>>`

Shifts bits right and fills the left side with zeros.

It is especially important for understanding negative integer values and bit-level operations.

### Example

```java
int x = -8;

System.out.println(x >> 1);   // -4
System.out.println(x >>> 1);  // 2147483644
```

---

## 🧠 Quick Bitwise Map

```text
&    → Both bits must be 1
|    → At least one bit is 1
^    → Different bits become 1
~    → Flip every bit
<<   → Shift left
>>   → Signed shift right
>>>  → Zero-fill shift right
```

---

## 🎤 Interview Quick Check

**Q1. What is `5 & 3`?**  
A: `1`.

**Q2. What is `5 ^ 3`?**  
A: `6`.

**Q3. What is the difference between `>>` and `>>>`?**  
A: `>>` preserves the sign during right shift; `>>>` fills the left side with zeros.

---

## 🔗 Navigation

⬅️ [Relational, Logical & Ternary](./04-relational-logical-ternary.md)

➡️ [new & Dot Operators](./06-new-and-dot-operators.md)

➡️ [Quick Revision](./07-operators-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

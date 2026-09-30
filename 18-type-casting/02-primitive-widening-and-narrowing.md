<a name="top"></a>

# 🔢 2. Primitive Widening & Narrowing

## 🟢 Widening Casting — Implicit

Widening converts a smaller/narrower primitive type to a compatible wider type.

Java can perform this conversion automatically.

### Common Conversion Paths

```text
byte → short → int → long → float → double
```

```text
char → int → long → float → double
```

### Example

```java
char ch = 'A';
int value = ch;

System.out.println(value);
```

Output:

```text
65
```

Another example:

```java
int value = 100;
double result = value;

System.out.println(result); // 100.0
```

### Syntax

```java
largerType variable = smallerTypeValue;
```

## 🔴 Narrowing Casting — Explicit

Narrowing converts a wider type to a narrower type.

Java normally requires an explicit cast.

### Syntax

```java
smallerType variable = (smallerType) largerTypeValue;
```

### Example

```java
int value = 65;
char ch = (char) value;

System.out.println(ch);
```

Output:

```text
A
```

## ⚠️ Possible Data Loss

Narrowing can lose information.

```java
int value = 130;
byte result = (byte) value;

System.out.println(result);
```

The result is affected by the target type's representable range.

So:

> **Widening is generally safer; narrowing requires deliberate conversion and may lose information.**

## 🧠 Widening vs Narrowing

| Feature | Widening | Narrowing |
|---|---|---|
| Direction | Narrower → wider | Wider → narrower |
| Cast required | Usually no | Yes |
| Common use | Safe promotion | Deliberate conversion |
| Data loss | Generally avoided by the conversion | Possible |

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What is widening casting?</summary>
<br>

Converting a narrower primitive type to a wider compatible primitive type, usually automatically.

</details>

<details>
<summary>2. What is narrowing casting?</summary>
<br>

Converting a wider primitive type to a narrower type, generally using an explicit cast.

</details>

<details>
<summary>3. Which one normally happens automatically?</summary>
<br>

Widening primitive conversion normally happens automatically.

</details>

<details>
<summary>4. Why can narrowing cause data loss?</summary>
<br>

The target type may not be able to represent the full range or precision of the source value.

</details>

<details>
<summary>5. Is char convertible to int by widening?</summary>
<br>

Yes. A char value can be widened to int.

</details>
## 🔗 Related Notes

- [Type Casting Overview →](01-type-casting-overview.md)
- [Numeric Literals →](03-numeric-literals-and-casting.md)
- [Reference Casting →](04-reference-upcasting-and-downcasting.md)
- [Quick Revision →](07-type-casting-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

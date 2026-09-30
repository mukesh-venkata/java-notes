<a name="top"></a>

# 🧬 3. Final Class

> **Core idea:** A `final` class cannot be extended by another class.

---

## 🧠 What is a Final Class?

A class declared with `final` cannot be inherited.

### Example

```java
final class Parent {
}

class Child extends Parent {   // ❌ Compilation error
}
```

Java rejects the `extends` relationship because `Parent` is final.

```text
final class Parent
        │
        │ ❌ cannot extend
        ↓
      Child
```

---

## Why Use a Final Class?

A final class is useful when a class should not have subclasses.

It can help prevent:

- 🧬 Further inheritance
- 🔄 Subclass-based modification of behavior
- 🧩 Extension where the class design does not allow it

---

## Examples from Java

Some important Java classes are declared final, including:

- `String`
- `Math`

For example, `String` cannot be extended:

```java
class MyString extends String {   // ❌ Compilation error
}
```

This is because `String` is a final class.

---

## Final Class and Final Method

These two restrictions are related but different.

| Feature | Restriction |
|---|---|
| `final` method | Method cannot be overridden |
| `final` class | Class cannot be extended |

A final class automatically prevents subclasses, so there can be no subclass that overrides its methods.

---

## Can a Final Class Have Methods?

**Yes.**

A final class can contain normal methods.

```java
final class Utility {

    void show() {
        System.out.println("Hello");
    }
}
```

The restriction is on **inheritance**, not on defining methods inside the class.

---

## 🧠 Memory Trick

> **final class = “No child class.”**

Remember the three forms:

```text
final variable → ❌ reassignment
final method   → ❌ overriding
final class    → ❌ inheritance
```

---

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. Can a final class be inherited?</summary>
<br>

No. A final class cannot be extended.

</details>

<details>
<summary>Q2. Can a final class contain methods?</summary>
<br>

Yes. It can contain fields, constructors, methods, and other class members according to normal Java rules.

</details>

<details>
<summary>Q3. Why would a class be declared final?</summary>
<br>

To prevent other classes from extending it.

</details>

<details>
<summary>Q4. What happens if we try to extend a final class?</summary>
<br>

The code fails to compile.

</details>
## ⚡ Quick Revision

```text
final class
     ↓
cannot be extended
     ↓
no subclass
```

---

## 🔗 Related Notes

- [Final Variable →](01-final-keyword-and-final-variable.md)
- [Final Method →](02-final-method.md)
- [Final Keyword Quick Revision →](04-final-keyword-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

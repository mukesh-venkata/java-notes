<a name="top"></a>

# ⚡ 4. Final Keyword — Quick Revision

> **30-second revision:** `final` adds a restriction. The exact restriction depends on whether it is applied to a variable, method, or class.

---

## 🧠 The One-Line Rule

| `final` applied to | What it prevents |
|---|---|
| Variable | Reassignment |
| Method | Overriding |
| Class | Inheritance / extension |

### Memory Trick

> **Variable → Value locked**  
> **Method → Override locked**  
> **Class → Inheritance locked**

---

## 1️⃣ Final Variable

```java
final int age = 27;

age = 30;   // ❌ Compilation error
```

**Remember:** A final variable must be assigned before it is read and cannot be reassigned.

For references, final prevents the reference from pointing to another object; it does not automatically make the object immutable.

---

## 2️⃣ Final Method

```java
class Parent {

    final void display() {
        System.out.println("Parent");
    }
}

class Child extends Parent {

    // display() cannot be overridden ❌
}
```

**Remember:** Final method → no overriding.

A final method can still be overloaded.

---

## 3️⃣ Final Class

```java
final class Parent {
}

class Child extends Parent {   // ❌ Compilation error
}
```

**Remember:** Final class → no inheritance.

---

## 🔥 Final Keyword Comparison

| Question | Final Variable | Final Method | Final Class |
|---|---|---|---|
| Can it be reassigned? | ❌ | — | — |
| Can it be overridden? | — | ❌ | — |
| Can it be extended? | — | — | ❌ |
| Main purpose | Prevent reassignment | Protect method implementation | Prevent inheritance |

---

## 🔄 `final` vs `finally` vs `finalize()`

These names look similar but mean different things.

| Term | Meaning |
|---|---|
| `final` | Java keyword for restricting reassignment, overriding, or inheritance |
| `finally` | Block associated with exception handling |
| `finalize()` | Old object-cleanup mechanism; deprecated and should not be used for new code |

> **Interview note:** `final`, `finally`, and `finalize()` are different Java concepts.

---

## 🎯 Interview Questions

1. **What is the purpose of `final` in Java?**  
   It restricts reassignment, method overriding, or class inheritance depending on where it is applied.

2. **Can a final variable be initialized later?**  
   Yes, if it is definitely assigned before use and assigned only once.

3. **Can a final method be overloaded?**  
   Yes.

4. **Can a final class be extended?**  
   No.

5. **Does a final reference make an object immutable?**  
   No. It prevents reassignment of the reference.

6. **What is the difference between `final`, `finally`, and `finalize()`?**  
   They are separate Java concepts: a keyword, an exception-handling block, and a deprecated method respectively.

---

## ⚡ 30-Second Recall

```text
             final
               │
      ┌────────┼────────┐
      ↓        ↓        ↓
   variable   method   class
      │        │        │
      ❌       ❌       ❌
 reassign   override  extend
```

> 🔒 **Final = restrict change.**

---

## 🔗 Related OOP Notes

- [Inheritance Basics →](../04-inheritance/01-inheritance-basics.md)
- [Method Overriding →](../../../11-methods/07-method-overriding.md)
- [Final Variable →](01-final-keyword-and-final-variable.md)
- [Final Method →](02-final-method.md)
- [Final Class →](03-final-class.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

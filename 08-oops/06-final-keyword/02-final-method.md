<a name="top"></a>

# 🚫 2. Final Method

> **Core idea:** `final` method cannot be overridden by a child class.

---

## 🧠 What is a Final Method?

A method declared with the `final` keyword cannot be overridden in a subclass.

### Example

```java
class Parent {

    final void display() {
        System.out.println("Parent");
    }
}

class Child extends Parent {

    // void display() { }   // ❌ Cannot override
}
```

The parent method implementation remains the inherited implementation.

```text
Parent
  │
  │ final display()
  ↓
Child
  │
  └── ❌ cannot override display()
```

---

## Why Use a Final Method?

A final method is useful when a class wants to prevent subclasses from replacing a particular method implementation.

Common reasons include:

- 🔒 Preserve a specific implementation
- 🚫 Prevent overriding
- 📐 Protect an important part of a class's behavior

### Example

```java
class Payment {

    final void validatePayment() {
        System.out.println("Validation logic");
    }
}

class OnlinePayment extends Payment {

    // Cannot replace validatePayment()
}
```

The subclass can still inherit and call the method.

---

## Final Method vs Overriding

### Without `final`

```java
class Parent {
    void display() {
        System.out.println("Parent");
    }
}

class Child extends Parent {
    @Override
    void display() {
        System.out.println("Child");
    }
}
```

Overriding is allowed.

### With `final`

```java
class Parent {
    final void display() {
        System.out.println("Parent");
    }
}

class Child extends Parent {
    // ❌ display() cannot be overridden
}
```

---

## ⚠️ Final Does Not Mean “No Other Method”

A subclass can still define a **different method**.

```java
class Parent {
    final void display() {
        System.out.println("Parent");
    }
}

class Child extends Parent {

    void show() {
        System.out.println("Child");
    }
}
```

The restriction applies specifically to overriding the final method.

---

## 🔍 Can a Final Method Be Overloaded?

**Yes.**

Overloading and overriding are different concepts.

```java
class Parent {

    final void display() {
        System.out.println("No arguments");
    }

    void display(int value) {
        System.out.println(value);
    }
}
```

The first method cannot be overridden, but methods can still be overloaded according to normal overloading rules.

---

## 🧠 Memory Trick

> **final method = “same implementation, no replacement by child.”**

---

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. Can a final method be overridden?</summary>
<br>

No. A final method cannot be overridden by a subclass.

</details>

<details>
<summary>Q2. Can a final method be overloaded?</summary>
<br>

Yes. final restricts overriding, not overloading.

</details>

<details>
<summary>Q3. Why use a final method?</summary>
<br>

To prevent subclasses from changing a particular inherited method implementation through overriding.

</details>

<details>
<summary>Q4. Does a final method become inaccessible to a child class?</summary>
<br>

No. It can still be inherited and used, subject to the method's normal access rules.

</details>
## ⚡ Quick Revision

```text
final method
     ↓
cannot be overridden
     ↓
implementation remains protected
```

---

## 🔗 Related Notes

- [Final Variable →](01-final-keyword-and-final-variable.md)
- [Final Class →](03-final-class.md)
- [Final Keyword Quick Revision →](04-final-keyword-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

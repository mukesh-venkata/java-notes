<a name="top"></a>

# 🧬 4. Reference Upcasting & Downcasting

> **Core idea:** Reference casting works with compatible classes/interfaces in a type hierarchy.

## 🟢 Upcasting — Implicit

Upcasting converts a child reference to a parent reference.

```java
class Parent {
    void parentMethod() {
        System.out.println("Parent");
    }
}

class Child extends Parent {
    void childMethod() {
        System.out.println("Child");
    }
}

Parent p = new Child();
```

This is automatic because every `Child` is also a `Parent`.

## 📌 What Can the Parent Reference Access?

Through `p`, members available through the `Parent` type can be accessed:

```java
p.parentMethod();
```

A child-specific method is not directly accessible through the parent reference:

```java
// p.childMethod();  // compilation error
```

This is a reference-type access rule.

## 🔴 Downcasting — Explicit

Downcasting converts a parent reference to a child reference.

```java
Parent p = new Child();
Child c = (Child) p;
```

Now:

```java
c.parentMethod();
c.childMethod();
```

## ⚠️ Runtime Safety

Downcasting is safe only when the actual object is compatible with the target type.

Safe:

```java
Parent p = new Child();
Child c = (Child) p;
```

Unsafe:

```java
Parent p = new Parent();
Child c = (Child) p; // ClassCastException at runtime
```

The important question is:

> **What is the actual object at runtime?**

not merely:

> What is the declared reference type?

## 🔍 Visual

```text
Parent p = new Child();

Reference type        Runtime object
     ↓                     ↓
   Parent  ───────────→   Child
                              ↓
                       (Child) p
                              ↓
                           Child
```

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. Is upcasting automatic?</summary>
<br>

Yes, when the reference types are compatible.

</details>

<details>
<summary>Q2. Is downcasting automatic?</summary>
<br>

No. An explicit cast is required.

</details>

<details>
<summary>Q3. When can downcasting fail?</summary>
<br>

When the runtime object is not compatible with the target child type.

</details>

<details>
<summary>Q4. What exception can occur?</summary>
<br>

ClassCastException.

</details>
## 🔗 Related Notes

- [Type Casting Overview →](01-type-casting-overview.md)
- [Widening & Narrowing →](02-primitive-widening-and-narrowing.md)
- [instanceof & ClassCastException →](05-instanceof-and-classcastexception.md)
- [Comparison →](06-type-casting-comparison.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

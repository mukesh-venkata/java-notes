<a name="top"></a>

# ⚡ `super` Keyword — Quick Revision

> **Topic 24 • 30-Second Revision**

## 🧠 Master Idea

~~~text
super
  ↓
IMMEDIATE PARENT
~~~

## 3 Main Uses

| Usage | Meaning |
|---|---|
| `super()` | Parent constructor |
| `super.method()` | Parent method implementation |
| `super.field` | Parent field |

## 🔗 Constructor

~~~text
new Child()
    ↓
Child constructor
    ↓
super(...)
    ↓
Parent constructor
~~~

Remember:

**Explicit `super(...)` → first statement**

## 🎯 Member Access

~~~text
this.field  → current object's field
super.field → parent field

this.method()  → current-object method
super.method() → parent implementation
~~~

## ⚠️ Important Rules

- `super` refers to the immediate parent.
- It does not directly refer to a grandparent.
- `super()` invokes an applicable parent constructor.
- Explicit `super()` must be first in the constructor.
- Parent constructors are not inherited.
- Private parent members cannot be directly accessed using `super`.

## 🧠 Memory Trick

**this → CURRENT**

**super → PARENT**

## 🎤 Interview Questions & Answers

> **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>What is `super`?</summary>
<br>



</details>

<details>
<summary>What is `super()`?</summary>
<br>



</details>

<details>
<summary>What is `super.method()`?</summary>
<br>



</details>

<details>
<summary>What is `super.field`?</summary>
<br>



</details>

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

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

## 🎤 Interview One-Liners

**What is `super`?**  
A keyword used to access the immediate superclass context.

**What is `super()`?**  
Parent constructor invocation.

**What is `super.method()`?**  
Parent method implementation.

**What is `super.field`?**  
Parent field access.

🏠 [Java Notes Home](../../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

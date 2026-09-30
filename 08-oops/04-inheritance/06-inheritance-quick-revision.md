<a name="top"></a>

# ⚡ Inheritance — Quick Revision

> **Topic 23 • 30-Second Revision**

## 🧠 Master Idea

~~~text
PARENT
   ↓ extends
CHILD
   ↓
Accessible inherited members
   +
Child-specific members
~~~

## 🔑 Core Terms

| Term | Meaning |
|---|---|
| Inheritance | Parent-child class relationship |
| Parent / Superclass | Class being extended |
| Child / Subclass | Class that extends parent |
| `extends` | Class inheritance keyword |
| IS-A | Parent-child relationship |
| `super` | Immediate parent reference/context |

## 🌳 Types

~~~text
Single       A → B
Multilevel   A → B → C
Hierarchical A → B
             A → C
~~~

**Multiple class inheritance:** ❌

**Multiple interfaces:** ✅

## 🔐 Access

- `public` → broadly accessible
- `protected` → same package + permitted subclass access
- package-private → same package
- `private` → declaring class only

**Inheritance does not remove access restrictions.**

## 🔗 `super`

~~~text
super()        → parent constructor
super.field    → parent field
super.method() → parent method implementation
~~~

## 🔄 Overriding

~~~text
Inheritance
    ↓
Method Overriding
    ↓
Parent reference + Child object
    ↓
Runtime dispatch
    ↓
Runtime polymorphism
~~~

## ⚠️ Must Remember

- Constructors are not inherited.
- Private members are not directly accessible in the child.
- Static methods are hidden, not overridden.
- Final instance methods cannot be overridden.
- An explicit `super(...)` constructor invocation must be first.
- An explicit `this(...)` constructor invocation must be first.

## 🎤 Interview One-Liners

**Inheritance?** Child class acquires accessible members from a parent class.

**Keyword?** `extends`.

**Multiple class inheritance?** Not supported in Java.

**Constructors inherited?** No.

**Private members directly accessible?** No.

**`super()`?** Invokes an immediate parent constructor.

**`super.method()`?** Invokes an accessible parent implementation.

🏠 [Java Notes Home](../../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

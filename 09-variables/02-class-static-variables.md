<a name="top"></a>

# 🏛️ Java Class / Static Variables

> **Topic 16 • Variables**

A **static variable** is a field declared with the `static` keyword and associated with the class rather than with an individual object.

---

## 📌 Declaration

```java
class Counter {
    static int count;
}
```

There is class-level state represented by `count`, rather than one independent field value for every object.

---

## 🛠️ Initialization

### At Declaration

```java
static int count = 10;
```

### Using a Static Initializer

```java
static int count;

static {
    count = 10;
}
```

A static initializer runs when the class is initialized.

---

## 📊 Default Value

A static field receives a default value if it is not explicitly initialized.

Examples:

| Type | Default |
|---|---|
| Integer types | `0` |
| `float` / `double` | `0.0` / `0.0d` |
| `boolean` | `false` |
| `char` | `'\\u0000'` |
| Reference | `null` |

---

## 🔑 Accessing a Static Variable

Prefer the class name:

```java
class Counter {
    static int count = 10;
}

System.out.println(Counter.count);
```

Using an object reference to access a static member is legal in Java in many cases, but it is generally clearer to use the class name because the member belongs to the class.

---

## 🧩 Shared Class-Level State

```java
class Counter {
    static int count = 0;

    Counter() {
        count++;
    }
}

Counter a = new Counter();
Counter b = new Counter();

System.out.println(Counter.count); // 2
```

The static field is associated with the class, so both constructor calls update the same class-level variable.

---

## ⚠️ Static Does Not Mean Constant

These are different concepts:

```java
static int count = 10;       // class-level variable; can change

static final int MAX = 100;  // class-level constant
```

`final` is about preventing reassignment of the variable after initialization; `static` is about class-level association.

---

## 🧠 Memory Note

The JVM specification does not require one exact physical memory region for static fields.

For interviews, say:

> **Static fields are associated with the class; exact runtime storage is JVM implementation-dependent.**

---

## 🎤 Interview Quick Check

**Q1. What keyword creates a static variable?**  
A: `static`.

**Q2. Is a static variable tied to each individual object?**  
A: No. It is associated with the class.

**Q3. Does static mean constant?**  
A: No. `final` is used for the no-reassignment property.

---

## 🔗 Navigation

⬅️ [Variables Overview](./01-variables-overview.md)

➡️ [Instance Variables](./03-instance-variables.md)

➡️ [Local Variables](./04-local-variables.md)

➡️ [Quick Revision](./05-variables-comparison-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

<a name="top"></a>

# ⚖️ Java Overriding vs Overloading

> **Topic 18 • Methods**

| Feature | Overloading | Overriding |
|---|---|---|
| Method name | Same | Same |
| Parameters | Different | Same signature |
| Typical relationship | Same class | Parent-child |
| Selection | Compile time | Runtime dynamic dispatch |
| Purpose | Multiple parameter forms | Specialized subclass behavior |

## 🧠 Memory Trick

```text
OVERLOAD  → Change parameter list
OVERRIDE  → Replace inherited behavior
```

## 💻 Examples

### Overloading

```java
void print(int x) { }
void print(String x) { }
```

### Overriding

```java
class Animal {
    void sound() { }
}

class Dog extends Animal {
    @Override
    void sound() { }
}
```

## 🎤 Interview Quick Check

**Main difference?**  
Overloading changes the parameter list; overriding supplies a subclass implementation for an inherited method with the same signature.

## 🔗 Navigation

⬅️ [Overloading](./06-method-overloading.md)

➡️ [Overriding](./07-method-overriding.md)

➡️ [Access & Overriding Rules](./09-method-access-and-overriding-rules.md)

➡️ [Quick Revision](./12-methods-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

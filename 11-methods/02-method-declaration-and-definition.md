<a name="top"></a>

# 📝 Java Method Declaration & Definition

> **Topic 18 • Methods**

A method is described through its declaration-related elements and implemented through its body.

## 📌 Method Declaration

A method declaration specifies information such as:

- Access modifier
- Return type
- Method name
- Parameter list

Example:

```java
public int add(int a, int b)
```

## 🧱 Method Body

The method body is the block inside `{ }`:

```java
{
    return a + b;
}
```

## 🔗 Complete Method

```java
public int add(int a, int b) {
    return a + b;
}
```

For practical Java learning, think:

```text
Method declaration/header + body
              ↓
        Complete method
```

A method invocation is different:

```java
public int add(int a, int b) { return a + b; } // declaration/definition

add(2, 3);                                    // invocation
```

## 🎤 Interview Quick Check

**What is the method body?**  
The block containing the method's executable statements.

**What is a method invocation?**  
A call that requests execution of a method.

## 🔗 Navigation

⬅️ [Methods Overview](./01-methods-overview.md)

➡️ [Method Signature](./03-method-signature.md)

➡️ [Quick Revision](./12-methods-quick-revision.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

<a name="top"></a>

# 🔐 1. Access Modifiers — Overview

> **Core idea:** Access modifiers control where Java classes and members can be accessed.

## Four Access Levels

| Modifier | General accessibility |
|---|---|
| `public` | Everywhere, subject to normal accessibility rules |
| `protected` | Same package + qualifying subclass access across packages |
| Package-private | Same package |
| `private` | Same class |

## Why Use Access Modifiers?

They help with encapsulation, controlled access, hiding implementation details, and designing clear APIs.

### public

```java
public int age;
```

Accessible from any package when the declaring type is accessible.

### protected

```java
protected int age;
```

Accessible in the same package and through qualifying subclass access across packages.

### Package-private

When no modifier is written:

```java
int age;
```

The member is accessible within the same package.

> `default` is commonly used to describe this access level, but it is not the modifier keyword written before a field or method.

### private

```java
private int age;
```

Accessible only inside the declaring class.

## 🧠 Memory Trick

**Public → Everywhere**  
**Protected → Package + Child**  
**Default → Package**  
**Private → Class**

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What are the four access levels?</summary>
<br>

public, protected, package-private, and private.

</details>

<details>
<summary>2. Which is most restrictive?</summary>
<br>

private.

</details>

<details>
<summary>3. What happens when no modifier is specified?</summary>
<br>

The member has package-private access, meaning it is directly accessible within the same package, subject to normal Java rules.

</details>

<details>
<summary>4. Are access modifiers related to encapsulation?</summary>
<br>

Yes. Access control helps restrict direct access to implementation details and supports encapsulation.

</details>
## 🔗 Related Notes

- [public & private →](02-public-and-private.md)
- [protected & default →](03-protected-and-default.md)
- [Accessibility Table →](04-accessibility-table-and-top-level-classes.md)
- [Quick Revision →](05-access-modifiers-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

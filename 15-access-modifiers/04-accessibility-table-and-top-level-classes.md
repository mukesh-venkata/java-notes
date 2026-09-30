<a name="top"></a>

# 📊 4. Accessibility Table & Top-Level Classes

## 📋 Accessibility Table

| Access Modifier | Same Class | Same Package | Subclass (Other Package) | Other-Package Unrelated Class |
|---|---:|---:|---:|---:|
| `public` | ✅ | ✅ | ✅ | ✅ |
| `protected` | ✅ | ✅ | ✅* | ❌ |
| package-private | ✅ | ✅ | ❌ | ❌ |
| `private` | ✅ | ❌ | ❌ | ❌ |

*Cross-package protected access follows Java's special inheritance/access rules.

## 🏛️ Top-Level Classes

A top-level class is declared directly in a compilation unit rather than nested inside another class.

A top-level class can be:

- `public`
- Package-private (no modifier)

### Public

```java
public class Employee {
}
```

### Package-Private

```java
class Employee {
}
```

### Not Allowed

```java
private class Employee { }    // ❌
protected class Employee { }  // ❌
```

`private` and `protected` can be used for nested classes, but not ordinary top-level classes.

## 🎯 Interview Questions

- Broadest access? **public**
- Most restrictive? **private**
- Can a top-level class be private? **No.**
- Can a top-level class be protected? **No.**
- What is the access level when no modifier is written? **Package-private.**

## 🔗 Related Notes

- [Overview →](01-access-modifiers-overview.md)
- [public & private →](02-public-and-private.md)
- [protected & default →](03-protected-and-default.md)
- [Quick Revision →](05-access-modifiers-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

<a name="top"></a>

# 🛡️ 3. protected & Default (Package-Private)

## protected

A `protected` member is accessible:

1. Within the same package
2. In a subclass in another package, subject to Java's protected-access rules

```java
package alpha;

public class Parent {
    protected int age = 27;
}
```

A subclass in another package can access the inherited member through the subclass context.

```java
package beta;

import alpha.Parent;

public class Child extends Parent {
    void show() {
        System.out.println(age);
    }
}
```

> ⚠️ Protected does **not** mean that every unrelated class in another package can access the member.

## Default / Package-Private

When no access modifier is specified, the declaration has package-private access.

```java
class Person {
    int age = 27;
}
```

It is accessible within the same package, but not directly from another package.

### Important

This is not valid:

```java
default int age; // ❌
```

The word **default** describes the access level; it is not the access modifier used for fields or methods.

## 🔍 Comparison

| Access location | protected | Package-private |
|---|---:|---:|
| Same class | ✅ | ✅ |
| Same package | ✅ | ✅ |
| Subclass in another package | ✅* | ❌ |
| Unrelated class in another package | ❌ | ❌ |

*Subject to protected inheritance/access rules.

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Can protected be accessed in the same package?</summary>
<br>

Yes. Protected members are accessible to classes in the same package.

</details>

<details>
<summary>Can a subclass in another package access it?</summary>
<br>

Yes, subject to protected access rules; from another package, access is through inheritance and has additional restrictions.

</details>

<details>
<summary>Can an unrelated class in another package access it directly?</summary>
<br>

No. An unrelated class in another package cannot directly access a protected member.

</details>

<details>
<summary>Is <code>default</code> the access-modifier keyword?</summary>
<br>

No. The access level is commonly called package-private or default access; it is obtained by omitting an access modifier.

</details>
## 🔗 Related Notes

- [Overview →](01-access-modifiers-overview.md)
- [public & private →](02-public-and-private.md)
- [Accessibility Table →](04-accessibility-table-and-top-level-classes.md)
- [Quick Revision →](05-access-modifiers-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

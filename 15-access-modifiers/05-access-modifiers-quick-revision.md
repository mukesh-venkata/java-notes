<a name="top"></a>

# ⚡ 5. Access Modifiers — Quick Revision

> **30-second revision:** Access modifiers control where Java classes and members can be accessed.

## 🧠 Four Access Levels

| Modifier | Same Class | Same Package | Other-Package Subclass | Other-Package Unrelated |
|---|---:|---:|---:|---:|
| `public` | ✅ | ✅ | ✅ | ✅ |
| `protected` | ✅ | ✅ | ✅* | ❌ |
| package-private | ✅ | ✅ | ❌ | ❌ |
| `private` | ✅ | ❌ | ❌ | ❌ |

*Protected access across packages is subject to Java's inheritance/access rules.

## 🔑 Memory Trick

**Public → Everywhere**  
**Protected → Package + Child**  
**Default → Package**  
**Private → Class**

## 🔒 Most Restrictive → Broadest

```text
private
   ↓
package-private
   ↓
protected
   ↓
public
```

## 📌 Important Rules

- `public` has the broadest access.
- `private` is limited to the declaring class.
- No modifier means package-private.
- `protected` allows same-package access and qualifying subclass access across packages.
- `default` is a descriptive term, not the modifier keyword for fields/methods.
- Top-level classes can be `public` or package-private.
- Top-level classes cannot be `private` or `protected`.

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
<summary>3. Can a top-level class be protected?</summary>
<br>

No.

</details>

<details>
<summary>4. Can a top-level class be private?</summary>
<br>

No.

</details>

<details>
<summary>5. Does protected mean every class in another package can access it?</summary>
<br>

No. Cross-package protected access is subject to the protected inheritance/access rules.

</details>

<details>
<summary>6. Is default the access modifier keyword for package-private fields/methods?</summary>
<br>

No. Package-private access is obtained by omitting an access modifier.

</details>
## 🔗 Related Notes

- [Overview →](01-access-modifiers-overview.md)
- [public & private →](02-public-and-private.md)
- [protected & default →](03-protected-and-default.md)
- [Accessibility Table →](04-accessibility-table-and-top-level-classes.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

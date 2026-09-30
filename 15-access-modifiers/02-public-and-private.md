<a name="top"></a>

# 🔓 2. public & private

## public

A `public` member has the broadest access level, provided its declaring type is accessible.

```java
class Person {
    public int age = 27;
}
```

## private

A `private` member is accessible only inside the class that declares it.

```java
class Person {
    private int age = 27;

    void showAge() {
        System.out.println(age);
    }
}
```

Another class cannot directly access `age`.

## 🧩 Encapsulation Example

```java
class BankAccount {
    private double balance;

    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
        }
    }

    public double getBalance() {
        return balance;
    }
}
```

The private state is accessed through controlled public methods.

## 🔍 Comparison

| Access | public | private |
|---|---:|---:|
| Same class | ✅ | ✅ |
| Same package | ✅ | ❌ |
| Subclass in another package | ✅* | ❌ |
| Unrelated class in another package | ✅* | ❌ |

*Normal type accessibility rules also apply.

## 🎯 Interview Questions

- Can another class directly access a private member? **No.**
- Can a subclass directly access a private parent member? **No.**
- Is private commonly used for encapsulation? **Yes.**

## 🔗 Related Notes

- [Overview →](01-access-modifiers-overview.md)
- [protected & default →](03-protected-and-default.md)
- [Accessibility Table →](04-accessibility-table-and-top-level-classes.md)
- [Quick Revision →](05-access-modifiers-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

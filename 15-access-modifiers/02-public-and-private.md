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

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Can another class directly access a private member?</summary>
<br>

No. A private member is directly accessible only within the class that declares it.

</details>

<details>
<summary>Can a subclass directly access a private parent member?</summary>
<br>

No. A subclass does not directly access the parent's private members; it must use accessible methods or other exposed APIs.

</details>

<details>
<summary>Is private commonly used for encapsulation?</summary>
<br>

Yes. Private fields combined with controlled methods are a common way to implement encapsulation.

</details>
## 🔗 Related Notes

- [Overview →](01-access-modifiers-overview.md)
- [protected & default →](03-protected-and-default.md)
- [Accessibility Table →](04-accessibility-table-and-top-level-classes.md)
- [Quick Revision →](05-access-modifiers-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

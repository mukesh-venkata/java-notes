<a name="top"></a>

# 🔐 Access Modifiers & Inheritance

> **Topic 23 • Inheritance**

Inheritance and access control are closely related.

A child class can use an inherited member only when Java's access rules allow that access.

## 1️⃣ Public

A `public` member is accessible wherever the class/member is accessible.

~~~java
class Parent {
    public int value = 10;
}

class Child extends Parent {
    void show() {
        System.out.println(value);
    }
}
~~~

A child can access the public member.

## 2️⃣ Protected

A `protected` member is accessible:

- Within the same package
- In subclasses, subject to Java's protected-access rules

Example:

~~~java
class Parent {
    protected int value = 10;
}

class Child extends Parent {
    void show() {
        System.out.println(value);
    }
}
~~~

A subclass can access the protected member through the inheritance relationship.

## 3️⃣ Default / Package-Private

When no access modifier is written, the member has package-private access.

~~~java
class Parent {
    int value = 10;
}
~~~

It is accessible within the same package, but a subclass in a different package does not gain ordinary direct access merely because it extends the class.

## 4️⃣ Private

A `private` member is accessible only within the class that declares it.

~~~java
class Parent {
    private int value = 10;
}

class Child extends Parent {
    void show() {
        // System.out.println(value); // error
    }
}
~~~

The child cannot directly access `value`.

A parent can provide controlled access:

~~~java
class Parent {
    private int value = 10;

    public int getValue() {
        return value;
    }
}
~~~

Then the child can use:

~~~java
getValue();
~~~

## 5️⃣ Access Comparison

| Modifier | Same Class | Same Package | Child in Other Package | Other Classes |
|---|:---:|:---:|:---:|:---:|
| public | ✅ | ✅ | ✅ | ✅ |
| protected | ✅ | ✅ | ✅* | ❌ outside allowed contexts |
| package-private | ✅ | ✅ | ❌ | ❌ |
| private | ✅ | ❌ | ❌ | ❌ |

* For protected access from a different package, Java applies specific subclass access rules; it is not unrestricted access through any reference.

## 6️⃣ Inheritance Does Not Remove Access Rules

A common beginner mistake is:

> “If Child extends Parent, Child can access everything in Parent.”

That is incorrect.

Inheritance and accessibility are separate concepts.

~~~text
Inheritance relationship
        +
Access modifier rules
        ↓
What Child can directly access
~~~

## 7️⃣ Fields and Methods

A child can use accessible inherited fields and methods.

However, **field access and method overriding are different concepts**.

For example, fields are not overridden in the same way instance methods are. If a parent and child declare fields with the same name, field hiding/shadowing rules apply.

Method overriding has its own rules and is covered separately.

## 8️⃣ Interview Questions

**Q1. Can a child directly access a private parent field?**  
No.

**Q2. Does protected work across packages?**  
Yes, but only under Java's specific protected-access rules for subclasses.

**Q3. Is package-private accessible to a subclass in another package?**  
No.

**Q4. Does inheritance make private members public/protected?**  
No.

➡️ [Inheritance Basics](./01-inheritance-basics.md)
➡️ [super & Constructor Chaining](./04-super-and-constructor-chaining.md)

🏠 [Java Notes Home](../../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)## 🎤 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. Can a child directly access a private parent field?</summary>
<br>

No. A private member is directly accessible only within the class that declares it.

</details>

<details>
<summary>Q2. Does protected work across packages?</summary>
<br>

Yes, but only under Java's specific protected-access rules for subclasses; it is not unrestricted access through any reference.

</details>

<details>
<summary>Q3. Is package-private accessible to a subclass in another package?</summary>
<br>

No. Package-private access is limited to the same package.

</details>

<details>
<summary>Q4. Does inheritance make private members public or protected?</summary>
<br>

No. Inheritance does not change the access modifier of a private member.

</details>
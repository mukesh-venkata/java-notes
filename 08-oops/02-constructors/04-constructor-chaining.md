<a name="top"></a>

# 🔗 Constructor Chaining

> **Topic 21 • Constructors**

**Constructor chaining** means one constructor invokes another constructor as part of object construction.

Java provides two important constructor-invocation forms:

- `this()` → another constructor in the **same class**
- `super()` → a constructor in the **parent class**

---

# 1️⃣ this() — Same-Class Constructor

Use `this()` to invoke another constructor in the same class.

```java
class Student {

    Student() {
        this(20);
        System.out.println("No-arg constructor");
    }

    Student(int age) {
        System.out.println(age);
    }
}
```

When:

```java
new Student();
```

the flow is:

```text
Student()
   ↓
this(20)
   ↓
Student(int)
   ↓
returns to Student()
```

This avoids duplicating initialization logic.

## 2️⃣ this() Must Be First

If you explicitly use `this()` in a constructor, it must be the **first statement**.

✅ Correct:

```java
Student() {
    this(20);
    System.out.println("Constructor");
}
```

❌ Incorrect:

```java
Student() {
    System.out.println("Before");
    this(20);
}
```

The second example does not compile.

---

# 3️⃣ super() — Parent Constructor

Use `super()` to invoke a constructor of the parent class.

```java
class Parent {

    Parent() {
        System.out.println("Parent constructor");
    }
}

class Child extends Parent {

    Child() {
        super();
        System.out.println("Child constructor");
    }
}
```

Creating:

```java
new Child();
```

gives the conceptual flow:

```text
Child()
   ↓
super()
   ↓
Parent()
   ↓
returns to Child()
```

## 4️⃣ super() Must Be First

If explicitly written, `super()` must also be the first statement in the constructor.

✅ Correct:

```java
Child() {
    super();
    System.out.println("Child");
}
```

❌ Incorrect:

```java
Child() {
    System.out.println("Before");
    super();
}
```

---

# 5️⃣ Implicit super()

If a constructor does not explicitly begin with a constructor-invocation statement, Java inserts an implicit `super()` when applicable.

Example:

```java
class Parent {
    Parent() {
        System.out.println("Parent");
    }
}

class Child extends Parent {
    Child() {
        System.out.println("Child");
    }
}
```

Conceptually, the child constructor behaves as though:

```java
Child() {
    super();
    System.out.println("Child");
}
```

This works only when the parent has an accessible no-argument constructor.

If the parent has only:

```java
Parent(int x) {
}
```

then the child must explicitly invoke an applicable parent constructor, for example:

```java
Child() {
    super(10);
}
```

---

# 6️⃣ this() and super() Cannot Both Be First

A constructor can explicitly start with either `this(...)` or `super(...)`, but not both.

❌ Invalid:

```java
Student() {
    this(20);
    super();
}
```

Why?

Because both are constructor-invocation statements and one constructor can have only one such first statement.

The chain can still eventually reach a parent constructor:

```text
Child()
  ↓
this(...)
  ↓
another Child constructor
  ↓
super(...)
  ↓
Parent constructor
```

---

# 7️⃣ Constructor Chaining Example

```java
class Student {

    String name;
    int age;

    Student() {
        this("Unknown", 0);
    }

    Student(String name) {
        this(name, 0);
    }

    Student(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
```

Now:

```java
new Student();
```

follows:

```text
Student()
   ↓
this("Unknown", 0)
   ↓
Student(String, int)
   ↓
fields initialized
```

This keeps the actual initialization logic in one place.

---

# 8️⃣ Constructor Chaining With Inheritance

Consider:

```java
class Parent {

    Parent(int value) {
        System.out.println("Parent: " + value);
    }
}

class Child extends Parent {

    Child() {
        super(10);
        System.out.println("Child");
    }
}
```

Flow:

```text
new Child()
    ↓
Child()
    ↓
super(10)
    ↓
Parent(int)
    ↓
Child constructor body
```

This is constructor chaining across an inheritance relationship.

---

# 9️⃣ Why Use Constructor Chaining?

Constructor chaining helps:

- Reuse initialization logic
- Avoid duplicated code
- Centralize object initialization
- Maintain consistent construction rules
- Connect child construction with parent construction

## 🧠 Memory Trick

**this() → SAME CLASS**

**super() → PARENT CLASS**

**FIRST STATEMENT → ALWAYS**

## 🎤 Interview Questions

**Q1. What is constructor chaining?**  
Invoking one constructor from another during object construction.

**Q2. What does `this()` do?**  
Invokes another constructor in the same class.

**Q3. What does `super()` do?**  
Invokes a constructor of the parent class.

**Q4. Where must `this()` or `super()` appear?**  
If explicitly used, it must be the first statement in the constructor.

**Q5. Can a constructor directly call both `this()` and `super()`?**  
No. It can explicitly start with only one constructor-invocation statement.

**Q6. What happens if the parent has no accessible no-argument constructor?**  
A child constructor cannot rely on an implicit `super()`; it must invoke an applicable parent constructor explicitly.

➡️ [Constructor Basics](./01-constructor-basics.md)  
➡️ [Constructor Overloading](./03-constructor-overloading.md)  
➡️ [Quick Revision](./05-constructors-quick-revision.md)

🏠 [Java Notes Home](../../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

# 🔗 `this()` and `this.method()`

> **Topic 22 • `this` Keyword**

Two important uses of `this` are related to calling members of the current class:

- `this()` → another constructor in the **same class**
- `this.methodName()` → an instance method on the **current object**

## 1️⃣ `this()` — Constructor Chaining

~~~java
class Student {
    Student() {
        this("Mukesh");
    }

    Student(String name) {
        System.out.println("Name: " + name);
    }
}
~~~

Flow:

~~~text
Student()
   ↓
this("Mukesh")
   ↓
Student(String)
   ↓
returns to Student()
~~~

## 2️⃣ First-Statement Rule

If explicitly used, `this()` must be the **first statement** in a constructor.

Correct:

~~~java
Student() {
    this("Mukesh");
    System.out.println("Done");
}
~~~

Incorrect:

~~~java
Student() {
    System.out.println("Before");
    this("Mukesh");
}
~~~

The second example does not compile.

A constructor cannot explicitly use both `this(...)` and `super(...)` because only one constructor-invocation statement can occupy the first position.

## 3️⃣ `this.method()`

~~~java
class Student {
    void display() {
        this.show();
    }

    void show() {
        System.out.println("Hello");
    }
}
~~~

`this.show()` means:

> Invoke `show()` on the current object.

## 4️⃣ Can `this` Be Omitted?

Yes, when there is no ambiguity:

~~~java
this.show();
~~~

and:

~~~java
show();
~~~

have the same intended receiver in this instance context.

## 5️⃣ Execution Flow

For `s.display()`:

~~~text
s.display()
     ↓
display()
     ↓
this.show()
     ↓
show() executes on s
     ↓
returns to display()
~~~

## 6️⃣ Comparison

| Form | Meaning |
|---|---|
| `this()` | Same-class constructor |
| `this(arg)` | Overloaded same-class constructor |
| `this.method()` | Current object's instance method |
| `method()` | Usually equivalent to `this.method()` in instance context |

## 🧠 Memory Trick

**Parentheses after `this` → constructor**

**Dot after `this` → member access**

## 🎤 Interview Questions

**Q1. What does `this()` do?**  
Invokes another constructor in the same class.

**Q2. Where must `this()` appear?**  
As the first statement when explicitly used in a constructor.

**Q3. What does `this.show()` do?**  
Calls `show()` on the current object.

**Q4. Can `this()` be used inside a normal method?**  
No. It is constructor-invocation syntax.

➡️ [Constructor Chaining](../02-constructors/04-constructor-chaining.md)
➡️ [Pass & Return `this`](./04-this-as-argument-and-return-value.md)

🏠 [Java Notes Home](../../README.md)

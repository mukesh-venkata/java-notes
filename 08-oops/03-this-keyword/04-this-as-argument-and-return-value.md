<a name="top"></a>

# 🔄 Passing and Returning `this`

> **Topic 22 • `this` Keyword**

Because `this` represents the current object, it can be used wherever an object reference is expected.

## 1️⃣ Passing `this` as an Argument

~~~java
class Student {
    void display() {
        show(this);
    }

    void show(Student s) {
        System.out.println("Received current object");
    }
}
~~~

Here `show(this)` passes the current `Student` object.

~~~text
current object
      ↓
     this
      ↓
show(this)
      ↓
parameter s refers to that object
~~~

## 2️⃣ Why Pass `this`?

It is useful when another method or object needs a reference to the current object.

~~~java
class Student {
    void register() {
        Registry.add(this);
    }
}

class Registry {
    static void add(Student student) {
        // student refers to the passed Student object
    }
}
~~~

## 3️⃣ Returning `this`

A method can return the current object:

~~~java
class Student {
    Student getObject() {
        return this;
    }
}
~~~

If:

~~~java
Student s = new Student();
Student result = s.getObject();
~~~

then `result` refers to the same object as `s`.

## 4️⃣ Method Chaining

Returning `this` is commonly used in fluent APIs.

~~~java
class Student {
    String name;
    int age;

    Student setName(String name) {
        this.name = name;
        return this;
    }

    Student setAge(int age) {
        this.age = age;
        return this;
    }
}
~~~

Now:

~~~java
Student s = new Student()
        .setName("Mukesh")
        .setAge(27);
~~~

Conceptually:

~~~text
new Student()
     ↓
setName()
     ↓ return this
same object
     ↓
setAge()
     ↓ return this
same object
~~~

## 5️⃣ Important Reference Concept

Passing or returning `this` does **not** create a new object.

~~~text
show(this)  → passes current object's reference
return this → returns current object's reference
~~~

## 6️⃣ Comparison

| Use | Meaning |
|---|---|
| `show(this)` | Pass current object reference |
| `return this` | Return current object reference |

## 🧠 Memory Trick

**PASS → current object goes out**

**RETURN → current object comes back**

## 🎤 Interview Questions

**Q1. Can `this` be passed as an argument?**  
Yes, when the parameter type is compatible.

**Q2. Does passing `this` create a new object?**  
No.

**Q3. Why return `this`?**  
To return the current object and, commonly, support method chaining.

**Q4. What is fluent method chaining?**  
A style where methods return an object, often `this`, allowing consecutive method calls.

➡️ [`this` Basics](./01-this-keyword-basics.md)
➡️ [Quick Revision](./05-this-keyword-quick-revision.md)

🏠 [Java Notes Home](../../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

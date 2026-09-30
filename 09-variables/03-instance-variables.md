# 🧱 Java Instance Variables

> **Topic 16 • Variables**

An **instance variable** is a field declared inside a class but outside methods, constructors and initializer blocks.

Each object has its own instance state.

---

## 📌 Declaration

```java
class Student {
    int age;
}
```

Here, `age` is an instance variable.

---

## 🧩 One Copy per Object

```java
class Student {
    String name;
    int age;
}

Student s1 = new Student();
Student s2 = new Student();

s1.age = 20;
s2.age = 25;
```

Conceptually:

```text
Student object 1
    age → 20

Student object 2
    age → 25
```

The objects maintain separate instance state.

---

## 🛠️ Initialization

### 1. At Declaration

```java
int age = 20;
```

### 2. Through a Constructor

```java
class Student {
    int age;

    Student(int age) {
        this.age = age;
    }
}
```

### 3. Through an Object Reference

```java
Student s = new Student();
s.age = 20;
```

---

## 📊 Default Value

Instance fields receive default values when no explicit initializer supplies a value.

```java
class Student {
    int age;
    boolean active;
    String name;
}
```

Conceptually:

```text
age    → 0
active → false
name   → null
```

---

## 🔑 Accessing an Instance Variable

Usually through an object reference:

```java
Student s = new Student();
s.age = 20;

System.out.println(s.age);
```

Inside an instance method, the field can also be accessed directly:

```java
class Student {
    int age;

    void display() {
        System.out.println(age);
    }
}
```

---

## 🗄️ Memory Note

An instance field is part of an object.

In common JVM implementations, objects are generally allocated in the heap, but the exact memory layout and optimizations are implementation-dependent.

---

## 🆚 Instance vs Static

| Feature | Instance | Static |
|---|---|---|
| Associated with | Object | Class |
| State | Per object | Class-level |
| Typical access | `object.field` | `Class.field` |
| Number of independent values | One per object | Shared class-level state |

---

## 🎤 Interview Quick Check

**Q1. Where is an instance variable declared?**  
A: Inside a class, outside methods, constructors and initializer blocks.

**Q2. Does each object have independent instance state?**  
A: Yes.

**Q3. Do instance fields receive default values?**  
A: Yes.

---

## 🔗 Navigation

⬅️ [Static Variables](./02-class-static-variables.md)

➡️ [Local Variables](./04-local-variables.md)

➡️ [Quick Revision](./05-variables-comparison-quick-revision.md)

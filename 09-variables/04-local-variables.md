# 📍 Java Local Variables

> **Topic 16 • Variables**

A **local variable** is declared inside a method, constructor, or block and is accessible only within its applicable scope.

---

## 📌 Example

```java
void display() {
    int age = 20;
    System.out.println(age);
}
```

Here, `age` is a local variable.

---

## 📍 Where Can Local Variables Be Declared?

### Inside a Method

```java
void display() {
    int age = 20;
}
```

### Inside a Constructor

```java
Student(int age) {
    int adjustedAge = age + 1;
}
```

### Inside a Block

```java
if (true) {
    int x = 10;
    System.out.println(x);
}
```

---

## ⚠️ No Automatic Default Value

This does **not** compile:

```java
int age;
System.out.println(age); // compile-time error
```

The compiler requires a local variable to be **definitely assigned** before it is read.

Correct:

```java
int age = 20;
System.out.println(age);
```

---

## 🎯 Scope

A local variable is accessible only within the scope where it is declared.

```java
if (true) {
    int x = 10;
    System.out.println(x); // valid
}

System.out.println(x); // compile-time error
```

---

## 🧠 Lifetime

A local variable is associated with the execution of its method, constructor or block.

Its practical storage is a JVM implementation detail. A common interview simplification is to associate locals with a stack frame, but modern JVMs may optimize representations.

---

## 🆚 Local vs Fields

| Feature | Local variable | Field |
|---|---|---|
| Declared | Method/constructor/block | Class body |
| Default value | No | Yes |
| Scope | Local | Depends on access modifier and object/class |
| State | Temporary execution state | Object/class state |

---

## 🎤 Interview Quick Check

**Q1. Do local variables get default values?**  
A: No.

**Q2. What happens if an uninitialized local variable is read?**  
A: The code fails to compile because the variable is not definitely assigned.

**Q3. Where is a local variable accessible?**  
A: Within its applicable lexical scope.

---

## 🔗 Navigation

⬅️ [Instance Variables](./03-instance-variables.md)

➡️ [Comparison & Quick Revision](./05-variables-comparison-quick-revision.md)

🏠 [Java Notes Home](../README.md)

<a name="top"></a>

# 📞 Java Method Execution

> **Topic 12 • Method Execution**

A method call is more than simply “jumping” to another method. During an invocation, the JVM keeps track of the current execution, creates runtime data for the new invocation, executes the method, and then returns control to the caller.

## 1️⃣ What Happens When a Method Is Called?

Consider:

```java
class Demo {
    public static void main(String[] args) {
        add();
        System.out.println("Back in main");
    }

    static void add() {
        int a = 10;
        int b = 20;
        int sum = a + b;
        System.out.println(sum);
    }
}
```

The conceptual flow is:

```text
main()
   ↓
calls add()
   ↓
add() invocation starts
   ↓
runtime frame for add() is created
   ↓
add() executes
   ↓
add() completes
   ↓
add() frame is discarded
   ↓
main() continues
```

## 2️⃣ Method Invocation

A **method invocation** means requesting a method to execute.

```java
add();
```

For a method with parameters:

```java
int result = add(10, 20);
```

The arguments are supplied to the invocation and are available as parameters during that method execution.

## 3️⃣ Method Invocation and Stack Frame

When a method is invoked, the runtime needs information associated with that particular invocation.

That information is represented conceptually by a **stack frame**.

```text
Method call
    ↓
New invocation
    ↓
Conceptual stack frame
    ↓
Method execution
```

A detailed explanation of frames is in **[Stack Frame](./02-stack-frame.md)**.

## 4️⃣ Example With a Return Value

```java
class Calculator {

    static int add(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        int result = add(10, 20);
        System.out.println(result);
    }
}
```

Conceptually:

```text
main()
  ↓
add(10, 20)
  ↓
a = 10, b = 20
  ↓
a + b = 30
  ↓
return 30
  ↓
main() receives 30
```

The caller can then continue executing with the returned value.

## 5️⃣ What Happens When a Method Returns?

For a normal return:

1. The method invocation completes.
2. Its runtime frame is no longer needed.
3. Control returns to the calling method.
4. A return value is available to the caller if the method has one.
5. The caller continues from the point after the invocation.

A method can also complete **abruptly**, for example because an exception is thrown. In that case, normal return to the immediate caller does not necessarily happen.

## 6️⃣ Method Call vs Method Definition

Do not confuse these two:

| Concept | Example | Meaning |
|---|---|---|
| Method definition | `static int add(int a, int b) { ... }` | Describes what the method does |
| Method invocation | `add(10, 20)` | Requests the method to execute |

## 7️⃣ Important Idea

Every active method invocation needs its own execution context.

For example:

```text
main()
  ↓
methodA()
  ↓
methodB()
```

At this moment, all three invocations are active. Their frames form part of the current call chain.

This leads naturally to the ideas of the **Java Stack** and **Call Stack**.

➡️ **[Stack Frame](./02-stack-frame.md)**  
➡️ **[Java Stack & Call Stack](./03-java-stack-and-call-stack.md)**

## 🧠 Memory Trick

**CALL → FRAME → EXECUTE → RETURN → CONTINUE**

## 🎤 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What happens when a method is invoked?</summary>
<br>

A new method invocation becomes active and the runtime creates the information needed to execute it, conceptually represented by a stack frame.

</details>

<details>
<summary>Q2. What happens after a method returns normally?</summary>
<br>

Its invocation completes, its frame is discarded, and control returns to the caller.

</details>

<details>
<summary>Q3. Is a method call the same as a method definition?</summary>
<br>

No. A definition describes the method; an invocation executes it.

</details>
## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

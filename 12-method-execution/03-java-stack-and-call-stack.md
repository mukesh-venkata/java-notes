<a name="top"></a>

# 🧵 Java Stack, Call Stack & Recursion

> **Topic 12 • Method Execution**

The **JVM stack**, **call stack**, and **recursion** are closely connected.

- **JVM Stack** → a stack associated with a thread.
- **Call Stack** → the active chain of method invocations represented through stack frames.
- **Recursion** → a method directly or indirectly calls itself, creating multiple active invocations.

## 1️⃣ Java / JVM Stack

Each thread has its own JVM stack.

```text
Thread
  ↓
JVM Stack
  ├── main() frame
  ├── methodA() frame
  └── methodB() frame
```

The stack is therefore associated with the execution of one thread.

## 2️⃣ What Is a Call Stack?

Suppose execution reaches:

```text
main()
   ↓
methodA()
   ↓
methodB()
   ↓
methodC()
```

The active calls can be visualized as:

```text
┌─────────────────────┐
│ methodC()           │ ← current call
├─────────────────────┤
│ methodB()           │
├─────────────────────┤
│ methodA()           │
├─────────────────────┤
│ main()              │
└─────────────────────┘
```

The call stack represents the current chain of active method invocations.

## 3️⃣ Why LIFO?

Method calls naturally follow **Last In, First Out** behavior.

```text
main()
  ↓
A()
  ↓
B()

B() finishes first
  ↓
A() continues
  ↓
main() continues
```

The most recently active call normally returns before the calls beneath it.

## 4️⃣ Example

```java
class Demo {

    static void methodC() {
        System.out.println("C");
    }

    static void methodB() {
        methodC();
        System.out.println("B");
    }

    static void methodA() {
        methodB();
        System.out.println("A");
    }

    public static void main(String[] args) {
        methodA();
        System.out.println("main");
    }
}
```

Conceptual execution:

```text
main
 ↓
A
 ↓
B
 ↓
C
 ↑
B continues
 ↑
A continues
 ↑
main continues
```

## 5️⃣ Call Stack and Stack Frames

The call stack is not a completely separate memory area.

It is a useful way to describe the currently active method-call chain using the frames associated with a thread's JVM stack.

```text
Thread
  ↓
JVM Stack
  ↓
Active Stack Frames
  ↓
Current Call Chain
```

## 6️⃣ Stack Trace

When an exception occurs, Java can print a **stack trace**.

A simplified chain might look like:

```text
main()
  ↓
service()
  ↓
repository()
  ↓
databaseCall()
```

This helps you understand which method calls were active when execution reached the failure.

## 7️⃣ Recursion

**Recursion** means a method directly or indirectly calls itself.

```java
static void countDown(int n) {

    if (n == 0) {
        return;
    }

    System.out.println(n);
    countDown(n - 1);
}
```

For `countDown(3)`:

```text
countDown(3)
      ↓
countDown(2)
      ↓
countDown(1)
      ↓
countDown(0)
      ↓
return
```

Each active recursive invocation has its own invocation state/frame.

## 8️⃣ Base Condition

A recursive method needs a condition that stops further recursive calls.

```java
if (n == 0) {
    return;
}
```

This is the **base condition**.

Without it, recursive calls may continue until the thread can no longer support more active stack frames.

## 9️⃣ Stack Unwinding

After the base condition is reached, active recursive calls return one by one.

```text
countDown(3)
      ↓
countDown(2)
      ↓
countDown(1)
      ↓
countDown(0)
      ↑
return
      ↑
return
      ↑
return
      ↑
return
```

This returning phase is commonly called **stack unwinding**.

## 🔟 Recursion With a Return Value

```java
static int factorial(int n) {

    if (n == 1) {
        return 1;
    }

    return n * factorial(n - 1);
}
```

For `factorial(4)`:

```text
factorial(4)
  ↓
4 × factorial(3)
  ↓
3 × factorial(2)
  ↓
2 × factorial(1)
  ↓
1
```

Then the results are resolved while calls return:

```text
1
↑
2 × 1 = 2
↑
3 × 2 = 6
↑
4 × 6 = 24
```

## 1️⃣1️⃣ StackOverflowError

Uncontrolled recursion can create too many active invocations.

```java
static void infinite() {
    infinite();
}
```

There is no stopping condition, so calls keep accumulating.

This can result in:

```text
java.lang.StackOverflowError
```

The exact limit depends on the runtime environment.

## 1️⃣2️⃣ Recursion vs Loop

| Recursion | Loop |
|---|---|
| Method calls itself | Repeats using loop syntax |
| Creates additional active invocations | Usually reuses the current method invocation |
| Useful for naturally recursive problems | Often simpler for straightforward repetition |
| Needs a valid stopping condition | Needs a valid loop condition |

## 🧠 Memory Tricks

**THREAD → JVM STACK → FRAMES → CALL CHAIN**

For recursion:

**RECURSE → MORE FRAMES → BASE CASE → UNWIND**

## 🎤 Interview Questions

**Q1. Does each thread have its own JVM stack?**  
Yes.

**Q2. What is a call stack?**  
The currently active chain of method invocations.

**Q3. Why is method execution described as LIFO?**  
Because the most recently active call normally completes and returns before the calls beneath it.

**Q4. Why does recursion use the stack?**  
Each active recursive invocation needs its own invocation state/frame.

**Q5. What is stack unwinding?**  
Active recursive calls return one by one after the base condition is reached.

**Q6. What can uncontrolled recursion cause?**  
It can exhaust stack space and result in StackOverflowError.

➡️ [Method Execution Quick Revision](./04-method-execution-quick-revision.md)

🏠 [Java Notes Home](../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

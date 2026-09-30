# 🧵 Java Stack, Call Stack & Recursion

> **Topic 19 • Method Execution**

## 1️⃣ Java Stack

Each thread has its own **JVM stack**. Active method invocations on that thread use stack frames associated with that stack.

~~~text
Thread
  ↓
JVM Stack
  ├── frame for main()
  ├── frame for methodA()
  └── frame for methodB()
~~~

This is why the stack is useful for understanding which methods are currently active.

## 2️⃣ What Is a Call Stack?

Suppose the program reaches:

~~~text
main()
   ↓
methodA()
   ↓
methodB()
   ↓
methodC()
~~~

The active calls can be visualized as:

~~~text
┌───────────────┐
│ methodC()     │ ← current call
├───────────────┤
│ methodB()     │
├───────────────┤
│ methodA()     │
├───────────────┤
│ main()        │
└───────────────┘
~~~

When methodC() finishes, its frame is discarded and execution continues in methodB().

## 3️⃣ Why Is This LIFO?

Method calls follow a **Last In, First Out** pattern.

~~~text
main → A → B

B finishes first
↓
A continues
↓
main continues
~~~

The most recently active method returns first.

## 4️⃣ Recursion

Recursion means a method calls itself.

~~~java
static void countDown(int n) {
    if (n == 0) {
        return;
    }

    System.out.println(n);
    countDown(n - 1);
}
~~~

For countDown(3):

~~~text
countDown(3)
      ↓
countDown(2)
      ↓
countDown(1)
      ↓
countDown(0)
      ↓
return
~~~

Each active recursive invocation has its own stack frame.

If recursive calls continue without reaching a proper stopping condition, too many active frames can exhaust stack space and result in StackOverflowError.

## 5️⃣ Connection to Debugging

A Java exception stack trace often shows the chain of method calls that led to the problem.

~~~text
main()
  ↓
service()
  ↓
repository()
  ↓
databaseCall()
~~~

Understanding the call stack makes stack traces much easier to read.

## 🧠 Easy Memory Trick

**Thread → Java Stack → Method Calls → Stack Frames**

## 🎤 Interview Questions

**Does every thread have its own JVM stack?**  
Yes.

**What is a call stack?**  
The active chain of method invocations, represented conceptually by stack frames.

**Why can recursion cause StackOverflowError?**  
Too many recursive invocations can remain active and exhaust available stack space.

**Why is this useful in debugging?**  
It helps you understand stack traces and the sequence of method calls.

⬅️ [Method Execution](./01-method-execution.md)  
➡️ [Quick Revision](./03-method-execution-quick-revision.md)

🏠 [Java Notes Home](../README.md)
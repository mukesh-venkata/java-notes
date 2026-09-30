# 🧵 Java Stack

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


## 🧠 Remember

**One Thread → One JVM Stack → Active Method Frames**

➡️ [Call Stack](./05-call-stack.md)

🏠 [Java Notes Home](../README.md)
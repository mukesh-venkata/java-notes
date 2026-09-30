# 📚 Java Call Stack

> **Topic 19 • Method Execution**

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

**Last method called → First method to return**

➡️ [Recursion & Stack](./06-recursion-and-stack.md)

🏠 [Java Notes Home](../README.md)
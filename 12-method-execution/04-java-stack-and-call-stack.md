# 🧵 Java Stack & Call Stack

> **Topic 19 • Method Execution**

Each thread has its own **JVM stack**. Active method calls are represented by stack frames.

## Simple Example

~~~text
main()
  ↓
methodA()
  ↓
methodB()
~~~

Think of the active calls as:

~~~text
┌─────────────┐
│ methodB()   │ ← current call
├─────────────┤
│ methodA()   │
├─────────────┤
│ main()      │
└─────────────┘
~~~

When methodB finishes, control returns to methodA.

## 🔁 Recursion

~~~text
factorial(4)
factorial(3)
factorial(2)
factorial(1)
~~~

Each active call has its own frame. Too many active calls can cause **StackOverflowError**.

### 🧠 Easy Trick

**Java Stack → Method Calls → Stack Frames**

⬅️ [Method Call](./01-method-call-and-stack-frame.md)  
➡️ [Quick Revision](./05-method-execution-quick-revision.md)
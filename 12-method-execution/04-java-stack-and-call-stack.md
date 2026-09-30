# 🧵 Java Stack & Call Stack

> **Topic 19 • Method Execution**

Each thread has its own **JVM stack**. Method invocations on that thread create frames associated with that stack.

## 🧵 One Thread → One JVM Stack

```text
Thread A
   ↓
JVM Stack A
   ├── frame
   ├── frame
   └── frame

Thread B
   ↓
JVM Stack B
   ├── frame
   └── frame
```

## 📚 Call Stack Example

Suppose:

```text
main()
  → methodA()
      → methodB()
          → methodC()
```

The active call path can be visualized as:

```text
┌──────────────┐
│ methodC()    │ ← most recent active call
├──────────────┤
│ methodB()    │
├──────────────┤
│ methodA()    │
├──────────────┤
│ main()       │
└──────────────┘
```

When `methodC()` returns, its frame is discarded and execution continues in `methodB()`.

## 🔁 Recursion Connection

For recursion:

```text
factorial(4)
factorial(3)
factorial(2)
factorial(1)
```

Each active invocation has its own frame.

If execution keeps creating frames without returning, the JVM can eventually throw `StackOverflowError`.

## ⚠️ JVM Specification vs Implementation

The JVM Specification defines a JVM stack for each thread and specifies frame behavior. Physical implementations can differ because JVMs may optimize execution, including through JIT compilation.

> **Java Stack is a JVM runtime concept; do not assume a single universal physical memory layout.**

## 🎤 Interview Quick Check

**Does every thread have its own JVM stack?**  
Yes.

**What is a call stack?**  
The active chain of method invocations, represented conceptually by stack frames.

**Why can recursion cause StackOverflowError?**  
Too many active recursive invocations can exhaust available stack space.

## 🔗 Navigation

⬅️ [Method Call](./01-method-call-and-stack-frame.md)  
➡️ [Stack Frame](./02-stack-frame.md)  
➡️ [Execution Flow](./03-method-execution-flow.md)  
➡️ [Quick Revision](./05-method-execution-quick-revision.md)

🏠 [Java Notes Home](../README.md)

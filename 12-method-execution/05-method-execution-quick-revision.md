# ⚡ Java Method Execution — Quick Revision

> **Topic 19 • 30-Second Revision**

## 🧠 Master Flow

```text
             METHOD CALL
                  ↓
          STACK FRAME CREATED
                  ↓
           FRAME BECOMES ACTIVE
                  ↓
            METHOD EXECUTES
                  ↓
           METHOD COMPLETES
                  ↓
            FRAME DISCARDED
                  ↓
          CONTROL → CALLER
```

## 📦 Stack Frame

Conceptually includes:

- Local variable array
- Operand stack
- Reference to the runtime constant pool

Implementation details may vary.

## 🧵 JVM Stack

```text
Each Thread
     ↓
Private JVM Stack
     ↓
Method invocations
     ↓
Stack frames
```

## 🔁 Recursion

```text
Recursive call
      ↓
New active invocation
      ↓
New frame
      ↓
Base case
      ↓
Frames return / discard
```

## 🎯 Interview One-Liners

**What is a stack frame?**  
Runtime data associated with one method invocation.

**When is it created?**  
When the method is invoked.

**When is it discarded?**  
When that invocation completes.

**Does each thread have its own JVM stack?**  
Yes.

**What is the operand stack?**  
A stack used by JVM bytecode instructions for intermediate computation.

**Why is this useful in debugging?**  
The active call path helps explain stack traces.

**Why can recursion cause StackOverflowError?**  
Too many active calls can exhaust available stack space.

## 🔗 Navigation

⬅️ [Method Call](./01-method-call-and-stack-frame.md)  
⬅️ [Stack Frame](./02-stack-frame.md)  
⬅️ [Execution Flow](./03-method-execution-flow.md)  
⬅️ [Java Stack & Call Stack](./04-java-stack-and-call-stack.md)

🏠 [Java Notes Home](../README.md)

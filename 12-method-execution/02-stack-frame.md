# 🧱 Java Stack Frame

> **Topic 19 • Method Execution**

A **stack frame** is the runtime data structure associated with one method invocation.

The JVM creates a new frame when a method is invoked and discards it when that invocation completes.

## 📦 Conceptual Components

### 1️⃣ Local Variable Array

Stores local variables and parameters used by the method.

### 2️⃣ Operand Stack

The JVM uses an operand stack for intermediate computation.

### 3️⃣ Reference to Runtime Constant Pool

A frame is associated with the runtime constant pool of the current class, supporting symbolic references needed during execution.

## 🧠 JVM-Spec Accuracy

The JVM Specification defines the conceptual structure and behavior of a frame. Actual JVM implementations may use additional internal data or optimize execution.

So avoid assuming that every physical frame has exactly the same memory layout.

## 🔄 Frame Lifetime

```text
Method invocation
       ↓
Frame created
       ↓
Frame becomes active
       ↓
Method executes
       ↓
Return / abrupt completion
       ↓
Frame discarded
```

## 🎤 Interview Quick Check

**What is a stack frame?**  
Runtime data associated with one method invocation.

**Name its conceptual components.**  
Local variable array, operand stack and reference to the runtime constant pool.

**When is a frame created?**  
When a method invocation occurs.

**When is it discarded?**  
When the invocation completes.

## 🔗 Navigation

⬅️ [Method Call](./01-method-call-and-stack-frame.md)  
➡️ [Execution Flow](./03-method-execution-flow.md)  
➡️ [Java Stack & Call Stack](./04-java-stack-and-call-stack.md)  
➡️ [Quick Revision](./05-method-execution-quick-revision.md)

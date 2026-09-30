# ⚡ Method Execution — Quick Revision

> **Topic 19 • 30-Second Revision**

## 🔄 Main Flow

~~~text
Method Call
    ↓
Stack Frame Created
    ↓
Method Executes
    ↓
Method Finishes
    ↓
Frame Discarded
    ↓
Control Returns to Caller
~~~

## 🧠 Remember

| Concept | Easy Meaning |
|---|---|
| Method invocation | Calling a method |
| Stack frame | Runtime data for one method call |
| JVM Stack | Stack associated with a thread |
| Call stack | Active chain of method calls |
| Recursion | Method calls itself |
| StackOverflowError | Too many active calls can exhaust stack space |

### 🔥 Formula

**CALL → FRAME → EXECUTE → RETURN**

### 🎯 Interview One-Liner

When a method is called, its invocation gets a stack frame; after the invocation completes, that frame is discarded and control returns to the caller.

🏠 [Java Notes Home](../README.md)
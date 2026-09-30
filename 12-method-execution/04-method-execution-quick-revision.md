# ⚡ Method Execution — Quick Revision

> **Topic 12 • 30-Second Revision**

## 🔄 Master Flow

```text
Method Call
    ↓
Invocation Starts
    ↓
Stack Frame
    ↓
Method Executes
    ↓
Method Returns / Completes
    ↓
Frame Discarded
    ↓
Caller Continues
```

## 🧠 Important Concepts

| Concept | Easy Meaning |
|---|---|
| Method invocation | A request to execute a method |
| Stack frame | Runtime data associated with one method invocation |
| JVM Stack | Per-thread stack used for active method execution |
| Call stack | Current chain of active method calls |
| LIFO | Last active call normally returns first |
| Recursion | A method calls itself directly or indirectly |
| Base condition | Stops recursive calls |
| Stack unwinding | Recursive calls return one by one |
| StackOverflowError | Can occur when excessive active calls exhaust stack space |

## 🔥 Memory Formulas

**CALL → FRAME → EXECUTE → RETURN → CONTINUE**

For recursion:

**RECURSE → MORE FRAMES → BASE CASE → UNWIND**

## 📌 One Mental Picture

```text
Thread
  ↓
JVM Stack
  ↓
Stack Frames
  ↓
Call Chain
  ↓
Current Method
```

## 🎯 Example

```text
main()
  ↓
methodA()
  ↓
methodB()
  ↓
methodB returns
  ↓
methodA returns
  ↓
main continues
```

## 🎤 Interview One-Liners

**Stack frame:** Runtime data associated with one method invocation.

**JVM stack:** A stack associated with each thread for active method execution.

**Call stack:** The currently active chain of method invocations.

**Recursion:** A method directly or indirectly invokes itself.

**StackOverflowError:** Can occur when excessive active calls exhaust stack space.

🏠 [Java Notes Home](../README.md)

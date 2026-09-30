# ⚡ Method Execution — Quick Revision

> **Topic 19 • 30 Seconds**

~~~text
Method Call
    ↓
Stack Frame
    ↓
Method Executes
    ↓
Method Finishes
    ↓
Frame Removed
    ↓
Back to Caller
~~~

**Stack Frame** → Working area for one active method call.

**Java Stack** → Stack associated with a thread.

**Call Stack** → Active chain of method calls.

**Recursion** → A method calling itself.

**StackOverflowError** → Can happen when too many calls remain active.

### 🎯 Interview Question

**What happens when a method is called?**

A stack frame is created, the method runs, and when it finishes the frame is removed and control returns to the caller.

🏠 [Java Notes Home](../README.md)
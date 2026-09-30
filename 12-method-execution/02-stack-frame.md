# 🧱 What Is a Stack Frame?

> **Topic 19 • Method Execution**

A **stack frame** is the JVM working area for **one method call**.

It helps keep track of things needed while that method runs, such as:

- Local variables
- Intermediate calculation data
- Information needed to execute the method

## Simple Picture

~~~text
add() frame
┌───────────────┐
│ local values  │
│ calculations  │
│ method info   │
└───────────────┘
~~~

When the method finishes, its frame is no longer needed.

> The JVM Specification describes frames conceptually. Actual JVM implementations can optimize the internal representation.

### 🧠 Remember

**Stack frame = working area for one method call.**

⬅️ [Method Call](./01-method-call-and-stack-frame.md)  
➡️ [Execution Flow](./03-method-execution-flow.md)  
➡️ [Quick Revision](./05-method-execution-quick-revision.md)
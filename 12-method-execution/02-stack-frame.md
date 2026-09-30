# 🧱 Java Stack Frame

> **Topic 19 • Method Execution**

## 2️⃣ What Is a Stack Frame?

A **stack frame** is the runtime data associated with one method invocation.

It conceptually contains information needed while that invocation is running, including:

- Local variables and parameters
- An operand stack used by JVM bytecode for intermediate calculations
- Information needed to support execution and return

For example, while add() is active, its invocation has its own frame:

~~~text
add() frame
┌─────────────────────┐
│ local variables     │
│ intermediate data   │
│ execution info      │
└─────────────────────┘
~~~

When the invocation finishes, the frame is discarded.

> The JVM Specification defines the conceptual frame structure. A real JVM may optimize its internal representation, so do not assume a fixed physical memory layout.


## 🧠 Remember

**One active method invocation → One conceptual stack frame**

➡️ [Method Call](./01-method-call.md)
➡️ [Method Execution Flow](./03-method-execution-flow.md)

🏠 [Java Notes Home](../README.md)
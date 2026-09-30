<a name="top"></a>

# 🧱 Java Stack Frame

> **Topic 12 • Method Execution**

A **stack frame** is the runtime data associated with one method invocation.

Whenever a method is active, the JVM specification models the execution of that invocation using a frame associated with the thread's JVM stack.

## 1️⃣ Why Do We Need a Stack Frame?

Suppose:

```java
static int add(int a, int b) {
    int sum = a + b;
    return sum;
}
```

While `add()` is executing, the runtime needs information such as:

- Parameter values
- Local variables
- Intermediate calculation data
- Information required to continue execution
- Information needed when the invocation returns

The frame provides the conceptual place for this invocation-specific execution state.

## 2️⃣ Conceptual Contents

A JVM stack frame is associated with:

### 🔹 Local Variables

Values such as parameters and local variables are represented in the frame's local-variable structure.

```java
static int add(int a, int b) {
    int sum = a + b;
    return sum;
}
```

Conceptually:

```text
add() frame
┌────────────────────────┐
│ parameters: a, b       │
│ local variable: sum    │
└────────────────────────┘
```

### 🔹 Operand Stack

JVM bytecode uses an **operand stack** for intermediate operations.

For example, a calculation such as:

```java
int sum = a + b;
```

is represented in bytecode using stack-based operations.

You do not need to manually manage this stack. The JVM handles it while executing bytecode.

### 🔹 Execution / Return Information

The frame also contains information needed to support execution and returning from the current invocation.

The JVM Specification describes these structures conceptually.

## 3️⃣ Important JVM Specification Note

Do not imagine every frame as a fixed physical box in RAM.

The JVM specification defines the behavior and conceptual structure. A real JVM implementation can optimize how this information is represented internally.

So this is useful:

```text
One active invocation
        ↓
One conceptual stack frame
```

But avoid claiming that every JVM must use an identical physical memory layout.

## 4️⃣ Frame Lifetime

A frame is created when a method invocation starts.

```text
Method invoked
      ↓
Frame becomes active
      ↓
Method executes
      ↓
Method completes
      ↓
Frame is discarded
```

If a method calls another method:

```text
main() frame
     ↓
methodA() frame
     ↓
methodB() frame
```

The newest active invocation is represented by the newest active frame in the call chain.

## 5️⃣ Example

```java
class Demo {

    static void methodA() {
        int x = 10;
        methodB();
    }

    static void methodB() {
        int y = 20;
    }

    public static void main(String[] args) {
        methodA();
    }
}
```

Conceptually, while `methodB()` is executing:

```text
┌─────────────────┐
│ methodB frame   │ ← current invocation
├─────────────────┤
│ methodA frame   │
├─────────────────┤
│ main frame      │
└─────────────────┘
```

When `methodB()` finishes, its frame is discarded and `methodA()` continues.

## 6️⃣ Stack Frame vs Object

These are different concepts.

| Stack Frame | Object |
|---|---|
| Associated with a method invocation | Created from a class |
| Holds invocation-specific execution data | Holds object state |
| Has a limited lifetime tied to the invocation | Lifetime is managed by the JVM/GC |
| Part of JVM stack execution model | Normally allocated in the heap in common JVM implementations |

Do not use the oversimplified rule “everything local is stack and every object is heap” as if it were the complete JVM specification. JVM implementations can optimize representations.

## 🧠 Memory Trick

**One active method invocation → One conceptual frame**

➡️ [Java Stack & Call Stack](./03-java-stack-and-call-stack.md)  
➡️ [Recursion & Stack](./04-recursion-and-stack.md)

## 🎤 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. What is a stack frame?</summary>
<br>

Runtime data associated with one method invocation. It conceptually holds information needed while that invocation executes.

</details>

<details>
<summary>Q2. What happens to a frame when the method finishes?</summary>
<br>

The method invocation completes and its frame is no longer active; the runtime can reclaim that invocation's stack space.

</details>

<details>
<summary>Q3. Does every JVM use the same physical frame layout?</summary>
<br>

No. The JVM specification defines required behavior, while implementations can use different internal representations and optimizations.

</details>
## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

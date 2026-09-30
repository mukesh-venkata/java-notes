# 📞 Java Method Execution

> **Topic 19 • Method Execution**

A method call is not just “jumping” to another method. The JVM keeps track of the current method, creates a runtime frame for the new invocation, executes it, and then returns control to the caller.

## 1️⃣ When a Method Is Called

~~~java
class Demo {
    public static void main(String[] args) {
        add();
        System.out.println("Back in main");
    }

    static void add() {
        int a = 10;
        int b = 20;
        int sum = a + b;
    }
}
~~~

The flow is:

~~~text
main()
   ↓
calls add()
   ↓
add() invocation starts
   ↓
Stack frame for add() is created
   ↓
add() executes
   ↓
add() completes
   ↓
add() frame is discarded
   ↓
main() continues
~~~

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

## 3️⃣ Method Return

When a method finishes normally:

1. Its invocation completes.
2. Its stack frame is discarded.
3. Control returns to the calling method.
4. If the method returns a value, the caller receives that value.

~~~java
static int add(int a, int b) {
    return a + b;
}

public static void main(String[] args) {
    int result = add(10, 20);
    System.out.println(result);
}
~~~

Conceptually:

~~~text
main()
  ↓
add(10, 20)
  ↓
return 30
  ↓
main() receives 30
~~~

A method can also complete abruptly, for example because of an exception. In that case, control does not necessarily return normally to the immediate caller.

## 🧠 Easy Memory Trick

**CALL → FRAME → EXECUTE → RETURN**

## 🎤 Interview Questions

**What happens when a method is called?**  
A new invocation and its stack frame are created, the method executes, and the frame is discarded when that invocation completes.

**What is a stack frame?**  
Runtime data associated with one method invocation.

**What happens when a method returns?**  
The invocation completes and control goes back to the caller, normally carrying a return value when the method has one.

➡️ [Stack & Call Stack](./02-stack-and-call-stack.md)  
➡️ [Quick Revision](./03-method-execution-quick-revision.md)

🏠 [Java Notes Home](../README.md)
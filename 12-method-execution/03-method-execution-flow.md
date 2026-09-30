# 🔄 Method Execution Flow

> **Topic 19 • Method Execution**

The easiest way to remember method execution is:

~~~text
1. Method is called
       ↓
2. Stack frame is created
       ↓
3. Method executes
       ↓
4. Method finishes
       ↓
5. Frame is removed
       ↓
6. Control returns to caller
~~~

## Example

~~~java
public static void main(String[] args) {
    add();
    System.out.println("Done");
}

static void add() {
    int sum = 10 + 20;
}
~~~

### 🐞 Why Learn This?

It helps you understand method calls, debugging, stack traces and recursion.

### 🧠 Remember

**Call → Frame → Execute → Return**

⬅️ [Stack Frame](./02-stack-frame.md)  
➡️ [Java Stack](./04-java-stack-and-call-stack.md)  
➡️ [Quick Revision](./05-method-execution-quick-revision.md)
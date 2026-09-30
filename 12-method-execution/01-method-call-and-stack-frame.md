# 📞 How a Method Call Works

> **Topic 19 • Method Execution**

When one method calls another, Java creates a **stack frame** for that active method call.

## Simple Flow

~~~text
main()
  ↓
calls add()
  ↓
add() gets a stack frame
  ↓
add() runs
  ↓
add() finishes
  ↓
back to main()
~~~

## Example

~~~java
public static void main(String[] args) {
    add();
    System.out.println("Back to main");
}

static void add() {
    int a = 10;
    int b = 20;
}
~~~

### 🧠 Remember

**One active method call → One stack frame**

➡️ [Stack Frame](./02-stack-frame.md)  
➡️ [Execution Flow](./03-method-execution-flow.md)  
➡️ [Quick Revision](./05-method-execution-quick-revision.md)

🏠 [Java Notes Home](../README.md)
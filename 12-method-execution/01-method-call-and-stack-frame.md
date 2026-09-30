# 📞 Java Method Call & Stack Frame

> **Topic 19 • Method Execution**

When a method is invoked, the JVM creates a new **stack frame** for that invocation and associates it with the current thread's JVM stack.

## 🔄 Basic Flow

```text
Method Call
    ↓
New Stack Frame
    ↓
Frame becomes active
    ↓
Method executes
```

## 💻 Example

```java
public class Demo {
    public static void main(String[] args) {
        add();
    }

    static void add() {
        int a = 10;
        int b = 20;
    }
}
```

Conceptually:

```text
main()
   ↓
main() frame
   ↓
calls add()
   ↓
add() frame
   ↓
add() executes
```

> **Each active method invocation has its own stack frame.**

This becomes especially important in recursion.

## 🎤 Interview Quick Check

**What happens when a method is invoked?**  
A new stack frame is created for that invocation.

**Where is the frame associated?**  
With the current thread's JVM stack.

**Does every method call share one frame?**  
No. Each active invocation has its own frame.

## 🔗 Navigation

➡️ [Stack Frame](./02-stack-frame.md)  
➡️ [Execution Flow](./03-method-execution-flow.md)  
➡️ [Java Stack & Call Stack](./04-java-stack-and-call-stack.md)  
➡️ [Quick Revision](./05-method-execution-quick-revision.md)

🏠 [Java Notes Home](../README.md)

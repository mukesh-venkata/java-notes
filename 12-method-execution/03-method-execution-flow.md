# 🔄 Java Method Execution Flow

> **Topic 19 • Method Execution**

A method call can be understood as a sequence involving frame creation, execution and return.

## 🧭 Complete Flow

```text
Method Call
     ↓
Stack Frame Created
     ↓
Frame Becomes Active
     ↓
Method Executes
     ↓
Method Completes
     ↓
Frame Discarded
     ↓
Control Returns to Caller
```

## 💻 Example

```java
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
```

### Conceptual Call Flow

```text
main()
  │
  ├── calls add()
  │       │
  │       ├── add() frame created
  │       ├── add() executes
  │       └── add() frame discarded
  │
  └── main() continues
```

## 🔙 Returning From a Method

When a method completes normally:

- Its invocation completes.
- Its frame is discarded.
- Control returns to the calling method.
- If the method returns a value, that value becomes available to the caller.

A method can also complete abruptly because of an exception. Exception handling rules then determine where control transfers.

## 🧠 Debugging Connection

Understanding frames helps explain a call stack such as:

```text
main()
  ↓
service()
  ↓
repository()
  ↓
databaseCall()
```

A stack trace records the active call path associated with an exception.

## 🎤 Interview Quick Check

**What happens after a method completes?**  
Its frame is discarded and control returns to the caller, unless execution completes abruptly.

**Why is this useful for debugging?**  
It helps explain call stacks and stack traces.

## 🔗 Navigation

⬅️ [Stack Frame](./02-stack-frame.md)  
➡️ [Java Stack & Call Stack](./04-java-stack-and-call-stack.md)  
➡️ [Quick Revision](./05-method-execution-quick-revision.md)

🏠 [Java Notes Home](../README.md)

# 📞 Java Method Call

> **Topic 19 • Method Execution**

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


## 🧠 Memory Trick

**CALL → EXECUTE → RETURN → CONTINUE**

➡️ [Stack Frame](./02-stack-frame.md)

🏠 [Java Notes Home](../README.md)
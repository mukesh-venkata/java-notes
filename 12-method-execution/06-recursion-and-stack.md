# 🔁 Recursion & Stack

> **Topic 19 • Method Execution**

## 4️⃣ Recursion

Recursion means a method calls itself.

~~~java
static void countDown(int n) {
    if (n == 0) {
        return;
    }

    System.out.println(n);
    countDown(n - 1);
}
~~~

For countDown(3):

~~~text
countDown(3)
      ↓
countDown(2)
      ↓
countDown(1)
      ↓
countDown(0)
      ↓
return
~~~

Each active recursive invocation has its own stack frame.

If recursive calls continue without reaching a proper stopping condition, too many active frames can exhaust stack space and result in StackOverflowError.


## 🧠 Remember

**Recursion → Multiple active calls → Multiple stack frames**

➡️ [Quick Revision](./07-method-execution-quick-revision.md)

🏠 [Java Notes Home](../README.md)
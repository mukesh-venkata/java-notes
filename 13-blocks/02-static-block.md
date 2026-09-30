# ⚡ Static Block

> **Topic 20 • Blocks**

A **static block** uses the static keyword.

~~~java
static {
    System.out.println("Static Block");
}
~~~

## When Does It Run?

It runs when the class is **initialized**.

For the normal application class containing main, this happens before main starts.

## How Many Times?

Static initialization runs once for the class. Multiple static blocks run in the order they appear.

~~~java
class Demo {
    static {
        System.out.println("First");
    }

    static {
        System.out.println("Second");
    }
}
~~~

Output:

~~~text
First
Second
~~~

### 🧠 Easy Trick

**Static → Class → Once**

### 🎯 Interview

**Does a static block run every time an object is created?**  
No. It belongs to class initialization.

➡️ [Instance Block](./03-instance-initialization-block.md)  
➡️ [Initialization Order](./04-constructor-and-initialization-order.md)
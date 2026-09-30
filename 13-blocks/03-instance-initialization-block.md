# 🟢 Instance Initialization Block

> **Topic 20 • Blocks**

An **instance block** is a block without the static keyword.

~~~java
class Student {

    {
        System.out.println("Instance Block");
    }

    Student() {
        System.out.println("Constructor");
    }
}
~~~

## When Does It Run?

It runs during **object creation**, before the constructor body.

~~~text
new Student()
      ↓
Instance Block
      ↓
Constructor
~~~

If two objects are created, the instance initialization runs for each object construction.

Multiple instance blocks follow their source order together with instance field initializers.

### 🧠 Easy Trick

**Instance → Object → Every construction**

### 🎯 Interview

**Does an instance block use static?**  
No.

**Does it run before the constructor body?**  
Yes.

➡️ [Static Block](./02-static-block.md)  
➡️ [Initialization Order](./04-constructor-and-initialization-order.md)
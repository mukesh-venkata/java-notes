# 🧱 Java Blocks

> **Topic 20 • Blocks**

A **block** is a group of Java statements inside curly braces.

~~~text
Blocks
 ├── Static Block
 └── Instance Block
       ↓
   Constructor
~~~

A constructor is not technically a block; its body is a block. We study it here because it is part of object creation.

## 1️⃣ Static Block

~~~java
static {
    System.out.println("Static Block");
}
~~~

Runs during **class initialization**.

## 2️⃣ Instance Block

~~~java
{
    System.out.println("Instance Block");
}
~~~

Runs during **object creation**, before the constructor body.

## 3️⃣ Constructor

Runs during object creation to initialize the object.

### 🧠 Easy Trick

**Class → Static**  
**Object → Instance → Constructor**

🏠 [Java Notes Home](../README.md)
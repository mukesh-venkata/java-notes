# 🧱 Java Blocks — Overview

> **Topic 20 • Blocks**

A **block** is a group of Java statements enclosed within `{ }`.

## Main Concepts

```text
BLOCKS
  ├── Static Block
  ├── Instance Initialization Block
  └── Constructor
```

> A constructor is not itself a block; its body is a block. It is included here because it participates directly in object initialization.

## 1️⃣ Static Block

```java
static {
    System.out.println("Static Block");
}
```
Runs during **class initialization**.

## 2️⃣ Instance Initialization Block

```java
{
    System.out.println("Instance Block");
}
```
Runs as part of each object construction, before that class's constructor body.

## 3️⃣ Constructor

A constructor initializes a newly created object and its body executes during object construction.

```java
class Student {
    Student() {
        System.out.println("Constructor");
    }
}
```

## 🧠 Big Picture

```text
Class initialization
       ↓
Static initialization

Object construction
       ↓
Instance initialization
       ↓
Constructor body
```

## 🎤 Interview Quick Check

**What is a block?** A group of statements enclosed in `{ }`.

**When does a static block execute?** During class initialization.

**Does a constructor itself count as a block?** No. Its body is a block.

## 🔗 Navigation

➡️ [Static Block](./02-static-block.md)  
➡️ [Instance Initialization Block](./03-instance-initialization-block.md)  
➡️ [Constructor & Initialization Order](./04-constructor-and-initialization-order.md)  
➡️ [Quick Revision](./05-blocks-quick-revision.md)

🏠 [Java Notes Home](../README.md)

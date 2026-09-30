# 07. Java Fundamentals — Quick Revision

## Java in One Flow

```text
Java Source (.java)
        ↓
      javac
        ↓
Bytecode (.class)
        ↓
       JVM
        ↓
  Machine Code
        ↓
    Execution
```

## JDK → JRE → JVM

- **JDK** → Development
- **JRE** → Runtime environment
- **JVM** → Executes bytecode

## JVM in One Line

```text
Class Loader
     ↓
Runtime Data Areas
     ↓
Execution Engine
     ↓
JNI
     ↓
Native Libraries
```

## JVM Key Components

- Class Loader
- Heap
- Method Area
- Java Stack
- PC Register
- Native Method Stack
- Execution Engine
- JNI
- Native Libraries

## Execution Engine

**Interpreter + JIT Compiler + Garbage Collector**

## Java Features

- Platform Independent
- WORA
- Portable
- Architecturally Neutral
- Multithreading
- Automatic Garbage Collection
- OOPs
- JIT Compiler

## One-Line Memory Trick

**JDK develops → JRE runs → JVM executes → JIT optimizes**

## Core Idea

> **Java code becomes bytecode, and the JVM provides the platform-specific runtime needed to execute it.**

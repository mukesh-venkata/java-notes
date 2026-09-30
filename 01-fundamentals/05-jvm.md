# 05. JVM — Java Virtual Machine

The **JVM (Java Virtual Machine)** is responsible for executing Java bytecode and providing the runtime environment for Java applications.

## What the JVM Does

- Loads Java bytecode
- Executes bytecode
- Manages memory
- Performs garbage collection
- Provides the runtime environment
- Interacts with native code when required

## Major JVM Components

### 1. Class Loader

Loads **.class files** into memory.

### 2. Heap Area

Stores:
- Objects
- Instance variables

The heap is shared among threads.

### 3. Method Area

Stores class-level information such as:
- Class metadata
- Static variables
- Runtime constant pool
- Method information

> JVM implementations can organize this area differently. In HotSpot, class metadata is primarily stored in **Metaspace**.

### 4. Java Stack

Each thread has its own Java stack.

Stores:
- Stack frames
- Local variables
- Method calls
- Intermediate values

### 5. Program Counter (PC) Register

Each thread has a PC register that keeps track of the **current bytecode instruction being executed**.

### 6. Native Method Stack

Stores information required for execution of **native methods**, such as methods implemented using C/C++.

### 7. Execution Engine

Executes Java bytecode.

Main components:
- **Interpreter** → Executes bytecode instruction by instruction
- **JIT Compiler** → Compiles frequently executed bytecode into native machine code at runtime
- **Garbage Collector** → Reclaims memory from unreachable objects

### 8. JNI — Java Native Interface

Allows Java code to interact with **native code**, such as C/C++.

### 9. Native Libraries

Platform-specific libraries used by native methods.

Examples include libraries such as **.dll, .dylib and .so**.

## JVM Flow

```text
.class File
    ↓
Class Loader
    ↓
Runtime Data Areas
    ├── Heap
    ├── Method Area
    ├── Java Stack
    ├── PC Register
    └── Native Method Stack
    ↓
Execution Engine
    ├── Interpreter
    ├── JIT Compiler
    └── Garbage Collector
    ↓
JNI
    ↓
Native Libraries
```

### 30-Second Revision

**Class Loader → Runtime Data Areas → Execution Engine → JNI → Native Libraries**


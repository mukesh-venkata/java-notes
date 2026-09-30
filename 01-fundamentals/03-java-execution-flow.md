# 03. Java Execution Flow
<div align="center">

![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Topic](https://img.shields.io/badge/Topic-Execution_Flow-2DD4BF?style=for-the-badge)

</div>

---


Java follows a compilation + runtime execution process.

## Core Flow

```text
Source Code (.java)
       ↓
Java Compiler (javac)
       ↓
Bytecode (.class)
       ↓
JVM
       ↓
Machine Code
       ↓
Execution
```

## Why Java Is Platform Independent

Java source code is compiled into **bytecode**, not directly into operating-system-specific machine code.

```text
                 Java Source
                     ↓
                   javac
                     ↓
                 Bytecode
                     ↓
                    JVM
          ┌──────────┼──────────┐
          ↓          ↓          ↓
       Windows      Linux      macOS
```

The JVM on each platform executes the same bytecode for that platform.

### WORA

**WORA = Write Once, Run Anywhere**

Write Java code once, compile it to bytecode, and run the bytecode on different platforms using a compatible JVM.

### 30-Second Revision

**.java → javac → .class → JVM → Machine Code → Execution**

**Key idea:** Bytecode + JVM gives Java its platform-independent execution model.


---

## 🧭 Navigation

⬅️ [Java Notes Home](../README.md) &nbsp; • &nbsp; 📚 [Fundamentals](./) &nbsp; • &nbsp; ☕ Keep learning!

# 04. JDK → JRE → JVM

JDK, JRE and JVM represent different layers of the Java platform.

## 1. JDK — Java Development Kit

Used for **developing Java applications**.

Contains:
- Development tools such as the Java compiler
- Runtime components
- Libraries required for development

Think: **JDK = Development**

## 2. JRE — Java Runtime Environment

Used to **run Java applications**.

Provides:
- JVM
- Required runtime libraries

Think: **JRE = Runtime**

## 3. JVM — Java Virtual Machine

Responsible for:
- Executing Java bytecode
- Managing memory
- Providing the runtime execution environment

Think: **JVM = Executes Bytecode**

## Conceptual Relationship

```text
┌─────────────────────────────┐
│            JDK              │
│     Development tools       │
│                             │
│   ┌─────────────────────┐   │
│   │        JRE          │   │
│   │   Runtime libraries │   │
│   │                     │   │
│   │   ┌─────────────┐   │   │
│   │   │     JVM     │   │   │
│   │   │ Execute     │   │   │
│   │   │ bytecode    │   │   │
│   │   └─────────────┘   │   │
│   └─────────────────────┘   │
└─────────────────────────────┘
```

### Important Note

Since Java 9, Oracle no longer distributes a separate traditional JRE as it did previously. However, the **JDK → JRE → JVM relationship remains useful for understanding the architecture of Java**.

### 30-Second Revision

**JDK → Develop**

**JRE → Run**

**JVM → Execute Bytecode**


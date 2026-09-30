# 01. Data Types Overview

<div align="center">

![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Topic](https://img.shields.io/badge/Topic-Data%20Types-2DD4BF?style=for-the-badge)

</div>

---

> **Data types define the type of data that a variable can hold.**

## 🧭 Java Data Types

~~~mermaid
flowchart TD
    A[Java Data Types] --> B[Primitive Data Types]
    A --> C[Non-Primitive / Reference Data Types]
    B --> B1[8 Built-in Types]
    C --> C1[String]
    C --> C2[Array]
    C --> C3[Interface]
    C --> C4[Class]
~~~

### 1️⃣ Primitive Data Types

Java has **8 primitive data types**.

~~~text
byte
short
int
long
float
double
boolean
char
~~~

### 2️⃣ Non-Primitive / Reference Data Types

Common reference types include **SAIC**:

~~~text
S → String
A → Array
I → Interface
C → Class
~~~

Reference variables can refer to objects, arrays, or other reference-type values.

## 🔍 Primitive vs Reference

| Primitive | Reference |
|---|---|
| 8 built-in types | Many possible types |
| Examples: int, double, char | Examples: String, arrays, classes |
| Represents a primitive value | Variable refers to an object/array/value |
| Cannot hold null | Can hold null |

## 🧠 Memory Picture

~~~text
Primitive

int age = 27;

age
┌───────┐
│  27   │
└───────┘


Reference

String name = "Java";

name
  │
  └──────────────► Object
                   ┌─────────┐
                   │ "Java"  │
                   └─────────┘
~~~

> **Important:** Exact memory representation depends on the JVM implementation and runtime environment.

## ⚡ 30-Second Revision

**Java Data Types = Primitive + Reference**

**Primitive = 8 types**

**Reference = SAIC → String, Array, Interface, Class**

<details>
<summary>🎯 Interview Quick Check</summary>

**Q: How many primitive data types are there in Java?**

**A:** 8 — byte, short, int, long, float, double, boolean and char.

**Q: What are reference data types?**

**A:** Types whose variables can refer to objects, arrays, or other reference-type values.

</details>

---

## 🧭 Navigation

⬅️ [Java Notes Home](../README.md) • 📚 Data Types

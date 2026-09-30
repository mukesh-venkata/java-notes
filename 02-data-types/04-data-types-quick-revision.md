<a name="top"></a>

# 04. Data Types — Quick Revision ⚡

<div align="center">

![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Revision](https://img.shields.io/badge/Quick-Revision-2DD4BF?style=for-the-badge)

</div>

---

## 🧠 Java Data Types

~~~mermaid
flowchart TD
    A[Java Data Types] --> B[Primitive - 8]
    A --> C[Reference]
    B --> B1[byte]
    B --> B2[short]
    B --> B3[int]
    B --> B4[long]
    B --> B5[float]
    B --> B6[double]
    B --> B7[boolean]
    B --> B8[char]
    C --> C1[String]
    C --> C2[Array]
    C --> C3[Interface]
    C --> C4[Class]
~~~

## 🔢 Primitive Types — At a Glance

| Type | Size | Key Point |
|---|---:|---|
| byte | 1 byte | -128 to 127 |
| short | 2 bytes | -32,768 to 32,767 |
| int | 4 bytes | -2³¹ to 2³¹ − 1 |
| long | 8 bytes | -2⁶³ to 2⁶³ − 1 |
| float | 4 bytes | Single precision |
| double | 8 bytes | Default decimal literal type |
| boolean | JVM-dependent | true / false |
| char | 2 bytes | UTF-16 code unit |

## 🧠 Number Pattern

~~~text
byte → short → int → long
 1       2       4      8 bytes
~~~

## 🔤 Reference Types — SAIC

~~~text
S → String
A → Array
I → Interface
C → Class
~~~

## 🆚 Primitive vs Reference

| Primitive | Reference |
|---|---|
| 8 built-in types | Many possible types |
| Holds a primitive value | Holds a reference |
| int age = 27 | String name = "Java" |
| Cannot be null | Can be null |

## 💻 Examples

~~~java
int age = 27;
double salary = 50000.50;
boolean active = true;
char grade = 'A';

String name = "Mukesh";
int[] numbers = {10, 20, 30};
~~~

## 🎯 Important Interview Points

**1. How many primitive types?**  
→ **8**

**2. Default decimal literal type?**  
→ **double**

**3. How to assign a decimal literal to float?**  
→ Use **f / F**

~~~java
float x = 10.5f;
~~~

**4. Is String primitive?**  
→ **No. String is a class/reference type.**

**5. Are arrays primitive?**  
→ **No. Arrays are objects/reference types.**

**6. Can int be null?**  
→ **No.**

**7. Can a reference variable be null?**  
→ **Yes.**

**8. What does SAIC mean?**  
→ **String, Array, Interface, Class**

## ⚡ Final Memory Map

~~~text
JAVA DATA TYPES
│
├── PRIMITIVE (8)
│   ├── Integer → byte, short, int, long
│   ├── Decimal → float, double
│   ├── boolean
│   └── char
│
└── REFERENCE
    └── SAIC
        ├── String
        ├── Array
        ├── Interface
        └── Class
~~~

<div align="center">

### 🧠 Remember

**Primitive = 8**

**Reference = SAIC**

**double = default decimal literal**

**null = reference types only**

</div>

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

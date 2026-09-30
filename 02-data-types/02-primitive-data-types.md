<a name="top"></a>

# 02. Primitive Data Types

<div align="center">

![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Topic](https://img.shields.io/badge/Topic-Primitive%20Types-2DD4BF?style=for-the-badge)

</div>

---

Java has **8 primitive data types**.

~~~mermaid
flowchart TD
    A[Primitive Data Types - 8] --> B[Integer Types - 4]
    A --> C[Floating-Point Types - 2]
    A --> D[boolean]
    A --> E[char]
    B --> B1[byte]
    B --> B2[short]
    B --> B3[int]
    B --> B4[long]
    C --> C1[float]
    C --> C2[double]
~~~

## 🔢 A. Number / Integer Types — 4

| Type | Size | Range |
|---|---:|---|
| **byte** | 1 byte (8 bits) | -128 to 127 |
| **short** | 2 bytes (16 bits) | -32,768 to 32,767 |
| **int** | 4 bytes (32 bits) | -2³¹ to 2³¹ − 1 |
| **long** | 8 bytes (64 bits) | -2⁶³ to 2⁶³ − 1 |

### 📌 Exact int Range

**-2,147,483,648 to 2,147,483,647**

### 📌 Exact long Range

**-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807**

### 🧠 Integer Memory Trick

~~~text
byte → 1 byte
short → 2 bytes
int  → 4 bytes
long → 8 bytes

1 → 2 → 4 → 8
~~~

## 🔢 B. Decimal / Floating-Point Types — 2

| Type | Size | Details |
|---|---:|---|
| **float** | 4 bytes (32 bits) | Single-precision floating-point |
| **double** | 8 bytes (64 bits) | Double-precision floating-point |

**double** is Java's default type for decimal/floating-point literals.

~~~java
double price = 99.99;
float price2 = 99.99f;
~~~

Without the suffix:

~~~java
float price = 99.99;   // compile-time error
~~~

## ✅ C. boolean — 1 Type

| Type | Size | Details |
|---|---|---|
| **boolean** | JVM specification does not define a fixed storage size | Stores true or false |

~~~java
boolean isActive = true;
boolean isLoggedIn = false;
~~~

> **Important:** Java does not specify a fixed number of bits/bytes for boolean. Its actual representation can depend on the JVM and data structure.

## 🔤 D. char — 1 Type

| Type | Size | Details |
|---|---:|---|
| **char** | 2 bytes (16 bits) | Stores a single UTF-16 code unit |

### Range

**U+0000 to U+FFFF**

~~~java
char grade = 'A';
char symbol = '$';
~~~

> A Java char is a UTF-16 code unit. Some Unicode code points require a surrogate pair.

## 📊 All 8 Primitive Types

| Category | Type | Size |
|---|---|---:|
| Integer | byte | 1 byte |
| Integer | short | 2 bytes |
| Integer | int | 4 bytes |
| Integer | long | 8 bytes |
| Floating-point | float | 4 bytes |
| Floating-point | double | 8 bytes |
| Boolean | boolean | JVM-dependent |
| Character | char | 2 bytes |

## 💻 Example

~~~java
public class PrimitiveDemo {

    public static void main(String[] args) {

        byte age = 27;
        short year = 2026;
        int salary = 500000;
        long population = 8000000000L;

        float percentage = 85.5f;
        double price = 999.99;

        boolean active = true;

        char grade = 'A';
    }
}
~~~

## 🧠 Easy Memory Map

~~~text
INTEGER       → byte, short, int, long
DECIMAL       → float, double
TRUE / FALSE  → boolean
CHARACTER     → char
~~~

## ⚡ 30-Second Revision

**Primitive = 8**

**4 integer + 2 floating-point + 1 boolean + 1 character**

**byte → short → int → long = 1 → 2 → 4 → 8 bytes**

<details>
<summary>🎯 Interview Quick Check</summary>

**Q: Default type of a decimal literal?**  
A: double.

**Q: How do you assign a decimal literal to float?**  
A: Use f or F, for example float x = 10.5f.

**Q: Is boolean always exactly 1 byte?**  
A: No. Java does not define a fixed storage size for boolean.

**Q: What is the int range?**  
A: -2³¹ to 2³¹ − 1.

</details>

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

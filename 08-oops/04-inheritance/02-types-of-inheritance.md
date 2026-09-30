<a name="top"></a>

# 🌳 Types of Inheritance in Java

> **Topic 23 • Inheritance**

Inheritance structures can be understood by looking at how parent and child classes are connected.

Java supports several inheritance structures through classes, while **multiple inheritance of classes is not supported**.

## 1️⃣ Single Inheritance

One child class extends one parent class.

~~~text
Animal
   ↓
 Dog
~~~

Example:

~~~java
class Animal {
    void eat() {}
}

class Dog extends Animal {
    void bark() {}
}
~~~

This is **single inheritance**.

## 2️⃣ Multilevel Inheritance

A class extends a class that itself extends another class.

~~~text
Animal
   ↓
Mammal
   ↓
Dog
~~~

Example:

~~~java
class Animal {
}

class Mammal extends Animal {
}

class Dog extends Mammal {
}
~~~

A Dog is indirectly related to Animal through Mammal.

## 3️⃣ Hierarchical Inheritance

Multiple child classes extend the same parent.

~~~text
       Animal
       /    \
     Dog    Cat
~~~

Example:

~~~java
class Animal {
    void eat() {}
}

class Dog extends Animal {
}

class Cat extends Animal {
}
~~~

The common behavior can live in the parent.

## 4️⃣ Multiple Inheritance

Multiple inheritance through **classes** would mean:

~~~text
ParentA     ParentB
    \       /
      Child
~~~

Java does **not** allow a class to extend multiple classes.

This is invalid:

~~~java
class Child extends ParentA, ParentB {
}
~~~

A major reason discussed in Java design is avoiding ambiguity when two parent classes provide conflicting implementations or state.

## 5️⃣ Multiple Inheritance Through Interfaces

Java allows a class to implement multiple interfaces.

~~~java
interface Printable {
    void print();
}

interface Scannable {
    void scan();
}

class Machine implements Printable, Scannable {

    public void print() {
    }

    public void scan() {
    }
}
~~~

Conceptually:

~~~text
Printable     Scannable
     \          /
       Machine
~~~

This is different from extending multiple classes.

## 6️⃣ Hybrid Inheritance

A hybrid structure combines more than one inheritance pattern.

Java does not support arbitrary hybrid inheritance through classes when that would require multiple class inheritance.

Interfaces can participate in more complex type relationships.

## 7️⃣ Quick Comparison

| Type | Structure | Java class support |
|---|---|---|
| Single | A → B | ✅ |
| Multilevel | A → B → C | ✅ |
| Hierarchical | A → B and A → C | ✅ |
| Multiple classes | A + B → C | ❌ |
| Multiple interfaces | I1 + I2 → C | ✅ |
| Hybrid | Combination | Depends on structure; multiple class inheritance is not allowed |

## 🧠 Memory Trick

**S-M-H**

**Single → Multilevel → Hierarchical**

Then remember:

**Multiple classes ❌ | Multiple interfaces ✅**

## 🎤 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. Does Java support multiple inheritance through classes?</summary>
<br>

No. A class cannot extend more than one class.

</details>

<details>
<summary>Q2. Can a class implement multiple interfaces?</summary>
<br>

Yes. A class can implement multiple interfaces.

</details>

<details>
<summary>Q3. What is multilevel inheritance?</summary>
<br>

An inheritance chain with multiple levels, such as A → B → C.

</details>

<details>
<summary>Q4. What is hierarchical inheritance?</summary>
<br>

Multiple child classes share the same parent class.

</details>
## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

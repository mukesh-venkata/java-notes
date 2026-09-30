# ✍️ Java Method Signature

> **Topic 18 • Methods**

A Java method's **signature** is based on its **method name and formal parameter types**.

## 📌 Example

```java
int add(int a, int b)
```

The signature is:

```text
add(int, int)
```

Parameter variable names are not part of the signature.

## ❌ Return Type Is Not Part of the Signature

These cannot coexist as overloads:

```java
int add(int a, int b)
double add(int a, int b)
```

The return type does not make the signatures different.

## 📊 What Counts?

| Element | Part of method signature? |
|---|:---:|
| Method name | ✅ |
| Parameter types | ✅ |
| Parameter names | ❌ |
| Return type | ❌ |
| Access modifier | ❌ |

## 🔗 Why This Matters

Method signatures are central to method overloading and overriding rules.

## 🎤 Interview Quick Check

**What is a method signature?**  
Method name + formal parameter types.

**Is return type part of a method signature?**  
No.

**Are parameter names part of it?**  
No.

## 🔗 Navigation

⬅️ [Declaration & Definition](./02-method-declaration-and-definition.md)

➡️ [Static & Instance Methods](./04-static-and-instance-methods.md)

➡️ [Overloading](./06-method-overloading.md)

➡️ [Quick Revision](./12-methods-quick-revision.md)

<a name="top"></a>

# ⚡ Java Variables — Comparison & Quick Revision

> **Topic 16 • 30-Second Revision**

## 🧠 Master Memory Trick

### **STATIC → CLASS | INSTANCE → OBJECT | LOCAL → SCOPE**

```text
STATIC
  ↓
Class-level state

INSTANCE
  ↓
Object-level state

LOCAL
  ↓
Method / constructor / block scope
```

---

## 📊 Master Comparison

| Feature | Static / Class | Instance | Local |
|---|---|---|---|
| Associated with | Class | Object | Method/constructor/block execution |
| Declared | Class body with `static` | Class body | Method/constructor/block |
| Independent copies | Class-level | Per object | Per execution/scope |
| Default value | Yes | Yes | No |
| Typical access | `Class.field` | `object.field` | Directly in scope |
| Typical role | Shared class state | Object state | Temporary computation |

---

## 🔥 Default Values

Fields receive defaults:

```text
byte/short/int/long → 0
float/double        → 0.0
boolean             → false
char                → '\\u0000'
reference           → null
```

Local variables:

```text
No automatic default
        ↓
Must be definitely assigned
        ↓
Before being read
```

---

## 🧩 Quick Examples

### Static

```java
class Counter {
    static int count = 0;
}
```

### Instance

```java
class Student {
    int age;
}
```

### Local

```java
void display() {
    int age = 20;
}
```

---

## 🆚 Three Questions

### Who owns it?

```text
Static   → Class
Instance → Object
Local    → Current execution scope
```

### Does it get a default value?

```text
Static   → Yes
Instance → Yes
Local    → No
```

### How is it usually accessed?

```text
Static   → Class.field
Instance → object.field
Local    → directly within scope
```

---

## 🎤 Interview One-Liners

**Static vs instance?**  
→ Static is associated with the class; instance state belongs separately to each object.

**Why no default value for locals?**  
→ Java requires local variables to be definitely assigned before they are read.

**Can a static field change?**  
→ Yes, unless it is also declared `final` or otherwise constrained by its declaration/access.

**Are static variables always stored in the Method Area?**  
→ Do not state this as a universal Java rule; exact runtime storage is JVM implementation-dependent.

**Are local variables always physically on the stack?**  
→ No. Stack-frame association is a useful model, but JVM implementations may optimize storage.

---

## 🗺️ Final Memory Map

```text
                       VARIABLES
                           │
          ┌────────────────┼────────────────┐
          │                │                │
       STATIC           INSTANCE           LOCAL
          │                │                │
        CLASS            OBJECT            SCOPE
          │                │                │
       shared          per-object       temporary
       state              state         execution state
```

---

## 🔗 Navigation

⬅️ [Variables Overview](./01-variables-overview.md)

⬅️ [Static Variables](./02-class-static-variables.md)

⬅️ [Instance Variables](./03-instance-variables.md)

⬅️ [Local Variables](./04-local-variables.md)

🏠 [Java Notes Home](../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

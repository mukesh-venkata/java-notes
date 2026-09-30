<a name="top"></a>

# ⚡ 7. Object Class — Quick Revision

> **30-second revision:** `Object` is the root class for Java class inheritance and provides commonly used methods for representation, equality, runtime type, copying, legacy finalization, and thread coordination.

## 🧠 Method Map

| Method | Purpose |
|---|---|
| `toString()` | String representation |
| `hashCode()` | Integer hash code |
| `equals(Object)` | Equality comparison |
| `getClass()` | Runtime class |
| `clone()` | Shallow copy mechanism |
| `finalize()` | Legacy finalization; do not use |
| `wait()` | Wait for notification/interruption |
| `wait(long)` | Timed wait |
| `wait(long, int)` | Timed wait with nanos component |
| `notify()` | Wake one waiting thread |
| `notifyAll()` | Wake all waiting threads |

## 🔗 Key Relationships

### Equality & Hashing

```text
equals() true
     ↓
same hashCode()
```

### Copying

```text
clone()
  ↓
shallow copy
  ↓
nested references may be shared
```

### Thread Coordination

```text
wait()
  ↓
releases monitor
  ↓
waiting
  ↓
notify() / notifyAll()
  ↓
reacquire monitor
```

## ⚠️ High-Value Rules

- `Object.equals()` is identity-based unless a class overrides it.
- Equal objects must have equal hash codes.
- Same hash code does not prove equality.
- `getClass()` reports the runtime class.
- `clone()` creates a shallow copy when supported.
- `Cloneable` is a marker interface.
- `finalize()` is deprecated/removed and should not be used.
- `wait()`, `notify()`, and `notifyAll()` require monitor ownership.
- `wait()` releases the object's monitor while waiting.

## 🧠 Memory Trick

```text
T → toString → Tell object's representation
H → hashCode  → Hash
E → equals    → Equality
G → getClass  → Get runtime class
C → clone     → Copy
F → finalize  → Legacy finalization
W → wait      → Wait
W → wait(time)→ Timed wait
W → wait(ns)  → Timed wait + nanos
N → notify    → Wake one
N → notifyAll → Wake all
```

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>1. What is the root class of the Java class hierarchy?</summary>
<br>

java.lang.Object for Java classes.

</details>

<details>
<summary>2. What is the difference between == and equals()?</summary>
<br>

== compares primitive values or object references depending on the operands; equals() is a method used for logical equality when a class overrides it.

</details>

<details>
<summary>3. Why should equals() and hashCode() usually be overridden together?</summary>
<br>

Because equal objects must have equal hash codes for hash-based collections to behave correctly.

</details>

<details>
<summary>4. What does getClass() return?</summary>
<br>

A Class<?> object representing the runtime class of the object.

</details>

<details>
<summary>5. What kind of copy does clone() create?</summary>
<br>

Object.clone() provides a shallow copy by default.

</details>

<details>
<summary>6. What is Cloneable?</summary>
<br>

A marker interface indicating support for the Object cloning mechanism.

</details>

<details>
<summary>7. Why should finalize() not be used?</summary>
<br>

Finalization is deprecated for removal and is not a reliable deterministic resource-cleanup mechanism.

</details>

<details>
<summary>8. What is the difference between wait() and Thread.sleep()?</summary>
<br>

wait() releases the object's monitor while waiting and is used for monitor-based coordination; Thread.sleep() pauses the current thread without releasing monitors it owns.

</details>

<details>
<summary>9. Why do wait(), notify(), and notifyAll() require monitor ownership?</summary>
<br>

They coordinate through an object's monitor, so the calling thread must own that monitor.

</details>

<details>
<summary>10. What is the difference between notify() and notifyAll()?</summary>
<br>

notify() wakes one waiting thread, while notifyAll() wakes all threads waiting on that object's monitor; awakened threads still must reacquire the monitor.

</details>
## 🔗 Related Notes

- [Object Class Overview →](01-object-class-overview.md)
- [toString(), hashCode() & equals() →](02-tostring-hashcode-equals.md)
- [getClass() →](03-getclass-and-runtime-type.md)
- [clone() & Shallow Copy →](04-clone-and-shallow-copy.md)
- [finalize() & Resource Cleanup →](05-finalize-and-resource-cleanup.md)
- [wait(), notify() & notifyAll() →](06-wait-notify-notifyall.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

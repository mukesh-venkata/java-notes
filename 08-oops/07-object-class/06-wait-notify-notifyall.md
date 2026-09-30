<a name="top"></a>

# ⏳ 6. wait(), notify() & notifyAll()

> **Core idea:** These Object methods support coordination between threads using an object's monitor.

## 🧠 wait()

`wait()` causes the current thread to wait until it is notified or interrupted.

Declaration:

```java
public final void wait() throws InterruptedException
```

The current thread must own the object's monitor when calling `wait()`.

Typically, this means the call occurs inside a synchronized block or synchronized method using the same object.

Example:

```java
synchronized (lock) {
    lock.wait();
}
```

When `wait()` is called, the thread releases that object's monitor and waits.

## ⏱️ wait(long timeout)

```java
lock.wait(1000);
```

The timeout is measured in milliseconds.

The thread can resume because of notification, interruption, or timeout.

## ⏱️ wait(long timeout, int nanos)

```java
lock.wait(1000, 500000);
```

This provides a timeout using milliseconds plus an additional nanosecond component.

The nanosecond argument must be in the valid range specified by the Java API.

## 🔔 notify()

`notify()` wakes one thread waiting on the same object's monitor.

```java
synchronized (lock) {
    lock.notify();
}
```

The awakened thread does not immediately continue executing the synchronized block; it must first reacquire the monitor.

## 📣 notifyAll()

`notifyAll()` wakes all threads waiting on the same object's monitor.

```java
synchronized (lock) {
    lock.notifyAll();
}
```

Those threads then compete to reacquire the monitor.

## 🔄 Relationship

```text
Thread
  ↓
wait()
  ↓
releases object's monitor
  ↓
waiting
  ↓
notify() / notifyAll()
  ↓
eligible to compete for monitor
  ↓
continues after reacquiring monitor
```

## ⚠️ Important Rules

- The current thread must own the object's monitor before calling `wait()`, `notify()`, or `notifyAll()`.
- Otherwise, Java throws `IllegalMonitorStateException`.
- These methods coordinate through the **same object monitor**.
- `wait()` releases the monitor while waiting.
- A thread awakened by `notify()` or `notifyAll()` must reacquire the monitor before continuing.

## 🧠 wait() vs sleep()

| `wait()` | `Thread.sleep()` |
|---|---|
| Method of `Object` | Static method of `Thread` |
| Used for thread coordination | Used for pausing execution |
| Must own the object's monitor | Does not require owning a monitor |
| Releases that object's monitor while waiting | Does not release monitors held by the thread |

## 🎯 Interview Questions & Answers

 **Try answering each question yourself first. Click the question to reveal the answer.**

<details>
<summary>Q1. Why are wait(), notify(), and notifyAll() methods of Object?</summary>
<br>

Because coordination is associated with an object's monitor, and every object can have a monitor.

</details>

<details>
<summary>Q2. What happens to the monitor when wait() is called?</summary>
<br>

The waiting thread releases that object's monitor and waits until it is notified or otherwise awakened.

</details>

<details>
<summary>Q3. Can notify() be called outside synchronized access to the same object?</summary>
<br>

No. The calling thread must own the object's monitor.

</details>

<details>
<summary>Q4. Does notify() immediately transfer the monitor to the awakened thread?</summary>
<br>

No. The awakened thread must compete to reacquire the monitor after the notifying thread releases it.

</details>

<details>
<summary>Q5. What exception occurs when monitor ownership is violated?</summary>
<br>

IllegalMonitorStateException.

</details>
## 🔗 Related Notes

- [Object Class Overview →](01-object-class-overview.md)
- [finalize() & Resource Cleanup →](05-finalize-and-resource-cleanup.md)
- [Quick Revision →](07-object-class-quick-revision.md)

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../../README.md) · 📁 [Section Home](./)

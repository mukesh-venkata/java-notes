# 🔀 Java Branching Statements — Overview

> **Topic 14 • Java Fundamentals**

Branching statements alter the normal sequential flow of execution.

---

## 🧠 Master Mnemonic

### **B-C-R**

| Letter | Statement | Main purpose |
|---|---|---|
| **B** | `break` | Exit a loop or switch |
| **C** | `continue` | Skip the current loop iteration |
| **R** | `return` | Exit the current method |

---

## 🔀 Flow Control Map

```text
             BRANCHING STATEMENTS
                     │
          ┌──────────┼──────────┐
          │          │          │
        break     continue     return
          │          │          │
       Exit loop   Skip       Exit method
       / switch    iteration
```

---

## 📌 Where They Apply

| Statement | Loop | switch | Method |
|---|:---:|:---:|:---:|
| `break` | ✅ | ✅ | ❌ |
| `continue` | ✅ | ❌ | ❌ |
| `return` | Can exit loop indirectly by leaving method | Can exit switch by leaving method | ✅ |

> A `return` always exits the current method. If it occurs inside a loop or switch within that method, execution leaves the method entirely.

---

## 🎯 Quick Mental Model

**break → stop the construct**

**continue → skip this iteration**

**return → leave the method**

---

## 🎤 Interview Quick Check

**Q1. What are branching statements?**  
A: Statements that alter the normal flow of program execution.

**Q2. What is the difference between `break` and `continue`?**  
A: `break` exits the loop or switch; `continue` skips the current loop iteration.

**Q3. What does `return` do?**  
A: It terminates the current method, optionally returning a value.

---

## 🔗 Navigation

➡️ [break Statement](./02-break-statement.md)

➡️ [continue Statement](./03-continue-statement.md)

➡️ [return Statement](./04-return-statement.md)

➡️ [Quick Revision](./05-branching-statements-quick-revision.md)

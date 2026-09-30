<a name="top"></a>

# ⚡ Java Branching Statements — Quick Revision

> **Topic 14 • 30-Second Revision**

## 🧠 Master Mnemonic

### **B-C-R**

| Letter | Statement | Remember |
|---|---|---|
| **B** | `break` | Exit loop / switch |
| **C** | `continue` | Skip current iteration |
| **R** | `return` | Exit current method |

---

## 🔀 Core Difference

```text
break
  ↓
Exit nearest applicable loop/switch

continue
  ↓
Skip remaining current iteration
  ↓
Next iteration

return
  ↓
Exit current method
```

---

## 📌 Quick Table

| Statement | Used with | Main effect |
|---|---|---|
| `break` | Loops, switch | Terminates nearest applicable construct |
| `continue` | Loops | Skips current iteration |
| `return` | Methods | Terminates current method |

---

## 🔥 Key Interview Points

**Can `break` exit a switch?**  
→ Yes.

**Can `continue` be used in a switch by itself?**  
→ No; it applies to loops.

**Does `continue` stop the loop?**  
→ No.

**What does `return` do?**  
→ Exits the current method, optionally returning a value.

**Can `break` and `continue` be labeled?**  
→ Yes. Java supports labeled `break` and labeled `continue`.

---

## 🧠 Final Memory Map

```text
             BRANCHING
                │
       ┌────────┼────────┐
       │        │        │
     break   continue   return
       │        │        │
      STOP     SKIP     EXIT
       │        │        │
   loop/switch iteration method
```

---

## 🔗 Navigation

⬅️ [Branching Overview](./01-branching-statements-overview.md)

⬅️ [break](./02-break-statement.md)

⬅️ [continue](./03-continue-statement.md)

⬅️ [return](./04-return-statement.md)

🏠 [Java Notes Home](../README.md)

---

## 🧭 Navigation

⬆️ [Back to Top](#top) · 🏠 [Java Notes Home](../README.md) · 📁 [Section Home](./)

# ⚡ Java Blocks — Quick Revision

> **Topic 20 • 30-Second Revision**

## 🧠 Master Map

```text
              JAVA INITIALIZATION
                      │
          ┌───────────┴───────────┐
          ↓                       ↓
  CLASS INITIALIZATION       OBJECT CONSTRUCTION
          │                       │
          ↓                       ↓
 Static fields / blocks    Instance fields / blocks
                                  ↓
                           Constructor body
```

## 📊 Quick Comparison

| Feature | Static Block | Instance Block | Constructor |
|---|---|---|---|
| Keyword | `static` | No `static` | Class name |
| Association | Class initialization | Object construction | Object construction |
| Frequency | Once per class initialization | Each object construction | Each constructor invocation |
| Purpose | Class-level initialization | Instance initialization | Object construction |

> A constructor is not itself a block; its body is a block.

## 🔥 Memory Trick

```text
CLASS
→ Static initialization

OBJECT
→ Instance initialization
→ Constructor
```

For a simple class:

```text
new Student()
      ↓
Instance field initialization
      ↓
Instance initialization block
      ↓
Constructor body
```

## 🎤 Interview One-Liners

**What is a block?** A group of statements enclosed in `{ }`.

**Static block?** A `static` block executed during class initialization.

**Instance initialization block?** A non-static initialization block executed as part of object construction.

**Does a static block run for every object?** No.

**Does an instance block run for every object construction?** Yes.

**Can multiple static/instance blocks exist?** Yes; initialization actions follow source order within the relevant phase.

## 🔗 Navigation

⬅️ [Blocks Overview](./01-blocks-overview.md)  
⬅️ [Static Block](./02-static-block.md)  
⬅️ [Instance Initialization Block](./03-instance-initialization-block.md)  
⬅️ [Constructor & Initialization Order](./04-constructor-and-initialization-order.md)

🏠 [Java Notes Home](../README.md)

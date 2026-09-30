# ⚡ Java Methods — Quick Revision

> **Topic 18 • 30-Second Revision**

## 🧠 Master Map

```text
                         METHODS
                            │
       ┌────────────────────┼────────────────────┐
       ↓                    ↓                    ↓
 Declaration            Types                 Binding
 Definition        Static / Instance      Early / Runtime
       │                    │                    │
       ↓                    ↓                    ↓
 Signature           Overloading          Overriding
                                                │
                         ┌──────────────────────┤
                         ↓                      ↓
                    Recursion              Method Hiding
```

## 📌 Core Rules

### Method Signature

```text
Signature = Name + Parameter Types
```

Return type is **not** part of the signature.

### Overloading

```text
Same name + different parameter list
→ overload
→ compile-time selection
```

### Overriding

```text
Inherited instance method
+ same signature
+ child implementation
→ overriding
→ runtime dynamic dispatch
```

### SPF

```text
S → Static  → hidden
P → Private → not overridden
F → Final   → cannot be overridden
```

### Recursion

```text
Recursive call
      ↓
Base case
      ↓
Return
```

### Method Hiding

```text
Static method + same signature in child
→ method hiding
→ no runtime overriding dispatch
```

## 📊 Overloading vs Overriding

| | Overloading | Overriding |
|---|---|---|
| Parameters | Different | Same signature |
| Relationship | Usually same class | Parent-child |
| Selection | Compile time | Runtime dispatch |
| Purpose | Multiple parameter forms | Specialized behavior |

## 🎤 Interview One-Liners

**Method?** → Named block of code that performs a task.

**Signature?** → Method name + formal parameter types.

**Can return type alone overload?** → No.

**Static method overridden?** → No, hidden.

**Final method overridden?** → No.

**Private method overridden?** → No, not in the normal overriding sense.

**Why `@Override`?** → Lets the compiler verify the intended override.

**Recursion?** → A method directly or indirectly calling itself.

## 🔗 Navigation

⬅️ [Methods Overview](./01-methods-overview.md)

⬅️ [Declaration & Definition](./02-method-declaration-and-definition.md)

⬅️ [Method Signature](./03-method-signature.md)

⬅️ [Static & Instance Methods](./04-static-and-instance-methods.md)

⬅️ [Method Binding](./05-method-binding.md)

⬅️ [Overloading](./06-method-overloading.md)

⬅️ [Overriding](./07-method-overriding.md)

⬅️ [Overriding vs Overloading](./08-overriding-vs-overloading.md)

⬅️ [Access & Overriding Rules](./09-method-access-and-overriding-rules.md)

⬅️ [Recursion](./10-recursion.md)

⬅️ [Method Hiding](./11-method-hiding.md)

🏠 [Java Notes Home](../README.md)

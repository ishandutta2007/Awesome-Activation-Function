# Gated Smooth Transformer Activations

## 📝 Overview
Modern Transformer architectures (such as LLaMA, Mistral, etc.) rely on gated smooth non-linearities. These functions combine gating mechanisms (like Gated Linear Units, GLUs) with smooth approximations (such as SiLU/Swish and GELU) to improve representation capacity.

## 🧮 Mathematical Formulation
$$\text{Swish}(x) = x \cdot \sigma(\beta x), \quad \text{SwiGLU}(x, y) = \text{Swish}(x) \cdot y$$

## 📊 Diagram
```mermaid
flowchart TD
    X[Input Vector] --> Split["Split Tensor (x1, x2)"]
    Split --> Path1["Gate Path: Swish(x1)"]
    Split --> Path2["Linear Path: x2"]
    Path1 --> Mult((Hadamard Mult))
    Path2 --> Mult
    Mult --> Out[Output Vector]
```

---

## 🔗 Navigation
- [Go back to README.md](../README.md)

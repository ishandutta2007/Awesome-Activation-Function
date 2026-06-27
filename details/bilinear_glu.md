# Bilinear Gated Linear Units (GLU)

## 📝 Overview
A Gated Linear Unit (GLU) is a neural network layer defined as the component-wise product of two linear transformations of the input, one of which is gated using a sigmoid function. Variants include SwiGLU and GEGLU.

## 🧮 Mathematical Formulation
$$\text{GLU}(x, W, V, b, c) = (xW + b) \otimes \sigma(xV + c)$$

## 📊 Diagram
```mermaid
flowchart TD
    X[Input x] --> Line1["Linear 1 (xW + b)"]
    X --> Line2["Linear 2 (xV + c)"]
    Line2 --> Sig[Sigmoid Gating]
    Line1 --> Mult((Hadamard Product))
    Sig --> Mult
    Mult --> Out[GLU Output]
```

---

## 🔗 Navigation
- [Go back to README.md](../README.md)

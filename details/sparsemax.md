# Sparsemax Normalization

## 📝 Overview
Sparsemax is an alternative to Softmax that is capable of outputting sparse probability distributions, meaning it can assign an exact probability of 0 to low-scoring classes.

## 🧮 Mathematical Formulation
$$\text{sparsemax}(z) = \text{argmin}_{p \in \Delta^{K-1}} \|p - z\|^2$$

## 📊 Diagram
```mermaid
flowchart LR
    Logits[Logits Vector] --> Proj[Euclidean Projection onto Simplex] --> SparseOut[Sparse Probabilities (exact 0s)]
```

---

## 🔗 Navigation
- [Go back to README.md](../README.md)

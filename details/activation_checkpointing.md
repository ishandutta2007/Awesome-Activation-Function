# Activation Checkpointing

## 📝 Overview
Activation checkpointing (also known as gradient checkpointing) is a technique used to train larger models by saving memory at the cost of extra compute. It stores only selected activations during the forward pass and recomputes others on-the-fly during backpropagation.

## 🧮 Mathematical Formulation
$$\text{Memory Complexity: } \mathcal{O}(\sqrt{N}) \text{ instead of } \mathcal{O}(N)$$

## 📊 Diagram
```mermaid
flowchart TD
    F1[Forward Step 1: Save State] --> F2[Forward Step 2: Discard State]
    F2 --> F3[Forward Step 3: Save State]
    F3 --> B3[Backward Step 3]
    B3 --> Recomp["Recompute Step 2 on-the-fly"]
    Recomp --> B2[Backward Step 2]
    B2 --> B1[Backward Step 1]
```

---

## 🔗 Navigation
- [Go back to README.md](../README.md)

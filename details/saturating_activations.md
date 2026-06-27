# Saturating Non-Linear Activations

## 📝 Overview
Saturating activations compress an infinite input domain into a finite, bounded output range. While useful for modeling probabilities or scaling outputs, they lead to gradient saturation where the derivative approaches zero for large absolute values.

## 🧮 Mathematical Formulation
$$f'(x) \to 0 \text{ as } |x| \to \infty$$

## 📊 Diagram
```mermaid
flowchart LR
    In[Large Input |x| >> 0] --> Sat["Saturating Function (e.g. Sigmoid)"] --> Grad[Gradient ~ 0]
```

---

## 🔗 Navigation
- [Go back to README.md](../README.md)

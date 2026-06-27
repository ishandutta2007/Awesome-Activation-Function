# Gumbel-Softmax Activation

## 📝 Overview
Gumbel-Softmax is a continuous distribution over the simplex that can be used to approximate categorical samples. It allows backpropagation through discrete categorical variables using the reparameterization trick.

## 🧮 Mathematical Formulation
$$y_i = \frac{\exp((\log(\pi_i) + g_i)/\tau)}{\sum_j \exp((\log(\pi_j) + g_j)/\tau)}$$

## 📊 Diagram
```mermaid
flowchart TD
    Logits[Class Logits] --> Add["Add Gumbel Noise g_i"]
    Add --> Temp["Scale by Temperature tau"]
    Temp --> Soft["Softmax Calculation"]
    Soft --> DifferentiableSample[Continuous Sample Output]
```

---

## 🔗 Navigation
- [Go back to README.md](../README.md)

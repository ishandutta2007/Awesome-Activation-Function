# Binary Step Activation Function

## 📝 Overview
The Binary Step function, also known as the threshold function, is the simplest activation function. It outputs a binary decision: 1 if the input is greater than or equal to a threshold, and 0 otherwise.

## 🧮 Mathematical Formulation
$$f(x) = \begin{cases} 0 & x < 0 \\ 1 & x \geq 0 \end{cases}$$

## 📊 Diagram
```mermaid
flowchart TD
    Input[Input x] --> Threshold{x >= 0?}
    Threshold -- Yes --> Output1[Output = 1]
    Threshold -- No --> Output0[Output = 0]
```

---

## 🔗 Navigation
- [Go back to README.md](../README.md)

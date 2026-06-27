# Autoregressive LLM Base Pre-Training Activations

## 📝 Overview
Large Language Models (LLMs) like Llama, Gemma, and Mistral use SwiGLU in their Feed-Forward Network (FFN) blocks to stabilize pre-training across trillions of tokens and improve downstream reasoning performance.

## 🧮 Mathematical Formulation
$$\text{FFN}_{\text{SwiGLU}}(x) = (\text{Swish}(xW) \otimes xV)U$$

## 📊 Diagram
```mermaid
flowchart TD
    X[Input Hidden State] --> GateProj["Gate Projection (W)"]
    X --> ValueProj["Value Projection (V)"]
    GateProj --> Swish[Swish Activation]
    Swish --> Mult((Hadamard Product))
    ValueProj --> Mult
    Mult --> OutProj["Down Projection (U)"]
    OutProj --> Out[Output Hidden State]
```

---

## 🔗 Navigation
- [Go back to README.md](../README.md)

# Generative Diffusion & Flow Matching Latent Engines

## 📝 Overview
Latent diffusion models (like Stable Diffusion) and Flow Matching models (like FLUX.1) utilize non-monotonic activations (GELU, Swish) to project continuous noise variables into target data distributions via ordinary differential equation (ODE) vector fields.

## 🧮 Mathematical Formulation
$$\text{ODE Trajectory: } \frac{dx}{dt} = v_t(x_t)$$

## 📊 Diagram
```mermaid
flowchart TD
    Noise[Gaussian Noise x_0] --> ODE["ODE Vector Field Integrator v_t(x_t)"]
    ODE --> Step["Smooth Activations mapping trajectories"]
    Step --> Image[Generated High-Fidelity Output x_1]
```

---

## 🔗 Navigation
- [Go back to README.md](../README.md)

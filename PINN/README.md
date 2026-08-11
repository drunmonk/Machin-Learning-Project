# Physics-Informed Neural Networks (PINNs) — PyTorch

PyTorch implementations of **Physics-Informed Neural Networks (PINNs)** for solving PDEs.

## Implemented

### 1. Burgers' Equation

Implemented a PINN to solve the 1D viscous Burgers' equation:

$$
u_t + uu_x = \nu u_{xx}
$$

### 2. Nonlinear Schrödinger Equation

Implemented a PINN for the nonlinear Schrödinger equation, predicting the real and imaginary components of the solution.

## Key Concepts

* Neural networks for PDE approximation
* Automatic differentiation with PyTorch
* PDE residual-based loss
* Initial and boundary conditions
* Physics-informed optimization

## Tech Stack

* Python
* PyTorch
* NumPy
* Matplotlib
* SciPy

## Goal

This project is part of my exploration of **Physics-Informed Machine Learning**, connecting my background in physics with deep learning and scientific computing.

## Reference

Based on the Physics-Informed Neural Networks work by **Raissi, Perdikaris & Karniadakis**.

🚧 **Work in Progress** — more PDEs and advanced PINN methods will be added.

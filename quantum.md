---
header: Quantum Mechanics
description: Physics for small things.
---

# Energy Quantization

In quantum mechanics, a photon's energy is released in discrete packets of energy called quanta.

It is characterized by the equation:

$$E = hv = \frac{hc}{v}$$

| Symbol | Meaning |
| ------ | ------- |
| $E$    | Energy of quanta |
| $h$    | Planck's Constant $6.626 \cdot 10^{-34} J \cdot s$ |
| v      | Frequency of radiation |

### Maximum Kinetic Energy of Photoelectron

$$K = \frac{1}{2}mv^2 = hv - \phi = hv - hv_0$$
$$v \geq v_0$$

$$\phi = h v_0$$

| Symbol | Meaning |
| ------ | ------- |
| $K$    | Max kinetic energy of photoelectron |
| $\phi$ | Work Function |
| v      | Frequency of radiation |

$\phi = hv_0$ is the minimum energy required to move an electron from the surface of a certain material. 

# Wave-Particle Duality

$$p = \frac{h}{\lambda}$$

# Heisenberg Uncertainty Principle

The Heisenberg uncertainty principle is especially useful for very small particles. It says that simultaneous measurements of two values has some error attached to it because of the scale.

$$\hbar = \frac{h}{2 \pi}$$

$$\Delta p \Delta x \geq \hbar$$

$$\Delta E \Delta t \geq \hbar$$

# The Wave Function

The wave function, $\Psi(x,t)$ describes the behavior of an electron in crystal.

It has the general form:

$$\Psi(x,t) = A e^{j(kx-\omega t)} + B e^{-j(kx-\omega t)}$$

### Probability Density Function

Alone, the wave function $\Psi(x, t)$ does not represent anything physcially. The probability density function,

$$|\Psi(x,t)|^2 = \Psi(x, t) \cdot \Psi^*(x,t)$$

represents the probability of finding the particle between $x$ and $x+dx$ at a certain time.

### Boundary Conditions

Given the [probability density function](#probability-density-function), $|\Psi(x)|^2$, we can say that, for a single particle:

$$\int_{- \infty}^\infty |\Psi(x)|^2 dx = 1$$

which states that over all of space, the probability of finding the particle is 100%.

# Schrodinger's Wave Equation

Schrodinger's wave equation describes the motion of electrons in a crystal and meshes the ideas of quantization and the wave-particle duality.

$$- \frac{\hbar^2}{2m} \cdot \frac{\partial^2 \psi(x,t)}{\partial x^2} + V(x) \psi(x, t) = j \hbar \frac{\partial \psi (x,t)}{\partial t} $$

### Electron in a Free Space

If an electron is in free space, it has no external forces acting on itself.

Therefore, we assume:

- $V(x) = 0$, the potential energy is zero.

### Infinite Potential Well



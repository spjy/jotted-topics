---
header: Electromagnetism
description: Electromagnetic forces.
---

# Coulomb's Law

Coulomb's law quantifies the relationship between two electrically charged particles. It is useful for finding the electric field due to **point charges**.

### Magnitude of Force

$$|F| = k_e \frac{q_1 q_2}{r^2}$$

- $q_1$ is the magnitude of the first charge.
- $q_2$ is the magnitude of the second charge.
- $k_e = 8.988 \times 10^9 N \cdot m^2 \cdot C^{-2} \text{}$
- $r$ is the distance between the two charges.

### Force Vector

$$\bold{F} = k_e \frac{q_1 q_2}{|\bold{r}_{21}|^2} \hat{\bold{r}}_{21} = k_e \frac{q_1 q_2}{|r_{21}|^2} \frac{\bold{r}_{21}}{|\bold{r}_{21}|}$$

- $q_1$ is the magnitude of the first charge.
- $q_2$ is the magnitude of the second charge.
- $k_e = 8.988 \times 10^9 N \cdot m^2 \cdot C^{-2} \text{}$
- $r_{21}$ is the vector from $q_2$ to $q_1$.

# Electric Field

### Electric Field Intensity

$$\bold{E} = \frac{\bold{F}_2}{q} = \frac{Q}{4 \pi \epsilon_0 R^2} \bold{r}$$

More generally,

$$\bold{E} = \sum_{i=1}^N \frac{Q_i}{4 \pi \epsilon_0 R_i^2} \bold{a}_{R_i}$$

# Electric Flux

The electric flux eminating from a charged sphere is proportional to the total charge of the sphere.

$$\psi_e = Q$$

### Electric Flux Density over Sphere

$$\bold{D} = \epsilon_0 \bold{E} = \frac{Q}{4 \pi r^2} \bold{a}_r$$

| Variable           | Meaning                                     |
| ------------------ | ------------------------------------------- |
| $\epsilon_0$       | $8.854 \times 10^{-12} F \cdot m^2 \text{}$ |
| $\bold{E} \text{}$ | Electric Field Intensity                    |
| $\bold{a}_r$       | Direction of Electric Flux Density          |

### Electric Flux over Closed Surface $s$

$$\Phi_E = \oint_s \epsilon_0 \bold{E} \cdot d\bold{s} = \frac{Q}{\epsilon_0}$$
---
header: Digital Image Processing
description: Changing images for the better (or worse).
---

# Finite Impulse Response Filters

$$y[m,n] = \sum_{k=-N}^N \sum_{l=-N}^N h[k,l] x[m-k,n-l]$$

# Edge Detection

## Continuous Time Gradient Methods

We can use the gradient of an image to find edges.

$$\nabla f(x,y) = \Bigg[\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \Bigg]$$

If the gradient is larger than some threshold $T$, we define those as edges.

$$e(x,y) = \begin{cases}
1 & |\nabla f(x,y)| > T \\
0 & \text{otherwise}
\end{cases}$$

## Discrete Time Gradient Methods

In order to find the gradient, we must use approximations using finite differences. In this case, it is the central difference:

$$\frac{\partial f(x,y)}{\partial x} \Big|_{x=m\Delta_x, y=n\Delta_y} \approx \frac{f[m+1,n]-f[m-1,n]}{2\Delta_x}$$

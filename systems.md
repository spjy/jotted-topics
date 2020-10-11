---
header: Systems
description: Big picture engineering.
---

# 1D Systems

## Continuous Time Fourier Transform

The Fourier Transform assists with analyzing signals in the frequency domain. It is a transform from the time domain to the frequency domain and decomposes a function into its frequencies, hence why it is multiplied by sinusoids.

$$F(f) = \int_{-\infty}^\infty f(t) e^{-i2\pi ft} dt$$

$$f(t) = \int_{-\infty}^\infty F(f) e^{i2\pi ft} df$$

## Continuous Time Signals

### Rectangle Function

$$\text{rect}(t) \triangleq 
\begin{cases}
  1 & |t| \leq 1/2 \\
  0 & \text{otherwise}
\end{cases}
$$

### Step Function

$$\text{step}(t) \triangleq 
\begin{cases}
  1 & t \geq 0 \\
  0 & t < 0
\end{cases}
$$

### Sign Function

$$\text{sign}(t) \triangleq 
\begin{cases}
  1 & t > 0 \\
  0 & t = 0 \\
  -1 & t < 0
\end{cases}
$$

### sinc Function

$$\text{sinc}(t) \triangleq \frac{sin(\pi t)}{\pi t}$$
$$\text{sinc}(0) \equiv \lim_{t \to 0} \frac{sin(\pi t)}{\pi t} = 1 \forall a \neq 0$$

### Lambda Function

$$\text{rect}(t) \triangleq 
\begin{cases}
  1 - |t| & |t| \leq 1 \\
  0 & |t| > 1
\end{cases}
$$

### Dirac Impulse

$$g(0) = \int_{-\infty}^\infty \delta(t) g(t) dt$$
$$g(t_0) = \int_{-\infty}^\infty \delta(t-t_0) g(t) dt$$
$$g(0) = \lim_{\epsilon \to 0} \int_{-\infty}^\infty \frac{1}{\epsilon} \text{rect}\Big(\frac{t}{\epsilon}\Big) g(t) dt$$
$$\delta (t) = \lim_{\epsilon \to 0} \frac{1}{\epsilon} \text{rect}\Big(\frac{t}{\epsilon}\Big)$$

# 2D Systems

## Continuous Space Fourier Transform 

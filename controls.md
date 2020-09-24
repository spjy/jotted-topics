---
header: Control Systems 
description: Analysis of preventing explosions.
---

# Frequency Modeling

## Transfer Function

An $n$th order LTI differential equation with output $c(t)$ and input $r(t)$ is defined as:

$$a_n \frac{d^n c(t)}{dt^n} + a_{n-1} \frac{d^{n-1} c(t)}{dt^{n-1}} + \dots + a_0 c(t) = b_m \frac{d^m c(t)}{dt^m} + b_{m-1} \frac{d^{m-1} r(t)}{dt^{m-1}} + \dots + b_0 r(t)$$

If we take the Laplace transform, the transfer function is defined as:

$$\frac{C(s)}{R(s)} = G(s) = \frac{b_m s^m + b_{m-1} s^{m-1} + \dots + b_0}{a_n s^n + a_{n-1} s^{n-1} + \dots a_0}$$

where the initial conditions are zero, or $a_0 = b_0 = 0$

## Linearization

If a nonlinear system is encountered, linearization of a system may be desired to simplify analysis. 

Given a point $(x_0, f_0)$, we can approximate a function $f(x)$ for a small range around that point:

$$f(x) - f(x_0) \approx \frac{df}{dx} \Big|_{x=x_0} (x-x_0)$$

$$\delta f(x) \approx m \Big|_{x=x_0} \delta x$$

# Time Response

Qualitative analysis of the transient response.

## Poles, Zeroes, System Response

A system's response consists of the sum of:
* Force Response
* Natural Response

## Poles

Poles of a transfer function cause it to become $\infty$ and also are any roots that the numerator and denominator share.

## Zeros

Zeros of a transfer function cause it to become $0$ and also are any roots that the numerator and denominator share.

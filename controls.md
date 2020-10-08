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

$$c(t) = c_{\text{forced}}(t) + c_{\text{natural}}(t)$$

The forced response consists of your input signal, whereas the natural response is what occurs in the system after the input.

## Poles

Poles of a transfer function cause it to become $\infty$ and also are any roots that the numerator and denominator share.

## Zeros

Zeros of a transfer function cause it to become $0$ and also are any roots that the numerator and denominator share.

## First Order System

The step response of a first order system is characterized by:

$$C(s) = R(s) G(s) = \frac{a}{s(s+a)}$$
$$c(t) = 1 - e^{-at}$$
$$c_{\text{forced}}(t) = 1$$
$$c_{\text{natural}}(t) = -e^{-at}$$

### Time Constant

The time constant is the time for the natural response e^{-at} to reach 63% of its final value.

$$\tau = \frac{1}{a}$$

### Rise Time

The rise time is the time to go from 0.1 $\rightarrow$ 0.9 of its final value.

$$T_r = \frac{2.2}{a}$$

### Settling Time

The settling time is the time at which the signal remains within $\pm$ 2% of the final value.

$$T_s = \frac{4}{a}$$

## Second Order System

The step response of a second order system is:

$$C(s) = G(s)R(s) = \frac{\omega_n^2}{s(s^2+2\zeta s+\omega_n^2)}$$

### Natural Frequency $\omega_n$

The natural frequency is the oscillation frequency of the system without damping.

### Damping Ratio $\zeta$

The damping ratio quantifies how much of the natural response's frequency is reduced.

Generally, a lower $\zeta$ corresponds to more oscillations (less dampening).

### Pole Locations

The pole locations of a second order system can be easily calculated from the natural frequency and damping ratio:

$$s_{1,2} = -\zeta w_n \pm w_n \sqrt{\zeta^2 - 1}$$

### Rise Time

See [rise time](#rise-time).

$$T_r = \frac{\pi - \tan^{-1}\frac{\sqrt{1-\zeta^2}}{\zeta}}{\omega_n (1-\zeta)}$$

### Peak Time

The peak time is the time to reach the maximum.

$$T_p = \frac{\pi}{\omega_n \sqrt{1-\zeta^2}}$$

### Percent Overshoot

The percent overshoot is how much the waveform overshoots the steady state value. It is the difference between the peak and the steady state value, expressed in terms of a percentage.

$$OS = e^{-(\zeta \pi / \sqrt{1-\zeta^2})}$$

### Settling Time 

See [settling time](#settling-time).

$$T_s = \frac{4}{\zeta \omega_n}$$

### Response Types

There are four types of responses to a second order transfer function.

#### Undamped ($\zeta = 0$)

The undamped case is where the transfer function freely oscillates with no damping at all.

#### Underdamped (0 < $\zeta$ < 1)

The underdamped case is the case where the transfer function has remnants of the undamped signal. It oscillates, but at a relatively lower frequency.

The poles are complex.

$$s_{1,2} = -\zeta \omega_n \pm \omega_n j \sqrt{1 - \zeta^2}$$

#### Critically Damped ($\zeta = 1$)

The critically damped case is the border between underdamped and overdamped case.

The poles are real and repeating.

$$s_{1,2} = -\omega_n$$

#### Overdamped ($\zeta > 1$)

The overdamped case is where the damping ratio has a large impact on the signal and oscillations are less apparent.

The poles are real and distinct.

$$s_{1,2} = -\zeta w_n \pm w_n \sqrt{\zeta^2 - 1}$$

### Dominant Pole Analysis 
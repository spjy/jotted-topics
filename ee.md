---
header: Electrical Engineering
description: Coulomb movements.
---

# Charge (q)

Measurement of the electrical property of atomic particles in coulombs (C) and is represented as the variable $q$. The charge of an electron is often denoted as the constant value:

$$e = -1.602 \times 10^{-19} C$$

Note:
1. In $1\text{C}$ of charge, there are $\displaystyle \frac{1}{1.602 \times 10^{-19}} = 6.24 \times 10^{18}$ electrons.
2. The charges that occur in nature are integral multiples of the electric charge $e$.
3. The law of conservation of charge states charge cannot be created or destroyed.

# Current (i)

Current is the time rate of change of charge and is represented as the variable $i$. Its unit of measurement is denoted as amperes (A). An ampere is equivilent to a $\text{coulomb / second}$.

$$i = \frac{dq}{dt}$$

The charge transferred between two time points is denoted as:

$$q = \int_{t_0}^t i \text{ } dt$$

## Types of Currents

#### Direct Current (DC)

DC current is one that flows in only one direction.

#### Alternating Current (AC)

AC current is one that changes direction with respect to time.

# Voltage (v)

Voltage is the potential difference between two points and is reepreseented as the variable $v$. In other words, it is the energy required to move from one point $a$ to another point $b$. Its unit of measurement is denoted as volts (V). A volt is equivilent to a $\text{joule / coulomb}$ or a $\text{newton} \cdot \text{meter / coulomb}$. Voltage is denoted as change in work over the change in charge:

$$v_{ab} = \frac{dw}{dq}$$

This means that a volt would deliver one joule of energy when one coulomb passes through a load.

# Power (p)

Power is the time rate of expending or absorbing energy and is represented as the variable $p$. Its unit of measurement is denoted as watts (W). A watt is equivilent to one $\text{joule / second}$.

$$p=\frac{dw}{dt}=vi$$

Conversely, we can calculate the energy absorbed:

$$w=\int_{t_0}^t p \text{ } dt = \int_{t_0}^t vi \text{ } dt$$

Note:
1. Positive power means power ($p=+vi$) is being absorbed.
2. Negative power means power ($p=-vi$) is being released.
3. The law of conservation of power states energy cannot be created or destroyed.

# Energy (w)

Energy is the ability to do work and is measured in joules (J).

# Circuit Elements

An electric circuit is a collection of connected elements.

## Types of Circuit Elements

#### Passive Circuit Element
A passive circuit element is not capable of generating electricity.

#### Active Circuit Element
A passive circuit element is capable of generating electricity.

## Types of Sources

#### Ideal Independent Source
An ideal independent source is an active circuit element that provides a pre-determined voltage or current independent of other circuit elements.

#### Ideal Dependent Source
An ideal dependent source is an active circuit element where the voltage or current is determined by its surrounding circuit elements.

# Resistance (R)
The resistance is the ability for an element to resist the flow of charge and is denoted by the variable $R$. Its unit of measure is ohms ($\Omega$). An ohm is equivilent to one $\text{volt / amp}

It depends on the material's length ($l$), cross sectional area ($A$) and resistivity ($\rho$).

$$R=\rho \frac{l}{A}$$

Note:
1. When $\displaystyle i=\lim_{R \rightarrow \infty} \frac{v}{R}=0$, or an element has no resistance, it is said to be a short circuit.
2. When $R=\infty$, or an element has infinite resistance, it is said to be an open circuit.

# Ohms Law
Ohm's law states voltage and current are directly proportional.

$$v=iR$$

# Circuit Topology

#### Branch (b)
A branch is a circuit element.

#### Node (n)
A node is a connection between two branches.

#### Loop (l)
A loop is a closed path within the circuit.

Branches, nodes and loops are connected by the equation:

$$b=l+n-1$$

Note:
1. If 2+ branches share a single node, they are said to be in series and have the same current.
2. If 2+ branches share 2+ nodes, they are said to be in parallel and have the same voltage.

# Kirchhoff's Laws

#### Kirchhoff's Current Law (KCL)
The sum of currents entering a node is zero.

$$\sum_{n=1}^N i_n=0$$

#### Kirchhoff's Voltage Law (KVL)
The sum of voltages around a loop is zero.

$$\sum_{m=1}^M v_m=0$$

# Equivilent Resistance

#### Series Resistance Addition
For resistors in series, the equivilent resistance is merely the sum of each resistance. For $n$ resistors in series:

$$R_{eq}=\sum_{n=1}^N R_n$$

#### Parallel Resistance Addition
For resistors in parallel, the equivilent resistance is the product of each resistance divided by their sum. For $n$ resistors in parallel:

$$\frac{1}{R_{eq}}=\frac{1}{R_{1}} + \frac{1}{R_{2}} + \ldots + \frac{1}{R_{n}}$$

# Voltage Division
For $N$ resistors in series with a source voltage $v$, the $n$th resistor has the voltage drop of:

$$\displaystyle v_n=\frac{R_n}{R_1+R_2+\ldots+R_N} v$$

# Current Division
For two resistors in parallel attached to a current source $i$, the current over resistor $R_1$ is:

$$\displaystyle i_1=\frac{R_2 \text{ } i}{R_1+R_2}$$

# Wye-Delta Transformations
Resistors can appear to not be in a parallel or series configuration. Wye-Delta ($Y-\Delta$) transformations solve this issue of combining resistors when this situation arises.

A $Y$ resistor configuration can be re-arranged into a $\Pi$ resistor configuration, while the $\Delta$ resistor configuration can be re-arranged to look like a $T$. This is called the $\Pi-T$ configuration.

For a $\Delta \rightarrow Y$ transformation:

$$R_1=\frac{R_b R_c}{R_a+R_b+R_c}$$
$$R_2=\frac{R_c R_a}{R_a+R_b+R_c}$$
$$R_3=\frac{R_a R_b}{R_a+R_b+R_c}$$

For a $Y \rightarrow \Delta$ transformation:

$$R_a = \frac{R_1R_2+R_2R_3+R_3R_1}{R_1}$$
$$R_b = \frac{R_1R_2+R_2R_3+R_3R_1}{R_2}$$
$$R_c = \frac{R_1R_2+R_2R_3+R_3R_1}{R_3}$$

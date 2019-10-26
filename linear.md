---
header: Linear Algebra
description: The study of linear equations.
---

## Linear Equations

A linear equation can be expressed as

$$y=a_1x_1 + a_2x_2 + a_3x_3 + ... + a_nx_n = b$$

where $a_1, a_2, a_3, ... , a_n, b$ are scalar coefficients and $x_1, x_2, x_3, ..., x_n$ are variables.

### Homogenous System of Linear Equations

A homogenous system of linear equations takes the form

$$a_{11}x_1+a_{12}x_2+...+a_{1n}x_n=0
\newline
\newline \vdots
\newline
a_{m1}x_1+a_{m2}x_2+...+a_{mn}x_n=0$$

This is system of linear equations is homogenous because the solution to the system has at least one trivial solution, $x_1=x_2= ... =x_n=0$.

#### Theorem of Homogenous Systems

A homogenous system with $n$ variables and $m$ equations has $\infty$ solutions if $n>m$.

## Augmented Matrix

Given a system of linear equations

$$a_{11}x_1+a_{12}x_2+...+a_{1n}x_n=b_1
\newline
\newline \vdots
\newline
a_{m1}x_1+a_{m2}x_2+...+a_{mn}x_n=b_n$$

We can extract the coefficients transform the system into an augmented matrix:

$$\left[
\begin{array}{cccc:c}
a_{11} & a_{12} & \dots & a_{1n} & b_1 \\ 
\vdots & \vdots & \ddots & \vdots & \vdots \\ 
a_{m1} & a_{m2} & \dots & a_{mn} & b_n \\
\end{array}
\right]$$

## Reduced Row Echelon Form

1. Any rows of zeroes are at the bottom.
2. The first non-zero entry of a non-zero row is one (1).
3. Starting from the top left, the leading one (1) appears to the right of the leading one (1) of the preceding row.
4. All other entries of a column containing a leading one (1) is zero (0).

## Scalars

A scalar is a single number.

## Vectors

A vector is column of an array numbers.

### Notation

$$ \bold{A} =
\left[
\begin{array}{c}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{array}
\right]$$

where $n$ is the number of rows in the vector.

## Matrices

A matrix is a two dimensional collection of numbers with a fixed number of rows and columns, of the form:

### Notation

$$ \bold{A}_{mn} =
\left[
\begin{array}{ccccc}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\ 
a_{m1} & a_{m2} & \dots & a_{mn} \\
\end{array}
\right]$$

where $A$ is an $m \times n$ matrix and $m$ are the rows and $n$ are the columns.

More generally,

$$\bold{A} =
\left[
\begin{array}{c}
a_{ij} 
\end{array}
\right]$$

$A$ is an $i \times j$ matrix where $i$ is the number of rows and $j$ is the number of columns.

### Rows

$\bold{A}_{i,:}$ denotes the $i$-th row of matrix $A$.

### Columns

$\bold{A}_{:,j}$ denotes the $j$-th column of matrix $A$.

### Entries

$\bold{A}_{i,j}$ denotes the $(i,j)$-th element of matrix $A$.

### Properties

Let

$$A =
\left[
\begin{array}{c}
a_{ij} 
\end{array}
\right]$$

$$B =
\left[
\begin{array}{c}
b_{ij} 
\end{array}
\right]$$

$$C =
\left[
\begin{array}{c}
c_{ij} 
\end{array}
\right]$$

and $c,d$ be scalars.

#### Addition

$$A + B =
\left[
\begin{array}{c}
a_{ij} + b_{ij}
\end{array}
\right]$$

#### Scalar Product

$$
c\bold{A} =
c \left[
\begin{array}{c}
a_{ij}
\end{array}
\right]
=
\left[
\begin{array}{c}
c a_{ij}
\end{array}
\right]
$$

#### Commutativity

$$\bold{A} + \bold{B} = \bold{B} + \bold{A} \text{}$$

#### Associativity

$$\bold{A} + (\bold{B} + \bold{C}) = (\bold{A} + \bold{B}) + \bold{C} \text{}$$

#### Scalar Distributivity

$$c(d\bold{A}) = (cd)\bold{A}$$

$$c(\bold{A} + \bold{B}) = c\bold{A} + d \bold{B}$$

$$(c + d) \bold{A} = c \bold{A} + d \bold{A}$$

#### Negativity

$$-\bold{A} =
\left[
\begin{array}{c}
- a_{ij}
\end{array}
\right]
$$

## Tensors

A tensor is a generalized form of vectors and scalars.

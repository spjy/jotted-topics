---
header: Discrete Math
description: Integer number of things.
---

# Basics of Math

### Variables

Variables are a placeholder for an unknown value to generalize it.

### Mathematical Statements

| Type        | Description                     | Example           |
| ----------- | ------------------------------- | ----------------- |
| Universal   | True for all elements in a set. | "For all ..."     |
| Conditional | True under a constraint.        | "If ... then ..." |
| Existential | True for at least one element.  | "There is a ..."  |

# Set Notation

A set is a collection of elements.

### Set Roster Notation

$$S = \left\{ x, y, z \right\}$$

### Symbols

| Symbol | Meaning      | Example   |
| ------ | ------------ | --------- |
| $\in$  | in           | $x \in S$ - "$x$ is an element of $S$" |
| $\dots$| and so forth | $\left\{ 1, 2, 3, ... \right\}$ - "Set of all positive integers" |
| $\mathbb{R} \text{}$ | Set of all real numbers | - |
| $\mathbb{Z} \text{}$ | Set of all integers | - |
| $\mathbb{Q} \text{}$ | Set of all rational numbers, quotients of integers | - |

### Axiom of Extension

A set is defined by its elements, not its element's order or frequency.

### Set Builder Notation

Set builder notation is a shorthand method to describe a set's elements. We can write it like:

| Notation                                     | Translation |
| -------------------------------------------- | ----------- |
| $\left\{ x \in S \mid P(x) \right\} \text{}$ | The set of all elements $x$ in $S$ such that $P(x)$ is true. | 

For instance, these two sets are equivilent:

$$\left\{ x \in \mathbb{R} \mid 10 \le x \le 15 \right\} = \left\{10, 11, 12, 13, 14, 15 \right\}$$

### Subset

Let $A$ and $B$ be sets. If $A$ is a subset of $B$, or $A \subseteq B$, then each element of $A$ is also an element of $B$.

| Notation         | Translation |
------------------ | ----------- |
| $A \subseteq B$  | $\forall$ elements $x$, if $x \in A$ then $x \in B$. | 
| $A \subsetneq B$ | There is at least one element $x \mid x \in A, x \not\in B$ |

#### Subset Example

Let's say $A$ and $B$ are sets.

$$A = \left\{ 1,2,3 \right\}$$
$$B = \left\{ 1,2,3,4 \right\}$$

$A \subseteq B$ because each element $x$ (1, 2 and 3) in $A$ exists in $B$.

#### Non-Subset Example

Let's say $A$ and $B$ are sets.

$$A = \left\{ 1,2,3 \right\}$$
$$B = \left\{ 1,2,4 \right\}$$

$A \subsetneq B$ because the element $3$ in $A$ does not exist in $B$.

### Proper Subset

- Let $A$ and $B$ be sets.
- If $A$ is a proper subset of $B$, then each element of $A$ is in $B$.
- There is at least one element of $B$ not in $A$.

In other words, $A$ cannot equal $B$. There must be at least one element that differs between the two sets.

### Ordered Pair

- Let $a$ and $b$ be elements.
- $(a, b)$ is an ordered pair with $a$ and $b$ together such that $a$ is the first element of the pair and $b$ is the second. 

Let $c$ and $d$ be two other elements, and let $(c, d)$ be another ordered pair. 

$(a, b)$ = $(c, d)$ is true if $a=c$ and $b=d$.

### Cartesian Product

- Let $A$ and $B$ be sets.
- The Cartesian product of $A$ and $B$, or $A \times B$, is the set of all ordered pairs $(a, b)$ such that $a \in B$ and $b \in B$ is:

$$A \times B = \left\{ (a, b) \mid a \in A, b \in B \right\}$$

#### Cartesian Product Example

Let $A = \left\{ 1, 2 \right\}$ and $\left\{ 3, 4 \right\}$. The Cartesian product of $A$ and $B$ is:

$$A \times B = \left\{ (1, 2), (1, 4), (2, 3), (2, 4) \right\} \text{}$$

#### Relationships

- Let $A$ and $B$ be sets.
- A relation $R$ from $A$ to $B$ is a subset of $A \times B$ ($R \subseteq A \times B$).

Now we can say:

- An ordered pair $(x, y) \in A \times B$, $x$ is related to $y$ by $R$, or $x$ $R$ $y$, iff $(x, y) \in R$.
- $A$ is the domain of $R$ and $B$ is the co-domain.
- $x$ $R$ $y$ means $(x,y) \in R$.
- $x$ $\not{R}$ $y$ means $(x,y) \not\in R$.


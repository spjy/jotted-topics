---
header: Probability
description: Probably relevant.
---

# Probabilistic Models

### Experiment

The problem at hand.

### Outcome

The results of the [experiment](#experiment).

### Sample Space ($\Omega$)

The set of all possible [outcomes](#outcome) of an [experiment](#experiment).

### Event

A subset of the [sample space](#sample-space-omega) containing the possible [outcomes](#outcome).

### Mutual Exclusivity (Disjointness)

Elements of the [sample space](#sample-space-omega) should be distinct.

### Collectively Exhaustive

All of the [events](#event) must be accounted for in the [sample space](#sample-space-omega).

# Probability Axioms

### Non-negativity

For each event $A$, 

$$\bold{P}(A) \geq 0$$

### Additivity

If the sets $A$ and $B$ are [disjoint](/sets/#disjoint) events, then:

$$\bold{P}(A \cup B) = \bold{P}(A) + \bold{P}(B)$$

### Normalization

The probability of the [sample space](#sample-space-omega) is equal to $1$.

$$\bold{P}(\Omega) = 1$$

# Discrete Models

### Discrete Probability

The probability of an event $\left\{s_1, s_2, ..., s_3\right\}$ is the sum of of the probabilities of its elements:

$$\bold{P}(\left\{s_1, s_2, ..., s_3\right\}) = \bold{P}(s_1) + \bold{P}(s_2) + ... + \bold{P}(s_n) $$

### Discrete Uniform Probability Law

Given an event $A$ with $n$ possible outcomes, the probability of any event $A$ is:

$$\bold{P}(A) = \frac{\text{number of elements of A}}{n}$$

# Conditional Probability

When only partial information is given and we want to know the outcome of an experiment, conditional probability is useful.

Let $A$ and $B$ be two events. The conditional probability of $A$ given $B$ is denoted as:

$$\bold{P}(A|B) = \frac{\bold{P}(A \cap B)}{\bold{P}(B)} = \frac{\text{number of elements} \in A \cap B}{\text{number of elements} \in B}$$

where $\bold{P}(B) \gt 0$.

In other words, the conditional probability is the ratio of $A$ and $B$ occurring to the probability of $B$ occurring. $B$ has already occurred, and so the only probability left of occurring is intersect between $A$ and $B$.

## Multiplication Rule

Assuming all of the conditioning events have positive probability,

$$\bold{P}(\bigcap^n_{i=1} A_i = \bold{P}(A_1) \bold{P}(A_2|A_1)\bold{P}(A_3|A_1 \cap A_2) ... \bold{P}(A_n | \bigcap^{n-1}_{i=1}) A_i)$$

This rule is often seen when multiplying independent events together in a tree diagram.

## Total Probability Theorem

Let $A_1 ... A_n$ be disjoint events that form a partition of the sample space and assume $\bold{P}(A_i) > 0 \forall i$. For any event $B$,

$$\bold{P}(B) = \bold{P}(A_1 \cap B) + ... + \bold{P}(A_n \cap B) \\
= \bold{P}(A_1)\bold{P}(B|A_1) + ... + \bold{P}(A_n)\bold{P}(B|A_n)$$

This theorem is often seen when adding together various event outcomes to calculate the probability of an event occurring.

## Bayes' Rule

Bayes' rule is used when finding the reversed conditional probability. 

$$\bold{P}(A_i | B) = \frac{\bold{P}(A_i)\bold{P}(B | A_i)}{\bold{P}(B)} = \frac{\bold{P}(A_i) \bold{P}(B|A_i)}{\bold{P}(A_1) \bold{P}(B|A_1) + ... + \bold{P}(A_n) \bold{P}(B|A_n)}$$

# Independence

$A$ is independent of $B$ if 

$$\bold{P}(A|B) = \bold{P}(A) = \frac{\bold{P}(A \cup B)}{\bold{P}(B)}$$

Also, if $\bold{P}(B) > 0$

$$\bold{P}(A|B) = \bold{P}(A)$$

# Counting Principle

Let's say there is a process consisting of $r$ stages.
- $n_1$ possible results in the first stage. 
- For every possible result of the first stage, there are $n_2$ possbile results at the second stage.

### $k$-permutations

Let's say we want to count the number of permutations with $n$ distinct objects, but we only have room to choose $k$ objects.

- $n$ distinct objects
- Pick only $k$ out of $n$ objects
- Order matters (number of arrangements)
- $n \geq k$

$$\frac{n!}{(n-k)!}$$

### Permutations

Let's say we have $n$ distinct objects and have $n$ spots. In other words, $n = k$. We aim to find how many sequences there are when choosing $k$ balls.

#### With Replacement

For the first spot, there are $n$ possibilities. Then, for the next spot, we replace the object, so the number of possibilities stays the same as the first, $n$.

We continue this until $k$.

$$n \cdot n \cdot n \cdots = n^k$$

#### Without Replacement

$$P^n_k = n(n-1)(n-2) \cdots 2 \cdot 1 = n!$$

For the first spot, there are $n$ possibilities. Then, for the next spot, we do not replace the object, so we lose one possibility; thus we are left with $n-1$ possibilities.

We continue this until $n - (k - 1)$.

### Combinations

#### Without Repetition

Let's say we want to count the number of combinations with $n$ distinct objects, but we only want to choose $k$ objects.

- $n$ distinct objects
- Pick only $k$ out of $n$ objects
- Order doesn't matter
- $n \geq k$

$${ n \choose k } = \frac{n!}{k!(n-k)!}$$

# Partitions

Let's say we wanted to split $n$ distinct objects into $r$ groups, and those groups are of size $n_1, n_2, \ldots, n_r$ where $n_1 + n_2 + \ldots + n_r = n$. 

In other words, $n_1, n_2, \ldots, n_r$ is just the partition of $n$.

We use the counting principle and define it as the multinomial coefficient,

$${n \choose n_1,n_2,\ldots, n_r} = {n \choose n_1} {n - n_1 \choose n_2} {n - n_1 - n_2 \choose n_3} \cdots {n - n_1 - \ldots - n_{r-1} \choose n_r}$$

$$\frac{n!}{n_1!(n-n_1)!} \cdot \frac{(n-n_1)!}{n_2!(n-n_1-n_2)!} \cdots \frac{n-n_1-\ldots-n_{r-1}!}{n_r!(n-n_1-\ldots-n_{r-1} - n_r)!}$$

First, we choose $n_1$ objects to insert into the first group from the pool of $n$.

Next, from the remaining pool of $n - n_1$, we choose however many objects we want to insert into group $n_2$.

We repeat this until the group $r$.

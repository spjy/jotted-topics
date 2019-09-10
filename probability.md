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

For each event $A$, $P(A) \geq 0$.

### Additivity

If the sets $A$ and $B$ are [disjoint](/sets/#disjoint) events, then:

$$P(A \cup B) = P(A) + P(B)$$

### Normalization

The probability of the [sample space](#sample-space-omega) is equal to $1$.

$$P(\Omega) = 1$$

# Discrete Models

### Discrete Probability

The probability of an event $\left\{s_1, s_2, ..., s_3\right\}$ is the sum of of the probabilities of its elements:

$$P(\left\{s_1, s_2, ..., s_3\right\}) = P(s_1) + P(s_2) + ... + P(s_n) $$

### Discrete Uniform Probability Law

Given an event $A$:

$$P(A) = \frac{\text{number of elements of A}}{n}$$

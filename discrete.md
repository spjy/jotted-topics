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
| $\mathbb{R} \text{}$ | Set of all real numbers | $\left\{ ..., -1, -\frac{1}{2}, 0, \frac{1}{2}, 1, ... \right\}$ |
| $\mathbb{Z} \text{}$ | Set of all integers | $\left\{ ..., -2, -1, 0, 1, 2, ... \right\} \text{}$ |
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

# Relations and Functions

### Cartesian Product

- Let $A$ and $B$ be sets.
- The Cartesian product of $A$ and $B$, or $A \times B$, is the set of all ordered pairs $(a, b)$ such that $a \in B$ and $b \in B$ is:

$$A \times B = \left\{ (a, b) \mid a \in A, b \in B \right\}$$

#### Cartesian Product Example

Let $A = \left\{ 1, 2 \right\}$ and $\left\{ 3, 4 \right\}$. The Cartesian product of $A$ and $B$ is:

$$A \times B = \left\{ (1, 2), (1, 4), (2, 3), (2, 4) \right\} \text{}$$

### Relationships

A relationship is the connection between two different things.

- Let $A$ and $B$ be sets.
- A relation set $R$ from $A$ to $B$ is a subset of $A \times B$ ($R \subseteq A \times B$).

Now we can say:

- An ordered pair $(x, y) \in A \times B$, we can state $x$ is related to $y$ by $R$, or $x$ $R$ $y$ iff $(x, y) \in R$.
- $A$ is the domain of $R$ and $B$ is the co-domain.
- $x$ $R$ $y$ means $(x,y) \in R$.
- $x$ $\not{R}$ $y$ means $(x,y) \not\in R$.

### Functions

A function $F$ from a set $A$ to set $B$ is the relationship between the domain $A$ and co-domain $B$. It has the restrictions that:

- $\forall x \in A, \exists y \in B \mid (x,y) \in F$
- $\forall x \in A$ and $y,z \in B$, if $(x, y) \in F$ and $(x,z) \in F \implies y=z$

In other words, for each $x$ in the domain, there exists a value for $x$ in the co-domain. Additionally, each element $x$ in the domain may map to exactly one value $y$ in the co-domain.

#### Function Notation

If $A$ and $B$ are sets and $F$ is a function from $A$ to $B$, then given any element $x \in A$, the unique element in $B$ that is related to $x$ by $F$ is $F(x)$, read as F of x.

#### Function Mapping Notation

Let $A$ and $B$ be sets and $f$ be a function. If $x \in A$ and $y \in B$, a function $f: A \rightarrow B$ is defined by $f: x \mapsto y$ means $f(x) = y$, the domain is defined on the set $A$ and the co-domain is defined on the set $B$.

# Logic and Statements

### Logical Connective Symbols

| Symbol   | Meaning           |
| -------- | ----------------- |
| $\lnot$  | negation (not)    |
| $\wedge$ | conjunction (and) |
| $\vee$   | disjunction (or)  |

### Structure

A compound statement is composed of:

- [Premises](#premise): Statements.
- [Conclusion](#conclusion): An assertion based on premises.

It usually takes the form of: 

If $p$ or $q$, then $r$. $q$. Therefore, $r$.

There is also:

| Structure           | Translation      |
| ------------------- | ---------------- |
| $p$ but $q$         | $p \wedge q$     |
| neither $p$ nor $q$ | $\lnot p$ $\vee$ $\lnot q$ |

### Statements

A statement is a sentence that is true or false but not both.

#### Statement Examples

- True: $1+1 = 2$
- False: $1+1 = 3$

#### Non-statement Examples

- $x + y > 0$ since it is true for some values but not for values $x + y \leq 0$

### Statement (Propositional) Form

A statement form is one that contains statement variables and [logical connectives](#logical-connective-symbols) only.

For example, the statement form of "$\text{My clothes are }$$\underbrace{\text{clean}}_p$ $\text{and not }$$\underbrace{\text{wrinkled}}_q$" would be $p$ $\wedge$ $\lnot q$.

### Truth Table

A truth table contains all of the possible combinations of a statement.

### Negation Truth Table

| $p$ | $\lnot p$ |
| - | - |
| T | F |
| F | T |

### Conjunction Truth Table

| $p$ | $q$ | $p \wedge q$ |
| - | - | - |
| T | T | T |
| T | F | F |
| F | T | F |
| F | F | F |

### Disjunction Truth Table


| $p$ | $q$ | $p \vee q$ |
| - | - | - |
| T | T | T |
| T | F | T |
| F | T | T |
| F | F | F |

### Logical Equivalence

Being logically equivalent means that two statement forms have identical truth values for each combination possibility.

If $P$ and $Q$ are two [statement forms](#statement-propositional-form) and they are logically equivalent, then $P \equiv Q$.

### Tautology

A statement form that is always true in every interpretation.

### Contradiction

A statement form that is always false in every interpretation.

#### Tautology and Contradiction Example

A tautology is denoted as $t$, while a contradiction is denoted as $c$.

| $p$ | $\lnot p$ | $p \lor \lnot p$ | $p \land \lnot p$ |
| --- | - | - | - |
| T | F | T | F |
| F | T | T | F |

$p \lor \lnot p$ is the definition of a tautology. All interpretations are true.

$p \land \lnot p$ is the definition of a contradiction. All interpretations are false.

# Conditional Statements

A conditional statement has the form: If $p$ then $q$. More formally, the notation is $p \rightarrow q$, which means $p$ implies $q$.

The truthfulness of $q$ is dependent on the statement of $p$.

### Hypothesis (Antecedent)

The if statement ($p$).

### Conclusion (Consequent)

The then statement ($q$).

### Conditional Statement Truth Table

| $p$ | $q$ | $p \rightarrow q$ |
| - | - | - |
| T | T | T |
| T | F | F |
| F | T | T |
| F | F | T |

### Vacuously True

An if statement is **vacuously true** (true by default) if the hypothesis is false.

### Negation of Conditional Statement

$$\lnot (p \rightarrow q) \equiv p \land \lnot q$$

### Contrapositive of Conditional Statement

$$p \rightarrow q \equiv \lnot q \rightarrow \lnot p$$

### Converse of Conditional Statement

Let "$p \rightarrow q$" be a conditional statement.

The **converse** of the statement is:

$$q \rightarrow p$$

### Inverse of Conditional Statement

Let "$p \rightarrow q$" be a conditional statement.

The **inverse** of the statement is:

$$\lnot p \rightarrow \lnot q$$

### Only If

$p$ only if $q$ means $p$ is true if $q$ is true, or in other words:

$$\lnot q \rightarrow \lnot p \equiv p \rightarrow q$$

### Biconditional

Let $p$ and $q$ be statement variables.

The **biconditional** of $p$ and $q$ is "$p$ if and only if (iff) $q$":

$$p \leftrightarrow q$$


### Sufficient Condition

Let $r$ be a **sufficient condition** for $s$. This means:

$$r \rightarrow s$$

or $r$ is sufficient to guarantee $s$ is true.

### Necessary Condition

Let $r$ be a **necessary condition** for $s$. This means:

$$\lnot r \rightarrow \lnot s$$

or if $r$ is false, $s$ is false.

### Sufficient and Necessary Condition

Let $r$ be a **sufficient and necessary** condition. This means:

$$r \leftrightarrow s$$

# Arguments

An argument is a sequence of statements.

### Argument Form

An argument form is the sequence of [statement forms](#statement-propositional-form).

### Premise

**Premises** are statements in an argument and all statement forms in an argument form except the final one.

### Conclusion

A **conclusion** is the final statement or statement form.

# Valid Argument Form

A **valid argument form** means if the premises are all true, the conclusion is true.

#### Critical Row

The **critical row** is the row of a truth table where all of the premises are true.

An argument form is said to be invalid if the [conclusion](#conclusion) is false in the critical row.

### Modus Ponens

**Modus Ponens** is a [valid argument form](#valid-argument-form) that says the conclusion is affirmed. It has the form:

$$
p \rightarrow q. \\
p. \\
\therefore q
$$



### Modus Tollens

**Modus Tollens** is a [valid argument form](#valid-argument-form) that says the conclusion is a denial. It is [logically equivalent](#logical-equivalence) to [Modus Ponens](#modus-ponens) through the [contrapositive](#contrapositive-of-conditional-statement) identity. It has the form:

$$
p \rightarrow q. \\
\lnot q. \\
\therefore \lnot p.
$$

### Rule of Inference

A **rule of inference** is a [valid argument form](#valid-argument-form).

#### Generalization

$$
p. \\
\therefore p \lor q.
$$

$$
q. \\
\therefore p \lor q.
$$

#### Elimination

$$
p \lor q. \\
\lnot q. \\
\therefore p.
$$

$$
p \lor q. \\
\lnot p. \\
\therefore q.
$$


#### Transitivity

$$
p \rightarrow q. \\
q \rightarrow r. \\
\therefore p \rightarrow r.
$$

### Division into Cases

$$
p \lor q. \\
p \rightarrow r. \\
q \rightarrow r. \\
\therefore r.
$$

### Sound Argument

An argument is **sound** iff it is valid and all its premises are true.

### Unsound Argument

An argument that is not sound.

# Fallacy (Invalid Argument)

A fallacy is an invalid argument due to an error in reasoning. In other words, the [critical row](#critical-row) contains [premises](#premise) that are true but the [conclusion](#conclusion) is false.

### Converse Error

The following argument is **invalid**:

$$
p \rightarrow q. \\
q. \\
\therefore p.
$$

### Inverse Error

The following argument is **invalid**:

$$
p \rightarrow q. \\
\lnot p. \\
\therefore \lnot q.
$$

# Contradictions

If the statement $p$ is false and leads logically to a contradiction, you can conclude $p$ is true.

$$
\lnot p \rightarrow c \\
\therefore p
$$

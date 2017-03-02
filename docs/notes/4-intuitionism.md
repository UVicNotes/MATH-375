# Intuitionism

Intuitionism is motivated by philosophical problems. The intuitionists view of infinite sets is that they are human constructions.

## Logic

**Example**

Consider,

$$
    A \wedge B
$$

In classical logic, you might say "Both $A$ and $B$ are true". But the intuitionist says "I have a proof for $A$ and a proof for $B$".

### Operations

* $A \wedge B$ &ndash; "I have a proof for $A$ and a proof for $B$"
* $A \vee B$ &ndash; "I have a proof for $A$ or I have a proof for $B$"
* $\neg A$ &ndash; "I can prove $A$ leads to a $\perp$"
* $A \to B$ &ndash; "If I can prove $A$ then I have a proof of $B$"

**Example**

Consider,

$$
    A \vee \neg A
$$

If I can't prove $A$ can I prove that $A$ leads to $\perp$? Not necessarily. Yay intuitionism.

### Quantification

* $\forall x F x$ &ndash; "I can prove $Fn$ for any number $n$"
* $\exists x F x$ &ndash; "I can prove $Fn$ for some specific $n$"

## Real Numbers

We can generate the fractions, $\mathbb Q$, using the natural numbers. For the fractions, if $a < b$, there is some $c$ such that $a < c < b$.

A **cut** in $\mathbb Q$ is a pair of disjoint sets $A$, $B$ such that $A \cup B = \mathbb Q$, $A \cap B = \varnothing$, and $\forall x \in A \forall y \in B, x < y$.

### Cauchy Sequences

$\{ a_n \}$ is Cauchy when:

$$
    \forall k \in \mathbb Z^+ \exists N \in \mathbb Z^+ \forall m,n >N \left( | a_m - a_n| < \frac{1}{k} \right)
$$

then, 

$$
    a_k = \left\{
      \begin{array}{lr}
        1 &\text{ if } P(k) \newline
        0 &\text{ otherwise }  \newline
      \end{array}
    \right.
$$

where $P(k)$ is the statement "$k$ is the smallest even number greater then $2$ that cannot be written as the sum of two primes".

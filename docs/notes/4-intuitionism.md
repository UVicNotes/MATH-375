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

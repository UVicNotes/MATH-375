# Set Theory

## Sets [<small>&icon-book;</small>](https://uvicnotes.github.io/MATH-122/notes/2-1-sets/)

* Sets can be defined by listing their elements, e.g., $S = \{0,1,2,3\}$ is a set.
* Set are completely defined by their elements, e.g., $\{0,1\} = \{1,0\}$.
* Sets can be defined by using criteria, e.g., $\{ x | x \in \mathbb N  \wedge x < 4\}$.
* We can state whether or not elements are in set, e.g., $2 \in S$ or $4 \not\in S$.
* We say $S \subseteq T$ if and only if every element of $S$ is also and element of $T$.

### Union and Intersection

Given two sets $A$ and $B$, we define the **union** as,

$$
    A \cup B = \{ x | x \in A \vee x \in B \}.
$$

Given two sets $A$ and $B$, we define the **intersection** as,

$$
    A \cup B = \{ x | x \in A \wedge x \in B \}.
$$

### Power Sets

Given a set $A$ , the **power set** of a set $A$ (denoted $\mathcal{P}(A)$) is the set whose elements are the subsets of $A$, i.e,

$$
    \mathcal P(A) = \{ x | x \subseteq A \}.
$$

**Example**

Let $A = \{ a, b, \}$. What is the power set of $A$?

Subsets of $A$ are:

* $\{ a \}$
* $\{ b \}$
* $\{ a, b \}$
* $\emptyset$

**_Solution_**

$$
    \mathcal{P}(A) = \{\{ a \}, \{ b \}, \{ a, b \}, \emptyset \}
$$


## Russell's Paradox [<small>&icon-wikipedia;</small>](https://en.wikipedia.org/wiki/Russell's_paradox)

Consider the set,

$$
    R = \{ x | x \not\in x \}
$$

is $R \in R$? We have two options

1. $R \in R$ then $R$ falls under $x \not\in x$, so $R \not\in R$.
2. $R \not\in R$ then $R$, since for $x = R$, $x \not\in x$, $R \in R$.

Therefore $R \in R$ if and only if $R \not\in R$.

## Zermelo–Fraenkel Set Theory [<small>&icon-wikipedia;</small>](https://en.wikipedia.org/wiki/Zermelo%E2%80%93Fraenkel_set_theory)

The **Zermelo–Fraenkel Choice (ZFC)** is an axiomatic approach for defining sets.

## Restricting Sets

We can restrict our definition of sets by not allowing **impredicative** ([&icon-wikipedia;](https://en.wikipedia.org/wiki/Impredicativity)) definitions, i.e., definitions that reference themselves. For example,

$$
    R = \{ x | x \not\in x \}
$$

is impredicative since it references $x$ to define $x$.

This restriction however can be too aggressive removing many otherwise viable sets.

### Comprehension

Let $\ell (x)$ be a formula with free variable $x$. So,

definitions that reference themselves. For example, given

$$
    \{ x | \ell(x) \}
$$

then $\ell(x)$ cannot be impredicative. Consider,

$$
    \forall y \exists z \forall x \big( x \in z \leftrightarrow \big( x \in y \wedge \ell(x) \big)  \big)
$$

the **comprehension** ([&icon-wikipedia;](https://en.wikipedia.org/wiki/Set-builder_notation)) restricts that $x$ must already be in an existing set, specifically $y$.

### Hierarchy of Sets [<small>&icon-wikipedia;</small>](https://en.wikipedia.org/wiki/Von_Neumann_universe)

We can define the hierarchy of sets as follows,

$$\begin{aligned}
    V_0 &= \varnothing \newline
    V_1 &= V_0 \cup \mathcal P(V_0) \newline
    V_2 &= V_1 \cup \mathcal P(V_1) \newline
    &~~\vdots \newline
    V_{n+1} &= V_n \cup \mathcal P(V_n) \newline
\end{aligned}$$

![hierarchy of sets](https://upload.wikimedia.org/wikipedia/commons/8/83/Von_Neumann_universe_4.png)






# Consistency

We define **syntax** or **semantics** as the notation used to communicate mathematical reasoning.

## Syntactic Completeness

$S$ is **syntactically complete** if, for every formula $A$, either $S \vdash A$ or $S \vdash \neg A$.

## Peano Arithmetic

Peano Arithmetic has **axioms**, which are facts that always hold true, and **rules**, which allow the inference of ideas.

We can define the natural numbers as

$$\begin{aligned}
    O &= 0 \newline
    S(O) = SO &= 1 \newline
    SSO = S^2O &= 2 \newline
    &~~\vdots \newline
\end{aligned}$$

Using Peano Arithmatic, $PA$,

$$\begin{aligned}
     PA &\vdash S^2 O + S^3 O = S^5 O \newline
     PA &\vdash \neg( S^2 O + S^3 O = S^6 O). \newline
\end{aligned}$$

### Representation and Decidability

A set $A \subseteq \mathbb N$ is **representable** when there is some formula $P(x)$ such that

$$\begin{aligned}
     \text{if } n \in A \text{, then } PA &\vdash P(n) \newline
     \text{if } n \not\in A \text{, then } PA &\vdash \neg P(n). \newline
\end{aligned}$$

A set $A$ is **decidable** I
f there is an algorithm for determining whether $n \in A$.

## Gödel Numbering

Given any number, there exists a unique prime factorization. Given a set of operators,

$$
    ~\underset { 0} {\vphantom{()} \wedge}
    ~\underset { 1} {\vphantom{()} \vee}
    ~\underset { 2} {\vphantom{()} \neg }
    ~\underset { 3} {\vphantom{()} \to}
    ~\underset { 4} {\vphantom{()} \iff}
    ~\underset { 5} {\vphantom{()} \forall}
    ~\underset { 6} {\vphantom{()} \exists}
    ~\underset { 7} {\vphantom{()} (}
    ~\underset { 8} {\vphantom{()} )}
    ~\underset { 9} {\vphantom{()} =}
    ~\underset {10} {\vphantom{()} 0}
    ~\underset {11} {\vphantom{()} S}
    ~\underset {12} {\vphantom{()} <}
    ~\underset {13} {\vphantom{()} +}
    ~\underset {14} {\vphantom{()} \cdot}
    ~\underset {15} {\vphantom{()} x_1}
    ~\ldots
    ~\underset {14 + n} {x_n}
$$

we can construct the Gödel number of any formula or equation by encoding the sequence $(x_1, x_2, \ldots, x_n)$ as

$$
    \text{enc}(x_1, x_2, \ldots, x_n) = 2^{x_1} \cdot 3^{x_2} \cdot 5^{x_3} \cdot \ldots \cdot p_n ^{x_n}
$$

where $p_i$ is the $i^\text{th}$ prime number. 

### Diagonalization

Let $\ulcorner \varphi \urcorner$ be the Gödel number of $\varphi$ and let,

$$
    \text{diag} \big(\ulcorner \varphi \urcorner \big) = \Big\ulcorner \exists x_1 \big( x_1 = \ulcorner \varphi \urcorner \wedge \varphi(x_1) \big) \Big\urcorner.
$$

For example,

$$
    \text{diag} \big(\ulcorner \text{wff} \urcorner \big) = \Big\ulcorner \exists x_1 \big( x_1 = \ulcorner \text{wff} \urcorner \wedge \text{wff}(x_1) \big) \Big\urcorner.
$$

### Omega-Consistency

A theory $T$ is $\omega$-consistent when, for some $\varphi$,

$$
    T \vdash \exists x \varphi (x)
$$

but, for every $n$,

$$
    T \vdash \neg \varphi (S^n O).
$$

For example, suppose $\mathbb N \cup \{ \text{puppy} \}$. Then $\exists x  ~ \text{Cute}(x)$ but $\neg ~ \text{Cute}(S^n O)$ for all $n \in \mathbb N$.

### Inconsistency

**Claim:** If $T$ is a decidable extension of $PA$, then:

1. If $T$ is consistent, then $T \not\vdash G$, and,
1. If $T$ is $\omega$-consistent, then $T \not\vdash \neg G$.

<!-- TODO
Suppose $PA$ is consistent. If $PA \vdash G$, then the proof has some number, say $m$. Then $PA \vdash \text{Proof} ( m, \ulcorner G \urcorner )$, so $PA \vdash \text{Proof} ( m, \text{diag}( \ulcorner U \urcorner ))$.
-->

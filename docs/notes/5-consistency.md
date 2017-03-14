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

### Gödel Numbering

Given any number, there exists a unique prime factorization. Given a set of operators,

$$
    ~\underset { 0} {\wedge}
    ~\underset { 1} {\vee}
    ~\underset { 2} {\neg }
    ~\underset { 3} {\to}
    ~\underset { 4} {\iff}
    ~\underset { 5} {\forall}
    ~\underset { 6} {\exists}
    ~\underset { 7} {(}
    ~\underset { 8} {)}
    ~\underset { 9} {=}
    ~\underset {10} {0}
    ~\underset {11} {S}
    ~\underset {12} {<}
    ~\underset {13} {+}
    ~\underset {14} {\cdot}
    ~\underset {15} {x_1}
    ~\ldots
    ~\underset {14 + n} {x_n}
$$

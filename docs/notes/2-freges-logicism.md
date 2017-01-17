# Frege's Logicism

## What is the number one?

Frege examines this question from a number of angles and uses it as an example extensively.

## Frege's Views

Frege disagreed with several prior philosophers of how Mathematics were defined

* [John Stuart Mill](https://en.wikipedia.org/wiki/John_Stuart_Mill), who wanted to base Mathematical knowledge on empirical knowledge.
* [Immanuel Kant](https://en.wikipedia.org/wiki/Immanuel_Kant), who suggested that there is some innate intuition in our minds that gives us definitions Mathematics.

Frege thought instead the theories of Mathematics should be based on **logic**. He developed a set of rules for this logic which he document in a book, [Begriffsschrift](https://en.wikipedia.org/wiki/Begriffsschrift).

Much of modern logic is based on Frege's work although [his notation](https://en.wikipedia.org/wiki/Begriffsschrift#Notation_and_the_system) has been mostly replaced by modern alternatives. Frege's system used some [second-order logic](/appx/logic#second-order-logic).

## Frege's Logic

If $\exists x_1 F(x)$ the $\neg \exists x_2 F(x)$, or "If there exists exactly one thing that is $F$ than there are not two thing that are $F$".

### Proving a Conditional

Suppose $\exists x_1 F(x)$, so $\exists x(F(x) \wedge \neg (F(y) \wedge x \neq y))$. Let $a$ be such that $F(a) \wedge \neq \exists y(F(y) \wedge a \neq y)$.

This implies $\neg \exists y (F(a) \wedge F(y) \wedge a \neq y)$. So $\neg \exists y(F(x) \wedge F(y) \wedge x \neq y)$.

## Equinerousity

The number of $F$'s is the same as the number of $G$'s.

$$
    \exists_5 x F(x) \wedge \exists_5 x G(x)
$$

"The number of $F$'s is 5 and the number of $G$'s is 5". We want to write an **equality** statement, "The number of $F$'s $=$ the number of $G$'s".

Frege defined a relationship, **equinerousity**. This relation is a bijection between the two quantities. For example the above statement would be equivalent to "$F$ is _equinumerous_ with G".

_definition_: $F$ is **equinumerous** with $G$ when

$$
    \exists R \left[
        \forall x \left( F(x) \to \exists_1 y \left( R \left( x,y \right) \right) \wedge G(y) \right)
    \wedge
        \forall x \left( G(x) \to \exists_1 y \left( R \left( y,x \right) \right) \wedge F(y) \right)
    \right]
$$

where $R$ is a [relation](/appx/logic#relations) from $F$ to $G$. Equinerousity is an [equivalence relation](https://uvicnotes.github.io/MATH-122/notes/2-4-equivalence-relations/) (reflexive, symmetric and transitive).

## The Julius Ceaser Problem

Is Julius Ceaser the number one?

## Defining Numbers

We can define numbers as follows,

$$
    \text{the number of $F$'s} = \text{the extension of the concept "equinumerous with $F$"}
$$

**Example**

Let $F$ be the things on the table. There are three things on the table so the number of $F$'s is $3$. There are many sets equinumerous with $F$, for example

* the set ${1,2,3}$
* the set of primary colors
* the set of wheels on the triangle

### Theorem

We can define the cardinal numbers as,

Given $n$, $n$ is a number if and only if there is some $F$ such that the number of $F$'s is $n$.

### Counting Sets

How do we know all the natural numbers exist?

\begin{aligned}
    &"x \neq x" ~\text{has number $0$} \\
    &"\text{is identical to $0$}" ~\text{has the number $1$} \\
    &"\text{is identical to $0$ or $1$}" ~\text{has the number $2$} \\
    &~~~~~~~~~~~~\vdots \\
\end{aligned}

## Succession

The number of $F$'s **succeeds** the number of $G$'s if and only if there is an object $x$ falling under $F$ and the number of $G$'s is the number of the concept "falling under $F$ but not identical to $x$".


---
title: Probability
type: concept
status: "canonical (draft; the finite core and where it stops)"
provenance: "murphy (the direction, AND is times and OR is plus, with factorial, permutation, combination and choose taught the usual way up until somewhere) + ai-synthesis (the conditions on the rules, the worked examples, the boundary, the flagged problems)"
sources: "[[Statistics]], [[Constructible Statistics]], [[Boolean Algebra]], [[Discrete Calculus]], [[Historical Order]], [[Creational Ultrafinitism]]"
updated: 2026-10-10
---

# Probability

Murphy's observation: *AND is times, OR is plus*, with factorial, permutation, combination and "choose", can be taught the usual way, up until somewhere. This page says what the usual way is, where it is exact, and where "somewhere" is.

## The core: probability is counting

On a finite set $\Omega$ of equally likely outcomes, $P(A)=|A|/|\Omega|$ (Laplace). Everything below is arithmetic on whole numbers and fractions.

## The dictionary, with its conditions [AI]

| Say | Do | Holds when |
|---|---|---|
| **AND** | multiply | the choices are *independent* (the rule of product); in general $P(A\wedge B)=P(A)\,P(B\mid A)$ |
| **OR** | add | the cases are *disjoint* (the rule of sum); in general $P(A\vee B)=P(A)+P(B)-P(A\wedge B)$ |
| **NOT** | subtract from $1$ | always: $P(\neg A)=1-P(A)$ |

The mnemonic is right, and the conditions are the lesson. **Heart or face card:** $\tfrac{13}{52}+\tfrac{12}{52}-\tfrac3{52}=\tfrac{22}{52}=\tfrac{11}{26}$, subtracting the 3 cards counted twice. For independent events with probabilities $a,b$: OR is $a+b-ab=1-(1-a)(1-b)$ (for $\tfrac13,\tfrac14$: $\tfrac12$ both ways, checked), the "not both fail" rule, which often is the easier way to compute it.

**Link to the Boolean algebra** ([[Boolean Algebra]]). There, OR is $+$ and AND is $\times$ on the two values with $1+1=1$. A probability is a *valuation* of that algebra by numbers: the idempotent $+$ becomes ordinary addition once the overlap is subtracted. Equivalently, on indicator values $x,y\in\{0,1\}$ AND is $xy$, NOT is $1-x$, OR is $x+y-xy$, and exclusive-or is $x+y$ **mod 2** ([[Modular Arithmetic]], the field $\mathrm{GF}(2)$).

## The counting toolkit

| Name | Symbol | Formula | Meaning |
|---|---|---|---|
| factorial | $n!$ | $n(n-1)\cdots1$ | arrangements of $n$ distinct things |
| permutation | $P(n,k)=n^{\underline k}$ | $n(n-1)\cdots(n-k+1)$ | ordered choices of $k$ from $n$; the **falling power** of [[Discrete Calculus]] |
| combination ("choose") | $\binom nk$ | $P(n,k)/k!$ | unordered choices |
| binomial theorem | | $(a+b)^n=\sum\binom nk a^kb^{n-k}$ | Pascal's triangle |

**A link to Discrete Calculus:** Pascal's rule $\binom{x+1}{k}-\binom xk=\binom x{k-1}$ says $\Delta\binom xk=\binom x{k-1}$ (checked for $x=9,k=4$: $84$ both ways). The binomial coefficients are the falling powers divided by $k!$, the basis in which Newton's forward-difference formula is written, so counting and the difference calculus are one subject.

## Worked examples (all computed in exact arithmetic)

- **Hands of cards.** There are $\binom{52}5=2{,}598{,}960$ five-card hands. A flush that is not a straight flush: $4\binom{13}5-40=5108$ hands, probability $\tfrac{1277}{649740}$.
- **The Chevalier de Méré** (as the history is usually told, to check). At least one six in four rolls of a die: $1-(\tfrac56)^4=\tfrac{671}{1296}\approx0.518$. At least one double six in twenty-four throws of two dice: $1-(\tfrac{35}{36})^{24}\approx0.491$. Using "NOT then subtract" is the whole method.
- **The birthday problem.** The chance that among $23$ people two share a birthday is $1-\dfrac{365^{\underline{23}}}{365^{23}}\approx0.5073$, and $23$ is the least group size for which it exceeds $\tfrac12$ (computed over all sizes up to 99).
- **Bayes' theorem.** A condition has prevalence $1\%$; a test has sensitivity $90\%$ and a false-positive rate of $9\%$. Given a positive test, the chance of the condition is $\dfrac{0.01\cdot0.9}{0.01\cdot0.9+0.99\cdot0.09}=\tfrac{10}{109}\approx9.2\%$: the counting version is "of 10,000 people, 90 true positives and 891 false ones".
- **Variance and the sampling distributions** of [[Constructible Statistics]] are the same counting on larger tables.

## Where the usual way holds, and where "somewhere" is

**Holds, exactly (finite sample spaces):** sample spaces as finite sets; the rules above; conditional probability and independence (a product condition); Bayes' theorem; expected value as a finite weighted sum; variance; the binomial and hypergeometric distributions; Chebyshev's inequality and its higher-moment ladder ([[Constructible Statistics]]); exact tests.

**Stops, at an infinity:**

| Usual topic | What it assumes | Replacement in the vault |
|---|---|---|
| Infinite sample spaces; countable additivity | a completed infinite totality | a finite space, or a stated *bound* on the number of trials |
| "First head at toss $n$" summing to $1$ | an infinite sum | the chance the first head is within $N$ tosses is exactly $1-2^{-N}$ ($\tfrac{1023}{1024}$ for $N=10$); "eventually" claims need an $N$ |
| Continuous random variables, densities, the integral | the continuum | a finite grid, with the density a named approximation with an error |
| Probability $0$ yet possible; "almost surely" | measure theory | not stated; the finite theory has no such events |
| The law of large numbers and CLT as limits | $n\to\infty$ | explicit finite bounds ([[Constructible Statistics]]) |
| "A random real number" | a completed ℝ | not available ([[Christians and the Reals]]) |
| Infinite expectations | a series without a bank | a finite stake (below) |

**The St. Petersburg paradox, finitely.** A coin is tossed until it first lands heads on toss $k$, and the player is paid $2^k$ (probability $2^{-k}$, so each term of the expectation is $1$ and the series diverges). With a *finite bank* that pays at most $2^m$, the expectation is exactly $m+1$ (computed for $m=1,\dots,20$): about $21$ for a bank near $10^6$, and about $665$ for a bank of $10^{200}$ (using $\log_2 10^{200}\approx664.4$). So the "infinite value" of the game is the growth of a logarithm in the size of the bank, and the paradox disappears once the stake is a number one can hold.

## What probability means (interpretation) [AI]

Classical (counting equally likely cases), frequentist, Bayesian and propensity readings differ about what a probability *is*. The finite core works under all of them. Two points for the vault:

- **"Equally likely" must come from somewhere.** The design-based approach gets it from a *randomizing act* (a shuffle, lots, dice), whose fairness is a physical fact with a certificate of its own ([[Constructible Statistics]], result 7).
- **Providence.** Chance is not an independent power. Proverbs 16:33 (the lot is cast, its every decision is from the LORD; to check) is the pastoral reading; it is a link, and not a premise of the mathematics.

## Teaching placement [AI]

Counting (arrangements, choose, Pascal's triangle) can sit with the number-theory stretch, since it is exact and symbol-light; probability proper follows the first symbols, near analytic geometry ([[Historical Order]]); statistics, for the majority, follows ([[Statistics]]).

## Hard problems

1. **How much of conditional probability and independence survives without infinite spaces** when the space is huge: a product over $n$ independent trials is still a finite count, but the space has $2^n$ outcomes and passes the threshold quickly ([[Creational Ultrafinitism]]).
2. **Continuous models.** The exact statement of a density as an approximation to a finite table, with an error, is not written.
3. **Randomness.** What makes a procedure a fair random act; deferred.
4. **History.** The attributions (Pascal and Fermat on the problem of points, the de Méré story) are recollections.

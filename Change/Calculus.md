---
title: Calculus
type: theory
status: canonical (first-order calculus; functions beyond the algebraic ones are open)
provenance: murphy (the definition $f(x+\varepsilon)=f(x)+f'(x)\varepsilon$ and the direction) + ai-synthesis (rules, examples, flagged problems)
sources: "[[Infinitesimals]], [[Discrete Calculus]]"
updated: 2026-10-09
---

# Calculus

"Regular" calculus, done with infinitesimals: the intuition of non-standard analysis (Newton, Leibniz, Robinson, Keisler: [[Infinitesimals#Robinson]]) with the arithmetic of smooth infinitesimal analysis (Bell: [[Infinitesimals#Smooth infinitesimal analysis]]). It is rung 2 of the Change ladder ([[Structure Hierarchies]]), and the same calculus as [[Discrete Calculus]] with the step below the resolution of the certificate.

## The definition

An **infinitesimal** here is a number $\varepsilon$ with $\varepsilon^2=0$. Under a microscope a curve is a straight line, and this is that statement. For a function $f$, its **derivative** $f'(x)$ is the number such that, for every such $\varepsilon$,

$$\boxed{\,f(x+\varepsilon)=f(x)+f'(x)\,\varepsilon\,}$$

It is the first-order truncation: no limit, no $\varepsilon$–$\delta$, no standard part. The value of $f$ one infinitesimal step away is the value here plus the slope times the step, exactly.

**Cancelling $\varepsilon$.** The derivative is *unique*: if $a\varepsilon=b\varepsilon$ for **every** $\varepsilon$ with $\varepsilon^2=0$, then $a=b$. (The dual numbers $a+b\varepsilon$ with $\varepsilon^2=0$ make this the statement that the coefficients are unique: [[Infinitesimals#The dual numbers: the exhibitable form]].) Two cautions, both from the logic of [[Infinitesimals]]:

- One may cancel $\varepsilon$ only when the equation holds for all nilsquare $\varepsilon$. A single $\varepsilon$ cannot be cancelled, and $\varepsilon$ has no reciprocal.
- One may not argue "either $\varepsilon=0$ or $\varepsilon\ne0$". Neither can be asserted, and neither $\varepsilon<\delta$ nor $\delta<\varepsilon$ can be decided.

## The rules: the rectangle, with the corner gone

Everything in [[Discrete Calculus]] holds here with the corner $\Delta f\,\Delta g$ replaced by $f'g'\varepsilon^2=0$.

**Product rule.** Grow the $f$ by $g$ rectangle by an infinitesimal step:
$$(f+f'\varepsilon)(g+g'\varepsilon)=fg+(fg'+gf')\varepsilon+f'g'\varepsilon^2=fg+(fg'+gf')\varepsilon.$$
So $(fg)'=fg'+gf'$. The side strip is $g\,f'\varepsilon$, the top strip is $f\,g'\varepsilon$, and the corner is $f'g'\varepsilon^2=0$. The figure of the discrete page, with $\Delta f=f'\varepsilon$ and $\Delta g=g'\varepsilon$.

**Power rule.** By the binomial theorem, $(x+\varepsilon)^n=x^n+nx^{n-1}\varepsilon+\binom n2x^{n-2}\varepsilon^2+\cdots=x^n+nx^{n-1}\varepsilon$. So $(x^n)'=nx^{n-1}$. Worked example, at $x=5$:
$$(5+\varepsilon)^3=125+75\varepsilon,$$
slope $75$. The discrete difference quotients at $x=5$ were $91,\ 76.51,\ 75.1501$ for steps $1,\ \tfrac1{10},\ \tfrac1{100}$ with exact error $3xh+h^2$. Here $h$ is infinitesimal, the error terms carry $\varepsilon^2=0$ or sit below the resolution, and what is left is $75$.

**Reciprocal.** $(f+f'\varepsilon)\Bigl(\dfrac1f-\dfrac{f'}{f^2}\varepsilon\Bigr)=1-\dfrac{f'^2}{f^2}\varepsilon^2=1$, so $\Bigl(\dfrac1f\Bigr)'=-\dfrac{f'}{f^2}$. At $x=2$: $\dfrac1{2+\varepsilon}=\dfrac12-\dfrac14\varepsilon$.

**Quotient.** $\Bigl(\dfrac fg\Bigr)'=\dfrac{gf'-fg'}{g^2}$ (the denominator is $g^2$ because $g(g+g'\varepsilon)=g^2$ to first order). It requires $g(x)$ to be invertible. Example: $f=3+\varepsilon$, $g=2+\varepsilon$: $\dfrac fg=\dfrac32-\dfrac14\varepsilon$.

**Chain rule: it holds.** Unlike discrete calculus, where $\Delta(f\circ g)$ does not factor, here $g'\varepsilon$ is again an infinitesimal, since $(g'\varepsilon)^2=g'^2\varepsilon^2=0$. So
$$f\bigl(g(x+\varepsilon)\bigr)=f\bigl(g(x)+g'(x)\varepsilon\bigr)=f(g(x))+f'(g(x))\,g'(x)\,\varepsilon,$$
and $(f\circ g)'=(f'\circ g)\,g'$. Example, $(x^2+1)^3$ at $x=2$: $g=x^2+1=5+4\varepsilon$, so $(5+4\varepsilon)^3=125+300\varepsilon$, matching $6x(x^2+1)^2=12\cdot25=300$. *The corner is what breaks the chain rule in the discrete case, and nilsquare steps are what rescue it.*

**Tangent line.** The equation $y=f(a)+f'(a)(x-a)$ is the definition read for a finite step; for an infinitesimal step it is exact.

## The integral

An **area function** $A(x)$ is the area under $y=f$ up to $x$. Adding a strip of width $\varepsilon$ adds a rectangle of height $f(x)$, with no triangle of corner left over:

$$A(x+\varepsilon)=A(x)+f(x)\,\varepsilon,$$

which says $A'=f$ (the integral is not secondary: it can be taken as primitive, and the derivative derived: see [[Fundamental Theorem of Calculus]]): the local half of the fundamental theorem, and just the definition applied to the area. The global half (if $F'=f$ then $\int_a^bf=F(b)-F(a)$), what it needs beyond the definition, and why no transcendental function is required, are on [[Fundamental Theorem of Calculus]].

Worked example: $F=\tfrac13x^3$ has $F'=x^2$, so $\int_0^1x^2\,dx=\tfrac13$. In [[Discrete Calculus]] the left sum with $n$ steps is exactly $\tfrac13-\tfrac1{2n}+\tfrac1{6n^2}$: the integral is the part free of $n$, and the infinitesimal calculus drops the rest.

## Higher order

$\varepsilon^2=0$ is first-order. For second derivatives and Taylor remainders one uses $\varepsilon^{n+1}=0$:
$$f(x+\varepsilon)=f(x)+f'(x)\varepsilon+\tfrac{f''(x)}2\varepsilon^2+\cdots+\tfrac{f^{(n)}(x)}{n!}\varepsilon^n.$$
Example with $\varepsilon^3=0$: $(x+\varepsilon)^3=x^3+3x^2\varepsilon+3x\varepsilon^2$, so $f''/2=3x$. Note that the sum of two nilsquares need not be nilsquare: $(\varepsilon_1+\varepsilon_2)^2=2\varepsilon_1\varepsilon_2$. How many orders the threshold allows is an open problem ([[Infinitesimals]], hard problem 4).

## What is taken from non-standard analysis, and what is not

- **Taken:** the intuition. The derivative is the slope between a point and one infinitesimally near it, and an integral is a sum of infinitely thin strips (Keisler's *Elementary Calculus*).
- **Not taken:** the hyperreal field. Robinson's ${}^*\mathbb R$ is an ordered field in classical logic where $0<\varepsilon<1/n$ for every $n$, and from it the derivative is recovered by the **standard part**, $f'(x)=\operatorname{st}\bigl((f(x+h)-f(x))/h\bigr)$ for an invertible infinitesimal $h$. Here there is no standard part and no order on infinitesimals: $f'(x)$ is a coefficient. See [[Infinitesimals#Robinson]].

## Exact versus honest [AI]

Every statement above is checkable by algebra on the dual numbers $a+b\varepsilon$, so for polynomials, and by the same cancellation for rational functions, the definition *is* a certificate. For other functions (the exponential, the logarithm, sine and cosine) the definition cannot be checked on the dual numbers alone: it needs the function itself. The honest route is the one of [[Discrete Calculus]]: the exponential is $E_h$ with $D_hE_h=E_h$ and its error bound, the logarithm is $H_n$ with $\gamma$, sine and cosine are the circle of $\oplus$. Calculus then says: *take the function as defined by its discrete ancestor and apply the definition above.* Written for the vault, that is the shape of *Infinity and Uncertainty*.

## Hard problems

1. **Existence.** For a given $f$, what warrants that the number $f'(x)$ exists? For polynomials and rational functions the derivative is a computed coefficient. For the others it is an axiom in SIA (Kock–Lawvere), which asserts "every function is microaffine". In the vault's terms: a certificate for $f'$ is needed, and its form for $\exp$, $\ln$ and the circle functions is the open item above.
2. **No excluded middle** (see [[Intermediate Value Theorem]] for the first case worked). Theorems that rest on case analysis (a function defined by cases, $|x|$, a step function, the extreme value theorem) are not available without it. SIA proves that every function is smooth, so there are no jumps and no corners: the Dirac "function" and the absolute value are not functions ([[Structure Hierarchies]], Change rung 7). Which of these a student of this calculus should lose, and which should be restored on bounded (decidable) domains ([[Future Directions]] item 7), is not settled.
3. **The two infinitesimals.** In [[Discrete Calculus]] a step $h$ has $h^2\ne0$ and the corner is kept; here $\varepsilon^2=0$. The bridge is a certificate that the discarded terms are below the resolution. For a polynomial it is exact; in general it is an error bound that has not been stated.
4. **Higher order** (above): how many orders.
5. **Calculus on $\mathbb K$.** [[Constructible Numbers]] are a field, and the dual numbers can be built over it, so the calculus of this page can be done with the vault's own numbers. Which functions, beyond the algebraic ones, are defined on them is the question of item 1.

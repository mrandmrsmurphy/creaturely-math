---
title: Fundamental Theorem of Calculus
type: theorem
status: canonical (finite form proved; infinitesimal form's global half flagged)
provenance: murphy (direction; definition of the derivative) + ai-synthesis (statements, examples, analysis of what each form needs)
sources: "[[Discrete Calculus]], [[Calculus]]"
updated: 2026-10-09
---

# Fundamental Theorem of Calculus

**The total change is the sum of the changes.** If you know how fast something is changing at every step, adding up the changes gives the net change; and if you add up a rate as you go, the running total changes at that rate. Differences and sums undo each other.

It has a **finite form** (exact, proved by cancellation) and an **infinitesimal form** (the first-order idealization of it). Both are kept in this vault, and neither needs a transcendental function.

## Finite form

For any $f$ on a lattice of steps, with the steps indexed $x=m,\dots,n-1$:

$$\sum_{x=m}^{n-1}\Delta f(x)=f(n)-f(m).$$

*Proof.* A running total starts at $f(m)$, and each step adds its $\Delta f$. Written out, $\bigl(f(m+1)-f(m)\bigr)+\bigl(f(m+2)-f(m+1)\bigr)+\cdots+\bigl(f(n)-f(n-1)\bigr)$: every interior value is added once and taken away once, leaving the last value minus the first. (Telescoping.)

**Two halves.**

- *Sum of differences:* the display above.
- *Difference of a sum:* if $S(n)=\sum_{x=m}^{n-1}f(x)$, then $\Delta S(n)=f(n)$. (The sum of one more term is the old sum plus that term.)

**Using it.** If $\Delta F=f$ ($F$ is an **antidifference** of $f$), then $\sum_{x=m}^{n-1}f(x)=F(n)-F(m)$. All examples are exact:

| $f$ | antidifference $F$ | sum | check |
|---|---|---|---|
| $x^2=x^{\underline2}+x^{\underline1}$ | $\tfrac13x^{\underline3}+\tfrac12x^{\underline2}$ | $\sum_{x=0}^{4}x^2=\tfrac{60}3+\tfrac{20}2=30$ | $0+1+4+9+16$ |
| $2^x$ | $2^x$ | $\sum_{x=0}^{4}2^x=2^5-2^0=31$ | $1+2+4+8+16$ |
| $\dfrac1{x(x+1)}$ | $-\dfrac1x$ | $\sum_{x=1}^{3}\dfrac1{x(x+1)}=1-\dfrac14=\dfrac34$ | $\tfrac12+\tfrac16+\tfrac1{12}$ |
| $\dfrac1{x+1}$ | $H_x$ | $\sum_{x=1}^{3}\dfrac1{x+1}=H_4-H_1=\dfrac{13}{12}$ | $\tfrac12+\tfrac13+\tfrac14$ |

(Antidifferences: [[Discrete Calculus]].) The last row is the logarithm's place: the harmonic number $H_x$ is a rational number for every $x$.

**Summation by parts** is the product rule summed. Grow an $f$ by $g$ rectangle from its first to its last size; the total growth $[fg]_m^n$ is the sum of the side strips, top strips and corners ([[Discrete Calculus]]), which gives $\sum f\,\Delta g=[fg]_m^n-\sum g\,\Delta f-\sum\Delta f\,\Delta g$.

## Infinitesimal form

With the definition $f(x+\varepsilon)=f(x)+f'(x)\varepsilon$, $\varepsilon^2=0$ ([[Calculus]]), it has a local half and a global half.

**Local.** Let $A(x)$ be the area under $y=f$ up to $x$. Moving $x$ by $\varepsilon$ adds a strip of width $\varepsilon$ and height $f(x)$, with no triangle left over (the corner is $\varepsilon\cdot f'\varepsilon=0$):

$$A(x+\varepsilon)=A(x)+f(x)\,\varepsilon,\qquad\text{so}\qquad A'=f.$$

This is the definition applied to the area (derivative-first); nothing is assumed beyond it. Taking the integral as primitive instead proves it: see below. It is the difference-of-a-sum half of the finite theorem with the step infinitesimal.

**Global.** If $F'=f$ then
$$\int_a^bf=F(b)-F(a).$$
This is the sum-of-differences half, and it needs two further things:

1. **Uniqueness.** Two antiderivatives differ by a constant: $G'=0$ implies $G$ is constant. One cannot get this by cancelling a single $\varepsilon$; it has to pass from steps of size $\varepsilon$ to a finite interval. SIA takes it as an axiom (the integration axiom, or constancy principle). The finite form proves the analogue: $\Delta G=0$ at every step of a lattice makes $G$ constant by walking along it, a bounded count. With a modulus of differentiability the infinitesimal form's uniqueness is proved the same way, by the mean value inequality ([[Mean Value Theorem]]).
2. **Existence.** That a given $f$ *has* an antiderivative. For polynomials it is explicit: $F=\tfrac1{n+1}x^{n+1}$ for $x^n$. For $1/x$ and $1/(1+x^2)$ no algebraic $F$ exists, and this is where $\ln$ and $\arctan$ enter as *new* functions.

**Worked example.** $F=\tfrac13x^3$, $F'=x^2$, so $\int_0^1x^2=F(1)-F(0)=\tfrac13$. The finite form at step $\tfrac1n$ gives $\tfrac13-\tfrac1{2n}+\tfrac1{6n^2}$ ($\tfrac18,\ \tfrac7{32},\ \tfrac{57}{200}$ for $n=2,4,10$). The integral is the part free of $n$, and the finite form carries its own error.

## Neither is prior: the integral first

The derivative looks primary on this page only because [[Calculus]] begins from the definition $f(x+\varepsilon)=f(x)+f'(x)\varepsilon$. The integral can be taken as the primitive instead, and the same theorem results. Historically it came first (Archimedes, Cavalieri, before Fermat and Newton); Wildberger's *Algebraic Calculus* is said to teach integration before differentiation and to avoid limits ([course page](https://njwildberger.com/2021/07/01/welcome-to-algebraic-calculus-one-2021/); his exact construction is not confirmed here, and the derivation below is mine, not his).

**Axioms for the integral of polynomials** (areas, not antiderivatives):

1. *Additive* over adjacent intervals, and *linear*: $\int(af+bg)=a\int f+b\int g$.
2. *Normalized:* $\int_0^11=1$ (the unit square has area 1).
3. *Scaling:* stretching the $x$-axis by $b$ multiplies area by $b$, so $\int_0^bf(x)\,dx=b\int_0^1f(bu)\,du$.
4. *Translation:* $\int_c^{c+b}f(x)\,dx=\int_0^bf(x+c)\,dx$.

**Derivation of $\int_0^bx^n\,dx=\dfrac{b^{n+1}}{n+1}$.** Let $a_k=\int_0^1x^k\,dx$, so $a_0=1$. Scaling gives $\int_0^bx^k\,dx=a_kb^{k+1}$. Now compute $\int_c^{c+b}x^n\,dx$ two ways, as $\int_0^{c+b}-\int_0^c$ (additivity) and by translation:
$$a_n\bigl((c+b)^{n+1}-c^{n+1}\bigr)=\sum_{k=0}^n\binom nk c^{n-k}\,a_k\,b^{k+1}.$$
Compare coefficients of $c^{n-k}b^{k+1}$: $a_n\binom{n+1}{k+1}=\binom nk a_k$. For $k=0$ this is $(n+1)a_n=a_0=1$, so $a_n=\frac1{n+1}$ (and every other $k$ agrees; checked for $n\le8$). No derivative and no limit was used, only algebra on the axioms.

**The derivative falls out.** For $A(x)=\int_0^xf$ with $f=x^n$:
$$A(x+h)-A(x)=\int_0^h(x+t)^n\,dt=\sum_k\binom nk x^{n-k}a_kh^{k+1}=x^n\,h+h^2(\cdots),$$
so $A(x+h)=A(x)+f(x)h+h^2(\cdots)$: the derivative of the area function is $f$, with its exact error. That is the local half, *proved* from the integral axioms instead of assumed.

**So the two are symmetric:**

| | Primitive | Derived |
|---|---|---|
| Derivative first | $f(x+\varepsilon)=f+f'\varepsilon$ | local half is the definition; the global half needs uniqueness of antiderivatives (an axiom) |
| Integral first | the axioms above | global half is free ($\int_a^bx^n=\frac{b^{n+1}-a^{n+1}}{n+1}$); the local half is the computation just shown |
| Finite | $\Delta$ (subtraction) and $\Sigma$ (counting) | $\Delta\Sigma=\mathrm{id}$ and $\Sigma\Delta=$ end minus start, both proved |
| SIA | Kock–Lawvere (derivative) *and* the integration axiom | two separate axioms (Bell states them separately) |

In the finite case $\Sigma$ is as basic as $\Delta$: a sum is counting. The vault may choose either order for teaching, and the finite form holds under both.

## Transcendental functions

The theorem does **not** need them. It says "*if* $F'=f$ then…", so any $F$ you can exhibit will do. Transcendentals enter only when one demands that **every** $f$ have an antiderivative and names the result:

- $\int dx/x$ is $\ln$; $\int dx/(1+x^2)$ is $\arctan$.
- In the vault the demand is the Level-9 definition: $e$ is the $x$ with unit area under $y=1/x$ from $1$ ([[Number Hierarchy]]), geometric first, computed second.
- The finite form never makes the demand. $H_n$ is the antidifference of $1/(n+1)$, a rational number, and $\gamma=\lim(H_n-\ln n)$ is the price of identifying it with the continuous logarithm ([[Discrete Calculus]]). On the circle the same pattern holds: the discrete "arctan" is the step count, a natural number.

## Which form is the theorem

The finite form is the theorem: proved exactly, for every step size, in a bounded count of steps. The infinitesimal form is its first-order idealization. Its local half costs nothing. Its global half is the finite theorem for a step below the resolution of the certificate: it sums a number of strips past the threshold (the unmanageable $N$ of [[Infinitesimals]]), with the error certificate of [[Discrete Calculus]] standing in for the limit. Everything the classical theorem is used for in this vault (areas, accumulation, $\int_1^e dx/x=1$) can be stated in the finite form with an explicit error.

## Hard problems

1. **The global step.** What is the precise certificate that lets "$\sum$ of strips of width $h$" be replaced by "$\int$" when $h$ is below the resolution? For polynomials it is exact (the $n$-free part). In general it is an error bound that has not been stated.
2. **Constancy.** The infinitesimal form's uniqueness is an axiom of SIA, not derived from $\varepsilon^2=0$. It is *proved*, for functions with a differentiability modulus, by the mean value inequality ([[Mean Value Theorem]]). Whether the vault adopts the axiom, or requires the modulus, or states it only for bounded intervals, is open ([[Future Directions]] item 7).
3. **Infinite intervals and series.** $\int_0^\infty$ and infinite sums assume a completed infinity. Under [[Creational Ultrafinitism]] they are bounded sums with a stated tail bound, or levels 13–14 of [[Number Hierarchy]] with a named method. Not written.
4. **Existence of antiderivatives** for the functions beyond the algebraic ones: the same open item as in [[Calculus]], hard problem 1.

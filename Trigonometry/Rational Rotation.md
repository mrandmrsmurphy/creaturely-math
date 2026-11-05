---
title: Rational Rotation
type: method
status: canonical
provenance: "murphy (the demand: sine and cosine are transcendental, levels 10–11 of [[Function Hierarchy]], so the vault needs a discrete, rational, angle-free alternative; the names dsin_N and dcos_N confirmed 2026-11-04; the slope-language reading, the identities, the cost count, the no-period and no-zero results, the Padé and trapezoid remarks and the generalisation, adopted 2026-11-04) + murphy+ai (the circle sequence and its stepping table in [[Discrete Calculus]], Part II, which this page extends) + ai-synthesis (the family indexed by $N$ as it came out of an LLM conversation Murphy pasted, restated in slope language; every check) + third-party (Chebyshev polynomials; Wildberger's spread polynomials; Niven on rational points of finite order; Padé approximants; each restated, not claimed)"
sources: "[[Sum of Slopes]], [[Slope]], [[Function Hierarchy]], [[Fourier Analysis]], [[Discrete Calculus]]"
updated: 2026-11-04
---

# Rational Rotation

A discrete, exact, rational replacement for the sine and cosine as *sequences*. No angle is named, no transcendental number appears, and every value is a fraction.

**The idea.** Fix a rational step. Turn the point $(1,0)$ by that step again and again. The two coordinates of the $k$-th point are the **tick cosine** $\operatorname{dcos}_N(k)$ and **tick sine** $\operatorname{dsin}_N(k)$. The graph is a set of isolated points; nothing joins them.

**Where it already lives.** This is the circle sequence of [[Discrete Calculus#Part II: the circle]], stepped by the half-wedge slope $u=\tfrac1N$: $N=2$ is that page's table $(\tfrac35,\tfrac45),(-\tfrac7{25},\tfrac{24}{25}),(-\tfrac{117}{125},\tfrac{44}{125}),\dots$ and $N=1$ is its $\cos_4,\sin_4$. This page adds the family over all $N$, the cost, the absence of a period and of a zero, the half-step, and the Padé and Euler comparisons.

## The step

For a whole number $N\ge1$ let

$$a=\frac{N^2-1}{N^2+1},\qquad b=\frac{2N}{N^2+1},\qquad a^2+b^2=1.$$

These are the legs over the hypotenuse of the right triangle with sides $N^2-1,\ 2N,\ N^2+1$ (a Pythagorean triple: $N=2$ gives $3,4,5$; $N=10$ gives $99,20,101$). The step is the turn that sends $(1,0)$ to $(a,b)$:

$$x_{k+1}=a\,x_k-b\,y_k,\qquad y_{k+1}=b\,x_k+a\,y_k,\qquad (x_0,y_0)=(1,0).$$

Matrix form $R_N=\begin{pmatrix}a&-b\\b&a\end{pmatrix}$; columns orthonormal, determinant $1$. Define $\operatorname{dcos}_N(k)=x_k$ and $\operatorname{dsin}_N(k)=y_k$.

**In slope language** ([[Sum of Slopes]]). The step is **twice the wedge of slope $1/N$**: the doubling law gives the slope of the step as
$$M=\frac{2\cdot\frac1N}{1-\frac1{N^2}}=\frac{2N}{N^2-1}=\frac ba\cdot\ \text{(rise over run of the triple)}.$$
The $k$-th point lies on the ray of slope $M\oplus M\oplus\cdots\oplus M$ ($k$ times, by the addition law). Checked for $N=2,3,5,10,12$, $k\le19$: $y_k/x_k$ equals the iterated sum of slopes, with no rounding.

| $k$ | $x_k$ | $y_k$ ($N=10$) |
|---|---|---|
| 0 | $1$ | $0$ |
| 1 | $\tfrac{99}{101}$ | $\tfrac{20}{101}$ |
| 2 | $\tfrac{9401}{10201}$ | $\tfrac{3960}{10201}$ |
| 3 | $\tfrac{851499}{1030301}$ | $\tfrac{580060}{1030301}$ |

## What is exact

All of these are rational identities, checked in exact fractions (not decimals).

1. **The circle, at every tick:** $x_k^2+y_k^2=1$. Checked for $N=10$, $k\le100$.
2. **Addition of ticks:** $x_{j+k}=x_jx_k-y_jy_k,\quad y_{j+k}=y_jx_k+x_jy_k$. So the doubling $x_{2k}=x_k^2-y_k^2,\ y_{2k}=2x_ky_k$. Checked for $N\in\{2,3,5,10,12\}$.
3. **A three-term recurrence:** $y_{k+1}+y_{k-1}=2a\,y_k$ (the same for $x$), with $y_0=0,\ y_1=b$. Checked for $N=10$, $k\le100$. Hence $x_k$ is a polynomial in $a$ and $y_k=b\times$ a polynomial in $a$: the Chebyshev polynomials of the first and second kind (third-party), which is why this is a **discrete harmonic oscillator** with no sine in sight.
4. **Spread polynomials** (third-party, [[Fourier Analysis#Spread polynomials (third-party: Wildberger)]]): $y_k^2=S_k(b^2)$, with $S_{n+1}=2(1-2s)S_n-S_{n-1}+2s$. Hand-check at $k=2$, $N=10$: $4\cdot\tfrac{400}{10201}\cdot\tfrac{9801}{10201}=\tfrac{15681600}{104060401}=\left(\tfrac{3960}{10201}\right)^2$. Machine-checked $k\le59$ for $N\in\{2,3,5,10,12\}$.
5. **Negative ticks are free:** $x_{-k}=x_k$, $y_{-k}=-y_k$ (the inverse of a rotation is its transpose).
6. **Closed form**, writing the pair as one Gaussian integer: $x_k+i\,y_k=\dfrac{(N+i)^{2k}}{(N^2+1)^k}$. The step is $\tfrac{N+i}{N-i}$, and $\tfrac{N+i}{N-i}=\tfrac{(N+i)^2}{N^2+1}=a+ib$. The $i$ is a bookkeeping device for the pair; the arithmetic is the arithmetic of the matrix.

## Level and cost

**Level** ([[Function Hierarchy]]). As a function of the tick count $k$, $\operatorname{dsin}_N$ and $\operatorname{dcos}_N$ are combinations of $+,-,\times,\div$ on rationals: **levels 1–4, exact, $\mathbb Z\to\mathbb Q$**, against level 10–11 for the transcendental sine at a rational input. What is given up is the continuous domain: there is no value "between" two ticks, and the half-step is not rational (below).

**Cost** (axis 2).
- *The size of the fractions.* For even $N$ the pair $(x_k,y_k)$ has common denominator exactly $(N^2+1)^k$ in lowest terms; for odd $N$ a factor $2$ cancels at each step and the denominator is $\bigl(\tfrac{N^2+1}2\bigr)^k$. Reason: $N+i$ and $N-i$ share no factor (apart from $1+i$, only when $N$ is odd), and $(N+i)^{2k}$ contains only the first. Digits therefore grow **linearly** in $k$, about $k\log_{10}(N^2+1)$ — compare the **doubling** of digits at each step of iterating $x^2+1$ ([[Function Hierarchy#Axis 2: the cost to a pixel range]]). Computed: $N=10$, $k=100$, $y_{100}$ has a 201-digit numerator and denominator $101^{100}$ exactly. Denominators for $N=2,3,5,10,12$ at $k\le4$ are $5^k,5^k,13^k,101^k,145^k$ as predicted.
- *The count of steps.* Doublings give $y_k$ in about $\log_2k$ multiplications, but the numbers are then as large as the answer, so the digits, not the steps, dominate.

## The wave, and what it lacks

**A period.** None, except at $N=1$ (the right-angle step: $(1,0),(0,1),(-1,0),(0,-1),(1,0),\dots$, period $4$). Reason: a rational rotation of finite order has order $1,2$ or $4$ only (third-party: Niven). Orders $3$ and $6$ — the equilateral and hexagon wedges — need $b=\tfrac{\sqrt3}2$, a Length of level 5 ([[Exact Slopes]]), not a rational. So for $N\ge2$ the orbit never closes: it is infinite, its points are all distinct, and **the wave is only nearly periodic**.

**A zero.** $y_k\ne0$ for every $k\ge1$, $N\ge2$ (a zero would force $x_k=\pm1$, a finite-order point). Yet the wave changes sign: for $N=10$, $y_{15}>0>y_{16}$ and $y_{47}>0>y_{48}$ (computed), so the sign changes lie *between* ticks. A "zero" is a sign change of consecutive points, a pixel-style claim certified by the two exact neighbours. Likewise the maximum: $y_k=1$ is never attained.

**A half-step.** The half of the step wedge has slope $1/N$ and cosine $N/\sqrt{N^2+1}$, a Length (level 5), never rational since $N^2<N^2+1<(N+1)^2$. So the point set cannot be refined *within* $\mathbb Q$ by halving; to refine, change the step (a new $N$, or the generalisation below), which starts a new point set. $R_{2N}$ is only about half of $R_N$.

**Scale.** For fixed $k$, $y_k\to0$ as $N$ grows, since $b\approx2/N$. To compare steps over a comparable span, the index must grow with $N$. A horizontal stretch of the display, $P_{N,c}=\{(ck,\operatorname{dsin}_N(k))\}$, is an operation on the finished point set and does not touch the recurrence.

**The shape that emerges.** For $N=10$ the sine-like sequence turns over every $32$ ticks or so (computed: the downward sign changes sit between ticks $15,16$ and $47,48$).

## Against Taylor and Padé

The pasted conversation compared the rotation with Taylor and Padé approximations. Three points.

1. **A Taylor or Padé approximation needs an angle to approximate at.** It approximates a given function of a given input, and here there is no such input. So they are approximations of a different object (the transcendental sine); the rotation is not an approximation of anything.
2. **The step *is* a Padé approximant.** $\tfrac{1+z/2}{1-z/2}$ is the $[1/1]$ Padé approximant of the exponential, and at $z=\tfrac{2i}N$ it equals $\tfrac{N+i}{N-i}=a+ib$ (checked). Every *diagonal* Padé approximant of the exponential has numerator and denominator that are conjugates on the imaginary axis, so it has modulus exactly $1$ there (third-party, standard; the $[1/1]$ case verified here). So the pasted claim that Padé "does not automatically preserve" the circle holds for off-diagonal approximants, not for the diagonal ones; and the diagonal $[m/m]$ steps are themselves rational points on the circle, i.e. rational rotations with a different step.
3. **Truncated Taylor (explicit Euler), the cautionary case.** The step $1+ih$ has squared radius $1+h^2$. For $h=\tfrac1{10}$, after $100$ steps the squared radius is $(1.01)^{100}=2.7048138\ldots$ (computed): the point has left the circle. The rational rotation is the **trapezoid rule** for the motion $x'=-y,\ y'=x$, which keeps the invariant $x^2+y^2$ *exactly*, where Euler keeps it only to $O(h)$ ([[Function Hierarchy#Differential equations]]). The certificate here is an identity, not an error theorem.

## Generalisation

The step need not be $\tfrac{N^2-1}{N^2+1}$. Any rational slope $m=p/q$ gives the step $a=\tfrac{q^2-p^2}{q^2+p^2},\ b=\tfrac{2pq}{q^2+p^2}$, and every rational point of the circle arises this way. The pasted family is $p=1$. A finer family (a given wedge approximated by a step of small $p,q$) is the problem of [[Slope Approximations]]: pick the rational slope nearest to the wedge wanted, double it, and the tick set follows.

## Other frameworks

For readers coming from the angle: the step is the turn through $2\arctan\tfrac1N$ (about $\tfrac2N$ of a radian for large $N$), the ticks are $\sin(k\varphi),\cos(k\varphi)$ with $\varphi=2\arctan\tfrac1N$, and a full turn takes about $\pi N$ ticks ($\approx31.4$ for $N=10$, against the observed spacing of about $32$). The vault does not use this definition; it is stated so the two can be compared.

## Hard problems

1. **A cost theorem for the wave.** The size of the fractions is argued above; no bound is proved for the cost of reaching a *target* wedge or a target $\varepsilon$ of closeness to a given point. ([[Function Hierarchy]] hard problem 1.)
2. **Almost-periods.** How close can $(x_k,y_k)$ come to $(1,0)$ for $k$ up to a stated bound? A Diophantine question (probably a continued-fraction question); not worked.
3. **Which wedge to name.** A right angle is exact ($N=1$) and a straight wedge is two of them. The interior wedge of an equilateral triangle or a regular hexagon needs a Length (level 5), so no rational step reaches it, and other wedges are approximated by a rational step. The relation to the exact table of [[Exact Slopes]] and to the 15 triangle cases of [[Constructible Trigonometry]] is open.
4. **Rational against constructible.** This is Wildberger's rational trigonometry in the vault's dress (spreads, spread polynomials); the comparison with constructible trigonometry is [[Future Directions]] item 9, still unwritten.
5. **Fourier on the tick set.** [[Fourier Analysis]] asks for a rational Fourier basis; $y_k$ and $x_k$ over the tick set are the natural candidates, and the orthogonality of $x_j$ against $y_k$ over a stated window is not worked here.

## Related

[[Sum of Slopes]] · [[Slope]] · [[Exact Slopes]] · [[Slope Approximations]] · [[Function Hierarchy]] · [[Fourier Analysis]] · [[Discrete Calculus]] · [[Constructible Trigonometry]]

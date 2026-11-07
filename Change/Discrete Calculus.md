---
title: Discrete Calculus
type: theory
status: canonical (the two drafts merged; bridge thesis and step-size dial developed)
provenance: murphy (the DC draft; the step-h scaling, the midpoint fact, the threshold rule, the role of E_h, the one-rule section and the arctan question, adopted 2026-11-04) + murphy+ai (the Algebra II / Precalculus supplement) + ai-synthesis (the merge)
sources: "[[SRC Discrete Calculus - From the Line to the Circle (DC draft, 2026-09).tex]], [[SRC Discrete Calculus Draft (Algebra II-Precalc)]]"
updated: 2026-11-04
---

# Discrete Calculus

Calculus on **steps, not slides**: exact, finite, limit-free. Rung 1 of the Change ladder ([[Structure Hierarchies]]).

## The thesis: the missing bridge

High-school algebra already contains calculus in embryo, and does not say so. Slope of a line, arithmetic and geometric sequences, the pattern in a table of values, $\sum$ notation, $P(n,k)$ and $\binom nk$ are all *differences and sums*. Traditional calculus then arrives with a limit, a new notation and a new kind of number, and the student sees no connection.

Discrete calculus is the connection. **One dial, the step size $h$:**

| $h$ | What it is | Where met |
|---|---|---|
| $h=1$ | sequences, tables, $\Delta$ and $\sum$ | Algebra II |
| $h$ any rational | the same rules, scaled; the difference quotient $\Delta_hf/h$ with its exact error | Precalculus |
| $h$ at the threshold | calculus: drop the terms below the resolution of the certificate | [[Infinitesimals]] |

Every rule is proved by algebra on the page, with no limit. Calculus is what is left when $h$ is too small to manage and one agrees, with a stated error bound, to ignore the terms it multiplies.

## The engine: growth of a rectangle

$\Delta f$ is the growth of $f$ over one step: a quantity $f$ that grows becomes $f+\Delta f$. Every rule below comes from multiplying out expressions of the form $(f+\Delta f)(g+\Delta g)$ and reading the pieces. $\Delta$ is linear: $\Delta(cf)=c\,\Delta f$ and $\Delta(f+g)=\Delta f+\Delta g$.

### Product rule: the rectangle

Take a rectangle $f$ wide and $g$ tall; its area is $fg$. Grow the width by $\Delta f$ and the height by $\Delta g$. The new rectangle is the old one plus three pieces:

![[DiscreteProductRule.svg|380]]

- a strip along the side, $g\cdot\Delta f$;
- a strip along the top, $f\cdot\Delta g$;
- a **corner**, $\Delta f\cdot\Delta g$.

$$\Delta(fg)=f\,\Delta g+g\,\Delta f+\Delta f\,\Delta g.$$

Figure: $f=5,\ g=3,\ \Delta f=2,\ \Delta g=1$: the area grows from $15$ to $28$, and $13=5+6+2$.

The corner is the whole difference from continuous calculus. When the steps are $\tfrac1N$ the strips are of size about $\tfrac1N$ and the corner about $\tfrac1{N^2}$; at the threshold it is below the resolution and is dropped. Here it is kept, and it is why the rule is exact.

### The other rules, from the same rectangle

- **Reciprocal.** The rectangle $f$ by $\tfrac1f$ has area $1$ and stays $1$: as one side grows by $\Delta f$ the other changes by $\Delta(1/f)$, and
$$f\,\Delta\!\Bigl(\tfrac1f\Bigr)+\tfrac1f\,\Delta f+\Delta f\,\Delta\!\Bigl(\tfrac1f\Bigr)=0.$$
Collect the $\Delta(1/f)$ terms: $\Delta(1/f)\,(f+\Delta f)=-\Delta f/f$, so
$$\Delta\!\Bigl(\frac1f\Bigr)=\frac{-\Delta f}{f\,(f+\Delta f)}.$$
- **Quotient.** The rectangle $f$ by $\tfrac1g$ grows by the same recipe, and the corner terms cancel:
$$\Delta\!\Bigl(\frac fg\Bigr)=\frac{g\,\Delta f-f\,\Delta g}{g\,(g+\Delta g)}.$$
The denominator is $g(g+\Delta g)$, not $g^2$.
- **Fundamental theorem** ([[Fundamental Theorem of Calculus]]). A running total starts at $f$ and each step adds its $\Delta f$, so $\displaystyle\sum_{x=m}^{n-1}\Delta f(x)=f(n)-f(m)$, telescoping.
- **Summation by parts.** Grow the rectangle step by step from $f_{\text{start}}g_{\text{start}}$ to $f_{\text{end}}g_{\text{end}}$. The total growth is the sum over steps of the side strip, the top strip and the corner:
$$\bigl[fg\bigr]_m^n=\sum_{x=m}^{n-1}f\,\Delta g+\sum_{x=m}^{n-1}g\,\Delta f+\sum_{x=m}^{n-1}\Delta f\,\Delta g.$$
Move two sums across to get $\sum f\,\Delta g$.
- **Squares and cubes.** A square of side $x$ with $\Delta x=1$ grows by two strips of $x$ and a corner of $1$: $\Delta x^2=2x+1$. A cube grows by three faces, three edges and one corner: $\Delta x^3=3x^2+3x+1$. These are the product rule applied twice.

## Falling powers: the basis adapted to $\Delta$

$x^{\underline k}=x(x-1)\cdots(x-k+1)$, which is the permutation count $P(x,k)$. Then

$$\Delta x^{\underline k}=k\,x^{\underline{k-1}}\qquad(\text{exact}).$$

Proof by induction with the product rule: write $F=x^{\underline{k-2}}$, so $x^{\underline{k-1}}=(x-k+2)F$ and $x^{\underline k}=(x-k+1)(x-k+2)F$. With $f=x^{\underline{k-1}}$, $g=x-k+1$, $\Delta g=1$:

$$\Delta x^{\underline k}=(x-k+1)(k-1)F+(x-k+2)F+(k-1)F=F\bigl[(k-1)(x-k+1)+x+1\bigr]=k(x-k+2)F=k\,x^{\underline{k-1}}.$$

The corner is why falling powers win: for $x(x-1)$ the width grows by $1$ while the height $x-1$ grows by $1$ as well, and $x\cdot1+(x-1)\cdot1+1\cdot1=2x$. Equivalently the rectangle $x$ by $x-1$ is the $x$-square with a row removed; it becomes the $x$-square with a column added, and the difference is two strips of length $x$ with no corner left over.

Ordinary powers are not adapted: $\Delta x^2=2x+1$, $\Delta x^3=3x^2+3x+1$. Convert with the Stirling recurrence $x\cdot x^{\underline k}=x^{\underline{k+1}}+k\,x^{\underline k}$:

$$x^2=x^{\underline2}+x^{\underline1},\qquad x^3=x^{\underline3}+3x^{\underline2}+x^{\underline1}$$

(the coefficients $1;\ 1,1;\ 1,3,1$ are the Stirling numbers of the second kind).

**Worked example: sum of squares.** $x^2=x^{\underline2}+x^{\underline1}$, and the antidifference of $x^{\underline k}$ is $x^{\underline{k+1}}/(k+1)$, so

$$\sum_{x=0}^{n-1}x^2=\frac{n^{\underline3}}3+\frac{n^{\underline2}}2.$$

For $n=5$: $\tfrac{60}{3}+\tfrac{20}{2}=30=0+1+4+9+16$.

## High-school algebra, read as discrete calculus

| High-school topic | In discrete-calculus terms |
|---|---|
| Slope of a line $\Delta y/\Delta x$ | the first difference quotient; a line is a function with constant $\Delta$ |
| Arithmetic sequence | constant $\Delta$ |
| Quadratic | constant $\Delta^2$ (second difference) |
| Geometric sequence $b^n$ | eigenfunction: $\Delta b^n=(b-1)b^n$ |
| $\sum$ notation and sum formulas | antidifference; the fundamental theorem is telescoping |
| $P(n,k)$, $\binom nk$ | falling powers; $\binom nk=n^{\underline k}/k!$ |
| "Find the pattern in the table" | a difference table; the degree is the order at which $\Delta^j$ becomes constant |
| Polynomial fitting | Newton's forward formula $f(n)=\sum_j\binom nj\Delta^jf(0)$ |
| Binomial theorem | $\Delta x^k=(x+1)^k-x^k$ (the row of Pascal's triangle with the top term removed) |
| Compound interest | $\Delta b^n$ with $b=1+r$; the road to $e$ |
| $i^n$, powers of a root of unity | rotating sequences ($\cos_4,\sin_4$ below) |

**Worked example: a difference table detects a cubic.** $f(n)=n^3-2n+5$ gives

| $n$ | 0 | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|---|
| $f$ | 5 | 4 | 9 | 26 | 61 | 120 |
| $\Delta f$ | $-1$ | 5 | 17 | 35 | 59 | |
| $\Delta^2f$ | 6 | 12 | 18 | 24 | | |
| $\Delta^3f$ | 6 | 6 | 6 | | | |

The third difference is constant, so $f$ is a cubic, and the first entry of each row gives its falling-power form (Newton): $f(n)=5-n^{\underline1}+3\,n^{\underline2}+n^{\underline3}$ (coefficients $\Delta^jf(0)/j!$). Check $n=3$: $5-3+18+6=26$.

## The step-size dial: from $\Delta$ to the derivative

With step $h$ on the lattice $x,\,x+h,\,x+2h,\dots$ write $\Delta_hf$ for the growth of $f$ over one step of size $h$, and the **difference quotient** $D_hf=\Delta_hf/h$. Everything above scales: the falling power with step $h$, $x^{\underline k}_h=x(x-h)(x-2h)\cdots(x-(k-1)h)$, satisfies $\Delta_hx^{\underline k}_h=kh\,x^{\underline{k-1}}_h$ exactly (checked), so $D_hx^{\underline k}_h=k\,x^{\underline{k-1}}_h$.

**Worked example: the cubic at $x=5$.** $D_h x^3=\dfrac{(x+h)^3-x^3}{h}=3x^2+3xh+h^2$ exactly. At $x=5$:

| $h$ | $1$ | $\tfrac1{10}$ | $\tfrac1{100}$ | the part free of $h$ |
|---|---|---|---|---|
| $D_hx^3$ | $91$ | $76.51$ | $75.1501$ | $75$ |

The slope is the $h$-free part, $3x^2=75$, and the error is exactly $3xh+h^2$. For a polynomial the difference quotient is a polynomial in $h$ and the derivative is its constant term. For $1/x$: $D_h(1/x)=-1/\bigl(x(x+h)\bigr)$, constant term $-1/x^2$. Nothing is estimated.

*Midpoint fact*: for $x^2$, $D_hx^2=2x+h=2\bigl(x+\tfrac h2\bigr)$, so the secant slope is exactly the tangent slope at the midpoint (Archimedes' observation).

**Worked example: the integral as a sum with its error.** Left sum of $x^2$ on $[0,1]$ with $n$ steps of $h=1/n$, by the falling-power sum:

$$\sum_{k=0}^{n-1}\Bigl(\tfrac kn\Bigr)^2\tfrac1n=\frac13-\frac1{2n}+\frac1{6n^2}.$$

$n=2$: $\tfrac18$; $n=4$: $\tfrac7{32}$; $n=10$: $\tfrac{57}{200}$ (all checked). "$\int_0^1x^2\,dx=\tfrac13$" is the $n$-free part, and the certificate is the explicit error $-\tfrac1{2n}+\tfrac1{6n^2}$.

**The rule at the threshold**: if $h$ is an infinitesimal in the sense of [[Infinitesimals]] (the reciprocal of a number past the threshold), then $f(x+h)=f(x)+h\,f'(x)$ exactly when $h^2=0$, and $D_hf=f'(x)$ is the first-order statement. Discrete calculus adds what the dual numbers lack: the exact error for $h\ne0$.

## Exponentials, logarithms, $e$

- **Exponential:** $\Delta b^n=(b-1)b^n$ (eigenfunction, eigenvalue $b-1$). Base 2 is $\Delta2^n=2^n$.
- **Step $h$:** on the lattice $h\mathbb Z$ the function $E_h(x)=(1+h)^{x/h}$ has $D_hE_h=E_h$ exactly. It plays the role of $e^x$ with a certificate attached. $e$ is approached by $E_{1/N}(1)=(1+\tfrac1N)^N$: $2,\ \tfrac94,\ \tfrac{625}{256},\ \tfrac{25937424601}{10^{10}}$ for $N=1,2,4,10$. Each is a rational number; $e$ is the family with its error bound.
- **Logarithm:** $H_n=\sum_{k=1}^n\frac1k$ has $\Delta H_n=\frac1{n+1}$ exactly. It is the antidifference of $1/n$, which falling powers cannot supply, as $\ln$ is the missing antiderivative of $x^{-1}$. The Euler–Mascheroni constant $\gamma=\lim(H_n-\ln n)\approx0.5772$ is the gap between the discrete and continuous logarithms: *the cost of discretization*. $H_n$ is unbounded: $H_{2^k}\ge1+\tfrac k2$ (group the terms in blocks of $2,4,8,\dots$, each block $>\tfrac12$).
- The antidifference of $\dfrac1{n(n+1)}$ is $-\dfrac1n$, since $\Delta\frac1n=-\dfrac1{n(n+1)}$.

## Algebra II prelude: alternating and rotating sequences

- $(-1)^n$; the floor $\lfloor x\rfloor$ (rounds toward $-\infty$: $\lfloor-2.3\rfloor=-3$); $n\bmod m=n-m\lfloor n/m\rfloor$; $(-1)^n=1-2(n\bmod2)$ ([[Modular Arithmetic]]).
- **Rotating sequences:** $\cos_4(n)=\operatorname{Re}(i^n)$, $\sin_4(n)=\operatorname{Im}(i^n)$ (period 4, the values $1,0,-1,0$ and $0,1,0,-1$), with $\cos_4(n)+\sin_4(n)=(-1)^{\lfloor n/2\rfloor}$ and $\cos_4(n)-\sin_4(n)=(-1)^{\lfloor(n+1)/2\rfloor}$. By the exponential rule with $b=i$: $\Delta\cos_4=-\cos_4-\sin_4$, $\Delta\sin_4=\cos_4-\sin_4$.
- **Spiral walk:** after $n$ steps of lengths $1,2,3,\dots$ turning left each time, the position is $S_n=\sum_{k=1}^nk\,i^{k-1}$; every block of four contributes $1+2i-3-4i=-2-2i$.

## Part II: the circle

(The page keeps the vault's slope language: see [[Slope]], [[Sum of Slopes]].)

**Rational parametrization.** $C(t)=\dfrac{1-t^2}{1+t^2}$, $S(t)=\dfrac{2t}{1+t^2}$, with $C^2+S^2=1$. Here $t$ is the slope of the half-wedge: the whole wedge has $\cos=1/\ell_{2x}=C(t)$ and slope $m_{2x}=S(t)/C(t)$ ([[Characteristic Length]]).

**The $\oplus$ operation:** $t\oplus u=\dfrac{t+u}{1-tu}$, the slope-addition law. Identity $0$, inverse $-t$, commutative, and associative: $(t\oplus u)\oplus v=\dfrac{t+u+v-tuv}{1-tu-tv-uv}$, which is symmetric in $t,u,v$. When $tu=1$ the sum is $\infty$ ($1\oplus1=\infty$); to keep a group, work on the projective line $\mathbb P^1(\mathbb K)$.

**Addition formulas** (pure rational algebra): $C(t\oplus u)=C(t)C(u)-S(t)S(u)$, $S(t\oplus u)=S(t)C(u)+C(t)S(u)$.

**Worked example.** $t=\tfrac12$: $(C,S)=(\tfrac35,\tfrac45)$. $u=\tfrac13$: $(\tfrac45,\tfrac35)$. Then $t\oplus u=\dfrac{5/6}{5/6}=1$, and $C=\tfrac35\cdot\tfrac45-\tfrac45\cdot\tfrac35=0$, $S=\tfrac{16}{25}+\tfrac9{25}=1$. A wedge of slope $\tfrac12$ and one of slope $\tfrac13$ together make a right half-wedge (slope 1): a right angle's half.

**Circular difference:** $\Delta_{\oplus,u}f(t)=f(t\oplus u)-f(t)$, with
$\Delta_{\oplus,u}C=(C(u)-1)C-S(u)S$, $\ \Delta_{\oplus,u}S=S(u)C+(C(u)-1)S$, and the telescoping theorem $\sum_{n<N}\Delta_{\oplus,u}f(t_n)=f(t_N)-f(t_0)$ for $t_n=t_{n-1}\oplus u$.

**Stepping by $u=\tfrac12$ from $t_0=0$:**

| $n$ | 0 | 1 | 2 | 3 | 4 |
|---|---|---|---|---|---|
| $t_n$ | $0$ | $\tfrac12$ | $\tfrac43$ | $\tfrac{11}2$ | $-\tfrac{24}7$ |
| $(C,S)$ | $(1,0)$ | $(\tfrac35,\tfrac45)$ | $(-\tfrac7{25},\tfrac{24}{25})$ | $(-\tfrac{117}{125},\tfrac{44}{125})$ | $(-\tfrac{527}{625},-\tfrac{336}{625})$ |

Pythagorean triples $3\text{-}4\text{-}5$, $7\text{-}24\text{-}25$, $44\text{-}117\text{-}125$, $336\text{-}527\text{-}625$: a rotating sequence of rational points that never repeats. With $u=1$ the same construction gives period 4, the sequence $\cos_4,\sin_4$ above. The family $u=\tfrac1N$, the size of its fractions and the reason it never closes are on [[Rational Rotation]].

### One rule for the line and the circle

Put $z(t)=C(t)+iS(t)$. The addition formulas say $z(t\oplus u)=z(t)\,z(u)$. For *any* function $\varphi$ that turns the step into a product, $\varphi(s\ast u)=\varphi(s)\varphi(u)$,

$$\Delta_u\varphi=\bigl(\varphi(u)-1\bigr)\varphi\qquad(\text{proof: }\varphi(s\ast u)-\varphi(s)=\varphi(s)\varphi(u)-\varphi(s)).$$

- Flat line, step group $(\mathbb Z,+)$: $\varphi(n)=b^n$, giving $\Delta b^n=(b-1)b^n$.
- Circle, step group $(\mathbb P^1,\oplus)$: $\varphi=z$, giving $\Delta_{\oplus,u}z=(z(u)-1)z$. Real and imaginary parts are exactly the circular derivatives above.
- With $u=1$: $z(1)=i$, so $\Delta i^n=(i-1)i^n$, the $\cos_4,\sin_4$ rules. The $\cos_4,\sin_4$ sequence is the circle sequence for the step $u=1$ ($t_n=1,\infty,-1,0,\dots$).

So the exponential rule and the circular derivatives are the same theorem. The discrete sine and cosine are the exponentials of the circle group.

**The arctan question**. The draft calls $\tfrac1{1+t^2}=\tfrac{1+C(t)}2$ "the discrete analogue of $\int\frac{dt}{1+t^2}=\arctan t$". But $\Delta_{\oplus,u}t=\dfrac{u(1+t^2)}{1-tu}$, so $\dfrac{\Delta t}{1+t^2}=\dfrac u{1-tu}$, and the draft writes down no antidifference for it. Where an antiderivative would be, the circle gives the **step count**: if $t_n=n\otimes u$, the antidifference of "one step" is $n$. That is what an angle measure would be here, and it is a natural number or nothing.

## The grand principle

**Chain rule.** $\Delta(f\circ g)$ does not factor as $(\Delta f)(g)\cdot\Delta g$. It does reduce when the inner map is affine, which is a change of step: $\Delta[f(an+b)]=(\Delta_af)(an+b)$ (checked for $f=n^3$, $a=3$, $b=2$). So substitution survives only as rescaling the step.

**Change of representation, not change of variables.** *Discrete calculus is substantially the art of finding the basis or representation adapted to the operator.*

| Operator | Maladapted | Adapted |
|---|---|---|
| $\Delta$ | $x^k$ | falling powers $x^{\underline k}$ (Stirling numbers convert) |
| $\Delta$ | $1/n$ | harmonic numbers $H_n$ |
| $\Delta_\oplus$ | $\dfrac1{1+t^2}$ | $\dfrac{1+C(t)}2$ |

The same calculus with the step below the resolution of the certificate is [[Calculus]]: $f(x+\varepsilon)=f(x)+f'(x)\varepsilon$ with $\varepsilon^2=0$. The corner $\Delta f\,\Delta g$ of the product rule becomes $f'g'\varepsilon^2=0$, and the chain rule, which fails here, holds there.

## Why it belongs in this vault

- **Certificate-clean:** every identity is proved by direct computation, exact. It is the "discrete foundation on which the abstraction of limits can be built."
- **Ultrafinitism:** a lattice with step $h$ at the threshold is a calculus with infinitesimals ([[Infinitesimals]]); the step is the reciprocal of a number past the threshold, and the first-order calculus carries an explicit error term ([[Future Directions]] item 5).
- **No angle measure:** the circle part is built from slopes and $\oplus$, as in [[Constructible Trigonometry]].
- **Tests for [[Future Directions]] item 5:** the fundamental theorem and the product rule are above, exact. $\int_1^e dx/x=1$ remains: its discrete form is $H_n$ against $E_h$.

## Hard problems

1. **The threshold and the dial.** "Drop the terms that $h$ multiplies" is exact for polynomials and rational functions (cancel, then set $h=0$). For $E_h$, $H_n$ and the circle, what is the certificate that licenses the passage? The error terms are explicit in the examples above, but no general statement is given for non-polynomial $f$. The named ancestors now have their certificates on [[Derivatives with Certificates]]; the general statement is the bridge theorem of the Agenda.
2. **$\gamma$.** $\gamma=\lim(H_n-\ln n)$ is a Level-11 object defined through $\ln$ (the logarithm that $e$, Level 9, is defined by), so "cost of discretization" is a gap between two objects of different standing ([[Number Hierarchy]]).
3. **Higher order.** Second differences are constant for quadratics and give $\Delta^2$ rules; Taylor remainders at the threshold need $h^3=0,\ h^4=0,\dots$ (see [[Infinitesimals]], hard problem 4).
4. **Part II is thin:** five short sections. Open: a second circular difference (the oscillator $\Delta^2 z=(z(u)-1)^2z$), summation of $\sum S(t_n)$, and the hyperbolic case.

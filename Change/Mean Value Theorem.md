---
title: Mean Value Theorem
type: theorem
status: "canonical (the exact statement rejected as EVT is; the inequality form and an approximate point form kept)"
provenance: "murphy (the position, MVT is about the same argument as EVT since it depends on it; the constructed failure, adopted 2026-11-04) + ai-synthesis (the dependence, the proof from telescoping, the cost, the flagged problems)"
sources: "[[Extreme Value Theorem]], [[Intermediate Value Theorem]], [[Fundamental Theorem of Calculus]], [[Calculus]], [[Certificates]]"
updated: 2026-10-09
---

# Mean Value Theorem

> **Standard statement.** If $f$ is continuous on $[a,b]$ and differentiable on $(a,b)$, there is a point $c$ in $(a,b)$ with
> $$f'(c)=\frac{f(b)-f(a)}{b-a}.$$

The slope of the chord equals the slope of the curve at some point between the ends.

## It depends on the EVT, and inherits its problems

The standard proof goes through **Rolle's theorem**. Subtract the chord: $g(x)=f(x)-f(a)-m(x-a)$ with $m=\frac{f(b)-f(a)}{b-a}$, so $g(a)=g(b)=0$. By the extreme value theorem $g$ attains a maximum and a minimum; unless $g\equiv0$, one of them is at an interior point $c$, and there $g'(c)=0$ (Fermat), so $f'(c)=m$.

So the point $c$ is **the location of an extremum of $g$**. Everything rejected on [[Extreme Value Theorem]] comes with it, in the same three forms:

1. **The point is claimed as a completed object**, the location of a supremum, from completeness.
2. **Its location is unstable.** (A constructed failure, below.)
3. **Its cost is hidden**, and, as for the EVT, it is exponential in the digits of precision.

The statement is rejected as is, for the same argument, and the vault keeps what survives.

### A constructed failure of the statement

The failure is of the *statement*, not only of the proof's choice of $c$. Let $f'-m=w_r$ be the piecewise linear function that starts at $w(0)=1$, descends to $r$ at $x=\tfrac14$, stays at $r$ on $[\tfrac14,\tfrac34]$, then descends to $-(1+6r)$ at $x=1$. Its integral is $0$ for every small $r$, so $f(1)-f(0)=m$ (checked). Then:

- if $r>0$, the only point where $f'=m$ is near $\tfrac34$ (at $\approx0.752$ for $r=0.01$);
- if $r<0$, the only such point is near $\tfrac14$ (at $\approx0.2475$ for $r=-0.01$);
- if $r=0$, every point of $[\tfrac14,\tfrac34]$ qualifies.

With $r$ given by an unsolved search ($r=0$ while it fails, $\pm2^{-m}$ when it succeeds at step $m$), outputting any $c$ with $f'(c)=m$ **exactly** decides the sign of $r$. The same device as in [[Intermediate Value Theorem]] and [[Extreme Value Theorem]]. And yet on the plateau *every* point has $|f'-m|=|r|$, as small as one likes: the **approximate** statement is easy where the exact one is impossible.

## What stays

### The differentiability modulus

As continuity needs a modulus for the IVT and EVT, differentiability needs one here. $f$ is differentiable on $[a,b]$ **with modulus** $\delta_d(\varepsilon)$ if
$$\bigl|f(x+h)-f(x)-f'(x)\,h\bigr|\le\varepsilon\,|h|\qquad\text{whenever }|h|\le\delta_d(\varepsilon)$$
(for $x$ and $x+h$ in $[a,b]$). This is the first-order statement $f(x+h)=f(x)+f'(x)h$ of [[Calculus]], *with its explicit error*, as a certificate. For a polynomial the error is an explicit polynomial in $h$ with a bound read off the coefficients.

### The mean value inequality (the useful theorem)

> **Theorem.** Let $f$ be differentiable on $[a,b]$ with modulus $\delta_d$, let $N$ be a whole number with $h=(b-a)/N\le\delta_d(\varepsilon)$, and let $x_i=a+ih$. Then
> $$\Bigl|\,f(b)-f(a)-h\sum_{i=0}^{N-1}f'(x_i)\Bigr|\le\varepsilon\,(b-a).$$
> In particular, $m=\frac{f(b)-f(a)}{b-a}$ lies within $\varepsilon$ of the mean of the samples $f'(x_i)$, so
> $$\min_if'(x_i)-\varepsilon\le m\le\max_if'(x_i)+\varepsilon,$$
> and, as $\varepsilon$ is arbitrary, **if $m_1\le f'\le m_2$ on $[a,b]$ then $m_1\le m\le m_2$.**

*Proof.* The fundamental theorem of the finite form telescopes: $f(b)-f(a)=\sum_i\bigl(f(x_{i+1})-f(x_i)\bigr)$ ([[Fundamental Theorem of Calculus]]). Each term equals $f'(x_i)h$ within $\varepsilon h$. Add the $N$ errors: at most $N\varepsilon h=\varepsilon(b-a)$. $\square$

No extremum, no Rolle, no EVT: the proof is **the exact finite theorem plus the stated error**. Its consequences are the ones the classical theorem is used for:

- **Lipschitz bound:** $|f'|\le L$ gives $|f(y)-f(x)|\le L|y-x|$. This is the modulus of continuity needed by the IVT and the EVT, from a bound on the derivative.
- **Monotonicity:** $f'\ge0$ gives $f$ non-decreasing.
- **Constancy:** if $f'=0$ everywhere on $[a,b]$ then $|f(b)-f(a)|\le\varepsilon(b-a)$ for every $\varepsilon$, so $f(b)=f(a)$. This proves the uniqueness half of the fundamental theorem of calculus (two antiderivatives differ by a constant), which [[Fundamental Theorem of Calculus]] had to take as an axiom of SIA: it follows from the modulus.

### The approximate point form

> **Approximate MVT.** Under the same hypotheses, and with $f'$ continuous with modulus $\delta'$, there is a rational $x$ in $[a,b]$ with $|f'(x)-m|\le2\varepsilon$.

*Proof.* From the samples, some $x_i$ has $f'(x_i)\ge m-\varepsilon$ and some $x_j$ has $f'(x_j)\le m+\varepsilon$. Apply the approximate IVT ([[Intermediate Value Theorem]]) to $f'-m$ between them. $\square$

**Worked example.** $f(x)=x^3$ on $[0,2]$, $\varepsilon=\tfrac1{10}$. Here $m=\tfrac{8-0}2=4$. The error $f(x+h)-f(x)-3x^2h=3xh^2+h^3$ is at most $\varepsilon h$ for $h\le\varepsilon/7$ on $[0,2]$ (checked at $x=2$), so $\delta_d=\tfrac1{70}$ and $N=140$.

- The sum $h\sum f'(x_i)=7.9145$ against $f(b)-f(a)=8$: difference $0.0855\le\varepsilon(b-a)=0.2$. The mean of the samples is $3.957$ against $m=4$.
- The sample minimum is at $x=0$ ($f'=0$), the maximum near $x=1.986$ ($f'=11.83$). Bisecting $f'-4$ between them ($8$ steps, using $\lceil\log_2\rceil(240)=8$) gives $x=\tfrac{5143}{4480}\approx1.1480$ with $|f'(x)-4|=0.046\le2\varepsilon$.
- The exact point is $c=\tfrac2{\sqrt3}\approx1.1547$.

**Cost.** Finding $x_i$ and $x_j$ takes the $N$ samples, **proportional to $1/\varepsilon$** (exponential in the digits), and the bisection after that is linear in the digits. This is the EVT's cost again, and for the same reason. Nothing is lost by it *as a theorem*: the **inequality form** is a *certificate* one reads off, and one need never run the $N$ samples to use it.

## Where the exact form returns

- **Polynomials.** $f(b)-f(a)=(b-a)\,Q(a,b)$ with $Q$ a polynomial (divided difference), so $m=Q(a,b)$ is an exact expression, and $c$ is a root of $f'(x)=Q(a,b)$, **named** by an isolating interval ([[Fundamental Theorem of Algebra]]). Examples, all exact:
  - $f=x^2$: $m=a+b$, so $c=\tfrac{a+b}2$, the midpoint (the fact from [[Discrete Calculus]]);
  - $f=x^3$: $m=a^2+ab+b^2$, so $c=\sqrt{(a^2+ab+b^2)/3}$; for $a=0,b=2$ this is $\tfrac2{\sqrt3}$, a constructible number ([[Constructible Numbers]]). For $a=\tfrac13$, $b=\tfrac52$: $m=\tfrac{259}{36}$ (checked).
- **Finite lattices.** The chord slope over a range is exactly the mean of the step slopes $\Delta f/h$ (telescoping), so some step has slope $\ge m$ and some $\le m$, and between them the step slopes cross $m$: a finite search, exact ([[Discrete Calculus]]).

## What it was used for

Taylor's remainder (Lagrange form) and L'Hôpital rest on the MVT and on the Cauchy MVT (the same argument with two functions). Here: the remainder for a polynomial is an explicit polynomial, and for a general $f$ it is the modulus $\delta_d$; in each case the error is *stated*, not "for some $c$".

## Hard problems

1. **The order of dependence.** The proof of the inequality form uses only the finite fundamental theorem and a modulus; the EVT is not used. Does the **point form** need only the IVT, as here, or something more for $f'$ merely a derivative (not continuous)? The classical Darboux property (a derivative has the intermediate value property) is not examined.
2. **Higher order.** Taylor's theorem with remainder needs $\varepsilon^{n+1}=0$-type moduli ([[Infinitesimals]], hard problem 4).
3. **Several variables.** The grid costs $(1/\varepsilon)^n$ ([[Extreme Value Theorem]], hard problem 3); the inequality form is dimension-free but the point form is not.

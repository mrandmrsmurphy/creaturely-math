---
title: Derivatives with Certificates
type: theory
status: "canonical (the four certificates with proofs; the general bridge theorem remains open)"
provenance: "murphy (the direction: sin and cos as on-series, never closed; term-by-term differentiation as the formal rule; the discrete ancestors E_h, H_n and the circle as the vault's definitions) + ai-synthesis (the certificates and their proofs)"
sources: "[[Calculus]], [[Discrete Calculus]], [[Rational Rotation]], [[Mean Value Theorem]], [[Number Hierarchy]]"
updated: 2026-11-07
---

# Derivatives with Certificates

The exponential, the logarithm and the circle functions are on-series — ongoing series we can never finish ([[Function Hierarchy]], levels 9–11). The ellipsis is not a certificate. This page writes the certificates: for each function, an explicit bound showing that the formal derivative *is* the derivative, and an explicit error between the discrete ancestor and the classical object.

**What a derivative certificate is.** A *derivative certificate* for $f$ at $x$ is a claimed value $f'(x)$ together with constants $C$ and $h_0$ such that

$$\bigl|f(x+h)-f(x)-f'(x)\,h\bigr|\le C\,h^2\qquad(|h|\le h_0).$$

This is exactly the license for the $\varepsilon^2=0$ calculus of [[Calculus]] — the first-order term is the whole story up to a term quadratic in the step — and it supplies the differentiability modulus of [[Mean Value Theorem]]: $\delta_d(\eta)=\eta/C$. It also answers [[Calculus]]'s existence question for these functions: the number $f'(x)$ exists because the bound exhibits it.

**Why the license must be proved.** Term-by-term differentiation is *false* for general convergent series of functions: $\sum_{n\ge1}\frac{\sin(nx)}{n}$ converges (to the sawtooth), while its formal derivative $\sum\cos(nx)$ diverges — the terms do not even tend to zero. Power series are different, but the difference is a theorem with constants, not a presumption. For the three on-series below, the certificate is the explicit tail control that the factorial denominators buy.

## The on-series and their tails

For rational input $x$ and rational resolution $\varepsilon$, each series is a Pixel factory ([[Numbers, Lengths and Pixels]]): rational bounds out, by tail estimates.

- **exp:** the ratio of consecutive tail terms is $|x|/(k+1)$, so for $|x|\le(N+2)/2$,
$$\Bigl|e^x-\sum_{k=0}^{N}\frac{x^k}{k!}\Bigr|\le\frac{2|x|^{N+1}}{(N+1)!}.$$
- **sin, cos:** alternating series with terms decreasing once the factorial outgrows $x^2$; the error is at most the first omitted term.

## exp

**Functional equation.** $e^x\cdot e^h=e^{x+h}$: the Cauchy product of the two series, since $\sum_{k+j=n}\frac{x^k}{k!}\frac{h^j}{j!}=\frac{(x+h)^n}{n!}$ by the binomial theorem — exact algebra on the coefficients, the tails controlled above.

**Derivative.** $e^{x+h}-e^x-he^x=e^x\bigl(e^h-1-h\bigr)$, and $e^h-1-h=\sum_{k\ge2}h^k/k!$, so for $|h|\le1$:

$$\bigl|e^{x+h}-e^x-h\,e^x\bigr|\le e^{|x|}\,h^2\sum_{k\ge2}\frac1{k!}=e^{|x|}\,h^2\,(e-2)\le e^{|x|}h^2.$$

Certificate: $C=e^{|x|}$, $h_0=1$, where $e^{|x|}$ is itself a Pixel by the tail bound.

**Against the discrete ancestor.** $E_h$ is the lattice exponential: $E_h(0)=1$, $E_h(x+h)=(1+h)E_h(x)$, so $D_hE_h=E_h$ *exactly* ([[Discrete Calculus]]). For $x=nh$, $h>0$:

- $E_h(x)\le e^x$ termwise: $\binom nk h^k=\dfrac{x^k}{k!}\prod_{j<k}\bigl(1-\tfrac jn\bigr)\le\dfrac{x^k}{k!}$.
- The deficit is first-order in $h$: since $1-\prod_{j<k}(1-\tfrac jn)\le\dfrac{k(k-1)}{2n}$ and $\sum_k k(k-1)\frac{x^k}{k!}=x^2e^x$,

$$e^x-E_h(x)\le\frac{x^2e^x}{2n}+\frac{2x^{n+1}}{(n+1)!}=\frac{xh}{2}\,e^x+\text{(tail)}.$$

The tail term is dwarfed by the first for any realistic $n$. So the discrete exponential converges to $e^x$ with an explicit, first-order error — the dial of [[Discrete Calculus]] made quantitative for $\exp$.

## ln

**Definition.** $\ln x$ is the area under $1/t$ from $1$ to $x$ (level 9 of [[Number Hierarchy]]; the certificates are rectangle sums). The functional equation $\ln(xy)=\ln x+\ln y$ is exact from the substitution $t=xu$: a strip of width $\Delta t=x\,\Delta u$ at height $1/t=1/(xu)$ has area $\Delta u/u$.

**Derivative from the shape.** For $h>0$ the strip from $x$ to $x+h$ has height between $1/(x+h)$ and $1/x$, so

$$\frac{h}{x+h}\le\ln(x+h)-\ln x\le\frac{h}{x},\qquad\text{hence}\qquad\Bigl|\ln(x+h)-\ln x-\frac{h}{x}\Bigr|\le\frac{h}{x}-\frac{h}{x+h}=\frac{h^2}{x(x+h)}.$$

For $h<0$ (with $x+h>0$) the same bound holds with the rectangles swapped. Certificate: $C=2/x^2$, $h_0=x/2$. No series is needed: the shape of $1/t$ is the whole argument.

**Against the discrete ancestor.** $H_n=1+\tfrac12+\cdots+\tfrac1n$ is the upper rectangle sum for $\ln$, and

$$\ln(n+1)\le H_n\le 1+\ln n$$

(both by rectangle comparison; checked at $n=1$: $\ln2\le1\le1$). So the harmonic numbers track the logarithm to within $1$ absolutely — the gap's limit $\gamma$ is a level-11 object the vault does not need here.

**Cost.** The $H_n$ route costs $n$ unit additions; the alternating series for $\ln(1+u)$ needs $|u|\le1$; for $x>2$, write $x=2^m u$ with $u\in[1,2)$ (exact rational bookkeeping) and use $\ln x=m\ln2+\ln u$.

## The circle: sin and cos

**The on-series identities.** $\cos^2x+\sin^2x=1$ and the two addition laws hold as exact identities of the on-series: the Cauchy products collapse term by term (checked at low orders: the $x^2$ coefficient of $\cos^2+\sin^2$ is $-1+1=0$, the $x^4$ coefficient $\tfrac13-\tfrac13=0$; the general coefficient vanishes by the binomial convolution). Hence $|\sin x|,|\cos x|\le1$, and $|\sin u|\le|u|$ (for $|u|\le1$ by the alternating tail; for $|u|\ge1$ since $|\sin u|\le1$).

**Derivative certificates.** For $|h|\le1$: $|\cos h-1|\le h^2/2$ and $|\sin h-h|\le|h|^3/6$ (alternating tails), so by the addition laws

$$\bigl|\sin(x+h)-\sin x-h\cos x\bigr|=\bigl|\sin x\,(\cos h-1)+\cos x\,(\sin h-h)\bigr|\le\frac{h^2}{2}+\frac{|h|^3}{6}\le\frac23h^2,$$

and the same for $\cos$ with $-h\sin x$ in place of $h\cos x$. Certificate: $C=\tfrac23$, $h_0=1$.

**Against the discrete ancestor: the rational rotation.** The tick step at level $N$ is a rigid rotation of the plane ($a^2+b^2=1$, checked on [[Rational Rotation]]), so the orbit is *exactly* $(\cos k\theta_N,\sin k\theta_N)$, where $\theta_N$ is the wedge of one tick — twice the wedge of slope $1/N$. The arctan on-series with its alternating tail gives

$$\Bigl|\theta_N-\frac2N\Bigr|\le\frac{2}{3N^3}.$$

And $|\sin a-\sin b|\le|a-b|$ (from $\sin a-\sin b=2\cos\frac{a+b}2\sin\frac{a-b}2$ and $|\sin u|\le|u|$), so the orbit against the classical graph:

$$\bigl|\operatorname{dsin}_N(k)-\sin(2k/N)\bigr|\le k\,\Bigl|\theta_N-\frac2N\Bigr|\le\frac{2k}{3N^3}.$$

The vault's honesty note: the orbit never needs radian measure to be *used* — the step count is the vault's angle ([[Discrete Calculus]]). The comparison exists to certify the classical picture against the vault's object, and it says the two agree to $O(k/N^3)$.

## What this closes

- [[Calculus]] hard problem 1 (the existence of $f'$ for $\exp$, $\ln$, $\sin$, $\cos$): the certificates above exhibit the derivatives with constants.
- [[Mean Value Theorem]] hard problem 1 (where $\delta_d$ comes from for these functions): $\delta_d(\eta)=\eta/C$ with $C=e^{|x|}$, $2/x^2$, $\tfrac23$ respectively.
- [[Calculus]] hard problem 2 (the bridge from $h^2\ne0$ to $\varepsilon^2=0$): answered *for these four functions* — the discarded terms are at most $Ch^2$, below any stated resolution once $h\le\min(h_0,\eta/C)$. The general bridge theorem (arbitrary $f$) remains open and stays on the Agenda.
- The term-by-term question: for these three on-series the formal derivative is *proved* the derivative, with constants. The sawtooth warning stands for general series.

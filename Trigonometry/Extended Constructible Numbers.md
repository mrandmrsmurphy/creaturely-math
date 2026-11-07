---
title: Extended Constructible Numbers
type: concept
status: canonical
provenance: murphy (definition); murphy+ai (teaching of addition, worked cases)
sources: "Murphy's Constructible Trigonometry textbook (2026)"
updated: 2026-10-07
---

# Extended Constructible Numbers

The number system of [[Constructible Trigonometry]]: the constructible field $\mathbb K$ ([[Constructible Numbers]]) with one extra symbol, $\infty$, the [[Slope]] of a vertical line and of a right angle.

## Definition

$$\mathbb K^+=\mathbb K\cup\{\infty\},$$

where arithmetic involving $\infty$ is largely **undefined**:

- For all $x\in\mathbb K$, $x+\infty$ and $\infty+x$ are undefined.
- For all $x\in\mathbb K$, $x\cdot\infty$ and $\infty\cdot x$ are undefined.
- For all $x\in\mathbb K$, $x/\infty$ and $\infty/x$ are undefined.
- For all $x\in\mathbb K$, $x/0=\infty$.
- $\infty\div\infty=1$.

So $\infty$ is not a number to compute with. It is a *value* that division by $0$ produces, and that a right angle has. Arithmetic is done in $\mathbb K$; $\infty$ is handled by stated rules.

**Open.** As written, $x/0=\infty$ includes $x=0$. Presumably $x\ne0$ is meant ($0/0$ is the slope between two equal points, which has no direction). $\infty$ also has no sign: there is no $-\infty$.

## Adding slopes in $\mathbb K^+$

The [[Sum of Slopes]] formula $\dfrac{m_A+m_B}{1-m_Am_B}$ adds and multiplies slopes, so it cannot be applied when a slope is $\infty$ — those operations are undefined. Addition of wedges is therefore taught **by cases**, and $\infty$ is never substituted into the formula:

| $m_A,\ m_B$ | $m_A\oplus m_B$ | why |
|---|---|---|
| both in $\mathbb K$, $m_Am_B\ne1$ | $\dfrac{m_A+m_B}{1-m_Am_B}$ | the formula |
| both in $\mathbb K$, $m_Am_B=1$ | $\infty$ | denominator $0$, numerator $\ne0$, so $x/0=\infty$: the wedges are complementary and make a right angle |
| $\infty$ and $m\ne0$ | $-\dfrac1m$ | a right angle plus a wedge turns it a quarter-turn; this uses only division in $\mathbb K$ |
| $\infty$ and $0$ | $\infty$ | adding nothing |
| $\infty$ and $\infty$ | $0$ | two right angles make a straight wedge |

Worked: $1\oplus1=\infty$; $2\oplus\tfrac12=\infty$; $\infty\oplus2=-\tfrac12$; $\infty\oplus\infty=0$. In row two the numerator is never $0$: $m_A=-m_B$ would give $m_Am_B=-m_A^2\le0\ne1$.

### Example

Let $m_1=\sqrt3$ and $m_2=\infty$ in $\mathbb K^+$. Then
$$
\begin{aligned}
m_1\oplus m_2&=\frac{\sqrt3+\infty}{1-\sqrt3\cdot\infty} && \text{the Sum of Slopes formula}\\
&=\frac{\frac{\sqrt3}{\infty}+\frac{\infty}{\infty}}{\frac1\infty-\sqrt3\,\frac{\infty}{\infty}} && \text{divide through by }\infty\\
&=\frac{0+1}{0-\sqrt3} && \text{the definition}\\
&=-\frac{\sqrt3}{3}.
\end{aligned}
$$
Here $\sqrt3$ is the slope of the wedge of an equilateral triangle, and $\infty$ is a right angle. Their sum is the slope of the wedge an equilateral wedge plus a right angle makes: the interior wedge of a regular dodecagon, with slope $-\sqrt3/3$. Addition in $\mathbb K^+$ preserves the geometric relationship between slopes and wedges, even for infinite slopes. The case table gives the same answer: $\infty\oplus\sqrt3=-1/\sqrt3=-\sqrt3/3$.

**Open.** The divide-through steps use $\sqrt3/\infty=0$ and $1/\infty=0$, which the definition above lists as undefined. Either add "$x/\infty=0$" to the definition (and read the substitution as a formal device that the case table justifies), or teach this example by the case table. The result is the same either way.

The one place $\infty$ is divided is $\infty\div\infty=1$: for a right angle, $\ell/m=\infty\div\infty=1$ (for a right angle, $m/\ell$ is $1$), so the [[Law of SAS Area]] gives $Q=\tfrac12ab$ when $C$ is a right angle.

The cases agree with writing slopes as ratios $[p:q]$ ($\infty=[1:0]$) and adding by $[p_1q_2+p_2q_1:\,q_1q_2-p_1p_2]$, which is never $[0:0]$ over a real field. That is a check, not the definition.

---
title: Nested Radicals
type: method
status: canonical (draft)
provenance: "murphy (article: nested radicals, the golden pair, the quartet, the claim that every polygon slope is a nest); murphy+ai (the doubled reciprocal length $k$, the doubling and halving rules, the quartet as conjugates, the polygons covered; every identity checked numerically)"
sources: "images/constructible.tex"
updated: 2026-10-08
---

# Nested Radicals

Halving a wedge takes a square root, so repeated halving builds **nested radicals**. This page is the machinery; the resulting values are on [[Exact Slopes]].

## The doubled reciprocal length

Write

$$k_x=\frac{2}{\ell_x}\qquad(\text{other frameworks: }2\cos x).$$

For a wedge $x$ with characteristic length $\ell_x$ ([[Characteristic Length]]), $k_x$ lies between $-2$ and $2$: a straight wedge has $k=-2$, a right angle has $k=0$ ($\ell=\infty$), and a vanishing wedge has $k=2$. Two rules, derived from [[Characteristic Length#Half a wedge]] and [[Sum of Slopes]]:

**Doubling.** $\ell_{2x}=\dfrac{\ell_x^2}{1-m_x^2}=\dfrac{\ell_x^2}{2-\ell_x^2}$ (as $\ell^2=1+m^2$), so

$$k_{2x}=k_x^2-2,\qquad m_{2x}=\frac{2m_x}{1-m_x^2}.$$

**Halving.** Inverting, for a wedge $x$ narrower than a straight wedge (so $x/2$ is acute),

$$k_{x/2}=\sqrt{2+k_x},\qquad m_{x/2}=\sqrt{\frac{2-k_x}{2+k_x}}=\sqrt{\frac{\ell_x-1}{\ell_x+1}}.$$

The last form uses the signed $\ell_x$: for an obtuse $x$, $\ell_x<0$ and $\dfrac{\ell_x-1}{\ell_x+1}=\dfrac{|\ell_x|+1}{|\ell_x|-1}>0$, so the same formula gives a half-wedge steeper than a slope of $1$, as it must. This is what the $\mp/\pm$ of the article's half-slope formula was recording, and signed $\ell$ makes it automatic. The root is always the positive one.

The doubling rule is the Chebyshev recursion: $k_{nx}=2T_n(k_x/2)$.

## Halving from the basic wedges

| wedge | $k$ | |
|---|---|---|
| straight (half a turn) | $-2$ | halves to a right angle |
| right angle (a quarter turn) | $0$ | |
| an eighth of a turn | $\sqrt2=\sqrt{2+0}$ | |
| a sixteenth | $\sqrt{2+\sqrt2}$ | |
| a thirty-second | $\sqrt{2+\sqrt{2+\sqrt2}}$ | and so on, indefinitely |
| a sixth of a turn | $1$ | |
| a twelfth | $\sqrt3=\sqrt{2+1}$ | |
| a twenty-fourth | $\sqrt{2+\sqrt3}$ | |

and $m_{x/2}=\sqrt{(2-k_x)/(2+k_x)}$ for each. The article writes $\sqrt1=\sqrt{2-\sqrt1}$ and $\sqrt3=\sqrt{2+\sqrt1}$ to show that $1$ and $\sqrt3$ are themselves nests.

## The golden pair

The pentagon's numbers, with $\varphi=\dfrac{1+\sqrt5}2$ and $\Phi=\varphi-1=\dfrac{-1+\sqrt5}2$:

- $\varphi=k$ of a tenth of a turn $=\sqrt{2+\Phi}$;
- $\Phi=k$ of a fifth of a turn $=\sqrt{2-\varphi}$.

The minus sign appears because $\Phi^2-2=-\varphi$: doubling a fifth of a turn gives two fifths of a turn, which is obtuse, and $k$ changes sign past a right angle. Numerically $\varphi\approx1.6180339887$ and $\Phi\approx0.6180339887$.

## The quartet

The triangle and the pentagon together give the **fifteen-gon**, and its numbers need four new constants. The article names them $\Xi,\xi,\Upsilon,\upsilon$. They are the doubled reciprocal lengths of the wedges $\tfrac1{30},\tfrac1{15},\tfrac2{15},\tfrac7{30}$ of a turn (in other frameworks $12^\circ,24^\circ,48^\circ,84^\circ$):

| | closed form | nest | value |
|---|---|---|---|
| $\Xi$ | $\dfrac{-1+\sqrt5+\sqrt{30+6\sqrt5}}4$ | $\sqrt{2+\xi}$ | $1.9562952015$ |
| $\xi$ | $\dfrac{1+\sqrt5+\sqrt{30-6\sqrt5}}4$ | $\sqrt{2+\Upsilon}$ | $1.8270909153$ |
| $\Upsilon$ | $\dfrac{1-\sqrt5+\sqrt{30+6\sqrt5}}4$ | $\sqrt{2-\upsilon}$ | $1.3382612127$ |
| $\upsilon$ | $\dfrac{-1-\sqrt5+\sqrt{30-6\sqrt5}}4$ | $\sqrt{2-\Xi}$ | $0.2090569265$ |

Checked: each closed form equals $2\cos$ of its wedge, and each nest relation holds numerically.

- **They are a cycle under doubling:** $\Xi^2-2=\xi$, $\xi^2-2=\Upsilon$, $\Upsilon^2-2=-\upsilon$, $\upsilon^2-2=-\Xi$.
- **They are one number and its conjugates.** $\Xi$, $\upsilon$, $-\Upsilon$, $-\xi$ are the four roots of
$$x^4+x^3-4x^2-4x+1=0,$$
the minimal polynomial of $\Xi$ (degree $4=\varphi(30)/2$). So the quartet is not four new ideas but the four conjugates of one, up to sign, which is why their closed forms differ only by the signs inside $\pm1\pm\sqrt5\pm\sqrt{30\pm6\sqrt5}$.

## Which wedges these cover

The seeds $\{1,\sqrt2,\sqrt3\}$, the golden pair, and the quartet, with repeated halving, give $k$ and so the slope of **every wedge that is a multiple of a $\tfrac1{120}$ of a turn** (in other frameworks every multiple of $3^\circ$) and every repeated half of one. These are the wedges of the regular polygons whose odd part of $n$ divides $15$: $n=2^a\cdot\{1,3,5,15\}$.

The **seventeen-gon**, constructible by Gauss, has $k=2\cos(\text{a seventeenth of a turn})$ of degree $8$ over $\mathbb Q$, and $257$ and $65537$ are the other known Fermat primes. Their polygons need further seeds beyond the quartet (from memory, to check).

## Exactness

Every $k$ and every slope here is in $\mathbb K$ ([[Constructible Numbers]]): only field operations and square roots are used, and nothing is approximated. The values are on [[Exact Slopes]].

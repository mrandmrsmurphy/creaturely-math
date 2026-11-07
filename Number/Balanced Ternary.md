---
title: Balanced Ternary
type: concept
status: canonical (draft)
provenance: "murphy+ai (Murphy's brief: his favorite base; the $\\bar1$ notation; the balance-beam weights; base 3 as the most efficient; balanced as modern because negatives are as valid as positives; the Setun computer; the engineering-not-law comment, adopted 2026-11-04. Worked material computed and checked exactly)"
updated: 2026-10-08
---

# Balanced Ternary

**Base 3 with digits $\bar1,\,0,\,1$**, where $\bar1$ ("one-bar") is the digit for $-1$. Each place is worth three times the one to its right, as in [[Binary]], but the digits are symmetric about zero instead of running from $0$ to $2$. Murphy's favorite base.

*Note:* Historical remarks are standard recollections and have not been checked against sources here. Numbers and tables were computed and verified exactly.

## Writing numbers

$$1\bar1\bar1_3 \;=\; 1\cdot9-1\cdot3-1\cdot1 \;=\; 5.$$

The places are $1,3,9,27,81,243,\dots$ Every whole number, positive, negative or zero, has exactly one balanced-ternary form with no leading zeros:

| $n$ | $n_3$ | $-n$ | $(-n)_3$ |
|---|---|---|---|
| 1 | $1$ | −1 | $\bar1$ |
| 2 | $1\bar1$ | −2 | $\bar11$ |
| 3 | $10$ | −3 | $\bar10$ |
| 4 | $11$ | −4 | $\bar1\bar1$ |
| 5 | $1\bar1\bar1$ | −5 | $\bar111$ |
| 6 | $1\bar10$ | −6 | $\bar110$ |
| 7 | $1\bar11$ | −7 | $\bar11\bar1$ |
| 8 | $10\bar1$ | −8 | $\bar101$ |
| 9 | $100$ | −9 | $\bar100$ |
| 10 | $101$ | −10 | $\bar10\bar1$ |
| 11 | $11\bar1$ | −11 | $\bar1\bar11$ |
| 12 | $110$ | −12 | $\bar1\bar10$ |
| 13 | $111$ | −13 | $\bar1\bar1\bar1$ |

**To convert a whole number:** divide by 3. If the remainder is $0$ or $1$, that is the digit. If it is $2$, write $\bar1$ and add one to the quotient (since $2=3-1$). Repeat. Example, $183$:

| 183 ÷ 3 | remainder | digit | next number |
|---|---|---|---|
| 183 | 0 | $0$ | 61 |
| 61 | 1 | $1$ | 20 |
| 20 | 2 | $\bar1$ | 7 |
| 7 | 1 | $1$ | 2 |
| 2 | 2 | $\bar1$ | 1 |
| 1 | 1 | $1$ | 0 |

Reading upward: $1\bar11\bar110_3=243-81+27-9+3=183$.

## The balance beam

You have a two-pan balance and want to weigh any whole number of pounds. The thrifty set of weights is $1,3,9,27,81,\dots$, one of each, and **weights may go on either pan**. Put the object $x$ on the left pan, and write $x$ in balanced ternary:

- digit $1$: that weight goes on the **right** pan (opposite the object);
- digit $\bar1$: that weight goes on the **left** pan (with the object);
- digit $0$: that weight stays off.

At balance, $x+(\text{left weights})=(\text{right weights})$, so $x=(\text{right})-(\text{left})$, which is exactly the balanced-ternary sum.

**Example: $x=7=1\bar11_3=9-3+1$.** Put $9$ and $1$ on the right pan, and $3$ on the left with the object: $7+3=10=9+1$. ✓

**How far do $k$ weights reach?** With $1,3,\dots,3^{k-1}$ every whole number from $-\tfrac{3^k-1}2$ to $\tfrac{3^k-1}2$ is reachable (checked by computing all combinations for $k=4$). Four weights $1,3,9,27$ weigh every whole number up to $40$; five weights up to $121$.

**Compare the weights if they may go only on one pan:** those need the binary set $1,2,4,8,\dots$, and four of them reach only $15$. Letting a weight go on the object's own pan buys more than a doubling: it is the use of a negative digit. The puzzle is old (often credited to Bachet, early 17th century; from memory).

## Why it is efficient

To write numbers up to $N$ in base $b$ one needs about $\log_bN=\ln N/\ln b$ digits, each of which must be chosen from $b$ symbols or states. The "cost" is therefore proportional to $b/\ln b$:

| base $b$ | 2 | 3 | 4 | 5 | 10 | 16 |
|---|---|---|---|---|---|---|
| $b/\ln b$ | 2.885 | **2.731** | 2.885 | 3.107 | 4.343 | 5.771 |

The minimum over all real $b$ is at $b=e\approx2.718$. Among whole numbers the winner is $3$, narrowly ahead of $2$ (and of $4$, which ties $2$ because $4=2^2$). This is the sense in which **3 is the most efficient base**. [[Binary]] has the advantage that two states are the easiest for a machine to tell apart. The margin between $2$ and $3$ is small (about 5%).

## Why balanced

*Balanced* means the digits are $\bar1,0,1$ instead of $0,1,2$. Negatives are built in, and several things get easier:

- **Sign.** The sign of the number is the sign of its leading (leftmost nonzero) digit. No separate sign symbol or sign bit is needed.
- **Negation.** Swap $1$ and $\bar1$ digit by digit (see the table above). No "complement" trick is required.
- **Rounding.** Cutting off digits after the point *is* rounding to the nearest. In ordinary base 3 or base 10 a cut-off number is always rounded down, and rounding to nearest takes an extra step.
- **Symmetry.** The digit set is its own mirror image, $d\mapsto-d$, with no preferred direction.

**A caution on "just as real".** Wildberger stresses that negatives are as important as positives, grounding it in antiparticles. But the physical world is not symmetric: matter vastly outnumbers antimatter, and no one yet knows why. The symmetry of balanced ternary is a property of the digit set, not evidence that the creation weighs plus and minus equally; see [[Theology of Number]] on the theological side.

This matches the story in [[Counting and Bases]]: subtraction fails in ℕ, so zero and the negatives are adjoined (debt, the reverse direction). Balanced ternary treats the negative digit as just as valid as the positive one; we write numbers using both directions from the start.

## Arithmetic

**Multiplication of digits** is the ordinary product: $1\cdot1=1$, $1\cdot\bar1=\bar1$, $\bar1\cdot\bar1=1$, anything times $0$ is $0$. There is no carry from a single-digit product. Multiplying by $3$ appends a $0$.

**Digit by digit, carries dropped,** this is arithmetic mod $3$: the digits $\bar1,0,1$ with their sum and product form the Galois field $\mathrm{GF}(3)=\mathbb Z/3$ ([[Modular Arithmetic]]). For example $1+1=\bar1$ and $\bar1\cdot\bar1=1$ at the digit level, with the carry carried to the next place.

**Addition of digits:** $1+\bar1=0$; $1+1=2=1\bar1$ (write $\bar1$, carry $1$); $\bar1+\bar1=-2=\bar11$ (write $1$, carry $\bar1$). Carry each pair leftward and add it to the next place.

**Example: $7+5$.** $1\bar11+1\bar1\bar1$:

- units: $1+\bar1=0$
- threes: $\bar1+\bar1=-2$: write $1$, carry $\bar1$
- nines: $1+1+\bar1=1$

Result $110_3=9+3=12$. ✓

## Fractions

Places to the right of the point are $\tfrac13,\tfrac19,\tfrac1{27},\dots$ The termination rule of [[Counting and Bases]] applies: $\tfrac1n$ terminates in base 3 exactly when $n$ is a power of 3. So $\tfrac13=0.1_3$ is finite, while $\tfrac12$ is not. $\tfrac12=0.\overline{1}_3=\tfrac13+\tfrac19+\tfrac1{27}+\cdots$ (the bar means the $1$ repeats forever). The sum checks: a geometric series with first term $\tfrac13$ and ratio $\tfrac13$ has sum $\tfrac{1/3}{1-1/3}=\tfrac12$.

## The Setun computer

The **Setun** was a ternary computer built at Moscow State University in the late 1950s (first running 1958) under Nikolay Brusentsov. It stored numbers in **balanced ternary**, with three-state elements (**trits**) instead of two-state bits. Its ternary logic used miniature ferrite magnetic cores and semiconductor diodes, not special "three-level transistors". The machine also contained some ordinary transistors and vacuum tubes in its supporting circuitry, so "no transistors anywhere" would be too strong. A modest number were built and used in the early 1960s, and a successor, Setun-70, followed around 1970. From memory: dates and numbers to be checked.

It is a working demonstration that the choice of base for machines is a matter of engineering, not a law of nature: on counting digits alone, $3$ wins by a hair.

## Other places it appears

- **Three-valued logic:** false / unknown / true as $\bar1,0,1$ (compare the Boolean algebra of [[Binary]]).
- **Kleene's three-valued logic** ([[Three-Valued Logic]]): with true $=1$, unknown $=0$, false $=\bar1$: AND is the minimum, OR is the maximum, NOT is negation, implication is $\max(-x,y)$, and the biconditional is the ordinary product $x\times y$ (checked against Kleene's tables). The words AND and OR are used for min and max so that $+$ and $\times$ keep their meaning of sum and product.
- **Sign of a number:** $-1,0,+1$ is the signum function, a balanced-ternary digit.

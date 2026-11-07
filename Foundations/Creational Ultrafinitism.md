---
title: Creational Ultrafinitism
aliases:
  - Tempered Ultrafinitism
type: concept
status: canonical
provenance: murphy (position; the physical-bound arithmetic and the bound's scope; absolute and relative feasibility) + ai-synthesis (rival critique)
sources: "[[SRC CCE Primer (2026-06)]], [[SRC Confession of Mathematics (2023-24)]], [[SRC me.md Math Section]]"
updated: 2026-11-07
---

# Creational Ultrafinitism

*Earlier name: tempered ultrafinitism.* **Creational** because the bound on a "biggest number" is the bound of the creation we live in: no actualized infinity exists in it, and God alone is infinite and eternal, not bound by his creation (Ps 90:2; Ps 145:3). **Tempered** survives as a description of the *manner*: graduated skepticism, and no quarrel with infinity as a limit-concept ([[Theological Grounds]]).

**How large mathematics is.** Murphy describes himself as "an ultra-finitist … by stalwart conviction" ([[SRC me.md Math Section]]). The version here, graduated rather than hard:

| | Verdict |
|---|---|
| **Potential infinity** (for every $n$ there is $n+1$) | **Accepted.** The natural numbers go on; you never reach the last. |
| **Actual infinity** (a completed $\mathbb{N}$, "bracket closed") | **Rejected.** Claims divine completeness; the Axiom of Infinity is "a theological claim disguised as a mathematical axiom." |
| **Cantorian arguments** (bijection, diagonal) | **Accepted as structural tools / boundary markers**; don't conclude you *possess* what they describe. See [[Infinity and Cantor]]. |
| **Very large finite numbers** | **Graduated skepticism**: past a threshold you hold *notation, not a number*. |

Aristotle (*Physics* III.4–8, 206a–207b): potential infinity belongs to the creature, actual infinity to God. Augustine and Aquinas follow.

## The key line

> *"You may imagine that you can imagine such a number, but you can't actually imagine it."*

- **Meta-level:** I can imagine the *process* (apply the exponent rule, write the notation, describe the algorithm).
- **Object-level:** I cannot *hold* $10^{200}$ in mind. The notation works; the number-as-possessed does not.

## The biggest number: $10^{200}$, as a gradient

Murphy picks **$10^{200}$ as the biggest number**. It is not a line in the sand. Skepticism is **graduated**: small numbers are held fully, and the further up you go, the more you are holding notation rather than a number. $10^{200}$ marks where the gradient ends, not where it begins.

**The physical bound.** There are about $10^{80}$ atoms in the observable universe and about $10^{60}$ Planck times in its age ($4\times10^{17}$ s divided by $5\times10^{-44}$ s). Their product, about $10^{140}$, bounds the number of physical "events." Even counting photons ($\approx10^{89}$) the product is about $10^{150}$. $10^{200}$ exceeds either by 50 to 60 orders of magnitude: beyond any computation the universe could contain. No certificate is possible "even in principle." These are standard estimates, not cited here.

**A sharper physical bound, and what it bounds.** The **Bekenstein bound** limits the information in a region: $I\le2\pi RE/(\hbar c\ln2)$ bits. With rough inputs for the observable universe (radius $4.4\times10^{26}$ m, critical density, so $E\approx3\times10^{71}$ J) this gives about $4\times10^{124}$ bits; the holographic (area) form gives about $3\times10^{123}$, and the Margolus–Levitin limit on operations over the age of the universe about $8\times10^{122}$. These are order-of-magnitude figures with their inputs flagged, and they are tighter than the $10^{140}$ above. They are upper bounds from the total energy; Lloyd's standard estimate is lower, about $10^{120}$ operations on about $10^{90}$ bits (about $10^{120}$ bits counting gravitational degrees of freedom), taken from his abstract as reported ([[Reading List]]). What they bound is **a representation that holds the items separately**: a list of $N$ distinct items needs at least $N$ bits, so $N$ cannot exceed about $10^{123}$–$10^{124}$, and for $N=10^{200}$ (with about $664$ bits to name each item) the list would need about $10^{203}$ bits, some $76$ orders more than the bound. What they do **not** bound is the *notation*: the number $10^{200}$ is described in $664$ bits. That is the vault's distinction between the process (meta-level) and the object ([[Creational Ultrafinitism]], above): the number can be reasoned about by its description; *holding that many items* cannot be done, in the universe or in a mind that is part of it.

**Two parts to the bound.** (1) *No actualized infinity exists in the creation* is a physical claim, and a contested one: space may be unbounded, and singularities (black holes) are where the equations blow up, though inaccessible. (2) The figures above ($10^{80}$ atoms, $10^{140}$ events) are for the **observable** universe. So the working bound is on **what a creature can access of the creation**: creational and creaturely at once, and a stronger claim to make than a fact about the whole cosmos. Scripture's own use of "innumerable" is relative in just this way: beyond number *for Abraham*, numbered by God (Gen 15:5; Gen 41:49; Ps 147:4).

**Esenin-Volpin's answer to "why not one more?"** Alexander Esenin-Volpin was the hard ultrafinitist. Harvey Friedman tells of asking him, in a lecture: *Do you believe in 1? Do you believe in 2? In $2^2$? $2^3$?* and so on up to $2^{100}$. Esenin-Volpin answered **yes** every time, but took longer each time: by Friedman's account, about $2^{100}$ times as long to answer for $2^{100}$ as for $2^1$ (a retelling by Scott Aaronson has the delay doubling at each step). So the answers do not flip at a line. The *cost* of the "yes" grows until it exceeds any possible resources.

That is the gradient. $2^{100}\approx1.27\times10^{30}$ is far below $10^{200}$ and already costs more than anyone could pay to hold digit by digit. The sorites objection ("where is the line?") loses its force when the answer is a cost that rises smoothly with size, not a boundary.

**Absolute and relative feasibility (Murphy).** The threshold question splits in two. *Absolute* feasibility is the philosophical horizon: there is a boundary beyond which a number or operation is not mathematically available to created minds, whatever the computer or technology — the physical bounds above are the working estimate of its upper edge. *Relative* feasibility is the working apparatus: what can be constructed and certified for a particular task, against a stated budget of resources ([[Computational Admissibility]]). The vault needs both, with the relationship defined; the distinction keeps the horizon from depending on any particular machine, and keeps finite notation from being mistaken for an available object.

## Against the alternatives

- **Against actual infinitism:** the diagonal is a boundary, not a collection tool. Almost every real is provably undefinable (the definable reals are countable) — "not a creaturely object."
- **Against standard finitism:** too restrictive. Potential infinity needs no divine capacity; limits and approximation are certificate-explicit; "much of standard analysis can be recovered without the Axiom of Infinity."
- **Against hard ultrafinitism** (Esenin-Volpin): the cutoff problem — *why not one more?* — "that's not a foundation; it's a cliff"; rejecting $n+1$ destabilizes elementary arithmetic; ultrafinitists can't agree where the line is. Murphy's skepticism is about *possession*, not about the rule $n\mapsto n+1$.

## The earlier statement (Confession, 2023)

> "We take it on faith that each and every number has a successor, which cannot be proven. As finite creatures, we cannot count beyond some (very large) number."

So the position predates the 2026 threshold arithmetic — the *principle* was already there; the *physical bound* is the newer move.

## Why the theology matters

Constructivists rarely answer *why* mathematics should be constructive ("more rigorous"). Murphy's answer is theological: **we are not God**, and treating completed infinite objects as available on demand claims divine epistemic capacity. Compare [[Scale and Bands]]: "idolatry of symbolic structure" — mistaking continuity of *notation* for continuity of *nature*. See also [[Five Acts]] (the foundations story as Babel).

## Where it bites in practice

- Induction and the infinitude of primes (taught in [[Proof Types]] as "humility about infinite cases") — are they *potential-infinite* statements, or claims about a completed totality? Item 6 in [[Future Directions]].
- The size of the cosmos: the medieval finite cosmos is argued to be *reasonable*, and modern infinite space a later image (Physics text ch. 10, see [[Number in Natural Philosophy]]).

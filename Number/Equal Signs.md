---
title: Equal Signs
type: concept
status: "draft (synthesis — the mapping is a proposal Murphy has not yet ratified; the pi_n refinement is his)"
provenance: "murphy (both source taxonomies; the pi_n convention) + ai-synthesis (the mapping; the sign-shift observation)"
sources: "[[SRC Mathematics (raw, 2026-05)]], [[SRC Constructible Trigonometry Textbook (md)]]"
updated: 2026-10-11
---

# Equal Signs — reconciling two taxonomies

The corpus has **two** classifications of equality that were developed separately:

**(1) The Constructible Trigonometry catechism ("Three Equal Signs"):**

1. **Exact equality (=)** — both sides exhibited or constructible in 𝕂. e.g. $1+1=2$; $\ell^2=1+m^2$.
2. **Algorithmic equality (≈, or "=" with caveat)** — right side an iterative approximation. e.g. $\sqrt2=1.41421356\ldots$ means the Babylonian method, continued, yields these digits.
3. **Formal identity (≡, or "=" in quotes)** — symbols manipulated by rules, no claim to exhibition. e.g. $\sum n=-\frac1{12}$ (regularized); $e^{i\pi}+1=0$.

The vignette: *"The modern mathematician uses one symbol for all three relations, trusting context. But context has failed."*

**(2) The Number Hierarchy ([[Number Hierarchy]]):** four certificate families — Exact (1–4), Inequality/asymptotic (5–6), Convergence (7–11), Existence-without-exhibition (12–14).

## Proposed mapping

| CT sign | Hierarchy levels | Comment |
|---|---|---|
| Exact (=) | 1–4 (exhibit); **5–6 as lengths** | See "relative to a representation" below |
| Algorithmic (≈) | 7–11 | digits/limits with stated error |
| Formal (≡) | 12–14 and the *defined-by-limit* items in 9–11 | convention or existence only |

## The tension this exposes

- Constructible Trigonometry: "diagonal $=\sqrt2$" is **exact** — the diagonal is *constructed*, and $\sqrt2\in\mathbb K$.
- Hierarchy: constructible numbers have **inequality** certificates; "equality is asymptotic."

Both are right, about different *targets*. The diagonal is exhibited **as a length**; but $\sqrt2=1.414\ldots$ equates it with a **digit string**, which is never exhibited. **Proposal: a certificate is relative to a representation** — (number, representation) pairs, e.g. (√2, geometric length) is exact; (√2, rational) is asymptotic; (√2, decimal) is algorithmic. This is a candidate foundation for the whole hierarchy. [[Future Directions]] item 3.

## The π_n refinement (Murphy)

The $\pi_n$ convention ([[Exact Until Output]]) shifts a border between the signs in the right direction. $\pi_7=3.1415926$ is **exact** (sign 1), because $\pi_7$ is a rational; $\pi=3.1415926\ldots$ is **algorithmic** (sign 2). The subscript converts a sign-2 claim into a sign-1 claim plus an exact inequality, $\pi_n\le\pi<\pi_n+10^{-n}$ — and the inequality is where the certificate lives. Bare $\pi$ offered with digits as its exhibit is the map billed as the land ([[Creaturely Realism]]).

## Cases where the sources disagree

- **$0.\overline9=1$** — Constructible Trigonometry: *formal identity* ("the left side names a process; the right side names a number. To equate them is to equate time with eternity… not wrong, but not innocent"). It is a **level-11** object (a limit): not a well-formed number, since it would require infinite work. Only if you grant the infinite limit concept is it coherent, and then $0.\overline9=1$ as a limit.
- **$\sin^2x+\cos^2x=1$** — *formal identity* if sin and cos are taken as transcendental functions; but in slope language $\ell^2=1+m^2$ is **exact**. The classification depends on whether sin/cos are functions or slope/length.

## Earlier root

The Confession (2023) already says: *"'Equal' in mathematics is not like 'equal' in normal speech."* and the $0.999\ldots$ vignette ([[Certificates]], [[Classroom Questions]]) trains the student to "tremble." The Babylonian habit — "they knew which divisions their system could perform exactly and which it could only approach. We have lost this honesty" — is the historical exemplar. See [[Counting and Bases]].

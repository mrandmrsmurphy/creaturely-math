---
title: Twelve Exercises
aliases:
  - Duodecim Exercitia
  - Noesis Exercises
type: framework
status: "canonical (names, Latin pairs and glosses are Murphy's; each worked example is marked [AI])"
provenance: "murphy (the twelve, their Latin pairs, the glosses: Sources/Quadriga Scientiae - Complete, Part I and Appendix A) + third-party (the Polya heuristics each expands) + ai-synthesis (the worked examples and the observations marked [AI])"
sources: "[[Noesis]], [[Quadriga for Mathematics]], [[Quadriga Scientiae - Complete]]"
updated: 2026-10-10
---

# The Twelve Exercises of Noesis

Twelve paired exercises, each a virtue of intellectual operation with its corresponding vice. They expand the heuristics George Pólya catalogued under *Devising a Plan* in *How to Solve It* (1945): Murphy keeps the content of 1 to 11, gives each a Latin name and a vice, grounds them theologically, and adds 12 (Rest, from Pólya's Poincaré anecdote). "The twelve exercises are not a checklist but a **palette**. The skilled practitioner knows which colour to apply, and when." No single exercise guarantees success; they are conditions of possibility, not recipes ([[Noesis]]).

## The table

| # | Exercise | Latin virtue / vice | Murphy's gloss |
|---|---|---|---|
| 1 | **Analogy** | *Similitudo / Alienatio* (analogy / alienation) | Jesus taught by a barrage of similes; many symbolic problems are understood by their likeness to what is already grasped. Vice: treating every problem as unprecedented. |
| 2 | **Generalization** | *Generalisatio / Fragmentatio* | Seeing your problem as part of a larger whole. Vice: trapped in isolated details. |
| 3 | **Specialization** | *Specialisatio / Levitas* (specialization / superficiality) | Pick a simpler case, reason it through, return with new insight. |
| 4 | **Break it up** | *Partitio / Indivisio* (division / indivisibility) | Subdivide into solvable parts and reassemble. Vice: the problem as an unanalyzable lump. |
| 5 | **Think backwards** | *Inversio / Unidirectio* | "I have the answer: what attributes must it have?" Vice: proceeding only in the direction the problem invites. |
| 6 | **Adding to the problem** | *Adjunctio / Exclusio* (conjunction / exclusion) | Counterintuitively, added parts can make a problem tractable. |
| 7 | **Logical extremes** | *Reductio ad Absurdum / Credulitas* | "If such-and-such were so, nonsense or impossibility would result": exclude avenues. Vice: accepting premises uncritically. |
| 8 | **Induction** | *Inductio / Temeritas* (induction / rashness) | Like recursion: find the process, not a straight line to the answer. Vice: leaping to conclusions on too little. |
| 9 | **Conjecture** | *Conjectura / Paralysis* | Play a hunch to its conclusion, "assuming they are not the same!" Vice: unable to act or think without a guarantee. |
| 10 | **Symmetry** | *Symmetria / Caecitas* (symmetry / blindness) | An eye for beauty "is the heart of mathematics". Careful not to create patterns that are not there. |
| 11 | **Reframing** | *Transpositio / Fixatio* (transposition / fixation) | Translate to another situation, notation or language. |
| 12 | **Rest** | *Incubatio / Anxietas* (incubation / anxiety) | Poincaré never worked on a problem more than a few hours; the mind (or the Spirit) goes on working unattended. Vice: forcing a solution by will. |

## One worked example each, from this vault [AI]

All numbers below were checked by direct calculation. These are my illustrations, not Murphy's; each links to the page where the idea lives.

1. **Analogy.** Forward difference and $\varepsilon$: $\Delta(x^2)=(x+1)^2-x^2=2x+1$, and $(x+\varepsilon)^2=x^2+2x\varepsilon$ when $\varepsilon^2=0$. The same shape, the "2x", appears in both, and the leftover $1$ is the corner of the square that $\varepsilon^2=0$ throws away ([[Discrete Calculus]], [[Calculus]]).
2. **Generalization.** $\Delta 2^n=2^{n+1}-2^n=2^n$ is the case $b=2$ of $\Delta b^n=(b-1)b^n$, which is itself a case of the one rule $\Delta_u\varphi=(\varphi(u)-1)\varphi$ for every homomorphism $\varphi$ ([[Discrete Calculus]]).
3. **Specialization.** Test Fermat's little theorem at small primes before proving it: $2^p\bmod p$ is $2$ for $p=3,5,7,11,13$ and fails for the composite $6$ ($2^6=64\equiv4$), so the test is meaningful ([[Fermat's Little Theorem]], [[GF(5)]], [[GF(7)]]).
4. **Break it up.** Solve $x\equiv2\pmod3$ and $x\equiv3\pmod5$ separately, then reassemble: $x=8\pmod{15}$ ([[Chinese Remainder Theorem]]).
5. **Think backwards.** What must $x$ be if $x^2\equiv-1\pmod5$? Only $x=2$ or $3$, since $2^2=4\equiv-1$ and $3^2=9\equiv-1$ ([[GF(5)]], and the splitting of $x^2+1$ in [[Fundamental Theorem of Algebra]]).
6. **Adding to the problem.** To find $\Delta(fg)$, add the missing corner to the $f\times g$ rectangle: $\Delta(fg)=f\Delta g+g\Delta f+\Delta f\Delta g$ ([[Discrete Calculus]]). Kronecker's adjoining a root of an irreducible polynomial is the same move in algebra ([[Fundamental Theorem of Algebra]]).
7. **Logical extremes.** Suppose $a^2=2b^2$ with $a/b$ in lowest terms: then $a$ is even, so $b$ is even, contradicting lowest terms. This proves *no ratio squares to 2*; it does not prove that an irrational number exists ([[Diagonal Argument]], [[Proof Types]]).
8. **Induction.** The sum of the first $n$ odd numbers is $n^2$ ($1+3+5+\cdots+19=100$ for $n=10$): each step adds the next odd number, the gnomon of the next square. The vault's audit of induction (potential versus completed $\mathbb N$) is in [[Proof Types]] and [[Future Directions]].
9. **Conjecture.** Work out $7^{10}\bmod5$ by the cycle of $2,4,3,1$ and conjecture that every power of $7$ repeats with period $4$; the conjecture is then proved by Euler or Fermat ([[Historical Order]], [[Euler's Theorem]]).
10. **Symmetry.** Wilson for $p=7$: the residues $2,\dots,5$ pair off with their inverses ($2\cdot4\equiv1$, $3\cdot5\equiv1$), leaving $1$ and $6\equiv-1$, so $6!=720\equiv-1\pmod7$ ([[Wilson's Theorem]]). The symmetries of the square (eight of them) are the first hands-on group ([[Symmetries of the Square]]).
11. **Reframing.** Replace the angle by the slope: a wedge is named by $m=\tfrac{\text{rise}}{\text{run}}$, a rational for the triangles that matter, and the angle sum becomes slope addition $\oplus$ ([[Slope]], [[Sum of Slopes]]). The contrapositive is the same exercise at the proof level ([[Proof Types]]).
12. **Rest.** No worked example is possible, which is the point: rest is a practice, not a technique. The source's authority is Poincaré's own account of incubation (anecdote as told by Pólya; not checked here).

## How the Exercises map to proof types

From the planning notes the source reports: the Exercises describe *how you find* a proof, the [[Proof Types]] *what you end with*. Murphy's tags: Counterexample and Contradiction ↔ Logical extremes (7); Contrapositive ↔ Reframing (11); Cases ↔ Break it up (4); Induction ↔ Induction (8); Extremal / minimal counterexample ↔ Specialization (3); Invariant / monovariant ↔ Symmetry (10); and "Extend it" ↔ Generalization (2) with Induction (8).

## Observations [AI]

- **Two vices.** Aristotle's virtues sit between an excess and a deficiency. Appendix A names one vice for each exercise, but the body text sometimes warns of the *other*: Symmetry ("do not create patterns that are not there") is the vice of seeing too much, while *Caecitas* is seeing too little; Conjecture warns of mistaking the hunch for the answer, while *Paralysis* is the opposite fault. Murphy may want the second vice named.
- **Glosses that differ.** The body of Part I glosses *Specialization* as "pick a simpler case" (Pólya's sense), but the Appendix glosses it as "drilling into the specific features that distinguish this problem". *Adding to the Problem* (add auxiliary parts) and *Adjunctio* (bring in outside methods and domains) also read differently. Which sense governs is for Murphy to say; the table above follows the body.
- **No exercise is specific to mathematics.** The twelve are Pólya's, and they travel to any symbolic work. What the vault adds is what they are exercised *on*: finite objects with certificates.

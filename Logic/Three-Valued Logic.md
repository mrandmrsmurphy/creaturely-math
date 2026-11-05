---
title: Three-Valued Logic
type: concept
status: canonical (draft)
provenance: murphy+ai (from Murphy's logic booklet; the laws below were verified by checking every case)
sources: "Murphy's logic booklet, *From Traditional Logic to Ternary Thought*"
updated: 2026-10-08
---

# Three-Valued Logic

Logic with a third value, **unknown** ($U$), besides true ($T$) and false ($F$). The system used here is **Kleene's strong three-valued logic (K3)**. It extends [[Boolean Algebra]] and, written as numbers, is the logic of [[Balanced Ternary]].

## What $U$ means

$U$ is **not "half true."** It marks a proposition whose truth is not yet known (a future event, an unproved conjecture, an unconnected wire) or that has no definite reference ("the future king of France is bald"). *Truth stays one; our access to it is partial.* The third value is about the knower, not about being: this fits [[Creaturely Realism]] (realist about the object, limited in access). It also sits comfortably with [[Certificates]]: $U$ is "no certificate yet," and a $U$ may later resolve to $T$ or $F$, and values already decided never change when it does (K3 is monotone).

## The tables

Negation: $\neg T=F$, $\neg U=U$, $\neg F=T$. The rest:

| $P$ | $Q$ | $P\wedge Q$ | $P\vee Q$ | $P\to Q$ | $P\leftrightarrow Q$ |
|---|---|---|---|---|---|
| T | T | T | T | T | T |
| T | U | U | T | U | U |
| T | F | F | T | F | F |
| U | T | U | T | T | U |
| U | U | U | U | U | U |
| U | F | F | U | U | U |
| F | T | F | T | T | F |
| F | U | F | U | T | U |
| F | F | F | F | T | T |

Rule of thumb: **a value is decided as soon as the known inputs decide it, and otherwise stays $U$.** $F\wedge U=F$ because one false conjunct settles the matter; $T\vee U=T$ likewise; $U\wedge T$ is $U$ because the unknown could still go either way. Implication is $\neg P\vee Q$, and the biconditional is $(P\to Q)\wedge(Q\to P)$.

## Numbers

Put $T=1$, $U=0$, $F=-1$. Then every operation is arithmetic on $\{-1,0,1\}$:

| logic | number |
|---|---|
| $\neg x$ | $-x$ |
| $x\wedge y$ (AND) | $\min(x,y)$ |
| $x\vee y$ (OR) | $\max(x,y)$ |
| $x\to y$ | $\max(-x,\,y)$ |
| $x\leftrightarrow y$ | $x\times y$ (ordinary product) |

Min and max are written AND and OR, so that $+$ and $\times$ keep their meaning of sum and product (see [[Balanced Ternary]]). That the biconditional is the plain product is a curiosity worth noticing: agreement is $+1$, opposition is $-1$, and anything involving the unknown is $0$.

## What survives and what is lost

**Survives** (all checked over every case): commutative, associative, both distributive laws, absorption, idempotence, double negation, De Morgan's laws, contraposition $(P\to Q)=(\neg Q\to\neg P)$, and **modus ponens** (if $P$ and $P\to Q$ are both true, so is $Q$).

**Lost:**

- **Excluded middle** ([[First Principles of Thought]]): $P\vee\neg P$ is $T$, $U$, $T$ for $P=T,U,F$.
- **Non-contradiction as an equation:** $P\wedge\neg P$ is $F$, $U$, $F$. What survives is the *weaker* statement that $P$ and $\neg P$ are never both true.
- **Tautologies altogether.** Give every variable the value $U$ and every operation returns $U$, so no formula is always true. Even $P\to P$ is $U$ when $P$ is $U$. This is the price of Kleene's choice; Łukasiewicz's three-valued logic makes $U\to U$ true and recovers $P\to P$, at the cost of a different implication (and then the biconditional is not the product). The vault uses Kleene.

The Boolean case sits inside: restrict to $\{T,F\}$, i.e. $\{1,-1\}$, and every table above is the Boolean one. Boolean algebra is the subsystem where nothing is unknown.

**Whether it is the same as intuitionistic logic:** no. Both give up excluded middle, but K3 has no tautologies at all and no implication that proves $P\to P$. The relation to the constructive schools in [[Schools Compared]] needs care before it is stated.

## Where it appears

- **Computing:** a signal that is floating or uninitialised; SQL's `NULL` follows Kleene's tables (from memory). A failure to tell "false" from "not yet computed" is a familiar cause of bugs.
- **Science and ordinary reasoning:** conjectures not yet proved, claims not yet tested.
- **Hardware:** [[Balanced Ternary]] describes the Setun, whose three-state elements are the physical counterpart of the three values.

## Open points

- The booklet teaches this in a classical Christian curriculum (traditional logic → Boolean → K3 → balanced ternary); the vault records the mathematics only.

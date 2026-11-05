---
name: project-rational-rotation
description: Rational Rotation page (2026-10-22): discrete exact tick sine/cosine from an LLM conversation Murphy pasted; what was verified, what is open
metadata:
  type: project
---

Page: `Trigonometry/Rational Rotation`. Construction: step (a,b)=((N²-1)/(N²+1), 2N/(N²+1)) applied repeatedly to (1,0); isolated points; horizontal stretch is display only. Source was an LLM conversation Murphy pasted; all numbers rechecked in exact fractions.

Findings of mine, **all adopted by Murphy 2026-11-04** (no longer marked [AI]): the step is twice the wedge of slope 1/N; denominator exactly (N²+1)^k so digits grow linearly; no period except N=1 (Niven), no zero for N≥2; half-step is a level-5 Length; step is the [1/1] Padé of exp, so the paste's claim that Padé does not preserve the circle is true only off the diagonal; Euler leaves the circle while the rational step (trapezoid rule) keeps it.

Open: almost-periods; cost to a target wedge; Fourier basis on ticks; comparison with Wildberger's rational trigonometry (Future Directions item 9). The Taylor-vs-exact cost comparison at k=100 was not done (Taylor needs an angle input). **Names settled 2026-11-04: dsin_N, dcos_N are the vault's names (Agenda A.6 closed).**

See [[feedback-no-sine-cosine]], [[project-function-hierarchy]].

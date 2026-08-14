# 基点穿折越理论泛化：如何选择最快收敛的基点，构造能充分生成人类数域空间的基点，并让每个空间都不处于无穷远

**Basepoint-Teleport (Worn-Zhe-Yue) Generalization: Choosing the Fastest-Converging Basepoint, Designing a Basepoint that Generates the Human Number-Field Space, and Removing Every Space from Infinity**

*2026-08-12 · Internal research paper · 方法基础: 基点穿折越 (Worn-Zhe-Yue)*

---

## Abstract

We address the basepoint-selection problem in the basepoint-teleport (穿折越, Worn-Zhe-Yue) framework: given a structure (here: the human number-field space), how do we choose the basepoint that (a) converges fastest to the basepoint-invariant structure, (b) is capable of *generating* the full number-field chain ℕ → ℤ → ℚ → ℝ → ℂ, and (c) removes every axis so that no space remains at infinity? We show that the number-field chain is a *convergence hierarchy*: each level incorporates the projection artifacts of the previous level as explicit structure (ℕ cannot see subtraction → ℤ adds inverses; ℤ cannot see division → ℚ adds fractions; ℚ cannot see limits → ℝ completes/compactifies, drawing ∞ into a finite circle; ℝ cannot see √-1 → ℂ takes the algebraic closure). The basepoint 1 (the unit) generates the entire chain through the operations of successor (ℕ), inverse (ℤ), reciprocal (ℚ), limit (ℝ), and rotation by 90° (ℂ, i = √-1). We define *axis peeling*: the removal of representation (projection-direction) dependence, so that every structure is expressed in basepoint-invariant coordinates. We give the fastest-convergence criterion: a basepoint converges fastest when it exposes the generating structure directly (coordinates are integers, or structure constants, or symmetry-adapted), so that the projection artifacts (irrationals, transcendentals, asymmetries) are recognized as such rather than carried as pseudo-properties. Finally, *no space remains at infinity*: each level is compactified (ℝ → S¹, ℂ → S²), so every space is finite and closed under its defining operation.

## 1. Introduction

### 1.1 Motivation

The number line is a pointed, directed structure: basepoint 0, unit 1, direction positive/negative. The basepoint-teleport (穿折越) framework treats a basepoint as a genuine degree of freedom: choosing a basepoint stabilizes relative structure while drifting the codomain. This paper asks the *design* question: which basepoint should we choose, and how should we design a basepoint that can generate the whole human number system?

Three sub-questions structure the paper:
1. **Fastest convergence**: which basepoint makes the structure converge fastest to its basepoint-invariant (axis-free) form?
2. **Generativity**: which basepoint can generate ℕ → ℤ → ℚ → ℝ → ℂ, the full number-field space?
3. **No infinity**: how do we peel away the axes so that no space sits at infinity?

### 1.2 Contributions

1. **The number-field chain as a convergence hierarchy** (Observation 2.1): each level ℕ → ℤ → ℚ → ℝ → ℂ incorporates the previous level's projection artifacts as explicit structure.
2. **The basepoint 1 generates the full chain** (Proposition 3.1): through successor (ℕ), inverse (ℤ), reciprocal (ℚ), limit (ℝ), rotation 90° (ℂ). The unit is the universal generator; i is the y-axis choice that closes the algebra.
3. **Axis peeling** (Definition 4.1): removing projection-direction dependence; a structure's axis-free form is its basepoint-invariant (D-space) form.
4. **Fastest-convergence criterion** (Principle 4.2): choose the basepoint exposing the generating structure directly, so projection artifacts are recognized rather than carried.
5. **Compactification removes infinity** (Observation 5.1): every level is compactified (ℝ → S¹, ℂ → S²); "not at infinity" means drawing ∞ into the finite structure.

### 1.3 Honest boundary

The individual facts are classical (KNOWN): the number-field tower, one-point compactification, algebraic closure. The contribution is the *unified basepoint-teleport design account*: the number system as a convergence hierarchy under basepoint choice, the unit as universal generator, the fastest-convergence criterion, and axis peeling. This unified account is original to this framework (NO_PRIOR_RESULT_FOUND in the searched sources).

## 2. The number-field chain as a convergence hierarchy

### 2.1 The levels and their blind spots

Each number system ℕ, ℤ, ℚ, ℝ, ℂ has a *blind spot*: an operation that is not closed within it. The next level is precisely the incorporation of that operation.

**Observation 2.1** (the convergence hierarchy). The chain ℕ → ℤ → ℚ → ℝ → ℂ is a hierarchy in which each level incorporates the previous level's blind spot as explicit structure:

| Level | Blind spot (projection artifact) | Incorporated by next level |
|---|---|---|
| ℕ | cannot see subtraction | ℤ adds additive inverses |
| ℤ | cannot see division | ℚ adds multiplicative inverses (fractions) |
| ℚ | cannot see limits | ℝ completes (Cauchy limits), draws ∞ into S¹ |
| ℝ | cannot see √-1 | ℂ takes algebraic closure, draws ∞ into S² |

**Observation 2.2** (projection reading). The blind spots are *projection artifacts* of the lower representation: "subtraction doesn't close in ℕ" is the artifact of the ℕ-axis (no negative direction); "division doesn't close in ℤ" is the artifact of the ℤ-axis (no reciprocal); "limits don't close in ℚ" is the artifact of the ℚ-axis (no completion); "√-1 doesn't exist in ℝ" is the artifact of the ℝ-axis (no perpendicular direction). Each level peels away one axis artifact and becomes more closed, more basepoint-independent.

## 3. Designing the generating basepoint

### 3.1 The unit 1 as universal generator

**Proposition 3.1** (the unit generates the full chain). Starting from the basepoint 1 and the unit element, the full number-field chain is generated by successive operations:

- **ℕ**: successor (add 1 repeatedly) — 1, 2, 3, ...
- **ℤ**: inverse (subtract 1, negate) — 0, -1, -2, ...
- **ℚ**: reciprocal (1/n) — 1/2, 1/3, ...
- **ℝ**: limit (Cauchy completion, Dedekind) — √2 as the limit of 1, 1.4, 1.41, 1.414, ...
- **ℂ**: rotation by 90° (i = √-1, i² = -1) — the algebraic closure

*The unit 1 is the universal basepoint: every number in every field is generated from it by the above operations.*

### 3.2 The 90° axis as the algebraic-closure basepoint

**Observation 3.2** (i is a y-axis choice). The imaginary unit i is the unit vector of the y-axis (90° rotation). Choosing the y-axis is choosing whether the system is algebraically closed: without the 90° direction (the y-axis), ℝ cannot see √-1; with it, ℂ closes.

**Observation 3.3** (y-axis = basepoint for closure). The y-axis is a basepoint in the C007 sense: it determines the codomain (whether the field is closed under √-1), while the underlying algebraic structure is basepoint-independent. Choosing the y-axis is choosing which projection of the number system to observe.

### 3.3 What a basepoint must carry to generate the number space

**Design principle 3.4** (a generating basepoint). To generate the full human number-field space, a basepoint must carry:
1. **A unit** (the 1, the seed of successor and of every multiplication);
2. **An inverse operation** (yielding negatives and reciprocals);
3. **A completion/limit** (yielding reals, drawing ∞ into finite form);
4. **A perpendicular direction** (yielding √-1, closing the algebra).

The basepoint 1 with the operations of successor/inverse/reciprocal/limit/rotation satisfies all four. This is the design of a basepoint that *sufficiently constructs the human number space*.

## 4. Choosing the fastest-converging basepoint

### 4.1 Convergence defined

**Definition 4.1** (axis peeling). *Axis peeling* is the removal of representation (projection-direction) dependence: expressing a structure in coordinates that depend only on the basepoint-invariant structure (the D-space of C007), not on the choice of axis direction.

**Definition 4.2** (convergence). A structure *converges* when axis peeling reaches a fixed point: the coordinates no longer change when the axis (projection direction) is further varied — i.e., the codomain equals the basepoint-invariant structure, with no remaining projection artifacts.

### 4.2 The fastest-convergence criterion

**Principle 4.3** (fastest convergence). A basepoint converges fastest when it *exposes the generating structure directly*: the coordinates are the integers (for axes), or the structure constants (for circles), or symmetry-adapted (for groups). In such coordinates, projection artifacts (irrationals, transcendentals, asymmetries) are recognized *as* artifacts rather than carried as pseudo-properties.

- **θ-axis**: choose the axis itself as the x'-axis ⟹ coordinates are integers; the "irrational" n·cos θ is recognized as a projection (fastest convergence: one rotation).
- **Real line**: choose the circle (S¹) ⟹ π, e are structure constants; their transcendence is recognized as a line-representation artifact (fastest convergence: one compactification).
- **NS**: choose O(n) over SO(n) ⟹ time reversal T is a group element; the "irreversibility" is recognized as an SO(n)-representation artifact (fastest convergence: one symmetry enlargement).

**Observation 4.4** (slow convergence). Choosing a basepoint that does not expose the generating structure carries artifacts as pseudo-properties: the real line "observes" √2 and π as if they were intrinsic irrationals; a basepoint adapted to the generating structure reveals them as projections. The former converges slowly (each artifact must be peeled one at a time); the latter converges in one step.

### 4.3 The convergence hierarchy as peeling order

**Observation 4.5** (the number chain is the peeling sequence). The chain ℕ → ℤ → ℚ → ℝ → ℂ is exactly the axis-peeling sequence: each step removes one axis artifact (subtraction, division, limits, √-1), and the fastest-converging basepoint is the one at the top of the chain (ℂ, the algebraic closure, where all blind spots are incorporated and the space is closed). But the *design* of that basepoint requires passing through all levels — the convergence is fastest precisely when every level's artifact has been incorporated.

## 5. No space remains at infinity

### 5.1 Compactification draws ∞ into the finite structure

**Observation 5.1** (every space is compactified). Each level of the number chain is compactified, so no space sits at infinity:

- **ℝ**: one-point compactification ≃ S¹ (the real line closes into a circle; +∞ and -∞ meet at one point).
- **ℂ**: one-point compactification ≃ S² (the Riemann sphere; ∞ is the north pole).
- **The circle axis (S¹)**: on it, the structure constants π and e are finite, intrinsic, and no number is "at infinity."

**Definition 5.2** (not at infinity). A space is *not at infinity* when it is compactified: every divergent point is drawn into the finite structure as a boundary or a meeting point, so no coordinate can escape the space.

**Observation 5.3** (peeling removes infinity). Axis peeling and compactification coincide: peeling the line's axis artifacts (irrationality of √2, transcendence of π, asymmetry of time) is the same as drawing those artifacts into explicit finite structure (projections along an axis, constants of a circle, group elements). A fully peeled space is finite, closed, and contains no ∞.

## 6. The design recipe: a basepoint for the human number space

**Design 6.1** (the recipe). To construct a basepoint that generates the full human number space and makes every space converge (finite, not at infinity):

1. **Start from the unit 1** — the seed of successor, inverse, reciprocal, limit, rotation.
2. **Add the inverse operation** (peel subtraction/division): ℤ, ℚ.
3. **Complete** (peel limits): ℝ; compactify to S¹ (draw ∞ in).
4. **Take the 90° direction** (peel √-1): ℂ; compactify to S² (draw ∞ in).
5. **Choose the fastest-converging coordinates** at each level: the generating-structure-adapted axis (integers along the θ-axis; structure constants on the circle; symmetry-adapted for groups).

The resulting space: ℂ, algebraically closed, compact (Riemann sphere), with every number expressible as a finite combination of basepoint-1 operations — no irrationality, no transcendence, no asymmetry, no infinity, except as recognized projection artifacts of a chosen (non-adapted) axis.

## 7. Conclusion

The human number-field space ℕ → ℤ → ℚ → ℝ → ℂ is a convergence hierarchy under basepoint choice: each level incorporates the previous level's projection artifacts (subtraction, division, limits, √-1) as explicit structure. The basepoint 1, together with the operations of successor/inverse/reciprocal/limit/90°-rotation, generates the full chain. The fastest-converging basepoint is the one that exposes the generating structure directly, so that irrationals, transcendentals, and asymmetries are recognized as projection artifacts rather than carried as pseudo-properties. Axis peeling removes representation dependence; compactification (ℝ → S¹, ℂ → S²) draws ∞ into the finite structure. The fully peeled space is finite, closed, and contains no point at infinity — a basepoint-invariant, axis-free, convergent design of the number system.

## Appendix A: identity checks (恒等式先验)

- 2·cos 45° = √2 (verified: 1.414214); 2·cos 30° = √3 (verified: 1.732051)
- e^(i·2πk) = 1 for all k ∈ ℤ (verified); e^(i·(2k+1)π) = -1 for all k ∈ ℤ (verified)
- Euler: e^(iπ) = -1 (verified: -1.000000 + 0.000000i)
- i² = -1 (algebraic closure of ℝ); Cauchy sequence 1, 1.4, 1.41, 1.414, ... → √2
- Compactifications: ℝ ∪ {∞} ≃ S¹; ℂ ∪ {∞} ≃ S² (classical, KNOWN)

## Appendix B: honesty boundaries

- All individual mathematical facts are classical (KNOWN): number-field tower, algebraic closure, one-point compactification, Euler's formula/identity.
- The *unified basepoint-teleport design account* — the number system as a convergence hierarchy, the unit as universal generator, the fastest-convergence criterion, axis peeling, and "no space at infinity" via compactification — is the paper's contribution (NO_PRIOR_RESULT_FOUND in the searched sources).
- This is a conceptual framework paper, not a theorem-proving paper (Lean formalization of the axis-peeling construction is future work).

# Model: Stone's theorem and uniqueness of the solution of the Schrödinger equation

Status: built 2026-11-18. Numbers and statements verified 2026-11-18 (sections 6 and 7). Updated 2026-11-19: time-dependent Hamiltonians (Q19 to Q21, regimes H7a to H7c, selection 4b); then the role of continuity in t in the uniqueness class (Q22, Q23, selection 4c). Both verified the same day. Status codes: V = found in a cited source; V (weak) = weak source (encyclopedia, lecture summary), analogy, or uncertain attribution; C = calculated or derived, method given; U = not verified.

Scope: the abstract initial-value problem iħ·dψ/dt = Hψ, ψ(0) = ψ₀, in a complex Hilbert space 𝓗, with a time-independent Hamiltonian H; since 2026-11-19 also what changes when H depends on t. The question is what Stone's theorem says, which part of "existence and uniqueness" it supplies, and which part comes from elsewhere. This is a model of a mathematical structure, so "processes" are mechanisms in the mathematics (as in `klein-gordon-probability-density.md`). Units with ħ = 1 are used below unless ħ is written.

## 1. Objects

**Hilbert space 𝓗**
- Complex, with inner product ⟨·,·⟩ (antilinear in the first slot here) and norm ‖ψ‖. Example: L²(ℝ³).

**Hamiltonian H**
- A linear operator defined on a dense subspace D(H) ⊂ 𝓗 (its domain). For unbounded H the domain is part of the definition of the operator.
- Symmetric: ⟨φ, Hψ⟩ = ⟨Hφ, ψ⟩ for φ, ψ in D(H). Consequence: ⟨ψ, Hψ⟩ is real.
- Self-adjoint: H = H*, which means symmetric and D(H*) = D(H). Equivalent criterion: H symmetric and Ran(H ± i) = 𝓗.
- Resolvent at ∓i (added 2026-11-19): for self-adjoint H, (H ± i)⁻¹ is defined on 𝓗, has norm ≤ 1, and maps 𝓗 onto D(H); the adjoint of (H + i)⁻¹ is (H − i)⁻¹.
- Essentially self-adjoint: the closure of H is self-adjoint; then H has one self-adjoint extension.
- Deficiency indices (n₊, n₋): dimensions of the solution spaces of H*χ = +iχ and H*χ = −iχ. Self-adjoint extensions exist when n₊ = n₋; there is one (the closure) when both are 0, and a family of them when n₊ = n₋ ≥ 1.

**One-parameter unitary group U(t), t ∈ ℝ**
- Each U(t) unitary; U(0) = 1; U(t + s) = U(t)U(s).
- Strongly continuous: t ↦ U(t)ψ is continuous in norm for each ψ.
- Generator: the operator A with D(A) = {ψ : the limit of (U(t)ψ − ψ)/t as t → 0 exists in norm} and iAψ equal to that limit (sign convention varies; with U(t) = e^{−itH}, the limit is −iHψ).

**Time-dependent Hamiltonian H(t) and unitary propagator U(t, s)** (added 2026-11-19)
- H(t): a family of self-adjoint operators, one for each t, each with its own domain D(H(t)).
- Unitary propagator: a two-parameter family of unitary operators, jointly strongly continuous in t and s, with U(t, t) = 1 and U(t, r)U(r, s) = U(t, s). It replaces the one-parameter group; for H(t) = H it reduces to U(t, s) = e^{−i(t−s)H}.

**Kinds of solution of i·dψ/dt = Hψ, ψ(0) = ψ₀**
- Strong (classical) solution: ψ(t) ∈ D(H) for each t, t ↦ ψ(t) differentiable in norm, equation holds in 𝓗.
- Generalized (mild) solution: ψ(t) = U(t)ψ₀ for ψ₀ outside D(H); continuous, in general not differentiable.
- Weak solution: t ↦ ψ(t) continuous and d/dt⟨φ, ψ(t)⟩ = −i⟨H*φ, ψ(t)⟩ for each φ in D(H*).
- Pairing-differentiable solution (added 2026-11-19; name used in this model only): ψ(t) ∈ 𝓗 for each t, and for each φ in D(H) the function t ↦ ⟨φ, ψ(t)⟩ is differentiable at every t of the interval, the initial time included, with derivative −i⟨Hφ, ψ(t)⟩. No continuity of t ↦ ψ(t) in norm is assumed.
- Solution of the partial differential equation outside 𝓗 (not square-integrable): a different problem.

**Worked example of a symmetric, non-self-adjoint H**
- H_min = −d²/dx² on L²(0, ∞) with domain the smooth functions vanishing near 0 and near ∞ (units ħ = 2m = 1).
- H_min*χ = ±iχ has one square-integrable solution each: χ±(x) = exp[−(1 ∓ i)x/√2], ‖χ±‖² = 1/√2. Deficiency indices (1, 1).
- Self-adjoint extensions: boundary conditions ψ′(0) = γψ(0), γ real, plus ψ(0) = 0 (Robin family; Dirichlet and Neumann are members).

## 2. Processes (mechanisms)

| # | Mechanism | Condition | Note |
|---|---|---|---|
| Q1 | Stone's theorem, direction "group → generator" | U(t) strongly continuous one-parameter unitary group | there is one self-adjoint H with U(t) = e^{−itH}; H is recovered as i × derivative of U(t) at t = 0 on the domain where that derivative exists |
| Q2 | Stone's theorem, direction "generator → group" | H self-adjoint | e^{−itH}, defined by the spectral theorem (functional calculus), is a strongly continuous one-parameter unitary group. The map H ↔ U(t) is one-to-one |
| Q3 | Existence of a strong solution | H self-adjoint, ψ₀ ∈ D(H) | ψ(t) = U(t)ψ₀ stays in D(H), is differentiable in norm, and satisfies i·dψ/dt = Hψ. Argument: (U(h) − 1)/h commutes with U(t), and U(t) is bounded |
| Q4 | Uniqueness of the strong solution by norm conservation | H symmetric (self-adjointness not needed for this step); also H(t) symmetric for each t | if φ(t) is a strong solution with φ(0) = 0, then d‖φ‖²/dt = 2·Im⟨φ, Hφ⟩ = 0, so ‖φ(t)‖ = 0. Applied to the difference of two solutions with the same ψ₀ |
| Q5 | Uniqueness by "undoing the evolution" | H self-adjoint (uses the group from Q2) | for a strong solution ψ(s), d/ds[U(t − s)ψ(s)] = U(t − s)(iH − iH)ψ(s) = 0, so ψ(t) = U(t)ψ₀ |
| Q6 | Uniqueness of the group with a given generator | two strongly continuous unitary groups with the same generator H | they agree on D(H) by Q4, and D(H) is dense, so they agree on 𝓗 by continuity. This is the "one-to-one" part of Q2 |
| Q7 | Extension to ψ₀ outside D(H) | H self-adjoint | U(t)ψ₀ is defined and continuous, norm-preserving, the limit of strong solutions; it is not differentiable in norm (if it were at one time, the group property would put ψ₀ in D(H)) |
| Q8 | Uniqueness of weak solutions | closed densely defined A on a Banach space; equation u′ = Au | unique weak solutions for every initial datum exist if and only if A generates a strongly continuous semigroup (Ball 1977). For A = −iH with H self-adjoint, Q2 supplies the (semi)group |
| Q9 | Failure for symmetric, non-self-adjoint H: several dynamics | n₊ = n₋ ≥ 1 | each self-adjoint extension (boundary condition) has its own group U_γ(t); the differential expression alone does not fix the evolution |
| Q10 | Failure for symmetric, non-self-adjoint H: weak solutions not unique, norm not conserved | n₊ ≥ 1 | ψ(t) = e^{t}·χ₊ solves i·∂ψ/∂t = −∂²ψ/∂x² with ‖ψ(t)‖² = e^{2t}/√2; see the note under the table |
| Q11 | Failure for symmetric H with n₊ ≠ n₋: no unitary dynamics | unequal deficiency indices | no self-adjoint extension, so by Q1 no unitary group has an extension of H as generator. Example usually quoted: −i·d/dx on the half-line (not looked up) |
| Q12 | Proving self-adjointness of concrete Hamiltonians | e.g. Kato–Rellich: A self-adjoint, B symmetric and A-bounded with relative bound < 1 ⟹ A + B self-adjoint on D(A) | covers −Δ + V with V = (L² part) + (bounded part) in three dimensions, which includes the Coulomb potential; atomic and molecular Hamiltonians (Kato 1951) |
| Q13 | Time-dependent Hamiltonian H(t): general situation | H depends on t | U(t, s) is a two-parameter propagator, not a one-parameter group; Stone's theorem does not apply and extra regularity conditions on H(t) are needed (Kato, Yosida, Simon, Kisyński, Yajima). Unlike the time-independent case there is no single general criterion. Details in Q19 to Q21 |
| Q14 | Bounded H | ‖H‖ < ∞ | U(t) = Σ(−itH)ⁿ/n! converges in norm; U(t) is then norm-continuous. Existence and uniqueness also follow from the ordinary theory of linear differential equations (the last sentence is U) |
| Q15 | Relaxed continuity hypothesis in Q1 | separable 𝓗 | weak measurability of t ↦ U(t) already implies strong continuity (von Neumann 1932) |
| Q16 | Solutions outside the Hilbert space | function not square-integrable, e.g. fast growth at infinity | Hilbert-space uniqueness does not cover them. For the heat equation Tychonoff built a non-zero solution with zero initial data; whether the same construction is written down for the free Schrödinger equation was not found |
| Q17 | Nonlinear Schrödinger equations | equation not linear in ψ | outside Stone's theorem; non-uniqueness of weak solutions is known in some settings |
| Q18 | Physical reading | — | unitarity = conservation of total probability ‖ψ‖²; reversibility = group property with negative t |
| Q19 | Bounded H(t): Dyson series | H(t) bounded and self-adjoint for each t, t ↦ H(t) strongly continuous | for each ψ₀ in 𝓗 there is one strongly differentiable solution; it defines a unitary propagator given by the Dyson (time-ordered) series (Reed–Simon Theorem X.69). Bounded weak solutions of the propagator equation coincide with it |
| Q20 | Unbounded H(t) with a common domain | each H(t) self-adjoint on the same dense domain D; C(t, s) = (H(t) − H(s))·(H(s) − ξ)⁻¹ and its limit C(t, s)/(t − s) as t → s uniformly bounded and strongly continuous (Yosida Theorem XIV.3.1; Reed–Simon Theorem X.70) | a unique unitary propagator exists; U(t, s)ψ₀ is a strong solution for ψ₀ in D. Existence is the hard part; uniqueness and unitarity follow from it by the norm argument Q4. Example: H(t) = Σ fᵢ(t)·Hᵢ self-adjoint on a fixed D with fᵢ continuously differentiable. For −½Δ + V(t, x), Yajima (1987) gives integrability conditions on V under which a unique unitary propagator exists |
| Q21 | Time-dependent domain | D(H(t)) changes with t (moving boundary conditions, time-dependent singular terms) | even when the expression of H(t) is continuously differentiable in t, well-posedness is not ensured by the standard methods; approaches of Simon and Kisyński use a constant form domain instead of a constant operator domain. A common domain is not necessary either: there are self-adjoint A(t) with smooth resolvents and a well-posed problem on a dense set whose domains intersect in {0} (Proc. AMS 1977) |
| Q22 | Uniqueness without assuming continuity in t | H self-adjoint; ψ a pairing-differentiable solution (section 1) on an interval containing t₀ | ψ(t) = U(t − t₀)ψ(t₀). Norm continuity is then a consequence, not a hypothesis. Proof in the note under the table |
| Q23 | Failure when ψ(t₀) is not tied to nearby times | equation imposed for t ≠ t₀ only (or for almost every t), with no continuity at t₀ | for g ≠ f in 𝓗, the function equal to U(t − t₀)g for t ≠ t₀ and to f at t = t₀ is in 𝓗 at each t, satisfies the equation at each t ≠ t₀ and has ψ(t₀) = f. So the initial value does not select a solution |

Note on Q10: ψ(t) = e^{t}χ₊ satisfies the weak form for H_min (test functions φ in D(H_min)), with ψ(0) = χ₊. It does not coincide with U_γ(t)χ₊ for a self-adjoint extension, because that one has constant norm. So the weak problem for H_min with initial datum χ₊ has more than one solution. χ₊ is not in the domain of the closure of H_min (which requires ψ(0) = ψ′(0) = 0), so Q4 is not contradicted.

Note on Q22 (proof, C). Let g(t) be the difference of two pairing-differentiable solutions with the same value at t₀, so g(t₀) = 0. Put B = (H + i)⁻¹ and u(t) = B*g(t) = (H − i)⁻¹g(t), so u(t) ∈ D(H) and g = (H − i)u.
1. For each η in 𝓗, Bη ∈ D(H) and ⟨η, u(t)⟩ = ⟨Bη, g(t)⟩, which is differentiable by hypothesis. With H·Bη = η − iBη the derivative is −i⟨η, g⟩ + ⟨η, u⟩ = ⟨η, −iHu(t)⟩. So u is weakly differentiable against every vector of 𝓗, with weak derivative −iHu(t).
2. At fixed t, for a sequence hₙ → 0 the quotients (u(t + hₙ) − u(t))/hₙ converge weakly, so they are bounded in norm (uniform boundedness principle). Hence ‖u(t + hₙ) − u(t)‖ ≤ C·|hₙ| → 0: u is continuous in norm.
3. For χ in D(H) and fixed T put F(t) = ⟨U(t − T)χ, u(t)⟩. Split F(t + h) − F(t) into ⟨(U(h) − 1)U(t − T)χ, u(t + h)⟩ + ⟨U(t − T)χ, u(t + h) − u(t)⟩. Divided by h, the first term tends to ⟨−iHUχ, u(t)⟩ = +i⟨Uχ, Hu(t)⟩ (Q3 and step 2), the second to ⟨Uχ, −iHu(t)⟩ = −i⟨Uχ, Hu(t)⟩ (step 1). So F′ = 0 at every t, F is constant, and F(t₀) = 0.
4. F(T) = ⟨χ, u(T)⟩ = 0 for each χ in the dense set D(H), so u(T) = 0 and g(T) = (H − i)u(T) = 0.
The step that replaces the continuity hypothesis is 1 to 2: smoothing with the bounded operator (H − i)⁻¹ turns pairings against D(H) into pairings against all of 𝓗, where uniform boundedness applies. Without the smoothing, uniform boundedness gives a bound for g(t) in the dual of D(H) only, not in 𝓗.

**Picture: what Stone's theorem is and is not doing.** Uniqueness of a strong solution is an energy-type estimate (Q4) and needs symmetry only. Stone's theorem (with the spectral theorem) supplies: existence (Q2, Q3); the statement that the object "the dynamics generated by H" is single-valued (Q6); the converse, that a unitary strongly continuous dynamics has one self-adjoint generator (Q1); and the criterion separating good from bad Hamiltonians (self-adjoint against merely symmetric, Q9 to Q11).

**Picture for H(t) (added 2026-11-19).** The uniqueness step (Q4) does not care whether H depends on t. What time-independence buys is existence with one clean criterion (self-adjointness, through Stone). With H(t), self-adjointness of each H(t) is kept as a hypothesis but is no longer known to be sufficient by itself; regularity in t (Q19, Q20) is added to get existence, and with existence the propagator is unique.

**Picture for the role of continuity in t (added 2026-11-19).** "ψ(·, t) ∈ L² at each t" by itself says nothing about how the values at different times are related; the link between times comes from the sense in which the equation holds. If the equation holds at every t including t₀ in the pairing sense, that already forces continuity (Q22). If the equation is not imposed at t₀, or on a set of times of measure zero that includes t₀, the initial value is disconnected from the rest (Q23).

## 3. Regimes

| # | Regime | Boundary | Existence | Uniqueness |
|---|---|---|---|---|
| H1 | H bounded and symmetric (then self-adjoint) | ‖H‖ < ∞ | yes, for each ψ₀, power series (Q14) | yes |
| H2 | H unbounded, self-adjoint, ψ₀ ∈ D(H) | H = H* | strong solution U(t)ψ₀ (Q3) | yes among strong solutions (Q4, Q5) |
| H3 | H self-adjoint, ψ₀ ∉ D(H) | — | no strong solution; generalized/weak solution U(t)ψ₀ (Q7) | yes among weak solutions (Q8); yes also among pairing-differentiable solutions, with no continuity assumed (Q22) |
| H3a | H self-adjoint; equation imposed only for t ≠ t₀ or for almost every t, no continuity in t | — | yes | no (Q23) |
| H3b | H self-adjoint; integral or almost-everywhere formulations with measurability in t and some link to t₀ | — | — | not worked in this model (U) |
| H4 | H essentially self-adjoint | closure is self-adjoint | as H2/H3 for the closure | yes; one group |
| H5 | H symmetric, n₊ = n₋ ≥ 1 | — | a strong solution for the closure of H may fail to exist for some ψ₀ in its domain (U); one group per extension | strong solutions of the closure: unique (Q4). Dynamics: not unique (Q9). Weak solutions: not unique (Q10) |
| H6 | H symmetric, n₊ ≠ n₋ | — | no unitary group (Q11) | strong solutions unique where they exist (Q4) |
| H7a | H(t) bounded, self-adjoint, strongly continuous in t | — | yes, for each ψ₀, Dyson series (Q19) | yes |
| H7b | H(t) unbounded, self-adjoint, common domain, regular in t | conditions of Q20 | unitary propagator; strong solution for ψ₀ in D | propagator unique; strong solutions unique (Q4) |
| H7c | H(t) self-adjoint for each t, but domain varying or no regularity in t | outside Q19, Q20 | not ensured; case-by-case theorems (Q21) | strong solutions unique where they exist (Q4); uniqueness of weak solutions not covered by this model (U) |
| H8 | Not in 𝓗, or nonlinear | — | outside the model | not guaranteed (Q16, Q17) |

## 4. Selection

### 4a. "How does it follow from Stone's theorem that the solution of the Schrödinger equation is unique?"

Conditions: time-independent self-adjoint H, solution sought in 𝓗 (regimes H2, H3).

**Kept:** Q2 and Q3 (existence, from Stone plus the spectral theorem); Q4 (uniqueness of strong solutions; this step does not use Stone); Q5 (the version of the uniqueness argument that does use the group); Q6 (uniqueness of the group, which is the uniqueness statement inside Stone's theorem); Q7, Q8 (initial data outside D(H)); Q9, Q10 (what goes wrong without self-adjointness, which shows what Stone's hypothesis buys).

**Mentioned briefly:** Q1 (converse), Q12, Q13.

**Left out, with reason:**
- Q14: special case of H2 with D(H) = 𝓗.
- Q15: concerns the hypothesis of Q1, not uniqueness of solutions.
- Q16, Q17: outside the Hilbert-space, linear setting of the question.
- Q11: no dynamics to be unique or not.

### 4b. "Is time-independence of H necessary for uniqueness?" (added 2026-11-19)

Conditions: H(t) self-adjoint for each t, solution sought in 𝓗 (regimes H7a to H7c).

**Kept:** Q4 (uniqueness of strong solutions holds for symmetric H(t)); Q13 (Stone does not apply); Q19, Q20 (sufficient conditions giving existence and a unique propagator); Q21 (where it can fail).

**Left out, with reason:**
- Q8: Ball's theorem is stated for a time-independent generator; it is not applied to H(t) here.
- Q16, Q17: outside the Hilbert-space, linear setting.

### 4c. "Does uniqueness fail if continuity in t is dropped and only 'L² at each t' is kept?" (added 2026-11-19)

Conditions: time-independent self-adjoint H, ψ(t) ∈ 𝓗 for each t (regimes H3, H3a, H3b).

**Kept:** Q22 (uniqueness survives when the equation holds in the pairing sense at every t), Q23 (it fails when the equation is not imposed at t₀), Q3 and Q2 (used in the proof of Q22).

**Left out, with reason:**
- Q8: Ball's theorem assumes continuity in its definition of weak solution, so it does not answer the question.
- Q9, Q10: H is self-adjoint here.
- H3b: not worked; stated as unverified in answers.

## 5. Known limits of this model

- For H(t), sufficient conditions are listed (Q19, Q20); no necessary-and-sufficient criterion is given, and no explicit counterexample of non-existence is worked.
- Uniqueness of weak solutions for unbounded H(t) is not covered.
- Q22 requires the pairings to be differentiable at every t. Versions with "almost every t", absolutely continuous pairings, or distributional solutions in (x, t) are not worked.
- Q22 rests on a proof written for this model; no published statement of it in this form was found.
- Hilbert-space (square-integrable) solutions; statements about the differential equation in larger function classes are not covered.
- Proofs are sketched; the spectral theorem and the proof of Stone's theorem itself are taken from the sources.
- Rigged Hilbert spaces, non-self-adjoint (dissipative) generators and contraction semigroups (Hille–Yosida, Lumer–Phillips) are not modelled.
- One worked example (half-line); no three-dimensional singular potential is worked.

## 6. Verification of numbers

This model contains few numbers.

Sources:
- [S1] Wikipedia, "Stone's theorem on one-parameter unitary groups": https://en.wikipedia.org/wiki/Stone%27s_theorem_on_one-parameter_unitary_groups
- [S2] J. M. Ball, Proc. Amer. Math. Soc. 63, 370–373 (1977): https://www.ams.org/proc/1977-063-02/S0002-9939-1977-0442748-6/
- [S3] B. Simon, "Tosio Kato's work on non-relativistic quantum mechanics: an outline", arXiv:1710.06999

| Quantity | Value | Status | Source or formula |
|---|---|---|---|
| Dates: Stone; von Neumann | 1930, 1932; 1932 | V (weak: encyclopedia) | S1 |
| Date: Ball's weak-solution theorem | 1977 | V | S2 |
| Date: Kato's self-adjointness theorem | published 1951 (proved by 1944) | V | S3 |
| Half-line example: solutions of −χ″ = ±iχ in L²(0, ∞) | χ± = exp[−(1 ∓ i)x/√2]; one each | C | sympy: residual 0; Re k = −1/√2 < 0; the other root grows |
| ‖χ±‖² | 1/√2 = 0.7071 | C | sympy: ∫₀^∞ e^{−√2·x}dx |
| Deficiency indices of H_min on the half-line | (1, 1) | C | count of the solutions above; agrees with the Robin one-parameter family in T5 |
| ψ = e^{t}χ₊ | i∂ψ/∂t + ∂²ψ/∂x² = 0; ‖ψ‖² = e^{2t}/√2 | C | sympy |
| Norm of (H ± i)⁻¹ | ≤ 1 | C | ‖(H ± i)ψ‖² = ‖Hψ‖² + ‖ψ‖² ≥ ‖ψ‖² for symmetric H |

## 7. Verification of statements

Sources for statements:
- [S1], [S2], [S3] as in section 6.
- [T1] P. Jorgensen, F. Tian, "Noncommutative analysis, multivariable spectral theory for operators in Hilbert space…", arXiv:1408.1164, section 2.A
- [T2] M. Penz, "The density-potential mapping in quantum dynamics", arXiv:1610.05552, Lemma 3.10
- [T3] K. Yajima, RIMS Kôkyûroku 755: https://www.kurims.kyoto-u.ac.jp/~kyodo/kokyuroku/contents/pdf/0755-07.pdf ; and arXiv:1508.05724 (introduction)
- [T4] arXiv:2112.11063 (introduction: Simon's and Kisyński's approaches to time-dependent Hamiltonians)
- [T5] Bonneau, Faraut, Valent, "Self-adjoint extensions of operators and the teaching of quantum mechanics", arXiv:quant-ph/0103153 (Am. J. Phys.); arXiv:1303.2343 (Robin boundary conditions)
- [T6] M. Loss, Georgia Tech lecture notes, "The Kato–Rellich theorem": https://loss.math.gatech.edu/17SPRINGTEA/7334/NOTES/section7katorellich.pdf ; arXiv:2003.06599
- [T7] EPFL lecture summary: https://graphsearch.epfl.ch/en/lecture/0_p228dm86
- [T8] J. Banasiak, lecture notes on semigroups (Łódź): https://im0.p.lodz.pl/~jbanasiak/Studia%20Doktoranckie/Pages%20from%20LNAFA9.pdf
- [T9] arXiv:2009.12793 (cites Tychonoff 1935 for the heat equation); arXiv:math/0503366 (non-uniqueness of weak solutions of the nonlinear Schrödinger equation)
- [T10] Yajima, Comm. Math. Phys. 110 (1987), abstract: https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-110/issue-3/Existence-of-solutions-for-Schr%C3%B6dinger-evolution-equations/cmp/1104159313.pdf ; Pacific J. Math. paper on invariant domains: https://www.projecteuclid.org/download/pdf_1/euclid.pjm/1102364184
- [T11] Bouclet, Germinet, Klein, Schenker, "Linear response theory for magnetic Schrödinger operators in disordered media", arXiv:math-ph/0408028, section 2.3 (Theorem 2.7 and its proof)
- [T12] Nachtergaele, Sims, Young, arXiv:1810.02428, section 2.2; Nachtergaele, Sims et al., arXiv:1410.8174 (bounded H(t), Dyson series)
- [T13] arXiv:1910.04135, Theorems 5.2 and 5.3 (H(t) = Σ fᵢ(t)Hᵢ on a fixed domain)
- [T14] arXiv:1501.02826, section 3 (definition of unitary propagator; time-dependent boundary conditions)
- [T15] Uniform boundedness and weak convergence: MIT 18.102 lecture 13 (mirror copy): https://mitocw.ups.edu.ec/courses/mathematics/18-102-introduction-to-functional-analysis-spring-2009/lecture-notes/MIT18_102s09_lec13.pdf ; arXiv:1901.03640 ; Wikipedia "Weak convergence (Hilbert space)": https://en.wikipedia.org/wiki/Weak_convergence_(Hilbert_space)
- [T16] M. V. Markin, arXiv:1803.10038 (weak solutions of y′ = Ay defined through pairings with D(A*))
- [T17] "On the absence of necessary conditions for linear evolution operators", Proc. Amer. Math. Soc. 64 (1977), abstract: https://www.ams.org/proc/1977-064-01/S0002-9939-1977-0500284-2/
- [T18] Where the uniqueness proofs are written out (looked up 2026-11-19): G. Teschl, "Mathematical Methods in Quantum Mechanics", 2nd ed., AMS GSM 157 (2014), §5.1, Lemma 5.2, p. 146 (author's online edition: https://www.mat.univie.ac.at/~gerald/ftp/book-schroe/schroe2.pdf); C. Remling, functional analysis lecture notes, ch. 13 "Stone's theorem and quantum dynamics", proof of Theorem 13.1, pp. 162–163: https://math.ou.edu/~cremling/teaching/lecturenotes/fa-new/ln13.pdf ; B. Driver, P. Tong, arXiv:1511.02447, Theorem 5.1; arXiv:2102.10189, appendix D.2 (cites Pazy, Theorem 4.1.3, for uniqueness in the abstract Cauchy problem); arXiv:2512.01966 and arXiv:2301.07344 (cite Engel–Nagel, Prop. II.6.2)

| Item | Statement | Status | Source |
|---|---|---|---|
| Objects | self-adjoint ⟺ symmetric and Ran(H ± i) = 𝓗 | V | T6 |
| Objects | (H ± i)⁻¹ defined on 𝓗 with range D(H); adjoint of (H + i)⁻¹ is (H − i)⁻¹ | C | Ran(H ± i) = 𝓗 (V, T6) plus the norm identity in section 6; the adjoint relation is the textbook rule (A⁻¹)* = (A*)⁻¹, not looked up (U for that rule) |
| Objects | deficiency indices and von Neumann's extension theorem; a symmetric differential operator can have many self-adjoint extensions, fixed by boundary conditions | V | T5 |
| Objects | n₊ ≠ n₋ ⟹ no self-adjoint extension | U | part of von Neumann's theorem; not seen in the excerpts read |
| Objects | generator = derivative of U(t) at t = 0, domain = vectors where the norm limit exists | V | S1 |
| Objects | definition of weak solution; classical solutions = strongly differentiable weak solutions (closed A) | V | S2, and a paper citing it (emis.univie.ac.at/journals/HOA/IJMMS/Volume32_9/813143.pdf); T16 uses the same pairing form |
| Objects | definition of unitary propagator (two-parameter, strongly continuous, composition law); reduces to e^{−i(t−s)H} for constant H | V | T14, T11, T10 |
| Q1 | each strongly continuous unitary group has one self-adjoint generator | V | S1, T1 |
| Q2 | self-adjoint H gives a strongly continuous unitary group via the spectral theorem; the correspondence is one-to-one | V | S1, T1 |
| Q3 | U(t)ψ₀ is a strong solution for ψ₀ ∈ D(H) | V, C | T10 (time-independent case: propagator is the one-parameter group, differentiable on the domain); domain invariance by the commutation argument |
| Q4 | a strong solution is unique; proof by taking the difference and showing its norm stays 0 | V | T2; T18 (Remling uses the same computation for the difference of two groups; Driver–Tong Theorem 5.1 states norm conservation and "at most one solution" for a time-dependent problem) |
| Q4 | the same result in the semigroup textbooks (Pazy Theorem 4.1.3; Engel–Nagel Prop. II.6.2) | V (weak: known through papers citing them; the books were not opened, and their proofs are for general semigroups, not the norm argument) | T18 |
| Q4 | the step needs symmetry only, not self-adjointness | C | the proof uses ⟨φ, Hφ⟩ real and nothing else about H |
| Q5 | d/ds[U(t − s)ψ(s)] = 0 | V, C | T18: Teschl Lemma 5.2 ("U(t)ψ₀ is the only solution") is proved by differentiating U(−t)ψ(t); product rule; needs ψ(s) ∈ D(H) and Q3 |
| Q6 | same generator ⟹ same group | V, C | one-to-one in S1, T1; density argument in T2 ("uniqueness on a dense set suffices because the evolution operator is bounded") |
| Q7 | U(t)ψ₀ for ψ₀ ∉ D(H) is continuous, in general not differentiable, not a classical solution | V (weak: stated for general semigroups) | T8; C for "not differentiable at one time ⟹ contradiction" via the group property |
| Q8 | unique weak solutions for every initial datum ⟺ A generates a strongly continuous semigroup | V | S2 |
| Q8 | −iH with H self-adjoint is such a generator | C | restriction of the unitary group of Q2 to t ≥ 0 |
| Q9 | different self-adjoint extensions describe different physics (spectra, dynamics) | V | T5 |
| Q10 | e^{t}χ₊ is a weak solution for H_min with growing norm | C | section 6; pairing with φ in D(H_min) and integrating by parts leaves no boundary term because φ vanishes near 0 |
| Q10 | hence weak solutions for H_min are not unique | C | compare with U_γ(t)χ₊ of constant norm; consistent with Q8 (−iH_min closure is not a generator of a group) |
| Q11 | −i·d/dx on the half-line has unequal deficiency indices | U | recalled; not looked up |
| Q12 | Kato–Rellich statement; Coulomb potential satisfies it; Kato 1951 for atomic and molecular Hamiltonians | V | T6, S3 |
| Q13 | for time-independent H existence of a unique dynamics is equivalent to self-adjointness via Stone; for H(t) further conditions are required | V | T3, T4 |
| Q13 | no general criterion comparable to Stone's theorem exists for H(t) | V | T14 ("unlike the time-independent case, there is no general…"), T4 |
| Q14 | U(t) norm-continuous ⟺ generator bounded | V (weak: encyclopedia) | S1 |
| Q14 | power series and ordinary ODE theory for bounded H | U | textbook, not looked up |
| Q15 | weak measurability suffices in a separable space (von Neumann 1932) | V (weak: encyclopedia) | S1 |
| Q16 | Tychonoff's non-uniqueness example for the heat equation | V (weak: cited in passing) | T9 |
| Q16 | analogous non-square-integrable null solutions for the free Schrödinger equation | U | not found |
| Q17 | non-uniqueness of weak solutions occurs for a nonlinear Schrödinger equation | V (weak: title and section heading only) | T9 |
| Q18 | unitarity = conservation of total probability | U | textbook, not looked up |
| Q19 | bounded, strongly continuous H(t): one strongly differentiable solution for each ψ₀; unitary propagator; Dyson series; Reed–Simon X.69 | V | T12 |
| Q19 | bounded weak solutions of the propagator equation coincide with it | V | T12 (arXiv:1410.8174) |
| Q19 | exact hypotheses of the theorem (self-adjoint, strongly continuous, bounded) | V (weak) | T12: the hypothesis list was cut in the excerpt read; reconstructed from the surrounding text |
| Q20 | hypotheses: common domain, C(t, s) and its limit uniformly bounded and strongly continuous; conclusion: unique unitary propagator (Yosida XIV.3.1, Reed–Simon X.70) | V | T11; T13 notes Reed–Simon state it for Banach spaces |
| Q20 | uniqueness and unitarity follow from existence plus norm conservation | V | T11 (proof of Theorem 2.7) |
| Q20 | H(t) = Σ fᵢ(t)Hᵢ on fixed D, fᵢ ∈ C¹ gives a strongly differentiable unitary propagator | V (weak) | T13: a third hypothesis of the theorem was cut in the excerpt read |
| Q20 | Yajima: conditions on V(t, x) giving a unique unitary propagator for −½Δ + V | V | T10 (abstract); the conditions themselves were not transcribed |
| Q21 | with a time-dependent domain, a continuously differentiable expression does not ensure well-posedness by standard methods; Simon and Kisyński use a constant form domain | V | T4 |
| Q21 | a common domain is not necessary: self-adjoint A(t) with smooth resolvents, unique solutions on a dense set, domains intersecting in {0} | V | T17 (abstract) |
| Q21 | an explicit H(t), self-adjoint for each t, for which no propagator exists | U | no counterexample found |
| Q22 | pairing-differentiable solutions are unique and equal U(t − t₀)ψ(t₀); norm continuity follows | C | proof in the note under the process table; uses Q2, Q3, the resolvent facts, and the uniform boundedness principle |
| Q22 | every weakly convergent sequence in a Hilbert space is bounded (uniform boundedness principle) | V | T15 |
| Q22 | a function on an interval with derivative 0 at every point is constant | U | mean value theorem, textbook, not looked up |
| Q22 | a published statement of Q22 in this form | U | not found; a 2024 note (arXiv:2406.02474) reports that suitably defined weak solutions of linear evolution problems gain time regularity, which is the same phenomenon in a different setting (analogy only) |
| Q23 | counterexample function satisfies the equation at t ≠ t₀ and has the prescribed value at t₀ | C | for t ≠ t₀ it coincides near t with U(t − t₀)g, a weak solution (Q7, Q8); at t₀ no condition is imposed |
| H3b | uniqueness for almost-everywhere or integral formulations | U | not worked |
| H7c | uniqueness of weak solutions for unbounded H(t) | U | not looked up |
| Picture | "the unitary group generated by a self-adjoint operator provides a unique solution to the Schrödinger equation" is taught together with Stone's theorem | V (weak: lecture summary) | T7 |
| Picture | division of labour: uniqueness of strong solutions from symmetry, existence and single-valued dynamics from self-adjointness | C | Q3, Q4, Q6, Q9, Q10 |
| Picture for H(t) | time-independence is used for existence through Stone, not for the uniqueness step | C | Q4 (V for H(t), T2 and T11) and Q13 |
| Picture for continuity | the link between times comes from the sense in which the equation holds | C | Q22, Q23 |
| H5 | a strong solution for the closure of a symmetric non-self-adjoint H can fail to exist | U | expected from semigroup theory (Hille–Yosida); not looked up |
| H7 | norm argument still gives uniqueness of strong solutions for symmetric H(t) | V | T2 (Lemma 3.10 is stated for the time-dependent problem), T11 |

Corrections:
- 2026-11-19: Q13 was a single line naming authors. Added Q19 (bounded H(t), Dyson series), Q20 (common domain plus regularity, Yosida/Reed–Simon), Q21 (time-dependent domain); regime H7 split into H7a to H7c; unitary propagator added to the objects; selection 4b added. Q10's table cell, which was cut off mid-sentence, now points to the note under the table. The limit "Time-independent H" in section 5 replaced by the two limits on H(t).
- 2026-11-19 (third update): added T18, textbook and lecture-note locations of the uniqueness proofs; Q5 raised from C to V, C. Reed–Simon vol. I (Theorem VIII.7) was not checked.
- 2026-11-19 (second update): the model treated norm continuity in t as part of the uniqueness class without saying whether it is needed. Added Q22 (it is not needed when the equation holds in the pairing sense at every t; proof), Q23 (uniqueness fails when the equation is not imposed at t₀), regimes H3a and H3b, the resolvent facts in the objects, selection 4c. Added to Q21 that a common domain is not necessary (T17), found while searching.

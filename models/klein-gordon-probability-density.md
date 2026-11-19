# Model: Klein-Gordon equation and its conserved density (why it cannot serve as a probability density)

Status: built 2026-11-13. Numbers and statements verified 2026-11-13 (sections 6 and 7). Status codes: V = found in a cited source; V (weak) = weak source, analogy, or uncertain attribution; C = calculated or derived, method given; U = not verified.

Scope: a complex scalar wave function φ(x, t) obeying the Klein-Gordon (KG) equation, read as the wave function of one relativistic spin-0 particle of mass m; free, or in a static electric potential. The question is which conserved density the equation supplies and what sign it can take. Worked example: charged pion. This is a model of a mathematical structure and its interpretation, so "processes" below are mechanisms in the equations, not events in time.

## 1. Objects

**Particle**
- Spin 0, mass m. Example: charged pion, m c² = 139.570 MeV; reduced Compton wavelength ħ/mc = 1.414 fm; 2mc² = 279.14 MeV.
- Relativistic energy-momentum relation E² = p²c² + m²c⁴. For each p it has two roots, E = ±E_p with E_p = √(p²c² + m²c⁴) ≥ mc².

**Klein-Gordon equation (free)**
- (1/c²)·∂²φ/∂t² − ∇²φ + (mc/ħ)²·φ = 0, obtained from the energy relation with E → iħ∂/∂t, p → −iħ∇.
- Second order in time: a solution is fixed by two independent functions at t = 0, φ and ∂φ/∂t.
- Plane-wave solutions exp[i(p·x ∓ E_p·t)/ħ]: "positive-frequency" (upper sign, energy +E_p) and "negative-frequency" (lower sign, energy −E_p).

**Schrödinger equation (for comparison)**
- iħ∂ψ/∂t = −(ħ²/2m)∇²ψ. First order in time: ψ at t = 0 fixes the solution.
- Conserved density ρ_S = |ψ|² ≥ 0, current j = (ħ/2mi)(ψ*∇ψ − ψ∇ψ*).

**KG conserved density and current**
- ρ = (iħ/2mc²)·(φ*·∂φ/∂t − φ·∂φ*/∂t)
- j = (ħ/2mi)·(φ*∇φ − φ∇φ*) (same form as Schrödinger's)
- ∂ρ/∂t + ∇·j = 0 for every solution. (ρ, j) form a four-vector.
- With a static potential energy V(x) (substitution iħ∂/∂t → iħ∂/∂t − V): ρ = (iħ/2mc²)(φ*∂φ/∂t − φ∂φ*/∂t) − (V/mc²)|φ|².

**Probability density (requirement)**
- A function that is ≥ 0 at every point and time and whose space integral is constant, so it can be normalized to 1.

## 2. Processes

| # | Mechanism | Condition | Size or note |
|---|---|---|---|
| K1 | Continuity equation from the KG equation: multiply the equation by φ*, subtract the complex conjugate | any solution | gives the ρ and j of section 1; the time derivative enters ρ because the equation has ∂²/∂t² |
| K2 | \|φ\|² is not conserved | solution containing both frequency signs (or, with several momenta, in general) | for a·e^{−iEt/ħ} + b·e^{+iEt/ħ} at one p, \|φ\|² oscillates at angular frequency 2E_p/ħ |
| K3 | Sign of ρ for a plane wave follows the sign of the energy | single plane wave | ρ = +(E_p/mc²)\|φ\|² for positive frequency, −(E_p/mc²)\|φ\|² for negative frequency |
| K4 | Free choice of initial data makes ρ(x, 0) of either sign | φ and ∂φ/∂t chosen independently at t = 0 | example: φ → φ* reverses the sign of ρ everywhere |
| K5 | Mixture of the two frequency signs at one momentum | a, b amplitudes | ρ = (E_p/mc²)(\|a\|² − \|b\|²), uniform in space and constant in time; negative when \|b\| > \|a\| |
| K6 | Interference between positive-frequency waves of different energy makes ρ locally negative | two (or more) positive-frequency components with E₁ ≠ E₂ and suitable amplitude ratio | for 1·(E₁) + r·(E₂): minimum of ρ ∝ (1 − r)(E₁ − E₂r), negative for E₁/E₂ < r < 1 (E₁ < E₂). Deepest minimum −(E₂ − E₁)²/(4E₂mc²) in units where the first wave alone has \|φ\|² = 1. Total ∫ρ stays positive |
| K7 | Non-relativistic limit | φ = ψ·e^{−imc²t/ħ}, with ψ varying slowly (energies above mc² much smaller than mc²) | ρ = \|ψ\|² + (iħ/2mc²)(ψ*∂ψ/∂t − ψ∂ψ*/∂t); second term of relative order (E − mc²)/mc² |
| K8 | Potential term in ρ | static potential energy V | stationary state of energy E: ρ = [(E − V)/mc²]·\|φ\|², negative where V > E |
| K9 | Klein zone: propagating solution inside a potential step higher than E + mc² | V₀ > E + mc² | transmitted wave has ρ < 0; reflection coefficient exceeds 1; read as pair creation at the step |
| K10 | Reinterpretation as charge density (Pauli and Weisskopf, 1934) | φ treated as a field and quantized | e·ρ is the net charge density of particles (charge +e) and antiparticles (charge −e); conserved total = e·(N₊ − N₋) |
| K11 | First-order two-component form (Feshbach-Villars) | algebraic rewriting of the KG equation | ρ = \|φ₁\|² − \|φ₂\|², a difference of two non-negative terms |
| K12 | Positive density from a different position operator (Newton-Wigner) | free particle, positive-frequency solutions only | \|ψ_NW\|² ≥ 0, but it is not the time component of a four-vector, is tied to one reference frame, and spreads faster than light |
| K13 | Dirac's route: first-order equation | spin ½ | density ψ†ψ ≥ 0; negative-energy solutions remain |
| K14 | Real (neutral) field | φ = φ* | ρ = 0 identically |

## 3. Regimes

| # | Regime | Boundary | What happens to ρ |
|---|---|---|---|
| G1 | Non-relativistic, positive frequency | momentum spread and mean momentum ≪ mc | ρ ≈ \|ψ\|² ≥ 0 up to corrections of order (E − mc²)/mc²; negative dips of K6 exist in principle but are of second order: −6 × 10⁻⁶ for p₂ = 0.1 mc |
| G2 | Relativistic, positive frequency only | momentum components differing by about mc or more; equivalently structure on the scale ħ/mc (1.4 fm for a pion) | ρ locally negative at the percent to tens-of-percent level: −0.030 for p₂ = mc, −0.37 for p₂ = 3mc (K6 units); ∫ρ > 0 |
| G3 | Both frequency signs present | allowed by the equation for arbitrary initial data | ρ of either sign; ∫ρ can be positive, zero or negative (K4, K5) |
| G4 | Potential above the energy | V > E | ρ < 0 in that region for a stationary state (K8) |
| G5 | Klein zone | V₀ > E + mc² (V₀ > 2mc² = 279 MeV for a pion at rest) | negative-ρ wave propagates; single-particle reading fails (K9) |
| G6 | Real field | φ = φ* | ρ ≡ 0 (K14) |
| G7 | Quantized field | — | ρ is a charge-density operator; probabilities come from the state vector and are ≥ 0 (K10) |

There is no regime of the free complex KG equation in which ρ is guaranteed ≥ 0 at every point for every solution: restricting to positive frequencies makes the total positive but K6 still allows local negative values.

## 4. Selection: "how does the Klein-Gordon equation lead to negative probabilities?"

Conditions: free particle, complex φ, single-particle reading.

**Kept:** K1 (which density is conserved), K2 (why |φ|² is not available), K3 to K5 (negative values with negative-frequency solutions), K6 (negative values without them), K7 (why the problem is invisible at low energy), K10 (resolution).

**Mentioned briefly:** K12, K13.

**Neglected, with reason:**
- K8, K9: no potential in the question (V = 0 makes the extra term zero).
- K11: a rewriting; adds no new sign behaviour beyond K3 to K5.
- K14: complex field assumed.

## 5. Known limits of this model

- Single-particle wave mechanics plus a statement of the field-theory reading; the quantized field is not constructed here.
- One space dimension in the worked examples; the sign arguments do not depend on dimension.
- Spin 0 only. Dirac's equation enters as a comparison.
- "Negative probability" is the traditional label. In the accepted theory no negative probability is predicted; the density that goes negative is a charge density.
- Interactions other than a static electric potential are left out.

## 6. Verification of numbers

Sources:
- [S1] Particle Data Group, π± mass: https://pdglive.lbl.gov/view/S008M

| Quantity | Value | Status | Source or formula |
|---|---|---|---|
| Charged pion mass | 139.57039 ± 0.00018 MeV | V | S1 |
| ħc | 197.327 MeV·fm | U | recalled (follows from exact SI constants); not looked up in this chat |
| Pion reduced Compton wavelength | 1.414 fm | C from a U constant | ħc / mc² |
| 2mc² for the pion | 279.14 MeV | C | 2 × S1 |
| Continuity equation | residual 0 | C | sympy: ∂ρ/∂t + ∂j/∂x = (iħ/2m)(φ*·KG[φ] − φ·KG[φ*]) |
| ρ for plane waves | ±E_p/mc² | C | sympy, direct substitution; agrees with T7, T12 |
| ρ for a·(+E) + b·(−E) | (E_p/mc²)(\|a\|² − \|b\|²) | C | sympy; cross terms cancel |
| \|φ\|² for the same mixture | oscillates at 2E_p/ħ | C | sympy time derivative non-zero |
| Minimum of ρ, two positive-frequency waves | (1 − r)(E₁ − E₂r)/mc² | C | ρ = [E₁ + E₂r² + (E₁ + E₂)r·cos(…)]/mc²; checked numerically on a grid |
| Deepest minimum | −(E₂ − E₁)²/(4E₂mc²) at r = (E₁ + E₂)/(2E₂) | C | minimizing over r |
| Example values (p₁ = 0; p₂ = 0.1, 1, 3 mc) | −6.2 × 10⁻⁶, −0.030, −0.37 | C | numpy |
| γ at v = 0.1c | 1.005 | C | 1/√(1 − 0.01) |

## 7. Verification of statements

Sources for statements:
- [T1] D. Gingrich, Univ. of Alberta PHYS 512 notes, "Conserved current and charge": https://sites.ualberta.ca/~gingrich/courses/phys512/node26.html ; "Klein paradox for spin-0 particles": https://sites.ualberta.ca/~gingrich/courses/phys512/node35.html
- [T2] C. Elster, Ohio Univ. lecture notes, ch. 3 "The Klein-Gordon equation": https://people.ohio.edu/elster/lectures/advqm_3.pdf
- [T3] arXiv:1602.03744, section 3
- [T4] arXiv:2207.14646, section B
- [T5] arXiv:1105.3660, section 2
- [T6] F. Dyson, 1951 Lectures on Advanced Quantum Mechanics, arXiv:quant-ph/0608140
- [T7] arXiv:1504.01164, appendix B
- [T8] Esposito, "Majorana and the Pauli-Weisskopf scalar electrodynamics", arXiv:0710.5914
- [T9] R. Sutherland, "Interpretation of the Klein-Gordon probability density", arXiv:1509.07380; Found. Phys. (2025): https://link.springer.com/article/10.1007/s10701-025-00820-x
- [T10] arXiv:quant-ph/0111060 (localization of Dirac and KG particles)
- [T11] arXiv:1802.04266; arXiv:hep-th/0702162 (Newton-Wigner density)
- [T12] arXiv:hep-th/0206250, section 4; arXiv:1602.00190, section 3
- [T13] arXiv:2209.06093, introduction

| Item | Statement | Status | Source |
|---|---|---|---|
| Objects | KG equation follows from the relativistic energy relation; second order in time | V | T2, T5 |
| Objects | Schrödinger density \|ψ\|² is non-negative and conserved, so it can be a probability density | V | T7 |
| Objects | (ρ, j) is a four-vector | V (weak) | T2 writes it as a four-current; transformation law not checked |
| K1 | derivation by multiplying with φ* and subtracting; form of ρ and j | V, C | T1, T2; sympy check in section 6 |
| K1 | time derivative appears in ρ because the equation is second order in time | V | T1, T3 |
| K2 | ∫\|φ\|² is not conserved under KG evolution | V, C | T5; section 6 |
| K3 | sign of ρ follows the sign of the energy for plane waves | V, C | T7; section 6 |
| K4 | φ and ∂φ/∂t can be chosen independently, so ρ can have either sign | V | T1, T2, T3 |
| K4 | φ → φ* reverses ρ | C | ρ is antisymmetric under exchange of φ and φ* |
| K5 | mixture formula | C | section 6 |
| K6 | ρ can be negative with positive-frequency components only | V | T9, T10 |
| K6 | formula for the minimum and the condition E₁/E₂ < r < 1 | C | section 6 |
| K6 | ∫ρ stays positive for positive-frequency solutions | V (weak) | physics-forum summary in the search results ("integral over positive-frequency parts minus integral over negative-frequency ones"); C for the two-wave case (mean = (E₁ + E₂r²)/mc² > 0) |
| K7 | ansatz φ = ψ·e^{−imc²t/ħ} gives the non-relativistic limit | V | T2 |
| K7 | ρ → \|ψ\|² with corrections of order (E − mc²)/mc² | C | substitute the ansatz in ρ |
| K8 | potential adds −(V/mc²)\|φ\|² to ρ; stationary state has ρ ∝ (E − V) | V | T12 |
| K9 | Klein zone at V₀ > E + mc²; transmitted density negative; reflection above 1; pair-creation reading | V | T1, T12 |
| K10 | Pauli and Weisskopf (1934) reinterpreted ρ as charge density of a quantized field with particles of both charges | V | T6, T7, T8, T2 |
| K10 | conserved quantity is N₊ − N₋ | V (weak) | T8 describes number operators for the two charges; the difference formula itself not quoted in the excerpt read |
| K11 | Feshbach-Villars form with ρ = \|φ₁\|² − \|φ₂\|² | V | T12, arXiv:2012.02725 |
| K12 | Newton-Wigner density is non-negative but not Lorentz-covariant and propagates faster than light | V | T11; T10 notes ψ*ψ is not a four-vector component |
| K13 | Dirac equation: first order, positive density, negative energies remain | V | T1, T3, T7 |
| K13 | Dirac's equation was the historical response to the KG density problem | V | T13, T8 |
| K14 | real field gives ρ = 0 | C | the two terms of ρ cancel when φ = φ* |
| G1, G2 | sizes of the negative dips and the ħ/mc scale | C | section 6; T10 and arXiv:1107.4459 link negative-energy effects to the Compton wavelength |
| G3 | no regime with ρ ≥ 0 guaranteed pointwise | C | follows from K4 and K6 |
| G7 | in the field theory probabilities are non-negative | V (weak) | forum statement and the LLM-written "Pauli-Weisskopf theorem" page in the search results; standard, but no primary source read |
| Limits | "the KG equation is no worse than the Dirac equation" for a single-particle density | V | T1 |

Corrections: none yet (first version).

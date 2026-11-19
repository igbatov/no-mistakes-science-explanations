# Model: quarter-wave plate (linearly polarized light turned into circularly polarized light)

Status: built 2026-11-13. Numbers and statements verified 2026-11-13 (sections 6 and 7). Status codes: V = found in a cited source; V (weak) = weak source (vendor page, patent, encyclopedia mirror or talk page), analogy, or uncertain attribution; C = calculated or derived from V items, method given; U = not verified.

Scope: a monochromatic or narrow-band plane wave travelling along z at normal incidence through a flat plate of a uniaxial birefringent crystal whose optic axis lies in the plane of the plate. Worked example: crystalline quartz at 589.3 nm. Related models: `zeeman-effect.md` (σ components seen along the field are circularly polarized), `sodium-emission-spectrum.md`.

## 1. Objects

**Incoming light**
- Plane wave along +z, vacuum wavelength λ, linearly polarized: E oscillates along one fixed direction in the xy plane, amplitude E₀.
- Example: λ = 589.3 nm, period 1.966 fs.

**Wave plate**
- Slab of birefringent crystal, thickness d, faces perpendicular to z.
- Two perpendicular directions in the plane of the plate: fast axis (refractive index n_f, lower) and slow axis (n_s, higher). Light polarized along the fast axis has the higher phase velocity c/n_f.
- Quartz at 589.3 nm: ordinary index 1.5443, extraordinary index 1.5534, Δn = n_s − n_f = 0.0091. Quartz is positive uniaxial (extraordinary index higher), so the slow axis is the optic axis.
- Retardance Γ = 2π·Δn·d/λ (phase by which the slow component lags the fast one on exit).
- Quarter-wave plate: Γ = π/2 (or π/2 plus a whole number of 2π).
- True zero-order quartz quarter-wave plate at 589.3 nm: d = λ/(4Δn) = 16.2 µm. The fast component fits 42.43 wavelengths in it, the slow component 42.68; the difference is 0.25. Time lag of the slow component: 0.49 fs.
- Multiple-order plate: a single quartz plate about 0.5 mm thick (7.7 waves of retardance at 589.3 nm); thickness is adjusted so the retardance is a whole number plus ¼.
- Compound zero-order plate: two thick plates with crossed axes whose retardances differ by ¼ wave.
- Quartz transmits from about 0.2 to 2 µm.

**Angle θ**
- Angle between the input polarization direction and the fast axis.

**Coordinates used in answers**
- Right-handed x, y, z with z the propagation direction; fast axis along x, slow axis along y.

## 2. Processes

| # | Process | Condition | Size or rate |
|---|---|---|---|
| W1 | Decomposition: the input field is the sum of a component along the fast axis and one along the slow axis | any θ; linear medium | amplitudes E₀·cos θ and E₀·sin θ, in phase on entry |
| W2 | Different phase velocity for the two components (birefringence) | n_s ≠ n_f | c/1.5443 against c/1.5534 in quartz: 0.59% apart |
| W3 | Accumulation of phase lag of the slow component | grows in proportion to depth in the plate | Γ = 2π·Δn·d/λ; 90° per 16.2 µm of quartz at 589.3 nm |
| W4 | Recombination behind the plate: the two components, now out of phase, add to a field whose tip traces an ellipse | Γ not a multiple of π and θ not 0° or 90° | ellipse has minor/major axis ratio tan θ (for Γ = 90°, θ ≤ 45°) with axes along fast and slow; circle when θ = 45° and Γ = 90° |
| W5 | Shortening of the wavelength inside the plate; frequency unchanged | n > 1 | 381.6 nm (fast) and 379.4 nm (slow) inside quartz for 589.3 nm in vacuum |
| W6 | Reflection at the two surfaces | index step air–crystal | uncoated quartz: 4.58% (fast) and 4.70% (slow) per surface from the normal-incidence Fresnel formula; transmitted amplitudes of the two components differ by 0.13% |
| W7 | Multiple reflections inside the plate (etalon effect) changing the effective retardance | coherent light, uncoated or poorly coated plate | not estimated |
| W8 | Wavelength dependence of the retardance | λ different from the design wavelength | zero-order quartz plate made for 589.3 nm gives 97° at 546.1 nm and 80° at 656.3 nm |
| W9 | Temperature dependence of the retardance | thickness and indices change with temperature | vendor figures: about 0.0001 wave per °C (zero-order) and 0.0015 wave per °C (multiple-order) |
| W10 | Dependence on angle of incidence | beam not perpendicular to the plate, or divergent | strong for multiple-order and compound zero-order plates; small for true zero-order plates |
| W11 | Absorption | outside the transparency range | quartz: transparent 0.2 to 2 µm |
| W12 | Optical activity of quartz (rotation of the polarization plane) | strongest for propagation along the optic axis | not estimated for propagation perpendicular to the optic axis, which is the wave-plate geometry |
| W13 | Sideways separation of the two beams (double refraction, walk-off) | oblique incidence or optic axis tilted out of the plate | assumed absent at normal incidence with the optic axis in the plate |
| W14 | Loss of a fixed phase relation because of finite bandwidth | time lag between components comparable to the coherence time | lag 0.49 fs (zero-order) against a coherence time of order 0.6 ns for a Doppler-broadened sodium lamp line (1.7 GHz) |

**Picture: two-component description.** The field behind the plate, with x fast and y slow, is E_x = E₀·cos θ·cos(ωt − kz), E_y = E₀·sin θ·cos(ωt − kz − Γ). For θ = 45°, Γ = 90°: E_x = (E₀/√2)·cos(ωt − kz), E_y = (E₀/√2)·sin(ωt − kz). The length of E is then constant, E₀/√2, and its direction turns once per period.

**Handedness for this geometry (θ = +45°, measured from fast axis x toward slow axis y).** At a fixed plane the tip of E turns from +x toward +y. With x, y, z right-handed and z the propagation direction, this is counterclockwise for a viewer who faces the source, and clockwise for a viewer looking along the beam. Names: left-circular in the convention of classical optics (viewer faces the source); right-handed in the IEEE convention. At a fixed time the field vectors along z form a left-handed screw. For θ = −45° (or with fast and slow axes exchanged) each of these reverses.

## 3. Regimes

**By input angle θ (plate with Γ = 90°)**
- θ = 0° or 90°: one component only; output linear, same direction as input.
- θ = ±45°: equal components; output circular, opposite handedness for the two signs.
- Other θ: elliptical, axes along fast and slow, axis ratio tan θ (θ ≤ 45°).

**By retardance Γ (input at θ = 45°)**
- Γ = 0 or a multiple of 2π: output equals input.
- Γ = π/2: circular (quarter-wave plate).
- Γ = π: linear, turned by 90° (half-wave plate).
- Γ = 3π/2: circular, opposite handedness to Γ = π/2.
- Other values: elliptical with axes at ±45° to the plate axes; axis ratio tan(Γ/2) or its inverse, whichever is below 1.

**By plate order**
- True zero-order (tens of µm of quartz): least sensitive to wavelength, temperature and angle.
- Compound zero-order: like zero-order for wavelength and temperature, like multiple-order (or worse) for angle of incidence.
- Multiple-order (about 0.5 to 1 mm): most sensitive to all three.

**By coherence of the light**
- Lag much shorter than the coherence time: fixed output state (W14 negligible).
- Lag comparable to the coherence time (very thick plate or broadband light): output partly depolarized.

**By input polarization state**
- Linear: as above.
- Circular: a quarter-wave plate turns it into linear at ±45° to the plate axes (the reverse of the main case).
- Unpolarized: stays unpolarized (not looked up).

## 4. Selection: "how does a quarter-wave plate turn linearly polarized light into circularly polarized light?"

Conditions: monochromatic light at the design wavelength, normal incidence, θ = 45°, ideal plate.

**Kept:** W1, W2, W3, W4.

**Neglected, with reason:**
- W5: changes the wavelength inside the plate for both components but the output state depends on the difference only; that difference is W3.
- W6: lowers the transmitted power by about 9% for an uncoated plate (U: Fresnel formula not looked up); the 0.13% amplitude imbalance changes the axis ratio from 1 to 0.9987.
- W7: not estimated (U).
- W8, W9, W10: zero at the design wavelength, reference temperature and normal incidence by the stated conditions.
- W11: quartz is transparent at 589 nm (inside the 0.2 to 2 µm range).
- W12, W13: assumed absent in this geometry (U).
- W14: 0.49 fs lag against 0.6 ns coherence time, a ratio of about 8 × 10⁻⁷.

## 5. Known limits of this model

- Plane wave, normal incidence, uniform plate. Real beams have a spread of angles (W10).
- Classical field description; photon spin is not used.
- The 16.2 µm plate is an illustration: quartz plates this thin are fragile, and commercial "true zero-order" plates are often polymer films or thin crystal bonded to glass.
- Dispersion of Δn is taken from three tabulated wavelengths only.
- Other ways to make circular light (Fresnel rhomb, liquid-crystal retarders, circular dichroic polarizers) are outside this model.
- Biaxial crystals and plates with a tilted optic axis are not covered.

## 6. Verification of numbers

Sources:
- [S1] OptoSigma, optical crystals reference data (quartz and calcite index tables, transmission range; excerpted from Chronological Scientific Tables): https://jp.optosigma.com/en_jp/category__opt_d__opt_d02
- [S2] HyperPhysics, birefringent materials: https://hyperphysics.gsu.edu/hbase/phyopt/biref.html
- [S3] KLA/Filmetrics refractive index database, quartz: https://www.kla.com/ko/products/instruments/refractive-index-database/quartz
- [S4] Edmund Optics, "Understanding waveplates": https://www.edmundoptics.com/knowledge-center/application-notes/optics/understanding-waveplates/
- [S5] MKS/Newport, zero-order quartz wave plate 10RP04-46: https://np.s2.mks.com/p/10RP04-46
- [S6] US patent 6384916 (retardance of a quarter-wave plate at other wavelengths): https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/6384916
- Sodium Doppler width 1.7 GHz: `zeeman-effect.md`, section 6.

| Quantity | Value | Status | Source or formula |
|---|---|---|---|
| Quartz indices at 589.3 nm | n_o = 1.5443, n_e = 1.5534 | V | S1, S2; S3 gives 1.54425 and 1.55338 at 590 nm |
| Quartz indices at 546.1, 656.3 nm | 1.5462/1.5553; 1.5419/1.5509 | V | S1 |
| Δn at 589.3 nm | 0.0091 | C | n_e − n_o; S3 states "only 0.009" |
| Quartz transmission range | 0.2 to 2 µm | V (weak: vendor table) | S1 |
| Retardance formula | Γ = 2π·Δn·d/λ | V | T1, T2 |
| Zero-order quarter-wave thickness | 16.2 µm | C | λ/(4Δn) = 589.3 nm / 0.0364 |
| Wavelengths inside quartz | 381.6, 379.4 nm | C | λ/n; relation itself is U (W5) |
| Waves inside the plate | 42.43, 42.68; difference 0.25 | C | d·n/λ |
| Time lag; optical period | 0.49 fs; 1.966 fs | C | d·Δn/c; λ/c |
| Phase velocities differ by | 0.59% | C | (n_e − n_o)/n_o |
| Multiple-order plate | about 0.5 mm of quartz | V (weak: vendor) | S4; another vendor page (T6) says about 1 mm |
| Retardance of 0.5 mm quartz at 589.3 nm | 7.7 waves | C | Δn·d/λ |
| Reflection per surface | 4.58%, 4.70% | C from a U formula | ((n − 1)/(n + 1))², not looked up |
| Amplitude imbalance from W6 | 0.13%; axis ratio 0.9987 | C from a U formula | √(T_slow/T_fast), T = (1 − R)², single pass |
| Retardance off the design wavelength | 97° at 546.1 nm; 80° at 656.3 nm | C | 360°·Δn(λ)·d/λ with S1 indices; S6 gives the simpler form 90°·λ₀/λ |
| Temperature coefficients | 0.0001 and 0.0015 wave per °C | V (weak: vendor) | S5 |
| Coherence time of a 1.7 GHz wide line | about 0.6 ns | C, order of magnitude | 1/Δν |
| Lag / coherence time | about 8 × 10⁻⁷ | C | 0.49 fs / 0.6 ns |
| Axis ratio tan θ for Γ = 90° | 0.27 (15°), 0.58 (30°), 1 (45°) | C | ellipse with semi-axes E₀·cos θ and E₀·sin θ along the plate axes |
| Axis ratio for θ = 45°, retardance Γ | tan(Γ/2) or its inverse | C | from the Stokes parameter S₃/S₀ = sin Γ, ratio = tan(½·arcsin(sin Γ)) |

## 7. Verification of statements

Sources for statements:
- [T1] IEEE Technology Navigator, optical retarders: https://technav.ieee.org/topic/optical-retarders/
- [T2] US patent 8786759 (description of wave plates): https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/8786759
- [T3] RP Photonics encyclopedia, waveplates: https://rp-photonics.com/waveplates.html
- [T4] Wikipedia "Waveplate" (mirror copy): https://bafybeiemxf5abjwjbikoz4mc3a3dla6ual3jsgpdr4cjr3oz3evfyavhwq.ipfs.4everland.io/wiki/Waveplate.html
- [T5] US patent 8274631 (retardance other than odd quarter waves, or angle other than 45°, gives elliptical light): https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/8274631
- [T6] FindLight blog, wave plate orders and angle dependence: https://findlight.net/blog/774
- [T7] Hale & Day, "Stability of birefringent linear retarders (waveplates)", Appl. Opt. 27, 5146 (1988), abstract: https://opg.optica.org/abstract.cfm?URI=ao-27-24-5146
- [T8] Handedness conventions: arXiv:1901.04581 (IEEE definition quoted; IEEE-RCP = classical LCP; fixed-time screw sense); Ocean Optics Web Book: https://oceanopticsbook.info/view/light-and-radiometry/polarization-stokes-vectors ; Wikipedia "Circular polarization": https://www.wikipedia.org/wiki/LHCP
- [T9] RP Photonics spotlight, "Can monochromatic light be unpolarized?": https://www.rp-photonics.com/spotlight_2019_08_26.html
- [S1], [S4], [S5], [S6] as in section 6.

| Item | Statement | Status | Source |
|---|---|---|---|
| Objects | plate has perpendicular fast and slow axes, both perpendicular to the beam; phase velocity is higher for polarization along the fast axis | V | T3, T1 |
| Objects | quartz is positive uniaxial (extraordinary index higher) | V | S1, S2 (index values) |
| Objects | in a wave plate the optic axis lies in the plane of the plate | V (weak) | T4 describes ordinary and extraordinary axes for normal incidence; cut geometry not stated explicitly in the excerpts read |
| W1 | light entering the plate can be decomposed into two orthogonally polarized waves along the plate axes | V | T2 |
| W1 | amplitudes E₀·cos θ, E₀·sin θ | C | projection of a vector on two perpendicular axes |
| W2, W3 | components travel at c/n_o and c/n_e; phase difference 2π·Δn·d/λ builds up | V | T4, T1, T2 |
| W4 | θ = 45° with a quarter-wave plate gives circular polarization | V | T1, T2, T3, T4 |
| W4 | θ = 0° or 90° leaves linear light linear; angles in between give elliptical light | V | T4, T5 |
| W4 | axis ratio tan θ | C | section 6 |
| W5 | frequency unchanged, wavelength λ/n inside | U | textbook, not looked up |
| W6 | reflection at uncoated surfaces; plates are usually anti-reflection coated | V for coating being standard (S4, S5); U for the size | Fresnel formula not looked up |
| W7 | etalon effect alters retardance | U | not looked up |
| W8 | single-material plate is accurate at its design wavelength only, because Δn·d/λ varies with wavelength | V | T1, S6 |
| W8, W9, W10 | multiple-order plates are more sensitive to wavelength, temperature and angle than zero-order plates | V | S4, T6, T7 |
| W9 | causes: thickness and indices change with temperature | V (weak: vendor blog) | T6 |
| W10 | compound zero-order plate behaves like zero-order for temperature and wavelength but like multiple-order for angle of incidence | V | T7 |
| W11 | quartz transparent at 589 nm | V (weak) | S1 |
| W12 | optical activity negligible in the wave-plate geometry | U | not looked up |
| W13 | no walk-off at normal incidence with optic axis in the plate | U | not looked up |
| W14 | negligible for a lamp line and a zero-order plate | C | 0.49 fs against 0.6 ns |
| W14 | a thick plate with broadband light depolarizes | U | not looked up |
| Picture | circular light = two perpendicular linear components of equal amplitude, 90° out of phase | V | T4 |
| Picture | constant length E₀/√2, one turn per period | C | cos² + sin² = 1 |
| Handedness | two opposite conventions exist; IEEE right-handed = classical-optics left-circular | V | T8 |
| Handedness | classical optics: right-circular = clockwise for a viewer facing the source, field vectors on a right-handed helix | V | T8 (Ocean Optics; Handbook of Optics footnote quoted on a Wikipedia talk page) |
| Handedness | fast axis x, slow axis y, θ = +45° gives rotation from +x toward +y: left-circular (classical), right-handed (IEEE), left-handed screw in space | C | E_x ∝ cos(ωt − kz), E_y ∝ sin(ωt − kz), compared with the V definitions; T8 (arXiv) confirms that IEEE-right-handed light forms a left-handed screw at fixed time |
| Regimes by Γ | half-wave plate at 45° turns linear polarization by 90° | V | T3 |
| Regimes by Γ | 3π/2 gives the opposite handedness | C | sin Γ changes sign |
| Regimes by Γ | plates with (2n + 1)·λ/4 retardance act as quarter-wave plates | V | T5 |
| Regimes | quarter-wave plate turns circular light into linear | V | T1, T2 |
| Regimes | unpolarized light stays unpolarized | U | not looked up |
| Selection | W1 to W4 are sufficient for the ideal case | C | all other processes are zero by the stated conditions, shown small by a number, or marked U |
| Related | strictly monochromatic light has a fixed polarization state | V | T9 |

Corrections: none yet (first version).

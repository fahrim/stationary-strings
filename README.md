# Stationary Strings — Series Map and Audit Trail

> **Türkçe:** [README_TR.md](./README_TR.md)

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE)

**One repository, one series, one numbering.** This repository is the index
for the *Stationary Strings* line of work: ten published theorem papers
(I–X), four application/audit papers (XI–XIV), and the independent letters
(L1, …). It exists because the work is deliberately self-critical: every
claim carries an evidence class, every error found is written down, and the
resulting ledger is machine-checkable.

> **Status:** working index. Theorems I–X are published (Zenodo DOIs below).
> Papers XI–XIV and the letters are **unpublished preprints under review**;
> their repos are private and their DOIs are pending deposit.

---

## 1. The naming scheme (one root, two lanes)

There is a single root — **Stationary Strings** — and no other product name.
The old "Grand Proof" label was removed on 20 October 2026 because it
overclaimed: paper XI is explicitly *not* a proof but a method that scores
its own claims.

| Lane | Numbering | Repositories | State |
|---|---|---|---|
| **Theory** (theorems, model construction) | I … X | `stationary-strings-i` … `-x` | published, DOI'd — **untouched** |
| **Application & audit** (tests, ledger, forensics) | XI … XIV | `stationary-strings-xi` … `-xiv` | private preprints, DOI pending |
| **Letters** (single, self-contained, model-free) | L1, L2, … | `stationary-strings-l1`, … | private preprints, DOI pending |

Supporting repositories: `stationary-strings-v` (the solver + cross-check
suite, public), `stationary-strings-viz` (3-D illustration package, private,
**illustration, not evidence**), `stationary-strings-workspace` (this
workspace's tooling).

---

## 2. Full map

| # | Paper | Repository | DOI | Evidence class | State |
|---|---|---|---|---|---|
| I | Rebirth of Perfect Order in the Absence of Time and Entropy | `stationary-strings-i` | [10.5281/zenodo.23408221](https://doi.org/10.5281/zenodo.23408221) | model ansatz | published |
| II | Relativity, Phase Transition and the Cosmological Cycle of Information | `stationary-strings-ii` | [10.5281/zenodo.23408234](https://doi.org/10.5281/zenodo.23408234) | model ansatz | published |
| III | Two-Dimensional Duality of Matter, Vortex Singularity and Phase Separation | `stationary-strings-iii` | [10.5281/zenodo.23408237](https://doi.org/10.5281/zenodo.23408237) | model ansatz | published |
| IV | Cosmic Fission, Vortex Fuel and the Singularity-Free Information Core | `stationary-strings-iv` | [10.5281/zenodo.23408245](https://doi.org/10.5281/zenodo.23408245) | model ansatz | published |
| V | Arrest of the Navier–Stokes Vortex Singularity by Elastic String Tension | `stationary-strings-v` | [10.5281/zenodo.23408253](https://doi.org/10.5281/zenodo.23408253) | framework + solver | published |
| VI | Dirac–Majorana Chiral Peeling, the Meral Baryogenesis Constant, ALPHA / 511 keV Synthesis | `stationary-strings-vi` | [10.5281/zenodo.23409493](https://doi.org/10.5281/zenodo.23409493) | framework + synthesis | published |
| VII | Self-Consistent Vortex Saturation in ALPHA Antimatter Traps, Exact 511 keV Ore–Powell Spectrum | `stationary-strings-vii` | [10.5281/zenodo.23427566](https://doi.org/10.5281/zenodo.23427566) | framework + falsifiable | published |
| VIII | Falsifiable Predictions, 511 keV Spectral Band, Uncertainty Quantification | `stationary-strings-viii` | [10.5281/zenodo.23436862](https://doi.org/10.5281/zenodo.23436862) | falsification | published |
| IX | Super-Brillouin Regime, Abrikosov–Diocotron Vortex Crystallization, Chiral-Elastic Annihilation Shield | `stationary-strings-ix` | [10.5281/zenodo.23436864](https://doi.org/10.5281/zenodo.23436864) | framework + cross-check | published |
| X | Tokamak H-Mode and ELM Suppression, Runaway Avalanche Quench, 30-Decade Universal Scaling Law | `stationary-strings-x` | [10.5281/zenodo.23437159](https://doi.org/10.5281/zenodo.23437159) | framework + cross-check | published |
| **XI** | **The Framework, a Degrees-of-Freedom Ledger and a Forensic Audit** | `stationary-strings-xi` | — | **methods + self-assessment** | private preprint |
| XII | Dark-Matter-Free Galactic Dynamics, SPARC Rotation Curves, EHT Ring Evidence | `stationary-strings-xii` | — | application + cross-check | private preprint |
| XIII | Navier–Stokes Vortex Saturation → 4D SU(3) Yang–Mills Mass-Gap Isomorphism, Glueball Spectrum | `stationary-strings-xiii` | — | application + analytic bound | private preprint |
| XIV | Benchtop Viscoelastic Vortex PIV, Vela Glitch Observations, Na-22 Positronium | `stationary-strings-xiv` | — | application + protocol | private preprint |
| **L1** | **The Three-Photon Positronium Spectrum — correction to arXiv:2605.21289 Eq. (12) and a one-hour laboratory test** | `stationary-strings-l1` | — | **independent of the series** | private preprint |

Supporting: `stationary-strings-v` (solver + verification), `stationary-strings-viz`
(3-D illustration, **not evidence**), `stationary-strings-workspace` (tooling).

---

## 3. What the ledger actually says

Paper XI publishes a machine-readable **degrees-of-freedom ledger** over 17
published comparisons. Each row states the observable, the literature value,
the model value, the free parameters entering, whether those parameters were
*fitted* to that datum, and a fragility measure.

| Class | Count | Meaning |
|---|---|---|
| FIT | 2 | parameters fitted to that datum |
| FIT-like | 2 | parameters fitted elsewhere, transferred |
| TRANSFER | 10 | locked core transferred, no free parameter |
| GENUINE | 2 | prediction with no free parameter |
| STRUCTURAL | 1 | definitional / not a comparison |

Grouping correlated rows leaves **8 independent observable groups against 9
free degrees of freedom — an evidence ratio of 0.889.** The fragility map
shows the one weak point: a 1 % shift of the locked constant
`C_univ = 1.6260379365521303` moves the glueball mean by 27.8 %, so the
1.56 % mean deviation quoted in paper XIII is **not robust** and is
labelled as such.

Verification infrastructure: **38 automated tests + 7 independent
cross-check scripts = 94 checks**, none of which imports the solver (the
cross-checks re-derive the locked constants from scratch; the audit
re-derives `C_univ` to 5.6×10⁻¹³ and `Π_Meral = μ_s` to 5.6×10⁻¹⁷).

## 4. Errors found and corrected

The forensic audit in paper XI lists eight error classes found **inside this
own work** and corrected: a non-self-adjoint discretisation, transposed
labels between sources, literature bands that do not exist in the cited
source ("ghost parameters"), an `H_0` dependence, a tautological lower
bound, over-claimed statements, and more. Two concrete examples:

- A variational `u = √x ψ` discretisation in the Yang–Mills operator
  violated the variational upper bound (λ₀ = 5.9158 > 5.6468) and was
  withdrawn and replaced by a finite-volume formulation with an
  **analytic, grid-independent Temple–Kato enclosure**
  λ₀ ∈ [5.4806777821, 5.7674115648] (constant-α) / [5.3686426884, 5.6467530803]
  (optimised), which brackets the continuum value λ₀ = 5.6102039939.
- A literature band quoted for the PEO polymer solution was traced to
  **no source at all** (the cited PDF and its LaTeX source were searched
  line by line); the claim was withdrawn and replaced by a two-regime
  laminar/elastic-turbulence resistance bridge that covers 97.9 % of the
  measured flow-resistance increase.

## 5. Letter L1 — the one model-free claim

L1 is deliberately outside the framework: it is a correction to a published
equation in an unrelated astrophysics paper.

The three-photon positronium spectrum published as Eq. (12) of
arXiv:2605.21289 is the **log-free** 1949 Ore–Powell expression. It is
unnormalised (∫₁⁵¹¹ Ω dE = 2343.47 instead of 1) and diverges as E⁻² at low
energy, i.e. it predicts more low-energy photons than the annihilation can
produce. The corrected form carries the original ln(1−x) factors, is exactly
normalised (∫₀⁵¹¹ Ω dE = 1 to 5×10⁻¹³) and vanishes as Ω(x) ~ (5/3)x.

A **one-hour** measurement with a 5 µCi ²²Na source, a silica aerogel and a
small HPGe detector separates the two forms by **7.8×10⁵ standard
deviations** in the band ratio R = N[10,100]/N[350,490]; the published form
predicts 5671× more low-energy counts than the corrected one.

> The measurement is **proposed, not performed**. The evidence for the
> correction is a term-by-term source audit against the 1949 original; the
> laboratory run is the falsification test of that audit.

---

## 6. Reproducing

```bash
git clone https://github.com/fahrim/stationary-strings-v.git
cd stationary-strings-v
python -W ignore duran_sicimler_sim/solver_engine.py       # T1–T37
python -W ignore duran_sicimler_sim/mini_check_ix.py        # 15/15
python -W ignore duran_sicimler_sim/mini_check_x.py         # 15/15
python -W ignore duran_sicimler_sim/mini_check_viii.py      # 8/8
python -W ignore duran_sicimler_sim/mini_check_gp1.py       # 15/15  (SS-XII)
python -W ignore duran_sicimler_sim/mini_check_gp2.py       # 17/17  (SS-XIII)
python -W ignore duran_sicimler_sim/mini_check_gp3.py       # 15/15  (SS-XIV)
python -W ignore duran_sicimler_sim/mini_check_audit.py     # 9/9   (series-wide audit)
python -W ignore duran_sicimler_sim/ledger.py               # ledger + LaTeX table check
python -W ignore duran_sicimler_sim/na22_experiment.py      # L1 protocol numbers
```

The cross-check scripts deliberately **do not import** the solver; they
re-derive each locked constant independently and compare.

## 7. Citation

Cite the individual paper you use; the series index is not itself a
reference. `CITATION.cff` in each repository holds the machine-readable
record, and `paper/ledger.json` in `stationary-strings-xi` holds the
machine-readable ledger.

## 8. License

CC BY 4.0 — see `LICENSE`. **Content is not peer-reviewed except where a
Zenodo DOI is listed in §2.**

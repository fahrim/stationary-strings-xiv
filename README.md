# Grand Proof III — Publication Package (Grand Proof Series III)

> **Türkçe:** [README_TR.md](./README_TR.md)

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE)

**Grand Proof III: Benchtop Viscoelastic Vortex PIV Experiment, Vela Pulsar Glitch Observations, and Sodium-22 Positronium Laboratory Evidence**

Author: Fahri Meral · Date: October 19, 2026 · Version: v1 (Grand Proof III)

> **Status:** Unpublished preprint (v1). Not peer-reviewed. *Zenodo DOI pending deposit.*

## Contents

| File | Description |
|---|---|
| `paper/grand_proof_III_deneysel_kanit_protokolu.tex` | Main paper, Turkish (Tables 1–3, Figure 1 2×2) |
| `paper/grand_proof_III_experimental_proof_protocol_EN.tex` | English version |
| `figs/fig15_benchtop_piv_vortex_vela_glitch_and_na22_lab.pdf` | Tests T35–T37 figure (TR, 2×2) |
| `figs/fig15_benchtop_piv_vortex_vela_glitch_and_na22_lab.png` | Tests T35–T37 figure preview (TR) |
| `figs/fig15_benchtop_piv_vortex_vela_glitch_and_na22_lab_en.pdf` | Tests T35–T37 figure (EN, 2×2) |
| `figs/fig15_benchtop_piv_vortex_vela_glitch_and_na22_lab_en.png` | Tests T35–T37 figure preview (EN) |
| `CITATION.cff` | Citation record |
| `LICENSE` | CC BY 4.0 |

## Key findings

- **T35 (Theorem GP-III.1):** Burgers-vortex benchtop PIV predictions —
  PEO core broadening `5.14198 mm` (`C_univ`), peak velocity braking
  `0.23703 m/s` (`C_univ^-1`), funnel suppression `8.09603 mm`
  (ratio `0.31402536`). The comparison bands quoted in earlier drafts are a
  **ghost parameter** (git archaeology: they entered with this work, no
  literature provenance) and are not claimed; the comparison is instead made
  against the primary source (Groisman & Steinberg 2000), whose measured
  flow-resistance increase `σ/σ_lam = 12–19` is reproduced by the locked
  many-mode barrier factor `S_loss = 19.7511425` as the envelope
  `[12.146791, 19.751143]` (97.9 % coverage), while the single-mode
  laminar ansatz does not explain it.
- **T36 (Theorem GP-III.2):** Vela glitch with **source-verified** inputs
  (`ν = 11.194615396005 Hz`, `|ν̇| = 1.55615e-11 Hz/s`, `ΔI/I ≥ 0.014`):
  `Δν/ν = 2.07112467e-6`, matching the 2004 event (`2.08e-6`) to 0.43 %
  and the largest 2000 event (`3.0858e-6`) to 32.9 %; measured healing
  fraction `Q_2000 = 0.02198`; relaxation scales 1.2 min / 0.53 / 3.29 /
  19.07 days.
- **T37 (Theorem GP-III.3):** positronium `O_exact` band ratio
  `0.08413579`; the published (ln-free) form gives `159.37` and the
  `(2m_e-E)^2` substituted form `9.31` — one hour of HPGe counting
  refutes both at `2.4e6 σ`.

## Numerical reproduction

Tests T35–T37 are produced with the solver in the **Paper V repository**
([`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)):

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py     # T1–T37 (38/38 PASS)
python duran_sicimler_sim/mini_check_gp3.py    # independent cross-check (15/15 PASS)
```

The independent cross-check never imports the solver. Figure 1 is produced by
the `fig15` function in `duran_sicimler_sim/generate_figures.py`.

## Citation

```bibtex
@misc{meral2026grandproofiii,
  author = {Fahri Meral},
  title  = {Grand Proof III: Benchtop Viscoelastic Vortex PIV Experiment, Vela Pulsar Glitch Observations, and Sodium-22 Positronium Laboratory Evidence},
  year   = {2026},
  url    = {https://github.com/fahrim/grand-proof-iii}
}
```

See also `CITATION.cff`.

## Related work

- `stationary-strings-i` … `stationary-strings-x` — Theorems I–X (the parent series).
- `grand-proof-i` — Dark-matter-free galactic dynamics, SPARC, EHT rings.
- `grand-proof-ii` — Yang–Mills mass gap, glueball spectrum, quark confinement.

## License

CC BY 4.0 — see `LICENSE`. Content is not peer-reviewed.

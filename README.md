# Grand Proof III — Publication Package (Grand Proof Series III)

> **Türkçe:** [README_TR.md](./README_TR.md)

**Grand Proof III: Benchtop Viscoelastic Vortex PIV Experiment, Vela Pulsar Glitch Observations, and Sodium-22 Positronium Laboratory Evidence**

Author: Fahri Meral · Date: October 19, 2026 · Version: v1 (Grand Proof III)

> **Status:** Unpublished preprint (v1). Not peer-reviewed.

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

## Results (zero free parameters)

- PEO vortex: core 5.14198 mm (C = 1.62603794, band center), velocity 0.23703 m/s,
  funnel 8.09603 mm (ratio 0.31402536, band center).
- Vela glitch 2.38190025e-6 vs (2.25 ± 0.35)e-6 (5.86%, 0.38σ);
  Q_fast 0.05910575, Q_total 0.13569214, both in [0.05, 0.18].
- Na-22 band ratio 0.08413579; false forms 9.31 / 159.37 refuted at 2.4e6σ.

## Numerical reproduction

Tests T35–T37 are produced with the solver in the **Paper V repository**
([`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)):

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py   # T1–T37 (38/38 PASS)
python duran_sicimler_sim/mini_check_gp3.py  # independent cross-check (12/12 PASS)
```

The independent cross-check never imports the solver.
Figure 1 is produced by the `fig15` function in `generate_figures.py`.

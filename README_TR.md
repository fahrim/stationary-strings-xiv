# Stationary Strings XIV — Yayın Paketi

> **English:** [README.md](./README.md)

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE)

**Stationary Strings XIV: İki Önerilen Masaütstü Testi (Viskoelastik Girdap PIV ve Sodyum-22 Pozitronyum) ve Vela Pulsar Glitch Gözlemleri**

> **All versions (concept DOI):** [10.5281/zenodo.23517484](https://doi.org/10.5281/zenodo.23517484)  
> **Previous version (v1):** [10.5281/zenodo.23517485](https://doi.org/10.5281/zenodo.23517485)

Yazar: Fahri Meral · Tarih: 19 Ekim 2026 · Sürüm: v1 (Stationary Strings XIV)

> **Durum:** Yayımlanmamış ön-baskı (v1). Hakem denetiminden geçmemiştir. *[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.23519746-blue.svg)](https://doi.org/10.5281/zenodo.23519746)*

## İçerik

| Dosya | Açıklama |
|---|---|
| `paper/stationary_strings_XIV_deneysel_kanit_protokolu.tex` | Ana makale, Türkçe (Tablo 1–3, Şekil 1 2×2) |
| `paper/stationary_strings_XIV_experimental_proof_protocol_EN.tex` | İngilizce sürüm |
| `figs/fig15_benchtop_piv_vortex_vela_glitch_and_na22_lab.pdf` | T35–T37 şekli (TR, 2×2) |
| `figs/fig15_benchtop_piv_vortex_vela_glitch_and_na22_lab.png` | T35–T37 şekil önizlemesi (TR) |
| `figs/fig15_benchtop_piv_vortex_vela_glitch_and_na22_lab_en.pdf` | T35–T37 şekli (EN, 2×2) |
| `figs/fig15_benchtop_piv_vortex_vela_glitch_and_na22_lab_en.png` | T35–T37 şekil önizlemesi (EN) |
| `CITATION.cff` | Atıf kaydı |
| `LICENSE` | CC BY 4.0 |

## Ana bulgular

- **T35 (Teorem XIV.1):** Burgers girdabı masaüstü PIV öngörüleri —
  PEO çekirdek genişlemesi `5,14198 mm` (`C_univ`), tepe hız frenlemesi
  `0,23703 m/s` (`C_univ^-1`), huni bastırması `8,09603 mm` (oran
  `0,31402536`). Önceki taslaklarda geçen karşılaştırma bantları bir
  **hayalet parametredir** (git arkeolojisi: bu çalışmayla girdi, literatür
  izi yok) ve iddia edilmez; karşılaştırma birincil kaynağa
  (Groisman & Steinberg 2000) yapılır: ölçülen akış direnci artışı
  `σ/σ_lam = 12–19`, kilitli çok-modlu bariyer çarpanı
  `S_loss = 19,7511425` ile zarf `[12,146791, 19,751143]` (%97,9 kapsama)
  olarak açılırken tek-modlu laminer ansatz açıklamaz.
- **T36 (Teorem XIV.2):** **kaynak-doğrulanmış** girdilerle Vela glitch
  (`ν = 11,194615396005 Hz`, `|ν̇| = 1,55615e-11 Hz/s`, `ΔI/I ≥ 0,014`):
  `Δν/ν = 2,07112467e-6`; 2004 olayıyla (`2,08e-6`) %0,43, en büyük 2000
  olayıyla (`3,0858e-6`) %32,9 sapma; ölçülen iyileşme kesri
  `Q_2000 = 0,02198`; gevşeme ölçekleri 1,2 dk / 0,53 / 3,29 / 19,07 gün.
- **T37 (Teorem XIV.3):** pozitronyum `O_exact` bant oranı `0,08413579`;
  yayımlanan (ln'siz) form `159,37`, `(2m_e-E)^2` ikameli form `9,31` — 1
  saatlik HPGe sayımı ikisini de `2,4e6 σ` ile çürütür.

## Sayısal yeniden-üretim

T35–T37 testleri **Makale V deposundaki** çözücüyle üretilir
([`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)):

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py     # T1–T37 (38/38 PASS)
python duran_sicimler_sim/mini_check_gp3.py    # bağımsız çapraz kontrol (15/15 PASS)
```

Bağımsız çapraz kontrol çözücüyü import etmez. Şekil 1,
`duran_sicimler_sim/generate_figures.py` içindeki `fig15` işleviyle üretilir.

## Atıf

```bibtex
@misc{meral2026grandproofiii,
  author = {Fahri Meral},
  title  = {Stationary Strings XIV: İki Önerilen Masaütstü Testi (Viskoelastik Girdap PIV ve Sodyum-22 Pozitronyum) ve Vela Pulsar Glitch Gözlemleri},
  year   = {2026},
  url    = {https://github.com/fahrim/stationary-strings-xiv},
  doi    = {10.5281/zenodo.23519746},
}
```

Ayrıca bkz. `CITATION.cff`.

## İlgili çalışmalar

- `stationary-strings-i` … `stationary-strings-x` — Teoremler I–X (ana seri).
- `stationary-strings-xii` — Karanlık-maddesiz galaktik dinamik, SPARC, EHT halkaları.
- `stationary-strings-xiii` — Yang–Mills kütle aralığı, glueball spektrumu, kuark kuşatması.

## Lisans

CC BY 4.0 — bkz. `LICENSE`. İçerik hakem denetiminden geçmemiştir.

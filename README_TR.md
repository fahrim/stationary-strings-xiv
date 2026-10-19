# Grand Proof III — Yayın Paketi (Büyük Kanıt Serisi III)

> **English:** [README.md](./README.md)

**Grand Proof III: Masaüstü Viskoelastik Girdap PIV Deneyi, Vela Pulsar Glitch Gözlemleri ve Sodyum-22 Pozitronyum Laboratuvar Kanıtı**

Yazar: Fahri Meral · Tarih: 19 Ekim 2026 · Sürüm: v1 (Grand Proof III)

> **Durum:** Yayımlanmamış ön-baskı (v1). Hakem denetiminden geçmemiştir.

## İçerik

| Dosya | Açıklama |
|---|---|
| `paper/grand_proof_III_deneysel_kanit_protokolu.tex` | Ana makale, Türkçe (Tablo 1–3, Şekil 1 2×2) |
| `paper/grand_proof_III_experimental_proof_protocol_EN.tex` | İngilizce sürüm |
| `figs/fig15_benchtop_piv_vortex_vela_glitch_and_na22_lab.pdf` | T35–T37 şekli (TR, 2×2) |
| `figs/fig15_benchtop_piv_vortex_vela_glitch_and_na22_lab.png` | T35–T37 şekil önizlemesi (TR) |
| `figs/fig15_benchtop_piv_vortex_vela_glitch_and_na22_lab_en.pdf` | T35–T37 şekli (EN, 2×2) |
| `figs/fig15_benchtop_piv_vortex_vela_glitch_and_na22_lab_en.png` | T35–T37 şekil önizlemesi (EN) |
| `CITATION.cff` | Atıf kaydı |
| `LICENSE` | CC BY 4.0 |

## Sonuçlar (sıfır serbest parametre)

- PEO girdap: çekirdek 5,14198 mm (C = 1,62603794, bant merkezi), hız 0,23703 m/s,
  huni 8,09603 mm (oran 0,31402536, bant merkezi).
- Vela glitch 2,38190025e-6, (2,25 ± 0,35)e-6 ile %5,86 (0,38σ);
  Q_fast 0,05910575, Q_total 0,13569214, ikisi de [0,05,0,18] içinde.
- Na-22 bant oranı 0,08413579; sahte formlar 9,31 / 159,37, 2,4e6σ ile çürütüldü.

## Sayısal yeniden-üretim

T35–T37 testleri **Makale V deposundaki** çözücüyle üretilir
([`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)):

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py   # T1–T37 (38/38 PASS)
python duran_sicimler_sim/mini_check_gp3.py  # bağımsız çapraz kontrol (12/12 PASS)
```

Bağımsız çapraz kontrol çözücüyü import etmez.
Şekil 1, `generate_figures.py` içindeki `fig15` işleviyle üretilir.

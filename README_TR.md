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

- PEO girdap: çekirdek 5,14198 mm (C = 1,62603794), hız 0,23703 m/s,
  huni 8,09603 mm (oran 0,31402536 = (1/a²)(1/(1+µ_s))). **Karşılaştırma
  bantları hayalet parametredir** (git arkeolojisi: bu çalışmayla girdi,
  literatür izi yok) ve iddia edilmez. Kaynak ölçümü a_ölçüm = 12–19
  verir; **model ölçümle çelişir**.
- Vela glitch 2,07112467e-6, kaynak-doğrulanmış girdilerle (ν = 11,194615 Hz,
  |ν̇| = 1,55615e-11 Hz/s, ΔI/I ≥ 0,014): 2004 olayından (2,08e-6) %0,43,
  en büyük 2000 olayından (3,0858e-6) %32,9; ölçülen iyileşme Q_2000 = 0,02198;
  gevşeme ölçekleri 1,2 dk / 0,53 / 3,29 / 19,07 gün.
- Na-22 bant oranı 0,08413579; sahte formlar 9,31 / 159,37, 2,4e6σ ile çürütüldü.

## Sayısal yeniden-üretim

T35–T37 testleri **Makale V deposundaki** çözücüyle üretilir
([`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)):

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py   # T1–T37 (38/38 PASS)
python duran_sicimler_sim/mini_check_gp3.py  # bağımsız çapraz kontrol (13/13 PASS)
```

Bağımsız çapraz kontrol çözücüyü import etmez.
Şekil 1, `generate_figures.py` içindeki `fig15` işleviyle üretilir.

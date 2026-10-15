# 🩸 Sistem Vitalitas, HP & Kelaparan Xuantian World

> **Modul:** 16 — Vitality & Hunger System
> **Rujukan:** `00_CORE_RULES_AI_GM.md`, `13_CULTIVATION_LAW_SYSTEM.md`, `INDEX.md`

---

## 1. Formula Perhitungan Max HP & Stamina

Status ketahanan fisik kultivator ditentukan oleh Ranah Kultivasi dan Hukum Elemen yang dipelajari:

### 1.1 Formula HP Maksimal
`MaxHP = CharacterBaseQiCap(realm, stage) × 0.4 × LawHPMultiplier`

*Contoh:* Kultivator Ranah *Kaimai Jing* Stage Awal (500 Qi) dengan Hukum Kayu Abadi (LawHPMultiplier ×1.5):
`MaxHP = 500 × 0.4 × 1.5 = 300 HP.`

### 1.2 Formula Max Stamina
`MaxStamina = 100 + (RealmIndex × 20)`

---

## 2. Sistem Kelaparan & Puasa Kultivasi (Fasting Mechanics)

Semakin tinggi Ranah Kultivasi seseorang, semakin sedikit kebutuhan makanan mortal karena tubuh dipenuhi oleh Qi Yuan.

### Tabel Daya Tahan Kelaparan Per Ranah Kultivasi
| Index | Ranah Kultivasi (Realm) | Waktu Sampai Kosong (0% Satiety) | Efek Kelaparan (Saat 0% Satiety) |
|---|---|---|---|
| 1 | **Lingquan Jing** | 12 Jam | HP & Qi Max -50%, Damage -30% |
| 2 | **Kaimai Jing** | 3 Hari | HP & Qi Max -30%, Stamina regen -50% |
| 3 | **Ningyuan Jing** | 14 Hari | HP & Qi Max -10% |
| 4 | **Lingyi Jing** | 30 Hari | Tidak ada penalti fisik signifikan |
| 5–9| **Xuantian Jing ke atas** | **Tak Terbatas (Bigusheng/Inedia)**| Kebal Kelaparan (Tubuh memakan Qi Langit) |

---

## 3. Efek Status Luka & Racun Pill (Pill Toxins)

### 3.1 Status Luka Fisik
* **Luka Ringan (HP 50%–75%):** Penalty Hit Chance -5%.
* **Luka Berat (HP 25%–49%):** Penalty Attack Power -25%, Qi Cost skill +20%.
* **Kritis / Coma (HP <25%):** Karakter tidak dapat melakukan Aksi Serangan Utama, butuh pertolongan medis/pill penyembuhan.

### 3.2 Racun Pill (Pill Toxin Accumulation)
Jika kultivator mengonsumsi terlalu banyak Pill kualitas rendah (*Low Purity*), akumulasi Toxin akan menumpuk di Dantian:
* **Toxin >30%:** Kecepatan regenerasi Qi -30%.
* **Toxin >60%:** Memicu Qi Deviation saat melakukan Breakthrough (-30% Breakthrough Chance).
* **Pembersihan Toxin:** Dapat dibersihkan dengan meditasi di *Shenmu Zhou*, meminum *Lotus Es Pill*, atau bantuan Alkemis Master.

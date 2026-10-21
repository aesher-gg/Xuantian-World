# 🩸 Xuantian World — Sistem Vitalitas (HP) & Kelangsungan Hidup

> **Modul:** 16 — Vitality & Hunger System
> **Prinsip:** Anti-Cheat Enforced — Root-Specific Scaling — Timestamped HP Logs
> **Rujukan:** `00_CORE_RULES_AI_GM.md` (aturan GM), `13_SPIRITUAL_ROOT_SYSTEM.md` (QiCap & Akar Spiritual), `15_ECONOMY_SYSTEM.md` (biaya pemulihan), `17_COMBAT_SYSTEM.md` (damage combat), `INDEX.md`

---

## 0. Filosofi Sistem Vitalitas & Kelaparan

Sama seperti Qi tunduk pada `QiCap` dan harga tunduk pada `FinalPrice`, HP (Vitalitas) dan rasa lapar juga tunduk pada formula tetap — tidak boleh dideklarasikan sepihak oleh player. Tiap Akar Spiritual punya karakter HP berbeda sesuai filosofinya, dan tiap Realm punya ketahanan lapar berbeda.

### Aturan Emas Anti-Cheat Vitalitas & Kelaparan
- HP TIDAK BOLEH dideklarasikan sepihak oleh player — dihitung AI GM lewat formula `HP(realm, stage, root)`.
- Kerusakan HP (damage) dicatat di log bertimestamp, tidak bisa diedit mundur atau "dilupakan" player.
- Regenerasi HP di luar batas alami hanya lewat pil/jasa tabib yang tunduk Sistem Ekonomi (`15_ECONOMY_SYSTEM.md`).
- Status kelaparan dihitung otomatis per jam in-game oleh AI GM, bukan klaim sepihak player.
- Breakthrough Realm langsung memperbarui HP Cap dan Fasting Multiplier karakter secara otomatis.

---

## 1. Formula Matematika Max HP, Stamina & Regenerasi Alami

Status ketahanan fisik kultivator ditentukan oleh Ranah Kultivasi, Stage, serta Akar Spiritual yang dimiliki:

### 1.1 Formula HP Maksimal (Max HP Formula)

```
BaseQiCap = RealmBaseQiCap(realm) × StageMultiplier(stage)
MaxHP = BaseQiCap × 0.40 × SpiritualRootHPMultiplier × (1 + BodyFortificationBonus)
```

*Tabel SpiritualRootHPMultiplier:*
* **Akar Spiritual Kayu Abadi (Wood Root):** `× 1.50`
* **Akar Spiritual Tanah & Segel (Earth Root):** `× 1.40`
* **Akar Spiritual Air & Es (Water/Ice Root):** `× 1.20`
* **Akar Spiritual Angin & Logam (Wind/Metal Root):** `× 1.00`
* **Akar Spiritual Api Purba (Fire Root):** `× 0.90`

*Contoh Calculation:* Kultivator Ranah *Kaimai Jing* Stage Tengah (750 Base Qi) dengan Akar Spiritual Kayu Abadi (1.50):
`MaxHP = 750 × 0.40 × 1.50 = 450 HP.`

### 1.2 Formula Max Stamina

```
MaxStamina = 100 + (RealmIndex × 20) + (BodyIntegrationStage × 10)
```

### 1.3 Formula Regenerasi HP Alami (Natural HP Regeneration)

```
HPRegenPerHour = MaxHP × 0.05 × RootRegenMultiplier × EnvironmentQiMultiplier
```
*(Akar Spiritual Kayu memberikan RootRegenMultiplier 1.5x, lingkungan Shenmu Zhou memberikan EnvironmentQiMultiplier 1.3x).*

---

## 2. Sistem Kelaparan & Puasa Kultivasi (Fasting & Inedia Mechanics)

Semakin tinggi Ranah Kultivasi seseorang, semakin sedikit kebutuhan makanan mortal karena tubuh dipenuhi oleh Qi Yuan.

### 2.1 Formula Penurunan Satiety (Kelaparan)

```
SatietyDropPerHour = 10% / FastingMultiplier(realm)
```

| Index | Ranah Kultivasi (Realm) | FastingMultiplier | Waktu Sampai Kosong (0% Satiety) |
|---|---|---|---|
| 1 | **Lingquan Jing** | 2.0x | 20 Jam |
| 2 | **Kaimai Jing** | 7.2x | 3 Hari (72 Jam) |
| 3 | **Ningyuan Jing** | 33.6x | 14 Hari (336 Jam) |
| 4 | **Lingyi Jing** | 72.0x | 30 Hari (720 Jam) |
| 5–9| **Xuantian Jing ke atas** | **Tak Terbatas (Inedia/Bigusheng)** | **Kebal Kelaparan (0% Drop)** |

### 2.2 Penalti Debuff Kelaparan
* **Satiety 26% – 100%:** Normal (Tanpa Debuff).
* **Satiety 11% – 25%:** Kelelahan Ringan (Stamina Regen -30%).
* **Satiety 1% – 10%:** Kelaparan Berat (Attack Power -25%, Qi Cost Skill +20%).
* **Satiety 0%:** Kelaparan Ekstrem (HP berkurang 5% MaxHP per jam sampai makan atau pingsan).

---

## 3. Formula Racun Pill (Pill Toxins) & Pembersihan Dantian

### 3.1 Penumpukan Pill Toxin

```
CurrentToxinPercent = Clamp(PreviousToxin + ConsumedPillToxin, 0%, 100%)
```

* **Toxin > 30%:** Kecepatan Regenerasi Qi Alami -30%.
* **Toxin > 60%:** Memicu Qi Deviation saat Breakthrough (-30% Breakthrough Chance, +20% Damage Tribulasi).
* **Toxin 100%:** Dantian Membeku (Karakter tidak dapat menyerap Qi sampai Toxin dibersihkan).

### 3.2 Formula Pembersihan Toxin

```
DailyToxinCleansed = BaseCleansingRate (5%) + (CleansingPillTier × 3%) + ShenmuZhouEnvironmentBonus (5%)
```

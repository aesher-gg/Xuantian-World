# 📜 Sistem Hukum Kultivasi & 9 Ranah Xuantian World

> **Modul:** 13 — Cultivation Law & Realm System
> **Rujukan:** `00_CORE_RULES_AI_GM.md`, `14_CRAFTING_AND_PROFESSIONS_SYSTEM.md`, `INDEX.md`

---

## 1. 9 Ranah Kultivasi Unik Xuantian World (Xuantian 9 Realms)

Di Xuantian World, jalur kultivasi menggunakan 9 Ranah Keagungan berikut:

```
[01. Lingquan Jing] -> [02. Kaimai Jing] -> [03. Ningyuan Jing]
                                                   |
[06. Tongtian Jing] <- [05. Xuantian Jing] <- [04. Lingyi Jing]
         |
[07. Faxiang Jing]  -> [08. Shenhuang Jing] -> [09. Hunyuan Jing (Fei Sheng)]
```

### 1.1 Formula Qi Capacity (QiCap Formula)
`CharacterQiCap = RealmBaseQiCap(realm) × StageMultiplier(stage)`

*StageMultiplier:*
* **Awal (Early Stage):** `× 1.0`
* **Tengah (Mid Stage):** `× 1.5`
* **Puncak (Peak Stage):** `× 2.0`

| Index | Nama Ranah (Realm) | Character Base QiCap | Stage Awal (Early) ×1.0 | Stage Tengah (Mid) ×1.5 | Stage Puncak (Peak) ×2.0 |
|---|---|---|---|---|---|
| 1 | **Lingquan Jing (灵泉境)** — Mata Air Spirit | 100 | 100 Qi | 150 Qi | 200 Qi |
| 2 | **Kaimai Jing (开脉境)** — Saluran Spirit | 500 | 500 Qi | 750 Qi | 1.000 Qi |
| 3 | **Ningyuan Jing (凝元境)** — Kondensasi Yuan | 2.500 | 2.500 Qi | 3.750 Qi | 5.000 Qi |
| 4 | **Lingyi Jing (灵意境)** — Kesadaran Spirit | 12.500 | 12.500 Qi | 18.750 Qi | 25.000 Qi |
| 5 | **Xuantian Jing (玄天境)** — Inti Xuantian | 62.500 | 62.500 Qi | 93.750 Qi | 125.000 Qi |
| 6 | **Tongtian Jing (通天境)** — Pilar Langit | 312.500 | 312.500 Qi | 468.750 Qi | 625.000 Qi |
| 7 | **Faxiang Jing (法相境)** — Avatar Dao | 1.562.500 | 1.562.500 Qi | 2.343.750 Qi | 3.125.000 Qi |
| 8 | **Shenhuang Jing (神皇境)** — Kaisar Divinitas | 7.812.500 | 7.812.500 Qi | 11.718.750 Qi | 15.625.000 Qi |
| 9 | **Hunyuan Jing (混元境)** — Primordial Hunyuan | 39.062.500 | 39.062.500 Qi | 58.593.750 Qi | 78.125.000 Qi |

### 1.2 Formula Regenerasi Qi Alami (Natural Qi Recovery)
`QiRegenPerHour = CharacterQiCap × 0.10 × EnvironmentQiMultiplier`

---

## 2. Mekanik Breakthrough & Tribulasi Langit (Heavenly Tribulation)

### 2.1 Formula Keberhasilan Breakthrough (Breakthrough Chance Formula)
`BaseChance = 50%`
`PillBonus = LowPurity (10%) | MidPurity (20%) | HighPurity (35%)`
`EnvironmentQiBonus = 10% (di wilayah ber-Qi tinggi yang cocok)`
`MeritBonus = MeritPoints × 0.1%`
`KarmaPenalty = SinPoints × 0.2%`
`PillToxinPenalty = CurrentToxinPercent × 0.3%`
`FinalBreakthroughChance = Clamp(BaseChance + PillBonus + EnvironmentQiBonus + MeritBonus - KarmaPenalty - PillToxinPenalty, 5%, 95%)`

### 2.2 Formula Damage Tribulasi Petir (Petir Langit Realm 4+)
Jika Roll Breakthrough gagal di Realm 4 ke atas, Tribulasi Petir memicu serangan balasan:

`LightningDamage = MaxHP × (0.30 + RealmIndex × 0.05) × (1 + SinPoints × 0.01) × (1 - MeritPoints × 0.005)`

---

## 3. 5 Hukum Elemen Utama & Multiplier Status

| Nama Hukum Elemen | HPMultiplier | AttackMultiplier | DefenseMultiplier | Efek Profesi Spesial |
|---|---|---|---|---|
| **Hukum Kayu Abadi (Wood Law)** | **×1.5** | ×1.0 | ×1.2 | +30% Kecepatan Tumbuh Berkebun & Penyembuhan |
| **Hukum Api Api Purba (Fire Law)** | ×0.9 | **×1.6** | ×0.9 | +25% Suhu & Purity Alkimia / Forging |
| **Hukum Angin & Pedang (Wind/Metal Law)**| ×1.0 | **×1.4** | ×1.0 | +20% Kelincahan / Niat Pedang |
| **Hukum Batu & Segel (Earth Law)** | **×1.4** | ×0.9 | **×1.6** | +30% Pertahanan Formasi & Talisman |
| **Hukum Air & Es Purba (Water/Ice Law)** | ×1.2 | ×1.1 | ×1.2 | +25% Efek Kontrol & Penjinakan Beast |

---

## 4. Sistem Karma (Merit & Sin)

* **Merit (Pahala/Kebaikan):** Diperoleh dari menolong fana, membasmi beast ganas, dan membela keadilan. Memberikan bonus ketahanan terhadap Tribulasi Langit (-15% Damage Petir Tribulasi).
* **Sin (Dosa/Karma Buruk):** Diperoleh dari membantai fana, perampokan, dan teknik iblis terlarang. Meningkatkan keganasan Petir Tribulasi (+30% Damage Petir Tribulasi & Pemicu Heart Demon).

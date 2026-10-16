# 🛠️ Sistem Kerajinan, Profesi & Formula Matematika Xuantian World

> **Modul:** 14 — Crafting & Professions Systems
> **Genre:** Xianxia Hardcore Realism
> **Rujukan:** `00_CORE_RULES_AI_GM.md`, `13_CULTIVATION_LAW_SYSTEM.md`, `15_ECONOMY_SYSTEM.md`, `INDEX.md`

---

## 1. Sistem Berkebun / Tanaman Obat Spirit (Spiritual Herb Farming)

Sistem berkebun memungkinkan kultivator menanam benih herbal spirit untuk digunakan sendiri dalam Alkimia atau dijual ke pasar obat.

### 1.1 Grade Tanah Spirit & Formula Waktu Tumbuh (Growth Time Calculation)
Waktu tumbuh tanaman obat spirit dihitung berdasarkan waktu standar benih dikurangi bonus grade tanah, pupuk Qi, dan Hukum Kayu Abadi:

`BaseGrowthDays = SeedStandardGrowthDays`
`SoilMultiplier = Grade 1 (1.0) | Grade 2 (0.75) | Grade 3 (0.50) | Grade 4 (0.25)`
`FertilizerDiscount = 0.30 (jika menggunakan Pupuk Qi Kayu) | 0.00 (tanpa pupuk)`
`WoodLawBonus = 0.30 (jika kultivator memiliki Hukum Kayu) | 0.00`
`ActualGrowthDays = Max(1, BaseGrowthDays × SoilMultiplier × (1.0 - FertilizerDiscount - WoodLawBonus))`

*Contoh:* Benih Lotus Es Abadi (Base: 14 hari) ditanam di Tanah Spirit Grade 3 (0.50) dengan Pupuk Qi (0.30) oleh pemegang Hukum Kayu (0.30):
`ActualGrowthDays = 14 × 0.50 × (1.0 - 0.30 - 0.30) = 7 × 0.40 = 2.8 Hari (dibulatkan 3 Hari).`

### 1.2 Formula Hasil Panen (Crop Yield Formula)
`HarvestYield = BaseYield (2–5 buah) × SoilYieldMultiplier × (1 + HerbalistSkillLevel × 0.10)`
*(Grade 4 Soil menggandakan BaseYield).*

---

## 2. Sistem Menjinakkan Beast (Beast Taming System)

### 2.1 Formula Keberhasilan Penjinakan (Taming Chance Formula)
`BaseChance = 30%`
`RealmDiffBonus = (CharacterRealmIndex - BeastRealmIndex) × 10%`
`HPDepletionBonus = (100% - BeastCurrentHP_Percent) × 0.40`
`SealTierBonus = SealTier × 10%`
`BaitBonus = 15% (jika menggunakan Pakan Kesukaan Spirit Beast)`
`WildnessPenalty = BeastTier × 5%`
`TamingSuccessChance = Clamp(BaseChance + RealmDiffBonus + HPDepletionBonus + SealTierBonus + BaitBonus - WildnessPenalty, 5%, 95%)`

### 2.2 Formula Degradasi & Peningkatan Kesetiaan (Loyalty System)
`LoyaltyGainPerFeeding = 5 + (AlchemistPillQuality × 2)`
`LoyaltyLossInBattleDefeat = 15 Points`
* Jika `Loyalty > 70`: Beast mendapat bonus Stats +10%.
* Jika `Loyalty < 30`: Beast berisiko membangkang (20% Chance membatalkan perintah) atau kabur.

---

## 3. Sistem Alkemis (Alchemy System)

### 3.1 Formula Kemurnian Pill (Alchemy Purity Formula)
`BasePurity = 50%`
`FlameQualityBonus = Mortal (0%) | Earth Qi (10%) | Natural Flame (20%) | Heavenly Flame (35%)`
`CauldronGradeBonus = CauldronTier × 5%`
`AlchemistSkillBonus = AlchemistLevel × 3%`
`DifficultyPenalty = (PillTier - AlchemistTier) × 15%`
`FinalPurity = Clamp(BasePurity + FlameQualityBonus + CauldronGradeBonus + AlchemistSkillBonus - DifficultyPenalty, 10%, 100%)`

### 3.2 Tabel Efek Kemurnian & Toxin Dantian
| Purity Range | Category | Multiplier Efek Pill | Akumulasi Pill Toxin Dantian |
|---|---|---|---|
| **10% – 49%** | Failed / Defective | 30% Efek | **+20% Toxin** |
| **50% – 69%** | Low Purity | 70% Efek | **+10% Toxin** |
| **70% – 89%** | Mid Purity | 100% Efek | **+3% Toxin** |
| **90% – 99%** | High Purity | 130% Efek | **0% Toxin (Bersih)** |
| **100%** | Perfect Pill (Danwen) | **160% Efek + Permanent Stat** | **0% Toxin (Murni)** |

---

## 4. Sistem Kapal Terbang Lintas Wilayah (Tiankong Feichuan Airship)

### 4.1 Formula Kecepatan Kapal Terbang (Airship Speed)
`BaseSpeed = Skiff (500 li/hari) | Freighter (1.000 li/hari) | Galleon (2.500 li/hari) | Battleship (4.000 li/hari)`
`PilotSkillBonus = PilotTier × 10%`
`Realm3QiDriveBonus = 100% (jika Pilot/Penumpang Realm 3+ menyuntikkan Qi Yuan)`
`FinalAirshipSpeed = BaseSpeed × (1.0 + PilotSkillBonus + Realm3QiDriveBonus)`

### 4.2 Consumable Fuel Formula
`SpiritStoneCostPerHour = (AirshipTier × 2 LSS) / (1.0 + Realm3QiDriveEfficiencyBonus)`

---

## 5. Sistem Formasi, Penempa & Jimat

### 5.1 Formula Barrier HP Formasi (Array Barrier Formula)
`BarrierHP = ArrayDiscBaseHP × (1 + ArrayMasterLevel × 0.15) × EnvironmentQiMultiplier`

### 5.2 Formula Durability & Damage Senjata Penempa (Forging Formula)
`WeaponDamage = BaseWeaponDamage × (1 + BlacksmithLevel × 0.08) × (1 + MetalTier × 0.10)`
`SoulBindingBonus = +20% Damage saat digunakan pemilik sah.`

### 5.3 Formula Success Rate Inskripsi Jimat (Talisman Crafting)
`TalismanSuccessChance = Clamp(60% + (TalismanMasterLevel - TalismanTier) × 10% + PaperQualityBonus, 10%, 95%)`

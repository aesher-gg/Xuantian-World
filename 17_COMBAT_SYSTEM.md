# ⚔️ Sistem Pertempuran Turn-Based & Formula Matematika Xuantian World

> **Modul:** 17 — Combat System
> **Rujukan:** `00_CORE_RULES_AI_GM.md`, `13_SPIRITUAL_ROOT_SYSTEM.md`, `14_CRAFTING_AND_PROFESSIONS_SYSTEM.md`, `INDEX.md`

---

## 1. Alur Pertempuran & Formula Inisiatif (Turn Initiative)

Pertempuran di Xuantian World berlangsung secara turn-based dengan urutan inisiatif:

### 1.1 Formula Inisiatif (Initiative Formula)
`BaseAgility = RealmIndex × 5`
`RootSpeedBonus = Wind/Metal Root (+5) | Other Roots (+0)`
`EquipmentSpeedBonus = Boots / Trinket Speed Bonus`
`InitiativeScore = BaseAgility + RootSpeedBonus + EquipmentSpeedBonus + (1d20 Roll)`

*Karakter/Musuh dengan `InitiativeScore` tertinggi bertindak lebih dahulu.*

### 1.2 Struktur Aksi per Giliran (Turn Action Allocation)
* **1 Aksi Utama (Main Action):** Menggunakan Teknik Senjata, Serangan Mantra Elemen, Melempar Talisman Combat, Memasang Formasi Portabel, atau Memerintahkan Spirit Beast.
* **1 Aksi Kecil (Bonus Action):** Mengonsumsi Pill Penyembuh, Memasang/Mengganti Equipment (1 item), Mengaktifkan Barrier Formasi.
* **1 Aksi Gerak (Movement Action):** Mendekat/Menjauh (Jarak Maksimal = 20 li / Turn).

---

## 2. Formula Matematika Damage, Defense & Hit Chance

### 2.1 Formula Attack Power (AP)
`AttackPower = CharacterQiCap × 0.15 × SpiritualRootAttackMultiplier × WeaponMultiplier × (1 + WeaponSoulBindingBonus)`

* **WeaponMultiplier:** Tier 1 (1.1x) | Tier 2 (1.25x) | Tier 3 (1.40x) | Tier 4 (1.60x) | Tier 5+ (2.0x+)
* **WeaponSoulBindingBonus:** +0.20 jika senjata telah menyatu dengan jiwa pengguna.

### 2.2 Formula Passive Defense (PD)
`PassiveDefense = CharacterQiCap × 0.05 × SpiritualRootDefenseMultiplier + ArmorDefenseRating`

### 2.3 Formula Hit Chance & Dodge
`BaseHit = 70%`
`RealmAdvantage = (AttackerRealmIndex - DefenderRealmIndex) × 5%`
`DodgePenalty = DefenderAgility × 0.5%`
`FinalHitChance = Clamp(BaseHit + RealmAdvantage - DodgePenalty + AccuracyBonus, 10%, 95%)`

### 2.4 Formula Critical Hit & Final Damage
`CritChance = 5% + (AttackerDexterity × 0.5%) + WindMetalRootBonus (5%)`
`CritDamageMultiplier = 1.50 (Standard) | 2.00 (High-Tier Weapon)`
`IsCrit = 1.50 jika Roll Crit Berhasil, sebaliknya 1.00`
`FinalDamage = Max(1, ((AttackPower × SkillMultiplier) - PassiveDefense) × IsCrit)`

---

## 3. Integrasi Aksi Profesi dalam Pertempuran

Karakter dengan spesialisasi profesi dapat menggunakan aksi khusus saat bertarung:

* **Alkemis (Pill Bom & Poison Gas):**
  `PillBombDamage = AlchemistLevel × 20 + FireFlameBonus (30)` (Ignore 30% Passive Defense).
* **Penjinak Beast (Spirit Beast Companion):**
  Spirit Beast bertindak dengan Inisiatif sendiri dan memiliki `AttackPower = BeastBaseQiCap × 0.12`.
* **Pembuat Formasi (Array Disc Barrier):**
  `BarrierHP = ArrayDiscBaseHP × (1 + ArrayMasterLevel × 0.15)`.
* **Pembuat Jimat (Combat Talisman):**
  `TalismanElementalDamage = TalismanTier × 50` (Konsumsi Qi = 0).

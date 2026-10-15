# ⚔️ Sistem Pertempuran Turn-Based Xuantian World

> **Modul:** 17 — Combat System
> **Rujukan:** `00_CORE_RULES_AI_GM.md`, `13_CULTIVATION_LAW_SYSTEM.md`, `14_CRAFTING_AND_PROFESSIONS_SYSTEM.md`, `INDEX.md`

---

## 1. Alur Pertempuran & Inisiatif (Turn Initiative)

Pertempuran di Xuantian World berlangsung secara turn-based dengan urutan inisiatif:

1. **Lemparan Inisiatif:** `Initiative = SpeedStat + RealmIndex + 1d20`
   *(Hukum Angin/Pedang memberikan bonus Inisiatif +5).*
2. **Aksi per Giliran (Turn Actions):**
   - **1 Aksi Utama (Main Action):** Menggunakan Teknik Senjata, Mantra Elemen, Melempar Talisman Combat, Memasang Formasi Portabel, atau Memerintahkan Spirit Beast.
   - **1 Aksi Kecil (Bonus Action):** Mengonsumsi Pill Penyembuh, Memasang/Mengganti Equipment, Mengaktifkan Barrier Formasi.
   - **1 Aksi Gerak (Movement):** Mendekat, Menjauh, atau Terbang.

---

## 2. Formula Perhitungan Pertempuran (Damage & Defense)

### 2.1 Power Serangan Dasar (Attack Power)
`AttackPower = CharacterBaseQiCap × 0.15 × LawAttackMultiplier × WeaponTierMultiplier`

### 2.2 Pertahanan Pasif (Passive Defense)
`PassiveDefense = CharacterBaseQiCap × 0.05 × LawDefenseMultiplier + ArmorDefense`

### 2.3 Peluang Kena (Hit Chance)
`HitChance = Clamp(70% + (RealmIndex_Penyerang - RealmIndex_Bertahan)×5% + SkillAccuracyBonus, 10%, 95%)`

### 2.4 Kerusakan Akhir (Final Damage Received)
`FinalDamage = Max(1, (AttackPower × SkillDamageMultiplier) - PassiveDefense)`

---

## 3. Integrasi Aksi Profesi dalam Pertempuran

Karakter dengan spesialisasi profesi dapat menggunakan aksi khusus saat bertarung:

* **Alkemis:** Melempar *Pill Bom Api* (Area Damage) atau *Pill Gas Racun* (Status Poison per giliran).
* **Penjinak Beast:** Memanggil Spirit Beast Pendamping ke arena (Beast bertindak dengan Inisiatif sendiri).
* **Pembuat Formasi:** Mengaktifkan *Piringan Formasi (Array Disc)* untuk membuat Barrier HP di sekitar diri sendiri dan sekutu.
* **Pembuat Jimat:** Melempar *Jimat Kilat Petir (Lightning Talisman)* tanpa memakan Qi karakter.

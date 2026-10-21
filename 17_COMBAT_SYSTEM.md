# ⚔️ Xuantian World — Sistem Pertempuran Turn-Based & Formula Combat

> **Modul:** 17 — Combat System
> **Prinsip:** Anti-Cheat Enforced — Strict Turn-Based — Root-Integrated Combat Math
> **Rujukan:** `00_CORE_RULES_AI_GM.md` (aturan GM), `13_SPIRITUAL_ROOT_SYSTEM.md` (QiCap & Akar Spiritual), `14_CRAFTING_AND_PROFESSIONS_SYSTEM.md` (profesi & item), `16_VITALITY_HUNGER_SYSTEM.md` (HP & Damage), `18_BESTIARY.md` (monster combat stats), `INDEX.md`

---

## 0. Filosofi Sistem Pertempuran

Pertarungan di Xuantian World harus terasa berbahaya, taktis, dan adil bagi **SEMUA** pihak — player, NPC, maupun monster. Setiap pihak yang terlibat pertarungan punya hak giliran yang sama, dan tidak ada pihak yang bisa "menyerang terus-menerus" sementara pihak lain dipaksa diam.

### Aturan Emas Anti-Cheat Pertempuran
- Giliran bersifat **WAJIB bergantian** — setelah 1 karakter bertindak, giliran otomatis pindah ke pihak berikutnya sesuai urutan Initiative. Tidak ada pengecualian.
- Player **TIDAK PERNAH** menentukan hasil aksi musuh — hanya AI GM yang memutuskan hasil aksi siapa pun selain aksi milik karakter player sendiri.
- Satu giliran = maksimal **1 Aksi Utama + 1 Aksi Kecil + 1 Aksi Gerak** — tidak bisa dipadatkan jadi "menyerang 10 kali sekaligus" lewat deskripsi naratif.
- NPC/monster **WAJIB bertindak sesuai Karakteristik & Sifat** yang sudah ditetapkan — tidak bisa "dilupakan" atau "dibuat pasif" oleh player tanpa alasan mekanik sah.
- Semua damage, Qi yang terpakai, dan hasil giliran dicatat di combat log bertimestamp — tidak bisa diedit mundur.

---

## 1. Alur Pertempuran & Formula Inisiatif (Turn Initiative)

Pertempuran di Xuantian World berlangsung secara turn-based dengan urutan inisiatif:

### 1.1 Formula Inisiatif (Initiative Formula)

```
InitiativeScore = (RealmIndex × 100 + StageBonus) + RootSpeedBonus + EquipmentSpeedBonus + Random(1–20)
```

- **RealmIndex:** 1–9 | **StageBonus:** Awal=0, Tengah=10, Puncak=20
- **RootSpeedBonus:** Akar Spiritual Angin/Logam (+15) | Lainnya (+0)
- **Random(1–20):** Lemparan dadu AI GM (bukan klaim player).

*Karakter/Musuh dengan `InitiativeScore` tertinggi bertindak lebih dahulu.*

### 1.2 Struktur Aksi per Giliran (Turn Action Allocation)
* **1 Aksi Utama (Main Action):** Menggunakan Teknik Senjata, Serangan Mantra Elemen, Melempar Talisman Combat, Memasang Formasi Portabel, atau Memerintahkan Spirit Beast.
* **1 Aksi Kecil (Bonus Action):** Mengonsumsi Pill Penyembuh, Memasang/Mengganti Equipment (1 item), Mengaktifkan Barrier Formasi.
* **1 Aksi Gerak (Movement Action):** Mendekat/Menjauh (Jarak Maksimal = 20 li / Turn).

---

## 2. Formula Matematika Damage, Defense & Hit Chance

### 2.1 Formula Attack Power (AP)

```
AttackPower = CharacterQiCap × 0.15 × SpiritualRootAttackMultiplier × WeaponMultiplier × (1 + WeaponSoulBindingBonus)
```

* **WeaponMultiplier:** Tier 1 (1.1x) | Tier 2 (1.25x) | Tier 3 (1.40x) | Tier 4 (1.60x) | Tier 5+ (2.0x+)
* **WeaponSoulBindingBonus:** +0.20 jika senjata telah menyatu dengan jiwa pengguna.

### 2.2 Formula Passive Defense (PD)

```
PassiveDefense = CharacterQiCap × 0.05 × SpiritualRootDefenseMultiplier + ArmorDefenseRating
```

### 2.3 Formula Hit Chance & Dodge

```
BaseHit = 70%
RealmAdvantage = (AttackerRealmIndex - DefenderRealmIndex) × 5%
DodgePenalty = DefenderAgility × 0.5%
FinalHitChance = Clamp(BaseHit + RealmAdvantage - DodgePenalty + AccuracyBonus, 10%, 95%)
```

### 2.4 Formula Critical Hit & Final Damage

```
CritChance = 5% + (AttackerDexterity × 0.5%) + WindMetalRootBonus (5%)
CritDamageMultiplier = 1.50 (Standard) | 2.00 (High-Tier Weapon)
IsCrit = 1.50 jika Roll Crit Berhasil, sebaliknya 1.00
FinalDamage = Max(1, ((AttackPower × SkillMultiplier) - PassiveDefense) × IsCrit)
```

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

# 📜 Sistem Akar Spiritual & 9 Ranah Xuantian World

> **Modul:** 13 — Spiritual Root System
> **Untuk:** Roleplay AI Game Master "Xuantian World"
> **Prinsip:** Anti-Cheat Enforced — Stable Tier Scaling — Karma-Linked Tribulation
> **Rujukan silang:** `00_CORE_RULES_AI_GM.md` (aturan wajib), `14_CRAFTING_AND_PROFESSIONS_SYSTEM.md` (profesi & kerajinan), `15_ECONOMY_SYSTEM.md` (harga bahan), `16_VITALITY_HUNGER_SYSTEM.md` (HP), `17_COMBAT_SYSTEM.md` (ATK & DEF), file regional `02`–`11` (Kerapatan Qi regional)

---

## 🧭 1. Filosofi Sistem Akar Spiritual

Setiap pembudidaya di Xuantian World terlahir dengan **Akar Spiritual (Spiritual Root / 灵根)** yang menentukan garis afinitas energi elemen (Kayu, Api, Angin & Logam, Tanah, Air & Es, dsb). Meskipun tiap jenis Akar Spiritual memberikan spesialisasi dan bonus statistik berbeda, **semua Akar Spiritual tunduk pada satu Formula Batas Qi (Qi Cap Formula)** yang sama agar menjaga keseimbangan dan mencegah power-creep.

**AI GM WAJIB menolak** klaim kekuatan/qi/item yang melampaui batas formula di bawah ini — tanpa pengecualian.

### Aturan Emas Anti-Cheat
- Qi/energi karakter tidak boleh melebihi `QiCap(realm, stage)` — dihitung ulang tiap turn oleh AI.
- Breakthrough (terobosan) HARUS memenuhi 3 syarat sekaligus: bahan minimum, insight/comprehension tervalidasi GM, dan (untuk realm 7+) selamat dari Tribulasi.
- Tidak ada retroactive edit stat oleh player — semua log qi/item bertimestamp dan tidak bisa diubah mundur.
- Item/pil hanya boleh menaikkan qi sebatas ±1 tier dari tier user saat ini (material tier matching).
- Akar Spiritual custom TETAP tunduk pada formula qi cap yang sama.

---

## 📊 2. 9 Ranah Kultivasi & Formula Qi Cap

### 2.1 Formula Inti Batas Qi (Qi Cap Formula)
$$\text{QiCap}(\text{realm}, \text{stage}) = \text{BaseQi}(\text{realm}) \times \text{StageMultiplier}(\text{stage})$$

- **Stage Multiplier:**
  - **Awal (Early):** `× 1.0`
  - **Tengah (Mid):** `× 1.5`
  - **Puncak (Peak):** `× 2.0`

### 2.2 Tabel 9 Ranah Kultivasi & Batas Qi

| Realm # | Nama Ranah Kultivasi | Base Qi (Awal) | Mid Qi (Tengah) | Peak Qi (Puncak) | Keterangan & Syarat Terobosan |
|---|---|---|---|---|---|
| 1 | **Lingquan Jing (灵泉境)** | 100 | 150 | 200 | Membuka mata air spirit di Dantian |
| 2 | **Kaimai Jing (开脉境)** | 500 | 750 | 1.000 | Membuka 108 urat spirit elemen |
| 3 | **Ningyuan Jing (凝元境)** | 2.500 | 3.750 | 5.000 | Memadatkan Qi gas menjadi Kristal Yuan |
| 4 | **Lingyi Jing (灵意境)** | 12.500 | 18.750 | 25.000 | Menyatu dengan kehendak elemen Akar Spiritual |
| 5 | **Xuantian Jing (玄天境)** | 62.500 | 93.750 | 125.000 | Membentuk Inti Dunia Xuantian di Dantian |
| 6 | **Tongtian Jing (通天境)** | 312.500 | 468.750 | 625.000 | Terhubung dengan pasokan Qi Langit & Bumi |
| 7 | **Faxiang Jing (法相境)** | 1.562.500 | 2.343.750 | 3.125.000 | Memanggil manifestasi Avatar Akar Spiritual |
| 8 | **Shenhuang Jing (神皇境)** | 7.812.500 | 11.718.750 | 15.625.000 | Membentuk Domain/Wilayah Elemen pribadi |
| 9 | **Hunyuan Jing (混元境)** | 39.062.500 | 58.593.750 | 78.125.000 | Keabadian sejati & persiapan Fei Sheng |

---

## ⚡ 3. 5 Jenis Akar Spiritual Utama & Multiplier Status

| Nama Akar Spiritual | HPMultiplier | AttackMultiplier | DefenseMultiplier | Efek Profesi Spesial |
|---|---|---|---|---|
| **Akar Spiritual Kayu Abadi (Wood Root)** | **×1.5** | ×1.0 | ×1.2 | +30% Kecepatan Tumbuh Berkebun & Penyembuhan |
| **Akar Spiritual Api Purba (Fire Root)** | ×0.9 | **×1.6** | ×0.9 | +25% Suhu & Purity Alkimia / Forging |
| **Akar Spiritual Angin & Logam (Wind/Metal Root)**| ×1.0 | **×1.4** | ×1.0 | +20% Kelincahan / Niat Pedang |
| **Akar Spiritual Tanah & Segel (Earth Root)** | **×1.4** | ×0.9 | **×1.6** | +30% Pertahanan Formasi & Talisman |
| **Akar Spiritual Air & Es Purba (Water/Ice Root)** | ×1.2 | ×1.1 | ×1.2 | +25% Efek Kontrol & Penjinakan Beast |

---

## 🌩️ 4. Terobosan Ranah (Breakthrough) & Tribulasi

1. **Realm 1 → Realm 6:** Memerlukan Pill Breakthrough sesuai Tier (`14_CRAFTING_AND_PROFESSIONS_SYSTEM.md`), lokasi dengan Qi Density seimbang, dan waktu pemurnian tanpa gangguan.
2. **Realm 7 → Realm 9 (Tribulasi Petir / Lightning Tribulation):**
   - Karakter harus menahan gempuran 3, 6, atau 9 sambaran Petir Tribulasi.
   - Kerusakan petir dipengaruhi oleh **Karma (Merit vs Sin)**:
     - Karma Positif (Merit > Sin): Kerusakan Petir berkurang -25%.
     - Karma Negatif (Sin > Merit): Kerusakan Petir meningkat +50% dan berisiko memicu Qi Deviation.

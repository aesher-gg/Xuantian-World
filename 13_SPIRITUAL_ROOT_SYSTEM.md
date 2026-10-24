# 📜 Xuantian World — Sistem Akar Spiritual & Ranah Kultivasi

> **Modul:** 13 — Spiritual Root System
> **Prinsip:** Anti-Cheat Enforced — Stable Tier Scaling — Karma-Linked Tribulation
> **Rujukan silang:** `00_CORE_RULES_AI_GM.md` (aturan wajib), `14_CRAFTING_AND_PROFESSIONS_SYSTEM.md` (profesi & kerajinan), `15_ECONOMY_SYSTEM.md` (harga bahan), `16_VITALITY_HUNGER_SYSTEM.md` (HP), `17_COMBAT_SYSTEM.md` (ATK & DEF), file regional `02`–`11` (Kerapatan Qi regional)

---

## 0. Filosofi Sistem

Setiap pembudidaya di Xuantian World terlahir dengan **Akar Spiritual (Spiritual Root / 灵根)** yang menentukan garis afinitas energi elemen (Kayu, Api, Angin & Logam, Tanah, Air & Es, dsb). Meskipun tiap jenis Akar Spiritual memberikan spesialisasi dan bonus statistik berbeda, **semua Akar Spiritual tunduk pada satu Formula Batas Qi (Qi Cap Formula)** yang sama agar menjaga keseimbangan dan mencegah power-creep.

### Aturan Emas Anti-Cheat Kultivasi
- Qi/energi karakter tidak boleh melebihi `QiCap(realm, stage)` — dihitung ulang tiap turn oleh AI GM. Player **TIDAK BOLEH** mendeklarasikan sendiri "Qi-ku naik jadi 10.000" tanpa terobosan sah tervalidasi GM.
- Breakthrough (terobosan) HARUS memenuhi 3 syarat sekaligus: bahan/pill minimum tervalidasi, insight/comprehension tervalidasi GM, dan (untuk realm 7+) selamat dari Tribulasi Petir.
- Tidak ada retroactive edit stat oleh player — semua log qi/item bertimestamp dan tidak bisa diubah mundur.
- Item/pil hanya boleh menaikkan qi sebatas ±1 tier dari tier user saat ini (material tier matching).
- Player **TIDAK BOLEH** mendeklarasikan sendiri "aku terobosan pakai Akar Spiritual X" di saat momen terobosan. AI GM yang menentukan berdasarkan teknik yang benar-benar dilatih sepanjang cerita.

---

## 📊 1. 9 Ranah Kultivasi & Formula Qi Cap

### 1.1 Formula Inti Batas Qi (Qi Cap Formula)

```
QiCap(realm, stage) = BaseQi(realm) × StageMultiplier(stage)
```

- **Stage Multiplier:**
  - **Awal (Early):** `× 1.0`
  - **Tengah (Mid):** `× 1.5`
  - **Puncak (Peak):** `× 2.0`

### 1.2 Tabel 9 Ranah Kultivasi & Batas Qi

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

## ⚡ 2. 5 Jenis Akar Spiritual Utama & Multiplier Status

| Nama Akar Spiritual | HPMultiplier | AttackMultiplier | DefenseMultiplier | Efek Profesi Spesial |
|---|---|---|---|---|
| **Akar Spiritual Kayu Abadi (Wood Root)** | **×1.5** | ×1.0 | ×1.2 | +30% Kecepatan Tumbuh Berkebun & Penyembuhan |
| **Akar Spiritual Api Purba (Fire Root)** | ×0.9 | **×1.6** | ×0.9 | +25% Suhu & Purity Alkimia / Forging |
| **Akar Spiritual Angin & Logam (Wind/Metal Root)**| ×1.0 | **×1.4** | ×1.0 | +20% Kelincahan / Niat Pedang |
| **Akar Spiritual Tanah & Segel (Earth Root)** | **×1.4** | ×0.9 | **×1.6** | +30% Pertahanan Formasi & Talisman |
| **Akar Spiritual Air & Es Purba (Water/Ice Root)** | ×1.2 | ×1.1 | ×1.2 | +25% Efek Kontrol & Penjinakan Beast |

---

## 🌀 3. Formula Regenerasi Qi Alami & Meditasi

Pemulihan energi Qi kultivator dibagi menjadi regenerasi pasif (per jam) dan pemulihan aktif (meditasi/retret):

### 3.1 Formula Regenerasi Qi Pasif (Passive Qi Regen)

```
QiRegenPerHour = QiCap × 0.05 × RootRegenMultiplier × EnvironmentQiModifier × (1.0 - PillToxinPercent)
```

- **RootRegenMultiplier:** Kayu (1.5x) | Air/Es (1.2x) | Angin/Logam (1.0x) | Tanah (1.0x) | Api (0.9x).
- **EnvironmentQiModifier:** Disesuaikan dengan Qi Density Modifier wilayah (misal Shenmu Zhou = 1.25x, Juejing Zhou = 1.50x chaotic, Beihan Zhou = 1.30x).
- **PillToxinPercent:** Penalti racun pill dantian (`16_VITALITY_HUNGER_SYSTEM.md`).

### 3.2 Formula Regenerasi Qi Meditasi Aktif (Meditation Qi Recovery)

```
MeditationQiPerMinute = (QiCap × 0.02) × (1 + ComprehensionLevel × 0.10) × SpiritStoneGatheringBonus
```

### 3.3 Efek Ruang Spesial & Dilatasi Waktu (Pocket World Time Dilation)
Untuk tempat khusus yang memiliki Dunia Kecil Mandiri (*Pocket World*), seperti **Gantungan Giok Alam Hunyuan** (`51_SPECIAL_ITEMS.md`):
- **Dilatasi Waktu 1:24:** **1 Jam meditasi di dalam dunia giok setara dengan 24 Jam (1 Hari) waktu dunia luar.**
- **Hasil Meditasi:** Memberikan pemulihan Qi Cap 100% instan dan melipatgandakan serapan wawasan/insight terobosan sebesar 24x lipat tanpa risiko penalti kelelahan Dantian.

---

## 🌟 4. Mekanik & Formula Keberhasilan Penerobosan (Breakthrough System)

Terobosan (*Breakthrough*) adalah proses menaikkan stage (Awal $\rightarrow$ Tengah $\rightarrow$ Puncak) atau menembus ranah kultivasi baru (Realm 1 $\rightarrow$ Realm 9). Di Xuantian World, **semakin tinggi Ranah Kultivasi, semakin ekstrem tingkat kesulitan dan risiko kegagalannya**.

### 4.1 Skala Kesulitan Terobosan Berjenjang (Progressive Breakthrough Scaling)

Tingkat keberhasilan dasar (*Base Success Rate*) menurun secara signifikan seiring tingginya Ranah, sementara syarat waktu meditasi stasioner dan durasi pemulihan Dantian meningkat secara eksponensial:

| Realm # | Nama Ranah Kultivasi | Base Rate Sub-Stage (Awal $\rightarrow$ Tengah $\rightarrow$ Puncak) | Base Rate Major Realm (Penembusan Ranah Baru) | Waktu Meditasi Minimum | Risiko Qi Deviation (Jika Gagal) |
|---|---|---|---|---|---|
| 1 | **Lingquan Jing (灵泉境)** | **85%** | **70%** (Tembus Realm 2) | 3 Jam | Minor (Kerusakan 10% HP) |
| 2 | **Kaimai Jing (开脉境)** | **75%** | **60%** (Tembus Realm 3) | 12 Jam | Ringan (Kerusakan 20% HP) |
| 3 | **Ningyuan Jing (凝元境)** | **65%** | **50%** (Tembus Realm 4) | 3 Hari | Sedang (Kerusakan 30% HP, Dantian Lelah 2 Hari) |
| 4 | **Lingyi Jing (灵意境)** | **55%** | **40%** (Tembus Realm 5) | 7 Hari | Berat (Kerusakan 40% HP, Dantian Retak Ringan) |
| 5 | **Xuantian Jing (玄天境)** | **45%** | **30%** (Tembus Realm 6) | 14 Hari | Sangat Berat (Kerusakan 50% HP, Dantian Retak) |
| 6 | **Tongtian Jing (通天境)** | **35%** | **20%** (Tembus Realm 7) | 1 Bulan | Parah (Kerusakan 60% HP, Toxin +30%) |
| 7 | **Faxiang Jing (法相境)** | **25%** | **15%** (Tembus Realm 8) + Tribulasi 3 Petir | 3 Bulan | Kritis (Kerusakan 75% HP, Penurunan 1 Sub-stage) |
| 8 | **Shenhuang Jing (神皇境)** | **15%** | **10%** (Tembus Realm 9) + Tribulasi 6 Petir | 6 Bulan | Ektrem (Kerusakan 90% HP, Dantian Hancur) |
| 9 | **Hunyuan Jing (混元境)** | **10%** | **5%** (Fei Sheng / Kenaikan Abadi) + Tribulasi 9 Petir | 1 Tahun | Maut / Permadeath (Dantian Meledak Fatal) |

### 4.2 Formula Persentase Keberhasilan Terobosan (Breakthrough Success Chance)

```
BreakthroughChance = Clamp(BaseRate(Realm, Stage) + PillQualityBonus + InsightBonus + EnvironmentBonus - ToxinPenalty - DeviationPenalty, 5%, 95%)
```
- **Pill Quality Bonus:**
  - *No Pill / Failed Pill:* `+0%`
  - *Low Purity Pill (50-69%):* `+10%`
  - *Mid Purity Pill (70-89%):* `+20%`
  - *High Purity Pill (90-99%):* `+35%`
  - *Perfect Pill (100% Danwen):* `+50%`
- **Insight & Comprehension Bonus:** `+5%` hingga `+20%` berdasarkan hasil pemahaman wawasan Dao/Akar Spiritual tervalidasi GM.
- **Environment Qi Bonus:** `+10%` jika berada di Spirit Vein / Markas Sekte berelemental sama.
- **Penalti Toxin & Deviation:** `-20%` jika Toxin > 30%, dan `-30%` jika mengalami trauma dantian.

### 4.2 Risiko Kegagalan & Qi Deviation (Penyimpangan Qi)
Jika roll keberhasilan terobosan gagal:
1. **Kegagalan Biasa (Roll = Chance - 20%):** Qi terbuang 50%, Dantian mengalami kelelahan selama 1 hari, tidak ada penurunan ranah.
2. **Qi Deviation / Penyimpangan Qi (Roll < Chance - 20%):** HP berkurang 40% MaxHP, Qi berkurang ke 0, Toxin Dantian bertambah +20%, dan mengalami trauma Dantian Retak (perlu obat tabib `40_WANDERING_PHYSICIAN_ASSOCIATION.md`).

---

## 🌩️ 5. Formula Damage & Mekanik Tribulasi Petir (Lightning Tribulation)

Penerobosan menuju Ranah 7 (*Faxiang Jing*), Ranah 8 (*Shenhuang Jing*), dan Ranah 9 (*Hunyuan Jing*) memicu Kemurkaan Langit berwujud **Tribulasi Petir (Lightning Tribulation / 雷劫)**.

### 5.1 Jumlah Sambaran Petir Tribulasi
- **Realm 6 $\rightarrow$ Realm 7 (Faxiang Jing):** 3 Sambaran Petir Spirit.
- **Realm 7 $\rightarrow$ Realm 8 (Shenhuang Jing):** 6 Sambaran Petir Divinitas.
- **Realm 8 $\rightarrow$ Realm 9 (Hunyuan Jing):** 9 Sambaran Petir Primordial.

### 5.2 Formula Kerusakan Petir per Sambaran (Lightning Strike Damage)

```
StrikeDamage = (TargetMaxHP × 0.40) × StrikeIndexMultiplier × KarmaMultiplier - ActiveDefenses
```

- **StrikeIndexMultiplier:** Sambaran 1–3 (`×1.0`), Sambaran 4–6 (`×1.3`), Sambaran 7–9 (`×1.7`).
- **KarmaMultiplier:** Ditentukan oleh Keseimbangan Karma (§6).
- **ActiveDefenses:** Pengurangan damage dari Zirah Spirit, Talisman Pelindung, Formasi Barrier, dan Jurus Pertahanan.

---

## ☯️ 6. Sistem Karma: Merit vs Sin Mechanics

Karma melacak keseimbangan moralitas dan tindakan pembudidaya di Xuantian World:

```
KarmaBalance = MeritPoints - SinPoints
```

### 6.1 Sumber Poin Merit & Sin
- **Merit Points (+):** Menyelamatkan desa fana (+10), membasmi Beast Bencana (+25), mengobati luka dalam pembudidaya lain (+15), menjaga integritas hutan/alam (+20).
- **Sin Points (-):** Memantai fana tanpa dosa (-30), menggunakan teknik pembunuhan jiwa hantu (-20), merampok pembudidaya muda (-15), mengkhianati janji darah sekte (-40).

### 6.2 Dampak Karma pada Tribulasi & Domain
| Status Karma | Karma Balance | KarmaMultiplier Tribulasi | Efek Tambahan di Dunia |
|---|---|---|---|
| **Puji Agung (Saintly Merit)** | Balance $\ge +100$ | **×0.75 (-25% Damage)** | Dihormati NPC Ortodoks, +15% Evasion terhadap serangan iblis |
| **Kebajikan (Positive)** | $+10 \le \text{Balance} < +100$ | **×0.90 (-10% Damage)** | Hubungan diplomatik sekte +10% |
| **Netral (Balanced)** | $-10 < \text{Balance} < +10$ | **×1.00 (Normal)** | Tanpa modifier |
| **Tercela (Sinful)** | $-100 < \text{Balance} \le -10$ | **×1.25 (+25% Damage)** | Rawan memicu Qi Deviation saat terobosan |
| **Iblis Purba (Demonic Sin)** | Balance $\le -100$ | **×1.50 (+50% Damage)** | Diburu Pasukan Kekaisaran & Sekte Ortodoks, Petir Tribulasi merah |

# 📜 Xuantian World — Sistem Akar Spiritual & Ranah Kultivasi (Spiritual Root System)

> **Modul:** 13 — Spiritual Root System
> **Untuk:** Roleplay AI Game Master Xuantian World
> **Prinsip:** Anti-Cheat Enforced — Stable Tier Scaling — Karma-Linked Tribulation
> **Rujukan silang:** `00_CORE_RULES_AI_GM.md` (aturan wajib), `14_CRAFTING_AND_PROFESSIONS_SYSTEM.md` (profesi & kerajinan), `15_ECONOMY_SYSTEM.md` (harga bahan), `16_VITALITY_HUNGER_SYSTEM.md` (HP & Toxin), `17_COMBAT_SYSTEM.md` (Formula Combat), file regional `02`–`11` (Kerapatan Qi regional)

---

## 🧭 1. Filosofi Sistem & Pembedaan Keberadaan Akar Spiritual

Setiap makhluk hidup di Xuantian World terlahir di bawah hukum alam benua kultivasi. Namun, **keberadaan Akar Spiritual (Spiritual Root / 灵根) tidak dimiliki oleh semua manusia fana secara otomatis**.

### 1.1 Klasifikasi Bangsa Fana (Mortal Division):
Masyarakat fana di Xuantian World terbagi menjadi dua golongan alami:
1. **Fana Murni Tanpa Akar Spiritual (Mortal without Spiritual Root):** Sekitar 85% populasi. Tubuh mereka tidak memiliki meridian penghantar Qi dan tidak mampu menyerap energi spirit alam semesta. Mereka tidak dapat berkultivasi menjadi pembudidaya sejati kecuali mendapatkan keajaiban purba (*Reconstituting Pill Grade 8+* atau pencerahan sumsum tulang oleh Dewa).
2. **Fana Ber-Akar Spiritual (Mortal with Spiritual Root):** Sekitar 15% populasi. Mereka terlahir dengan benih Akar Spiritual bawaan (Kayu, Api, Angin/Logam, Tanah, atau Air/Es) yang dapat diaktifkan saat memasuki Ranah *Lingquan Jing* melalui pengujian batu penguji spirit atau bimbingan sekte/perguruan.

### Aturan Emas Anti-Cheat Kultivasi
- Qi/energi karakter tidak boleh melebihi `QiCap(realm, stage)` — dihitung ulang tiap turn oleh AI GM. Player **TIDAK BOLEH** mendeklarasikan sendiri "Qi-ku naik jadi 10.000" tanpa terobosan sah tervalidasi GM.
- Breakthrough (terobosan) HARUS memenuhi syarat mutlak: akumulasi Qi 95%+, bahan/pill minimum tervalidasi, insight/comprehension tervalidasi GM, dan (untuk realm 7+) selamat dari Tribulasi Petir.
- Tidak ada retroactive edit stat oleh player — semua log qi/item bertimestamp dan tidak bisa diubah mundur.
- Item/pil hanya boleh menaikkan qi sebatas ±1 tier dari tier user saat ini (material tier matching).
- Akar Spiritual custom TETAP tunduk pada formula qi cap yang sama — hanya reskin mekanik elemen, bukan reskin batas.
- **Akar Spiritual Bawaan vs Teknik Elemen:** Akar Spiritual adalah benih potensi bawaan raga (85% fana tidak memiliki, 15% fana memiliki). Namun, pengaktifan benih Akar Spiritual dan penguasaan Teknik Elemen **WAJIB** memiliki riwayat asal-usul yang sah yang tercatat di log karakter (§3.0 & §3.1). Deklarasi sepihak tanpa riwayat pengujian/latihan = otomatis DITOLAK.

---

## 🌀 2. Struktur Ranah Universal (9 Major Realm × 3 Stage = 27 Sub-Tier)

Semua Akar Spiritual memakai kerangka ranah kultivasi resmi Xuantian World (Base Qi & Qi Cap asli tervalidasi):

| # | Major Realm | Base Qi (Awal) | Mid Qi (Tengah) | Peak Qi (Puncak) | Keterangan & Syarat Terobosan |
|---|---|---|---|---|---|
| 1 | **Lingquan Jing (灵泉境)** | 100 | 150 | 200 | Membuka mata air spirit di Dantian |
| 2 | **Kaimai Jing (开脉境)** | 500 | 750 | 1.000 | Membuka 108 urat spirit elemen |
| 3 | **Ningyuan Jing (凝元境)** | 2.500 | 3.750 | 5.000 | Memadatkan Qi gas menjadi Kristal Yuan |
| 4 | **Lingyi Jing (灵意境)** | 12.500 | 18.750 | 25.000 | Menyatu dengan kehendak elemen Akar Spiritual |
| 5 | **Xuantian Jing (玄天境)** | 62.500 | 93.750 | 125.000 | Membentuk Inti Dunia Xuantian di Dantian |
| 6 | **Tongtian Jing (通天境)** | 312.500 | 468.750 | 625.000 | Terhubung dengan pasokan Qi Langit & Bumi |
| 7 | **Faxiang Jing (法相境)** | 1.562.500 | 2.343.750 | 3.125.000 | Memanggil manifestasi Avatar Akar Spiritual |
| 8 | **Shenhuang Jing (神皇境)** | 7.812.500 | 11.718.750 | 15.625.000 | Membentuk Domain/Wilayah Elemen pribadi |
| 9 | **Hunyuan Jing (混元境)** | 39.062.500 | 58.593.750 | 78.125.000 | Keabadian sejati & persiapan Kenaikan Abadi (Fei Sheng) |

Tiap Major Realm punya 3 Stage: **Awal (×1,0) $\rightarrow$ Tengah (×1,5) $\rightarrow$ Puncak (×2,0)**.

### 🔒 Formula Qi Cap Asli Xuantian World (WAJIB DIPAKAI AI GM)

```
QiCap(realm, stage) = BaseQi(realm) × StageMultiplier(stage)
```

*Contoh:* Xuantian Jing Puncak = 62.500 × 2,0 = **125.000 poin Qi maksimum**. Klaim di atas ini otomatis DITOLAK sistem.

---

## ⚡ 3. Jenis Akar Spiritual Utama & Afinitas Elemen

### 🔐 3.0 Asal-Usul Pengaktifan Akar Spiritual (Spiritual Root Activation Origin)

Meskipun benih Akar Spiritual sudah ada di dalam raga 15% bangsa fana sejak lahir, **pengaktifan dan pemurnian Akar Spiritual untuk pertama kalinya WAJIB dicatat di log karakter lewat salah satu jalur sah berikut:**

| Jalur Pengaktifan Akar | Syarat & Prosedur Sah | Contoh Tidak Sah (Ditolak) |
|---|---|---|
| **1. Batu Penguji Spirit (Testing Stone)** | Diuji di Sekte/Perguruan/Pasar Kota menggunakan Batu Penguji Spirit Grade 1+ untuk mendeteksi benih elemen bawaan. | Player langsung menyatakan "aku punya Akar Spiritual Mutasi Petir" tanpa pernah diuji. |
| **2. Pil Pemurni Akar Spirit** | Mengonsumsi Pil Pemurni Akar Spirit (seperti *Awakening Pill*) tervalidasi di inventory untuk membangunkan benih tersembunyi. | Player mengklaim meminum obat gaib tanpa item tercatat di inventory. |
| **3. Bimbingan Ketukan Dantian** | Bimbingan meditasi oleh Tetua/Guru Ranah *Xuantian Jing* ke atas yang menyalurkan Qi untuk membuka mata air Dantian. | Player menyatakan Dantiannya terbuka sendiri tanpa bantuan/meditasi yang dinarasikan. |

---

### 📜 3.1 Asal-Usul Teknik & Jurus Elemen (Elemental Technique Origin)

Penguasaan teknik/jurus elemen untuk menyalurkan energi Akar Spiritual **BERBEDA** dari pengaktifan benih raga. Jurus elemen hanya sah jika didapatkan dari salah satu dari 3 jalur berikut:

| Jalur Asal-Usul Teknik | Syarat & Prosedur Sah | Contoh Tidak Sah (Ditolak) |
|---|---|---|
| **1. Guru / Sekte / Perguruan** | Diajarkan oleh NPC Guru/Sekte melalui adegan latihan nyata yang dinarasikan dan dicatat oleh AI GM. | Player tiba-tiba bilang "guruku dulu mengajariku Jurus Es" tanpa adegan pengajaran di cerita. |
| **2. Kitab Manual Pusaka** | Mempelajari Kitab/Gulungan Jurus yang ada di inventory resmi (didapat dari looting/pembelian/hadiah). | Player mengklaim tahu jurus rahasia tanpa kitab tercatat di inventory. |
| **3. Pencerahan Dao (Enlightenment)** | Dipicu oleh AI GM setelah pengumpulan Insight Point lewat meditasi ekstrim atau pertarungan hidup-mati. | Player mendadak menyatakan "aku menciptakan jurus elemen baru" di tengah pertarungan tanpa pencerahan GM. |

### A. 🌿 Akar Spiritual Kayu Abadi (Wood Root)
- **Afinitas Utama:** Qi Kayu / Alam / Hutan Purba.
- **Bonus Status:** HP Multiplier ×1.5, Defense Multiplier ×1.2.
- **Efek Profesi Spesial:** +30% Kecepatan Tumbuh Berkebun & Penyembuhan Luka Dalam.
- **Organisasi Pengguna:** Sekte Induk Shenmu, Perguruan Berkebun Biyang.

### B. 🔥 Akar Spiritual Api Purba (Fire Root)
- **Afinitas Utama:** Qi Api / Lava / Kawah Vulkanik.
- **Bonus Status:** Attack Multiplier ×1.6, HP Multiplier ×0.9.
- **Efek Profesi Spesial:** +25% Suhu Kuali & Purity Alkimia / Penempaan Besi.
- **Organisasi Pengguna:** Sekte Alkimia Danhuang, Istana Api Chiyan.

### C. 🗡️ Akar Spiritual Angin & Logam (Wind/Metal Root)
- **Afinitas Utama:** Qi Angin / Logam / Niat Pedang (*Sword Intent*).
- **Bonus Status:** Attack Multiplier ×1.4, Kelincahan +20%.
- **Efek Profesi Spesial:** +20% Critical Hit Chance & Penembusan Zirah Fisik.
- **Organisasi Pengguna:** Paviliun Pedang Canglong, Sekte Pedang Kekaisaran Tianjing.

### D. 🛡️ Akar Spiritual Tanah & Segel (Earth Root)
- **Afinitas Utama:** Qi Tanah / Batu / Formasi Barrier.
- **Bonus Status:** Defense Multiplier ×1.6, HP Multiplier ×1.4.
- **Efek Profesi Spesial:** +30% Pertahanan Formasi & Kekuatan Inskripsi Talisman.
- **Organisasi Pengguna:** Perguruan Formasi Tiangong, Sekte Jimat Gurun Huangsha.

### E. 🌊 Akar Spiritual Air & Es Purba (Water/Ice Root)
- **Afinitas Utama:** Qi Air / Es / Lautan.
- **Bonus Status:** HP Multiplier ×1.2, Attack Multiplier ×1.1, Defense Multiplier ×1.2.
- **Efek Profesi Spesial:** +25% Efek Kontrol / Pembekuan & Penjinakan Spirit Beast.
- **Organisasi Pengguna:** Istana Kemurnian Giok Laut, Perguruan Alkimia Es Beihan.

---

## 🌀 4. Formula Regenerasi Qi & Meditasi

### 4.1 Formula Regenerasi Qi Pasif (Passive Qi Regen)

```
QiRegenPerHour = QiCap × 0.05 × RootRegenMultiplier × EnvironmentQiModifier × (1.0 - PillToxinPercent)
```
- **RootRegenMultiplier:** Kayu (1.5x) | Air/Es (1.2x) | Angin/Logam (1.0x) | Tanah (1.0x) | Api (0.9x).
- **EnvironmentQiModifier:** Disesuaikan dengan Qi Density Modifier wilayah (misal Shenmu Zhou = 1.25x, Juejing Zhou = 1.50x chaotic).
- **PillToxinPercent:** Penalti racun pill dantian (`16_VITALITY_HUNGER_SYSTEM.md`).

### 4.2 Formula Regenerasi Qi Meditasi Aktif (Meditation Qi Recovery)

```
MeditationQiPerMinute = (QiCap × 0.02) × (1 + ComprehensionLevel × 0.10) × SpiritStoneGatheringBonus
```

### 4.3 Efek Ruang Spesial & Dilatasi Waktu (Pocket World Time Dilation)
Untuk tempat khusus yang memiliki Dunia Kecil Mandiri (*Pocket World*), seperti **Gantungan Giok Alam Hunyuan** (`51_SPECIAL_ITEMS.md`):
- **Dilatasi Waktu 1:24:** **1 Jam meditasi di dalam dunia giok setara dengan 24 Jam (1 Hari) waktu dunia luar.**
- **Hasil Meditasi:** Memberikan pemulihan Qi Cap 100% instan dan melipatgandakan serapan wawasan/insight terobosan sebesar 24x lipat tanpa risiko penalti kelelahan Dantian.

---

## 🌟 5. Skala Kesulitan Terobosan Berjenjang (Breakthrough System)

Terobosan (*Breakthrough*) adalah proses menaikkan stage (Awal $\rightarrow$ Tengah $\rightarrow$ Puncak) atau menembus ranah kultivasi baru (Realm 1 $\rightarrow$ Realm 9). Di Xuantian World, **semakin tinggi Ranah Kultivasi, semakin ekstrem tingkat kesulitan dan risiko kegagalannya**.

### 5.1 Skala Kesulitan Terobosan Berjenjang (Progressive Breakthrough Scaling)

| Realm # | Nama Ranah Kultivasi | Base Rate Sub-Stage (Awal $\rightarrow$ Tengah $\rightarrow$ Puncak) | Base Rate Major Realm (Penembusan Ranah Baru) | Waktu Meditasi Minimum | Risiko Qi Deviation (Jika Gagal) |
|---|---|---|---|---|---|
| 1 | **Lingquan Jing (灵泉境)** | **85%** | **70%** (Tembus Realm 2) | 3 Jam | Minor (Kerusakan 10% HP) |
| 2 | **Kaimai Jing (开脉境)** | **75%** | **60%** (Tembus Realm 3) | 12 Jam | Ringan (Kerusakan 20% HP) |
| 3 | **Ningyuan Jing (凝元境)** | **65%** | **50%** (Tembus Realm 4) | 3 Hari | Sedang (Kerusakan 30% HP, Dantian Lelah 2 Hari) |
| 4 | **Lingyi Jing (灵意境)** | **55%** | **40%** (Tembus Realm 5) | 7 Hari | Berat (Kerusakan 40% HP, Dantian Retak Ringan) |
| 5 | **Xuantian Jing (玄天境)** | **45%** | **30%** (Tembus Realm 6) | 14 Hari | Sangat Berat (Kerusakan 50% HP, Dantian Retak) |
| 6 | **Tongtian Jing (通天境)** | **35%** | **20%** (Tembus Realm 7) | 1 Bulan | Parah (Kerusakan 60% HP, Toxin +30%) |
| 7 | **Faxiang Jing (法相境)** | **25%** | **15%** (Tembus Realm 8) + Tribulasi 3 Petir | 3 Bulan | Kritis (Kerusakan 75% HP, Penurunan 1 Sub-stage) |
| 8 | **Shenhuang Jing (神皇境)** | **15%** | **10%** (Tembus Realm 9) + Tribulasi 6 Petir | 6 Bulan | Ekstrem (Kerusakan 90% HP, Dantian Hancur) |
| 9 | **Hunyuan Jing (混元境)** | **10%** | **5%** (Fei Sheng / Kenaikan Abadi) + Tribulasi 9 Petir | 1 Tahun | Maut / Permadeath (Dantian Meledak Fatal) |

---

### 5.2 Aturan & Formula Spesifik Terobosan Sub-Stage (Awal $\rightarrow$ Tengah $\rightarrow$ Puncak)

#### A. Syarat Mutlak Akumulasi Qi Sub-Stage
Kultivator **WAJIB** memenuhi syarat akumulasi Qi minimal sebelum dapat mengajukan percakapan terobosan sub-stage:
```
RequiredQiToBreakthrough = CurrentQiCap × 0.95
```

#### B. Formula Keberhasilan Terobosan Sub-Stage

```
SubStageBreakthroughChance = Clamp(BaseRateSubStage(Realm) + SubStagePillBonus + InsightBonus + EnvironmentBonus - ToxinPenalty, 5%, 95%)
```
- **Awal $\rightarrow$ Tengah:** Base Rate = `BaseRateSubStage(Realm)`, Bakar 50% Qi.
- **Tengah $\rightarrow$ Puncak:** Base Rate = `BaseRateSubStage(Realm) - 10%`, Bakar 75% Qi.
- **Bonus Pill Sub-Stage:** Low Purity (+10%), Mid Purity (+15%), High Purity (+25%), Perfect Danwen (+35%).

---

### 5.3 Aturan & Formula Spesifik Terobosan Major Realm (Puncak $\rightarrow$ Ranah Baru)

```
MajorRealmBreakthroughChance = Clamp(BaseRateMajor(Realm) + MajorPillBonus + InsightBonus + EnvironmentBonus - ToxinPenalty - TraumaPenalty, 5%, 95%)
```

- **Syarat Mutlak Major Realm:**
  1. Qi karakter harus mencapai `100% Peak QiCap`.
  2. **WAJIB** menggunakan **Pill Breakthrough Major Realm** bersesuaian Tier (misal *Pill Terobos Kaimai* untuk Realm 1 $\rightarrow$ 2). Terobosan Major Realm tanpa Pil mengalami penalti `-40% Success Rate`.
  3. Memenuhi syarat waktu meditasi stasioner minimum (Tabel §5.1).
  4. Untuk terobosan menuju Realm 7+, wajib selamat dari Tribulasi Petir (§6).

---

## 🌩️ 6. Formula Damage & Mekanik Tribulasi Petir (Lightning Tribulation)

Penerobosan menuju Ranah 7 (*Faxiang Jing*), Ranah 8 (*Shenhuang Jing*), dan Ranah 9 (*Hunyuan Jing*) memicu Kemurkaan Langit berwujud **Tribulasi Petir (Lightning Tribulation / 雷劫)**.

### 6.1 Jumlah Sambaran Petir Tribulasi
- **Realm 6 $\rightarrow$ Realm 7 (Faxiang Jing):** 3 Sambaran Petir Spirit.
- **Realm 7 $\rightarrow$ Realm 8 (Shenhuang Jing):** 6 Sambaran Petir Divinitas.
- **Realm 8 $\rightarrow$ Realm 9 (Hunyuan Jing):** 9 Sambaran Petir Primordial.

### 6.2 Formula Kerusakan Petir per Sambaran (Lightning Strike Damage)

```
StrikeDamage = (TargetMaxHP × 0.40) × StrikeIndexMultiplier × KarmaMultiplier - ActiveDefenses
```
- **StrikeIndexMultiplier:** Sambaran 1–3 (`×1.0`), Sambaran 4–6 (`×1.3`), Sambaran 7–9 (`×1.7`).
- **KarmaMultiplier:** Ditentukan oleh Keseimbangan Karma (§7).

---

## ☯️ 7. Sistem Karma: Merit vs Sin Mechanics

```
KarmaBalance = MeritPoints - SinPoints
```

### 7.1 Dampak Karma pada Tribulasi & Domain
| Status Karma | Karma Balance | KarmaMultiplier Tribulasi | Efek Tambahan di Dunia |
|---|---|---|---|
| **Puji Agung (Saintly Merit)** | Balance $\ge +100$ | **×0.75 (-25% Damage)** | Dihormati NPC Ortodoks, +15% Evasion terhadap serangan iblis |
| **Kebajikan (Positive)** | $+10 \le \text{Balance} < +100$ | **×0.90 (-10% Damage)** | Hubungan diplomatik sekte +10% |
| **Netral (Balanced)** | $-10 < \text{Balance} < +10$ | **×1.00 (Normal)** | Tanpa modifier |
| **Tercela (Sinful)** | $-100 < \text{Balance} \le -10$ | **×1.25 (+25% Damage)** | Rawan memicu Qi Deviation saat terobosan |
| **Iblis Purba (Demonic Sin)** | Balance $\le -100$ | **×1.50 (+50% Damage)** | Diburu Pasukan Kekaisaran & Sekte Ortodoks, Petir Tribulasi merah |

---

## 🛡️ 8. Checklist Validasi AI GM (WAJIB DICEK SETIAP BREAKTHROUGH)

- [ ] Teknik/Akar Spiritual yang dipakai sudah tercatat di **Spiritual Root Origin Log** karakter (Guru/Manual/Pencerahan tervalidasi, bukan deklarasi sepihak saat momen terobosan)?
- [ ] Qi reported $\ge 95\%$ dari `QiCap(realm, stage)` saat ini?
- [ ] Untuk Major Realm: Pil Terobos bersesuaian Tier sudah tercatat di inventory?
- [ ] Syarat waktu meditasi minimum (Tabel §5.1) terpenuhi dan lokasi stasioner/aman?
- [ ] Untuk Realm 7+: Tribulasi Petir telah dihitung damagenya dengan formula §6?
- [ ] Karma Balance dihitung dari log aksi tervalidasi?

Jika salah satu poin gagal $\rightarrow$ breakthrough **DITOLAK**, sistem memberi alasan spesifik ke pemain.

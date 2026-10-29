# 🌾 Xuantian World — Sistem Pertanian & Berkebun Obat Spirit

> **Modul:** 15 — Spiritual Herb Farming System
> **Prinsip:** Anti-Cheat Enforced — Soil Grade & Growth Formula — Verified Item Origin Logging
> **Rujukan silang:** `00_CORE_RULES_AI_GM.md` (aturan wajib GM), `02_SHENMU_ZHOU.md` (wilayah kebun obat utama), `13_SPIRITUAL_ROOT_SYSTEM.md` (Akar Spiritual Kayu Abadi), `14_CRAFTING_AND_PROFESSIONS_SYSTEM.md` (profesi & alkimia), `18_ECONOMY_SYSTEM.md` (harga bahan & Item Origin Log), `32_PERGURUAN_BERKEBUN_BIYANG.md` (perguruan berkebun), `50_SPECIAL_ITEMS.md` (Dunia Kecil Gantungan Giok)

---

## 0. Filosofi Sistem Berkebun Obat Spirit

Sistem berkebun memungkinkan kultivator menanam, merawat, dan memanen benih herbal spirit untuk digunakan sendiri dalam Alkimia atau dijual ke pasar obat. Keberhasilan dan waktu tumbuh tanaman obat spirit tunduk pada formula matematis tetap.

### Aturan Emas Anti-Cheat Berkebun Spirit
- **Waktu Tumbuh Nyata In-Game:** Tanaman obat tidak tumbuh secara instan. AI GM WAJIB menghitung waktu tumbuh berdasarkan formula dan melacak akumulasi waktu in-game.
- **Wajib Item Origin Log:** Setiap panen herbal spirit Tier 3+ WAJIB mencatat **Item Origin Log** (penanam, grade tanah, lokasi, timestamp).
- **Hasil Panen Terikat Formula:** Jumlah panen dan kualitas hasil dipengaruhi langsung oleh grade tanah, pupuk Qi, level skill herbalis, dan Akar Spiritual Kayu Abadi.

---

## 1. Grade Tanah Spirit & Formula Waktu Tumbuh (Growth Time Calculation)

Waktu tumbuh tanaman obat spirit dihitung berdasarkan waktu standar benih dikurangi bonus grade tanah, pupuk Qi, dan Akar Spiritual Kayu Abadi:

```
BaseGrowthDays = SeedStandardGrowthDays
SoilMultiplier = Grade 1 (1.0) | Grade 2 (0.75) | Grade 3 (0.50) | Grade 4 (0.25)
FertilizerDiscount = 0.30 (jika menggunakan Pupuk Qi Kayu) | 0.00 (tanpa pupuk)
WoodRootBonus = 0.30 (jika kultivator memiliki Akar Spiritual Kayu Abadi) | 0.00
ActualGrowthDays = Max(1, BaseGrowthDays × SoilMultiplier × (1.0 - FertilizerDiscount - WoodRootBonus))
```

*Contoh Perhitungan:* Benih Lotus Es Abadi (Base: 14 hari) ditanam di Tanah Spirit Grade 3 (`SoilMultiplier = 0.50`) dengan Pupuk Qi (`0.30`) oleh kultivator ber-Akar Spiritual Kayu (`0.30`):
$$\text{ActualGrowthDays} = 14 \times 0.50 \times (1.0 - 0.30 - 0.30) = 7 \times 0.40 = 2.8 \text{ Hari (dibulatkan 3 Hari)}.$$

---

## 2. Formula Hasil Panen & Kualitas Herbal (Crop Yield & Quality)

```
HarvestYield = BaseYield (2–5 buah) × SoilYieldMultiplier × (1 + HerbalistSkillLevel × 0.10)
```

- **SoilYieldMultiplier:** Grade 1 (`1.0x`), Grade 2 (`1.3x`), Grade 3 (`1.6x`), Grade 4 (`2.0x`).
- **Peluang Panen Grade High (Perfect Herb):** `10% + (HerbalistSkillLevel × 5%)`.

---

## 3. Perguruan & Lokasi Utama Berkebun

- **Perguruan Berkebun Obat Biyang** (`32_PERGURUAN_BERKEBUN_BIYANG.md`): Pusat pelatihan analisis tanah spirit dan pupuk Qi.
- **Shenmu Zhou** (`02_SHENMU_ZHOU.md`): Wilayah utama kebun obat dengan bonus Wood Qi Modifier 1.25x.
- **Dunia Kecil Gantungan Giok Alam Hunyuan** (`50_SPECIAL_ITEMS.md`): Tanah Spirit Grade 9 khusus yang dapat menumbuhkan tanaman obat Tier tinggi dalam waktu **3 sampai 7 hari** tanpa bantuan pupuk/alat bantu lain.

---

## 4. Katalog Material Kustom & Resep Pertanian

### 4.1 Material & Resep Hutan Bambu Giok
Material langka dari Hutan Bambu Giok (`02_SHENMU_ZHOU.md` §2.6):

| Nama Material / Resep | Jenis Profesi / Kegunaan | Tier Bahan | Efek / Hasil Olahan |
|---|---|---|---|
| **Bambu Roh Hijau** *(Green Spirit Bamboo)* | Penempaan / Kerajinan | Tier 1–2 | Bahan baku pedang kayu spirit, tongkat formasi, dan perabotan kebun obat. |
| **Embun Giok** *(Jade Dew)* | Alkimia / Herbal | Tier 1 | Bahan pencampur ramuan pemulihan ringan (+15 HP, meredakan haus). |
| **Rumput Penjernih Qi** *(Qi Cleansing Grass)* | Alkimia / Herbal | Tier 1–2 | Bahan baku *Pil Penjernih Qi* (Meredakan konsumsi Qi kabut -50% selama 1 jam). |
| **Serat Urat Giok** *(Jade Vein Fiber)* | Jimat / Formasi | Tier 3–4 | Bahan baku benang piringan formasi dan kertas jimat pelindung jiwa. |
| **Pecahan Pedang Giok** *(Jade Sword Shard)* | Penempaan / Niat Pedang | Tier 4–5 | Bahan campuran peleburan zirah giok dan penelitian inskripsi pedang kuno. |
| **Benih Leluhur Giok** *(Ancestral Jade Seed)* | Berkebun / Alkimia | Tier 6–7 | Benih purba langka untuk ditanam di Tanah Spirit Grade 4 (Menghasilkan *Buah Giok Leluhur*). |
| **Inti Roh Purba** *(Ancient Spirit Core)* | Alkimia / Penempaan | Tier 6–7 | Bahan baku utama *Pill Terobos Nadi Giok* (Breakthrough Realm 5–6) dan Artefak Jiwa. |

### 4.2 Material & Resep Ekspansi Shenmu Zhou
Material kustom dari lokasi-lokasi baru Shenmu Zhou (`02_SHENMU_ZHOU.md` §2.13–2.24):

| Nama Material / Resep | Jenis Profesi / Kegunaan | Tier Bahan | Efek / Hasil Olahan |
|---|---|---|---|
| **Akar Wangi Spiritual** *(Fragrant Root)* | Alkimia / Herbal | Tier 1–2 | Bahan racikan Pil Penenang Jiwa & pakan khusus serangga spirit. |
| **Sutra Spiritual Qingshang** *(Qingshang Spirit Silk)* | Penempaan / Kerajinan | Tier 2–3 | Bahan kain pelindung Qi ringan, jubah perjalanan tahan gesekan, dan perban herbal. |
| **Kayu Lumu Terdaftar** *(Registered Lumu Wood)* | Kerajinan / Formasi | Tier 2–3 | Bahan baku utama perkakas kebun, busur kayu spirit, dan komponen piringan formasi. |
| **Mineral Penghantar Guruh** *(Thunder Conductor Mineral)* | Penempaan / Formasi | Tier 3–4 | Komponen piringan formasi petir dan campuran leburan zirah tahan kilat. |
| **Anyaman Akar Spiritual** *(Spiritual Root Weave)* | Kerajinan Penjelajah | Tier 2–3 | Bahan baku tali panjat ber-Qi tinggi, jembatan gantung portabel, dan jaring penjinak beast. |
| **Spora Bunga Mayat** *(Corpse Flower Spores)* | Toksikologi / Alkimia | Tier 4–5 | Bahan baku racun biologis pelumpuh dan racikan obat pemurni sampel purba. |

### 4.3 Material & Resep Dataran Makam Kekaisaran
Material bersejarah dan spiritual dari Dataran Makam Kekaisaran (`03_ZHONGHUA_ZHOU.md` §2.5):

| Nama Material / Resep | Jenis Profesi / Kegunaan | Tier Bahan | Efek / Hasil Olahan |
|---|---|---|---|
| **Batu Prasasti Kuno** *(Ancient Stele Stone)* | Formasi / Penempaan | Tier 1–2 | Bahan baku penyusun piringan formasi segel dan restorasi jalan batu kekaisaran. |
| **Kayu Pinus Tua** *(Old Pine Wood)* | Kerajinan / Penempaan | Tier 1–2 | Bahan perabotan kayu spirit tahan cuaca dan tiang penyangga lorong makam. |
| **Pecahan Formasi** *(Array Shard)* | Formasi / Jimat | Tier 3–4 | Komponen penarik energi Qi untuk piringan formasi pertahanan portabel. |
| **Logam Pemakaman** *(Mausoleum Metal)* | Penempaan Besi | Tier 3–4 | Bahan campuran pembuatan zirah pengawal dan senjata pembunuh roh. |
| **Fragmen Senjata Kuno** *(Ancient Weapon Shard)* | Penempaan / Penelitian | Tier 4–5 | Bahan lebur besi tua ber-Qi tinggi untuk menempa ulang senjata bersertifikat kekaisaran. |
| **Catatan Dinasti** *(Dynasty Record Scroll)* | Penelitian / Quest | Tier 4–5 | Bahan analisis sejarah kuno yang dijual ke rumah lelang atau diserahkan ke peneliti. |
| **Inti Konstruksi** *(Construct Core)* | Formasi / Penempaan | Tier 4–5 | Inti penggerak boneka penjaga batu dan formasi otomatis makam. |
| **Segel Kekaisaran Rusak** *(Damaged Imperial Seal)* | Identifikasi / Quest | Tier 5–6 | Barang kuno bernilai tinggi untuk membuktikan klaim silsilah dinasti atau membuka rahasia segel. |

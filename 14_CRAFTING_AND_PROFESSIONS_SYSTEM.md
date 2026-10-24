# 🛠️ Xuantian World — Sistem Kerajinan, Profesi & Kerajinan Spiritual

> **Modul:** 14 — Crafting & Professions System
> **Prinsip:** Anti-Cheat Enforced — Material-Matching Tier Scaling — Verified Item Origin Logging
> **Rujukan silang:** `00_CORE_RULES_AI_GM.md` (aturan wajib GM), `13_SPIRITUAL_ROOT_SYSTEM.md` (Akar Spiritual & QiCap), `15_ECONOMY_SYSTEM.md` (harga bahan & Item Origin Log), `16_VITALITY_HUNGER_SYSTEM.md` (Pill Toxin), `18_BESTIARY.md` (bahan beast), file regional `02`–`11` (kebun obat & sumber daya)

---

## 0. Filosofi Sistem Profesi & Kerajinan

Di Xuantian World, jalan profesi (Alkemis, Penjinak Beast, Petani Obat Spirit, Master Formasi, Penempa Besi Spirit, Master Jimat, dan Pilot Kapal Terbang) bukan sekadar pendukung narasi, melainkan **fondasi ekonomi dan pilar kultivasi**. Sama seperti Qi tunduk pada `QiCap` dan harga tunduk pada `FinalBuyPrice`, seluruh produk profesi dan keberhasilan proses pembuatan item **tunduk pada formula matematis tetap**.

**AI GM WAJIB menghitung hasil pembuatan item secara adil lewat formula di bawah ini — DILARANG menerima klaim keberhasilan sepihak dari player tanpa proses perhitungan dan konsumsi bahan yang sah.**

### Aturan Emas Anti-Cheat Profesi & Kerajinan
- **Hasil Tidak Boleh Dideklarasikan Sepihak:** Player **TIDAK BISA** menyatakan "aku berhasil membuat Pill Danwen 100%" atau "senjata tempaanku langsung Grade 8" tanpa roll probabilitas AI GM dan pemenuhan syarat resep/bahan.
- **Wajib Item Origin Log:** Setiap barang bernilai profesi (Tier 3+ atau Pill Purity 70%+) WAJIB mencatat **Item Origin Log** (pembuat, lokasi pembuatan, bahan yang dipakai, timestamp). Barang tanpa origin log tidak sah digunakan untuk breakthrough atau dijual di Rumah Lelang Wanbao.
- **Prinsip Keselarasan Tier (Tier Matching):** Pembuatan item Tier X memerlukan bahan baku minimal Tier X-1 hingga Tier X. Bahan berkualitas rendah tidak bisa dipaksa untuk menghasilkan item ber-grade tinggi.
- **Risiko Kegagalan Realistis:** Kegagalan proses alkimia, penempaan, atau penjinakan beast berisiko menghancurkan bahan baku, memicu ledakan kuali (damage HP), atau serangan balik dari Spirit Beast.
- **Skala Waktu Proses In-Game:** Pembuatan item atau proses retret profesi memakan waktu in-game nyata (`00_CORE_RULES_AI_GM.md` §1.8), bukan selesai dalam hitungan sekejap tanpa jeda waktu.

---

## 🌾 1. Sistem Pertanian & Berkebun Obat Spirit (Spiritual Herb Farming)

Sistem berkebun memungkinkan kultivator menanam benih herbal spirit untuk digunakan sendiri dalam Alkimia atau dijual ke pasar obat.

### 1.1 Grade Tanah Spirit & Formula Waktu Tumbuh (Growth Time Calculation)
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

### 1.2 Formula Hasil Panen & Kualitas Herbal (Crop Yield & Quality)

```
HarvestYield = BaseYield (2–5 buah) × SoilYieldMultiplier × (1 + HerbalistSkillLevel × 0.10)
```

- **SoilYieldMultiplier:** Grade 1 (`1.0x`), Grade 2 (`1.3x`), Grade 3 (`1.6x`), Grade 4 (`2.0x`).
- **Peluang Panen Grade High (Perfect Herb):** `10% + (HerbalistSkillLevel × 5%)`.

### 1.3 Perguruan & Lokasi Utama Berkebun
- **Perguruan Berkebun Obat Biyang** (`20_PERGURUAN_BERKEBUN_BIYANG.md`): Pusat pelatihan analisis tanah spirit dan pupuk Qi.
- **Shenmu Zhou** (`02_SHENMU_ZHOU.md`): Wilayah utama kebun obat dengan bonus Wood Qi Modifier 1.25x.
- **Dunia Kecil Gantungan Giok Alam Hunyuan** (`51_SPECIAL_ITEMS.md`): Tanah Spirit Grade 9 khusus yang dapat menumbuhkan tanaman obat Tier tinggi dalam waktu **3 sampai 7 hari** tanpa bantuan pupuk/alat bantu lain.

### 1.4 Material Kustom & Resep Spesialis Hutan Bambu Giok (Jade Bamboo Sea Materials)
Material langka dari Hutan Bambu Giok (`02_SHENMU_ZHOU.md` §2.6) yang dapat diolah dalam berbagai profesi:

| Nama Material / Resep | Jenis Profesi / Kegunaan | Tier Bahan | Efek / Hasil Olahan |
|---|---|---|---|
| **Bambu Roh Hijau** *(Green Spirit Bamboo)* | Penempaan / Kerajinan | Tier 1–2 | Bahan baku pedang kayu spirit, tongkat formasi, dan perabotan kebun obat. |
| **Embun Giok** *(Jade Dew)* | Alkimia / Herbal | Tier 1 | Bahan pencampur ramuan pemulihan ringan (+15 HP, meredakan haus). |
| **Rumput Penjernih Qi** *(Qi Cleansing Grass)* | Alkimia / Herbal | Tier 1–2 | Bahan baku *Pil Penjernih Qi* (Meredakan konsumsi Qi kabut -50% selama 1 jam). |
| **Serat Urat Giok** *(Jade Vein Fiber)* | Jimat / Formasi | Tier 3–4 | Bahan baku benang piringan formasi dan kertas jimat pelindung jiwa. |
| **Pecahan Pedang Giok** *(Jade Sword Shard)* | Penempaan / Niat Pedang | Tier 4–5 | Bahan campuran peleburan zirah giok dan penelitian inskripsi pedang kuno. |
| **Benih Leluhur Giok** *(Ancestral Jade Seed)* | Berkebun / Alkimia | Tier 6–7 | Benih purba langka untuk ditanam di Tanah Spirit Grade 4 (Menghasilkan *Buah Giok Leluhur*). |
| **Inti Roh Purba** *(Ancient Spirit Core)* | Alkimia / Penempaan | Tier 6–7 | Bahan baku utama *Pill Terobos Nadi Giok* (Breakthrough Realm 5–6) dan Artefak Jiwa. |

### 1.5 Material Kustom & Resep Ekspansi Shenmu Zhou (Shenmu Zhou Expansion Materials)
Material kustom dari lokasi-lokasi baru Shenmu Zhou (`02_SHENMU_ZHOU.md` §2.13–2.24):

| Nama Material / Resep | Jenis Profesi / Kegunaan | Tier Bahan | Efek / Hasil Olahan |
|---|---|---|---|
| **Akar Wangi Spiritual** *(Fragrant Root)* | Alkimia / Herbal | Tier 1–2 | Bahan racikan Pil Penenang Jiwa & pakan khusus serangga spirit. |
| **Sutra Spiritual Qingshang** *(Qingshang Spirit Silk)* | Penempaan / Kerajinan | Tier 2–3 | Bahan kain pelindung Qi ringan, jubah perjalanan tahan gesekan, dan perban herbal. |
| **Kayu Lumu Terdaftar** *(Registered Lumu Wood)* | Kerajinan / Formasi | Tier 2–3 | Bahan baku utama perkakas kebun, busur kayu spirit, dan komponen piringan formasi. |
| **Mineral Penghantar Guruh** *(Thunder Conductor Mineral)* | Penempaan / Formasi | Tier 3–4 | Komponen piringan formasi petir dan campuran leburan zirah tahan kilat. |
| **Anyaman Akar Spiritual** *(Spiritual Root Weave)* | Kerajinan Penjelajah | Tier 2–3 | Bahan baku tali panjat ber-Qi tinggi, jembatan gantung portabel, dan jaring penjinak beast. |
| **Spora Bunga Mayat** *(Corpse Flower Spores)* | Toksikologi / Alkimia | Tier 4–5 | Bahan baku racun biologis pelumpuh dan racikan obat pemurni sampel purba. |

### 1.6 Material Kustom & Resep Dataran Makam Kekaisaran (Imperial Mausoleum Plains Materials)
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

---

## 🐾 2. Sistem Penjinakan & Pelatihan Beast (Beast Taming System)

Penjinak Beast (*Beast Tamer*) bertugas melatih, memasang jimat penjinak, dan mengikat kontrak kesetaraan dengan Spirit Beast.

### 2.1 Formula Keberhasilan Penjinakan (Taming Chance Formula)

```
BaseChance = 30%
RealmDiffBonus = (CharacterRealmIndex - BeastRealmIndex) × 10%
HPDepletionBonus = (100% - BeastCurrentHP_Percent) × 0.40
SealTierBonus = SealTier × 10%
BaitBonus = 15% (jika menggunakan Pakan Kesukaan Spirit Beast)
WildnessPenalty = BeastTier × 5%
TamingSuccessChance = Clamp(BaseChance + RealmDiffBonus + HPDepletionBonus + SealTierBonus + BaitBonus - WildnessPenalty, 5%, 95%)
```

*Contoh Perhitungan:* Kultivator Ranah *Xuantian Jing* (Realm 5) mencoba menjinakkan Beruang Spirit Kayu (Tier 3, HP tersisa 20%) menggunakan Jimat Penjinak Tier 3 (`SealTier = 3`) dan Pakan Kesukaan:
$$\text{RealmDiffBonus} = (5 - 3) \times 10\% = +20\%$$
$$\text{HPDepletionBonus} = (100\% - 20\%) \times 0.40 = +32\%$$
$$\text{TamingSuccessChance} = 30\% + 20\% + 32\% + 30\% + 15\% - 15\% = 112\% \rightarrow \text{Hardcap } 95\%.$$

### 2.2 Formula Kesetiaan & Peningkatan Status Beast (Loyalty System)

```
LoyaltyGainPerFeeding = 5 + (AlchemistPillQuality × 2)
LoyaltyLossInBattleDefeat = 15 Points
```

| Tingkat Loyalty | Status Kesetiaan | Efek Statistik Spirit Beast |
|---|---|---|
| **71 – 100** | Sangat Setia | Bonus Attack & Defense Beast **+10%** |
| **31 – 70** | Setia / Normal | Statistik Normal |
| **0 – 30** | Membangkang | 20% peluang menolak perintah bertarung / berisiko kabur |

### 2.3 Perguruan & Serikat Penjinak Beast
- **Perguruan Penjinak Beast Qingling** (`21_PERGURUAN_BEAST_QINGLING.md`): Pusat latihan komunikasi batin dan kontrak kesetaraan.
- **Serikat Penjinak Beast Xuantian** (`12_CROSS_REGION_ORGANIZATIONS.md`): Pengelola pendaftaran dan arena sertifikasi beast.

---

## 🧪 3. Sistem Alkemis & Pemurnian Pill (Alchemy System)

Alkemis meracik tanaman obat spirit dan organ beast menjadi Pill Penyembuh, Pill Pemurni, dan Pill Breakthrough.

### 3.1 Formula Kemurnian Pill (Alchemy Purity Formula)

```
BasePurity = 50%
FlameQualityBonus = Mortal (0%) | Earth Qi (10%) | Natural Flame (20%) | Heavenly Flame (35%)
CauldronGradeBonus = CauldronTier × 5%
AlchemistSkillBonus = AlchemistLevel × 3%
DifficultyPenalty = (PillTier - AlchemistTier) × 15%
FinalPurity = Clamp(BasePurity + FlameQualityBonus + CauldronGradeBonus + AlchemistSkillBonus - DifficultyPenalty, 10%, 100%)
```

### 3.2 Tabel Efek Kemurnian & Toxin Dantian

| Purity Range | Category | Multiplier Efek Pill | Akumulasi Pill Toxin Dantian |
|---|---|---|---|
| **10% – 49%** | Failed / Defective | 30% Efek | **+20% Toxin** (Memicu Dantian Membeku) |
| **50% – 69%** | Low Purity | 70% Efek | **+10% Toxin** |
| **70% – 89%** | Mid Purity | 100% Efek | **+3% Toxin** |
| **90% – 99%** | High Purity | 130% Efek | **0% Toxin (Sangat Bersih)** |
| **100%** | Perfect Pill (Danwen) | **160% Efek + Permanent Stat** | **0% Toxin (Murni Sempurna)** |

*Risiko Ledakan Kuali (Cauldron Explosion):* Jika `FinalPurity < 20%`, kuali berisiko meledak memberikan Kerusakan Api `PillTier × 50 HP` pada Alkemis.

### 3.3 Sekte & Perguruan Alkimia Utama
- **Sekte Alkimia Danhuang** (`22_DANHUANG_ALCHEMIST_SECT.md`): Penguasa resep Pill Breakthrough di Chiyan Zhou.
- **Perguruan Alkimia Es Beihan** (`29_PERGURUAN_ALKEMIA_ES_BEIHAN.md`): Spesialis ramuan es pemulih dantian retak.

---

## 🛸 4. Sistem Kapal Terbang Lintas Wilayah (Tiankong Feichuan Airship)

Master Kemudi dan Mekanik mengoperasikan armada penerbangan melayang untuk transportasi antar-wilayah.

### 4.1 Formula Kecepatan Kapal Terbang (Airship Speed)

```
BaseSpeed = Skiff (500 li/hari) | Freighter (1.000 li/hari) | Galleon (2.500 li/hari) | Battleship (4.000 li/hari)
PilotSkillBonus = PilotTier × 10%
Realm3QiDriveBonus = 100% (jika Pilot/Penumpang Realm 3+ menyuntikkan Qi Yuan)
FinalAirshipSpeed = BaseSpeed × (1.0 + PilotSkillBonus + Realm3QiDriveBonus)
```

### 4.2 Formula Konsumsi Batu Spirit (Fuel Consumption)

```
SpiritStoneCostPerHour = (AirshipTier × 2 LSS) / (1.0 + Realm3QiDriveEfficiencyBonus)
```

### 4.3 Perguruan & Serikat Airship Utama
- **Serikat Airship Tiangong** (`12_CROSS_REGION_ORGANIZATIONS.md`): Monopoli lisensi penerbangan & galangan kapal.
- **Perguruan Kemudi Udara Tiangong** (`27_PERGURUAN_KEMUDI_TIANGONG.md`): Lembaga sertifikasi pilot dan navigasi badai.

---

## 🔮 5. Sistem Formasi, Penempaan Besi Spirit & Jimat

### 5.1 Formula Barrier HP Formasi (Array Barrier Formula)

```
BarrierHP = ArrayDiscBaseHP × (1 + ArrayMasterLevel × 0.15) × EnvironmentQiMultiplier
```
* **Perguruan Formasi Tiangong** (`26_PERGURUAN_FORMASI_TIANGONG.md`): Pusat pembuatan piringan formasi portabel.

### 5.2 Formula Durability & Damage Senjata Penempa (Forging Formula)

```
WeaponDamage = BaseWeaponDamage × (1 + BlacksmithLevel × 0.08) × (1 + MetalTier × 0.10)
SoulBindingBonus = +20% Damage saat digunakan pemilik sah.
```
* **Perguruan Penempa Besi Shendu** (`24_PERGURUAN_PENEMPA_SHENDU.md`): Pusat penempaan zirah dan senjata meteorit lava.

### 5.3 Formula Success Rate Inskripsi Jimat (Talisman Crafting)

```
TalismanSuccessChance = Clamp(60% + (TalismanMasterLevel - TalismanTier) × 10% + PaperQualityBonus, 10%, 95%)
```
* **Sekte Jimat Gurun Huangsha** (`25_PERGURUAN_JIMAT_HUANGSHA.md`): Pusat pembuatan jimat pelindung dan tinta darah beast.

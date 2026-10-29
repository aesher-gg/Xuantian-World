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

## 4. Katalog Tanaman Spiritual Lintas Wilayah (Tier 1 – 9)

Katalog resmi seluruh tanaman spiritual (herbal, rumput spirit, teh spirit, bambu spirit, pohon buah spirit, dan jamur purba) yang tumbuh di 10 Wilayah Utama Xuantian World:

### 🌿 Tier 1 – Ranah Fana & Lingquan (Mortal & Foundation Plants)
| Nama Tanaman | Kategori / Jenis | Wilayah Asal | Standar Waktu Tumbuh | Utama Kegunaan / Efek | Harga Pasaran Standar |
|---|---|---|---|---|---|
| **Rumput Penjernih Qi** *(Qi Cleansing Grass)* | Rumput Spirit | Shenmu Zhou / Zhonghua Zhou | 3 Hari | Bahan ramuan pembersih konsumsi Qi kabut -50% selama 1 jam | 50 Tael Tembaga / ikat |
| **Bambu Roh Hijau** *(Green Spirit Bamboo)* | Bambu Spirit | Shenmu Zhou (Hutan Bambu Giok) | 5 Hari | Bahan perkakas kebun, pedang kayu spirit, & komponen piringan formasi Tier 1 | 1 Tael Perak / batang |
| **Akar Wangi Spiritual** *(Fragrant Root)* | Akar Herbal | Shenmu Zhou | 4 Hari | Racikan Pil Penenang Jiwa & pakan serangga spirit | 80 Tael Tembaga / akar |
| **Teh Awan Hijau** *(Green Cloud Tea)* | Daun Teh Spirit | Zhonghua Zhou | 7 Hari | Minuman seduhan pemulih Stamina +15 HP & kejernihan pikiran | 2 Tael Perak / liang |
| **Rumput Pasir Emas** *(Golden Sand Grass)* | Rumput Spirit | Xixuan Zhou | 4 Hari | Tinta jimat pelindung ringan & ramuan Tahan Panas Gurun | 1 Tael Perak / ikat |

---

### 🌿 Tier 2 – Ranah Kaimai (Meridian Awakening Plants)
| Nama Tanaman | Kategori / Jenis | Wilayah Asal | Standar Waktu Tumbuh | Utama Kegunaan / Efek | Harga Pasaran Standar |
|---|---|---|---|---|---|
| **Ginseng Nadi Merah** *(Red Vein Ginseng)* | Akar Herbal | Shenmu Zhou / Zhonghua Zhou | 10 Hari | Bahan utama *Pil Pembuka Nadi* (Bonus Breakthrough Realm 2 +10%) | 15 Tael Perak / batang |
| **Teh Embun Bintang** *(Star Dew Tea)* | Daun Teh Spirit | Canglong Zhou / Tiangong Zhou | 12 Hari | Meningkatkan kecepatan regenerasi Qi +10% selama 6 jam saat diseduh | 25 Tael Perak / liang |
| **Bunga Es Hanbing** *(Hanbing Frost Flower)* | Bunga Spirit | Beihan Zhou | 8 Hari | Bahan racikan Pil Penawar Racun Api & Pil Alkimia Es Tier 2 | 20 Tael Perak / tangkai |
| **Pohon Kayu Lumu** *(Lumu Wood Tree)* | Pohon Spirit | Shenmu Zhou | 15 Hari | Batang kayu fleksibel ber-Qi tinggi untuk perkakas & busur spirit | 5 LSS (Batu Spirit Low) / log |
| **Jamur Bayangan Kelam** *(Dark Shadow Mushroom)* | Jamur Spirit | Youming Zhou | 7 Hari | Bahan racun biologis pelumpuh saraf & Pil Penyamaran Bayangan | 18 Tael Perak / buah |

---

### 🌿 Tier 3 – Ranah Ningyuan (Qi Condensed Plants)
| Nama Tanaman | Kategori / Jenis | Wilayah Asal | Standar Waktu Tumbuh | Utama Kegunaan / Efek | Harga Pasaran Standar |
|---|---|---|---|---|---|
| **Lotus Es Abadi** *(Eternal Frost Lotus)* | Bunga Spirit | Beihan Zhou / Canghai Zhou | 20 Hari | Bahan utama *Pil Penjernih Dantian* & Pemulih Retak Dantian (+25% Purity) | 30 LSS |
| **Teh Niat Pedang Qingfeng** *(Qingfeng Sword Intent Tea)* | Daun Teh Spirit | Canglong Zhou | 25 Hari | Memberikan buff sementara *Niat Pedang Tajam* (+15% Physical Attack) | 45 LSS / liang |
| **Buah Kristal Api Lava** *(Lava Fire Crystal Fruit)* | Pohon Buah Spirit | Chiyan Zhou | 30 Hari | Bahan utama *Pil Pemurni Nyala Api* & Pakan Beast Elemen Api | 50 LSS / buah |
| **Serat Urat Giok** *(Jade Vein Fiber Bamboo)* | Bambu Spirit | Shenmu Zhou | 18 Hari | Benang piringan formasi ruang portabel & kertas jimat segel jiwa | 35 LSS / gulung |
| **Rumput Inskripsi Rune** *(Rune Inscription Grass)* | Rumput Spirit | Xixuan Zhou | 22 Hari | Tinta jimat khusus inskripsi rune pertahanan Benteng Pasir | 40 LSS / ikat |

---

## 🌿 Tier 4 – Ranah Lingyi (Spiritual Intent Plants)
| Nama Tanaman | Kategori / Jenis | Wilayah Asal | Standar Waktu Tumbuh | Utama Kegunaan / Efek | Harga Pasaran Standar |
|---|---|---|---|---|---|
| **Lingzhi Darah Sembilan Urat** *(Nine-Vein Blood Lingzhi)* | Jamur Purba | Shenmu Zhou / Zhonghua Zhou | 45 Hari | Bahan baku utama *Pil Pemulih Jiwa & Nadi* (+100% HP, memulihkan organ hancur) | 150 LSS |
| **Pohon Meteorit Merah** *(Red Meteorite Tree)* | Pohon Spirit | Chiyan Zhou | 60 Hari | Kayu tahan leburan magma untuk arsitektur kuali & piringan formasi api | 200 LSS / batang |
| **Teh Bunga Es Lautan** *(Ocean Ice Blossom Tea)* | Daun Teh Spirit | Canghai Zhou | 40 Hari | Meredakan Pill Toxin Dantian -15% & memberikan perlindungan tekanan laut dalam | 180 LSS / liang |
| **Spora Bunga Mayat** *(Corpse Flower Spores)* | Bunga Beracun | Youming Zhou | 35 Hari | Bahan racun tingkat tinggi pelumpuh Qi Yuan kultivator Realm 4 | 160 LSS / botol |
| **Bambu Petir Guruh** *(Thunder Conduit Bamboo)* | Bambu Spirit | Juejing Zhou / Tiangong Zhou | 50 Hari | Batang bambu penghantar energi petir tanah untuk Senjata & Formasi Kilat | 220 LSS / batang |

---

## 🌿 Tier 5 – Ranah Xuantian (Profound Sky Plants)
| Nama Tanaman | Kategori / Jenis | Wilayah Asal | Standar Waktu Tumbuh | Utama Kegunaan / Efek | Harga Pasaran Standar |
|---|---|---|---|---|---|
| **Ginseng Spirit 1.000 Tahun** *(1000-Year Spirit Ginseng)* | Akar Herbal Purba | Shenmu Zhou (Dataran Abu Hijau) | 90 Hari | Bahan racikan *Pil Breakthrough Xuantian* (Bonus Success Chance +20%) | 800 LSS |
| **Lotus Giok Tiga Nadi** *(Three-Vein Jade Lotus)* | Bunga Spirit Purba | Shenmu Zhou (Hutan Bambu Giok) | 75 Hari | Bahan resep *Pil Pemurni Inti Dantian* & Restorasi Akar Spiritual | 750 LSS |
| **Teh Giok Leluhur Kekaisaran** *(Imperial Ancestral Jade Tea)* | Daun Teh Spirit | Zhonghua Zhou (Taman Sembilan Naga) | 100 Hari | Menjelaskan wawasan hukum Dao, memberikan akumulasi QiCap +5% permanen | 1.200 LSS / liang |
| **Buah Batu Bintang Melayang** *(Floating Starstone Fruit)* | Pohon Buah Spirit | Tiangong Zhou | 80 Hari | Bahan inti penggerak gravitasi Kapal Terbang Kelas Galleon & Pill Levitasi | 950 LSS / buah |
| **Akar Hitam Penjernih Jiwa** *(Soul Cleansing Black Root)* | Akar Beracun Purba | Youming Zhou | 85 Hari | Menghapus kutukan jiwa & memisahkan kesadaran iblis yang merintangi Dantian | 850 LSS |

---

## 🌿 Tier 6 – Ranah Tongtian (Heaven Connecting Plants)
| Nama Tanaman | Kategori / Jenis | Wilayah Asal | Standar Waktu Tumbuh | Utama Kegunaan / Efek | Harga Pasaran Standar |
|---|---|---|---|---|---|
| **Buah Giok Leluhur** *(Ancestral Jade Fruit)* | Buah Purba | Shenmu Zhou (Sanctum Pohon Leluhur) | 150 Hari | Bahan baku utama *Pill Terobos Nadi Giok* (Breakthrough Realm 5–6) | 3.500 LSS |
| **Anggrek Jiwa Kristal Es Purba** *(Ancient Ice Crystal Orchid)* | Bunga Spirit Purba | Beihan Zhou (Danau Es Cermin Jiwa) | 120 Hari | Mencegah *Qi Deviation* tingkat berat saat penerobosan Ranah Tongtian | 3.000 LSS |
| **Bambu Bambu Pedang Naga** *(Dragon Sword Bamboo)* | Bambu Purba | Canglong Zhou | 140 Hari | Bahan lebur pedang spirit tiada tanding ber-Qi Niat Pedang Azure Dragon | 4.000 LSS / batang |
| **Teh Nirwana Api Berapi** *(Fiery Nirvana Tea)* | Daun Teh Spirit | Chiyan Zhou (Kawah Kristal Api) | 160 Hari | Memberikan kekebalan Kerusakan Api 80% selama 24 jam & memicu pembakaran Dantian murni | 4.500 LSS / liang |
| **Bunga Moko Gurun Suci** *(Sacred Desert Moko Flower)* | Bunga Purba | Xixuan Zhou | 130 Hari | Bahan utama jimat pelindung jiwa purba Grade 6 & Pil Transformasi Tubuh Emas | 3.200 LSS |

---

## 🌿 Tier 7 – Ranah Faxiang (Avatar Manifestation Plants)
| Nama Tanaman | Kategori / Jenis | Wilayah Asal | Standar Waktu Tumbuh | Utama Kegunaan / Efek | Harga Pasaran Standar |
|---|---|---|---|---|---|
| **Pohon Induk Wanling Spirit** *(Wanling Mother Tree Branch)* | Pohon Purba Mitos | Shenmu Zhou (Kerajaan Wanling) | 300 Hari | Bahan baku Artefak Jiwa Avatar & Pil Penjelmaan Avatar Dao | 15.000 LSS |
| **Buah Teratai Samudra Bintang** *(Star Ocean Lotus Fruit)* | Buah Spirit Purba | Canghai Zhou (Palung Bintang Giok) | 250 Hari | Membuka koordinat lautan jiwa & memperluas kapasitas Avatar Faxiang +30% | 12.000 LSS |
| **Teh Bintang Sembilan Naga** *(Nine Dragon Star Tea)* | Daun Teh Spirit Mitos | Zhonghua Zhou | 280 Hari | Menyuntikkan kehendak Kekaisaran Purba, meningkatkan Hit Chance Avatar +25% | 18.000 LSS / liang |
| **Jamur Retakan Ruang Purba** *(Void Crack Ancient Mushroom)* | Jamur Anomali | Juejing Zhou | 220 Hari | Bahan piringan formasi pemindah ruang antar-wilayah jarak jauh | 14.000 LSS |
| **Rumput Petir Tribulasi Es** *(Ice Tribulation Thunder Grass)* | Rumput Anomali | Beihan Zhou / Juejing Zhou | 260 Hari | Bahan peredam serangan Tribulasi Petir Es Realm 7 (-40% Damage Tribulasi) | 16.000 LSS |

---

## 🌿 Tier 8 – Ranah Shenhuang (Divine Emperor Plants)
| Nama Tanaman | Kategori / Jenis | Wilayah Asal | Standar Waktu Tumbuh | Utama Kegunaan / Efek | Harga Pasaran Standar |
|---|---|---|---|---|---|
| **Buah Domain Dewa Primordial** *(Primordial God Domain Fruit)* | Buah Legend | Shenmu Zhou / Tiangong Zhou | 500 Hari | Inti racikan *Pil Pembuka Domain Shenhuang* (Menjamin pembentukan Domain Elemen) | 80.000 LSS |
| **Kayu Pohon Shenmu Purba** *(Ancient Shenmu Core Wood)* | Kayu Legend Mitos | Shenmu Zhou (Pohon Induk Shenmu) | 600 Hari | Bahan pembuat Kuali Alkimia Grade 8 & Struktur Kapal Terbang Kelas Battleship Utama | 120.000 LSS / log |
| **Teh Abadi Hunyuan** *(Hunyuan Immortal Tea)* | Daun Teh Legend | Di Mana Saja (Sangat Langka) | 450 Hari | Menghapus seluruh akumulasi Pill Toxin Dantian menjadi 0% seketika | 90.000 LSS / liang |
| **Bunga Api Iblis Sembilan Neraka** *(Nine Hells Demon Fire Flower)* | Bunga Legend Iblis | Youming Zhou | 480 Hari | Bahan resep Pil Pembalik Takdir Iblis & Pembakar Jiwa Musuh | 75.000 LSS |
| **Lotus Bintang Laut Purba** *(Ancient Star Sea Lotus)* | Bunga Legend | Canghai Zhou | 520 Hari | Bahan pembuat *Zirah Pelindung Jiwa Bintang* (Menolak 1x serangan mati) | 85.000 LSS |

---

## 🌿 Tier 9 – Ranah Hunyuan & Fei Sheng (Immortal / Ascendant Plants)
| Nama Tanaman | Kategori / Jenis | Wilayah Asal | Standar Waktu Tumbuh | Utama Kegunaan / Efek | Harga Pasaran Standar |
|---|---|---|---|---|---|
| **Buah Dewa Hunyuan Purba** *(Primordial Hunyuan Divine Fruit)* | Buah Mitos Tertinggi | Shenmu Zhou (Sanctum Pohon Induk) | 1.000 Hari | Bahan resep utama *Pil Kenaikan Abadi (Fei Sheng Dan)* — Peluang lolos Tribulasi +50% | 500.000 LSS (Hanya Lelang) |
| **Teh Dao Abadi Primordial** *(Primordial Immortal Dao Tea)* | Daun Teh Mitos | Dunia Kecil Gantungan Giok / Shenmu | 800 Hari | Menyatu penuh dengan kehendak Dewa Primordial Hunyuan, memicu pemahaman Dao Mutlak | 350.000 LSS / liang |
| **Pohon Bintang Teratai Langit** *(Celestial Lotus Star Tree)* | Pohon Mitos | Tiangong Zhou / Juejing Zhou | 1.200 Hari | Bahan konstruksi Artefak Kayu Grade 9 & Istana Melayang Abadi | 600.000 LSS |
| **Rebung Bambu Purba Hunyuan** *(Hunyuan Ancient Bamboo Shoot)* | Bambu Mitos | Shenmu Zhou (Hutan Bambu Giok Layer III) | 900 Hari | Menembus batas Dantian, memberikan QiCap tambahan +10.000.000 permanen | 400.000 LSS |
| **Ginseng Keabadian Jiwa Purba** *(Immortal Soul Ancient Ginseng)* | Akar Mitos | Zhonghua Zhou / Shenmu Zhou | 1.500 Hari | Menghidupkan kembali kultivator yang telah gugur fisik (selama Jiwa Abadi belum hancur) | 750.000 LSS |

---

## 5. Material Kustom & Resep Spesialis Pertanian Regional

### 5.1 Material & Resep Hutan Bambu Giok
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

### 5.2 Material & Resep Ekspansi Shenmu Zhou
Material kustom dari lokasi-lokasi baru Shenmu Zhou (`02_SHENMU_ZHOU.md` §2.13–2.24):

| Nama Material / Resep | Jenis Profesi / Kegunaan | Tier Bahan | Efek / Hasil Olahan |
|---|---|---|---|
| **Akar Wangi Spiritual** *(Fragrant Root)* | Alkimia / Herbal | Tier 1–2 | Bahan racikan Pil Penenang Jiwa & pakan khusus serangga spirit. |
| **Sutra Spiritual Qingshang** *(Qingshang Spirit Silk)* | Penempaan / Kerajinan | Tier 2–3 | Bahan kain pelindung Qi ringan, jubah perjalanan tahan gesekan, dan perban herbal. |
| **Kayu Lumu Terdaftar** *(Registered Lumu Wood)* | Kerajinan / Formasi | Tier 2–3 | Bahan baku utama perkakas kebun, busur kayu spirit, dan komponen piringan formasi. |
| **Mineral Penghantar Guruh** *(Thunder Conductor Mineral)* | Penempaan / Formasi | Tier 3–4 | Komponen piringan formasi petir dan campuran leburan zirah tahan kilat. |
| **Anyaman Akar Spiritual** *(Spiritual Root Weave)* | Kerajinan Penjelajah | Tier 2–3 | Bahan baku tali panjat ber-Qi tinggi, jembatan gantung portabel, dan jaring penjinak beast. |
| **Spora Bunga Mayat** *(Corpse Flower Spores)* | Toksikologi / Alkimia | Tier 4–5 | Bahan baku racun biologis pelumpuh dan racikan obat pemurni sampel purba. |

### 5.3 Material & Resep Dataran Makam Kekaisaran
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

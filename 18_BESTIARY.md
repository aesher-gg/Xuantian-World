# 🦁 Xuantian World — Bestiarium & Spirit Beast 10 Wilayah

> **Modul:** 18 — Bestiary
> **Prinsip:** Anti-Cheat Enforced — Ecosystem Danger Scaling — Verified Loot Logging
> **Rujukan:** `00_CORE_RULES_AI_GM.md` (aturan GM), `14_CRAFTING_AND_PROFESSIONS_SYSTEM.md` (profesi & bahan), `15_ECONOMY_SYSTEM.md` (harga & origin log), `17_COMBAT_SYSTEM.md` (combat stats), `INDEX.md`

---

## 0. Filosofi Sistem Bestiarium

Spirit Beast dan monster di Xuantian World bukan sekadar target buruan pasif — mereka adalah entitas hidup yang mengisi ekosistem 10 Wilayah Utama. Kemunculan monster di perjalanan (*Ambush / Encounter*) dihitung otomatis oleh AI GM berdasarkan tingkat bahaya wilayah dan waktu perjalanan in-game.

### Aturan Emas Anti-Cheat Bestiarium
- Kemunculan monster dan serangan mendadak (*Ambush*) TIDAK PERNAH dideklarasikan sepihak oleh player — dihitung AI GM berdasarkan Danger Modifier wilayah dan waktu perjalanan.
- Player **TIDAK BISA** menentukan sendiri jenis loot yang didapatkan dari monster — AI GM melempar peluang drop item berdasarkan formula resmi *setelah* monster benar-benar dikalahkan.
- Setiap loot bernilai yang didapatkan dari pemburuan Spirit Beast WAJIB dicatat di **Item Origin Log** (`15_ECONOMY_SYSTEM.md`) sebelum dapat dijual, ditempa, atau digunakan untuk breakthrough.
- Monster bertindak sesuai Karakteristik, Taktik, dan Insting wilayahnya — AI GM bertindak sebagai pengendali monster secara realistis dan adil.

---

## 1. Klasifikasi Tier Spirit Beast & Tingkat Bahaya

Spirit Beast di Xuantian World diklasifikasikan ke dalam 9 Tier yang setara dengan 9 Ranah Kultivasi:

| Tier Beast | Setara Ranah Kultivasi | Tingkat Penjinakan | Karakteristik & Habitat Utama |
|---|---|---|---|
| **Tier 1 (Unggas/Binatang Spirit Muda)** | Lingquan Jing | Sangat Mudah | Unggas Hutan, Kelinci Spirit, Serigala Angin Muda |
| **Tier 2 (Beast Hutan Terlatih)** | Kaimai Jing | Mudah | Harimau Taring Besi, Ular Hijau Kayu, Bangau Zamrud |
| **Tier 3 (Beast Spirit Elit)** | Ningyuan Jing | Sedang | Serigala Salju Es, Beruang Spirit Kayu, Elang Badai |
| **Tier 4 (Raja Beast Regional)** | Lingyi Jing | Sulit | Naga Laut Bersisik Giok, Serpent Sembilan Kepiting |
| **Tier 5 (Beast Kuno Berkesadaran)** | Xuantian Jing | Sangat Sulit | Burung Feniks Api Chiyan, Kura-kura Batu Purba |
| **Tier 6 (Bentuk Bencana Alam)** | Tongtian Jing | Ekstrem | Naga Terbang Langit Tiangong, Serpent Retakan Ruang |
| **Tier 7–9 (Beast Mythical Purba)** | Faxiang Jing ke atas | Mitos / Kuno | Rajawali Purba Hunyuan, Qilin Kayu Shenmu Purba |

---

## 2. Formula & Penentuan Sistem Drop Loot

Drop item dievaluasi oleh AI GM **setelah** pertempuran selesai. Perhitungan peluang mendapatkan item loot mengikuti formula standar Xuantian World di bawah ini:

$$\text{PeluangDrop(Item)} = \text{BaseRate(Rarity)} \times \text{TierModifier(TierBeast)} - (\text{KerusakanJasad} \times 10\%)$$

### Tabel Rarity & Base Drop Rate Item

| Rarity Item | Base Drop Rate | Contoh Jenis Item |
|---|---|---|
| **Umum (Common)** | 70% – 90% | Daging spirit, bulu, kulit, taring biasa, cangkang |
| **Jarang (Rare)** | 30% – 50% | Inti Spirit Beast (Tier 1–3), empedu, kelenjar racun |
| **Langka (Epic)** | 10% – 25% | Sisik naga, darah murni spirit, Inti Beast (Tier 4–6) |
| **Legendaris (Mythic)** | 1% – 5% | Inti Beast Purba (Tier 7–9), Kristal Ruang Purba, Mutiara Hunyuan |

### Tabel Modifier Tier Beast
* **Tier 1 – 3:** $\text{TierModifier} = 1.0$ (Sangat stabil)
* **Tier 4 – 6:** $\text{TierModifier} = 0.85$ (Bahan lebih langka & terkonsentrasi)
* **Tier 7 – 9:** $\text{TierModifier} = 0.70$ (Item kelas Mythical, sangat langka)

---

## 3. Spirit Beast Lintas Wilayah (Cross-Region Beasts)

Beast lintas wilayah adalah entitas spiritual yang dapat ditemukan mengembara di perbatasan, jalur perdagangan kapal terbang, maupun di seluruh 10 Wilayah Utama.

| Nama Beast | Jenis / Kategori | Tier | Loot |
|---|---|---|---|
| Burung Merpati Pos Spirit | Unggas Udara | Tier 1 | Bulu Merpati Spirit (85% (Umum))<br>Daging Spirit (75% (Umum)) |
| Kuda Spirit Langkah Cepat | Mamalia Darat | Tier 2 | Kulit Kuda Spirit (80% (Umum))<br>Inti Qi Muda (35% (Jarang)) |
| Rajawali Badai Langit | Unggas Udara | Tier 3 | Sayap Besi Spirit (75% (Umum))<br>Inti Beast Tier 3 (30% (Jarang)) |
| Paus Udara Melayang | Aquatic / Aerial | Tier 4 | Kulit Paus Udara (70% (Umum))<br>Inti Air-Ruang Tier 4 (20% (Langka)) |
| Serpent Raksasa Retakan Ruang | Anomali Purba | Tier 6 | Kristal Ruang Purba (60% (Umum))<br>Darah Beast Purba (15% (Langka))<br>Inti Ruang Tier 6 (5% (Legendaris)) |
| Rajawali Purba Hunyuan | Beast Mythical | Tier 9 | Bulu Suci Langit (50% (Umum))<br>Inti Rajawali Hunyuan (2% (Legendaris)) |

---

## 4. Katalog Spirit Beast 10 Wilayah Utama

---

### 4.1 🌿 Shenmu Zhou (Kayu & Hutan Purba)

| Nama Beast | Jenis / Kategori | Tier | Loot |
|---|---|---|---|
| Kelinci Spirit Daun Hijau | Mamalia Kecil | Tier 1 | Bulu Kelinci Spirit (85% (Umum))<br>Daging Spirit (75% (Umum)) |
| Ulat Sutra Spiritual | Serangga Spirit | Tier 1 | Benang Sutra Spirit (85% (Umum))<br>Kepompong Spirit (40% (Jarang)) |
| Kelinci Giok Roh | Mamalia Spirit | Tier 1 | Bulu Kelinci Giok (85% (Umum))<br>Daging Spirit (75% (Umum)) |
| Unggas Hutan Shenmu | Unggas Hutan | Tier 1 | Bulu Unggas Spirit (80% (Umum))<br>Telur Spirit (40% (Jarang)) |
| Bangau Bulu Zamrud | Unggas Udara | Tier 2 | Bulu Zamrud (80% (Umum))<br>Inti Kayu Tier 2 (35% (Jarang)) |
| Ular Hijau Sulur Kayu | Reptil Kayu | Tier 2 | Kulit Ular Kayu (75% (Umum))<br>Bisa Kayu Ringan (35% (Jarang)) |
| Cacing Spiritual Akar Merah | Annelida Spirit | Tier 2 | Lendir Akar Merah (75% (Umum))<br>Inti Tier 2 (35% (Jarang)) |
| Ular Bambu Bercorak | Reptil Bambu | Tier 2 | Bisa Ular Bambu (75% (Umum))<br>Kantung Racun Bambu (35% (Jarang))<br>Kulit Ular (35% (Jarang)) |
| Kera Batu Hijau | Primata Hutan | Tier 2 | Batu Mineral Giok (75% (Umum))<br>Inti Tier 2 (35% (Jarang)) |
| Babi Hutan Taring Bambu | Mamalia Darat | Tier 2 | Taring Bambu (80% (Umum))<br>Daging Spirit (75% (Umum)) |
| Serigala Angin Shenmu | Predator Darat | Tier 2 | Taring Serigala Spirit (75% (Umum))<br>Inti Tier 2 (30% (Jarang)) |
| Beruang Spirit Elemen Kayu | Spirit Beast / Tank | Tier 3 | Kulit Tebal (75% (Umum))<br>Empedu Beruang Spirit (35% (Jarang))<br>Inti Kayu Tier 3 (30% (Jarang)) |
| Rusa Tanduk Kristal Spirit | Herbivora Spirit | Tier 3 | Tanduk Kristal Spirit (70% (Umum))<br>Darah Spirit Murni (30% (Jarang)) |
| Rusa Kabut Giok | Herbivora Spirit | Tier 3 | Tanduk Obat Giok (70% (Umum))<br>Darah Spirit Murni (30% (Jarang)) |
| Kera Pembawa Benih Obat | Primata Spirit | Tier 3 | Benih Obat Spirit Random (75% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Serigala Giok Berkabut | Predator Kabut | Tier 3 | Bulu Serigala Giok (75% (Umum))<br>Inti Kayu Tier 3 (30% (Jarang)) |
| Belalang Pedang Bambu | Serangga Penyerang | Tier 3 | Sayap Bilah Bambu (75% (Umum))<br>Cakar Pedang (35% (Jarang)) |
| Kura-kura Tempurung Lumut Purba | Reptil Air/Darat | Tier 4 | Tempurung Batu Kayu (70% (Umum))<br>Inti Kayu Tier 4 (20% (Langka)) |
| Laba-laba Sulur Pelumpuh | Serangga Spirit | Tier 4 | Sutra Pelumpuh Spirit (65% (Umum))<br>Bisa Laba-laba (20% (Langka)) |
| Laba-laba Urat Giok | Serangga Lorong | Tier 4 | Sutra Urat Giok (65% (Umum))<br>Inti Kayu Tier 4 (20% (Langka)) |
| Beruang Roh Bambu Hitam | Tank / Beast Elit | Tier 4 | Kulit Bambu Hitam (70% (Umum))<br>Empedu Beruang (20% (Langka))<br>Inti Tier 4 (18% (Langka)) |
| Elang Hijau Pelindung Kanopi | Unggas Udara | Tier 4 | Bulu Sayap Angin (65% (Umum))<br>Inti Tier 4 (18% (Langka)) |
| Harimau Dahan Shenmu | Predator Elit | Tier 5 | Taring Harimau Spirit (60% (Umum))<br>Inti Kayu Tier 5 (15% (Langka)) |
| Ular Sulur Sembilan Daun | Reptil Purba | Tier 5 | Sisik Sembilan Daun (60% (Umum))<br>Bisa Racun Shenmu (12% (Langka)) |
| Bunga Mayat Leluhur | Tumbuhan Purba / Boss | Tier 5 | Spora Bunga Mayat (60% (Umum))<br>Akar Purba Beracun (12% (Langka)) |
| Roh Bambu Tanpa Nama | Entitas Spiritual | Tier 5 | Esensi Jiwa Bambu (60% (Umum))<br>Inti Tier 5 (15% (Langka)) |
| Penjaga Leluhur Berakar | Boss Elit / Guardian | Tier 5 | Kayu Akar Purba (60% (Umum))<br>Inti Tier 5 (12% (Langka)) |
| Gajah Akar Kayu Purba | Beast Raksasa | Tier 6 | Gading Kayu Purba (55% (Umum))<br>Inti Tier 6 (10% (Langka)) |
| Ular Naga Giok Purba | Beast Penguasa | Tier 6 | Sisik Naga Giok (55% (Umum))<br>Inti Naga Kayu Tier 6 (10% (Langka)) |
| Kura-kura Segel Gunung | Penjaga Kuno | Tier 6 | Tempurung Segel Giok (55% (Umum))<br>Inti Tier 6 (8% (Langka)) |
| Kelinci Bulan Shenmu | Beast Spirit Suci | Tier 6 | Bulu Bulan Spirit (55% (Umum))<br>Darah Suci Kayu (8% (Langka)) |
| Merak Bulu Pelangi Spirit | Unggas Spirit | Tier 7 | Bulu Pelangi Shenmu (50% (Umum))<br>Inti Tier 7 (4% (Legendaris)) |
| Trenggiling Pelindung Akar | Beast Pertahanan | Tier 7 | Sisik Pelindung Akar (50% (Umum))<br>Inti Tier 7 (3% (Legendaris)) |
| Naga Kayu Hijau Purba | Naga Purba | Tier 8 | Sisik Naga Kayu (45% (Umum))<br>Inti Naga Tier 8 (2% (Legendaris)) |
| Feniks Kayu Penyeimbang Alam | Feniks Spirit | Tier 8 | Bulu Abadi Feniks (40% (Umum))<br>Darah Feniks Kayu (2% (Legendaris)) |
| Qilin Kayu Shenmu Purba | Mythical Guardian | Tier 9 | Tanduk Qilin Purba (40% (Umum))<br>Darah Hunyuan (1% (Legendaris))<br>Inti Qilin Tier 9 (1% (Legendaris)) |

---

### 4.2 🏰 Zhonghua Zhou (Dataran Tengah & Kekaisaran)

| Nama Beast | Jenis / Kategori | Tier | Loot |
|---|---|---|---|
| Anjing Penjaga Halaman Spirit | Mamalia Kecil | Tier 1 | Kulit Anjing Spirit (85% (Umum)) |
| Gagak Batu | Unggas Spiritual | Tier 1 | Bulu Gagak Batu (85% (Umum))<br>Cakar Spirit (75% (Umum)) |
| Babi Hutan Taring Besi | Mamalia Darat | Tier 2 | Taring Besi (80% (Umum))<br>Daging Spirit (75% (Umum)) |
| Roh Prajurit Gugur | Undead / Spirit | Tier 2 | Serpihan Baju Zirah Kuno (75% (Umum))<br>Kristal Jiwa Tier 2 (35% (Jarang)) |
| Boneka Penjaga Rusak | Konstruksi Spiritual | Tier 2 | Pecahan Inti Konstruksi (75% (Umum))<br>Komponen Mekanis (35% (Jarang)) |
| Macan Besi Pegunungan | Predator Darat | Tier 3 | Kulit Macan Besi (75% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Ular Danau Leluhur | Reptil Danau | Tier 3 | Sisik Ular Danau (75% (Umum))<br>Empedu Ular (35% (Jarang)) |
| Elang Pengawal Bukit | Unggas Udara | Tier 3 | Bulu Elang Spirit (70% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Serigala Karang Sungai | Predator Air/Darat | Tier 3 | Taring Serigala Sungai (70% (Umum))<br>Kulit Serigala (35% (Jarang)) |
| Naga Sungai Longjiang | Aquatic Dragon | Tier 4 | Sisik Naga Sungai (65% (Umum))<br>Inti Air Tier 4 (20% (Langka)) |
| Prajurit Boneka Kekaisaran | Konstruksi Spiritual | Tier 4 | Inti Konstruksi Tier 4 (65% (Umum))<br>Pecahan Zirah Batu (18% (Langka)) |
| Pengawal Batu | Konstruksi Spiritual | Tier 4 | Batu Formasi Makam (65% (Umum))<br>Komponen Mekanis (18% (Langka)) |
| Banteng Tanduk Perunggu | Beast Raga Besi | Tier 4 | Tanduk Perunggu Spirit (65% (Umum))<br>Inti Tier 4 (18% (Langka)) |
| Beruang Pelindung Lembah | Tank / Elit | Tier 4 | Empedu Beruang (65% (Umum))<br>Inti Tier 4 (18% (Langka)) |
| Singa Bintang Kekaisaran | Spirit Beast Elit | Tier 5 | Surai Singa Bintang (60% (Umum))<br>Inti Tier 5 (15% (Langka)) |
| Ular Emas Pelindung Makam | Reptil Purba | Tier 5 | Sisik Emas Purba (60% (Umum))<br>Inti Tier 5 (12% (Langka)) |
| Roh Pelayan Makam | Roh Spiritual | Tier 5 | Fragmen Memori Kuno (60% (Umum))<br>Kristal Jiwa Tier 5 (15% (Langka)) |
| Penjaga Segel Tanpa Nama | Entitas Penjaga | Tier 5 | Batu Segel Kekaisaran (60% (Umum))<br>Inti Tier 5 (12% (Langka)) |
| Kuda Sembrani Langit | Beast Terbang | Tier 6 | Sayap Sembrani Spirit (55% (Umum))<br>Inti Tier 6 (10% (Langka)) |
| Bao-Penguasa Bukit Bintang | Predator Mitos | Tier 6 | Kulit Totem Bao (55% (Umum))<br>Inti Tier 6 (8% (Langka)) |
| Naga Emas Pelindung Dinasti | Imperial Dragon | Tier 7 | Sisik Naga Emas (50% (Umum))<br>Inti Tier 7 (4% (Legendaris)) |
| Burung Hong Kekaisaran | Unggas Suci | Tier 7 | Bulu Hong Suci (50% (Umum))<br>Darah Spirit Hong (3% (Legendaris)) |
| Kura-kura Bintang Sembilan Naga | Guardian Purba | Tier 8 | Tempurung Bintang Purba (45% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Qilin Mas Kekaisaran | Mythical Beast | Tier 8 | Tanduk Qilin Emas (40% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Naga Bintang Hunyuan Kekaisaran | Primordial Dragon | Tier 9 | Sisik Bintang Hunyuan (40% (Umum))<br>Inti Naga Bintang Tier 9 (1% (Legendaris)) |

---

### 4.3 🐉 Canglong Zhou (Pegunungan Pedang & Wind/Metal Qi)

| Nama Beast | Jenis / Kategori | Tier | Loot |
|---|---|---|---|
| Tupai Angin Puncak | Mamalia Kecil | Tier 1 | Bulu Tupai Spirit (85% (Umum)) |
| Kambing Tebing Taring Besi | Herbivora Tebing | Tier 1 | Tanduk Kambing Besi (80% (Umum)) |
| Elang Angin Taring Besi | Unggas Udara | Tier 2 | Bulu Besi Spirit (80% (Umum))<br>Inti Angin Tier 2 (35% (Jarang)) |
| Monyet Pedang Tebing | Primata Tebing | Tier 2 | Cakar Monyet Tebing (75% (Umum))<br>Inti Tier 2 (35% (Jarang)) |
| Macan Tutul Petir Pegunungan | Predator Kilat | Tier 3 | Kulit Macan Tutul Petir (75% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Serigala Taring Logam | Predator Besi | Tier 3 | Taring Logam Spirit (70% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Naga Spirit Sisik Perak | Naga Pegunungan | Tier 4 | Sisik Perak Spirit (65% (Umum))<br>Inti Naga Tier 4 (20% (Langka)) |
| Gryphon Angin Puncak | Flying Beast | Tier 4 | Sayap Gryphon Spirit (65% (Umum))<br>Inti Tier 4 (18% (Langka)) |
| Ular Taring Pedang | Reptil Tajam | Tier 4 | Taring Pedang Spirit (65% (Umum))<br>Bisa Ular (18% (Langka)) |
| Elang Badai Logam | Unggas Badai | Tier 5 | Bulu Badai Besi (60% (Umum))<br>Inti Tier 5 (15% (Langka)) |
| Singa Taring Pedang Canglong | Predator Elit | Tier 5 | Surai Taring Pedang (60% (Umum))<br>Inti Tier 5 (12% (Langka)) |
| Beruang Besi Pembelah Batu | Tank Beast | Tier 6 | Cakar Besi Beruang (55% (Umum))<br>Inti Tier 6 (10% (Langka)) |
| Naga Angin Canglong Purba | Naga Wind-Qi | Tier 6 | Sisik Naga Angin (55% (Umum))<br>Inti Tier 6 (8% (Langka)) |
| Rajawali Pedang Bintang | Unggas Pedang | Tier 7 | Bulu Pedang Bintang (50% (Umum))<br>Inti Tier 7 (4% (Legendaris)) |
| Harimau Taring Naga Perak | Beast Elit Perak | Tier 7 | Taring Naga Perak (50% (Umum))<br>Inti Tier 7 (3% (Legendaris)) |
| Naga Terbang Pedang Canglong | Naga Udara | Tier 8 | Sayap Naga Pedang (45% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Burung Feniks Angin Perak | Feniks Angin | Tier 8 | Bulu Feniks Perak (40% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Naga Purba Canglong Sword-Intent | Ancient Sword Dragon | Tier 9 | Kristal Sword-Intent Purba (40% (Umum))<br>Inti Naga Canglong Tier 9 (1% (Legendaris)) |

---

### 4.4 🌋 Chiyan Zhou (Api & Lava)

| Nama Beast | Jenis / Kategori | Tier | Loot |
|---|---|---|---|
| Tikus Api Kawah | Mamalia Kecil | Tier 1 | Bulu Tahan Api (85% (Umum)) |
| Kadal Batu Panas | Reptil Panas | Tier 1 | Sisik Batu Panas (80% (Umum)) |
| Kadal Lava Berlapis Besi | Reptil Lava | Tier 2 | Kulit Tahan Api (80% (Umum))<br>Inti Api Tier 2 (35% (Jarang)) |
| Ular Api Merah | Reptil Beracun | Tier 2 | Bisa Api (75% (Umum))<br>Kulit Ular Api (35% (Jarang)) |
| Kalajengking Abu Vulkanik | Serangga Abu | Tier 3 | Sengat Kalajengking Abu (75% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Serigala Api Neraka | Predator Api | Tier 3 | Bulu Api Neraka (70% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Salamander Api Purba | Amfibi Lava | Tier 4 | Kulit Salamander Api (65% (Umum))<br>Inti Tier 4 (20% (Langka)) |
| Banteng Lava Taring Merah | Beast Lava | Tier 4 | Tanduk Lava Spirit (65% (Umum))<br>Inti Tier 4 (18% (Langka)) |
| Burung Feniks Api Chiyan | Feniks Api | Tier 5 | Bulu Feniks Chiyan (60% (Umum))<br>Inti Api Tier 5 (15% (Langka)) |
| Kera Api Kawah Shendu | Primata Api | Tier 5 | Taring Kera Api (60% (Umum))<br>Inti Tier 5 (12% (Langka)) |
| Naga Lava Sisik Merah | Naga Lava | Tier 6 | Sisik Naga Lava (55% (Umum))<br>Inti Tier 6 (10% (Langka)) |
| Golem Lava Kawah | Elemental Lava | Tier 6 | Batu Meteorit Api (55% (Umum))<br>Kristal Inti Lava (8% (Langka)) |
| Singa Api Chiyan Purba | Beast Api Purba | Tier 7 | Surai Api Chiyan (50% (Umum))<br>Inti Tier 7 (4% (Legendaris)) |
| Ular Berkepala Tiga Api Lava | Reptil Tiga Warna | Tier 7 | Sisik Api Tiga Warna (50% (Umum))<br>Inti Tier 7 (3% (Legendaris)) |
| Naga Api Bintang Chiyan | Naga Bintang Api | Tier 8 | Sisik Naga Bintang Api (45% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Feniks Api Abadi Lava | Feniks Lava Purba | Tier 8 | Bulu Abadi Chiyan (40% (Umum))<br>Darah Feniks Api (2% (Legendaris)) |
| Naga Purba Jantung Bintang Api | Primordial Fire Dragon | Tier 9 | Kristal Api Purba Hunyuan (40% (Umum))<br>Inti Bintang Api Tier 9 (1% (Legendaris)) |

---

### 4.5 🌊 Canghai Zhou (Lautan & Kepulauan)

| Nama Beast | Jenis / Kategori | Tier | Loot |
|---|---|---|---|
| Ikan Terbang Spirit | Ikan Terbang | Tier 1 | Sisik Ikan Spirit (85% (Umum)) |
| Kepiting Cangkang Batu | Krustasea | Tier 1 | Cangkang Batu Spirit (80% (Umum)) |
| Siput Mutiara Spirit | Moluska Laut | Tier 2 | Cangkang Siput (80% (Umum))<br>Mutiara Spirit Low-Grade (35% (Jarang)) |
| Ular Laut Sisik Hijau | Reptil Laut | Tier 2 | Sisik Hijau (75% (Umum))<br>Bisa Ular Laut (35% (Jarang)) |
| Hiu Bersisik Perak | Predator Laut | Tier 3 | Taring Hiu Spirit (75% (Umum))<br>Sisik Perak (35% (Jarang))<br>Inti Tier 3 (30% (Jarang)) |
| Gurita Gurita Rawa Laut | Moluska Tentakel | Tier 3 | Tentakel Gurita Spirit (70% (Umum))<br>Tinta Hitam Laut (30% (Jarang)) |
| Naga Laut Bersisik Giok | Naga Laut | Tier 4 | Sisik Giok Laut (65% (Umum))<br>Inti Naga Air Tier 4 (20% (Langka)) |
| Paus Spirit Samudra | Beast Raksasa Laut | Tier 4 | Minyak Paus Spirit (65% (Umum))<br>Inti Tier 4 (18% (Langka)) |
| Kepulauan Kraken Muda | Kraken Laut | Tier 5 | Tentakel Kraken Spirit (60% (Umum))<br>Inti Tier 5 (15% (Langka)) |
| Pari Elektrik Samudra | Ikan Elektrik | Tier 5 | Kulit Elektrik Spirit (60% (Umum))<br>Inti Tier 5 (12% (Langka)) |
| Naga Air Gelombang Samudra | Naga Gelombang | Tier 6 | Sisik Naga Air (55% (Umum))<br>Inti Tier 6 (10% (Langka)) |
| Kura-kura Island-Back Purba | Kura-kura Raksasa | Tier 6 | Tempurung Pulau Purba (55% (Umum))<br>Inti Tier 6 (8% (Langka)) |
| Kraken Raksasa Samudra | Mythical Kraken | Tier 7 | Tinta Kraken Purba (50% (Umum))<br>Inti Kraken Tier 7 (4% (Legendaris)) |
| Naga Laut Sisik Emas | Naga Laut Emas | Tier 7 | Sisik Naga Emas Laut (50% (Umum))<br>Inti Tier 7 (3% (Legendaris)) |
| Ular Laut Sembilan Kepala | Reptil Samudra | Tier 8 | Sisik Sembilan Kepala (45% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Paus Purba Samudra Canghai | Beast Samudra | Tier 8 | Kristal Samudra Purba (40% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Naga Purba Canghai Mutiara Suci | Primordial Sea Dragon | Tier 9 | Inti Naga Samudra (40% (Umum))<br>Mutiara Purba Canghai (1% (Legendaris)) |

---

### 4.6 🏜️ Xixuan Zhou (Gurun Pasir Suci)

| Nama Beast | Jenis / Kategori | Tier | Loot |
|---|---|---|---|
| Kadal Pasir Emas | Reptil Gurun | Tier 1 | Sisik Pasir (85% (Umum)) |
| Kumbang Pasir Besi | Serangga Gurun | Tier 1 | Cangkang Kumbang (80% (Umum)) |
| Cacing Pasir Besi | Cacing Gurun | Tier 2 | Kulit Cacing Besi (80% (Umum))<br>Inti Tier 2 (35% (Jarang)) |
| Ular Pasir Taring Merah | Reptil Beracun | Tier 2 | Bisa Pasir (75% (Umum))<br>Kulit Ular (35% (Jarang)) |
| Kalajengking Emas Pasir | Serangga Emas | Tier 3 | Sengat Emas Spirit (75% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Elang Badai Gurun | Unggas Udara | Tier 3 | Bulu Elang Badai (70% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Serigala Pasir Gurun | Predator Gurun | Tier 4 | Taring Serigala Pasir (65% (Umum))<br>Inti Tier 4 (20% (Langka)) |
| Cacing Pasir Raksasa | Cacing Raksasa | Tier 4 | Kulit Cacing Raksasa (65% (Umum))<br>Inti Tier 4 (18% (Langka)) |
| Elang Pasir Iblis | Unggas Iblis | Tier 5 | Bulu Iblis Gurun (60% (Umum))<br>Inti Tier 5 (15% (Langka)) |
| Banteng Batu Gurun Emas | Beast Batu Pasir | Tier 5 | Tanduk Emas Gurun (60% (Umum))<br>Inti Tier 5 (12% (Langka)) |
| Skorpion Emas Legendaris | Ancient Guardian | Tier 6 | Sengat Skorpion Emas (55% (Umum))<br>Inti Tier 6 (10% (Langka)) |
| Naga Pasir Emas Gurun | Naga Pasir | Tier 6 | Sisik Naga Pasir (55% (Umum))<br>Inti Tier 6 (8% (Langka)) |
| Gryphon Pasir Suci | Flying Beast | Tier 7 | Bulu Gryphon Gurun (50% (Umum))<br>Inti Tier 7 (4% (Legendaris)) |
| Cacing Ruang Pasir Purba | Cacing Anomali | Tier 7 | Kulit Pasir Purba (50% (Umum))<br>Inti Cacing Ruang (3% (Legendaris)) |
| Naga Gurun Pasir Emas Purba | Naga Gurun Purba | Tier 8 | Sisik Naga Gurun (45% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Sphinx Batu Segel Purba | Guardian Reruntuhan | Tier 8 | Kristal Batu Segel (40% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Qilin Pasir Suci Hunyuan | Mythical Guardian | Tier 9 | Tanduk Qilin Gurun (40% (Umum))<br>Inti Qilin Pasir Tier 9 (1% (Legendaris)) |

---

### 4.7 ❄️ Beihan Zhou (Padang Es Abadi)

| Nama Beast | Jenis / Kategori | Tier | Loot |
|---|---|---|---|
| Kelinci Es Salju | Mamalia Kecil | Tier 1 | Bulu Kelinci Es (85% (Umum)) |
| Unggas Es Salju | Unggas Salju | Tier 1 | Bulu Unggas Es (80% (Umum)) |
| Rubah Es Berekor Dua | Mamalia Es | Tier 2 | Bulu Rubah Es (80% (Umum))<br>Inti Es Tier 2 (35% (Jarang)) |
| Ular Es Salju | Reptil Salju | Tier 2 | Bisa Es Salju (75% (Umum))<br>Kulit Ular Es (35% (Jarang)) |
| Serigala Salju Pemburu | Predator Salju | Tier 3 | Taring Serigala Salju (75% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Burung Hantu Kristal Es | Unggas Malam | Tier 3 | Bulu Kristal Es (70% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Beruang Es Kristal Purba | Tank Es | Tier 4 | Empedu Beruang Es (65% (Umum))<br>Inti Es Tier 4 (20% (Langka)) |
| Rubah Salju Berekor Sembilan | Spirit Fox | Tier 4 | Bulu Rubah Sembilan Ekor (65% (Umum))<br>Inti Tier 4 (18% (Langka)) |
| Serigala Es Abadi Guardian | Ancient Guardian | Tier 5 | Taring Serigala Abadi (60% (Umum))<br>Inti Tier 5 (15% (Langka)) |
| Naga Es Kristal Salju | Naga Es | Tier 5 | Sisik Naga Es (60% (Umum))<br>Inti Tier 5 (12% (Langka)) |
| Goliath Es Padang Salju | Golem Es | Tier 6 | Kristal Es Padang Salju (55% (Umum))<br>Inti Tier 6 (10% (Langka)) |
| Burung Feniks Salju Abadi | Feniks Es | Tier 6 | Bulu Feniks Salju (55% (Umum))<br>Inti Tier 6 (8% (Langka)) |
| Naga Padang Es Abadi | Naga Abadi | Tier 7 | Sisik Naga Es Abadi (50% (Umum))<br>Inti Tier 7 (4% (Legendaris)) |
| Beruang Es Purba Hunyuan | Beast Purba | Tier 7 | Cakar Beruang Es Purba (50% (Umum))<br>Inti Tier 7 (3% (Legendaris)) |
| Feniks Es Salju Purba | Feniks Purba | Tier 8 | Bulu Feniks Es Purba (45% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Naga Es Kristal Bintang | Naga Bintang Es | Tier 8 | Sisik Naga Bintang Es (40% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Naga Purba Beihan Es Abadi | Primordial Frost Dragon | Tier 9 | Kristal Es Suci Hunyuan (40% (Umum))<br>Inti Es Abadi Beihan Tier 9 (1% (Legendaris)) |

---

### 4.8 🖤 Youming Zhou (Bayangan & Racun)

| Nama Beast | Jenis / Kategori | Tier | Loot |
|---|---|---|---|
| Kelelawar Bayangan Malam | Unggas Malam | Tier 1 | Sayap Kelelawar Spirit (85% (Umum)) |
| Katak Rawa Beracun | Amfibi Toksik | Tier 1 | Bisa Katak Rawa (80% (Umum)) |
| Ular Rawa Taring Hitam | Reptil Beracun | Tier 2 | Bisa Taring Hitam (80% (Umum))<br>Inti Tier 2 (35% (Jarang)) |
| Laba-laba Bayangan Malam | Serangga Bayangan | Tier 2 | Sutra Bayangan (75% (Umum))<br>Bisa Laba-laba (35% (Jarang)) |
| Kutu Iblis Pemakan Qi | Serangga Iblis | Tier 3 | Cangkang Kutu Iblis (75% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Serigala Api Hitam | Predator Api Hitam | Tier 3 | Bulu Api Hitam (70% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Kalajengking Bayangan Purba | Serangga Purba | Tier 4 | Sengat Bayangan Purba (65% (Umum))<br>Inti Tier 4 (20% (Langka)) |
| Mayat Hidup Rawa Jiwa | Undead Rawa | Tier 4 | Sisa Zirah Lapuk (65% (Umum))<br>Kristal Jiwa Kelam (18% (Langka)) |
| Naga Bayangan Api Hitam | Naga Bayangan | Tier 5 | Sisik Naga Bayangan (60% (Umum))<br>Inti Tier 5 (15% (Langka)) |
| Ular Rawa Sembilan Kepala Racun | Reptil Sembilan Kepala | Tier 5 | Bisa Sembilan Racun (60% (Umum))<br>Inti Tier 5 (12% (Langka)) |
| Serigala Bayangan Youming | Predator Bayangan | Tier 6 | Kulit Serigala Bayangan (55% (Umum))<br>Inti Tier 6 (10% (Langka)) |
| Golem Bayangan Rawa Kelam | Golem Bayangan | Tier 6 | Kristal Bayangan Kelam (55% (Umum))<br>Inti Tier 6 (8% (Langka)) |
| Naga Api Hitam Youming Purba | Naga Purba | Tier 7 | Sisik Naga Api Hitam (50% (Umum))<br>Inti Tier 7 (4% (Legendaris)) |
| Hydra Racun Rawa Youming | Mythical Hydra | Tier 7 | Darah Hydra Racun (50% (Umum))<br>Inti Tier 7 (3% (Legendaris)) |
| Naga Bayangan Sembilan Jiwa | Naga Sembilan Jiwa | Tier 8 | Sisik Naga Sembilan Jiwa (45% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Iblis Bayangan Purba Youming | Demon Purba | Tier 8 | Kristal Iblis Purba (40% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Naga Purba Youming Api Hitam Hunyuan | Primordial Shadow Dragon | Tier 9 | Kristal Bayangan Suci (40% (Umum))<br>Inti Youming Api Hitam Tier 9 (1% (Legendaris)) |

---

### 4.9 🛸 Tiangong Zhou (Penerbangan Udara & Langit)

| Nama Beast | Jenis / Kategori | Tier | Loot |
|---|---|---|---|
| Burung Pipit Angin Udara | Unggas Udara | Tier 1 | Bulu Pipit Spirit (85% (Umum)) |
| Kelelawar Angin Langit | Mamalia Udara | Tier 1 | Sayap Kelelawar Spirit (80% (Umum)) |
| Burung Angin Taring Besi | Unggas Besi | Tier 2 | Bulu Angin Besi (80% (Umum))<br>Inti Tier 2 (35% (Jarang)) |
| Elang Udara Awan Tipis | Unggas Awan | Tier 2 | Bulu Elang Awan (75% (Umum))<br>Inti Tier 2 (35% (Jarang)) |
| Rajawali Badai Langit | Unggas Badai | Tier 3 | Sayap Besi Spirit (75% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Burung Hantu Angin Malam | Unggas Malam | Tier 3 | Bulu Angin Malam (70% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Gryphon Udara Tiangong | Flying Beast | Tier 4 | Bulu Gryphon Langit (65% (Umum))<br>Inti Tier 4 (20% (Langka)) |
| Paus Udara Melayang | Beast Raksasa | Tier 4 | Kulit Paus Udara (65% (Umum))<br>Inti Tier 4 (18% (Langka)) |
| Naga Angin Langit Tiangong | Naga Langit | Tier 5 | Sisik Naga Angin (60% (Umum))<br>Inti Tier 5 (15% (Langka)) |
| Rajawali Petir Awan Hitam | Unggas Petir | Tier 5 | Bulu Petir Awan (60% (Umum))<br>Inti Tier 5 (12% (Langka)) |
| Naga Terbang Langit Tiangong | Naga Airship Guard | Tier 6 | Sayap Naga Terbang (55% (Umum))<br>Inti Tier 6 (10% (Langka)) |
| Paus Langit Melayang Purba | Beast Langit Purba | Tier 6 | Kristal Paus Langit (55% (Umum))<br>Inti Tier 6 (8% (Langka)) |
| Gryphon Badai Petir Tiangong | Flying Gryphon Elit | Tier 7 | Bulu Gryphon Petir (50% (Umum))<br>Inti Tier 7 (4% (Legendaris)) |
| Naga Langit Ruang Tiangong | Naga Ruang | Tier 7 | Sisik Naga Ruang (50% (Umum))<br>Inti Tier 7 (3% (Legendaris)) |
| Rajawali Purba Langit Tiangong | Unggas Purba | Tier 8 | Bulu Rajawali Purba (45% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Naga Angin Bintang Tiangong | Naga Bintang | Tier 8 | Sisik Naga Bintang (40% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Rajawali Purba Hunyuan Tiangong | Primordial Sky Eagle | Tier 9 | Bulu Suci Langit (40% (Umum))<br>Inti Rajawali Hunyuan Tier 9 (1% (Legendaris)) |

---

### 4.10 ☠️ Juejing Zhou (Zona Terlarang & Anomali Ruang)

| Nama Beast | Jenis / Kategori | Tier | Loot |
|---|---|---|---|
| Tikus Anomali Ruang | Mamalia Kecil | Tier 1 | Bulu Anomali (85% (Umum)) |
| Kadal Petir Tanah Purba | Reptil Petir | Tier 1 | Sisik Petir Tanah (80% (Umum)) |
| Serigala Taring Ruang | Predator Ruang | Tier 3 | Taring Serigala Ruang (75% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Kera Anomali Petir | Primata Anomali | Tier 3 | Kulit Kera Petir (70% (Umum))<br>Inti Tier 3 (30% (Jarang)) |
| Chimera Batu Purba | Beast Purba | Tier 4 | Tanduk Chimera Purba (65% (Umum))<br>Inti Tier 4 (20% (Langka)) |
| Ular Retakan Ruang | Reptil Ruang | Tier 4 | Sisik Retakan Ruang (65% (Umum))<br>Inti Tier 4 (18% (Langka)) |
| Beast Kuno Juejing | Beast Kuno | Tier 5 | Taring Beast Kuno (60% (Umum))<br>Inti Tier 5 (15% (Langka)) |
| Serigala Anomali Ruang Purba | Predator Purba | Tier 5 | Kulit Ruang Purba (60% (Umum))<br>Inti Tier 5 (12% (Langka)) |
| Serpent Raksasa Retakan Ruang | Serpent Ruang | Tier 6 | Darah Beast Purba (55% (Umum))<br>Kristal Ruang Purba (10% (Langka))<br>Inti Tier 6 (5% (Legendaris)) |
| Golem Anomali Ruang Juejing | Golem Anomali | Tier 6 | Kristal Golem Ruang (55% (Umum))<br>Inti Tier 6 (8% (Langka)) |
| Chimera Retakan Ruang Purba | Chimera Ruang | Tier 7 | Tanduk Chimera Ruang (50% (Umum))<br>Inti Tier 7 (4% (Legendaris)) |
| Beast Ruang Purba Juejing | Beast Anomali Elit | Tier 7 | Kulit Beast Ruang (50% (Umum))<br>Inti Tier 7 (3% (Legendaris)) |
| Naga Retakan Ruang Purba | Naga Ruang Purba | Tier 8 | Sisik Naga Ruang Purba (45% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Iblis Anomali Ruang Juejing | Demon Ruang | Tier 8 | Kristal Iblis Ruang (40% (Umum))<br>Inti Tier 8 (2% (Legendaris)) |
| Naga Purba Retakan Ruang Hunyuan | Primordial Rift Dragon | Tier 9 | Kristal Ruang Purba Hunyuan (40% (Umum))<br>Inti Retakan Ruang Tier 9 (1% (Legendaris)) |

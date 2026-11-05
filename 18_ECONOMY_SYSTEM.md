# 💰 Xuantian World — Sistem Ekonomi, Perdagangan & Valuation

> **Modul:** 18 — Economy System
> **Prinsip:** Anti-Cheat Enforced — Dynamic Supply-Demand — Item Origin Logging — Fixed Math Valuation
> **Rujukan:** `00_CORE_RULES_AI_GM.md`, `12_CROSS_REGION_ORGANIZATIONS.md`, `14_CRAFTING_AND_PROFESSIONS_SYSTEM.md`, `42_PERGURUAN_DAGANG_JIUZHOU.md`, `45_SERIKAT_YOUXIA_SANXIU.md`, `INDEX.md`

---

## 0. Filosofi Sistem Ekonomi & Anti-Cheat Valuation

Sama seperti konsentrasi Qi tunduk pada `QiCap` formula (`13_SPIRITUAL_ROOT_SYSTEM.md`), setiap nilai komoditas, barang, artefak, dan jasa di Xuantian World tunduk pada **Formula Harga Dasar** yang tetap. AI GM WAJIB menghitung seluruh harga jual-beli melalui formula di bawah ini dan DILARANG MENERIMA klaim harga sepihak dari pemain tanpa dasar perhitungan matematis.

```
===============================================================================
                       ATURAN EMAS ANTI-CHEAT EKONOMI
===============================================================================
 1. NO ARBITRARY PRICE: Harga tidak boleh ditebak atau disepakati sepihak.
 2. ITEM ORIGIN LOG REQUIRED: Barang Tier 3+ WAJIB memiliki Origin Log.
 3. BARTER HARD CAP: Tawar-menawar dibatasi maksimal ±15% dari harga formula.
 4. SCARCITY MODIFIER: Fluktuasi wilayah dibatasi multiplier 0,5× s/d 2,5×.
 5. TIMESTAMPED TRANSACTION: Seluruh transaksi dicatat bertimestamp resmi.
===============================================================================
```

---

## 1. Mata Uang Resmi & Formula Konversi Benua

Transaksi di Xuantian World membedakan sirkulasi mata uang fana (*Mortal Currency*), mata uang transisi komoditas ber-Qi (*Jade Tael*), dan giok roh kultivator (*Spirit Jade*):

### 1.1 Mata Uang Fana (Mortal Currency)
* **Copper Tael:** Unit terkecil untuk kebutuhan harian mortal.
* **Silver Tael:** `1 Silver Tael = 100 Copper Tael`

### 1.2 Mata Uang Transisi Fana & Kultivator (Spiritual Commodity Currency)
* **Jade Tael:** `1 Jade Tael = 100 Silver Tael = 10.000 Copper Tael`
  *Mata uang perantara yang digunakan oleh kalangan fana kaya, pedagang besar, dan kultivator saat bertransaksi untuk bahan herbal, benih, komoditas kerajinan, atau benda yang memiliki energi spiritual/Qi ringan.*

### 1.3 Giok Roh Kultivator (Spirit Jade)
Kualitas Giok Roh dibagi menjadi 4 tingkatan: Rendah, Menengah, Tinggi, dan Purba.
* **Giok Roh Rendah (Low-Grade Spirit Jade):** `1 Low-Grade Spirit Jade = 10 Jade Tael = 1.000 Silver Tael = 100.000 Copper Tael`
* **Giok Roh Menengah (Mid-Grade Spirit Jade):** `1 Mid-Grade Spirit Jade = 100 Low-Grade Spirit Jade`
* **Giok Roh Tinggi (High-Grade Spirit Jade):** `1 High-Grade Spirit Jade = 100 Mid-Grade Spirit Jade = 10.000 Low-Grade Spirit Jade`
* **Giok Roh Purba (Ancient Spirit Jade):** `1 Ancient Spirit Jade = 100 High-Grade Spirit Jade = 10.000 Mid-Grade Spirit Jade = 1.000.000 Low-Grade Spirit Jade`

---

## 2. Formula Matematika Ekonomi & Perdagangan

### 2.1 Formula Harga Pembelian Dinamis (Dynamic Buying Price)

```
FinalBuyPrice = ItemBaseValue × DiscountModifier × RegionScarcityMultiplier
```

*Parameter Formula:*
* **ItemBaseValue:** Nilai acuan standar barang berdasarkan Grade/Tier.
* **DiscountModifier:** `1.0 - (BarterSkillLevel × 0.03) - (FactionAffinityBonus × 0.05)` *(Maksimal diskon 30% / Modifier minimal 0.70).*
* **RegionScarcityMultiplier:** Indeks kelangkaan wilayah (0.5× untuk wilayah asal produsen, 1.0× wilayah normal, 1.5× s/d 2.5× wilayah terisolasi/gurun/zona terlarang).

#### 📐 Contoh Perhitungan Worked-Out (Buying Lotus Es):
Seorang kultivator membeli *Lotus Es Abadi Grade 4* (Base: 20 Low-Grade Spirit Jade) di *Shenmu Zhou* (Scarcity 1.5x) dengan Skill Barter Level 3 (0.09) dan Affinity Faksi +10% (0.10):
```
DiscountModifier = 1.0 - 0.09 - 0.10 = 0.81
FinalBuyPrice = 20 Low-Grade Spirit Jade × 0.81 × 1.5 = 24.3 Low-Grade Spirit Jade (Dibulatkan: 24 Low-Grade Spirit Jade + 3 Jade Tael).
```

---

### 2.2 Formula Penjualan Barang / Loot Player (Player Selling Price)

```
PlayerSellValue = ItemBaseValue × 0.50 × (1 + (BarterSkillLevel × 0.05))
```
*(Maksimal harga jual player ke NPC / Tokoh Guild = 80% dari ItemBaseValue).*

---

### 2.3 Formula Pajak Komisi Lelang Wanbao & Guild

```
AuctionCommission = FinalBidAmount × (0.10 - (YouxiaRankBonus × 0.01))
SellerPayout = FinalBidAmount - AuctionCommission
```

---

## 3. Katalog Harga Acuan Komoditas, Barang & Jasa Benua

### 3.1 Bahan Profesi, Benih & Hasil Panen Herbal
| Komoditas / Bahan | Grade / Tier | Base Price | Wilayah Produsen Utama (Scarcity 0.5×) |
|---|---|---|---|
| Benih Lingzhi Hijau | Tier 1 | 5 Silver Tael | Shenmu Zhou (2.5 Silver Tael) |
| Benih Rumput Qi Yuan | Tier 2 | 2 Jade Tael | Shenmu Zhou (1 Jade Tael) |
| Benih Lotus Es Abadi | Tier 4 | 20 Low-Grade Spirit Jade | Beihan Zhou (10 Low-Grade Spirit Jade) |
| Benih Ginseng Naga Purba | Tier 7 | 50 Mid-Grade Spirit Jade | Shenmu Zhou (25 Mid-Grade Spirit Jade) |
| Pupuk Qi Kayu Shenmu | Grade 2 Soil | 50 Silver Tael / karung | Lembah Biyang (25 Silver Tael) |
| Ingot Besi Spirit (Spirit Iron) | Tier 1–3 | 1 Jade Tael / ingot | Chiyan Zhou (0.5 Jade Tael) |
| Bijih Besi Meteorit Merah | Tier 4–6 | 10 Low-Grade Spirit Jade / ingot | Shendu / Chiyan (5 Low-Grade Spirit Jade) |
| Kertas Sutra Jimat Kosong | Tier 1–3 | 1 Silver Tael / lembar | Xixuan Zhou (0.5 Silver Tael) |
| Botol Bisa Ular Rawa | Tier 2–4 | 5 Silver Tael / botol | Youming Zhou (2.5 Silver Tael) |

### 3.2 Tiket & Layanan Transportasi Kapal Terbang (Tiankong Feichuan)
| Jenis Rute / Moda Feichuan | Kapasitas Moda | Harga Tiket Standard | Durasi Tempuh Lintas Wilayah |
|---|---|---|---|
| **Lokal Antar-Kota** *(Skiff)* | 1–3 Penumpang | 1–3 Jade Tael | 2–6 Jam |
| **Lintas Wilayah Tetangga** *(Galleon)* | 50–100 Penumpang | 15 Low-Grade Spirit Jade | 12–15 Jam |
| **Lintas Wilayah Jauh** *(Heavy Galleon)* | 200+ Penumpang | 28 Low-Grade Spirit Jade | 22–26 Jam |
| **Rute Zona Terlarang** *(Warship)* | Pasukan Pengawal | 100 Low-Grade Spirit Jade | 36 Jam (Sangat Berbahaya) |

### 3.3 Spirit Beast, Egg & Jimat Penjinak
| Item / Beast | Tier / Rank | Harga Pasar Standard | Pemasok Utama |
|---|---|---|---|
| Jimat Penjinak Beast Pemula | Tier 1 | 1 Low-Grade Spirit Jade | Perguruan Qingling / Guild |
| Jimat Penjinak Beast Master | Tier 3 | 20 Low-Grade Spirit Jade | Perguruan Qingling / Guild |
| Egg Spirit Beast Unggas Hutan | Tier 1 Beast | 5 Low-Grade Spirit Jade | Desa Qingling (Shenmu) |
| Egg Serigala Bayangan Kabut | Tier 2 Beast | 15 Low-Grade Spirit Jade | Desa Qingling (Shenmu) |
| Egg Spirit Beast Serigala Es | Tier 3 Beast | 50 Low-Grade Spirit Jade | Kota Hanbing (Beihan) |
| Egg Spirit Beast Dragonblood | Tier 6 Beast | 10 High-Grade Spirit Jade | Wanbao Auction House |

---

## 4. Sistem Registrasi Item Origin Log Resmi

Setiap barang bernilai tinggi (Tier 3+ / Grade High / Artefak Legendaris) WAJIB mencantumkan catatan **Origin Log** di profil barang:

```
[ITEM ORIGIN LOG]
- Item Name: Pedang Besi Meteorit Grade 5
- Origin Creator: Master Penempa Shendu (NPC ID: 24-01)
- Timestamp: Year 15000, Month 3, Day 12
- Extraction Location: Kawah Shendu, Chiyan Zhou
- Verifier Stamp: Serikat Youxia Sanxiu Tianjing (Log #YX-88421)
```

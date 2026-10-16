# 💰 Sistem Ekonomi & Perdagangan Xuantian World

> **Modul:** 15 — Economy System
> **Rujukan:** `00_CORE_RULES_AI_GM.md`, `14_CRAFTING_AND_PROFESSIONS_SYSTEM.md`, `INDEX.md`

---

## 1. Mata Uang Resmi & Formula Konversi

Di Xuantian World, transaksi fana dan kultivator dipisahkan secara tegas:

### 1.1 Mudarat/Sirkulasi Mata Uang Fana (Mortal Currency)
* **Tael Tembaga (Copper Tael - CT)**
* **Tael Perak (Silver Tael - ST):** `1 ST = 100 CT`
* **Tael Emas (Gold Tael - GT):** `1 GT = 100 ST = 10.000 CT`

### 1.2 Mata Uang Kultivator (Spiritual Stones)
* **Batu Spirit Kualitas Rendah (Low-Grade Spirit Stone - LSS):** `1 LSS = 10 GT = 1.000 ST`
* **Batu Spirit Kualitas Sedang (Mid-Grade Spirit Stone - MSS):** `1 MSS = 100 LSS`
* **Batu Spirit Kualitas Tinggi (High-Grade Spirit Stone - HSS):** `1 HSS = 100 MSS = 10.000 LSS`
* **Batu Spirit Purba (Ancient Spirit Stone - ASS):** `1 ASS = 100 HSS = 1.000.000 LSS`

---

## 2. Formula Matematika Ekonomi & Perdagangan

### 2.1 Formula Harga Pasar Dinamis (Dynamic Market Price)
Harga barang di toko, pasar, dan lelang dipengaruhi oleh reputasi karakter, hubungan faksi, serta tingkat kelangkaan wilayah:

`BasePrice = ItemStandardValue`
`DiscountModifier = 1.0 - (MerchantReputationTier × 0.05) - (FactionAffinityBonus × 0.10)`
`RegionScarcityMultiplier = RegionalAvailabilityIndex (0.8 hingga 2.5)`
`FinalBuyPrice = BasePrice × DiscountModifier × RegionScarcityMultiplier`

*Contoh:* Lotus Es Abadi (Base: 20 LSS) dibeli di *Shenmu Zhou* (Scarcity 1.5x) oleh karakter dengan Faction Affinity +10% (0.10):
`FinalBuyPrice = 20 × (1.0 - 0.10) × 1.5 = 20 × 0.90 × 1.5 = 27 LSS.`

### 2.2 Formula Penjualan Barang Bekas / Loot
`PlayerSellValue = BasePrice × 0.50 × (1 + BarterSkillLevel × 0.05)`
*(Maksimal harga jual player = 80% dari BasePrice).*

### 2.3 Formula Pajak Lelang Wanbao (Auction House Fee)
`AuctionCommission = FinalBidAmount × (0.10 - (VIPTier × 0.02))`
`SellerPayout = FinalBidAmount - AuctionCommission`

---

## 3. Daftar Harga Acuan Barang & Jasa

### 3.1 Bahan Profesi & Benih Obat Spirit
| Item / Bahan | Grade / Tier | Base Price | Region Scarcity Terendah |
|---|---|---|---|
| Benih Lingzhi Hijau | Tier 1 | 5 ST | Shenmu Zhou (4 ST) |
| Benih Rumput Qi Yuan | Tier 2 | 2 GT | Shenmu Zhou (1.5 GT) |
| Benih Lotus Es Abadi | Tier 4 | 20 LSS | Beihan Zhou (12 LSS) |
| Benih Ginseng Naga Purba | Tier 7 | 50 MSS | Shenmu Zhou (35 MSS) |
| Pupuk Qi Kayu Shenmu | Grade 2 Soil | 50 ST / karung | Shenmu Zhou (30 ST) |
| Kertas Jimat Spirit Kosong | Tier 1–3 | 1 ST / lembar | Xixuan Zhou (0.8 ST) |
| Tinta Darah Beast Spirit | Tier 1–3 | 5 ST / botol | Qingling / Bestiary |
| Ingot Besi Spirit (Spirit Iron) | Tier 1–3 | 1 GT / ingot | Chiyan Zhou (0.7 GT) |

### 3.2 Tiket & Layanan Transportasi Kapal Terbang
| Rute Penerbangan | Moda / Tier | Harga Tiket Standard |
|---|---|---|
| Antar Kota Lokal (Satu Wilayah) | Skiff / Commercial | 1–3 GT |
| Lintas Wilayah Tetangga (mis. Shenmu → Zhonghua) | Passenger Galleon (Tier 3) | 15 LSS |
| Lintas Wilayah Jauh (mis. Shenmu → Beihan / Canghai) | Heavy Galleon | 28 LSS |
| Rute Zona Terlarang (Juejing Zhou) | War Battleship (Tier 4) | 100 LSS |

### 3.3 Spirit Beast & Jimat Penjinak
| Item / Beast | Tier / Rank | Harga Pasar |
|---|---|---|
| Jimat Penjinak Beast Pemula | Tier 1 | 1 LSS |
| Jimat Penjinak Beast Master | Tier 3 | 20 LSS |
| Egg Spirit Beast Unggas Hutan | Tier 1 Beast | 5 LSS |
| Egg Spirit Beast Serigala Es | Tier 3 Beast | 50 LSS |
| Egg Spirit Beast Dragonblood | Tier 6 Beast | 10 HSS |

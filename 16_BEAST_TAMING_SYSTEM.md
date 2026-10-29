# 🐾 Xuantian World — Sistem Penjinakan & Pelatihan Spirit Beast

> **Modul:** 16 — Beast Taming System
> **Prinsip:** Anti-Cheat Enforced — Equal Contract & Taming Scaling — Verified Beast Registry
> **Rujukan silang:** `00_CORE_RULES_AI_GM.md` (aturan wajib GM), `12_CROSS_REGION_ORGANIZATIONS.md` (Serikat Penjinak Beast), `13_SPIRITUAL_ROOT_SYSTEM.md` (Akar Spiritual & QiCap), `14_CRAFTING_AND_PROFESSIONS_SYSTEM.md` (profesi & pakan), `20_COMBAT_SYSTEM.md` (combat stats beast), `21_BESTIARY.md` (katalog beast & taming prerequisites), `33_PERGURUAN_BEAST_QINGLING.md` (perguruan penjinak beast)

---

## 0. Filosofi Sistem Penjinakan & Pelatihan Spirit Beast

Penjinak Beast (*Beast Tamer*) bertugas melatih, memasang jimat penjinak, dan mengikat kontrak kesetaraan atau perhambaan dengan Spirit Beast. Keberhasilan proses penjinakan, tingkat kesetiaan, serta peningkatan statistik Spirit Beast tunduk pada aturan dan formula matematis yang ketat.

### Aturan Emas Anti-Cheat Penjinakan Beast
- **Dilarang Klaim Penjinakan Otomatis:** Player TIDAK BISA mengklaim Spirit Beast liar otomatis menjadi peliharaan/tunggangan tanpa melalui kalkulasi roll probabilitas keberhasilan penjinakan AI GM.
- **Risiko Serangan Balik (Backlash):** Kegagalan penjinakan pada beast dengan Tier tinggi atau HP penuh berisiko memicu amukan Beast (*Beast Rage*) yang menyerang langsung ke Penjinak.
- **Registrasi & Identitas Beast:** Setiap Spirit Beast yang berhasil dijinakkan WAJIB memiliki status Loyalty dan tercatat dalam save file karakter player.

---

## 1. Formula Keberhasilan Penjinakan (Taming Chance Formula)

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

---

## 2. Formula Kesetiaan & Peningkatan Status Beast (Loyalty System)

```
LoyaltyGainPerFeeding = 5 + (AlchemistPillQuality × 2)
LoyaltyLossInBattleDefeat = 15 Points
```

| Tingkat Loyalty | Status Kesetiaan | Efek Statistik Spirit Beast |
|---|---|---|
| **71 – 100** | Sangat Setia | Bonus Attack & Defense Beast **+10%** |
| **31 – 70** | Setia / Normal | Statistik Normal |
| **0 – 30** | Membangkang | 20% peluang menolak perintah bertarung / berisiko kabur |

---

## 3. Perguruan & Serikat Penjinak Beast

- **Perguruan Penjinak Beast Qingling** (`33_PERGURUAN_BEAST_QINGLING.md`): Pusat latihan komunikasi batin, seni penjinakan, dan kontrak kesetaraan.
- **Serikat Penjinak Beast Xuantian** (`12_CROSS_REGION_ORGANIZATIONS.md`): Pengelola pendaftaran, transaksi beast, dan arena sertifikasi penjinak.
- **Katalog Spirit Beast Liar & Tunggangan:** `21_BESTIARY.md` (Mencantumkan seluruh spesies Spirit Beast beserta status taming `[Wajib Dijinakkan]`).

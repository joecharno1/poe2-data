# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-02T21:24:36+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **21169** (21169 priced in exalted)
- Distinct bases: 570 · distinct mods: 756 · mod rows: 115919
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-02T21:06:08+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×32.09** (median |log error| 3.4686)
- Within ±30% of asking price: **31%**
- Skill vs constant-price guess: **-0.01** (> 0 = the mods carry signal)
- Calibration: 68% of actuals above prediction (target ≈ 75%)

| group | n_test | ×err | ±30% | skill |
|---|---|---|---|---|
| accessory.belt | 371 | ×511.42 | 20% | +0.12 |
| armour.boots | 310 | ×17.98 | 25% | +0.06 |
| accessory.amulet | 310 | ×28.64 | 4% | -0.16 |
| armour.gloves | 304 | ×31.17 | 22% | -0.01 |
| armour.helmet | 302 | ×231.37 | 26% | +0.06 |
| armour.chest | 295 | ×69.90 | 14% | +0.00 |
| weapon.wand | 264 | ×250.39 | 24% | -0.02 |
| weapon.crossbow | 241 | ×43.50 | 22% | +0.04 |
| other | 241 | ×1.00 | 68% | +0.02 |
| accessory.ring | 230 | ×23.33 | 2% | -0.44 |
| weapon.bow | 226 | ×48.43 | 19% | +0.08 |
| weapon.sceptre | 133 | ×1.00 | 100% | +0.00 |
| armour.shield | 99 | ×1.00 | 100% | n/a |
| armour.focus | 94 | ×1.00 | 99% | -0.00 |
| weapon.spear | 86 | ×1.00 | 100% | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### accessory.belt — n=1795, R²=-0.8044

intercept: `2.2679`  ·  log_price: True  ·  ilvl: `-0.02804`  ·  n_mods: `-0.01294`  ·  n_top_tier: `-0.12370`  ·  corrupted: `0.09938`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 0.42895 |
| `crafted.stat_3249412463` | 0.42042 |
| `implicit.stat_731781020` | 0.26037 |
| `explicit.stat_3299347043@T1` | 0.24463 |
| `pseudo.total_ele_res>=80` | 0.21912 |
| `explicit.stat_3299347043@T2` | 0.21544 |
| `explicit.stat_3585532255@T1` | 0.18620 |
| `explicit.stat_809229260@T1` | 0.17070 |
| `explicit.stat_1412217137@T2` | 0.16900 |
| `explicit.stat_3372524247@T1` | 0.16761 |
| `explicit.stat_3325883026@T2` | 0.15922 |
| `explicit.stat_2881298780@T2` | 0.15877 |

### armour.chest — n=1723, R²=-0.7429

intercept: `8.1175`  ·  log_price: True  ·  ilvl: `-0.10280`  ·  n_mods: `-0.03621`  ·  n_top_tier: `0.37483`  ·  corrupted: `-1.20414`  ·  n_sockets: `0.01752`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 8.18229 |
| `explicit.stat_3981240776@T1` | 2.74238 |
| `explicit.stat_3372524247@T1` | 2.64460 |
| `explicit.stat_4220027924@T1` | 1.40262 |
| `explicit.stat_3299347043@T1` | 1.02157 |
| `explicit.stat_2339757871@T1` | -0.96715 |
| `explicit.stat_3301100256@T2` | -0.90792 |
| `explicit.stat_3261801346@T1` | -0.86810 |
| `explicit.stat_3261801346@T2` | 0.79699 |
| `explicit.stat_2339757871@T2` | -0.68200 |
| `explicit.stat_986397080@T1` | -0.61162 |
| `explicit.stat_2451402625@T1` | -0.58562 |

### armour.boots — n=1714, R²=-0.6134

intercept: `7.7920`  ·  log_price: True  ·  ilvl: `-0.09746`  ·  n_mods: `-0.05091`  ·  n_top_tier: `0.82073`  ·  corrupted: `-0.06766`  ·  n_sockets: `0.06993`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 4.94242 |
| `rune.stat_836936635` | 2.62364 |
| `desecrated.stat_2250533757@T2` | 1.29604 |
| `explicit.stat_3261801346@T2` | -1.17134 |
| `explicit.stat_3321629045@T2` | -1.07979 |
| `explicit.stat_124859000@T2` | -1.03873 |
| `explicit.stat_2339757871@T1` | -1.03091 |
| `explicit.stat_2923486259@T2` | -1.01318 |
| `explicit.stat_2923486259@T1` | -1.01065 |
| `explicit.stat_2451402625@T2` | -1.00914 |
| `explicit.stat_3484657501@T2` | -0.99500 |
| `explicit.stat_3362812763@T2` | -0.99436 |

### armour.helmet — n=1700, R²=-0.8748

intercept: `7.4099`  ·  log_price: True  ·  ilvl: `-0.09399`  ·  n_mods: `-0.02917`  ·  n_top_tier: `0.25180`  ·  corrupted: `0.37554`  ·  n_sockets: `-0.04581`

| stat_id | coef |
|---|---|
| `desecrated.stat_3917489142@T1` | -5.05967 |
| `explicit.stat_4220027924@T1` | 3.11899 |
| `crafted.stat_3917489142@T1` | 2.43835 |
| `desecrated.stat_3299347043@T2` | 1.33379 |
| `explicit.stat_2339757871@T1` | 1.31891 |
| `explicit.stat_3325883026@T1` | -0.52766 |
| `desecrated.stat_4015621042@T2` | -0.51513 |
| `explicit.stat_3484657501@T1` | -0.50399 |
| `explicit.stat_1263695895@T2` | -0.47953 |
| `explicit.stat_53045048@T2` | -0.44647 |
| `explicit.stat_2923486259@T2` | -0.44482 |
| `desecrated.stat_3917489142` | 0.43280 |

### armour.gloves — n=1679, R²=-0.7436

intercept: `7.6962`  ·  log_price: True  ·  ilvl: `-0.09784`  ·  n_mods: `-0.00578`  ·  n_top_tier: `0.28974`  ·  corrupted: `-0.14466`  ·  n_sockets: `-0.05791`

| stat_id | coef |
|---|---|
| `explicit.stat_4067062424@T2` | 4.58905 |
| `explicit.stat_3372524247@T1` | 3.78739 |
| `desecrated.stat_3299347043@T1` | -1.94465 |
| `rune.stat_201332984` | 1.94187 |
| `explicit.stat_2339757871@T1` | -1.49162 |
| `explicit.stat_1999113824@T2` | 1.30318 |
| `explicit.stat_1754445556@T2` | 1.05413 |
| `explicit.stat_2451402625@T2` | -0.76272 |
| `explicit.stat_9187492@T1` | 0.74227 |
| `explicit.stat_124859000@T2` | -0.62494 |
| `explicit.stat_53045048@T1` | -0.57124 |
| `explicit.stat_1671376347@T2` | -0.57095 |

### accessory.amulet — n=1549, R²=-0.5999

intercept: `10.8485`  ·  log_price: True  ·  ilvl: `-0.10684`  ·  n_mods: `-0.67947`  ·  n_top_tier: `1.25840`  ·  corrupted: `-2.25031`  ·  n_sockets: `-1.50195`

| stat_id | coef |
|---|---|
| `explicit.stat_328541901@T1` | -5.44295 |
| `explicit.stat_2748665614@T2` | -4.99253 |
| `explicit.stat_4220027924@T2` | -4.05728 |
| `explicit.stat_2901986750@T1` | -3.92110 |
| `explicit.stat_2482852589@T1` | -3.56645 |
| `explicit.stat_2748665614@T1` | -3.33616 |
| `explicit.stat_3325883026@T2` | -3.26772 |
| `explicit.stat_1444556985@T1` | 3.16196 |
| `explicit.stat_803737631@T2` | -2.87749 |
| `explicit.stat_2482852589@T2` | -2.82373 |
| `explicit.stat_3556824919@T2` | -2.73778 |
| `explicit.stat_983749596@T1` | -2.66339 |

### weapon.wand — n=1530, R²=-0.7966

intercept: `7.5348`  ·  log_price: True  ·  ilvl: `-0.09419`  ·  n_mods: `-0.03963`  ·  n_top_tier: `0.26438`  ·  corrupted: `2.69191`  ·  n_sockets: `-0.01915`

| stat_id | coef |
|---|---|
| `explicit.stat_1600707273@T1` | 6.32775 |
| `explicit.stat_1545858329@T1` | 6.10578 |
| `explicit.stat_591105508@T1` | 5.91024 |
| `explicit.stat_4226189338@T1` | 5.70408 |
| `explicit.stat_2254480358@T1` | 5.68262 |
| `explicit.stat_274716455@T2` | 5.06342 |
| `explicit.stat_2231156303@T1` | 4.58872 |
| `explicit.stat_124131830@T1` | 4.34549 |
| `explicit.stat_736967255@T2` | 2.98836 |
| `crafted.stat_124131830` | 1.24284 |
| `explicit.stat_2974417149@T1` | 1.10799 |
| `explicit.stat_4226189338@T2` | 0.72960 |

### accessory.ring — n=1434, R²=-0.3813

intercept: `7.0836`  ·  log_price: True  ·  ilvl: `-0.05440`  ·  n_mods: `-0.31808`  ·  n_top_tier: `0.77665`  ·  corrupted: `1.41706`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T2` | -5.03412 |
| `explicit.stat_1263695895@T1` | -3.66782 |
| `explicit.stat_3962278098@T1` | -3.61052 |
| `explicit.stat_3695891184@T1` | -3.28068 |
| `explicit.stat_1379411836@T1` | 2.80792 |
| `explicit.stat_1263695895@T2` | -2.57065 |
| `explicit.stat_3962278098@T2` | -2.29991 |
| `explicit.stat_3917489142@T2` | -2.01588 |
| `explicit.stat_2901986750@T2` | -1.91838 |
| `explicit.stat_1754445556@T2` | -1.82758 |
| `explicit.stat_3325883026@T2` | -1.77190 |
| `explicit.stat_1050105434@T1` | -1.70742 |

### weapon.bow — n=1331, R²=-0.7236

intercept: `8.2165`  ·  log_price: True  ·  ilvl: `-0.10042`  ·  n_mods: `-0.09676`  ·  n_top_tier: `0.14847`  ·  corrupted: `1.26228`  ·  n_sockets: `0.02819`

| stat_id | coef |
|---|---|
| `desecrated.stat_1200678966@T1` | -9.10578 |
| `desecrated.stat_210067635@T1` | 7.96855 |
| `explicit.stat_1037193709@T1` | 4.77260 |
| `desecrated.stat_666077204@T1` | -4.54414 |
| `explicit.stat_518292764@T1` | 3.58123 |
| `explicit.stat_2463230181@T1` | 3.57109 |
| `rune.stat_3885405204` | -3.19897 |
| `explicit.stat_1202301673@T1` | 2.38642 |
| `explicit.stat_3336890334@T1` | 2.33852 |
| `explicit.stat_1509134228@T1` | 1.58745 |
| `explicit.stat_210067635@T2` | 0.91353 |
| `explicit.stat_821021828@T2` | -0.70139 |

### weapon.crossbow — n=1317, R²=-0.7313

intercept: `7.7983`  ·  log_price: True  ·  ilvl: `-0.09825`  ·  n_mods: `-0.00976`  ·  n_top_tier: `0.67624`  ·  corrupted: `3.48719`  ·  n_sockets: `0.01013`

| stat_id | coef |
|---|---|
| `desecrated.stat_2760344900@T1` | -14.51668 |
| `crafted.stat_210067635@T2` | 6.54608 |
| `explicit.stat_1037193709@T1` | 5.59073 |
| `explicit.stat_3336890334@T1` | 4.35139 |
| `explicit.stat_1980802737@T2` | 2.80218 |
| `explicit.stat_1980802737` | 2.80218 |
| `explicit.stat_1967051901@T2` | 2.12436 |
| `explicit.stat_709508406@T1` | 2.05349 |
| `explicit.stat_1967051901@T1` | -1.77086 |
| `explicit.stat_691932474@T2` | -1.62926 |
| `explicit.stat_691932474@T1` | -1.06333 |
| `crafted.stat_3035140377` | 1.03293 |

### other — n=1148, R²=-0.1058

intercept: `0.0001`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_1368271171@T1` | 0.69306 |
| `rune.stat_3990135792` | -0.08180 |
| `rune.stat_2974417149` | 0.03272 |
| `explicit.stat_124131830@T1` | 0.01747 |
| `explicit.stat_3962278098` | 0.01110 |
| `explicit.stat_3291658075` | 0.00503 |
| `crafted.stat_210067635@T2` | 0.00031 |
| `explicit.stat_1368271171@T2` | -0.00014 |
| `explicit.stat_55876295@T1` | -0.00010 |
| `explicit.stat_2974417149@T1` | 0.00008 |
| `explicit.stat_803737631@T2` | -0.00008 |
| `explicit.stat_789117908@T2` | 0.00007 |

### weapon.sceptre — n=612, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3984865854` | 0.00000 |
| `explicit.stat_101878827` | 0.00000 |
| `explicit.stat_101878827@T1` | 0.00000 |
| `explicit.stat_101878827@T2` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_1250712710` | 0.00000 |
| `explicit.stat_1250712710@T1` | 0.00000 |
| `explicit.stat_1250712710@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |

### weapon.spear — n=543, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1202301673@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |

### armour.focus — n=535, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2891184298` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T1` | -0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |
| `explicit.stat_2231156303` | 0.00000 |
| `explicit.stat_2231156303@T1` | 0.00000 |

### armour.shield — n=457, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  n_sockets: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1568848828` | 0.00000 |
| `explicit.stat_1011760251` | 0.00000 |
| `explicit.stat_1011760251@T1` | -0.00000 |
| `explicit.stat_1011760251@T2` | -0.00000 |
| `explicit.stat_1062208444` | 0.00000 |
| `explicit.stat_1062208444@T1` | 0.00000 |
| `explicit.stat_1062208444@T2` | 0.00000 |
| `explicit.stat_1301765461` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |
| `explicit.stat_1978899297` | 0.00000 |

## Coverage (listings per base)

- … **Dueling Wand** — 480 listings (480 priced) [1.0–719.7 ex]
- … **Obliterator Bow** — 390 listings (390 priced) [0.8–719.7 ex]
- … **Utility Belt** — 340 listings (340 priced) [1.0–719.7 ex]
- … **Siphoning Wand** — 292 listings (292 priced) [1.0–719.7 ex]
- … **Warmonger Bow** — 279 listings (279 priced) [1.0–719.7 ex]
- … **Galvanic Wand** — 272 listings (272 priced) [1.0–719.7 ex]
- … **Gold Amulet** — 263 listings (263 priced) [0.3–719.7 ex]
- … **Solar Amulet** — 261 listings (261 priced) [1.0–719.7 ex]
- … **Attuned Wand** — 253 listings (253 priced) [0.3–719.7 ex]
- … **Plate Belt** — 244 listings (244 priced) [1.0–719.7 ex]
- … **Trarthan Cannon** — 242 listings (242 priced) [0.7–719.7 ex]
- … **Withered Wand** — 237 listings (237 priced) [1.0–719.7 ex]
- … **Desolate Crossbow** — 235 listings (235 priced) [1.0–719.7 ex]
- … **Ancestral Tiara** — 230 listings (230 priced) [1.0–719.7 ex]
- … **Rattling Sceptre** — 214 listings (214 priced) [1.0–1.3 ex]
- … **Heavy Belt** — 213 listings (213 priced) [0.5–719.7 ex]
- … **Long Belt** — 211 listings (211 priced) [1.0–719.7 ex]
- … **Siege Crossbow** — 210 listings (210 priced) [0.3–719.7 ex]
- … **Gemini Bow** — 202 listings (202 priced) [1.0–719.7 ex]
- … **Prismatic Ring** — 200 listings (200 priced) [0.4–719.7 ex]
- … **Double Belt** — 192 listings (192 priced) [0.8–719.7 ex]
- … **Rawhide Belt** — 192 listings (192 priced) [1.0–719.7 ex]
- … **Stellar Amulet** — 191 listings (191 priced) [1.0–719.7 ex]
- … **Amethyst Ring** — 189 listings (189 priced) [1.0–719.7 ex]
- … **Lapis Amulet** — 186 listings (186 priced) [0.6–719.7 ex]

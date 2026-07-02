# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-02T22:06:03+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **22570** (22570 priced in exalted)
- Distinct bases: 580 · distinct mods: 773 · mod rows: 123620
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-02T21:49:15+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×43.02** (median |log error| 3.7617)
- Within ±30% of asking price: **29%**
- Skill vs constant-price guess: **+0.02** (> 0 = the mods carry signal)
- Calibration: 71% of actuals above prediction (target ≈ 75%)

| group | n_test | ×err | ±30% | skill |
|---|---|---|---|---|
| accessory.belt | 405 | ×83.55 | 27% | +0.13 |
| armour.gloves | 382 | ×326.46 | 18% | +0.05 |
| armour.chest | 373 | ×205.90 | 11% | +0.09 |
| weapon.wand | 337 | ×380.09 | 19% | +0.08 |
| accessory.ring | 330 | ×25.02 | 3% | -0.77 |
| armour.boots | 327 | ×12.55 | 27% | +0.05 |
| armour.helmet | 314 | ×48.00 | 27% | +0.04 |
| weapon.crossbow | 292 | ×230.49 | 16% | +0.11 |
| weapon.bow | 291 | ×181.51 | 16% | +0.07 |
| accessory.amulet | 288 | ×28.72 | 4% | -0.13 |
| other | 241 | ×1.00 | 68% | +0.02 |
| weapon.sceptre | 125 | ×1.00 | 100% | +0.00 |
| weapon.spear | 123 | ×1.00 | 100% | +0.00 |
| armour.focus | 120 | ×1.00 | 99% | -0.00 |
| armour.shield | 84 | ×1.00 | 100% | n/a |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### accessory.belt — n=1909, R²=-0.834

intercept: `2.0347`  ·  log_price: True  ·  ilvl: `-0.02482`  ·  n_mods: `-0.01216`  ·  n_top_tier: `-0.05671`  ·  corrupted: `0.05185`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 0.26257 |
| `explicit.stat_3299347043@T1` | 0.24745 |
| `pseudo.total_ele_res>=80` | 0.22009 |
| `explicit.stat_3299347043@T2` | 0.20325 |
| `explicit.stat_174664100` | 0.13187 |
| `explicit.stat_1014398896` | 0.12346 |
| `explicit.stat_3811191316` | 0.11279 |
| `explicit.stat_2881298780@T2` | 0.10451 |
| `explicit.stat_3585532255@T1` | 0.09958 |
| `explicit.stat_3372524247@T1` | 0.09781 |
| `explicit.stat_2881298780@T1` | 0.09664 |
| `explicit.stat_809229260@T1` | 0.09512 |

### armour.boots — n=1857, R²=-0.6567

intercept: `7.8704`  ·  log_price: True  ·  ilvl: `-0.09795`  ·  n_mods: `-0.06186`  ·  n_top_tier: `0.55651`  ·  corrupted: `-0.09124`  ·  n_sockets: `0.12623`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 5.55884 |
| `explicit.stat_2339757871@T1` | -0.95482 |
| `explicit.stat_3261801346@T2` | -0.86516 |
| `explicit.stat_3484657501@T2` | -0.75834 |
| `explicit.stat_3321629045@T2` | -0.75308 |
| `explicit.stat_124859000@T2` | -0.71824 |
| `explicit.stat_2923486259@T2` | -0.71572 |
| `explicit.stat_2923486259@T1` | -0.71105 |
| `explicit.stat_3484657501@T1` | -0.70905 |
| `explicit.stat_2451402625@T1` | -0.70482 |
| `explicit.stat_2160282525@T2` | -0.66069 |
| `explicit.stat_2451402625@T2` | -0.65748 |

### armour.chest — n=1837, R²=-0.7052

intercept: `8.4549`  ·  log_price: True  ·  ilvl: `-0.10750`  ·  n_mods: `-0.05516`  ·  n_top_tier: `0.51292`  ·  corrupted: `-2.27682`  ·  n_sockets: `0.17571`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 6.14068 |
| `explicit.stat_3981240776@T1` | 2.39514 |
| `explicit.stat_3372524247@T1` | 2.20438 |
| `explicit.stat_3299347043@T1` | 1.98152 |
| `explicit.stat_2339757871@T2` | -1.23678 |
| `explicit.stat_2339757871@T1` | -1.20765 |
| `explicit.stat_3261801346@T1` | -1.04337 |
| `explicit.stat_3301100256@T2` | -0.93904 |
| `explicit.stat_1671376347@T1` | 0.78181 |
| `explicit.stat_124859000@T2` | -0.77306 |
| `explicit.stat_124859000@T1` | -0.77191 |
| `explicit.stat_986397080@T1` | -0.75523 |

### armour.helmet — n=1836, R²=-0.8916

intercept: `7.5199`  ·  log_price: True  ·  ilvl: `-0.09523`  ·  n_mods: `-0.04743`  ·  n_top_tier: `0.17836`  ·  corrupted: `0.61906`  ·  n_sockets: `-0.01189`

| stat_id | coef |
|---|---|
| `desecrated.stat_3917489142@T1` | -5.31748 |
| `explicit.stat_4220027924@T1` | 2.41514 |
| `desecrated.stat_3299347043@T2` | 1.92148 |
| `desecrated.stat_4015621042@T2` | -1.88301 |
| `crafted.stat_3917489142@T1` | 1.81969 |
| `explicit.stat_1263695895@T1` | -0.57561 |
| `explicit.stat_1263695895@T2` | -0.53637 |
| `explicit.stat_2923486259@T2` | -0.47625 |
| `explicit.stat_3917489142@T2` | -0.46536 |
| `explicit.stat_2339757871@T1` | 0.46536 |
| `desecrated.stat_3917489142` | 0.44171 |
| `explicit.stat_3484657501@T1` | -0.43224 |

### armour.gloves — n=1800, R²=-0.8011

intercept: `7.7365`  ·  log_price: True  ·  ilvl: `-0.09938`  ·  n_mods: `0.01868`  ·  n_top_tier: `0.72630`  ·  corrupted: `2.28248`  ·  n_sockets: `0.02078`

| stat_id | coef |
|---|---|
| `explicit.stat_3372524247@T1` | 4.42077 |
| `explicit.stat_4067062424@T2` | 4.39500 |
| `explicit.stat_2451402625@T2` | -1.14925 |
| `explicit.stat_1754445556@T2` | 1.14102 |
| `explicit.stat_124859000@T2` | -1.05128 |
| `explicit.stat_1671376347@T2` | -1.01213 |
| `explicit.stat_3484657501@T2` | -0.91146 |
| `explicit.stat_124859000@T1` | -0.90128 |
| `explicit.stat_2797971005@T2` | -0.88597 |
| `explicit.stat_2339757871@T1` | -0.87022 |
| `explicit.stat_2923486259@T2` | -0.86949 |
| `explicit.stat_1368271171@T1` | -0.84601 |

### accessory.amulet — n=1667, R²=-0.6629

intercept: `10.7352`  ·  log_price: True  ·  ilvl: `-0.10461`  ·  n_mods: `-0.65963`  ·  n_top_tier: `1.56037`  ·  corrupted: `-2.57662`  ·  n_sockets: `-1.28743`

| stat_id | coef |
|---|---|
| `explicit.stat_328541901@T1` | -5.75415 |
| `explicit.stat_2748665614@T2` | -5.34148 |
| `explicit.stat_4220027924@T2` | -4.16704 |
| `explicit.stat_2482852589@T1` | -3.83052 |
| `explicit.stat_2748665614@T1` | -3.77258 |
| `explicit.stat_803737631@T1` | -3.74889 |
| `explicit.stat_803737631@T2` | -3.40886 |
| `explicit.stat_3325883026@T2` | -3.36366 |
| `explicit.stat_2866361420@T2` | -3.24018 |
| `explicit.stat_2482852589@T2` | -3.20338 |
| `explicit.stat_983749596@T1` | -3.04767 |
| `explicit.stat_1050105434@T1` | -2.88559 |

### weapon.wand — n=1652, R²=-0.8512

intercept: `7.5991`  ·  log_price: True  ·  ilvl: `-0.09499`  ·  n_mods: `-0.02272`  ·  n_top_tier: `0.29943`  ·  corrupted: `0.38929`  ·  n_sockets: `-0.06253`

| stat_id | coef |
|---|---|
| `explicit.stat_1600707273@T1` | 6.24450 |
| `explicit.stat_591105508@T1` | 5.90898 |
| `explicit.stat_4226189338@T1` | 5.79778 |
| `explicit.stat_2254480358@T1` | 5.73148 |
| `explicit.stat_124131830@T1` | 5.14522 |
| `explicit.stat_274716455@T2` | 5.14280 |
| `explicit.stat_2231156303@T1` | 4.36352 |
| `explicit.stat_1545858329@T1` | 3.10563 |
| `crafted.stat_124131830` | 1.64360 |
| `explicit.stat_2974417149@T1` | 1.02365 |
| `explicit.stat_124131830@T2` | -0.62726 |
| `explicit.stat_1263695895@T2` | -0.50370 |

### accessory.ring — n=1524, R²=-0.3087

intercept: `8.3173`  ·  log_price: True  ·  ilvl: `-0.05158`  ·  n_mods: `-0.37510`  ·  n_top_tier: `0.20609`  ·  corrupted: `1.69363`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T2` | -4.64288 |
| `explicit.stat_3695891184@T1` | -2.81130 |
| `explicit.stat_1263695895@T1` | -2.60569 |
| `explicit.stat_3962278098@T1` | -2.11385 |
| `explicit.stat_1379411836@T1` | 2.06653 |
| `explicit.stat_3962278098@T2` | -1.84812 |
| `explicit.stat_2923486259@T1` | 1.80695 |
| `explicit.stat_1050105434@T1` | -1.77602 |
| `explicit.stat_1263695895@T2` | -1.62252 |
| `explicit.stat_2891184298@T1` | 1.55911 |
| `explicit.stat_2901986750@T2` | -1.50580 |
| `explicit.stat_3291658075@T1` | 1.47344 |

### weapon.bow — n=1431, R²=-0.745

intercept: `7.9565`  ·  log_price: True  ·  ilvl: `-0.09768`  ·  n_mods: `-0.09240`  ·  n_top_tier: `0.02701`  ·  corrupted: `-0.38710`  ·  n_sockets: `0.04473`

| stat_id | coef |
|---|---|
| `desecrated.stat_1200678966@T1` | -8.99861 |
| `explicit.stat_1037193709@T1` | 5.45564 |
| `desecrated.stat_210067635@T1` | 4.71709 |
| `explicit.stat_2463230181@T1` | 3.75237 |
| `explicit.stat_518292764@T1` | 3.53224 |
| `explicit.stat_3336890334@T1` | 2.64179 |
| `rune.stat_3885405204` | -2.51376 |
| `explicit.stat_1202301673@T1` | 2.49050 |
| `explicit.stat_210067635@T2` | 1.35139 |
| `explicit.stat_1509134228@T1` | 1.20065 |
| `crafted.stat_3035140377` | 0.94686 |
| `desecrated.stat_666077204@T1` | -0.82772 |

### weapon.crossbow — n=1405, R²=-0.781

intercept: `7.7664`  ·  log_price: True  ·  ilvl: `-0.09777`  ·  n_mods: `-0.01814`  ·  n_top_tier: `0.50536`  ·  corrupted: `-1.36020`  ·  n_sockets: `-0.02243`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 5.68832 |
| `crafted.stat_210067635@T2` | 4.93922 |
| `explicit.stat_3336890334@T1` | 4.85437 |
| `explicit.stat_709508406@T1` | 3.00301 |
| `explicit.stat_1980802737@T2` | 2.91668 |
| `explicit.stat_1980802737` | 2.91668 |
| `explicit.stat_1967051901@T2` | 2.60153 |
| `crafted.stat_3035140377` | 0.99942 |
| `explicit.stat_691932474@T1` | -0.80673 |
| `explicit.stat_691932474@T2` | -0.79416 |
| `explicit.stat_3695891184@T2` | -0.65530 |
| `explicit.stat_1940865751@T2` | -0.64498 |

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

### weapon.sceptre — n=648, R²=0.0

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

### weapon.spear — n=576, R²=0.0

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

### armour.focus — n=559, R²=0.0

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

### armour.shield — n=477, R²=0.0

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

- … **Dueling Wand** — 515 listings (515 priced) [1.0–719.7 ex]
- … **Obliterator Bow** — 413 listings (413 priced) [0.8–719.7 ex]
- … **Utility Belt** — 359 listings (359 priced) [1.0–719.7 ex]
- … **Siphoning Wand** — 311 listings (311 priced) [1.0–719.7 ex]
- … **Warmonger Bow** — 297 listings (297 priced) [1.0–719.7 ex]
- … **Galvanic Wand** — 287 listings (287 priced) [1.0–719.7 ex]
- … **Solar Amulet** — 286 listings (286 priced) [1.0–719.7 ex]
- … **Attuned Wand** — 276 listings (276 priced) [0.3–719.7 ex]
- … **Gold Amulet** — 276 listings (276 priced) [0.3–719.7 ex]
- … **Plate Belt** — 263 listings (263 priced) [1.0–719.7 ex]
- … **Trarthan Cannon** — 261 listings (261 priced) [0.7–719.7 ex]
- … **Withered Wand** — 260 listings (260 priced) [1.0–719.7 ex]
- … **Desolate Crossbow** — 249 listings (249 priced) [1.0–719.7 ex]
- … **Ancestral Tiara** — 248 listings (248 priced) [1.0–719.7 ex]
- … **Heavy Belt** — 227 listings (227 priced) [0.5–719.7 ex]
- … **Rattling Sceptre** — 227 listings (227 priced) [1.0–1.3 ex]
- … **Siege Crossbow** — 226 listings (226 priced) [0.3–719.7 ex]
- … **Long Belt** — 217 listings (217 priced) [1.0–719.7 ex]
- … **Gemini Bow** — 215 listings (215 priced) [1.0–719.7 ex]
- … **Prismatic Ring** — 211 listings (211 priced) [0.4–719.7 ex]
- … **Rawhide Belt** — 207 listings (207 priced) [1.0–719.7 ex]
- … **Amethyst Ring** — 203 listings (203 priced) [1.0–719.7 ex]
- … **Double Belt** — 203 listings (203 priced) [0.8–719.7 ex]
- … **Lapis Amulet** — 201 listings (201 priced) [0.6–719.7 ex]
- … **Stellar Amulet** — 198 listings (198 priced) [1.0–719.7 ex]

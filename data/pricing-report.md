# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-03T01:30:32+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **30033** (30033 priced in exalted)
- Distinct bases: 673 · distinct mods: 1124 · mod rows: 158804
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-03T01:18:41+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×31.32** (median |log error| 3.4444)
- Within ±30% of asking price: **29%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 70% of actuals above prediction (target ≈ 75%)

| group | n_test | ×err | ±30% | skill |
|---|---|---|---|---|
| armour.gloves | 507 | ×455.50 | 21% | +0.00 |
| accessory.belt | 484 | ×22.23 | 37% | +0.04 |
| armour.boots | 448 | ×4.61 | 28% | +0.06 |
| accessory.amulet | 448 | ×75.41 | 3% | +0.19 |
| armour.chest | 439 | ×35.64 | 15% | +0.04 |
| armour.helmet | 433 | ×187.54 | 28% | +0.03 |
| accessory.ring | 424 | ×20.85 | 3% | -1.53 |
| weapon.wand | 367 | ×142.68 | 23% | +0.09 |
| weapon.bow | 347 | ×26.25 | 25% | +0.08 |
| weapon.crossbow | 290 | ×113.06 | 19% | +0.10 |
| other | 289 | ×9.76 | 15% | +0.38 |
| weapon.sceptre | 144 | ×1.00 | 99% | +0.00 |
| armour.focus | 139 | ×1.00 | 100% | +0.00 |
| weapon.spear | 117 | ×1.00 | 100% | n/a |
| armour.shield | 114 | ×1.00 | 100% | n/a |
| armour.quiver | 42 | ×1.00 | 100% | n/a |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### accessory.belt — n=2495, R²=-0.8111

intercept: `2.1203`  ·  log_price: True  ·  ilvl: `-0.02603`  ·  n_mods: `-0.01200`  ·  n_top_tier: `-0.02338`  ·  corrupted: `0.03883`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 0.68484 |
| `pseudo.total_ele_res>=80` | 0.22796 |
| `explicit.stat_3299347043@T1` | 0.21501 |
| `explicit.stat_2639966148` | 0.21117 |
| `implicit.stat_731781020` | 0.20143 |
| `explicit.stat_174664100` | 0.15929 |
| `explicit.stat_3299347043@T2` | 0.15230 |
| `explicit.stat_1014398896` | 0.12157 |
| `explicit.stat_3811191316` | 0.10594 |
| `explicit.stat_3372524247@T1` | 0.09873 |
| `explicit.stat_3585532255@T1` | 0.07601 |
| `explicit.stat_4220027924@T1` | 0.07213 |

### armour.boots — n=2413, R²=-0.7008

intercept: `7.5258`  ·  log_price: True  ·  ilvl: `-0.09315`  ·  n_mods: `-0.04770`  ·  n_top_tier: `0.47580`  ·  corrupted: `0.17356`  ·  n_sockets: `0.03009`  ·  quality: `0.01358`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 5.71322 |
| `explicit.stat_3261801346@T2` | -0.83759 |
| `explicit.stat_2451402625@T1` | -0.68117 |
| `explicit.stat_124859000@T2` | -0.65209 |
| `explicit.stat_3321629045@T1` | -0.63465 |
| `explicit.stat_3484657501@T2` | -0.62828 |
| `explicit.stat_2923486259@T2` | -0.57585 |
| `explicit.stat_1062208444@T1` | -0.57396 |
| `explicit.stat_3261801346@T1` | -0.56765 |
| `explicit.stat_3321629045@T2` | -0.55690 |
| `explicit.stat_3484657501@T1` | -0.54874 |
| `explicit.stat_3299347043@T1` | -0.54364 |

### armour.chest — n=2376, R²=-0.8297

intercept: `8.1031`  ·  log_price: True  ·  ilvl: `-0.10328`  ·  n_mods: `-0.01434`  ·  n_top_tier: `0.58122`  ·  corrupted: `-1.41937`  ·  n_sockets: `0.05774`  ·  quality: `0.07967`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 7.30993 |
| `explicit.stat_3981240776@T1` | 3.47012 |
| `explicit.stat_1671376347@T1` | 2.94962 |
| `explicit.stat_2339757871@T1` | -2.86686 |
| `explicit.stat_2339757871@T2` | -2.51694 |
| `explicit.stat_3372524247@T1` | 1.49042 |
| `explicit.stat_4220027924@T1` | 1.13133 |
| `explicit.stat_2923486259@T2` | -0.96770 |
| `explicit.stat_3261801346@T1` | -0.96033 |
| `explicit.stat_3301100256@T2` | -0.86988 |
| `explicit.stat_915769802@T1` | -0.86614 |
| `explicit.stat_4052037485@T1` | -0.85660 |

### armour.helmet — n=2376, R²=-0.898

intercept: `7.5364`  ·  log_price: True  ·  ilvl: `-0.09607`  ·  n_mods: `-0.02819`  ·  n_top_tier: `0.67360`  ·  corrupted: `1.71698`  ·  n_sockets: `0.08109`  ·  quality: `-0.00341`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 7.57294 |
| `desecrated.stat_4015621042@T1` | -4.95584 |
| `explicit.stat_4220027924@T1` | 2.43964 |
| `explicit.stat_2923486259@T2` | -0.94438 |
| `explicit.stat_2923486259@T1` | -0.88835 |
| `explicit.stat_3261801346@T2` | -0.88333 |
| `explicit.stat_53045048@T2` | -0.84822 |
| `explicit.stat_3917489142@T2` | -0.82124 |
| `explicit.stat_3362812763@T2` | -0.79486 |
| `explicit.stat_3362812763@T1` | -0.74118 |
| `explicit.stat_1999113824@T1` | -0.74015 |
| `explicit.stat_587431675@T2` | -0.73632 |

### armour.gloves — n=2323, R²=-0.8803

intercept: `7.4985`  ·  log_price: True  ·  ilvl: `-0.09666`  ·  n_mods: `0.05197`  ·  n_top_tier: `0.35569`  ·  corrupted: `0.82168`  ·  n_sockets: `0.00687`  ·  quality: `-0.06464`

| stat_id | coef |
|---|---|
| `explicit.stat_4067062424@T2` | 3.79040 |
| `explicit.stat_3372524247@T1` | 2.79148 |
| `explicit.stat_1671376347@T1` | 2.50879 |
| `rune.stat_201332984` | 1.40848 |
| `explicit.stat_9187492@T1` | 0.90886 |
| `explicit.stat_9187492@T2` | -0.79309 |
| `explicit.stat_2451402625@T2` | -0.74702 |
| `explicit.stat_3321629045@T1` | -0.53966 |
| `explicit.stat_3321629045@T2` | -0.52872 |
| `explicit.stat_4052037485@T1` | -0.52002 |
| `explicit.stat_124859000@T2` | -0.48788 |
| `explicit.stat_3484657501@T2` | -0.48078 |

### accessory.amulet — n=2124, R²=-0.5667

intercept: `10.2696`  ·  log_price: True  ·  ilvl: `-0.10514`  ·  n_mods: `-0.71464`  ·  n_top_tier: `1.61594`  ·  corrupted: `-1.81226`  ·  n_sockets: `-0.43125`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -6.64614 |
| `explicit.stat_2923486259@T2` | -5.88556 |
| `explicit.stat_1050105434@T1` | -5.85227 |
| `explicit.stat_2748665614@T2` | -5.00819 |
| `explicit.stat_328541901@T1` | -4.56220 |
| `explicit.stat_983749596@T1` | -4.50061 |
| `explicit.stat_4220027924@T2` | -4.38259 |
| `explicit.stat_2482852589@T1` | -4.33384 |
| `explicit.stat_2482852589@T2` | -4.00707 |
| `explicit.stat_4080418644@T1` | -3.69942 |
| `explicit.stat_803737631@T2` | -3.33060 |
| `explicit.stat_1671376347@T2` | -3.26728 |

### other — n=2094, R²=0.362

intercept: `1.3814`  ·  log_price: True  ·  ilvl: `0.00486`  ·  n_mods: `-0.02883`  ·  n_top_tier: `0.21343`  ·  corrupted: `0.40570`  ·  n_sockets: `-0.05673`  ·  quality: `0.03331`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.77546 |
| `explicit.stat_124131830` | -0.60498 |
| `explicit.stat_4080418644@T1` | -0.59212 |
| `crafted.stat_124131830` | -0.49455 |
| `explicit.stat_915769802@T1` | -0.47272 |
| `explicit.stat_2974417149@T2` | -0.46660 |
| `explicit.stat_124131830@T2` | 0.45398 |
| `explicit.stat_3261801346@T1` | -0.41014 |
| `explicit.stat_915769802@T2` | -0.36292 |
| `explicit.stat_2974417149@T1` | 0.35283 |
| `explicit.stat_3372524247@T1` | -0.33928 |
| `explicit.stat_691932474@T2` | -0.33872 |

### weapon.wand — n=1989, R²=-0.906

intercept: `7.7255`  ·  log_price: True  ·  ilvl: `-0.09563`  ·  n_mods: `-0.06982`  ·  n_top_tier: `0.28446`  ·  corrupted: `-0.22804`  ·  n_sockets: `-0.03588`  ·  quality: `0.04599`

| stat_id | coef |
|---|---|
| `explicit.stat_1600707273@T1` | 6.12420 |
| `explicit.stat_2254480358@T1` | 6.06320 |
| `explicit.stat_1545858329@T1` | 5.94746 |
| `explicit.stat_591105508@T1` | 5.80074 |
| `explicit.stat_4226189338@T1` | 4.96372 |
| `explicit.stat_124131830@T1` | 4.87580 |
| `explicit.stat_274716455@T2` | 3.97915 |
| `explicit.stat_2974417149@T1` | 1.86951 |
| `crafted.stat_124131830` | 1.49911 |
| `explicit.stat_1263695895@T1` | -0.80728 |
| `explicit.stat_124131830@T2` | -0.78649 |
| `explicit.stat_1263695895@T2` | -0.70554 |

### accessory.ring — n=1936, R²=-0.2113

intercept: `7.2488`  ·  log_price: True  ·  ilvl: `-0.00908`  ·  n_mods: `-0.06142`  ·  n_top_tier: `0.15566`  ·  corrupted: `0.30737`  ·  n_sockets: `3.35568`  ·  quality: `0.03745`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T2` | -5.70248 |
| `explicit.stat_803737631@T2` | -4.41905 |
| `explicit.stat_1050105434@T1` | -4.31057 |
| `explicit.stat_3325883026@T1` | 3.50696 |
| `explicit.stat_3325883026@T2` | -2.31907 |
| `explicit.stat_2923486259@T2` | -1.79885 |
| `explicit.stat_2557965901@T1` | -1.17790 |
| `explicit.stat_707457662@T1` | 1.14785 |
| `explicit.stat_707457662@T2` | 1.09430 |
| `explicit.stat_3299347043@T1` | -1.01870 |
| `explicit.stat_1263695895@T1` | -1.01821 |
| `explicit.stat_3695891184@T1` | -0.93666 |

### weapon.bow — n=1645, R²=-0.7799

intercept: `8.1715`  ·  log_price: True  ·  ilvl: `-0.10059`  ·  n_mods: `-0.07616`  ·  n_top_tier: `-0.07712`  ·  corrupted: `1.76244`  ·  n_sockets: `0.06846`  ·  quality: `-0.03657`

| stat_id | coef |
|---|---|
| `desecrated.stat_1200678966@T1` | -7.47469 |
| `desecrated.stat_666077204@T1` | -5.92760 |
| `explicit.stat_1037193709@T1` | 5.68798 |
| `explicit.stat_518292764@T1` | 4.98051 |
| `explicit.stat_2463230181@T1` | 4.92370 |
| `explicit.stat_1202301673@T1` | 4.42766 |
| `desecrated.stat_210067635@T1` | 3.42357 |
| `rune.stat_3885405204` | -2.65145 |
| `explicit.stat_210067635@T2` | 1.84551 |
| `explicit.stat_1509134228@T1` | 1.65922 |
| `explicit.stat_1263695895@T1` | 1.14500 |
| `explicit.stat_1263695895@T2` | 0.89856 |

### weapon.crossbow — n=1583, R²=-0.8243

intercept: `8.2561`  ·  log_price: True  ·  ilvl: `-0.10387`  ·  n_mods: `-0.01863`  ·  n_top_tier: `0.53012`  ·  corrupted: `1.33090`  ·  n_sockets: `0.04492`  ·  quality: `0.08048`

| stat_id | coef |
|---|---|
| `desecrated.stat_2760344900@T1` | -14.96730 |
| `crafted.stat_210067635@T2` | -9.83255 |
| `explicit.stat_1037193709@T1` | 5.71159 |
| `explicit.stat_3336890334@T1` | 5.26485 |
| `explicit.stat_709508406@T1` | 4.94676 |
| `explicit.stat_1980802737@T2` | 2.82487 |
| `explicit.stat_1980802737` | 2.82487 |
| `desecrated.stat_3131442032@T1` | 1.16109 |
| `desecrated.stat_1365232741@T1` | 1.16109 |
| `crafted.stat_3035140377` | 1.06142 |
| `desecrated.stat_2760344900` | 0.99245 |
| `explicit.stat_691932474@T1` | -0.91174 |

### weapon.sceptre — n=743, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1798257884` | 0.00000 |
| `desecrated.stat_1050105434` | 0.00000 |
| `desecrated.stat_1798257884` | 0.00000 |
| `desecrated.stat_3984865854` | 0.00000 |
| `explicit.stat_101878827` | 0.00000 |
| `explicit.stat_101878827@T1` | 0.00000 |
| `explicit.stat_101878827@T2` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_1250712710` | 0.00000 |
| `explicit.stat_1250712710@T1` | 0.00000 |

### weapon.spear — n=649, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
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

### armour.focus — n=640, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1671376347` | 0.00000 |
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

### armour.shield — n=527, R²=0.0

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
| `explicit.stat_1301765461@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |

### jewel — n=327, R²=0.0169

intercept: `-1.8621`  ·  log_price: True  ·  ilvl: `0.02676`  ·  n_mods: `0.49547`  ·  n_top_tier: `0.06086`  ·  corrupted: `-1.55256`

| stat_id | coef |
|---|---|
| `explicit.stat_1310194496@T1` | 9.00526 |
| `explicit.stat_2011656677@T1` | 8.98941 |
| `explicit.stat_680068163@T1` | 8.72909 |
| `explicit.stat_3028809864@T1` | -8.25071 |
| `explicit.stat_1782086450@T1` | -7.22415 |
| `explicit.stat_1852872083@T1` | 7.11883 |
| `explicit.stat_2194114101@T1` | 6.98029 |
| `explicit.stat_2843214518@T1` | 6.71585 |
| `explicit.stat_293638271@T1` | 6.19114 |
| `explicit.stat_1569101201@T1` | 5.86778 |
| `explicit.stat_2653955271@T1` | 5.76844 |
| `explicit.stat_1772247089@T1` | -5.68956 |

### armour.quiver — n=194, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1241625305` | 0.00000 |
| `explicit.stat_1241625305@T1` | 0.00000 |
| `explicit.stat_1241625305@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | -0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1573130764` | 0.00000 |
| `explicit.stat_1573130764@T1` | 0.00000 |
| `explicit.stat_1573130764@T2` | 0.00000 |
| `explicit.stat_1754445556` | 0.00000 |

### weapon.staff — n=162, R²=-0.0175

intercept: `0.0001`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3015669065@T2` | -0.00002 |
| `explicit.stat_293638271@T1` | 0.00002 |
| `explicit.stat_3695891184@T1` | -0.00002 |
| `explicit.stat_3695891184@T2` | -0.00001 |
| `explicit.stat_3015669065@T1` | -0.00001 |
| `explicit.stat_2505884597@T2` | -0.00001 |
| `explicit.stat_1368271171@T2` | 0.00001 |
| `explicit.stat_3639275092@T2` | -0.00001 |
| `explicit.stat_1263695895@T1` | -0.00001 |
| `explicit.stat_789117908@T2` | 0.00001 |
| `explicit.stat_2974417149@T2` | -0.00001 |
| `explicit.stat_328541901@T2` | 0.00001 |

### weapon.warstaff — n=162, R²=-0.0481

intercept: `0.0002`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_387439868@T1` | 0.00003 |
| `explicit.stat_328541901@T2` | -0.00003 |
| `explicit.stat_387439868@T2` | 0.00003 |
| `explicit.stat_691932474@T2` | 0.00002 |
| `explicit.stat_3261801346@T1` | -0.00002 |
| `explicit.stat_3261801346@T2` | -0.00002 |
| `explicit.stat_3639275092@T2` | -0.00002 |
| `explicit.stat_691932474@T1` | 0.00001 |
| `explicit.stat_3336890334@T2` | 0.00001 |
| `explicit.stat_1509134228@T2` | -0.00001 |
| `explicit.stat_55876295@T1` | 0.00001 |
| `explicit.stat_55876295@T2` | 0.00001 |

### flask.charm — n=148, R²=-0.19

intercept: `0.2417`  ·  log_price: True  ·  ilvl: `0.00161`  ·  n_mods: `-0.03304`  ·  n_top_tier: `-0.07297`  ·  quality: `-0.00637`

| stat_id | coef |
|---|---|
| `implicit.stat_3676540188` | -1.30525 |
| `explicit.stat_1873752457` | 0.30049 |
| `implicit.stat_3854901951` | 0.08211 |
| `implicit.stat_3699444296` | -0.05798 |
| `implicit.stat_2016937536` | 0.03894 |
| `implicit.stat_1412682799` | -0.02769 |
| `implicit.stat_2994271459` | 0.02413 |
| `implicit.stat_2778646494` | 0.01095 |
| `explicit.stat_2566921799` | -0.00454 |
| `explicit.stat_828533480` | 0.00311 |
| `explicit.stat_2541588185` | 0.00280 |
| `explicit.stat_2365392475` | 0.00183 |

### weapon.twomace — n=145, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |
| `explicit.stat_1940865751` | 0.00000 |
| `explicit.stat_1940865751@T2` | 0.00000 |
| `explicit.stat_210067635` | 0.00000 |
| `explicit.stat_2694482655` | 0.00000 |
| `explicit.stat_3336890334` | 0.00000 |

## Coverage (listings per base)

- … **Dueling Wand** — 634 listings (634 priced) [1.0–719.7 ex]
- … **Utility Belt** — 617 listings (617 priced) [1.0–737.3 ex]
- … **Obliterator Bow** — 490 listings (490 priced) [0.5–719.7 ex]
- … **Stellar Amulet** — 394 listings (394 priced) [0.4–737.3 ex]
- … **Siphoning Wand** — 369 listings (369 priced) [1.0–719.7 ex]
- … **Solar Amulet** — 367 listings (367 priced) [1.0–737.3 ex]
- … **Warmonger Bow** — 356 listings (356 priced) [1.0–719.7 ex]
- … **Plate Belt** — 352 listings (352 priced) [1.0–737.3 ex]
- … **Gold Amulet** — 348 listings (348 priced) [0.3–737.3 ex]
- … **Galvanic Wand** — 341 listings (341 priced) [1.0–719.7 ex]
- … **Attuned Wand** — 337 listings (337 priced) [0.3–719.7 ex]
- … **Ancestral Tiara** — 334 listings (334 priced) [1.0–737.3 ex]
- … **Heavy Belt** — 308 listings (308 priced) [0.5–737.3 ex]
- … **Withered Wand** — 308 listings (308 priced) [1.0–719.7 ex]
- … **Long Belt** — 293 listings (293 priced) [1.0–737.3 ex]
- … **Trarthan Cannon** — 292 listings (292 priced) [0.7–719.7 ex]
- … **Amethyst Ring** — 286 listings (286 priced) [1.0–737.3 ex]
- … **Prismatic Ring** — 283 listings (283 priced) [0.4–737.3 ex]
- … **Rawhide Belt** — 276 listings (276 priced) [1.0–737.3 ex]
- … **Lapis Amulet** — 273 listings (273 priced) [0.6–737.3 ex]
- … **Amber Amulet** — 272 listings (272 priced) [0.3–737.3 ex]
- … **Desolate Crossbow** — 272 listings (272 priced) [1.0–719.7 ex]
- … **Double Belt** — 257 listings (257 priced) [0.8–737.3 ex]
- … **Rattling Sceptre** — 257 listings (257 priced) [1.0–50.0 ex]
- … **Gold Ring** — 255 listings (255 priced) [0.7–737.3 ex]

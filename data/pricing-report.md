# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-19T19:24:12+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **660592** (658535 priced in exalted)
- Distinct bases: 996 · distinct mods: 3286 · mod rows: 3128611
- Sold signals: **24533** sold · 376245 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-19T19:11:10+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×20.94** (median |log error| 3.0418)
- Within ±30% of asking price: **13%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.16** · typical error ×52.77 · ±30% 5% · n=96306
- Premium segment (60ex+): skill **+0.16** · typical error ×218.24 · ±30% 0% · n=64798

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 13947 | ×56.13 | 21% | +0.03 | +0.06 |
| jewel | 13332 | ×10.36 | 5% | +0.11 | +0.12 |
| accessory.amulet | 12565 | ×44.72 | 18% | +0.04 | +0.03 |
| accessory.belt | 9124 | ×13.18 | 5% | +0.01 | +0.03 |
| armour.chest | 8832 | ×15.73 | 11% | +0.11 | +0.13 |
| armour.helmet | 8604 | ×17.07 | 6% | +0.13 | +0.16 |
| armour.boots | 7944 | ×23.94 | 11% | +0.13 | +0.14 |
| armour.gloves | 7831 | ×25.34 | 8% | +0.13 | +0.13 |
| other | 7761 | ×5.55 | 40% | +0.09 | +0.15 |
| weapon.wand | 4708 | ×41.56 | 16% | +0.09 | +0.10 |
| weapon.bow | 3696 | ×25.50 | 12% | +0.15 | +0.16 |
| weapon.crossbow | 3504 | ×26.14 | 15% | +0.11 | +0.15 |
| weapon.warstaff | 2366 | ×17.25 | 7% | +0.21 | +0.21 |
| weapon.staff | 2251 | ×20.41 | 6% | +0.18 | +0.16 |
| weapon.sceptre | 2216 | ×21.37 | 5% | +0.13 | +0.13 |
| weapon.spear | 1765 | ×20.12 | 8% | +0.12 | +0.13 |
| armour.focus | 1432 | ×19.57 | 6% | +0.11 | +0.12 |
| armour.quiver | 1378 | ×21.38 | 7% | +0.16 | +0.17 |
| armour.shield | 1140 | ×16.25 | 7% | +0.09 | +0.10 |
| flask.charm | 1120 | ×12.77 | 28% | -0.00 | +0.02 |
| weapon.twomace | 1056 | ×8.88 | 8% | +0.12 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=72055, R²=-0.9703

intercept: `-1.9160`  ·  log_price: True  ·  ilvl: `0.02497`  ·  n_mods: `0.90803`  ·  n_top_tier: `-0.35272`  ·  corrupted: `0.34315`  ·  quality: `-0.00606`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.62944 |
| `explicit.stat_3485067555@T1` | 2.33549 |
| `explicit.stat_3374165039@T1` | -1.97062 |
| `explicit.stat_1594812856@T1` | 1.75008 |
| `explicit.stat_1569101201@T1` | -1.62644 |
| `explicit.stat_4147897060@T1` | -1.55941 |
| `explicit.stat_2301718443@T1` | 1.53332 |
| `explicit.stat_2523933828@T1` | -1.40528 |
| `explicit.stat_3473929743@T1` | -1.38456 |
| `explicit.stat_3780644166@T1` | -1.32014 |
| `explicit.stat_1805182458@T1` | -1.24899 |
| `explicit.stat_1697447343@T1` | -1.24720 |

### accessory.ring — n=63549, R²=-2.0305

intercept: `3.2799`  ·  log_price: True  ·  ilvl: `-0.04059`  ·  n_mods: `0.00098`  ·  n_top_tier: `1.13242`  ·  corrupted: `0.01239`  ·  n_sockets: `1.83228`  ·  quality: `0.02298`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.16115 |
| `explicit.stat_2231156303@T1` | -1.15320 |
| `explicit.stat_1573130764@T2` | -1.15270 |
| `explicit.stat_803737631@T1` | -1.15156 |
| `explicit.stat_4220027924@T2` | -1.15131 |
| `explicit.stat_4080418644@T1` | -1.14534 |
| `explicit.stat_736967255@T2` | -1.14201 |
| `explicit.stat_789117908@T1` | -1.14163 |
| `explicit.stat_789117908@T2` | -1.14135 |
| `explicit.stat_3291658075@T2` | -1.14037 |
| `explicit.stat_3261801346@T1` | -1.13997 |
| `explicit.stat_3325883026@T1` | -1.13964 |

### other — n=62856, R²=-0.5988

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `0.36837`  ·  corrupted: `0.31617`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.57050 |
| `implicit.stat_2219129443` | 0.37297 |
| `explicit.stat_2482852589@T1` | 0.30789 |
| `explicit.stat_3299347043@T1` | -0.27494 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_4041853756` | 0.23024 |
| `explicit.stat_3291658075@T1` | -0.16182 |
| `explicit.stat_2891184298@T1` | 0.14725 |
| `explicit.stat_2968503605@T1` | -0.12533 |
| `explicit.stat_3141070085@T1` | -0.12292 |
| `explicit.stat_2106365538@T1` | -0.11094 |
| `explicit.stat_789117908@T1` | -0.10233 |

### accessory.amulet — n=57424, R²=-2.1561

intercept: `3.7019`  ·  log_price: True  ·  ilvl: `-0.04581`  ·  n_mods: `-0.01970`  ·  n_top_tier: `1.52216`  ·  corrupted: `0.06133`  ·  n_sockets: `-0.13985`  ·  quality: `0.03906`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -2.12695 |
| `explicit.stat_3299347043@T2` | -1.89888 |
| `explicit.stat_587431675@T2` | -1.66033 |
| `explicit.stat_803737631@T1` | -1.61848 |
| `explicit.stat_2974417149@T1` | -1.61655 |
| `explicit.stat_2866361420@T2` | -1.58815 |
| `explicit.stat_2974417149@T2` | -1.58057 |
| `explicit.stat_1050105434@T2` | -1.57076 |
| `explicit.stat_2866361420@T1` | -1.56879 |
| `explicit.stat_803737631@T2` | -1.56815 |
| `explicit.stat_472520716@T2` | -1.55408 |
| `explicit.stat_1671376347@T2` | -1.55311 |

### accessory.belt — n=41878, R²=-0.7173

intercept: `6.6791`  ·  log_price: True  ·  ilvl: `-0.05430`  ·  n_mods: `-0.42237`  ·  n_top_tier: `0.81192`  ·  corrupted: `0.87816`  ·  n_sockets: `0.27537`

| stat_id | coef |
|---|---|
| `explicit.stat_2881298780@T1` | -1.35411 |
| `explicit.stat_51994685@T1` | -1.11733 |
| `explicit.stat_3299347043@T1` | -1.07976 |
| `explicit.stat_1570770415@T2` | -1.03789 |
| `explicit.stat_3299347043@T2` | -0.95505 |
| `explicit.stat_1570770415@T1` | -0.92180 |
| `explicit.stat_3372524247@T2` | -0.90580 |
| `explicit.stat_809229260@T1` | -0.88627 |
| `explicit.stat_809229260@T2` | -0.88338 |
| `explicit.stat_4080418644@T1` | -0.84863 |
| `explicit.stat_2881298780@T2` | -0.83663 |
| `explicit.stat_644456512@T1` | -0.83532 |

### armour.chest — n=41491, R²=-1.3801

intercept: `4.0148`  ·  log_price: True  ·  ilvl: `-0.04853`  ·  n_mods: `-0.06488`  ·  n_top_tier: `0.41131`  ·  corrupted: `0.18856`  ·  n_sockets: `0.09363`  ·  quality: `0.05695`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.94384 |
| `explicit.stat_3981240776@T1` | 0.88758 |
| `explicit.stat_2339757871@T2` | -0.86587 |
| `explicit.stat_986397080@T2` | -0.79801 |
| `explicit.stat_986397080@T1` | -0.74938 |
| `explicit.stat_2339757871@T1` | -0.69040 |
| `explicit.stat_3484657501@T1` | -0.60960 |
| `explicit.stat_1692879867@T2` | -0.58218 |
| `explicit.stat_3372524247@T1` | 0.56502 |
| `explicit.stat_2451402625@T1` | -0.54474 |
| `explicit.stat_3033371881@T1` | 0.52519 |
| `explicit.stat_915769802@T2` | -0.49614 |

### armour.helmet — n=40350, R²=-1.1443

intercept: `3.6439`  ·  log_price: True  ·  ilvl: `-0.04554`  ·  n_mods: `-0.07737`  ·  n_top_tier: `0.46744`  ·  corrupted: `0.61017`  ·  n_sockets: `0.19089`  ·  quality: `0.05106`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.34761 |
| `crafted.stat_3917489142@T1` | -2.06072 |
| `explicit.stat_3917489142@T2` | -1.14988 |
| `explicit.stat_1999113824@T1` | -0.85775 |
| `explicit.stat_3321629045@T2` | -0.82419 |
| `explicit.stat_3917489142@T1` | -0.80309 |
| `explicit.stat_1263695895@T1` | -0.71507 |
| `explicit.stat_2162097452@T2` | -0.70988 |
| `explicit.stat_2923486259@T1` | 0.70645 |
| `explicit.stat_803737631@T1` | -0.69089 |
| `explicit.stat_803737631@T2` | -0.68547 |
| `explicit.stat_1999113824@T2` | -0.63831 |

### armour.boots — n=37525, R²=-1.3888

intercept: `4.2149`  ·  log_price: True  ·  ilvl: `-0.05120`  ·  n_mods: `-0.06332`  ·  n_top_tier: `0.57250`  ·  corrupted: `0.14366`  ·  n_sockets: `0.13578`  ·  quality: `0.05255`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.55923 |
| `explicit.stat_2339757871@T1` | -1.25991 |
| `crafted.stat_3917489142@T1` | 1.10049 |
| `explicit.stat_2923486259@T2` | -0.92178 |
| `explicit.stat_3299347043@T1` | -0.89548 |
| `explicit.stat_3917489142@T2` | -0.79898 |
| `explicit.stat_2160282525@T1` | -0.74239 |
| `explicit.stat_1999113824@T2` | -0.71560 |
| `explicit.stat_1062208444@T2` | -0.71087 |
| `explicit.stat_1874553720@T1` | -0.70384 |
| `explicit.stat_4052037485@T2` | -0.69596 |
| `explicit.stat_3484657501@T2` | -0.69181 |

### armour.gloves — n=36485, R²=-1.2899

intercept: `3.8574`  ·  log_price: True  ·  ilvl: `-0.04988`  ·  n_mods: `-0.05658`  ·  n_top_tier: `0.69792`  ·  corrupted: `0.06061`  ·  n_sockets: `0.23772`  ·  quality: `0.04708`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 3.04985 |
| `explicit.stat_2923486259@T1` | -1.37953 |
| `explicit.stat_3321629045@T2` | -1.16699 |
| `explicit.stat_3484657501@T2` | -1.16162 |
| `explicit.stat_3484657501@T1` | -1.08229 |
| `explicit.stat_803737631@T2` | -1.01311 |
| `explicit.stat_4052037485@T1` | -0.88175 |
| `explicit.stat_124859000@T2` | -0.87419 |
| `explicit.stat_3321629045@T1` | -0.83239 |
| `explicit.stat_3639275092@T1` | -0.82926 |
| `explicit.stat_4052037485@T2` | -0.81048 |
| `explicit.stat_124859000@T1` | -0.77632 |

### weapon.wand — n=21997, R²=-2.0099

intercept: `3.7014`  ·  log_price: True  ·  ilvl: `-0.04602`  ·  n_mods: `-0.04638`  ·  n_top_tier: `0.43420`  ·  corrupted: `0.00883`  ·  n_sockets: `0.05804`  ·  quality: `0.01933`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -3.07603 |
| `explicit.stat_1545858329@T1` | 2.46236 |
| `explicit.stat_2254480358@T1` | 2.41357 |
| `explicit.stat_124131830@T1` | 2.05815 |
| `explicit.stat_591105508@T1` | 1.91709 |
| `explicit.stat_4226189338@T1` | 1.89108 |
| `explicit.stat_736967255@T2` | 1.77079 |
| `crafted.stat_124131830` | 1.24969 |
| `explicit.stat_2254480358@T2` | 0.98853 |
| `explicit.stat_4226189338@T2` | 0.94050 |
| `explicit.stat_1600707273@T1` | 0.88060 |
| `explicit.stat_1263695895@T2` | -0.80091 |

### flask.charm — n=18247, R²=-0.6283

intercept: `0.1104`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.36682`  ·  corrupted: `1.59690`  ·  quality: `0.00280`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.77912 |
| `explicit.stat_1056492907` | 2.67685 |
| `explicit.stat_3246948616` | 1.51909 |
| `explicit.stat_828533480@T2` | -1.36685 |
| `explicit.stat_1120862500@T2` | -1.36683 |
| `explicit.stat_1873752457@T2` | -1.36682 |
| `explicit.stat_3196823591@T2` | -1.36677 |
| `explicit.stat_2365392475@T2` | -1.36677 |
| `explicit.stat_2676834156@T2` | -1.36666 |
| `explicit.stat_388617051@T2` | -1.36656 |
| `explicit.stat_1873752457@T1` | -1.36656 |
| `explicit.stat_828533480@T1` | -1.36583 |

### weapon.bow — n=17524, R²=-1.7127

intercept: `3.8281`  ·  log_price: True  ·  ilvl: `-0.04431`  ·  n_mods: `-0.11090`  ·  n_top_tier: `0.61743`  ·  corrupted: `0.49719`  ·  n_sockets: `0.08951`  ·  quality: `0.02987`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.60545 |
| `explicit.stat_3336890334@T1` | 1.30301 |
| `crafted.stat_3035140377` | 1.26161 |
| `desecrated.stat_666077204@T1` | 1.17101 |
| `explicit.stat_1263695895@T1` | -1.04690 |
| `explicit.stat_709508406@T1` | 0.93909 |
| `explicit.stat_2463230181@T2` | -0.91995 |
| `explicit.stat_1263695895@T2` | -0.91554 |
| `explicit.stat_3639275092@T1` | -0.76102 |
| `explicit.stat_3695891184@T2` | -0.75337 |
| `explicit.stat_1368271171@T2` | -0.73785 |
| `explicit.stat_3639275092@T2` | -0.73278 |

### weapon.crossbow — n=16471, R²=-1.7725

intercept: `3.9121`  ·  log_price: True  ·  ilvl: `-0.04724`  ·  n_mods: `-0.07480`  ·  n_top_tier: `0.46732`  ·  corrupted: `0.08753`  ·  n_sockets: `0.09724`  ·  quality: `0.02714`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.48150 |
| `explicit.stat_1202301673@T1` | 1.38266 |
| `explicit.stat_1980802737` | 1.30681 |
| `explicit.stat_2250681686@T2` | -1.01169 |
| `explicit.stat_2250681686` | 0.80806 |
| `crafted.stat_3035140377` | 0.77843 |
| `explicit.stat_3336890334@T2` | -0.68528 |
| `explicit.stat_3336890334@T1` | -0.67662 |
| `explicit.stat_1509134228@T2` | -0.61762 |
| `explicit.stat_1037193709@T1` | -0.60969 |
| `explicit.stat_1263695895@T2` | -0.59060 |
| `explicit.stat_1037193709@T2` | -0.58198 |

### weapon.warstaff — n=11260, R²=-0.3398

intercept: `-11.0545`  ·  log_price: True  ·  ilvl: `0.14820`  ·  n_mods: `-0.21068`  ·  n_top_tier: `0.32786`  ·  corrupted: `0.42459`  ·  n_sockets: `0.16785`  ·  quality: `0.05861`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.26310 |
| `explicit.stat_328541901@T1` | -0.87033 |
| `desecrated.stat_3291658075@T1` | -0.82056 |
| `desecrated.stat_473429811@T1` | -0.82056 |
| `explicit.stat_1037193709@T1` | 0.76959 |
| `desecrated.stat_9187492` | 0.76203 |
| `explicit.stat_1509134228@T1` | 0.73553 |
| `explicit.stat_328541901@T2` | -0.73220 |
| `explicit.stat_1368271171@T1` | -0.69651 |
| `rune.stat_243313994` | 0.69311 |
| `explicit.stat_691932474@T2` | -0.67557 |
| `explicit.stat_748522257@T2` | 0.53600 |

### weapon.staff — n=10659, R²=-0.3732

intercept: `-15.5169`  ·  log_price: True  ·  ilvl: `0.19992`  ·  n_mods: `-0.08659`  ·  n_top_tier: `0.47025`  ·  corrupted: `0.88140`  ·  n_sockets: `0.17572`  ·  quality: `0.03644`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.33922 |
| `explicit.stat_591105508@T1` | 2.16487 |
| `explicit.stat_1545858329@T1` | 1.80832 |
| `explicit.stat_124131830@T1` | 1.56600 |
| `explicit.stat_293638271@T2` | -1.28811 |
| `explicit.stat_1600707273@T1` | 1.09839 |
| `explicit.stat_2254480358@T1` | 1.04768 |
| `explicit.stat_473429811@T2` | -0.79215 |
| `explicit.stat_2254480358@T2` | 0.68527 |
| `explicit.stat_591105508@T2` | 0.67657 |
| `rune.stat_124131830` | 0.65550 |
| `explicit.stat_4226189338@T2` | 0.59015 |

### weapon.sceptre — n=10479, R²=-0.3388

intercept: `-20.9731`  ·  log_price: True  ·  ilvl: `0.26821`  ·  n_mods: `0.02781`  ·  n_top_tier: `0.26740`  ·  corrupted: `0.02238`  ·  n_sockets: `0.20521`  ·  quality: `0.02754`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.32590 |
| `explicit.stat_3057012405@T1` | 1.45007 |
| `explicit.stat_1263695895@T2` | -1.12053 |
| `explicit.stat_2162097452@T2` | 1.10074 |
| `explicit.stat_1263695895@T1` | -0.95507 |
| `explicit.stat_2854751904@T2` | -0.77335 |
| `explicit.stat_1250712710@T2` | 0.75476 |
| `explicit.stat_101878827@T2` | 0.74417 |
| `explicit.stat_1798257884@T2` | 0.72986 |
| `explicit.stat_101878827@T1` | 0.68544 |
| `explicit.stat_849987426@T1` | 0.61059 |
| `explicit.stat_289128254@T1` | 0.57946 |

### weapon.spear — n=8435, R²=-0.3755

intercept: `-13.5029`  ·  log_price: True  ·  ilvl: `0.18603`  ·  n_mods: `-0.18624`  ·  n_top_tier: `0.75179`  ·  corrupted: `-0.25472`  ·  n_sockets: `0.22980`  ·  quality: `0.06872`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.72088 |
| `explicit.stat_1202301673@T1` | 1.40023 |
| `explicit.stat_1509134228@T1` | 1.29134 |
| `desecrated.stat_210067635@T1` | -1.25641 |
| `explicit.stat_1940865751@T2` | -1.14429 |
| `explicit.stat_4080418644@T2` | -1.13034 |
| `explicit.stat_691932474@T1` | -1.10031 |
| `explicit.stat_9187492@T1` | 1.08886 |
| `explicit.stat_691932474@T2` | -1.06729 |
| `crafted.stat_3035140377` | 0.91507 |
| `explicit.stat_3336890334@T2` | -0.89733 |
| `explicit.stat_3261801346@T1` | -0.86067 |

### armour.focus — n=6883, R²=-0.3366

intercept: `-15.4836`  ·  log_price: True  ·  ilvl: `0.19742`  ·  n_mods: `-0.16909`  ·  n_top_tier: `0.86879`  ·  corrupted: `0.12967`  ·  n_sockets: `0.28495`  ·  quality: `0.05107`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.77407 |
| `crafted.stat_2974417149@T1` | 1.44177 |
| `crafted.stat_737908626@T2` | 1.38875 |
| `explicit.stat_4220027924@T1` | -1.38718 |
| `explicit.stat_4220027924@T2` | -1.23203 |
| `explicit.stat_2231156303@T2` | -1.13639 |
| `explicit.stat_274716455@T2` | -1.09236 |
| `explicit.stat_2231156303@T1` | -1.09139 |
| `explicit.stat_2339757871@T2` | -1.03985 |
| `explicit.stat_2974417149@T1` | -1.02937 |
| `explicit.stat_4015621042@T1` | -0.95456 |
| `explicit.stat_2974417149@T2` | -0.95390 |

### armour.quiver — n=6461, R²=-0.2904

intercept: `-16.4877`  ·  log_price: True  ·  ilvl: `0.20253`  ·  n_mods: `-0.11319`  ·  n_top_tier: `0.83551`  ·  corrupted: `0.85422`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.29108 |
| `explicit.stat_2463230181@T1` | 1.82091 |
| `explicit.stat_1573130764@T1` | -1.41780 |
| `explicit.stat_681332047@T2` | -1.37895 |
| `explicit.stat_1573130764@T2` | -1.16858 |
| `explicit.stat_4067062424@T1` | -1.03787 |
| `explicit.stat_803737631@T1` | -0.97773 |
| `explicit.stat_681332047@T1` | -0.97299 |
| `explicit.stat_803737631@T2` | -0.94073 |
| `explicit.stat_2321178454@T2` | -0.83632 |
| `explicit.stat_2463230181@T2` | 0.83552 |
| `explicit.stat_3261801346@T1` | -0.74064 |

### armour.shield — n=5554, R²=-0.4276

intercept: `-13.1871`  ·  log_price: True  ·  ilvl: `0.17482`  ·  n_mods: `-0.11534`  ·  n_top_tier: `0.69038`  ·  corrupted: `-0.35153`  ·  n_sockets: `0.38443`  ·  quality: `0.06148`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.38799 |
| `explicit.stat_4095671657@T1` | -1.26683 |
| `explicit.stat_3321629045@T2` | -1.20624 |
| `explicit.stat_4095671657@T2` | -1.14788 |
| `explicit.stat_3484657501@T1` | -1.10341 |
| `explicit.stat_3033371881@T2` | -1.06326 |
| `explicit.stat_3855016469@T1` | -1.02484 |
| `explicit.stat_328541901@T1` | -0.98016 |
| `explicit.stat_3484657501@T2` | -0.97616 |
| `explicit.stat_2451402625@T1` | -0.92163 |
| `explicit.stat_2901986750@T1` | -0.91865 |
| `explicit.stat_4052037485@T1` | -0.84730 |

### weapon.twomace — n=5114, R²=-0.4353

intercept: `-11.1615`  ·  log_price: True  ·  ilvl: `0.15293`  ·  n_mods: `-0.22531`  ·  n_top_tier: `0.30041`  ·  corrupted: `0.67772`  ·  n_sockets: `0.16073`  ·  quality: `0.06214`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.32264 |
| `explicit.stat_1037193709@T1` | -1.81602 |
| `explicit.stat_1263695895@T2` | -1.19334 |
| `explicit.stat_3336890334@T1` | -1.10582 |
| `explicit.stat_2694482655@T1` | 1.06792 |
| `explicit.stat_9187492@T1` | -0.92003 |
| `explicit.stat_691932474@T1` | -0.80026 |
| `explicit.stat_210067635@T2` | 0.73414 |
| `explicit.stat_518292764@T1` | 0.72806 |
| `explicit.stat_387439868@T2` | -0.70487 |
| `explicit.stat_1509134228@T1` | 0.67855 |
| `explicit.stat_709508406@T1` | 0.64691 |

## Coverage (listings per base)

- … **Sapphire** — 33247 listings (33192 priced) [0.3–3985176410.3 ex]
- … **Emerald** — 32400 listings (32359 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 24865 listings (24835 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11967 listings (11949 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10732 listings (10709 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10390 listings (10366 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 10291 listings (10280 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 9694 listings (9672 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9615 listings (9593 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 9196 listings (9183 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7964 listings (7949 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7681 listings (7672 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7568 listings (7559 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 7071 listings (7050 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6649 listings (6642 priced) [0.3–19945827.9 ex]
- … **Jade Amulet** — 6562 listings (6548 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 6555 listings (6536 priced) [0.2–39887666593.4 ex]
- … **Plate Belt** — 6544 listings (6516 priced) [0.3–398912568423.8 ex]
- … **Amber Amulet** — 6517 listings (6510 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6433 listings (6404 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6321 listings (6311 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 6308 listings (6300 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5982 listings (5979 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5908 listings (5894 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5794 listings (5784 priced) [0.3–398912568423.8 ex]

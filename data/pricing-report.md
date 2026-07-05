# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-05T06:32:40+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **150148** (150148 priced in exalted)
- Distinct bases: 900 · distinct mods: 2325 · mod rows: 715198
- Sold signals: **36600** sold · 69010 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-05T06:26:36+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.98** (median |log error| 2.0773)
- Within ±30% of asking price: **33%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 64% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×19.30 · ±30% 21% · n=19419
- Premium segment (60ex+): skill **+0.10** · typical error ×113.70 · ±30% 0% · n=10881
- Sold listings (clearing prices): skill **+0.09** · typical error ×44.33 · ±30% 20% · n=6607

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 2624 | ×7.30 | 5% | -0.02 | -0.03 |
| accessory.amulet | 2571 | ×22.63 | 9% | -0.05 | -0.09 |
| accessory.belt | 2380 | ×9.47 | 28% | +0.04 | +0.07 |
| armour.chest | 2310 | ×6.00 | 42% | -0.00 | -0.02 |
| armour.helmet | 2252 | ×10.00 | 41% | -0.00 | -0.03 |
| armour.boots | 2136 | ×10.00 | 38% | -0.00 | +0.00 |
| jewel | 2131 | ×7.83 | 7% | -0.01 | +0.04 |
| armour.gloves | 2118 | ×10.00 | 35% | -0.00 | -0.00 |
| other | 2087 | ×9.98 | 36% | +0.41 | +0.37 |
| weapon.wand | 1571 | ×9.07 | 34% | +0.03 | +0.08 |
| weapon.bow | 1325 | ×8.06 | 38% | +0.07 | +0.09 |
| weapon.crossbow | 1244 | ×8.62 | 34% | +0.07 | +0.12 |
| weapon.warstaff | 311 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.sceptre | 307 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.staff | 287 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.spear | 284 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.focus | 225 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 208 | ×1.00 | 96% | +0.00 | +0.00 |
| armour.shield | 189 | ×1.00 | 95% | +0.00 | +0.00 |
| flask.charm | 165 | ×1.00 | 100% | n/a | - |
| weapon.twomace | 137 | ×1.00 | 96% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=18141, R²=-0.408

intercept: `1.5716`  ·  log_price: True  ·  ilvl: `0.00103`  ·  n_mods: `0.02775`  ·  n_top_tier: `0.40077`  ·  corrupted: `3.51633`  ·  n_sockets: `-0.02079`  ·  quality: `-0.00188`

| stat_id | coef |
|---|---|
| `explicit.stat_3141070085@T1` | 4.82502 |
| `explicit.stat_1589917703@T1` | 4.05274 |
| `explicit.stat_101878827@T1` | 4.02195 |
| `explicit.stat_2106365538@T1` | 3.72573 |
| `explicit.stat_2891184298@T1` | 3.24162 |
| `explicit.stat_2968503605@T1` | 2.70847 |
| `explicit.stat_2974417149@T1` | 1.14549 |
| `explicit.stat_3917489142@T1` | 0.59264 |
| `explicit.stat_789117908@T1` | -0.52335 |
| `explicit.stat_1050105434@T1` | -0.52014 |
| `explicit.stat_3299347043@T1` | 0.33546 |
| `explicit.stat_3141070085` | -0.29108 |

### accessory.ring — n=12235, R²=-1.7001

intercept: `3.7988`  ·  log_price: True  ·  ilvl: `-0.03447`  ·  n_mods: `-0.18031`  ·  n_top_tier: `0.36878`  ·  corrupted: `0.81909`  ·  n_sockets: `3.47850`  ·  quality: `0.00922`

| stat_id | coef |
|---|---|
| `explicit.stat_2557965901@T2` | -2.75254 |
| `explicit.stat_3299347043@T1` | -2.73045 |
| `explicit.stat_2557965901@T1` | -2.54393 |
| `explicit.stat_1379411836@T1` | -2.15664 |
| `explicit.stat_3962278098@T1` | -1.95773 |
| `explicit.stat_1263695895@T2` | -1.62841 |
| `explicit.stat_1368271171@T1` | -1.59136 |
| `explicit.stat_3299347043@T2` | -1.48187 |
| `explicit.stat_1368271171@T2` | -1.45346 |
| `explicit.stat_1379411836@T2` | -1.30482 |
| `explicit.stat_2923486259@T1` | -1.17911 |
| `explicit.stat_2144192055@T1` | -1.15239 |

### accessory.amulet — n=11987, R²=-2.3425

intercept: `4.2892`  ·  log_price: True  ·  ilvl: `-0.05382`  ·  n_mods: `-0.02715`  ·  n_top_tier: `1.15685`  ·  corrupted: `0.14217`  ·  n_sockets: `-0.02204`  ·  quality: `0.18179`

| stat_id | coef |
|---|---|
| `explicit.stat_2748665614@T1` | -2.25080 |
| `explicit.stat_2748665614@T2` | -1.96903 |
| `explicit.stat_3261801346@T1` | -1.38749 |
| `explicit.stat_4080418644@T1` | -1.36092 |
| `explicit.stat_3325883026@T1` | -1.35085 |
| `explicit.stat_3556824919@T2` | -1.30174 |
| `explicit.stat_2974417149@T1` | -1.29944 |
| `explicit.stat_1379411836@T2` | -1.29634 |
| `explicit.stat_472520716@T2` | -1.27128 |
| `explicit.stat_2482852589@T1` | -1.26608 |
| `explicit.stat_983749596@T1` | -1.26395 |
| `explicit.stat_3299347043@T1` | -1.26139 |

### accessory.belt — n=10987, R²=-1.2651

intercept: `3.5833`  ·  log_price: True  ·  ilvl: `-0.04368`  ·  n_mods: `-0.02131`  ·  n_top_tier: `0.07405`  ·  corrupted: `0.03802`  ·  n_sockets: `-0.24594`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.11266 |
| `explicit.stat_2923486259@T2` | 0.82060 |
| `explicit.stat_2923486259@T1` | 0.54074 |
| `explicit.stat_3299347043@T1` | -0.39943 |
| `explicit.stat_3372524247@T1` | 0.32534 |
| `explicit.stat_1836676211@T1` | 0.20597 |
| `explicit.stat_1412217137@T1` | -0.12834 |
| `explicit.stat_809229260@T2` | -0.12561 |
| `explicit.stat_1389754388@T1` | -0.12117 |
| `explicit.stat_2881298780@T1` | -0.11680 |
| `explicit.stat_3325883026@T1` | -0.10507 |
| `explicit.stat_1836676211@T2` | -0.10235 |

### jewel — n=10877, R²=-0.9007

intercept: `-1.3914`  ·  log_price: True  ·  ilvl: `0.03586`  ·  n_mods: `0.19725`  ·  n_top_tier: `-0.41611`  ·  corrupted: `0.43349`  ·  quality: `0.22413`

| stat_id | coef |
|---|---|
| `explicit.stat_1459321413@T1` | 3.74082 |
| `explicit.stat_280731498@T1` | 3.03063 |
| `explicit.stat_795138349@T1` | -3.02634 |
| `explicit.stat_3192728503@T1` | 3.02338 |
| `explicit.stat_1697951953@T1` | -2.95991 |
| `explicit.stat_1062710370@T1` | -2.83728 |
| `explicit.stat_1316278494@T1` | -2.83560 |
| `explicit.stat_1569101201@T1` | 2.77766 |
| `explicit.stat_3851254963@T1` | 2.76576 |
| `explicit.stat_2301718443@T1` | -2.74333 |
| `explicit.stat_3596695232@T1` | 2.72729 |
| `explicit.stat_1836676211@T1` | 2.70880 |

### armour.chest — n=10706, R²=-0.24

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.01614`  ·  corrupted: `0.00003`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_4015621042` | 0.03265 |
| `explicit.stat_4080418644@T2` | -0.01617 |
| `explicit.stat_915769802@T2` | -0.01616 |
| `explicit.stat_3261801346@T1` | -0.01616 |
| `explicit.stat_124859000@T2` | -0.01616 |
| `explicit.stat_4080418644@T1` | -0.01615 |
| `explicit.stat_2923486259@T2` | -0.01615 |
| `explicit.stat_3033371881@T2` | -0.01615 |
| `explicit.stat_2881298780@T1` | -0.01615 |
| `explicit.stat_2881298780@T2` | -0.01615 |
| `explicit.stat_2451402625@T2` | -0.01615 |
| `explicit.stat_4052037485@T2` | -0.01615 |

### armour.helmet — n=10562, R²=-0.2366

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.18860`  ·  corrupted: `0.00083`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3321629045@T1` | -0.18862 |
| `explicit.stat_803737631@T2` | -0.18862 |
| `explicit.stat_3484657501@T1` | -0.18861 |
| `explicit.stat_3362812763@T2` | -0.18861 |
| `explicit.stat_4052037485@T1` | -0.18861 |
| `explicit.stat_1062208444@T2` | -0.18861 |
| `explicit.stat_4220027924@T2` | -0.18861 |
| `explicit.stat_3325883026@T2` | -0.18861 |
| `explicit.stat_3484657501@T2` | -0.18861 |
| `explicit.stat_2451402625@T1` | -0.18861 |
| `explicit.stat_3362812763@T1` | -0.18861 |
| `explicit.stat_2451402625@T2` | -0.18861 |

### armour.boots — n=9912, R²=-0.217

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00055`  ·  corrupted: `0.00001`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `pseudo.total_chaos_res` | 0.09429 |
| `explicit.stat_2923486259` | -0.09428 |
| `desecrated.stat_1671376347` | 0.00436 |
| `desecrated.stat_2250533757@T2` | -0.00098 |
| `explicit.stat_2339757871@T1` | -0.00069 |
| `explicit.stat_3362812763@T2` | -0.00060 |
| `explicit.stat_1062208444@T2` | -0.00059 |
| `explicit.stat_2923486259@T2` | -0.00058 |
| `explicit.stat_3362812763@T1` | -0.00058 |
| `explicit.stat_4080418644@T1` | -0.00057 |
| `explicit.stat_99927264@T2` | -0.00057 |
| `explicit.stat_2451402625@T2` | -0.00057 |

### armour.gloves — n=9812, R²=-0.2447

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.05700`  ·  corrupted: `0.00006`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.17623 |
| `explicit.stat_2339757871@T1` | -0.05744 |
| `explicit.stat_3484657501@T2` | -0.05703 |
| `explicit.stat_1062208444@T1` | -0.05703 |
| `explicit.stat_4015621042@T1` | -0.05703 |
| `explicit.stat_3695891184@T1` | -0.05703 |
| `explicit.stat_2797971005@T2` | -0.05702 |
| `explicit.stat_1754445556@T1` | -0.05702 |
| `explicit.stat_328541901@T2` | -0.05702 |
| `explicit.stat_681332047@T2` | -0.05702 |
| `explicit.stat_3321629045@T2` | -0.05701 |
| `explicit.stat_124859000@T2` | -0.05701 |

### weapon.wand — n=7264, R²=-1.6791

intercept: `3.3630`  ·  log_price: True  ·  ilvl: `-0.04197`  ·  n_mods: `-0.01041`  ·  n_top_tier: `0.25363`  ·  corrupted: `-0.01779`  ·  n_sockets: `-0.00217`  ·  quality: `0.00757`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.83754 |
| `explicit.stat_591105508@T1` | 2.08431 |
| `explicit.stat_4226189338@T1` | 2.06104 |
| `explicit.stat_1545858329@T1` | 2.04060 |
| `explicit.stat_2254480358@T1` | 2.01938 |
| `explicit.stat_1600707273@T2` | 1.40296 |
| `crafted.stat_124131830` | 1.16141 |
| `explicit.stat_2968503605@T1` | 0.38689 |
| `explicit.stat_736967255@T2` | 0.35980 |
| `explicit.stat_2768835289@T2` | -0.33164 |
| `explicit.stat_737908626@T1` | -0.33155 |
| `explicit.stat_3962278098@T2` | -0.31984 |

### weapon.bow — n=6049, R²=-1.638

intercept: `3.3691`  ·  log_price: True  ·  ilvl: `-0.04188`  ·  n_mods: `-0.02099`  ·  n_top_tier: `0.30296`  ·  corrupted: `-0.05215`  ·  n_sockets: `0.00556`  ·  quality: `-0.00041`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -5.73311 |
| `explicit.stat_2463230181@T1` | 2.00402 |
| `explicit.stat_1509134228@T1` | 1.89238 |
| `crafted.stat_3035140377` | 1.58261 |
| `explicit.stat_518292764@T1` | 1.51086 |
| `explicit.stat_1202301673@T1` | 1.39615 |
| `rune.stat_3885405204` | -0.65983 |
| `desecrated.stat_210067635@T1` | -0.61900 |
| `explicit.stat_2694482655@T1` | -0.38687 |
| `explicit.stat_1940865751@T1` | -0.38017 |
| `explicit.stat_3261801346@T1` | -0.35962 |
| `explicit.stat_1940865751@T2` | -0.35180 |

### weapon.crossbow — n=5770, R²=-1.514

intercept: `3.3834`  ·  log_price: True  ·  ilvl: `-0.04230`  ·  n_mods: `-0.00095`  ·  n_top_tier: `0.32844`  ·  corrupted: `-0.01432`  ·  n_sockets: `0.01042`  ·  quality: `-0.00098`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -3.32943 |
| `explicit.stat_2250681686` | 3.01432 |
| `explicit.stat_1509134228@T1` | 1.97316 |
| `explicit.stat_709508406@T1` | 1.93980 |
| `explicit.stat_1037193709@T1` | 1.92733 |
| `explicit.stat_1202301673@T1` | 1.53521 |
| `explicit.stat_3336890334@T1` | 1.50179 |
| `crafted.stat_3035140377` | 1.02431 |
| `rune.stat_2246411426` | -0.65640 |
| `explicit.stat_691932474@T1` | -0.65604 |
| `rune.stat_55876295` | 0.64616 |
| `rune.stat_669069897` | -0.48339 |

### flask.charm — n=1552, R²=-0.2547

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_2541588185@T2` | 0.00002 |
| `explicit.stat_1366840608@T2` | 0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `implicit.stat_4010341289` | -0.00001 |
| `explicit.stat_3196823591@T2` | 0.00001 |
| `explicit.stat_3849649145` | -0.00001 |
| `explicit.stat_828533480@T2` | 0.00001 |
| `explicit.stat_2365392475@T2` | 0.00001 |
| `implicit.stat_1810482573` | -0.00000 |
| `implicit.stat_2016937536` | 0.00000 |
| `implicit.stat_3676540188` | -0.00000 |

### weapon.sceptre — n=1451, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1798257884` | 0.00000 |
| `desecrated.stat_1050105434` | 0.00000 |
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

### weapon.warstaff — n=1428, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_1037193709` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_1940865751` | 0.00000 |
| `desecrated.stat_210067635` | 0.00000 |
| `desecrated.stat_2694482655` | 0.00000 |
| `desecrated.stat_3261801346` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |
| `desecrated.stat_387439868` | 0.00000 |

### weapon.staff — n=1349, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_124131830` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T1` | 0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |

### weapon.spear — n=1321, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1202301673@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |

### armour.focus — n=1068, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1671376347` | 0.00000 |
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

### armour.quiver — n=1023, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1241625305` | 0.00000 |
| `desecrated.stat_3032590688` | 0.00000 |
| `desecrated.stat_3714003708` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1241625305` | 0.00000 |
| `explicit.stat_1241625305@T1` | 0.00000 |
| `explicit.stat_1241625305@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | -0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1573130764` | 0.00000 |

### armour.shield — n=928, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1568848828` | 0.00000 |
| `explicit.stat_1011760251` | 0.00000 |
| `explicit.stat_1011760251@T1` | -0.00000 |
| `explicit.stat_1011760251@T2` | 0.00000 |
| `explicit.stat_1062208444` | 0.00000 |
| `explicit.stat_1062208444@T1` | 0.00000 |
| `explicit.stat_1062208444@T2` | 0.00000 |
| `explicit.stat_1301765461` | 0.00000 |
| `explicit.stat_1301765461@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |

### weapon.twomace — n=734, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |
| `explicit.stat_1940865751` | 0.00000 |

## Coverage (listings per base)

- … **Emerald** — 5523 listings (5523 priced) [0.8–856.7 ex]
- … **Sapphire** — 5477 listings (5477 priced) [0.7–856.7 ex]
- … **Ruby** — 4372 listings (4372 priced) [0.3–856.7 ex]
- … **Utility Belt** — 3416 listings (3416 priced) [0.3–5014962.3 ex]
- … **Stellar Amulet** — 2563 listings (2563 priced) [0.3–38371.8 ex]
- … **Dueling Wand** — 2252 listings (2252 priced) [1.0–856.7 ex]
- … **Gold Amulet** — 2204 listings (2204 priced) [0.6–856.7 ex]
- … **Prismatic Ring** — 2200 listings (2200 priced) [0.3–856.7 ex]
- … **Solar Amulet** — 2197 listings (2197 priced) [1.0–856.7 ex]
- … **Amethyst Ring** — 2088 listings (2088 priced) [0.8–856.7 ex]
- … **Gold Ring** — 2044 listings (2044 priced) [0.5–856.7 ex]
- … **Obliterator Bow** — 1708 listings (1708 priced) [0.6–856.7 ex]
- … **Plate Belt** — 1681 listings (1681 priced) [1.0–856.7 ex]
- … **Topaz Ring** — 1669 listings (1669 priced) [1.0–856.7 ex]
- … **Sapphire Ring** — 1659 listings (1659 priced) [0.9–856.7 ex]
- … **Ruby Ring** — 1613 listings (1613 priced) [0.6–856.7 ex]
- … **Heavy Belt** — 1569 listings (1569 priced) [0.5–856.7 ex]
- … **Lapis Amulet** — 1507 listings (1507 priced) [0.6–856.7 ex]
- … **Ancestral Tiara** — 1493 listings (1493 priced) [1.0–856.7 ex]
- … **Amber Amulet** — 1435 listings (1435 priced) [0.6–856.7 ex]
- … **Jade Amulet** — 1430 listings (1430 priced) [0.6–856.7 ex]
- … **Unset Ring** — 1307 listings (1307 priced) [1.0–856.7 ex]
- … **Bloodstone Amulet** — 1295 listings (1295 priced) [1.0–856.7 ex]
- … **Galvanic Wand** — 1294 listings (1294 priced) [0.5–856.7 ex]
- … **Siphoning Wand** — 1289 listings (1289 priced) [1.0–856.7 ex]

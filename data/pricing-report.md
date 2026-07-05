# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-05T08:43:03+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **155126** (155126 priced in exalted)
- Distinct bases: 904 · distinct mods: 2346 · mod rows: 737759
- Sold signals: **35819** sold · 75269 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-05T08:37:16+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×8.30** (median |log error| 2.1165)
- Within ±30% of asking price: **30%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 65% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×25.29 · ±30% 13% · n=20137
- Premium segment (60ex+): skill **+0.11** · typical error ×148.46 · ±30% 0% · n=11368
- Sold listings (clearing prices): skill **+0.12** · typical error ×58.45 · ±30% 16% · n=5830

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 2774 | ×7.05 | 5% | -0.01 | -0.01 |
| accessory.amulet | 2745 | ×26.10 | 10% | -0.04 | -0.11 |
| accessory.belt | 2477 | ×9.50 | 29% | +0.04 | +0.08 |
| armour.chest | 2374 | ×8.72 | 27% | +0.02 | +0.10 |
| armour.helmet | 2359 | ×8.47 | 22% | +0.02 | +0.06 |
| jewel | 2271 | ×7.62 | 7% | -0.00 | +0.04 |
| armour.boots | 2222 | ×10.00 | 37% | -0.00 | -0.03 |
| armour.gloves | 2193 | ×10.00 | 36% | -0.00 | -0.02 |
| other | 2100 | ×9.96 | 36% | +0.40 | +0.37 |
| weapon.wand | 1608 | ×9.05 | 35% | +0.03 | +0.09 |
| weapon.bow | 1323 | ×8.83 | 36% | +0.08 | +0.06 |
| weapon.crossbow | 1243 | ×9.03 | 31% | +0.06 | +0.13 |
| weapon.warstaff | 317 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.sceptre | 297 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.staff | 295 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.spear | 286 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 226 | ×1.00 | 96% | +0.00 | +0.00 |
| armour.focus | 219 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.shield | 199 | ×1.00 | 95% | +0.00 | +0.00 |
| flask.charm | 149 | ×1.00 | 100% | n/a | - |
| weapon.twomace | 149 | ×1.00 | 96% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=18763, R²=-0.4194

intercept: `1.5794`  ·  log_price: True  ·  ilvl: `0.00092`  ·  n_mods: `0.02024`  ·  n_top_tier: `0.40916`  ·  corrupted: `3.35735`  ·  n_sockets: `-0.02032`  ·  quality: `-0.00181`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 4.26136 |
| `explicit.stat_3141070085@T1` | 4.23513 |
| `explicit.stat_1589917703@T1` | 4.04647 |
| `explicit.stat_101878827@T1` | 4.01600 |
| `explicit.stat_2106365538@T1` | 3.67141 |
| `explicit.stat_2891184298@T1` | 3.47010 |
| `explicit.stat_2974417149@T1` | 1.12514 |
| `explicit.stat_3917489142@T1` | 0.66178 |
| `explicit.stat_1050105434@T1` | -0.61187 |
| `explicit.stat_789117908@T1` | -0.60708 |
| `explicit.stat_2968503605@T1` | 0.40490 |
| `explicit.stat_3299347043@T1` | 0.34112 |

### accessory.ring — n=12781, R²=-1.6401

intercept: `4.3239`  ·  log_price: True  ·  ilvl: `-0.03781`  ·  n_mods: `-0.21875`  ·  n_top_tier: `0.14213`  ·  corrupted: `0.78347`  ·  n_sockets: `3.58418`  ·  quality: `0.02773`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 2.53578 |
| `explicit.stat_1379411836@T1` | -2.47484 |
| `explicit.stat_707457662@T2` | 2.41318 |
| `explicit.stat_3299347043@T1` | -2.16232 |
| `explicit.stat_3962278098@T1` | -1.39572 |
| `explicit.stat_1379411836@T2` | -1.27696 |
| `explicit.stat_1573130764@T1` | -1.20354 |
| `explicit.stat_1368271171@T1` | -1.13952 |
| `explicit.stat_2923486259@T1` | -1.08894 |
| `explicit.stat_1368271171@T2` | -1.06803 |
| `explicit.stat_3299347043@T2` | -1.05506 |
| `explicit.stat_2557965901@T1` | 0.99981 |

### accessory.amulet — n=12487, R²=-2.2697

intercept: `4.0962`  ·  log_price: True  ·  ilvl: `-0.05088`  ·  n_mods: `-0.02821`  ·  n_top_tier: `0.76951`  ·  corrupted: `0.13083`  ·  n_sockets: `-0.07307`  ·  quality: `-0.01690`

| stat_id | coef |
|---|---|
| `explicit.stat_2748665614@T1` | -1.51061 |
| `explicit.stat_9187492@T2` | 1.47413 |
| `explicit.stat_2748665614@T2` | -1.25975 |
| `explicit.stat_1202301673@T2` | 1.20829 |
| `explicit.stat_124131830@T2` | 1.04556 |
| `explicit.stat_124131830` | 0.99304 |
| `explicit.stat_983749596@T1` | -0.97197 |
| `explicit.stat_3261801346@T1` | -0.95073 |
| `explicit.stat_3299347043@T1` | -0.91122 |
| `explicit.stat_4080418644@T1` | -0.89214 |
| `explicit.stat_2482852589@T1` | -0.87347 |
| `explicit.stat_1379411836@T2` | -0.87155 |

### jewel — n=11497, R²=-0.8761

intercept: `-1.3424`  ·  log_price: True  ·  ilvl: `0.03479`  ·  n_mods: `0.20670`  ·  n_top_tier: `-0.41637`  ·  corrupted: `0.48297`  ·  quality: `0.22302`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | 6.50740 |
| `explicit.stat_3973629633@T1` | 3.54771 |
| `explicit.stat_1405298142@T1` | 3.20267 |
| `explicit.stat_1697951953@T1` | -3.16889 |
| `explicit.stat_1062710370@T1` | -3.05141 |
| `explicit.stat_21071013@T1` | 3.01072 |
| `explicit.stat_3851254963@T1` | 2.84750 |
| `explicit.stat_1869147066@T1` | 2.68031 |
| `explicit.stat_1836676211@T1` | 2.63769 |
| `explicit.stat_795138349@T1` | -2.61283 |
| `explicit.stat_1459321413@T1` | 2.55685 |
| `explicit.stat_2106365538@T1` | -2.42014 |

### accessory.belt — n=11308, R²=-1.2685

intercept: `3.6973`  ·  log_price: True  ·  ilvl: `-0.04485`  ·  n_mods: `-0.02491`  ·  n_top_tier: `0.08367`  ·  corrupted: `0.04386`  ·  n_sockets: `-0.16489`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.12440 |
| `explicit.stat_2923486259@T2` | 0.60561 |
| `explicit.stat_3372524247@T1` | 0.49670 |
| `explicit.stat_3299347043@T1` | -0.37804 |
| `explicit.stat_2923486259@T1` | 0.33014 |
| `explicit.stat_3299347043@T2` | -0.18654 |
| `explicit.stat_2881298780@T1` | -0.13603 |
| `explicit.stat_809229260@T2` | -0.13286 |
| `explicit.stat_1389754388@T1` | -0.12638 |
| `explicit.stat_3325883026@T1` | -0.12384 |
| `explicit.stat_1412217137@T1` | -0.12329 |
| `explicit.stat_2639966148` | 0.11896 |

### armour.chest — n=11040, R²=-1.3752

intercept: `3.9043`  ·  log_price: True  ·  ilvl: `-0.04822`  ·  n_mods: `-0.01712`  ·  n_top_tier: `0.51683`  ·  corrupted: `0.07362`  ·  n_sockets: `-0.00081`  ·  quality: `0.01239`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.16814 |
| `explicit.stat_3981240776@T1` | 1.53595 |
| `explicit.stat_915769802@T1` | -0.62194 |
| `explicit.stat_3261801346@T2` | -0.62005 |
| `explicit.stat_4080418644@T2` | -0.61117 |
| `explicit.stat_328541901@T1` | -0.60267 |
| `explicit.stat_4015621042@T1` | -0.60029 |
| `explicit.stat_3261801346@T1` | -0.59140 |
| `explicit.stat_4015621042@T2` | -0.58629 |
| `explicit.stat_4080418644@T1` | -0.58557 |
| `explicit.stat_986397080@T2` | -0.58095 |
| `explicit.stat_2339757871@T2` | -0.57623 |

### armour.helmet — n=10866, R²=-1.3782

intercept: `4.4099`  ·  log_price: True  ·  ilvl: `-0.05514`  ·  n_mods: `-0.02712`  ·  n_top_tier: `0.74060`  ·  corrupted: `0.48084`  ·  n_sockets: `-0.01004`  ·  quality: `0.02166`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.39450 |
| `crafted.stat_3917489142@T1` | 1.50020 |
| `explicit.stat_1263695895@T1` | -0.86666 |
| `explicit.stat_3325883026@T1` | -0.83391 |
| `explicit.stat_3033371881@T1` | -0.83124 |
| `explicit.stat_3321629045@T2` | -0.81962 |
| `explicit.stat_4052037485@T2` | -0.81850 |
| `explicit.stat_3325883026@T2` | -0.81752 |
| `explicit.stat_53045048@T1` | -0.81153 |
| `explicit.stat_803737631@T2` | -0.80678 |
| `explicit.stat_3033371881@T2` | -0.80387 |
| `explicit.stat_3261801346@T2` | -0.80151 |

### armour.boots — n=10200, R²=-0.19

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.01013`  ·  corrupted: `0.00001`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 0.24219 |
| `pseudo.total_chaos_res` | 0.09225 |
| `explicit.stat_2923486259` | -0.09224 |
| `desecrated.stat_1671376347` | 0.03921 |
| `desecrated.stat_2250533757` | 0.01481 |
| `explicit.stat_2923486259@T1` | 0.01045 |
| `explicit.stat_2339757871@T1` | -0.01026 |
| `explicit.stat_3362812763@T2` | -0.01014 |
| `explicit.stat_99927264@T2` | -0.01014 |
| `explicit.stat_2451402625@T2` | -0.01014 |
| `explicit.stat_3484657501@T1` | -0.01014 |
| `explicit.stat_3917489142@T2` | -0.01014 |

### armour.gloves — n=10096, R²=-0.2263

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.46486`  ·  corrupted: `0.00594`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -0.46512 |
| `explicit.stat_3484657501@T2` | -0.46489 |
| `explicit.stat_1062208444@T1` | -0.46488 |
| `explicit.stat_4015621042@T1` | -0.46488 |
| `explicit.stat_3362812763@T1` | -0.46488 |
| `explicit.stat_4080418644@T1` | -0.46488 |
| `explicit.stat_2797971005@T2` | -0.46488 |
| `explicit.stat_3695891184@T1` | -0.46488 |
| `explicit.stat_328541901@T2` | -0.46487 |
| `explicit.stat_3362812763@T2` | -0.46487 |
| `explicit.stat_3917489142@T2` | -0.46487 |
| `explicit.stat_1368271171@T1` | -0.46487 |

### weapon.wand — n=7416, R²=-1.6738

intercept: `3.4631`  ·  log_price: True  ·  ilvl: `-0.04327`  ·  n_mods: `-0.01330`  ·  n_top_tier: `0.16884`  ·  corrupted: `-0.03042`  ·  n_sockets: `-0.00086`  ·  quality: `0.01309`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.84834 |
| `explicit.stat_591105508@T1` | 2.18199 |
| `explicit.stat_4226189338@T1` | 2.15791 |
| `explicit.stat_1545858329@T1` | 2.11309 |
| `explicit.stat_2254480358@T1` | 2.03969 |
| `explicit.stat_1600707273@T2` | 1.42564 |
| `explicit.stat_736967255@T2` | 1.16127 |
| `crafted.stat_124131830` | 0.99088 |
| `explicit.stat_2968503605@T1` | 0.74170 |
| `rune.stat_3278136794` | 0.26552 |
| `explicit.stat_2768835289@T2` | -0.26097 |
| `explicit.stat_737908626@T1` | -0.24726 |

### weapon.bow — n=6177, R²=-1.6012

intercept: `3.4798`  ·  log_price: True  ·  ilvl: `-0.04322`  ·  n_mods: `-0.02168`  ·  n_top_tier: `0.23920`  ·  corrupted: `-0.05402`  ·  n_sockets: `0.00649`  ·  quality: `0.00161`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -6.10484 |
| `explicit.stat_2463230181@T1` | 2.06343 |
| `explicit.stat_1509134228@T1` | 1.90142 |
| `explicit.stat_1202301673@T1` | 1.79408 |
| `explicit.stat_518292764@T1` | 1.77513 |
| `crafted.stat_3035140377` | 1.56144 |
| `rune.stat_3885405204` | -0.54217 |
| `desecrated.stat_210067635@T1` | -0.40764 |
| `desecrated.stat_666077204` | 0.35471 |
| `explicit.stat_3261801346@T1` | -0.30584 |
| `explicit.stat_1037193709@T1` | -0.30284 |
| `explicit.stat_2694482655@T1` | -0.30011 |

### weapon.crossbow — n=5884, R²=-1.4926

intercept: `3.4856`  ·  log_price: True  ·  ilvl: `-0.04385`  ·  n_mods: `0.00119`  ·  n_top_tier: `0.42100`  ·  corrupted: `-0.00349`  ·  n_sockets: `0.01363`  ·  quality: `0.00055`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 1.91558 |
| `explicit.stat_1037193709@T1` | 1.89187 |
| `explicit.stat_709508406@T1` | 1.85243 |
| `explicit.stat_1544773869@T1` | 1.84612 |
| `explicit.stat_1202301673@T1` | 1.45396 |
| `explicit.stat_2250681686@T2` | -1.41814 |
| `crafted.stat_3035140377` | 1.06809 |
| `explicit.stat_2250681686` | 1.01504 |
| `explicit.stat_691932474@T1` | -0.72096 |
| `rune.stat_2246411426` | -0.64371 |
| `rune.stat_55876295` | 0.63281 |
| `explicit.stat_1202301673@T2` | -0.49715 |

### flask.charm — n=1664, R²=-0.2283

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_2541588185@T2` | 0.00002 |
| `explicit.stat_2566921799` | 0.00001 |
| `implicit.stat_4010341289` | -0.00001 |
| `explicit.stat_1366840608@T2` | 0.00001 |
| `explicit.stat_2365392475@T2` | 0.00001 |
| `explicit.stat_828533480@T2` | 0.00000 |
| `implicit.stat_2016937536` | 0.00000 |
| `explicit.stat_3849649145` | -0.00000 |
| `implicit.stat_3676540188` | -0.00000 |
| `explicit.stat_3196823591@T2` | 0.00000 |
| `implicit.stat_1810482573` | -0.00000 |

### weapon.sceptre — n=1477, R²=0.0

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

### weapon.warstaff — n=1459, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_1037193709` | 0.00000 |
| `desecrated.stat_1368271171` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_1940865751` | 0.00000 |
| `desecrated.stat_210067635` | 0.00000 |
| `desecrated.stat_2694482655` | 0.00000 |
| `desecrated.stat_3261801346` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |

### weapon.staff — n=1382, R²=0.0

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

### weapon.spear — n=1339, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `crafted.stat_210067635` | 0.00000 |
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

### armour.focus — n=1078, R²=0.0

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

### armour.quiver — n=1039, R²=0.0

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

### armour.shield — n=937, R²=0.0

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

### weapon.twomace — n=744, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

- … **Emerald** — 5831 listings (5831 priced) [0.7–856.7 ex]
- … **Sapphire** — 5768 listings (5768 priced) [0.7–856.7 ex]
- … **Ruby** — 4586 listings (4586 priced) [0.3–856.7 ex]
- … **Utility Belt** — 3523 listings (3523 priced) [0.3–5014962.3 ex]
- … **Stellar Amulet** — 2639 listings (2639 priced) [0.3–38371.8 ex]
- … **Gold Amulet** — 2301 listings (2301 priced) [0.7–856.7 ex]
- … **Dueling Wand** — 2290 listings (2290 priced) [1.0–856.7 ex]
- … **Prismatic Ring** — 2288 listings (2288 priced) [0.3–856.7 ex]
- … **Solar Amulet** — 2283 listings (2283 priced) [1.0–856.7 ex]
- … **Amethyst Ring** — 2184 listings (2184 priced) [0.8–856.7 ex]
- … **Gold Ring** — 2132 listings (2132 priced) [0.5–856.7 ex]
- … **Topaz Ring** — 1741 listings (1741 priced) [1.0–856.7 ex]
- … **Obliterator Bow** — 1740 listings (1740 priced) [0.6–856.7 ex]
- … **Plate Belt** — 1723 listings (1723 priced) [1.0–856.7 ex]
- … **Sapphire Ring** — 1721 listings (1721 priced) [0.9–856.7 ex]
- … **Ruby Ring** — 1679 listings (1679 priced) [0.6–856.7 ex]
- … **Heavy Belt** — 1622 listings (1622 priced) [0.5–856.7 ex]
- … **Lapis Amulet** — 1560 listings (1560 priced) [0.6–856.7 ex]
- … **Ancestral Tiara** — 1536 listings (1536 priced) [1.0–856.7 ex]
- … **Amber Amulet** — 1495 listings (1495 priced) [0.7–856.7 ex]
- … **Jade Amulet** — 1487 listings (1487 priced) [0.7–856.7 ex]
- … **Unset Ring** — 1360 listings (1360 priced) [1.0–856.7 ex]
- … **Bloodstone Amulet** — 1348 listings (1348 priced) [1.0–856.7 ex]
- … **Pearl Ring** — 1346 listings (1346 priced) [0.8–856.7 ex]
- … **Azure Amulet** — 1332 listings (1332 priced) [1.0–856.7 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-05T04:21:49+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **145097** (145097 priced in exalted)
- Distinct bases: 898 · distinct mods: 2305 · mod rows: 692062
- Sold signals: **36260** sold · 63733 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-05T04:16:20+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.96** (median |log error| 2.0747)
- Within ±30% of asking price: **32%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 64% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.07** · typical error ×23.14 · ±30% 22% · n=19289
- Premium segment (60ex+): skill **+0.08** · typical error ×98.10 · ±30% 0% · n=10959
- Sold listings (clearing prices): skill **+0.08** · typical error ×30.26 · ±30% 21% · n=6897

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 2556 | ×7.43 | 5% | -0.02 | -0.03 |
| accessory.amulet | 2531 | ×20.40 | 9% | -0.05 | -0.10 |
| accessory.belt | 2292 | ×6.10 | 36% | +0.03 | +0.05 |
| armour.chest | 2239 | ×10.00 | 38% | +0.00 | -0.01 |
| armour.helmet | 2214 | ×10.00 | 35% | -0.01 | -0.02 |
| armour.gloves | 2079 | ×10.00 | 33% | -0.00 | -0.01 |
| armour.boots | 2077 | ×10.00 | 31% | -0.01 | +0.00 |
| jewel | 2024 | ×7.75 | 7% | -0.02 | +0.02 |
| other | 1961 | ×9.99 | 35% | +0.41 | +0.37 |
| weapon.wand | 1536 | ×9.03 | 36% | +0.04 | +0.10 |
| weapon.bow | 1291 | ×8.34 | 38% | +0.07 | +0.09 |
| weapon.crossbow | 1235 | ×8.63 | 34% | +0.07 | +0.11 |
| weapon.warstaff | 306 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.sceptre | 296 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.staff | 282 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.spear | 271 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.focus | 223 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 214 | ×1.00 | 96% | +0.00 | +0.00 |
| armour.shield | 194 | ×1.00 | 95% | +0.00 | +0.00 |
| weapon.twomace | 151 | ×1.00 | 96% | +0.00 | +0.00 |
| flask.charm | 135 | ×1.00 | 100% | n/a | - |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=17530, R²=-0.4238

intercept: `1.5980`  ·  log_price: True  ·  ilvl: `0.00045`  ·  n_mods: `0.00652`  ·  n_top_tier: `0.33493`  ·  corrupted: `3.39836`  ·  n_sockets: `-0.01023`  ·  quality: `-0.00103`

| stat_id | coef |
|---|---|
| `explicit.stat_101878827@T1` | 4.13589 |
| `explicit.stat_1589917703@T1` | 4.01241 |
| `explicit.stat_2106365538@T1` | 4.00306 |
| `explicit.stat_2891184298@T1` | 3.13847 |
| `explicit.stat_2968503605@T1` | 2.78364 |
| `explicit.stat_3141070085@T1` | 1.66727 |
| `explicit.stat_2974417149@T1` | 1.15139 |
| `explicit.stat_3917489142@T1` | 0.43249 |
| `explicit.stat_1050105434@T1` | -0.39515 |
| `explicit.stat_789117908@T1` | -0.37936 |
| `explicit.stat_3299347043@T1` | 0.28479 |
| `implicit.stat_1379411836` | -0.27273 |

### accessory.ring — n=11695, R²=-1.7471

intercept: `3.3656`  ·  log_price: True  ·  ilvl: `-0.02983`  ·  n_mods: `-0.09490`  ·  n_top_tier: `0.15223`  ·  corrupted: `0.64988`  ·  n_sockets: `3.28350`  ·  quality: `0.01835`

| stat_id | coef |
|---|---|
| `explicit.stat_2557965901@T1` | 2.79239 |
| `explicit.stat_2557965901@T2` | 2.19196 |
| `explicit.stat_1368271171@T1` | -1.59217 |
| `explicit.stat_707457662@T1` | -1.34806 |
| `explicit.stat_1368271171@T2` | -1.33239 |
| `explicit.stat_3299347043@T1` | -1.27670 |
| `explicit.stat_3962278098@T1` | -1.18858 |
| `explicit.stat_1263695895@T2` | -1.12523 |
| `explicit.stat_2144192055@T1` | -1.08505 |
| `explicit.stat_1573130764@T1` | -1.06088 |
| `explicit.stat_1379411836@T1` | -0.99772 |
| `explicit.stat_1379411836@T2` | -0.90924 |

### accessory.amulet — n=11501, R²=-2.4029

intercept: `4.4838`  ·  log_price: True  ·  ilvl: `-0.05602`  ·  n_mods: `-0.04372`  ·  n_top_tier: `1.19537`  ·  corrupted: `0.08208`  ·  n_sockets: `-0.06015`  ·  quality: `0.18482`

| stat_id | coef |
|---|---|
| `explicit.stat_2748665614@T1` | -2.06455 |
| `explicit.stat_983749596@T1` | -1.91717 |
| `explicit.stat_2748665614@T2` | -1.85103 |
| `explicit.stat_983749596@T2` | -1.62644 |
| `explicit.stat_3556824919@T2` | -1.52747 |
| `explicit.stat_4080418644@T1` | -1.49671 |
| `explicit.stat_1202301673@T2` | 1.45547 |
| `explicit.stat_3261801346@T1` | -1.42971 |
| `explicit.stat_3372524247@T2` | -1.37501 |
| `explicit.stat_2974417149@T1` | -1.37284 |
| `explicit.stat_803737631@T1` | -1.36405 |
| `explicit.stat_1671376347@T1` | -1.36354 |

### accessory.belt — n=10651, R²=-0.0857

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.89586`  ·  corrupted: `0.00001`  ·  n_sockets: `4.31253`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.28051 |
| `explicit.stat_1389754388@T2` | -0.89587 |
| `explicit.stat_51994685@T1` | -0.89587 |
| `explicit.stat_2923486259@T1` | -0.89587 |
| `explicit.stat_1389754388@T1` | -0.89587 |
| `explicit.stat_2923486259@T2` | -0.89587 |
| `explicit.stat_3325883026@T1` | -0.89587 |
| `explicit.stat_1050105434@T2` | -0.89587 |
| `explicit.stat_1570770415@T1` | -0.89587 |
| `explicit.stat_644456512@T2` | -0.89587 |
| `explicit.stat_51994685@T2` | -0.89586 |
| `explicit.stat_644456512@T1` | -0.89586 |

### armour.chest — n=10368, R²=-0.2362

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.04716`  ·  corrupted: `0.00005`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_4080418644@T2` | -0.04719 |
| `explicit.stat_3261801346@T1` | -0.04718 |
| `explicit.stat_124859000@T2` | -0.04718 |
| `explicit.stat_915769802@T2` | -0.04717 |
| `explicit.stat_4080418644@T1` | -0.04717 |
| `explicit.stat_3033371881@T2` | -0.04716 |
| `explicit.stat_4052037485@T2` | -0.04716 |
| `explicit.stat_2881298780@T1` | -0.04716 |
| `explicit.stat_2923486259@T2` | -0.04716 |
| `explicit.stat_2451402625@T2` | -0.04716 |
| `explicit.stat_2881298780@T2` | -0.04716 |
| `explicit.stat_3484657501@T1` | -0.04716 |

### jewel — n=10253, R²=-0.8961

intercept: `-1.3535`  ·  log_price: True  ·  ilvl: `0.03582`  ·  n_mods: `0.18877`  ·  n_top_tier: `-0.41613`  ·  corrupted: `0.45403`

| stat_id | coef |
|---|---|
| `explicit.stat_2301718443@T1` | -4.77548 |
| `explicit.stat_1697951953@T1` | -3.18848 |
| `explicit.stat_1062710370@T1` | -3.12274 |
| `explicit.stat_3192728503@T1` | 2.97031 |
| `explicit.stat_795138349@T1` | -2.95524 |
| `explicit.stat_3851254963@T1` | 2.81398 |
| `explicit.stat_1316278494@T1` | -2.80756 |
| `explicit.stat_1459321413@T1` | 2.62305 |
| `explicit.stat_1569101201@T1` | 2.60675 |
| `explicit.stat_1836676211@T1` | 2.52590 |
| `explicit.stat_3596695232@T1` | 2.44092 |
| `explicit.stat_2011656677@T1` | 2.35658 |

### armour.helmet — n=10233, R²=-0.2161

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.34565`  ·  corrupted: `0.00871`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_803737631@T2` | -0.34567 |
| `explicit.stat_3321629045@T1` | -0.34567 |
| `explicit.stat_1062208444@T2` | -0.34566 |
| `explicit.stat_53045048@T2` | -0.34566 |
| `explicit.stat_3362812763@T2` | -0.34566 |
| `explicit.stat_3325883026@T2` | -0.34566 |
| `explicit.stat_3484657501@T1` | -0.34566 |
| `explicit.stat_3325883026@T1` | -0.34565 |
| `explicit.stat_4220027924@T2` | -0.34565 |
| `explicit.stat_3484657501@T2` | -0.34565 |
| `explicit.stat_2451402625@T1` | -0.34565 |
| `explicit.stat_4052037485@T1` | -0.34565 |

### armour.boots — n=9596, R²=-0.2068

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.06446`  ·  corrupted: `0.00001`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_4080418644@T1` | -0.11415 |
| `desecrated.stat_2250533757@T2` | -0.09523 |
| `pseudo.total_chaos_res` | 0.09431 |
| `explicit.stat_2923486259` | -0.09430 |
| `explicit.stat_1062208444@T2` | -0.08003 |
| `explicit.stat_3362812763@T2` | -0.06585 |
| `explicit.stat_2339757871@T1` | -0.06469 |
| `explicit.stat_3639275092@T1` | -0.06451 |
| `explicit.stat_99927264@T2` | -0.06450 |
| `explicit.stat_2923486259@T2` | -0.06449 |
| `explicit.stat_2451402625@T2` | -0.06449 |
| `explicit.stat_3033371881@T2` | -0.06448 |

### armour.gloves — n=9528, R²=-0.2428

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.10318`  ·  corrupted: `0.00007`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.17874 |
| `explicit.stat_2339757871@T1` | -0.10374 |
| `explicit.stat_4015621042@T1` | -0.10322 |
| `explicit.stat_3484657501@T2` | -0.10321 |
| `explicit.stat_2797971005@T2` | -0.10321 |
| `explicit.stat_3695891184@T1` | -0.10321 |
| `explicit.stat_1062208444@T1` | -0.10320 |
| `explicit.stat_124859000@T2` | -0.10320 |
| `explicit.stat_4080418644@T1` | -0.10319 |
| `explicit.stat_681332047@T2` | -0.10319 |
| `explicit.stat_1754445556@T1` | -0.10319 |
| `explicit.stat_328541901@T2` | -0.10319 |

### weapon.wand — n=7083, R²=-1.6841

intercept: `3.4295`  ·  log_price: True  ·  ilvl: `-0.04275`  ·  n_mods: `-0.01168`  ·  n_top_tier: `0.14126`  ·  corrupted: `-0.01289`  ·  n_sockets: `-0.00086`  ·  quality: `0.00406`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 4.00465 |
| `explicit.stat_591105508@T1` | 2.21850 |
| `explicit.stat_1545858329@T1` | 2.17440 |
| `explicit.stat_4226189338@T1` | 2.16878 |
| `explicit.stat_2254480358@T1` | 2.15717 |
| `explicit.stat_1600707273@T2` | 1.53410 |
| `crafted.stat_124131830` | 1.27280 |
| `explicit.stat_736967255@T2` | 0.48602 |
| `rune.stat_3278136794` | 0.27151 |
| `explicit.stat_2968503605@T1` | 0.26153 |
| `explicit.stat_2768835289@T2` | -0.22296 |
| `explicit.stat_293638271@T2` | -0.19629 |

### weapon.bow — n=5923, R²=-1.6259

intercept: `3.3788`  ·  log_price: True  ·  ilvl: `-0.04191`  ·  n_mods: `-0.02223`  ·  n_top_tier: `0.26183`  ·  corrupted: `-0.04545`  ·  n_sockets: `0.00323`  ·  quality: `-0.00103`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -5.98825 |
| `explicit.stat_2463230181@T1` | 2.03569 |
| `explicit.stat_1509134228@T1` | 1.93535 |
| `explicit.stat_518292764@T1` | 1.69677 |
| `crafted.stat_3035140377` | 1.53505 |
| `explicit.stat_1202301673@T1` | 0.84342 |
| `rune.stat_3885405204` | -0.69869 |
| `desecrated.stat_210067635@T1` | -0.54579 |
| `desecrated.stat_666077204` | 0.35559 |
| `explicit.stat_1940865751@T1` | -0.34124 |
| `explicit.stat_2694482655@T1` | -0.32970 |
| `explicit.stat_3261801346@T1` | -0.31806 |

### weapon.crossbow — n=5663, R²=-1.5162

intercept: `3.4618`  ·  log_price: True  ·  ilvl: `-0.04335`  ·  n_mods: `-0.00071`  ·  n_top_tier: `0.40197`  ·  corrupted: `-0.04707`  ·  n_sockets: `0.00932`  ·  quality: `-0.00069`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -3.32730 |
| `explicit.stat_2250681686` | 2.94126 |
| `explicit.stat_1509134228@T1` | 1.87479 |
| `explicit.stat_709508406@T1` | 1.86863 |
| `explicit.stat_1037193709@T1` | 1.86190 |
| `explicit.stat_3336890334@T1` | 1.48663 |
| `explicit.stat_1202301673@T1` | 1.12516 |
| `crafted.stat_3035140377` | 1.11186 |
| `explicit.stat_691932474@T1` | -0.95915 |
| `rune.stat_2246411426` | -0.65514 |
| `rune.stat_55876295` | 0.64470 |
| `rune.stat_669069897` | -0.48408 |

### flask.charm — n=1437, R²=-0.2902

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00005 |
| `explicit.stat_1873752457@T2` | -0.00001 |
| `explicit.stat_2541588185@T2` | 0.00001 |
| `explicit.stat_1120862500@T2` | -0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `explicit.stat_388617051@T2` | -0.00001 |
| `explicit.stat_3849649145` | -0.00001 |
| `implicit.stat_4010341289` | -0.00001 |
| `implicit.stat_2016937536` | 0.00001 |
| `implicit.stat_1810482573` | -0.00001 |
| `explicit.stat_828533480@T1` | -0.00001 |
| `explicit.stat_1873752457@T1` | -0.00001 |

### weapon.sceptre — n=1428, R²=0.0

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

### weapon.warstaff — n=1396, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1037193709` | 0.00000 |
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

### weapon.staff — n=1319, R²=0.0

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

### weapon.spear — n=1298, R²=0.0

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

### armour.focus — n=1055, R²=0.0

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

### armour.quiver — n=1007, R²=0.0

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

### armour.shield — n=917, R²=0.0

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

### weapon.twomace — n=728, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |
| `explicit.stat_1940865751` | 0.00000 |
| `explicit.stat_1940865751@T1` | 0.00000 |

## Coverage (listings per base)

- … **Emerald** — 5220 listings (5220 priced) [0.8–856.7 ex]
- … **Sapphire** — 5180 listings (5180 priced) [0.7–856.7 ex]
- … **Ruby** — 4155 listings (4155 priced) [0.3–856.7 ex]
- … **Utility Belt** — 3307 listings (3307 priced) [0.3–4644180.3 ex]
- … **Stellar Amulet** — 2492 listings (2492 priced) [0.3–38371.8 ex]
- … **Dueling Wand** — 2198 listings (2198 priced) [1.0–856.7 ex]
- … **Gold Amulet** — 2134 listings (2134 priced) [0.6–856.7 ex]
- … **Prismatic Ring** — 2122 listings (2122 priced) [0.3–856.7 ex]
- … **Solar Amulet** — 2121 listings (2121 priced) [1.0–856.7 ex]
- … **Amethyst Ring** — 2018 listings (2018 priced) [0.8–856.7 ex]
- … **Gold Ring** — 1951 listings (1951 priced) [0.6–856.7 ex]
- … **Obliterator Bow** — 1676 listings (1676 priced) [0.6–856.7 ex]
- … **Plate Belt** — 1627 listings (1627 priced) [1.0–856.7 ex]
- … **Sapphire Ring** — 1595 listings (1595 priced) [0.9–856.7 ex]
- … **Topaz Ring** — 1595 listings (1595 priced) [1.0–856.7 ex]
- … **Ruby Ring** — 1550 listings (1550 priced) [0.6–856.7 ex]
- … **Heavy Belt** — 1513 listings (1513 priced) [0.5–856.7 ex]
- … **Ancestral Tiara** — 1454 listings (1454 priced) [1.0–856.7 ex]
- … **Lapis Amulet** — 1435 listings (1435 priced) [0.6–856.7 ex]
- … **Amber Amulet** — 1380 listings (1380 priced) [0.6–856.7 ex]
- … **Jade Amulet** — 1362 listings (1362 priced) [0.6–856.7 ex]
- … **Galvanic Wand** — 1258 listings (1258 priced) [0.5–856.7 ex]
- … **Siphoning Wand** — 1257 listings (1257 priced) [1.0–856.7 ex]
- … **Unset Ring** — 1255 listings (1255 priced) [1.0–856.7 ex]
- … **Bloodstone Amulet** — 1245 listings (1245 priced) [1.0–856.7 ex]

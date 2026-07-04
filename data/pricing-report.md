# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-04T15:25:22+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **113583** (113583 priced in exalted)
- Distinct bases: 874 · distinct mods: 2142 · mod rows: 548149
- Sold signals: **29290** sold · 35427 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-04T15:19:54+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.58** (median |log error| 2.0255)
- Within ±30% of asking price: **28%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 67% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×33.52 · ±30% 6% · n=15815
- Premium segment (60ex+): skill **+0.11** · typical error ×176.55 · ±30% 0% · n=9063
- Sold listings (clearing prices): skill **-0.08** · typical error ×1.82 · ±30% 51% · n=6659

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.amulet | 1932 | ×28.86 | 10% | -0.02 | -0.09 |
| accessory.ring | 1887 | ×6.33 | 7% | +0.05 | +0.03 |
| accessory.belt | 1842 | ×9.56 | 26% | +0.01 | +0.03 |
| armour.helmet | 1768 | ×8.61 | 22% | +0.01 | +0.09 |
| armour.chest | 1733 | ×8.01 | 22% | +0.03 | +0.10 |
| armour.gloves | 1655 | ×8.59 | 23% | +0.03 | +0.05 |
| armour.boots | 1609 | ×8.97 | 23% | +0.01 | +0.06 |
| other | 1515 | ×5.97 | 33% | +0.42 | +0.39 |
| jewel | 1319 | ×6.83 | 9% | -0.00 | +0.07 |
| weapon.wand | 1262 | ×9.22 | 35% | +0.06 | +0.07 |
| weapon.bow | 1057 | ×8.90 | 35% | +0.06 | +0.04 |
| weapon.crossbow | 998 | ×7.81 | 33% | +0.09 | +0.10 |
| weapon.sceptre | 258 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.spear | 225 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.warstaff | 219 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.staff | 214 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.focus | 204 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 182 | ×1.00 | 95% | +0.00 | +0.00 |
| armour.shield | 177 | ×1.00 | 96% | +0.00 | +0.00 |
| weapon.twomace | 130 | ×1.00 | 98% | +0.00 | +0.00 |
| flask.charm | 78 | ×1.00 | 69% | -0.00 | -0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=13415, R²=-0.28

intercept: `1.5658`  ·  log_price: True  ·  ilvl: `0.00466`  ·  n_mods: `0.04520`  ·  n_top_tier: `0.13441`  ·  corrupted: `0.37138`  ·  n_sockets: `-0.12416`  ·  quality: `-0.01372`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.60341 |
| `explicit.stat_124131830` | -0.55093 |
| `implicit.stat_3182714256` | 0.46030 |
| `implicit.stat_718638445` | 0.46018 |
| `explicit.stat_2974417149@T1` | 0.34918 |
| `implicit.stat_1379411836` | -0.31989 |
| `explicit.stat_1050105434@T2` | -0.28771 |
| `explicit.stat_2891184298@T1` | -0.28526 |
| `explicit.stat_789117908@T1` | 0.28461 |
| `implicit.stat_958696139` | 0.25264 |
| `explicit.stat_3299347043@T2` | -0.19574 |
| `implicit.stat_4041853756` | 0.19328 |

### accessory.amulet — n=8805, R²=-2.2157

intercept: `4.8750`  ·  log_price: True  ·  ilvl: `-0.05813`  ·  n_mods: `-0.10549`  ·  n_top_tier: `0.17837`  ·  corrupted: `-0.00925`  ·  n_sockets: `0.15869`  ·  quality: `0.16511`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | 2.90955 |
| `explicit.stat_2162097452@T2` | -1.97456 |
| `explicit.stat_3372524247@T1` | 1.94298 |
| `explicit.stat_3981240776@T2` | -1.90829 |
| `explicit.stat_3981240776@T1` | -1.68088 |
| `explicit.stat_9187492` | 1.54164 |
| `explicit.stat_124131830@T2` | 1.24580 |
| `explicit.stat_2162097452` | 1.15299 |
| `explicit.stat_803737631@T1` | -1.14271 |
| `explicit.stat_124131830` | 1.01769 |
| `explicit.stat_803737631@T2` | -0.98155 |
| `explicit.stat_1671376347@T1` | 0.94427 |

### accessory.ring — n=8629, R²=-1.9235

intercept: `3.2078`  ·  log_price: True  ·  ilvl: `-0.02717`  ·  n_mods: `-0.08204`  ·  n_top_tier: `0.44492`  ·  corrupted: `0.32206`  ·  n_sockets: `3.59324`  ·  quality: `0.02221`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 2.78582 |
| `explicit.stat_707457662@T2` | 2.57703 |
| `explicit.stat_3299347043@T1` | -1.95934 |
| `explicit.stat_1573130764@T1` | -1.87914 |
| `explicit.stat_1671376347@T1` | -1.73777 |
| `explicit.stat_3962278098@T2` | -1.50649 |
| `explicit.stat_1050105434@T1` | -1.09930 |
| `explicit.stat_789117908@T1` | -1.06513 |
| `explicit.stat_2923486259@T1` | -0.99919 |
| `explicit.stat_3032590688@T1` | -0.98849 |
| `explicit.stat_1379411836@T1` | -0.86965 |
| `explicit.stat_1050105434@T2` | -0.86676 |

### accessory.belt — n=8470, R²=-1.2341

intercept: `4.1583`  ·  log_price: True  ·  ilvl: `-0.05057`  ·  n_mods: `-0.02911`  ·  n_top_tier: `0.00010`  ·  corrupted: `0.23098`  ·  n_sockets: `-0.07957`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.74251 |
| `explicit.stat_2923486259@T1` | 1.70447 |
| `explicit.stat_1836676211@T1` | 1.19755 |
| `explicit.stat_2923486259@T2` | 0.99456 |
| `implicit.stat_731781020` | 0.20755 |
| `explicit.stat_1671376347@T1` | 0.20200 |
| `explicit.stat_3299347043@T1` | -0.13462 |
| `explicit.stat_4220027924@T1` | 0.10812 |
| `explicit.stat_3299347043@T2` | -0.09864 |
| `explicit.stat_3585532255@T1` | 0.09142 |
| `explicit.stat_3585532255@T2` | 0.08216 |
| `explicit.stat_174664100` | 0.07877 |

### armour.chest — n=8210, R²=-1.3542

intercept: `3.7397`  ·  log_price: True  ·  ilvl: `-0.04617`  ·  n_mods: `-0.02661`  ·  n_top_tier: `0.82184`  ·  corrupted: `-0.03600`  ·  n_sockets: `-0.00048`  ·  quality: `0.00952`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 1.85024 |
| `implicit.stat_2251279027` | 1.58367 |
| `explicit.stat_3981240776@T1` | 1.21926 |
| `explicit.stat_2923486259@T1` | -0.99594 |
| `explicit.stat_2339757871@T1` | -0.98565 |
| `explicit.stat_3261801346@T2` | -0.95758 |
| `explicit.stat_3261801346@T1` | -0.93601 |
| `explicit.stat_915769802@T1` | -0.90885 |
| `explicit.stat_986397080@T2` | -0.90880 |
| `explicit.stat_4080418644@T2` | -0.90872 |
| `explicit.stat_2923486259@T2` | -0.90601 |
| `explicit.stat_3301100256@T2` | -0.89918 |

### armour.helmet — n=8170, R²=-1.318

intercept: `4.2051`  ·  log_price: True  ·  ilvl: `-0.05291`  ·  n_mods: `-0.02319`  ·  n_top_tier: `0.72452`  ·  corrupted: `0.15744`  ·  n_sockets: `-0.03011`  ·  quality: `0.02604`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.99334 |
| `explicit.stat_2339757871@T1` | -1.91473 |
| `explicit.stat_3033371881@T1` | -1.00099 |
| `explicit.stat_3033371881@T2` | -0.95900 |
| `explicit.stat_803737631@T2` | -0.88206 |
| `explicit.stat_3362812763@T1` | -0.85022 |
| `explicit.stat_3321629045@T2` | -0.82236 |
| `explicit.stat_3325883026@T1` | -0.82037 |
| `explicit.stat_3261801346@T2` | -0.81393 |
| `explicit.stat_53045048@T2` | -0.79837 |
| `explicit.stat_4052037485@T2` | -0.79722 |
| `explicit.stat_53045048@T1` | -0.79655 |

### armour.boots — n=7601, R²=-1.0932

intercept: `4.0005`  ·  log_price: True  ·  ilvl: `-0.04983`  ·  n_mods: `-0.03227`  ·  n_top_tier: `0.36268`  ·  corrupted: `0.00089`  ·  n_sockets: `0.03685`  ·  quality: `0.03056`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 5.71240 |
| `explicit.stat_2250533757@T1` | 1.79925 |
| `explicit.stat_2339757871@T1` | -1.33336 |
| `explicit.stat_4220027924@T1` | 1.19647 |
| `explicit.stat_3362812763@T1` | -0.55419 |
| `explicit.stat_3321629045@T1` | -0.51168 |
| `explicit.stat_3362812763@T2` | -0.50407 |
| `explicit.stat_2160282525@T1` | -0.46002 |
| `explicit.stat_3033371881@T2` | -0.45442 |
| `explicit.stat_1874553720@T2` | -0.45342 |
| `explicit.stat_1874553720@T1` | -0.44196 |
| `explicit.stat_2160282525@T2` | -0.44077 |

### armour.gloves — n=7533, R²=-1.3154

intercept: `4.0971`  ·  log_price: True  ·  ilvl: `-0.05247`  ·  n_mods: `0.01072`  ·  n_top_tier: `0.86018`  ·  corrupted: `0.05092`  ·  n_sockets: `0.03011`  ·  quality: `0.02433`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.99092 |
| `explicit.stat_4015621042@T1` | -0.99219 |
| `explicit.stat_681332047@T2` | -0.95492 |
| `explicit.stat_803737631@T1` | -0.94870 |
| `explicit.stat_9187492@T2` | -0.94474 |
| `explicit.stat_1671376347@T1` | 0.94036 |
| `explicit.stat_2557965901@T2` | -0.92858 |
| `explicit.stat_4052037485@T2` | -0.92436 |
| `explicit.stat_803737631@T2` | -0.92347 |
| `explicit.stat_3032590688@T1` | -0.91815 |
| `explicit.stat_2451402625@T2` | -0.91546 |
| `explicit.stat_3033371881@T2` | -0.90397 |

### jewel — n=6840, R²=-0.9798

intercept: `-1.5353`  ·  log_price: True  ·  ilvl: `0.03731`  ·  n_mods: `0.19455`  ·  n_top_tier: `-0.40645`  ·  corrupted: `0.53047`

| stat_id | coef |
|---|---|
| `explicit.stat_1869147066@T1` | 4.67895 |
| `explicit.stat_153777645@T1` | 4.24201 |
| `explicit.stat_1697951953@T1` | 4.17751 |
| `explicit.stat_1569101201@T1` | 3.81488 |
| `explicit.stat_491450213@T1` | 3.56936 |
| `explicit.stat_2456523742@T1` | 3.40605 |
| `explicit.stat_2301718443@T1` | -2.97541 |
| `explicit.stat_3973629633@T1` | 2.59913 |
| `explicit.stat_3377888098@T1` | -2.44321 |
| `explicit.stat_1805182458@T1` | -2.40610 |
| `explicit.stat_627767961@T1` | -2.35839 |
| `explicit.stat_1836676211@T1` | -2.31893 |

### weapon.wand — n=5879, R²=-1.5898

intercept: `3.4325`  ·  log_price: True  ·  ilvl: `-0.04251`  ·  n_mods: `-0.01764`  ·  n_top_tier: `0.64419`  ·  corrupted: `0.00704`  ·  n_sockets: `0.00419`  ·  quality: `0.02481`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.97745 |
| `explicit.stat_591105508@T1` | 1.71034 |
| `explicit.stat_1545858329@T1` | 1.69067 |
| `explicit.stat_4226189338@T1` | 1.61129 |
| `explicit.stat_2254480358@T1` | 1.60803 |
| `explicit.stat_736967255@T2` | 1.40549 |
| `explicit.stat_1600707273@T1` | 1.26745 |
| `explicit.stat_1600707273@T2` | 1.04479 |
| `crafted.stat_124131830` | 1.03888 |
| `explicit.stat_293638271@T2` | -0.76003 |
| `explicit.stat_124131830@T2` | -0.74554 |
| `explicit.stat_2768835289@T2` | -0.73087 |

### weapon.bow — n=5030, R²=-1.5644

intercept: `3.4516`  ·  log_price: True  ·  ilvl: `-0.04268`  ·  n_mods: `-0.02902`  ·  n_top_tier: `0.22828`  ·  corrupted: `-0.06277`  ·  n_sockets: `0.00796`  ·  quality: `-0.00239`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -7.82010 |
| `explicit.stat_2463230181@T1` | 2.03862 |
| `explicit.stat_1509134228@T1` | 1.92326 |
| `explicit.stat_518292764@T1` | 1.91402 |
| `explicit.stat_1202301673@T1` | 1.56804 |
| `crafted.stat_3035140377` | 1.09625 |
| `desecrated.stat_210067635@T1` | 1.05470 |
| `desecrated.stat_518292764` | 0.58656 |
| `rune.stat_3885405204` | -0.58161 |
| `desecrated.stat_666077204` | 0.48736 |
| `explicit.stat_821021828@T1` | -0.37040 |
| `explicit.stat_1263695895@T1` | -0.34818 |

### weapon.crossbow — n=4748, R²=-1.412

intercept: `3.5236`  ·  log_price: True  ·  ilvl: `-0.04404`  ·  n_mods: `0.00167`  ·  n_top_tier: `0.39607`  ·  corrupted: `-0.00872`  ·  n_sockets: `0.02457`  ·  quality: `-0.00583`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -3.28934 |
| `desecrated.stat_1365232741@T1` | -3.14654 |
| `desecrated.stat_3131442032@T1` | -3.14654 |
| `explicit.stat_2250681686` | 2.94527 |
| `explicit.stat_709508406@T1` | 1.94314 |
| `explicit.stat_3336890334@T1` | 1.89869 |
| `explicit.stat_1037193709@T1` | 1.86812 |
| `explicit.stat_1967051901@T1` | 1.57940 |
| `explicit.stat_1509134228@T1` | 1.40049 |
| `explicit.stat_691932474@T1` | -1.31576 |
| `crafted.stat_3035140377` | 1.12611 |
| `explicit.stat_1202301673@T1` | 1.09529 |

### weapon.sceptre — n=1282, R²=0.0

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

### weapon.warstaff — n=1146, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

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
| `desecrated.stat_3336890334` | 0.00000 |
| `desecrated.stat_387439868` | 0.00000 |
| `desecrated.stat_4258524206` | 0.00000 |

### weapon.spear — n=1142, R²=0.0

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
| `explicit.stat_1263695895@T2` | -0.00000 |

### weapon.staff — n=1084, R²=0.0

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

### armour.focus — n=973, R²=0.0

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

### flask.charm — n=923, R²=-0.4606

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2541588185@T2` | 0.24991 |
| `explicit.stat_1873752457` | 0.00016 |
| `explicit.stat_1120862500@T2` | -0.00006 |
| `explicit.stat_2365392475@T2` | -0.00003 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_1873752457@T2` | -0.00003 |
| `explicit.stat_2566921799` | 0.00003 |
| `explicit.stat_3849649145` | -0.00002 |
| `explicit.stat_828533480@T2` | -0.00002 |
| `explicit.stat_828533480@T1` | -0.00002 |
| `explicit.stat_1366840608@T2` | 0.00002 |
| `explicit.stat_388617051@T2` | -0.00001 |

### armour.quiver — n=888, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`

| stat_id | coef |
|---|---|
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
| `explicit.stat_1573130764@T1` | 0.00000 |

### armour.shield — n=847, R²=0.0

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

### weapon.twomace — n=624, R²=0.0

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

- … **Emerald** — 3591 listings (3591 priced) [0.5–856.7 ex]
- … **Sapphire** — 3509 listings (3509 priced) [0.4–856.7 ex]
- … **Ruby** — 2825 listings (2825 priced) [0.3–856.7 ex]
- … **Utility Belt** — 2691 listings (2691 priced) [0.3–77723.4 ex]
- … **Stellar Amulet** — 2008 listings (2008 priced) [0.3–38861.7 ex]
- … **Dueling Wand** — 1856 listings (1856 priced) [0.8–856.7 ex]
- … **Solar Amulet** — 1646 listings (1646 priced) [1.0–856.7 ex]
- … **Gold Amulet** — 1618 listings (1618 priced) [0.6–856.7 ex]
- … **Prismatic Ring** — 1560 listings (1560 priced) [0.3–856.7 ex]
- … **Amethyst Ring** — 1477 listings (1477 priced) [0.8–856.7 ex]
- … **Gold Ring** — 1456 listings (1456 priced) [0.7–856.7 ex]
- … **Obliterator Bow** — 1422 listings (1422 priced) [0.9–856.7 ex]
- … **Plate Belt** — 1310 listings (1310 priced) [1.0–856.7 ex]
- … **Topaz Ring** — 1204 listings (1204 priced) [1.0–856.7 ex]
- … **Heavy Belt** — 1201 listings (1201 priced) [0.5–856.7 ex]
- … **Sapphire Ring** — 1190 listings (1190 priced) [0.5–856.7 ex]
- … **Ancestral Tiara** — 1172 listings (1172 priced) [1.0–856.7 ex]
- … **Ruby Ring** — 1140 listings (1140 priced) [0.4–856.7 ex]
- … **Lapis Amulet** — 1092 listings (1092 priced) [0.6–856.7 ex]
- … **Galvanic Wand** — 1063 listings (1063 priced) [1.0–856.7 ex]
- … **Amber Amulet** — 1060 listings (1060 priced) [0.6–856.7 ex]
- … **Jade Amulet** — 1056 listings (1056 priced) [0.6–856.7 ex]
- … **Siphoning Wand** — 1039 listings (1039 priced) [1.0–856.7 ex]
- … **Warmonger Bow** — 1011 listings (1011 priced) [1.0–856.7 ex]
- … **Attuned Wand** — 970 listings (970 priced) [0.3–856.7 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-04T11:05:12+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **102861** (102861 priced in exalted)
- Distinct bases: 861 · distinct mods: 2076 · mod rows: 498099
- Sold signals: **24134** sold · 27961 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-04T11:00:44+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.66** (median |log error| 2.0362)
- Within ±30% of asking price: **29%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 65% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×25.96 · ±30% 11% · n=14262
- Premium segment (60ex+): skill **+0.11** · typical error ×141.75 · ±30% 1% · n=8004
- Sold listings (clearing prices): skill **-0.00** · typical error ×3.72 · ±30% 40% · n=6504

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.amulet | 1747 | ×17.90 | 7% | -0.06 | -0.10 |
| accessory.belt | 1704 | ×9.28 | 26% | +0.02 | +0.04 |
| accessory.ring | 1670 | ×7.09 | 6% | -0.00 | +0.02 |
| armour.helmet | 1632 | ×8.60 | 21% | +0.01 | +0.06 |
| armour.chest | 1620 | ×7.68 | 23% | +0.04 | +0.10 |
| armour.gloves | 1465 | ×10.00 | 36% | -0.02 | -0.07 |
| armour.boots | 1442 | ×10.00 | 31% | -0.01 | -0.08 |
| other | 1348 | ×9.94 | 27% | +0.38 | +0.36 |
| weapon.wand | 1155 | ×9.18 | 32% | +0.04 | +0.08 |
| jewel | 1129 | ×5.94 | 10% | +0.05 | +0.07 |
| weapon.bow | 1014 | ×8.73 | 34% | +0.08 | +0.08 |
| weapon.crossbow | 946 | ×8.55 | 29% | +0.07 | +0.10 |
| weapon.sceptre | 239 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.staff | 210 | ×1.00 | 95% | +0.00 | +0.00 |
| weapon.spear | 207 | ×1.00 | 100% | n/a | - |
| armour.focus | 201 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.warstaff | 197 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 160 | ×1.00 | 98% | +0.00 | +0.00 |
| armour.shield | 157 | ×1.00 | 96% | +0.00 | +0.00 |
| weapon.twomace | 117 | ×1.00 | 98% | +0.00 | +0.00 |
| flask.charm | 62 | ×1.00 | 87% | -0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=12078, R²=-0.3255

intercept: `1.5442`  ·  log_price: True  ·  ilvl: `0.00367`  ·  n_mods: `0.00684`  ·  n_top_tier: `0.14077`  ·  corrupted: `4.07705`  ·  n_sockets: `-0.07969`  ·  quality: `-0.00952`

| stat_id | coef |
|---|---|
| `explicit.stat_101878827@T1` | 4.47298 |
| `explicit.stat_3141070085@T1` | 4.45317 |
| `explicit.stat_2968503605@T1` | 4.13419 |
| `explicit.stat_736967255@T1` | 1.44313 |
| `explicit.stat_789117908@T1` | 0.95696 |
| `explicit.stat_2974417149@T1` | 0.70987 |
| `explicit.stat_124131830` | -0.69901 |
| `explicit.stat_2891184298@T1` | -0.54292 |
| `implicit.stat_1379411836` | -0.28051 |
| `implicit.stat_718638445` | 0.24541 |
| `implicit.stat_3182714256` | 0.24536 |
| `explicit.stat_1671376347@T2` | -0.22942 |

### accessory.amulet — n=7947, R²=-2.3466

intercept: `4.9947`  ·  log_price: True  ·  ilvl: `-0.05669`  ·  n_mods: `-0.12402`  ·  n_top_tier: `0.03660`  ·  corrupted: `-0.20771`  ·  n_sockets: `0.25789`  ·  quality: `0.68594`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | 2.95333 |
| `explicit.stat_1671376347@T1` | 2.13481 |
| `explicit.stat_587431675@T1` | 1.90043 |
| `explicit.stat_9187492` | 1.81213 |
| `explicit.stat_2162097452@T2` | -1.69628 |
| `explicit.stat_9187492@T2` | -1.41690 |
| `explicit.stat_3261801346@T2` | 1.24669 |
| `explicit.stat_2162097452` | 1.24269 |
| `explicit.stat_124131830` | 1.12557 |
| `explicit.stat_2923486259@T1` | -0.93471 |
| `explicit.stat_3981240776@T2` | -0.89130 |
| `explicit.stat_3981240776@T1` | -0.88829 |

### accessory.ring — n=7764, R²=-1.8416

intercept: `4.2138`  ·  log_price: True  ·  ilvl: `-0.02492`  ·  n_mods: `-0.26654`  ·  n_top_tier: `0.67841`  ·  corrupted: `0.47808`  ·  n_sockets: `2.90242`  ·  quality: `0.03514`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 3.49796 |
| `explicit.stat_707457662@T2` | 3.23271 |
| `explicit.stat_2557965901@T2` | 2.33016 |
| `explicit.stat_2557965901@T1` | 2.14792 |
| `explicit.stat_1573130764@T1` | -2.07983 |
| `explicit.stat_3299347043@T1` | -2.00855 |
| `explicit.stat_2923486259@T2` | -1.53380 |
| `explicit.stat_2923486259@T1` | -1.44899 |
| `explicit.stat_3695891184@T1` | -1.38405 |
| `explicit.stat_1368271171@T2` | -1.25288 |
| `explicit.stat_1368271171@T1` | -1.23107 |
| `explicit.stat_2231156303@T2` | -1.20683 |

### accessory.belt — n=7741, R²=-1.2326

intercept: `4.1627`  ·  log_price: True  ·  ilvl: `-0.05000`  ·  n_mods: `-0.03016`  ·  n_top_tier: `0.10547`  ·  corrupted: `0.10523`  ·  n_sockets: `-0.13095`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.81445 |
| `explicit.stat_2923486259@T2` | 1.14649 |
| `explicit.stat_2923486259@T1` | 1.10804 |
| `explicit.stat_1836676211@T1` | 0.59655 |
| `explicit.stat_3299347043@T1` | -0.29431 |
| `explicit.stat_3299347043@T2` | -0.22863 |
| `explicit.stat_1389754388@T1` | -0.16295 |
| `explicit.stat_4080418644@T2` | -0.15747 |
| `explicit.stat_809229260@T2` | -0.15384 |
| `explicit.stat_2881298780@T1` | -0.14941 |
| `explicit.stat_644456512@T2` | -0.13853 |
| `explicit.stat_3325883026@T1` | -0.13360 |

### armour.chest — n=7469, R²=-1.3609

intercept: `3.6106`  ·  log_price: True  ·  ilvl: `-0.04491`  ·  n_mods: `-0.02376`  ·  n_top_tier: `0.68181`  ·  corrupted: `0.06359`  ·  n_sockets: `-0.01259`  ·  quality: `0.02070`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 1.93046 |
| `implicit.stat_2251279027` | 1.67196 |
| `explicit.stat_3981240776@T1` | 1.18626 |
| `explicit.stat_2923486259@T1` | -0.93663 |
| `explicit.stat_3261801346@T2` | -0.84517 |
| `explicit.stat_3261801346@T1` | -0.80984 |
| `explicit.stat_3301100256@T2` | -0.80620 |
| `explicit.stat_2923486259@T2` | -0.80267 |
| `explicit.stat_2339757871@T1` | -0.79085 |
| `explicit.stat_4052037485@T1` | -0.78810 |
| `explicit.stat_3033371881@T1` | -0.76942 |
| `explicit.stat_986397080@T2` | -0.75260 |

### armour.helmet — n=7454, R²=-1.3156

intercept: `4.0791`  ·  log_price: True  ·  ilvl: `-0.05173`  ·  n_mods: `-0.01814`  ·  n_top_tier: `0.75091`  ·  corrupted: `0.15199`  ·  n_sockets: `-0.02337`  ·  quality: `0.03616`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 7.67430 |
| `explicit.stat_2339757871@T1` | -1.71470 |
| `explicit.stat_3033371881@T1` | -1.45676 |
| `explicit.stat_3033371881@T2` | -1.40195 |
| `explicit.stat_3362812763@T1` | -0.97679 |
| `explicit.stat_3325883026@T1` | -0.92932 |
| `explicit.stat_3362812763@T2` | -0.92527 |
| `explicit.stat_803737631@T2` | -0.88411 |
| `explicit.stat_4015621042@T2` | -0.84997 |
| `explicit.stat_3325883026@T2` | -0.84549 |
| `explicit.stat_3321629045@T2` | -0.84270 |
| `explicit.stat_2451402625@T1` | -0.82988 |

### armour.boots — n=6868, R²=-0.1594

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.59996`  ·  corrupted: `0.00001`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1062208444@T1` | -0.60000 |
| `explicit.stat_3484657501@T1` | -0.59999 |
| `explicit.stat_3033371881@T2` | -0.59999 |
| `explicit.stat_3484657501@T2` | -0.59999 |
| `explicit.stat_4220027924@T1` | -0.59998 |
| `explicit.stat_2339757871@T1` | -0.59998 |
| `explicit.stat_3362812763@T2` | -0.59998 |
| `explicit.stat_1062208444@T2` | -0.59997 |
| `explicit.stat_3639275092@T1` | -0.59997 |
| `explicit.stat_3261801346@T2` | -0.59997 |
| `explicit.stat_1050105434@T2` | -0.59997 |
| `explicit.stat_2451402625@T1` | -0.59997 |

### armour.gloves — n=6817, R²=-0.2306

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.05468`  ·  corrupted: `0.01330`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3556824919@T1` | 0.42589 |
| `explicit.stat_4067062424@T1` | 0.41552 |
| `desecrated.stat_3032590688` | 0.16212 |
| `explicit.stat_2923486259@T2` | 0.06253 |
| `explicit.stat_2339757871@T1` | -0.05587 |
| `explicit.stat_3484657501@T2` | -0.05474 |
| `explicit.stat_4052037485@T1` | -0.05473 |
| `explicit.stat_4015621042@T1` | -0.05470 |
| `explicit.stat_3484657501@T1` | -0.05470 |
| `explicit.stat_2451402625@T2` | -0.05470 |
| `explicit.stat_2797971005@T2` | -0.05469 |
| `explicit.stat_3362812763@T1` | -0.05469 |

### jewel — n=5708, R²=-0.9868

intercept: `-1.6097`  ·  log_price: True  ·  ilvl: `0.04029`  ·  n_mods: `0.12281`  ·  n_top_tier: `-0.44346`  ·  corrupted: `0.48534`

| stat_id | coef |
|---|---|
| `explicit.stat_1569159338@T1` | 5.51400 |
| `explicit.stat_2456523742@T1` | 5.37928 |
| `explicit.stat_3377888098@T1` | -4.63102 |
| `explicit.stat_2011656677@T1` | 4.43774 |
| `explicit.stat_293638271@T1` | -4.40535 |
| `explicit.stat_3851254963@T1` | 4.11286 |
| `explicit.stat_795138349@T1` | -3.87120 |
| `explicit.stat_21071013@T1` | 3.75130 |
| `explicit.stat_3787460122@T1` | 3.63888 |
| `explicit.stat_1697951953@T1` | 3.31995 |
| `explicit.stat_429143663@T1` | 3.18667 |
| `explicit.stat_1836676211@T1` | -3.15390 |

### weapon.wand — n=5419, R²=-1.5786

intercept: `3.3613`  ·  log_price: True  ·  ilvl: `-0.04184`  ·  n_mods: `-0.01433`  ·  n_top_tier: `0.38404`  ·  corrupted: `0.00158`  ·  n_sockets: `0.01308`  ·  quality: `0.02569`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.13236 |
| `explicit.stat_591105508@T1` | 1.99595 |
| `explicit.stat_1545858329@T1` | 1.91575 |
| `explicit.stat_736967255@T2` | 1.72546 |
| `explicit.stat_4226189338@T1` | 1.70937 |
| `explicit.stat_2254480358@T1` | 1.44172 |
| `explicit.stat_1600707273@T2` | 1.37890 |
| `crafted.stat_124131830` | 1.20941 |
| `explicit.stat_1600707273@T1` | 0.96813 |
| `explicit.stat_124131830@T2` | -0.49606 |
| `explicit.stat_2768835289@T2` | -0.48012 |
| `explicit.stat_3962278098@T2` | -0.47238 |

### weapon.bow — n=4634, R²=-1.5002

intercept: `3.3537`  ·  log_price: True  ·  ilvl: `-0.04169`  ·  n_mods: `-0.02276`  ·  n_top_tier: `0.35103`  ·  corrupted: `-0.06471`  ·  n_sockets: `0.00997`  ·  quality: `-0.00194`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -6.87436 |
| `explicit.stat_2463230181@T1` | 1.93625 |
| `explicit.stat_1509134228@T1` | 1.81927 |
| `explicit.stat_518292764@T1` | 1.77863 |
| `explicit.stat_1202301673@T1` | 1.65679 |
| `crafted.stat_3035140377` | 1.10365 |
| `explicit.stat_821021828@T1` | -0.48683 |
| `explicit.stat_2694482655@T1` | -0.47049 |
| `explicit.stat_1940865751@T1` | -0.44364 |
| `explicit.stat_1263695895@T1` | -0.43868 |
| `explicit.stat_821021828@T2` | -0.43100 |
| `explicit.stat_691932474@T2` | -0.41975 |

### weapon.crossbow — n=4352, R²=-1.3674

intercept: `3.5698`  ·  log_price: True  ·  ilvl: `-0.04488`  ·  n_mods: `0.00359`  ·  n_top_tier: `0.27044`  ·  corrupted: `0.07176`  ·  n_sockets: `0.03204`  ·  quality: `-0.00570`

| stat_id | coef |
|---|---|
| `desecrated.stat_3131442032@T1` | -5.40075 |
| `desecrated.stat_1365232741@T1` | -5.40075 |
| `explicit.stat_2250681686@T2` | -3.24562 |
| `explicit.stat_2250681686` | 3.05559 |
| `explicit.stat_709508406@T1` | 2.10925 |
| `explicit.stat_3336890334@T1` | 2.01089 |
| `explicit.stat_1037193709@T1` | 1.98526 |
| `explicit.stat_1509134228@T1` | 1.85126 |
| `explicit.stat_1202301673@T1` | 1.55768 |
| `explicit.stat_691932474@T1` | -1.50540 |
| `explicit.stat_1967051901@T1` | 1.30621 |
| `explicit.stat_1263695895@T1` | 1.03805 |

### weapon.sceptre — n=1217, R²=0.0

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

### weapon.spear — n=1080, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
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

### weapon.warstaff — n=1033, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_210067635` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |
| `desecrated.stat_387439868` | 0.00000 |
| `desecrated.stat_4258524206` | 0.00000 |
| `desecrated.stat_4258524206@T1` | -0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |

### weapon.staff — n=995, R²=0.0

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

### armour.focus — n=939, R²=0.0

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

### flask.charm — n=898, R²=-0.3837

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2541588185@T2` | 0.24984 |
| `explicit.stat_1873752457` | 0.00011 |
| `explicit.stat_1120862500@T2` | -0.00006 |
| `explicit.stat_1873752457@T2` | -0.00003 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_2566921799` | 0.00002 |
| `explicit.stat_2365392475@T2` | -0.00002 |
| `explicit.stat_3849649145` | -0.00002 |
| `explicit.stat_3196823591@T2` | 0.00001 |
| `implicit.stat_3676540188` | -0.00001 |
| `explicit.stat_828533480@T2` | -0.00001 |
| `implicit.stat_1810482573` | -0.00001 |

### armour.quiver — n=810, R²=0.0

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

### armour.shield — n=800, R²=0.0

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

### weapon.twomace — n=572, R²=0.0

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

- … **Emerald** — 3058 listings (3058 priced) [0.5–856.7 ex]
- … **Sapphire** — 2933 listings (2933 priced) [0.4–856.7 ex]
- … **Utility Belt** — 2463 listings (2463 priced) [0.3–52877.4 ex]
- … **Ruby** — 2406 listings (2406 priced) [0.3–856.7 ex]
- … **Stellar Amulet** — 1819 listings (1819 priced) [0.3–39823.2 ex]
- … **Dueling Wand** — 1720 listings (1720 priced) [0.8–856.7 ex]
- … **Solar Amulet** — 1500 listings (1500 priced) [1.0–856.7 ex]
- … **Gold Amulet** — 1453 listings (1453 priced) [0.6–856.7 ex]
- … **Prismatic Ring** — 1387 listings (1387 priced) [0.3–856.7 ex]
- … **Obliterator Bow** — 1328 listings (1328 priced) [0.4–856.7 ex]
- … **Amethyst Ring** — 1324 listings (1324 priced) [0.8–856.7 ex]
- … **Gold Ring** — 1295 listings (1295 priced) [0.7–856.7 ex]
- … **Plate Belt** — 1200 listings (1200 priced) [1.0–856.7 ex]
- … **Heavy Belt** — 1099 listings (1099 priced) [0.5–856.7 ex]
- … **Sapphire Ring** — 1080 listings (1080 priced) [0.5–856.7 ex]
- … **Topaz Ring** — 1079 listings (1079 priced) [1.0–856.7 ex]
- … **Ancestral Tiara** — 1067 listings (1067 priced) [1.0–856.7 ex]
- … **Ruby Ring** — 1016 listings (1016 priced) [0.4–856.7 ex]
- … **Galvanic Wand** — 985 listings (985 priced) [1.0–856.7 ex]
- … **Lapis Amulet** — 985 listings (985 priced) [0.6–856.7 ex]
- … **Jade Amulet** — 956 listings (956 priced) [0.6–856.7 ex]
- … **Amber Amulet** — 951 listings (951 priced) [0.6–856.7 ex]
- … **Siphoning Wand** — 947 listings (947 priced) [1.0–856.7 ex]
- … **Warmonger Bow** — 931 listings (931 priced) [0.9–856.7 ex]
- … **Attuned Wand** — 896 listings (896 priced) [0.3–856.7 ex]

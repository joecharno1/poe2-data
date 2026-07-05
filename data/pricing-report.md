# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-05T00:01:12+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **134778** (134778 priced in exalted)
- Distinct bases: 892 · distinct mods: 2252 · mod rows: 645077
- Sold signals: **34188** sold · 54362 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-04T23:53:15+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.86** (median |log error| 2.0623)
- Within ±30% of asking price: **29%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 65% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×23.57 · ±30% 12% · n=18503
- Premium segment (60ex+): skill **+0.10** · typical error ×131.20 · ±30% 1% · n=10548
- Sold listings (clearing prices): skill **+0.01** · typical error ×6.09 · ±30% 41% · n=5966

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 2331 | ×7.22 | 6% | -0.03 | -0.03 |
| accessory.amulet | 2235 | ×24.30 | 8% | -0.04 | -0.08 |
| accessory.belt | 2186 | ×9.49 | 25% | +0.03 | +0.06 |
| armour.chest | 2076 | ×8.51 | 22% | +0.02 | +0.08 |
| armour.helmet | 2060 | ×8.63 | 21% | +0.01 | +0.08 |
| armour.gloves | 1906 | ×10.00 | 36% | +0.00 | -0.03 |
| armour.boots | 1904 | ×6.95 | 34% | -0.01 | -0.03 |
| other | 1813 | ×9.98 | 36% | +0.43 | +0.41 |
| jewel | 1780 | ×7.33 | 7% | -0.01 | +0.02 |
| weapon.wand | 1401 | ×9.08 | 34% | +0.05 | +0.09 |
| weapon.bow | 1232 | ×8.84 | 36% | +0.09 | +0.06 |
| weapon.crossbow | 1177 | ×8.61 | 30% | +0.07 | +0.14 |
| weapon.sceptre | 275 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.spear | 273 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.warstaff | 267 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.staff | 263 | ×1.00 | 98% | +0.00 | +0.00 |
| armour.focus | 216 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 216 | ×1.00 | 96% | +0.00 | +0.00 |
| armour.shield | 187 | ×1.00 | 95% | +0.00 | +0.00 |
| weapon.twomace | 150 | ×1.00 | 97% | +0.00 | +0.00 |
| flask.charm | 125 | ×1.00 | 100% | n/a | - |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=16324, R²=-0.398

intercept: `1.4937`  ·  log_price: True  ·  ilvl: `0.00343`  ·  n_mods: `0.07903`  ·  n_top_tier: `0.18447`  ·  corrupted: `3.22178`  ·  n_sockets: `-0.06254`  ·  quality: `-0.00670`

| stat_id | coef |
|---|---|
| `explicit.stat_2891184298@T1` | 4.50567 |
| `explicit.stat_1589917703@T1` | 4.26679 |
| `explicit.stat_3141070085@T1` | 4.24188 |
| `explicit.stat_101878827@T1` | 4.22452 |
| `explicit.stat_2968503605@T1` | 4.22334 |
| `explicit.stat_2974417149@T1` | 1.87492 |
| `implicit.stat_3182714256` | 0.39597 |
| `implicit.stat_718638445` | 0.39230 |
| `implicit.stat_1379411836` | -0.30229 |
| `implicit.stat_958696139` | 0.27799 |
| `explicit.stat_124131830` | 0.26260 |
| `explicit.stat_1050105434@T1` | 0.24840 |

### accessory.ring — n=10646, R²=-1.8157

intercept: `3.5168`  ·  log_price: True  ·  ilvl: `-0.02720`  ·  n_mods: `-0.16384`  ·  n_top_tier: `0.59699`  ·  corrupted: `0.50534`  ·  n_sockets: `3.51847`  ·  quality: `0.01509`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.69882 |
| `explicit.stat_707457662@T2` | 4.30131 |
| `explicit.stat_1573130764@T1` | -1.94175 |
| `explicit.stat_3299347043@T1` | -1.83039 |
| `explicit.stat_1368271171@T1` | -1.82183 |
| `explicit.stat_2231156303@T1` | -1.42559 |
| `explicit.stat_2231156303@T2` | -1.41381 |
| `explicit.stat_3291658075@T2` | -1.40795 |
| `explicit.stat_3695891184@T2` | -1.37115 |
| `explicit.stat_1368271171@T2` | -1.32548 |
| `explicit.stat_2923486259@T1` | -1.27792 |
| `explicit.stat_789117908@T1` | -1.22609 |

### accessory.amulet — n=10514, R²=-2.4114

intercept: `4.2568`  ·  log_price: True  ·  ilvl: `-0.05303`  ·  n_mods: `-0.06602`  ·  n_top_tier: `1.00800`  ·  corrupted: `-0.01848`  ·  n_sockets: `0.09950`  ·  quality: `0.16863`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | 2.58706 |
| `explicit.stat_3981240776@T2` | -2.48330 |
| `explicit.stat_2162097452@T2` | -2.45221 |
| `explicit.stat_3981240776@T1` | -2.41358 |
| `explicit.stat_2748665614@T1` | -2.19624 |
| `explicit.stat_2748665614@T2` | -1.74465 |
| `explicit.stat_803737631@T1` | -1.64495 |
| `explicit.stat_803737631@T2` | -1.60409 |
| `explicit.stat_2923486259@T1` | -1.57738 |
| `explicit.stat_3556824919@T1` | -1.51319 |
| `explicit.stat_4080418644@T1` | -1.42013 |
| `explicit.stat_3917489142@T2` | -1.40502 |

### accessory.belt — n=9936, R²=-1.2629

intercept: `3.7096`  ·  log_price: True  ·  ilvl: `-0.04483`  ·  n_mods: `-0.02202`  ·  n_top_tier: `-0.04651`  ·  corrupted: `0.05368`  ·  n_sockets: `-0.12126`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 2.09102 |
| `explicit.stat_2923486259@T1` | 1.82607 |
| `explicit.stat_1836676211@T1` | 1.07108 |
| `explicit.stat_2923486259@T2` | 0.80524 |
| `explicit.stat_3372524247@T1` | 0.28621 |
| `explicit.stat_3299347043@T1` | -0.22870 |
| `explicit.stat_4220027924@T1` | 0.14596 |
| `explicit.stat_1671376347@T1` | 0.14506 |
| `explicit.stat_3299347043@T2` | -0.13055 |
| `explicit.stat_2639966148` | 0.12320 |
| `explicit.stat_3585532255@T1` | 0.10389 |
| `explicit.stat_3585532255@T2` | 0.09762 |

### armour.chest — n=9684, R²=-1.3909

intercept: `3.7998`  ·  log_price: True  ·  ilvl: `-0.04678`  ·  n_mods: `-0.02283`  ·  n_top_tier: `0.49824`  ·  corrupted: `-0.01360`  ·  n_sockets: `-0.00515`  ·  quality: `0.01479`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.93919 |
| `explicit.stat_3981240776@T1` | 1.59778 |
| `rune.stat_836936635` | 1.49975 |
| `explicit.stat_2339757871@T2` | -0.63070 |
| `explicit.stat_3981240776@T2` | 0.62838 |
| `explicit.stat_2339757871@T1` | -0.61747 |
| `explicit.stat_4015621042@T2` | -0.60471 |
| `explicit.stat_3261801346@T2` | -0.59936 |
| `explicit.stat_3261801346@T1` | -0.59408 |
| `explicit.stat_2923486259@T1` | -0.56814 |
| `explicit.stat_986397080@T2` | -0.56458 |
| `explicit.stat_915769802@T1` | -0.56362 |

### armour.helmet — n=9564, R²=-1.3595

intercept: `4.4483`  ·  log_price: True  ·  ilvl: `-0.05627`  ·  n_mods: `-0.02536`  ·  n_top_tier: `0.80637`  ·  corrupted: `0.17280`  ·  n_sockets: `-0.00708`  ·  quality: `0.01560`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 5.97472 |
| `explicit.stat_2339757871@T1` | -1.79445 |
| `explicit.stat_3033371881@T1` | -1.00215 |
| `explicit.stat_3033371881@T2` | -0.95627 |
| `explicit.stat_4052037485@T2` | -0.95027 |
| `explicit.stat_3325883026@T1` | -0.92599 |
| `explicit.stat_803737631@T2` | -0.91700 |
| `explicit.stat_3325883026@T2` | -0.89606 |
| `explicit.stat_3321629045@T2` | -0.89605 |
| `explicit.stat_53045048@T1` | -0.88754 |
| `explicit.stat_1263695895@T1` | -0.87724 |
| `explicit.stat_3639275092@T1` | -0.87433 |

### jewel — n=8982, R²=-0.9311

intercept: `-1.2950`  ·  log_price: True  ·  ilvl: `0.03638`  ·  n_mods: `0.15368`  ·  n_top_tier: `-0.40691`  ·  corrupted: `0.43859`

| stat_id | coef |
|---|---|
| `explicit.stat_2301718443@T1` | -7.07679 |
| `explicit.stat_2456523742@T1` | 4.84681 |
| `explicit.stat_2011656677@T1` | 4.72299 |
| `explicit.stat_3759663284@T1` | -3.67119 |
| `explicit.stat_1569101201@T1` | 3.33797 |
| `explicit.stat_1062710370@T1` | -3.17705 |
| `explicit.stat_21071013@T1` | -3.03780 |
| `explicit.stat_1852872083@T1` | -2.60733 |
| `explicit.stat_1459321413@T1` | 2.56076 |
| `explicit.stat_3141070085@T1` | 2.47878 |
| `explicit.stat_3851254963@T1` | 2.43476 |
| `explicit.stat_795138349@T1` | -2.34007 |

### armour.boots — n=8965, R²=-0.1548

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.12723`  ·  corrupted: `0.00002`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 0.55494 |
| `explicit.stat_2923486259@T1` | 0.24306 |
| `explicit.stat_2339757871@T1` | -0.12741 |
| `explicit.stat_1062208444@T1` | -0.12726 |
| `explicit.stat_3639275092@T1` | -0.12725 |
| `explicit.stat_2451402625@T2` | -0.12724 |
| `explicit.stat_99927264@T2` | -0.12724 |
| `explicit.stat_3484657501@T1` | -0.12724 |
| `explicit.stat_3325883026@T2` | -0.12724 |
| `explicit.stat_4220027924@T1` | -0.12724 |
| `explicit.stat_2451402625@T1` | -0.12724 |
| `explicit.stat_3484657501@T2` | -0.12724 |

### armour.gloves — n=8905, R²=-0.2363

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.09614`  ·  corrupted: `0.00490`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 0.33203 |
| `desecrated.stat_3032590688` | 0.15498 |
| `explicit.stat_2339757871@T1` | -0.09641 |
| `explicit.stat_4015621042@T1` | -0.09617 |
| `explicit.stat_3362812763@T1` | -0.09616 |
| `explicit.stat_1062208444@T1` | -0.09616 |
| `explicit.stat_3484657501@T2` | -0.09616 |
| `explicit.stat_4080418644@T1` | -0.09616 |
| `explicit.stat_2797971005@T2` | -0.09616 |
| `explicit.stat_3917489142@T2` | -0.09615 |
| `explicit.stat_3695891184@T1` | -0.09615 |
| `explicit.stat_1671376347@T1` | -0.09615 |

### weapon.wand — n=6706, R²=-1.6434

intercept: `3.4562`  ·  log_price: True  ·  ilvl: `-0.04294`  ·  n_mods: `-0.01609`  ·  n_top_tier: `0.29394`  ·  corrupted: `-0.00986`  ·  n_sockets: `-0.00556`  ·  quality: `0.01975`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.58628 |
| `explicit.stat_1545858329@T1` | 2.03109 |
| `explicit.stat_591105508@T1` | 2.02770 |
| `explicit.stat_4226189338@T1` | 2.00336 |
| `explicit.stat_2254480358@T1` | 1.92666 |
| `explicit.stat_1600707273@T2` | 1.36576 |
| `explicit.stat_2968503605@T1` | 1.28574 |
| `crafted.stat_124131830` | 1.11889 |
| `explicit.stat_2768835289@T2` | -0.42354 |
| `explicit.stat_3962278098@T2` | -0.37044 |
| `explicit.stat_2968503605@T2` | -0.35731 |
| `explicit.stat_736967255@T2` | 0.33942 |

### weapon.bow — n=5664, R²=-1.5694

intercept: `3.4438`  ·  log_price: True  ·  ilvl: `-0.04285`  ·  n_mods: `-0.02929`  ·  n_top_tier: `0.41235`  ·  corrupted: `-0.06429`  ·  n_sockets: `0.00305`  ·  quality: `-0.00217`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -3.84508 |
| `explicit.stat_2463230181@T1` | 1.86560 |
| `explicit.stat_1509134228@T1` | 1.72402 |
| `explicit.stat_518292764@T1` | 1.69061 |
| `explicit.stat_1202301673@T1` | 1.66402 |
| `crafted.stat_3035140377` | 0.83663 |
| `rune.stat_3885405204` | -0.71182 |
| `desecrated.stat_210067635@T1` | -0.53801 |
| `explicit.stat_821021828@T1` | -0.51443 |
| `explicit.stat_1940865751@T1` | -0.50975 |
| `explicit.stat_2694482655@T1` | -0.48819 |
| `explicit.stat_691932474@T2` | -0.47998 |

### weapon.crossbow — n=5384, R²=-1.4465

intercept: `3.5545`  ·  log_price: True  ·  ilvl: `-0.04452`  ·  n_mods: `-0.00438`  ·  n_top_tier: `0.19308`  ·  corrupted: `-0.03504`  ·  n_sockets: `0.02128`  ·  quality: `-0.00347`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -3.33323 |
| `explicit.stat_2250681686` | 3.14973 |
| `desecrated.stat_1365232741@T1` | -2.32082 |
| `desecrated.stat_3131442032@T1` | -2.32082 |
| `explicit.stat_709508406@T1` | 2.14077 |
| `explicit.stat_1037193709@T1` | 2.06380 |
| `explicit.stat_3336890334@T1` | 2.05070 |
| `explicit.stat_1509134228@T1` | 2.03860 |
| `explicit.stat_1202301673@T1` | 1.77488 |
| `explicit.stat_691932474@T1` | -1.45675 |
| `explicit.stat_1263695895@T1` | 1.19880 |
| `crafted.stat_3035140377` | 1.11127 |

### weapon.sceptre — n=1386, R²=0.0

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

### weapon.warstaff — n=1333, R²=0.0

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

### weapon.spear — n=1261, R²=0.0

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

### weapon.staff — n=1260, R²=0.0

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

### flask.charm — n=1190, R²=-0.3972

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00005 |
| `explicit.stat_2365392475@T1` | -0.00004 |
| `explicit.stat_1120862500@T2` | -0.00003 |
| `explicit.stat_1873752457@T2` | -0.00003 |
| `explicit.stat_388617051@T2` | -0.00003 |
| `explicit.stat_828533480@T1` | -0.00002 |
| `explicit.stat_1873752457@T1` | -0.00002 |
| `explicit.stat_2365392475@T2` | -0.00002 |
| `explicit.stat_828533480@T2` | -0.00002 |
| `explicit.stat_2676834156@T2` | -0.00002 |
| `explicit.stat_1056492907` | 0.00002 |
| `explicit.stat_2566921799` | 0.00002 |

### armour.focus — n=1028, R²=0.0

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

### armour.quiver — n=983, R²=0.0

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

### armour.shield — n=898, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

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

### weapon.twomace — n=705, R²=0.0

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

- … **Emerald** — 4642 listings (4642 priced) [0.8–856.7 ex]
- … **Sapphire** — 4572 listings (4572 priced) [0.7–856.7 ex]
- … **Ruby** — 3712 listings (3712 priced) [0.3–856.7 ex]
- … **Utility Belt** — 3104 listings (3104 priced) [0.3–77723.4 ex]
- … **Stellar Amulet** — 2335 listings (2335 priced) [0.3–38371.8 ex]
- … **Dueling Wand** — 2100 listings (2100 priced) [1.0–856.7 ex]
- … **Gold Amulet** — 1962 listings (1962 priced) [0.8–856.7 ex]
- … **Solar Amulet** — 1953 listings (1953 priced) [1.0–856.7 ex]
- … **Prismatic Ring** — 1947 listings (1947 priced) [0.3–856.7 ex]
- … **Amethyst Ring** — 1837 listings (1837 priced) [0.8–856.7 ex]
- … **Gold Ring** — 1771 listings (1771 priced) [0.8–856.7 ex]
- … **Obliterator Bow** — 1604 listings (1604 priced) [0.8–856.7 ex]
- … **Plate Belt** — 1539 listings (1539 priced) [1.0–856.7 ex]
- … **Topaz Ring** — 1462 listings (1462 priced) [1.0–856.7 ex]
- … **Sapphire Ring** — 1443 listings (1443 priced) [0.9–856.7 ex]
- … **Heavy Belt** — 1411 listings (1411 priced) [0.5–856.7 ex]
- … **Ruby Ring** — 1409 listings (1409 priced) [1.0–856.7 ex]
- … **Ancestral Tiara** — 1365 listings (1365 priced) [1.0–856.7 ex]
- … **Lapis Amulet** — 1309 listings (1309 priced) [0.6–856.7 ex]
- … **Amber Amulet** — 1271 listings (1271 priced) [0.8–856.7 ex]
- … **Jade Amulet** — 1252 listings (1252 priced) [0.8–856.7 ex]
- … **Galvanic Wand** — 1205 listings (1205 priced) [0.6–856.7 ex]
- … **Siphoning Wand** — 1187 listings (1187 priced) [1.0–856.7 ex]
- … **Unset Ring** — 1138 listings (1138 priced) [1.0–856.7 ex]
- … **Warmonger Bow** — 1130 listings (1130 priced) [1.0–856.7 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-14T16:29:50+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **474828** (473863 priced in exalted)
- Distinct bases: 979 · distinct mods: 3051 · mod rows: 2255542
- Sold signals: **26722** sold · 263324 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-14T16:19:55+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.48** (median |log error| 3.1128)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×52.42 · ±30% 7% · n=67776
- Premium segment (60ex+): skill **+0.08** · typical error ×171.50 · ±30% 0% · n=44806

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 9383 | ×53.60 | 21% | +0.05 | +0.08 |
| accessory.amulet | 8740 | ×52.39 | 21% | +0.03 | +0.03 |
| jewel | 8706 | ×8.93 | 6% | +0.02 | +0.06 |
| accessory.belt | 6746 | ×10.04 | 17% | +0.03 | +0.03 |
| armour.chest | 6542 | ×16.35 | 5% | +0.01 | +0.03 |
| armour.helmet | 6454 | ×16.35 | 7% | +0.02 | +0.03 |
| armour.boots | 6001 | ×20.71 | 5% | +0.05 | +0.07 |
| armour.gloves | 5840 | ×20.27 | 5% | +0.05 | +0.07 |
| other | 5116 | ×9.93 | 35% | +0.09 | +0.19 |
| weapon.wand | 3800 | ×36.24 | 18% | +0.07 | +0.08 |
| weapon.bow | 3056 | ×30.44 | 18% | +0.09 | +0.08 |
| weapon.crossbow | 2889 | ×22.17 | 22% | +0.08 | +0.12 |
| weapon.warstaff | 1625 | ×29.85 | 20% | +0.10 | +0.09 |
| weapon.staff | 1515 | ×50.89 | 15% | +0.07 | +0.07 |
| weapon.sceptre | 1506 | ×42.98 | 7% | +0.12 | +0.10 |
| weapon.spear | 1278 | ×49.46 | 19% | +0.08 | +0.07 |
| armour.focus | 1026 | ×35.62 | 8% | +0.11 | +0.12 |
| armour.quiver | 1020 | ×31.11 | 13% | +0.07 | +0.12 |
| armour.shield | 834 | ×15.39 | 19% | +0.02 | +0.02 |
| flask.charm | 795 | ×50.00 | 35% | +0.02 | +0.03 |
| weapon.twomace | 752 | ×18.41 | 18% | +0.06 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=46674, R²=-0.8546

intercept: `-1.6109`  ·  log_price: True  ·  ilvl: `0.02972`  ·  n_mods: `0.53289`  ·  n_top_tier: `-0.14887`  ·  corrupted: `0.08943`  ·  quality: `0.22997`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.97680 |
| `explicit.stat_2301718443@T1` | 2.80688 |
| `explicit.stat_3780644166@T1` | -2.43681 |
| `explicit.stat_1697447343@T1` | -2.42719 |
| `explicit.stat_795138349@T1` | -2.06449 |
| `explicit.stat_234296660@T1` | -1.91680 |
| `explicit.stat_3485067555@T1` | 1.83977 |
| `explicit.stat_239367161@T1` | -1.78051 |
| `explicit.stat_3473929743@T1` | -1.77067 |
| `explicit.stat_627767961@T1` | -1.75801 |
| `explicit.stat_3174700878@T1` | 1.71976 |
| `explicit.stat_1405298142@T1` | -1.71898 |

### other — n=46177, R²=-0.4447

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00005`  ·  n_top_tier: `0.69314`  ·  corrupted: `0.69404`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1589917703@T1` | 3.18368 |
| `explicit.stat_3291658075@T1` | 2.77868 |
| `explicit.stat_2231156303@T1` | 1.96446 |
| `explicit.stat_101878827@T1` | 1.80378 |
| `explicit.stat_1050105434@T1` | -1.18886 |
| `explicit.stat_2968503605@T1` | 1.10910 |
| `explicit.stat_2891184298@T1` | 1.09736 |
| `explicit.stat_789117908@T1` | -1.08846 |
| `explicit.stat_3917489142@T1` | 0.98372 |
| `explicit.stat_2974417149@T1` | 0.88667 |
| `explicit.stat_2482852589@T1` | 0.87261 |
| `explicit.stat_3141070085@T1` | -0.74622 |

### accessory.ring — n=42913, R²=-1.9617

intercept: `3.8696`  ·  log_price: True  ·  ilvl: `-0.04776`  ·  n_mods: `0.00105`  ·  n_top_tier: `0.39365`  ·  corrupted: `0.08402`  ·  n_sockets: `1.46791`  ·  quality: `0.06783`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -0.44059 |
| `explicit.stat_2231156303@T1` | -0.43650 |
| `explicit.stat_803737631@T1` | -0.42096 |
| `explicit.stat_3325883026@T1` | -0.41997 |
| `explicit.stat_3962278098@T2` | -0.41879 |
| `explicit.stat_3291658075@T2` | -0.41782 |
| `explicit.stat_2144192055@T1` | -0.41701 |
| `explicit.stat_1368271171@T2` | -0.41677 |
| `explicit.stat_3291658075@T1` | -0.41638 |
| `explicit.stat_1263695895@T1` | -0.41586 |
| `explicit.stat_4220027924@T2` | -0.41409 |
| `explicit.stat_1263695895@T2` | -0.41310 |

### accessory.amulet — n=39830, R²=-2.1376

intercept: `3.9157`  ·  log_price: True  ·  ilvl: `-0.04770`  ·  n_mods: `-0.02041`  ·  n_top_tier: `1.11625`  ·  corrupted: `0.04228`  ·  n_sockets: `-0.11708`  ·  quality: `0.00160`

| stat_id | coef |
|---|---|
| `explicit.stat_2748665614@T1` | -1.20986 |
| `explicit.stat_2748665614@T2` | -1.19125 |
| `explicit.stat_472520716@T1` | -1.17158 |
| `explicit.stat_2162097452@T2` | -1.16986 |
| `explicit.stat_803737631@T1` | -1.16556 |
| `explicit.stat_2901986750@T1` | -1.16506 |
| `explicit.stat_1050105434@T2` | -1.16465 |
| `explicit.stat_472520716@T2` | -1.16431 |
| `explicit.stat_2974417149@T1` | -1.15158 |
| `explicit.stat_3917489142@T2` | -1.15146 |
| `explicit.stat_3917489142@T1` | -1.14748 |
| `explicit.stat_2866361420@T1` | -1.14545 |

### accessory.belt — n=30934, R²=-0.2749

intercept: `3.8660`  ·  log_price: True  ·  ilvl: `-0.01759`  ·  n_mods: `-0.20862`  ·  n_top_tier: `0.40926`  ·  corrupted: `0.32730`  ·  n_sockets: `-0.20700`

| stat_id | coef |
|---|---|
| `implicit.stat_731781020` | 0.95459 |
| `explicit.stat_1389754388@T1` | -0.64882 |
| `explicit.stat_2881298780@T1` | -0.54970 |
| `explicit.stat_3299347043@T1` | -0.53002 |
| `explicit.stat_51994685@T1` | -0.52646 |
| `explicit.stat_1389754388@T2` | -0.49415 |
| `explicit.stat_3299347043@T2` | -0.48813 |
| `explicit.stat_2923486259@T1` | -0.48523 |
| `explicit.stat_809229260@T2` | -0.48450 |
| `explicit.stat_2923486259@T2` | -0.48441 |
| `explicit.stat_1050105434@T1` | -0.47815 |
| `explicit.stat_1671376347@T2` | -0.47377 |

### armour.chest — n=30568, R²=-0.636

intercept: `3.9534`  ·  log_price: True  ·  ilvl: `-0.03609`  ·  n_mods: `-0.13992`  ·  n_top_tier: `0.37415`  ·  corrupted: `0.34371`  ·  n_sockets: `0.11326`  ·  quality: `0.02426`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.61250 |
| `explicit.stat_4080418644@T1` | -0.89568 |
| `explicit.stat_2923486259@T1` | -0.77093 |
| `explicit.stat_3484657501@T1` | -0.62805 |
| `explicit.stat_3261801346@T2` | -0.62474 |
| `explicit.stat_124859000@T2` | -0.60869 |
| `explicit.stat_4080418644@T2` | -0.52773 |
| `explicit.stat_3362812763@T1` | -0.52238 |
| `explicit.stat_2451402625@T2` | -0.51399 |
| `explicit.stat_3325883026@T2` | -0.50189 |
| `explicit.stat_915769802@T2` | -0.49743 |
| `explicit.stat_3639275092@T2` | -0.48578 |

### armour.helmet — n=29835, R²=-0.5004

intercept: `3.4109`  ·  log_price: True  ·  ilvl: `-0.02909`  ·  n_mods: `-0.11479`  ·  n_top_tier: `0.43705`  ·  corrupted: `0.85971`  ·  n_sockets: `0.06394`  ·  quality: `0.02932`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.38671 |
| `explicit.stat_2339757871@T1` | -0.88604 |
| `explicit.stat_53045048@T2` | -0.78936 |
| `explicit.stat_3917489142@T2` | -0.77549 |
| `explicit.stat_3261801346@T1` | -0.63223 |
| `explicit.stat_3321629045@T2` | -0.62894 |
| `explicit.stat_53045048@T1` | -0.59276 |
| `explicit.stat_3362812763@T2` | -0.57854 |
| `explicit.stat_1263695895@T2` | -0.56635 |
| `explicit.stat_1999113824@T1` | -0.54436 |
| `explicit.stat_3261801346@T2` | -0.52980 |
| `explicit.stat_1050105434@T2` | -0.51560 |

### armour.boots — n=27983, R²=-0.99

intercept: `4.4035`  ·  log_price: True  ·  ilvl: `-0.05066`  ·  n_mods: `-0.09242`  ·  n_top_tier: `0.62126`  ·  corrupted: `0.34415`  ·  n_sockets: `0.07068`  ·  quality: `0.02263`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.62077 |
| `explicit.stat_2250533757@T1` | 1.24919 |
| `explicit.stat_3299347043@T1` | -1.14604 |
| `explicit.stat_1062208444@T2` | -1.11098 |
| `explicit.stat_3917489142@T2` | -1.05699 |
| `explicit.stat_3917489142@T1` | -0.96143 |
| `explicit.stat_2923486259@T2` | -0.90110 |
| `explicit.stat_328541901@T1` | -0.87851 |
| `explicit.stat_2160282525@T1` | -0.82354 |
| `explicit.stat_53045048@T1` | -0.81089 |
| `explicit.stat_3321629045@T1` | -0.80337 |
| `explicit.stat_4052037485@T2` | -0.79259 |

### armour.gloves — n=27309, R²=-0.9204

intercept: `3.8437`  ·  log_price: True  ·  ilvl: `-0.04866`  ·  n_mods: `-0.10443`  ·  n_top_tier: `0.47988`  ·  corrupted: `0.16431`  ·  n_sockets: `0.25607`  ·  quality: `0.03373`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | -5.16344 |
| `explicit.stat_2339757871@T1` | 1.84598 |
| `explicit.stat_3484657501@T2` | -1.38568 |
| `explicit.stat_803737631@T2` | -1.12214 |
| `explicit.stat_3917489142@T2` | -0.91729 |
| `explicit.stat_3484657501@T1` | -0.87584 |
| `explicit.stat_3321629045@T2` | -0.83303 |
| `explicit.stat_803737631@T1` | -0.83000 |
| `explicit.stat_1573130764@T1` | -0.81995 |
| `explicit.stat_9187492@T1` | 0.78847 |
| `explicit.stat_3917489142@T1` | -0.72685 |
| `explicit.stat_2923486259@T1` | -0.69308 |

### weapon.wand — n=17691, R²=-2.171

intercept: `3.8226`  ·  log_price: True  ·  ilvl: `-0.04723`  ·  n_mods: `-0.01588`  ·  n_top_tier: `0.32956`  ·  corrupted: `0.00159`  ·  n_sockets: `0.03439`  ·  quality: `0.00287`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.19404 |
| `rune.stat_124131830` | -3.12332 |
| `explicit.stat_2254480358@T1` | 2.75414 |
| `explicit.stat_591105508@T1` | 1.99681 |
| `explicit.stat_4226189338@T1` | 1.98735 |
| `explicit.stat_124131830@T1` | 1.98391 |
| `explicit.stat_736967255@T2` | 1.23367 |
| `crafted.stat_124131830` | 1.13709 |
| `explicit.stat_2768835289@T2` | 1.09921 |
| `explicit.stat_2254480358@T2` | 1.05324 |
| `explicit.stat_4226189338@T2` | 0.82629 |
| `explicit.stat_1600707273@T1` | 0.53288 |

### weapon.bow — n=14333, R²=-2.0014

intercept: `3.4520`  ·  log_price: True  ·  ilvl: `-0.04179`  ·  n_mods: `-0.03030`  ·  n_top_tier: `0.64114`  ·  corrupted: `-0.07055`  ·  n_sockets: `-0.00661`  ·  quality: `0.02914`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.33126 |
| `explicit.stat_1202301673@T1` | 1.61707 |
| `crafted.stat_3035140377` | 1.34711 |
| `desecrated.stat_666077204@T1` | 0.79864 |
| `explicit.stat_1263695895@T1` | -0.77332 |
| `explicit.stat_1263695895@T2` | -0.70553 |
| `explicit.stat_1368271171@T2` | -0.69843 |
| `explicit.stat_1509134228@T1` | -0.69476 |
| `explicit.stat_3695891184@T2` | -0.69150 |
| `explicit.stat_3695891184@T1` | -0.68664 |
| `explicit.stat_1037193709@T1` | -0.67869 |
| `explicit.stat_2694482655@T2` | -0.67444 |

### weapon.crossbow — n=13555, R²=-2.0135

intercept: `3.5579`  ·  log_price: True  ·  ilvl: `-0.04377`  ·  n_mods: `-0.00977`  ·  n_top_tier: `0.70953`  ·  corrupted: `-0.01162`  ·  n_sockets: `0.01227`  ·  quality: `0.00954`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.93284 |
| `explicit.stat_2250681686@T2` | -1.61035 |
| `explicit.stat_709508406@T1` | 1.53778 |
| `explicit.stat_1202301673@T1` | 1.31764 |
| `explicit.stat_1980802737` | 1.19057 |
| `explicit.stat_2250681686` | 0.95739 |
| `crafted.stat_3035140377` | 0.91692 |
| `explicit.stat_1202301673@T2` | -0.86235 |
| `explicit.stat_1263695895@T2` | -0.85245 |
| `explicit.stat_1263695895@T1` | -0.82474 |
| `explicit.stat_669069897@T1` | -0.77627 |
| `explicit.stat_1037193709@T2` | -0.76211 |

### flask.charm — n=11866, R²=-0.5175

intercept: `0.0007`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.67644`  ·  corrupted: `2.08380`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.37191 |
| `explicit.stat_1056492907` | 3.53165 |
| `explicit.stat_828533480@T2` | -2.67645 |
| `explicit.stat_3196823591@T2` | -2.67644 |
| `explicit.stat_2676834156@T2` | -2.67644 |
| `explicit.stat_1120862500@T2` | -2.67644 |
| `explicit.stat_1366840608@T2` | -2.67644 |
| `explicit.stat_2541588185@T2` | -2.67643 |
| `explicit.stat_828533480@T1` | -2.67643 |
| `explicit.stat_1873752457@T2` | -2.67643 |
| `explicit.stat_388617051@T2` | -2.67642 |
| `explicit.stat_1873752457@T1` | -2.67642 |

### weapon.warstaff — n=8056, R²=-0.5339

intercept: `-3.8899`  ·  log_price: True  ·  ilvl: `0.05372`  ·  n_mods: `-0.12210`  ·  n_top_tier: `0.65522`  ·  corrupted: `0.22530`  ·  n_sockets: `0.06413`  ·  quality: `0.06057`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.39530 |
| `explicit.stat_1037193709@T1` | 1.18078 |
| `explicit.stat_328541901@T1` | -1.08464 |
| `explicit.stat_328541901@T2` | -1.04867 |
| `crafted.stat_210067635@T2` | 0.82053 |
| `explicit.stat_55876295@T2` | -0.78287 |
| `explicit.stat_1037193709@T2` | -0.75536 |
| `explicit.stat_1940865751@T1` | -0.73069 |
| `explicit.stat_3336890334@T2` | -0.71613 |
| `explicit.stat_691932474@T2` | -0.71367 |
| `explicit.stat_55876295@T1` | -0.70792 |
| `explicit.stat_791928121@T2` | -0.69710 |

### weapon.staff — n=7429, R²=-0.5308

intercept: `-7.4028`  ·  log_price: True  ·  ilvl: `0.09508`  ·  n_mods: `-0.06992`  ·  n_top_tier: `0.34011`  ·  corrupted: `0.01264`  ·  n_sockets: `0.17015`  ·  quality: `0.06092`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 1.99931 |
| `explicit.stat_124131830@T1` | 1.92398 |
| `rune.stat_124131830` | 1.56411 |
| `explicit.stat_1600707273@T1` | 1.49420 |
| `explicit.stat_1545858329@T1` | 1.40958 |
| `explicit.stat_2254480358@T1` | 1.18341 |
| `explicit.stat_591105508@T1` | 1.08689 |
| `explicit.stat_2768835289@T2` | 0.83206 |
| `explicit.stat_4226189338@T2` | 0.82633 |
| `explicit.stat_3962278098@T2` | 0.68769 |
| `explicit.stat_1600707273@T2` | 0.57731 |
| `explicit.stat_1263695895@T2` | -0.57024 |

### weapon.sceptre — n=7424, R²=-0.4531

intercept: `-12.2804`  ·  log_price: True  ·  ilvl: `0.15456`  ·  n_mods: `-0.04134`  ·  n_top_tier: `0.63856`  ·  corrupted: `0.56084`  ·  n_sockets: `0.16605`  ·  quality: `0.06484`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.07302 |
| `explicit.stat_2162097452@T2` | 1.18357 |
| `explicit.stat_1263695895@T1` | -1.14205 |
| `explicit.stat_4080418644@T1` | -1.11047 |
| `explicit.stat_1263695895@T2` | -1.08302 |
| `explicit.stat_1574590649@T2` | -1.06936 |
| `explicit.stat_2347036682@T2` | -0.91497 |
| `explicit.stat_289128254@T2` | -0.77391 |
| `explicit.stat_1050105434@T2` | -0.75453 |
| `explicit.stat_2854751904@T2` | -0.72846 |
| `explicit.stat_3639275092@T2` | -0.62290 |
| `explicit.stat_4080418644@T2` | -0.60916 |

### weapon.spear — n=6192, R²=-0.6267

intercept: `-4.5124`  ·  log_price: True  ·  ilvl: `0.05969`  ·  n_mods: `-0.02275`  ·  n_top_tier: `0.74141`  ·  corrupted: `-0.05804`  ·  n_sockets: `0.10325`  ·  quality: `0.10355`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -5.14711 |
| `explicit.stat_1202301673@T1` | 2.16498 |
| `explicit.stat_9187492@T1` | 1.77337 |
| `crafted.stat_3035140377` | 1.11624 |
| `explicit.stat_1509134228@T1` | 0.90762 |
| `explicit.stat_55876295@T1` | -0.87160 |
| `desecrated.stat_210067635@T1` | -0.83351 |
| `explicit.stat_55876295@T2` | -0.82268 |
| `explicit.stat_1263695895@T2` | -0.82033 |
| `explicit.stat_1037193709@T1` | -0.81915 |
| `explicit.stat_1509134228@T2` | -0.75478 |
| `explicit.stat_3261801346@T2` | -0.72790 |

### armour.focus — n=5052, R²=-0.4573

intercept: `-10.2886`  ·  log_price: True  ·  ilvl: `0.12822`  ·  n_mods: `-0.07956`  ·  n_top_tier: `0.83896`  ·  corrupted: `0.76103`  ·  n_sockets: `0.37270`  ·  quality: `0.06811`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -4.08332 |
| `explicit.stat_4220027924@T2` | -1.18241 |
| `explicit.stat_3291658075@T1` | -1.08543 |
| `explicit.stat_3962278098@T2` | -1.07250 |
| `explicit.stat_3962278098@T1` | -1.04878 |
| `explicit.stat_2923486259@T1` | -0.95828 |
| `explicit.stat_736967255@T2` | -0.92916 |
| `explicit.stat_2974417149@T1` | -0.90304 |
| `explicit.stat_3372524247@T2` | -0.86267 |
| `explicit.stat_2231156303@T2` | -0.86200 |
| `explicit.stat_737908626@T2` | -0.84312 |
| `explicit.stat_2891184298@T2` | -0.83901 |

### armour.quiver — n=4735, R²=-0.4148

intercept: `-9.9479`  ·  log_price: True  ·  ilvl: `0.12161`  ·  n_mods: `-0.02721`  ·  n_top_tier: `0.89548`  ·  corrupted: `0.62166`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.17424 |
| `explicit.stat_2463230181@T1` | 2.60432 |
| `explicit.stat_2321178454@T2` | -1.32913 |
| `explicit.stat_2463230181@T2` | 1.26541 |
| `explicit.stat_681332047@T2` | -1.22379 |
| `explicit.stat_4067062424@T1` | -1.17083 |
| `explicit.stat_1573130764@T2` | -1.04486 |
| `explicit.stat_3261801346@T1` | -1.03632 |
| `explicit.stat_1573130764@T1` | -0.96979 |
| `explicit.stat_803737631@T2` | -0.90529 |
| `explicit.stat_2321178454@T1` | -0.87496 |
| `explicit.stat_1241625305@T2` | -0.84408 |

### armour.shield — n=4136, R²=-0.5689

intercept: `-7.6913`  ·  log_price: True  ·  ilvl: `0.09924`  ·  n_mods: `-0.05832`  ·  n_top_tier: `0.56078`  ·  corrupted: `0.22837`  ·  n_sockets: `0.13994`  ·  quality: `0.05227`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.97439 |
| `explicit.stat_1011760251@T1` | -1.52739 |
| `explicit.stat_1011760251@T2` | -1.08621 |
| `explicit.stat_2339757871@T1` | -0.98631 |
| `explicit.stat_4095671657@T1` | -0.80225 |
| `explicit.stat_328541901@T1` | -0.79265 |
| `explicit.stat_2923486259@T2` | -0.77349 |
| `explicit.stat_2481353198@T2` | -0.76495 |
| `explicit.stat_3372524247@T2` | -0.75084 |
| `explicit.stat_2481353198@T1` | -0.74940 |
| `explicit.stat_3321629045@T2` | -0.72872 |
| `explicit.stat_2881298780@T1` | -0.71445 |

### weapon.twomace — n=3807, R²=-0.5249

intercept: `-8.0310`  ·  log_price: True  ·  ilvl: `0.10455`  ·  n_mods: `-0.09452`  ·  n_top_tier: `0.48572`  ·  corrupted: `0.74294`  ·  n_sockets: `0.15681`  ·  quality: `0.03968`

| stat_id | coef |
|---|---|
| `desecrated.stat_1509134228@T1` | 2.34097 |
| `desecrated.stat_210067635@T1` | -2.06462 |
| `explicit.stat_1037193709@T1` | -1.46990 |
| `explicit.stat_3336890334@T1` | -1.28377 |
| `crafted.stat_3035140377` | 1.12233 |
| `explicit.stat_1263695895@T1` | -0.87917 |
| `explicit.stat_387439868@T2` | -0.82714 |
| `explicit.stat_1037193709@T2` | -0.78611 |
| `explicit.stat_518292764@T2` | -0.78585 |
| `explicit.stat_1263695895@T2` | -0.77617 |
| `explicit.stat_3695891184@T1` | -0.69395 |
| `explicit.stat_3639275092@T1` | -0.65934 |

## Coverage (listings per base)

- … **Sapphire** — 21828 listings (21798 priced) [0.3–7553463.8 ex]
- … **Emerald** — 21542 listings (21514 priced) [0.3–7553463.8 ex]
- … **Ruby** — 16446 listings (16432 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 9045 listings (9036 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 7346 listings (7336 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 7206 listings (7193 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 7041 listings (7034 priced) [0.2–19945827.9 ex]
- … **Gold Amulet** — 6739 listings (6729 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 6719 listings (6715 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 6604 listings (6593 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5632 listings (5617 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5501 listings (5495 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 5288 listings (5284 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5271 listings (5268 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 4798 listings (4784 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4727 listings (4722 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4633 listings (4626 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4577 listings (4575 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4577 listings (4571 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4535 listings (4529 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4426 listings (4421 priced) [0.3–4275054.0 ex]
- … **Obliterator Bow** — 4295 listings (4282 priced) [0.3–42622633798.0 ex]
- … **Heavy Belt** — 4282 listings (4279 priced) [0.3–2608914286.6 ex]
- … **Pearl Ring** — 4253 listings (4248 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 4174 listings (4174 priced) [0.3–123132003.2 ex]

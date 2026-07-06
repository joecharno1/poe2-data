# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-06T05:34:06+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **205614** (205525 priced in exalted)
- Distinct bases: 925 · distinct mods: 2542 · mod rows: 974530
- Sold signals: **37278** sold · 108325 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-06T05:27:34+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×13.87** (median |log error| 2.6298)
- Within ±30% of asking price: **22%**
- Skill vs constant-price guess: **+0.02** (> 0 = the mods carry signal)
- Calibration: 74% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.07** · typical error ×30.84 · ±30% 16% · n=29233
- Premium segment (60ex+): skill **+0.08** · typical error ×150.23 · ±30% 0% · n=17120
- Sold listings (clearing prices): skill **+0.34** · typical error ×6.67 · ±30% 0% · n=10

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 3758 | ×31.61 | 13% | +0.01 | -0.01 |
| accessory.amulet | 3673 | ×40.56 | 20% | +0.00 | +0.02 |
| jewel | 3230 | ×8.42 | 6% | +0.03 | +0.07 |
| accessory.belt | 3171 | ×9.09 | 28% | +0.04 | +0.04 |
| armour.chest | 3076 | ×10.00 | 32% | -0.00 | +0.00 |
| armour.helmet | 2997 | ×10.00 | 30% | -0.00 | +0.00 |
| armour.boots | 2805 | ×8.96 | 25% | -0.00 | +0.04 |
| armour.gloves | 2779 | ×11.02 | 5% | -0.02 | +0.02 |
| other | 2681 | ×9.97 | 38% | +0.06 | +0.16 |
| weapon.wand | 1979 | ×10.28 | 28% | +0.04 | +0.09 |
| weapon.bow | 1624 | ×9.83 | 25% | +0.06 | +0.07 |
| weapon.crossbow | 1524 | ×10.11 | 25% | +0.07 | +0.10 |
| weapon.warstaff | 498 | ×47.00 | 19% | +0.00 | +0.00 |
| weapon.staff | 470 | ×30.00 | 24% | +0.00 | +0.00 |
| weapon.sceptre | 448 | ×50.00 | 15% | +0.00 | +0.00 |
| weapon.spear | 356 | ×50.00 | 17% | -0.00 | +0.00 |
| armour.focus | 305 | ×20.00 | 20% | +0.23 | +0.00 |
| armour.quiver | 255 | ×35.00 | 14% | +0.00 | +0.00 |
| armour.shield | 233 | ×45.00 | 13% | +0.00 | +0.00 |
| flask.charm | 232 | ×2.00 | 47% | -0.00 | +0.00 |
| weapon.twomace | 192 | ×25.00 | 18% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=23827, R²=-0.4982

intercept: `1.6091`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00120`  ·  n_top_tier: `0.36538`  ·  corrupted: `3.39491`  ·  n_sockets: `-0.00005`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2891184298@T1` | 2.20697 |
| `explicit.stat_2974417149@T1` | 1.28717 |
| `explicit.stat_3291658075@T1` | 1.15699 |
| `explicit.stat_2106365538@T1` | 0.56924 |
| `explicit.stat_1589917703@T1` | -0.56816 |
| `explicit.stat_1050105434@T1` | -0.48842 |
| `explicit.stat_3141070085@T1` | 0.44726 |
| `explicit.stat_2968503605@T1` | 0.31887 |
| `explicit.stat_1589917703` | 0.31686 |
| `implicit.stat_1379411836` | -0.26844 |
| `explicit.stat_3917489142@T1` | 0.25599 |
| `implicit.stat_4041853756` | 0.23013 |

### accessory.ring — n=17530, R²=-2.1208

intercept: `5.3607`  ·  log_price: True  ·  ilvl: `-0.06243`  ·  n_mods: `-0.05417`  ·  n_top_tier: `-0.21663`  ·  corrupted: `0.76027`  ·  n_sockets: `3.72575`  ·  quality: `0.09178`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T2` | 1.90978 |
| `explicit.stat_1754445556@T1` | 1.65414 |
| `explicit.stat_3032590688@T2` | 1.63521 |
| `explicit.stat_2557965901@T1` | 0.69368 |
| `explicit.stat_707457662@T1` | 0.67091 |
| `explicit.stat_2557965901@T2` | 0.60371 |
| `implicit.stat_2748665614` | 0.46065 |
| `explicit.stat_1379411836@T1` | -0.43163 |
| `explicit.stat_2923486259@T1` | 0.41784 |
| `explicit.stat_707457662@T2` | 0.41045 |
| `explicit.stat_2923486259@T2` | 0.38094 |
| `explicit.stat_3372524247@T1` | 0.34507 |

### accessory.amulet — n=16858, R²=-2.2044

intercept: `4.0231`  ·  log_price: True  ·  ilvl: `-0.04890`  ·  n_mods: `-0.02380`  ·  n_top_tier: `0.23892`  ·  corrupted: `0.06643`  ·  n_sockets: `-0.03092`  ·  quality: `-0.00956`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -2.86261 |
| `explicit.stat_983749596@T2` | -2.15300 |
| `explicit.stat_3981240776@T2` | 1.36504 |
| `explicit.stat_124131830@T2` | 0.67552 |
| `explicit.stat_1202301673` | 0.66757 |
| `explicit.stat_124131830` | 0.62951 |
| `explicit.stat_1202301673@T2` | 0.56025 |
| `explicit.stat_3299347043@T1` | -0.50920 |
| `explicit.stat_2748665614@T1` | -0.41894 |
| `explicit.stat_983749596` | 0.37279 |
| `explicit.stat_3299347043@T2` | -0.37193 |
| `explicit.stat_2748665614@T2` | -0.34853 |

### jewel — n=16722, R²=-0.731

intercept: `-1.2689`  ·  log_price: True  ·  ilvl: `0.03613`  ·  n_mods: `0.24430`  ·  n_top_tier: `-0.39494`  ·  corrupted: `0.58121`  ·  quality: `0.20721`

| stat_id | coef |
|---|---|
| `explicit.stat_1869147066@T1` | 4.21680 |
| `explicit.stat_3824372849@T1` | 3.99149 |
| `explicit.stat_3714003708@T1` | -3.28493 |
| `explicit.stat_2118708619@T1` | -3.02291 |
| `explicit.stat_1316278494@T1` | -2.73535 |
| `explicit.stat_153777645@T1` | 2.60400 |
| `explicit.stat_1569101201@T1` | 2.49592 |
| `explicit.stat_3377888098@T1` | -2.43724 |
| `explicit.stat_2456523742@T1` | 2.37135 |
| `explicit.stat_2106365538@T1` | -2.33631 |
| `explicit.stat_1697951953@T1` | -2.29025 |
| `explicit.stat_1697447343@T1` | 2.23287 |

### accessory.belt — n=14451, R²=-0.0774

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.24439`  ·  corrupted: `0.00001`  ·  n_sockets: `1.57626`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.38831 |
| `explicit.stat_1389754388@T1` | -0.24441 |
| `explicit.stat_51994685@T1` | -0.24441 |
| `explicit.stat_1389754388@T2` | -0.24440 |
| `explicit.stat_644456512@T2` | -0.24440 |
| `explicit.stat_51994685@T2` | -0.24440 |
| `explicit.stat_3325883026@T1` | -0.24439 |
| `explicit.stat_1570770415@T1` | -0.24439 |
| `explicit.stat_644456512@T1` | -0.24439 |
| `explicit.stat_1570770415@T2` | -0.24439 |
| `explicit.stat_1836676211@T2` | -0.24439 |
| `explicit.stat_2881298780@T2` | -0.24439 |

### armour.chest — n=14231, R²=-0.2363

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.00577`  ·  corrupted: `0.00007`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_2923486259` | -0.03420 |
| `pseudo.total_chaos_res` | 0.03420 |
| `explicit.stat_2923486259` | -0.03420 |
| `desecrated.stat_3981240776` | 0.02170 |
| `desecrated.stat_4220027924` | -0.01213 |
| `desecrated.stat_3372524247` | -0.01157 |
| `pseudo.total_ele_res` | 0.01144 |
| `rune.stat_1671376347` | -0.01144 |
| `explicit.stat_1671376347` | -0.01144 |
| `rune.stat_4220027924` | -0.01144 |
| `explicit.stat_3372524247` | -0.01144 |
| `implicit.stat_3372524247` | -0.01144 |

### armour.helmet — n=13946, R²=-0.2531

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00274`  ·  corrupted: `0.00496`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3917489142` | 0.05249 |
| `rune.stat_3523867985` | 0.00770 |
| `explicit.stat_4080418644@T2` | -0.00277 |
| `explicit.stat_1062208444@T2` | -0.00276 |
| `explicit.stat_3321629045@T1` | -0.00276 |
| `explicit.stat_53045048@T2` | -0.00275 |
| `explicit.stat_803737631@T2` | -0.00275 |
| `explicit.stat_3325883026@T2` | -0.00275 |
| `explicit.stat_3033371881@T1` | -0.00275 |
| `explicit.stat_2451402625@T1` | -0.00275 |
| `explicit.stat_328541901@T2` | -0.00274 |
| `explicit.stat_4220027924@T2` | -0.00274 |

### armour.boots — n=13113, R²=-0.2625

intercept: `2.6110`  ·  log_price: True  ·  ilvl: `-0.00660`  ·  n_mods: `-0.04282`  ·  n_top_tier: `0.20937`  ·  corrupted: `0.07962`  ·  n_sockets: `0.01719`  ·  quality: `0.00216`

| stat_id | coef |
|---|---|
| `explicit.stat_1062208444@T2` | -1.29089 |
| `explicit.stat_4080418644@T1` | -1.29062 |
| `explicit.stat_2339757871@T1` | -0.70338 |
| `desecrated.stat_2250533757@T2` | -0.35836 |
| `rune.stat_836936635` | -0.30913 |
| `explicit.stat_3362812763@T1` | -0.30153 |
| `explicit.stat_3484657501@T2` | -0.29141 |
| `explicit.stat_328541901@T1` | -0.28836 |
| `explicit.stat_1062208444@T1` | -0.26269 |
| `explicit.stat_2451402625@T2` | -0.26001 |
| `explicit.stat_3261801346@T2` | -0.25836 |
| `explicit.stat_3917489142@T2` | -0.25797 |

### armour.gloves — n=12916, R²=-0.4595

intercept: `2.6927`  ·  log_price: True  ·  ilvl: `-0.02539`  ·  n_mods: `-0.03308`  ·  n_top_tier: `0.48275`  ·  corrupted: `0.17526`  ·  n_sockets: `0.06997`  ·  quality: `0.00120`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.49547 |
| `explicit.stat_803737631@T2` | -1.07864 |
| `explicit.stat_2797971005@T1` | -1.05265 |
| `explicit.stat_681332047@T2` | -0.95147 |
| `explicit.stat_2797971005@T2` | -0.88786 |
| `explicit.stat_3484657501@T2` | -0.82684 |
| `explicit.stat_1573130764@T1` | -0.82381 |
| `explicit.stat_124859000@T1` | -0.72504 |
| `explicit.stat_3033371881@T2` | -0.70970 |
| `explicit.stat_3032590688@T1` | -0.70736 |
| `explicit.stat_1573130764@T2` | -0.70317 |
| `explicit.stat_3695891184@T1` | -0.67961 |

### weapon.wand — n=9196, R²=-1.8409

intercept: `3.5245`  ·  log_price: True  ·  ilvl: `-0.04398`  ·  n_mods: `-0.01082`  ·  n_top_tier: `0.93274`  ·  corrupted: `0.06026`  ·  n_sockets: `-0.00123`  ·  quality: `0.00951`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.74643 |
| `explicit.stat_4226189338@T1` | 1.46357 |
| `explicit.stat_2254480358@T1` | 1.44516 |
| `explicit.stat_591105508@T1` | 1.37266 |
| `explicit.stat_3962278098@T2` | -1.03479 |
| `explicit.stat_2768835289@T2` | -1.00727 |
| `explicit.stat_737908626@T1` | -0.99760 |
| `explicit.stat_2968503605@T2` | -0.98540 |
| `explicit.stat_473429811@T1` | -0.96634 |
| `explicit.stat_2505884597@T2` | -0.95137 |
| `explicit.stat_737908626@T2` | -0.95027 |
| `explicit.stat_789117908@T2` | -0.94877 |

### weapon.bow — n=7573, R²=-1.7289

intercept: `3.4244`  ·  log_price: True  ·  ilvl: `-0.04240`  ·  n_mods: `-0.01868`  ·  n_top_tier: `0.31240`  ·  corrupted: `-0.04370`  ·  n_sockets: `0.00388`  ·  quality: `0.00499`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.23402 |
| `explicit.stat_2463230181@T1` | 1.91675 |
| `explicit.stat_1202301673@T1` | 1.91319 |
| `crafted.stat_3035140377` | 1.62592 |
| `explicit.stat_518292764@T1` | 1.28953 |
| `explicit.stat_1509134228@T1` | 0.60696 |
| `explicit.stat_55876295@T1` | -0.43271 |
| `explicit.stat_55876295@T2` | -0.39716 |
| `explicit.stat_2694482655@T1` | -0.38179 |
| `explicit.stat_1037193709@T1` | -0.37797 |
| `explicit.stat_3261801346@T1` | -0.37777 |
| `explicit.stat_3336890334@T2` | -0.36326 |

### weapon.crossbow — n=7137, R²=-1.6062

intercept: `3.5349`  ·  log_price: True  ·  ilvl: `-0.04420`  ·  n_mods: `-0.00460`  ·  n_top_tier: `0.37683`  ·  corrupted: `-0.08406`  ·  n_sockets: `0.00391`  ·  quality: `0.00269`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 1.99740 |
| `explicit.stat_1037193709@T1` | 1.88034 |
| `explicit.stat_709508406@T1` | 1.82645 |
| `explicit.stat_1202301673@T1` | 1.79396 |
| `explicit.stat_2250681686@T2` | -1.36384 |
| `crafted.stat_3035140377` | 1.20091 |
| `explicit.stat_2250681686` | 1.02675 |
| `rune.stat_2246411426` | -0.67052 |
| `rune.stat_55876295` | 0.66897 |
| `explicit.stat_691932474@T1` | -0.49925 |
| `explicit.stat_1202301673@T2` | -0.46988 |
| `explicit.stat_669069897@T1` | -0.45709 |

### flask.charm — n=3093, R²=-0.1062

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00004`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1056492907` | 1.60936 |
| `explicit.stat_1873752457@T2` | -0.00001 |
| `explicit.stat_828533480@T1` | -0.00001 |
| `explicit.stat_1873752457@T1` | -0.00001 |
| `explicit.stat_1120862500@T2` | -0.00001 |
| `explicit.stat_388617051@T2` | -0.00001 |
| `explicit.stat_1873752457` | 0.00001 |
| `explicit.stat_828533480@T2` | -0.00001 |
| `explicit.stat_2676834156@T2` | -0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `explicit.stat_3196823591@T2` | -0.00001 |
| `implicit.stat_3676540188` | -0.00000 |

### weapon.warstaff — n=2306, R²=-0.1818

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1509134228` | 0.00003 |
| `rune.stat_1039491398` | -0.00003 |
| `explicit.stat_1509134228@T2` | 0.00002 |
| `rune.stat_1037193709` | 0.00002 |
| `explicit.stat_9187492@T1` | 0.00002 |
| `explicit.stat_709508406@T2` | 0.00001 |
| `desecrated.stat_518292764` | -0.00001 |
| `explicit.stat_3336890334@T2` | -0.00001 |
| `rune.stat_1817052494` | -0.00001 |
| `explicit.stat_3261801346@T1` | 0.00001 |
| `explicit.stat_709508406@T1` | -0.00001 |
| `explicit.stat_518292764@T1` | 0.00001 |

### weapon.sceptre — n=2207, R²=-0.1944

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3984865854` | -0.01787 |
| `desecrated.stat_1050105434` | 0.01512 |
| `explicit.stat_1263695895@T1` | 0.00002 |
| `explicit.stat_101878827@T2` | 0.00002 |
| `explicit.stat_3057012405@T1` | 0.00002 |
| `explicit.stat_2162097452@T1` | 0.00001 |
| `explicit.stat_1998951374@T1` | 0.00001 |
| `explicit.stat_4010677958@T1` | 0.00001 |
| `explicit.stat_2162097452@T2` | 0.00001 |
| `explicit.stat_1998951374@T2` | 0.00001 |
| `explicit.stat_1250712710@T1` | -0.00001 |
| `explicit.stat_4010677958@T2` | 0.00001 |

### weapon.staff — n=2202, R²=-0.1893

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00001`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_3990135792` | -0.13411 |
| `rune.stat_2974417149` | 0.08047 |
| `explicit.stat_473429811@T1` | 0.00004 |
| `explicit.stat_124131830@T1` | 0.00004 |
| `explicit.stat_3291658075@T2` | 0.00003 |
| `explicit.stat_2254480358@T1` | 0.00003 |
| `explicit.stat_2968503605@T2` | 0.00002 |
| `explicit.stat_274716455@T1` | 0.00002 |
| `explicit.stat_591105508@T2` | 0.00002 |
| `explicit.stat_124131830@T2` | 0.00002 |
| `explicit.stat_737908626@T2` | 0.00002 |
| `explicit.stat_1600707273@T2` | 0.00002 |

### weapon.spear — n=1937, R²=-0.1836

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | -0.00004 |
| `explicit.stat_1509134228@T1` | 0.00003 |
| `explicit.stat_1263695895@T2` | -0.00003 |
| `explicit.stat_9187492@T1` | -0.00002 |
| `explicit.stat_210067635@T1` | 0.00001 |
| `explicit.stat_1368271171@T1` | 0.00001 |
| `explicit.stat_518292764@T1` | 0.00001 |
| `explicit.stat_3639275092@T1` | 0.00001 |
| `explicit.stat_2694482655@T2` | 0.00001 |
| `explicit.stat_2694482655@T1` | 0.00001 |
| `explicit.stat_1940865751@T1` | 0.00001 |
| `explicit.stat_1037193709@T1` | 0.00001 |

### armour.focus — n=1621, R²=0.1103

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00004`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.74240 |
| `desecrated.stat_2910761524@T1` | 0.91025 |
| `desecrated.stat_3393628375` | 0.54786 |
| `desecrated.stat_2910761524` | -0.11752 |
| `crafted.stat_4015621042` | 0.06758 |
| `desecrated.stat_4220027924` | 0.00649 |
| `desecrated.stat_737908626` | -0.00295 |
| `explicit.stat_328541901@T2` | -0.00002 |
| `explicit.stat_3291658075@T1` | -0.00001 |
| `explicit.stat_2923486259@T1` | -0.00001 |
| `explicit.stat_2231156303@T1` | -0.00001 |
| `explicit.stat_3639275092@T1` | -0.00001 |

### armour.quiver — n=1559, R²=-0.2107

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00002`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | -0.00007 |
| `explicit.stat_2463230181@T2` | -0.00003 |
| `explicit.stat_681332047@T1` | -0.00001 |
| `explicit.stat_3714003708@T2` | -0.00001 |
| `explicit.stat_3714003708@T1` | -0.00001 |
| `explicit.stat_3695891184@T2` | 0.00001 |
| `explicit.stat_803737631@T2` | -0.00001 |
| `explicit.stat_3695891184@T1` | 0.00001 |
| `explicit.stat_3032590688@T1` | -0.00001 |
| `explicit.stat_3759663284@T1` | 0.00001 |
| `explicit.stat_1573130764@T2` | -0.00001 |
| `explicit.stat_4067062424@T1` | 0.00001 |

### armour.shield — n=1393, R²=-0.2163

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00009`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 0.29486 |
| `explicit.stat_1978899297@T1` | 0.00159 |
| `explicit.stat_1978899297@T2` | -0.00049 |
| `explicit.stat_1978899297` | 0.00039 |
| `explicit.stat_1011760251@T1` | -0.00021 |
| `explicit.stat_1301765461@T2` | -0.00019 |
| `explicit.stat_2339757871@T1` | -0.00014 |
| `explicit.stat_1011760251@T2` | -0.00014 |
| `explicit.stat_3639275092@T1` | -0.00011 |
| `explicit.stat_2901986750@T1` | -0.00010 |
| `explicit.stat_3855016469@T1` | -0.00010 |
| `explicit.stat_3372524247@T2` | -0.00010 |

### weapon.twomace — n=1177, R²=-0.2379

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | 0.00004 |
| `explicit.stat_1509134228@T1` | 0.00003 |
| `explicit.stat_821021828@T2` | -0.00002 |
| `explicit.stat_518292764@T1` | 0.00002 |
| `explicit.stat_821021828@T1` | -0.00002 |
| `explicit.stat_1263695895@T2` | 0.00002 |
| `explicit.stat_3336890334@T2` | 0.00002 |
| `explicit.stat_387439868@T1` | 0.00002 |
| `explicit.stat_791928121@T1` | 0.00001 |
| `explicit.stat_709508406@T2` | 0.00001 |
| `explicit.stat_1368271171@T2` | 0.00001 |
| `explicit.stat_791928121@T2` | 0.00001 |

## Coverage (listings per base)

- … **Emerald** — 8241 listings (8241 priced) [0.7–42426.8 ex]
- … **Sapphire** — 8221 listings (8220 priced) [0.6–7379.9 ex]
- … **Ruby** — 6399 listings (6399 priced) [0.3–28868.8 ex]
- … **Utility Belt** — 4413 listings (4411 priced) [0.3–4555741.7 ex]
- … **Stellar Amulet** — 3318 listings (3318 priced) [0.3–4547453.5 ex]
- … **Prismatic Ring** — 3112 listings (3111 priced) [0.3–36899.4 ex]
- … **Solar Amulet** — 3034 listings (3034 priced) [0.3–4547453.5 ex]
- … **Gold Amulet** — 2973 listings (2973 priced) [0.7–292542.5 ex]
- … **Amethyst Ring** — 2957 listings (2956 priced) [0.3–71450.3 ex]
- … **Gold Ring** — 2847 listings (2846 priced) [0.3–10825.8 ex]
- … **Dueling Wand** — 2845 listings (2843 priced) [1.0–4599254.4 ex]
- … **Sapphire Ring** — 2376 listings (2376 priced) [0.6–10825.8 ex]
- … **Topaz Ring** — 2335 listings (2335 priced) [1.0–10825.8 ex]
- … **Ruby Ring** — 2266 listings (2266 priced) [0.6–44279.2 ex]
- … **Plate Belt** — 2207 listings (2207 priced) [0.3–4547453.5 ex]
- … **Obliterator Bow** — 2169 listings (2166 priced) [0.3–22139622146.9 ex]
- … **Heavy Belt** — 2094 listings (2094 priced) [0.3–3637.8 ex]
- … **Lapis Amulet** — 2073 listings (2073 priced) [0.6–4547453.5 ex]
- … **Amber Amulet** — 2030 listings (2030 priced) [0.6–4547453.5 ex]
- … **Jade Amulet** — 2028 listings (2028 priced) [0.3–4547453.5 ex]
- … **Ancestral Tiara** — 1997 listings (1995 priced) [0.3–365678.1 ex]
- … **Unset Ring** — 1891 listings (1891 priced) [0.3–5093.0 ex]
- … **Bloodstone Amulet** — 1857 listings (1857 priced) [1.0–7275.7 ex]
- … **Pearl Ring** — 1827 listings (1827 priced) [0.3–7176.6 ex]
- … **Azure Amulet** — 1811 listings (1811 priced) [1.0–28284.5 ex]

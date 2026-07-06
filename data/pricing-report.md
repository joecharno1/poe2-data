# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-06T07:15:06+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **209289** (209192 priced in exalted)
- Distinct bases: 929 · distinct mods: 2565 · mod rows: 992122
- Sold signals: **36961** sold · 109802 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-06T07:08:14+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×14.82** (median |log error| 2.6958)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.02** (> 0 = the mods carry signal)
- Calibration: 76% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.04** · typical error ×36.48 · ±30% 13% · n=30107
- Premium segment (60ex+): skill **+0.06** · typical error ×170.87 · ±30% 0% · n=17875
- Sold listings (clearing prices): skill **+0.34** · typical error ×6.65 · ±30% 0% · n=10

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 3908 | ×32.15 | 14% | +0.01 | -0.00 |
| accessory.amulet | 3732 | ×43.30 | 20% | +0.01 | +0.01 |
| jewel | 3300 | ×8.62 | 7% | +0.04 | +0.07 |
| accessory.belt | 3225 | ×10.00 | 22% | +0.02 | +0.00 |
| armour.chest | 3139 | ×10.00 | 29% | -0.00 | +0.01 |
| armour.helmet | 3046 | ×10.00 | 27% | -0.00 | +0.01 |
| armour.boots | 2861 | ×9.61 | 6% | -0.00 | +0.02 |
| armour.gloves | 2848 | ×14.02 | 5% | -0.01 | +0.03 |
| other | 2677 | ×9.94 | 38% | +0.05 | +0.15 |
| weapon.wand | 2028 | ×10.41 | 29% | +0.04 | +0.06 |
| weapon.bow | 1651 | ×10.07 | 24% | +0.06 | +0.07 |
| weapon.crossbow | 1566 | ×10.25 | 27% | +0.07 | +0.09 |
| weapon.warstaff | 477 | ×46.00 | 20% | +0.00 | +0.00 |
| weapon.sceptre | 454 | ×50.00 | 14% | +0.00 | +0.00 |
| weapon.staff | 453 | ×30.00 | 24% | +0.00 | +0.00 |
| weapon.spear | 429 | ×50.00 | 16% | -0.00 | +0.00 |
| armour.focus | 359 | ×30.00 | 19% | +0.21 | +0.00 |
| armour.quiver | 285 | ×49.00 | 14% | +0.00 | +0.00 |
| armour.shield | 275 | ×40.00 | 15% | +0.00 | +0.00 |
| weapon.twomace | 245 | ×50.00 | 17% | +0.00 | +0.00 |
| flask.charm | 226 | ×5.00 | 42% | -0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=24134, R²=-0.504

intercept: `1.6082`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `0.01536`  ·  n_top_tier: `0.34327`  ·  corrupted: `2.63349`  ·  n_sockets: `-0.00006`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_2891184298@T1` | 1.80414 |
| `explicit.stat_1589917703@T1` | -1.10836 |
| `explicit.stat_2974417149@T1` | 0.88773 |
| `explicit.stat_3291658075@T1` | 0.85189 |
| `explicit.stat_2106365538@T1` | 0.76049 |
| `explicit.stat_3917489142@T1` | 0.62899 |
| `explicit.stat_1050105434@T1` | -0.48900 |
| `explicit.stat_3141070085@T1` | 0.46249 |
| `explicit.stat_1589917703` | 0.35393 |
| `explicit.stat_2968503605@T1` | 0.33564 |
| `implicit.stat_1379411836` | -0.27073 |
| `implicit.stat_4041853756` | 0.22872 |

### accessory.ring — n=17848, R²=-2.1285

intercept: `5.0768`  ·  log_price: True  ·  ilvl: `-0.05909`  ·  n_mods: `-0.04510`  ·  n_top_tier: `-0.20767`  ·  corrupted: `0.69802`  ·  n_sockets: `3.72336`  ·  quality: `0.11944`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T2` | 2.04171 |
| `explicit.stat_1754445556@T1` | 1.88824 |
| `explicit.stat_3032590688@T2` | 1.61696 |
| `explicit.stat_2557965901@T1` | 0.74699 |
| `explicit.stat_2557965901@T2` | 0.63970 |
| `explicit.stat_1379411836@T1` | -0.60871 |
| `explicit.stat_736967255@T1` | 0.45544 |
| `explicit.stat_1263695895@T1` | 0.42930 |
| `implicit.stat_2748665614` | 0.40940 |
| `explicit.stat_2923486259@T2` | 0.38408 |
| `explicit.stat_4080418644@T2` | 0.34952 |
| `explicit.stat_2901986750@T1` | 0.34714 |

### accessory.amulet — n=17155, R²=-2.1964

intercept: `3.9429`  ·  log_price: True  ·  ilvl: `-0.04806`  ·  n_mods: `-0.02402`  ·  n_top_tier: `0.26014`  ·  corrupted: `0.08472`  ·  n_sockets: `-0.02609`  ·  quality: `-0.01406`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -3.56983 |
| `explicit.stat_983749596@T2` | -2.65767 |
| `explicit.stat_3981240776@T2` | 1.50857 |
| `explicit.stat_124131830@T2` | 0.72511 |
| `explicit.stat_1202301673` | 0.64638 |
| `explicit.stat_1202301673@T2` | 0.62328 |
| `explicit.stat_124131830` | 0.60607 |
| `explicit.stat_3299347043@T1` | -0.48715 |
| `explicit.stat_983749596` | 0.47048 |
| `explicit.stat_2748665614@T1` | -0.44945 |
| `explicit.stat_2748665614@T2` | -0.38684 |
| `explicit.stat_3299347043@T2` | -0.38393 |

### jewel — n=17100, R²=-0.7251

intercept: `-1.2406`  ·  log_price: True  ·  ilvl: `0.03601`  ·  n_mods: `0.23676`  ·  n_top_tier: `-0.34390`  ·  corrupted: `0.56844`  ·  quality: `0.20727`

| stat_id | coef |
|---|---|
| `explicit.stat_3714003708@T1` | -3.48033 |
| `explicit.stat_3824372849@T1` | 3.28544 |
| `explicit.stat_1316278494@T1` | -2.96757 |
| `explicit.stat_2456523742@T1` | 2.88320 |
| `explicit.stat_1869147066@T1` | 2.69939 |
| `explicit.stat_153777645@T1` | 2.67626 |
| `explicit.stat_1569101201@T1` | 2.49524 |
| `explicit.stat_293638271@T1` | 2.11478 |
| `explicit.stat_2106365538@T1` | -2.11342 |
| `explicit.stat_1697951953@T1` | -2.03408 |
| `explicit.stat_3780644166@T1` | 1.99566 |
| `explicit.stat_416040624@T1` | -1.95566 |

### accessory.belt — n=14666, R²=-0.0831

intercept: `2.3029`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.03710`  ·  corrupted: `0.00005`  ·  n_sockets: `-0.00037`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.53124 |
| `explicit.stat_2639966148` | 0.12245 |
| `pseudo.total_ele_res>=80` | 0.06891 |
| `explicit.stat_174664100` | 0.04467 |
| `explicit.stat_3811191316` | 0.04115 |
| `explicit.stat_770672621` | 0.03949 |
| `explicit.stat_1389754388@T1` | -0.03716 |
| `explicit.stat_644456512@T2` | -0.03713 |
| `explicit.stat_644456512@T1` | -0.03713 |
| `explicit.stat_51994685@T1` | -0.03713 |
| `explicit.stat_915769802@T2` | -0.03713 |
| `explicit.stat_915769802@T1` | -0.03712 |

### armour.chest — n=14457, R²=-0.2505

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.00244`  ·  corrupted: `0.00009`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_1978899297` | -0.41018 |
| `implicit.stat_2923486259` | -0.02747 |
| `pseudo.total_chaos_res` | 0.02747 |
| `explicit.stat_2923486259` | -0.02747 |
| `desecrated.stat_3981240776` | 0.00270 |
| `explicit.stat_3261801346@T1` | -0.00249 |
| `explicit.stat_915769802@T1` | -0.00247 |
| `explicit.stat_4080418644@T2` | -0.00247 |
| `explicit.stat_3033371881@T2` | -0.00247 |
| `explicit.stat_4080418644@T1` | -0.00247 |
| `explicit.stat_915769802@T2` | -0.00246 |
| `explicit.stat_3325883026@T1` | -0.00246 |

### armour.helmet — n=14163, R²=-0.2589

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00285`  ·  corrupted: `0.00202`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3917489142` | 0.04555 |
| `rune.stat_3523867985` | 0.00728 |
| `explicit.stat_1062208444@T2` | -0.00307 |
| `explicit.stat_4080418644@T2` | -0.00291 |
| `explicit.stat_53045048@T2` | -0.00287 |
| `explicit.stat_3321629045@T1` | -0.00287 |
| `explicit.stat_803737631@T2` | -0.00287 |
| `explicit.stat_3033371881@T1` | -0.00287 |
| `explicit.stat_3325883026@T2` | -0.00286 |
| `explicit.stat_328541901@T2` | -0.00286 |
| `explicit.stat_53045048@T1` | -0.00286 |
| `explicit.stat_1999113824@T1` | -0.00286 |

### armour.boots — n=13311, R²=-0.5464

intercept: `4.1970`  ·  log_price: True  ·  ilvl: `-0.04407`  ·  n_mods: `-0.20339`  ·  n_top_tier: `0.47745`  ·  corrupted: `0.47243`  ·  n_sockets: `0.16645`  ·  quality: `0.01269`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.81014 |
| `rune.stat_836936635` | -2.15718 |
| `explicit.stat_1062208444@T2` | -1.28567 |
| `explicit.stat_3362812763@T1` | -1.20048 |
| `desecrated.stat_2250533757@T2` | -1.00285 |
| `explicit.stat_328541901@T1` | -0.98345 |
| `explicit.stat_2250533757@T1` | 0.96484 |
| `explicit.stat_2923486259@T2` | -0.95317 |
| `explicit.stat_3917489142@T2` | -0.94150 |
| `explicit.stat_4080418644@T1` | -0.79977 |
| `explicit.stat_1062208444@T1` | -0.78702 |
| `explicit.stat_3033371881@T2` | -0.77944 |

### armour.gloves — n=13125, R²=-0.7533

intercept: `3.1139`  ·  log_price: True  ·  ilvl: `-0.04221`  ·  n_mods: `-0.03028`  ·  n_top_tier: `0.68542`  ·  corrupted: `0.43835`  ·  n_sockets: `0.15372`  ·  quality: `0.00179`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.84834 |
| `explicit.stat_2797971005@T1` | -1.51982 |
| `explicit.stat_124859000@T1` | -1.49942 |
| `explicit.stat_681332047@T2` | -1.47929 |
| `explicit.stat_2797971005@T2` | -1.32549 |
| `explicit.stat_803737631@T2` | -1.28751 |
| `explicit.stat_3032590688@T1` | -1.14216 |
| `explicit.stat_1573130764@T1` | -1.10760 |
| `explicit.stat_1754445556@T1` | -1.02622 |
| `explicit.stat_1573130764@T2` | -0.97411 |
| `explicit.stat_3321629045@T2` | -0.95983 |
| `explicit.stat_2557965901@T1` | -0.95774 |

### weapon.wand — n=9315, R²=-1.9086

intercept: `3.4554`  ·  log_price: True  ·  ilvl: `-0.04311`  ·  n_mods: `-0.01255`  ·  n_top_tier: `0.79528`  ·  corrupted: `0.01211`  ·  n_sockets: `0.00084`  ·  quality: `0.00461`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.11942 |
| `explicit.stat_4226189338@T1` | 1.58776 |
| `explicit.stat_2254480358@T1` | 1.58014 |
| `explicit.stat_591105508@T1` | 1.50686 |
| `explicit.stat_2768835289@T2` | -0.91583 |
| `explicit.stat_3962278098@T2` | -0.85848 |
| `explicit.stat_2968503605@T2` | -0.85689 |
| `explicit.stat_737908626@T1` | -0.85623 |
| `explicit.stat_473429811@T1` | -0.82357 |
| `explicit.stat_737908626@T2` | -0.82302 |
| `explicit.stat_293638271@T2` | -0.82288 |
| `explicit.stat_1050105434@T1` | -0.81271 |

### weapon.bow — n=7692, R²=-1.7636

intercept: `3.4707`  ·  log_price: True  ·  ilvl: `-0.04291`  ·  n_mods: `-0.01822`  ·  n_top_tier: `0.32052`  ·  corrupted: `-0.03816`  ·  n_sockets: `0.00149`  ·  quality: `0.00409`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.41394 |
| `explicit.stat_1202301673@T1` | 1.92476 |
| `explicit.stat_2463230181@T1` | 1.91413 |
| `crafted.stat_3035140377` | 1.66462 |
| `explicit.stat_518292764@T1` | 1.10132 |
| `explicit.stat_55876295@T1` | -0.42065 |
| `explicit.stat_55876295@T2` | -0.39452 |
| `explicit.stat_2694482655@T1` | -0.38684 |
| `explicit.stat_1037193709@T1` | -0.37533 |
| `explicit.stat_3261801346@T1` | -0.36433 |
| `explicit.stat_3336890334@T2` | -0.36342 |
| `explicit.stat_821021828@T2` | -0.35986 |

### weapon.crossbow — n=7278, R²=-1.6737

intercept: `3.4653`  ·  log_price: True  ·  ilvl: `-0.04330`  ·  n_mods: `-0.00237`  ·  n_top_tier: `0.17700`  ·  corrupted: `-0.06408`  ·  n_sockets: `-0.00026`  ·  quality: `0.00317`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 2.11983 |
| `explicit.stat_1037193709@T1` | 2.10806 |
| `explicit.stat_709508406@T1` | 2.04712 |
| `explicit.stat_1202301673@T1` | 2.03330 |
| `crafted.stat_3035140377` | 1.28182 |
| `explicit.stat_2250681686@T2` | -1.24756 |
| `explicit.stat_2250681686` | 1.11669 |
| `rune.stat_2246411426` | -0.58775 |
| `rune.stat_55876295` | 0.58067 |
| `rune.stat_669069897` | -0.43336 |
| `rune.stat_1586906534` | 0.35622 |
| `explicit.stat_691932474@T1` | -0.24174 |

### flask.charm — n=3219, R²=-0.1263

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00004`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1056492907` | 1.60971 |
| `explicit.stat_1873752457@T2` | -0.00001 |
| `explicit.stat_1120862500@T2` | -0.00001 |
| `explicit.stat_1873752457@T1` | -0.00001 |
| `explicit.stat_828533480@T2` | -0.00001 |
| `explicit.stat_1873752457` | -0.00001 |
| `explicit.stat_828533480@T1` | -0.00001 |
| `explicit.stat_2365392475@T2` | 0.00001 |
| `explicit.stat_388617051@T2` | -0.00001 |
| `explicit.stat_3246948616` | 0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `implicit.stat_3310778564` | -0.00001 |

### weapon.warstaff — n=2379, R²=-0.1997

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1037193709` | 0.25641 |
| `rune.stat_3336890334` | 0.23589 |
| `rune.stat_2430860292` | -0.12188 |
| `rune.stat_1817052494` | -0.10256 |
| `rune.stat_1509134228` | 0.00352 |
| `rune.stat_1039491398` | -0.00317 |
| `rune.stat_2077615515` | 0.00042 |
| `crafted.stat_210067635@T2` | -0.00007 |
| `explicit.stat_1509134228@T2` | 0.00002 |
| `explicit.stat_9187492@T1` | 0.00002 |
| `explicit.stat_709508406@T2` | 0.00001 |
| `explicit.stat_3336890334@T2` | -0.00001 |

### weapon.sceptre — n=2268, R²=-0.2144

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1050105434` | 0.01354 |
| `desecrated.stat_3984865854` | -0.00951 |
| `explicit.stat_2162097452@T1` | 0.00002 |
| `explicit.stat_1263695895@T1` | 0.00002 |
| `explicit.stat_1250712710@T1` | -0.00002 |
| `explicit.stat_3057012405@T1` | 0.00002 |
| `explicit.stat_101878827@T2` | 0.00001 |
| `explicit.stat_4010677958@T1` | 0.00001 |
| `explicit.stat_2347036682@T2` | -0.00001 |
| `explicit.stat_1998951374@T1` | 0.00001 |
| `explicit.stat_3984865854@T2` | -0.00001 |
| `explicit.stat_2162097452@T2` | 0.00001 |

### weapon.staff — n=2265, R²=-0.2065

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00001`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_3990135792` | -0.13412 |
| `rune.stat_2974417149` | 0.08047 |
| `explicit.stat_124131830@T1` | 0.00004 |
| `explicit.stat_473429811@T1` | 0.00004 |
| `explicit.stat_3291658075@T2` | 0.00003 |
| `explicit.stat_2254480358@T1` | 0.00003 |
| `explicit.stat_124131830@T2` | 0.00002 |
| `explicit.stat_2968503605@T2` | 0.00002 |
| `explicit.stat_274716455@T1` | 0.00002 |
| `explicit.stat_591105508@T2` | 0.00002 |
| `explicit.stat_1600707273@T2` | 0.00002 |
| `explicit.stat_737908626@T2` | 0.00002 |

### weapon.spear — n=2004, R²=-0.2145

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | -0.00004 |
| `explicit.stat_1263695895@T2` | -0.00003 |
| `explicit.stat_1509134228@T1` | 0.00003 |
| `explicit.stat_210067635@T1` | 0.00002 |
| `explicit.stat_2694482655@T1` | 0.00002 |
| `explicit.stat_1037193709@T1` | 0.00002 |
| `explicit.stat_3639275092@T1` | 0.00002 |
| `explicit.stat_518292764@T1` | 0.00002 |
| `explicit.stat_748522257@T2` | 0.00001 |
| `explicit.stat_1368271171@T1` | 0.00001 |
| `explicit.stat_518292764@T2` | 0.00001 |
| `explicit.stat_2694482655@T2` | 0.00001 |

### armour.focus — n=1669, R²=0.0623

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `-0.00004`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.75606 |
| `desecrated.stat_2910761524@T1` | 0.91794 |
| `desecrated.stat_3393628375` | 0.54935 |
| `desecrated.stat_2910761524` | -0.11726 |
| `crafted.stat_4015621042` | 0.06745 |
| `desecrated.stat_4220027924` | 0.00482 |
| `desecrated.stat_737908626` | -0.00174 |
| `explicit.stat_328541901@T2` | -0.00003 |
| `explicit.stat_3291658075@T1` | -0.00002 |
| `explicit.stat_4220027924@T1` | -0.00002 |
| `explicit.stat_2923486259@T1` | -0.00002 |
| `explicit.stat_2231156303@T1` | -0.00002 |

### armour.quiver — n=1585, R²=-0.2249

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00003`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | -0.00006 |
| `explicit.stat_2463230181@T2` | -0.00002 |
| `explicit.stat_681332047@T1` | -0.00002 |
| `explicit.stat_3714003708@T2` | -0.00001 |
| `explicit.stat_3714003708@T1` | -0.00001 |
| `explicit.stat_3695891184@T1` | 0.00001 |
| `explicit.stat_681332047@T2` | -0.00001 |
| `explicit.stat_3695891184@T2` | 0.00001 |
| `explicit.stat_3759663284@T1` | 0.00001 |
| `explicit.stat_4067062424@T1` | 0.00001 |
| `explicit.stat_803737631@T2` | -0.00001 |
| `explicit.stat_1368271171@T2` | -0.00001 |

### armour.shield — n=1431, R²=-0.2303

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00007`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 0.29498 |
| `explicit.stat_1978899297@T1` | 0.00111 |
| `explicit.stat_1978899297@T2` | -0.00034 |
| `explicit.stat_1978899297` | 0.00026 |
| `explicit.stat_1011760251@T1` | -0.00018 |
| `explicit.stat_1301765461@T2` | -0.00016 |
| `explicit.stat_2339757871@T1` | -0.00013 |
| `explicit.stat_1011760251@T2` | -0.00011 |
| `explicit.stat_2901986750@T1` | -0.00008 |
| `explicit.stat_3484657501@T1` | -0.00008 |
| `explicit.stat_3639275092@T1` | -0.00008 |
| `explicit.stat_3855016469@T1` | -0.00008 |

### weapon.twomace — n=1224, R²=-0.2703

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | -0.00004 |
| `explicit.stat_3336890334@T1` | -0.00004 |
| `explicit.stat_669069897@T1` | -0.00004 |
| `explicit.stat_821021828@T2` | -0.00004 |
| `explicit.stat_821021828@T1` | -0.00003 |
| `explicit.stat_669069897@T2` | -0.00003 |
| `explicit.stat_1037193709@T2` | -0.00003 |
| `explicit.stat_1940865751@T1` | -0.00003 |
| `explicit.stat_387439868@T2` | -0.00002 |
| `explicit.stat_55876295@T2` | -0.00002 |
| `explicit.stat_1263695895@T2` | -0.00002 |
| `explicit.stat_1368271171@T1` | -0.00002 |

## Coverage (listings per base)

- … **Emerald** — 8400 listings (8400 priced) [0.7–4745587.6 ex]
- … **Sapphire** — 8397 listings (8396 priced) [0.6–4745587.6 ex]
- … **Ruby** — 6524 listings (6524 priced) [0.3–28868.8 ex]
- … **Utility Belt** — 4475 listings (4473 priced) [0.3–4555741.7 ex]
- … **Stellar Amulet** — 3364 listings (3364 priced) [0.3–4547453.5 ex]
- … **Prismatic Ring** — 3162 listings (3161 priced) [0.3–36899.4 ex]
- … **Solar Amulet** — 3087 listings (3087 priced) [0.4–4547453.5 ex]
- … **Gold Amulet** — 3018 listings (3018 priced) [0.7–292542.5 ex]
- … **Amethyst Ring** — 3002 listings (3001 priced) [0.4–71450.3 ex]
- … **Gold Ring** — 2892 listings (2891 priced) [0.4–10825.8 ex]
- … **Dueling Wand** — 2877 listings (2875 priced) [1.0–4599254.4 ex]
- … **Sapphire Ring** — 2410 listings (2410 priced) [0.7–10825.8 ex]
- … **Topaz Ring** — 2369 listings (2369 priced) [1.0–44572.1 ex]
- … **Ruby Ring** — 2313 listings (2313 priced) [0.7–44279.2 ex]
- … **Plate Belt** — 2240 listings (2240 priced) [0.4–4547453.5 ex]
- … **Obliterator Bow** — 2207 listings (2204 priced) [0.3–22139622146.9 ex]
- … **Heavy Belt** — 2114 listings (2114 priced) [0.4–3714.3 ex]
- … **Lapis Amulet** — 2100 listings (2100 priced) [0.4–4547453.5 ex]
- … **Amber Amulet** — 2068 listings (2068 priced) [0.7–4547453.5 ex]
- … **Jade Amulet** — 2055 listings (2055 priced) [0.4–4547453.5 ex]
- … **Ancestral Tiara** — 2024 listings (2022 priced) [0.4–594295.2 ex]
- … **Unset Ring** — 1936 listings (1936 priced) [0.4–5093.0 ex]
- … **Bloodstone Amulet** — 1887 listings (1887 priced) [1.0–7275.7 ex]
- … **Pearl Ring** — 1858 listings (1858 priced) [0.4–7176.6 ex]
- … **Azure Amulet** — 1852 listings (1852 priced) [1.0–29714.8 ex]

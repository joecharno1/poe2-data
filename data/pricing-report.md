# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-06T10:35:32+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **216915** (216803 priced in exalted)
- Distinct bases: 931 · distinct mods: 2600 · mod rows: 1029065
- Sold signals: **36243** sold · 113048 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-06T10:29:20+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×15.44** (median |log error| 2.7372)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.02** (> 0 = the mods carry signal)
- Calibration: 76% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.07** · typical error ×41.39 · ±30% 14% · n=31342
- Premium segment (60ex+): skill **+0.08** · typical error ×158.36 · ±30% 0% · n=18907
- Sold listings (clearing prices): skill **+0.34** · typical error ×6.52 · ±30% 0% · n=10

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 4050 | ×36.70 | 15% | +0.03 | +0.04 |
| accessory.amulet | 3884 | ×49.14 | 19% | +0.01 | +0.02 |
| jewel | 3497 | ×8.80 | 7% | +0.04 | +0.08 |
| accessory.belt | 3317 | ×10.00 | 23% | +0.03 | +0.01 |
| armour.chest | 3267 | ×10.00 | 22% | +0.00 | +0.02 |
| armour.helmet | 3115 | ×10.00 | 23% | +0.00 | -0.01 |
| armour.boots | 2955 | ×9.86 | 24% | -0.00 | +0.03 |
| armour.gloves | 2937 | ×12.06 | 8% | -0.00 | +0.01 |
| other | 2805 | ×9.97 | 37% | +0.07 | +0.01 |
| weapon.wand | 2078 | ×12.98 | 26% | +0.05 | +0.08 |
| weapon.bow | 1690 | ×10.31 | 25% | +0.07 | +0.06 |
| weapon.crossbow | 1610 | ×10.84 | 22% | +0.08 | +0.09 |
| weapon.staff | 515 | ×30.00 | 21% | +0.00 | +0.00 |
| weapon.warstaff | 481 | ×25.00 | 21% | +0.00 | +0.00 |
| weapon.sceptre | 459 | ×63.00 | 14% | +0.00 | +0.00 |
| weapon.spear | 411 | ×30.00 | 18% | +0.00 | +0.00 |
| armour.focus | 376 | ×51.00 | 15% | +0.02 | +0.02 |
| armour.quiver | 366 | ×50.00 | 12% | +0.00 | +0.00 |
| armour.shield | 332 | ×46.00 | 13% | +0.00 | +0.00 |
| weapon.twomace | 270 | ×42.21 | 17% | +0.00 | +0.00 |
| flask.charm | 259 | ×20.00 | 42% | -0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=24710, R²=-0.4753

intercept: `1.6078`  ·  log_price: True  ·  ilvl: `0.00003`  ·  n_mods: `0.02810`  ·  n_top_tier: `0.42396`  ·  corrupted: `3.69275`  ·  n_sockets: `-0.00015`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_1589917703@T1` | 3.77638 |
| `explicit.stat_2106365538@T1` | 3.75631 |
| `explicit.stat_101878827@T1` | 2.84496 |
| `explicit.stat_3291658075@T1` | 2.63119 |
| `explicit.stat_2891184298@T1` | 2.00538 |
| `explicit.stat_2974417149@T1` | 0.81149 |
| `explicit.stat_3917489142@T1` | 0.77126 |
| `explicit.stat_1050105434@T1` | -0.68212 |
| `explicit.stat_789117908@T1` | -0.29751 |
| `implicit.stat_1379411836` | -0.27290 |
| `explicit.stat_2968503605@T1` | 0.24543 |
| `explicit.stat_3141070085@T1` | 0.24064 |

### accessory.ring — n=18500, R²=-2.1051

intercept: `5.2445`  ·  log_price: True  ·  ilvl: `-0.06183`  ·  n_mods: `-0.03113`  ·  n_top_tier: `-0.24765`  ·  corrupted: `0.77902`  ·  n_sockets: `3.66305`  ·  quality: `0.11921`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T2` | 1.66491 |
| `explicit.stat_2557965901@T1` | 0.93699 |
| `explicit.stat_2557965901@T2` | 0.82209 |
| `explicit.stat_1379411836@T1` | -0.76010 |
| `explicit.stat_1263695895@T1` | 0.70726 |
| `explicit.stat_3372524247@T1` | 0.66755 |
| `explicit.stat_1754445556@T1` | 0.60499 |
| `explicit.stat_707457662@T1` | 0.49597 |
| `explicit.stat_2923486259@T2` | 0.47354 |
| `explicit.stat_3032590688@T2` | 0.46041 |
| `explicit.stat_1379411836@T2` | -0.44467 |
| `explicit.stat_3032590688@T1` | 0.40523 |

### jewel — n=17897, R²=-0.6968

intercept: `-1.2485`  ·  log_price: True  ·  ilvl: `0.03729`  ·  n_mods: `0.22127`  ·  n_top_tier: `-0.25732`  ·  corrupted: `0.23811`  ·  quality: `0.21984`

| stat_id | coef |
|---|---|
| `explicit.stat_3714003708@T1` | -3.40700 |
| `explicit.stat_3824372849@T1` | 2.93821 |
| `explicit.stat_1869147066@T1` | 2.74617 |
| `explicit.stat_1697951953@T1` | -2.74468 |
| `explicit.stat_1316278494@T1` | -2.63893 |
| `explicit.stat_3780644166@T1` | 2.46046 |
| `explicit.stat_2118708619@T1` | -2.31842 |
| `explicit.stat_2456523742@T1` | 2.28002 |
| `explicit.stat_293638271@T1` | 2.26059 |
| `explicit.stat_2106365538@T1` | -2.22086 |
| `explicit.stat_2594634307@T1` | 2.20583 |
| `explicit.stat_153777645@T1` | 2.08569 |

### accessory.amulet — n=17768, R²=-2.1714

intercept: `3.9568`  ·  log_price: True  ·  ilvl: `-0.04815`  ·  n_mods: `-0.02382`  ·  n_top_tier: `0.13234`  ·  corrupted: `0.09031`  ·  n_sockets: `0.10432`  ·  quality: `-0.01123`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -2.55298 |
| `explicit.stat_983749596@T2` | -1.92447 |
| `explicit.stat_3981240776@T2` | 1.28847 |
| `explicit.stat_124131830` | 0.77886 |
| `explicit.stat_1202301673` | 0.70488 |
| `explicit.stat_124131830@T2` | 0.55869 |
| `explicit.stat_3299347043@T1` | -0.45534 |
| `explicit.stat_3556824919@T1` | 0.41893 |
| `explicit.stat_983749596` | 0.34918 |
| `explicit.stat_3372524247@T1` | 0.30673 |
| `explicit.stat_3299347043@T2` | -0.29311 |
| `explicit.stat_1202301673@T2` | 0.28312 |

### accessory.belt — n=15139, R²=-0.0837

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.04928`  ·  corrupted: `0.00003`  ·  n_sockets: `-0.00001`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.45762 |
| `explicit.stat_2639966148` | 0.12655 |
| `pseudo.total_ele_res>=80` | 0.06900 |
| `explicit.stat_174664100` | 0.05028 |
| `explicit.stat_1389754388@T1` | -0.04931 |
| `explicit.stat_51994685@T1` | -0.04930 |
| `explicit.stat_644456512@T2` | -0.04929 |
| `explicit.stat_1389754388@T2` | -0.04929 |
| `explicit.stat_644456512@T1` | -0.04929 |
| `explicit.stat_915769802@T2` | -0.04929 |
| `explicit.stat_1570770415@T1` | -0.04929 |
| `explicit.stat_3325883026@T1` | -0.04929 |

### armour.chest — n=14948, R²=-0.2071

intercept: `2.3031`  ·  log_price: True  ·  ilvl: `-0.00001`  ·  n_mods: `-0.00007`  ·  n_top_tier: `0.18542`  ·  corrupted: `0.00049`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_1978899297` | -0.69347 |
| `explicit.stat_3261801346@T1` | -0.18554 |
| `explicit.stat_4080418644@T2` | -0.18553 |
| `explicit.stat_915769802@T1` | -0.18550 |
| `explicit.stat_915769802@T2` | -0.18549 |
| `explicit.stat_3325883026@T1` | -0.18548 |
| `explicit.stat_3261801346@T2` | -0.18546 |
| `explicit.stat_4080418644@T1` | -0.18546 |
| `explicit.stat_3033371881@T2` | -0.18546 |
| `explicit.stat_124859000@T2` | -0.18545 |
| `explicit.stat_3484657501@T1` | -0.18545 |
| `explicit.stat_4015621042@T1` | -0.18545 |

### armour.helmet — n=14627, R²=-0.2393

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.03580`  ·  corrupted: `0.18844`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_3523867985` | 0.04796 |
| `desecrated.stat_3917489142` | 0.04672 |
| `explicit.stat_1062208444@T2` | -0.03742 |
| `explicit.stat_4080418644@T2` | -0.03710 |
| `explicit.stat_803737631@T2` | -0.03583 |
| `explicit.stat_53045048@T2` | -0.03582 |
| `explicit.stat_3362812763@T1` | -0.03582 |
| `explicit.stat_3321629045@T1` | -0.03582 |
| `explicit.stat_3033371881@T1` | -0.03582 |
| `explicit.stat_3325883026@T2` | -0.03581 |
| `explicit.stat_328541901@T2` | -0.03581 |
| `explicit.stat_3362812763@T2` | -0.03581 |

### armour.boots — n=13740, R²=-0.2471

intercept: `2.4444`  ·  log_price: True  ·  ilvl: `-0.00297`  ·  n_mods: `-0.01961`  ·  n_top_tier: `0.14425`  ·  corrupted: `0.04016`  ·  n_sockets: `0.00604`  ·  quality: `0.00112`

| stat_id | coef |
|---|---|
| `explicit.stat_4080418644@T1` | -0.72987 |
| `desecrated.stat_2250533757@T2` | -0.41519 |
| `explicit.stat_1062208444@T2` | -0.33266 |
| `explicit.stat_2339757871@T1` | -0.31058 |
| `explicit.stat_3362812763@T1` | -0.19237 |
| `explicit.stat_3261801346@T2` | -0.18720 |
| `explicit.stat_1062208444@T1` | -0.18523 |
| `explicit.stat_3917489142@T2` | -0.17089 |
| `explicit.stat_328541901@T1` | -0.16947 |
| `explicit.stat_2451402625@T2` | -0.16873 |
| `explicit.stat_2923486259@T2` | -0.16767 |
| `explicit.stat_3033371881@T2` | -0.16596 |

### armour.gloves — n=13542, R²=-0.3686

intercept: `2.6750`  ·  log_price: True  ·  ilvl: `-0.01743`  ·  n_mods: `-0.04485`  ·  n_top_tier: `0.34295`  ·  corrupted: `0.25755`  ·  n_sockets: `0.05349`  ·  quality: `0.00396`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -0.96779 |
| `explicit.stat_3484657501@T2` | -0.73990 |
| `explicit.stat_681332047@T2` | -0.71111 |
| `explicit.stat_803737631@T2` | -0.70030 |
| `explicit.stat_2797971005@T1` | -0.63579 |
| `explicit.stat_2797971005@T2` | -0.63355 |
| `explicit.stat_1573130764@T1` | -0.57130 |
| `explicit.stat_3695891184@T1` | -0.48317 |
| `explicit.stat_4015621042@T1` | -0.47597 |
| `explicit.stat_2557965901@T1` | -0.45731 |
| `explicit.stat_3032590688@T1` | -0.45545 |
| `explicit.stat_328541901@T1` | -0.45034 |

### weapon.wand — n=9601, R²=-1.8959

intercept: `3.6100`  ·  log_price: True  ·  ilvl: `-0.04512`  ·  n_mods: `-0.00979`  ·  n_top_tier: `0.85616`  ·  corrupted: `0.00120`  ·  n_sockets: `0.00452`  ·  quality: `0.01431`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.05265 |
| `explicit.stat_4226189338@T1` | 1.55976 |
| `explicit.stat_2254480358@T1` | 1.55086 |
| `explicit.stat_591105508@T1` | 1.50897 |
| `explicit.stat_2768835289@T2` | -0.98311 |
| `explicit.stat_3962278098@T2` | -0.94558 |
| `explicit.stat_737908626@T1` | -0.91593 |
| `explicit.stat_737908626@T2` | -0.89667 |
| `explicit.stat_2968503605@T2` | -0.89486 |
| `explicit.stat_473429811@T1` | -0.88994 |
| `explicit.stat_293638271@T2` | -0.87894 |
| `explicit.stat_2231156303@T2` | -0.87707 |

### weapon.bow — n=7890, R²=-1.8118

intercept: `3.4873`  ·  log_price: True  ·  ilvl: `-0.04325`  ·  n_mods: `-0.01326`  ·  n_top_tier: `0.23841`  ·  corrupted: `-0.02851`  ·  n_sockets: `0.00037`  ·  quality: `0.00386`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.17510 |
| `crafted.stat_3035140377` | 2.06462 |
| `explicit.stat_1202301673@T1` | 2.05006 |
| `explicit.stat_2463230181@T1` | 1.98745 |
| `desecrated.stat_666077204@T1` | 1.97274 |
| `explicit.stat_518292764@T1` | 0.73382 |
| `explicit.stat_55876295@T1` | -0.32345 |
| `explicit.stat_2694482655@T1` | -0.30916 |
| `explicit.stat_55876295@T2` | -0.29361 |
| `explicit.stat_1037193709@T1` | -0.27474 |
| `explicit.stat_3261801346@T1` | -0.27214 |
| `explicit.stat_669069897@T2` | -0.27007 |

### weapon.crossbow — n=7471, R²=-1.6257

intercept: `3.5876`  ·  log_price: True  ·  ilvl: `-0.04483`  ·  n_mods: `-0.00883`  ·  n_top_tier: `0.39290`  ·  corrupted: `-0.06030`  ·  n_sockets: `0.00500`  ·  quality: `0.00239`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 1.88760 |
| `explicit.stat_1509134228@T1` | 1.87310 |
| `explicit.stat_709508406@T1` | 1.82201 |
| `explicit.stat_1202301673@T1` | 1.72619 |
| `explicit.stat_2250681686@T2` | -1.35530 |
| `crafted.stat_3035140377` | 1.21693 |
| `explicit.stat_2250681686` | 1.02203 |
| `rune.stat_2246411426` | -0.63844 |
| `explicit.stat_691932474@T1` | -0.63255 |
| `rune.stat_55876295` | 0.62762 |
| `explicit.stat_1202301673@T2` | -0.53077 |
| `explicit.stat_669069897@T1` | -0.49874 |

### flask.charm — n=3477, R²=-0.0862

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60509 |
| `explicit.stat_1056492907` | 2.99568 |
| `explicit.stat_3138344128` | 0.00875 |
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_3246948616` | 0.00002 |
| `explicit.stat_1873752457@T2` | -0.00001 |
| `explicit.stat_1873752457@T1` | -0.00001 |
| `explicit.stat_828533480@T2` | -0.00001 |
| `explicit.stat_828533480@T1` | -0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `explicit.stat_2676834156@T2` | -0.00001 |
| `explicit.stat_1120862500@T2` | -0.00001 |

### weapon.warstaff — n=2563, R²=-0.2458

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 0.44007 |
| `rune.stat_1037193709` | 0.27326 |
| `rune.stat_3336890334` | 0.18238 |
| `crafted.stat_210067635@T2` | 0.10973 |
| `rune.stat_1817052494` | -0.10930 |
| `rune.stat_2430860292` | -0.09423 |
| `rune.stat_1509134228` | 0.00950 |
| `rune.stat_1039491398` | -0.00855 |
| `explicit.stat_1509134228@T2` | 0.00003 |
| `explicit.stat_9187492@T1` | 0.00002 |
| `desecrated.stat_9187492` | 0.00002 |
| `explicit.stat_709508406@T2` | 0.00001 |

### weapon.sceptre — n=2452, R²=-0.277

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `desecrated.stat_1050105434` | 0.01279 |
| `desecrated.stat_3984865854` | -0.00553 |
| `explicit.stat_2162097452@T1` | 0.00004 |
| `explicit.stat_1263695895@T1` | 0.00004 |
| `explicit.stat_1998951374@T1` | 0.00002 |
| `explicit.stat_2162097452@T2` | 0.00002 |
| `explicit.stat_4010677958@T1` | 0.00002 |
| `explicit.stat_3057012405@T1` | 0.00002 |
| `explicit.stat_1798257884@T2` | 0.00002 |
| `explicit.stat_1998951374@T2` | 0.00002 |
| `explicit.stat_101878827@T2` | 0.00002 |
| `explicit.stat_1250712710@T2` | 0.00002 |

### weapon.staff — n=2427, R²=-0.2497

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_3990135792` | -0.13412 |
| `rune.stat_2974417149` | 0.08047 |
| `explicit.stat_124131830@T1` | 0.00004 |
| `explicit.stat_473429811@T1` | 0.00004 |
| `explicit.stat_3291658075@T2` | 0.00002 |
| `explicit.stat_274716455@T1` | 0.00002 |
| `explicit.stat_124131830@T2` | 0.00002 |
| `explicit.stat_293638271@T1` | 0.00002 |
| `explicit.stat_2968503605@T2` | 0.00002 |
| `explicit.stat_2254480358@T1` | 0.00002 |
| `explicit.stat_737908626@T2` | 0.00002 |
| `explicit.stat_2974417149@T2` | 0.00002 |

### weapon.spear — n=2118, R²=-0.2478

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_210067635@T1` | 0.00003 |
| `explicit.stat_1263695895@T1` | -0.00003 |
| `explicit.stat_1263695895@T2` | -0.00003 |
| `explicit.stat_1509134228@T1` | 0.00002 |
| `explicit.stat_2694482655@T1` | 0.00002 |
| `explicit.stat_3639275092@T1` | 0.00002 |
| `explicit.stat_9187492@T1` | -0.00002 |
| `explicit.stat_518292764@T1` | 0.00001 |
| `explicit.stat_1202301673@T2` | -0.00001 |
| `explicit.stat_748522257@T2` | 0.00001 |
| `explicit.stat_1509134228@T2` | 0.00001 |
| `explicit.stat_4080418644@T1` | -0.00001 |

### armour.focus — n=1766, R²=-0.029

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `-0.00005`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.53201 |
| `desecrated.stat_3465022881@T1` | 1.77754 |
| `desecrated.stat_2910761524@T1` | 0.96137 |
| `desecrated.stat_3393628375` | 0.53772 |
| `desecrated.stat_378817135@T1` | -0.25866 |
| `desecrated.stat_2910761524` | -0.11575 |
| `desecrated.stat_3465022881` | -0.10080 |
| `crafted.stat_4015621042` | 0.06673 |
| `desecrated.stat_378817135` | 0.05922 |
| `desecrated.stat_4220027924` | 0.00462 |
| `desecrated.stat_274716455` | 0.00133 |
| `desecrated.stat_4015621042` | 0.00061 |

### armour.quiver — n=1672, R²=-0.2655

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00003`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | -0.00006 |
| `explicit.stat_2463230181@T2` | -0.00002 |
| `explicit.stat_681332047@T1` | -0.00002 |
| `explicit.stat_3714003708@T2` | -0.00001 |
| `explicit.stat_3759663284@T1` | 0.00001 |
| `explicit.stat_3714003708@T1` | -0.00001 |
| `explicit.stat_681332047@T2` | -0.00001 |
| `explicit.stat_4067062424@T1` | 0.00001 |
| `explicit.stat_1241625305@T1` | 0.00001 |
| `explicit.stat_3695891184@T1` | 0.00001 |
| `explicit.stat_803737631@T2` | -0.00001 |
| `explicit.stat_1754445556@T1` | 0.00001 |

### armour.shield — n=1535, R²=-0.2871

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.10197`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 0.19317 |
| `explicit.stat_1011760251@T1` | -0.10206 |
| `explicit.stat_1301765461@T2` | -0.10203 |
| `explicit.stat_2339757871@T1` | -0.10200 |
| `explicit.stat_1011760251@T2` | -0.10200 |
| `explicit.stat_3771516363@T1` | -0.10198 |
| `explicit.stat_3639275092@T1` | -0.10198 |
| `explicit.stat_3855016469@T1` | -0.10198 |
| `explicit.stat_3484657501@T1` | -0.10198 |
| `explicit.stat_3639275092@T2` | -0.10198 |
| `explicit.stat_1062208444@T1` | -0.10198 |
| `explicit.stat_3372524247@T2` | -0.10197 |

### weapon.twomace — n=1298, R²=-0.2806

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1039491398` | 0.09607 |
| `rune.stat_1509134228` | -0.03469 |
| `explicit.stat_1037193709@T1` | -0.00005 |
| `explicit.stat_3336890334@T1` | -0.00005 |
| `explicit.stat_821021828@T1` | -0.00005 |
| `explicit.stat_821021828@T2` | -0.00005 |
| `explicit.stat_669069897@T1` | -0.00004 |
| `explicit.stat_1037193709@T2` | -0.00004 |
| `explicit.stat_669069897@T2` | -0.00003 |
| `explicit.stat_387439868@T2` | -0.00003 |
| `explicit.stat_1368271171@T1` | -0.00003 |
| `explicit.stat_1940865751@T1` | -0.00003 |

## Coverage (listings per base)

- … **Emerald** — 8764 listings (8764 priced) [0.7–5018207.5 ex]
- … **Sapphire** — 8730 listings (8729 priced) [0.6–5018207.5 ex]
- … **Ruby** — 6784 listings (6783 priced) [0.3–28868.8 ex]
- … **Utility Belt** — 4614 listings (4612 priced) [0.3–4555741.7 ex]
- … **Stellar Amulet** — 3448 listings (3448 priced) [0.3–4547453.5 ex]
- … **Prismatic Ring** — 3263 listings (3262 priced) [0.3–36899.4 ex]
- … **Solar Amulet** — 3194 listings (3191 priced) [0.4–4547453.5 ex]
- … **Gold Amulet** — 3122 listings (3122 priced) [0.4–292542.5 ex]
- … **Amethyst Ring** — 3098 listings (3097 priced) [0.4–71450.3 ex]
- … **Gold Ring** — 2982 listings (2981 priced) [0.4–10825.8 ex]
- … **Dueling Wand** — 2967 listings (2965 priced) [1.0–4599254.4 ex]
- … **Sapphire Ring** — 2480 listings (2480 priced) [0.4–70346.0 ex]
- … **Topaz Ring** — 2448 listings (2448 priced) [1.0–44572.1 ex]
- … **Ruby Ring** — 2390 listings (2390 priced) [0.8–44279.2 ex]
- … **Plate Belt** — 2294 listings (2294 priced) [0.4–4547453.5 ex]
- … **Obliterator Bow** — 2272 listings (2268 priced) [0.3–22139622146.9 ex]
- … **Lapis Amulet** — 2176 listings (2176 priced) [0.4–4547453.5 ex]
- … **Heavy Belt** — 2169 listings (2169 priced) [0.4–211038.1 ex]
- … **Amber Amulet** — 2145 listings (2145 priced) [0.4–4547453.5 ex]
- … **Ancestral Tiara** — 2141 listings (2139 priced) [0.6–5018207.5 ex]
- … **Jade Amulet** — 2120 listings (2119 priced) [0.4–4547453.5 ex]
- … **Unset Ring** — 1997 listings (1997 priced) [0.4–14467.7 ex]
- … **Bloodstone Amulet** — 1951 listings (1951 priced) [0.4–7275.7 ex]
- … **Pearl Ring** — 1929 listings (1929 priced) [0.4–14467.7 ex]
- … **Azure Amulet** — 1917 listings (1917 priced) [0.4–29714.8 ex]

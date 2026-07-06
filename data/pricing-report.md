# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-06T16:50:54+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **232516** (232340 priced in exalted)
- Distinct bases: 933 · distinct mods: 2630 · mod rows: 1104183
- Sold signals: **34892** sold · 121902 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-06T16:44:20+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×15.37** (median |log error| 2.7323)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 77% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.10** · typical error ×50.59 · ±30% 9% · n=33488
- Premium segment (60ex+): skill **+0.10** · typical error ×245.75 · ±30% 0% · n=20204

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 4304 | ×12.67 | 4% | +0.04 | +0.08 |
| accessory.amulet | 4129 | ×56.56 | 19% | +0.02 | +0.03 |
| jewel | 3719 | ×8.29 | 7% | +0.04 | +0.07 |
| accessory.belt | 3464 | ×10.92 | 20% | +0.05 | +0.08 |
| armour.chest | 3440 | ×10.28 | 20% | +0.06 | +0.09 |
| armour.helmet | 3311 | ×12.40 | 18% | +0.05 | +0.08 |
| armour.boots | 3177 | ×10.00 | 24% | +0.01 | +0.00 |
| armour.gloves | 3100 | ×14.54 | 25% | -0.00 | +0.00 |
| other | 2940 | ×10.00 | 35% | +0.19 | +0.10 |
| weapon.wand | 2213 | ×28.84 | 21% | +0.06 | +0.05 |
| weapon.bow | 1794 | ×11.12 | 21% | +0.07 | +0.08 |
| weapon.crossbow | 1707 | ×15.06 | 19% | +0.08 | +0.09 |
| weapon.warstaff | 615 | ×45.00 | 20% | +0.00 | +0.00 |
| weapon.staff | 563 | ×50.00 | 19% | +0.00 | +0.00 |
| weapon.sceptre | 559 | ×50.00 | 15% | +0.00 | +0.00 |
| weapon.spear | 465 | ×30.00 | 21% | +0.00 | +0.00 |
| armour.quiver | 417 | ×45.00 | 18% | +0.00 | +0.00 |
| armour.focus | 407 | ×50.00 | 15% | +0.02 | +0.02 |
| flask.charm | 323 | ×20.00 | 40% | -0.00 | +0.00 |
| armour.shield | 320 | ×10.00 | 15% | +0.00 | +0.00 |
| weapon.twomace | 286 | ×10.00 | 16% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=25884, R²=-0.3682

intercept: `1.6069`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `0.06465`  ·  n_top_tier: `1.16278`  ·  corrupted: `2.45943`  ·  n_sockets: `-0.00022`  ·  quality: `-0.00002`

| stat_id | coef |
|---|---|
| `explicit.stat_2891184298@T1` | 2.83093 |
| `explicit.stat_3291658075@T1` | 2.81958 |
| `explicit.stat_3141070085@T1` | 2.51866 |
| `explicit.stat_1589917703@T1` | 2.48428 |
| `explicit.stat_1050105434@T1` | -2.48271 |
| `explicit.stat_101878827@T1` | 2.45386 |
| `explicit.stat_2106365538@T1` | 2.30546 |
| `explicit.stat_3917489142@T1` | 2.12366 |
| `explicit.stat_789117908@T1` | -1.71458 |
| `explicit.stat_2974417149@T1` | 1.04246 |
| `explicit.stat_2968503605@T1` | 0.42674 |
| `implicit.stat_2901986750` | 0.30122 |

### accessory.ring — n=19837, R²=-1.2817

intercept: `4.3497`  ·  log_price: True  ·  ilvl: `-0.03890`  ·  n_mods: `-0.14371`  ·  n_top_tier: `-0.24506`  ·  corrupted: `0.87351`  ·  n_sockets: `1.11063`  ·  quality: `0.04325`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.74727 |
| `explicit.stat_2557965901@T1` | 3.41744 |
| `explicit.stat_707457662@T2` | 3.41043 |
| `explicit.stat_2557965901@T2` | 3.09707 |
| `explicit.stat_1379411836@T1` | -1.85074 |
| `explicit.stat_2923486259@T2` | 1.35458 |
| `explicit.stat_1379411836@T2` | -1.11586 |
| `explicit.stat_736967255@T1` | 0.99591 |
| `explicit.stat_2923486259@T1` | 0.97164 |
| `explicit.stat_1754445556@T1` | 0.87266 |
| `explicit.stat_3032590688@T2` | 0.85402 |
| `explicit.stat_3261801346@T2` | 0.71285 |

### jewel — n=19405, R²=-0.6543

intercept: `-1.1864`  ·  log_price: True  ·  ilvl: `0.03844`  ·  n_mods: `0.16007`  ·  n_top_tier: `-0.11432`  ·  corrupted: `0.17069`  ·  quality: `0.21858`

| stat_id | coef |
|---|---|
| `explicit.stat_21071013@T1` | -3.58697 |
| `explicit.stat_3714003708@T1` | -3.44353 |
| `explicit.stat_1316278494@T1` | -3.21452 |
| `explicit.stat_3824372849@T1` | 3.16089 |
| `explicit.stat_1697951953@T1` | -2.59069 |
| `explicit.stat_1569101201@T1` | 2.58373 |
| `explicit.stat_3780644166@T1` | 2.44064 |
| `explicit.stat_416040624@T1` | -2.32501 |
| `explicit.stat_153777645@T1` | 2.19864 |
| `explicit.stat_2106365538@T1` | -2.15367 |
| `explicit.stat_818778753@T1` | -2.13978 |
| `explicit.stat_2456523742@T1` | 2.12051 |

### accessory.amulet — n=19011, R²=-2.0737

intercept: `4.2728`  ·  log_price: True  ·  ilvl: `-0.05215`  ·  n_mods: `-0.02485`  ·  n_top_tier: `0.34489`  ·  corrupted: `0.08351`  ·  n_sockets: `1.79665`  ·  quality: `-0.05679`

| stat_id | coef |
|---|---|
| `explicit.stat_3981240776@T2` | 1.78759 |
| `explicit.stat_3981240776@T1` | 1.39408 |
| `explicit.stat_124131830` | 1.20804 |
| `explicit.stat_1202301673` | 0.96490 |
| `explicit.stat_3372524247@T1` | 0.69389 |
| `explicit.stat_3556824919@T1` | 0.56613 |
| `explicit.stat_3299347043@T1` | -0.51111 |
| `explicit.stat_983749596@T2` | -0.48720 |
| `explicit.stat_9187492@T2` | 0.48409 |
| `explicit.stat_3299347043@T2` | -0.44593 |
| `explicit.stat_3917489142@T2` | -0.44267 |
| `explicit.stat_2748665614@T1` | -0.43467 |

### accessory.belt — n=16061, R²=-1.3658

intercept: `3.3691`  ·  log_price: True  ·  ilvl: `-0.04053`  ·  n_mods: `-0.01998`  ·  n_top_tier: `0.04749`  ·  corrupted: `0.60248`  ·  n_sockets: `-0.09292`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 2.91838 |
| `explicit.stat_3372524247@T1` | 0.23931 |
| `explicit.stat_2923486259@T2` | 0.22097 |
| `explicit.stat_1836676211@T1` | 0.18127 |
| `pseudo.total_ele_res>=80` | 0.12866 |
| `explicit.stat_2923486259@T1` | 0.11324 |
| `explicit.stat_3299347043@T1` | -0.11030 |
| `explicit.stat_809229260@T2` | -0.08360 |
| `explicit.stat_2639966148` | 0.08271 |
| `explicit.stat_3299347043@T2` | -0.08111 |
| `explicit.stat_174664100` | 0.08103 |
| `explicit.stat_2881298780@T1` | -0.08065 |

### armour.chest — n=15901, R²=-1.3694

intercept: `3.8777`  ·  log_price: True  ·  ilvl: `-0.04790`  ·  n_mods: `-0.02398`  ·  n_top_tier: `0.46088`  ·  corrupted: `0.18213`  ·  n_sockets: `0.02175`  ·  quality: `0.01960`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.89150 |
| `explicit.stat_3981240776@T1` | 1.34137 |
| `explicit.stat_3981240776@T2` | 0.72649 |
| `explicit.stat_4015621042@T1` | -0.63699 |
| `explicit.stat_4080418644@T2` | -0.54350 |
| `explicit.stat_3261801346@T2` | -0.52343 |
| `explicit.stat_4080418644@T1` | -0.52215 |
| `explicit.stat_3325883026@T2` | -0.51550 |
| `explicit.stat_986397080@T2` | -0.51279 |
| `explicit.stat_1692879867@T1` | -0.50409 |
| `explicit.stat_3321629045@T1` | -0.50206 |
| `explicit.stat_2451402625@T1` | -0.49609 |

### armour.helmet — n=15553, R²=-1.3957

intercept: `4.4644`  ·  log_price: True  ·  ilvl: `-0.05580`  ·  n_mods: `-0.02544`  ·  n_top_tier: `0.55280`  ·  corrupted: `0.36075`  ·  n_sockets: `-0.01065`  ·  quality: `0.01836`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.73314 |
| `explicit.stat_2339757871@T1` | -3.94185 |
| `explicit.stat_53045048@T1` | -0.74266 |
| `explicit.stat_4015621042@T2` | -0.66931 |
| `explicit.stat_1062208444@T2` | -0.66251 |
| `explicit.stat_2162097452@T2` | -0.65763 |
| `explicit.stat_1263695895@T1` | -0.64483 |
| `explicit.stat_53045048@T2` | -0.63315 |
| `explicit.stat_803737631@T2` | -0.62783 |
| `explicit.stat_4015621042@T1` | -0.60910 |
| `explicit.stat_4080418644@T2` | -0.60375 |
| `explicit.stat_4052037485@T2` | -0.59299 |

### armour.boots — n=14636, R²=-0.1939

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.32551`  ·  corrupted: `0.00034`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2250533757@T2` | -0.98790 |
| `explicit.stat_2339757871@T1` | -0.32556 |
| `explicit.stat_3362812763@T2` | -0.32553 |
| `explicit.stat_2451402625@T2` | -0.32553 |
| `explicit.stat_2923486259@T2` | -0.32553 |
| `explicit.stat_124859000@T1` | -0.32553 |
| `explicit.stat_3362812763@T1` | -0.32552 |
| `explicit.stat_99927264@T2` | -0.32552 |
| `explicit.stat_3261801346@T2` | -0.32552 |
| `explicit.stat_1062208444@T1` | -0.32552 |
| `explicit.stat_99927264@T1` | -0.32552 |
| `explicit.stat_3917489142@T2` | -0.32552 |

### armour.gloves — n=14394, R²=-0.28

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00340`  ·  corrupted: `0.06604`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3372524247@T1` | 0.17357 |
| `desecrated.stat_3032590688` | 0.09372 |
| `desecrated.stat_4067062424` | 0.08225 |
| `desecrated.stat_1573130764` | 0.05382 |
| `explicit.stat_4067062424@T1` | 0.05114 |
| `pseudo.total_ele_res>=80` | 0.02043 |
| `pseudo.total_life` | 0.01150 |
| `explicit.stat_3299347043` | -0.01150 |
| `rune.stat_3299347043` | -0.01150 |
| `explicit.stat_9187492@T2` | -0.00517 |
| `explicit.stat_9187492@T1` | 0.00481 |
| `desecrated.stat_3299347043` | -0.00470 |

### weapon.wand — n=10178, R²=-1.8703

intercept: `3.6055`  ·  log_price: True  ·  ilvl: `-0.04507`  ·  n_mods: `-0.00796`  ·  n_top_tier: `0.40208`  ·  corrupted: `0.01540`  ·  n_sockets: `0.00310`  ·  quality: `0.02475`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.75795 |
| `explicit.stat_2254480358@T1` | 2.01354 |
| `explicit.stat_4226189338@T1` | 1.98631 |
| `explicit.stat_591105508@T1` | 1.97891 |
| `explicit.stat_1600707273@T1` | 1.69457 |
| `explicit.stat_1545858329@T1` | 1.25765 |
| `explicit.stat_1600707273@T2` | 0.77733 |
| `crafted.stat_124131830` | 0.76956 |
| `explicit.stat_736967255@T2` | 0.73228 |
| `explicit.stat_3962278098@T2` | -0.46805 |
| `explicit.stat_737908626@T2` | -0.46373 |
| `explicit.stat_737908626@T1` | -0.45245 |

### weapon.bow — n=8367, R²=-1.8304

intercept: `3.4319`  ·  log_price: True  ·  ilvl: `-0.04267`  ·  n_mods: `-0.01026`  ·  n_top_tier: `0.36074`  ·  corrupted: `-0.06163`  ·  n_sockets: `0.00245`  ·  quality: `0.00350`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | 1.90945 |
| `explicit.stat_1202301673@T1` | 1.90721 |
| `desecrated.stat_210067635@T1` | -1.68872 |
| `explicit.stat_518292764@T1` | 1.26831 |
| `crafted.stat_3035140377` | 1.24188 |
| `desecrated.stat_666077204@T1` | -1.05995 |
| `explicit.stat_55876295@T1` | -0.43708 |
| `explicit.stat_2694482655@T1` | -0.41753 |
| `explicit.stat_3261801346@T1` | -0.40777 |
| `explicit.stat_55876295@T2` | -0.40755 |
| `explicit.stat_1037193709@T1` | -0.39585 |
| `explicit.stat_3261801346@T2` | -0.39426 |

### weapon.crossbow — n=7916, R²=-1.6661

intercept: `3.5184`  ·  log_price: True  ·  ilvl: `-0.04397`  ·  n_mods: `-0.00579`  ·  n_top_tier: `0.46494`  ·  corrupted: `-0.02579`  ·  n_sockets: `0.01013`  ·  quality: `0.00424`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 1.78349 |
| `explicit.stat_1509134228@T1` | 1.74321 |
| `explicit.stat_709508406@T1` | 1.72863 |
| `explicit.stat_1202301673@T1` | 1.68132 |
| `explicit.stat_2250681686@T2` | -1.36697 |
| `crafted.stat_3035140377` | 1.15379 |
| `explicit.stat_2250681686` | 0.98872 |
| `explicit.stat_691932474@T1` | -0.79859 |
| `rune.stat_2246411426` | -0.64034 |
| `rune.stat_55876295` | 0.63317 |
| `explicit.stat_1202301673@T2` | -0.59197 |
| `explicit.stat_669069897@T2` | -0.55014 |

### flask.charm — n=4005, R²=-0.1325

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00009`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60510 |
| `explicit.stat_1056492907` | 2.98465 |
| `explicit.stat_3138344128` | 0.01559 |
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_1873752457@T2` | -0.00002 |
| `explicit.stat_2676834156@T2` | -0.00002 |
| `explicit.stat_1873752457@T1` | -0.00002 |
| `explicit.stat_828533480@T2` | -0.00002 |
| `explicit.stat_828533480@T1` | -0.00002 |
| `explicit.stat_3246948616` | 0.00002 |
| `explicit.stat_3196823591@T2` | -0.00002 |
| `explicit.stat_388617051@T2` | -0.00002 |

### weapon.warstaff — n=2946, R²=-0.3435

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 2.30136 |
| `rune.stat_1037193709` | 0.26849 |
| `rune.stat_3336890334` | 0.16343 |
| `rune.stat_1817052494` | -0.10739 |
| `rune.stat_2430860292` | -0.08444 |
| `crafted.stat_210067635@T2` | 0.00453 |
| `rune.stat_1509134228` | 0.00158 |
| `rune.stat_1039491398` | -0.00143 |
| `desecrated.stat_9187492` | 0.00003 |
| `explicit.stat_1509134228@T2` | 0.00003 |
| `desecrated.stat_518292764` | -0.00003 |
| `rune.stat_2077615515` | 0.00002 |

### weapon.staff — n=2788, R²=-0.342

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 4.20571 |
| `rune.stat_3990135792` | -0.13411 |
| `rune.stat_2974417149` | 0.08046 |
| `explicit.stat_473429811@T1` | 0.00021 |
| `crafted.stat_124131830` | 0.00006 |
| `explicit.stat_124131830@T1` | 0.00003 |
| `explicit.stat_2254480358@T1` | 0.00003 |
| `explicit.stat_4226189338@T1` | 0.00003 |
| `explicit.stat_3278136794@T2` | 0.00002 |
| `explicit.stat_124131830@T2` | 0.00002 |
| `explicit.stat_274716455@T1` | 0.00002 |
| `explicit.stat_2968503605@T2` | 0.00002 |

### weapon.sceptre — n=2787, R²=-0.3721

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00013`

| stat_id | coef |
|---|---|
| `rune.stat_3984865854` | 0.04380 |
| `rune.stat_1611856026` | 0.02190 |
| `desecrated.stat_1050105434` | 0.01270 |
| `desecrated.stat_3984865854` | -0.00514 |
| `explicit.stat_2162097452@T1` | 0.00037 |
| `explicit.stat_1263695895@T1` | 0.00006 |
| `explicit.stat_1798257884@T2` | 0.00004 |
| `explicit.stat_3057012405@T1` | 0.00003 |
| `explicit.stat_2162097452@T2` | 0.00003 |
| `explicit.stat_4010677958@T1` | 0.00003 |
| `explicit.stat_1263695895@T2` | 0.00003 |
| `explicit.stat_101878827@T2` | 0.00002 |

### weapon.spear — n=2431, R²=-0.3255

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.49787 |
| `crafted.stat_518292764` | 0.72874 |
| `rune.stat_1509134228` | -0.01189 |
| `rune.stat_1039491398` | 0.01189 |
| `explicit.stat_210067635@T1` | 0.00005 |
| `explicit.stat_1263695895@T2` | -0.00004 |
| `explicit.stat_1263695895@T1` | -0.00004 |
| `explicit.stat_1940865751@T1` | 0.00003 |
| `explicit.stat_2694482655@T1` | 0.00003 |
| `explicit.stat_1509134228@T1` | 0.00002 |
| `explicit.stat_709508406@T1` | 0.00002 |
| `explicit.stat_3639275092@T1` | 0.00002 |

### armour.focus — n=1997, R²=-0.1896

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `-0.00007`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.51090 |
| `desecrated.stat_3465022881@T1` | 1.92583 |
| `desecrated.stat_2910761524@T1` | 0.92025 |
| `desecrated.stat_3393628375` | 0.53649 |
| `desecrated.stat_3465022881` | -0.11200 |
| `desecrated.stat_2910761524` | -0.10842 |
| `crafted.stat_4015621042` | 0.06669 |
| `desecrated.stat_4015621042` | 0.03537 |
| `rune.stat_3523867985` | 0.00587 |
| `desecrated.stat_274716455` | 0.00524 |
| `desecrated.stat_4220027924` | 0.00469 |
| `desecrated.stat_737908626` | -0.00140 |

### armour.quiver — n=1901, R²=-0.3705

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00003`

| stat_id | coef |
|---|---|
| `desecrated.stat_3759663284` | 0.00099 |
| `explicit.stat_2463230181@T1` | -0.00008 |
| `explicit.stat_2463230181@T2` | -0.00004 |
| `explicit.stat_681332047@T1` | -0.00004 |
| `explicit.stat_3714003708@T1` | -0.00003 |
| `explicit.stat_3714003708@T2` | -0.00003 |
| `explicit.stat_681332047@T2` | -0.00003 |
| `explicit.stat_803737631@T2` | -0.00003 |
| `explicit.stat_1368271171@T2` | -0.00003 |
| `explicit.stat_3032590688@T1` | -0.00002 |
| `explicit.stat_1573130764@T1` | -0.00002 |
| `explicit.stat_3032590688@T2` | -0.00002 |

### armour.shield — n=1685, R²=-0.3261

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.06713`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.69783 |
| `explicit.stat_1301765461@T1` | 0.26806 |
| `explicit.stat_1978899297@T2` | -0.23395 |
| `explicit.stat_1978899297` | 0.16679 |
| `explicit.stat_1011760251@T1` | -0.06720 |
| `explicit.stat_1301765461@T2` | -0.06718 |
| `explicit.stat_2339757871@T1` | -0.06717 |
| `explicit.stat_3639275092@T2` | -0.06715 |
| `explicit.stat_3639275092@T1` | -0.06715 |
| `explicit.stat_1011760251@T2` | -0.06715 |
| `explicit.stat_2481353198@T1` | -0.06715 |
| `explicit.stat_3771516363@T1` | -0.06715 |

### weapon.twomace — n=1445, R²=-0.3331

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00004`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1039491398` | 0.12662 |
| `rune.stat_1509134228` | -0.04572 |
| `desecrated.stat_1509134228` | 0.02424 |
| `explicit.stat_3336890334@T1` | -0.00009 |
| `explicit.stat_1263695895@T1` | -0.00008 |
| `explicit.stat_1037193709@T1` | -0.00008 |
| `explicit.stat_1037193709@T2` | -0.00007 |
| `explicit.stat_1263695895@T2` | -0.00007 |
| `explicit.stat_669069897@T1` | -0.00007 |
| `explicit.stat_669069897@T2` | -0.00006 |
| `explicit.stat_821021828@T1` | -0.00006 |
| `explicit.stat_387439868@T2` | -0.00006 |

## Coverage (listings per base)

- … **Emerald** — 9434 listings (9434 priced) [0.7–7553463.8 ex]
- … **Sapphire** — 9363 listings (9362 priced) [0.6–7553463.8 ex]
- … **Ruby** — 7303 listings (7302 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 4892 listings (4890 priced) [0.3–4877938.3 ex]
- … **Stellar Amulet** — 3647 listings (3647 priced) [0.3–4547453.5 ex]
- … **Prismatic Ring** — 3485 listings (3484 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 3413 listings (3408 priced) [0.4–4906562.9 ex]
- … **Amethyst Ring** — 3322 listings (3321 priced) [0.4–71450.3 ex]
- … **Gold Amulet** — 3304 listings (3304 priced) [0.5–292542.5 ex]
- … **Gold Ring** — 3168 listings (3167 priced) [0.4–24532814.5 ex]
- … **Dueling Wand** — 3139 listings (3136 priced) [1.0–3736768402.2 ex]
- … **Sapphire Ring** — 2645 listings (2645 priced) [0.4–24532814.5 ex]
- … **Topaz Ring** — 2608 listings (2608 priced) [1.0–24532814.5 ex]
- … **Ruby Ring** — 2538 listings (2538 priced) [0.5–146119.1 ex]
- … **Plate Belt** — 2439 listings (2439 priced) [0.4–4877938.3 ex]
- … **Obliterator Bow** — 2409 listings (2404 priced) [0.3–22139622146.9 ex]
- … **Lapis Amulet** — 2313 listings (2313 priced) [0.4–4547453.5 ex]
- … **Heavy Belt** — 2300 listings (2300 priced) [0.4–4877938.3 ex]
- … **Amber Amulet** — 2293 listings (2293 priced) [0.5–4547453.5 ex]
- … **Ancestral Tiara** — 2292 listings (2290 priced) [0.6–5018207.5 ex]
- … **Jade Amulet** — 2269 listings (2268 priced) [0.4–4547453.5 ex]
- … **Unset Ring** — 2121 listings (2121 priced) [0.4–24532814.5 ex]
- … **Bloodstone Amulet** — 2103 listings (2103 priced) [0.4–7275.7 ex]
- … **Pearl Ring** — 2065 listings (2065 priced) [0.4–24532814.5 ex]
- … **Azure Amulet** — 2036 listings (2036 priced) [0.4–4877938.3 ex]

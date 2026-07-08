# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-08T06:48:04+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **315767** (315355 priced in exalted)
- Distinct bases: 954 · distinct mods: 2811 · mod rows: 1498751
- Sold signals: **30786** sold · 169237 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-08T06:38:34+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×20.14** (median |log error| 3.0026)
- Within ±30% of asking price: **15%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.08** · typical error ×47.65 · ±30% 7% · n=45821
- Premium segment (60ex+): skill **+0.09** · typical error ×226.11 · ±30% 0% · n=28496

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 5978 | ×50.74 | 20% | +0.03 | +0.04 |
| accessory.amulet | 5650 | ×38.02 | 19% | +0.02 | +0.02 |
| jewel | 5230 | ×8.63 | 7% | +0.01 | +0.04 |
| accessory.belt | 4620 | ×10.00 | 19% | +0.03 | +0.03 |
| armour.chest | 4534 | ×10.21 | 7% | +0.06 | +0.07 |
| armour.helmet | 4408 | ×12.39 | 6% | +0.03 | +0.04 |
| armour.boots | 4146 | ×17.15 | 9% | +0.11 | +0.13 |
| armour.gloves | 4019 | ×18.53 | 7% | +0.11 | +0.11 |
| other | 3818 | ×9.83 | 38% | +0.05 | +0.15 |
| weapon.wand | 2804 | ×36.53 | 21% | +0.06 | +0.06 |
| weapon.bow | 2222 | ×20.06 | 20% | +0.08 | +0.10 |
| weapon.crossbow | 2050 | ×17.92 | 19% | +0.09 | +0.12 |
| weapon.warstaff | 1032 | ×70.92 | 16% | +0.02 | +0.04 |
| weapon.sceptre | 944 | ×50.00 | 12% | +0.08 | +0.04 |
| weapon.staff | 880 | ×50.00 | 19% | +0.04 | +0.06 |
| weapon.spear | 804 | ×40.00 | 18% | +0.02 | +0.01 |
| armour.focus | 632 | ×610.33 | 12% | +0.02 | +0.06 |
| armour.quiver | 616 | ×74.94 | 12% | -0.00 | +0.05 |
| armour.shield | 534 | ×20.00 | 17% | +0.02 | +0.03 |
| weapon.twomace | 479 | ×30.00 | 12% | +0.02 | +0.07 |
| flask.charm | 413 | ×5.00 | 38% | -0.00 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=32752, R²=-0.5816

intercept: `1.6076`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `0.00431`  ·  n_top_tier: `0.35576`  ·  corrupted: `0.79278`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2891184298@T1` | 1.45585 |
| `explicit.stat_3291658075@T1` | 1.04316 |
| `explicit.stat_2974417149@T1` | 0.87686 |
| `explicit.stat_101878827@T1` | -0.70198 |
| `explicit.stat_3917489142@T1` | 0.54841 |
| `explicit.stat_1050105434@T1` | -0.50403 |
| `explicit.stat_2106365538@T1` | 0.42039 |
| `explicit.stat_1589917703@T1` | 0.32982 |
| `explicit.stat_789117908@T1` | -0.29679 |
| `explicit.stat_3141070085@T1` | -0.27650 |
| `implicit.stat_1379411836` | -0.25437 |
| `implicit.stat_4041853756` | 0.22985 |

### jewel — n=28382, R²=-0.6208

intercept: `-1.0893`  ·  log_price: True  ·  ilvl: `0.03697`  ·  n_mods: `0.13321`  ·  n_top_tier: `-0.02474`  ·  corrupted: `0.23047`  ·  quality: `0.21793`

| stat_id | coef |
|---|---|
| `explicit.stat_3741323227@T1` | -3.58199 |
| `explicit.stat_1569101201@T1` | 3.39401 |
| `explicit.stat_3192728503@T1` | -3.39398 |
| `explicit.stat_3714003708@T1` | -2.94122 |
| `explicit.stat_1569159338@T1` | -2.63451 |
| `explicit.stat_1316278494@T1` | -2.60348 |
| `explicit.stat_2527686725@T1` | 1.88642 |
| `explicit.stat_234296660@T1` | -1.80741 |
| `explicit.stat_2106365538@T1` | -1.78170 |
| `explicit.stat_1594812856@T1` | -1.71924 |
| `explicit.stat_4045894391@T1` | -1.71258 |
| `explicit.stat_3374165039@T1` | -1.60676 |

### accessory.ring — n=27435, R²=-1.9563

intercept: `4.8387`  ·  log_price: True  ·  ilvl: `-0.05817`  ·  n_mods: `-0.00329`  ·  n_top_tier: `0.27281`  ·  corrupted: `0.89995`  ·  n_sockets: `-0.18312`  ·  quality: `0.08457`

| stat_id | coef |
|---|---|
| `explicit.stat_1379411836@T1` | -1.70542 |
| `explicit.stat_1379411836@T2` | -1.34974 |
| `explicit.stat_1671376347@T1` | 1.04021 |
| `explicit.stat_707457662@T1` | 0.40986 |
| `explicit.stat_1263695895@T1` | -0.38200 |
| `explicit.stat_803737631@T1` | -0.33880 |
| `explicit.stat_803737631@T2` | -0.33682 |
| `explicit.stat_3291658075@T2` | -0.33145 |
| `explicit.stat_1263695895@T2` | -0.32552 |
| `explicit.stat_3291658075@T1` | -0.32325 |
| `explicit.stat_2231156303@T1` | -0.31522 |
| `explicit.stat_1368271171@T1` | -0.30721 |

### accessory.amulet — n=25977, R²=-2.0715

intercept: `4.0801`  ·  log_price: True  ·  ilvl: `-0.04905`  ·  n_mods: `-0.03237`  ·  n_top_tier: `1.00586`  ·  corrupted: `0.08408`  ·  n_sockets: `0.85631`  ·  quality: `-0.00179`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.24123 |
| `explicit.stat_983749596@T1` | -1.14990 |
| `explicit.stat_983749596@T2` | -1.12541 |
| `explicit.stat_587431675@T1` | -1.11604 |
| `explicit.stat_3325883026@T1` | -1.10463 |
| `explicit.stat_2748665614@T1` | -1.10429 |
| `explicit.stat_2748665614@T2` | -1.08161 |
| `explicit.stat_3325883026@T2` | -1.07941 |
| `explicit.stat_472520716@T1` | -1.07267 |
| `explicit.stat_3489782002@T2` | -1.07169 |
| `explicit.stat_472520716@T2` | -1.07000 |
| `explicit.stat_3917489142@T2` | -1.06244 |

### accessory.belt — n=21111, R²=-0.1391

intercept: `2.3063`  ·  log_price: True  ·  ilvl: `-0.00004`  ·  n_mods: `-0.00051`  ·  n_top_tier: `0.00119`  ·  corrupted: `0.00054`  ·  n_sockets: `-0.69272`

| stat_id | coef |
|---|---|
| `explicit.stat_2639966148` | 0.06046 |
| `pseudo.total_ele_res>=80` | 0.05970 |
| `explicit.stat_3811191316` | 0.04926 |
| `explicit.stat_174664100` | 0.04296 |
| `explicit.stat_770672621` | 0.03122 |
| `pseudo.total_chaos_res` | 0.02386 |
| `explicit.stat_2923486259` | -0.02381 |
| `explicit.stat_3742865955` | 0.02187 |
| `explicit.stat_2957407601` | 0.01988 |
| `implicit.stat_644456512` | -0.01872 |
| `explicit.stat_1485480327` | 0.01458 |
| `explicit.stat_1389754388@T1` | -0.00188 |

### armour.chest — n=20888, R²=-0.8893

intercept: `4.1771`  ·  log_price: True  ·  ilvl: `-0.04837`  ·  n_mods: `-0.10614`  ·  n_top_tier: `0.52434`  ·  corrupted: `0.06815`  ·  n_sockets: `0.06221`  ·  quality: `0.02490`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.87693 |
| `explicit.stat_915769802@T1` | -1.11548 |
| `explicit.stat_4015621042@T1` | -1.00317 |
| `explicit.stat_3321629045@T1` | -0.83145 |
| `explicit.stat_986397080@T2` | -0.78132 |
| `explicit.stat_915769802@T2` | -0.77062 |
| `explicit.stat_3261801346@T1` | -0.71907 |
| `explicit.stat_3325883026@T2` | -0.70398 |
| `explicit.stat_2923486259@T1` | -0.70190 |
| `explicit.stat_4080418644@T2` | -0.67494 |
| `explicit.stat_3484657501@T1` | -0.65791 |
| `explicit.stat_3261801346@T2` | -0.65401 |

### armour.helmet — n=20467, R²=-0.7382

intercept: `4.1293`  ·  log_price: True  ·  ilvl: `-0.05043`  ·  n_mods: `-0.11147`  ·  n_top_tier: `0.48633`  ·  corrupted: `0.76435`  ·  n_sockets: `0.01272`  ·  quality: `0.02770`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.98252 |
| `explicit.stat_53045048@T2` | -1.11609 |
| `explicit.stat_4080418644@T2` | -0.95624 |
| `explicit.stat_1062208444@T2` | -0.91855 |
| `explicit.stat_3362812763@T1` | -0.90848 |
| `explicit.stat_53045048@T1` | -0.90200 |
| `explicit.stat_3362812763@T2` | -0.66542 |
| `explicit.stat_328541901@T2` | -0.66378 |
| `explicit.stat_2162097452@T2` | -0.64397 |
| `explicit.stat_803737631@T2` | -0.63231 |
| `explicit.stat_1050105434@T1` | -0.62096 |
| `explicit.stat_1263695895@T1` | -0.59750 |

### armour.boots — n=19324, R²=-1.0203

intercept: `4.2603`  ·  log_price: True  ·  ilvl: `-0.05196`  ·  n_mods: `-0.07972`  ·  n_top_tier: `0.44947`  ·  corrupted: `0.40278`  ·  n_sockets: `0.11800`  ·  quality: `0.01895`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.62911 |
| `explicit.stat_2339757871@T1` | -1.16961 |
| `explicit.stat_2923486259@T2` | -0.86373 |
| `rune.stat_836936635` | -0.75236 |
| `explicit.stat_3362812763@T1` | -0.69108 |
| `explicit.stat_1062208444@T2` | -0.68856 |
| `explicit.stat_3917489142@T2` | -0.65186 |
| `explicit.stat_4220027924@T1` | 0.64637 |
| `explicit.stat_328541901@T1` | -0.64533 |
| `explicit.stat_3321629045@T1` | -0.63541 |
| `explicit.stat_3484657501@T2` | -0.61328 |
| `explicit.stat_99927264@T1` | -0.61186 |

### armour.gloves — n=18833, R²=-1.0749

intercept: `3.7940`  ·  log_price: True  ·  ilvl: `-0.05195`  ·  n_mods: `-0.05587`  ·  n_top_tier: `0.47141`  ·  corrupted: `0.25113`  ·  n_sockets: `0.33651`  ·  quality: `0.01694`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.93178 |
| `explicit.stat_681332047@T2` | -1.03448 |
| `explicit.stat_328541901@T1` | -0.94621 |
| `explicit.stat_3484657501@T2` | -0.86973 |
| `explicit.stat_803737631@T2` | -0.86666 |
| `explicit.stat_2797971005@T2` | -0.81776 |
| `explicit.stat_2797971005@T1` | -0.70039 |
| `explicit.stat_3299347043@T2` | -0.68700 |
| `explicit.stat_3033371881@T2` | -0.67169 |
| `explicit.stat_9187492@T1` | 0.66367 |
| `explicit.stat_4220027924@T2` | -0.64476 |
| `explicit.stat_2557965901@T1` | -0.62098 |

### weapon.wand — n=12928, R²=-2.0228

intercept: `3.6472`  ·  log_price: True  ·  ilvl: `-0.04559`  ·  n_mods: `-0.00640`  ·  n_top_tier: `0.85105`  ·  corrupted: `-0.01643`  ·  n_sockets: `0.01910`  ·  quality: `0.02472`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.24566 |
| `explicit.stat_591105508@T1` | 1.53620 |
| `explicit.stat_4226189338@T1` | 1.52828 |
| `explicit.stat_124131830@T1` | 1.52491 |
| `explicit.stat_1545858329@T1` | 1.49616 |
| `explicit.stat_1600707273@T1` | 1.47904 |
| `explicit.stat_736967255@T2` | 0.94264 |
| `explicit.stat_737908626@T1` | -0.89338 |
| `explicit.stat_2768835289@T2` | -0.89079 |
| `explicit.stat_2968503605@T2` | -0.87802 |
| `explicit.stat_3015669065@T1` | -0.87795 |
| `explicit.stat_1368271171@T2` | -0.87681 |

### weapon.bow — n=10525, R²=-1.9659

intercept: `3.3707`  ·  log_price: True  ·  ilvl: `-0.04170`  ·  n_mods: `-0.01158`  ·  n_top_tier: `0.48135`  ·  corrupted: `0.01755`  ·  n_sockets: `0.00329`  ·  quality: `0.01113`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.95381 |
| `explicit.stat_2463230181@T1` | 1.77784 |
| `explicit.stat_1202301673@T1` | 1.54864 |
| `crafted.stat_3035140377` | 1.13211 |
| `rune.stat_3885405204` | -0.60374 |
| `explicit.stat_55876295@T1` | -0.54612 |
| `explicit.stat_3695891184@T2` | -0.53280 |
| `explicit.stat_3336890334@T2` | -0.52660 |
| `explicit.stat_3695891184@T1` | -0.51802 |
| `explicit.stat_2694482655@T1` | -0.51738 |
| `explicit.stat_3261801346@T1` | -0.51369 |
| `explicit.stat_3639275092@T1` | -0.51161 |

### weapon.crossbow — n=9911, R²=-1.7723

intercept: `3.6758`  ·  log_price: True  ·  ilvl: `-0.04576`  ·  n_mods: `-0.00743`  ·  n_top_tier: `0.68118`  ·  corrupted: `-0.01762`  ·  n_sockets: `0.01770`  ·  quality: `0.00755`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -2.75373 |
| `explicit.stat_1980802737` | 2.03684 |
| `explicit.stat_709508406@T1` | 1.49910 |
| `explicit.stat_2250681686@T2` | -1.47778 |
| `explicit.stat_1202301673@T1` | 1.28337 |
| `explicit.stat_1037193709@T1` | 1.06159 |
| `explicit.stat_1509134228@T1` | 1.02718 |
| `explicit.stat_1202301673@T2` | -0.94355 |
| `explicit.stat_2250681686` | 0.81858 |
| `explicit.stat_1509134228@T2` | -0.80198 |
| `crafted.stat_3035140377` | 0.77024 |
| `explicit.stat_691932474@T1` | -0.75227 |

### flask.charm — n=6765, R²=-0.3467

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00004`  ·  corrupted: `0.24520`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.43448 |
| `explicit.stat_1056492907` | 2.99570 |
| `explicit.stat_2676834156@T1` | 0.71993 |
| `explicit.stat_2541588185@T1` | 0.47414 |
| `explicit.stat_3138344128` | 0.02133 |
| `explicit.stat_2678930256` | 0.01404 |
| `explicit.stat_3246948616` | 0.00004 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_1120862500@T2` | -0.00004 |
| `explicit.stat_2676834156@T2` | -0.00004 |
| `explicit.stat_828533480@T1` | -0.00003 |
| `explicit.stat_1873752457@T1` | -0.00003 |

### weapon.warstaff — n=4821, R²=-0.5585

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00638`  ·  n_sockets: `0.00001`  ·  quality: `0.00234`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 2.83284 |
| `rune.stat_731403740` | 1.50467 |
| `explicit.stat_9187492@T1` | 0.85534 |
| `rune.stat_1712188793` | -0.81500 |
| `desecrated.stat_9187492` | 0.65923 |
| `crafted.stat_210067635@T2` | -0.43295 |
| `desecrated.stat_518292764` | 0.38036 |
| `rune.stat_3336890334` | 0.12532 |
| `crafted.stat_3035140377` | 0.10812 |
| `rune.stat_1509134228` | 0.09105 |
| `desecrated.stat_669069897` | -0.08119 |
| `rune.stat_2430860292` | -0.06190 |

### weapon.staff — n=4496, R²=-0.5918

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00003`  ·  n_sockets: `0.00001`  ·  quality: `0.00792`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.48735 |
| `explicit.stat_4226189338@T1` | 2.30250 |
| `explicit.stat_1600707273@T1` | 1.60911 |
| `explicit.stat_2254480358@T1` | 0.83351 |
| `explicit.stat_473429811@T1` | 0.80849 |
| `explicit.stat_3962278098@T2` | 0.69178 |
| `explicit.stat_2254480358@T2` | 0.61911 |
| `crafted.stat_124131830` | 0.42961 |
| `explicit.stat_3291658075@T2` | 0.27292 |
| `rune.stat_3990135792` | -0.23112 |
| `rune.stat_975988108` | -0.13589 |
| `rune.stat_2974417149` | 0.11871 |

### weapon.sceptre — n=4483, R²=-0.5984

intercept: `-0.0196`  ·  log_price: True  ·  ilvl: `0.00024`  ·  n_mods: `-0.00008`  ·  n_top_tier: `0.28696`  ·  corrupted: `1.34240`  ·  n_sockets: `0.00057`  ·  quality: `0.08560`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.01512 |
| `explicit.stat_1798257884@T2` | 0.39808 |
| `explicit.stat_3984865854@T1` | 0.32756 |
| `explicit.stat_4080418644@T2` | -0.28771 |
| `explicit.stat_1263695895@T2` | -0.28755 |
| `explicit.stat_2347036682@T2` | -0.28753 |
| `explicit.stat_4080418644@T1` | -0.28748 |
| `explicit.stat_1250712710@T1` | -0.28725 |
| `explicit.stat_328541901@T1` | -0.28723 |
| `explicit.stat_3984865854@T2` | -0.28712 |
| `explicit.stat_1263695895@T1` | -0.28706 |
| `explicit.stat_2347036682@T1` | -0.28702 |

### weapon.spear — n=3869, R²=-0.5909

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00077`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.07958 |
| `crafted.stat_3035140377` | 1.70932 |
| `explicit.stat_210067635@T1` | 0.85872 |
| `crafted.stat_518292764` | 0.81813 |
| `explicit.stat_1509134228@T1` | 0.40694 |
| `rune.stat_1039491398` | 0.08228 |
| `crafted.stat_210067635` | 0.08172 |
| `desecrated.stat_1509134228` | 0.01069 |
| `rune.stat_1509134228` | 0.00263 |
| `explicit.stat_709508406@T1` | 0.00130 |
| `desecrated.stat_691932474` | -0.00070 |
| `explicit.stat_1940865751@T1` | 0.00032 |

### armour.focus — n=3132, R²=-0.6395

intercept: `-0.0032`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.30731`  ·  corrupted: `0.00006`  ·  n_sockets: `0.00009`  ·  quality: `0.02926`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -5.86829 |
| `crafted.stat_737908626@T2` | -4.77876 |
| `desecrated.stat_378817135@T1` | -1.27961 |
| `desecrated.stat_3393628375` | 0.42178 |
| `crafted.stat_2974417149@T1` | -0.37628 |
| `explicit.stat_789117908@T2` | -0.30743 |
| `explicit.stat_3291658075@T1` | -0.30741 |
| `explicit.stat_736967255@T2` | -0.30740 |
| `explicit.stat_274716455@T1` | -0.30740 |
| `explicit.stat_274716455@T2` | -0.30738 |
| `explicit.stat_2923486259@T1` | -0.30737 |
| `explicit.stat_4052037485@T2` | -0.30737 |

### armour.quiver — n=2957, R²=-0.6497

intercept: `-0.0060`  ·  log_price: True  ·  ilvl: `0.00007`  ·  n_mods: `0.00002`  ·  n_top_tier: `0.54245`  ·  corrupted: `0.00046`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.47446 |
| `explicit.stat_2463230181@T1` | 0.75067 |
| `explicit.stat_681332047@T2` | -0.54318 |
| `explicit.stat_681332047@T1` | -0.54312 |
| `explicit.stat_1573130764@T1` | -0.54279 |
| `explicit.stat_2194114101@T2` | -0.54268 |
| `explicit.stat_1368271171@T2` | -0.54263 |
| `explicit.stat_1573130764@T2` | -0.54262 |
| `explicit.stat_2321178454@T2` | -0.54262 |
| `explicit.stat_3714003708@T2` | -0.54253 |
| `explicit.stat_803737631@T2` | -0.54250 |
| `explicit.stat_3261801346@T1` | -0.54244 |

### armour.shield — n=2551, R²=-0.5039

intercept: `-0.0008`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.28816`  ·  corrupted: `0.06491`  ·  n_sockets: `0.00001`  ·  quality: `0.06904`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.77941 |
| `explicit.stat_1978899297@T2` | -0.44752 |
| `explicit.stat_1011760251@T1` | -0.29788 |
| `explicit.stat_1011760251@T2` | -0.29463 |
| `explicit.stat_328541901@T1` | -0.28823 |
| `explicit.stat_328541901@T2` | -0.28821 |
| `explicit.stat_2481353198@T1` | -0.28821 |
| `explicit.stat_2339757871@T1` | -0.28821 |
| `explicit.stat_3484657501@T1` | -0.28819 |
| `explicit.stat_2481353198@T2` | -0.28819 |
| `explicit.stat_3372524247@T2` | -0.28819 |
| `explicit.stat_2901986750@T1` | -0.28819 |

### weapon.twomace — n=2232, R²=-0.5518

intercept: `-0.0010`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00869`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.27367 |
| `crafted.stat_3035140377` | 1.39448 |
| `explicit.stat_1509134228@T1` | 0.60282 |
| `desecrated.stat_1509134228@T1` | -0.33845 |
| `explicit.stat_387439868@T1` | 0.19497 |
| `desecrated.stat_210067635` | 0.15134 |
| `crafted.stat_210067635` | 0.13874 |
| `rune.stat_1039491398` | 0.12470 |
| `explicit.stat_1368271171@T2` | 0.12242 |
| `desecrated.stat_1940865751` | -0.08990 |
| `crafted.stat_1940865751` | 0.05979 |
| `rune.stat_1509134228` | -0.04503 |

## Coverage (listings per base)

- … **Sapphire** — 13530 listings (13513 priced) [0.3–7553463.8 ex]
- … **Emerald** — 13387 listings (13379 priced) [0.4–7553463.8 ex]
- … **Ruby** — 10341 listings (10331 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 6243 listings (6239 priced) [0.3–5288620.9 ex]
- … **Prismatic Ring** — 4760 listings (4758 priced) [0.3–24532814.5 ex]
- … **Stellar Amulet** — 4714 listings (4714 priced) [0.3–35690283.3 ex]
- … **Solar Amulet** — 4650 listings (4642 priced) [1.0–66666666.0 ex]
- … **Amethyst Ring** — 4558 listings (4557 priced) [0.3–71450.3 ex]
- … **Gold Amulet** — 4456 listings (4451 priced) [0.2–4894457.0 ex]
- … **Gold Ring** — 4320 listings (4318 priced) [0.3–24532814.5 ex]
- … **Dueling Wand** — 4068 listings (4063 priced) [0.3–3736768402.2 ex]
- … **Sapphire Ring** — 3618 listings (3614 priced) [0.3–24532814.5 ex]
- … **Ruby Ring** — 3513 listings (3513 priced) [0.3–37474957.5 ex]
- … **Topaz Ring** — 3493 listings (3492 priced) [0.3–123132003.2 ex]
- … **Plate Belt** — 3188 listings (3185 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 3131 listings (3130 priced) [0.3–5286174.1 ex]
- … **Ancestral Tiara** — 3125 listings (3122 priced) [0.6–41469259.3 ex]
- … **Obliterator Bow** — 3097 listings (3090 priced) [0.4–22139622146.9 ex]
- … **Amber Amulet** — 3075 listings (3074 priced) [0.2–124352753.2 ex]
- … **Jade Amulet** — 3072 listings (3071 priced) [0.2–4547453.5 ex]
- … **Heavy Belt** — 2988 listings (2988 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 2917 listings (2917 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 2875 listings (2875 priced) [0.3–329628.5 ex]
- … **Pearl Ring** — 2800 listings (2800 priced) [0.3–24532814.5 ex]
- … **Azure Amulet** — 2745 listings (2745 priced) [0.3–123132003.2 ex]

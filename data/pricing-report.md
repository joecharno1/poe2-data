# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-07T05:48:38+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **261863** (261600 priced in exalted)
- Distinct bases: 940 · distinct mods: 2690 · mod rows: 1243959
- Sold signals: **33180** sold · 136708 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-07T05:34:46+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×15.23** (median |log error| 2.7235)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 77% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.04** · typical error ×35.47 · ±30% 11% · n=37385
- Premium segment (60ex+): skill **+0.05** · typical error ×181.04 · ±30% 0% · n=22847

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 4838 | ×13.11 | 4% | +0.03 | +0.05 |
| accessory.amulet | 4660 | ×53.93 | 20% | +0.02 | +0.02 |
| jewel | 4152 | ×8.86 | 6% | +0.03 | +0.05 |
| accessory.belt | 3867 | ×10.00 | 19% | +0.02 | +0.02 |
| armour.chest | 3822 | ×9.85 | 23% | +0.00 | +0.01 |
| armour.helmet | 3695 | ×9.99 | 24% | -0.00 | +0.01 |
| armour.boots | 3535 | ×10.99 | 7% | +0.02 | +0.06 |
| armour.gloves | 3441 | ×14.47 | 5% | +0.03 | +0.06 |
| other | 3143 | ×9.97 | 37% | +0.05 | +0.16 |
| weapon.wand | 2398 | ×21.28 | 23% | +0.05 | +0.06 |
| weapon.bow | 1991 | ×13.79 | 21% | +0.09 | +0.09 |
| weapon.crossbow | 1881 | ×14.29 | 18% | +0.08 | +0.10 |
| weapon.warstaff | 756 | ×55.00 | 25% | +0.01 | +0.01 |
| weapon.sceptre | 729 | ×63.00 | 19% | +0.01 | +0.02 |
| weapon.staff | 686 | ×50.00 | 24% | +0.03 | +0.01 |
| weapon.spear | 626 | ×50.00 | 22% | +0.01 | +0.00 |
| armour.quiver | 489 | ×70.00 | 16% | +0.00 | +0.02 |
| armour.focus | 484 | ×55.00 | 16% | +0.01 | +0.02 |
| armour.shield | 435 | ×20.00 | 22% | +0.01 | +0.01 |
| flask.charm | 379 | ×1.00 | 57% | -0.00 | +0.00 |
| weapon.twomace | 365 | ×20.00 | 24% | +0.08 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=28149, R²=-0.5103

intercept: `1.6053`  ·  log_price: True  ·  ilvl: `0.00005`  ·  n_mods: `0.03211`  ·  n_top_tier: `0.42188`  ·  corrupted: `1.36933`  ·  n_sockets: `-0.00010`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_2891184298@T1` | 1.94513 |
| `explicit.stat_3291658075@T1` | 1.93678 |
| `explicit.stat_3141070085@T1` | -1.74074 |
| `explicit.stat_2106365538@T1` | 1.58952 |
| `explicit.stat_101878827@T1` | 1.27956 |
| `explicit.stat_2974417149@T1` | 0.94855 |
| `explicit.stat_3917489142@T1` | 0.77846 |
| `explicit.stat_1050105434@T1` | -0.64825 |
| `explicit.stat_1589917703@T1` | 0.54343 |
| `explicit.stat_3141070085` | 0.30738 |
| `implicit.stat_1379411836` | -0.27343 |
| `explicit.stat_789117908@T1` | -0.26042 |

### accessory.ring — n=22398, R²=-1.2553

intercept: `4.7257`  ·  log_price: True  ·  ilvl: `-0.04235`  ·  n_mods: `-0.15236`  ·  n_top_tier: `0.01369`  ·  corrupted: `0.76137`  ·  n_sockets: `0.48134`  ·  quality: `0.05505`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.94029 |
| `explicit.stat_707457662@T2` | 3.62077 |
| `explicit.stat_1379411836@T1` | -2.25193 |
| `explicit.stat_1379411836@T2` | -1.92694 |
| `explicit.stat_1368271171@T2` | -1.14048 |
| `explicit.stat_2923486259@T2` | 0.95159 |
| `explicit.stat_1368271171@T1` | -0.88268 |
| `explicit.stat_1573130764@T1` | -0.71851 |
| `explicit.stat_736967255@T1` | 0.70668 |
| `explicit.stat_707457662` | -0.69706 |
| `explicit.stat_4080418644@T2` | 0.64465 |
| `explicit.stat_2557965901@T1` | -0.56640 |

### jewel — n=22382, R²=-0.6323

intercept: `-1.0542`  ·  log_price: True  ·  ilvl: `0.03724`  ·  n_mods: `0.09440`  ·  n_top_tier: `-0.00018`  ·  corrupted: `0.32062`  ·  quality: `0.21253`

| stat_id | coef |
|---|---|
| `explicit.stat_3714003708@T1` | -4.06213 |
| `explicit.stat_1869147066@T1` | 3.49171 |
| `explicit.stat_3192728503@T1` | -3.23751 |
| `explicit.stat_1316278494@T1` | -3.21495 |
| `explicit.stat_1697951953@T1` | -3.19319 |
| `explicit.stat_1854213750@T1` | -3.05253 |
| `explicit.stat_1569101201@T1` | 3.02354 |
| `explicit.stat_21071013@T1` | -2.65633 |
| `explicit.stat_153777645@T1` | 2.11841 |
| `explicit.stat_1569159338@T1` | 1.98397 |
| `explicit.stat_234296660@T1` | -1.97454 |
| `explicit.stat_1405298142@T1` | 1.90479 |

### accessory.amulet — n=21386, R²=-2.0902

intercept: `4.1900`  ·  log_price: True  ·  ilvl: `-0.05087`  ·  n_mods: `-0.02104`  ·  n_top_tier: `1.14251`  ·  corrupted: `0.12870`  ·  n_sockets: `2.21980`  ·  quality: `-0.00523`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | -2.52093 |
| `explicit.stat_983749596@T1` | -1.56547 |
| `explicit.stat_3299347043@T1` | -1.52016 |
| `explicit.stat_983749596@T2` | -1.50601 |
| `explicit.stat_2748665614@T1` | -1.30860 |
| `explicit.stat_2748665614@T2` | -1.29158 |
| `explicit.stat_3299347043@T2` | -1.24818 |
| `explicit.stat_3325883026@T1` | -1.24817 |
| `explicit.stat_3917489142@T2` | -1.23703 |
| `explicit.stat_3917489142@T1` | -1.23443 |
| `explicit.stat_3489782002@T2` | -1.22173 |
| `explicit.stat_587431675@T1` | -1.21483 |

### accessory.belt — n=17855, R²=-0.1377

intercept: `2.3076`  ·  log_price: True  ·  ilvl: `-0.00005`  ·  n_mods: `-0.00064`  ·  n_top_tier: `0.40491`  ·  corrupted: `0.00066`  ·  n_sockets: `-2.12508`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.96768 |
| `explicit.stat_3325883026@T1` | -0.40598 |
| `explicit.stat_1389754388@T1` | -0.40572 |
| `explicit.stat_915769802@T2` | -0.40550 |
| `explicit.stat_51994685@T1` | -0.40549 |
| `explicit.stat_915769802@T1` | -0.40538 |
| `explicit.stat_644456512@T1` | -0.40533 |
| `explicit.stat_644456512@T2` | -0.40527 |
| `explicit.stat_2881298780@T1` | -0.40521 |
| `explicit.stat_1389754388@T2` | -0.40519 |
| `explicit.stat_2923486259@T2` | -0.40517 |
| `explicit.stat_3299347043@T1` | -0.40510 |

### armour.chest — n=17660, R²=-0.2657

intercept: `2.4315`  ·  log_price: True  ·  ilvl: `-0.00244`  ·  n_mods: `-0.01593`  ·  n_top_tier: `0.05951`  ·  corrupted: `0.02720`  ·  n_sockets: `-0.00100`  ·  quality: `0.00084`

| stat_id | coef |
|---|---|
| `implicit.stat_1978899297` | -1.45512 |
| `explicit.stat_4080418644@T2` | -0.09910 |
| `explicit.stat_915769802@T1` | -0.09450 |
| `implicit.stat_2251279027` | 0.08751 |
| `explicit.stat_915769802@T2` | -0.07982 |
| `explicit.stat_3261801346@T1` | -0.07822 |
| `explicit.stat_3261801346@T2` | -0.07439 |
| `explicit.stat_4015621042@T1` | -0.07314 |
| `explicit.stat_3033371881@T2` | -0.07152 |
| `explicit.stat_2451402625@T1` | -0.07138 |
| `explicit.stat_986397080@T2` | -0.07093 |
| `explicit.stat_3484657501@T1` | -0.06978 |

### armour.helmet — n=17289, R²=-0.2757

intercept: `2.3394`  ·  log_price: True  ·  ilvl: `-0.00076`  ·  n_mods: `-0.00444`  ·  n_top_tier: `0.11078`  ·  corrupted: `0.13660`  ·  n_sockets: `-0.00061`  ·  quality: `0.00073`

| stat_id | coef |
|---|---|
| `explicit.stat_1062208444@T2` | -0.37126 |
| `explicit.stat_4080418644@T2` | -0.26853 |
| `explicit.stat_53045048@T2` | -0.11698 |
| `explicit.stat_53045048@T1` | -0.11623 |
| `explicit.stat_328541901@T2` | -0.11543 |
| `explicit.stat_1263695895@T2` | -0.11520 |
| `explicit.stat_803737631@T2` | -0.11406 |
| `explicit.stat_3484657501@T2` | -0.11393 |
| `explicit.stat_1263695895@T1` | -0.11227 |
| `explicit.stat_2451402625@T1` | -0.11216 |
| `explicit.stat_1050105434@T1` | -0.11216 |
| `explicit.stat_3362812763@T1` | -0.11198 |

### armour.boots — n=16260, R²=-0.7061

intercept: `4.2621`  ·  log_price: True  ·  ilvl: `-0.04879`  ·  n_mods: `-0.15641`  ·  n_top_tier: `0.54577`  ·  corrupted: `0.46889`  ·  n_sockets: `0.22434`  ·  quality: `0.00854`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | -2.01712 |
| `explicit.stat_2339757871@T1` | -1.14654 |
| `explicit.stat_2250533757@T1` | 1.08665 |
| `explicit.stat_1062208444@T2` | -1.07982 |
| `explicit.stat_3362812763@T1` | -1.05209 |
| `explicit.stat_328541901@T1` | -0.96164 |
| `explicit.stat_2923486259@T2` | -0.95333 |
| `explicit.stat_3321629045@T1` | -0.81906 |
| `explicit.stat_99927264@T1` | -0.81251 |
| `explicit.stat_2160282525@T1` | -0.78842 |
| `explicit.stat_1062208444@T1` | -0.78805 |
| `explicit.stat_3033371881@T2` | -0.78523 |

### armour.gloves — n=15977, R²=-0.8473

intercept: `3.4070`  ·  log_price: True  ·  ilvl: `-0.04683`  ·  n_mods: `-0.07370`  ·  n_top_tier: `0.40351`  ·  corrupted: `0.22413`  ·  n_sockets: `0.34718`  ·  quality: `0.00425`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -6.40747 |
| `explicit.stat_803737631@T1` | -1.04196 |
| `explicit.stat_681332047@T2` | -1.01747 |
| `explicit.stat_803737631@T2` | -0.95524 |
| `explicit.stat_3484657501@T2` | -0.83041 |
| `explicit.stat_328541901@T1` | -0.83027 |
| `explicit.stat_2797971005@T2` | -0.79288 |
| `explicit.stat_2797971005@T1` | -0.78667 |
| `explicit.stat_3033371881@T2` | -0.76852 |
| `explicit.stat_124859000@T1` | -0.67339 |
| `explicit.stat_3032590688@T1` | -0.66959 |
| `explicit.stat_1671376347@T2` | -0.63037 |

### weapon.wand — n=11207, R²=-2.0133

intercept: `3.4117`  ·  log_price: True  ·  ilvl: `-0.04259`  ·  n_mods: `-0.00443`  ·  n_top_tier: `0.17647`  ·  corrupted: `0.06552`  ·  n_sockets: `0.00028`  ·  quality: `0.01600`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.26151 |
| `explicit.stat_124131830@T1` | 2.24327 |
| `explicit.stat_591105508@T1` | 2.20972 |
| `explicit.stat_4226189338@T1` | 2.19997 |
| `explicit.stat_1600707273@T1` | 1.98509 |
| `explicit.stat_736967255@T2` | 1.33515 |
| `explicit.stat_1600707273@T2` | 0.85163 |
| `crafted.stat_124131830` | 0.78921 |
| `explicit.stat_1545858329@T1` | 0.71156 |
| `rune.stat_3278136794` | 0.33354 |
| `explicit.stat_737908626@T1` | -0.23474 |
| `explicit.stat_737908626@T2` | -0.20375 |

### weapon.bow — n=9181, R²=-1.8631

intercept: `3.4452`  ·  log_price: True  ·  ilvl: `-0.04265`  ·  n_mods: `-0.00979`  ·  n_top_tier: `0.46526`  ·  corrupted: `-0.02343`  ·  n_sockets: `0.00476`  ·  quality: `0.00605`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | 1.79914 |
| `explicit.stat_1202301673@T1` | 1.74844 |
| `desecrated.stat_210067635@T1` | -1.65236 |
| `explicit.stat_518292764@T1` | 1.16139 |
| `crafted.stat_3035140377` | 1.14481 |
| `desecrated.stat_666077204@T1` | -0.61089 |
| `explicit.stat_55876295@T1` | -0.51466 |
| `explicit.stat_2694482655@T1` | -0.50832 |
| `explicit.stat_669069897@T2` | -0.50819 |
| `explicit.stat_3261801346@T1` | -0.50132 |
| `explicit.stat_55876295@T2` | -0.49616 |
| `explicit.stat_3695891184@T2` | -0.49525 |

### weapon.crossbow — n=8694, R²=-1.6968

intercept: `3.5578`  ·  log_price: True  ·  ilvl: `-0.04439`  ·  n_mods: `-0.00416`  ·  n_top_tier: `0.56188`  ·  corrupted: `-0.04915`  ·  n_sockets: `0.01748`  ·  quality: `0.00566`

| stat_id | coef |
|---|---|
| `explicit.stat_709508406@T1` | 1.62510 |
| `explicit.stat_1202301673@T1` | 1.60071 |
| `explicit.stat_1037193709@T1` | 1.58207 |
| `explicit.stat_2250681686@T2` | -1.44897 |
| `rune.stat_55876295` | 1.22222 |
| `explicit.stat_1509134228@T1` | 1.21260 |
| `crafted.stat_3035140377` | 1.10725 |
| `rune.stat_2246411426` | -1.10622 |
| `explicit.stat_2250681686` | 0.92673 |
| `explicit.stat_1202301673@T2` | -0.66798 |
| `explicit.stat_691932474@T1` | -0.64926 |
| `explicit.stat_669069897@T1` | -0.63761 |

### flask.charm — n=4999, R²=-0.2158

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00004`  ·  corrupted: `0.00006`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.04302 |
| `explicit.stat_1056492907` | 2.99569 |
| `explicit.stat_3138344128` | 0.02219 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_828533480@T1` | -0.00004 |
| `explicit.stat_828533480@T2` | -0.00004 |
| `explicit.stat_1873752457@T1` | -0.00004 |
| `explicit.stat_388617051@T2` | -0.00004 |
| `explicit.stat_3196823591@T2` | -0.00004 |
| `explicit.stat_2541588185@T2` | -0.00004 |
| `explicit.stat_2676834156@T2` | -0.00003 |
| `explicit.stat_2365392475@T2` | -0.00003 |

### weapon.warstaff — n=3649, R²=-0.4556

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | -3.96551 |
| `desecrated.stat_2231156303@T1` | -3.96551 |
| `rune.stat_243313994` | 3.28915 |
| `rune.stat_731403740` | 1.61197 |
| `rune.stat_1712188793` | -1.10427 |
| `desecrated.stat_9187492` | 0.74931 |
| `desecrated.stat_2527686725` | 0.26651 |
| `rune.stat_3336890334` | 0.22572 |
| `rune.stat_2430860292` | -0.11657 |
| `crafted.stat_210067635@T2` | 0.06706 |
| `desecrated.stat_2231156303` | 0.04574 |
| `rune.stat_1509134228` | 0.03695 |

### weapon.sceptre — n=3457, R²=-0.4166

intercept: `-0.0008`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.73714`  ·  n_sockets: `0.00002`  ·  quality: `0.04595`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.25580 |
| `rune.stat_1611856026` | 0.07147 |
| `rune.stat_3984865854` | 0.05661 |
| `rune.stat_3412619569` | 0.02878 |
| `rune.stat_1798257884` | 0.02878 |
| `desecrated.stat_1050105434` | 0.00330 |
| `explicit.stat_1798257884@T2` | 0.00020 |
| `explicit.stat_1263695895@T1` | 0.00007 |
| `explicit.stat_2162097452@T2` | 0.00005 |
| `explicit.stat_3057012405@T1` | 0.00004 |
| `explicit.stat_4010677958@T1` | 0.00003 |
| `explicit.stat_1263695895@T2` | 0.00003 |

### weapon.staff — n=3430, R²=-0.4699

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.64578 |
| `rune.stat_3990135792` | -0.21730 |
| `rune.stat_2974417149` | 0.11002 |
| `rune.stat_975988108` | -0.10511 |
| `crafted.stat_124131830` | 0.06475 |
| `explicit.stat_2254480358@T1` | 0.04678 |
| `explicit.stat_473429811@T1` | 0.00026 |
| `explicit.stat_124131830@T1` | 0.00007 |
| `explicit.stat_1600707273@T1` | 0.00005 |
| `explicit.stat_124131830@T2` | 0.00004 |
| `explicit.stat_3962278098@T2` | 0.00003 |
| `explicit.stat_2891184298@T2` | 0.00002 |

### weapon.spear — n=3008, R²=-0.4936

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `rune.stat_1039491398` | 0.21608 |
| `rune.stat_1509134228` | -0.20584 |
| `explicit.stat_210067635@T1` | 0.10161 |
| `explicit.stat_709508406@T1` | 0.00012 |
| `explicit.stat_2694482655@T1` | 0.00003 |
| `explicit.stat_3639275092@T1` | 0.00003 |
| `explicit.stat_1263695895@T2` | -0.00003 |
| `explicit.stat_1509134228@T1` | 0.00002 |
| `explicit.stat_3639275092@T2` | 0.00002 |
| `explicit.stat_3336890334@T2` | 0.00002 |
| `explicit.stat_4080418644@T1` | -0.00002 |
| `explicit.stat_210067635@T2` | 0.00002 |

### armour.focus — n=2383, R²=-0.3682

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00021`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.51112 |
| `crafted.stat_737908626@T2` | -2.81287 |
| `crafted.stat_2974417149@T1` | 1.16268 |
| `desecrated.stat_2910761524@T1` | 0.91662 |
| `desecrated.stat_3393628375` | 0.53650 |
| `desecrated.stat_378817135@T1` | 0.37350 |
| `pseudo.total_chaos_res` | 0.14708 |
| `explicit.stat_2923486259` | -0.14708 |
| `crafted.stat_737908626` | 0.11172 |
| `desecrated.stat_2910761524` | -0.10785 |
| `crafted.stat_4015621042` | 0.06670 |
| `rune.stat_3523867985` | 0.03469 |

### armour.quiver — n=2300, R²=-0.5011

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00010`  ·  corrupted: `0.00003`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 0.23444 |
| `desecrated.stat_2194114101` | 0.18441 |
| `desecrated.stat_3714003708` | 0.06224 |
| `desecrated.stat_3932115504` | -0.01951 |
| `explicit.stat_3759663284@T1` | 0.01669 |
| `desecrated.stat_3759663284` | 0.01629 |
| `desecrated.stat_1241625305` | 0.00031 |
| `explicit.stat_2463230181@T1` | -0.00015 |
| `explicit.stat_681332047@T2` | -0.00012 |
| `explicit.stat_2321178454@T2` | -0.00011 |
| `explicit.stat_2463230181@T2` | -0.00011 |
| `explicit.stat_681332047@T1` | -0.00011 |

### armour.shield — n=2041, R²=-0.4416

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.15146`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00037`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.86587 |
| `explicit.stat_1301765461@T1` | 0.54154 |
| `explicit.stat_1978899297@T2` | -0.33642 |
| `explicit.stat_1978899297` | 0.18494 |
| `explicit.stat_1011760251@T1` | -0.15156 |
| `explicit.stat_1011760251@T2` | -0.15152 |
| `explicit.stat_2481353198@T1` | -0.15151 |
| `explicit.stat_2481353198@T2` | -0.15149 |
| `explicit.stat_3484657501@T1` | -0.15149 |
| `explicit.stat_328541901@T1` | -0.15148 |
| `explicit.stat_3639275092@T1` | -0.15148 |
| `explicit.stat_2923486259@T2` | -0.15148 |

### weapon.twomace — n=1753, R²=-0.3923

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00006`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_518292764@T1` | 1.67973 |
| `explicit.stat_1509134228@T1` | 1.60931 |
| `desecrated.stat_210067635` | 0.19970 |
| `rune.stat_1039491398` | 0.13248 |
| `rune.stat_1509134228` | -0.04784 |
| `rune.stat_3336890334` | 0.01772 |
| `desecrated.stat_691932474` | 0.01037 |
| `rune.stat_2430860292` | 0.00915 |
| `explicit.stat_3336890334@T1` | -0.00011 |
| `explicit.stat_1037193709@T1` | -0.00011 |
| `explicit.stat_1037193709@T2` | -0.00009 |
| `explicit.stat_387439868@T2` | -0.00009 |

## Coverage (listings per base)

- … **Emerald** — 10783 listings (10775 priced) [0.6–7553463.8 ex]
- … **Sapphire** — 10704 listings (10691 priced) [0.3–7553463.8 ex]
- … **Ruby** — 8335 listings (8325 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 5329 listings (5325 priced) [0.3–4877938.3 ex]
- … **Stellar Amulet** — 4010 listings (4010 priced) [0.3–35690283.3 ex]
- … **Prismatic Ring** — 3925 listings (3924 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 3838 listings (3833 priced) [0.3–66666666.0 ex]
- … **Amethyst Ring** — 3738 listings (3737 priced) [0.3–71450.3 ex]
- … **Gold Amulet** — 3685 listings (3685 priced) [0.3–292542.5 ex]
- … **Gold Ring** — 3573 listings (3572 priced) [0.3–24532814.5 ex]
- … **Dueling Wand** — 3503 listings (3499 priced) [0.7–3736768402.2 ex]
- … **Sapphire Ring** — 2962 listings (2961 priced) [0.3–24532814.5 ex]
- … **Topaz Ring** — 2899 listings (2898 priced) [1.0–24532814.5 ex]
- … **Ruby Ring** — 2873 listings (2873 priced) [0.3–146119.1 ex]
- … **Plate Belt** — 2704 listings (2702 priced) [0.3–4877938.3 ex]
- … **Obliterator Bow** — 2652 listings (2646 priced) [0.4–22139622146.9 ex]
- … **Lapis Amulet** — 2594 listings (2594 priced) [0.3–4547453.5 ex]
- … **Ancestral Tiara** — 2574 listings (2572 priced) [0.6–5125681.0 ex]
- … **Amber Amulet** — 2566 listings (2565 priced) [0.3–4547453.5 ex]
- … **Heavy Belt** — 2552 listings (2552 priced) [0.3–4877938.3 ex]
- … **Jade Amulet** — 2539 listings (2538 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 2387 listings (2387 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 2368 listings (2368 priced) [0.3–14638.0 ex]
- … **Pearl Ring** — 2329 listings (2329 priced) [0.3–24532814.5 ex]
- … **Azure Amulet** — 2287 listings (2287 priced) [0.3–4877938.3 ex]

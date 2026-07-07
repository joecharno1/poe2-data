# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-07T11:53:56+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **275021** (274719 priced in exalted)
- Distinct bases: 944 · distinct mods: 2729 · mod rows: 1306752
- Sold signals: **32489** sold · 145391 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-07T11:44:50+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×15.13** (median |log error| 2.7164)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 76% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×35.88 · ±30% 13% · n=39227
- Premium segment (60ex+): skill **+0.06** · typical error ×159.16 · ±30% 0% · n=24141

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 5138 | ×11.88 | 4% | +0.04 | +0.05 |
| accessory.amulet | 4928 | ×53.06 | 20% | +0.02 | +0.02 |
| jewel | 4465 | ×8.43 | 7% | +0.01 | +0.03 |
| accessory.belt | 4038 | ×10.00 | 20% | +0.04 | +0.04 |
| armour.chest | 3969 | ×10.00 | 24% | +0.01 | +0.01 |
| armour.helmet | 3879 | ×10.00 | 23% | +0.00 | +0.00 |
| armour.boots | 3667 | ×10.00 | 23% | +0.00 | +0.02 |
| armour.gloves | 3625 | ×11.06 | 9% | +0.01 | +0.02 |
| other | 3276 | ×9.73 | 38% | +0.06 | +0.15 |
| weapon.wand | 2537 | ×22.55 | 22% | +0.06 | +0.06 |
| weapon.bow | 2000 | ×18.13 | 19% | +0.10 | +0.11 |
| weapon.crossbow | 1866 | ×11.43 | 20% | +0.08 | +0.10 |
| weapon.warstaff | 849 | ×77.56 | 19% | +0.01 | +0.01 |
| weapon.sceptre | 746 | ×75.00 | 16% | +0.02 | +0.03 |
| weapon.staff | 737 | ×55.00 | 21% | +0.03 | +0.03 |
| weapon.spear | 618 | ×58.00 | 23% | +0.00 | +0.00 |
| armour.focus | 523 | ×58.00 | 14% | +0.01 | +0.02 |
| armour.quiver | 519 | ×79.85 | 18% | +0.00 | +0.04 |
| armour.shield | 422 | ×30.00 | 19% | +0.02 | +0.03 |
| flask.charm | 382 | ×3.00 | 47% | -0.00 | +0.01 |
| weapon.twomace | 376 | ×27.64 | 22% | +0.08 | +0.02 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=29276, R²=-0.5501

intercept: `1.6035`  ·  log_price: True  ·  ilvl: `0.00008`  ·  n_mods: `0.03051`  ·  n_top_tier: `0.36653`  ·  corrupted: `1.39850`  ·  n_sockets: `-0.00014`  ·  quality: `-0.00002`

| stat_id | coef |
|---|---|
| `explicit.stat_2891184298@T1` | 1.85851 |
| `explicit.stat_3291658075@T1` | 1.35655 |
| `explicit.stat_2974417149@T1` | 0.95426 |
| `explicit.stat_2106365538@T1` | 0.77977 |
| `explicit.stat_3917489142@T1` | 0.69865 |
| `explicit.stat_1050105434@T1` | -0.55508 |
| `explicit.stat_1589917703@T1` | -0.43080 |
| `explicit.stat_101878827@T1` | 0.29592 |
| `explicit.stat_2968503605@T1` | 0.28821 |
| `implicit.stat_1379411836` | -0.27305 |
| `implicit.stat_4041853756` | 0.22719 |
| `implicit.stat_3879011313` | 0.22719 |

### jewel — n=23884, R²=-0.6591

intercept: `-1.0201`  ·  log_price: True  ·  ilvl: `0.03541`  ·  n_mods: `0.12295`  ·  n_top_tier: `-0.00052`  ·  corrupted: `0.37165`  ·  quality: `0.21418`

| stat_id | coef |
|---|---|
| `explicit.stat_1569101201@T1` | 3.64526 |
| `explicit.stat_3714003708@T1` | -3.42768 |
| `explicit.stat_3192728503@T1` | -3.40524 |
| `explicit.stat_1316278494@T1` | -3.08722 |
| `explicit.stat_1697951953@T1` | -3.04337 |
| `explicit.stat_21071013@T1` | -2.66224 |
| `explicit.stat_1594812856@T1` | -2.61894 |
| `explicit.stat_3668351662@T1` | -2.57519 |
| `explicit.stat_153777645@T1` | 2.51050 |
| `explicit.stat_1854213750@T1` | -2.34193 |
| `explicit.stat_1869147066@T1` | 2.29951 |
| `explicit.stat_2527686725@T1` | 2.15303 |

### accessory.ring — n=23661, R²=-1.2592

intercept: `4.6898`  ·  log_price: True  ·  ilvl: `-0.04341`  ·  n_mods: `-0.15080`  ·  n_top_tier: `-0.02545`  ·  corrupted: `0.73942`  ·  n_sockets: `-1.49112`  ·  quality: `0.03707`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.13310 |
| `explicit.stat_707457662@T2` | 2.95489 |
| `explicit.stat_1379411836@T1` | -2.30822 |
| `explicit.stat_1379411836@T2` | -1.90914 |
| `explicit.stat_1368271171@T2` | -1.04943 |
| `explicit.stat_2923486259@T2` | 0.85195 |
| `explicit.stat_1368271171@T1` | -0.84503 |
| `explicit.stat_3299347043@T1` | -0.73854 |
| `explicit.stat_736967255@T1` | 0.71916 |
| `explicit.stat_4080418644@T2` | 0.68575 |
| `explicit.stat_707457662` | -0.55378 |
| `explicit.stat_328541901@T1` | 0.52959 |

### accessory.amulet — n=22555, R²=-2.1097

intercept: `4.3145`  ·  log_price: True  ·  ilvl: `-0.05215`  ·  n_mods: `-0.02998`  ·  n_top_tier: `1.15937`  ·  corrupted: `0.12743`  ·  n_sockets: `1.69613`  ·  quality: `-0.00725`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | -2.67638 |
| `explicit.stat_3299347043@T1` | -1.30320 |
| `explicit.stat_2748665614@T1` | -1.29011 |
| `explicit.stat_3325883026@T1` | -1.27860 |
| `explicit.stat_983749596@T2` | -1.27758 |
| `explicit.stat_983749596@T1` | -1.26987 |
| `explicit.stat_2748665614@T2` | -1.26103 |
| `explicit.stat_3917489142@T2` | -1.25863 |
| `explicit.stat_3489782002@T2` | -1.23838 |
| `explicit.stat_3917489142@T1` | -1.23824 |
| `explicit.stat_3325883026@T2` | -1.21496 |
| `explicit.stat_1671376347@T2` | -1.20889 |

### accessory.belt — n=18702, R²=-0.1081

intercept: `2.3029`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.17362`  ·  corrupted: `0.00005`  ·  n_sockets: `-0.00005`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -0.17366 |
| `explicit.stat_51994685@T1` | -0.17365 |
| `explicit.stat_2923486259@T2` | -0.17365 |
| `explicit.stat_644456512@T1` | -0.17365 |
| `explicit.stat_1570770415@T1` | -0.17364 |
| `explicit.stat_644456512@T2` | -0.17363 |
| `explicit.stat_1389754388@T2` | -0.17363 |
| `explicit.stat_915769802@T1` | -0.17363 |
| `explicit.stat_3325883026@T1` | -0.17363 |
| `explicit.stat_3299347043@T2` | -0.17362 |
| `explicit.stat_51994685@T2` | -0.17362 |
| `explicit.stat_2923486259@T1` | -0.17362 |

### armour.chest — n=18478, R²=-0.2445

intercept: `2.3032`  ·  log_price: True  ·  ilvl: `-0.00001`  ·  n_mods: `-0.00008`  ·  n_top_tier: `0.05525`  ·  corrupted: `0.00026`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_1978899297` | -0.69318 |
| `explicit.stat_915769802@T1` | -0.05538 |
| `explicit.stat_3261801346@T1` | -0.05538 |
| `explicit.stat_915769802@T2` | -0.05537 |
| `explicit.stat_4080418644@T2` | -0.05534 |
| `explicit.stat_3484657501@T1` | -0.05532 |
| `explicit.stat_2923486259@T1` | -0.05530 |
| `explicit.stat_1692879867@T1` | -0.05529 |
| `explicit.stat_3033371881@T2` | -0.05529 |
| `explicit.stat_986397080@T2` | -0.05529 |
| `explicit.stat_3372524247@T2` | -0.05529 |
| `explicit.stat_124859000@T2` | -0.05529 |

### armour.helmet — n=18102, R²=-0.2469

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.24475`  ·  corrupted: `1.10036`  ·  n_sockets: `-0.00000`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 1.17554 |
| `explicit.stat_4080418644@T2` | -0.24479 |
| `explicit.stat_1062208444@T2` | -0.24478 |
| `explicit.stat_3362812763@T2` | -0.24478 |
| `explicit.stat_53045048@T2` | -0.24477 |
| `explicit.stat_3362812763@T1` | -0.24477 |
| `explicit.stat_2451402625@T1` | -0.24477 |
| `explicit.stat_2451402625@T2` | -0.24477 |
| `explicit.stat_53045048@T1` | -0.24476 |
| `explicit.stat_328541901@T2` | -0.24476 |
| `explicit.stat_803737631@T2` | -0.24476 |
| `explicit.stat_3484657501@T2` | -0.24476 |

### armour.boots — n=17046, R²=-0.2768

intercept: `2.3078`  ·  log_price: True  ·  ilvl: `-0.00011`  ·  n_mods: `-0.00070`  ·  n_top_tier: `0.13816`  ·  corrupted: `0.00245`  ·  n_sockets: `0.00018`  ·  quality: `0.00003`

| stat_id | coef |
|---|---|
| `explicit.stat_1062208444@T2` | -0.14100 |
| `explicit.stat_2451402625@T2` | -0.13950 |
| `explicit.stat_1062208444@T1` | -0.13943 |
| `explicit.stat_3261801346@T2` | -0.13912 |
| `desecrated.stat_2250533757@T2` | -0.13906 |
| `explicit.stat_3917489142@T2` | -0.13902 |
| `explicit.stat_99927264@T2` | -0.13895 |
| `explicit.stat_328541901@T1` | -0.13891 |
| `explicit.stat_3321629045@T2` | -0.13881 |
| `explicit.stat_2923486259@T2` | -0.13875 |
| `explicit.stat_2923486259@T1` | -0.13870 |
| `explicit.stat_2339757871@T1` | -0.13867 |

### armour.gloves — n=16685, R²=-0.4757

intercept: `2.9541`  ·  log_price: True  ·  ilvl: `-0.02824`  ·  n_mods: `-0.09351`  ·  n_top_tier: `0.28347`  ·  corrupted: `0.22124`  ·  n_sockets: `0.21891`  ·  quality: `0.00903`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.26611 |
| `explicit.stat_803737631@T2` | -0.91501 |
| `explicit.stat_3033371881@T2` | -0.76167 |
| `explicit.stat_53045048@T1` | -0.68876 |
| `explicit.stat_3484657501@T2` | -0.65108 |
| `explicit.stat_681332047@T2` | -0.56907 |
| `explicit.stat_3033371881@T1` | -0.53714 |
| `explicit.stat_3362812763@T2` | -0.53679 |
| `explicit.stat_3695891184@T1` | -0.46931 |
| `explicit.stat_2451402625@T2` | -0.46332 |
| `explicit.stat_3917489142@T2` | -0.45500 |
| `explicit.stat_1573130764@T1` | -0.42942 |

### weapon.wand — n=11591, R²=-1.9668

intercept: `3.4751`  ·  log_price: True  ·  ilvl: `-0.04344`  ·  n_mods: `-0.00879`  ·  n_top_tier: `0.85152`  ·  corrupted: `0.07607`  ·  n_sockets: `0.01190`  ·  quality: `0.01803`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.20151 |
| `explicit.stat_2254480358@T1` | 1.59824 |
| `explicit.stat_591105508@T1` | 1.52582 |
| `explicit.stat_4226189338@T1` | 1.52522 |
| `explicit.stat_1600707273@T1` | 1.46481 |
| `explicit.stat_1545858329@T1` | 1.43604 |
| `explicit.stat_737908626@T1` | -0.93175 |
| `explicit.stat_3962278098@T2` | -0.89907 |
| `explicit.stat_2768835289@T2` | -0.89747 |
| `explicit.stat_473429811@T1` | -0.88888 |
| `explicit.stat_473429811@T2` | -0.88825 |
| `explicit.stat_2968503605@T2` | -0.87791 |

### weapon.bow — n=9473, R²=-1.8294

intercept: `3.4659`  ·  log_price: True  ·  ilvl: `-0.04307`  ·  n_mods: `-0.00888`  ·  n_top_tier: `0.58202`  ·  corrupted: `-0.02209`  ·  n_sockets: `0.00782`  ·  quality: `0.00286`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.87563 |
| `explicit.stat_2463230181@T1` | 1.71816 |
| `explicit.stat_1202301673@T1` | 1.61344 |
| `explicit.stat_518292764@T1` | 1.23901 |
| `crafted.stat_3035140377` | 1.11556 |
| `desecrated.stat_666077204@T1` | -0.70661 |
| `explicit.stat_55876295@T1` | -0.65494 |
| `explicit.stat_2694482655@T1` | -0.63529 |
| `explicit.stat_3261801346@T1` | -0.63128 |
| `explicit.stat_669069897@T2` | -0.62450 |
| `explicit.stat_1037193709@T1` | -0.62384 |
| `explicit.stat_55876295@T2` | -0.62195 |

### weapon.crossbow — n=8948, R²=-1.7237

intercept: `3.6493`  ·  log_price: True  ·  ilvl: `-0.04549`  ·  n_mods: `-0.00364`  ·  n_top_tier: `0.70204`  ·  corrupted: `-0.03708`  ·  n_sockets: `0.01738`  ·  quality: `0.00509`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -1.50316 |
| `explicit.stat_1202301673@T1` | 1.49991 |
| `explicit.stat_709508406@T1` | 1.48421 |
| `explicit.stat_1037193709@T1` | 1.20770 |
| `crafted.stat_3035140377` | 0.88960 |
| `rune.stat_55876295` | 0.86440 |
| `explicit.stat_2250681686` | 0.84888 |
| `explicit.stat_1509134228@T1` | 0.84321 |
| `rune.stat_2246411426` | -0.79817 |
| `explicit.stat_1202301673@T2` | -0.79244 |
| `explicit.stat_669069897@T1` | -0.77947 |
| `explicit.stat_669069897@T2` | -0.76592 |

### flask.charm — n=5452, R²=-0.2408

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00004`  ·  corrupted: `0.00014`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.04267 |
| `explicit.stat_1056492907` | 2.99574 |
| `explicit.stat_2676834156@T1` | 1.60866 |
| `explicit.stat_3138344128` | 0.02230 |
| `explicit.stat_2678930256` | 0.00193 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_828533480@T2` | -0.00003 |
| `explicit.stat_828533480@T1` | -0.00003 |
| `explicit.stat_3196823591@T2` | -0.00003 |
| `explicit.stat_388617051@T2` | -0.00003 |
| `explicit.stat_1120862500@T2` | -0.00003 |

### weapon.warstaff — n=3943, R²=-0.4528

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | -5.37690 |
| `desecrated.stat_2231156303@T1` | -5.37690 |
| `rune.stat_243313994` | 3.27059 |
| `rune.stat_731403740` | 1.59482 |
| `rune.stat_1712188793` | -1.04065 |
| `desecrated.stat_9187492` | 0.82991 |
| `desecrated.stat_2527686725` | 0.24681 |
| `desecrated.stat_518292764` | 0.21375 |
| `rune.stat_3336890334` | 0.18410 |
| `rune.stat_2430860292` | -0.09304 |
| `desecrated.stat_2231156303` | 0.08201 |
| `desecrated.stat_55876295` | -0.06880 |

### weapon.staff — n=3668, R²=-0.4975

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.64574 |
| `crafted.stat_124131830` | 0.29037 |
| `rune.stat_3990135792` | -0.15470 |
| `rune.stat_975988108` | -0.12520 |
| `rune.stat_2974417149` | 0.08761 |
| `explicit.stat_473429811@T1` | 0.04189 |
| `explicit.stat_2254480358@T1` | 0.01789 |
| `desecrated.stat_2974417149` | 0.01354 |
| `explicit.stat_1600707273@T1` | 0.00072 |
| `explicit.stat_2254480358@T2` | 0.00012 |
| `explicit.stat_3962278098@T2` | 0.00006 |
| `explicit.stat_124131830@T1` | 0.00006 |

### weapon.sceptre — n=3664, R²=-0.451

intercept: `-0.0008`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00146`  ·  corrupted: `0.81785`  ·  n_sockets: `0.00001`  ·  quality: `0.03905`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.30108 |
| `rune.stat_1611856026` | 0.07352 |
| `rune.stat_3984865854` | 0.06192 |
| `desecrated.stat_3984865854` | 0.03163 |
| `rune.stat_3412619569` | 0.03000 |
| `rune.stat_1798257884` | 0.03000 |
| `desecrated.stat_1798257884` | 0.01829 |
| `desecrated.stat_1050105434` | 0.01063 |
| `explicit.stat_3984865854@T2` | -0.00148 |
| `explicit.stat_2347036682@T2` | -0.00148 |
| `explicit.stat_1250712710@T1` | -0.00148 |
| `explicit.stat_2347036682@T1` | -0.00147 |

### weapon.spear — n=3173, R²=-0.4895

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.49769 |
| `explicit.stat_210067635@T1` | 0.69310 |
| `rune.stat_1039491398` | 0.22053 |
| `rune.stat_1509134228` | -0.16405 |
| `crafted.stat_210067635` | 0.00965 |
| `explicit.stat_1202301673@T1` | 0.00746 |
| `explicit.stat_3639275092@T1` | 0.00004 |
| `explicit.stat_1509134228@T1` | 0.00004 |
| `explicit.stat_3639275092@T2` | 0.00003 |
| `explicit.stat_210067635@T2` | 0.00003 |
| `explicit.stat_3336890334@T1` | 0.00003 |
| `explicit.stat_3336890334@T2` | 0.00003 |

### armour.focus — n=2549, R²=-0.4241

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.05535`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00062`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.16780 |
| `crafted.stat_737908626@T2` | -3.86399 |
| `crafted.stat_2974417149@T1` | -3.64372 |
| `desecrated.stat_3393628375` | 0.51306 |
| `crafted.stat_737908626` | 0.14741 |
| `explicit.stat_2923486259` | -0.14365 |
| `pseudo.total_chaos_res` | 0.14365 |
| `crafted.stat_2974417149` | 0.08233 |
| `crafted.stat_4015621042` | 0.06601 |
| `explicit.stat_2923486259@T1` | -0.05538 |
| `explicit.stat_736967255@T2` | -0.05537 |
| `explicit.stat_328541901@T2` | -0.05537 |

### armour.quiver — n=2431, R²=-0.534

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.03899`  ·  corrupted: `0.00003`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 4.89217 |
| `desecrated.stat_3932115504` | -0.31359 |
| `desecrated.stat_2194114101` | 0.18632 |
| `desecrated.stat_3714003708` | 0.06902 |
| `explicit.stat_681332047@T2` | -0.03903 |
| `explicit.stat_681332047@T1` | -0.03902 |
| `explicit.stat_2321178454@T2` | -0.03901 |
| `explicit.stat_1573130764@T1` | -0.03901 |
| `explicit.stat_803737631@T2` | -0.03900 |
| `explicit.stat_1368271171@T2` | -0.03900 |
| `explicit.stat_3714003708@T2` | -0.03900 |
| `explicit.stat_1573130764@T2` | -0.03900 |

### armour.shield — n=2143, R²=-0.4433

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.27246`  ·  corrupted: `0.00004`  ·  n_sockets: `0.00001`  ·  quality: `0.00966`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.72782 |
| `explicit.stat_1978899297@T2` | -0.42203 |
| `explicit.stat_1301765461@T1` | 0.42063 |
| `explicit.stat_1011760251@T1` | -0.27444 |
| `explicit.stat_1011760251@T2` | -0.27377 |
| `explicit.stat_2481353198@T1` | -0.27251 |
| `explicit.stat_2481353198@T2` | -0.27250 |
| `explicit.stat_3484657501@T1` | -0.27248 |
| `explicit.stat_2339757871@T1` | -0.27248 |
| `explicit.stat_1062208444@T2` | -0.27248 |
| `explicit.stat_3639275092@T2` | -0.27247 |
| `explicit.stat_328541901@T1` | -0.27247 |

### weapon.twomace — n=1845, R²=-0.4172

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00579`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_518292764@T1` | 2.29678 |
| `desecrated.stat_1509134228@T1` | 1.62003 |
| `explicit.stat_1509134228@T1` | 0.70742 |
| `rune.stat_1039491398` | 0.11927 |
| `desecrated.stat_210067635` | 0.07103 |
| `rune.stat_1509134228` | -0.04307 |
| `crafted.stat_210067635` | 0.02656 |
| `desecrated.stat_691932474` | 0.01035 |
| `crafted.stat_1940865751` | 0.00742 |
| `explicit.stat_3336890334@T1` | -0.00588 |
| `explicit.stat_1037193709@T1` | -0.00586 |
| `explicit.stat_1037193709@T2` | -0.00583 |

## Coverage (listings per base)

- … **Emerald** — 11403 listings (11395 priced) [0.5–7553463.8 ex]
- … **Sapphire** — 11397 listings (11383 priced) [0.3–7553463.8 ex]
- … **Ruby** — 8846 listings (8836 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 5568 listings (5564 priced) [0.2–5288620.9 ex]
- … **Stellar Amulet** — 4165 listings (4165 priced) [0.3–35690283.3 ex]
- … **Prismatic Ring** — 4154 listings (4153 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 4068 listings (4062 priced) [0.3–66666666.0 ex]
- … **Amethyst Ring** — 3931 listings (3930 priced) [0.3–71450.3 ex]
- … **Gold Amulet** — 3889 listings (3889 priced) [0.3–292542.5 ex]
- … **Gold Ring** — 3762 listings (3761 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 3629 listings (3625 priced) [0.3–3736768402.2 ex]
- … **Sapphire Ring** — 3143 listings (3140 priced) [0.3–24532814.5 ex]
- … **Topaz Ring** — 3047 listings (3046 priced) [0.3–123132003.2 ex]
- … **Ruby Ring** — 3024 listings (3024 priced) [0.3–37474957.5 ex]
- … **Plate Belt** — 2830 listings (2828 priced) [0.3–4877938.3 ex]
- … **Obliterator Bow** — 2749 listings (2743 priced) [0.3–22139622146.9 ex]
- … **Ancestral Tiara** — 2716 listings (2714 priced) [0.6–37474957.5 ex]
- … **Lapis Amulet** — 2712 listings (2712 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 2680 listings (2679 priced) [0.3–113795639.4 ex]
- … **Jade Amulet** — 2679 listings (2678 priced) [0.3–4547453.5 ex]
- … **Heavy Belt** — 2667 listings (2667 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 2542 listings (2542 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 2507 listings (2507 priced) [0.3–14638.0 ex]
- … **Pearl Ring** — 2433 listings (2433 priced) [0.3–24532814.5 ex]
- … **Azure Amulet** — 2397 listings (2397 priced) [0.2–123132003.2 ex]

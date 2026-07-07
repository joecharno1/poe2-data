# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-07T16:33:35+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **285271** (284948 priced in exalted)
- Distinct bases: 949 · distinct mods: 2764 · mod rows: 1355463
- Sold signals: **31978** sold · 152094 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-07T16:24:23+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×17.48** (median |log error| 2.8612)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 75% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.07** · typical error ×44.96 · ±30% 12% · n=41212
- Premium segment (60ex+): skill **+0.08** · typical error ×172.33 · ±30% 0% · n=25859

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 5371 | ×11.41 | 4% | +0.03 | +0.05 |
| accessory.amulet | 5137 | ×56.66 | 20% | +0.02 | +0.02 |
| jewel | 4720 | ×8.39 | 8% | +0.00 | +0.03 |
| accessory.belt | 4212 | ×19.93 | 21% | +0.05 | +0.08 |
| armour.chest | 4119 | ×10.00 | 27% | +0.01 | +0.02 |
| armour.helmet | 4037 | ×10.00 | 25% | +0.01 | +0.01 |
| armour.boots | 3788 | ×14.34 | 22% | +0.00 | +0.00 |
| armour.gloves | 3752 | ×10.04 | 22% | +0.00 | +0.01 |
| other | 3438 | ×9.14 | 35% | +0.18 | +0.49 |
| weapon.wand | 2602 | ×21.63 | 22% | +0.07 | +0.07 |
| weapon.bow | 2083 | ×19.44 | 19% | +0.09 | +0.10 |
| weapon.crossbow | 1974 | ×16.35 | 19% | +0.09 | +0.11 |
| weapon.warstaff | 845 | ×78.46 | 19% | +0.01 | +0.01 |
| weapon.staff | 831 | ×57.00 | 19% | +0.04 | +0.02 |
| weapon.sceptre | 741 | ×94.32 | 14% | +0.04 | +0.03 |
| weapon.spear | 723 | ×50.00 | 22% | +0.02 | +0.02 |
| armour.focus | 554 | ×659.97 | 10% | +0.00 | +0.02 |
| armour.quiver | 546 | ×149.99 | 13% | +0.00 | +0.04 |
| armour.shield | 474 | ×82.11 | 18% | +0.01 | +0.02 |
| weapon.twomace | 376 | ×27.64 | 20% | +0.07 | +0.03 |
| flask.charm | 374 | ×10.00 | 42% | -0.00 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=30096, R²=-0.4059

intercept: `1.5930`  ·  log_price: True  ·  ilvl: `0.00028`  ·  n_mods: `0.16327`  ·  n_top_tier: `1.49456`  ·  corrupted: `1.70048`  ·  n_sockets: `-0.00242`  ·  quality: `-0.00028`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -3.48557 |
| `explicit.stat_3917489142@T1` | 2.64430 |
| `explicit.stat_3291658075@T1` | 2.28034 |
| `explicit.stat_789117908@T1` | -2.11829 |
| `explicit.stat_2891184298@T1` | 1.98038 |
| `explicit.stat_101878827@T1` | 1.64247 |
| `explicit.stat_3141070085@T1` | 1.63054 |
| `explicit.stat_1589917703@T1` | 1.61569 |
| `explicit.stat_2974417149@T1` | 1.55082 |
| `explicit.stat_2106365538@T1` | 1.34693 |
| `explicit.stat_2968503605@T1` | 1.18711 |
| `implicit.stat_3182714256` | 0.49569 |

### jewel — n=25022, R²=-0.6382

intercept: `-1.0931`  ·  log_price: True  ·  ilvl: `0.03615`  ·  n_mods: `0.12606`  ·  n_top_tier: `-0.00006`  ·  corrupted: `0.46228`  ·  quality: `0.21020`

| stat_id | coef |
|---|---|
| `explicit.stat_1569101201@T1` | 3.62247 |
| `explicit.stat_3714003708@T1` | -3.34685 |
| `explicit.stat_1854213750@T1` | -3.24796 |
| `explicit.stat_1594812856@T1` | -3.20918 |
| `explicit.stat_1316278494@T1` | -3.19887 |
| `explicit.stat_3668351662@T1` | -3.17702 |
| `explicit.stat_153777645@T1` | 2.83096 |
| `explicit.stat_3741323227@T1` | -2.82037 |
| `explicit.stat_21071013@T1` | -2.78032 |
| `explicit.stat_1697951953@T1` | -2.62058 |
| `explicit.stat_3192728503@T1` | -2.29904 |
| `explicit.stat_2106365538@T1` | -2.02577 |

### accessory.ring — n=24620, R²=-1.2346

intercept: `4.6408`  ·  log_price: True  ·  ilvl: `-0.04304`  ·  n_mods: `-0.16095`  ·  n_top_tier: `0.02907`  ·  corrupted: `0.81142`  ·  n_sockets: `-1.49569`  ·  quality: `0.03527`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.28403 |
| `explicit.stat_707457662@T2` | 3.05912 |
| `explicit.stat_1379411836@T1` | -2.41901 |
| `explicit.stat_1379411836@T2` | -1.95334 |
| `explicit.stat_1368271171@T2` | -1.17951 |
| `explicit.stat_1368271171@T1` | -0.96571 |
| `explicit.stat_2923486259@T2` | 0.76485 |
| `explicit.stat_4080418644@T2` | 0.63399 |
| `explicit.stat_736967255@T1` | 0.61400 |
| `explicit.stat_707457662` | -0.59754 |
| `explicit.stat_3299347043@T1` | -0.51067 |
| `explicit.stat_1573130764@T1` | -0.50612 |

### accessory.amulet — n=23416, R²=-2.0893

intercept: `4.3563`  ·  log_price: True  ·  ilvl: `-0.05269`  ·  n_mods: `-0.02847`  ·  n_top_tier: `1.06811`  ·  corrupted: `0.11709`  ·  n_sockets: `1.00399`  ·  quality: `-0.00611`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | -2.78997 |
| `explicit.stat_983749596@T1` | -1.25224 |
| `explicit.stat_3299347043@T1` | -1.22841 |
| `explicit.stat_983749596@T2` | -1.21092 |
| `explicit.stat_3917489142@T2` | -1.18722 |
| `explicit.stat_3325883026@T1` | -1.17985 |
| `explicit.stat_3917489142@T1` | -1.16971 |
| `explicit.stat_3489782002@T2` | -1.14712 |
| `explicit.stat_472520716@T1` | -1.14172 |
| `explicit.stat_587431675@T1` | -1.13856 |
| `explicit.stat_2748665614@T1` | -1.13610 |
| `explicit.stat_3325883026@T2` | -1.12891 |

### accessory.belt — n=19319, R²=-1.4051

intercept: `3.6255`  ·  log_price: True  ·  ilvl: `-0.04318`  ·  n_mods: `-0.02001`  ·  n_top_tier: `0.74685`  ·  corrupted: `0.57805`  ·  n_sockets: `-0.12463`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -0.79571 |
| `explicit.stat_809229260@T2` | -0.78698 |
| `explicit.stat_2881298780@T1` | -0.77523 |
| `explicit.stat_4220027924@T2` | -0.77308 |
| `explicit.stat_51994685@T1` | -0.77224 |
| `explicit.stat_3299347043@T2` | -0.76580 |
| `explicit.stat_3299347043@T1` | -0.76484 |
| `explicit.stat_2923486259@T2` | -0.75990 |
| `explicit.stat_915769802@T2` | -0.75886 |
| `explicit.stat_1671376347@T2` | -0.75642 |
| `explicit.stat_644456512@T2` | -0.75169 |
| `explicit.stat_3325883026@T1` | -0.75151 |

### armour.chest — n=19104, R²=-0.2152

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.17395`  ·  corrupted: `0.02526`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 0.22724 |
| `explicit.stat_915769802@T2` | -0.17397 |
| `explicit.stat_4080418644@T2` | -0.17397 |
| `explicit.stat_2339757871@T2` | -0.17397 |
| `explicit.stat_915769802@T1` | -0.17397 |
| `explicit.stat_3261801346@T1` | -0.17397 |
| `explicit.stat_3484657501@T1` | -0.17396 |
| `explicit.stat_2881298780@T1` | -0.17396 |
| `explicit.stat_124859000@T2` | -0.17396 |
| `explicit.stat_3261801346@T2` | -0.17396 |
| `explicit.stat_1062208444@T2` | -0.17396 |
| `explicit.stat_53045048@T2` | -0.17396 |

### armour.helmet — n=18708, R²=-0.2334

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.48098`  ·  corrupted: `1.59676`  ·  n_sockets: `0.00001`  ·  quality: `0.00003`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.76454 |
| `explicit.stat_1263695895@T1` | -0.48102 |
| `explicit.stat_1263695895@T2` | -0.48101 |
| `explicit.stat_2451402625@T1` | -0.48100 |
| `explicit.stat_3362812763@T2` | -0.48100 |
| `explicit.stat_3362812763@T1` | -0.48100 |
| `explicit.stat_53045048@T2` | -0.48099 |
| `explicit.stat_3484657501@T2` | -0.48099 |
| `explicit.stat_2451402625@T2` | -0.48099 |
| `explicit.stat_4080418644@T2` | -0.48099 |
| `explicit.stat_3917489142@T2` | -0.48099 |
| `explicit.stat_53045048@T1` | -0.48099 |

### armour.boots — n=17618, R²=-0.2667

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.35263`  ·  corrupted: `0.07358`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2250533757@T2` | -0.35265 |
| `explicit.stat_3917489142@T2` | -0.35265 |
| `explicit.stat_2339757871@T1` | -0.35264 |
| `explicit.stat_2451402625@T2` | -0.35264 |
| `explicit.stat_2923486259@T2` | -0.35264 |
| `explicit.stat_99927264@T2` | -0.35264 |
| `explicit.stat_3261801346@T2` | -0.35264 |
| `explicit.stat_1999113824@T1` | -0.35264 |
| `explicit.stat_1062208444@T1` | -0.35264 |
| `explicit.stat_3917489142@T1` | -0.35263 |
| `explicit.stat_1062208444@T2` | -0.35263 |
| `explicit.stat_99927264@T1` | -0.35263 |

### armour.gloves — n=17234, R²=-0.321

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00027`  ·  corrupted: `0.01284`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.10362 |
| `desecrated.stat_4067062424` | 0.09459 |
| `desecrated.stat_1573130764` | 0.04975 |
| `pseudo.total_ele_res>=80` | 0.03622 |
| `explicit.stat_3372524247@T1` | 0.01660 |
| `explicit.stat_2923486259@T1` | 0.00526 |
| `desecrated.stat_3299347043` | 0.00462 |
| `explicit.stat_9187492@T1` | 0.00431 |
| `explicit.stat_9187492@T2` | -0.00206 |
| `explicit.stat_9187492` | 0.00182 |
| `explicit.stat_2339757871@T1` | -0.00036 |
| `explicit.stat_3484657501@T2` | -0.00033 |

### weapon.wand — n=11925, R²=-1.9977

intercept: `3.4040`  ·  log_price: True  ·  ilvl: `-0.04255`  ·  n_mods: `-0.00959`  ·  n_top_tier: `0.95909`  ·  corrupted: `0.04216`  ·  n_sockets: `0.00855`  ·  quality: `0.01538`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.55432 |
| `explicit.stat_2254480358@T1` | 1.47663 |
| `explicit.stat_591105508@T1` | 1.41354 |
| `explicit.stat_4226189338@T1` | 1.39394 |
| `explicit.stat_1545858329@T1` | 1.34315 |
| `explicit.stat_1600707273@T1` | 1.34046 |
| `explicit.stat_737908626@T1` | -1.01832 |
| `explicit.stat_3962278098@T2` | -0.99621 |
| `explicit.stat_473429811@T2` | -0.99617 |
| `explicit.stat_473429811@T1` | -0.99468 |
| `explicit.stat_2768835289@T2` | -0.98826 |
| `explicit.stat_3639275092@T1` | -0.97770 |

### weapon.bow — n=9712, R²=-1.8736

intercept: `3.4377`  ·  log_price: True  ·  ilvl: `-0.04270`  ·  n_mods: `-0.01090`  ·  n_top_tier: `0.64672`  ·  corrupted: `0.00350`  ·  n_sockets: `0.00336`  ·  quality: `0.00645`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.05057 |
| `explicit.stat_2463230181@T1` | 1.64413 |
| `explicit.stat_1202301673@T1` | 1.48173 |
| `explicit.stat_518292764@T1` | 1.17908 |
| `crafted.stat_3035140377` | 1.12650 |
| `rune.stat_3885405204` | -0.73485 |
| `explicit.stat_55876295@T1` | -0.70791 |
| `explicit.stat_3261801346@T1` | -0.69489 |
| `explicit.stat_2694482655@T1` | -0.69173 |
| `explicit.stat_3695891184@T2` | -0.68866 |
| `explicit.stat_669069897@T2` | -0.68786 |
| `explicit.stat_3336890334@T2` | -0.68154 |

### weapon.crossbow — n=9186, R²=-1.7279

intercept: `3.5828`  ·  log_price: True  ·  ilvl: `-0.04477`  ·  n_mods: `-0.00235`  ·  n_top_tier: `0.75519`  ·  corrupted: `-0.02537`  ·  n_sockets: `0.01810`  ·  quality: `0.00620`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -1.57389 |
| `explicit.stat_709508406@T1` | 1.41946 |
| `explicit.stat_1037193709@T1` | 1.38919 |
| `explicit.stat_1202301673@T1` | 1.37717 |
| `explicit.stat_1202301673@T2` | -0.90140 |
| `crafted.stat_3035140377` | 0.88676 |
| `rune.stat_55876295` | 0.88637 |
| `explicit.stat_1509134228@T1` | 0.87114 |
| `explicit.stat_691932474@T1` | -0.86645 |
| `explicit.stat_669069897@T1` | -0.85778 |
| `explicit.stat_669069897@T2` | -0.85341 |
| `rune.stat_2246411426` | -0.83728 |

### flask.charm — n=5807, R²=-0.2795

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00004`  ·  corrupted: `0.08112`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.01954 |
| `explicit.stat_1056492907` | 3.21840 |
| `explicit.stat_2676834156@T1` | 1.60936 |
| `explicit.stat_3138344128` | 0.02221 |
| `explicit.stat_2678930256` | 0.00119 |
| `explicit.stat_2541588185@T1` | 0.00043 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_1873752457@T1` | -0.00004 |
| `explicit.stat_3196823591@T2` | -0.00004 |
| `explicit.stat_828533480@T1` | -0.00004 |
| `explicit.stat_828533480@T2` | -0.00004 |
| `explicit.stat_388617051@T2` | -0.00003 |

### weapon.warstaff — n=4140, R²=-0.4758

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00001`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00003`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | -4.65275 |
| `desecrated.stat_2527686725@T1` | -4.65275 |
| `rune.stat_243313994` | 3.25757 |
| `rune.stat_731403740` | 1.56479 |
| `rune.stat_1712188793` | -0.95268 |
| `desecrated.stat_9187492` | 0.81130 |
| `desecrated.stat_2527686725` | 0.24858 |
| `desecrated.stat_518292764` | 0.12314 |
| `rune.stat_3336890334` | 0.10691 |
| `crafted.stat_210067635@T2` | 0.08856 |
| `desecrated.stat_55876295` | -0.08737 |
| `desecrated.stat_2231156303` | 0.06545 |

### weapon.staff — n=3869, R²=-0.5245

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00004`  ·  n_sockets: `0.00001`  ·  quality: `0.00002`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.64545 |
| `crafted.stat_124131830` | 0.32903 |
| `explicit.stat_1600707273@T1` | 0.19382 |
| `rune.stat_3990135792` | -0.19165 |
| `explicit.stat_2254480358@T1` | 0.14812 |
| `rune.stat_975988108` | -0.12479 |
| `rune.stat_2974417149` | 0.10348 |
| `desecrated.stat_2974417149` | 0.01380 |
| `explicit.stat_124131830@T1` | 0.01103 |
| `explicit.stat_2254480358@T2` | 0.00823 |
| `explicit.stat_4226189338@T1` | 0.00657 |
| `explicit.stat_473429811@T1` | 0.00106 |

### weapon.sceptre — n=3861, R²=-0.4927

intercept: `-0.0009`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.15255`  ·  corrupted: `1.23542`  ·  n_sockets: `0.00001`  ·  quality: `0.05109`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.14982 |
| `explicit.stat_2347036682@T2` | -0.15257 |
| `explicit.stat_3984865854@T2` | -0.15257 |
| `explicit.stat_2347036682@T1` | -0.15257 |
| `explicit.stat_1250712710@T1` | -0.15256 |
| `explicit.stat_4080418644@T1` | -0.15256 |
| `explicit.stat_4080418644@T2` | -0.15256 |
| `explicit.stat_1574590649@T1` | -0.15256 |
| `explicit.stat_1574590649@T2` | -0.15256 |
| `explicit.stat_3639275092@T2` | -0.15255 |
| `explicit.stat_789117908@T1` | -0.15255 |
| `explicit.stat_2854751904@T1` | -0.15255 |

### weapon.spear — n=3358, R²=-0.4973

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00002`  ·  corrupted: `-0.00003`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.49789 |
| `explicit.stat_210067635@T1` | 1.20485 |
| `crafted.stat_518292764` | 1.09426 |
| `rune.stat_1039491398` | 0.19785 |
| `explicit.stat_1202301673@T1` | 0.14050 |
| `rune.stat_1509134228` | -0.13042 |
| `crafted.stat_210067635` | 0.07145 |
| `desecrated.stat_1509134228` | 0.00637 |
| `explicit.stat_1509134228@T1` | 0.00454 |
| `desecrated.stat_691932474` | -0.00285 |
| `explicit.stat_3336890334@T1` | 0.00012 |
| `explicit.stat_3639275092@T1` | 0.00005 |

### armour.focus — n=2739, R²=-0.5551

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.07631`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00479`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.02793 |
| `crafted.stat_737908626@T2` | -4.32841 |
| `crafted.stat_2974417149@T1` | 0.51918 |
| `desecrated.stat_3393628375` | 0.50359 |
| `crafted.stat_737908626` | 0.15477 |
| `pseudo.total_chaos_res` | 0.13942 |
| `explicit.stat_2923486259` | -0.13942 |
| `explicit.stat_2891184298@T2` | -0.07633 |
| `explicit.stat_736967255@T2` | -0.07633 |
| `explicit.stat_2923486259@T1` | -0.07632 |
| `explicit.stat_328541901@T2` | -0.07632 |
| `explicit.stat_3291658075@T1` | -0.07632 |

### armour.quiver — n=2563, R²=-0.5536

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.18527`  ·  corrupted: `0.00003`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.62337 |
| `explicit.stat_3759663284@T1` | 0.50089 |
| `explicit.stat_681332047@T2` | -0.18532 |
| `explicit.stat_681332047@T1` | -0.18531 |
| `explicit.stat_2321178454@T2` | -0.18529 |
| `explicit.stat_1573130764@T1` | -0.18529 |
| `explicit.stat_1368271171@T2` | -0.18529 |
| `explicit.stat_3714003708@T2` | -0.18528 |
| `explicit.stat_803737631@T2` | -0.18528 |
| `explicit.stat_1573130764@T2` | -0.18528 |
| `explicit.stat_2194114101@T2` | -0.18528 |
| `explicit.stat_2194114101@T1` | -0.18527 |

### armour.shield — n=2240, R²=-0.4251

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.32950`  ·  corrupted: `0.00147`  ·  n_sockets: `0.00001`  ·  quality: `0.03670`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.76216 |
| `explicit.stat_1978899297@T2` | -0.47679 |
| `explicit.stat_1301765461@T1` | 0.36351 |
| `explicit.stat_1011760251@T1` | -0.33815 |
| `explicit.stat_1011760251@T2` | -0.33526 |
| `explicit.stat_2481353198@T1` | -0.32954 |
| `explicit.stat_328541901@T1` | -0.32953 |
| `explicit.stat_2481353198@T2` | -0.32953 |
| `explicit.stat_1062208444@T2` | -0.32953 |
| `explicit.stat_3372524247@T2` | -0.32952 |
| `explicit.stat_3639275092@T1` | -0.32952 |
| `explicit.stat_3484657501@T1` | -0.32952 |

### weapon.twomace — n=1937, R²=-0.4647

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.14115`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_669069897` | -2.88791 |
| `rune.stat_1586906534` | 2.12706 |
| `explicit.stat_1509134228@T1` | 1.46830 |
| `desecrated.stat_210067635@T1` | 0.50908 |
| `desecrated.stat_210067635` | 0.14356 |
| `explicit.stat_3336890334@T1` | -0.14122 |
| `explicit.stat_1037193709@T1` | -0.14120 |
| `explicit.stat_1037193709@T2` | -0.14119 |
| `explicit.stat_821021828@T1` | -0.14118 |
| `explicit.stat_387439868@T2` | -0.14118 |
| `explicit.stat_3336890334@T2` | -0.14118 |
| `explicit.stat_1940865751@T2` | -0.14118 |

## Coverage (listings per base)

- … **Emerald** — 11940 listings (11932 priced) [0.4–7553463.8 ex]
- … **Sapphire** — 11905 listings (11889 priced) [0.3–7553463.8 ex]
- … **Ruby** — 9204 listings (9194 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 5745 listings (5741 priced) [0.2–5288620.9 ex]
- … **Stellar Amulet** — 4299 listings (4299 priced) [0.2–35690283.3 ex]
- … **Prismatic Ring** — 4296 listings (4294 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 4219 listings (4213 priced) [0.3–66666666.0 ex]
- … **Amethyst Ring** — 4073 listings (4072 priced) [0.3–71450.3 ex]
- … **Gold Amulet** — 4046 listings (4046 priced) [0.2–292542.5 ex]
- … **Gold Ring** — 3914 listings (3913 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 3754 listings (3749 priced) [0.3–3736768402.2 ex]
- … **Sapphire Ring** — 3271 listings (3267 priced) [0.3–24532814.5 ex]
- … **Topaz Ring** — 3171 listings (3170 priced) [0.3–123132003.2 ex]
- … **Ruby Ring** — 3149 listings (3149 priced) [0.3–37474957.5 ex]
- … **Plate Belt** — 2921 listings (2919 priced) [0.3–4877938.3 ex]
- … **Obliterator Bow** — 2831 listings (2824 priced) [0.3–22139622146.9 ex]
- … **Lapis Amulet** — 2829 listings (2829 priced) [0.3–4547453.5 ex]
- … **Ancestral Tiara** — 2811 listings (2809 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 2782 listings (2781 priced) [0.2–124352753.2 ex]
- … **Jade Amulet** — 2780 listings (2779 priced) [0.2–4547453.5 ex]
- … **Heavy Belt** — 2751 listings (2751 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 2641 listings (2641 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 2593 listings (2593 priced) [0.3–14638.0 ex]
- … **Pearl Ring** — 2518 listings (2518 priced) [0.3–24532814.5 ex]
- … **Azure Amulet** — 2463 listings (2463 priced) [0.2–123132003.2 ex]

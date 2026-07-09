# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-09T17:20:00+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **382605** (381963 priced in exalted)
- Distinct bases: 964 · distinct mods: 2931 · mod rows: 1817246
- Sold signals: **28577** sold · 203625 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-09T17:08:33+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×18.67** (median |log error| 2.9269)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 77% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.07** · typical error ×42.58 · ±30% 13% · n=56128
- Premium segment (60ex+): skill **+0.08** · typical error ×146.54 · ±30% 0% · n=35733

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 7430 | ×13.48 | 4% | +0.05 | +0.07 |
| accessory.amulet | 6927 | ×50.66 | 20% | +0.02 | +0.02 |
| jewel | 6668 | ×8.15 | 8% | +0.01 | +0.04 |
| accessory.belt | 5503 | ×9.89 | 22% | +0.01 | +0.01 |
| armour.chest | 5299 | ×10.20 | 22% | +0.01 | +0.01 |
| armour.helmet | 5285 | ×14.06 | 21% | +0.01 | +0.02 |
| armour.boots | 4912 | ×10.46 | 21% | +0.01 | +0.02 |
| armour.gloves | 4852 | ×30.37 | 19% | +0.00 | +0.02 |
| other | 4502 | ×10.00 | 35% | +0.07 | +0.18 |
| weapon.wand | 3176 | ×45.96 | 18% | +0.06 | +0.05 |
| weapon.bow | 2526 | ×26.61 | 17% | +0.09 | +0.10 |
| weapon.crossbow | 2410 | ×23.00 | 18% | +0.10 | +0.13 |
| weapon.warstaff | 1306 | ×99.99 | 14% | +0.08 | +0.08 |
| weapon.staff | 1239 | ×62.00 | 12% | +0.07 | +0.07 |
| weapon.sceptre | 1210 | ×65.26 | 10% | +0.09 | +0.09 |
| weapon.spear | 1026 | ×50.00 | 16% | +0.06 | +0.06 |
| armour.focus | 820 | ×69.57 | 13% | +0.09 | +0.13 |
| armour.quiver | 776 | ×59.99 | 12% | +0.04 | +0.10 |
| armour.shield | 663 | ×30.00 | 14% | +0.04 | +0.08 |
| weapon.twomace | 599 | ×23.00 | 13% | +0.06 | +0.09 |
| flask.charm | 577 | ×10.00 | 37% | +0.00 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=38261, R²=-0.4616

intercept: `1.6067`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `0.00854`  ·  n_top_tier: `0.66657`  ·  corrupted: `1.07320`  ·  n_sockets: `-0.00005`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.55368 |
| `explicit.stat_2106365538@T1` | 3.34181 |
| `explicit.stat_2482852589@T1` | 2.89622 |
| `explicit.stat_1589917703@T1` | 2.02552 |
| `explicit.stat_101878827@T1` | 1.24126 |
| `explicit.stat_1050105434@T1` | -1.18725 |
| `explicit.stat_3917489142@T1` | 1.11041 |
| `explicit.stat_789117908@T1` | -0.92927 |
| `explicit.stat_2974417149@T1` | 0.88420 |
| `explicit.stat_2891184298@T1` | 0.57953 |
| `explicit.stat_3141070085@T1` | -0.31320 |
| `explicit.stat_2968503605@T1` | 0.29554 |

### jewel — n=36012, R²=-0.6801

intercept: `-1.2962`  ·  log_price: True  ·  ilvl: `0.03536`  ·  n_mods: `0.26022`  ·  n_top_tier: `-0.06768`  ·  corrupted: `0.30185`  ·  quality: `0.22483`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -5.13630 |
| `explicit.stat_3780644166@T1` | -3.58511 |
| `explicit.stat_1569101201@T1` | 3.31763 |
| `explicit.stat_3741323227@T1` | -2.99433 |
| `explicit.stat_3485067555@T1` | 2.51951 |
| `explicit.stat_1316278494@T1` | -2.40082 |
| `explicit.stat_2527686725@T1` | 2.16834 |
| `explicit.stat_1315743832@T1` | 1.91441 |
| `explicit.stat_234296660@T1` | -1.86242 |
| `explicit.stat_795138349@T1` | -1.83154 |
| `explicit.stat_3714003708@T1` | -1.81627 |
| `explicit.stat_627767961@T1` | -1.76972 |

### accessory.ring — n=33957, R²=-1.2185

intercept: `3.8972`  ·  log_price: True  ·  ilvl: `-0.04129`  ·  n_mods: `-0.03503`  ·  n_top_tier: `0.03489`  ·  corrupted: `0.95249`  ·  n_sockets: `1.15994`  ·  quality: `0.01342`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 3.46040 |
| `explicit.stat_707457662@T2` | 3.28496 |
| `explicit.stat_1573130764@T1` | -1.00388 |
| `explicit.stat_1379411836@T1` | -0.93397 |
| `explicit.stat_1263695895@T1` | -0.81455 |
| `explicit.stat_2923486259@T2` | 0.76099 |
| `explicit.stat_1368271171@T1` | -0.74732 |
| `explicit.stat_2923486259@T1` | 0.69803 |
| `explicit.stat_1379411836@T2` | -0.65590 |
| `explicit.stat_1368271171@T2` | -0.59625 |
| `explicit.stat_3325883026@T1` | -0.58733 |
| `explicit.stat_2231156303@T1` | -0.54399 |

### accessory.amulet — n=31865, R²=-2.0977

intercept: `4.1603`  ·  log_price: True  ·  ilvl: `-0.05013`  ·  n_mods: `-0.02855`  ·  n_top_tier: `1.04708`  ·  corrupted: `0.15664`  ·  n_sockets: `0.46687`  ·  quality: `-0.00265`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.31025 |
| `explicit.stat_983749596@T2` | -1.25345 |
| `explicit.stat_2748665614@T2` | -1.15312 |
| `explicit.stat_2748665614@T1` | -1.14971 |
| `explicit.stat_472520716@T1` | -1.14487 |
| `explicit.stat_3917489142@T2` | -1.14122 |
| `explicit.stat_3917489142@T1` | -1.13156 |
| `explicit.stat_3299347043@T1` | -1.13073 |
| `explicit.stat_587431675@T1` | -1.12628 |
| `explicit.stat_472520716@T2` | -1.12191 |
| `explicit.stat_3299347043@T2` | -1.11014 |
| `explicit.stat_2106365538@T1` | -1.10297 |

### accessory.belt — n=25219, R²=-0.1604

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00478`  ·  corrupted: `0.00004`  ·  n_sockets: `-0.69311`

| stat_id | coef |
|---|---|
| `explicit.stat_2639966148` | 0.15908 |
| `pseudo.total_ele_res>=80` | 0.06080 |
| `explicit.stat_174664100` | 0.05416 |
| `explicit.stat_3811191316` | 0.04618 |
| `explicit.stat_770672621` | 0.03277 |
| `explicit.stat_3742865955` | 0.02248 |
| `pseudo.total_chaos_res` | 0.02201 |
| `explicit.stat_2923486259` | -0.02201 |
| `explicit.stat_2957407601` | 0.01887 |
| `explicit.stat_1485480327` | 0.01583 |
| `explicit.stat_1389754388@T1` | -0.00479 |
| `explicit.stat_51994685@T1` | -0.00479 |

### armour.chest — n=24950, R²=-0.2642

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.05105`  ·  corrupted: `0.00014`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 0.22663 |
| `explicit.stat_915769802@T2` | -0.05108 |
| `explicit.stat_915769802@T1` | -0.05108 |
| `explicit.stat_4080418644@T2` | -0.05107 |
| `explicit.stat_3325883026@T2` | -0.05107 |
| `explicit.stat_3484657501@T1` | -0.05107 |
| `explicit.stat_3261801346@T2` | -0.05107 |
| `explicit.stat_1062208444@T2` | -0.05106 |
| `explicit.stat_2923486259@T2` | -0.05106 |
| `explicit.stat_2451402625@T2` | -0.05106 |
| `explicit.stat_4080418644@T1` | -0.05106 |
| `explicit.stat_3321629045@T1` | -0.05106 |

### armour.helmet — n=24404, R²=-0.2994

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.36874`  ·  corrupted: `1.60931`  ·  n_sockets: `0.00001`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.28441 |
| `explicit.stat_3362812763@T2` | -0.36876 |
| `explicit.stat_2451402625@T1` | -0.36876 |
| `explicit.stat_53045048@T2` | -0.36875 |
| `explicit.stat_1263695895@T1` | -0.36875 |
| `explicit.stat_803737631@T2` | -0.36875 |
| `explicit.stat_4080418644@T2` | -0.36875 |
| `explicit.stat_4080418644@T1` | -0.36875 |
| `explicit.stat_53045048@T1` | -0.36874 |
| `explicit.stat_3917489142@T2` | -0.36874 |
| `explicit.stat_1263695895@T2` | -0.36874 |
| `explicit.stat_3362812763@T1` | -0.36874 |

### armour.boots — n=22904, R²=-0.3333

intercept: `2.3084`  ·  log_price: True  ·  ilvl: `-0.00010`  ·  n_mods: `-0.00085`  ·  n_top_tier: `0.14704`  ·  corrupted: `0.00428`  ·  n_sockets: `0.00004`  ·  quality: `0.00007`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 0.91888 |
| `explicit.stat_1062208444@T2` | -0.21586 |
| `desecrated.stat_2250533757@T2` | -0.15019 |
| `explicit.stat_2339757871@T1` | -0.14804 |
| `explicit.stat_1999113824@T1` | -0.14802 |
| `explicit.stat_3261801346@T2` | -0.14797 |
| `explicit.stat_2923486259@T2` | -0.14781 |
| `explicit.stat_3917489142@T2` | -0.14780 |
| `explicit.stat_2923486259@T1` | -0.14767 |
| `explicit.stat_1999113824@T2` | -0.14757 |
| `explicit.stat_1671376347@T2` | -0.14755 |
| `explicit.stat_1062208444@T1` | -0.14752 |

### armour.gloves — n=22302, R²=-0.3885

intercept: `2.3102`  ·  log_price: True  ·  ilvl: `-0.00020`  ·  n_mods: `-0.00144`  ·  n_top_tier: `0.02182`  ·  corrupted: `0.00838`  ·  n_sockets: `0.00113`  ·  quality: `0.00035`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | 0.38523 |
| `desecrated.stat_3032590688` | 0.10908 |
| `desecrated.stat_4067062424` | 0.09633 |
| `rune.stat_789117908` | -0.03566 |
| `explicit.stat_803737631@T2` | -0.02510 |
| `explicit.stat_3484657501@T2` | -0.02491 |
| `explicit.stat_681332047@T2` | -0.02406 |
| `explicit.stat_3695891184@T1` | -0.02365 |
| `explicit.stat_2797971005@T2` | -0.02333 |
| `explicit.stat_1573130764@T1` | -0.02317 |
| `explicit.stat_4080418644@T2` | -0.02302 |
| `explicit.stat_328541901@T2` | -0.02263 |

### weapon.wand — n=14879, R²=-2.1108

intercept: `3.8565`  ·  log_price: True  ·  ilvl: `-0.04792`  ·  n_mods: `-0.01093`  ·  n_top_tier: `0.46144`  ·  corrupted: `-0.04309`  ·  n_sockets: `0.03046`  ·  quality: `0.00947`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 3.10303 |
| `explicit.stat_1545858329@T1` | 2.06093 |
| `explicit.stat_4226189338@T1` | 2.04307 |
| `explicit.stat_591105508@T1` | 1.88865 |
| `explicit.stat_1600707273@T1` | 1.73463 |
| `explicit.stat_124131830@T1` | 1.44079 |
| `explicit.stat_736967255@T2` | 1.00367 |
| `crafted.stat_124131830` | 0.91609 |
| `explicit.stat_3015669065@T1` | -0.53210 |
| `explicit.stat_2974417149@T1` | 0.52268 |
| `explicit.stat_2231156303@T2` | -0.51289 |
| `explicit.stat_3962278098@T2` | -0.49997 |

### weapon.bow — n=12151, R²=-1.9126

intercept: `3.4737`  ·  log_price: True  ·  ilvl: `-0.04269`  ·  n_mods: `-0.02401`  ·  n_top_tier: `0.67383`  ·  corrupted: `0.38258`  ·  n_sockets: `0.00705`  ·  quality: `0.01199`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 2.89139 |
| `desecrated.stat_210067635@T1` | -2.40065 |
| `rune.stat_3885405204` | -2.25172 |
| `crafted.stat_3035140377` | 1.50835 |
| `explicit.stat_2463230181@T1` | 1.42119 |
| `explicit.stat_1202301673@T1` | 1.38162 |
| `explicit.stat_55876295@T1` | -0.79470 |
| `explicit.stat_1037193709@T1` | -0.77298 |
| `explicit.stat_1037193709@T2` | -0.75187 |
| `explicit.stat_55876295@T2` | -0.72132 |
| `explicit.stat_3336890334@T2` | -0.71491 |
| `explicit.stat_3261801346@T1` | -0.71395 |

### weapon.crossbow — n=11423, R²=-1.8508

intercept: `3.6395`  ·  log_price: True  ·  ilvl: `-0.04494`  ·  n_mods: `-0.01102`  ·  n_top_tier: `0.70565`  ·  corrupted: `-0.03031`  ·  n_sockets: `0.02698`  ·  quality: `0.00223`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.84415 |
| `explicit.stat_2250681686@T2` | -1.43484 |
| `explicit.stat_709508406@T1` | 1.37647 |
| `explicit.stat_1202301673@T1` | 1.23130 |
| `explicit.stat_1980802737` | 1.09142 |
| `explicit.stat_1202301673@T2` | -0.93705 |
| `explicit.stat_1263695895@T2` | -0.91443 |
| `crafted.stat_3035140377` | 0.84721 |
| `explicit.stat_1509134228@T2` | -0.84512 |
| `rune.stat_55876295` | 0.78128 |
| `explicit.stat_1037193709@T2` | -0.76835 |
| `explicit.stat_2250681686` | 0.76422 |

### flask.charm — n=8923, R²=-0.4406

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.07064`  ·  corrupted: `0.69305`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.90007 |
| `explicit.stat_1056492907` | 3.40113 |
| `explicit.stat_2676834156@T1` | 1.53880 |
| `explicit.stat_2541588185@T1` | 0.40808 |
| `explicit.stat_388617051@T2` | -0.07065 |
| `explicit.stat_828533480@T2` | -0.07065 |
| `explicit.stat_2676834156@T2` | -0.07064 |
| `explicit.stat_1120862500@T2` | -0.07064 |
| `explicit.stat_1873752457@T2` | -0.07064 |
| `explicit.stat_1873752457@T1` | -0.07064 |
| `explicit.stat_828533480@T1` | -0.07064 |
| `explicit.stat_3196823591@T2` | -0.07063 |

### weapon.warstaff — n=6292, R²=-0.6146

intercept: `-0.0942`  ·  log_price: True  ·  ilvl: `0.00127`  ·  n_mods: `-0.00294`  ·  n_top_tier: `0.31731`  ·  corrupted: `0.26089`  ·  n_sockets: `0.00240`  ·  quality: `0.06704`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.27669 |
| `explicit.stat_9187492@T1` | 1.09206 |
| `rune.stat_731403740` | 0.99651 |
| `crafted.stat_210067635@T2` | -0.65504 |
| `desecrated.stat_9187492` | 0.53305 |
| `explicit.stat_1509134228@T2` | 0.43294 |
| `crafted.stat_3035140377` | 0.40174 |
| `rune.stat_1712188793` | -0.37895 |
| `explicit.stat_1037193709@T1` | 0.36519 |
| `explicit.stat_1509134228@T1` | -0.32591 |
| `explicit.stat_328541901@T1` | -0.32586 |
| `desecrated.stat_518292764` | 0.32559 |

### weapon.sceptre — n=5812, R²=-0.5336

intercept: `-7.3291`  ·  log_price: True  ·  ilvl: `0.09181`  ·  n_mods: `-0.04668`  ·  n_top_tier: `0.38376`  ·  corrupted: `1.10849`  ·  n_sockets: `0.20193`  ·  quality: `0.09189`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.14089 |
| `explicit.stat_4080418644@T1` | -0.81313 |
| `explicit.stat_4080418644@T2` | -0.70524 |
| `explicit.stat_1263695895@T2` | -0.62033 |
| `explicit.stat_2162097452@T2` | 0.60324 |
| `explicit.stat_2854751904@T1` | -0.58506 |
| `explicit.stat_1798257884@T2` | 0.57951 |
| `explicit.stat_1574590649@T2` | -0.54538 |
| `explicit.stat_1263695895@T1` | -0.52795 |
| `explicit.stat_2347036682@T2` | -0.49625 |
| `explicit.stat_3639275092@T2` | -0.45450 |
| `explicit.stat_328541901@T1` | -0.42245 |

### weapon.staff — n=5798, R²=-0.6194

intercept: `-0.7435`  ·  log_price: True  ·  ilvl: `0.00921`  ·  n_mods: `0.00009`  ·  n_top_tier: `0.11266`  ·  corrupted: `0.21328`  ·  n_sockets: `0.03381`  ·  quality: `0.02513`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 3.94570 |
| `explicit.stat_4226189338@T1` | 2.40554 |
| `explicit.stat_2254480358@T1` | 1.89633 |
| `explicit.stat_1600707273@T1` | 1.74195 |
| `explicit.stat_2254480358@T2` | 1.64671 |
| `explicit.stat_1545858329@T1` | 1.52517 |
| `explicit.stat_124131830@T1` | 1.22865 |
| `explicit.stat_4226189338@T2` | 1.19494 |
| `explicit.stat_2768835289@T2` | 0.81038 |
| `explicit.stat_3291658075@T2` | 0.75654 |
| `explicit.stat_3962278098@T2` | 0.62761 |
| `explicit.stat_2231156303@T2` | 0.58070 |

### weapon.spear — n=4893, R²=-0.6762

intercept: `-0.0748`  ·  log_price: True  ·  ilvl: `0.00098`  ·  n_mods: `-0.00041`  ·  n_top_tier: `0.28050`  ·  corrupted: `-0.00050`  ·  n_sockets: `0.00266`  ·  quality: `0.09115`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.42284 |
| `explicit.stat_9187492@T1` | 1.32929 |
| `explicit.stat_210067635@T1` | 0.82088 |
| `crafted.stat_3035140377` | 0.73270 |
| `explicit.stat_3336890334@T1` | 0.73013 |
| `crafted.stat_518292764` | 0.69366 |
| `explicit.stat_1509134228@T1` | 0.41250 |
| `explicit.stat_1037193709@T1` | 0.33012 |
| `explicit.stat_691932474@T1` | -0.28275 |
| `explicit.stat_55876295@T1` | -0.28247 |
| `explicit.stat_1202301673@T2` | -0.28165 |
| `explicit.stat_4080418644@T2` | -0.28151 |

### armour.focus — n=3922, R²=-0.5835

intercept: `-3.5066`  ·  log_price: True  ·  ilvl: `0.04322`  ·  n_mods: `-0.01552`  ·  n_top_tier: `0.74422`  ·  corrupted: `0.05083`  ·  n_sockets: `0.13652`  ·  quality: `0.09515`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 10.45608 |
| `desecrated.stat_2910761524@T1` | 4.38334 |
| `crafted.stat_737908626@T2` | -4.16958 |
| `desecrated.stat_3393628375@T1` | 2.63918 |
| `crafted.stat_2974417149@T1` | -2.03586 |
| `explicit.stat_124131830@T2` | -0.89551 |
| `explicit.stat_4220027924@T2` | -0.86895 |
| `explicit.stat_2923486259@T1` | -0.84159 |
| `explicit.stat_2891184298@T2` | -0.81653 |
| `explicit.stat_789117908@T2` | -0.80891 |
| `explicit.stat_3291658075@T1` | -0.80556 |
| `explicit.stat_736967255@T2` | -0.80439 |

### armour.quiver — n=3706, R²=-0.5857

intercept: `-2.4221`  ·  log_price: True  ·  ilvl: `0.02801`  ·  n_mods: `0.02102`  ·  n_top_tier: `1.07585`  ·  corrupted: `0.81680`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 10.86778 |
| `explicit.stat_2463230181@T2` | -1.48472 |
| `explicit.stat_681332047@T2` | -1.26196 |
| `explicit.stat_1573130764@T1` | -1.18419 |
| `explicit.stat_2194114101@T2` | -1.17166 |
| `explicit.stat_681332047@T1` | -1.15633 |
| `explicit.stat_1573130764@T2` | -1.14960 |
| `explicit.stat_1368271171@T2` | -1.12748 |
| `explicit.stat_2321178454@T2` | -1.10664 |
| `explicit.stat_3261801346@T1` | -1.09905 |
| `explicit.stat_3714003708@T2` | -1.09137 |
| `explicit.stat_1368271171@T1` | -1.08052 |

### armour.shield — n=3200, R²=-0.6245

intercept: `-0.5597`  ·  log_price: True  ·  ilvl: `0.00700`  ·  n_mods: `0.00050`  ·  n_top_tier: `0.37959`  ·  corrupted: `0.16950`  ·  n_sockets: `-0.00015`  ·  quality: `0.07703`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.86813 |
| `explicit.stat_1978899297@T2` | -0.55142 |
| `explicit.stat_1011760251@T1` | 0.44809 |
| `explicit.stat_4220027924@T1` | 0.44709 |
| `explicit.stat_328541901@T1` | -0.42061 |
| `explicit.stat_2481353198@T2` | -0.41436 |
| `explicit.stat_2481353198@T1` | -0.41402 |
| `explicit.stat_328541901@T2` | -0.40603 |
| `explicit.stat_1011760251@T2` | -0.40055 |
| `explicit.stat_2339757871@T1` | -0.39285 |
| `explicit.stat_3372524247@T2` | -0.39275 |
| `explicit.stat_2881298780@T1` | -0.39065 |

### weapon.twomace — n=2916, R²=-0.5723

intercept: `-1.5463`  ·  log_price: True  ·  ilvl: `0.01974`  ·  n_mods: `-0.00889`  ·  n_top_tier: `0.86626`  ·  corrupted: `0.72520`  ·  n_sockets: `0.03571`  ·  quality: `0.03388`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.03074 |
| `crafted.stat_3035140377` | 1.07896 |
| `explicit.stat_1037193709@T1` | -0.99089 |
| `explicit.stat_3336890334@T1` | -0.97506 |
| `explicit.stat_387439868@T2` | -0.96146 |
| `explicit.stat_1263695895@T1` | -0.94688 |
| `explicit.stat_1263695895@T2` | -0.93434 |
| `explicit.stat_1037193709@T2` | -0.92907 |
| `explicit.stat_821021828@T2` | -0.92052 |
| `explicit.stat_709508406@T1` | -0.91068 |
| `explicit.stat_3639275092@T1` | -0.90146 |
| `explicit.stat_3695891184@T1` | -0.89926 |

## Coverage (listings per base)

- … **Sapphire** — 17010 listings (16985 priced) [0.4–7553463.8 ex]
- … **Emerald** — 16769 listings (16753 priced) [0.4–7553463.8 ex]
- … **Ruby** — 12901 listings (12889 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 7337 listings (7331 priced) [0.2–5288620.9 ex]
- … **Prismatic Ring** — 5888 listings (5882 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 5732 listings (5722 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 5617 listings (5614 priced) [0.2–4323655.9 ex]
- … **Stellar Amulet** — 5528 listings (5525 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 5408 listings (5399 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 5244 listings (5240 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 4708 listings (4698 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4401 listings (4396 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 4287 listings (4284 priced) [1.0–307202867.9 ex]
- … **Ruby Ring** — 4262 listings (4260 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 3877 listings (3872 priced) [0.2–5286174.1 ex]
- … **Lapis Amulet** — 3828 listings (3826 priced) [0.2–5286174.1 ex]
- … **Ancestral Tiara** — 3792 listings (3786 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3732 listings (3731 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3730 listings (3728 priced) [0.2–4547453.5 ex]
- … **Unset Ring** — 3620 listings (3619 priced) [0.2–24532814.5 ex]
- … **Obliterator Bow** — 3618 listings (3609 priced) [0.4–42622633798.0 ex]
- … **Heavy Belt** — 3568 listings (3567 priced) [0.2–4877938.3 ex]
- … **Bloodstone Amulet** — 3515 listings (3513 priced) [0.2–4275054.0 ex]
- … **Pearl Ring** — 3406 listings (3404 priced) [0.2–24532814.5 ex]
- … **Lunar Amulet** — 3351 listings (3348 priced) [0.4–4877938.3 ex]

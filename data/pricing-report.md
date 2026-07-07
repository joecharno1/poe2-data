# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-07T08:59:00+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **268196** (267902 priced in exalted)
- Distinct bases: 942 · distinct mods: 2709 · mod rows: 1274326
- Sold signals: **32835** sold · 139929 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-07T08:50:39+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×18.59** (median |log error| 2.9227)
- Within ±30% of asking price: **15%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×50.02 · ±30% 6% · n=38303
- Premium segment (60ex+): skill **+0.07** · typical error ×236.56 · ±30% 0% · n=23546

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 4975 | ×49.53 | 18% | +0.02 | +0.04 |
| accessory.amulet | 4789 | ×50.47 | 21% | +0.01 | +0.02 |
| jewel | 4337 | ×8.46 | 7% | +0.01 | +0.03 |
| accessory.belt | 3954 | ×11.78 | 6% | +0.04 | +0.04 |
| armour.chest | 3904 | ×10.30 | 6% | +0.03 | +0.05 |
| armour.helmet | 3798 | ×9.39 | 7% | +0.02 | +0.02 |
| armour.boots | 3612 | ×12.59 | 9% | +0.12 | +0.15 |
| armour.gloves | 3548 | ×18.01 | 6% | +0.09 | +0.12 |
| other | 3283 | ×9.99 | 39% | +0.06 | +0.16 |
| weapon.wand | 2440 | ×23.53 | 22% | +0.07 | +0.06 |
| weapon.bow | 2022 | ×15.18 | 18% | +0.10 | +0.11 |
| weapon.crossbow | 1885 | ×16.44 | 18% | +0.08 | +0.11 |
| weapon.warstaff | 804 | ×78.40 | 21% | +0.01 | +0.01 |
| weapon.sceptre | 725 | ×82.11 | 17% | +0.01 | +0.02 |
| weapon.staff | 687 | ×55.00 | 22% | +0.03 | +0.01 |
| weapon.spear | 630 | ×57.00 | 22% | +0.01 | +0.00 |
| armour.quiver | 500 | ×82.11 | 17% | +0.00 | +0.02 |
| armour.focus | 496 | ×59.99 | 16% | +0.02 | +0.03 |
| armour.shield | 426 | ×20.00 | 22% | +0.01 | +0.01 |
| weapon.twomace | 375 | ×20.00 | 23% | +0.08 | +0.02 |
| flask.charm | 334 | ×1.00 | 51% | -0.00 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=28712, R²=-0.5776

intercept: `1.6052`  ·  log_price: True  ·  ilvl: `0.00005`  ·  n_mods: `0.02069`  ·  n_top_tier: `0.32776`  ·  corrupted: `1.08436`  ·  n_sockets: `-0.00008`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_2891184298@T1` | 1.28353 |
| `explicit.stat_2974417149@T1` | 0.93179 |
| `explicit.stat_3291658075@T1` | 0.66934 |
| `explicit.stat_3917489142@T1` | 0.60288 |
| `explicit.stat_2106365538@T1` | 0.54363 |
| `explicit.stat_1050105434@T1` | -0.49786 |
| `explicit.stat_101878827@T1` | 0.34430 |
| `implicit.stat_1379411836` | -0.27131 |
| `explicit.stat_1589917703@T1` | 0.24787 |
| `implicit.stat_4041853756` | 0.22824 |
| `implicit.stat_3879011313` | 0.22818 |
| `explicit.stat_2901986750` | 0.14828 |

### jewel — n=23133, R²=-0.6597

intercept: `-1.0260`  ·  log_price: True  ·  ilvl: `0.03677`  ·  n_mods: `0.11494`  ·  n_top_tier: `-0.02302`  ·  corrupted: `0.32498`  ·  quality: `0.21178`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.97694 |
| `explicit.stat_3714003708@T1` | -3.76248 |
| `explicit.stat_1569101201@T1` | 3.65665 |
| `explicit.stat_1869147066@T1` | 3.54957 |
| `explicit.stat_1697951953@T1` | -3.39623 |
| `explicit.stat_1316278494@T1` | -3.31193 |
| `explicit.stat_1854213750@T1` | -3.24387 |
| `explicit.stat_21071013@T1` | -3.12845 |
| `explicit.stat_3174700878@T1` | 2.32342 |
| `explicit.stat_2527686725@T1` | 2.15667 |
| `explicit.stat_3283482523@T1` | -2.11160 |
| `explicit.stat_1405298142@T1` | 2.07968 |

### accessory.ring — n=23023, R²=-2.0676

intercept: `5.0474`  ·  log_price: True  ·  ilvl: `-0.05984`  ·  n_mods: `-0.01816`  ·  n_top_tier: `-0.15394`  ·  corrupted: `0.62332`  ·  n_sockets: `3.47753`  ·  quality: `0.09732`

| stat_id | coef |
|---|---|
| `explicit.stat_1379411836@T1` | -0.73680 |
| `explicit.stat_707457662@T1` | 0.64623 |
| `explicit.stat_1379411836@T2` | -0.51821 |
| `explicit.stat_1671376347@T1` | 0.49581 |
| `explicit.stat_328541901@T1` | 0.45065 |
| `explicit.stat_4080418644@T2` | 0.44562 |
| `explicit.stat_707457662@T2` | 0.42537 |
| `explicit.stat_1573130764@T2` | 0.36930 |
| `explicit.stat_2923486259@T2` | 0.34674 |
| `explicit.stat_2923486259@T1` | 0.34649 |
| `explicit.stat_1754445556@T1` | 0.34421 |
| `explicit.stat_3032590688@T1` | 0.34245 |

### accessory.amulet — n=21963, R²=-2.1186

intercept: `4.1651`  ·  log_price: True  ·  ilvl: `-0.05031`  ·  n_mods: `-0.02788`  ·  n_top_tier: `1.13917`  ·  corrupted: `0.10260`  ·  n_sockets: `2.18161`  ·  quality: `-0.00694`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | -2.79469 |
| `explicit.stat_983749596@T1` | -1.72122 |
| `explicit.stat_983749596@T2` | -1.61581 |
| `explicit.stat_3299347043@T1` | -1.58348 |
| `explicit.stat_2748665614@T1` | -1.27819 |
| `explicit.stat_2748665614@T2` | -1.26016 |
| `explicit.stat_3299347043@T2` | -1.24812 |
| `explicit.stat_3325883026@T1` | -1.24357 |
| `explicit.stat_3917489142@T2` | -1.24113 |
| `explicit.stat_3917489142@T1` | -1.22461 |
| `explicit.stat_3489782002@T2` | -1.21134 |
| `explicit.stat_3325883026@T2` | -1.20062 |

### accessory.belt — n=18261, R²=-0.3282

intercept: `5.8724`  ·  log_price: True  ·  ilvl: `-0.03777`  ·  n_mods: `-0.41226`  ·  n_top_tier: `0.54558`  ·  corrupted: `0.45632`  ·  n_sockets: `-1.46222`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.88991 |
| `implicit.stat_731781020` | -1.36247 |
| `explicit.stat_1389754388@T1` | -1.21321 |
| `explicit.stat_644456512@T1` | -0.86170 |
| `explicit.stat_2923486259@T2` | -0.83150 |
| `explicit.stat_809229260@T2` | -0.79884 |
| `explicit.stat_2881298780@T1` | -0.79344 |
| `explicit.stat_915769802@T2` | -0.78806 |
| `explicit.stat_3325883026@T1` | -0.72603 |
| `explicit.stat_51994685@T1` | -0.72189 |
| `explicit.stat_644456512@T2` | -0.72142 |
| `explicit.stat_2923486259@T1` | -0.69572 |

### armour.chest — n=18042, R²=-0.7676

intercept: `4.0333`  ·  log_price: True  ·  ilvl: `-0.04392`  ·  n_mods: `-0.12904`  ·  n_top_tier: `0.55859`  ·  corrupted: `0.21017`  ·  n_sockets: `0.07090`  ·  quality: `0.01974`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.48029 |
| `explicit.stat_915769802@T1` | -1.03654 |
| `explicit.stat_3033371881@T2` | -1.01661 |
| `explicit.stat_3261801346@T1` | -0.99824 |
| `explicit.stat_3321629045@T1` | -0.89031 |
| `explicit.stat_3261801346@T2` | -0.86652 |
| `explicit.stat_4015621042@T1` | -0.84071 |
| `explicit.stat_3325883026@T2` | -0.79304 |
| `explicit.stat_986397080@T2` | -0.78890 |
| `explicit.stat_3484657501@T1` | -0.77268 |
| `explicit.stat_3372524247@T2` | -0.76154 |
| `explicit.stat_4080418644@T2` | -0.73624 |

### armour.helmet — n=17698, R²=-0.4907

intercept: `3.8607`  ·  log_price: True  ·  ilvl: `-0.03648`  ·  n_mods: `-0.13819`  ·  n_top_tier: `0.38367`  ·  corrupted: `0.75991`  ·  n_sockets: `-0.03336`  ·  quality: `0.01846`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.99386 |
| `explicit.stat_4080418644@T2` | -1.15833 |
| `explicit.stat_1062208444@T2` | -1.13934 |
| `explicit.stat_53045048@T1` | -0.69908 |
| `explicit.stat_328541901@T2` | -0.63365 |
| `explicit.stat_53045048@T2` | -0.61522 |
| `explicit.stat_3484657501@T2` | -0.58478 |
| `explicit.stat_2451402625@T1` | -0.52881 |
| `explicit.stat_2162097452@T2` | -0.49285 |
| `explicit.stat_2451402625@T2` | -0.48890 |
| `explicit.stat_1050105434@T1` | -0.48119 |
| `explicit.stat_803737631@T2` | -0.46897 |

### armour.boots — n=16624, R²=-0.931

intercept: `4.2011`  ·  log_price: True  ·  ilvl: `-0.05088`  ·  n_mods: `-0.09989`  ·  n_top_tier: `0.60978`  ·  corrupted: `0.50246`  ·  n_sockets: `0.18210`  ·  quality: `0.01612`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.87174 |
| `rune.stat_836936635` | -1.32754 |
| `explicit.stat_2250533757@T1` | 1.32334 |
| `explicit.stat_3362812763@T1` | -1.07091 |
| `explicit.stat_2923486259@T2` | -0.98002 |
| `explicit.stat_99927264@T1` | -0.95737 |
| `explicit.stat_1062208444@T2` | -0.90898 |
| `explicit.stat_328541901@T1` | -0.88783 |
| `explicit.stat_2160282525@T1` | -0.85974 |
| `explicit.stat_3362812763@T2` | -0.83144 |
| `explicit.stat_3917489142@T2` | -0.80343 |
| `explicit.stat_2160282525@T2` | -0.78347 |

### armour.gloves — n=16316, R²=-1.0064

intercept: `3.4285`  ·  log_price: True  ·  ilvl: `-0.04878`  ·  n_mods: `-0.02994`  ·  n_top_tier: `0.31801`  ·  corrupted: `0.19420`  ·  n_sockets: `0.36142`  ·  quality: `0.00680`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.59180 |
| `explicit.stat_803737631@T1` | -0.88418 |
| `explicit.stat_681332047@T2` | -0.85450 |
| `explicit.stat_803737631@T2` | -0.84496 |
| `explicit.stat_3033371881@T2` | -0.82521 |
| `explicit.stat_124859000@T1` | -0.81939 |
| `explicit.stat_3484657501@T2` | -0.75270 |
| `explicit.stat_1999113824@T1` | 0.72295 |
| `explicit.stat_9187492@T1` | 0.66742 |
| `explicit.stat_53045048@T1` | -0.64926 |
| `explicit.stat_3033371881@T1` | -0.63389 |
| `explicit.stat_328541901@T1` | -0.59921 |

### weapon.wand — n=11377, R²=-1.9596

intercept: `3.6437`  ·  log_price: True  ·  ilvl: `-0.04555`  ·  n_mods: `-0.00725`  ·  n_top_tier: `0.38983`  ·  corrupted: `0.10501`  ·  n_sockets: `0.00572`  ·  quality: `0.01875`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.66666 |
| `explicit.stat_2254480358@T1` | 2.06720 |
| `explicit.stat_591105508@T1` | 2.02658 |
| `explicit.stat_4226189338@T1` | 2.00488 |
| `explicit.stat_1600707273@T1` | 1.88385 |
| `explicit.stat_1545858329@T1` | 1.57367 |
| `explicit.stat_736967255@T2` | 1.15071 |
| `crafted.stat_124131830` | 0.86837 |
| `explicit.stat_1600707273@T2` | 0.76463 |
| `explicit.stat_737908626@T1` | -0.47371 |
| `explicit.stat_2968503605@T2` | -0.42350 |
| `explicit.stat_473429811@T1` | -0.41800 |

### weapon.bow — n=9316, R²=-1.8235

intercept: `3.4737`  ·  log_price: True  ·  ilvl: `-0.04313`  ·  n_mods: `-0.01243`  ·  n_top_tier: `0.56478`  ·  corrupted: `-0.03500`  ·  n_sockets: `0.00708`  ·  quality: `0.00424`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.80634 |
| `explicit.stat_2463230181@T1` | 1.71269 |
| `explicit.stat_1202301673@T1` | 1.62205 |
| `explicit.stat_518292764@T1` | 1.38808 |
| `crafted.stat_3035140377` | 1.12090 |
| `explicit.stat_55876295@T1` | -0.64080 |
| `explicit.stat_2694482655@T1` | -0.62953 |
| `explicit.stat_669069897@T2` | -0.61699 |
| `explicit.stat_3261801346@T1` | -0.61051 |
| `explicit.stat_1368271171@T2` | -0.60919 |
| `explicit.stat_55876295@T2` | -0.60544 |
| `explicit.stat_1037193709@T1` | -0.60428 |

### weapon.crossbow — n=8799, R²=-1.6779

intercept: `3.6925`  ·  log_price: True  ·  ilvl: `-0.04604`  ·  n_mods: `-0.00680`  ·  n_top_tier: `0.57552`  ·  corrupted: `-0.05555`  ·  n_sockets: `0.01951`  ·  quality: `0.00580`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 1.66386 |
| `explicit.stat_709508406@T1` | 1.63157 |
| `explicit.stat_1202301673@T1` | 1.59511 |
| `explicit.stat_2250681686@T2` | -1.45065 |
| `explicit.stat_1509134228@T1` | 1.25114 |
| `rune.stat_55876295` | 1.09250 |
| `rune.stat_2246411426` | -0.99250 |
| `crafted.stat_3035140377` | 0.97389 |
| `explicit.stat_2250681686` | 0.92250 |
| `explicit.stat_1202301673@T2` | -0.69560 |
| `explicit.stat_691932474@T1` | -0.69248 |
| `explicit.stat_669069897@T2` | -0.66627 |

### flask.charm — n=5217, R²=-0.2256

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00019`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.04276 |
| `explicit.stat_1056492907` | 2.99575 |
| `explicit.stat_2676834156@T1` | 0.55278 |
| `explicit.stat_3138344128` | 0.02221 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_828533480@T2` | -0.00003 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_828533480@T1` | -0.00003 |
| `explicit.stat_388617051@T2` | -0.00003 |
| `explicit.stat_3196823591@T2` | -0.00003 |
| `explicit.stat_2541588185@T2` | -0.00003 |
| `explicit.stat_1120862500@T2` | -0.00002 |

### weapon.warstaff — n=3797, R²=-0.4427

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | -5.38735 |
| `desecrated.stat_2231156303@T1` | -5.38735 |
| `rune.stat_243313994` | 3.29830 |
| `rune.stat_731403740` | 1.59921 |
| `rune.stat_1712188793` | -1.11401 |
| `desecrated.stat_9187492` | 0.80785 |
| `desecrated.stat_2527686725` | 0.24680 |
| `rune.stat_3336890334` | 0.19958 |
| `desecrated.stat_518292764` | 0.18136 |
| `rune.stat_2430860292` | -0.10245 |
| `desecrated.stat_2231156303` | 0.08224 |
| `rune.stat_1509134228` | 0.03777 |

### weapon.sceptre — n=3555, R²=-0.4381

intercept: `-0.0008`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.72476`  ·  n_sockets: `0.00001`  ·  quality: `0.03578`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.30250 |
| `rune.stat_1611856026` | 0.07429 |
| `rune.stat_3984865854` | 0.06452 |
| `rune.stat_1798257884` | 0.03118 |
| `rune.stat_3412619569` | 0.03118 |
| `desecrated.stat_1798257884` | 0.01829 |
| `desecrated.stat_1050105434` | 0.01110 |
| `desecrated.stat_3984865854` | 0.00203 |
| `explicit.stat_1263695895@T1` | 0.00005 |
| `explicit.stat_1250712710@T1` | -0.00005 |
| `explicit.stat_3984865854@T2` | -0.00005 |
| `explicit.stat_2347036682@T2` | -0.00004 |

### weapon.staff — n=3524, R²=-0.4764

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.64575 |
| `crafted.stat_124131830` | 0.22509 |
| `explicit.stat_2254480358@T1` | 0.18641 |
| `rune.stat_3990135792` | -0.15195 |
| `rune.stat_975988108` | -0.13553 |
| `rune.stat_2974417149` | 0.08760 |
| `explicit.stat_1600707273@T1` | 0.00259 |
| `explicit.stat_473429811@T1` | 0.00101 |
| `explicit.stat_2254480358@T2` | 0.00009 |
| `explicit.stat_124131830@T1` | 0.00007 |
| `explicit.stat_124131830@T2` | 0.00004 |
| `explicit.stat_3962278098@T2` | 0.00003 |

### weapon.spear — n=3089, R²=-0.483

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00002`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.66864 |
| `explicit.stat_210067635@T1` | 0.26512 |
| `rune.stat_1039491398` | 0.22532 |
| `rune.stat_1509134228` | -0.18933 |
| `crafted.stat_210067635` | 0.00965 |
| `explicit.stat_1202301673@T1` | 0.00016 |
| `explicit.stat_3639275092@T1` | 0.00005 |
| `explicit.stat_709508406@T1` | 0.00004 |
| `explicit.stat_2694482655@T1` | 0.00004 |
| `explicit.stat_1509134228@T1` | 0.00004 |
| `explicit.stat_3336890334@T2` | 0.00004 |
| `explicit.stat_3336890334@T1` | 0.00004 |

### armour.focus — n=2453, R²=-0.3946

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.01015`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00002`  ·  quality: `0.00006`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.52288 |
| `crafted.stat_737908626@T2` | -1.81493 |
| `crafted.stat_2974417149@T1` | -1.26833 |
| `desecrated.stat_3393628375` | 0.53660 |
| `pseudo.total_chaos_res` | 0.14831 |
| `explicit.stat_2923486259` | -0.14831 |
| `crafted.stat_737908626` | 0.09555 |
| `crafted.stat_4015621042` | 0.06671 |
| `crafted.stat_2974417149` | 0.05678 |
| `rune.stat_3523867985` | 0.03813 |
| `desecrated.stat_4052037485` | 0.02697 |
| `explicit.stat_2923486259@T1` | -0.01017 |

### armour.quiver — n=2358, R²=-0.5107

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00757`  ·  corrupted: `0.00003`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 4.88587 |
| `desecrated.stat_3932115504` | -0.30434 |
| `desecrated.stat_2194114101` | 0.18629 |
| `desecrated.stat_3714003708` | 0.06523 |
| `explicit.stat_3759663284@T1` | 0.02862 |
| `desecrated.stat_3759663284` | 0.01136 |
| `explicit.stat_681332047@T2` | -0.00760 |
| `explicit.stat_681332047@T1` | -0.00759 |
| `explicit.stat_2321178454@T2` | -0.00759 |
| `explicit.stat_803737631@T2` | -0.00758 |
| `explicit.stat_3714003708@T2` | -0.00758 |
| `explicit.stat_1573130764@T1` | -0.00758 |

### armour.shield — n=2082, R²=-0.4356

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.13988`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00185`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.84606 |
| `explicit.stat_1301765461@T1` | 0.55320 |
| `explicit.stat_1978899297@T2` | -0.34003 |
| `explicit.stat_1978899297` | 0.20013 |
| `explicit.stat_1011760251@T1` | -0.14020 |
| `explicit.stat_1011760251@T2` | -0.14008 |
| `explicit.stat_2481353198@T1` | -0.13993 |
| `explicit.stat_2481353198@T2` | -0.13991 |
| `explicit.stat_3484657501@T1` | -0.13990 |
| `explicit.stat_3639275092@T2` | -0.13989 |
| `explicit.stat_1062208444@T2` | -0.13989 |
| `explicit.stat_1301765461@T2` | -0.13989 |

### weapon.twomace — n=1795, R²=-0.3985

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.03559`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1509134228@T1` | 2.39108 |
| `explicit.stat_518292764@T1` | 2.26694 |
| `desecrated.stat_210067635@T1` | 0.99391 |
| `explicit.stat_1509134228@T1` | 0.65754 |
| `rune.stat_1039491398` | 0.12770 |
| `desecrated.stat_1940865751` | 0.09413 |
| `rune.stat_1509134228` | -0.04612 |
| `explicit.stat_3336890334@T1` | -0.03567 |
| `explicit.stat_1037193709@T1` | -0.03564 |
| `explicit.stat_1037193709@T2` | -0.03562 |
| `explicit.stat_387439868@T2` | -0.03562 |
| `explicit.stat_1940865751@T2` | -0.03561 |

## Coverage (listings per base)

- … **Emerald** — 11083 listings (11075 priced) [0.6–7553463.8 ex]
- … **Sapphire** — 11065 listings (11051 priced) [0.3–7553463.8 ex]
- … **Ruby** — 8602 listings (8592 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 5444 listings (5440 priced) [0.3–4877938.3 ex]
- … **Stellar Amulet** — 4088 listings (4088 priced) [0.3–35690283.3 ex]
- … **Prismatic Ring** — 4043 listings (4042 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 3959 listings (3953 priced) [0.3–66666666.0 ex]
- … **Amethyst Ring** — 3834 listings (3833 priced) [0.3–71450.3 ex]
- … **Gold Amulet** — 3789 listings (3789 priced) [0.3–292542.5 ex]
- … **Gold Ring** — 3675 listings (3674 priced) [0.3–24532814.5 ex]
- … **Dueling Wand** — 3565 listings (3561 priced) [0.3–3736768402.2 ex]
- … **Sapphire Ring** — 3041 listings (3039 priced) [0.3–24532814.5 ex]
- … **Topaz Ring** — 2971 listings (2970 priced) [1.0–123132003.2 ex]
- … **Ruby Ring** — 2950 listings (2950 priced) [0.3–37474957.5 ex]
- … **Plate Belt** — 2763 listings (2761 priced) [0.3–4877938.3 ex]
- … **Obliterator Bow** — 2695 listings (2689 priced) [0.4–22139622146.9 ex]
- … **Ancestral Tiara** — 2656 listings (2654 priced) [0.6–37474957.5 ex]
- … **Lapis Amulet** — 2652 listings (2652 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 2621 listings (2620 priced) [0.3–113795639.4 ex]
- … **Jade Amulet** — 2617 listings (2616 priced) [0.3–4547453.5 ex]
- … **Heavy Belt** — 2614 listings (2614 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 2463 listings (2463 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 2424 listings (2424 priced) [0.3–14638.0 ex]
- … **Pearl Ring** — 2378 listings (2378 priced) [0.3–24532814.5 ex]
- … **Azure Amulet** — 2335 listings (2335 priced) [0.3–123132003.2 ex]

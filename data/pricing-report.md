# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-06T21:30:54+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **244312** (244121 priced in exalted)
- Distinct bases: 935 · distinct mods: 2654 · mod rows: 1160579
- Sold signals: **34152** sold · 128787 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-06T21:24:05+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×14.90** (median |log error| 2.7015)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 77% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.09** · typical error ×43.73 · ±30% 9% · n=35203
- Premium segment (60ex+): skill **+0.09** · typical error ×238.22 · ±30% 0% · n=21134

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 4563 | ×13.87 | 4% | +0.03 | +0.05 |
| accessory.amulet | 4393 | ×56.76 | 20% | +0.02 | +0.03 |
| jewel | 3840 | ×9.03 | 6% | +0.04 | +0.07 |
| accessory.belt | 3654 | ×11.78 | 21% | +0.04 | +0.08 |
| armour.chest | 3599 | ×10.27 | 22% | +0.05 | +0.08 |
| armour.helmet | 3443 | ×13.43 | 18% | +0.06 | +0.08 |
| armour.boots | 3308 | ×10.00 | 27% | +0.00 | +0.00 |
| armour.gloves | 3249 | ×10.00 | 26% | +0.00 | +0.01 |
| other | 3006 | ×10.00 | 34% | +0.13 | +0.40 |
| weapon.wand | 2280 | ×22.34 | 21% | +0.06 | +0.04 |
| weapon.bow | 1888 | ×11.13 | 18% | +0.09 | +0.11 |
| weapon.crossbow | 1775 | ×11.62 | 17% | +0.09 | +0.10 |
| weapon.sceptre | 658 | ×50.00 | 18% | +0.00 | +0.01 |
| weapon.warstaff | 650 | ×50.00 | 25% | +0.01 | +0.00 |
| weapon.staff | 596 | ×54.09 | 18% | +0.01 | -0.00 |
| weapon.spear | 545 | ×51.00 | 19% | +0.00 | +0.00 |
| armour.focus | 449 | ×50.00 | 16% | +0.00 | -0.00 |
| armour.quiver | 446 | ×40.00 | 16% | +0.00 | +0.00 |
| armour.shield | 392 | ×10.00 | 20% | -0.00 | +0.03 |
| flask.charm | 357 | ×1.00 | 50% | -0.00 | -0.00 |
| weapon.twomace | 335 | ×12.11 | 21% | +0.03 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=26742, R²=-0.365

intercept: `1.6065`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `0.08567`  ·  n_top_tier: `1.21076`  ·  corrupted: `2.30033`  ·  n_sockets: `-0.00027`  ·  quality: `-0.00003`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 2.78528 |
| `explicit.stat_1050105434@T1` | -2.63246 |
| `explicit.stat_2891184298@T1` | 2.60450 |
| `explicit.stat_3141070085@T1` | 2.38055 |
| `explicit.stat_1589917703@T1` | 2.34570 |
| `explicit.stat_101878827@T1` | 2.31130 |
| `explicit.stat_3917489142@T1` | 2.27012 |
| `explicit.stat_2106365538@T1` | 2.10587 |
| `explicit.stat_789117908@T1` | -1.75825 |
| `explicit.stat_2974417149@T1` | 1.10661 |
| `explicit.stat_3299347043@T1` | 0.37974 |
| `explicit.stat_2968503605@T1` | 0.34976 |

### accessory.ring — n=20843, R²=-1.2475

intercept: `4.5384`  ·  log_price: True  ·  ilvl: `-0.03981`  ·  n_mods: `-0.15662`  ·  n_top_tier: `-0.12889`  ·  corrupted: `0.64317`  ·  n_sockets: `0.74661`  ·  quality: `0.04587`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 5.15425 |
| `explicit.stat_707457662@T2` | 3.77980 |
| `explicit.stat_1379411836@T1` | -2.11447 |
| `explicit.stat_2557965901@T1` | 1.52557 |
| `explicit.stat_2557965901@T2` | 1.44567 |
| `explicit.stat_1379411836@T2` | -1.43509 |
| `explicit.stat_2923486259@T2` | 1.14888 |
| `explicit.stat_736967255@T1` | 0.92592 |
| `explicit.stat_1368271171@T2` | -0.79794 |
| `explicit.stat_707457662` | -0.71793 |
| `explicit.stat_2923486259@T1` | 0.71775 |
| `explicit.stat_328541901@T1` | 0.71511 |

### jewel — n=20524, R²=-0.6184

intercept: `-1.1123`  ·  log_price: True  ·  ilvl: `0.03845`  ·  n_mods: `0.11369`  ·  n_top_tier: `-0.05747`  ·  corrupted: `0.31520`  ·  quality: `0.20991`

| stat_id | coef |
|---|---|
| `explicit.stat_3714003708@T1` | -3.47884 |
| `explicit.stat_1316278494@T1` | -3.23478 |
| `explicit.stat_1697951953@T1` | -2.79628 |
| `explicit.stat_3473929743@T1` | 2.78554 |
| `explicit.stat_1569101201@T1` | 2.54470 |
| `explicit.stat_1869147066@T1` | 2.44651 |
| `explicit.stat_21071013@T1` | -2.10497 |
| `explicit.stat_872504239@T1` | -1.84227 |
| `explicit.stat_818778753@T1` | -1.81988 |
| `explicit.stat_3283482523@T1` | -1.71399 |
| `explicit.stat_3544800472@T1` | -1.63676 |
| `explicit.stat_234296660@T1` | -1.63051 |

### accessory.amulet — n=19937, R²=-2.0719

intercept: `4.4146`  ·  log_price: True  ·  ilvl: `-0.05369`  ·  n_mods: `-0.02517`  ·  n_top_tier: `1.13135`  ·  corrupted: `0.09091`  ·  n_sockets: `2.00973`  ·  quality: `-0.07700`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.53226 |
| `explicit.stat_983749596@T1` | -1.47923 |
| `explicit.stat_983749596@T2` | -1.45969 |
| `explicit.stat_3299347043@T2` | -1.34172 |
| `explicit.stat_1202301673@T2` | -1.32562 |
| `explicit.stat_3917489142@T1` | -1.24948 |
| `explicit.stat_3917489142@T2` | -1.24575 |
| `explicit.stat_2748665614@T1` | -1.21816 |
| `explicit.stat_3325883026@T1` | -1.21309 |
| `explicit.stat_1671376347@T2` | -1.20817 |
| `explicit.stat_3489782002@T2` | -1.20750 |
| `explicit.stat_4080418644@T1` | -1.20724 |

### accessory.belt — n=16755, R²=-1.3761

intercept: `3.5722`  ·  log_price: True  ·  ilvl: `-0.04295`  ·  n_mods: `-0.01923`  ·  n_top_tier: `0.40654`  ·  corrupted: `0.35691`  ·  n_sockets: `-0.10668`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.20452 |
| `explicit.stat_809229260@T2` | -0.44527 |
| `explicit.stat_1389754388@T1` | -0.44385 |
| `explicit.stat_3299347043@T2` | -0.43329 |
| `explicit.stat_3325883026@T1` | -0.43178 |
| `explicit.stat_3299347043@T1` | -0.43050 |
| `explicit.stat_2881298780@T1` | -0.42897 |
| `explicit.stat_644456512@T2` | -0.42881 |
| `explicit.stat_4220027924@T2` | -0.42236 |
| `explicit.stat_915769802@T2` | -0.42071 |
| `explicit.stat_915769802@T1` | -0.42038 |
| `explicit.stat_1412217137@T2` | -0.41389 |

### armour.chest — n=16599, R²=-1.4035

intercept: `3.7817`  ·  log_price: True  ·  ilvl: `-0.04666`  ·  n_mods: `-0.02117`  ·  n_top_tier: `0.53877`  ·  corrupted: `0.06360`  ·  n_sockets: `0.01714`  ·  quality: `0.02102`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.81240 |
| `explicit.stat_4015621042@T1` | -0.67291 |
| `explicit.stat_4080418644@T2` | -0.62396 |
| `explicit.stat_915769802@T1` | -0.59885 |
| `explicit.stat_3325883026@T2` | -0.58079 |
| `explicit.stat_3261801346@T2` | -0.57606 |
| `explicit.stat_1692879867@T1` | -0.57506 |
| `explicit.stat_4080418644@T1` | -0.57156 |
| `explicit.stat_3321629045@T1` | -0.57072 |
| `explicit.stat_1999113824@T1` | -0.56943 |
| `explicit.stat_2451402625@T1` | -0.56638 |
| `explicit.stat_4220027924@T2` | -0.56589 |

### armour.helmet — n=16235, R²=-1.3782

intercept: `4.6157`  ·  log_price: True  ·  ilvl: `-0.05770`  ·  n_mods: `-0.03267`  ·  n_top_tier: `0.57840`  ·  corrupted: `0.53523`  ·  n_sockets: `0.01477`  ·  quality: `0.02261`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.97599 |
| `explicit.stat_2339757871@T1` | -2.82333 |
| `explicit.stat_53045048@T1` | -0.84052 |
| `explicit.stat_4015621042@T2` | -0.73004 |
| `explicit.stat_1263695895@T1` | -0.70240 |
| `explicit.stat_53045048@T2` | -0.67740 |
| `explicit.stat_1062208444@T2` | -0.65909 |
| `explicit.stat_2162097452@T2` | -0.65710 |
| `explicit.stat_328541901@T2` | -0.64720 |
| `explicit.stat_587431675@T2` | -0.63865 |
| `explicit.stat_803737631@T2` | -0.63763 |
| `explicit.stat_4052037485@T2` | -0.63679 |

### armour.boots — n=15296, R²=-0.2349

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.38362`  ·  corrupted: `0.00250`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2250533757@T2` | -0.41592 |
| `explicit.stat_2339757871@T1` | -0.38370 |
| `explicit.stat_2451402625@T2` | -0.38363 |
| `explicit.stat_3917489142@T2` | -0.38363 |
| `explicit.stat_3362812763@T2` | -0.38363 |
| `explicit.stat_2923486259@T2` | -0.38363 |
| `explicit.stat_3261801346@T2` | -0.38363 |
| `explicit.stat_3362812763@T1` | -0.38363 |
| `explicit.stat_3325883026@T1` | -0.38362 |
| `explicit.stat_99927264@T1` | -0.38362 |
| `explicit.stat_99927264@T2` | -0.38362 |
| `explicit.stat_124859000@T2` | -0.38362 |

### armour.gloves — n=15033, R²=-0.293

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00081`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.10539 |
| `desecrated.stat_4067062424` | 0.07337 |
| `pseudo.total_life` | 0.01018 |
| `explicit.stat_3299347043` | -0.01018 |
| `rune.stat_3299347043` | -0.01018 |
| `pseudo.total_ele_res>=80` | 0.00760 |
| `desecrated.stat_3299347043` | -0.00521 |
| `explicit.stat_3372524247@T1` | 0.00278 |
| `explicit.stat_4067062424@T1` | 0.00064 |
| `desecrated.stat_1573130764` | 0.00029 |
| `explicit.stat_9187492@T1` | 0.00025 |
| `explicit.stat_2339757871@T1` | -0.00021 |

### weapon.wand — n=10631, R²=-1.925

intercept: `3.5948`  ·  log_price: True  ·  ilvl: `-0.04493`  ·  n_mods: `-0.00549`  ·  n_top_tier: `0.32272`  ·  corrupted: `0.05790`  ·  n_sockets: `-0.00305`  ·  quality: `0.02123`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.70239 |
| `explicit.stat_2254480358@T1` | 2.11586 |
| `explicit.stat_591105508@T1` | 2.07811 |
| `explicit.stat_4226189338@T1` | 2.06563 |
| `explicit.stat_1600707273@T1` | 1.84856 |
| `explicit.stat_1545858329@T1` | 1.25517 |
| `explicit.stat_1600707273@T2` | 0.90453 |
| `crafted.stat_124131830` | 0.76513 |
| `explicit.stat_736967255@T2` | 0.75298 |
| `explicit.stat_3962278098@T2` | -0.39147 |
| `explicit.stat_737908626@T2` | -0.36477 |
| `explicit.stat_737908626@T1` | -0.35853 |

### weapon.bow — n=8717, R²=-1.7772

intercept: `3.4481`  ·  log_price: True  ·  ilvl: `-0.04279`  ·  n_mods: `-0.01556`  ·  n_top_tier: `0.44477`  ·  corrupted: `-0.03170`  ·  n_sockets: `0.00630`  ·  quality: `0.00453`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | 1.75672 |
| `explicit.stat_1202301673@T1` | 1.75042 |
| `desecrated.stat_210067635@T1` | -1.68684 |
| `explicit.stat_518292764@T1` | 1.26918 |
| `crafted.stat_3035140377` | 1.18683 |
| `desecrated.stat_666077204@T1` | 0.65561 |
| `explicit.stat_55876295@T1` | -0.56075 |
| `explicit.stat_2694482655@T1` | -0.52424 |
| `explicit.stat_1037193709@T1` | -0.52152 |
| `explicit.stat_55876295@T2` | -0.51523 |
| `rune.stat_3885405204` | -0.51393 |
| `explicit.stat_3261801346@T1` | -0.50804 |

### weapon.crossbow — n=8256, R²=-1.5577

intercept: `3.5227`  ·  log_price: True  ·  ilvl: `-0.04403`  ·  n_mods: `-0.01399`  ·  n_top_tier: `0.69264`  ·  corrupted: `0.01593`  ·  n_sockets: `0.01973`  ·  quality: `0.00705`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 1.50208 |
| `explicit.stat_709508406@T1` | 1.48258 |
| `explicit.stat_2250681686@T2` | -1.38215 |
| `explicit.stat_1509134228@T1` | 1.37696 |
| `explicit.stat_1202301673@T1` | 1.32787 |
| `crafted.stat_3035140377` | 1.00883 |
| `explicit.stat_691932474@T1` | -0.99977 |
| `explicit.stat_2250681686` | 0.89526 |
| `explicit.stat_1202301673@T2` | -0.89119 |
| `explicit.stat_669069897@T2` | -0.87547 |
| `explicit.stat_669069897@T1` | -0.84854 |
| `rune.stat_55876295` | 0.82875 |

### flask.charm — n=4377, R²=-0.1485

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00004`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60746 |
| `explicit.stat_1056492907` | 2.99570 |
| `explicit.stat_3138344128` | 0.01956 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_3196823591@T2` | -0.00003 |
| `explicit.stat_388617051@T2` | -0.00003 |
| `explicit.stat_2541588185@T2` | -0.00003 |
| `explicit.stat_828533480@T1` | -0.00003 |
| `explicit.stat_828533480@T2` | -0.00003 |
| `explicit.stat_2676834156@T2` | -0.00003 |
| `explicit.stat_1873752457` | 0.00002 |

### weapon.warstaff — n=3257, R²=-0.3961

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | -3.41320 |
| `desecrated.stat_2231156303@T1` | -3.41320 |
| `rune.stat_243313994` | 2.30051 |
| `rune.stat_1037193709` | 0.28502 |
| `desecrated.stat_2527686725` | 0.27185 |
| `rune.stat_3336890334` | 0.23021 |
| `rune.stat_2430860292` | -0.11894 |
| `rune.stat_1817052494` | -0.11401 |
| `crafted.stat_210067635@T2` | 0.06559 |
| `desecrated.stat_2231156303` | 0.03196 |
| `desecrated.stat_9187492` | 0.00344 |
| `rune.stat_1509134228` | 0.00018 |

### weapon.staff — n=3077, R²=-0.4054

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.64582 |
| `rune.stat_3990135792` | -0.13257 |
| `rune.stat_975988108` | -0.11498 |
| `rune.stat_2974417149` | 0.07954 |
| `crafted.stat_124131830` | 0.00379 |
| `explicit.stat_2254480358@T1` | 0.00203 |
| `explicit.stat_473429811@T1` | 0.00043 |
| `explicit.stat_3962278098@T2` | 0.00005 |
| `explicit.stat_124131830@T1` | 0.00004 |
| `explicit.stat_124131830@T2` | 0.00004 |
| `explicit.stat_1600707273@T1` | 0.00004 |
| `explicit.stat_2891184298@T2` | 0.00003 |

### weapon.sceptre — n=3074, R²=-0.4321

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00180`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 0.10072 |
| `rune.stat_1611856026` | 0.08840 |
| `rune.stat_3984865854` | 0.08160 |
| `desecrated.stat_1050105434` | 0.00848 |
| `desecrated.stat_3984865854` | -0.00307 |
| `explicit.stat_1263695895@T1` | 0.00007 |
| `explicit.stat_1250712710@T1` | -0.00003 |
| `explicit.stat_1798257884@T2` | 0.00003 |
| `explicit.stat_1263695895@T2` | 0.00002 |
| `explicit.stat_3984865854@T2` | -0.00002 |
| `explicit.stat_2162097452@T2` | 0.00002 |
| `explicit.stat_3057012405@T1` | 0.00002 |

### weapon.spear — n=2691, R²=-0.412

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_518292764` | 0.88636 |
| `rune.stat_1509134228` | -0.07611 |
| `rune.stat_1039491398` | 0.07611 |
| `explicit.stat_210067635@T1` | 0.01737 |
| `desecrated.stat_691932474` | -0.00123 |
| `desecrated.stat_1509134228` | 0.00083 |
| `explicit.stat_1263695895@T2` | -0.00005 |
| `explicit.stat_1263695895@T1` | -0.00005 |
| `explicit.stat_2694482655@T1` | 0.00004 |
| `explicit.stat_709508406@T1` | 0.00002 |
| `explicit.stat_3639275092@T1` | 0.00002 |
| `explicit.stat_9187492@T2` | -0.00002 |

### armour.focus — n=2182, R²=-0.2727

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00004`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00001`  ·  quality: `0.00003`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.51110 |
| `crafted.stat_2974417149@T1` | -4.72551 |
| `desecrated.stat_378817135@T1` | -2.02953 |
| `desecrated.stat_2910761524@T1` | 0.91739 |
| `desecrated.stat_3393628375` | 0.53650 |
| `desecrated.stat_378817135` | 0.19564 |
| `desecrated.stat_2910761524` | -0.10795 |
| `crafted.stat_2974417149` | 0.08129 |
| `crafted.stat_4015621042` | 0.06669 |
| `desecrated.stat_4015621042` | 0.03537 |
| `rune.stat_3523867985` | 0.01483 |
| `desecrated.stat_274716455` | 0.00524 |

### armour.quiver — n=2050, R²=-0.4396

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00004`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | -0.00008 |
| `explicit.stat_681332047@T1` | -0.00005 |
| `explicit.stat_681332047@T2` | -0.00005 |
| `explicit.stat_803737631@T2` | -0.00005 |
| `explicit.stat_2321178454@T2` | -0.00005 |
| `explicit.stat_1573130764@T1` | -0.00005 |
| `explicit.stat_2463230181@T2` | -0.00004 |
| `explicit.stat_3714003708@T2` | -0.00004 |
| `explicit.stat_1368271171@T2` | -0.00004 |
| `explicit.stat_3032590688@T1` | -0.00004 |
| `explicit.stat_3032590688@T2` | -0.00004 |
| `explicit.stat_3714003708@T1` | -0.00004 |

### armour.shield — n=1868, R²=-0.3745

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.16291`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.84438 |
| `explicit.stat_1978899297@T2` | -0.35243 |
| `explicit.stat_1978899297` | 0.18950 |
| `explicit.stat_1011760251@T1` | -0.16298 |
| `explicit.stat_2481353198@T1` | -0.16295 |
| `explicit.stat_1301765461@T2` | -0.16293 |
| `explicit.stat_1011760251@T2` | -0.16293 |
| `explicit.stat_2481353198@T2` | -0.16293 |
| `explicit.stat_2339757871@T1` | -0.16292 |
| `explicit.stat_2901986750@T2` | -0.16292 |
| `explicit.stat_3484657501@T1` | -0.16292 |
| `explicit.stat_3639275092@T1` | -0.16291 |

### weapon.twomace — n=1587, R²=-0.3951

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00918`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1039491398` | 0.11077 |
| `rune.stat_1509134228` | -0.04001 |
| `desecrated.stat_1509134228` | 0.02300 |
| `explicit.stat_518292764@T1` | 0.01485 |
| `desecrated.stat_691932474` | 0.01033 |
| `explicit.stat_1037193709@T1` | -0.00922 |
| `explicit.stat_3336890334@T1` | -0.00922 |
| `explicit.stat_1037193709@T2` | -0.00920 |
| `explicit.stat_1940865751@T2` | -0.00920 |
| `explicit.stat_387439868@T2` | -0.00920 |
| `explicit.stat_691932474@T2` | -0.00920 |
| `explicit.stat_669069897@T2` | -0.00920 |

## Coverage (listings per base)

- … **Emerald** — 9924 listings (9924 priced) [0.7–7553463.8 ex]
- … **Sapphire** — 9857 listings (9855 priced) [0.6–7553463.8 ex]
- … **Ruby** — 7714 listings (7713 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 5055 listings (5053 priced) [0.3–4877938.3 ex]
- … **Stellar Amulet** — 3803 listings (3803 priced) [0.3–4547453.5 ex]
- … **Prismatic Ring** — 3661 listings (3660 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 3571 listings (3566 priced) [0.4–66666666.0 ex]
- … **Amethyst Ring** — 3494 listings (3493 priced) [0.4–71450.3 ex]
- … **Gold Amulet** — 3445 listings (3445 priced) [0.5–292542.5 ex]
- … **Gold Ring** — 3330 listings (3329 priced) [0.4–24532814.5 ex]
- … **Dueling Wand** — 3303 listings (3300 priced) [1.0–3736768402.2 ex]
- … **Sapphire Ring** — 2765 listings (2765 priced) [0.4–24532814.5 ex]
- … **Topaz Ring** — 2727 listings (2727 priced) [1.0–24532814.5 ex]
- … **Ruby Ring** — 2661 listings (2661 priced) [0.6–146119.1 ex]
- … **Plate Belt** — 2551 listings (2550 priced) [0.4–4877938.3 ex]
- … **Obliterator Bow** — 2516 listings (2511 priced) [0.3–22139622146.9 ex]
- … **Lapis Amulet** — 2432 listings (2432 priced) [0.4–4547453.5 ex]
- … **Ancestral Tiara** — 2400 listings (2398 priced) [0.6–5125681.0 ex]
- … **Heavy Belt** — 2398 listings (2398 priced) [0.4–4877938.3 ex]
- … **Amber Amulet** — 2386 listings (2386 priced) [0.5–4547453.5 ex]
- … **Jade Amulet** — 2375 listings (2374 priced) [0.4–4547453.5 ex]
- … **Unset Ring** — 2222 listings (2222 priced) [0.4–24532814.5 ex]
- … **Bloodstone Amulet** — 2208 listings (2208 priced) [0.4–7275.7 ex]
- … **Pearl Ring** — 2173 listings (2173 priced) [0.4–24532814.5 ex]
- … **Azure Amulet** — 2134 listings (2134 priced) [0.4–4877938.3 ex]

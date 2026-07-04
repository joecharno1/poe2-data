# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-04T08:56:14+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **97157** (97157 priced in exalted)
- Distinct bases: 857 · distinct mods: 2023 · mod rows: 471438
- Sold signals: **22476** sold · 22890 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-04T08:51:48+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.39** (median |log error| 2.0)
- Within ±30% of asking price: **30%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 64% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×23.24 · ±30% 12% · n=13495
- Premium segment (60ex+): skill **+0.10** · typical error ×156.33 · ±30% 0% · n=7708
- Sold listings (clearing prices): skill **+0.03** · typical error ×7.72 · ±30% 34% · n=7608

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.amulet | 1615 | ×14.35 | 6% | -0.06 | -0.11 |
| accessory.belt | 1599 | ×9.16 | 26% | +0.03 | +0.09 |
| accessory.ring | 1572 | ×7.20 | 5% | -0.01 | -0.02 |
| armour.helmet | 1516 | ×8.53 | 21% | -0.01 | +0.08 |
| armour.chest | 1510 | ×7.27 | 22% | +0.02 | +0.09 |
| armour.gloves | 1374 | ×10.00 | 38% | -0.01 | -0.06 |
| armour.boots | 1340 | ×10.00 | 36% | -0.02 | -0.10 |
| other | 1246 | ×8.65 | 30% | +0.43 | +0.41 |
| weapon.wand | 1105 | ×8.58 | 37% | +0.06 | +0.08 |
| jewel | 1034 | ×6.63 | 9% | +0.00 | +0.09 |
| weapon.bow | 941 | ×8.52 | 36% | +0.06 | +0.07 |
| weapon.crossbow | 868 | ×8.25 | 34% | +0.05 | +0.12 |
| weapon.sceptre | 230 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.spear | 205 | ×1.00 | 100% | n/a | - |
| weapon.warstaff | 198 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.staff | 186 | ×1.00 | 96% | +0.00 | +0.00 |
| armour.focus | 179 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 150 | ×1.00 | 97% | +0.00 | +0.00 |
| armour.shield | 142 | ×1.00 | 95% | +0.00 | +0.00 |
| weapon.twomace | 102 | ×1.00 | 97% | +0.00 | +0.00 |
| flask.charm | 42 | ×1.00 | 98% | -0.00 | -1.25 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=11403, R²=-0.2858

intercept: `1.5464`  ·  log_price: True  ·  ilvl: `0.00258`  ·  n_mods: `0.02679`  ·  n_top_tier: `0.20452`  ·  corrupted: `3.92743`  ·  n_sockets: `-0.05769`  ·  quality: `-0.00609`

| stat_id | coef |
|---|---|
| `explicit.stat_3141070085@T1` | 4.49824 |
| `explicit.stat_101878827@T1` | 4.33673 |
| `explicit.stat_736967255@T1` | 1.38674 |
| `explicit.stat_789117908@T1` | 0.63697 |
| `explicit.stat_124131830` | -0.63060 |
| `explicit.stat_2974417149@T1` | 0.62513 |
| `explicit.stat_2891184298@T1` | -0.60574 |
| `explicit.stat_4052037485@T1` | -0.50463 |
| `explicit.stat_3299347043@T2` | -0.36562 |
| `explicit.stat_3299347043@T1` | -0.35178 |
| `explicit.stat_1671376347@T2` | -0.33095 |
| `explicit.stat_3917489142@T1` | -0.32966 |

### accessory.amulet — n=7448, R²=-2.4623

intercept: `5.0542`  ·  log_price: True  ·  ilvl: `-0.05744`  ·  n_mods: `-0.11305`  ·  n_top_tier: `0.23178`  ·  corrupted: `-0.22722`  ·  n_sockets: `-0.24201`  ·  quality: `0.82905`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | 2.76408 |
| `explicit.stat_2923486259@T1` | -2.38053 |
| `explicit.stat_2923486259@T2` | -1.95520 |
| `explicit.stat_2162097452@T2` | -1.77620 |
| `explicit.stat_1671376347@T1` | 1.52142 |
| `explicit.stat_9187492` | 1.38695 |
| `explicit.stat_472520716@T2` | -1.29770 |
| `explicit.stat_9187492@T2` | -1.26870 |
| `explicit.stat_2162097452` | 1.10015 |
| `explicit.stat_124131830` | 1.09079 |
| `explicit.stat_472520716@T1` | -0.97485 |
| `explicit.stat_587431675@T1` | 0.90350 |

### accessory.belt — n=7353, R²=-1.2425

intercept: `4.2779`  ·  log_price: True  ·  ilvl: `-0.05159`  ·  n_mods: `-0.02834`  ·  n_top_tier: `0.08172`  ·  corrupted: `0.08638`  ·  n_sockets: `-0.15043`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.46066 |
| `explicit.stat_2923486259@T2` | 1.28960 |
| `explicit.stat_2923486259@T1` | 0.56690 |
| `explicit.stat_3299347043@T1` | -0.39978 |
| `explicit.stat_3299347043@T2` | -0.25042 |
| `explicit.stat_1836676211@T1` | 0.20403 |
| `explicit.stat_1389754388@T1` | -0.14580 |
| `explicit.stat_4080418644@T2` | -0.13266 |
| `explicit.stat_2881298780@T1` | -0.13105 |
| `explicit.stat_809229260@T2` | -0.12297 |
| `explicit.stat_4220027924@T1` | 0.12060 |
| `explicit.stat_644456512@T2` | -0.11339 |

### accessory.ring — n=7291, R²=-1.9226

intercept: `4.5241`  ·  log_price: True  ·  ilvl: `-0.03135`  ·  n_mods: `-0.23836`  ·  n_top_tier: `0.48999`  ·  corrupted: `0.52855`  ·  n_sockets: `2.96550`  ·  quality: `0.03467`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T2` | 2.55457 |
| `explicit.stat_707457662@T1` | 2.33850 |
| `explicit.stat_1263695895@T2` | -2.13923 |
| `explicit.stat_1573130764@T1` | -1.98659 |
| `explicit.stat_1263695895@T1` | -1.78042 |
| `explicit.stat_2923486259@T2` | -1.51150 |
| `explicit.stat_1368271171@T1` | -1.45331 |
| `explicit.stat_2923486259@T1` | -1.38760 |
| `explicit.stat_1050105434@T2` | -1.11404 |
| `explicit.stat_1368271171@T2` | -1.09954 |
| `explicit.stat_789117908@T1` | -1.08031 |
| `explicit.stat_1379411836@T1` | -1.07917 |

### armour.helmet — n=7063, R²=-1.3217

intercept: `4.0246`  ·  log_price: True  ·  ilvl: `-0.05076`  ·  n_mods: `-0.02258`  ·  n_top_tier: `0.75924`  ·  corrupted: `0.10253`  ·  n_sockets: `-0.01407`  ·  quality: `0.02695`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 5.25285 |
| `explicit.stat_2339757871@T1` | -1.58691 |
| `explicit.stat_3033371881@T1` | -1.11898 |
| `explicit.stat_3033371881@T2` | -1.09704 |
| `explicit.stat_3362812763@T1` | -0.94213 |
| `explicit.stat_1263695895@T1` | -0.94013 |
| `explicit.stat_3362812763@T2` | -0.88890 |
| `explicit.stat_3325883026@T1` | -0.87635 |
| `explicit.stat_803737631@T2` | -0.86660 |
| `explicit.stat_4052037485@T2` | -0.84994 |
| `explicit.stat_3321629045@T2` | -0.84554 |
| `explicit.stat_3639275092@T1` | -0.83324 |

### armour.chest — n=7061, R²=-1.4194

intercept: `3.6743`  ·  log_price: True  ·  ilvl: `-0.04573`  ·  n_mods: `-0.02373`  ·  n_top_tier: `0.59622`  ·  corrupted: `-0.02225`  ·  n_sockets: `-0.00576`  ·  quality: `0.01973`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 2.63809 |
| `implicit.stat_2251279027` | 1.75933 |
| `explicit.stat_3981240776@T1` | 1.13738 |
| `explicit.stat_2923486259@T1` | -0.87333 |
| `explicit.stat_2923486259@T2` | -0.81708 |
| `explicit.stat_2339757871@T1` | -0.78412 |
| `explicit.stat_3261801346@T1` | -0.76278 |
| `explicit.stat_3261801346@T2` | -0.74855 |
| `explicit.stat_4052037485@T1` | -0.73735 |
| `explicit.stat_3301100256@T2` | -0.69694 |
| `explicit.stat_915769802@T1` | -0.67859 |
| `explicit.stat_3033371881@T1` | -0.67377 |

### armour.boots — n=6499, R²=-0.1953

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.23115`  ·  corrupted: `0.00002`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -0.23120 |
| `explicit.stat_4220027924@T1` | -0.23118 |
| `explicit.stat_1062208444@T1` | -0.23118 |
| `explicit.stat_3033371881@T2` | -0.23117 |
| `explicit.stat_3484657501@T1` | -0.23117 |
| `explicit.stat_3484657501@T2` | -0.23117 |
| `explicit.stat_1062208444@T2` | -0.23117 |
| `explicit.stat_3261801346@T2` | -0.23116 |
| `explicit.stat_2451402625@T1` | -0.23116 |
| `explicit.stat_124859000@T2` | -0.23116 |
| `explicit.stat_3325883026@T1` | -0.23116 |
| `explicit.stat_3639275092@T1` | -0.23116 |

### armour.gloves — n=6452, R²=-0.2427

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00793`  ·  corrupted: `0.00603`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_4067062424@T1` | 0.21616 |
| `desecrated.stat_3032590688` | 0.16879 |
| `explicit.stat_2923486259` | -0.05182 |
| `pseudo.total_chaos_res` | 0.05182 |
| `desecrated.stat_3299347043` | 0.00904 |
| `explicit.stat_2339757871@T1` | -0.00820 |
| `explicit.stat_3484657501@T2` | -0.00797 |
| `explicit.stat_4052037485@T1` | -0.00797 |
| `explicit.stat_4015621042@T1` | -0.00795 |
| `explicit.stat_3484657501@T1` | -0.00795 |
| `explicit.stat_3917489142@T2` | -0.00794 |
| `explicit.stat_2797971005@T2` | -0.00794 |

### weapon.wand — n=5158, R²=-1.6112

intercept: `3.2446`  ·  log_price: True  ·  ilvl: `-0.04052`  ·  n_mods: `-0.01474`  ·  n_top_tier: `0.10082`  ·  corrupted: `0.03983`  ·  n_sockets: `0.00326`  ·  quality: `0.02840`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.27011 |
| `explicit.stat_1600707273@T1` | 2.23913 |
| `explicit.stat_1545858329@T1` | 2.18122 |
| `explicit.stat_736967255@T2` | 2.08111 |
| `explicit.stat_124131830@T1` | 1.94466 |
| `explicit.stat_1600707273@T2` | 1.70150 |
| `explicit.stat_4226189338@T1` | 1.59013 |
| `crafted.stat_124131830` | 1.23866 |
| `explicit.stat_124131830@T2` | -0.32230 |
| `rune.stat_3990135792` | -0.22454 |
| `explicit.stat_2231156303@T2` | -0.18249 |
| `explicit.stat_473429811@T1` | -0.18237 |

### jewel — n=5119, R²=-1.0186

intercept: `-1.6147`  ·  log_price: True  ·  ilvl: `0.03866`  ·  n_mods: `0.19643`  ·  n_top_tier: `-0.50997`  ·  corrupted: `0.47979`

| stat_id | coef |
|---|---|
| `explicit.stat_153777645@T1` | 5.73837 |
| `explicit.stat_2011656677@T1` | 5.38343 |
| `explicit.stat_3851254963@T1` | 5.33670 |
| `explicit.stat_1569101201@T1` | 5.29180 |
| `explicit.stat_3028809864@T1` | -5.20547 |
| `explicit.stat_1459321413@T1` | 5.20364 |
| `explicit.stat_429143663@T1` | 5.15669 |
| `explicit.stat_293638271@T1` | -4.84071 |
| `explicit.stat_3787460122@T1` | 4.80362 |
| `explicit.stat_2301718443@T1` | -4.59602 |
| `explicit.stat_2456523742@T1` | 3.83218 |
| `explicit.stat_1569159338@T1` | 3.56435 |

### weapon.bow — n=4424, R²=-1.4879

intercept: `3.4147`  ·  log_price: True  ·  ilvl: `-0.04216`  ·  n_mods: `-0.02914`  ·  n_top_tier: `0.37471`  ·  corrupted: `0.07293`  ·  n_sockets: `0.00550`  ·  quality: `-0.00398`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -7.42080 |
| `explicit.stat_2463230181@T1` | 1.89432 |
| `explicit.stat_1509134228@T1` | 1.84839 |
| `explicit.stat_518292764@T1` | 1.62271 |
| `explicit.stat_1202301673@T1` | 1.58242 |
| `crafted.stat_3035140377` | 1.09836 |
| `desecrated.stat_210067635@T1` | -0.78481 |
| `explicit.stat_821021828@T1` | -0.56056 |
| `explicit.stat_1263695895@T1` | -0.55989 |
| `explicit.stat_821021828@T2` | -0.50557 |
| `explicit.stat_1940865751@T1` | -0.48199 |
| `explicit.stat_691932474@T2` | -0.45015 |

### weapon.crossbow — n=4150, R²=-1.4402

intercept: `3.3820`  ·  log_price: True  ·  ilvl: `-0.04273`  ·  n_mods: `0.00544`  ·  n_top_tier: `0.26233`  ·  corrupted: `0.01478`  ·  n_sockets: `0.02499`  ·  quality: `-0.01089`

| stat_id | coef |
|---|---|
| `desecrated.stat_3131442032@T1` | -3.31990 |
| `desecrated.stat_1365232741@T1` | -3.31990 |
| `explicit.stat_1037193709@T1` | 2.06389 |
| `explicit.stat_3336890334@T1` | 2.02401 |
| `explicit.stat_709508406@T1` | 1.93451 |
| `explicit.stat_691932474@T1` | -1.34420 |
| `crafted.stat_3035140377` | 1.14784 |
| `explicit.stat_1967051901@T1` | 1.10974 |
| `explicit.stat_1509134228@T1` | 1.05075 |
| `explicit.stat_1263695895@T1` | 0.75988 |
| `explicit.stat_1202301673@T1` | 0.60510 |
| `explicit.stat_1263695895@T2` | -0.42896 |

### weapon.sceptre — n=1180, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1798257884` | 0.00000 |
| `desecrated.stat_1050105434` | 0.00000 |
| `desecrated.stat_1250712710` | 0.00000 |
| `desecrated.stat_1798257884` | 0.00000 |
| `desecrated.stat_3984865854` | 0.00000 |
| `explicit.stat_101878827` | 0.00000 |
| `explicit.stat_101878827@T1` | 0.00000 |
| `explicit.stat_101878827@T2` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_1250712710` | 0.00000 |

### weapon.spear — n=1052, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1202301673@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |

### weapon.warstaff — n=970, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_210067635` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |
| `desecrated.stat_387439868` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |

### weapon.staff — n=936, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_124131830` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T1` | 0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |

### armour.focus — n=919, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1671376347` | 0.00000 |
| `desecrated.stat_2891184298` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T1` | -0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |
| `explicit.stat_2231156303` | 0.00000 |

### flask.charm — n=859, R²=-0.3817

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00014 |
| `explicit.stat_1120862500@T2` | -0.00004 |
| `explicit.stat_2541588185@T2` | 0.00004 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_3849649145` | -0.00003 |
| `explicit.stat_1873752457@T2` | -0.00002 |
| `explicit.stat_828533480@T2` | -0.00002 |
| `explicit.stat_2566921799` | 0.00002 |
| `explicit.stat_1366840608@T2` | 0.00002 |
| `explicit.stat_3196823591@T2` | -0.00002 |
| `implicit.stat_1412682799` | 0.00001 |
| `implicit.stat_4010341289` | -0.00001 |

### armour.shield — n=787, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1568848828` | 0.00000 |
| `explicit.stat_1011760251` | 0.00000 |
| `explicit.stat_1011760251@T1` | -0.00000 |
| `explicit.stat_1011760251@T2` | 0.00000 |
| `explicit.stat_1062208444` | 0.00000 |
| `explicit.stat_1062208444@T1` | 0.00000 |
| `explicit.stat_1062208444@T2` | 0.00000 |
| `explicit.stat_1301765461` | 0.00000 |
| `explicit.stat_1301765461@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |

### armour.quiver — n=787, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1241625305` | 0.00000 |
| `explicit.stat_1241625305@T1` | 0.00000 |
| `explicit.stat_1241625305@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | -0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1573130764` | 0.00000 |
| `explicit.stat_1573130764@T1` | 0.00000 |
| `explicit.stat_1573130764@T2` | 0.00000 |

### weapon.twomace — n=550, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |
| `explicit.stat_1940865751` | 0.00000 |
| `explicit.stat_1940865751@T1` | 0.00000 |

## Coverage (listings per base)

- … **Emerald** — 2792 listings (2792 priced) [0.5–856.7 ex]
- … **Sapphire** — 2689 listings (2689 priced) [0.4–856.7 ex]
- … **Utility Belt** — 2333 listings (2333 priced) [0.3–12057.7 ex]
- … **Ruby** — 2175 listings (2175 priced) [0.3–856.7 ex]
- … **Stellar Amulet** — 1741 listings (1741 priced) [0.3–37188.0 ex]
- … **Dueling Wand** — 1639 listings (1639 priced) [0.8–856.7 ex]
- … **Solar Amulet** — 1406 listings (1406 priced) [1.0–856.7 ex]
- … **Gold Amulet** — 1358 listings (1358 priced) [0.4–856.7 ex]
- … **Prismatic Ring** — 1295 listings (1295 priced) [0.3–856.7 ex]
- … **Obliterator Bow** — 1269 listings (1269 priced) [0.4–856.7 ex]
- … **Amethyst Ring** — 1250 listings (1250 priced) [0.8–856.7 ex]
- … **Gold Ring** — 1221 listings (1221 priced) [0.7–856.7 ex]
- … **Plate Belt** — 1134 listings (1134 priced) [1.0–856.7 ex]
- … **Heavy Belt** — 1052 listings (1052 priced) [0.5–856.7 ex]
- … **Ancestral Tiara** — 1022 listings (1022 priced) [1.0–856.7 ex]
- … **Topaz Ring** — 1017 listings (1017 priced) [1.0–856.7 ex]
- … **Sapphire Ring** — 1010 listings (1010 priced) [0.5–856.7 ex]
- … **Ruby Ring** — 951 listings (951 priced) [0.4–856.7 ex]
- … **Galvanic Wand** — 938 listings (938 priced) [1.0–856.7 ex]
- … **Lapis Amulet** — 933 listings (933 priced) [0.6–856.7 ex]
- … **Jade Amulet** — 898 listings (898 priced) [0.4–856.7 ex]
- … **Amber Amulet** — 895 listings (895 priced) [0.4–856.7 ex]
- … **Siphoning Wand** — 894 listings (894 priced) [1.0–856.7 ex]
- … **Warmonger Bow** — 891 listings (891 priced) [0.9–856.7 ex]
- … **Attuned Wand** — 867 listings (867 priced) [0.3–856.7 ex]

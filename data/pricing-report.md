# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-20T20:29:47+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **691850** (689698 priced in exalted)
- Distinct bases: 999 · distinct mods: 3310 · mod rows: 3274923
- Sold signals: **24327** sold · 393936 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-20T20:15:48+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×20.44** (median |log error| 3.0175)
- Within ±30% of asking price: **15%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.17** · typical error ×54.94 · ±30% 5% · n=100474
- Premium segment (60ex+): skill **+0.16** · typical error ×260.11 · ±30% 0% · n=67206

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 14754 | ×53.05 | 21% | +0.04 | +0.06 |
| jewel | 13989 | ×10.15 | 5% | +0.11 | +0.13 |
| accessory.amulet | 13301 | ×38.26 | 18% | +0.04 | +0.05 |
| accessory.belt | 9525 | ×17.63 | 7% | +0.09 | +0.11 |
| armour.chest | 9174 | ×15.56 | 18% | +0.09 | +0.11 |
| armour.helmet | 8985 | ×20.79 | 12% | +0.11 | +0.12 |
| armour.boots | 8287 | ×24.32 | 19% | +0.10 | +0.13 |
| armour.gloves | 8138 | ×32.24 | 13% | +0.09 | +0.11 |
| other | 8038 | ×3.63 | 41% | +0.10 | +0.15 |
| weapon.wand | 4864 | ×39.52 | 14% | +0.11 | +0.12 |
| weapon.bow | 3803 | ×27.04 | 12% | +0.16 | +0.16 |
| weapon.crossbow | 3597 | ×25.59 | 13% | +0.12 | +0.16 |
| weapon.warstaff | 2468 | ×13.69 | 7% | +0.21 | +0.21 |
| weapon.staff | 2373 | ×17.57 | 6% | +0.18 | +0.17 |
| weapon.sceptre | 2339 | ×20.39 | 5% | +0.09 | +0.10 |
| weapon.spear | 1855 | ×14.76 | 7% | +0.14 | +0.15 |
| armour.focus | 1531 | ×13.13 | 7% | +0.11 | +0.14 |
| armour.quiver | 1449 | ×19.36 | 6% | +0.12 | +0.13 |
| armour.shield | 1193 | ×9.64 | 8% | +0.10 | +0.11 |
| flask.charm | 1179 | ×12.06 | 27% | -0.02 | +0.00 |
| weapon.twomace | 1103 | ×8.54 | 10% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=76863, R²=-0.9762

intercept: `-1.9132`  ·  log_price: True  ·  ilvl: `0.02417`  ·  n_mods: `0.83317`  ·  n_top_tier: `-0.26259`  ·  corrupted: `0.41462`  ·  quality: `-0.00283`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.49708 |
| `explicit.stat_3485067555@T1` | 2.39396 |
| `explicit.stat_1869147066@T1` | -1.92251 |
| `explicit.stat_1594812856@T1` | 1.77420 |
| `explicit.stat_1569101201@T1` | -1.57134 |
| `explicit.stat_3780644166@T1` | -1.48422 |
| `explicit.stat_3174700878@T1` | 1.41363 |
| `explicit.stat_239367161@T1` | -1.29238 |
| `explicit.stat_3668351662@T1` | -1.21719 |
| `explicit.stat_4147897060@T1` | -1.15999 |
| `explicit.stat_429143663@T1` | 1.15470 |
| `explicit.stat_234296660@T1` | -1.14946 |

### accessory.ring — n=67249, R²=-2.0263

intercept: `3.3490`  ·  log_price: True  ·  ilvl: `-0.04176`  ·  n_mods: `0.00053`  ·  n_top_tier: `0.99033`  ·  corrupted: `0.00994`  ·  n_sockets: `2.01155`  ·  quality: `0.03165`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.01563 |
| `explicit.stat_803737631@T1` | -1.01370 |
| `explicit.stat_2231156303@T1` | -1.00578 |
| `explicit.stat_4080418644@T1` | -1.00514 |
| `explicit.stat_4220027924@T2` | -1.00502 |
| `explicit.stat_2557965901@T1` | -1.00442 |
| `explicit.stat_3325883026@T1` | -1.00365 |
| `explicit.stat_1573130764@T2` | -1.00257 |
| `explicit.stat_736967255@T2` | -1.00149 |
| `explicit.stat_2891184298@T2` | -1.00128 |
| `explicit.stat_2557965901@T2` | -1.00010 |
| `explicit.stat_2923486259@T2` | -0.99899 |

### other — n=65879, R²=-0.6881

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.01695`  ·  n_top_tier: `0.32963`  ·  corrupted: `0.06938`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.37501 |
| `explicit.stat_3917489142@T1` | -0.24021 |
| `explicit.stat_3299347043@T1` | -0.22314 |
| `explicit.stat_2974417149@T1` | 0.10378 |
| `explicit.stat_789117908@T1` | -0.07930 |
| `implicit.stat_2219129443` | 0.06091 |
| `explicit.stat_736967255@T1` | -0.05849 |
| `explicit.stat_2106365538@T1` | -0.05407 |
| `implicit.stat_3182714256` | 0.05088 |
| `implicit.stat_718638445` | 0.05087 |
| `implicit.stat_2901986750` | -0.04322 |
| `pseudo.total_ele_res>=40` | -0.04190 |

### accessory.amulet — n=60507, R²=-2.1416

intercept: `3.4499`  ·  log_price: True  ·  ilvl: `-0.04344`  ·  n_mods: `-0.02070`  ·  n_top_tier: `1.32672`  ·  corrupted: `0.11424`  ·  n_sockets: `-0.10591`  ·  quality: `0.05225`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T2` | -1.73978 |
| `explicit.stat_3299347043@T1` | -1.67697 |
| `explicit.stat_803737631@T1` | -1.47584 |
| `explicit.stat_2866361420@T2` | -1.42708 |
| `explicit.stat_2974417149@T1` | -1.42177 |
| `explicit.stat_587431675@T2` | -1.41861 |
| `explicit.stat_2866361420@T1` | -1.40319 |
| `explicit.stat_803737631@T2` | -1.40250 |
| `explicit.stat_2974417149@T2` | -1.39519 |
| `explicit.stat_1050105434@T2` | -1.37835 |
| `explicit.stat_4080418644@T1` | -1.36812 |
| `explicit.stat_2901986750@T1` | -1.36496 |

### accessory.belt — n=43610, R²=-1.3034

intercept: `5.8209`  ·  log_price: True  ·  ilvl: `-0.06292`  ·  n_mods: `-0.13004`  ·  n_top_tier: `0.38950`  ·  corrupted: `1.15669`  ·  n_sockets: `0.93017`

| stat_id | coef |
|---|---|
| `implicit.stat_731781020` | -1.19283 |
| `explicit.stat_2923486259@T1` | 1.07997 |
| `explicit.stat_3299347043@T1` | -0.89778 |
| `explicit.stat_2923486259@T2` | 0.82833 |
| `explicit.stat_3299347043@T2` | -0.65590 |
| `explicit.stat_2881298780@T1` | -0.49723 |
| `explicit.stat_51994685@T1` | -0.46876 |
| `explicit.stat_1570770415@T2` | -0.43300 |
| `explicit.stat_3372524247@T2` | -0.42249 |
| `explicit.stat_4220027924@T2` | -0.39230 |
| `explicit.stat_644456512@T1` | -0.39126 |
| `explicit.stat_4080418644@T2` | -0.37404 |

### armour.chest — n=43167, R²=-1.605

intercept: `3.7558`  ·  log_price: True  ·  ilvl: `-0.04618`  ·  n_mods: `-0.03017`  ·  n_top_tier: `0.38162`  ·  corrupted: `0.29624`  ·  n_sockets: `0.05056`  ·  quality: `0.06938`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.80297 |
| `explicit.stat_3981240776@T1` | 0.99635 |
| `explicit.stat_986397080@T2` | -0.60590 |
| `explicit.stat_986397080@T1` | -0.57065 |
| `explicit.stat_3372524247@T1` | 0.51456 |
| `explicit.stat_3484657501@T1` | -0.50163 |
| `explicit.stat_2339757871@T2` | -0.46478 |
| `explicit.stat_1692879867@T2` | -0.44153 |
| `explicit.stat_3301100256@T2` | -0.43806 |
| `explicit.stat_915769802@T2` | -0.43695 |
| `explicit.stat_4080418644@T2` | -0.42913 |
| `explicit.stat_2451402625@T1` | -0.42554 |

### armour.helmet — n=41963, R²=-1.4511

intercept: `3.5463`  ·  log_price: True  ·  ilvl: `-0.04504`  ·  n_mods: `-0.04663`  ·  n_top_tier: `0.61193`  ·  corrupted: `0.64720`  ·  n_sockets: `0.14405`  ·  quality: `0.05770`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.81601 |
| `explicit.stat_3917489142@T2` | -1.13331 |
| `explicit.stat_1263695895@T1` | -1.13227 |
| `explicit.stat_3917489142@T1` | -0.97177 |
| `explicit.stat_1263695895@T2` | -0.80755 |
| `explicit.stat_1999113824@T1` | -0.78101 |
| `explicit.stat_3321629045@T2` | -0.78021 |
| `explicit.stat_2162097452@T2` | -0.75152 |
| `explicit.stat_803737631@T1` | -0.73668 |
| `explicit.stat_4052037485@T2` | -0.71176 |
| `explicit.stat_803737631@T2` | -0.69797 |
| `explicit.stat_1999113824@T2` | -0.69138 |

### armour.boots — n=38937, R²=-1.6769

intercept: `3.6955`  ·  log_price: True  ·  ilvl: `-0.04562`  ·  n_mods: `-0.02284`  ·  n_top_tier: `0.47899`  ·  corrupted: `0.13180`  ·  n_sockets: `0.06101`  ·  quality: `0.06656`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.74681 |
| `crafted.stat_3917489142@T1` | 1.54161 |
| `explicit.stat_2339757871@T1` | -1.33603 |
| `explicit.stat_2923486259@T1` | 0.76503 |
| `explicit.stat_3917489142@T2` | -0.61067 |
| `explicit.stat_3299347043@T1` | -0.57031 |
| `explicit.stat_2923486259@T2` | -0.55836 |
| `explicit.stat_1874553720@T1` | -0.54657 |
| `explicit.stat_1999113824@T2` | -0.53754 |
| `explicit.stat_328541901@T2` | -0.53606 |
| `explicit.stat_2160282525@T1` | -0.52671 |
| `explicit.stat_3321629045@T2` | -0.52231 |

### armour.gloves — n=37909, R²=-1.6044

intercept: `3.7961`  ·  log_price: True  ·  ilvl: `-0.05013`  ·  n_mods: `0.00138`  ·  n_top_tier: `0.71130`  ·  corrupted: `-0.02147`  ·  n_sockets: `0.19890`  ·  quality: `0.06020`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 4.45229 |
| `explicit.stat_2923486259@T1` | -1.19611 |
| `explicit.stat_3321629045@T2` | -1.02022 |
| `explicit.stat_3484657501@T2` | -0.99122 |
| `explicit.stat_2923486259@T2` | -0.98656 |
| `explicit.stat_4052037485@T1` | -0.95988 |
| `explicit.stat_4015621042@T2` | -0.93543 |
| `explicit.stat_9187492@T2` | -0.92049 |
| `explicit.stat_4052037485@T2` | -0.89623 |
| `explicit.stat_3484657501@T1` | -0.88587 |
| `explicit.stat_124859000@T1` | -0.87118 |
| `explicit.stat_803737631@T2` | -0.86372 |

### weapon.wand — n=22610, R²=-1.8748

intercept: `3.9755`  ·  log_price: True  ·  ilvl: `-0.04908`  ·  n_mods: `-0.07165`  ·  n_top_tier: `0.39254`  ·  corrupted: `0.03312`  ·  n_sockets: `0.05047`  ·  quality: `0.04287`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -3.80958 |
| `explicit.stat_1545858329@T1` | 2.78295 |
| `explicit.stat_2254480358@T1` | 2.44047 |
| `explicit.stat_124131830@T1` | 2.20264 |
| `explicit.stat_591105508@T1` | 2.01000 |
| `explicit.stat_736967255@T2` | 1.70365 |
| `explicit.stat_4226189338@T1` | 1.51807 |
| `explicit.stat_2254480358@T2` | 1.26824 |
| `crafted.stat_124131830` | 1.11897 |
| `explicit.stat_4226189338@T2` | 0.80281 |
| `explicit.stat_1263695895@T2` | -0.79906 |
| `explicit.stat_1263695895@T1` | -0.73143 |

### flask.charm — n=19315, R²=-0.6517

intercept: `0.1044`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.60911`  ·  corrupted: `1.50929`  ·  quality: `0.00577`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.77924 |
| `explicit.stat_1056492907` | 2.64012 |
| `explicit.stat_3246948616` | 1.60936 |
| `explicit.stat_828533480@T2` | -1.60914 |
| `explicit.stat_1120862500@T2` | -1.60914 |
| `explicit.stat_1873752457@T2` | -1.60912 |
| `explicit.stat_2676834156@T2` | -1.60905 |
| `explicit.stat_2365392475@T2` | -1.60905 |
| `explicit.stat_3196823591@T2` | -1.60894 |
| `explicit.stat_388617051@T2` | -1.60571 |
| `explicit.stat_828533480@T1` | -1.60324 |
| `explicit.stat_2541588185@T2` | -1.59808 |

### weapon.bow — n=18033, R²=-1.78

intercept: `3.9918`  ·  log_price: True  ·  ilvl: `-0.04807`  ·  n_mods: `-0.07531`  ·  n_top_tier: `0.80277`  ·  corrupted: `0.77175`  ·  n_sockets: `0.04245`  ·  quality: `0.02920`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 2.76251 |
| `desecrated.stat_210067635@T1` | -1.88775 |
| `explicit.stat_1263695895@T1` | -1.26019 |
| `crafted.stat_3035140377` | 1.25554 |
| `explicit.stat_1263695895@T2` | -1.15553 |
| `explicit.stat_3336890334@T1` | 1.07408 |
| `explicit.stat_709508406@T1` | 1.02930 |
| `explicit.stat_2463230181@T2` | -0.95453 |
| `explicit.stat_1509134228@T1` | -0.92104 |
| `explicit.stat_3695891184@T2` | -0.89676 |
| `explicit.stat_1368271171@T2` | -0.89178 |
| `explicit.stat_210067635@T2` | -0.86846 |

### weapon.crossbow — n=16921, R²=-1.6619

intercept: `4.0140`  ·  log_price: True  ·  ilvl: `-0.04794`  ·  n_mods: `-0.09603`  ·  n_top_tier: `0.41367`  ·  corrupted: `0.09757`  ·  n_sockets: `0.09519`  ·  quality: `0.02887`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.53991 |
| `explicit.stat_1980802737` | 1.35545 |
| `explicit.stat_2250681686@T2` | -1.31181 |
| `explicit.stat_1202301673@T1` | 1.23251 |
| `explicit.stat_1509134228@T1` | 0.94812 |
| `explicit.stat_2250681686` | 0.92750 |
| `crafted.stat_3035140377` | 0.85491 |
| `explicit.stat_3695891184@T1` | -0.69805 |
| `explicit.stat_3336890334@T2` | -0.68584 |
| `explicit.stat_3695891184@T2` | -0.65083 |
| `explicit.stat_691932474@T1` | -0.61930 |
| `explicit.stat_387439868@T1` | 0.59325 |

### weapon.warstaff — n=11737, R²=-0.3533

intercept: `-9.9358`  ·  log_price: True  ·  ilvl: `0.13399`  ·  n_mods: `-0.20819`  ·  n_top_tier: `0.40990`  ·  corrupted: `0.23207`  ·  n_sockets: `0.11640`  ·  quality: `0.05815`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.15886 |
| `explicit.stat_328541901@T2` | -0.95847 |
| `rune.stat_243313994` | 0.94027 |
| `desecrated.stat_2231156303@T1` | 0.86032 |
| `desecrated.stat_2527686725@T1` | 0.86032 |
| `explicit.stat_328541901@T1` | -0.83729 |
| `desecrated.stat_9187492` | 0.80397 |
| `explicit.stat_1037193709@T1` | 0.62755 |
| `explicit.stat_1368271171@T1` | -0.59775 |
| `explicit.stat_691932474@T2` | -0.58497 |
| `explicit.stat_821021828@T2` | -0.55934 |
| `explicit.stat_210067635@T2` | -0.53029 |

### weapon.staff — n=11133, R²=-0.3594

intercept: `-15.8843`  ·  log_price: True  ·  ilvl: `0.20364`  ·  n_mods: `-0.06957`  ·  n_top_tier: `0.45373`  ·  corrupted: `0.66864`  ·  n_sockets: `0.17858`  ·  quality: `0.03171`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.13794 |
| `explicit.stat_591105508@T1` | 1.80308 |
| `explicit.stat_124131830@T1` | 1.75277 |
| `explicit.stat_1545858329@T1` | 1.61269 |
| `explicit.stat_1600707273@T1` | 1.43220 |
| `explicit.stat_2254480358@T1` | 1.35503 |
| `explicit.stat_293638271@T2` | -1.00610 |
| `explicit.stat_3962278098@T2` | 0.80199 |
| `explicit.stat_1263695895@T2` | -0.78062 |
| `explicit.stat_2254480358@T2` | 0.76804 |
| `explicit.stat_473429811@T2` | -0.62388 |
| `rune.stat_124131830` | 0.60317 |

### weapon.sceptre — n=10937, R²=-0.3376

intercept: `-21.8385`  ·  log_price: True  ·  ilvl: `0.27659`  ·  n_mods: `0.02821`  ·  n_top_tier: `0.17704`  ·  corrupted: `0.09091`  ·  n_sockets: `0.23837`  ·  quality: `0.03194`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.57681 |
| `explicit.stat_3057012405@T1` | 1.39830 |
| `explicit.stat_2162097452@T2` | 1.30782 |
| `explicit.stat_1263695895@T2` | -1.11566 |
| `explicit.stat_101878827@T2` | 0.90385 |
| `explicit.stat_1798257884@T2` | 0.85692 |
| `explicit.stat_1263695895@T1` | -0.81641 |
| `explicit.stat_101878827@T1` | 0.81638 |
| `explicit.stat_2854751904@T2` | -0.80606 |
| `explicit.stat_849987426@T1` | 0.71682 |
| `explicit.stat_1998951374@T1` | 0.54033 |
| `explicit.stat_770672621@T1` | -0.47431 |

### weapon.spear — n=8853, R²=-0.3832

intercept: `-13.4338`  ·  log_price: True  ·  ilvl: `0.18363`  ·  n_mods: `-0.13934`  ·  n_top_tier: `0.56577`  ·  corrupted: `-0.62972`  ·  n_sockets: `0.21858`  ·  quality: `0.07797`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -4.89310 |
| `crafted.stat_210067635@T2` | -3.09042 |
| `explicit.stat_1202301673@T1` | 1.37077 |
| `explicit.stat_9187492@T1` | 1.15650 |
| `explicit.stat_1940865751@T2` | -1.02425 |
| `crafted.stat_3035140377` | 0.90684 |
| `desecrated.stat_210067635@T1` | -0.86496 |
| `explicit.stat_1509134228@T1` | 0.85311 |
| `explicit.stat_4080418644@T2` | -0.84349 |
| `explicit.stat_748522257@T2` | -0.76125 |
| `explicit.stat_3261801346@T1` | -0.75285 |
| `explicit.stat_691932474@T2` | -0.74643 |

### armour.focus — n=7240, R²=-0.3356

intercept: `-16.3108`  ·  log_price: True  ·  ilvl: `0.20617`  ·  n_mods: `-0.09325`  ·  n_top_tier: `0.92294`  ·  corrupted: `0.05208`  ·  n_sockets: `0.27863`  ·  quality: `0.02591`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.52932 |
| `explicit.stat_4220027924@T1` | -1.48383 |
| `explicit.stat_2768835289@T1` | -1.21526 |
| `explicit.stat_2923486259@T2` | -1.18234 |
| `explicit.stat_4220027924@T2` | -1.17298 |
| `explicit.stat_2231156303@T2` | -1.09928 |
| `explicit.stat_3291658075@T1` | -1.08741 |
| `explicit.stat_4015621042@T1` | -1.07379 |
| `explicit.stat_2339757871@T2` | -0.99779 |
| `explicit.stat_274716455@T1` | -0.98340 |
| `explicit.stat_737908626@T2` | -0.96321 |
| `explicit.stat_2231156303@T1` | -0.95867 |

### armour.quiver — n=6747, R²=-0.2922

intercept: `-17.4103`  ·  log_price: True  ·  ilvl: `0.20771`  ·  n_mods: `-0.04390`  ·  n_top_tier: `0.72827`  ·  corrupted: `0.96674`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.81036 |
| `explicit.stat_681332047@T2` | -1.61151 |
| `explicit.stat_681332047@T1` | -1.35959 |
| `explicit.stat_1573130764@T2` | -1.02491 |
| `explicit.stat_2463230181@T1` | 1.01781 |
| `explicit.stat_1573130764@T1` | -0.90246 |
| `explicit.stat_4067062424@T1` | -0.75621 |
| `explicit.stat_803737631@T1` | -0.74165 |
| `explicit.stat_2194114101@T2` | -0.73289 |
| `explicit.stat_803737631@T2` | -0.64037 |
| `explicit.stat_3261801346@T1` | -0.58988 |
| `explicit.stat_2321178454@T2` | -0.58291 |

### armour.shield — n=5820, R²=-0.432

intercept: `-13.2645`  ·  log_price: True  ·  ilvl: `0.17510`  ·  n_mods: `-0.08458`  ·  n_top_tier: `0.53364`  ·  corrupted: `-0.35748`  ·  n_sockets: `0.41251`  ·  quality: `0.05247`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.21769 |
| `explicit.stat_3855016469@T1` | -1.10556 |
| `explicit.stat_4095671657@T2` | -1.01938 |
| `explicit.stat_4095671657@T1` | -1.01280 |
| `explicit.stat_3321629045@T2` | -1.00721 |
| `explicit.stat_1011760251@T1` | -0.99213 |
| `explicit.stat_3676141501@T1` | 0.94275 |
| `explicit.stat_1301765461@T1` | 0.81073 |
| `explicit.stat_4220027924@T1` | -0.79077 |
| `explicit.stat_2901986750@T1` | -0.78480 |
| `explicit.stat_2481353198@T2` | -0.73487 |
| `explicit.stat_1671376347@T1` | -0.72519 |

### weapon.twomace — n=5314, R²=-0.4552

intercept: `-10.5347`  ·  log_price: True  ·  ilvl: `0.14055`  ·  n_mods: `-0.19035`  ·  n_top_tier: `0.43501`  ·  corrupted: `0.58603`  ·  n_sockets: `0.14676`  ·  quality: `0.06447`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.00417 |
| `explicit.stat_1037193709@T1` | -1.53135 |
| `explicit.stat_3336890334@T1` | -1.27937 |
| `explicit.stat_9187492@T1` | -0.96883 |
| `explicit.stat_2694482655@T1` | 0.92789 |
| `explicit.stat_3695891184@T1` | -0.83177 |
| `explicit.stat_1263695895@T2` | -0.82628 |
| `explicit.stat_3695891184@T2` | -0.73666 |
| `explicit.stat_518292764@T1` | 0.65295 |
| `explicit.stat_691932474@T1` | -0.64351 |
| `explicit.stat_387439868@T2` | -0.59022 |
| `crafted.stat_3035140377` | 0.58665 |

## Coverage (listings per base)

- … **Sapphire** — 35402 listings (35346 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 34492 listings (34450 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 26413 listings (26382 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 12452 listings (12434 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11336 listings (11312 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10962 listings (10937 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 10853 listings (10841 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10213 listings (10190 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10149 listings (10126 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 9661 listings (9648 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8427 listings (8412 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8099 listings (8090 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8020 listings (8011 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7280 listings (7258 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6964 listings (6957 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 6948 listings (6929 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6895 listings (6881 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6843 listings (6836 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6803 listings (6775 priced) [0.3–398912568423.8 ex]
- … **Ancestral Tiara** — 6716 listings (6687 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6680 listings (6671 priced) [0.2–275252424.7 ex]
- … **Bloodstone Amulet** — 6629 listings (6619 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6300 listings (6297 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6195 listings (6181 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6035 listings (6025 priced) [0.3–398912568423.8 ex]

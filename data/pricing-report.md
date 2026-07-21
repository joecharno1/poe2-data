# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-21T13:28:47+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **710929** (708676 priced in exalted)
- Distinct bases: 1001 · distinct mods: 3320 · mod rows: 3362615
- Sold signals: **24195** sold · 404580 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-21T13:15:28+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×17.88** (median |log error| 2.8835)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.16** · typical error ×49.63 · ±30% 5% · n=103398
- Premium segment (60ex+): skill **+0.16** · typical error ×270.43 · ±30% 0% · n=68477

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 15264 | ×48.99 | 21% | +0.04 | +0.06 |
| jewel | 14627 | ×9.78 | 4% | +0.11 | +0.13 |
| accessory.amulet | 13684 | ×33.56 | 17% | +0.04 | +0.04 |
| accessory.belt | 9752 | ×20.01 | 20% | +0.05 | +0.07 |
| armour.chest | 9430 | ×13.48 | 19% | +0.09 | +0.11 |
| armour.helmet | 9229 | ×21.54 | 14% | +0.10 | +0.11 |
| armour.boots | 8520 | ×19.70 | 16% | +0.12 | +0.14 |
| armour.gloves | 8313 | ×25.24 | 11% | +0.10 | +0.12 |
| other | 8254 | ×2.02 | 41% | +0.11 | +0.16 |
| weapon.wand | 4956 | ×29.77 | 11% | +0.13 | +0.13 |
| weapon.bow | 3908 | ×19.28 | 8% | +0.19 | +0.21 |
| weapon.crossbow | 3672 | ×21.39 | 12% | +0.13 | +0.18 |
| weapon.warstaff | 2550 | ×13.38 | 7% | +0.21 | +0.21 |
| weapon.staff | 2445 | ×15.33 | 6% | +0.12 | +0.13 |
| weapon.sceptre | 2398 | ×19.59 | 5% | +0.09 | +0.09 |
| weapon.spear | 1922 | ×12.63 | 7% | +0.12 | +0.15 |
| armour.focus | 1576 | ×13.68 | 7% | +0.12 | +0.13 |
| armour.quiver | 1483 | ×16.68 | 7% | +0.12 | +0.14 |
| armour.shield | 1222 | ×8.14 | 8% | +0.10 | +0.11 |
| flask.charm | 1199 | ×10.00 | 27% | +0.02 | +0.03 |
| weapon.twomace | 1125 | ×8.88 | 7% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=80172, R²=-0.9778

intercept: `-1.8920`  ·  log_price: True  ·  ilvl: `0.02365`  ·  n_mods: `0.87512`  ·  n_top_tier: `-0.29949`  ·  corrupted: `0.29640`  ·  quality: `0.00362`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.11886 |
| `explicit.stat_1594812856@T1` | 1.68294 |
| `explicit.stat_3485067555@T1` | 1.66856 |
| `explicit.stat_239367161@T1` | -1.59775 |
| `explicit.stat_3668351662@T1` | -1.55420 |
| `explicit.stat_627767961@T1` | -1.48146 |
| `explicit.stat_3174700878@T1` | 1.48120 |
| `explicit.stat_3028809864@T1` | -1.37253 |
| `explicit.stat_234296660@T1` | -1.27904 |
| `explicit.stat_1697447343@T1` | -1.25980 |
| `explicit.stat_1869147066@T1` | -1.20315 |
| `explicit.stat_4147897060@T1` | -1.10928 |

### accessory.ring — n=69469, R²=-2.0078

intercept: `3.3372`  ·  log_price: True  ·  ilvl: `-0.04163`  ·  n_mods: `0.00067`  ·  n_top_tier: `0.99454`  ·  corrupted: `0.00793`  ·  n_sockets: `2.21786`  ·  quality: `0.02131`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.03706 |
| `explicit.stat_803737631@T1` | -1.01913 |
| `explicit.stat_4080418644@T1` | -1.01395 |
| `explicit.stat_2891184298@T2` | -1.01210 |
| `explicit.stat_2231156303@T1` | -1.01122 |
| `explicit.stat_4220027924@T2` | -1.00985 |
| `explicit.stat_2923486259@T2` | -1.00961 |
| `explicit.stat_736967255@T2` | -1.00792 |
| `explicit.stat_1263695895@T2` | -1.00782 |
| `explicit.stat_1573130764@T2` | -1.00635 |
| `explicit.stat_3917489142@T2` | -1.00285 |
| `explicit.stat_3962278098@T1` | -1.00278 |

### other — n=67696, R²=-0.6918

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.01725`  ·  n_top_tier: `0.32933`  ·  corrupted: `0.04022`  ·  n_sockets: `-0.00005`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.42814 |
| `explicit.stat_3299347043@T1` | -0.24456 |
| `explicit.stat_3917489142@T1` | -0.19657 |
| `explicit.stat_2974417149@T1` | 0.10351 |
| `explicit.stat_789117908@T1` | -0.07825 |
| `explicit.stat_736967255@T1` | -0.05390 |
| `implicit.stat_3182714256` | 0.05178 |
| `implicit.stat_718638445` | 0.05178 |
| `explicit.stat_2106365538@T1` | -0.04760 |
| `implicit.stat_2219129443` | 0.04364 |
| `implicit.stat_2901986750` | -0.03847 |
| `implicit.stat_3879011313` | 0.03293 |

### accessory.amulet — n=62370, R²=-2.1405

intercept: `3.3459`  ·  log_price: True  ·  ilvl: `-0.04244`  ·  n_mods: `-0.01717`  ·  n_top_tier: `1.24504`  ·  corrupted: `0.12496`  ·  n_sockets: `-0.05895`  ·  quality: `0.03823`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.89044 |
| `explicit.stat_3299347043@T2` | -1.75981 |
| `explicit.stat_587431675@T2` | -1.38743 |
| `explicit.stat_2974417149@T1` | -1.34227 |
| `explicit.stat_2866361420@T2` | -1.33393 |
| `explicit.stat_2866361420@T1` | -1.32926 |
| `explicit.stat_2974417149@T2` | -1.32094 |
| `explicit.stat_803737631@T1` | -1.31379 |
| `explicit.stat_4080418644@T1` | -1.29459 |
| `explicit.stat_124131830@T2` | -1.29100 |
| `explicit.stat_803737631@T2` | -1.28341 |
| `explicit.stat_2901986750@T1` | -1.28210 |

### accessory.belt — n=44609, R²=-1.778

intercept: `3.9288`  ·  log_price: True  ·  ilvl: `-0.04709`  ·  n_mods: `-0.02514`  ·  n_top_tier: `0.29504`  ·  corrupted: `1.33712`  ·  n_sockets: `1.37180`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.33825 |
| `explicit.stat_4220027924@T1` | 0.46116 |
| `explicit.stat_2923486259@T2` | 0.39103 |
| `explicit.stat_3299347043@T1` | -0.34777 |
| `explicit.stat_2881298780@T1` | -0.33569 |
| `explicit.stat_3299347043@T2` | -0.33427 |
| `explicit.stat_51994685@T1` | -0.32521 |
| `explicit.stat_915769802@T1` | -0.31985 |
| `explicit.stat_809229260@T2` | -0.31611 |
| `explicit.stat_1570770415@T2` | -0.31307 |
| `explicit.stat_3325883026@T1` | -0.30945 |
| `explicit.stat_915769802@T2` | -0.30155 |

### armour.chest — n=44197, R²=-1.6752

intercept: `3.5462`  ·  log_price: True  ·  ilvl: `-0.04377`  ·  n_mods: `-0.02118`  ·  n_top_tier: `0.38256`  ·  corrupted: `0.41902`  ·  n_sockets: `0.03563`  ·  quality: `0.06492`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.78178 |
| `explicit.stat_986397080@T2` | -0.50002 |
| `explicit.stat_3372524247@T1` | 0.49488 |
| `explicit.stat_3484657501@T1` | -0.48499 |
| `explicit.stat_986397080@T1` | -0.47843 |
| `explicit.stat_2339757871@T2` | -0.47398 |
| `explicit.stat_1692879867@T2` | -0.44528 |
| `explicit.stat_4080418644@T2` | -0.44262 |
| `explicit.stat_3301100256@T2` | -0.43467 |
| `explicit.stat_915769802@T2` | -0.42369 |
| `explicit.stat_1999113824@T2` | -0.41425 |
| `explicit.stat_4080418644@T1` | -0.40603 |

### armour.helmet — n=42974, R²=-1.5756

intercept: `3.3547`  ·  log_price: True  ·  ilvl: `-0.04254`  ·  n_mods: `-0.03459`  ·  n_top_tier: `0.61723`  ·  corrupted: `0.58628`  ·  n_sockets: `0.12090`  ·  quality: `0.06011`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.84652 |
| `crafted.stat_3917489142@T1` | 1.20771 |
| `explicit.stat_1263695895@T1` | -1.00017 |
| `explicit.stat_3917489142@T2` | -0.94140 |
| `explicit.stat_3917489142@T1` | -0.84123 |
| `explicit.stat_4052037485@T2` | -0.75592 |
| `explicit.stat_2162097452@T2` | -0.75311 |
| `explicit.stat_1999113824@T1` | -0.74695 |
| `explicit.stat_1263695895@T2` | -0.72492 |
| `explicit.stat_803737631@T1` | -0.70451 |
| `explicit.stat_1999113824@T2` | -0.70135 |
| `explicit.stat_3321629045@T2` | -0.69750 |

### armour.boots — n=39799, R²=-1.5618

intercept: `3.9211`  ·  log_price: True  ·  ilvl: `-0.04796`  ·  n_mods: `-0.04012`  ·  n_top_tier: `0.42674`  ·  corrupted: `0.05726`  ·  n_sockets: `0.09743`  ·  quality: `0.06108`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.97809 |
| `explicit.stat_2250533757@T1` | 1.74586 |
| `crafted.stat_3917489142@T1` | 1.36081 |
| `explicit.stat_2923486259@T1` | 0.77838 |
| `explicit.stat_3299347043@T1` | -0.72930 |
| `explicit.stat_2923486259@T2` | -0.56894 |
| `explicit.stat_3917489142@T2` | -0.54374 |
| `explicit.stat_2160282525@T1` | -0.52306 |
| `explicit.stat_1999113824@T2` | -0.51558 |
| `explicit.stat_1671376347@T2` | -0.50487 |
| `explicit.stat_3033371881@T2` | 0.50477 |
| `explicit.stat_1874553720@T1` | -0.49570 |

### armour.gloves — n=38821, R²=-1.464

intercept: `3.7336`  ·  log_price: True  ·  ilvl: `-0.04977`  ·  n_mods: `-0.01557`  ·  n_top_tier: `0.77127`  ·  corrupted: `0.00476`  ·  n_sockets: `0.28263`  ·  quality: `0.05063`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.43961 |
| `explicit.stat_2923486259@T1` | -1.35533 |
| `explicit.stat_3484657501@T2` | -1.14885 |
| `explicit.stat_2923486259@T2` | -1.09243 |
| `explicit.stat_3484657501@T1` | -1.05548 |
| `explicit.stat_124859000@T1` | -1.05315 |
| `explicit.stat_4052037485@T2` | -1.02469 |
| `explicit.stat_3321629045@T2` | -0.99920 |
| `explicit.stat_4052037485@T1` | -0.98736 |
| `explicit.stat_803737631@T2` | -0.93720 |
| `explicit.stat_124859000@T2` | -0.91816 |
| `explicit.stat_4015621042@T2` | -0.91558 |

### weapon.wand — n=22971, R²=-1.7012

intercept: `3.6211`  ·  log_price: True  ·  ilvl: `-0.04470`  ·  n_mods: `-0.10206`  ·  n_top_tier: `0.45045`  ·  corrupted: `0.20129`  ·  n_sockets: `0.04014`  ·  quality: `0.03562`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.07692 |
| `explicit.stat_2254480358@T1` | 2.36202 |
| `explicit.stat_1545858329@T1` | 2.20821 |
| `explicit.stat_124131830@T1` | 1.93211 |
| `explicit.stat_591105508@T1` | 1.88124 |
| `explicit.stat_736967255@T2` | 1.46594 |
| `explicit.stat_2254480358@T2` | 1.23727 |
| `explicit.stat_1263695895@T2` | -1.09787 |
| `explicit.stat_4226189338@T1` | 1.08980 |
| `crafted.stat_124131830` | 1.08735 |
| `explicit.stat_1263695895@T1` | -0.96088 |
| `explicit.stat_3962278098@T2` | -0.95836 |

### flask.charm — n=19892, R²=-0.654

intercept: `0.1120`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.70646`  ·  corrupted: `1.52895`  ·  quality: `0.01044`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.59641 |
| `explicit.stat_1056492907` | 2.61112 |
| `explicit.stat_3246948616` | 1.70919 |
| `explicit.stat_1120862500@T2` | -1.70650 |
| `explicit.stat_828533480@T2` | -1.70649 |
| `explicit.stat_1873752457@T2` | -1.70646 |
| `explicit.stat_3196823591@T2` | -1.70641 |
| `explicit.stat_2676834156@T2` | -1.70640 |
| `explicit.stat_2365392475@T2` | -1.70639 |
| `explicit.stat_828533480@T1` | -1.70524 |
| `explicit.stat_388617051@T2` | -1.70193 |
| `explicit.stat_2541588185@T2` | -1.69732 |

### weapon.bow — n=18339, R²=-1.5481

intercept: `3.6117`  ·  log_price: True  ·  ilvl: `-0.04211`  ·  n_mods: `-0.12300`  ·  n_top_tier: `0.65819`  ·  corrupted: `0.60356`  ·  n_sockets: `0.12759`  ·  quality: `0.02401`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 2.19696 |
| `desecrated.stat_210067635@T1` | -1.65786 |
| `explicit.stat_1263695895@T1` | -1.41316 |
| `crafted.stat_210067635@T2` | -1.20123 |
| `explicit.stat_1263695895@T2` | -1.17635 |
| `crafted.stat_3035140377` | 1.07335 |
| `explicit.stat_2463230181@T2` | -1.04430 |
| `explicit.stat_3695891184@T1` | -0.91818 |
| `explicit.stat_3336890334@T1` | 0.89581 |
| `explicit.stat_3695891184@T2` | -0.87609 |
| `explicit.stat_2463230181@T1` | -0.87504 |
| `explicit.stat_1368271171@T2` | -0.84728 |

### weapon.crossbow — n=17177, R²=-1.5626

intercept: `3.7827`  ·  log_price: True  ·  ilvl: `-0.04489`  ·  n_mods: `-0.11144`  ·  n_top_tier: `0.43142`  ·  corrupted: `0.04229`  ·  n_sockets: `0.10299`  ·  quality: `0.01907`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.85858 |
| `explicit.stat_2250681686@T2` | -1.42852 |
| `explicit.stat_1980802737` | 1.37635 |
| `explicit.stat_2250681686` | 1.05734 |
| `explicit.stat_1202301673@T1` | 1.04272 |
| `explicit.stat_1509134228@T1` | 0.96232 |
| `crafted.stat_3035140377` | 0.83463 |
| `explicit.stat_709508406@T1` | 0.82392 |
| `explicit.stat_3695891184@T2` | -0.79859 |
| `explicit.stat_3695891184@T1` | -0.79007 |
| `explicit.stat_3336890334@T2` | -0.73047 |
| `explicit.stat_691932474@T1` | -0.62536 |

### weapon.warstaff — n=11998, R²=-0.3401

intercept: `-10.3572`  ·  log_price: True  ·  ilvl: `0.13962`  ·  n_mods: `-0.21571`  ·  n_top_tier: `0.44599`  ·  corrupted: `0.23448`  ·  n_sockets: `0.12780`  ·  quality: `0.05501`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 1.33672 |
| `desecrated.stat_2231156303@T1` | 1.33672 |
| `crafted.stat_210067635@T2` | 0.99816 |
| `explicit.stat_328541901@T2` | -0.97678 |
| `explicit.stat_821021828@T2` | -0.86800 |
| `explicit.stat_328541901@T1` | -0.82851 |
| `desecrated.stat_9187492` | 0.80543 |
| `rune.stat_243313994` | 0.68398 |
| `explicit.stat_1037193709@T2` | -0.63703 |
| `explicit.stat_9187492@T2` | -0.58909 |
| `explicit.stat_691932474@T2` | -0.57667 |
| `explicit.stat_1037193709@T1` | 0.56304 |

### weapon.staff — n=11400, R²=-0.3606

intercept: `-15.6970`  ·  log_price: True  ·  ilvl: `0.19968`  ·  n_mods: `-0.07081`  ·  n_top_tier: `0.48415`  ·  corrupted: `0.72237`  ·  n_sockets: `0.15911`  ·  quality: `0.03481`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.01872 |
| `explicit.stat_1600707273@T1` | 1.60090 |
| `explicit.stat_124131830@T1` | 1.58413 |
| `explicit.stat_1545858329@T1` | 1.48696 |
| `explicit.stat_591105508@T1` | 1.30024 |
| `explicit.stat_293638271@T2` | -1.07214 |
| `explicit.stat_473429811@T2` | -0.86731 |
| `explicit.stat_2254480358@T1` | 0.85727 |
| `explicit.stat_3962278098@T2` | 0.80875 |
| `explicit.stat_124131830@T2` | 0.62620 |
| `crafted.stat_124131830` | 0.61568 |
| `explicit.stat_3015669065@T2` | -0.55912 |

### weapon.sceptre — n=11191, R²=-0.3466

intercept: `-20.7126`  ·  log_price: True  ·  ilvl: `0.26227`  ·  n_mods: `-0.03439`  ·  n_top_tier: `0.04995`  ·  corrupted: `0.33373`  ·  n_sockets: `0.20836`  ·  quality: `0.03915`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.72020 |
| `explicit.stat_2162097452@T2` | 1.43978 |
| `explicit.stat_3057012405@T1` | 1.15585 |
| `explicit.stat_1263695895@T2` | -1.06647 |
| `explicit.stat_1263695895@T1` | -1.00584 |
| `explicit.stat_101878827@T2` | 0.95502 |
| `explicit.stat_101878827@T1` | 0.93852 |
| `explicit.stat_1798257884@T2` | 0.93358 |
| `explicit.stat_2854751904@T2` | -0.64878 |
| `explicit.stat_2347036682@T2` | -0.56185 |
| `explicit.stat_849987426@T2` | 0.52440 |
| `explicit.stat_849987426@T1` | 0.52153 |

### weapon.spear — n=9061, R²=-0.3867

intercept: `-13.2262`  ·  log_price: True  ·  ilvl: `0.17906`  ·  n_mods: `-0.12147`  ·  n_top_tier: `0.57668`  ·  corrupted: `-0.52723`  ·  n_sockets: `0.16890`  ·  quality: `0.07362`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -5.12335 |
| `crafted.stat_210067635@T2` | -3.33276 |
| `explicit.stat_1202301673@T1` | 0.97952 |
| `explicit.stat_1940865751@T2` | -0.97299 |
| `crafted.stat_3035140377` | 0.97140 |
| `explicit.stat_3336890334@T2` | -0.96920 |
| `explicit.stat_9187492@T1` | 0.95179 |
| `desecrated.stat_210067635@T1` | -0.91470 |
| `explicit.stat_4080418644@T2` | -0.89475 |
| `explicit.stat_1037193709@T1` | -0.87498 |
| `explicit.stat_691932474@T2` | -0.84537 |
| `explicit.stat_748522257@T2` | -0.78222 |

### armour.focus — n=7419, R²=-0.3346

intercept: `-15.4003`  ·  log_price: True  ·  ilvl: `0.19486`  ·  n_mods: `-0.11960`  ·  n_top_tier: `0.94711`  ·  corrupted: `0.09093`  ·  n_sockets: `0.27256`  ·  quality: `0.02999`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 2.99733 |
| `explicit.stat_2923486259@T1` | -1.65221 |
| `explicit.stat_4220027924@T1` | -1.48663 |
| `explicit.stat_2923486259@T2` | -1.17932 |
| `explicit.stat_4220027924@T2` | -1.15695 |
| `explicit.stat_2231156303@T2` | -1.08551 |
| `explicit.stat_2339757871@T2` | -1.06180 |
| `explicit.stat_4015621042@T1` | -1.05665 |
| `explicit.stat_2231156303@T1` | -1.02371 |
| `explicit.stat_1050105434@T2` | -1.00295 |
| `explicit.stat_737908626@T2` | -0.96946 |
| `explicit.stat_2768835289@T1` | -0.95437 |

### armour.quiver — n=6901, R²=-0.2868

intercept: `-18.3952`  ·  log_price: True  ·  ilvl: `0.21850`  ·  n_mods: `-0.03422`  ·  n_top_tier: `0.72582`  ·  corrupted: `0.98741`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.74294 |
| `explicit.stat_681332047@T2` | -1.52998 |
| `explicit.stat_681332047@T1` | -1.31885 |
| `explicit.stat_1573130764@T2` | -1.11004 |
| `explicit.stat_1573130764@T1` | -1.06321 |
| `explicit.stat_2194114101@T2` | -0.92620 |
| `explicit.stat_4067062424@T1` | -0.73837 |
| `explicit.stat_803737631@T1` | -0.67020 |
| `explicit.stat_3261801346@T1` | -0.64351 |
| `explicit.stat_2321178454@T2` | -0.63601 |
| `explicit.stat_2463230181@T1` | 0.57758 |
| `explicit.stat_803737631@T2` | -0.55520 |

### armour.shield — n=5946, R²=-0.4275

intercept: `-12.7654`  ·  log_price: True  ·  ilvl: `0.16896`  ·  n_mods: `-0.14226`  ·  n_top_tier: `0.61756`  ·  corrupted: `-0.27004`  ·  n_sockets: `0.39898`  ·  quality: `0.04782`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.29560 |
| `explicit.stat_2901986750@T1` | -1.26200 |
| `explicit.stat_328541901@T1` | -1.18477 |
| `explicit.stat_3321629045@T2` | -1.07925 |
| `explicit.stat_2481353198@T1` | -1.07870 |
| `explicit.stat_2481353198@T2` | -1.03527 |
| `explicit.stat_3033371881@T2` | -0.96771 |
| `explicit.stat_4095671657@T2` | -0.96206 |
| `explicit.stat_328541901@T2` | -0.92770 |
| `explicit.stat_3484657501@T1` | -0.90684 |
| `explicit.stat_2923486259@T1` | -0.90220 |
| `explicit.stat_4095671657@T1` | -0.85982 |

### weapon.twomace — n=5424, R²=-0.4513

intercept: `-11.9070`  ·  log_price: True  ·  ilvl: `0.15731`  ·  n_mods: `-0.20723`  ·  n_top_tier: `0.40603`  ·  corrupted: `0.76130`  ·  n_sockets: `0.12962`  ·  quality: `0.06945`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.08677 |
| `explicit.stat_1037193709@T1` | -1.78777 |
| `explicit.stat_1263695895@T2` | -1.54601 |
| `explicit.stat_3336890334@T1` | -1.35467 |
| `explicit.stat_1263695895@T1` | -1.16911 |
| `explicit.stat_2694482655@T1` | 0.98175 |
| `explicit.stat_9187492@T1` | -0.83453 |
| `explicit.stat_3695891184@T1` | -0.82807 |
| `explicit.stat_518292764@T2` | -0.76782 |
| `explicit.stat_3695891184@T2` | -0.74051 |
| `explicit.stat_691932474@T1` | -0.65381 |
| `explicit.stat_821021828@T1` | -0.61839 |

## Coverage (listings per base)

- … **Sapphire** — 36852 listings (36793 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 35926 listings (35881 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 27464 listings (27433 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 12739 listings (12721 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11670 listings (11646 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 11327 listings (11301 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 11194 listings (11182 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10510 listings (10484 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10466 listings (10443 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 9947 listings (9934 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8680 listings (8665 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8327 listings (8318 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8261 listings (8252 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7410 listings (7387 priced) [0.3–4297682211.9 ex]
- … **Unset Ring** — 7180 listings (7161 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7166 listings (7159 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 7104 listings (7089 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 7041 listings (7033 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6945 listings (6917 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6913 listings (6904 priced) [0.2–275252424.7 ex]
- … **Ancestral Tiara** — 6875 listings (6846 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6810 listings (6800 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6493 listings (6490 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6383 listings (6369 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6167 listings (6155 priced) [0.3–398912568423.8 ex]

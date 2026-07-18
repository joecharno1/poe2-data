# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-18T17:02:15+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **623073** (621186 priced in exalted)
- Distinct bases: 993 · distinct mods: 3253 · mod rows: 2950667
- Sold signals: **24894** sold · 354441 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-18T16:49:47+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.55** (median |log error| 3.1157)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.15** · typical error ×57.57 · ±30% 5% · n=90899
- Premium segment (60ex+): skill **+0.15** · typical error ×245.70 · ±30% 0% · n=61828

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 13015 | ×55.56 | 21% | +0.03 | +0.05 |
| jewel | 12227 | ×10.77 | 5% | +0.08 | +0.11 |
| accessory.amulet | 11844 | ×48.70 | 19% | +0.04 | +0.04 |
| accessory.belt | 8650 | ×19.28 | 5% | +0.05 | +0.07 |
| armour.chest | 8368 | ×16.64 | 8% | +0.11 | +0.13 |
| armour.helmet | 8182 | ×18.14 | 6% | +0.10 | +0.13 |
| armour.boots | 7610 | ×32.86 | 16% | +0.11 | +0.14 |
| armour.gloves | 7466 | ×31.73 | 9% | +0.12 | +0.14 |
| other | 7340 | ×2.00 | 42% | +0.10 | +0.16 |
| weapon.wand | 4517 | ×49.13 | 17% | +0.08 | +0.11 |
| weapon.bow | 3541 | ×27.40 | 12% | +0.14 | +0.16 |
| weapon.crossbow | 3330 | ×31.67 | 16% | +0.09 | +0.14 |
| weapon.warstaff | 2215 | ×25.85 | 6% | +0.19 | +0.19 |
| weapon.staff | 2080 | ×36.05 | 5% | +0.15 | +0.14 |
| weapon.sceptre | 2043 | ×29.34 | 5% | +0.19 | +0.18 |
| weapon.spear | 1620 | ×31.60 | 9% | +0.10 | +0.11 |
| armour.focus | 1367 | ×18.65 | 7% | +0.15 | +0.16 |
| armour.quiver | 1309 | ×25.36 | 7% | +0.16 | +0.18 |
| armour.shield | 1065 | ×22.97 | 8% | +0.07 | +0.10 |
| flask.charm | 1048 | ×15.76 | 29% | +0.01 | +0.03 |
| weapon.twomace | 985 | ×7.94 | 10% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=66779, R²=-0.953

intercept: `-1.8647`  ·  log_price: True  ·  ilvl: `0.02529`  ·  n_mods: `0.87176`  ·  n_top_tier: `-0.33566`  ·  corrupted: `0.25138`  ·  quality: `-0.00336`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.14602 |
| `explicit.stat_3374165039@T1` | -2.33600 |
| `explicit.stat_3780644166@T1` | -2.18661 |
| `explicit.stat_3485067555@T1` | 1.88973 |
| `explicit.stat_4147897060@T1` | -1.66016 |
| `explicit.stat_1805182458@T1` | -1.60038 |
| `explicit.stat_21071013@T1` | 1.59810 |
| `explicit.stat_318953428@T1` | -1.56929 |
| `explicit.stat_2523933828@T1` | -1.50788 |
| `explicit.stat_1697447343@T1` | -1.37674 |
| `explicit.stat_627767961@T1` | -1.33346 |
| `explicit.stat_1315743832@T1` | -1.30044 |

### other — n=59571, R²=-0.6229

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00003`  ·  n_top_tier: `0.34731`  ·  corrupted: `0.33683`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_2219129443` | 0.41386 |
| `explicit.stat_1050105434@T1` | -0.35155 |
| `implicit.stat_3879011313` | 0.31476 |
| `implicit.stat_4041853756` | 0.22801 |
| `explicit.stat_3299347043@T1` | -0.19907 |
| `explicit.stat_2974417149@T1` | 0.12669 |
| `explicit.stat_736967255@T1` | 0.10136 |
| `explicit.stat_3917489142@T1` | 0.09766 |
| `implicit.stat_1379411836` | -0.08514 |
| `explicit.stat_3291658075@T1` | -0.07981 |
| `explicit.stat_2482852589@T1` | 0.07947 |
| `explicit.stat_789117908@T1` | -0.07365 |

### accessory.ring — n=59427, R²=-2.0388

intercept: `3.4379`  ·  log_price: True  ·  ilvl: `-0.04249`  ·  n_mods: `-0.00003`  ·  n_top_tier: `1.08819`  ·  corrupted: `0.02300`  ·  n_sockets: `0.31944`  ·  quality: `0.01339`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.13390 |
| `explicit.stat_1573130764@T2` | -1.13042 |
| `explicit.stat_2231156303@T1` | -1.12841 |
| `explicit.stat_4220027924@T2` | -1.11365 |
| `explicit.stat_3325883026@T1` | -1.11166 |
| `explicit.stat_789117908@T2` | -1.10835 |
| `explicit.stat_4080418644@T1` | -1.10807 |
| `explicit.stat_803737631@T1` | -1.10785 |
| `explicit.stat_789117908@T1` | -1.10624 |
| `explicit.stat_3325883026@T2` | -1.10304 |
| `explicit.stat_2923486259@T2` | -1.10178 |
| `explicit.stat_3032590688@T2` | -1.10105 |

### accessory.amulet — n=53992, R²=-2.1665

intercept: `3.7272`  ·  log_price: True  ·  ilvl: `-0.04547`  ·  n_mods: `-0.02068`  ·  n_top_tier: `1.28064`  ·  corrupted: `0.04267`  ·  n_sockets: `-0.14706`  ·  quality: `0.00117`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.77539 |
| `explicit.stat_3299347043@T2` | -1.51784 |
| `explicit.stat_587431675@T2` | -1.36002 |
| `explicit.stat_2974417149@T1` | -1.34895 |
| `explicit.stat_2866361420@T2` | -1.33610 |
| `explicit.stat_2974417149@T2` | -1.33570 |
| `explicit.stat_472520716@T2` | -1.33492 |
| `explicit.stat_803737631@T1` | -1.33288 |
| `explicit.stat_2866361420@T1` | -1.33078 |
| `explicit.stat_1050105434@T2` | -1.32747 |
| `explicit.stat_803737631@T2` | -1.32029 |
| `explicit.stat_789117908@T1` | -1.30933 |

### accessory.belt — n=39703, R²=-0.873

intercept: `7.1379`  ·  log_price: True  ·  ilvl: `-0.06614`  ·  n_mods: `-0.32345`  ·  n_top_tier: `0.90917`  ·  corrupted: `1.24840`  ·  n_sockets: `0.38935`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.73162 |
| `implicit.stat_731781020` | -1.56423 |
| `explicit.stat_3299347043@T2` | -1.29192 |
| `explicit.stat_2881298780@T1` | -1.16758 |
| `explicit.stat_51994685@T1` | -1.11872 |
| `explicit.stat_1389754388@T1` | -1.09900 |
| `explicit.stat_3372524247@T2` | -1.06569 |
| `explicit.stat_644456512@T1` | -1.05753 |
| `explicit.stat_1570770415@T1` | -1.05722 |
| `explicit.stat_1570770415@T2` | -0.97616 |
| `explicit.stat_4220027924@T2` | -0.95619 |
| `explicit.stat_809229260@T2` | -0.94605 |

### armour.chest — n=39384, R²=-1.2857

intercept: `4.0999`  ·  log_price: True  ·  ilvl: `-0.04842`  ·  n_mods: `-0.09399`  ·  n_top_tier: `0.47794`  ·  corrupted: `0.22539`  ·  n_sockets: `0.16239`  ·  quality: `0.04887`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.99658 |
| `explicit.stat_986397080@T2` | -0.83582 |
| `explicit.stat_3484657501@T1` | -0.77637 |
| `explicit.stat_3981240776@T1` | 0.71656 |
| `explicit.stat_986397080@T1` | -0.70383 |
| `explicit.stat_124859000@T1` | -0.68783 |
| `explicit.stat_2339757871@T2` | -0.65094 |
| `explicit.stat_3301100256@T2` | -0.64863 |
| `explicit.stat_1692879867@T2` | -0.63867 |
| `explicit.stat_3033371881@T1` | 0.62355 |
| `explicit.stat_915769802@T2` | -0.60421 |
| `explicit.stat_3299347043@T2` | -0.58590 |

### armour.helmet — n=38321, R²=-1.0646

intercept: `3.7492`  ·  log_price: True  ·  ilvl: `-0.04629`  ·  n_mods: `-0.09345`  ·  n_top_tier: `0.47766`  ·  corrupted: `0.67112`  ·  n_sockets: `0.13262`  ·  quality: `0.04991`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | -3.44583 |
| `explicit.stat_2339757871@T1` | -2.43580 |
| `explicit.stat_3917489142@T2` | -1.22914 |
| `explicit.stat_1999113824@T1` | -0.90793 |
| `explicit.stat_3917489142@T1` | -0.84707 |
| `explicit.stat_803737631@T2` | -0.81941 |
| `explicit.stat_803737631@T1` | -0.76296 |
| `explicit.stat_3321629045@T2` | -0.70135 |
| `explicit.stat_2162097452@T2` | -0.68545 |
| `explicit.stat_4052037485@T2` | -0.64203 |
| `explicit.stat_2451402625@T2` | -0.63554 |
| `explicit.stat_1999113824@T2` | -0.60748 |

### armour.boots — n=35633, R²=-1.489

intercept: `4.0247`  ·  log_price: True  ·  ilvl: `-0.04908`  ·  n_mods: `-0.04570`  ·  n_top_tier: `0.61730`  ·  corrupted: `-0.01929`  ·  n_sockets: `0.07103`  ·  quality: `0.05943`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.58258 |
| `crafted.stat_3917489142@T1` | 1.33788 |
| `explicit.stat_2339757871@T1` | -1.27328 |
| `explicit.stat_3299347043@T1` | -0.94763 |
| `explicit.stat_3917489142@T2` | -0.85599 |
| `explicit.stat_2923486259@T2` | -0.73954 |
| `explicit.stat_1062208444@T2` | -0.73134 |
| `explicit.stat_1874553720@T1` | -0.71777 |
| `explicit.stat_2923486259@T1` | 0.70577 |
| `explicit.stat_2160282525@T1` | -0.70080 |
| `explicit.stat_3484657501@T2` | -0.69724 |
| `explicit.stat_1999113824@T2` | -0.69379 |

### armour.gloves — n=34698, R²=-1.3536

intercept: `3.9035`  ·  log_price: True  ·  ilvl: `-0.04973`  ·  n_mods: `-0.06043`  ·  n_top_tier: `0.65175`  ·  corrupted: `0.07834`  ·  n_sockets: `0.18837`  ·  quality: `0.04262`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.47131 |
| `explicit.stat_2923486259@T1` | -1.27619 |
| `explicit.stat_3484657501@T2` | -1.13640 |
| `rune.stat_201332984` | 1.07673 |
| `explicit.stat_3484657501@T1` | -1.04777 |
| `explicit.stat_3321629045@T2` | -0.94499 |
| `explicit.stat_803737631@T2` | -0.90019 |
| `explicit.stat_803737631@T1` | -0.88093 |
| `explicit.stat_9187492@T1` | 0.80076 |
| `explicit.stat_9187492@T2` | -0.79806 |
| `explicit.stat_3917489142@T2` | -0.78922 |
| `explicit.stat_2923486259@T2` | -0.76786 |

### weapon.wand — n=21128, R²=-2.0879

intercept: `3.6956`  ·  log_price: True  ·  ilvl: `-0.04576`  ·  n_mods: `-0.04074`  ·  n_top_tier: `0.39064`  ·  corrupted: `-0.02286`  ·  n_sockets: `0.06501`  ·  quality: `0.01727`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.09153 |
| `rune.stat_124131830` | -2.64780 |
| `explicit.stat_2254480358@T1` | 2.49113 |
| `explicit.stat_124131830@T1` | 2.14329 |
| `explicit.stat_4226189338@T1` | 1.94681 |
| `explicit.stat_591105508@T1` | 1.88312 |
| `explicit.stat_736967255@T2` | 1.73321 |
| `crafted.stat_124131830` | 1.29314 |
| `explicit.stat_1600707273@T1` | 1.03179 |
| `explicit.stat_4226189338@T2` | 0.98315 |
| `explicit.stat_2254480358@T2` | 0.95370 |
| `explicit.stat_1263695895@T2` | -0.75221 |

### flask.charm — n=16950, R²=-0.6053

intercept: `0.0755`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.89623`  ·  corrupted: `1.60859`  ·  quality: `0.00043`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.77830 |
| `explicit.stat_1056492907` | 2.90652 |
| `explicit.stat_828533480@T2` | -1.89627 |
| `explicit.stat_1873752457@T2` | -1.89623 |
| `explicit.stat_1120862500@T2` | -1.89623 |
| `explicit.stat_388617051@T2` | -1.89622 |
| `explicit.stat_1873752457@T1` | -1.89621 |
| `explicit.stat_3196823591@T2` | -1.89620 |
| `explicit.stat_2676834156@T2` | -1.89619 |
| `explicit.stat_2365392475@T2` | -1.89618 |
| `explicit.stat_828533480@T1` | -1.89489 |
| `explicit.stat_1366840608@T2` | -1.89164 |

### weapon.bow — n=16885, R²=-1.7884

intercept: `3.7979`  ·  log_price: True  ·  ilvl: `-0.04320`  ·  n_mods: `-0.12464`  ·  n_top_tier: `0.63078`  ·  corrupted: `0.34114`  ·  n_sockets: `0.09365`  ·  quality: `0.03296`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.03881 |
| `crafted.stat_3035140377` | 1.36827 |
| `explicit.stat_2463230181@T2` | -1.16013 |
| `explicit.stat_1263695895@T1` | -1.15648 |
| `desecrated.stat_210067635@T1` | -1.11139 |
| `explicit.stat_1263695895@T2` | -0.98630 |
| `explicit.stat_2463230181@T1` | -0.95711 |
| `explicit.stat_3336890334@T1` | 0.95477 |
| `explicit.stat_3695891184@T2` | -0.88997 |
| `explicit.stat_3695891184@T1` | -0.86715 |
| `explicit.stat_1509134228@T1` | -0.81439 |
| `explicit.stat_518292764@T2` | -0.80594 |

### weapon.crossbow — n=15811, R²=-1.8468

intercept: `3.8751`  ·  log_price: True  ·  ilvl: `-0.04633`  ·  n_mods: `-0.07586`  ·  n_top_tier: `0.59868`  ·  corrupted: `0.03069`  ·  n_sockets: `0.06489`  ·  quality: `0.01667`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.81773 |
| `explicit.stat_1980802737` | 1.26543 |
| `explicit.stat_2250681686@T2` | -1.22945 |
| `explicit.stat_1202301673@T1` | 1.07767 |
| `explicit.stat_2250681686` | 0.85491 |
| `rune.stat_731403740` | 0.79974 |
| `explicit.stat_1509134228@T2` | -0.79490 |
| `explicit.stat_1263695895@T2` | -0.78683 |
| `crafted.stat_3035140377` | 0.78051 |
| `explicit.stat_709508406@T1` | 0.76984 |
| `explicit.stat_2694482655@T1` | -0.74296 |
| `explicit.stat_3336890334@T2` | -0.73450 |

### weapon.warstaff — n=10549, R²=-0.3591

intercept: `-10.5226`  ·  log_price: True  ·  ilvl: `0.14310`  ·  n_mods: `-0.22778`  ·  n_top_tier: `0.25932`  ·  corrupted: `0.35442`  ·  n_sockets: `0.17841`  ·  quality: `0.05674`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 3.12947 |
| `desecrated.stat_2527686725@T1` | 3.12947 |
| `crafted.stat_210067635@T2` | 1.42328 |
| `desecrated.stat_473429811@T1` | -1.06351 |
| `desecrated.stat_3291658075@T1` | -1.06351 |
| `rune.stat_243313994` | 0.88138 |
| `desecrated.stat_9187492` | 0.77471 |
| `explicit.stat_328541901@T1` | -0.73285 |
| `explicit.stat_1509134228@T1` | 0.67745 |
| `explicit.stat_328541901@T2` | -0.66175 |
| `explicit.stat_9187492@T1` | 0.62235 |
| `explicit.stat_1037193709@T1` | 0.61788 |

### weapon.staff — n=9904, R²=-0.3769

intercept: `-16.1418`  ·  log_price: True  ·  ilvl: `0.20816`  ·  n_mods: `-0.14461`  ·  n_top_tier: `0.53279`  ·  corrupted: `0.57214`  ·  n_sockets: `0.20803`  ·  quality: `0.03465`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.90933 |
| `explicit.stat_4226189338@T1` | 1.89776 |
| `explicit.stat_591105508@T1` | 1.70470 |
| `explicit.stat_293638271@T2` | -1.59580 |
| `explicit.stat_124131830@T1` | 1.54608 |
| `explicit.stat_1600707273@T1` | 0.97088 |
| `rune.stat_124131830` | 0.92544 |
| `explicit.stat_274716455@T1` | -0.91523 |
| `explicit.stat_2254480358@T2` | 0.76176 |
| `explicit.stat_124131830@T2` | 0.72470 |
| `explicit.stat_591105508@T2` | 0.69730 |
| `explicit.stat_2254480358@T1` | 0.66437 |

### weapon.sceptre — n=9758, R²=-0.3309

intercept: `-20.8241`  ·  log_price: True  ·  ilvl: `0.27044`  ·  n_mods: `-0.04833`  ·  n_top_tier: `-0.01168`  ·  corrupted: `0.33786`  ·  n_sockets: `0.25092`  ·  quality: `0.03092`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.76891 |
| `explicit.stat_1250712710@T2` | 1.68600 |
| `explicit.stat_2162097452@T2` | 1.64869 |
| `explicit.stat_3057012405@T1` | 1.53252 |
| `explicit.stat_101878827@T2` | 0.93493 |
| `explicit.stat_101878827@T1` | 0.92660 |
| `explicit.stat_849987426@T1` | 0.88637 |
| `explicit.stat_1250712710@T1` | 0.73293 |
| `explicit.stat_1798257884@T2` | 0.72433 |
| `desecrated.stat_2162097452` | 0.67905 |
| `explicit.stat_1050105434@T1` | 0.65219 |
| `explicit.stat_1998951374@T1` | 0.63946 |

### weapon.spear — n=7917, R²=-0.3971

intercept: `-12.7279`  ·  log_price: True  ·  ilvl: `0.17715`  ·  n_mods: `-0.20831`  ·  n_top_tier: `0.69271`  ·  corrupted: `0.07338`  ·  n_sockets: `0.21351`  ·  quality: `0.07879`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -5.27094 |
| `explicit.stat_1202301673@T1` | 1.39456 |
| `explicit.stat_4080418644@T2` | -1.27667 |
| `explicit.stat_1509134228@T1` | 1.27291 |
| `desecrated.stat_210067635@T1` | -1.14507 |
| `explicit.stat_9187492@T1` | 1.03673 |
| `explicit.stat_4080418644@T1` | -1.01233 |
| `explicit.stat_1940865751@T2` | -0.95796 |
| `explicit.stat_9187492@T2` | -0.95312 |
| `explicit.stat_3261801346@T1` | -0.94237 |
| `explicit.stat_691932474@T2` | -0.93750 |
| `explicit.stat_3336890334@T2` | -0.88128 |

### armour.focus — n=6476, R²=-0.3553

intercept: `-14.4202`  ·  log_price: True  ·  ilvl: `0.18674`  ·  n_mods: `-0.16935`  ·  n_top_tier: `0.88519`  ·  corrupted: `0.28350`  ·  n_sockets: `0.47619`  ·  quality: `0.06045`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 3.43846 |
| `explicit.stat_2923486259@T1` | -1.54017 |
| `explicit.stat_4220027924@T2` | -1.39332 |
| `explicit.stat_4220027924@T1` | -1.36784 |
| `explicit.stat_2231156303@T2` | -1.12733 |
| `explicit.stat_2974417149@T1` | -1.10834 |
| `explicit.stat_3291658075@T1` | -1.06056 |
| `explicit.stat_2974417149@T2` | -0.99492 |
| `explicit.stat_274716455@T2` | -0.96190 |
| `explicit.stat_736967255@T2` | -0.93724 |
| `explicit.stat_737908626@T2` | -0.91622 |
| `explicit.stat_1050105434@T2` | -0.86834 |

### armour.quiver — n=6082, R²=-0.2994

intercept: `-15.5771`  ·  log_price: True  ·  ilvl: `0.19060`  ·  n_mods: `-0.11959`  ·  n_top_tier: `0.85776`  ·  corrupted: `0.69405`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.40715 |
| `explicit.stat_2463230181@T1` | 2.54731 |
| `explicit.stat_681332047@T2` | -1.40885 |
| `explicit.stat_1573130764@T1` | -1.38293 |
| `explicit.stat_2463230181@T2` | 1.18742 |
| `explicit.stat_803737631@T2` | -0.98913 |
| `explicit.stat_4067062424@T1` | -0.93910 |
| `explicit.stat_1573130764@T2` | -0.92401 |
| `explicit.stat_2321178454@T2` | -0.91667 |
| `explicit.stat_803737631@T1` | -0.87471 |
| `explicit.stat_681332047@T1` | -0.87270 |
| `explicit.stat_4067062424@T2` | -0.83031 |

### armour.shield — n=5271, R²=-0.4602

intercept: `-12.5864`  ·  log_price: True  ·  ilvl: `0.16658`  ·  n_mods: `-0.06893`  ·  n_top_tier: `0.64668`  ·  corrupted: `-0.31024`  ·  n_sockets: `0.36026`  ·  quality: `0.06781`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.35369 |
| `explicit.stat_3321629045@T2` | -1.30736 |
| `explicit.stat_1301765461@T1` | 1.25659 |
| `explicit.stat_328541901@T1` | -1.05013 |
| `explicit.stat_4095671657@T1` | -1.04076 |
| `explicit.stat_3484657501@T2` | -0.92365 |
| `explicit.stat_2901986750@T1` | -0.91828 |
| `explicit.stat_3033371881@T2` | -0.91721 |
| `explicit.stat_2451402625@T1` | -0.89491 |
| `explicit.stat_3855016469@T1` | -0.86279 |
| `explicit.stat_2451402625@T2` | -0.84674 |
| `explicit.stat_3261801346@T1` | -0.79709 |

### weapon.twomace — n=4853, R²=-0.4499

intercept: `-10.3323`  ·  log_price: True  ·  ilvl: `0.14314`  ·  n_mods: `-0.21674`  ·  n_top_tier: `0.31134`  ·  corrupted: `0.02750`  ·  n_sockets: `0.13327`  ·  quality: `0.05993`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.16318 |
| `desecrated.stat_1509134228@T1` | 1.78486 |
| `explicit.stat_1037193709@T1` | -1.36537 |
| `explicit.stat_3336890334@T1` | -0.95369 |
| `explicit.stat_9187492@T1` | -0.81981 |
| `explicit.stat_387439868@T2` | -0.75950 |
| `crafted.stat_3035140377` | 0.70992 |
| `explicit.stat_1263695895@T2` | -0.70655 |
| `explicit.stat_210067635@T2` | 0.57157 |
| `explicit.stat_691932474@T1` | -0.53227 |
| `explicit.stat_1509134228@T1` | 0.50406 |
| `explicit.stat_3695891184@T1` | -0.50378 |

## Coverage (listings per base)

- … **Sapphire** — 30999 listings (30945 priced) [0.3–885594757.8 ex]
- … **Emerald** — 30136 listings (30095 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 23089 listings (23059 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11320 listings (11305 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10118 listings (10097 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 9784 listings (9760 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9639 listings (9631 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 9117 listings (9098 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9001 listings (8982 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8699 listings (8687 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7478 listings (7465 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7227 listings (7219 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7117 listings (7111 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6765 listings (6744 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6286 listings (6279 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 6193 listings (6165 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 6167 listings (6150 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6158 listings (6146 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6116 listings (6109 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6075 listings (6048 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 5993 listings (5984 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5896 listings (5889 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5605 listings (5602 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5575 listings (5563 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5468 listings (5459 priced) [0.3–398912568423.8 ex]

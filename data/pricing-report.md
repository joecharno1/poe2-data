# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-19T16:20:02+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **656117** (654067 priced in exalted)
- Distinct bases: 996 · distinct mods: 3282 · mod rows: 3107694
- Sold signals: **24563** sold · 373402 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-19T16:06:51+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×21.45** (median |log error| 3.0655)
- Within ±30% of asking price: **13%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.16** · typical error ×54.35 · ±30% 5% · n=95722
- Premium segment (60ex+): skill **+0.16** · typical error ×221.25 · ±30% 0% · n=64463

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 13803 | ×56.08 | 21% | +0.03 | +0.05 |
| jewel | 13190 | ×10.19 | 5% | +0.10 | +0.11 |
| accessory.amulet | 12531 | ×42.47 | 18% | +0.04 | +0.04 |
| accessory.belt | 9043 | ×15.00 | 5% | +0.02 | +0.05 |
| armour.chest | 8773 | ×14.86 | 8% | +0.12 | +0.14 |
| armour.helmet | 8548 | ×17.30 | 6% | +0.11 | +0.14 |
| armour.boots | 7951 | ×27.35 | 15% | +0.12 | +0.14 |
| armour.gloves | 7750 | ×27.04 | 8% | +0.13 | +0.14 |
| other | 7676 | ×5.03 | 37% | +0.09 | +0.15 |
| weapon.wand | 4673 | ×45.02 | 15% | +0.09 | +0.11 |
| weapon.bow | 3677 | ×29.04 | 13% | +0.14 | +0.16 |
| weapon.crossbow | 3481 | ×28.13 | 16% | +0.10 | +0.14 |
| weapon.warstaff | 2347 | ×18.82 | 7% | +0.21 | +0.22 |
| weapon.staff | 2242 | ×23.46 | 6% | +0.17 | +0.16 |
| weapon.sceptre | 2206 | ×22.50 | 5% | +0.13 | +0.13 |
| weapon.spear | 1690 | ×20.10 | 8% | +0.12 | +0.13 |
| armour.focus | 1459 | ×18.43 | 6% | +0.11 | +0.12 |
| armour.quiver | 1376 | ×24.20 | 7% | +0.16 | +0.18 |
| flask.charm | 1136 | ×14.98 | 28% | +0.01 | +0.03 |
| armour.shield | 1124 | ×16.63 | 7% | +0.09 | +0.11 |
| weapon.twomace | 1044 | ×8.26 | 8% | +0.11 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=71418, R²=-0.9668

intercept: `-1.9159`  ·  log_price: True  ·  ilvl: `0.02533`  ·  n_mods: `0.90712`  ·  n_top_tier: `-0.35913`  ·  corrupted: `0.33367`  ·  quality: `-0.00481`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.50265 |
| `explicit.stat_3485067555@T1` | 2.34423 |
| `explicit.stat_3374165039@T1` | -2.26293 |
| `explicit.stat_1594812856@T1` | 1.71251 |
| `explicit.stat_1569101201@T1` | -1.64032 |
| `explicit.stat_2523933828@T1` | -1.61151 |
| `explicit.stat_1805182458@T1` | -1.59036 |
| `explicit.stat_4147897060@T1` | -1.50347 |
| `explicit.stat_3780644166@T1` | -1.43126 |
| `explicit.stat_21071013@T1` | 1.36496 |
| `explicit.stat_3473929743@T1` | -1.35214 |
| `explicit.stat_3377888098@T1` | -1.28620 |

### accessory.ring — n=63039, R²=-2.0255

intercept: `3.3509`  ·  log_price: True  ·  ilvl: `-0.04142`  ·  n_mods: `0.00096`  ·  n_top_tier: `1.07434`  ·  corrupted: `0.01378`  ·  n_sockets: `0.12394`  ·  quality: `0.02584`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.10724 |
| `explicit.stat_1573130764@T2` | -1.09773 |
| `explicit.stat_2231156303@T1` | -1.09738 |
| `explicit.stat_4220027924@T2` | -1.09578 |
| `explicit.stat_803737631@T1` | -1.09363 |
| `explicit.stat_4080418644@T1` | -1.08970 |
| `explicit.stat_2901986750@T2` | -1.08684 |
| `explicit.stat_789117908@T1` | -1.08668 |
| `explicit.stat_789117908@T2` | -1.08471 |
| `explicit.stat_736967255@T2` | -1.08364 |
| `explicit.stat_3325883026@T1` | -1.08325 |
| `explicit.stat_3917489142@T2` | -1.08088 |

### other — n=62487, R²=-0.5619

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.46133`  ·  corrupted: `0.23411`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.46577 |
| `explicit.stat_3141070085@T1` | -0.42825 |
| `explicit.stat_3299347043@T1` | -0.37895 |
| `explicit.stat_2106365538@T1` | -0.34555 |
| `explicit.stat_3291658075@T1` | -0.29294 |
| `explicit.stat_2231156303@T1` | -0.26815 |
| `explicit.stat_789117908@T1` | -0.26700 |
| `explicit.stat_2482852589@T1` | 0.25425 |
| `implicit.stat_2219129443` | 0.23211 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_101878827@T1` | -0.21988 |

### accessory.amulet — n=57008, R²=-2.1678

intercept: `3.6081`  ·  log_price: True  ·  ilvl: `-0.04432`  ·  n_mods: `-0.02272`  ·  n_top_tier: `1.44040`  ·  corrupted: `0.04911`  ·  n_sockets: `-0.13690`  ·  quality: `0.01501`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -2.09430 |
| `explicit.stat_3299347043@T2` | -1.83489 |
| `explicit.stat_587431675@T2` | -1.57578 |
| `explicit.stat_2974417149@T1` | -1.52716 |
| `explicit.stat_803737631@T1` | -1.52498 |
| `explicit.stat_2866361420@T2` | -1.50592 |
| `explicit.stat_2866361420@T1` | -1.49393 |
| `explicit.stat_2974417149@T2` | -1.49267 |
| `explicit.stat_1050105434@T2` | -1.48852 |
| `explicit.stat_803737631@T2` | -1.48708 |
| `explicit.stat_4080418644@T1` | -1.47281 |
| `explicit.stat_3489782002@T2` | -1.47004 |

### accessory.belt — n=41648, R²=-0.972

intercept: `6.5812`  ·  log_price: True  ·  ilvl: `-0.06241`  ·  n_mods: `-0.28538`  ·  n_top_tier: `0.64050`  ·  corrupted: `1.06771`  ·  n_sockets: `0.47998`

| stat_id | coef |
|---|---|
| `implicit.stat_731781020` | -1.13691 |
| `explicit.stat_3299347043@T1` | -1.01362 |
| `explicit.stat_2881298780@T1` | -0.95696 |
| `explicit.stat_1570770415@T2` | -0.90906 |
| `explicit.stat_51994685@T1` | -0.83787 |
| `explicit.stat_3299347043@T2` | -0.82656 |
| `explicit.stat_1570770415@T1` | -0.82353 |
| `explicit.stat_3372524247@T2` | -0.78832 |
| `explicit.stat_4220027924@T2` | -0.71371 |
| `explicit.stat_644456512@T1` | -0.69897 |
| `explicit.stat_4080418644@T2` | -0.67295 |
| `explicit.stat_915769802@T2` | -0.61500 |

### armour.chest — n=41264, R²=-1.2799

intercept: `4.1792`  ·  log_price: True  ·  ilvl: `-0.05041`  ·  n_mods: `-0.08202`  ·  n_top_tier: `0.40290`  ·  corrupted: `0.25150`  ·  n_sockets: `0.13771`  ·  quality: `0.05651`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.95690 |
| `explicit.stat_986397080@T2` | -0.84157 |
| `explicit.stat_3981240776@T1` | 0.81375 |
| `explicit.stat_2339757871@T2` | -0.80240 |
| `explicit.stat_986397080@T1` | -0.75454 |
| `explicit.stat_2339757871@T1` | -0.63851 |
| `explicit.stat_3484657501@T1` | -0.61003 |
| `explicit.stat_1692879867@T2` | -0.60737 |
| `explicit.stat_3372524247@T1` | 0.56692 |
| `explicit.stat_2451402625@T1` | -0.54065 |
| `explicit.stat_3484657501@T2` | -0.50358 |
| `explicit.stat_915769802@T2` | -0.50101 |

### armour.helmet — n=40134, R²=-1.1115

intercept: `3.7125`  ·  log_price: True  ·  ilvl: `-0.04623`  ·  n_mods: `-0.08348`  ·  n_top_tier: `0.48755`  ·  corrupted: `0.64608`  ·  n_sockets: `0.17005`  ·  quality: `0.05225`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.56368 |
| `crafted.stat_3917489142@T1` | -2.42085 |
| `explicit.stat_3917489142@T2` | -1.22238 |
| `explicit.stat_3917489142@T1` | -0.86592 |
| `explicit.stat_1999113824@T1` | -0.86227 |
| `explicit.stat_3321629045@T2` | -0.82056 |
| `explicit.stat_2923486259@T1` | 0.73450 |
| `explicit.stat_1263695895@T1` | -0.73132 |
| `explicit.stat_2162097452@T2` | -0.71575 |
| `explicit.stat_803737631@T1` | -0.68478 |
| `explicit.stat_803737631@T2` | -0.67916 |
| `explicit.stat_1999113824@T2` | -0.57485 |

### armour.boots — n=37304, R²=-1.4881

intercept: `4.2132`  ·  log_price: True  ·  ilvl: `-0.05138`  ·  n_mods: `-0.04970`  ·  n_top_tier: `0.55204`  ·  corrupted: `0.10377`  ·  n_sockets: `0.08857`  ·  quality: `0.05885`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.65325 |
| `crafted.stat_3917489142@T1` | 1.20826 |
| `explicit.stat_2339757871@T1` | -0.88058 |
| `explicit.stat_3299347043@T1` | -0.84121 |
| `explicit.stat_3917489142@T2` | -0.82969 |
| `explicit.stat_2923486259@T2` | -0.80013 |
| `explicit.stat_2923486259@T1` | 0.68908 |
| `explicit.stat_2160282525@T1` | -0.68699 |
| `explicit.stat_1999113824@T2` | -0.68622 |
| `explicit.stat_1062208444@T2` | -0.66422 |
| `explicit.stat_3484657501@T2` | -0.66179 |
| `explicit.stat_4052037485@T2` | -0.64729 |

### armour.gloves — n=36271, R²=-1.2924

intercept: `3.8434`  ·  log_price: True  ·  ilvl: `-0.04985`  ·  n_mods: `-0.05702`  ·  n_top_tier: `0.70618`  ·  corrupted: `-0.00798`  ·  n_sockets: `0.24423`  ·  quality: `0.04637`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.80956 |
| `explicit.stat_2923486259@T1` | -1.24174 |
| `explicit.stat_3484657501@T2` | -1.19113 |
| `explicit.stat_3484657501@T1` | -1.13626 |
| `explicit.stat_3321629045@T2` | -1.11436 |
| `explicit.stat_803737631@T2` | -1.07056 |
| `explicit.stat_3321629045@T1` | -0.89725 |
| `explicit.stat_124859000@T2` | -0.86392 |
| `explicit.stat_803737631@T1` | -0.85403 |
| `explicit.stat_4052037485@T2` | -0.84314 |
| `explicit.stat_4052037485@T1` | -0.83441 |
| `explicit.stat_3917489142@T2` | -0.82960 |

### weapon.wand — n=21875, R²=-1.9556

intercept: `3.7953`  ·  log_price: True  ·  ilvl: `-0.04728`  ·  n_mods: `-0.05292`  ·  n_top_tier: `0.45363`  ·  corrupted: `-0.00760`  ·  n_sockets: `0.06125`  ·  quality: `0.02422`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.99436 |
| `explicit.stat_1545858329@T1` | 2.68426 |
| `explicit.stat_124131830@T1` | 2.40509 |
| `explicit.stat_2254480358@T1` | 2.31162 |
| `explicit.stat_591105508@T1` | 1.94493 |
| `explicit.stat_4226189338@T1` | 1.83513 |
| `explicit.stat_736967255@T2` | 1.75693 |
| `crafted.stat_124131830` | 1.23863 |
| `explicit.stat_2254480358@T2` | 0.95017 |
| `explicit.stat_1600707273@T1` | 0.92710 |
| `explicit.stat_4226189338@T2` | 0.91303 |
| `explicit.stat_1263695895@T2` | -0.88053 |

### flask.charm — n=18073, R²=-0.624

intercept: `0.1102`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.06629`  ·  corrupted: `1.59657`  ·  quality: `0.00319`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.68143 |
| `explicit.stat_1056492907` | 2.66192 |
| `explicit.stat_3246948616` | 1.15800 |
| `explicit.stat_828533480@T2` | -1.06632 |
| `explicit.stat_1120862500@T2` | -1.06629 |
| `explicit.stat_1873752457@T2` | -1.06629 |
| `explicit.stat_3196823591@T2` | -1.06625 |
| `explicit.stat_2365392475@T2` | -1.06624 |
| `explicit.stat_2676834156@T2` | -1.06623 |
| `explicit.stat_388617051@T2` | -1.06570 |
| `explicit.stat_1873752457@T1` | -1.06539 |
| `explicit.stat_828533480@T1` | -1.06537 |

### weapon.bow — n=17438, R²=-1.8059

intercept: `3.9353`  ·  log_price: True  ·  ilvl: `-0.04634`  ·  n_mods: `-0.08530`  ·  n_top_tier: `0.64895`  ·  corrupted: `0.41775`  ·  n_sockets: `0.08045`  ·  quality: `0.03518`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.84151 |
| `crafted.stat_3035140377` | 1.37640 |
| `explicit.stat_3336890334@T1` | 1.36365 |
| `desecrated.stat_666077204@T1` | 1.00655 |
| `explicit.stat_1263695895@T1` | -0.95089 |
| `explicit.stat_709508406@T1` | 0.87388 |
| `explicit.stat_1263695895@T2` | -0.87298 |
| `explicit.stat_210067635@T2` | -0.75725 |
| `explicit.stat_3639275092@T1` | -0.74913 |
| `explicit.stat_1368271171@T2` | -0.72808 |
| `explicit.stat_3695891184@T2` | -0.72787 |
| `explicit.stat_669069897@T1` | -0.72227 |

### weapon.crossbow — n=16388, R²=-1.8521

intercept: `4.0026`  ·  log_price: True  ·  ilvl: `-0.04889`  ·  n_mods: `-0.05583`  ·  n_top_tier: `0.50233`  ·  corrupted: `0.04494`  ·  n_sockets: `0.07110`  ·  quality: `0.02932`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.66644 |
| `explicit.stat_1202301673@T1` | 1.50569 |
| `explicit.stat_2250681686@T2` | -1.33385 |
| `explicit.stat_1980802737` | 1.28551 |
| `explicit.stat_2250681686` | 0.96766 |
| `explicit.stat_709508406@T1` | 0.90113 |
| `crafted.stat_3035140377` | 0.74598 |
| `explicit.stat_1263695895@T2` | -0.69453 |
| `explicit.stat_1509134228@T1` | 0.66656 |
| `explicit.stat_1509134228@T2` | -0.65735 |
| `explicit.stat_3336890334@T2` | -0.63891 |
| `explicit.stat_3336890334@T1` | -0.61711 |

### weapon.warstaff — n=11179, R²=-0.3322

intercept: `-11.2137`  ·  log_price: True  ·  ilvl: `0.15013`  ·  n_mods: `-0.20853`  ·  n_top_tier: `0.30120`  ·  corrupted: `0.46743`  ·  n_sockets: `0.15208`  ·  quality: `0.05871`

| stat_id | coef |
|---|---|
| `desecrated.stat_3291658075@T1` | -1.46948 |
| `desecrated.stat_473429811@T1` | -1.46948 |
| `crafted.stat_210067635@T2` | 1.25193 |
| `explicit.stat_1037193709@T1` | 0.80630 |
| `explicit.stat_1509134228@T1` | 0.78809 |
| `desecrated.stat_9187492` | 0.75588 |
| `rune.stat_243313994` | 0.71823 |
| `explicit.stat_328541901@T1` | -0.67254 |
| `explicit.stat_518292764@T1` | 0.66541 |
| `explicit.stat_691932474@T2` | -0.60284 |
| `explicit.stat_1368271171@T1` | -0.59965 |
| `explicit.stat_748522257@T2` | 0.57678 |

### weapon.staff — n=10567, R²=-0.3776

intercept: `-15.6297`  ·  log_price: True  ·  ilvl: `0.20038`  ·  n_mods: `-0.07893`  ·  n_top_tier: `0.42536`  ·  corrupted: `0.81875`  ·  n_sockets: `0.18152`  ·  quality: `0.03539`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.09931 |
| `explicit.stat_591105508@T1` | 2.04164 |
| `explicit.stat_1545858329@T1` | 1.94019 |
| `explicit.stat_124131830@T1` | 1.37982 |
| `explicit.stat_293638271@T2` | -1.26022 |
| `explicit.stat_2254480358@T1` | 1.14577 |
| `explicit.stat_1600707273@T1` | 0.99593 |
| `explicit.stat_2254480358@T2` | 0.85025 |
| `explicit.stat_473429811@T2` | -0.72215 |
| `explicit.stat_3962278098@T2` | 0.60795 |
| `explicit.stat_591105508@T2` | 0.59589 |
| `explicit.stat_1600707273@T2` | 0.56443 |

### weapon.sceptre — n=10395, R²=-0.3414

intercept: `-21.2503`  ·  log_price: True  ·  ilvl: `0.27181`  ·  n_mods: `0.02300`  ·  n_top_tier: `0.19312`  ·  corrupted: `0.02471`  ·  n_sockets: `0.18378`  ·  quality: `0.02821`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.51401 |
| `explicit.stat_3057012405@T1` | 1.53994 |
| `explicit.stat_2162097452@T2` | 1.25809 |
| `explicit.stat_1798257884@T2` | 0.86550 |
| `explicit.stat_1263695895@T1` | -0.85718 |
| `explicit.stat_1263695895@T2` | -0.85185 |
| `explicit.stat_849987426@T1` | 0.77910 |
| `explicit.stat_1250712710@T2` | 0.74896 |
| `explicit.stat_101878827@T2` | 0.73359 |
| `explicit.stat_101878827@T1` | 0.71510 |
| `explicit.stat_2854751904@T2` | -0.62435 |
| `explicit.stat_3850614073@T1` | 0.51118 |

### weapon.spear — n=8365, R²=-0.3766

intercept: `-13.1821`  ·  log_price: True  ·  ilvl: `0.18178`  ·  n_mods: `-0.17988`  ·  n_top_tier: `0.76155`  ·  corrupted: `-0.08554`  ·  n_sockets: `0.20304`  ·  quality: `0.06871`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.38158 |
| `desecrated.stat_210067635@T1` | -1.31214 |
| `explicit.stat_1509134228@T1` | 1.30791 |
| `explicit.stat_1202301673@T1` | 1.23845 |
| `explicit.stat_9187492@T1` | 1.21764 |
| `explicit.stat_1940865751@T2` | -1.20986 |
| `explicit.stat_691932474@T1` | -1.16930 |
| `explicit.stat_9187492@T2` | -1.04540 |
| `explicit.stat_4080418644@T2` | -1.01047 |
| `explicit.stat_691932474@T2` | -0.99464 |
| `crafted.stat_3035140377` | 0.90927 |
| `explicit.stat_3336890334@T2` | -0.87612 |

### armour.focus — n=6833, R²=-0.3357

intercept: `-15.0380`  ·  log_price: True  ·  ilvl: `0.19257`  ·  n_mods: `-0.17193`  ·  n_top_tier: `0.85339`  ·  corrupted: `0.09485`  ·  n_sockets: `0.30349`  ·  quality: `0.05152`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.56589 |
| `explicit.stat_4220027924@T1` | -1.31092 |
| `crafted.stat_2974417149@T1` | 1.29897 |
| `explicit.stat_4220027924@T2` | -1.23546 |
| `explicit.stat_2231156303@T2` | -1.14775 |
| `explicit.stat_2231156303@T1` | -1.07545 |
| `explicit.stat_274716455@T2` | -1.04975 |
| `explicit.stat_2339757871@T2` | -1.00464 |
| `explicit.stat_2974417149@T1` | -0.98364 |
| `explicit.stat_4015621042@T1` | -0.87631 |
| `explicit.stat_1050105434@T2` | -0.85050 |
| `explicit.stat_737908626@T2` | -0.83404 |

### armour.quiver — n=6405, R²=-0.2967

intercept: `-16.2989`  ·  log_price: True  ·  ilvl: `0.20033`  ·  n_mods: `-0.10587`  ·  n_top_tier: `0.82926`  ·  corrupted: `0.73058`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.16526 |
| `explicit.stat_2463230181@T1` | 2.28456 |
| `explicit.stat_681332047@T2` | -1.41569 |
| `explicit.stat_1573130764@T1` | -1.28805 |
| `explicit.stat_1573130764@T2` | -1.13762 |
| `explicit.stat_2463230181@T2` | 1.02593 |
| `explicit.stat_803737631@T2` | -0.96375 |
| `explicit.stat_803737631@T1` | -0.92125 |
| `explicit.stat_681332047@T1` | -0.91786 |
| `explicit.stat_2321178454@T2` | -0.84717 |
| `explicit.stat_4067062424@T1` | -0.82448 |
| `explicit.stat_2194114101@T2` | -0.78762 |

### armour.shield — n=5518, R²=-0.4209

intercept: `-14.1669`  ·  log_price: True  ·  ilvl: `0.18679`  ·  n_mods: `-0.07868`  ·  n_top_tier: `0.65578`  ·  corrupted: `-0.35191`  ·  n_sockets: `0.45048`  ·  quality: `0.06535`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.51969 |
| `explicit.stat_3321629045@T2` | -1.16356 |
| `explicit.stat_3484657501@T1` | -1.09951 |
| `explicit.stat_3855016469@T1` | -1.08228 |
| `explicit.stat_2901986750@T1` | -1.06299 |
| `explicit.stat_2339757871@T2` | -1.02804 |
| `explicit.stat_4095671657@T1` | -1.01711 |
| `explicit.stat_1011760251@T1` | -0.98754 |
| `explicit.stat_4095671657@T2` | -0.98694 |
| `explicit.stat_3033371881@T2` | -0.97888 |
| `explicit.stat_328541901@T1` | -0.95295 |
| `explicit.stat_3484657501@T2` | -0.94887 |

### weapon.twomace — n=5070, R²=-0.4451

intercept: `-10.2615`  ·  log_price: True  ·  ilvl: `0.14127`  ·  n_mods: `-0.22899`  ·  n_top_tier: `0.46460`  ·  corrupted: `0.35044`  ·  n_sockets: `0.16743`  ·  quality: `0.05949`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.18058 |
| `desecrated.stat_1509134228@T1` | 1.99493 |
| `explicit.stat_1037193709@T1` | -1.67098 |
| `explicit.stat_1263695895@T2` | -1.34557 |
| `explicit.stat_3336890334@T1` | -1.27248 |
| `explicit.stat_9187492@T1` | -1.01655 |
| `explicit.stat_691932474@T1` | -0.95133 |
| `explicit.stat_387439868@T2` | -0.85649 |
| `explicit.stat_3695891184@T1` | -0.72454 |
| `explicit.stat_1263695895@T1` | -0.66765 |
| `explicit.stat_821021828@T2` | -0.64731 |
| `explicit.stat_387439868@T1` | -0.64595 |

## Coverage (listings per base)

- … **Sapphire** — 32989 listings (32934 priced) [0.3–3985176410.3 ex]
- … **Emerald** — 32129 listings (32088 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 24634 listings (24604 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11906 listings (11888 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10651 listings (10628 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10319 listings (10295 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 10195 listings (10184 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 9634 listings (9612 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9537 listings (9515 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 9131 listings (9118 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7920 listings (7905 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7628 listings (7619 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7509 listings (7500 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 7034 listings (7013 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6608 listings (6601 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 6512 listings (6484 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 6511 listings (6492 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6510 listings (6496 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6475 listings (6468 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6398 listings (6369 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6283 listings (6273 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 6256 listings (6248 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5931 listings (5928 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5867 listings (5853 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5755 listings (5745 priced) [0.3–398912568423.8 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-15T19:32:55+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **521522** (520396 priced in exalted)
- Distinct bases: 983 · distinct mods: 3124 · mod rows: 2474090
- Sold signals: **26047** sold · 292030 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-15T19:22:44+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.20** (median |log error| 3.1862)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×56.23 · ±30% 5% · n=75161
- Premium segment (60ex+): skill **+0.12** · typical error ×226.49 · ±30% 0% · n=50224

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 10442 | ×52.85 | 22% | +0.06 | +0.09 |
| jewel | 9726 | ×9.63 | 5% | +0.03 | +0.07 |
| accessory.amulet | 9595 | ×50.75 | 19% | +0.03 | +0.03 |
| accessory.belt | 7344 | ×15.58 | 4% | +0.02 | +0.03 |
| armour.chest | 7125 | ×23.00 | 7% | +0.10 | +0.12 |
| armour.helmet | 7022 | ×20.83 | 5% | +0.05 | +0.07 |
| armour.boots | 6459 | ×36.15 | 11% | +0.11 | +0.12 |
| armour.gloves | 6367 | ×26.42 | 6% | +0.13 | +0.15 |
| other | 5770 | ×3.61 | 41% | +0.09 | +0.15 |
| weapon.wand | 3982 | ×33.58 | 18% | +0.07 | +0.09 |
| weapon.bow | 3211 | ×27.82 | 17% | +0.11 | +0.13 |
| weapon.crossbow | 3026 | ×23.65 | 19% | +0.09 | +0.12 |
| weapon.warstaff | 1817 | ×32.17 | 15% | +0.12 | +0.10 |
| weapon.staff | 1707 | ×57.00 | 12% | +0.09 | +0.10 |
| weapon.sceptre | 1697 | ×38.97 | 6% | +0.15 | +0.14 |
| weapon.spear | 1400 | ×58.41 | 15% | +0.09 | +0.09 |
| armour.focus | 1178 | ×40.23 | 7% | +0.14 | +0.16 |
| armour.quiver | 1098 | ×29.08 | 9% | +0.10 | +0.13 |
| armour.shield | 926 | ×17.71 | 14% | +0.03 | +0.04 |
| flask.charm | 919 | ×30.00 | 35% | +0.03 | +0.06 |
| weapon.twomace | 830 | ×17.93 | 13% | +0.06 | +0.06 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=52737, R²=-0.8989

intercept: `-1.6992`  ·  log_price: True  ·  ilvl: `0.02721`  ·  n_mods: `0.60772`  ·  n_top_tier: `-0.15157`  ·  corrupted: `0.24504`  ·  quality: `0.23205`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.05874 |
| `explicit.stat_2301718443@T1` | 2.56528 |
| `explicit.stat_627767961@T1` | -2.33568 |
| `explicit.stat_3485067555@T1` | 2.02990 |
| `explicit.stat_1805182458@T1` | -2.01075 |
| `explicit.stat_3780644166@T1` | -1.87526 |
| `explicit.stat_239367161@T1` | -1.82374 |
| `explicit.stat_1062710370@T1` | -1.74266 |
| `explicit.stat_924253255@T1` | -1.43659 |
| `explicit.stat_2523933828@T1` | -1.40067 |
| `explicit.stat_3166958180@T1` | -1.39799 |
| `explicit.stat_3119612865@T1` | -1.38550 |

### other — n=50260, R²=-0.6177

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.36265`  ·  corrupted: `0.33128`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.57537 |
| `explicit.stat_2974417149@T1` | 0.46492 |
| `explicit.stat_2482852589@T1` | -0.31198 |
| `explicit.stat_789117908@T1` | -0.28544 |
| `explicit.stat_3299347043@T1` | -0.27099 |
| `implicit.stat_3879011313` | 0.23104 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23026 |
| `explicit.stat_3141070085@T1` | -0.22740 |
| `explicit.stat_2106365538@T1` | -0.21127 |
| `explicit.stat_2968503605@T1` | 0.20484 |
| `explicit.stat_2891184298@T1` | 0.19570 |

### accessory.ring — n=47795, R²=-1.9876

intercept: `3.4632`  ·  log_price: True  ·  ilvl: `-0.04284`  ·  n_mods: `0.00163`  ·  n_top_tier: `0.93399`  ·  corrupted: `0.02955`  ·  n_sockets: `1.56785`  ·  quality: `0.07314`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -0.96508 |
| `explicit.stat_3325883026@T1` | -0.96227 |
| `explicit.stat_1368271171@T2` | -0.96109 |
| `explicit.stat_803737631@T1` | -0.96051 |
| `explicit.stat_1573130764@T1` | -0.96010 |
| `explicit.stat_2144192055@T1` | -0.95637 |
| `explicit.stat_3291658075@T1` | -0.95514 |
| `explicit.stat_3291658075@T2` | -0.95202 |
| `explicit.stat_4220027924@T2` | -0.95177 |
| `explicit.stat_3325883026@T2` | -0.95147 |
| `explicit.stat_1368271171@T1` | -0.94932 |
| `explicit.stat_1050105434@T2` | -0.94766 |

### accessory.amulet — n=44037, R²=-2.1407

intercept: `3.8635`  ·  log_price: True  ·  ilvl: `-0.04732`  ·  n_mods: `-0.02376`  ·  n_top_tier: `0.93147`  ·  corrupted: `0.02811`  ·  n_sockets: `-0.11953`  ·  quality: `0.00018`

| stat_id | coef |
|---|---|
| `explicit.stat_803737631@T1` | -1.01616 |
| `explicit.stat_472520716@T2` | -1.01595 |
| `explicit.stat_472520716@T1` | -1.00723 |
| `explicit.stat_2901986750@T1` | -0.99602 |
| `explicit.stat_1050105434@T2` | -0.98532 |
| `explicit.stat_803737631@T2` | -0.97883 |
| `explicit.stat_2974417149@T2` | -0.97290 |
| `explicit.stat_3917489142@T2` | -0.97043 |
| `explicit.stat_2974417149@T1` | -0.96921 |
| `explicit.stat_2866361420@T2` | -0.96898 |
| `explicit.stat_3917489142@T1` | -0.96223 |
| `explicit.stat_2866361420@T1` | -0.96069 |

### accessory.belt — n=33763, R²=-0.6165

intercept: `6.3870`  ·  log_price: True  ·  ilvl: `-0.05340`  ·  n_mods: `-0.40345`  ·  n_top_tier: `1.10732`  ·  corrupted: `0.85977`  ·  n_sockets: `-0.81096`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.77779 |
| `explicit.stat_3299347043@T1` | -1.69074 |
| `explicit.stat_2881298780@T1` | -1.61806 |
| `explicit.stat_644456512@T1` | -1.42506 |
| `explicit.stat_3299347043@T2` | -1.41381 |
| `explicit.stat_809229260@T2` | -1.31790 |
| `explicit.stat_51994685@T1` | -1.29917 |
| `explicit.stat_1389754388@T2` | -1.27781 |
| `explicit.stat_4080418644@T2` | -1.25122 |
| `explicit.stat_3325883026@T1` | -1.24657 |
| `explicit.stat_2923486259@T1` | -1.23134 |
| `explicit.stat_809229260@T1` | -1.22656 |

### armour.chest — n=33419, R²=-1.076

intercept: `4.2992`  ·  log_price: True  ·  ilvl: `-0.04982`  ·  n_mods: `-0.11099`  ·  n_top_tier: `0.55966`  ·  corrupted: `0.22376`  ·  n_sockets: `0.13610`  ·  quality: `0.03885`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.04663 |
| `explicit.stat_3484657501@T1` | -0.93612 |
| `explicit.stat_4080418644@T1` | -0.91582 |
| `explicit.stat_986397080@T2` | -0.79262 |
| `explicit.stat_1999113824@T1` | -0.72115 |
| `explicit.stat_4080418644@T2` | -0.70452 |
| `explicit.stat_1692879867@T2` | -0.69614 |
| `explicit.stat_1692879867@T1` | -0.69591 |
| `explicit.stat_2451402625@T1` | -0.68816 |
| `explicit.stat_2451402625@T2` | -0.68664 |
| `explicit.stat_3301100256@T2` | -0.68538 |
| `explicit.stat_3372524247@T2` | -0.67681 |

### armour.helmet — n=32552, R²=-0.9214

intercept: `4.0735`  ·  log_price: True  ·  ilvl: `-0.05024`  ·  n_mods: `-0.12123`  ·  n_top_tier: `0.43082`  ·  corrupted: `0.71055`  ·  n_sockets: `0.18314`  ·  quality: `0.04226`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.31723 |
| `explicit.stat_3917489142@T2` | -1.10135 |
| `explicit.stat_1999113824@T1` | -0.82425 |
| `explicit.stat_53045048@T2` | -0.80306 |
| `explicit.stat_3261801346@T1` | -0.77766 |
| `crafted.stat_3917489142@T1` | -0.74884 |
| `explicit.stat_3321629045@T2` | -0.68067 |
| `explicit.stat_3917489142@T1` | -0.65593 |
| `explicit.stat_1263695895@T1` | -0.65014 |
| `explicit.stat_1050105434@T2` | -0.60510 |
| `explicit.stat_803737631@T2` | -0.55220 |
| `explicit.stat_1999113824@T2` | -0.53989 |

### armour.boots — n=30441, R²=-1.2784

intercept: `4.3528`  ·  log_price: True  ·  ilvl: `-0.05205`  ·  n_mods: `-0.07270`  ·  n_top_tier: `0.63701`  ·  corrupted: `0.21683`  ·  n_sockets: `0.15063`  ·  quality: `0.03043`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.30238 |
| `explicit.stat_2339757871@T1` | -1.54882 |
| `explicit.stat_2250533757@T1` | 1.41501 |
| `explicit.stat_3299347043@T1` | -1.07697 |
| `explicit.stat_2923486259@T2` | -0.93386 |
| `explicit.stat_3917489142@T2` | -0.85998 |
| `explicit.stat_1062208444@T2` | -0.80055 |
| `explicit.stat_1999113824@T2` | -0.79905 |
| `explicit.stat_2160282525@T1` | -0.79527 |
| `explicit.stat_53045048@T1` | -0.75192 |
| `explicit.stat_1671376347@T2` | -0.74675 |
| `explicit.stat_1874553720@T1` | -0.73111 |

### armour.gloves — n=29683, R²=-1.1281

intercept: `3.9390`  ·  log_price: True  ·  ilvl: `-0.05066`  ·  n_mods: `-0.06285`  ·  n_top_tier: `0.51869`  ·  corrupted: `0.15675`  ·  n_sockets: `0.21408`  ·  quality: `0.03968`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 3.59104 |
| `rune.stat_201332984` | -2.79236 |
| `explicit.stat_3484657501@T2` | -1.16236 |
| `explicit.stat_3484657501@T1` | -1.02929 |
| `explicit.stat_2923486259@T1` | -0.93485 |
| `explicit.stat_803737631@T2` | -0.87899 |
| `explicit.stat_3321629045@T2` | -0.84792 |
| `explicit.stat_9187492@T1` | 0.84718 |
| `explicit.stat_803737631@T1` | -0.77072 |
| `explicit.stat_1999113824@T2` | -0.72135 |
| `explicit.stat_2451402625@T2` | -0.67826 |
| `explicit.stat_2451402625@T1` | -0.66487 |

### weapon.wand — n=18919, R²=-2.1996

intercept: `3.5836`  ·  log_price: True  ·  ilvl: `-0.04424`  ·  n_mods: `-0.01886`  ·  n_top_tier: `0.68916`  ·  corrupted: `0.04664`  ·  n_sockets: `0.03743`  ·  quality: `0.00336`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.75528 |
| `explicit.stat_1545858329@T1` | 2.44639 |
| `explicit.stat_2254480358@T1` | 2.18498 |
| `explicit.stat_4226189338@T1` | 1.78571 |
| `explicit.stat_591105508@T1` | 1.68014 |
| `explicit.stat_124131830@T1` | 1.58144 |
| `explicit.stat_736967255@T2` | 1.52249 |
| `crafted.stat_124131830` | 1.10649 |
| `explicit.stat_2254480358@T2` | 0.82379 |
| `explicit.stat_1263695895@T2` | -0.80447 |
| `explicit.stat_737908626@T1` | -0.79024 |
| `explicit.stat_3962278098@T2` | -0.75896 |

### weapon.bow — n=15216, R²=-1.9631

intercept: `3.5715`  ·  log_price: True  ·  ilvl: `-0.04300`  ·  n_mods: `-0.03865`  ·  n_top_tier: `0.58035`  ·  corrupted: `-0.07924`  ·  n_sockets: `0.01296`  ·  quality: `0.03472`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.81496 |
| `explicit.stat_1202301673@T1` | 1.61743 |
| `crafted.stat_3035140377` | 1.42234 |
| `desecrated.stat_666077204@T1` | 1.34295 |
| `explicit.stat_2463230181@T2` | -0.91311 |
| `explicit.stat_1263695895@T1` | -0.79045 |
| `explicit.stat_1263695895@T2` | -0.76680 |
| `explicit.stat_518292764@T2` | -0.67564 |
| `explicit.stat_3695891184@T2` | -0.66944 |
| `explicit.stat_1037193709@T1` | -0.65238 |
| `explicit.stat_1509134228@T1` | -0.64507 |
| `explicit.stat_3695891184@T1` | -0.63836 |

### weapon.crossbow — n=14327, R²=-1.9605

intercept: `3.6102`  ·  log_price: True  ·  ilvl: `-0.04410`  ·  n_mods: `-0.02242`  ·  n_top_tier: `0.69015`  ·  corrupted: `0.03193`  ·  n_sockets: `0.02344`  ·  quality: `0.01008`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.93989 |
| `explicit.stat_709508406@T1` | 1.51153 |
| `explicit.stat_2250681686@T2` | -1.41829 |
| `explicit.stat_1202301673@T1` | 1.37711 |
| `explicit.stat_1980802737` | 1.20576 |
| `crafted.stat_3035140377` | 0.91586 |
| `explicit.stat_1263695895@T2` | -0.85085 |
| `explicit.stat_2250681686` | 0.82981 |
| `explicit.stat_1263695895@T1` | -0.78555 |
| `explicit.stat_2694482655@T1` | -0.77985 |
| `explicit.stat_1509134228@T2` | -0.77605 |
| `explicit.stat_1544773869@T2` | -0.74913 |

### flask.charm — n=13529, R²=-0.5448

intercept: `0.0190`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.83262`  ·  corrupted: `2.02760`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.43518 |
| `explicit.stat_1056492907` | 3.21264 |
| `explicit.stat_828533480@T2` | -2.83264 |
| `explicit.stat_828533480@T1` | -2.83262 |
| `explicit.stat_2676834156@T2` | -2.83262 |
| `explicit.stat_2541588185@T2` | -2.83262 |
| `explicit.stat_1120862500@T2` | -2.83261 |
| `explicit.stat_3196823591@T2` | -2.83261 |
| `explicit.stat_1873752457@T2` | -2.83260 |
| `explicit.stat_388617051@T2` | -2.83260 |
| `explicit.stat_2365392475@T2` | -2.83259 |
| `explicit.stat_1366840608@T2` | -2.83258 |

### weapon.warstaff — n=8914, R²=-0.4388

intercept: `-7.8463`  ·  log_price: True  ·  ilvl: `0.10672`  ·  n_mods: `-0.17512`  ·  n_top_tier: `0.52620`  ·  corrupted: `0.20994`  ·  n_sockets: `0.16158`  ·  quality: `0.05932`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.19447 |
| `explicit.stat_328541901@T1` | -1.10089 |
| `explicit.stat_328541901@T2` | -1.01517 |
| `explicit.stat_1037193709@T1` | 0.96927 |
| `desecrated.stat_2527686725@T1` | 0.82179 |
| `desecrated.stat_2231156303@T1` | 0.82179 |
| `explicit.stat_1037193709@T2` | -0.70928 |
| `crafted.stat_210067635@T2` | 0.70109 |
| `desecrated.stat_9187492` | 0.67736 |
| `explicit.stat_55876295@T2` | -0.64763 |
| `explicit.stat_1940865751@T1` | -0.58220 |
| `explicit.stat_3695891184@T2` | -0.52672 |

### weapon.staff — n=8316, R²=-0.4382

intercept: `-11.3164`  ·  log_price: True  ·  ilvl: `0.14668`  ·  n_mods: `-0.11812`  ·  n_top_tier: `0.59593`  ·  corrupted: `0.24698`  ·  n_sockets: `0.21584`  ·  quality: `0.04325`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.55630 |
| `explicit.stat_3962278098@T2` | 1.16774 |
| `explicit.stat_4226189338@T2` | 1.14860 |
| `explicit.stat_124131830@T2` | 1.13354 |
| `explicit.stat_293638271@T2` | -1.06103 |
| `explicit.stat_4226189338@T1` | 1.05960 |
| `explicit.stat_591105508@T1` | 0.98390 |
| `explicit.stat_124131830@T1` | 0.89430 |
| `explicit.stat_2768835289@T2` | 0.81019 |
| `explicit.stat_1263695895@T2` | -0.80319 |
| `explicit.stat_2505884597@T2` | -0.75075 |
| `explicit.stat_2974417149@T1` | -0.69109 |

### weapon.sceptre — n=8233, R²=-0.3824

intercept: `-17.3681`  ·  log_price: True  ·  ilvl: `0.22075`  ·  n_mods: `-0.02591`  ·  n_top_tier: `0.30495`  ·  corrupted: `0.52366`  ·  n_sockets: `0.18665`  ·  quality: `0.04982`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.73880 |
| `explicit.stat_2162097452@T2` | 1.62927 |
| `explicit.stat_3057012405@T1` | 1.14382 |
| `explicit.stat_1250712710@T2` | 1.07148 |
| `explicit.stat_1263695895@T1` | -0.84410 |
| `explicit.stat_101878827@T1` | 0.77840 |
| `explicit.stat_2347036682@T1` | 0.71911 |
| `explicit.stat_1263695895@T2` | -0.68882 |
| `explicit.stat_2347036682@T2` | -0.66199 |
| `explicit.stat_289128254@T2` | -0.56923 |
| `explicit.stat_2854751904@T2` | -0.53522 |
| `explicit.stat_1574590649@T2` | -0.51145 |

### weapon.spear — n=6794, R²=-0.5081

intercept: `-8.5599`  ·  log_price: True  ·  ilvl: `0.11639`  ·  n_mods: `-0.06159`  ·  n_top_tier: `0.73123`  ·  corrupted: `-0.08232`  ·  n_sockets: `0.21291`  ·  quality: `0.09277`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.28174 |
| `explicit.stat_1202301673@T1` | 2.07826 |
| `explicit.stat_9187492@T1` | 1.44052 |
| `explicit.stat_1509134228@T1` | 1.20589 |
| `explicit.stat_210067635@T1` | 1.09616 |
| `explicit.stat_1263695895@T2` | -1.08929 |
| `explicit.stat_1037193709@T1` | -1.06372 |
| `crafted.stat_3035140377` | 1.03843 |
| `explicit.stat_55876295@T1` | -0.97522 |
| `desecrated.stat_210067635@T1` | -0.84805 |
| `explicit.stat_691932474@T1` | -0.84517 |
| `explicit.stat_1940865751@T2` | -0.77236 |

### armour.focus — n=5571, R²=-0.4083

intercept: `-12.6504`  ·  log_price: True  ·  ilvl: `0.16274`  ·  n_mods: `-0.15612`  ·  n_top_tier: `0.77788`  ·  corrupted: `0.95907`  ·  n_sockets: `0.45623`  ·  quality: `0.07020`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 3.74695 |
| `crafted.stat_737908626@T2` | 3.16358 |
| `explicit.stat_4220027924@T2` | -1.33921 |
| `explicit.stat_3962278098@T1` | -1.25165 |
| `explicit.stat_736967255@T2` | -1.09750 |
| `explicit.stat_2923486259@T1` | -0.99325 |
| `explicit.stat_2231156303@T1` | -0.97561 |
| `explicit.stat_2974417149@T2` | -0.95370 |
| `explicit.stat_2339757871@T2` | -0.91190 |
| `explicit.stat_2231156303@T2` | -0.88312 |
| `explicit.stat_3962278098@T2` | -0.88017 |
| `explicit.stat_737908626@T2` | -0.85447 |

### armour.quiver — n=5184, R²=-0.3713

intercept: `-13.1852`  ·  log_price: True  ·  ilvl: `0.15970`  ·  n_mods: `-0.07801`  ·  n_top_tier: `0.91046`  ·  corrupted: `0.45284`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 2.48331 |
| `explicit.stat_2463230181@T1` | 2.02062 |
| `explicit.stat_681332047@T2` | -1.41467 |
| `explicit.stat_4067062424@T1` | -1.23127 |
| `explicit.stat_2321178454@T2` | -1.21252 |
| `explicit.stat_803737631@T2` | -1.17054 |
| `explicit.stat_1573130764@T1` | -1.13630 |
| `explicit.stat_1573130764@T2` | -1.06772 |
| `explicit.stat_2194114101@T2` | -1.03347 |
| `explicit.stat_4067062424@T2` | -1.00551 |
| `explicit.stat_681332047@T1` | -0.95100 |
| `explicit.stat_2321178454@T1` | -0.94811 |

### armour.shield — n=4528, R²=-0.536

intercept: `-9.8179`  ·  log_price: True  ·  ilvl: `0.12751`  ·  n_mods: `-0.06200`  ·  n_top_tier: `0.49351`  ·  corrupted: `-0.26624`  ·  n_sockets: `0.12769`  ·  quality: `0.07027`

| stat_id | coef |
|---|---|
| `explicit.stat_1011760251@T1` | -1.31763 |
| `explicit.stat_1301765461@T1` | 1.19154 |
| `explicit.stat_1011760251@T2` | -1.07902 |
| `explicit.stat_3676141501@T1` | 0.96170 |
| `explicit.stat_4095671657@T1` | -0.95583 |
| `explicit.stat_3033371881@T2` | -0.91802 |
| `explicit.stat_3484657501@T1` | -0.86920 |
| `explicit.stat_3855016469@T1` | -0.85780 |
| `explicit.stat_3484657501@T2` | -0.84963 |
| `explicit.stat_2481353198@T2` | -0.77120 |
| `explicit.stat_3321629045@T2` | -0.74720 |
| `explicit.stat_2923486259@T2` | -0.73387 |

### weapon.twomace — n=4158, R²=-0.5259

intercept: `-9.6965`  ·  log_price: True  ·  ilvl: `0.12825`  ·  n_mods: `-0.15936`  ·  n_top_tier: `0.41447`  ·  corrupted: `0.35326`  ·  n_sockets: `0.13486`  ·  quality: `0.05265`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.14527 |
| `desecrated.stat_1509134228@T1` | 3.11669 |
| `explicit.stat_1037193709@T1` | -1.81000 |
| `explicit.stat_3336890334@T1` | -0.98388 |
| `crafted.stat_3035140377` | 0.96194 |
| `explicit.stat_387439868@T2` | -0.86116 |
| `explicit.stat_1037193709@T2` | -0.80571 |
| `explicit.stat_3639275092@T1` | -0.74390 |
| `explicit.stat_518292764@T2` | -0.74183 |
| `explicit.stat_2694482655@T1` | -0.65225 |
| `explicit.stat_9187492@T1` | -0.59400 |
| `explicit.stat_3639275092@T2` | -0.54893 |

## Coverage (listings per base)

- … **Sapphire** — 24572 listings (24535 priced) [0.3–7553463.8 ex]
- … **Emerald** — 24115 listings (24085 priced) [0.3–7553463.8 ex]
- … **Ruby** — 18489 listings (18473 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 9817 listings (9808 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8177 listings (8166 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 7928 listings (7911 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 7821 listings (7814 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 7454 listings (7443 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 7335 listings (7331 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 7310 listings (7296 priced) [0.2–91750808.2 ex]
- … **Sapphire Ring** — 6115 listings (6109 priced) [0.2–307202867.9 ex]
- … **Dueling Wand** — 6032 listings (6015 priced) [0.3–4297682211.9 ex]
- … **Topaz Ring** — 5849 listings (5844 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5804 listings (5801 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5226 listings (5209 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5197 listings (5192 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 5080 listings (5066 priced) [0.6–398912568423.8 ex]
- … **Amber Amulet** — 5047 listings (5043 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 5047 listings (5040 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 5008 listings (5001 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4884 listings (4878 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 4717 listings (4711 priced) [0.2–275252424.7 ex]
- … **Heavy Belt** — 4688 listings (4684 priced) [0.3–398912568423.8 ex]
- … **Azure Amulet** — 4623 listings (4623 priced) [0.3–123132003.2 ex]
- … **Obliterator Bow** — 4574 listings (4558 priced) [0.3–42622633798.0 ex]

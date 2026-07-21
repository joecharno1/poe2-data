# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-21T05:33:42+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **702351** (700118 priced in exalted)
- Distinct bases: 1000 · distinct mods: 3316 · mod rows: 3323169
- Sold signals: **24253** sold · 400076 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-21T05:20:40+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×23.94** (median |log error| 3.1756)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×75.88 · ±30% 4% · n=101907
- Premium segment (60ex+): skill **+0.12** · typical error ×380.12 · ±30% 0% · n=67773

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 14954 | ×47.27 | 21% | +0.04 | +0.06 |
| jewel | 14350 | ×56.98 | 22% | +0.02 | +0.03 |
| accessory.amulet | 13449 | ×31.35 | 17% | +0.04 | +0.04 |
| accessory.belt | 9582 | ×20.45 | 23% | +0.02 | +0.05 |
| armour.chest | 9334 | ×16.13 | 23% | +0.08 | +0.10 |
| armour.helmet | 9125 | ×28.55 | 20% | +0.07 | +0.10 |
| armour.boots | 8377 | ×23.43 | 21% | +0.09 | +0.12 |
| armour.gloves | 8267 | ×35.21 | 16% | +0.07 | +0.09 |
| other | 8183 | ×2.00 | 41% | +0.12 | +0.18 |
| weapon.wand | 4896 | ×39.85 | 16% | +0.10 | +0.11 |
| weapon.bow | 3846 | ×29.33 | 13% | +0.14 | +0.16 |
| weapon.crossbow | 3624 | ×24.34 | 17% | +0.10 | +0.14 |
| weapon.warstaff | 2492 | ×13.91 | 7% | +0.21 | +0.22 |
| weapon.staff | 2418 | ×15.71 | 6% | +0.14 | +0.13 |
| weapon.sceptre | 2361 | ×19.20 | 4% | +0.08 | +0.09 |
| weapon.spear | 1887 | ×13.02 | 7% | +0.15 | +0.15 |
| armour.focus | 1570 | ×13.01 | 7% | +0.12 | +0.13 |
| armour.quiver | 1461 | ×17.55 | 6% | +0.12 | +0.14 |
| armour.shield | 1201 | ×9.37 | 8% | +0.10 | +0.12 |
| flask.charm | 1194 | ×10.01 | 28% | -0.01 | +0.01 |
| weapon.twomace | 1112 | ×9.24 | 8% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=78689, R²=-1.9038

intercept: `-0.0531`  ·  log_price: True  ·  ilvl: `0.00066`  ·  n_mods: `1.02339`  ·  n_top_tier: `-0.91450`  ·  corrupted: `1.25307`  ·  quality: `0.30147`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 3.52898 |
| `explicit.stat_1604736568@T1` | -2.40392 |
| `explicit.stat_1604736568` | 2.29805 |
| `explicit.stat_3556824919@T1` | 1.03471 |
| `explicit.stat_3174700878@T1` | 0.94850 |
| `explicit.stat_3473929743@T1` | -0.90238 |
| `explicit.stat_587431675@T1` | -0.86196 |
| `explicit.stat_274716455@T1` | -0.78512 |
| `explicit.stat_2194114101@T1` | -0.76971 |
| `explicit.stat_681332047@T1` | -0.72086 |
| `explicit.stat_2456523742@T1` | 0.63655 |
| `explicit.stat_2482852589@T1` | -0.56660 |

### accessory.ring — n=68394, R²=-2.0196

intercept: `3.3815`  ·  log_price: True  ·  ilvl: `-0.04222`  ·  n_mods: `0.00081`  ·  n_top_tier: `0.97570`  ·  corrupted: `0.01042`  ·  n_sockets: `2.04107`  ·  quality: `0.02098`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.01427 |
| `explicit.stat_4080418644@T1` | -1.00051 |
| `explicit.stat_803737631@T1` | -0.99936 |
| `explicit.stat_2231156303@T1` | -0.99762 |
| `explicit.stat_3325883026@T1` | -0.99629 |
| `explicit.stat_2891184298@T2` | -0.99406 |
| `explicit.stat_4220027924@T2` | -0.99048 |
| `explicit.stat_736967255@T2` | -0.98910 |
| `explicit.stat_2923486259@T2` | -0.98796 |
| `explicit.stat_3291658075@T2` | -0.98793 |
| `explicit.stat_2891184298@T1` | -0.98590 |
| `explicit.stat_1573130764@T2` | -0.98360 |

### other — n=66843, R²=-0.6508

intercept: `1.6093`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.11015`  ·  n_top_tier: `0.23642`  ·  corrupted: `0.02275`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_718638445` | 0.33049 |
| `implicit.stat_3182714256` | 0.33048 |
| `explicit.stat_1050105434@T1` | -0.32060 |
| `implicit.stat_2219129443` | 0.21923 |
| `explicit.stat_3299347043@T1` | -0.20174 |
| `explicit.stat_2974417149@T1` | 0.15852 |
| `explicit.stat_3917489142@T1` | -0.12498 |
| `implicit.stat_958696139` | -0.11014 |
| `implicit.stat_1416292992` | -0.07344 |
| `explicit.stat_789117908@T1` | -0.06351 |
| `implicit.stat_3879011313` | 0.05832 |
| `implicit.stat_3032590688` | -0.04405 |

### accessory.amulet — n=61448, R²=-2.1366

intercept: `3.3934`  ·  log_price: True  ·  ilvl: `-0.04294`  ·  n_mods: `-0.02014`  ·  n_top_tier: `1.22305`  ·  corrupted: `0.11873`  ·  n_sockets: `-0.07539`  ·  quality: `0.05393`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.81956 |
| `explicit.stat_3299347043@T2` | -1.72856 |
| `explicit.stat_587431675@T2` | -1.41552 |
| `explicit.stat_2866361420@T2` | -1.32579 |
| `explicit.stat_2866361420@T1` | -1.32346 |
| `explicit.stat_2974417149@T1` | -1.32031 |
| `explicit.stat_803737631@T1` | -1.31416 |
| `explicit.stat_2974417149@T2` | -1.30049 |
| `explicit.stat_1050105434@T2` | -1.27299 |
| `explicit.stat_803737631@T2` | -1.26935 |
| `explicit.stat_4080418644@T1` | -1.26865 |
| `explicit.stat_1050105434@T1` | -1.25975 |

### accessory.belt — n=44137, R²=-2.0155

intercept: `1.0985`  ·  log_price: True  ·  ilvl: `-0.01324`  ·  n_mods: `-0.00546`  ·  n_top_tier: `0.41024`  ·  corrupted: `1.11423`  ·  n_sockets: `1.40207`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 0.69445 |
| `explicit.stat_3299347043@T1` | -0.41869 |
| `explicit.stat_51994685@T1` | -0.41802 |
| `explicit.stat_3299347043@T2` | -0.41735 |
| `explicit.stat_809229260@T2` | -0.41570 |
| `explicit.stat_2881298780@T1` | -0.41550 |
| `explicit.stat_3325883026@T1` | -0.41453 |
| `explicit.stat_915769802@T1` | -0.41451 |
| `explicit.stat_1570770415@T2` | -0.41267 |
| `explicit.stat_4220027924@T2` | -0.41216 |
| `explicit.stat_3372524247@T2` | -0.41190 |
| `explicit.stat_3325883026@T2` | -0.41056 |

### armour.chest — n=43823, R²=-1.8028

intercept: `3.1708`  ·  log_price: True  ·  ilvl: `-0.03926`  ·  n_mods: `-0.01110`  ·  n_top_tier: `0.34028`  ·  corrupted: `0.23130`  ·  n_sockets: `0.01465`  ·  quality: `0.07361`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.66333 |
| `explicit.stat_986397080@T2` | -0.41555 |
| `explicit.stat_986397080@T1` | -0.40400 |
| `explicit.stat_1692879867@T2` | -0.36966 |
| `explicit.stat_915769802@T2` | -0.36923 |
| `explicit.stat_4080418644@T2` | -0.36613 |
| `explicit.stat_3484657501@T1` | -0.36582 |
| `explicit.stat_4080418644@T1` | -0.36463 |
| `explicit.stat_915769802@T1` | -0.36244 |
| `explicit.stat_3301100256@T2` | -0.35205 |
| `explicit.stat_1062208444@T2` | -0.34882 |
| `explicit.stat_1999113824@T2` | -0.34805 |

### armour.helmet — n=42589, R²=-1.8269

intercept: `3.1443`  ·  log_price: True  ·  ilvl: `-0.03979`  ·  n_mods: `-0.01099`  ·  n_top_tier: `0.60251`  ·  corrupted: `0.48669`  ·  n_sockets: `0.03880`  ·  quality: `0.07483`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.10219 |
| `crafted.stat_3917489142@T1` | 0.88373 |
| `explicit.stat_1263695895@T1` | -0.83924 |
| `explicit.stat_3917489142@T2` | -0.75043 |
| `explicit.stat_2162097452@T2` | -0.74474 |
| `explicit.stat_1263695895@T2` | -0.71581 |
| `explicit.stat_3917489142@T1` | -0.68348 |
| `explicit.stat_4015621042@T2` | -0.66222 |
| `explicit.stat_4052037485@T2` | -0.64565 |
| `explicit.stat_1999113824@T1` | -0.63682 |
| `explicit.stat_803737631@T1` | -0.63417 |
| `explicit.stat_3321629045@T2` | -0.63305 |

### armour.boots — n=39443, R²=-1.7759

intercept: `3.3347`  ·  log_price: True  ·  ilvl: `-0.04117`  ·  n_mods: `-0.01585`  ·  n_top_tier: `0.39340`  ·  corrupted: `0.00010`  ·  n_sockets: `0.04236`  ·  quality: `0.07052`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.84850 |
| `crafted.stat_3917489142@T1` | 1.65140 |
| `explicit.stat_2339757871@T1` | -1.06825 |
| `explicit.stat_2923486259@T1` | 0.75909 |
| `explicit.stat_3299347043@T1` | -0.49195 |
| `explicit.stat_3917489142@T2` | -0.46923 |
| `explicit.stat_2923486259@T2` | -0.43564 |
| `explicit.stat_1671376347@T2` | -0.43228 |
| `explicit.stat_1874553720@T1` | -0.42578 |
| `explicit.stat_3321629045@T2` | -0.42433 |
| `explicit.stat_328541901@T2` | -0.42159 |
| `explicit.stat_2160282525@T1` | -0.42036 |

### armour.gloves — n=38449, R²=-1.7995

intercept: `3.7909`  ·  log_price: True  ·  ilvl: `-0.04957`  ·  n_mods: `0.00046`  ·  n_top_tier: `0.79144`  ·  corrupted: `-0.05806`  ·  n_sockets: `0.13717`  ·  quality: `0.06282`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 1.97741 |
| `explicit.stat_2923486259@T2` | -1.06018 |
| `explicit.stat_4052037485@T2` | -1.03745 |
| `explicit.stat_4052037485@T1` | -1.02998 |
| `explicit.stat_9187492@T2` | -0.97722 |
| `explicit.stat_3484657501@T2` | -0.96756 |
| `explicit.stat_4015621042@T2` | -0.93195 |
| `explicit.stat_3321629045@T2` | -0.91792 |
| `explicit.stat_803737631@T2` | -0.89620 |
| `explicit.stat_3484657501@T1` | -0.88494 |
| `explicit.stat_124859000@T1` | -0.88073 |
| `explicit.stat_803737631@T1` | -0.87296 |

### weapon.wand — n=22807, R²=-2.0032

intercept: `4.1722`  ·  log_price: True  ·  ilvl: `-0.05171`  ·  n_mods: `-0.05399`  ·  n_top_tier: `0.33007`  ·  corrupted: `0.00410`  ·  n_sockets: `0.02545`  ·  quality: `0.04699`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.01584 |
| `explicit.stat_1545858329@T1` | 3.07295 |
| `explicit.stat_2254480358@T1` | 2.67867 |
| `explicit.stat_124131830@T1` | 2.28426 |
| `explicit.stat_591105508@T1` | 2.16374 |
| `explicit.stat_4226189338@T1` | 1.90283 |
| `explicit.stat_736967255@T2` | 1.84713 |
| `explicit.stat_2254480358@T2` | 1.36370 |
| `crafted.stat_124131830` | 1.20761 |
| `explicit.stat_4226189338@T2` | 0.99501 |
| `explicit.stat_1545858329@T2` | 0.74688 |
| `explicit.stat_1263695895@T1` | -0.69452 |

### flask.charm — n=19619, R²=-0.6549

intercept: `0.1041`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.60930`  ·  corrupted: `1.52910`  ·  quality: `0.01032`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.66756 |
| `explicit.stat_1056492907` | 2.68940 |
| `explicit.stat_3246948616` | 1.60940 |
| `explicit.stat_1120862500@T2` | -1.60933 |
| `explicit.stat_828533480@T2` | -1.60932 |
| `explicit.stat_1873752457@T2` | -1.60930 |
| `explicit.stat_3196823591@T2` | -1.60925 |
| `explicit.stat_2676834156@T2` | -1.60925 |
| `explicit.stat_2365392475@T2` | -1.60924 |
| `explicit.stat_388617051@T2` | -1.60770 |
| `explicit.stat_828533480@T1` | -1.60635 |
| `explicit.stat_1873752457@T1` | -1.60218 |

### weapon.bow — n=18181, R²=-1.8973

intercept: `4.0014`  ·  log_price: True  ·  ilvl: `-0.04846`  ·  n_mods: `-0.05687`  ·  n_top_tier: `0.82245`  ·  corrupted: `0.65765`  ·  n_sockets: `0.01663`  ·  quality: `0.03815`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 3.24314 |
| `desecrated.stat_210067635@T1` | -2.00401 |
| `explicit.stat_1263695895@T1` | -1.27111 |
| `explicit.stat_1263695895@T2` | -1.23379 |
| `crafted.stat_3035140377` | 1.18250 |
| `explicit.stat_709508406@T1` | 1.10835 |
| `explicit.stat_1509134228@T1` | -0.95062 |
| `explicit.stat_821021828@T2` | -0.88875 |
| `explicit.stat_2463230181@T2` | -0.88365 |
| `explicit.stat_1368271171@T1` | -0.88233 |
| `explicit.stat_210067635@T2` | -0.88110 |
| `explicit.stat_1368271171@T2` | -0.87897 |

### weapon.crossbow — n=17071, R²=-1.8848

intercept: `4.0322`  ·  log_price: True  ·  ilvl: `-0.04937`  ·  n_mods: `-0.04323`  ·  n_top_tier: `0.29198`  ·  corrupted: `0.03667`  ·  n_sockets: `0.03528`  ·  quality: `0.03037`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.74648 |
| `explicit.stat_1202301673@T1` | 1.67759 |
| `explicit.stat_2250681686@T2` | -1.42695 |
| `explicit.stat_1980802737` | 1.40450 |
| `explicit.stat_2250681686` | 1.22934 |
| `explicit.stat_1509134228@T1` | 1.17603 |
| `crafted.stat_3035140377` | 0.84598 |
| `explicit.stat_518292764@T1` | 0.55132 |
| `explicit.stat_1263695895@T2` | -0.51062 |
| `explicit.stat_387439868@T1` | 0.48507 |
| `explicit.stat_709508406@T1` | 0.40686 |
| `explicit.stat_3336890334@T2` | -0.40372 |

### weapon.warstaff — n=11898, R²=-0.3375

intercept: `-10.2888`  ·  log_price: True  ·  ilvl: `0.13823`  ·  n_mods: `-0.21735`  ·  n_top_tier: `0.39577`  ·  corrupted: `0.26721`  ·  n_sockets: `0.12707`  ·  quality: `0.05806`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.10541 |
| `desecrated.stat_2527686725@T1` | 1.07380 |
| `desecrated.stat_2231156303@T1` | 1.07380 |
| `explicit.stat_328541901@T2` | -0.93373 |
| `desecrated.stat_9187492` | 0.81369 |
| `explicit.stat_821021828@T2` | -0.78886 |
| `rune.stat_243313994` | 0.76373 |
| `explicit.stat_328541901@T1` | -0.71630 |
| `explicit.stat_2694482655@T1` | 0.61496 |
| `explicit.stat_691932474@T2` | -0.57651 |
| `explicit.stat_1037193709@T2` | -0.56467 |
| `explicit.stat_1037193709@T1` | 0.52413 |

### weapon.staff — n=11288, R²=-0.3613

intercept: `-15.4725`  ·  log_price: True  ·  ilvl: `0.19719`  ·  n_mods: `-0.06773`  ·  n_top_tier: `0.48177`  ·  corrupted: `0.70931`  ·  n_sockets: `0.15677`  ·  quality: `0.03433`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.05841 |
| `explicit.stat_1600707273@T1` | 1.63738 |
| `explicit.stat_1545858329@T1` | 1.44774 |
| `explicit.stat_591105508@T1` | 1.43728 |
| `explicit.stat_124131830@T1` | 1.38612 |
| `explicit.stat_293638271@T2` | -1.06835 |
| `rune.stat_124131830` | 1.00665 |
| `explicit.stat_2254480358@T1` | 0.96715 |
| `explicit.stat_3962278098@T2` | 0.82427 |
| `explicit.stat_1263695895@T2` | -0.74764 |
| `explicit.stat_124131830@T2` | 0.68902 |
| `explicit.stat_473429811@T2` | -0.66854 |

### weapon.sceptre — n=11071, R²=-0.3414

intercept: `-21.2263`  ·  log_price: True  ·  ilvl: `0.26867`  ·  n_mods: `0.02827`  ·  n_top_tier: `0.09820`  ·  corrupted: `0.26534`  ·  n_sockets: `0.22975`  ·  quality: `0.02995`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.72886 |
| `explicit.stat_2162097452@T2` | 1.41311 |
| `explicit.stat_3057012405@T1` | 1.00723 |
| `explicit.stat_1263695895@T2` | -0.95858 |
| `explicit.stat_1798257884@T2` | 0.93648 |
| `explicit.stat_101878827@T2` | 0.92342 |
| `explicit.stat_101878827@T1` | 0.86483 |
| `explicit.stat_849987426@T1` | 0.75728 |
| `explicit.stat_1263695895@T1` | -0.74526 |
| `explicit.stat_2854751904@T2` | -0.74389 |
| `explicit.stat_2347036682@T1` | 0.66688 |
| `explicit.stat_4080418644@T2` | -0.55281 |

### weapon.spear — n=8971, R²=-0.3837

intercept: `-13.6814`  ·  log_price: True  ·  ilvl: `0.18547`  ·  n_mods: `-0.12781`  ·  n_top_tier: `0.62951`  ·  corrupted: `-0.55710`  ·  n_sockets: `0.18345`  ·  quality: `0.06913`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -4.20687 |
| `crafted.stat_210067635@T2` | -3.61693 |
| `explicit.stat_1202301673@T1` | 1.12113 |
| `explicit.stat_4080418644@T2` | -1.04078 |
| `explicit.stat_1940865751@T2` | -1.00745 |
| `desecrated.stat_210067635@T1` | -0.98590 |
| `explicit.stat_9187492@T1` | 0.97950 |
| `crafted.stat_3035140377` | 0.97905 |
| `explicit.stat_691932474@T2` | -0.86113 |
| `explicit.stat_3336890334@T2` | -0.84944 |
| `explicit.stat_3261801346@T1` | -0.78150 |
| `explicit.stat_748522257@T2` | -0.75729 |

### armour.focus — n=7332, R²=-0.3388

intercept: `-16.6102`  ·  log_price: True  ·  ilvl: `0.20946`  ·  n_mods: `-0.08832`  ·  n_top_tier: `0.86541`  ·  corrupted: `-0.00463`  ·  n_sockets: `0.28319`  ·  quality: `0.02890`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.52314 |
| `explicit.stat_4220027924@T1` | -1.37133 |
| `crafted.stat_2974417149@T1` | 1.06189 |
| `explicit.stat_4220027924@T2` | -1.05066 |
| `explicit.stat_2923486259@T2` | -1.02446 |
| `explicit.stat_4015621042@T1` | -1.01493 |
| `explicit.stat_2768835289@T1` | -1.01155 |
| `explicit.stat_2231156303@T1` | -0.99446 |
| `explicit.stat_2231156303@T2` | -0.93538 |
| `explicit.stat_1050105434@T2` | -0.89213 |
| `explicit.stat_2339757871@T2` | -0.88545 |
| `explicit.stat_3291658075@T1` | -0.88426 |

### armour.quiver — n=6832, R²=-0.289

intercept: `-17.7065`  ·  log_price: True  ·  ilvl: `0.21065`  ·  n_mods: `-0.04339`  ·  n_top_tier: `0.67743`  ·  corrupted: `0.97609`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.58108 |
| `explicit.stat_681332047@T2` | -1.58984 |
| `explicit.stat_681332047@T1` | -1.39654 |
| `explicit.stat_1573130764@T2` | -1.09159 |
| `explicit.stat_1573130764@T1` | -1.03196 |
| `explicit.stat_2194114101@T2` | -0.84254 |
| `explicit.stat_803737631@T1` | -0.76931 |
| `explicit.stat_4067062424@T1` | -0.70683 |
| `explicit.stat_2321178454@T2` | -0.60231 |
| `explicit.stat_803737631@T2` | -0.59915 |
| `explicit.stat_3261801346@T1` | -0.56479 |
| `explicit.stat_4067062424@T2` | -0.47899 |

### armour.shield — n=5874, R²=-0.4377

intercept: `-12.2774`  ·  log_price: True  ·  ilvl: `0.16282`  ·  n_mods: `-0.12002`  ·  n_top_tier: `0.57638`  ·  corrupted: `-0.40762`  ·  n_sockets: `0.40952`  ·  quality: `0.05786`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.32038 |
| `explicit.stat_2901986750@T1` | -1.11695 |
| `explicit.stat_328541901@T1` | -1.10143 |
| `explicit.stat_2339757871@T1` | -1.07857 |
| `explicit.stat_1011760251@T1` | -0.96601 |
| `explicit.stat_3321629045@T2` | -0.95761 |
| `explicit.stat_328541901@T2` | -0.88707 |
| `explicit.stat_3033371881@T2` | -0.85548 |
| `explicit.stat_3484657501@T1` | -0.83481 |
| `explicit.stat_2481353198@T1` | -0.83227 |
| `explicit.stat_2481353198@T2` | -0.80728 |
| `explicit.stat_3261801346@T1` | -0.79369 |

### weapon.twomace — n=5369, R²=-0.4495

intercept: `-11.2985`  ·  log_price: True  ·  ilvl: `0.15013`  ·  n_mods: `-0.19203`  ·  n_top_tier: `0.38838`  ·  corrupted: `0.70441`  ·  n_sockets: `0.13315`  ·  quality: `0.06286`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.10884 |
| `explicit.stat_1037193709@T1` | -1.54065 |
| `explicit.stat_1263695895@T2` | -1.52148 |
| `explicit.stat_3336890334@T1` | -1.30982 |
| `explicit.stat_2694482655@T1` | 1.15417 |
| `explicit.stat_1263695895@T1` | -1.03898 |
| `explicit.stat_3695891184@T1` | -0.78790 |
| `explicit.stat_9187492@T1` | -0.75393 |
| `explicit.stat_3695891184@T2` | -0.68931 |
| `explicit.stat_518292764@T2` | -0.64338 |
| `explicit.stat_387439868@T2` | -0.56528 |
| `explicit.stat_709508406@T1` | 0.52152 |

## Coverage (listings per base)

- … **Sapphire** — 36175 listings (36116 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 35265 listings (35220 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 27015 listings (26984 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 12615 listings (12597 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11503 listings (11479 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 11151 listings (11125 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 11036 listings (11024 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10378 listings (10353 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10308 listings (10285 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 9793 listings (9780 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8573 listings (8558 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8218 listings (8209 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8149 listings (8140 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7342 listings (7319 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 7075 listings (7068 priced) [0.3–3985176410.3 ex]
- … **Unset Ring** — 7061 listings (7042 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 7000 listings (6985 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 6935 listings (6927 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6869 listings (6841 priced) [0.3–398912568423.8 ex]
- … **Ancestral Tiara** — 6806 listings (6777 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6804 listings (6795 priced) [0.2–275252424.7 ex]
- … **Bloodstone Amulet** — 6725 listings (6715 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6390 listings (6387 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6295 listings (6281 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6104 listings (6092 priced) [0.3–398912568423.8 ex]

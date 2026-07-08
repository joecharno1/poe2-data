# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-08T09:59:01+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **321784** (321359 priced in exalted)
- Distinct bases: 955 · distinct mods: 2830 · mod rows: 1527176
- Sold signals: **30560** sold · 172129 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-08T09:49:31+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×21.88** (median |log error| 3.0857)
- Within ±30% of asking price: **15%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.08** · typical error ×56.38 · ±30% 5% · n=46928
- Premium segment (60ex+): skill **+0.09** · typical error ×249.11 · ±30% 0% · n=29317

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 6144 | ×49.90 | 19% | +0.03 | +0.04 |
| accessory.amulet | 5786 | ×44.70 | 20% | +0.03 | +0.03 |
| jewel | 5454 | ×8.41 | 7% | +0.01 | +0.05 |
| accessory.belt | 4662 | ×12.98 | 5% | +0.00 | +0.01 |
| armour.chest | 4593 | ×12.22 | 7% | +0.09 | +0.10 |
| armour.helmet | 4515 | ×14.75 | 6% | +0.04 | +0.06 |
| armour.boots | 4208 | ×18.68 | 10% | +0.11 | +0.12 |
| armour.gloves | 4177 | ×21.54 | 6% | +0.11 | +0.11 |
| other | 3882 | ×9.81 | 38% | +0.05 | +0.15 |
| weapon.wand | 2816 | ×35.14 | 21% | +0.06 | +0.07 |
| weapon.bow | 2267 | ×19.13 | 21% | +0.08 | +0.10 |
| weapon.crossbow | 2119 | ×19.95 | 20% | +0.09 | +0.10 |
| weapon.warstaff | 1063 | ×61.00 | 18% | +0.03 | +0.04 |
| weapon.sceptre | 977 | ×50.00 | 13% | +0.08 | +0.04 |
| weapon.staff | 971 | ×50.00 | 18% | +0.04 | +0.06 |
| weapon.spear | 801 | ×40.41 | 17% | +0.02 | +0.03 |
| armour.focus | 685 | ×605.89 | 12% | +0.02 | +0.07 |
| armour.quiver | 621 | ×75.93 | 12% | +0.00 | +0.04 |
| armour.shield | 537 | ×25.00 | 18% | +0.02 | +0.04 |
| weapon.twomace | 472 | ×20.00 | 14% | +0.01 | +0.06 |
| flask.charm | 433 | ×10.00 | 37% | -0.00 | -0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=33270, R²=-0.5676

intercept: `1.6061`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `0.00940`  ·  n_top_tier: `0.35998`  ·  corrupted: `0.84129`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2891184298@T1` | 1.50662 |
| `explicit.stat_3291658075@T1` | 1.10760 |
| `explicit.stat_2974417149@T1` | 0.89690 |
| `explicit.stat_101878827@T1` | -0.74514 |
| `explicit.stat_3917489142@T1` | 0.53643 |
| `explicit.stat_1050105434@T1` | -0.49698 |
| `explicit.stat_2106365538@T1` | 0.40975 |
| `explicit.stat_1589917703@T1` | 0.32338 |
| `explicit.stat_3141070085@T1` | -0.29663 |
| `explicit.stat_789117908@T1` | -0.28838 |
| `implicit.stat_1379411836` | -0.24819 |
| `implicit.stat_4041853756` | 0.22937 |

### jewel — n=29128, R²=-0.6361

intercept: `-1.1438`  ·  log_price: True  ·  ilvl: `0.03641`  ·  n_mods: `0.19316`  ·  n_top_tier: `-0.06283`  ·  corrupted: `0.32058`  ·  quality: `0.21543`

| stat_id | coef |
|---|---|
| `explicit.stat_1569101201@T1` | 3.65001 |
| `explicit.stat_3741323227@T1` | -3.51351 |
| `explicit.stat_1569159338@T1` | -3.31797 |
| `explicit.stat_3192728503@T1` | -3.31163 |
| `explicit.stat_1062710370@T1` | -2.51039 |
| `explicit.stat_2527686725@T1` | 2.27006 |
| `explicit.stat_1316278494@T1` | -2.26567 |
| `explicit.stat_440490623@T1` | -2.16097 |
| `explicit.stat_3714003708@T1` | -2.06206 |
| `explicit.stat_1854213750@T1` | -1.83737 |
| `explicit.stat_234296660@T1` | -1.80619 |
| `explicit.stat_627767961@T1` | -1.74788 |

### accessory.ring — n=28040, R²=-1.9735

intercept: `4.5998`  ·  log_price: True  ·  ilvl: `-0.05524`  ·  n_mods: `-0.00081`  ·  n_top_tier: `0.43614`  ·  corrupted: `0.87642`  ·  n_sockets: `-0.18688`  ·  quality: `0.08178`

| stat_id | coef |
|---|---|
| `explicit.stat_1379411836@T1` | -1.60331 |
| `explicit.stat_1379411836@T2` | -1.31411 |
| `explicit.stat_1671376347@T1` | 1.06515 |
| `explicit.stat_1263695895@T1` | -0.57264 |
| `explicit.stat_1368271171@T1` | -0.51277 |
| `explicit.stat_1263695895@T2` | -0.51239 |
| `explicit.stat_803737631@T1` | -0.48987 |
| `explicit.stat_3291658075@T2` | -0.48628 |
| `explicit.stat_3291658075@T1` | -0.48159 |
| `explicit.stat_803737631@T2` | -0.47882 |
| `explicit.stat_1368271171@T2` | -0.47366 |
| `explicit.stat_2231156303@T1` | -0.47058 |

### accessory.amulet — n=26518, R²=-2.0662

intercept: `4.0676`  ·  log_price: True  ·  ilvl: `-0.04893`  ·  n_mods: `-0.03006`  ·  n_top_tier: `1.10012`  ·  corrupted: `0.06651`  ·  n_sockets: `1.03341`  ·  quality: `-0.00070`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.36588 |
| `explicit.stat_983749596@T1` | -1.32632 |
| `explicit.stat_983749596@T2` | -1.30548 |
| `explicit.stat_587431675@T1` | -1.20265 |
| `explicit.stat_2748665614@T1` | -1.19812 |
| `explicit.stat_3325883026@T1` | -1.18656 |
| `explicit.stat_2748665614@T2` | -1.17525 |
| `explicit.stat_472520716@T2` | -1.17034 |
| `explicit.stat_3325883026@T2` | -1.16329 |
| `explicit.stat_472520716@T1` | -1.16116 |
| `explicit.stat_3489782002@T2` | -1.15949 |
| `explicit.stat_3917489142@T2` | -1.15405 |

### accessory.belt — n=21462, R²=-0.3592

intercept: `5.7686`  ·  log_price: True  ·  ilvl: `-0.03723`  ·  n_mods: `-0.41968`  ·  n_top_tier: `0.59905`  ·  corrupted: `0.57969`  ·  n_sockets: `-0.00839`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.90720 |
| `explicit.stat_1389754388@T1` | -1.27818 |
| `explicit.stat_51994685@T1` | -0.96378 |
| `explicit.stat_2881298780@T1` | -0.96228 |
| `explicit.stat_3325883026@T1` | -0.92258 |
| `explicit.stat_2923486259@T2` | -0.78649 |
| `explicit.stat_644456512@T1` | -0.78484 |
| `explicit.stat_1836676211@T2` | -0.77287 |
| `explicit.stat_2881298780@T2` | -0.73069 |
| `explicit.stat_1570770415@T1` | -0.72658 |
| `explicit.stat_1671376347@T2` | -0.71786 |
| `explicit.stat_1389754388@T2` | -0.70228 |

### armour.chest — n=21277, R²=-0.9671

intercept: `4.5126`  ·  log_price: True  ·  ilvl: `-0.05341`  ·  n_mods: `-0.10008`  ·  n_top_tier: `0.56920`  ·  corrupted: `0.10990`  ·  n_sockets: `0.03849`  ·  quality: `0.02793`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.01568 |
| `explicit.stat_915769802@T1` | -1.01439 |
| `explicit.stat_4015621042@T1` | -0.99540 |
| `explicit.stat_3321629045@T1` | -0.88017 |
| `explicit.stat_915769802@T2` | -0.86634 |
| `explicit.stat_4080418644@T2` | -0.73431 |
| `explicit.stat_986397080@T2` | -0.72572 |
| `explicit.stat_3261801346@T2` | -0.71048 |
| `explicit.stat_3261801346@T1` | -0.69964 |
| `explicit.stat_3484657501@T1` | -0.69868 |
| `explicit.stat_3325883026@T2` | -0.68575 |
| `explicit.stat_3362812763@T2` | -0.67080 |

### armour.helmet — n=20841, R²=-0.7999

intercept: `4.3299`  ·  log_price: True  ·  ilvl: `-0.05346`  ·  n_mods: `-0.12357`  ·  n_top_tier: `0.58235`  ·  corrupted: `0.75430`  ·  n_sockets: `0.00517`  ·  quality: `0.03475`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.40347 |
| `explicit.stat_53045048@T2` | -1.16299 |
| `explicit.stat_3362812763@T1` | -1.08927 |
| `explicit.stat_4080418644@T2` | -1.03782 |
| `explicit.stat_53045048@T1` | -0.93398 |
| `explicit.stat_1263695895@T1` | -0.93108 |
| `explicit.stat_1062208444@T2` | -0.89887 |
| `explicit.stat_2339757871@T1` | -0.81860 |
| `explicit.stat_2162097452@T2` | -0.75229 |
| `explicit.stat_803737631@T2` | -0.75071 |
| `explicit.stat_3362812763@T2` | -0.74326 |
| `explicit.stat_587431675@T2` | -0.73652 |

### armour.boots — n=19674, R²=-1.1123

intercept: `4.1856`  ·  log_price: True  ·  ilvl: `-0.05111`  ·  n_mods: `-0.06058`  ·  n_top_tier: `0.52582`  ·  corrupted: `0.39212`  ·  n_sockets: `0.06054`  ·  quality: `0.02510`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.61117 |
| `explicit.stat_2339757871@T1` | -0.83691 |
| `explicit.stat_2923486259@T2` | -0.81826 |
| `explicit.stat_4220027924@T1` | 0.78096 |
| `explicit.stat_3362812763@T1` | -0.74851 |
| `explicit.stat_3917489142@T2` | -0.70514 |
| `explicit.stat_328541901@T1` | -0.67780 |
| `explicit.stat_99927264@T1` | -0.67204 |
| `explicit.stat_1062208444@T2` | -0.67186 |
| `explicit.stat_3321629045@T1` | -0.64344 |
| `desecrated.stat_2250533757@T2` | -0.62942 |
| `explicit.stat_1671376347@T2` | -0.62121 |

### armour.gloves — n=19180, R²=-1.0298

intercept: `3.8780`  ·  log_price: True  ·  ilvl: `-0.05270`  ·  n_mods: `-0.06309`  ·  n_top_tier: `0.49119`  ·  corrupted: `0.30211`  ·  n_sockets: `0.33963`  ·  quality: `0.02114`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.81965 |
| `explicit.stat_681332047@T2` | -1.06300 |
| `explicit.stat_328541901@T1` | -0.99115 |
| `explicit.stat_803737631@T2` | -0.91827 |
| `explicit.stat_3484657501@T2` | -0.91266 |
| `explicit.stat_2797971005@T2` | -0.83135 |
| `explicit.stat_803737631@T1` | -0.75403 |
| `explicit.stat_2797971005@T1` | -0.73619 |
| `explicit.stat_3299347043@T2` | -0.71023 |
| `explicit.stat_3033371881@T2` | -0.69767 |
| `explicit.stat_4220027924@T2` | -0.68048 |
| `explicit.stat_3484657501@T1` | -0.65616 |

### weapon.wand — n=13073, R²=-2.0638

intercept: `3.6789`  ·  log_price: True  ·  ilvl: `-0.04592`  ·  n_mods: `-0.00719`  ·  n_top_tier: `0.60901`  ·  corrupted: `0.00070`  ·  n_sockets: `0.01940`  ·  quality: `0.01853`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.48869 |
| `explicit.stat_591105508@T1` | 1.77703 |
| `explicit.stat_4226189338@T1` | 1.76181 |
| `explicit.stat_1545858329@T1` | 1.74468 |
| `explicit.stat_1600707273@T1` | 1.68717 |
| `explicit.stat_124131830@T1` | 1.62701 |
| `explicit.stat_736967255@T2` | 1.16222 |
| `crafted.stat_124131830` | 0.74984 |
| `explicit.stat_2768835289@T2` | -0.65637 |
| `explicit.stat_737908626@T1` | -0.64794 |
| `explicit.stat_2231156303@T2` | -0.63439 |
| `explicit.stat_473429811@T1` | -0.63319 |

### weapon.bow — n=10687, R²=-2.0205

intercept: `3.3871`  ·  log_price: True  ·  ilvl: `-0.04198`  ·  n_mods: `-0.01092`  ·  n_top_tier: `0.45543`  ·  corrupted: `0.00548`  ·  n_sockets: `0.00122`  ·  quality: `0.00561`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.34507 |
| `explicit.stat_2463230181@T1` | 1.81477 |
| `explicit.stat_1202301673@T1` | 1.70669 |
| `desecrated.stat_666077204@T1` | 1.61075 |
| `crafted.stat_3035140377` | 1.44212 |
| `rune.stat_3885405204` | -0.62989 |
| `explicit.stat_55876295@T1` | -0.50915 |
| `explicit.stat_3336890334@T2` | -0.49886 |
| `explicit.stat_2694482655@T1` | -0.49746 |
| `explicit.stat_3695891184@T2` | -0.49354 |
| `explicit.stat_3639275092@T1` | -0.48101 |
| `explicit.stat_3261801346@T1` | -0.48026 |

### weapon.crossbow — n=10023, R²=-1.8139

intercept: `3.8386`  ·  log_price: True  ·  ilvl: `-0.04769`  ·  n_mods: `-0.00501`  ·  n_top_tier: `0.58306`  ·  corrupted: `-0.04863`  ·  n_sockets: `0.01144`  ·  quality: `0.00273`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -2.71991 |
| `explicit.stat_1980802737` | 2.09415 |
| `explicit.stat_709508406@T1` | 1.61134 |
| `explicit.stat_1202301673@T1` | 1.59562 |
| `explicit.stat_2250681686@T2` | -1.44574 |
| `explicit.stat_1509134228@T1` | 0.97729 |
| `explicit.stat_2250681686` | 0.88085 |
| `explicit.stat_1037193709@T1` | 0.84664 |
| `crafted.stat_3035140377` | 0.80284 |
| `rune.stat_669069897` | -0.74543 |
| `explicit.stat_1202301673@T2` | -0.70660 |
| `explicit.stat_1509134228@T2` | -0.65939 |

### flask.charm — n=6962, R²=-0.3669

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.32874`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.48036 |
| `explicit.stat_1056492907` | 2.99574 |
| `explicit.stat_2541588185@T1` | 0.48867 |
| `explicit.stat_2676834156@T1` | 0.37887 |
| `explicit.stat_3138344128` | 0.02138 |
| `explicit.stat_2678930256` | 0.00436 |
| `explicit.stat_3246948616` | 0.00005 |
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_1873752457@T2` | -0.00003 |
| `explicit.stat_1120862500@T2` | -0.00003 |
| `explicit.stat_2676834156@T2` | -0.00003 |
| `explicit.stat_828533480@T1` | -0.00002 |

### weapon.warstaff — n=4937, R²=-0.5551

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.00004`  ·  corrupted: `0.02909`  ·  n_sockets: `0.00001`  ·  quality: `0.00402`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 2.21993 |
| `rune.stat_731403740` | 1.57454 |
| `explicit.stat_9187492@T1` | 1.30429 |
| `rune.stat_1712188793` | -0.75082 |
| `desecrated.stat_9187492` | 0.61906 |
| `crafted.stat_210067635@T2` | -0.47646 |
| `desecrated.stat_518292764` | 0.37949 |
| `crafted.stat_3035140377` | 0.17115 |
| `explicit.stat_2694482655@T1` | 0.13821 |
| `desecrated.stat_669069897` | -0.09526 |
| `rune.stat_1509134228` | 0.08732 |
| `rune.stat_3336890334` | 0.06210 |

### weapon.staff — n=4590, R²=-0.5896

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00003`  ·  n_sockets: `0.00001`  ·  quality: `0.00327`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.06152 |
| `explicit.stat_4226189338@T1` | 2.30250 |
| `explicit.stat_1600707273@T1` | 1.60935 |
| `explicit.stat_2254480358@T1` | 1.60931 |
| `explicit.stat_2254480358@T2` | 1.51714 |
| `explicit.stat_3962278098@T2` | 0.69214 |
| `explicit.stat_473429811@T1` | 0.63916 |
| `explicit.stat_124131830@T1` | 0.52504 |
| `explicit.stat_3291658075@T2` | 0.46439 |
| `crafted.stat_124131830` | 0.41645 |
| `rune.stat_3990135792` | -0.14849 |
| `rune.stat_975988108` | -0.11805 |

### weapon.sceptre — n=4577, R²=-0.5981

intercept: `-0.0232`  ·  log_price: True  ·  ilvl: `0.00029`  ·  n_mods: `-0.00010`  ·  n_top_tier: `0.36788`  ·  corrupted: `1.44345`  ·  n_sockets: `0.00066`  ·  quality: `0.08653`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.93394 |
| `explicit.stat_4080418644@T2` | -0.36869 |
| `explicit.stat_4080418644@T1` | -0.36863 |
| `explicit.stat_1263695895@T2` | -0.36854 |
| `explicit.stat_2347036682@T2` | -0.36848 |
| `explicit.stat_1250712710@T1` | -0.36818 |
| `explicit.stat_3984865854@T2` | -0.36806 |
| `explicit.stat_328541901@T1` | -0.36801 |
| `explicit.stat_789117908@T1` | -0.36792 |
| `explicit.stat_1263695895@T1` | -0.36790 |
| `explicit.stat_3639275092@T2` | -0.36787 |
| `explicit.stat_2347036682@T1` | -0.36782 |

### weapon.spear — n=3940, R²=-0.5938

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00002`  ·  quality: `0.00350`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.29984 |
| `crafted.stat_3035140377` | 1.84040 |
| `explicit.stat_210067635@T1` | 1.09801 |
| `crafted.stat_518292764` | 0.81812 |
| `explicit.stat_1509134228@T1` | 0.53449 |
| `crafted.stat_210067635` | 0.12159 |
| `rune.stat_1039491398` | 0.08253 |
| `desecrated.stat_210067635` | -0.03746 |
| `explicit.stat_709508406@T1` | 0.01210 |
| `desecrated.stat_1509134228` | 0.00644 |
| `explicit.stat_9187492@T1` | 0.00329 |
| `explicit.stat_1940865751@T1` | 0.00172 |

### armour.focus — n=3182, R²=-0.6451

intercept: `-0.0081`  ·  log_price: True  ·  ilvl: `0.00010`  ·  n_mods: `-0.00004`  ·  n_top_tier: `0.42813`  ·  corrupted: `0.00616`  ·  n_sockets: `0.00015`  ·  quality: `0.03857`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -4.92966 |
| `desecrated.stat_3393628375@T1` | -4.87887 |
| `desecrated.stat_378817135@T1` | -0.93853 |
| `crafted.stat_2974417149@T1` | 0.61846 |
| `explicit.stat_3291658075@T1` | -0.42845 |
| `explicit.stat_789117908@T2` | -0.42839 |
| `explicit.stat_736967255@T2` | -0.42839 |
| `explicit.stat_274716455@T1` | -0.42836 |
| `explicit.stat_274716455@T2` | -0.42830 |
| `explicit.stat_4220027924@T2` | -0.42826 |
| `explicit.stat_4052037485@T2` | -0.42824 |
| `explicit.stat_2891184298@T2` | -0.42824 |

### armour.quiver — n=3005, R²=-0.636

intercept: `-0.0105`  ·  log_price: True  ·  ilvl: `0.00012`  ·  n_mods: `0.00004`  ·  n_top_tier: `0.51697`  ·  corrupted: `0.00113`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.49328 |
| `explicit.stat_2463230181@T1` | 1.09084 |
| `explicit.stat_681332047@T2` | -0.51813 |
| `explicit.stat_681332047@T1` | -0.51796 |
| `explicit.stat_1573130764@T1` | -0.51753 |
| `explicit.stat_2194114101@T2` | -0.51732 |
| `explicit.stat_1368271171@T2` | -0.51728 |
| `explicit.stat_1573130764@T2` | -0.51728 |
| `explicit.stat_2321178454@T2` | -0.51723 |
| `explicit.stat_3714003708@T2` | -0.51719 |
| `explicit.stat_803737631@T2` | -0.51710 |
| `explicit.stat_3261801346@T1` | -0.51697 |

### armour.shield — n=2593, R²=-0.5119

intercept: `-0.0010`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.34715`  ·  corrupted: `0.05369`  ·  n_sockets: `0.00001`  ·  quality: `0.06923`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.76820 |
| `explicit.stat_1978899297@T2` | -0.49596 |
| `explicit.stat_4220027924@T1` | 0.45088 |
| `explicit.stat_1011760251@T1` | -0.34821 |
| `explicit.stat_1011760251@T2` | -0.34786 |
| `explicit.stat_328541901@T1` | -0.34724 |
| `explicit.stat_2339757871@T1` | -0.34721 |
| `explicit.stat_328541901@T2` | -0.34721 |
| `explicit.stat_3484657501@T1` | -0.34719 |
| `explicit.stat_2481353198@T1` | -0.34719 |
| `explicit.stat_3372524247@T2` | -0.34718 |
| `explicit.stat_3484657501@T2` | -0.34718 |

### weapon.twomace — n=2286, R²=-0.5615

intercept: `-0.0012`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.31840`  ·  corrupted: `0.00003`  ·  n_sockets: `0.00002`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.52357 |
| `crafted.stat_3035140377` | 1.39544 |
| `desecrated.stat_1509134228@T1` | -0.36488 |
| `explicit.stat_3336890334@T1` | -0.31853 |
| `explicit.stat_1037193709@T1` | -0.31851 |
| `explicit.stat_1263695895@T1` | -0.31846 |
| `explicit.stat_387439868@T2` | -0.31846 |
| `explicit.stat_1037193709@T2` | -0.31845 |
| `explicit.stat_821021828@T2` | -0.31845 |
| `explicit.stat_821021828@T1` | -0.31844 |
| `explicit.stat_1263695895@T2` | -0.31844 |
| `explicit.stat_3336890334@T2` | -0.31843 |

## Coverage (listings per base)

- … **Sapphire** — 13871 listings (13854 priced) [0.3–7553463.8 ex]
- … **Emerald** — 13727 listings (13716 priced) [0.4–7553463.8 ex]
- … **Ruby** — 10570 listings (10560 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 6353 listings (6349 priced) [0.3–5288620.9 ex]
- … **Prismatic Ring** — 4865 listings (4863 priced) [0.3–24532814.5 ex]
- … **Stellar Amulet** — 4795 listings (4795 priced) [0.3–35690283.3 ex]
- … **Solar Amulet** — 4764 listings (4756 priced) [1.0–66666666.0 ex]
- … **Amethyst Ring** — 4660 listings (4659 priced) [0.3–4323655.9 ex]
- … **Gold Amulet** — 4536 listings (4531 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 4405 listings (4403 priced) [0.3–24532814.5 ex]
- … **Dueling Wand** — 4121 listings (4116 priced) [0.3–3736768402.2 ex]
- … **Sapphire Ring** — 3685 listings (3681 priced) [0.3–24532814.5 ex]
- … **Ruby Ring** — 3575 listings (3575 priced) [0.3–37474957.5 ex]
- … **Topaz Ring** — 3562 listings (3561 priced) [1.0–123132003.2 ex]
- … **Plate Belt** — 3244 listings (3241 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 3202 listings (3201 priced) [0.3–5286174.1 ex]
- … **Ancestral Tiara** — 3188 listings (3185 priced) [0.6–41469259.3 ex]
- … **Obliterator Bow** — 3140 listings (3132 priced) [0.4–22139622146.9 ex]
- … **Amber Amulet** — 3130 listings (3129 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3115 listings (3114 priced) [0.3–4547453.5 ex]
- … **Heavy Belt** — 3044 listings (3044 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 2974 listings (2974 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 2944 listings (2944 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 2856 listings (2856 priced) [0.3–24532814.5 ex]
- … **Lunar Amulet** — 2801 listings (2799 priced) [0.3–4877938.3 ex]

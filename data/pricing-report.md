# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-18T10:53:53+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **613979** (612141 priced in exalted)
- Distinct bases: 991 · distinct mods: 3238 · mod rows: 2907753
- Sold signals: **24983** sold · 348951 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-18T10:41:34+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.69** (median |log error| 3.2062)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×72.51 · ±30% 5% · n=89446
- Premium segment (60ex+): skill **+0.13** · typical error ×336.40 · ±30% 0% · n=60879

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 12789 | ×55.42 | 21% | +0.03 | +0.05 |
| jewel | 12003 | ×10.83 | 5% | +0.08 | +0.11 |
| accessory.amulet | 11659 | ×44.69 | 19% | +0.04 | +0.04 |
| accessory.belt | 8542 | ×25.87 | 17% | +0.07 | +0.10 |
| armour.chest | 8206 | ×17.26 | 22% | +0.08 | +0.10 |
| armour.helmet | 8109 | ×25.63 | 16% | +0.08 | +0.10 |
| armour.boots | 7486 | ×38.71 | 21% | +0.08 | +0.11 |
| armour.gloves | 7348 | ×41.87 | 18% | +0.07 | +0.09 |
| other | 7167 | ×2.00 | 43% | +0.10 | +0.17 |
| weapon.wand | 4447 | ×51.70 | 17% | +0.08 | +0.10 |
| weapon.bow | 3460 | ×29.01 | 12% | +0.14 | +0.17 |
| weapon.crossbow | 3297 | ×34.27 | 16% | +0.10 | +0.13 |
| weapon.warstaff | 2172 | ×29.52 | 6% | +0.17 | +0.15 |
| weapon.staff | 2048 | ×41.17 | 5% | +0.14 | +0.13 |
| weapon.sceptre | 2013 | ×32.08 | 5% | +0.20 | +0.20 |
| weapon.spear | 1612 | ×34.16 | 10% | +0.10 | +0.11 |
| armour.focus | 1353 | ×18.87 | 7% | +0.16 | +0.18 |
| armour.quiver | 1267 | ×25.62 | 7% | +0.16 | +0.17 |
| armour.shield | 1058 | ×21.50 | 8% | +0.07 | +0.10 |
| flask.charm | 1052 | ×17.35 | 32% | +0.00 | +0.04 |
| weapon.twomace | 943 | ×8.85 | 10% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=65564, R²=-0.9418

intercept: `-1.8414`  ·  log_price: True  ·  ilvl: `0.02551`  ·  n_mods: `0.85968`  ·  n_top_tier: `-0.33384`  ·  corrupted: `0.27832`  ·  quality: `0.00201`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.32543 |
| `explicit.stat_3374165039@T1` | -2.25372 |
| `explicit.stat_3485067555@T1` | 1.96349 |
| `explicit.stat_2523933828@T1` | -1.76708 |
| `explicit.stat_627767961@T1` | -1.62069 |
| `explicit.stat_318953428@T1` | -1.57528 |
| `explicit.stat_4147897060@T1` | -1.57283 |
| `explicit.stat_1805182458@T1` | -1.42250 |
| `explicit.stat_239367161@T1` | -1.38597 |
| `explicit.stat_3166958180@T1` | -1.33059 |
| `explicit.stat_3174700878@T1` | 1.30572 |
| `explicit.stat_1315743832@T1` | -1.27310 |

### other — n=58757, R²=-0.549

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00003`  ·  n_top_tier: `0.47759`  ·  corrupted: `0.27181`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.49343 |
| `explicit.stat_3141070085@T1` | -0.48544 |
| `explicit.stat_2106365538@T1` | -0.44453 |
| `explicit.stat_101878827@T1` | -0.24642 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_2219129443` | 0.23025 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_2231156303@T1` | -0.22946 |
| `explicit.stat_2482852589@T1` | -0.22187 |
| `explicit.stat_1589917703@T1` | -0.21704 |
| `explicit.stat_736967255@T1` | 0.10581 |
| `explicit.stat_789117908@T1` | -0.09563 |

### accessory.ring — n=58427, R²=-2.0362

intercept: `3.4437`  ·  log_price: True  ·  ilvl: `-0.04256`  ·  n_mods: `-0.00121`  ·  n_top_tier: `1.05160`  ·  corrupted: `0.02085`  ·  n_sockets: `-0.05159`  ·  quality: `0.00528`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.11547 |
| `explicit.stat_1573130764@T2` | -1.10394 |
| `explicit.stat_2231156303@T1` | -1.09597 |
| `explicit.stat_4220027924@T2` | -1.07648 |
| `explicit.stat_789117908@T1` | -1.07183 |
| `explicit.stat_2923486259@T2` | -1.07143 |
| `explicit.stat_789117908@T2` | -1.07109 |
| `explicit.stat_4080418644@T1` | -1.07050 |
| `explicit.stat_803737631@T1` | -1.07005 |
| `explicit.stat_3032590688@T2` | -1.06751 |
| `explicit.stat_3325883026@T1` | -1.06638 |
| `explicit.stat_3291658075@T1` | -1.06610 |

### accessory.amulet — n=53133, R²=-2.155

intercept: `3.7585`  ·  log_price: True  ·  ilvl: `-0.04584`  ·  n_mods: `-0.02284`  ·  n_top_tier: `1.13917`  ·  corrupted: `0.03855`  ·  n_sockets: `-0.14823`  ·  quality: `0.00090`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.54229 |
| `explicit.stat_3299347043@T2` | -1.33520 |
| `explicit.stat_472520716@T2` | -1.21817 |
| `explicit.stat_587431675@T2` | -1.21389 |
| `explicit.stat_2974417149@T1` | -1.20802 |
| `explicit.stat_2866361420@T2` | -1.20642 |
| `explicit.stat_2974417149@T2` | -1.20512 |
| `explicit.stat_803737631@T1` | -1.20107 |
| `explicit.stat_2866361420@T1` | -1.19578 |
| `explicit.stat_1050105434@T2` | -1.18263 |
| `explicit.stat_803737631@T2` | -1.18057 |
| `explicit.stat_1671376347@T2` | -1.16991 |

### accessory.belt — n=39190, R²=-1.4832

intercept: `4.5156`  ·  log_price: True  ·  ilvl: `-0.05332`  ·  n_mods: `-0.04840`  ·  n_top_tier: `0.62906`  ·  corrupted: `1.22547`  ·  n_sockets: `0.06308`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.15712 |
| `explicit.stat_2923486259@T1` | 0.98925 |
| `explicit.stat_3299347043@T2` | -0.75702 |
| `explicit.stat_2881298780@T1` | -0.71444 |
| `explicit.stat_4220027924@T2` | -0.67917 |
| `explicit.stat_3325883026@T1` | -0.66549 |
| `explicit.stat_51994685@T1` | -0.66487 |
| `explicit.stat_809229260@T2` | -0.65741 |
| `explicit.stat_1389754388@T1` | -0.64660 |
| `explicit.stat_1570770415@T2` | -0.64587 |
| `explicit.stat_644456512@T1` | -0.63757 |
| `explicit.stat_915769802@T2` | -0.63489 |

### armour.chest — n=38893, R²=-1.7299

intercept: `3.3243`  ·  log_price: True  ·  ilvl: `-0.04079`  ·  n_mods: `-0.02100`  ·  n_top_tier: `0.47368`  ·  corrupted: `0.11650`  ·  n_sockets: `0.02763`  ·  quality: `0.05758`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.65385 |
| `explicit.stat_986397080@T2` | -0.57002 |
| `explicit.stat_3981240776@T1` | 0.55325 |
| `explicit.stat_986397080@T1` | -0.52734 |
| `explicit.stat_3484657501@T1` | -0.52147 |
| `explicit.stat_915769802@T2` | -0.51418 |
| `explicit.stat_2339757871@T2` | -0.51265 |
| `explicit.stat_1692879867@T2` | -0.50351 |
| `explicit.stat_3299347043@T2` | -0.50228 |
| `explicit.stat_124859000@T1` | -0.50219 |
| `explicit.stat_1692879867@T1` | -0.50210 |
| `explicit.stat_915769802@T1` | -0.50072 |

### armour.helmet — n=37804, R²=-1.5897

intercept: `3.4048`  ·  log_price: True  ·  ilvl: `-0.04308`  ·  n_mods: `-0.02663`  ·  n_top_tier: `0.46858`  ·  corrupted: `0.72747`  ·  n_sockets: `0.06085`  ·  quality: `0.05821`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.23664 |
| `crafted.stat_3917489142@T1` | -1.78130 |
| `explicit.stat_3917489142@T2` | -0.94284 |
| `explicit.stat_3917489142@T1` | -0.85530 |
| `explicit.stat_2162097452@T2` | -0.63073 |
| `explicit.stat_4052037485@T2` | -0.59479 |
| `explicit.stat_1999113824@T1` | -0.58038 |
| `explicit.stat_1263695895@T1` | -0.57913 |
| `explicit.stat_2162097452@T1` | 0.55047 |
| `explicit.stat_803737631@T1` | -0.54948 |
| `explicit.stat_803737631@T2` | -0.53491 |
| `explicit.stat_53045048@T1` | -0.53308 |

### armour.boots — n=35155, R²=-1.7472

intercept: `3.2709`  ·  log_price: True  ·  ilvl: `-0.04033`  ·  n_mods: `-0.01584`  ·  n_top_tier: `0.68071`  ·  corrupted: `-0.00964`  ·  n_sockets: `0.02036`  ·  quality: `0.06086`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.50214 |
| `crafted.stat_3917489142@T1` | 1.23353 |
| `explicit.stat_2339757871@T1` | -0.91069 |
| `explicit.stat_3299347043@T1` | -0.81937 |
| `explicit.stat_3917489142@T2` | -0.79306 |
| `explicit.stat_2923486259@T2` | -0.72158 |
| `explicit.stat_1874553720@T1` | -0.71497 |
| `explicit.stat_1062208444@T2` | -0.71007 |
| `explicit.stat_2160282525@T1` | -0.70978 |
| `explicit.stat_3299347043@T2` | -0.70757 |
| `explicit.stat_3917489142@T1` | -0.70115 |
| `explicit.stat_4052037485@T2` | -0.70083 |

### armour.gloves — n=34294, R²=-1.9169

intercept: `3.4852`  ·  log_price: True  ·  ilvl: `-0.04400`  ·  n_mods: `-0.01548`  ·  n_top_tier: `0.55621`  ·  corrupted: `0.01032`  ·  n_sockets: `0.04639`  ·  quality: `0.05138`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.12374 |
| `rune.stat_201332984` | 1.73227 |
| `rune.stat_836936635` | 1.30160 |
| `explicit.stat_1671376347@T1` | 1.06170 |
| `explicit.stat_2923486259@T1` | -0.82557 |
| `explicit.stat_9187492@T2` | -0.80231 |
| `explicit.stat_9187492@T1` | 0.80216 |
| `explicit.stat_3484657501@T2` | -0.72154 |
| `explicit.stat_2923486259@T2` | -0.69814 |
| `explicit.stat_3484657501@T1` | -0.66858 |
| `explicit.stat_3321629045@T2` | -0.66693 |
| `explicit.stat_803737631@T2` | -0.63963 |

### weapon.wand — n=20896, R²=-2.1026

intercept: `3.6842`  ·  log_price: True  ·  ilvl: `-0.04555`  ·  n_mods: `-0.03585`  ·  n_top_tier: `0.40740`  ·  corrupted: `-0.02669`  ·  n_sockets: `0.05621`  ·  quality: `0.01113`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.15196 |
| `rune.stat_124131830` | -2.77710 |
| `explicit.stat_2254480358@T1` | 2.56980 |
| `explicit.stat_124131830@T1` | 2.13673 |
| `explicit.stat_4226189338@T1` | 1.93846 |
| `explicit.stat_591105508@T1` | 1.91221 |
| `explicit.stat_736967255@T2` | 1.76963 |
| `crafted.stat_124131830` | 1.28952 |
| `explicit.stat_2254480358@T2` | 1.05812 |
| `explicit.stat_4226189338@T2` | 1.00744 |
| `explicit.stat_2768835289@T2` | -0.75195 |
| `explicit.stat_1263695895@T2` | -0.72278 |

### weapon.bow — n=16710, R²=-1.7959

intercept: `3.8440`  ·  log_price: True  ·  ilvl: `-0.04374`  ·  n_mods: `-0.12226`  ·  n_top_tier: `0.64831`  ·  corrupted: `0.22013`  ·  n_sockets: `0.09245`  ·  quality: `0.03153`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.57911 |
| `crafted.stat_3035140377` | 1.43408 |
| `desecrated.stat_210067635@T1` | -1.20053 |
| `explicit.stat_1263695895@T1` | -1.10878 |
| `explicit.stat_2463230181@T2` | -1.07001 |
| `explicit.stat_518292764@T2` | -1.00557 |
| `explicit.stat_1263695895@T2` | -0.97761 |
| `explicit.stat_1202301673@T1` | 0.92260 |
| `explicit.stat_2463230181@T1` | -0.91333 |
| `explicit.stat_3695891184@T2` | -0.87518 |
| `explicit.stat_3695891184@T1` | -0.85726 |
| `explicit.stat_3336890334@T1` | 0.83438 |

### flask.charm — n=16600, R²=-0.5967

intercept: `0.0813`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.84000`  ·  corrupted: `1.60891`  ·  quality: `0.00013`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.85823 |
| `explicit.stat_1056492907` | 2.90643 |
| `explicit.stat_828533480@T2` | -1.84003 |
| `explicit.stat_1873752457@T2` | -1.84000 |
| `explicit.stat_1120862500@T2` | -1.84000 |
| `explicit.stat_388617051@T2` | -1.83999 |
| `explicit.stat_1873752457@T1` | -1.83998 |
| `explicit.stat_3196823591@T2` | -1.83997 |
| `explicit.stat_2676834156@T2` | -1.83996 |
| `explicit.stat_2365392475@T2` | -1.83996 |
| `explicit.stat_828533480@T1` | -1.83816 |
| `explicit.stat_1366840608@T2` | -1.83806 |

### weapon.crossbow — n=15672, R²=-1.8021

intercept: `3.8523`  ·  log_price: True  ·  ilvl: `-0.04613`  ·  n_mods: `-0.07413`  ·  n_top_tier: `0.62244`  ·  corrupted: `0.01762`  ·  n_sockets: `0.08210`  ·  quality: `0.02112`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.68764 |
| `explicit.stat_1980802737` | 1.26115 |
| `explicit.stat_2250681686@T2` | -1.15533 |
| `explicit.stat_1202301673@T1` | 1.00935 |
| `explicit.stat_1509134228@T2` | -0.78488 |
| `crafted.stat_3035140377` | 0.78372 |
| `explicit.stat_2250681686` | 0.78363 |
| `explicit.stat_2694482655@T1` | -0.78027 |
| `explicit.stat_1037193709@T1` | -0.77309 |
| `rune.stat_731403740` | 0.77008 |
| `explicit.stat_1263695895@T2` | -0.74853 |
| `explicit.stat_3695891184@T1` | -0.71760 |

### weapon.warstaff — n=10374, R²=-0.3525

intercept: `-10.4368`  ·  log_price: True  ·  ilvl: `0.14353`  ·  n_mods: `-0.24908`  ·  n_top_tier: `0.21609`  ·  corrupted: `0.27219`  ·  n_sockets: `0.19453`  ·  quality: `0.05841`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 2.11811 |
| `desecrated.stat_2527686725@T1` | 2.11811 |
| `desecrated.stat_3291658075@T1` | -1.68466 |
| `desecrated.stat_473429811@T1` | -1.68466 |
| `crafted.stat_210067635@T2` | 1.39992 |
| `rune.stat_243313994` | 0.89885 |
| `explicit.stat_1509134228@T1` | 0.80246 |
| `desecrated.stat_9187492` | 0.78898 |
| `explicit.stat_328541901@T1` | -0.77324 |
| `explicit.stat_9187492@T1` | 0.71137 |
| `explicit.stat_328541901@T2` | -0.66454 |
| `explicit.stat_1037193709@T1` | 0.56371 |

### weapon.staff — n=9729, R²=-0.3726

intercept: `-15.8671`  ·  log_price: True  ·  ilvl: `0.20543`  ·  n_mods: `-0.16448`  ·  n_top_tier: `0.55563`  ·  corrupted: `0.67733`  ·  n_sockets: `0.22176`  ·  quality: `0.03301`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.14745 |
| `explicit.stat_1545858329@T1` | 1.76336 |
| `explicit.stat_293638271@T2` | -1.66357 |
| `explicit.stat_591105508@T1` | 1.35584 |
| `explicit.stat_124131830@T1` | 1.18889 |
| `explicit.stat_2254480358@T2` | 0.94134 |
| `rune.stat_124131830` | 0.92932 |
| `explicit.stat_274716455@T1` | -0.86966 |
| `explicit.stat_1600707273@T1` | 0.83228 |
| `explicit.stat_293638271@T1` | -0.72806 |
| `explicit.stat_124131830@T2` | 0.67607 |
| `explicit.stat_2968503605@T1` | -0.67230 |

### weapon.sceptre — n=9613, R²=-0.3272

intercept: `-20.8145`  ·  log_price: True  ·  ilvl: `0.26842`  ·  n_mods: `-0.00612`  ·  n_top_tier: `0.16720`  ·  corrupted: `0.29968`  ·  n_sockets: `0.27105`  ·  quality: `0.03262`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.88172 |
| `explicit.stat_1250712710@T2` | 1.64821 |
| `explicit.stat_2162097452@T2` | 1.55321 |
| `explicit.stat_3057012405@T1` | 1.31776 |
| `explicit.stat_101878827@T1` | 0.84514 |
| `explicit.stat_101878827@T2` | 0.79870 |
| `explicit.stat_1798257884@T2` | 0.72568 |
| `explicit.stat_1250712710@T1` | 0.62693 |
| `explicit.stat_2347036682@T2` | -0.59963 |
| `explicit.stat_849987426@T1` | 0.52772 |
| `explicit.stat_1263695895@T2` | -0.48719 |
| `explicit.stat_1998951374@T1` | 0.47594 |

### weapon.spear — n=7794, R²=-0.4094

intercept: `-12.8397`  ·  log_price: True  ·  ilvl: `0.17808`  ·  n_mods: `-0.17809`  ·  n_top_tier: `0.79929`  ·  corrupted: `-0.00396`  ·  n_sockets: `0.18928`  ·  quality: `0.06008`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.96290 |
| `explicit.stat_1202301673@T1` | 1.47943 |
| `explicit.stat_1509134228@T1` | 1.20789 |
| `desecrated.stat_210067635@T1` | -1.18915 |
| `explicit.stat_4080418644@T2` | -1.17625 |
| `explicit.stat_9187492@T1` | 1.16801 |
| `explicit.stat_9187492@T2` | -1.03709 |
| `crafted.stat_3035140377` | 1.03266 |
| `explicit.stat_1940865751@T2` | -1.01149 |
| `explicit.stat_3261801346@T1` | -1.00200 |
| `explicit.stat_748522257@T2` | -0.95234 |
| `explicit.stat_691932474@T2` | -0.94036 |

### armour.focus — n=6378, R²=-0.3614

intercept: `-14.2124`  ·  log_price: True  ·  ilvl: `0.18420`  ·  n_mods: `-0.13777`  ·  n_top_tier: `0.81581`  ·  corrupted: `0.37603`  ·  n_sockets: `0.44023`  ·  quality: `0.06284`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 3.40096 |
| `explicit.stat_4220027924@T2` | -1.35680 |
| `explicit.stat_2923486259@T1` | -1.23027 |
| `explicit.stat_4220027924@T1` | -1.21278 |
| `explicit.stat_2231156303@T2` | -1.12586 |
| `explicit.stat_2974417149@T1` | -0.90960 |
| `explicit.stat_2974417149@T2` | -0.89995 |
| `explicit.stat_736967255@T2` | -0.89946 |
| `explicit.stat_2891184298@T1` | -0.89887 |
| `explicit.stat_1050105434@T2` | -0.79869 |
| `explicit.stat_737908626@T2` | -0.79650 |
| `explicit.stat_2231156303@T1` | -0.78041 |

### armour.quiver — n=5990, R²=-0.2999

intercept: `-14.8318`  ·  log_price: True  ·  ilvl: `0.18213`  ·  n_mods: `-0.12268`  ·  n_top_tier: `0.82720`  ·  corrupted: `0.68959`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.73348 |
| `explicit.stat_2463230181@T1` | 2.63328 |
| `explicit.stat_1573130764@T1` | -1.39896 |
| `explicit.stat_681332047@T2` | -1.28796 |
| `explicit.stat_2463230181@T2` | 1.20728 |
| `explicit.stat_803737631@T2` | -0.98228 |
| `explicit.stat_4067062424@T1` | -0.94072 |
| `explicit.stat_2321178454@T2` | -0.91636 |
| `explicit.stat_1573130764@T2` | -0.80002 |
| `explicit.stat_2194114101@T2` | -0.79153 |
| `explicit.stat_3261801346@T1` | -0.78676 |
| `explicit.stat_803737631@T1` | -0.78223 |

### armour.shield — n=5204, R²=-0.4636

intercept: `-12.1766`  ·  log_price: True  ·  ilvl: `0.16189`  ·  n_mods: `-0.07128`  ·  n_top_tier: `0.80389`  ·  corrupted: `-0.21614`  ·  n_sockets: `0.31895`  ·  quality: `0.06206`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.49606 |
| `explicit.stat_3321629045@T2` | -1.38743 |
| `explicit.stat_2901986750@T1` | -1.24423 |
| `explicit.stat_3855016469@T1` | -1.23753 |
| `explicit.stat_2923486259@T2` | -1.10411 |
| `explicit.stat_2451402625@T1` | -1.06837 |
| `explicit.stat_3484657501@T2` | -1.06312 |
| `explicit.stat_3033371881@T2` | -1.04683 |
| `explicit.stat_328541901@T1` | -1.03444 |
| `explicit.stat_1301765461@T1` | 1.02820 |
| `explicit.stat_2451402625@T2` | -1.01987 |
| `explicit.stat_3261801346@T1` | -1.01909 |

### weapon.twomace — n=4766, R²=-0.4472

intercept: `-10.5852`  ·  log_price: True  ·  ilvl: `0.14719`  ·  n_mods: `-0.24257`  ·  n_top_tier: `0.31618`  ·  corrupted: `0.00513`  ·  n_sockets: `0.16618`  ·  quality: `0.05991`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.17506 |
| `desecrated.stat_1509134228@T1` | 1.63802 |
| `explicit.stat_1037193709@T1` | -1.55887 |
| `explicit.stat_3336890334@T1` | -1.06176 |
| `explicit.stat_387439868@T2` | -0.79425 |
| `explicit.stat_1263695895@T2` | -0.77470 |
| `crafted.stat_3035140377` | 0.75607 |
| `explicit.stat_9187492@T1` | -0.73441 |
| `explicit.stat_691932474@T1` | -0.69553 |
| `explicit.stat_3695891184@T1` | -0.58798 |
| `explicit.stat_1037193709@T2` | -0.55955 |
| `explicit.stat_1509134228@T1` | 0.53376 |

## Coverage (listings per base)

- … **Sapphire** — 30431 listings (30377 priced) [0.3–885594757.8 ex]
- … **Emerald** — 29633 listings (29592 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 22705 listings (22678 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11194 listings (11179 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 9943 listings (9922 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 9624 listings (9601 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9484 listings (9476 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8974 listings (8957 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8846 listings (8827 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8578 listings (8566 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7362 listings (7351 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7083 listings (7077 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7014 listings (7008 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6701 listings (6680 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6183 listings (6176 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 6115 listings (6088 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 6068 listings (6051 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6053 listings (6041 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6037 listings (6030 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5965 listings (5939 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5894 listings (5885 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5804 listings (5797 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5521 listings (5518 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5498 listings (5486 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5402 listings (5393 priced) [0.3–398912568423.8 ex]

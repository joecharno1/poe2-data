# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-16T01:30:21+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **530896** (529553 priced in exalted)
- Distinct bases: 984 · distinct mods: 3142 · mod rows: 2517681
- Sold signals: **25936** sold · 298320 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-16T01:22:11+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×23.68** (median |log error| 3.1645)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×70.92 · ±30% 5% · n=76729
- Premium segment (60ex+): skill **+0.11** · typical error ×333.35 · ±30% 0% · n=51429

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 10661 | ×39.79 | 22% | +0.05 | +0.07 |
| jewel | 10003 | ×9.77 | 5% | +0.04 | +0.08 |
| accessory.amulet | 9826 | ×43.62 | 20% | +0.03 | +0.04 |
| accessory.belt | 7467 | ×19.42 | 6% | +0.05 | +0.08 |
| armour.chest | 7286 | ×22.61 | 22% | +0.06 | +0.10 |
| armour.helmet | 7109 | ×27.48 | 18% | +0.06 | +0.09 |
| armour.boots | 6601 | ×29.96 | 22% | +0.06 | +0.08 |
| armour.gloves | 6477 | ×37.83 | 21% | +0.06 | +0.07 |
| other | 5844 | ×1.94 | 43% | +0.10 | +0.17 |
| weapon.wand | 4049 | ×34.82 | 17% | +0.07 | +0.08 |
| weapon.bow | 3234 | ×28.98 | 17% | +0.11 | +0.10 |
| weapon.crossbow | 3040 | ×27.87 | 16% | +0.09 | +0.13 |
| weapon.warstaff | 1884 | ×34.62 | 14% | +0.12 | +0.11 |
| weapon.sceptre | 1770 | ×45.24 | 6% | +0.15 | +0.15 |
| weapon.staff | 1768 | ×60.24 | 12% | +0.10 | +0.10 |
| weapon.spear | 1388 | ×53.67 | 16% | +0.09 | +0.09 |
| armour.focus | 1192 | ×39.07 | 7% | +0.14 | +0.16 |
| armour.quiver | 1107 | ×27.54 | 8% | +0.11 | +0.13 |
| flask.charm | 970 | ×25.00 | 35% | +0.04 | +0.06 |
| armour.shield | 943 | ×25.67 | 13% | +0.03 | +0.04 |
| weapon.twomace | 848 | ×19.89 | 13% | +0.08 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=54059, R²=-0.9231

intercept: `-1.7176`  ·  log_price: True  ·  ilvl: `0.02679`  ·  n_mods: `0.59800`  ·  n_top_tier: `-0.12866`  ·  corrupted: `0.34117`  ·  quality: `0.22635`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.30098 |
| `explicit.stat_2301718443@T1` | 3.03657 |
| `explicit.stat_627767961@T1` | -2.34184 |
| `explicit.stat_3780644166@T1` | -2.11152 |
| `explicit.stat_1805182458@T1` | -2.05321 |
| `explicit.stat_3485067555@T1` | 1.98621 |
| `explicit.stat_239367161@T1` | -1.60541 |
| `explicit.stat_2523933828@T1` | -1.54006 |
| `explicit.stat_234296660@T1` | -1.52657 |
| `explicit.stat_1697951953@T1` | -1.51637 |
| `explicit.stat_3166958180@T1` | -1.50864 |
| `explicit.stat_872504239@T1` | 1.48493 |

### other — n=51103, R²=-0.638

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.34659`  ·  corrupted: `0.34647`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.43348 |
| `explicit.stat_2974417149@T1` | 0.38368 |
| `explicit.stat_3299347043@T1` | -0.33686 |
| `implicit.stat_3879011313` | 0.32877 |
| `explicit.stat_2482852589@T1` | -0.28770 |
| `implicit.stat_2219129443` | 0.23062 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_789117908@T1` | -0.22474 |
| `explicit.stat_2106365538@T1` | -0.15391 |
| `implicit.stat_1379411836` | -0.13090 |
| `explicit.stat_1050105434@T1` | -0.12658 |
| `explicit.stat_3917489142@T1` | 0.09975 |

### accessory.ring — n=48868, R²=-1.9966

intercept: `3.5316`  ·  log_price: True  ·  ilvl: `-0.04364`  ·  n_mods: `0.00114`  ·  n_top_tier: `0.94198`  ·  corrupted: `0.02442`  ·  n_sockets: `2.18359`  ·  quality: `0.06971`

| stat_id | coef |
|---|---|
| `explicit.stat_2557965901@T1` | -1.04234 |
| `explicit.stat_2557965901@T2` | -1.01690 |
| `explicit.stat_2231156303@T1` | -0.97584 |
| `explicit.stat_3325883026@T1` | -0.97334 |
| `explicit.stat_1263695895@T1` | -0.97116 |
| `explicit.stat_803737631@T1` | -0.97069 |
| `explicit.stat_1368271171@T2` | -0.96730 |
| `explicit.stat_3325883026@T2` | -0.96509 |
| `explicit.stat_2144192055@T1` | -0.96306 |
| `explicit.stat_2231156303@T2` | -0.96281 |
| `explicit.stat_1263695895@T2` | -0.95973 |
| `explicit.stat_3291658075@T1` | -0.95940 |

### accessory.amulet — n=44954, R²=-2.1397

intercept: `3.6728`  ·  log_price: True  ·  ilvl: `-0.04490`  ·  n_mods: `-0.02467`  ·  n_top_tier: `0.92871`  ·  corrupted: `0.03994`  ·  n_sockets: `-0.11601`  ·  quality: `-0.00397`

| stat_id | coef |
|---|---|
| `explicit.stat_472520716@T2` | -1.04098 |
| `explicit.stat_472520716@T1` | -1.02826 |
| `explicit.stat_2901986750@T1` | -1.01971 |
| `explicit.stat_587431675@T2` | -1.00044 |
| `explicit.stat_803737631@T1` | -0.99244 |
| `explicit.stat_1050105434@T2` | -0.97739 |
| `explicit.stat_2866361420@T2` | -0.96931 |
| `explicit.stat_3917489142@T2` | -0.96691 |
| `explicit.stat_3489782002@T2` | -0.96549 |
| `explicit.stat_2974417149@T1` | -0.96339 |
| `explicit.stat_803737631@T2` | -0.95929 |
| `explicit.stat_3261801346@T1` | -0.95564 |

### accessory.belt — n=34334, R²=-0.9955

intercept: `6.0590`  ·  log_price: True  ·  ilvl: `-0.06247`  ·  n_mods: `-0.24673`  ·  n_top_tier: `1.10816`  ·  corrupted: `0.87786`  ·  n_sockets: `-0.19162`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.61519 |
| `explicit.stat_2881298780@T1` | -1.53721 |
| `explicit.stat_3299347043@T1` | -1.48974 |
| `explicit.stat_644456512@T1` | -1.43916 |
| `explicit.stat_3299347043@T2` | -1.40082 |
| `explicit.stat_809229260@T2` | -1.35563 |
| `explicit.stat_4220027924@T2` | -1.33685 |
| `explicit.stat_809229260@T1` | -1.25644 |
| `explicit.stat_4080418644@T2` | -1.24304 |
| `explicit.stat_1671376347@T2` | -1.17773 |
| `explicit.stat_3325883026@T1` | -1.15794 |
| `explicit.stat_644456512@T2` | -1.13616 |

### armour.chest — n=33960, R²=-1.6986

intercept: `3.5033`  ·  log_price: True  ·  ilvl: `-0.04317`  ·  n_mods: `-0.01651`  ·  n_top_tier: `0.47429`  ·  corrupted: `0.07407`  ·  n_sockets: `0.02213`  ·  quality: `0.05192`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.86478 |
| `explicit.stat_3981240776@T1` | 1.08121 |
| `explicit.stat_986397080@T2` | -0.57233 |
| `explicit.stat_986397080@T1` | -0.53978 |
| `explicit.stat_4015621042@T1` | -0.53749 |
| `explicit.stat_3484657501@T1` | -0.52658 |
| `explicit.stat_4080418644@T1` | -0.50591 |
| `explicit.stat_4080418644@T2` | -0.50489 |
| `explicit.stat_3372524247@T2` | -0.50382 |
| `explicit.stat_2451402625@T2` | -0.50321 |
| `explicit.stat_1692879867@T1` | -0.49689 |
| `explicit.stat_1999113824@T1` | -0.49529 |

### armour.helmet — n=33007, R²=-1.6429

intercept: `3.6091`  ·  log_price: True  ·  ilvl: `-0.04562`  ·  n_mods: `-0.02577`  ·  n_top_tier: `0.46009`  ·  corrupted: `0.87321`  ·  n_sockets: `0.04310`  ·  quality: `0.05334`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.79733 |
| `crafted.stat_3917489142@T1` | 1.91835 |
| `explicit.stat_1263695895@T1` | -0.66494 |
| `explicit.stat_3917489142@T2` | -0.65328 |
| `explicit.stat_1263695895@T2` | -0.61052 |
| `explicit.stat_4052037485@T2` | -0.56028 |
| `explicit.stat_3917489142@T1` | -0.54632 |
| `explicit.stat_1999113824@T1` | -0.53713 |
| `explicit.stat_2162097452@T2` | -0.52653 |
| `explicit.stat_3321629045@T2` | -0.51997 |
| `explicit.stat_3261801346@T1` | -0.51179 |
| `explicit.stat_803737631@T1` | -0.50210 |

### armour.boots — n=30926, R²=-1.7869

intercept: `3.3327`  ·  log_price: True  ·  ilvl: `-0.04108`  ·  n_mods: `-0.01201`  ·  n_top_tier: `0.63624`  ·  corrupted: `0.01932`  ·  n_sockets: `0.01942`  ·  quality: `0.03481`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.24000 |
| `explicit.stat_2339757871@T1` | -0.88066 |
| `explicit.stat_3917489142@T2` | -0.72700 |
| `explicit.stat_3299347043@T1` | -0.70986 |
| `desecrated.stat_2250533757@T2` | -0.69211 |
| `explicit.stat_2923486259@T2` | -0.67903 |
| `explicit.stat_2160282525@T1` | -0.67245 |
| `explicit.stat_1671376347@T2` | -0.66469 |
| `explicit.stat_1062208444@T2` | -0.66303 |
| `explicit.stat_99927264@T1` | -0.65983 |
| `explicit.stat_3484657501@T2` | -0.65666 |
| `explicit.stat_53045048@T1` | -0.65421 |

### armour.gloves — n=30094, R²=-1.8912

intercept: `3.5053`  ·  log_price: True  ·  ilvl: `-0.04421`  ·  n_mods: `-0.00573`  ·  n_top_tier: `0.48014`  ·  corrupted: `-0.00071`  ·  n_sockets: `0.03582`  ·  quality: `0.05014`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | -2.44779 |
| `explicit.stat_2339757871@T1` | 2.18726 |
| `explicit.stat_1671376347@T1` | 0.99547 |
| `explicit.stat_9187492@T1` | 0.90516 |
| `explicit.stat_9187492@T2` | -0.76802 |
| `explicit.stat_3484657501@T2` | -0.60873 |
| `explicit.stat_3484657501@T1` | -0.56055 |
| `explicit.stat_3321629045@T2` | -0.55775 |
| `explicit.stat_1999113824@T1` | 0.55603 |
| `explicit.stat_803737631@T2` | -0.55110 |
| `explicit.stat_4052037485@T1` | -0.53722 |
| `explicit.stat_3321629045@T1` | -0.51431 |

### weapon.wand — n=19141, R²=-2.2161

intercept: `3.6140`  ·  log_price: True  ·  ilvl: `-0.04462`  ·  n_mods: `-0.01524`  ·  n_top_tier: `0.73019`  ·  corrupted: `0.03958`  ·  n_sockets: `0.02621`  ·  quality: `0.00380`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.57819 |
| `rune.stat_124131830` | -2.52022 |
| `explicit.stat_2254480358@T1` | 2.28311 |
| `explicit.stat_4226189338@T1` | 1.67927 |
| `explicit.stat_591105508@T1` | 1.63642 |
| `explicit.stat_124131830@T1` | 1.58368 |
| `explicit.stat_736967255@T2` | 1.49657 |
| `crafted.stat_124131830` | 1.13068 |
| `explicit.stat_1263695895@T2` | -0.84960 |
| `explicit.stat_737908626@T1` | -0.81582 |
| `explicit.stat_2254480358@T2` | 0.81505 |
| `explicit.stat_1263695895@T1` | -0.81117 |

### weapon.bow — n=15363, R²=-1.9644

intercept: `3.5275`  ·  log_price: True  ·  ilvl: `-0.04262`  ·  n_mods: `-0.03559`  ·  n_top_tier: `0.59950`  ·  corrupted: `-0.03340`  ·  n_sockets: `0.00870`  ·  quality: `0.03313`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.85322 |
| `explicit.stat_1202301673@T1` | 1.57793 |
| `crafted.stat_3035140377` | 1.40771 |
| `explicit.stat_2463230181@T2` | -0.92462 |
| `desecrated.stat_666077204@T1` | 0.87309 |
| `explicit.stat_1263695895@T1` | -0.85712 |
| `explicit.stat_1263695895@T2` | -0.81082 |
| `explicit.stat_1940865751@T1` | 0.71958 |
| `explicit.stat_3695891184@T2` | -0.70545 |
| `explicit.stat_518292764@T2` | -0.70177 |
| `explicit.stat_669069897@T1` | -0.66625 |
| `explicit.stat_3695891184@T1` | -0.66506 |

### weapon.crossbow — n=14454, R²=-1.831

intercept: `3.7450`  ·  log_price: True  ·  ilvl: `-0.04537`  ·  n_mods: `-0.04879`  ·  n_top_tier: `0.79210`  ·  corrupted: `0.03240`  ·  n_sockets: `0.05498`  ·  quality: `0.00947`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.94958 |
| `explicit.stat_2250681686@T2` | -1.43626 |
| `explicit.stat_709508406@T1` | 1.23942 |
| `explicit.stat_1202301673@T1` | 1.21871 |
| `explicit.stat_1980802737` | 1.15265 |
| `explicit.stat_1263695895@T2` | -1.00534 |
| `explicit.stat_1263695895@T1` | -0.98903 |
| `explicit.stat_2694482655@T1` | -0.94418 |
| `explicit.stat_210067635@T2` | -0.94282 |
| `explicit.stat_1509134228@T2` | -0.91358 |
| `explicit.stat_210067635@T1` | -0.89571 |
| `explicit.stat_3695891184@T1` | -0.88765 |

### flask.charm — n=13842, R²=-0.5551

intercept: `0.0143`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.68141`  ·  corrupted: `1.99439`  ·  quality: `0.00005`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.47391 |
| `explicit.stat_1056492907` | 3.16992 |
| `explicit.stat_828533480@T2` | -2.68143 |
| `explicit.stat_1120862500@T2` | -2.68141 |
| `explicit.stat_828533480@T1` | -2.68141 |
| `explicit.stat_2676834156@T2` | -2.68140 |
| `explicit.stat_3196823591@T2` | -2.68140 |
| `explicit.stat_2541588185@T2` | -2.68140 |
| `explicit.stat_1873752457@T2` | -2.68140 |
| `explicit.stat_388617051@T2` | -2.68139 |
| `explicit.stat_2365392475@T2` | -2.68138 |
| `explicit.stat_1873752457@T1` | -2.68137 |

### weapon.warstaff — n=9043, R²=-0.4282

intercept: `-8.7934`  ·  log_price: True  ·  ilvl: `0.11875`  ·  n_mods: `-0.17728`  ·  n_top_tier: `0.48716`  ·  corrupted: `0.24040`  ·  n_sockets: `0.13904`  ·  quality: `0.05923`

| stat_id | coef |
|---|---|
| `explicit.stat_328541901@T1` | -1.03339 |
| `rune.stat_243313994` | 1.02580 |
| `explicit.stat_1037193709@T1` | 1.00947 |
| `explicit.stat_328541901@T2` | -0.80764 |
| `crafted.stat_210067635@T2` | 0.80707 |
| `desecrated.stat_2231156303@T1` | 0.69145 |
| `desecrated.stat_2527686725@T1` | 0.69145 |
| `desecrated.stat_9187492` | 0.68461 |
| `explicit.stat_1037193709@T2` | -0.66297 |
| `explicit.stat_9187492@T1` | 0.63249 |
| `explicit.stat_55876295@T2` | -0.54100 |
| `explicit.stat_518292764@T1` | -0.53452 |

### weapon.staff — n=8454, R²=-0.4327

intercept: `-12.4628`  ·  log_price: True  ·  ilvl: `0.16197`  ·  n_mods: `-0.12172`  ·  n_top_tier: `0.49986`  ·  corrupted: `0.43413`  ·  n_sockets: `0.21908`  ·  quality: `0.04132`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.92199 |
| `explicit.stat_591105508@T1` | 1.28880 |
| `explicit.stat_4226189338@T1` | 1.27920 |
| `explicit.stat_124131830@T2` | 1.18967 |
| `explicit.stat_124131830@T1` | 1.12480 |
| `explicit.stat_293638271@T2` | -1.02855 |
| `explicit.stat_4226189338@T2` | 0.92676 |
| `explicit.stat_3962278098@T2` | 0.89989 |
| `explicit.stat_1600707273@T1` | 0.79044 |
| `explicit.stat_2768835289@T2` | 0.76970 |
| `explicit.stat_1263695895@T2` | -0.68779 |
| `explicit.stat_2505884597@T2` | -0.66500 |

### weapon.sceptre — n=8371, R²=-0.368

intercept: `-18.2585`  ·  log_price: True  ·  ilvl: `0.23224`  ·  n_mods: `-0.02864`  ·  n_top_tier: `0.23615`  ·  corrupted: `0.60036`  ·  n_sockets: `0.20714`  ·  quality: `0.04372`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.98797 |
| `explicit.stat_2162097452@T2` | 1.73245 |
| `explicit.stat_1250712710@T2` | 1.31381 |
| `explicit.stat_3057012405@T1` | 1.16281 |
| `explicit.stat_2347036682@T1` | 0.78639 |
| `explicit.stat_101878827@T1` | 0.68833 |
| `explicit.stat_2347036682@T2` | -0.67232 |
| `explicit.stat_1263695895@T1` | -0.66467 |
| `explicit.stat_1574590649@T1` | -0.63303 |
| `explicit.stat_1263695895@T2` | -0.52954 |
| `explicit.stat_328541901@T2` | 0.50766 |
| `explicit.stat_2854751904@T2` | -0.48052 |

### weapon.spear — n=6896, R²=-0.4872

intercept: `-9.1585`  ·  log_price: True  ·  ilvl: `0.12463`  ·  n_mods: `-0.07543`  ·  n_top_tier: `0.72036`  ·  corrupted: `0.00716`  ·  n_sockets: `0.23658`  ·  quality: `0.08899`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -2.81759 |
| `explicit.stat_1202301673@T1` | 2.15973 |
| `explicit.stat_9187492@T1` | 1.48587 |
| `explicit.stat_1509134228@T1` | 1.34773 |
| `explicit.stat_1263695895@T2` | -1.15130 |
| `explicit.stat_1037193709@T1` | -1.13430 |
| `crafted.stat_3035140377` | 1.01358 |
| `explicit.stat_691932474@T1` | -0.91744 |
| `explicit.stat_55876295@T1` | -0.90964 |
| `desecrated.stat_210067635@T1` | -0.79047 |
| `explicit.stat_1940865751@T2` | -0.77304 |
| `explicit.stat_3695891184@T2` | -0.70781 |

### armour.focus — n=5653, R²=-0.3943

intercept: `-12.5485`  ·  log_price: True  ·  ilvl: `0.16100`  ·  n_mods: `-0.16354`  ·  n_top_tier: `0.71653`  ·  corrupted: `0.68752`  ·  n_sockets: `0.46120`  ·  quality: `0.07518`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 4.79311 |
| `crafted.stat_737908626@T2` | 1.27522 |
| `explicit.stat_3962278098@T1` | -1.25897 |
| `explicit.stat_4220027924@T2` | -1.18651 |
| `explicit.stat_736967255@T2` | -0.97084 |
| `explicit.stat_2231156303@T1` | -0.91507 |
| `explicit.stat_2923486259@T1` | -0.90926 |
| `explicit.stat_3291658075@T1` | -0.89527 |
| `explicit.stat_2231156303@T2` | -0.87723 |
| `explicit.stat_737908626@T2` | -0.83801 |
| `explicit.stat_3962278098@T2` | -0.83078 |
| `explicit.stat_2339757871@T2` | -0.81548 |

### armour.quiver — n=5275, R²=-0.3661

intercept: `-12.8068`  ·  log_price: True  ·  ilvl: `0.15587`  ·  n_mods: `-0.10728`  ·  n_top_tier: `0.83444`  ·  corrupted: `0.50945`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.27724 |
| `explicit.stat_2463230181@T1` | 2.22011 |
| `explicit.stat_681332047@T2` | -1.28354 |
| `explicit.stat_2321178454@T2` | -1.21360 |
| `explicit.stat_4067062424@T1` | -1.21282 |
| `explicit.stat_1573130764@T1` | -1.06277 |
| `explicit.stat_803737631@T2` | -1.04808 |
| `explicit.stat_2463230181@T2` | 1.00356 |
| `explicit.stat_4067062424@T2` | -0.96011 |
| `explicit.stat_1573130764@T2` | -0.93314 |
| `explicit.stat_2321178454@T1` | -0.90935 |
| `explicit.stat_2194114101@T2` | -0.87170 |

### armour.shield — n=4610, R²=-0.5294

intercept: `-9.5749`  ·  log_price: True  ·  ilvl: `0.12512`  ·  n_mods: `-0.08448`  ·  n_top_tier: `0.51550`  ·  corrupted: `-0.30096`  ·  n_sockets: `0.14891`  ·  quality: `0.06493`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.60146 |
| `explicit.stat_2481353198@T2` | -1.00711 |
| `explicit.stat_2339757871@T1` | -0.96679 |
| `explicit.stat_3676141501@T1` | 0.94781 |
| `explicit.stat_1011760251@T1` | -0.92349 |
| `explicit.stat_3484657501@T2` | -0.91803 |
| `explicit.stat_1011760251@T2` | -0.91384 |
| `explicit.stat_3484657501@T1` | -0.90732 |
| `explicit.stat_3855016469@T1` | -0.87655 |
| `explicit.stat_2481353198@T1` | -0.87453 |
| `explicit.stat_2923486259@T2` | -0.82913 |
| `explicit.stat_3033371881@T2` | -0.81249 |

### weapon.twomace — n=4212, R²=-0.5198

intercept: `-9.6869`  ·  log_price: True  ·  ilvl: `0.12947`  ·  n_mods: `-0.17055`  ·  n_top_tier: `0.32155`  ·  corrupted: `0.10995`  ·  n_sockets: `0.11015`  ·  quality: `0.03833`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.32928 |
| `desecrated.stat_1509134228@T1` | 3.11445 |
| `explicit.stat_1037193709@T1` | -1.59125 |
| `explicit.stat_3336890334@T1` | -0.98830 |
| `crafted.stat_3035140377` | 0.86318 |
| `explicit.stat_387439868@T2` | -0.78310 |
| `explicit.stat_1037193709@T2` | -0.66644 |
| `explicit.stat_518292764@T2` | -0.60421 |
| `explicit.stat_3639275092@T1` | -0.59142 |
| `explicit.stat_9187492@T1` | -0.56204 |
| `explicit.stat_210067635@T2` | 0.51305 |
| `explicit.stat_518292764@T1` | 0.49828 |

## Coverage (listings per base)

- … **Sapphire** — 25187 listings (25143 priced) [0.3–7553463.8 ex]
- … **Emerald** — 24679 listings (24648 priced) [0.3–7553463.8 ex]
- … **Ruby** — 18939 listings (18919 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 9973 listings (9959 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8356 listings (8340 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8110 listings (8091 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8003 listings (7996 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 7597 listings (7583 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 7476 listings (7467 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 7457 listings (7439 priced) [0.2–91750808.2 ex]
- … **Sapphire Ring** — 6245 listings (6237 priced) [0.2–307202867.9 ex]
- … **Dueling Wand** — 6105 listings (6087 priced) [0.3–4297682211.9 ex]
- … **Topaz Ring** — 5976 listings (5971 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5931 listings (5925 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5341 listings (5319 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5294 listings (5289 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 5161 listings (5143 priced) [0.6–398912568423.8 ex]
- … **Amber Amulet** — 5156 listings (5150 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 5153 listings (5145 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 5128 listings (5115 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4990 listings (4982 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 4829 listings (4822 priced) [0.2–275252424.7 ex]
- … **Heavy Belt** — 4757 listings (4750 priced) [0.3–398912568423.8 ex]
- … **Azure Amulet** — 4709 listings (4708 priced) [0.3–123132003.2 ex]
- … **Lunar Amulet** — 4679 listings (4669 priced) [0.3–91750808.2 ex]

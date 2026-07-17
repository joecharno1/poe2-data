# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-17T06:04:05+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **571261** (569682 priced in exalted)
- Distinct bases: 987 · distinct mods: 3198 · mod rows: 2704369
- Sold signals: **25425** sold · 323060 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-17T05:56:10+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×26.02** (median |log error| 3.2589)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 80% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×71.04 · ±30% 5% · n=82906
- Premium segment (60ex+): skill **+0.12** · typical error ×348.77 · ±30% 0% · n=56134

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 11680 | ×55.15 | 22% | +0.03 | +0.05 |
| jewel | 11015 | ×10.85 | 4% | +0.06 | +0.10 |
| accessory.amulet | 10644 | ×49.30 | 20% | +0.03 | +0.04 |
| accessory.belt | 7966 | ×21.42 | 23% | +0.03 | +0.06 |
| armour.chest | 7731 | ×20.88 | 24% | +0.07 | +0.10 |
| armour.helmet | 7510 | ×29.51 | 22% | +0.05 | +0.07 |
| armour.boots | 7051 | ×37.21 | 20% | +0.08 | +0.11 |
| armour.gloves | 6852 | ×42.50 | 17% | +0.07 | +0.10 |
| other | 6503 | ×1.92 | 44% | +0.10 | +0.18 |
| weapon.wand | 4270 | ×45.78 | 16% | +0.08 | +0.09 |
| weapon.bow | 3362 | ×35.17 | 15% | +0.13 | +0.14 |
| weapon.crossbow | 3149 | ×35.91 | 17% | +0.09 | +0.12 |
| weapon.warstaff | 2026 | ×37.36 | 9% | +0.14 | +0.12 |
| weapon.staff | 1886 | ×52.06 | 7% | +0.11 | +0.11 |
| weapon.sceptre | 1877 | ×44.30 | 4% | +0.18 | +0.19 |
| weapon.spear | 1497 | ×44.26 | 14% | +0.08 | +0.09 |
| armour.focus | 1256 | ×25.34 | 6% | +0.15 | +0.18 |
| armour.quiver | 1198 | ×27.43 | 7% | +0.13 | +0.15 |
| flask.charm | 1012 | ×33.31 | 31% | +0.05 | +0.07 |
| armour.shield | 982 | ×21.30 | 8% | +0.04 | +0.06 |
| weapon.twomace | 895 | ×9.40 | 11% | +0.07 | +0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=59884, R²=-0.9423

intercept: `-1.8243`  ·  log_price: True  ·  ilvl: `0.02605`  ·  n_mods: `0.72678`  ·  n_top_tier: `-0.21615`  ·  corrupted: `0.33609`  ·  quality: `0.22649`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.23365 |
| `explicit.stat_2301718443@T1` | 2.65850 |
| `explicit.stat_1805182458@T1` | -2.24573 |
| `explicit.stat_3374165039@T1` | -2.23106 |
| `explicit.stat_3485067555@T1` | 1.81263 |
| `explicit.stat_686254215@T1` | -1.71691 |
| `explicit.stat_239367161@T1` | -1.53828 |
| `explicit.stat_491450213@T1` | 1.51939 |
| `explicit.stat_3166958180@T1` | -1.45391 |
| `explicit.stat_1315743832@T1` | -1.44258 |
| `explicit.stat_3780644166@T1` | -1.43087 |
| `explicit.stat_2523933828@T1` | -1.36862 |

### other — n=54840, R²=-0.6552

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.34680`  ·  corrupted: `0.24061`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2974417149@T1` | 0.36914 |
| `explicit.stat_3299347043@T1` | -0.31685 |
| `explicit.stat_3291658075@T1` | 0.25870 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_2106365538@T1` | -0.13371 |
| `explicit.stat_1050105434@T1` | -0.11603 |
| `explicit.stat_2482852589@T1` | -0.10565 |
| `implicit.stat_2923486259` | -0.09247 |
| `pseudo.total_chaos_res` | 0.09247 |
| `explicit.stat_789117908@T1` | -0.04112 |

### accessory.ring — n=53412, R²=-2.0256

intercept: `3.4385`  ·  log_price: True  ·  ilvl: `-0.04253`  ·  n_mods: `0.00006`  ·  n_top_tier: `1.05336`  ·  corrupted: `0.02367`  ·  n_sockets: `2.18821`  ·  quality: `0.07734`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -1.09216 |
| `explicit.stat_3299347043@T1` | -1.08021 |
| `explicit.stat_1573130764@T1` | -1.07890 |
| `explicit.stat_1368271171@T2` | -1.07598 |
| `explicit.stat_2231156303@T2` | -1.07554 |
| `explicit.stat_1263695895@T2` | -1.07366 |
| `explicit.stat_4220027924@T2` | -1.07345 |
| `explicit.stat_3325883026@T1` | -1.07321 |
| `explicit.stat_803737631@T1` | -1.07308 |
| `explicit.stat_4067062424@T2` | -1.07133 |
| `explicit.stat_2144192055@T1` | -1.07032 |
| `explicit.stat_3032590688@T2` | -1.06994 |

### accessory.amulet — n=48906, R²=-2.1562

intercept: `3.6183`  ·  log_price: True  ·  ilvl: `-0.04424`  ·  n_mods: `-0.02652`  ·  n_top_tier: `0.99945`  ·  corrupted: `0.07995`  ·  n_sockets: `-0.11541`  ·  quality: `-0.00117`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.13318 |
| `explicit.stat_2974417149@T1` | -1.08842 |
| `explicit.stat_587431675@T2` | -1.08280 |
| `explicit.stat_472520716@T2` | -1.07398 |
| `explicit.stat_803737631@T1` | -1.06445 |
| `explicit.stat_2974417149@T2` | -1.06261 |
| `explicit.stat_1050105434@T2` | -1.04902 |
| `explicit.stat_3299347043@T2` | -1.04797 |
| `explicit.stat_803737631@T2` | -1.04360 |
| `explicit.stat_2866361420@T2` | -1.04268 |
| `explicit.stat_472520716@T1` | -1.02978 |
| `explicit.stat_2866361420@T1` | -1.02917 |

### accessory.belt — n=36605, R²=-1.8117

intercept: `2.9829`  ·  log_price: True  ·  ilvl: `-0.03599`  ·  n_mods: `-0.01836`  ·  n_top_tier: `0.91670`  ·  corrupted: `0.86591`  ·  n_sockets: `0.76292`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -0.95695 |
| `explicit.stat_2881298780@T1` | -0.94633 |
| `explicit.stat_4220027924@T2` | -0.94287 |
| `explicit.stat_3299347043@T2` | -0.93728 |
| `explicit.stat_809229260@T2` | -0.93517 |
| `explicit.stat_1389754388@T1` | -0.93446 |
| `explicit.stat_3325883026@T1` | -0.92451 |
| `explicit.stat_51994685@T1` | -0.92386 |
| `explicit.stat_1671376347@T2` | -0.92263 |
| `explicit.stat_3372524247@T2` | -0.92257 |
| `explicit.stat_915769802@T1` | -0.92236 |
| `explicit.stat_915769802@T2` | -0.91873 |

### armour.chest — n=36398, R²=-1.7483

intercept: `3.3359`  ·  log_price: True  ·  ilvl: `-0.04099`  ·  n_mods: `-0.01552`  ·  n_top_tier: `0.48008`  ·  corrupted: `0.04707`  ·  n_sockets: `0.02358`  ·  quality: `0.06051`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.58480 |
| `explicit.stat_3981240776@T1` | 1.05050 |
| `explicit.stat_986397080@T2` | -0.53266 |
| `explicit.stat_4080418644@T2` | -0.51763 |
| `explicit.stat_1692879867@T1` | -0.51318 |
| `explicit.stat_915769802@T2` | -0.51106 |
| `explicit.stat_4080418644@T1` | -0.50833 |
| `explicit.stat_3372524247@T2` | -0.50404 |
| `explicit.stat_986397080@T1` | -0.50371 |
| `explicit.stat_2451402625@T2` | -0.50335 |
| `explicit.stat_4015621042@T1` | -0.50098 |
| `explicit.stat_915769802@T1` | -0.49786 |

### armour.helmet — n=35328, R²=-1.796

intercept: `3.4667`  ·  log_price: True  ·  ilvl: `-0.04333`  ·  n_mods: `-0.01997`  ·  n_top_tier: `0.36317`  ·  corrupted: `0.78111`  ·  n_sockets: `0.03620`  ·  quality: `0.05104`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.93919 |
| `explicit.stat_1263695895@T1` | -0.58776 |
| `explicit.stat_3917489142@T2` | -0.49921 |
| `explicit.stat_1263695895@T2` | -0.49337 |
| `explicit.stat_2162097452@T2` | -0.47558 |
| `explicit.stat_4052037485@T2` | -0.44554 |
| `explicit.stat_3917489142@T1` | -0.42625 |
| `explicit.stat_1999113824@T1` | -0.40198 |
| `explicit.stat_3321629045@T2` | -0.40190 |
| `explicit.stat_3484657501@T1` | -0.38752 |
| `explicit.stat_1050105434@T1` | -0.38131 |
| `explicit.stat_803737631@T2` | -0.37722 |

### armour.boots — n=33084, R²=-1.7364

intercept: `3.4774`  ·  log_price: True  ·  ilvl: `-0.04254`  ·  n_mods: `-0.01952`  ·  n_top_tier: `0.67219`  ·  corrupted: `0.01107`  ·  n_sockets: `0.02699`  ·  quality: `0.04776`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.37336 |
| `explicit.stat_2250533757@T1` | 1.39308 |
| `explicit.stat_2339757871@T1` | -1.04999 |
| `explicit.stat_3299347043@T1` | -0.87044 |
| `explicit.stat_3917489142@T2` | -0.83259 |
| `explicit.stat_3917489142@T1` | -0.74218 |
| `explicit.stat_2160282525@T1` | -0.72355 |
| `explicit.stat_2923486259@T2` | -0.70688 |
| `explicit.stat_1671376347@T2` | -0.70298 |
| `explicit.stat_3299347043@T2` | -0.70087 |
| `explicit.stat_3484657501@T2` | -0.69894 |
| `explicit.stat_1999113824@T2` | -0.69085 |

### armour.gloves — n=32133, R²=-1.7895

intercept: `3.6412`  ·  log_price: True  ·  ilvl: `-0.04563`  ·  n_mods: `-0.01541`  ·  n_top_tier: `0.60805`  ·  corrupted: `0.03769`  ·  n_sockets: `0.04990`  ·  quality: `0.04436`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 1.08675 |
| `explicit.stat_9187492@T2` | -0.87712 |
| `explicit.stat_2923486259@T1` | -0.86867 |
| `explicit.stat_9187492@T1` | 0.83914 |
| `explicit.stat_3484657501@T2` | -0.74449 |
| `explicit.stat_1671376347@T1` | 0.74124 |
| `explicit.stat_3321629045@T2` | -0.72287 |
| `explicit.stat_4052037485@T1` | -0.70561 |
| `explicit.stat_803737631@T2` | -0.68568 |
| `explicit.stat_3484657501@T1` | -0.66647 |
| `explicit.stat_124859000@T2` | -0.66644 |
| `explicit.stat_1999113824@T2` | -0.66297 |

### weapon.wand — n=20006, R²=-2.1367

intercept: `3.7429`  ·  log_price: True  ·  ilvl: `-0.04621`  ·  n_mods: `-0.03776`  ·  n_top_tier: `0.56059`  ·  corrupted: `0.04204`  ·  n_sockets: `0.07470`  ·  quality: `0.01497`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.50609 |
| `explicit.stat_2254480358@T1` | 2.40438 |
| `rune.stat_124131830` | -2.39516 |
| `explicit.stat_4226189338@T1` | 2.05733 |
| `explicit.stat_124131830@T1` | 1.77068 |
| `explicit.stat_591105508@T1` | 1.75773 |
| `explicit.stat_736967255@T2` | 1.57899 |
| `crafted.stat_124131830` | 1.21325 |
| `explicit.stat_1600707273@T1` | 1.12070 |
| `explicit.stat_4226189338@T2` | 0.87879 |
| `explicit.stat_1600707273@T2` | -0.83620 |
| `explicit.stat_1263695895@T1` | -0.80559 |

### weapon.bow — n=16020, R²=-1.884

intercept: `3.6940`  ·  log_price: True  ·  ilvl: `-0.04350`  ·  n_mods: `-0.07317`  ·  n_top_tier: `0.61610`  ·  corrupted: `0.24258`  ·  n_sockets: `0.03241`  ·  quality: `0.03637`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.31264 |
| `desecrated.stat_210067635@T1` | -1.53387 |
| `crafted.stat_3035140377` | 1.45162 |
| `explicit.stat_1202301673@T1` | 1.36844 |
| `explicit.stat_2463230181@T1` | -1.25053 |
| `explicit.stat_2463230181@T2` | -1.14827 |
| `explicit.stat_1263695895@T1` | -1.00875 |
| `explicit.stat_1263695895@T2` | -0.96986 |
| `explicit.stat_518292764@T2` | -0.95972 |
| `explicit.stat_3336890334@T1` | 0.94497 |
| `explicit.stat_1940865751@T1` | 0.75298 |
| `explicit.stat_3695891184@T2` | -0.75181 |

### flask.charm — n=15138, R²=-0.5757

intercept: `0.0634`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `2.34710`  ·  corrupted: `1.85775`  ·  quality: `0.00023`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60988 |
| `explicit.stat_1056492907` | 2.93588 |
| `explicit.stat_828533480@T2` | -2.34712 |
| `explicit.stat_1873752457@T2` | -2.34709 |
| `explicit.stat_2676834156@T2` | -2.34708 |
| `explicit.stat_388617051@T2` | -2.34708 |
| `explicit.stat_1120862500@T2` | -2.34708 |
| `explicit.stat_3196823591@T2` | -2.34708 |
| `explicit.stat_828533480@T1` | -2.34707 |
| `explicit.stat_2365392475@T2` | -2.34707 |
| `explicit.stat_1873752457@T1` | -2.34707 |
| `explicit.stat_1366840608@T2` | -2.34673 |

### weapon.crossbow — n=15036, R²=-1.886

intercept: `3.8464`  ·  log_price: True  ·  ilvl: `-0.04693`  ·  n_mods: `-0.04504`  ·  n_top_tier: `0.70824`  ·  corrupted: `0.02288`  ·  n_sockets: `0.04787`  ·  quality: `0.02174`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.86785 |
| `explicit.stat_2250681686@T2` | -1.43140 |
| `explicit.stat_1202301673@T1` | 1.36484 |
| `explicit.stat_1980802737` | 1.19757 |
| `explicit.stat_709508406@T1` | 0.86086 |
| `explicit.stat_2250681686` | 0.86050 |
| `explicit.stat_2694482655@T1` | -0.83561 |
| `explicit.stat_1263695895@T2` | -0.83178 |
| `explicit.stat_1509134228@T2` | -0.82422 |
| `explicit.stat_1263695895@T1` | -0.81404 |
| `crafted.stat_3035140377` | 0.80368 |
| `explicit.stat_709508406@T2` | -0.78869 |

### weapon.warstaff — n=9656, R²=-0.3758

intercept: `-9.7379`  ·  log_price: True  ·  ilvl: `0.13342`  ·  n_mods: `-0.21273`  ·  n_top_tier: `0.31229`  ·  corrupted: `0.18639`  ·  n_sockets: `0.19630`  ·  quality: `0.06154`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 1.15750 |
| `desecrated.stat_2231156303@T1` | 1.15750 |
| `crafted.stat_210067635@T2` | 1.12617 |
| `explicit.stat_1037193709@T1` | 1.10549 |
| `rune.stat_243313994` | 0.85807 |
| `explicit.stat_328541901@T1` | -0.84271 |
| `explicit.stat_328541901@T2` | -0.83859 |
| `desecrated.stat_9187492` | 0.74721 |
| `explicit.stat_9187492@T1` | 0.73310 |
| `explicit.stat_1509134228@T1` | 0.64751 |
| `explicit.stat_748522257@T2` | 0.53620 |
| `crafted.stat_3035140377` | 0.45180 |

### weapon.staff — n=9054, R²=-0.4009

intercept: `-13.9489`  ·  log_price: True  ·  ilvl: `0.18204`  ·  n_mods: `-0.15781`  ·  n_top_tier: `0.47059`  ·  corrupted: `0.42606`  ·  n_sockets: `0.27670`  ·  quality: `0.04078`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.94974 |
| `explicit.stat_4226189338@T1` | 1.78176 |
| `explicit.stat_591105508@T1` | 1.22426 |
| `explicit.stat_293638271@T2` | -1.07925 |
| `explicit.stat_124131830@T1` | 1.04308 |
| `explicit.stat_124131830@T2` | 0.81435 |
| `explicit.stat_2254480358@T2` | 0.81070 |
| `explicit.stat_2505884597@T2` | -0.74897 |
| `explicit.stat_2254480358@T1` | 0.71345 |
| `explicit.stat_4226189338@T2` | 0.71195 |
| `explicit.stat_3962278098@T2` | 0.67001 |
| `rune.stat_124131830` | 0.66594 |

### weapon.sceptre — n=8936, R²=-0.3515

intercept: `-18.3821`  ·  log_price: True  ·  ilvl: `0.23560`  ·  n_mods: `-0.09250`  ·  n_top_tier: `0.28211`  ·  corrupted: `0.40933`  ·  n_sockets: `0.28920`  ·  quality: `0.03938`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.79327 |
| `explicit.stat_2162097452@T2` | 1.64579 |
| `explicit.stat_1250712710@T2` | 1.30036 |
| `explicit.stat_3057012405@T1` | 1.06679 |
| `explicit.stat_1263695895@T1` | -0.86935 |
| `explicit.stat_1263695895@T2` | -0.81472 |
| `explicit.stat_1574590649@T1` | -0.68474 |
| `explicit.stat_101878827@T1` | 0.66589 |
| `explicit.stat_2347036682@T2` | -0.63517 |
| `explicit.stat_2347036682@T1` | 0.63358 |
| `explicit.stat_849987426@T1` | 0.62045 |
| `explicit.stat_1574590649@T2` | -0.46356 |

### weapon.spear — n=7312, R²=-0.4344

intercept: `-11.3164`  ·  log_price: True  ·  ilvl: `0.15966`  ·  n_mods: `-0.15651`  ·  n_top_tier: `0.81580`  ·  corrupted: `-0.37468`  ·  n_sockets: `0.27029`  ·  quality: `0.05819`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.11313 |
| `explicit.stat_1509134228@T1` | 1.75477 |
| `explicit.stat_1202301673@T1` | 1.51386 |
| `crafted.stat_3035140377` | 1.14150 |
| `explicit.stat_9187492@T1` | 1.11375 |
| `explicit.stat_1037193709@T1` | -1.08951 |
| `explicit.stat_4080418644@T2` | -1.00884 |
| `explicit.stat_691932474@T1` | -0.98675 |
| `explicit.stat_9187492@T2` | -0.89730 |
| `explicit.stat_3261801346@T1` | -0.89707 |
| `explicit.stat_1940865751@T2` | -0.85427 |
| `explicit.stat_1263695895@T2` | -0.80938 |

### armour.focus — n=5999, R²=-0.3714

intercept: `-11.9775`  ·  log_price: True  ·  ilvl: `0.15812`  ·  n_mods: `-0.16943`  ·  n_top_tier: `0.79984`  ·  corrupted: `0.51481`  ·  n_sockets: `0.43056`  ·  quality: `0.06969`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 8.53499 |
| `explicit.stat_4220027924@T2` | -1.34500 |
| `explicit.stat_3962278098@T1` | -1.10962 |
| `explicit.stat_3291658075@T1` | -0.94146 |
| `explicit.stat_2891184298@T2` | -0.90764 |
| `explicit.stat_2339757871@T2` | -0.90052 |
| `explicit.stat_2231156303@T2` | -0.89329 |
| `explicit.stat_4052037485@T2` | -0.84080 |
| `explicit.stat_2974417149@T2` | -0.83502 |
| `explicit.stat_737908626@T2` | -0.81786 |
| `explicit.stat_2974417149@T1` | -0.80927 |
| `explicit.stat_4220027924@T1` | -0.76948 |

### armour.quiver — n=5624, R²=-0.3166

intercept: `-14.2784`  ·  log_price: True  ·  ilvl: `0.17704`  ·  n_mods: `-0.13813`  ·  n_top_tier: `0.83248`  ·  corrupted: `0.82020`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.27022 |
| `explicit.stat_2463230181@T1` | 3.22495 |
| `explicit.stat_2463230181@T2` | 1.57486 |
| `explicit.stat_681332047@T2` | -1.41508 |
| `explicit.stat_1573130764@T1` | -1.14327 |
| `explicit.stat_2321178454@T2` | -1.10366 |
| `explicit.stat_803737631@T2` | -1.06185 |
| `explicit.stat_4067062424@T1` | -0.99234 |
| `explicit.stat_1573130764@T2` | -0.93311 |
| `explicit.stat_2321178454@T1` | -0.92301 |
| `explicit.stat_681332047@T1` | -0.90047 |
| `explicit.stat_803737631@T1` | -0.86998 |

### armour.shield — n=4883, R²=-0.4947

intercept: `-10.4562`  ·  log_price: True  ·  ilvl: `0.14084`  ·  n_mods: `-0.12025`  ·  n_top_tier: `0.70189`  ·  corrupted: `-0.26096`  ·  n_sockets: `0.27459`  ·  quality: `0.06518`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.40991 |
| `explicit.stat_328541901@T1` | -1.25459 |
| `explicit.stat_2339757871@T1` | -1.20870 |
| `explicit.stat_2481353198@T2` | -1.14936 |
| `explicit.stat_328541901@T2` | -1.09285 |
| `explicit.stat_3484657501@T2` | -1.08555 |
| `explicit.stat_3321629045@T2` | -1.06491 |
| `explicit.stat_3033371881@T2` | -1.05715 |
| `explicit.stat_2901986750@T1` | -0.99592 |
| `explicit.stat_4095671657@T1` | -0.97314 |
| `explicit.stat_2923486259@T1` | -0.94905 |
| `explicit.stat_2451402625@T1` | -0.92241 |

### weapon.twomace — n=4480, R²=-0.4921

intercept: `-9.4801`  ·  log_price: True  ·  ilvl: `0.13124`  ·  n_mods: `-0.18944`  ·  n_top_tier: `0.38665`  ·  corrupted: `-0.05320`  ·  n_sockets: `0.15632`  ·  quality: `0.05648`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.69619 |
| `desecrated.stat_1509134228@T1` | 2.62250 |
| `explicit.stat_1037193709@T1` | -1.56467 |
| `crafted.stat_3035140377` | 0.95196 |
| `explicit.stat_387439868@T2` | -0.90000 |
| `explicit.stat_1037193709@T2` | -0.78368 |
| `explicit.stat_9187492@T1` | -0.74659 |
| `explicit.stat_1263695895@T2` | -0.70691 |
| `explicit.stat_691932474@T1` | -0.69785 |
| `explicit.stat_210067635@T1` | 0.62178 |
| `explicit.stat_3336890334@T1` | -0.58444 |
| `explicit.stat_669069897@T2` | -0.49839 |

## Coverage (listings per base)

- … **Sapphire** — 27784 listings (27736 priced) [0.3–885594757.8 ex]
- … **Emerald** — 27242 listings (27203 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 20831 listings (20807 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10549 listings (10534 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 9107 listings (9089 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8806 listings (8787 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8705 listings (8697 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8266 listings (8250 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8120 listings (8102 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8047 listings (8036 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6764 listings (6754 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6495 listings (6489 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6457 listings (6451 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6410 listings (6391 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 5726 listings (5719 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 5714 listings (5691 priced) [0.3–398912568423.8 ex]
- … **Jade Amulet** — 5607 listings (5596 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 5586 listings (5569 priced) [0.2–24532814.5 ex]
- … **Amber Amulet** — 5576 listings (5569 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5514 listings (5493 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5410 listings (5401 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5305 listings (5298 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5104 listings (5102 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5077 listings (5065 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5075 listings (5067 priced) [0.3–398912568423.8 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-18T04:41:34+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **605396** (603587 priced in exalted)
- Distinct bases: 990 · distinct mods: 3231 · mod rows: 2867684
- Sold signals: **25083** sold · 343890 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-18T04:29:23+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×25.52** (median |log error| 3.2394)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×69.17 · ±30% 5% · n=88187
- Premium segment (60ex+): skill **+0.13** · typical error ×326.26 · ±30% 0% · n=59933

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 12564 | ×56.19 | 21% | +0.02 | +0.04 |
| jewel | 11810 | ×11.14 | 4% | +0.08 | +0.11 |
| accessory.amulet | 11494 | ×50.59 | 20% | +0.04 | +0.03 |
| accessory.belt | 8375 | ×24.98 | 10% | +0.10 | +0.12 |
| armour.chest | 8168 | ×19.08 | 22% | +0.08 | +0.10 |
| armour.helmet | 7978 | ×23.42 | 16% | +0.08 | +0.10 |
| armour.boots | 7410 | ×35.76 | 22% | +0.08 | +0.10 |
| armour.gloves | 7266 | ×40.33 | 16% | +0.07 | +0.10 |
| other | 7057 | ×2.00 | 43% | +0.10 | +0.17 |
| weapon.wand | 4391 | ×55.87 | 19% | +0.07 | +0.09 |
| weapon.bow | 3479 | ×35.09 | 15% | +0.11 | +0.13 |
| weapon.crossbow | 3249 | ×35.19 | 17% | +0.09 | +0.14 |
| weapon.warstaff | 2174 | ×32.65 | 7% | +0.17 | +0.15 |
| weapon.staff | 2013 | ×48.75 | 5% | +0.14 | +0.13 |
| weapon.sceptre | 1933 | ×33.23 | 5% | +0.20 | +0.20 |
| weapon.spear | 1580 | ×38.83 | 11% | +0.09 | +0.10 |
| armour.focus | 1327 | ×22.96 | 6% | +0.16 | +0.18 |
| armour.quiver | 1266 | ×27.32 | 6% | +0.15 | +0.14 |
| flask.charm | 1087 | ×17.09 | 32% | +0.01 | +0.04 |
| armour.shield | 1041 | ×24.93 | 7% | +0.06 | +0.08 |
| weapon.twomace | 949 | ×12.15 | 10% | +0.09 | +0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=64323, R²=-0.949

intercept: `-1.9186`  ·  log_price: True  ·  ilvl: `0.02611`  ·  n_mods: `0.90099`  ·  n_top_tier: `-0.36793`  ·  corrupted: `0.26789`  ·  quality: `0.22708`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.65808 |
| `explicit.stat_3374165039@T1` | -2.12322 |
| `explicit.stat_3485067555@T1` | 1.79422 |
| `explicit.stat_318953428@T1` | -1.77632 |
| `explicit.stat_2301718443@T1` | 1.61886 |
| `explicit.stat_1805182458@T1` | -1.56590 |
| `explicit.stat_2523933828@T1` | -1.41112 |
| `explicit.stat_3166958180@T1` | -1.37914 |
| `explicit.stat_4147897060@T1` | -1.37341 |
| `explicit.stat_1869147066@T1` | -1.36138 |
| `explicit.stat_3091578504@T1` | -1.35429 |
| `explicit.stat_239367161@T1` | -1.35264 |

### other — n=57972, R²=-0.5717

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.43588`  ·  corrupted: `0.25735`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | 1.28653 |
| `explicit.stat_1050105434@T1` | -0.42213 |
| `explicit.stat_2106365538@T1` | -0.40278 |
| `explicit.stat_3141070085@T1` | -0.39220 |
| `explicit.stat_3291658075@T1` | 0.24318 |
| `explicit.stat_789117908@T1` | -0.23662 |
| `explicit.stat_3917489142@T1` | -0.23170 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_2974417149@T1` | 0.18438 |
| `explicit.stat_2482852589@T1` | -0.15182 |

### accessory.ring — n=57477, R²=-2.0465

intercept: `3.3331`  ·  log_price: True  ·  ilvl: `-0.04116`  ·  n_mods: `0.00041`  ·  n_top_tier: `1.04788`  ·  corrupted: `0.01761`  ·  n_sockets: `-0.08060`  ·  quality: `0.01841`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.09299 |
| `explicit.stat_1573130764@T2` | -1.08421 |
| `explicit.stat_2231156303@T1` | -1.08018 |
| `explicit.stat_4220027924@T2` | -1.06735 |
| `explicit.stat_803737631@T1` | -1.06433 |
| `explicit.stat_789117908@T1` | -1.06350 |
| `explicit.stat_789117908@T2` | -1.06291 |
| `explicit.stat_4080418644@T1` | -1.06247 |
| `explicit.stat_2144192055@T1` | -1.06216 |
| `explicit.stat_2231156303@T2` | -1.06055 |
| `explicit.stat_1368271171@T2` | -1.06033 |
| `explicit.stat_3032590688@T2` | -1.05961 |

### accessory.amulet — n=52316, R²=-2.1559

intercept: `3.8124`  ·  log_price: True  ·  ilvl: `-0.04632`  ·  n_mods: `-0.02236`  ·  n_top_tier: `1.18178`  ·  corrupted: `0.04241`  ·  n_sockets: `-0.14012`  ·  quality: `0.00156`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.55956 |
| `explicit.stat_3299347043@T2` | -1.35511 |
| `explicit.stat_2974417149@T2` | -1.24766 |
| `explicit.stat_2974417149@T1` | -1.24465 |
| `explicit.stat_2866361420@T2` | -1.24181 |
| `explicit.stat_803737631@T1` | -1.23431 |
| `explicit.stat_472520716@T2` | -1.23251 |
| `explicit.stat_587431675@T2` | -1.22823 |
| `explicit.stat_2866361420@T1` | -1.22516 |
| `explicit.stat_1050105434@T2` | -1.22256 |
| `explicit.stat_803737631@T2` | -1.21922 |
| `explicit.stat_1671376347@T2` | -1.21277 |

### accessory.belt — n=38721, R²=-1.2543

intercept: `5.5379`  ·  log_price: True  ·  ilvl: `-0.06183`  ·  n_mods: `-0.11204`  ·  n_top_tier: `0.75545`  ·  corrupted: `1.21620`  ·  n_sockets: `0.20081`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.69645 |
| `explicit.stat_3299347043@T2` | -1.08363 |
| `explicit.stat_2881298780@T1` | -0.94454 |
| `explicit.stat_4220027924@T2` | -0.89769 |
| `explicit.stat_51994685@T1` | -0.83632 |
| `explicit.stat_644456512@T1` | -0.83118 |
| `explicit.stat_809229260@T2` | -0.78998 |
| `explicit.stat_1389754388@T1` | -0.78608 |
| `explicit.stat_3372524247@T2` | -0.77048 |
| `explicit.stat_3325883026@T1` | -0.76276 |
| `explicit.stat_1570770415@T2` | -0.75433 |
| `explicit.stat_1570770415@T1` | -0.75088 |

### armour.chest — n=38404, R²=-1.7201

intercept: `3.3561`  ·  log_price: True  ·  ilvl: `-0.04123`  ·  n_mods: `-0.02148`  ·  n_top_tier: `0.52413`  ·  corrupted: `0.25105`  ·  n_sockets: `0.02638`  ·  quality: `0.05850`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.65572 |
| `explicit.stat_3981240776@T1` | 1.01776 |
| `explicit.stat_986397080@T2` | -0.60596 |
| `explicit.stat_986397080@T1` | -0.57018 |
| `explicit.stat_3484657501@T1` | -0.56492 |
| `explicit.stat_915769802@T2` | -0.56240 |
| `explicit.stat_3299347043@T2` | -0.55392 |
| `explicit.stat_1692879867@T1` | -0.55181 |
| `explicit.stat_915769802@T1` | -0.55166 |
| `explicit.stat_1692879867@T2` | -0.55116 |
| `explicit.stat_124859000@T1` | -0.54682 |
| `explicit.stat_4080418644@T2` | -0.54387 |

### armour.helmet — n=37299, R²=-1.5984

intercept: `3.4272`  ·  log_price: True  ·  ilvl: `-0.04328`  ·  n_mods: `-0.03011`  ·  n_top_tier: `0.42249`  ·  corrupted: `0.75990`  ·  n_sockets: `0.08223`  ·  quality: `0.05311`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.06078 |
| `crafted.stat_3917489142@T1` | -1.33835 |
| `explicit.stat_3917489142@T2` | -0.81722 |
| `explicit.stat_3917489142@T1` | -0.71112 |
| `explicit.stat_1263695895@T1` | -0.66375 |
| `explicit.stat_2162097452@T2` | -0.60462 |
| `explicit.stat_4052037485@T2` | -0.55749 |
| `explicit.stat_2162097452@T1` | 0.55521 |
| `explicit.stat_1263695895@T2` | -0.53183 |
| `explicit.stat_1999113824@T1` | -0.52455 |
| `explicit.stat_803737631@T2` | -0.49277 |
| `explicit.stat_53045048@T1` | -0.48288 |

### armour.boots — n=34707, R²=-1.768

intercept: `3.2856`  ·  log_price: True  ·  ilvl: `-0.04042`  ·  n_mods: `-0.01580`  ·  n_top_tier: `0.68809`  ·  corrupted: `0.00434`  ·  n_sockets: `0.02097`  ·  quality: `0.05643`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.43799 |
| `crafted.stat_3917489142@T1` | 1.19861 |
| `explicit.stat_2339757871@T1` | -0.89709 |
| `explicit.stat_3917489142@T2` | -0.86667 |
| `explicit.stat_3299347043@T1` | -0.81662 |
| `explicit.stat_3917489142@T1` | -0.79072 |
| `explicit.stat_1062208444@T2` | -0.72368 |
| `explicit.stat_2923486259@T2` | -0.72355 |
| `explicit.stat_2160282525@T1` | -0.71985 |
| `explicit.stat_1874553720@T1` | -0.71672 |
| `explicit.stat_3299347043@T2` | -0.71353 |
| `explicit.stat_4052037485@T2` | -0.71083 |

### armour.gloves — n=33888, R²=-1.7818

intercept: `3.7087`  ·  log_price: True  ·  ilvl: `-0.04702`  ·  n_mods: `-0.02071`  ·  n_top_tier: `0.58007`  ·  corrupted: `-0.03008`  ·  n_sockets: `0.08342`  ·  quality: `0.04821`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | 1.76480 |
| `explicit.stat_2339757871@T1` | 1.59870 |
| `rune.stat_836936635` | 1.19484 |
| `explicit.stat_2923486259@T1` | -1.02242 |
| `explicit.stat_1671376347@T1` | 0.94988 |
| `explicit.stat_9187492@T2` | -0.84707 |
| `explicit.stat_9187492@T1` | 0.84546 |
| `explicit.stat_3484657501@T2` | -0.79609 |
| `explicit.stat_2923486259@T2` | -0.77766 |
| `explicit.stat_3321629045@T2` | -0.76228 |
| `explicit.stat_3484657501@T1` | -0.73513 |
| `explicit.stat_3917489142@T2` | -0.67152 |

### weapon.wand — n=20695, R²=-2.2229

intercept: `3.6902`  ·  log_price: True  ·  ilvl: `-0.04556`  ·  n_mods: `-0.02715`  ·  n_top_tier: `0.48646`  ·  corrupted: `0.05870`  ·  n_sockets: `0.05182`  ·  quality: `0.00648`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.07285 |
| `rune.stat_124131830` | -2.74242 |
| `explicit.stat_2254480358@T1` | 2.48310 |
| `explicit.stat_4226189338@T1` | 2.33905 |
| `explicit.stat_124131830@T1` | 1.87142 |
| `explicit.stat_591105508@T1` | 1.85642 |
| `explicit.stat_736967255@T2` | 1.69080 |
| `crafted.stat_124131830` | 1.30096 |
| `explicit.stat_2254480358@T2` | 0.86700 |
| `explicit.stat_4226189338@T2` | 0.73975 |
| `explicit.stat_1263695895@T1` | -0.72918 |
| `explicit.stat_1263695895@T2` | -0.72596 |

### weapon.bow — n=16579, R²=-2.0187

intercept: `3.6609`  ·  log_price: True  ·  ilvl: `-0.04326`  ·  n_mods: `-0.06268`  ·  n_top_tier: `0.66739`  ·  corrupted: `0.12062`  ·  n_sockets: `0.02496`  ·  quality: `0.03238`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.54626 |
| `explicit.stat_1202301673@T1` | 1.38634 |
| `desecrated.stat_210067635@T1` | -1.18960 |
| `desecrated.stat_666077204@T1` | -1.16459 |
| `explicit.stat_1263695895@T1` | -1.00870 |
| `explicit.stat_1263695895@T2` | -0.93323 |
| `explicit.stat_3695891184@T2` | -0.77365 |
| `explicit.stat_3695891184@T1` | -0.75348 |
| `explicit.stat_2463230181@T2` | -0.74055 |
| `explicit.stat_518292764@T2` | -0.73345 |
| `explicit.stat_2463230181@T1` | -0.73233 |
| `explicit.stat_1037193709@T1` | -0.73146 |

### flask.charm — n=16302, R²=-0.5888

intercept: `0.0775`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.83406`  ·  corrupted: `1.60789`  ·  quality: `0.00022`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.85942 |
| `explicit.stat_1056492907` | 3.00836 |
| `explicit.stat_828533480@T2` | -1.83409 |
| `explicit.stat_1873752457@T2` | -1.83405 |
| `explicit.stat_1120862500@T2` | -1.83405 |
| `explicit.stat_1873752457@T1` | -1.83403 |
| `explicit.stat_388617051@T2` | -1.83403 |
| `explicit.stat_2676834156@T2` | -1.83403 |
| `explicit.stat_3196823591@T2` | -1.83402 |
| `explicit.stat_2365392475@T2` | -1.83401 |
| `explicit.stat_828533480@T1` | -1.83289 |
| `explicit.stat_1366840608@T2` | -1.83211 |

### weapon.crossbow — n=15532, R²=-1.844

intercept: `3.7791`  ·  log_price: True  ·  ilvl: `-0.04580`  ·  n_mods: `-0.06576`  ·  n_top_tier: `0.48813`  ·  corrupted: `0.03537`  ·  n_sockets: `0.05482`  ·  quality: `0.02219`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.70111 |
| `explicit.stat_1980802737` | 1.34960 |
| `explicit.stat_1202301673@T1` | 1.29605 |
| `explicit.stat_2250681686@T2` | -1.16633 |
| `explicit.stat_709508406@T1` | 0.96424 |
| `explicit.stat_2250681686` | 0.87882 |
| `explicit.stat_518292764@T1` | 0.78610 |
| `crafted.stat_3035140377` | 0.76165 |
| `explicit.stat_1263695895@T2` | -0.69683 |
| `explicit.stat_1263695895@T1` | -0.65575 |
| `explicit.stat_1509134228@T2` | -0.64110 |
| `explicit.stat_1037193709@T1` | -0.63939 |

### weapon.warstaff — n=10247, R²=-0.3552

intercept: `-10.7382`  ·  log_price: True  ·  ilvl: `0.14703`  ·  n_mods: `-0.24775`  ·  n_top_tier: `0.22184`  ·  corrupted: `0.31452`  ·  n_sockets: `0.20044`  ·  quality: `0.06172`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 2.00818 |
| `desecrated.stat_2231156303@T1` | 2.00818 |
| `desecrated.stat_3291658075@T1` | -1.43783 |
| `desecrated.stat_473429811@T1` | -1.43783 |
| `crafted.stat_210067635@T2` | 1.40428 |
| `rune.stat_243313994` | 0.93792 |
| `explicit.stat_1509134228@T1` | 0.81925 |
| `explicit.stat_328541901@T1` | -0.80152 |
| `explicit.stat_328541901@T2` | -0.76548 |
| `desecrated.stat_9187492` | 0.71201 |
| `explicit.stat_709508406@T1` | 0.69898 |
| `explicit.stat_1037193709@T1` | 0.64252 |

### weapon.staff — n=9587, R²=-0.3792

intercept: `-15.8589`  ·  log_price: True  ·  ilvl: `0.20553`  ·  n_mods: `-0.15750`  ·  n_top_tier: `0.50848`  ·  corrupted: `0.51923`  ·  n_sockets: `0.23638`  ·  quality: `0.03293`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.00163 |
| `explicit.stat_4226189338@T1` | 1.94938 |
| `explicit.stat_591105508@T1` | 1.59260 |
| `explicit.stat_293638271@T2` | -1.47381 |
| `explicit.stat_2254480358@T2` | 1.17464 |
| `explicit.stat_124131830@T1` | 1.14394 |
| `explicit.stat_1600707273@T1` | 0.98313 |
| `explicit.stat_591105508@T2` | 0.88669 |
| `explicit.stat_124131830@T2` | 0.71826 |
| `explicit.stat_3291658075@T2` | -0.71798 |
| `explicit.stat_274716455@T1` | -0.71747 |
| `explicit.stat_3695891184@T1` | -0.70798 |

### weapon.sceptre — n=9453, R²=-0.3333

intercept: `-20.8271`  ·  log_price: True  ·  ilvl: `0.26775`  ·  n_mods: `-0.03187`  ·  n_top_tier: `0.02964`  ·  corrupted: `0.46007`  ·  n_sockets: `0.26517`  ·  quality: `0.03241`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 3.16562 |
| `explicit.stat_2162097452@T2` | 1.77835 |
| `explicit.stat_1250712710@T2` | 1.71573 |
| `explicit.stat_3057012405@T1` | 1.36980 |
| `explicit.stat_101878827@T1` | 1.07641 |
| `explicit.stat_101878827@T2` | 0.92363 |
| `explicit.stat_2347036682@T1` | 0.71197 |
| `explicit.stat_1250712710@T1` | 0.62469 |
| `explicit.stat_849987426@T1` | 0.60392 |
| `explicit.stat_1798257884@T2` | 0.60032 |
| `explicit.stat_4080418644@T1` | 0.56220 |
| `explicit.stat_4010677958@T1` | 0.52167 |

### weapon.spear — n=7690, R²=-0.4081

intercept: `-12.7393`  ·  log_price: True  ·  ilvl: `0.17894`  ·  n_mods: `-0.20459`  ·  n_top_tier: `0.64881`  ·  corrupted: `0.06934`  ·  n_sockets: `0.23162`  ·  quality: `0.06212`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.90263 |
| `explicit.stat_1202301673@T1` | 1.58145 |
| `explicit.stat_9187492@T1` | 1.26731 |
| `crafted.stat_3035140377` | 1.12987 |
| `desecrated.stat_210067635@T1` | -1.08831 |
| `explicit.stat_4080418644@T2` | -0.97453 |
| `explicit.stat_709508406@T1` | 0.95029 |
| `explicit.stat_1509134228@T1` | 0.92626 |
| `explicit.stat_9187492@T2` | -0.87653 |
| `explicit.stat_3261801346@T1` | -0.84569 |
| `explicit.stat_1940865751@T2` | -0.79513 |
| `explicit.stat_3261801346@T2` | -0.79275 |

### armour.focus — n=6304, R²=-0.3612

intercept: `-13.4972`  ·  log_price: True  ·  ilvl: `0.17754`  ·  n_mods: `-0.18763`  ·  n_top_tier: `0.86710`  ·  corrupted: `0.43885`  ·  n_sockets: `0.43327`  ·  quality: `0.06025`

| stat_id | coef |
|---|---|
| `explicit.stat_4220027924@T2` | -1.41597 |
| `explicit.stat_4220027924@T1` | -1.33180 |
| `explicit.stat_2231156303@T2` | -1.31463 |
| `explicit.stat_2923486259@T1` | -1.11101 |
| `explicit.stat_2231156303@T1` | -1.09605 |
| `crafted.stat_2974417149@T1` | 1.04782 |
| `crafted.stat_737908626@T2` | -0.94886 |
| `explicit.stat_736967255@T2` | -0.91107 |
| `explicit.stat_2974417149@T1` | -0.90117 |
| `explicit.stat_2339757871@T2` | -0.85183 |
| `explicit.stat_4052037485@T2` | -0.83026 |
| `explicit.stat_737908626@T2` | -0.82284 |

### armour.quiver — n=5912, R²=-0.3126

intercept: `-14.3996`  ·  log_price: True  ·  ilvl: `0.17686`  ·  n_mods: `-0.11504`  ·  n_top_tier: `0.91895`  ·  corrupted: `0.65575`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.57837 |
| `explicit.stat_2463230181@T1` | 3.07794 |
| `explicit.stat_2463230181@T2` | 1.56830 |
| `explicit.stat_1573130764@T1` | -1.30543 |
| `explicit.stat_681332047@T2` | -1.28020 |
| `explicit.stat_2321178454@T2` | -1.02246 |
| `explicit.stat_4067062424@T1` | -1.00850 |
| `explicit.stat_803737631@T2` | -0.99998 |
| `explicit.stat_803737631@T1` | -0.95967 |
| `explicit.stat_2194114101@T2` | -0.89799 |
| `explicit.stat_3261801346@T1` | -0.87584 |
| `explicit.stat_1573130764@T2` | -0.87350 |

### armour.shield — n=5133, R²=-0.4623

intercept: `-11.7912`  ·  log_price: True  ·  ilvl: `0.15788`  ·  n_mods: `-0.10862`  ·  n_top_tier: `0.59790`  ·  corrupted: `-0.27947`  ·  n_sockets: `0.32052`  ·  quality: `0.06163`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.28387 |
| `explicit.stat_3321629045@T2` | -1.21503 |
| `explicit.stat_1301765461@T1` | 0.98494 |
| `explicit.stat_2481353198@T2` | -0.97201 |
| `explicit.stat_2923486259@T2` | -0.93697 |
| `explicit.stat_3484657501@T2` | -0.91531 |
| `explicit.stat_4095671657@T1` | -0.89147 |
| `explicit.stat_3033371881@T2` | -0.88815 |
| `explicit.stat_328541901@T1` | -0.88506 |
| `explicit.stat_3855016469@T1` | -0.80787 |
| `explicit.stat_2451402625@T1` | -0.79933 |
| `explicit.stat_4095671657@T2` | -0.79313 |

### weapon.twomace — n=4704, R²=-0.4707

intercept: `-9.8351`  ·  log_price: True  ·  ilvl: `0.13630`  ·  n_mods: `-0.22262`  ·  n_top_tier: `0.28138`  ·  corrupted: `-0.09147`  ·  n_sockets: `0.17161`  ·  quality: `0.05636`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.40457 |
| `desecrated.stat_1509134228@T1` | 1.69738 |
| `explicit.stat_1037193709@T1` | -1.39592 |
| `explicit.stat_1263695895@T2` | -0.80481 |
| `crafted.stat_3035140377` | 0.78491 |
| `explicit.stat_3336890334@T1` | -0.71186 |
| `explicit.stat_9187492@T1` | -0.69385 |
| `explicit.stat_210067635@T2` | 0.65359 |
| `explicit.stat_387439868@T2` | -0.65154 |
| `explicit.stat_1509134228@T1` | 0.58571 |
| `explicit.stat_691932474@T1` | -0.56542 |
| `explicit.stat_3695891184@T1` | -0.54966 |

## Coverage (listings per base)

- … **Sapphire** — 29843 listings (29793 priced) [0.3–885594757.8 ex]
- … **Emerald** — 29130 listings (29089 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 22313 listings (22287 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11054 listings (11039 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 9787 listings (9766 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 9459 listings (9436 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9331 listings (9323 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8839 listings (8822 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8707 listings (8688 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8477 listings (8465 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7248 listings (7237 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6958 listings (6952 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6908 listings (6902 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6640 listings (6619 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6104 listings (6097 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 6032 listings (6005 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 5984 listings (5967 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 5961 listings (5950 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 5943 listings (5936 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5891 listings (5865 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5804 listings (5795 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5712 listings (5705 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5455 listings (5452 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5415 listings (5403 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5350 listings (5341 priced) [0.3–398912568423.8 ex]

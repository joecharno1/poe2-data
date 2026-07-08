# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-08T03:46:50+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **309732** (309349 priced in exalted)
- Distinct bases: 954 · distinct mods: 2803 · mod rows: 1470091
- Sold signals: **31045** sold · 165349 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-08T03:37:04+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×16.67** (median |log error| 2.8134)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 77% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.02** · typical error ×40.86 · ±30% 10% · n=44998
- Premium segment (60ex+): skill **+0.04** · typical error ×175.18 · ±30% 0% · n=27983

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 5903 | ×11.90 | 4% | +0.03 | +0.05 |
| accessory.amulet | 5520 | ×49.72 | 20% | +0.03 | +0.02 |
| jewel | 5134 | ×8.30 | 8% | +0.01 | +0.04 |
| accessory.belt | 4481 | ×10.00 | 22% | +0.05 | +0.05 |
| armour.chest | 4444 | ×8.93 | 14% | +0.01 | +0.02 |
| armour.helmet | 4272 | ×10.00 | 22% | +0.00 | +0.01 |
| armour.boots | 4096 | ×13.63 | 5% | +0.02 | +0.02 |
| armour.gloves | 4025 | ×14.68 | 5% | +0.02 | +0.03 |
| other | 3684 | ×9.75 | 37% | +0.05 | +0.16 |
| weapon.wand | 2707 | ×33.43 | 23% | +0.05 | +0.06 |
| weapon.bow | 2218 | ×20.51 | 20% | +0.08 | +0.08 |
| weapon.crossbow | 2039 | ×18.09 | 20% | +0.09 | +0.11 |
| weapon.warstaff | 979 | ×70.00 | 17% | +0.02 | +0.02 |
| weapon.staff | 940 | ×55.00 | 19% | +0.04 | +0.06 |
| weapon.sceptre | 938 | ×74.94 | 11% | +0.07 | +0.03 |
| weapon.spear | 763 | ×45.00 | 19% | +0.04 | +0.03 |
| armour.focus | 655 | ×550.38 | 10% | +0.02 | +0.06 |
| armour.quiver | 617 | ×72.28 | 13% | +0.00 | +0.04 |
| armour.shield | 517 | ×20.00 | 18% | +0.02 | +0.03 |
| weapon.twomace | 462 | ×20.00 | 12% | +0.02 | +0.07 |
| flask.charm | 402 | ×5.00 | 41% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=32241, R²=-0.5002

intercept: `1.6049`  ·  log_price: True  ·  ilvl: `0.00006`  ·  n_mods: `0.02297`  ·  n_top_tier: `0.50263`  ·  corrupted: `0.75808`  ·  n_sockets: `-0.00006`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 2.72529 |
| `explicit.stat_3141070085@T1` | -1.97542 |
| `explicit.stat_2891184298@T1` | 1.87033 |
| `explicit.stat_2106365538@T1` | 1.60879 |
| `explicit.stat_1589917703@T1` | -1.37675 |
| `explicit.stat_101878827@T1` | -1.05285 |
| `explicit.stat_2974417149@T1` | 0.95297 |
| `explicit.stat_3917489142@T1` | 0.93294 |
| `explicit.stat_1050105434@T1` | -0.84518 |
| `explicit.stat_789117908@T1` | -0.66276 |
| `explicit.stat_1589917703` | 0.34955 |
| `explicit.stat_3141070085` | 0.32368 |

### jewel — n=27659, R²=-0.6211

intercept: `-1.0590`  ·  log_price: True  ·  ilvl: `0.03615`  ·  n_mods: `0.14672`  ·  n_top_tier: `-0.02943`  ·  corrupted: `0.22196`  ·  quality: `0.21945`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.99326 |
| `explicit.stat_1569101201@T1` | 3.70417 |
| `explicit.stat_1316278494@T1` | -2.70132 |
| `explicit.stat_3741323227@T1` | -2.69181 |
| `explicit.stat_3714003708@T1` | -2.66378 |
| `explicit.stat_1854213750@T1` | -2.38672 |
| `explicit.stat_1569159338@T1` | -2.11096 |
| `explicit.stat_4045894391@T1` | -1.95547 |
| `explicit.stat_1697951953@T1` | -1.93549 |
| `explicit.stat_3374165039@T1` | -1.84917 |
| `explicit.stat_153777645@T1` | 1.79861 |
| `explicit.stat_3668351662@T1` | -1.65058 |

### accessory.ring — n=26852, R²=-1.2283

intercept: `4.2974`  ·  log_price: True  ·  ilvl: `-0.04220`  ·  n_mods: `-0.08169`  ·  n_top_tier: `0.17194`  ·  corrupted: `1.00633`  ·  n_sockets: `-1.08466`  ·  quality: `0.03699`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.63439 |
| `explicit.stat_707457662@T2` | 3.59732 |
| `explicit.stat_1379411836@T1` | -2.36822 |
| `explicit.stat_1379411836@T2` | -1.91395 |
| `explicit.stat_2557965901@T1` | 1.09416 |
| `explicit.stat_2557965901@T2` | 0.93717 |
| `explicit.stat_1368271171@T2` | -0.93199 |
| `explicit.stat_1368271171@T1` | -0.83636 |
| `explicit.stat_2231156303@T1` | -0.83623 |
| `explicit.stat_2231156303@T2` | -0.72343 |
| `explicit.stat_707457662` | -0.67502 |
| `explicit.stat_3695891184@T1` | -0.59931 |

### accessory.amulet — n=25422, R²=-2.0855

intercept: `4.1272`  ·  log_price: True  ·  ilvl: `-0.04981`  ·  n_mods: `-0.03060`  ·  n_top_tier: `0.98012`  ·  corrupted: `0.14091`  ·  n_sockets: `1.43949`  ·  quality: `-0.00354`

| stat_id | coef |
|---|---|
| `explicit.stat_587431675@T1` | -1.11318 |
| `explicit.stat_3299347043@T1` | -1.10760 |
| `explicit.stat_983749596@T1` | -1.09100 |
| `explicit.stat_3325883026@T1` | -1.08609 |
| `explicit.stat_2748665614@T1` | -1.08548 |
| `explicit.stat_983749596@T2` | -1.08215 |
| `explicit.stat_3917489142@T2` | -1.07686 |
| `explicit.stat_3917489142@T1` | -1.06245 |
| `explicit.stat_3325883026@T2` | -1.06120 |
| `explicit.stat_2748665614@T2` | -1.05965 |
| `explicit.stat_3489782002@T2` | -1.05622 |
| `explicit.stat_472520716@T2` | -1.04772 |

### accessory.belt — n=20743, R²=-0.1222

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.06642`  ·  corrupted: `0.00004`  ·  n_sockets: `-0.00007`

| stat_id | coef |
|---|---|
| `explicit.stat_2639966148` | 0.15576 |
| `explicit.stat_1389754388@T1` | -0.06645 |
| `explicit.stat_51994685@T1` | -0.06644 |
| `explicit.stat_2923486259@T2` | -0.06644 |
| `explicit.stat_1570770415@T1` | -0.06644 |
| `explicit.stat_1836676211@T2` | -0.06643 |
| `explicit.stat_644456512@T1` | -0.06643 |
| `explicit.stat_644456512@T2` | -0.06643 |
| `explicit.stat_1389754388@T2` | -0.06643 |
| `explicit.stat_51994685@T2` | -0.06642 |
| `explicit.stat_4220027924@T2` | -0.06642 |
| `explicit.stat_3299347043@T2` | -0.06642 |

### armour.chest — n=20515, R²=-0.354

intercept: `3.0524`  ·  log_price: True  ·  ilvl: `-0.01641`  ·  n_mods: `-0.08097`  ·  n_top_tier: `0.30651`  ·  corrupted: `0.18181`  ·  n_sockets: `0.01058`  ·  quality: `0.00636`

| stat_id | coef |
|---|---|
| `implicit.stat_1978899297` | -1.29619 |
| `rune.stat_836936635` | -0.76594 |
| `implicit.stat_2251279027` | 0.68339 |
| `explicit.stat_915769802@T1` | -0.61881 |
| `explicit.stat_3261801346@T1` | -0.61223 |
| `explicit.stat_3321629045@T1` | -0.50730 |
| `explicit.stat_915769802@T2` | -0.48528 |
| `explicit.stat_3261801346@T2` | -0.43254 |
| `explicit.stat_3484657501@T1` | -0.41167 |
| `explicit.stat_3325883026@T2` | -0.40641 |
| `explicit.stat_4015621042@T1` | -0.39578 |
| `explicit.stat_986397080@T2` | -0.38496 |

### armour.helmet — n=20089, R²=-0.28

intercept: `2.3451`  ·  log_price: True  ·  ilvl: `-0.00086`  ·  n_mods: `-0.00536`  ·  n_top_tier: `0.24277`  ·  corrupted: `0.75772`  ·  n_sockets: `0.00008`  ·  quality: `0.00128`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 0.93771 |
| `explicit.stat_1062208444@T2` | -0.30702 |
| `explicit.stat_4080418644@T2` | -0.25568 |
| `explicit.stat_53045048@T2` | -0.25370 |
| `explicit.stat_3362812763@T2` | -0.25048 |
| `explicit.stat_2451402625@T1` | -0.24966 |
| `explicit.stat_803737631@T2` | -0.24900 |
| `explicit.stat_53045048@T1` | -0.24884 |
| `explicit.stat_3362812763@T1` | -0.24834 |
| `explicit.stat_4052037485@T2` | -0.24433 |
| `explicit.stat_4080418644@T1` | -0.24419 |
| `explicit.stat_3321629045@T2` | -0.24394 |

### armour.boots — n=18969, R²=-0.6341

intercept: `4.3575`  ·  log_price: True  ·  ilvl: `-0.04658`  ·  n_mods: `-0.19428`  ·  n_top_tier: `0.54169`  ·  corrupted: `0.50586`  ·  n_sockets: `0.19268`  ·  quality: `0.01163`

| stat_id | coef |
|---|---|
| `explicit.stat_1062208444@T2` | -1.14693 |
| `explicit.stat_3321629045@T1` | -1.04875 |
| `explicit.stat_2250533757@T1` | 0.96206 |
| `explicit.stat_328541901@T1` | -0.95897 |
| `explicit.stat_2339757871@T1` | -0.92699 |
| `explicit.stat_2923486259@T2` | -0.92023 |
| `explicit.stat_2451402625@T2` | -0.89279 |
| `explicit.stat_3321629045@T2` | -0.79423 |
| `explicit.stat_3484657501@T2` | -0.74171 |
| `explicit.stat_1999113824@T1` | -0.71658 |
| `explicit.stat_1671376347@T2` | -0.71329 |
| `explicit.stat_1062208444@T1` | -0.69525 |

### armour.gloves — n=18524, R²=-0.7356

intercept: `3.5226`  ·  log_price: True  ·  ilvl: `-0.04415`  ·  n_mods: `-0.12595`  ·  n_top_tier: `0.49627`  ·  corrupted: `0.35316`  ·  n_sockets: `0.35014`  ·  quality: `0.01394`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.27850 |
| `explicit.stat_3484657501@T2` | -1.09663 |
| `explicit.stat_803737631@T2` | -1.06714 |
| `explicit.stat_3033371881@T2` | -0.94789 |
| `explicit.stat_3033371881@T1` | -0.90105 |
| `explicit.stat_3695891184@T1` | -0.89201 |
| `explicit.stat_328541901@T1` | -0.86630 |
| `explicit.stat_2797971005@T2` | -0.85639 |
| `explicit.stat_3695891184@T2` | -0.82470 |
| `explicit.stat_53045048@T1` | -0.77723 |
| `explicit.stat_681332047@T2` | -0.76273 |
| `explicit.stat_1754445556@T1` | -0.71155 |

### weapon.wand — n=12763, R²=-2.0827

intercept: `3.6373`  ·  log_price: True  ·  ilvl: `-0.04543`  ·  n_mods: `-0.00901`  ·  n_top_tier: `0.74611`  ·  corrupted: `0.03762`  ·  n_sockets: `0.01417`  ·  quality: `0.01271`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.29094 |
| `explicit.stat_124131830@T1` | 1.64633 |
| `explicit.stat_4226189338@T1` | 1.63953 |
| `explicit.stat_591105508@T1` | 1.62507 |
| `explicit.stat_1545858329@T1` | 1.59890 |
| `explicit.stat_1600707273@T1` | 1.54681 |
| `explicit.stat_736967255@T2` | 0.80498 |
| `explicit.stat_737908626@T1` | -0.79597 |
| `explicit.stat_2768835289@T2` | -0.77533 |
| `explicit.stat_2231156303@T2` | -0.77226 |
| `explicit.stat_328541901@T1` | -0.76723 |
| `explicit.stat_473429811@T1` | -0.76576 |

### weapon.bow — n=10413, R²=-1.9913

intercept: `3.3292`  ·  log_price: True  ·  ilvl: `-0.04126`  ·  n_mods: `-0.01002`  ·  n_top_tier: `0.46379`  ·  corrupted: `-0.01462`  ·  n_sockets: `0.00300`  ·  quality: `0.00715`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | 1.79686 |
| `desecrated.stat_210067635@T1` | -1.74732 |
| `explicit.stat_1202301673@T1` | 1.58183 |
| `crafted.stat_3035140377` | 1.12820 |
| `desecrated.stat_666077204@T1` | 0.72344 |
| `explicit.stat_55876295@T1` | -0.52133 |
| `explicit.stat_3695891184@T2` | -0.50251 |
| `explicit.stat_2694482655@T1` | -0.50204 |
| `explicit.stat_3336890334@T2` | -0.49809 |
| `explicit.stat_3261801346@T1` | -0.49454 |
| `explicit.stat_3695891184@T1` | -0.49322 |
| `explicit.stat_3639275092@T1` | -0.49042 |

### weapon.crossbow — n=9784, R²=-1.8113

intercept: `3.6961`  ·  log_price: True  ·  ilvl: `-0.04610`  ·  n_mods: `-0.00460`  ·  n_top_tier: `0.51707`  ·  corrupted: `-0.03376`  ·  n_sockets: `0.01424`  ·  quality: `0.00378`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -2.67330 |
| `explicit.stat_1980802737` | 2.13570 |
| `explicit.stat_709508406@T1` | 1.65036 |
| `explicit.stat_1202301673@T1` | 1.64418 |
| `explicit.stat_2250681686@T2` | -1.41292 |
| `explicit.stat_1509134228@T1` | 1.29677 |
| `explicit.stat_2250681686` | 0.91262 |
| `explicit.stat_1037193709@T1` | 0.85788 |
| `crafted.stat_3035140377` | 0.80623 |
| `explicit.stat_1202301673@T2` | -0.65123 |
| `explicit.stat_1509134228@T2` | -0.59816 |
| `explicit.stat_669069897@T1` | -0.57614 |

### flask.charm — n=6568, R²=-0.3358

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.24374`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.53165 |
| `explicit.stat_1056492907` | 3.02034 |
| `explicit.stat_2676834156@T1` | 1.60932 |
| `explicit.stat_2541588185@T1` | 0.19492 |
| `explicit.stat_3138344128` | 0.02180 |
| `explicit.stat_2678930256` | 0.00147 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_3246948616` | 0.00004 |
| `explicit.stat_1120862500@T2` | -0.00004 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_2676834156@T2` | -0.00003 |
| `explicit.stat_1873752457` | 0.00003 |

### weapon.warstaff — n=4705, R²=-0.551

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00165`  ·  n_sockets: `0.00001`  ·  quality: `0.00021`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | -4.01907 |
| `desecrated.stat_2231156303@T1` | -4.01907 |
| `rune.stat_243313994` | 2.95300 |
| `rune.stat_731403740` | 1.49175 |
| `crafted.stat_210067635@T2` | -0.88353 |
| `rune.stat_1712188793` | -0.81384 |
| `desecrated.stat_9187492` | 0.71572 |
| `explicit.stat_9187492@T1` | 0.66188 |
| `desecrated.stat_518292764` | 0.32878 |
| `desecrated.stat_2527686725` | 0.25019 |
| `rune.stat_3336890334` | 0.11249 |
| `desecrated.stat_669069897` | -0.09034 |

### weapon.staff — n=4404, R²=-0.5852

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00885`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.46880 |
| `explicit.stat_4226189338@T1` | 2.30251 |
| `explicit.stat_2254480358@T1` | 1.01221 |
| `explicit.stat_1600707273@T1` | 0.86725 |
| `explicit.stat_3962278098@T2` | 0.69142 |
| `explicit.stat_2254480358@T2` | 0.44004 |
| `crafted.stat_124131830` | 0.43506 |
| `explicit.stat_473429811@T1` | 0.39479 |
| `rune.stat_3990135792` | -0.23512 |
| `explicit.stat_3291658075@T2` | 0.23455 |
| `rune.stat_975988108` | -0.13618 |
| `rune.stat_2974417149` | 0.12110 |

### weapon.sceptre — n=4379, R²=-0.5888

intercept: `-0.0086`  ·  log_price: True  ·  ilvl: `0.00011`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.48247`  ·  corrupted: `1.68914`  ·  n_sockets: `0.00024`  ·  quality: `0.09371`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.81819 |
| `explicit.stat_4080418644@T2` | -0.48278 |
| `explicit.stat_2347036682@T2` | -0.48270 |
| `explicit.stat_4080418644@T1` | -0.48270 |
| `explicit.stat_1263695895@T2` | -0.48268 |
| `explicit.stat_1250712710@T1` | -0.48258 |
| `explicit.stat_3984865854@T2` | -0.48257 |
| `explicit.stat_328541901@T1` | -0.48252 |
| `explicit.stat_2347036682@T1` | -0.48251 |
| `explicit.stat_1574590649@T1` | -0.48246 |
| `explicit.stat_789117908@T1` | -0.48246 |
| `explicit.stat_3639275092@T2` | -0.48245 |

### weapon.spear — n=3774, R²=-0.5875

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00002`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00039`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.29859 |
| `crafted.stat_3035140377` | 1.71304 |
| `explicit.stat_210067635@T1` | 0.83420 |
| `crafted.stat_518292764` | 0.80847 |
| `rune.stat_1039491398` | 0.08435 |
| `explicit.stat_1509134228@T1` | 0.04278 |
| `crafted.stat_210067635` | 0.00928 |
| `desecrated.stat_1509134228` | 0.00889 |
| `rune.stat_1509134228` | -0.00126 |
| `explicit.stat_709508406@T1` | 0.00118 |
| `desecrated.stat_691932474` | -0.00062 |
| `explicit.stat_9187492@T1` | 0.00013 |

### armour.focus — n=3067, R²=-0.6141

intercept: `-0.0015`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.44652`  ·  corrupted: `0.00003`  ·  n_sockets: `0.00004`  ·  quality: `0.03407`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -5.45127 |
| `crafted.stat_737908626@T2` | -4.64950 |
| `desecrated.stat_378817135@T1` | -1.21477 |
| `crafted.stat_2974417149@T1` | -0.72339 |
| `explicit.stat_789117908@T2` | -0.44657 |
| `explicit.stat_274716455@T1` | -0.44656 |
| `explicit.stat_2891184298@T2` | -0.44656 |
| `explicit.stat_2923486259@T1` | -0.44655 |
| `explicit.stat_3291658075@T1` | -0.44655 |
| `explicit.stat_274716455@T2` | -0.44655 |
| `explicit.stat_736967255@T2` | -0.44654 |
| `explicit.stat_2339757871@T2` | -0.44654 |

### armour.quiver — n=2898, R²=-0.6462

intercept: `-0.0029`  ·  log_price: True  ·  ilvl: `0.00003`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.49279`  ·  corrupted: `0.00018`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.49925 |
| `explicit.stat_681332047@T2` | -0.49312 |
| `explicit.stat_681332047@T1` | -0.49309 |
| `explicit.stat_1573130764@T1` | -0.49290 |
| `explicit.stat_1368271171@T2` | -0.49289 |
| `explicit.stat_2194114101@T2` | -0.49288 |
| `explicit.stat_2321178454@T2` | -0.49288 |
| `explicit.stat_1573130764@T2` | -0.49284 |
| `explicit.stat_803737631@T2` | -0.49282 |
| `explicit.stat_3714003708@T2` | -0.49279 |
| `explicit.stat_3261801346@T1` | -0.49278 |
| `explicit.stat_2194114101@T1` | -0.49278 |

### armour.shield — n=2481, R²=-0.4842

intercept: `-0.0007`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.26676`  ·  corrupted: `0.00180`  ·  n_sockets: `0.00001`  ·  quality: `0.06867`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.78700 |
| `explicit.stat_1978899297@T2` | -0.43303 |
| `explicit.stat_1011760251@T1` | -0.27093 |
| `explicit.stat_1011760251@T2` | -0.26953 |
| `explicit.stat_328541901@T1` | -0.26682 |
| `explicit.stat_2339757871@T1` | -0.26681 |
| `explicit.stat_2481353198@T1` | -0.26681 |
| `explicit.stat_328541901@T2` | -0.26680 |
| `explicit.stat_2481353198@T2` | -0.26679 |
| `explicit.stat_3372524247@T2` | -0.26679 |
| `explicit.stat_3484657501@T1` | -0.26678 |
| `explicit.stat_2901986750@T2` | -0.26678 |

### weapon.twomace — n=2183, R²=-0.5346

intercept: `-0.0008`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.31986`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.35039 |
| `desecrated.stat_210067635@T1` | -1.04075 |
| `rune.stat_709508406` | 0.66640 |
| `explicit.stat_1509134228@T1` | 0.62393 |
| `desecrated.stat_1509134228@T1` | -0.60166 |
| `explicit.stat_3336890334@T1` | -0.31998 |
| `explicit.stat_1037193709@T1` | -0.31996 |
| `explicit.stat_1037193709@T2` | -0.31990 |
| `explicit.stat_1263695895@T1` | -0.31990 |
| `explicit.stat_821021828@T1` | -0.31990 |
| `explicit.stat_387439868@T2` | -0.31989 |
| `explicit.stat_3336890334@T2` | -0.31989 |

## Coverage (listings per base)

- … **Sapphire** — 13170 listings (13153 priced) [0.4–7553463.8 ex]
- … **Emerald** — 13072 listings (13064 priced) [0.4–7553463.8 ex]
- … **Ruby** — 10128 listings (10118 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 6146 listings (6142 priced) [0.3–5288620.9 ex]
- … **Prismatic Ring** — 4684 listings (4682 priced) [0.3–24532814.5 ex]
- … **Stellar Amulet** — 4610 listings (4610 priced) [0.3–35690283.3 ex]
- … **Solar Amulet** — 4565 listings (4558 priced) [0.4–66666666.0 ex]
- … **Amethyst Ring** — 4468 listings (4467 priced) [0.4–71450.3 ex]
- … **Gold Amulet** — 4364 listings (4359 priced) [0.2–4894457.0 ex]
- … **Gold Ring** — 4225 listings (4223 priced) [0.4–24532814.5 ex]
- … **Dueling Wand** — 4014 listings (4009 priced) [0.3–3736768402.2 ex]
- … **Sapphire Ring** — 3539 listings (3535 priced) [0.4–24532814.5 ex]
- … **Ruby Ring** — 3454 listings (3454 priced) [0.4–37474957.5 ex]
- … **Topaz Ring** — 3408 listings (3407 priced) [0.4–123132003.2 ex]
- … **Plate Belt** — 3144 listings (3141 priced) [0.3–5286174.1 ex]
- … **Ancestral Tiara** — 3064 listings (3061 priced) [0.6–41469259.3 ex]
- … **Obliterator Bow** — 3064 listings (3057 priced) [0.4–22139622146.9 ex]
- … **Lapis Amulet** — 3046 listings (3045 priced) [0.4–5286174.1 ex]
- … **Jade Amulet** — 3008 listings (3007 priced) [0.2–4547453.5 ex]
- … **Amber Amulet** — 3006 listings (3005 priced) [0.2–124352753.2 ex]
- … **Heavy Belt** — 2935 listings (2935 priced) [0.4–4877938.3 ex]
- … **Unset Ring** — 2865 listings (2865 priced) [0.4–24532814.5 ex]
- … **Bloodstone Amulet** — 2812 listings (2812 priced) [0.4–329628.5 ex]
- … **Pearl Ring** — 2750 listings (2750 priced) [0.4–24532814.5 ex]
- … **Azure Amulet** — 2690 listings (2690 priced) [0.4–123132003.2 ex]

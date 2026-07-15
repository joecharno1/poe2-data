# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-15T10:39:38+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **505703** (504643 priced in exalted)
- Distinct bases: 982 · distinct mods: 3099 · mod rows: 2399731
- Sold signals: **26268** sold · 281718 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-15T10:31:45+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×27.10** (median |log error| 3.2997)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.10** · typical error ×85.14 · ±30% 5% · n=72898
- Premium segment (60ex+): skill **+0.10** · typical error ×379.02 · ±30% 0% · n=48731

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 10086 | ×48.95 | 21% | +0.06 | +0.07 |
| jewel | 9385 | ×9.50 | 5% | +0.02 | +0.06 |
| accessory.amulet | 9313 | ×52.07 | 21% | +0.03 | +0.03 |
| accessory.belt | 7160 | ×27.24 | 23% | +0.05 | +0.07 |
| armour.chest | 6912 | ×26.66 | 25% | +0.05 | +0.08 |
| armour.helmet | 6825 | ×33.89 | 20% | +0.06 | +0.08 |
| armour.boots | 6368 | ×41.16 | 23% | +0.06 | +0.08 |
| armour.gloves | 6208 | ×44.93 | 21% | +0.05 | +0.07 |
| other | 5510 | ×1.71 | 45% | +0.10 | +0.18 |
| weapon.wand | 3893 | ×38.82 | 19% | +0.07 | +0.09 |
| weapon.bow | 3145 | ×28.17 | 18% | +0.10 | +0.10 |
| weapon.crossbow | 2967 | ×28.06 | 19% | +0.09 | +0.12 |
| weapon.warstaff | 1772 | ×32.34 | 16% | +0.11 | +0.10 |
| weapon.staff | 1666 | ×57.41 | 14% | +0.09 | +0.08 |
| weapon.sceptre | 1643 | ×41.83 | 7% | +0.14 | +0.14 |
| weapon.spear | 1362 | ×78.52 | 16% | +0.08 | +0.08 |
| armour.focus | 1146 | ×39.97 | 8% | +0.13 | +0.13 |
| armour.quiver | 1076 | ×30.84 | 9% | +0.10 | +0.13 |
| flask.charm | 933 | ×50.00 | 34% | +0.03 | +0.06 |
| armour.shield | 890 | ×17.97 | 16% | +0.03 | +0.03 |
| weapon.twomace | 803 | ×17.40 | 13% | +0.07 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=50713, R²=-0.92

intercept: `-1.6526`  ·  log_price: True  ·  ilvl: `0.02687`  ·  n_mods: `0.61027`  ·  n_top_tier: `-0.15877`  ·  corrupted: `0.36233`  ·  quality: `0.23846`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.39174 |
| `explicit.stat_2301718443@T1` | 3.28855 |
| `explicit.stat_627767961@T1` | -2.40317 |
| `explicit.stat_1697951953@T1` | -2.09237 |
| `explicit.stat_3780644166@T1` | -2.08634 |
| `explicit.stat_1697447343@T1` | -1.94321 |
| `explicit.stat_3174700878@T1` | 1.87787 |
| `explicit.stat_239367161@T1` | -1.77652 |
| `explicit.stat_3091578504@T1` | -1.75484 |
| `explicit.stat_3485067555@T1` | 1.74833 |
| `explicit.stat_924253255@T1` | -1.69173 |
| `explicit.stat_1805182458@T1` | -1.67398 |

### other — n=48938, R²=-0.6293

intercept: `1.6076`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `0.03750`  ·  n_top_tier: `0.30911`  ·  corrupted: `0.26965`  ·  n_sockets: `-0.00005`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2974417149@T1` | 0.41739 |
| `explicit.stat_3299347043@T1` | -0.35627 |
| `explicit.stat_3291658075@T1` | 0.34294 |
| `implicit.stat_3879011313` | 0.34158 |
| `implicit.stat_2219129443` | 0.33442 |
| `explicit.stat_2482852589@T1` | -0.28941 |
| `explicit.stat_789117908@T1` | -0.24016 |
| `implicit.stat_4041853756` | 0.22651 |
| `explicit.stat_1050105434@T1` | -0.19990 |
| `implicit.stat_1379411836` | -0.14643 |
| `explicit.stat_2106365538@T1` | -0.12173 |
| `implicit.stat_3182714256` | 0.11255 |

### accessory.ring — n=46167, R²=-1.9874

intercept: `3.2546`  ·  log_price: True  ·  ilvl: `-0.04033`  ·  n_mods: `0.00293`  ·  n_top_tier: `0.90875`  ·  corrupted: `0.03290`  ·  n_sockets: `-0.05123`  ·  quality: `0.07859`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -0.95646 |
| `explicit.stat_2231156303@T1` | -0.94824 |
| `explicit.stat_3325883026@T1` | -0.93943 |
| `explicit.stat_2144192055@T1` | -0.93442 |
| `explicit.stat_1368271171@T2` | -0.93344 |
| `explicit.stat_803737631@T1` | -0.92942 |
| `explicit.stat_3291658075@T2` | -0.92752 |
| `explicit.stat_4220027924@T2` | -0.92645 |
| `explicit.stat_1050105434@T1` | -0.92569 |
| `explicit.stat_3291658075@T1` | -0.92512 |
| `explicit.stat_3325883026@T2` | -0.92388 |
| `explicit.stat_3962278098@T2` | -0.92371 |

### accessory.amulet — n=42634, R²=-2.1371

intercept: `3.8469`  ·  log_price: True  ·  ilvl: `-0.04683`  ·  n_mods: `-0.02677`  ·  n_top_tier: `0.95453`  ·  corrupted: `0.04799`  ·  n_sockets: `-0.12860`  ·  quality: `-0.00115`

| stat_id | coef |
|---|---|
| `explicit.stat_472520716@T2` | -1.06451 |
| `explicit.stat_472520716@T1` | -1.05512 |
| `explicit.stat_2162097452@T2` | -1.03622 |
| `explicit.stat_803737631@T1` | -1.03012 |
| `explicit.stat_2901986750@T1` | -1.01456 |
| `explicit.stat_1050105434@T2` | -1.01006 |
| `explicit.stat_803737631@T2` | -0.99889 |
| `explicit.stat_2866361420@T2` | -0.99535 |
| `explicit.stat_3917489142@T2` | -0.99111 |
| `explicit.stat_2482852589@T2` | -0.98903 |
| `explicit.stat_2891184298@T1` | -0.98729 |
| `explicit.stat_789117908@T2` | -0.98646 |

### accessory.belt — n=32820, R²=-1.6742

intercept: `3.2718`  ·  log_price: True  ·  ilvl: `-0.03980`  ·  n_mods: `-0.01835`  ·  n_top_tier: `1.54681`  ·  corrupted: `0.29632`  ·  n_sockets: `1.52156`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.69745 |
| `explicit.stat_2881298780@T1` | -1.58830 |
| `explicit.stat_1389754388@T1` | -1.58357 |
| `explicit.stat_3299347043@T2` | -1.57395 |
| `explicit.stat_809229260@T2` | -1.57381 |
| `explicit.stat_3325883026@T1` | -1.56905 |
| `explicit.stat_51994685@T1` | -1.56556 |
| `explicit.stat_4220027924@T2` | -1.56428 |
| `explicit.stat_1671376347@T2` | -1.56356 |
| `explicit.stat_3585532255@T2` | -1.54900 |
| `explicit.stat_644456512@T1` | -1.54788 |
| `explicit.stat_809229260@T1` | -1.54787 |

### armour.chest — n=32454, R²=-1.7858

intercept: `3.2738`  ·  log_price: True  ·  ilvl: `-0.04042`  ·  n_mods: `-0.01085`  ·  n_top_tier: `0.44297`  ·  corrupted: `0.18484`  ·  n_sockets: `0.01220`  ·  quality: `0.02880`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.67122 |
| `explicit.stat_3981240776@T1` | 0.82594 |
| `explicit.stat_4080418644@T2` | -0.48215 |
| `explicit.stat_986397080@T2` | -0.47905 |
| `explicit.stat_4080418644@T1` | -0.47435 |
| `explicit.stat_3484657501@T1` | -0.46650 |
| `explicit.stat_986397080@T1` | -0.46414 |
| `explicit.stat_2451402625@T2` | -0.46293 |
| `explicit.stat_3372524247@T2` | -0.46196 |
| `explicit.stat_124859000@T2` | -0.46190 |
| `explicit.stat_2923486259@T2` | -0.46124 |
| `explicit.stat_915769802@T1` | -0.45986 |

### armour.helmet — n=31629, R²=-1.6804

intercept: `3.7527`  ·  log_price: True  ·  ilvl: `-0.04723`  ·  n_mods: `-0.02692`  ·  n_top_tier: `0.43340`  ·  corrupted: `0.65733`  ·  n_sockets: `0.02247`  ·  quality: `0.05618`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.03644 |
| `crafted.stat_3917489142@T1` | 2.60756 |
| `explicit.stat_1263695895@T1` | -0.73613 |
| `explicit.stat_1263695895@T2` | -0.61398 |
| `explicit.stat_3917489142@T2` | -0.60247 |
| `explicit.stat_2162097452@T2` | -0.50542 |
| `explicit.stat_3917489142@T1` | -0.50406 |
| `explicit.stat_3261801346@T2` | -0.47877 |
| `explicit.stat_3261801346@T1` | -0.47827 |
| `explicit.stat_3321629045@T2` | -0.47229 |
| `explicit.stat_53045048@T1` | -0.47141 |
| `explicit.stat_1999113824@T1` | -0.47065 |

### armour.boots — n=29637, R²=-1.7845

intercept: `3.3554`  ·  log_price: True  ·  ilvl: `-0.04142`  ·  n_mods: `-0.01095`  ·  n_top_tier: `0.76828`  ·  corrupted: `-0.01476`  ·  n_sockets: `0.01124`  ·  quality: `0.02475`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 1.50231 |
| `explicit.stat_2250533757@T1` | 1.28989 |
| `explicit.stat_2339757871@T1` | -0.89602 |
| `explicit.stat_3917489142@T2` | -0.87450 |
| `explicit.stat_3917489142@T1` | -0.82803 |
| `explicit.stat_3299347043@T1` | -0.80198 |
| `explicit.stat_2160282525@T1` | -0.80036 |
| `explicit.stat_2923486259@T2` | -0.79634 |
| `explicit.stat_4080418644@T1` | -0.79499 |
| `explicit.stat_1671376347@T2` | -0.78929 |
| `explicit.stat_3362812763@T1` | -0.78510 |
| `explicit.stat_1062208444@T2` | -0.78077 |

### armour.gloves — n=28872, R²=-1.9284

intercept: `3.4784`  ·  log_price: True  ·  ilvl: `-0.04386`  ·  n_mods: `-0.00304`  ·  n_top_tier: `0.54316`  ·  corrupted: `-0.01390`  ·  n_sockets: `0.02425`  ·  quality: `0.04936`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | -6.73469 |
| `explicit.stat_1671376347@T1` | 1.03797 |
| `explicit.stat_9187492@T1` | 0.88090 |
| `explicit.stat_9187492@T2` | -0.86395 |
| `explicit.stat_3484657501@T2` | -0.67550 |
| `explicit.stat_4052037485@T1` | -0.61664 |
| `explicit.stat_3484657501@T1` | -0.61651 |
| `explicit.stat_803737631@T2` | -0.61406 |
| `explicit.stat_3321629045@T2` | -0.59731 |
| `explicit.stat_3321629045@T1` | -0.57211 |
| `explicit.stat_3917489142@T2` | -0.56702 |
| `explicit.stat_803737631@T1` | -0.56513 |

### weapon.wand — n=18487, R²=-2.2713

intercept: `3.8055`  ·  log_price: True  ·  ilvl: `-0.04698`  ·  n_mods: `-0.01737`  ·  n_top_tier: `0.47194`  ·  corrupted: `0.01329`  ·  n_sockets: `0.03812`  ·  quality: `0.00265`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -3.25726 |
| `explicit.stat_1545858329@T1` | 3.17989 |
| `explicit.stat_2254480358@T1` | 2.85519 |
| `explicit.stat_4226189338@T1` | 1.89598 |
| `explicit.stat_124131830@T1` | 1.87167 |
| `explicit.stat_591105508@T1` | 1.84879 |
| `explicit.stat_736967255@T2` | 1.54732 |
| `crafted.stat_124131830` | 1.21701 |
| `explicit.stat_2254480358@T2` | 0.61344 |
| `explicit.stat_1263695895@T2` | -0.60972 |
| `explicit.stat_1263695895@T1` | -0.58945 |
| `explicit.stat_737908626@T1` | -0.54951 |

### weapon.bow — n=14880, R²=-2.0068

intercept: `3.5137`  ·  log_price: True  ·  ilvl: `-0.04246`  ·  n_mods: `-0.03374`  ·  n_top_tier: `0.63885`  ·  corrupted: `-0.10243`  ·  n_sockets: `0.00656`  ·  quality: `0.03111`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.06007 |
| `explicit.stat_1202301673@T1` | 1.58773 |
| `crafted.stat_3035140377` | 1.37574 |
| `explicit.stat_1263695895@T1` | -0.87360 |
| `explicit.stat_1263695895@T2` | -0.85243 |
| `explicit.stat_2463230181@T2` | -0.72792 |
| `explicit.stat_3695891184@T2` | -0.71658 |
| `explicit.stat_3695891184@T1` | -0.70381 |
| `explicit.stat_518292764@T2` | -0.68932 |
| `explicit.stat_1509134228@T1` | -0.68806 |
| `explicit.stat_2694482655@T2` | -0.68744 |
| `explicit.stat_669069897@T1` | -0.68158 |

### weapon.crossbow — n=14040, R²=-1.9385

intercept: `3.9030`  ·  log_price: True  ·  ilvl: `-0.04764`  ·  n_mods: `-0.01613`  ·  n_top_tier: `0.72500`  ·  corrupted: `0.08174`  ·  n_sockets: `0.02181`  ·  quality: `0.01353`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -2.48021 |
| `explicit.stat_1980802737@T2` | -1.99174 |
| `explicit.stat_2250681686` | 1.84663 |
| `explicit.stat_709508406@T1` | 1.50492 |
| `explicit.stat_1202301673@T1` | 1.43333 |
| `explicit.stat_1980802737` | 1.21840 |
| `crafted.stat_3035140377` | 0.91885 |
| `explicit.stat_1263695895@T2` | -0.88099 |
| `explicit.stat_1263695895@T1` | -0.81982 |
| `explicit.stat_2694482655@T1` | -0.78401 |
| `explicit.stat_669069897@T1` | -0.78053 |
| `explicit.stat_1202301673@T2` | -0.76789 |

### flask.charm — n=12970, R²=-0.5401

intercept: `0.0070`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.67630`  ·  corrupted: `2.19449`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.27492 |
| `explicit.stat_1056492907` | 3.35254 |
| `explicit.stat_828533480@T2` | -2.67632 |
| `explicit.stat_828533480@T1` | -2.67630 |
| `explicit.stat_2541588185@T2` | -2.67630 |
| `explicit.stat_2676834156@T2` | -2.67630 |
| `explicit.stat_1873752457@T2` | -2.67630 |
| `explicit.stat_1120862500@T2` | -2.67629 |
| `explicit.stat_3196823591@T2` | -2.67629 |
| `explicit.stat_388617051@T2` | -2.67628 |
| `explicit.stat_1366840608@T2` | -2.67628 |
| `explicit.stat_2365392475@T2` | -2.67628 |

### weapon.warstaff — n=8574, R²=-0.4665

intercept: `-6.8386`  ·  log_price: True  ·  ilvl: `0.09371`  ·  n_mods: `-0.17543`  ·  n_top_tier: `0.61841`  ·  corrupted: `0.19374`  ·  n_sockets: `0.10214`  ·  quality: `0.05459`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.46469 |
| `explicit.stat_1037193709@T1` | 1.25774 |
| `explicit.stat_328541901@T1` | -1.13059 |
| `explicit.stat_328541901@T2` | -1.11590 |
| `explicit.stat_55876295@T2` | -0.83486 |
| `explicit.stat_1037193709@T2` | -0.82409 |
| `desecrated.stat_9187492` | 0.71648 |
| `explicit.stat_1940865751@T1` | -0.66385 |
| `explicit.stat_210067635@T1` | -0.65980 |
| `explicit.stat_55876295@T1` | -0.65737 |
| `explicit.stat_3695891184@T2` | -0.62287 |
| `explicit.stat_791928121@T2` | -0.61124 |

### weapon.staff — n=8024, R²=-0.4503

intercept: `-10.5983`  ·  log_price: True  ·  ilvl: `0.13790`  ·  n_mods: `-0.11481`  ·  n_top_tier: `0.46675`  ·  corrupted: `0.07135`  ·  n_sockets: `0.21304`  ·  quality: `0.04913`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.44150 |
| `explicit.stat_4226189338@T1` | 1.40080 |
| `explicit.stat_4226189338@T2` | 1.32937 |
| `explicit.stat_1600707273@T1` | 1.18412 |
| `explicit.stat_1545858329@T1` | 1.16057 |
| `explicit.stat_2254480358@T1` | 1.09653 |
| `explicit.stat_124131830@T2` | 1.08610 |
| `explicit.stat_2768835289@T2` | 1.01192 |
| `explicit.stat_293638271@T2` | -0.79249 |
| `explicit.stat_591105508@T1` | 0.75591 |
| `explicit.stat_2254480358@T2` | 0.69601 |
| `explicit.stat_2974417149@T1` | -0.68409 |

### weapon.sceptre — n=7949, R²=-0.4017

intercept: `-15.6779`  ·  log_price: True  ·  ilvl: `0.19845`  ·  n_mods: `-0.04819`  ·  n_top_tier: `0.60672`  ·  corrupted: `0.64776`  ·  n_sockets: `0.20059`  ·  quality: `0.05813`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.10002 |
| `explicit.stat_2162097452@T2` | 1.14410 |
| `explicit.stat_1263695895@T2` | -1.04377 |
| `explicit.stat_2347036682@T2` | -0.98905 |
| `explicit.stat_1263695895@T1` | -0.88935 |
| `explicit.stat_289128254@T2` | -0.84582 |
| `explicit.stat_1574590649@T2` | -0.80929 |
| `explicit.stat_4080418644@T1` | -0.76417 |
| `explicit.stat_2854751904@T2` | -0.76265 |
| `explicit.stat_1050105434@T2` | -0.71571 |
| `explicit.stat_3057012405@T1` | 0.62312 |
| `explicit.stat_789117908@T2` | -0.62179 |

### weapon.spear — n=6571, R²=-0.5234

intercept: `-8.8958`  ·  log_price: True  ·  ilvl: `0.11961`  ·  n_mods: `-0.04843`  ·  n_top_tier: `0.71447`  ·  corrupted: `-0.13162`  ·  n_sockets: `0.18841`  ·  quality: `0.09974`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.00516 |
| `explicit.stat_1202301673@T1` | 2.00426 |
| `explicit.stat_9187492@T1` | 1.91341 |
| `explicit.stat_1263695895@T2` | -1.13197 |
| `explicit.stat_1509134228@T1` | 1.05326 |
| `crafted.stat_3035140377` | 1.01232 |
| `desecrated.stat_210067635@T1` | -0.99556 |
| `explicit.stat_55876295@T1` | -0.98187 |
| `explicit.stat_210067635@T1` | 0.95070 |
| `explicit.stat_1037193709@T1` | -0.90611 |
| `explicit.stat_55876295@T2` | -0.81750 |
| `explicit.stat_1940865751@T2` | -0.80069 |

### armour.focus — n=5406, R²=-0.4279

intercept: `-11.7406`  ·  log_price: True  ·  ilvl: `0.15019`  ·  n_mods: `-0.16030`  ·  n_top_tier: `0.84936`  ·  corrupted: `0.81061`  ·  n_sockets: `0.48884`  ·  quality: `0.06716`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 1.55970 |
| `explicit.stat_4220027924@T2` | -1.25645 |
| `explicit.stat_3962278098@T1` | -1.21374 |
| `explicit.stat_736967255@T2` | -1.19288 |
| `explicit.stat_2923486259@T1` | -1.08365 |
| `explicit.stat_3962278098@T2` | -1.03346 |
| `explicit.stat_2231156303@T1` | -1.00699 |
| `explicit.stat_2974417149@T2` | -0.98952 |
| `explicit.stat_2231156303@T2` | -0.97479 |
| `explicit.stat_737908626@T2` | -0.95461 |
| `explicit.stat_4015621042@T1` | -0.95419 |
| `explicit.stat_3291658075@T1` | -0.93829 |

### armour.quiver — n=5032, R²=-0.3728

intercept: `-11.2604`  ·  log_price: True  ·  ilvl: `0.13691`  ·  n_mods: `-0.05921`  ·  n_top_tier: `0.83776`  ·  corrupted: `0.46343`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 7.14119 |
| `explicit.stat_4067062424@T1` | -1.35488 |
| `explicit.stat_2321178454@T2` | -1.26342 |
| `explicit.stat_681332047@T2` | -1.08836 |
| `explicit.stat_1573130764@T1` | -1.00121 |
| `explicit.stat_1573130764@T2` | -0.98517 |
| `explicit.stat_803737631@T2` | -0.94260 |
| `explicit.stat_2463230181@T1` | 0.92606 |
| `explicit.stat_4067062424@T2` | -0.84696 |
| `explicit.stat_3261801346@T1` | -0.81539 |
| `explicit.stat_2321178454@T1` | -0.81357 |
| `explicit.stat_2194114101@T2` | -0.79129 |

### armour.shield — n=4376, R²=-0.552

intercept: `-8.5496`  ·  log_price: True  ·  ilvl: `0.11072`  ·  n_mods: `-0.06522`  ·  n_top_tier: `0.53668`  ·  corrupted: `-0.11789`  ·  n_sockets: `0.11268`  ·  quality: `0.05941`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.23004 |
| `explicit.stat_1011760251@T2` | -1.00743 |
| `explicit.stat_2481353198@T2` | -1.00001 |
| `explicit.stat_4095671657@T1` | -0.99021 |
| `explicit.stat_2481353198@T1` | -0.96124 |
| `explicit.stat_2923486259@T2` | -0.81115 |
| `explicit.stat_3033371881@T2` | -0.80211 |
| `explicit.stat_3321629045@T2` | -0.79629 |
| `explicit.stat_328541901@T1` | -0.76955 |
| `explicit.stat_3484657501@T1` | -0.76713 |
| `explicit.stat_2339757871@T1` | -0.76320 |
| `explicit.stat_3855016469@T1` | -0.75154 |

### weapon.twomace — n=4026, R²=-0.4979

intercept: `-9.4356`  ·  log_price: True  ·  ilvl: `0.12487`  ·  n_mods: `-0.15690`  ·  n_top_tier: `0.52415`  ·  corrupted: `0.41170`  ·  n_sockets: `0.16944`  ·  quality: `0.04855`

| stat_id | coef |
|---|---|
| `desecrated.stat_1509134228@T1` | 2.21940 |
| `desecrated.stat_210067635@T1` | -2.06772 |
| `explicit.stat_1037193709@T1` | -1.87697 |
| `explicit.stat_3336890334@T1` | -1.50211 |
| `explicit.stat_1263695895@T1` | -1.18648 |
| `explicit.stat_518292764@T2` | -1.09987 |
| `crafted.stat_3035140377` | 1.09435 |
| `explicit.stat_1263695895@T2` | -1.01803 |
| `explicit.stat_387439868@T2` | -0.85161 |
| `explicit.stat_1037193709@T2` | -0.83468 |
| `explicit.stat_3639275092@T1` | -0.80275 |
| `explicit.stat_3695891184@T1` | -0.72495 |

## Coverage (listings per base)

- … **Sapphire** — 23627 listings (23592 priced) [0.3–7553463.8 ex]
- … **Emerald** — 23264 listings (23234 priced) [0.3–7553463.8 ex]
- … **Ruby** — 17810 listings (17795 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 9576 listings (9567 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 7910 listings (7900 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 7689 listings (7674 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 7576 listings (7569 priced) [0.2–19945827.9 ex]
- … **Gold Amulet** — 7226 listings (7216 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 7142 listings (7138 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 7071 listings (7058 priced) [0.2–91750808.2 ex]
- … **Sapphire Ring** — 5898 listings (5892 priced) [0.2–307202867.9 ex]
- … **Dueling Wand** — 5882 listings (5866 priced) [0.3–4297682211.9 ex]
- … **Topaz Ring** — 5655 listings (5650 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5621 listings (5618 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 5092 listings (5076 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5040 listings (5035 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4936 listings (4924 priced) [0.6–398912568423.8 ex]
- … **Amber Amulet** — 4901 listings (4897 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 4897 listings (4891 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4855 listings (4848 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4746 listings (4741 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 4561 listings (4555 priced) [0.2–275252424.7 ex]
- … **Heavy Belt** — 4559 listings (4555 priced) [0.3–398912568423.8 ex]
- … **Azure Amulet** — 4476 listings (4476 priced) [0.3–123132003.2 ex]
- … **Obliterator Bow** — 4451 listings (4438 priced) [0.3–42622633798.0 ex]

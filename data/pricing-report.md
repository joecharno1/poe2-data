# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-09T12:17:57+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **372893** (372273 priced in exalted)
- Distinct bases: 963 · distinct mods: 2923 · mod rows: 1770578
- Sold signals: **28834** sold · 199351 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-09T12:05:37+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×19.70** (median |log error| 2.9806)
- Within ±30% of asking price: **12%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×46.51 · ±30% 6% · n=54584
- Premium segment (60ex+): skill **+0.08** · typical error ×199.74 · ±30% 0% · n=34471

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 7238 | ×12.33 | 4% | +0.04 | +0.06 |
| accessory.amulet | 6794 | ×48.26 | 20% | +0.02 | +0.03 |
| jewel | 6441 | ×8.04 | 8% | +0.02 | +0.04 |
| accessory.belt | 5343 | ×10.65 | 6% | +0.01 | +0.02 |
| armour.chest | 5231 | ×15.65 | 6% | +0.06 | +0.09 |
| armour.helmet | 5167 | ×13.81 | 6% | +0.01 | +0.04 |
| armour.boots | 4792 | ×21.17 | 7% | +0.11 | +0.14 |
| armour.gloves | 4722 | ×22.71 | 5% | +0.04 | +0.06 |
| other | 4380 | ×9.85 | 38% | +0.06 | +0.15 |
| weapon.wand | 3107 | ×43.75 | 19% | +0.07 | +0.06 |
| weapon.bow | 2507 | ×25.80 | 18% | +0.09 | +0.10 |
| weapon.crossbow | 2363 | ×22.24 | 19% | +0.11 | +0.13 |
| weapon.warstaff | 1270 | ×83.29 | 15% | +0.07 | +0.07 |
| weapon.sceptre | 1171 | ×50.01 | 12% | +0.09 | +0.08 |
| weapon.staff | 1170 | ×50.00 | 15% | +0.06 | +0.05 |
| weapon.spear | 986 | ×50.00 | 16% | +0.05 | +0.05 |
| armour.focus | 802 | ×74.68 | 14% | +0.07 | +0.12 |
| armour.quiver | 743 | ×59.99 | 13% | +0.03 | +0.09 |
| flask.charm | 645 | ×76.59 | 32% | +0.00 | +0.02 |
| armour.shield | 634 | ×30.00 | 14% | +0.05 | +0.10 |
| weapon.twomace | 582 | ×20.00 | 15% | +0.07 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=37494, R²=-0.5464

intercept: `1.6076`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `0.00428`  ·  n_top_tier: `0.43631`  ·  corrupted: `0.79899`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 1.27030 |
| `explicit.stat_2891184298@T1` | 0.90266 |
| `explicit.stat_2974417149@T1` | 0.87720 |
| `explicit.stat_1589917703@T1` | -0.80043 |
| `explicit.stat_3917489142@T1` | 0.67465 |
| `explicit.stat_1050105434@T1` | -0.65009 |
| `explicit.stat_2482852589@T1` | 0.61042 |
| `explicit.stat_789117908@T1` | -0.48338 |
| `explicit.stat_2106365538@T1` | 0.37659 |
| `explicit.stat_3141070085@T1` | 0.25076 |
| `explicit.stat_2968503605@T1` | 0.24703 |
| `implicit.stat_1379411836` | -0.23080 |

### jewel — n=34938, R²=-0.6743

intercept: `-1.2642`  ·  log_price: True  ·  ilvl: `0.03559`  ·  n_mods: `0.19554`  ·  n_top_tier: `-0.01570`  ·  corrupted: `0.35447`  ·  quality: `0.22289`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -4.43710 |
| `explicit.stat_3741323227@T1` | -3.40463 |
| `explicit.stat_3780644166@T1` | -3.34733 |
| `explicit.stat_1569101201@T1` | 2.93511 |
| `explicit.stat_2527686725@T1` | 2.06280 |
| `explicit.stat_1697951953@T1` | -2.05573 |
| `explicit.stat_3714003708@T1` | -2.04240 |
| `explicit.stat_234296660@T1` | -2.01515 |
| `explicit.stat_1315743832@T1` | 1.93845 |
| `explicit.stat_1316278494@T1` | -1.92615 |
| `explicit.stat_1423639565@T1` | -1.81889 |
| `explicit.stat_3174700878@T1` | 1.74732 |

### accessory.ring — n=33056, R²=-1.204

intercept: `3.8414`  ·  log_price: True  ·  ilvl: `-0.03957`  ·  n_mods: `-0.03537`  ·  n_top_tier: `-0.05893`  ·  corrupted: `1.05180`  ·  n_sockets: `0.76793`  ·  quality: `0.02954`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 3.91163 |
| `explicit.stat_707457662@T2` | 3.86360 |
| `explicit.stat_2557965901@T1` | 1.55724 |
| `explicit.stat_2557965901@T2` | 1.41095 |
| `explicit.stat_1379411836@T1` | -1.12040 |
| `explicit.stat_2923486259@T1` | 0.90323 |
| `explicit.stat_1573130764@T1` | -0.86884 |
| `explicit.stat_2923486259@T2` | 0.79840 |
| `explicit.stat_1368271171@T1` | -0.75777 |
| `explicit.stat_1263695895@T1` | -0.68485 |
| `explicit.stat_1368271171@T2` | -0.68012 |
| `explicit.stat_4080418644@T2` | 0.66940 |

### accessory.amulet — n=31070, R²=-2.0935

intercept: `3.9757`  ·  log_price: True  ·  ilvl: `-0.04804`  ·  n_mods: `-0.02546`  ·  n_top_tier: `0.67013`  ·  corrupted: `0.11976`  ·  n_sockets: `0.04732`  ·  quality: `-0.00234`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.13526 |
| `explicit.stat_124131830` | 1.08156 |
| `explicit.stat_983749596@T2` | -0.97737 |
| `explicit.stat_3981240776@T2` | 0.92661 |
| `explicit.stat_3981240776@T1` | 0.82953 |
| `explicit.stat_3299347043@T1` | -0.81782 |
| `explicit.stat_3299347043@T2` | -0.79586 |
| `explicit.stat_472520716@T1` | -0.77818 |
| `explicit.stat_472520716@T2` | -0.75652 |
| `explicit.stat_2748665614@T2` | -0.75467 |
| `explicit.stat_3917489142@T2` | -0.74068 |
| `explicit.stat_3917489142@T1` | -0.73462 |

### accessory.belt — n=24664, R²=-0.3503

intercept: `5.1436`  ·  log_price: True  ·  ilvl: `-0.03129`  ·  n_mods: `-0.34177`  ·  n_top_tier: `0.68534`  ·  corrupted: `0.55442`  ·  n_sockets: `-0.09095`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.17246 |
| `explicit.stat_3325883026@T1` | -1.12428 |
| `explicit.stat_51994685@T1` | -1.07575 |
| `explicit.stat_2881298780@T1` | -0.98984 |
| `explicit.stat_1389754388@T2` | -0.84409 |
| `explicit.stat_2923486259@T2` | -0.84012 |
| `explicit.stat_644456512@T1` | -0.78547 |
| `explicit.stat_2923486259@T1` | -0.76895 |
| `explicit.stat_2881298780@T2` | -0.75882 |
| `explicit.stat_1671376347@T2` | -0.75089 |
| `explicit.stat_1570770415@T1` | -0.73982 |
| `explicit.stat_4220027924@T2` | -0.73893 |

### armour.chest — n=24405, R²=-0.9166

intercept: `4.3375`  ·  log_price: True  ·  ilvl: `-0.04891`  ·  n_mods: `-0.13108`  ·  n_top_tier: `0.46383`  ·  corrupted: `0.09212`  ·  n_sockets: `0.12335`  ·  quality: `0.02738`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.16317 |
| `explicit.stat_915769802@T1` | -0.81521 |
| `explicit.stat_3325883026@T2` | -0.78606 |
| `explicit.stat_2923486259@T1` | -0.72770 |
| `explicit.stat_3321629045@T1` | -0.68392 |
| `explicit.stat_2451402625@T2` | -0.64738 |
| `explicit.stat_3484657501@T1` | -0.62356 |
| `explicit.stat_915769802@T2` | -0.62297 |
| `explicit.stat_4080418644@T1` | -0.61288 |
| `explicit.stat_4080418644@T2` | -0.61082 |
| `explicit.stat_986397080@T2` | -0.59459 |
| `explicit.stat_4015621042@T1` | -0.58113 |

### armour.helmet — n=23886, R²=-0.4472

intercept: `3.4452`  ·  log_price: True  ·  ilvl: `-0.02705`  ·  n_mods: `-0.11220`  ·  n_top_tier: `0.41952`  ·  corrupted: `0.85088`  ·  n_sockets: `0.03901`  ·  quality: `0.02999`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.05701 |
| `explicit.stat_1263695895@T1` | -0.68981 |
| `explicit.stat_53045048@T2` | -0.64148 |
| `explicit.stat_3362812763@T2` | -0.61795 |
| `explicit.stat_4080418644@T1` | -0.61287 |
| `explicit.stat_4080418644@T2` | -0.57632 |
| `explicit.stat_2339757871@T1` | -0.56823 |
| `explicit.stat_1999113824@T1` | -0.52489 |
| `explicit.stat_3362812763@T1` | -0.51044 |
| `explicit.stat_53045048@T1` | -0.50445 |
| `explicit.stat_3917489142@T2` | -0.49458 |
| `explicit.stat_328541901@T2` | -0.48953 |

### armour.boots — n=22382, R²=-1.0506

intercept: `4.5208`  ·  log_price: True  ·  ilvl: `-0.05393`  ·  n_mods: `-0.09741`  ·  n_top_tier: `0.59639`  ·  corrupted: `0.37464`  ·  n_sockets: `0.11716`  ·  quality: `0.01671`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | -1.78841 |
| `explicit.stat_2339757871@T1` | -1.64178 |
| `explicit.stat_2250533757@T1` | 1.42871 |
| `desecrated.stat_2250533757@T2` | -0.97778 |
| `explicit.stat_1062208444@T2` | -0.95516 |
| `explicit.stat_2923486259@T2` | -0.95173 |
| `explicit.stat_1999113824@T2` | -0.93080 |
| `explicit.stat_1999113824@T1` | -0.89870 |
| `explicit.stat_3362812763@T1` | -0.88365 |
| `explicit.stat_3917489142@T2` | -0.82918 |
| `rune.stat_836936635` | -0.79040 |
| `explicit.stat_2160282525@T1` | -0.78322 |

### armour.gloves — n=21805, R²=-0.9192

intercept: `4.1391`  ·  log_price: True  ·  ilvl: `-0.05273`  ·  n_mods: `-0.14115`  ·  n_top_tier: `0.50644`  ·  corrupted: `0.21516`  ·  n_sockets: `0.32805`  ·  quality: `0.02631`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.40890 |
| `explicit.stat_3484657501@T2` | -1.07108 |
| `explicit.stat_681332047@T2` | -1.03728 |
| `explicit.stat_803737631@T2` | -1.02487 |
| `explicit.stat_3299347043@T2` | -0.83053 |
| `explicit.stat_2797971005@T2` | -0.78832 |
| `explicit.stat_328541901@T1` | -0.74914 |
| `explicit.stat_3695891184@T2` | -0.74312 |
| `explicit.stat_9187492@T1` | 0.71140 |
| `explicit.stat_3695891184@T1` | -0.71100 |
| `explicit.stat_3484657501@T1` | -0.70085 |
| `explicit.stat_328541901@T2` | -0.68923 |

### weapon.wand — n=14551, R²=-2.0624

intercept: `3.8219`  ·  log_price: True  ·  ilvl: `-0.04754`  ·  n_mods: `-0.01078`  ·  n_top_tier: `0.60536`  ·  corrupted: `-0.02733`  ·  n_sockets: `0.03026`  ·  quality: `0.00747`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.66202 |
| `explicit.stat_4226189338@T1` | 1.88764 |
| `explicit.stat_591105508@T1` | 1.76517 |
| `explicit.stat_1545858329@T1` | 1.75995 |
| `explicit.stat_124131830@T1` | 1.64070 |
| `explicit.stat_1600707273@T1` | 1.63442 |
| `explicit.stat_736967255@T2` | 1.55671 |
| `crafted.stat_124131830` | 0.95987 |
| `explicit.stat_1600707273@T2` | 0.69623 |
| `explicit.stat_3015669065@T1` | -0.67750 |
| `explicit.stat_3015669065@T2` | -0.64919 |
| `explicit.stat_2231156303@T2` | -0.64819 |

### weapon.bow — n=11871, R²=-1.9706

intercept: `3.4459`  ·  log_price: True  ·  ilvl: `-0.04246`  ·  n_mods: `-0.01717`  ·  n_top_tier: `0.72076`  ·  corrupted: `0.26961`  ·  n_sockets: `0.00128`  ·  quality: `0.01028`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.38281 |
| `explicit.stat_2463230181@T1` | 1.46959 |
| `rune.stat_3885405204` | -1.46787 |
| `explicit.stat_1202301673@T1` | 1.40401 |
| `crafted.stat_3035140377` | 1.39648 |
| `explicit.stat_55876295@T1` | -0.82729 |
| `explicit.stat_1037193709@T1` | -0.79257 |
| `explicit.stat_55876295@T2` | -0.76828 |
| `explicit.stat_3336890334@T2` | -0.76694 |
| `explicit.stat_1037193709@T2` | -0.76287 |
| `explicit.stat_3695891184@T2` | -0.75281 |
| `explicit.stat_3261801346@T1` | -0.75199 |

### weapon.crossbow — n=11153, R²=-1.8555

intercept: `3.6134`  ·  log_price: True  ·  ilvl: `-0.04461`  ·  n_mods: `-0.01359`  ·  n_top_tier: `0.54493`  ·  corrupted: `-0.03282`  ·  n_sockets: `0.02734`  ·  quality: `0.00473`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.79183 |
| `explicit.stat_709508406@T1` | 1.56067 |
| `explicit.stat_1202301673@T1` | 1.45485 |
| `explicit.stat_2250681686@T2` | -1.39867 |
| `explicit.stat_1980802737` | 1.21016 |
| `explicit.stat_1509134228@T1` | 1.06107 |
| `crafted.stat_3035140377` | 0.90612 |
| `explicit.stat_2250681686` | 0.88772 |
| `explicit.stat_1202301673@T2` | -0.79912 |
| `explicit.stat_1509134228@T2` | -0.70352 |
| `explicit.stat_1263695895@T2` | -0.66041 |
| `explicit.stat_1037193709@T1` | 0.63383 |

### flask.charm — n=8596, R²=-0.4385

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.06618`  ·  corrupted: `0.57718`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.00644 |
| `explicit.stat_1056492907` | 3.40054 |
| `explicit.stat_2676834156@T1` | 1.54326 |
| `explicit.stat_2541588185@T1` | 0.32416 |
| `explicit.stat_388617051@T2` | -0.06618 |
| `explicit.stat_828533480@T2` | -0.06618 |
| `explicit.stat_2676834156@T2` | -0.06618 |
| `explicit.stat_1873752457@T2` | -0.06618 |
| `explicit.stat_1120862500@T2` | -0.06618 |
| `explicit.stat_3196823591@T2` | -0.06618 |
| `explicit.stat_1873752457@T1` | -0.06617 |
| `explicit.stat_828533480@T1` | -0.06617 |

### weapon.warstaff — n=6057, R²=-0.61

intercept: `-0.0406`  ·  log_price: True  ·  ilvl: `0.00054`  ·  n_mods: `-0.00113`  ·  n_top_tier: `0.30356`  ·  corrupted: `0.44233`  ·  n_sockets: `0.00097`  ·  quality: `0.04961`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.56102 |
| `rune.stat_731403740` | 1.16750 |
| `explicit.stat_9187492@T1` | 0.69256 |
| `crafted.stat_210067635@T2` | -0.66081 |
| `desecrated.stat_9187492` | 0.49822 |
| `rune.stat_1712188793` | -0.45195 |
| `crafted.stat_3035140377` | 0.36647 |
| `desecrated.stat_518292764` | 0.32106 |
| `explicit.stat_328541901@T1` | -0.30699 |
| `explicit.stat_1509134228@T1` | -0.30692 |
| `explicit.stat_328541901@T2` | -0.30641 |
| `explicit.stat_3336890334@T2` | -0.30543 |

### weapon.staff — n=5592, R²=-0.6385

intercept: `-0.1776`  ·  log_price: True  ·  ilvl: `0.00221`  ·  n_mods: `-0.00033`  ·  n_top_tier: `0.18271`  ·  corrupted: `0.09837`  ·  n_sockets: `0.00668`  ·  quality: `0.00487`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 4.34013 |
| `explicit.stat_4226189338@T1` | 2.36822 |
| `explicit.stat_2254480358@T1` | 1.41875 |
| `explicit.stat_1600707273@T1` | 1.41424 |
| `explicit.stat_2254480358@T2` | 1.41010 |
| `explicit.stat_1545858329@T1` | 1.40320 |
| `explicit.stat_4226189338@T2` | 1.24735 |
| `explicit.stat_124131830@T1` | 1.24356 |
| `explicit.stat_2768835289@T2` | 0.97629 |
| `explicit.stat_3962278098@T2` | 0.56435 |
| `explicit.stat_473429811@T1` | 0.50851 |
| `explicit.stat_3291658075@T2` | 0.50718 |

### weapon.sceptre — n=5582, R²=-0.6166

intercept: `-3.2725`  ·  log_price: True  ·  ilvl: `0.04136`  ·  n_mods: `-0.02857`  ·  n_top_tier: `0.35821`  ·  corrupted: `1.20100`  ·  n_sockets: `0.06008`  ·  quality: `0.09269`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.84341 |
| `explicit.stat_3984865854@T1` | 0.81562 |
| `explicit.stat_1798257884@T2` | 0.55417 |
| `explicit.stat_4080418644@T1` | -0.51345 |
| `explicit.stat_2162097452@T2` | 0.48607 |
| `explicit.stat_4080418644@T2` | -0.46671 |
| `explicit.stat_1263695895@T1` | -0.45930 |
| `explicit.stat_1263695895@T2` | -0.45286 |
| `explicit.stat_1574590649@T2` | -0.43011 |
| `explicit.stat_2347036682@T2` | -0.40869 |
| `explicit.stat_3639275092@T2` | -0.39690 |
| `explicit.stat_2854751904@T1` | -0.39197 |

### weapon.spear — n=4707, R²=-0.669

intercept: `-0.0319`  ·  log_price: True  ·  ilvl: `0.00042`  ·  n_mods: `-0.00015`  ·  n_top_tier: `0.33012`  ·  corrupted: `0.00032`  ·  n_sockets: `0.00084`  ·  quality: `0.05328`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 1.95712 |
| `explicit.stat_9187492@T1` | 1.27889 |
| `crafted.stat_3035140377` | 1.27648 |
| `explicit.stat_210067635@T1` | 0.77011 |
| `explicit.stat_3336890334@T1` | 0.76862 |
| `crafted.stat_518292764` | 0.69471 |
| `explicit.stat_691932474@T1` | -0.33108 |
| `explicit.stat_1263695895@T2` | -0.33103 |
| `explicit.stat_55876295@T1` | -0.33091 |
| `explicit.stat_4080418644@T2` | -0.33056 |
| `explicit.stat_709508406@T2` | -0.33043 |
| `explicit.stat_1202301673@T2` | -0.33040 |

### armour.focus — n=3782, R²=-0.6159

intercept: `-1.9061`  ·  log_price: True  ·  ilvl: `0.02352`  ·  n_mods: `-0.00293`  ·  n_top_tier: `0.61525`  ·  corrupted: `-0.01047`  ·  n_sockets: `0.08863`  ·  quality: `0.08677`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -7.12551 |
| `desecrated.stat_378817135@T1` | 5.75751 |
| `desecrated.stat_2910761524@T1` | 4.11063 |
| `desecrated.stat_3393628375@T1` | 3.59046 |
| `explicit.stat_1671376347@T1` | 0.94406 |
| `explicit.stat_124131830@T2` | -0.76314 |
| `explicit.stat_4220027924@T2` | -0.68357 |
| `explicit.stat_3962278098@T2` | -0.66544 |
| `explicit.stat_2231156303@T2` | -0.66056 |
| `explicit.stat_789117908@T2` | -0.65745 |
| `explicit.stat_736967255@T2` | -0.64952 |
| `explicit.stat_2891184298@T2` | -0.64639 |

### armour.quiver — n=3589, R²=-0.6044

intercept: `-2.1089`  ·  log_price: True  ·  ilvl: `0.02418`  ·  n_mods: `0.01790`  ·  n_top_tier: `1.14700`  ·  corrupted: `0.35993`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 11.48888 |
| `explicit.stat_2463230181@T2` | -1.49815 |
| `explicit.stat_681332047@T2` | -1.30373 |
| `explicit.stat_681332047@T1` | -1.24694 |
| `explicit.stat_1573130764@T1` | -1.22934 |
| `explicit.stat_1573130764@T2` | -1.21770 |
| `explicit.stat_2194114101@T2` | -1.21424 |
| `explicit.stat_1368271171@T2` | -1.19178 |
| `explicit.stat_2321178454@T2` | -1.16941 |
| `explicit.stat_3714003708@T2` | -1.16130 |
| `explicit.stat_1368271171@T1` | -1.15538 |
| `explicit.stat_3261801346@T1` | -1.15247 |

### armour.shield — n=3082, R²=-0.6064

intercept: `-0.1967`  ·  log_price: True  ·  ilvl: `0.00246`  ·  n_mods: `0.00002`  ·  n_top_tier: `0.42107`  ·  corrupted: `0.20524`  ·  n_sockets: `0.00198`  ·  quality: `0.07041`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.86249 |
| `explicit.stat_1978899297@T2` | -0.57987 |
| `explicit.stat_1011760251@T2` | -0.44976 |
| `explicit.stat_328541901@T1` | -0.43539 |
| `explicit.stat_328541901@T2` | -0.43301 |
| `explicit.stat_2339757871@T1` | -0.43116 |
| `explicit.stat_2481353198@T2` | -0.42958 |
| `explicit.stat_2481353198@T1` | -0.42758 |
| `explicit.stat_3676141501@T2` | -0.42704 |
| `explicit.stat_1671376347@T1` | -0.42629 |
| `explicit.stat_3372524247@T2` | -0.42600 |
| `explicit.stat_3484657501@T1` | -0.42561 |

### weapon.twomace — n=2801, R²=-0.5715

intercept: `-0.8907`  ·  log_price: True  ·  ilvl: `0.01139`  ·  n_mods: `-0.00419`  ·  n_top_tier: `0.82505`  ·  corrupted: `0.70715`  ·  n_sockets: `0.01481`  ·  quality: `0.01845`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.25371 |
| `crafted.stat_3035140377` | 1.04269 |
| `explicit.stat_1037193709@T1` | -0.88520 |
| `explicit.stat_3336890334@T1` | -0.86903 |
| `explicit.stat_387439868@T2` | -0.86822 |
| `explicit.stat_1037193709@T2` | -0.86062 |
| `explicit.stat_3695891184@T1` | -0.84872 |
| `explicit.stat_821021828@T2` | -0.84477 |
| `explicit.stat_709508406@T1` | -0.84458 |
| `explicit.stat_3639275092@T1` | -0.84344 |
| `explicit.stat_691932474@T1` | -0.84307 |
| `explicit.stat_3695891184@T2` | -0.84103 |

## Coverage (listings per base)

- … **Sapphire** — 16535 listings (16510 priced) [0.4–7553463.8 ex]
- … **Emerald** — 16328 listings (16312 priced) [0.4–7553463.8 ex]
- … **Ruby** — 12583 listings (12571 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 7185 listings (7179 priced) [0.2–5288620.9 ex]
- … **Prismatic Ring** — 5743 listings (5737 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 5591 listings (5581 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 5487 listings (5484 priced) [0.2–4323655.9 ex]
- … **Stellar Amulet** — 5415 listings (5412 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 5294 listings (5286 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 5110 listings (5106 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 4598 listings (4588 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4292 listings (4287 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 4165 listings (4162 priced) [1.0–307202867.9 ex]
- … **Ruby Ring** — 4147 listings (4145 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 3787 listings (3782 priced) [0.2–5286174.1 ex]
- … **Lapis Amulet** — 3732 listings (3730 priced) [0.2–5286174.1 ex]
- … **Ancestral Tiara** — 3688 listings (3683 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3645 listings (3644 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3632 listings (3630 priced) [0.2–4547453.5 ex]
- … **Obliterator Bow** — 3534 listings (3525 priced) [0.4–42622633798.0 ex]
- … **Unset Ring** — 3520 listings (3519 priced) [0.2–24532814.5 ex]
- … **Heavy Belt** — 3509 listings (3508 priced) [0.2–4877938.3 ex]
- … **Bloodstone Amulet** — 3413 listings (3411 priced) [0.2–4275054.0 ex]
- … **Pearl Ring** — 3334 listings (3332 priced) [0.2–24532814.5 ex]
- … **Azure Amulet** — 3258 listings (3258 priced) [0.2–123132003.2 ex]

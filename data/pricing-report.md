# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-17T20:23:57+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **592803** (591068 priced in exalted)
- Distinct bases: 989 · distinct mods: 3217 · mod rows: 2807966
- Sold signals: **25224** sold · 336402 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-17T20:13:18+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.81** (median |log error| 3.2113)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 80% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×60.31 · ±30% 5% · n=86249
- Premium segment (60ex+): skill **+0.14** · typical error ×246.44 · ±30% 0% · n=58343

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 12245 | ×55.12 | 21% | +0.03 | +0.04 |
| jewel | 11537 | ×10.89 | 5% | +0.07 | +0.11 |
| accessory.amulet | 11185 | ×48.25 | 20% | +0.03 | +0.04 |
| accessory.belt | 8260 | ×16.33 | 4% | -0.00 | +0.01 |
| armour.chest | 7955 | ×17.14 | 9% | +0.10 | +0.13 |
| armour.helmet | 7786 | ×17.89 | 7% | +0.13 | +0.15 |
| armour.boots | 7295 | ×35.28 | 16% | +0.11 | +0.13 |
| armour.gloves | 7059 | ×33.35 | 9% | +0.11 | +0.14 |
| other | 6865 | ×6.24 | 40% | +0.09 | +0.15 |
| weapon.wand | 4371 | ×49.06 | 15% | +0.08 | +0.11 |
| weapon.bow | 3445 | ×31.62 | 14% | +0.14 | +0.16 |
| weapon.crossbow | 3230 | ×34.67 | 15% | +0.09 | +0.13 |
| weapon.warstaff | 2112 | ×30.23 | 8% | +0.17 | +0.14 |
| weapon.staff | 1980 | ×42.67 | 6% | +0.13 | +0.12 |
| weapon.sceptre | 1943 | ×34.69 | 5% | +0.19 | +0.20 |
| weapon.spear | 1543 | ×40.09 | 12% | +0.08 | +0.09 |
| armour.focus | 1286 | ×23.42 | 6% | +0.15 | +0.16 |
| armour.quiver | 1244 | ×25.02 | 7% | +0.14 | +0.15 |
| flask.charm | 1073 | ×15.00 | 31% | +0.02 | +0.05 |
| armour.shield | 1021 | ×19.55 | 7% | +0.05 | +0.08 |
| weapon.twomace | 925 | ×9.67 | 10% | +0.09 | +0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=62754, R²=-0.9517

intercept: `-1.8679`  ·  log_price: True  ·  ilvl: `0.02568`  ·  n_mods: `0.84460`  ·  n_top_tier: `-0.31561`  ·  corrupted: `0.29788`  ·  quality: `0.22310`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.54711 |
| `explicit.stat_3374165039@T1` | -2.19837 |
| `explicit.stat_3485067555@T1` | 2.08425 |
| `explicit.stat_1805182458@T1` | -1.98045 |
| `explicit.stat_1869147066@T1` | -1.90013 |
| `explicit.stat_2301718443@T1` | 1.72825 |
| `explicit.stat_239367161@T1` | -1.44120 |
| `explicit.stat_2523933828@T1` | -1.42972 |
| `explicit.stat_3166958180@T1` | -1.42648 |
| `explicit.stat_3787460122@T1` | 1.37901 |
| `explicit.stat_4147897060@T1` | -1.30116 |
| `explicit.stat_1315743832@T1` | -1.29163 |

### other — n=56789, R²=-0.4689

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.68943`  ·  corrupted: `0.26350`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2106365538@T1` | -0.90685 |
| `explicit.stat_789117908@T1` | -0.76585 |
| `implicit.stat_2901986750` | 0.56493 |
| `explicit.stat_2901986750` | 0.55087 |
| `explicit.stat_3299347043@T1` | 0.52053 |
| `explicit.stat_3141070085@T1` | -0.34561 |
| `explicit.stat_1050105434@T1` | -0.33865 |
| `explicit.stat_1589917703@T1` | 0.24542 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23026 |
| `explicit.stat_2974417149@T1` | 0.20868 |

### accessory.ring — n=55926, R²=-2.0435

intercept: `3.2404`  ·  log_price: True  ·  ilvl: `-0.04008`  ·  n_mods: `0.00103`  ·  n_top_tier: `1.00097`  ·  corrupted: `0.01678`  ·  n_sockets: `2.19525`  ·  quality: `0.08140`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -1.03388 |
| `explicit.stat_1573130764@T1` | -1.03053 |
| `explicit.stat_1573130764@T2` | -1.02584 |
| `explicit.stat_4220027924@T2` | -1.01933 |
| `explicit.stat_789117908@T1` | -1.01867 |
| `explicit.stat_1368271171@T2` | -1.01858 |
| `explicit.stat_2231156303@T2` | -1.01755 |
| `explicit.stat_3291658075@T2` | -1.01683 |
| `explicit.stat_2144192055@T1` | -1.01534 |
| `explicit.stat_3291658075@T1` | -1.01533 |
| `explicit.stat_789117908@T2` | -1.01469 |
| `explicit.stat_2901986750@T1` | -1.01426 |

### accessory.amulet — n=51006, R²=-2.1528

intercept: `3.7139`  ·  log_price: True  ·  ilvl: `-0.04520`  ·  n_mods: `-0.02058`  ·  n_top_tier: `1.07302`  ·  corrupted: `0.03899`  ·  n_sockets: `-0.12555`  ·  quality: `0.05923`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.35193 |
| `explicit.stat_3299347043@T2` | -1.21093 |
| `explicit.stat_2974417149@T2` | -1.13937 |
| `explicit.stat_2974417149@T1` | -1.13677 |
| `explicit.stat_472520716@T2` | -1.13626 |
| `explicit.stat_587431675@T2` | -1.13583 |
| `explicit.stat_803737631@T1` | -1.13553 |
| `explicit.stat_2866361420@T2` | -1.13385 |
| `explicit.stat_2866361420@T1` | -1.12396 |
| `explicit.stat_1050105434@T2` | -1.11563 |
| `explicit.stat_803737631@T2` | -1.11475 |
| `explicit.stat_1671376347@T2` | -1.10434 |

### accessory.belt — n=37923, R²=-0.7032

intercept: `6.9990`  ·  log_price: True  ·  ilvl: `-0.05621`  ·  n_mods: `-0.44892`  ·  n_top_tier: `0.78358`  ·  corrupted: `0.89812`  ·  n_sockets: `-0.11338`

| stat_id | coef |
|---|---|
| `implicit.stat_731781020` | -2.04387 |
| `explicit.stat_3299347043@T1` | -1.73164 |
| `explicit.stat_3299347043@T2` | -1.31914 |
| `explicit.stat_2881298780@T1` | -1.25432 |
| `explicit.stat_644456512@T1` | -1.24467 |
| `explicit.stat_51994685@T1` | -1.04117 |
| `explicit.stat_1389754388@T1` | -0.97288 |
| `explicit.stat_809229260@T2` | -0.95103 |
| `explicit.stat_809229260@T1` | -0.94305 |
| `explicit.stat_4220027924@T2` | -0.94089 |
| `explicit.stat_3372524247@T2` | -0.86179 |
| `explicit.stat_915769802@T2` | -0.80496 |

### armour.chest — n=37648, R²=-1.3314

intercept: `4.1565`  ·  log_price: True  ·  ilvl: `-0.04837`  ·  n_mods: `-0.08729`  ·  n_top_tier: `0.50973`  ·  corrupted: `0.23842`  ·  n_sockets: `0.16621`  ·  quality: `0.05307`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.90850 |
| `explicit.stat_3981240776@T1` | 0.97446 |
| `explicit.stat_986397080@T2` | -0.86274 |
| `explicit.stat_2339757871@T2` | -0.76805 |
| `explicit.stat_3484657501@T1` | -0.73080 |
| `explicit.stat_986397080@T1` | -0.70000 |
| `explicit.stat_124859000@T1` | -0.68562 |
| `explicit.stat_3033371881@T1` | 0.64436 |
| `explicit.stat_3301100256@T2` | -0.60395 |
| `explicit.stat_1692879867@T2` | -0.60011 |
| `explicit.stat_4080418644@T2` | -0.59801 |
| `explicit.stat_3299347043@T2` | -0.59773 |

### armour.helmet — n=36560, R²=-1.1474

intercept: `3.7533`  ·  log_price: True  ·  ilvl: `-0.04692`  ·  n_mods: `-0.08934`  ·  n_top_tier: `0.49967`  ·  corrupted: `0.70980`  ·  n_sockets: `0.22489`  ·  quality: `0.04332`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | -3.93380 |
| `explicit.stat_2339757871@T1` | -2.53290 |
| `explicit.stat_3917489142@T2` | -1.13878 |
| `explicit.stat_1999113824@T1` | -0.91119 |
| `explicit.stat_1263695895@T1` | -0.80886 |
| `explicit.stat_3917489142@T1` | -0.78523 |
| `explicit.stat_4052037485@T2` | -0.76601 |
| `explicit.stat_803737631@T2` | -0.69641 |
| `explicit.stat_2162097452@T2` | -0.68686 |
| `explicit.stat_803737631@T1` | -0.67564 |
| `explicit.stat_3321629045@T2` | -0.65697 |
| `explicit.stat_1999113824@T2` | -0.65662 |

### armour.boots — n=34128, R²=-1.4988

intercept: `3.9741`  ·  log_price: True  ·  ilvl: `-0.04846`  ·  n_mods: `-0.04069`  ·  n_top_tier: `0.59749`  ·  corrupted: `0.02242`  ·  n_sockets: `0.07335`  ·  quality: `0.05581`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.00027 |
| `explicit.stat_2250533757@T1` | 1.48143 |
| `explicit.stat_3299347043@T1` | -0.97101 |
| `explicit.stat_2339757871@T1` | -0.96652 |
| `explicit.stat_3917489142@T2` | -0.94912 |
| `explicit.stat_3917489142@T1` | -0.80014 |
| `explicit.stat_2923486259@T2` | -0.78660 |
| `explicit.stat_1062208444@T2` | -0.69272 |
| `explicit.stat_3484657501@T2` | -0.69149 |
| `explicit.stat_1999113824@T2` | -0.68072 |
| `explicit.stat_2160282525@T1` | -0.67436 |
| `explicit.stat_4052037485@T2` | -0.67032 |

### armour.gloves — n=33259, R²=-1.3722

intercept: `3.8886`  ·  log_price: True  ·  ilvl: `-0.05019`  ·  n_mods: `-0.05426`  ·  n_top_tier: `0.68674`  ·  corrupted: `0.05626`  ·  n_sockets: `0.20152`  ·  quality: `0.03844`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.34560 |
| `explicit.stat_2923486259@T1` | -1.19901 |
| `explicit.stat_3321629045@T2` | -1.10986 |
| `rune.stat_836936635` | 1.09163 |
| `explicit.stat_3484657501@T2` | -1.07635 |
| `explicit.stat_3484657501@T1` | -0.97276 |
| `explicit.stat_803737631@T1` | -0.94127 |
| `explicit.stat_803737631@T2` | -0.93931 |
| `explicit.stat_4052037485@T1` | -0.90208 |
| `explicit.stat_3321629045@T1` | -0.89062 |
| `explicit.stat_1999113824@T2` | -0.83588 |
| `explicit.stat_328541901@T1` | -0.82538 |

### weapon.wand — n=20454, R²=-2.0032

intercept: `3.5733`  ·  log_price: True  ·  ilvl: `-0.04411`  ·  n_mods: `-0.06228`  ·  n_top_tier: `0.44273`  ·  corrupted: `0.17370`  ·  n_sockets: `0.15414`  ·  quality: `0.00937`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.53119 |
| `rune.stat_124131830` | -2.42623 |
| `explicit.stat_2254480358@T1` | 2.23532 |
| `explicit.stat_4226189338@T1` | 1.94253 |
| `explicit.stat_124131830@T1` | 1.88843 |
| `explicit.stat_591105508@T1` | 1.75043 |
| `explicit.stat_736967255@T2` | 1.64234 |
| `crafted.stat_124131830` | 1.21379 |
| `explicit.stat_1600707273@T1` | 0.99306 |
| `explicit.stat_2254480358@T2` | 0.99246 |
| `explicit.stat_4226189338@T2` | 0.98376 |
| `explicit.stat_3962278098@T2` | -0.82911 |

### weapon.bow — n=16392, R²=-1.8396

intercept: `3.8253`  ·  log_price: True  ·  ilvl: `-0.04409`  ·  n_mods: `-0.10219`  ·  n_top_tier: `0.61666`  ·  corrupted: `0.34063`  ·  n_sockets: `0.04876`  ·  quality: `0.03223`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.52596 |
| `desecrated.stat_210067635@T1` | -1.40849 |
| `explicit.stat_1202301673@T1` | 1.34139 |
| `desecrated.stat_666077204@T1` | -1.11572 |
| `explicit.stat_1263695895@T1` | -1.07553 |
| `explicit.stat_1263695895@T2` | -0.97084 |
| `explicit.stat_2463230181@T2` | -0.86015 |
| `explicit.stat_3695891184@T2` | -0.81136 |
| `explicit.stat_518292764@T2` | -0.79291 |
| `explicit.stat_3695891184@T1` | -0.78344 |
| `explicit.stat_1509134228@T1` | -0.78217 |
| `explicit.stat_3336890334@T1` | 0.73573 |

### flask.charm — n=15912, R²=-0.5784

intercept: `0.0835`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `2.21862`  ·  corrupted: `1.60878`  ·  quality: `0.00009`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.85988 |
| `explicit.stat_1056492907` | 2.91156 |
| `explicit.stat_828533480@T2` | -2.21865 |
| `explicit.stat_1873752457@T2` | -2.21862 |
| `explicit.stat_388617051@T2` | -2.21861 |
| `explicit.stat_1120862500@T2` | -2.21861 |
| `explicit.stat_1873752457@T1` | -2.21860 |
| `explicit.stat_2676834156@T2` | -2.21860 |
| `explicit.stat_3196823591@T2` | -2.21859 |
| `explicit.stat_2365392475@T2` | -2.21858 |
| `explicit.stat_1366840608@T2` | -2.21815 |
| `explicit.stat_828533480@T1` | -2.21718 |

### weapon.crossbow — n=15367, R²=-1.8047

intercept: `3.8320`  ·  log_price: True  ·  ilvl: `-0.04616`  ·  n_mods: `-0.07429`  ·  n_top_tier: `0.62510`  ·  corrupted: `0.07290`  ·  n_sockets: `0.06087`  ·  quality: `0.01954`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.72814 |
| `explicit.stat_1980802737` | 1.27394 |
| `explicit.stat_2250681686@T2` | -1.19440 |
| `explicit.stat_1202301673@T1` | 1.11629 |
| `explicit.stat_2250681686` | 0.83635 |
| `explicit.stat_709508406@T1` | 0.83539 |
| `explicit.stat_1263695895@T2` | -0.82240 |
| `explicit.stat_1263695895@T1` | -0.79469 |
| `explicit.stat_1037193709@T1` | -0.79105 |
| `explicit.stat_2694482655@T1` | -0.78161 |
| `explicit.stat_709508406@T2` | -0.75957 |
| `explicit.stat_3695891184@T2` | -0.73771 |

### weapon.warstaff — n=10062, R²=-0.3614

intercept: `-10.5447`  ·  log_price: True  ·  ilvl: `0.14414`  ·  n_mods: `-0.23868`  ·  n_top_tier: `0.30027`  ·  corrupted: `0.38497`  ·  n_sockets: `0.18206`  ·  quality: `0.06204`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 1.81880 |
| `desecrated.stat_2527686725@T1` | 1.81880 |
| `crafted.stat_210067635@T2` | 1.47120 |
| `explicit.stat_1037193709@T1` | 0.97135 |
| `rune.stat_243313994` | 0.87773 |
| `explicit.stat_328541901@T1` | -0.84782 |
| `explicit.stat_328541901@T2` | -0.77805 |
| `desecrated.stat_9187492` | 0.73912 |
| `explicit.stat_709508406@T1` | 0.63236 |
| `explicit.stat_9187492@T1` | 0.61447 |
| `explicit.stat_1509134228@T1` | 0.57622 |
| `explicit.stat_1940865751@T1` | -0.55254 |

### weapon.staff — n=9378, R²=-0.3838

intercept: `-15.0005`  ·  log_price: True  ·  ilvl: `0.19479`  ·  n_mods: `-0.13053`  ·  n_top_tier: `0.58916`  ·  corrupted: `0.46483`  ·  n_sockets: `0.27723`  ·  quality: `0.03305`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.05748 |
| `explicit.stat_1545858329@T1` | 1.71076 |
| `explicit.stat_591105508@T1` | 1.55983 |
| `explicit.stat_293638271@T2` | -1.34679 |
| `explicit.stat_124131830@T1` | 1.17545 |
| `explicit.stat_2254480358@T2` | 1.07077 |
| `explicit.stat_124131830@T2` | 0.87024 |
| `explicit.stat_591105508@T2` | 0.85900 |
| `explicit.stat_1600707273@T1` | 0.74878 |
| `explicit.stat_2968503605@T1` | -0.72305 |
| `explicit.stat_274716455@T1` | -0.71464 |
| `explicit.stat_1050105434@T2` | -0.70956 |

### weapon.sceptre — n=9272, R²=-0.3384

intercept: `-19.9028`  ·  log_price: True  ·  ilvl: `0.25523`  ·  n_mods: `-0.06779`  ·  n_top_tier: `0.17239`  ·  corrupted: `0.47674`  ·  n_sockets: `0.29419`  ·  quality: `0.03426`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.88777 |
| `explicit.stat_2162097452@T2` | 1.66365 |
| `explicit.stat_1250712710@T2` | 1.59350 |
| `explicit.stat_3057012405@T1` | 1.26225 |
| `explicit.stat_101878827@T1` | 0.70546 |
| `explicit.stat_2347036682@T1` | 0.68406 |
| `explicit.stat_2347036682@T2` | -0.57547 |
| `explicit.stat_101878827@T2` | 0.55049 |
| `explicit.stat_1250712710@T1` | 0.47785 |
| `explicit.stat_849987426@T1` | 0.45412 |
| `explicit.stat_1263695895@T2` | -0.40659 |
| `explicit.stat_1798257884@T2` | 0.39946 |

### weapon.spear — n=7542, R²=-0.4224

intercept: `-12.0009`  ·  log_price: True  ·  ilvl: `0.16932`  ·  n_mods: `-0.19093`  ·  n_top_tier: `0.85209`  ·  corrupted: `0.10969`  ·  n_sockets: `0.21639`  ·  quality: `0.06434`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -5.16329 |
| `explicit.stat_1202301673@T1` | 1.66456 |
| `explicit.stat_4080418644@T2` | -1.18729 |
| `desecrated.stat_210067635@T1` | -1.15549 |
| `crafted.stat_3035140377` | 1.02929 |
| `explicit.stat_3261801346@T1` | -1.00739 |
| `explicit.stat_691932474@T1` | -0.97786 |
| `explicit.stat_748522257@T2` | -0.94289 |
| `explicit.stat_709508406@T1` | 0.94100 |
| `explicit.stat_3695891184@T2` | -0.92149 |
| `explicit.stat_1940865751@T2` | -0.91848 |
| `explicit.stat_3261801346@T2` | -0.91295 |

### armour.focus — n=6186, R²=-0.3683

intercept: `-12.7895`  ·  log_price: True  ·  ilvl: `0.16879`  ·  n_mods: `-0.18462`  ·  n_top_tier: `0.92195`  ·  corrupted: `0.34766`  ·  n_sockets: `0.43222`  ·  quality: `0.06373`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 6.64171 |
| `explicit.stat_4220027924@T2` | -1.41545 |
| `explicit.stat_2231156303@T2` | -1.32528 |
| `explicit.stat_4220027924@T1` | -1.26451 |
| `explicit.stat_2231156303@T1` | -1.10544 |
| `explicit.stat_3291658075@T1` | -1.05864 |
| `explicit.stat_2923486259@T1` | -1.05833 |
| `explicit.stat_2339757871@T2` | -0.99049 |
| `explicit.stat_737908626@T2` | -0.86021 |
| `explicit.stat_4052037485@T2` | -0.85444 |
| `explicit.stat_3962278098@T2` | -0.83353 |
| `explicit.stat_3372524247@T2` | -0.82722 |

### armour.quiver — n=5806, R²=-0.3193

intercept: `-13.6269`  ·  log_price: True  ·  ilvl: `0.17001`  ·  n_mods: `-0.15013`  ·  n_top_tier: `0.87004`  ·  corrupted: `0.73802`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.85490 |
| `explicit.stat_2463230181@T1` | 3.40495 |
| `explicit.stat_2463230181@T2` | 1.76167 |
| `explicit.stat_681332047@T2` | -1.29674 |
| `explicit.stat_1573130764@T1` | -1.24065 |
| `explicit.stat_803737631@T2` | -1.11481 |
| `explicit.stat_2321178454@T2` | -0.99922 |
| `explicit.stat_803737631@T1` | -0.99843 |
| `explicit.stat_4067062424@T1` | -0.92872 |
| `explicit.stat_1573130764@T2` | -0.91760 |
| `explicit.stat_3261801346@T1` | -0.87521 |
| `explicit.stat_2321178454@T1` | -0.83245 |

### armour.shield — n=5009, R²=-0.4824

intercept: `-10.8318`  ·  log_price: True  ·  ilvl: `0.14508`  ·  n_mods: `-0.12144`  ·  n_top_tier: `0.75167`  ·  corrupted: `-0.28811`  ·  n_sockets: `0.32535`  ·  quality: `0.06036`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.51139 |
| `explicit.stat_3321629045@T2` | -1.30417 |
| `explicit.stat_3484657501@T2` | -1.14316 |
| `explicit.stat_2481353198@T2` | -1.14017 |
| `explicit.stat_3855016469@T1` | -1.13419 |
| `explicit.stat_3033371881@T2` | -1.07184 |
| `explicit.stat_2923486259@T2` | -1.05707 |
| `explicit.stat_2451402625@T1` | -0.97117 |
| `explicit.stat_4095671657@T1` | -0.94635 |
| `explicit.stat_1011760251@T2` | -0.92238 |
| `explicit.stat_2901986750@T1` | -0.91067 |
| `explicit.stat_2923486259@T1` | -0.88919 |

### weapon.twomace — n=4605, R²=-0.4811

intercept: `-9.5942`  ·  log_price: True  ·  ilvl: `0.13246`  ·  n_mods: `-0.20144`  ·  n_top_tier: `0.28976`  ·  corrupted: `-0.11671`  ·  n_sockets: `0.17837`  ·  quality: `0.06394`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.92428 |
| `desecrated.stat_1509134228@T1` | 1.48521 |
| `explicit.stat_1037193709@T1` | -1.33466 |
| `crafted.stat_3035140377` | 0.81533 |
| `explicit.stat_1263695895@T2` | -0.80230 |
| `explicit.stat_387439868@T2` | -0.62160 |
| `explicit.stat_1509134228@T1` | 0.61662 |
| `explicit.stat_691932474@T1` | -0.60150 |
| `explicit.stat_210067635@T2` | 0.58573 |
| `explicit.stat_210067635@T1` | 0.58015 |
| `explicit.stat_3336890334@T1` | -0.55023 |
| `explicit.stat_9187492@T1` | -0.54380 |

## Coverage (listings per base)

- … **Sapphire** — 29084 listings (29034 priced) [0.3–885594757.8 ex]
- … **Emerald** — 28466 listings (28425 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 21780 listings (21755 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10854 listings (10839 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 9545 listings (9524 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 9209 listings (9189 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9092 listings (9084 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8641 listings (8625 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8479 listings (8460 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8317 listings (8305 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7056 listings (7046 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6767 listings (6761 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6742 listings (6736 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6557 listings (6536 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 5951 listings (5944 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 5906 listings (5881 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 5840 listings (5823 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 5814 listings (5803 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 5790 listings (5783 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5763 listings (5737 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5656 listings (5647 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5550 listings (5543 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5320 listings (5317 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5284 listings (5272 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5256 listings (5247 priced) [0.3–398912568423.8 ex]

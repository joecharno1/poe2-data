# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-17T10:49:32+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **577572** (575982 priced in exalted)
- Distinct bases: 987 · distinct mods: 3207 · mod rows: 2734050
- Sold signals: **25350** sold · 326633 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-17T10:41:21+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×26.70** (median |log error| 3.2845)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 80% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×73.97 · ±30% 5% · n=83995
- Premium segment (60ex+): skill **+0.12** · typical error ×346.64 · ±30% 0% · n=56815

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 11861 | ×54.13 | 22% | +0.03 | +0.05 |
| jewel | 11142 | ×10.73 | 4% | +0.07 | +0.10 |
| accessory.amulet | 10871 | ×49.68 | 20% | +0.03 | +0.04 |
| accessory.belt | 8026 | ×28.35 | 21% | +0.05 | +0.08 |
| armour.chest | 7819 | ×22.71 | 24% | +0.06 | +0.09 |
| armour.helmet | 7632 | ×31.77 | 19% | +0.06 | +0.08 |
| armour.boots | 7117 | ×41.19 | 21% | +0.08 | +0.10 |
| armour.gloves | 6969 | ×42.68 | 14% | +0.08 | +0.11 |
| other | 6581 | ×1.87 | 44% | +0.10 | +0.18 |
| weapon.wand | 4306 | ×45.55 | 15% | +0.08 | +0.11 |
| weapon.bow | 3384 | ×32.91 | 14% | +0.14 | +0.15 |
| weapon.crossbow | 3188 | ×40.03 | 16% | +0.09 | +0.13 |
| weapon.warstaff | 2051 | ×31.07 | 9% | +0.15 | +0.13 |
| weapon.staff | 1927 | ×51.17 | 7% | +0.12 | +0.12 |
| weapon.sceptre | 1888 | ×40.06 | 4% | +0.19 | +0.20 |
| weapon.spear | 1496 | ×40.27 | 13% | +0.09 | +0.09 |
| armour.focus | 1269 | ×22.96 | 6% | +0.15 | +0.17 |
| armour.quiver | 1215 | ×27.29 | 7% | +0.14 | +0.16 |
| flask.charm | 1050 | ×22.00 | 31% | +0.05 | +0.07 |
| armour.shield | 1010 | ×19.83 | 7% | +0.05 | +0.05 |
| weapon.twomace | 898 | ×9.31 | 11% | +0.08 | +0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=60843, R²=-0.9438

intercept: `-1.8199`  ·  log_price: True  ·  ilvl: `0.02615`  ·  n_mods: `0.73513`  ·  n_top_tier: `-0.23242`  ·  corrupted: `0.36684`  ·  quality: `0.22467`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.35833 |
| `explicit.stat_2301718443@T1` | 2.67239 |
| `explicit.stat_1805182458@T1` | -2.26455 |
| `explicit.stat_3374165039@T1` | -2.06701 |
| `explicit.stat_3485067555@T1` | 2.02207 |
| `explicit.stat_686254215@T1` | -1.69071 |
| `explicit.stat_1697951953@T1` | -1.66785 |
| `explicit.stat_491450213@T1` | 1.65258 |
| `explicit.stat_3166958180@T1` | -1.60570 |
| `explicit.stat_2523933828@T1` | -1.53120 |
| `explicit.stat_3780644166@T1` | -1.44669 |
| `explicit.stat_239367161@T1` | -1.42393 |

### other — n=55420, R²=-0.6563

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.34677`  ·  corrupted: `0.27788`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2974417149@T1` | 0.37261 |
| `explicit.stat_3299347043@T1` | -0.32213 |
| `explicit.stat_3291658075@T1` | 0.29631 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_2106365538@T1` | -0.12450 |
| `explicit.stat_1050105434@T1` | -0.11261 |
| `implicit.stat_2923486259` | -0.09848 |
| `pseudo.total_chaos_res` | 0.09847 |
| `explicit.stat_2482852589@T1` | -0.09805 |
| `explicit.stat_789117908@T1` | -0.04890 |

### accessory.ring — n=54154, R²=-2.0232

intercept: `3.4785`  ·  log_price: True  ·  ilvl: `-0.04305`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.01391`  ·  corrupted: `0.01983`  ·  n_sockets: `2.18843`  ·  quality: `0.07868`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -1.05484 |
| `explicit.stat_1573130764@T1` | -1.05138 |
| `explicit.stat_1368271171@T2` | -1.03794 |
| `explicit.stat_3299347043@T1` | -1.03733 |
| `explicit.stat_2231156303@T2` | -1.03645 |
| `explicit.stat_1573130764@T2` | -1.03522 |
| `explicit.stat_4220027924@T2` | -1.03517 |
| `explicit.stat_2144192055@T1` | -1.03346 |
| `explicit.stat_1263695895@T2` | -1.03111 |
| `explicit.stat_1368271171@T1` | -1.03002 |
| `explicit.stat_1263695895@T1` | -1.02977 |
| `explicit.stat_803737631@T1` | -1.02945 |

### accessory.amulet — n=49517, R²=-2.1577

intercept: `3.6242`  ·  log_price: True  ·  ilvl: `-0.04445`  ·  n_mods: `-0.02457`  ·  n_top_tier: `0.98052`  ·  corrupted: `0.04682`  ·  n_sockets: `-0.10401`  ·  quality: `0.00006`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.20375 |
| `explicit.stat_2974417149@T1` | -1.07143 |
| `explicit.stat_587431675@T2` | -1.04958 |
| `explicit.stat_472520716@T2` | -1.04439 |
| `explicit.stat_803737631@T1` | -1.03398 |
| `explicit.stat_1050105434@T2` | -1.03150 |
| `explicit.stat_2866361420@T2` | -1.02657 |
| `explicit.stat_2974417149@T2` | -1.02059 |
| `explicit.stat_3299347043@T2` | -1.02055 |
| `explicit.stat_803737631@T2` | -1.01547 |
| `explicit.stat_1671376347@T2` | -1.01082 |
| `explicit.stat_2866361420@T1` | -1.00945 |

### accessory.belt — n=36937, R²=-1.6302

intercept: `3.8950`  ·  log_price: True  ·  ilvl: `-0.04638`  ·  n_mods: `-0.03371`  ·  n_top_tier: `0.88474`  ·  corrupted: `0.79033`  ·  n_sockets: `0.16674`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -0.94992 |
| `explicit.stat_2881298780@T1` | -0.93563 |
| `explicit.stat_4220027924@T2` | -0.93147 |
| `explicit.stat_3299347043@T2` | -0.92162 |
| `explicit.stat_809229260@T2` | -0.91515 |
| `explicit.stat_1389754388@T1` | -0.91231 |
| `explicit.stat_51994685@T1` | -0.90809 |
| `explicit.stat_915769802@T1` | -0.89952 |
| `explicit.stat_3325883026@T1` | -0.89504 |
| `explicit.stat_915769802@T2` | -0.89407 |
| `explicit.stat_3372524247@T2` | -0.89239 |
| `explicit.stat_644456512@T1` | -0.89151 |

### armour.chest — n=36736, R²=-1.7693

intercept: `3.2672`  ·  log_price: True  ·  ilvl: `-0.04022`  ·  n_mods: `-0.01385`  ·  n_top_tier: `0.50497`  ·  corrupted: `0.05376`  ·  n_sockets: `0.02229`  ·  quality: `0.06314`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.61926 |
| `explicit.stat_3981240776@T1` | 0.80270 |
| `explicit.stat_986397080@T2` | -0.54638 |
| `explicit.stat_4080418644@T2` | -0.53897 |
| `explicit.stat_1692879867@T1` | -0.53749 |
| `explicit.stat_915769802@T2` | -0.53484 |
| `explicit.stat_4080418644@T1` | -0.52693 |
| `explicit.stat_2451402625@T2` | -0.52641 |
| `explicit.stat_986397080@T1` | -0.52510 |
| `explicit.stat_3372524247@T2` | -0.52355 |
| `explicit.stat_915769802@T1` | -0.52262 |
| `explicit.stat_1692879867@T2` | -0.51976 |

### armour.helmet — n=35676, R²=-1.6771

intercept: `3.6481`  ·  log_price: True  ·  ilvl: `-0.04586`  ·  n_mods: `-0.02552`  ·  n_top_tier: `0.42081`  ·  corrupted: `0.75134`  ·  n_sockets: `0.06620`  ·  quality: `0.05212`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.98390 |
| `explicit.stat_1263695895@T1` | -0.65604 |
| `explicit.stat_3917489142@T2` | -0.64814 |
| `explicit.stat_2162097452@T2` | -0.58296 |
| `explicit.stat_1263695895@T2` | -0.55020 |
| `explicit.stat_3917489142@T1` | -0.54534 |
| `explicit.stat_4052037485@T2` | -0.51334 |
| `explicit.stat_1999113824@T1` | -0.50827 |
| `crafted.stat_3917489142@T1` | 0.49190 |
| `explicit.stat_3321629045@T2` | -0.47127 |
| `explicit.stat_1062208444@T2` | -0.45592 |
| `explicit.stat_3484657501@T1` | -0.45329 |

### armour.boots — n=33378, R²=-1.7588

intercept: `3.4132`  ·  log_price: True  ·  ilvl: `-0.04174`  ·  n_mods: `-0.01768`  ·  n_top_tier: `0.69183`  ·  corrupted: `-0.00329`  ·  n_sockets: `0.02081`  ·  quality: `0.04998`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.13356 |
| `explicit.stat_2250533757@T1` | 1.35626 |
| `explicit.stat_2339757871@T1` | -0.92204 |
| `explicit.stat_3299347043@T1` | -0.87609 |
| `explicit.stat_3917489142@T2` | -0.81753 |
| `explicit.stat_3299347043@T2` | -0.73319 |
| `explicit.stat_3917489142@T1` | -0.73128 |
| `explicit.stat_2923486259@T2` | -0.72507 |
| `explicit.stat_2160282525@T1` | -0.72494 |
| `explicit.stat_3484657501@T2` | -0.71969 |
| `explicit.stat_1671376347@T2` | -0.71419 |
| `explicit.stat_53045048@T1` | -0.71148 |

### armour.gloves — n=32446, R²=-1.6753

intercept: `3.8568`  ·  log_price: True  ·  ilvl: `-0.04874`  ·  n_mods: `-0.02254`  ·  n_top_tier: `0.60706`  ·  corrupted: `0.04081`  ·  n_sockets: `0.08594`  ·  quality: `0.04555`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 1.76104 |
| `rune.stat_836936635` | 1.17646 |
| `explicit.stat_1671376347@T1` | 0.84654 |
| `explicit.stat_9187492@T2` | -0.83606 |
| `explicit.stat_9187492@T1` | 0.82085 |
| `explicit.stat_3321629045@T2` | -0.79168 |
| `explicit.stat_4052037485@T1` | -0.75968 |
| `explicit.stat_3484657501@T2` | -0.74338 |
| `explicit.stat_2923486259@T1` | -0.72247 |
| `explicit.stat_1754445556@T2` | -0.72040 |
| `explicit.stat_803737631@T2` | -0.70903 |
| `explicit.stat_803737631@T1` | -0.70296 |

### weapon.wand — n=20142, R²=-2.0759

intercept: `3.8093`  ·  log_price: True  ·  ilvl: `-0.04703`  ·  n_mods: `-0.04488`  ·  n_top_tier: `0.60836`  ·  corrupted: `0.08769`  ·  n_sockets: `0.10100`  ·  quality: `0.01211`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.76488 |
| `explicit.stat_4226189338@T1` | 2.56553 |
| `rune.stat_124131830` | -2.22277 |
| `explicit.stat_2254480358@T1` | 2.21731 |
| `explicit.stat_124131830@T1` | 1.82245 |
| `explicit.stat_591105508@T1` | 1.72970 |
| `explicit.stat_736967255@T2` | 1.61459 |
| `crafted.stat_124131830` | 1.23804 |
| `explicit.stat_1600707273@T1` | 1.03847 |
| `explicit.stat_1263695895@T1` | -0.90672 |
| `explicit.stat_1263695895@T2` | -0.87067 |
| `explicit.stat_4226189338@T2` | 0.84648 |

### weapon.bow — n=16151, R²=-1.8749

intercept: `3.8351`  ·  log_price: True  ·  ilvl: `-0.04539`  ·  n_mods: `-0.07359`  ·  n_top_tier: `0.63376`  ·  corrupted: `0.25143`  ·  n_sockets: `0.03764`  ·  quality: `0.03191`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.45831 |
| `desecrated.stat_210067635@T1` | -1.51007 |
| `explicit.stat_1202301673@T1` | 1.46113 |
| `crafted.stat_3035140377` | 1.41550 |
| `explicit.stat_2463230181@T1` | -1.05581 |
| `explicit.stat_2463230181@T2` | -1.02527 |
| `explicit.stat_1263695895@T1` | -1.00539 |
| `explicit.stat_3336890334@T1` | 1.00238 |
| `explicit.stat_1263695895@T2` | -0.96345 |
| `explicit.stat_3695891184@T2` | -0.81916 |
| `explicit.stat_518292764@T2` | -0.81730 |
| `explicit.stat_1037193709@T1` | -0.77066 |

### flask.charm — n=15394, R²=-0.5801

intercept: `0.0636`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `2.48738`  ·  corrupted: `1.86135`  ·  quality: `0.00028`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60590 |
| `explicit.stat_1056492907` | 2.93897 |
| `explicit.stat_828533480@T2` | -2.48741 |
| `explicit.stat_1873752457@T2` | -2.48737 |
| `explicit.stat_388617051@T2` | -2.48737 |
| `explicit.stat_1120862500@T2` | -2.48737 |
| `explicit.stat_2676834156@T2` | -2.48736 |
| `explicit.stat_3196823591@T2` | -2.48736 |
| `explicit.stat_1873752457@T1` | -2.48735 |
| `explicit.stat_2365392475@T2` | -2.48734 |
| `explicit.stat_828533480@T1` | -2.48536 |
| `explicit.stat_1366840608@T2` | -2.48382 |

### weapon.crossbow — n=15136, R²=-1.8596

intercept: `4.0054`  ·  log_price: True  ·  ilvl: `-0.04882`  ·  n_mods: `-0.05215`  ·  n_top_tier: `0.66264`  ·  corrupted: `0.02823`  ·  n_sockets: `0.04990`  ·  quality: `0.02941`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -2.31415 |
| `explicit.stat_1980802737@T2` | -1.80686 |
| `explicit.stat_2250681686` | 1.76935 |
| `explicit.stat_1202301673@T1` | 1.43840 |
| `explicit.stat_1980802737` | 1.22034 |
| `explicit.stat_1263695895@T1` | -0.88462 |
| `explicit.stat_1263695895@T2` | -0.85274 |
| `crafted.stat_3035140377` | 0.78805 |
| `explicit.stat_1509134228@T2` | -0.78744 |
| `explicit.stat_1940865751@T1` | -0.76030 |
| `explicit.stat_2694482655@T1` | -0.75482 |
| `explicit.stat_3695891184@T1` | -0.74305 |

### weapon.warstaff — n=9792, R²=-0.3637

intercept: `-9.8147`  ·  log_price: True  ·  ilvl: `0.13533`  ·  n_mods: `-0.22448`  ·  n_top_tier: `0.25698`  ·  corrupted: `0.29943`  ·  n_sockets: `0.16042`  ·  quality: `0.06179`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 2.15626 |
| `desecrated.stat_2231156303@T1` | 2.15626 |
| `desecrated.stat_3291658075@T1` | -1.54167 |
| `desecrated.stat_473429811@T1` | -1.54167 |
| `crafted.stat_210067635@T2` | 1.19171 |
| `explicit.stat_1037193709@T1` | 0.95444 |
| `rune.stat_243313994` | 0.92753 |
| `explicit.stat_9187492@T1` | 0.71960 |
| `desecrated.stat_9187492` | 0.70430 |
| `explicit.stat_328541901@T2` | -0.67628 |
| `explicit.stat_328541901@T1` | -0.66726 |
| `explicit.stat_748522257@T2` | 0.63255 |

### weapon.staff — n=9144, R²=-0.396

intercept: `-14.3575`  ·  log_price: True  ·  ilvl: `0.18738`  ·  n_mods: `-0.15651`  ·  n_top_tier: `0.50853`  ·  corrupted: `0.43668`  ·  n_sockets: `0.27221`  ·  quality: `0.04358`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.82925 |
| `explicit.stat_4226189338@T1` | 1.72187 |
| `explicit.stat_591105508@T1` | 1.40859 |
| `explicit.stat_293638271@T2` | -1.18597 |
| `explicit.stat_2254480358@T2` | 1.12230 |
| `explicit.stat_124131830@T1` | 1.09057 |
| `explicit.stat_2254480358@T1` | 0.85490 |
| `explicit.stat_124131830@T2` | 0.79511 |
| `explicit.stat_2505884597@T2` | -0.75708 |
| `explicit.stat_3962278098@T2` | 0.68851 |
| `explicit.stat_4226189338@T2` | 0.64902 |
| `explicit.stat_591105508@T2` | 0.62662 |

### weapon.sceptre — n=9019, R²=-0.3412

intercept: `-19.6018`  ·  log_price: True  ·  ilvl: `0.25118`  ·  n_mods: `-0.08906`  ·  n_top_tier: `0.28534`  ·  corrupted: `0.33247`  ·  n_sockets: `0.31182`  ·  quality: `0.04000`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.68074 |
| `explicit.stat_1250712710@T2` | 1.55270 |
| `explicit.stat_2162097452@T2` | 1.50239 |
| `explicit.stat_3057012405@T1` | 1.02293 |
| `explicit.stat_101878827@T1` | 0.85661 |
| `explicit.stat_2347036682@T1` | 0.63502 |
| `explicit.stat_849987426@T1` | 0.61388 |
| `explicit.stat_2347036682@T2` | -0.59832 |
| `explicit.stat_1263695895@T2` | -0.55809 |
| `explicit.stat_1574590649@T1` | -0.53475 |
| `explicit.stat_101878827@T2` | 0.49603 |
| `explicit.stat_289128254@T2` | -0.42127 |

### weapon.spear — n=7371, R²=-0.4256

intercept: `-11.4585`  ·  log_price: True  ·  ilvl: `0.16134`  ·  n_mods: `-0.14961`  ·  n_top_tier: `0.78884`  ·  corrupted: `-0.26551`  ·  n_sockets: `0.24744`  ·  quality: `0.05970`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.21870 |
| `explicit.stat_1202301673@T1` | 1.79572 |
| `explicit.stat_1509134228@T1` | 1.31520 |
| `explicit.stat_9187492@T1` | 1.27166 |
| `crafted.stat_3035140377` | 1.10024 |
| `explicit.stat_1037193709@T1` | -0.92962 |
| `explicit.stat_4080418644@T2` | -0.92817 |
| `explicit.stat_9187492@T2` | -0.92356 |
| `explicit.stat_3261801346@T1` | -0.87985 |
| `explicit.stat_691932474@T1` | -0.85277 |
| `explicit.stat_3261801346@T2` | -0.77582 |
| `explicit.stat_709508406@T1` | 0.76868 |

### armour.focus — n=6047, R²=-0.3735

intercept: `-12.2290`  ·  log_price: True  ·  ilvl: `0.16150`  ·  n_mods: `-0.16089`  ·  n_top_tier: `0.77439`  ·  corrupted: `0.30426`  ·  n_sockets: `0.42840`  ·  quality: `0.07051`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 7.32337 |
| `explicit.stat_4220027924@T2` | -1.29199 |
| `explicit.stat_3962278098@T1` | -1.17626 |
| `explicit.stat_2231156303@T2` | -0.92703 |
| `explicit.stat_3291658075@T1` | -0.89125 |
| `explicit.stat_2339757871@T2` | -0.88769 |
| `explicit.stat_2891184298@T2` | -0.87787 |
| `explicit.stat_737908626@T2` | -0.85381 |
| `explicit.stat_2974417149@T1` | -0.84583 |
| `explicit.stat_4052037485@T2` | -0.77727 |
| `explicit.stat_2231156303@T1` | -0.73637 |
| `explicit.stat_2339757871@T1` | -0.72347 |

### armour.quiver — n=5669, R²=-0.3158

intercept: `-13.7753`  ·  log_price: True  ·  ilvl: `0.16943`  ·  n_mods: `-0.14322`  ·  n_top_tier: `0.84579`  ·  corrupted: `0.82907`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.78680 |
| `explicit.stat_2463230181@T1` | 3.46275 |
| `explicit.stat_2463230181@T2` | 1.79801 |
| `explicit.stat_681332047@T2` | -1.30380 |
| `explicit.stat_1573130764@T1` | -1.16275 |
| `explicit.stat_2321178454@T2` | -1.08577 |
| `explicit.stat_803737631@T2` | -1.06686 |
| `explicit.stat_4067062424@T1` | -0.99250 |
| `explicit.stat_1573130764@T2` | -0.93860 |
| `explicit.stat_2321178454@T1` | -0.88068 |
| `explicit.stat_803737631@T1` | -0.84574 |
| `explicit.stat_3261801346@T1` | -0.77449 |

### armour.shield — n=4919, R²=-0.4941

intercept: `-10.5153`  ·  log_price: True  ·  ilvl: `0.14154`  ·  n_mods: `-0.10535`  ·  n_top_tier: `0.67285`  ·  corrupted: `-0.33498`  ·  n_sockets: `0.24898`  ·  quality: `0.06687`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.33462 |
| `explicit.stat_328541901@T1` | -1.17909 |
| `explicit.stat_328541901@T2` | -1.17237 |
| `explicit.stat_2339757871@T1` | -1.11765 |
| `explicit.stat_3484657501@T2` | -1.10173 |
| `explicit.stat_3321629045@T2` | -1.07217 |
| `explicit.stat_3033371881@T2` | -1.03245 |
| `explicit.stat_2481353198@T2` | -0.98348 |
| `explicit.stat_2901986750@T1` | -0.91062 |
| `explicit.stat_1671376347@T1` | -0.88302 |
| `explicit.stat_2451402625@T1` | -0.85978 |
| `explicit.stat_2923486259@T2` | -0.84969 |

### weapon.twomace — n=4515, R²=-0.4946

intercept: `-9.1919`  ·  log_price: True  ·  ilvl: `0.12732`  ·  n_mods: `-0.18201`  ·  n_top_tier: `0.49875`  ·  corrupted: `-0.00787`  ·  n_sockets: `0.14634`  ·  quality: `0.05507`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -5.63105 |
| `desecrated.stat_1509134228@T1` | 1.97064 |
| `explicit.stat_1037193709@T1` | -1.61349 |
| `explicit.stat_387439868@T2` | -0.96356 |
| `crafted.stat_3035140377` | 0.93473 |
| `explicit.stat_1037193709@T2` | -0.85166 |
| `explicit.stat_9187492@T1` | -0.84125 |
| `explicit.stat_1263695895@T2` | -0.81764 |
| `explicit.stat_691932474@T1` | -0.81693 |
| `explicit.stat_3336890334@T1` | -0.62810 |
| `explicit.stat_669069897@T2` | -0.59436 |
| `explicit.stat_669069897@T1` | -0.57959 |

## Coverage (listings per base)

- … **Sapphire** — 28217 listings (28169 priced) [0.3–885594757.8 ex]
- … **Emerald** — 27660 listings (27621 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 21131 listings (21107 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10648 listings (10633 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 9225 listings (9207 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8932 listings (8913 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8824 listings (8816 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8392 listings (8376 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8238 listings (8220 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8123 listings (8112 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6856 listings (6846 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6574 listings (6568 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6543 listings (6537 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6454 listings (6435 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 5788 listings (5781 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 5758 listings (5734 priced) [0.3–398912568423.8 ex]
- … **Jade Amulet** — 5663 listings (5652 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 5662 listings (5645 priced) [0.2–24532814.5 ex]
- … **Amber Amulet** — 5637 listings (5630 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5584 listings (5563 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5472 listings (5463 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5378 listings (5371 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5171 listings (5169 priced) [0.3–3985176410.3 ex]
- … **Heavy Belt** — 5130 listings (5122 priced) [0.3–398912568423.8 ex]
- … **Lunar Amulet** — 5123 listings (5111 priced) [0.3–91750808.2 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-13T22:39:07+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **444183** (443310 priced in exalted)
- Distinct bases: 977 · distinct mods: 3019 · mod rows: 2111672
- Sold signals: **27231** sold · 243130 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-13T22:28:46+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×26.60** (median |log error| 3.2808)
- Within ±30% of asking price: **15%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×71.74 · ±30% 5% · n=64013
- Premium segment (60ex+): skill **+0.11** · typical error ×267.17 · ±30% 0% · n=42133

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 8716 | ×52.86 | 20% | +0.03 | +0.05 |
| accessory.amulet | 8128 | ×53.63 | 22% | +0.02 | +0.02 |
| jewel | 8003 | ×8.46 | 7% | +0.02 | +0.05 |
| accessory.belt | 6341 | ×23.49 | 4% | +0.05 | +0.06 |
| armour.chest | 6198 | ×20.50 | 8% | +0.10 | +0.11 |
| armour.helmet | 6064 | ×20.11 | 6% | +0.08 | +0.12 |
| armour.boots | 5659 | ×25.00 | 15% | +0.07 | +0.10 |
| armour.gloves | 5526 | ×34.35 | 10% | +0.08 | +0.10 |
| other | 4967 | ×9.97 | 38% | +0.08 | +0.14 |
| weapon.wand | 3631 | ×38.80 | 20% | +0.07 | +0.07 |
| weapon.bow | 2931 | ×29.64 | 16% | +0.09 | +0.10 |
| weapon.crossbow | 2754 | ×22.36 | 19% | +0.10 | +0.14 |
| weapon.warstaff | 1586 | ×49.76 | 18% | +0.09 | +0.11 |
| weapon.staff | 1470 | ×71.69 | 18% | +0.07 | +0.08 |
| weapon.sceptre | 1450 | ×62.58 | 13% | +0.09 | +0.10 |
| weapon.spear | 1215 | ×47.49 | 20% | +0.08 | +0.07 |
| armour.focus | 983 | ×44.29 | 10% | +0.13 | +0.12 |
| armour.quiver | 963 | ×32.42 | 14% | +0.06 | +0.11 |
| armour.shield | 799 | ×13.88 | 18% | +0.03 | +0.04 |
| weapon.twomace | 709 | ×39.63 | 16% | +0.06 | +0.08 |
| flask.charm | 692 | ×10.00 | 36% | +0.01 | +0.02 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=43531, R²=-0.5046

intercept: `1.6013`  ·  log_price: True  ·  ilvl: `0.00010`  ·  n_mods: `0.02780`  ·  n_top_tier: `0.54901`  ·  corrupted: `0.52358`  ·  n_sockets: `-0.00011`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 2.10372 |
| `explicit.stat_2891184298@T1` | 0.96120 |
| `explicit.stat_1050105434@T1` | -0.78524 |
| `explicit.stat_2974417149@T1` | 0.73157 |
| `explicit.stat_3917489142@T1` | 0.69327 |
| `explicit.stat_789117908@T1` | -0.65593 |
| `implicit.stat_1379411836` | -0.23278 |
| `implicit.stat_4041853756` | 0.22747 |
| `implicit.stat_3879011313` | 0.22747 |
| `explicit.stat_3299347043@T1` | -0.17361 |
| `implicit.stat_2923486259` | -0.12239 |
| `pseudo.total_chaos_res` | 0.11998 |

### jewel — n=42603, R²=-0.7677

intercept: `-1.4826`  ·  log_price: True  ·  ilvl: `0.03235`  ·  n_mods: `0.45745`  ·  n_top_tier: `-0.15811`  ·  corrupted: `0.20857`  ·  quality: `0.22933`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.78597 |
| `explicit.stat_1697447343@T1` | -2.77675 |
| `explicit.stat_2301718443@T1` | 2.73560 |
| `explicit.stat_153777645@T1` | -2.59754 |
| `explicit.stat_627767961@T1` | -2.49383 |
| `explicit.stat_1315743832@T1` | 2.25629 |
| `explicit.stat_3485067555@T1` | 2.25207 |
| `explicit.stat_3174700878@T1` | 2.18491 |
| `explicit.stat_3780644166@T1` | -2.06857 |
| `explicit.stat_3741323227@T1` | -1.96348 |
| `explicit.stat_795138349@T1` | -1.87825 |
| `explicit.stat_3473929743@T1` | -1.82489 |

### accessory.ring — n=39834, R²=-1.9567

intercept: `3.5931`  ·  log_price: True  ·  ilvl: `-0.04415`  ·  n_mods: `0.00224`  ·  n_top_tier: `0.41138`  ·  corrupted: `0.32377`  ·  n_sockets: `-0.10274`  ·  quality: `0.04835`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -0.44837 |
| `explicit.stat_3325883026@T1` | -0.44410 |
| `explicit.stat_3962278098@T2` | -0.44036 |
| `explicit.stat_1573130764@T1` | -0.43808 |
| `explicit.stat_1263695895@T1` | -0.43562 |
| `explicit.stat_3032590688@T2` | -0.43522 |
| `explicit.stat_3291658075@T2` | -0.43351 |
| `explicit.stat_3917489142@T2` | -0.43277 |
| `explicit.stat_2144192055@T1` | -0.43166 |
| `explicit.stat_1368271171@T2` | -0.43105 |
| `explicit.stat_1379411836@T1` | -0.42914 |
| `explicit.stat_4220027924@T2` | -0.42833 |

### accessory.amulet — n=37107, R²=-2.1184

intercept: `3.9001`  ·  log_price: True  ·  ilvl: `-0.04738`  ·  n_mods: `-0.02166`  ·  n_top_tier: `0.97216`  ·  corrupted: `0.04384`  ·  n_sockets: `-0.05099`  ·  quality: `0.00142`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T2` | -1.19440 |
| `explicit.stat_2748665614@T1` | -1.08708 |
| `explicit.stat_2748665614@T2` | -1.06783 |
| `explicit.stat_3299347043@T2` | -1.05165 |
| `explicit.stat_3299347043@T1` | -1.05127 |
| `explicit.stat_472520716@T1` | -1.02728 |
| `explicit.stat_3917489142@T2` | -1.02635 |
| `explicit.stat_2901986750@T1` | -1.02408 |
| `explicit.stat_1050105434@T2` | -1.01464 |
| `explicit.stat_3917489142@T1` | -1.01345 |
| `explicit.stat_472520716@T2` | -1.00894 |
| `explicit.stat_2974417149@T1` | -1.00821 |

### accessory.belt — n=29023, R²=-0.7599

intercept: `7.0626`  ·  log_price: True  ·  ilvl: `-0.06052`  ·  n_mods: `-0.41451`  ·  n_top_tier: `1.09110`  ·  corrupted: `1.21197`  ·  n_sockets: `0.50782`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.69100 |
| `explicit.stat_51994685@T1` | -1.68638 |
| `explicit.stat_2881298780@T1` | -1.67299 |
| `explicit.stat_3299347043@T1` | -1.48771 |
| `explicit.stat_809229260@T2` | -1.35031 |
| `explicit.stat_3299347043@T2` | -1.30714 |
| `explicit.stat_1671376347@T2` | -1.23561 |
| `explicit.stat_1389754388@T2` | -1.22840 |
| `explicit.stat_644456512@T1` | -1.22779 |
| `explicit.stat_4220027924@T2` | -1.20668 |
| `explicit.stat_3585532255@T2` | -1.20261 |
| `explicit.stat_1050105434@T2` | -1.19640 |

### armour.chest — n=28724, R²=-1.1329

intercept: `4.4826`  ·  log_price: True  ·  ilvl: `-0.05339`  ·  n_mods: `-0.08612`  ·  n_top_tier: `0.51214`  ·  corrupted: `0.38620`  ·  n_sockets: `0.09001`  ·  quality: `0.03246`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.04700 |
| `explicit.stat_3981240776@T1` | 0.96509 |
| `explicit.stat_4080418644@T1` | -0.75471 |
| `explicit.stat_915769802@T2` | -0.71716 |
| `explicit.stat_3484657501@T1` | -0.68866 |
| `explicit.stat_124859000@T2` | -0.65182 |
| `explicit.stat_915769802@T1` | -0.62607 |
| `explicit.stat_4080418644@T2` | -0.62042 |
| `explicit.stat_986397080@T2` | -0.61713 |
| `explicit.stat_3301100256@T1` | -0.60114 |
| `explicit.stat_3321629045@T1` | -0.59868 |
| `explicit.stat_2881298780@T2` | -0.59220 |

### armour.helmet — n=28065, R²=-0.9918

intercept: `4.0084`  ·  log_price: True  ·  ilvl: `-0.05027`  ·  n_mods: `-0.08736`  ·  n_top_tier: `0.47556`  ·  corrupted: `0.66572`  ·  n_sockets: `0.11379`  ·  quality: `0.04585`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.81147 |
| `explicit.stat_2339757871@T1` | -2.64106 |
| `explicit.stat_1263695895@T1` | -1.22145 |
| `explicit.stat_53045048@T2` | -0.88292 |
| `explicit.stat_53045048@T1` | -0.85114 |
| `explicit.stat_1999113824@T1` | -0.83367 |
| `explicit.stat_1263695895@T2` | -0.75970 |
| `explicit.stat_803737631@T2` | -0.70563 |
| `explicit.stat_3917489142@T2` | -0.69136 |
| `explicit.stat_328541901@T2` | -0.65317 |
| `explicit.stat_124859000@T2` | -0.61320 |
| `explicit.stat_2162097452@T2` | -0.59143 |

### armour.boots — n=26320, R²=-1.4584

intercept: `4.1235`  ·  log_price: True  ·  ilvl: `-0.05031`  ·  n_mods: `-0.03085`  ·  n_top_tier: `0.66780`  ·  corrupted: `0.18215`  ·  n_sockets: `-0.00383`  ·  quality: `0.02990`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.53106 |
| `explicit.stat_2923486259@T2` | -0.90115 |
| `explicit.stat_3917489142@T2` | -0.88212 |
| `explicit.stat_2339757871@T1` | -0.87936 |
| `desecrated.stat_2250533757@T2` | -0.87779 |
| `explicit.stat_3917489142@T1` | -0.84292 |
| `explicit.stat_4052037485@T2` | -0.81971 |
| `explicit.stat_53045048@T1` | -0.77958 |
| `explicit.stat_3299347043@T1` | -0.77954 |
| `explicit.stat_1062208444@T2` | -0.75195 |
| `explicit.stat_3362812763@T1` | -0.74819 |
| `explicit.stat_2160282525@T1` | -0.72959 |

### armour.gloves — n=25651, R²=-1.427

intercept: `4.1428`  ·  log_price: True  ·  ilvl: `-0.05374`  ·  n_mods: `-0.03096`  ·  n_top_tier: `0.49882`  ·  corrupted: `0.03928`  ·  n_sockets: `0.10533`  ·  quality: `0.03848`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.67295 |
| `explicit.stat_3484657501@T2` | -1.16437 |
| `explicit.stat_9187492@T1` | 0.86641 |
| `explicit.stat_3484657501@T1` | -0.84397 |
| `explicit.stat_803737631@T2` | -0.78492 |
| `explicit.stat_9187492@T2` | -0.77311 |
| `explicit.stat_1671376347@T1` | 0.75431 |
| `rune.stat_201332984` | 0.74028 |
| `explicit.stat_2923486259@T1` | -0.70299 |
| `explicit.stat_3917489142@T2` | -0.69333 |
| `explicit.stat_3321629045@T1` | -0.67584 |
| `explicit.stat_2923486259@T2` | -0.64604 |

### weapon.wand — n=16844, R²=-2.2506

intercept: `3.8219`  ·  log_price: True  ·  ilvl: `-0.04763`  ·  n_mods: `-0.00886`  ·  n_top_tier: `0.10970`  ·  corrupted: `-0.07559`  ·  n_sockets: `0.03826`  ·  quality: `-0.00210`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.00411 |
| `rune.stat_124131830` | -2.88486 |
| `explicit.stat_2254480358@T1` | 2.73416 |
| `explicit.stat_591105508@T1` | 2.25314 |
| `explicit.stat_124131830@T1` | 2.21803 |
| `explicit.stat_4226189338@T1` | 2.18595 |
| `explicit.stat_736967255@T2` | 1.65388 |
| `explicit.stat_2768835289@T2` | 1.38592 |
| `crafted.stat_124131830` | 1.22347 |
| `explicit.stat_2254480358@T2` | 0.86658 |
| `explicit.stat_737908626@T1` | -0.19105 |
| `explicit.stat_2968503605@T1` | -0.18977 |

### weapon.bow — n=13701, R²=-1.9662

intercept: `3.3974`  ·  log_price: True  ·  ilvl: `-0.04126`  ·  n_mods: `-0.03248`  ·  n_top_tier: `0.71728`  ·  corrupted: `-0.04504`  ·  n_sockets: `-0.00705`  ·  quality: `0.03217`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.99388 |
| `explicit.stat_1202301673@T1` | 1.43789 |
| `crafted.stat_3035140377` | 1.26420 |
| `explicit.stat_1263695895@T1` | -0.85638 |
| `explicit.stat_1509134228@T1` | -0.78690 |
| `explicit.stat_55876295@T1` | -0.78584 |
| `explicit.stat_1368271171@T2` | -0.77979 |
| `explicit.stat_3695891184@T2` | -0.77589 |
| `explicit.stat_669069897@T1` | -0.77464 |
| `explicit.stat_821021828@T2` | -0.77138 |
| `explicit.stat_518292764@T2` | -0.76910 |
| `explicit.stat_1037193709@T2` | -0.76908 |

### weapon.crossbow — n=12906, R²=-1.8512

intercept: `3.5342`  ·  log_price: True  ·  ilvl: `-0.04356`  ·  n_mods: `-0.01737`  ·  n_top_tier: `0.76436`  ·  corrupted: `-0.01395`  ·  n_sockets: `0.04589`  ·  quality: `0.01068`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.97295 |
| `explicit.stat_2250681686@T2` | -1.46987 |
| `explicit.stat_709508406@T1` | 1.42800 |
| `explicit.stat_1980802737` | 1.14791 |
| `explicit.stat_1202301673@T2` | -1.12855 |
| `explicit.stat_1263695895@T2` | -0.97579 |
| `explicit.stat_1544773869@T2` | -0.97449 |
| `explicit.stat_1263695895@T1` | -0.93088 |
| `explicit.stat_1202301673@T1` | 0.92261 |
| `explicit.stat_3695891184@T1` | -0.88819 |
| `crafted.stat_3035140377` | 0.86850 |
| `explicit.stat_1509134228@T2` | -0.86601 |

### flask.charm — n=10783, R²=-0.488

intercept: `0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `1.59349`  ·  corrupted: `1.89462`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.37339 |
| `explicit.stat_1056492907` | 3.39888 |
| `explicit.stat_828533480@T2` | -1.59350 |
| `explicit.stat_1120862500@T2` | -1.59349 |
| `explicit.stat_3196823591@T2` | -1.59349 |
| `explicit.stat_1366840608@T2` | -1.59349 |
| `explicit.stat_1873752457@T1` | -1.59349 |
| `explicit.stat_1873752457@T2` | -1.59349 |
| `explicit.stat_2676834156@T2` | -1.59348 |
| `explicit.stat_828533480@T1` | -1.59348 |
| `explicit.stat_388617051@T2` | -1.59347 |
| `explicit.stat_2541588185@T2` | -1.59347 |

### weapon.warstaff — n=7495, R²=-0.5402

intercept: `-2.8213`  ·  log_price: True  ·  ilvl: `0.04020`  ·  n_mods: `-0.11578`  ·  n_top_tier: `0.62936`  ·  corrupted: `0.15944`  ·  n_sockets: `0.05984`  ·  quality: `0.07019`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.32307 |
| `explicit.stat_328541901@T2` | -0.90400 |
| `explicit.stat_328541901@T1` | -0.87931 |
| `explicit.stat_691932474@T2` | -0.73237 |
| `explicit.stat_210067635@T1` | -0.71468 |
| `explicit.stat_55876295@T1` | -0.70448 |
| `explicit.stat_3336890334@T2` | -0.68683 |
| `explicit.stat_55876295@T2` | -0.68311 |
| `explicit.stat_1940865751@T1` | -0.65626 |
| `explicit.stat_1037193709@T1` | 0.64482 |
| `explicit.stat_3336890334@T1` | -0.63483 |
| `explicit.stat_1263695895@T1` | -0.62781 |

### weapon.sceptre — n=6941, R²=-0.4803

intercept: `-11.6002`  ·  log_price: True  ·  ilvl: `0.14500`  ·  n_mods: `-0.02440`  ·  n_top_tier: `0.37714`  ·  corrupted: `0.30558`  ·  n_sockets: `0.22273`  ·  quality: `0.08721`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.05976 |
| `explicit.stat_2162097452@T2` | 1.37761 |
| `explicit.stat_4080418644@T1` | -0.88506 |
| `explicit.stat_1574590649@T2` | -0.81656 |
| `explicit.stat_1263695895@T2` | -0.71087 |
| `explicit.stat_2347036682@T2` | -0.66486 |
| `explicit.stat_1263695895@T1` | -0.64412 |
| `explicit.stat_2854751904@T2` | -0.61274 |
| `explicit.stat_4080418644@T2` | -0.59752 |
| `explicit.stat_289128254@T2` | -0.55520 |
| `explicit.stat_1050105434@T2` | -0.53733 |
| `explicit.stat_770672621@T1` | -0.43040 |

### weapon.staff — n=6912, R²=-0.6102

intercept: `-4.6799`  ·  log_price: True  ·  ilvl: `0.05917`  ·  n_mods: `-0.02632`  ·  n_top_tier: `0.27687`  ·  corrupted: `0.09379`  ·  n_sockets: `0.13489`  ·  quality: `0.05032`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.01564 |
| `explicit.stat_124131830@T1` | 1.82165 |
| `explicit.stat_1545858329@T1` | 1.70418 |
| `explicit.stat_2254480358@T1` | 1.40314 |
| `explicit.stat_2768835289@T2` | 1.36325 |
| `rune.stat_124131830` | 1.10652 |
| `explicit.stat_1600707273@T1` | 0.99204 |
| `explicit.stat_3291658075@T2` | 0.97661 |
| `explicit.stat_2254480358@T2` | 0.82254 |
| `explicit.stat_3962278098@T2` | 0.54262 |
| `explicit.stat_2974417149@T1` | -0.47679 |
| `crafted.stat_124131830` | 0.47569 |

### weapon.spear — n=5860, R²=-0.6608

intercept: `-2.9897`  ·  log_price: True  ·  ilvl: `0.03942`  ·  n_mods: `-0.01881`  ·  n_top_tier: `0.32541`  ·  corrupted: `-0.08849`  ·  n_sockets: `0.07168`  ·  quality: `0.10810`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T1` | 2.67483 |
| `explicit.stat_1202301673@T1` | 2.31950 |
| `crafted.stat_210067635@T2` | -1.74148 |
| `crafted.stat_3035140377` | 1.11265 |
| `explicit.stat_210067635@T1` | 0.84230 |
| `explicit.stat_1509134228@T1` | 0.67907 |
| `explicit.stat_55876295@T1` | -0.42863 |
| `explicit.stat_55876295@T2` | -0.37363 |
| `explicit.stat_1263695895@T2` | -0.34968 |
| `explicit.stat_748522257@T1` | -0.34385 |
| `explicit.stat_748522257@T2` | -0.33827 |
| `explicit.stat_1509134228@T2` | -0.31834 |

### armour.focus — n=4783, R²=-0.4601

intercept: `-9.2272`  ·  log_price: True  ·  ilvl: `0.11392`  ·  n_mods: `-0.05873`  ·  n_top_tier: `0.85917`  ·  corrupted: `0.67607`  ·  n_sockets: `0.40151`  ·  quality: `0.07641`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 5.62883 |
| `explicit.stat_4220027924@T2` | -1.22409 |
| `explicit.stat_4220027924@T1` | -1.14589 |
| `explicit.stat_2923486259@T1` | -1.09176 |
| `explicit.stat_3962278098@T1` | -1.06242 |
| `explicit.stat_2891184298@T2` | -0.96050 |
| `explicit.stat_328541901@T2` | -0.95311 |
| `explicit.stat_736967255@T2` | -0.94692 |
| `crafted.stat_737908626@T2` | -0.94520 |
| `explicit.stat_737908626@T2` | -0.93465 |
| `explicit.stat_3962278098@T2` | -0.89672 |
| `explicit.stat_2974417149@T1` | -0.88151 |

### armour.quiver — n=4449, R²=-0.4636

intercept: `-8.3949`  ·  log_price: True  ·  ilvl: `0.10181`  ·  n_mods: `-0.02896`  ·  n_top_tier: `0.67494`  ·  corrupted: `0.48475`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 12.30755 |
| `explicit.stat_2463230181@T1` | 2.48163 |
| `explicit.stat_2463230181@T2` | 1.33399 |
| `explicit.stat_2321178454@T2` | -1.00325 |
| `explicit.stat_1573130764@T1` | -0.98191 |
| `explicit.stat_2194114101@T2` | -0.95302 |
| `explicit.stat_681332047@T2` | -0.92189 |
| `desecrated.stat_3932115504` | -0.82789 |
| `explicit.stat_3261801346@T1` | -0.80127 |
| `explicit.stat_1573130764@T2` | -0.78769 |
| `explicit.stat_4067062424@T1` | -0.75010 |
| `explicit.stat_1368271171@T2` | -0.71045 |

### armour.shield — n=3911, R²=-0.5784

intercept: `-6.4653`  ·  log_price: True  ·  ilvl: `0.08193`  ·  n_mods: `-0.02327`  ·  n_top_tier: `0.61675`  ·  corrupted: `0.29742`  ·  n_sockets: `0.05539`  ·  quality: `0.05092`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.58405 |
| `explicit.stat_2339757871@T1` | -1.08667 |
| `explicit.stat_1011760251@T1` | -1.07625 |
| `explicit.stat_1011760251@T2` | -0.96533 |
| `explicit.stat_2881298780@T1` | -0.91791 |
| `explicit.stat_2481353198@T2` | -0.91528 |
| `explicit.stat_328541901@T1` | -0.89787 |
| `explicit.stat_2481353198@T1` | -0.85694 |
| `explicit.stat_328541901@T2` | -0.81882 |
| `explicit.stat_3033371881@T1` | 0.79369 |
| `explicit.stat_2881298780@T2` | -0.77194 |
| `explicit.stat_3372524247@T2` | -0.76726 |

### weapon.twomace — n=3557, R²=-0.5105

intercept: `-9.2581`  ·  log_price: True  ·  ilvl: `0.12063`  ·  n_mods: `-0.09374`  ·  n_top_tier: `0.31864`  ·  corrupted: `0.73962`  ·  n_sockets: `0.12888`  ·  quality: `0.04119`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.93556 |
| `desecrated.stat_1509134228@T1` | 2.66854 |
| `explicit.stat_210067635@T1` | 1.22003 |
| `crafted.stat_3035140377` | 1.09683 |
| `explicit.stat_1037193709@T1` | -1.07280 |
| `explicit.stat_1509134228@T1` | 0.85742 |
| `explicit.stat_387439868@T2` | -0.75493 |
| `explicit.stat_3336890334@T1` | -0.72301 |
| `explicit.stat_821021828@T2` | -0.71517 |
| `explicit.stat_1037193709@T2` | -0.59816 |
| `explicit.stat_709508406@T1` | -0.54309 |
| `explicit.stat_518292764@T2` | -0.53395 |

## Coverage (listings per base)

- … **Sapphire** — 20009 listings (19982 priced) [0.3–7553463.8 ex]
- … **Emerald** — 19728 listings (19704 priced) [0.3–7553463.8 ex]
- … **Ruby** — 15121 listings (15109 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 8558 listings (8549 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 6848 listings (6839 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 6694 listings (6681 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 6604 listings (6599 priced) [0.2–19945827.9 ex]
- … **Stellar Amulet** — 6324 listings (6320 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 6288 listings (6278 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 6148 listings (6139 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5342 listings (5328 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5110 listings (5104 priced) [0.2–307202867.9 ex]
- … **Ruby Ring** — 4930 listings (4928 priced) [0.2–37474957.5 ex]
- … **Topaz Ring** — 4924 listings (4920 priced) [0.3–307202867.9 ex]
- … **Plate Belt** — 4491 listings (4479 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4438 listings (4434 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4338 listings (4331 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4315 listings (4313 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4270 listings (4265 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4209 listings (4205 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4125 listings (4121 priced) [0.3–4275054.0 ex]
- … **Obliterator Bow** — 4112 listings (4100 priced) [0.3–42622633798.0 ex]
- … **Heavy Belt** — 4022 listings (4020 priced) [0.3–2608914286.6 ex]
- … **Pearl Ring** — 3939 listings (3935 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 3883 listings (3883 priced) [0.3–123132003.2 ex]

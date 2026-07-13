# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-13T19:48:01+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **438233** (437380 priced in exalted)
- Distinct bases: 974 · distinct mods: 3006 · mod rows: 2083910
- Sold signals: **27345** sold · 239408 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-13T19:35:38+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×18.45** (median |log error| 2.9153)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.05** · typical error ×47.34 · ±30% 9% · n=63384
- Premium segment (60ex+): skill **+0.07** · typical error ×156.95 · ±30% 0% · n=41754

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 8552 | ×13.53 | 4% | +0.05 | +0.06 |
| accessory.amulet | 8005 | ×54.74 | 22% | +0.02 | +0.02 |
| jewel | 7903 | ×8.20 | 7% | +0.02 | +0.05 |
| accessory.belt | 6277 | ×10.00 | 18% | +0.04 | +0.04 |
| armour.chest | 6112 | ×12.05 | 10% | +0.01 | +0.02 |
| armour.helmet | 6001 | ×11.49 | 15% | +0.01 | +0.03 |
| armour.boots | 5555 | ×17.97 | 5% | +0.03 | +0.06 |
| armour.gloves | 5450 | ×20.84 | 5% | +0.01 | +0.03 |
| other | 4915 | ×9.97 | 35% | +0.08 | +0.14 |
| weapon.wand | 3571 | ×36.13 | 19% | +0.07 | +0.08 |
| weapon.bow | 2900 | ×30.69 | 16% | +0.09 | +0.10 |
| weapon.crossbow | 2731 | ×22.39 | 19% | +0.10 | +0.14 |
| weapon.warstaff | 1517 | ×49.92 | 18% | +0.08 | +0.11 |
| weapon.staff | 1438 | ×70.20 | 18% | +0.06 | +0.08 |
| weapon.sceptre | 1420 | ×66.35 | 13% | +0.08 | +0.10 |
| weapon.spear | 1217 | ×49.95 | 19% | +0.08 | +0.07 |
| armour.focus | 991 | ×46.54 | 13% | +0.13 | +0.12 |
| armour.quiver | 947 | ×34.30 | 14% | +0.06 | +0.09 |
| armour.shield | 814 | ×12.51 | 17% | +0.04 | +0.05 |
| weapon.twomace | 728 | ×38.48 | 15% | +0.06 | +0.09 |
| flask.charm | 684 | ×10.00 | 35% | +0.01 | +0.02 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=43029, R²=-0.4718

intercept: `1.6026`  ·  log_price: True  ·  ilvl: `0.00009`  ·  n_mods: `0.02551`  ·  n_top_tier: `0.64863`  ·  corrupted: `0.67489`  ·  n_sockets: `-0.00013`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 2.73053 |
| `explicit.stat_2891184298@T1` | 1.42632 |
| `explicit.stat_1050105434@T1` | -1.03725 |
| `explicit.stat_3917489142@T1` | 1.01780 |
| `explicit.stat_789117908@T1` | -0.97589 |
| `explicit.stat_2974417149@T1` | 0.92968 |
| `explicit.stat_736967255@T1` | -0.41616 |
| `explicit.stat_1589917703@T1` | 0.32841 |
| `explicit.stat_3141070085@T1` | -0.24249 |
| `implicit.stat_1379411836` | -0.23109 |
| `implicit.stat_4041853756` | 0.22769 |
| `implicit.stat_3879011313` | 0.22769 |

### jewel — n=42012, R²=-0.7611

intercept: `-1.4628`  ·  log_price: True  ·  ilvl: `0.03282`  ·  n_mods: `0.44190`  ·  n_top_tier: `-0.15699`  ·  corrupted: `0.15861`  ·  quality: `0.23189`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -4.31410 |
| `explicit.stat_153777645@T1` | -2.53740 |
| `explicit.stat_3174700878@T1` | 2.38050 |
| `explicit.stat_1697447343@T1` | -2.37716 |
| `explicit.stat_3741323227@T1` | -2.36583 |
| `explicit.stat_2301718443@T1` | 2.32764 |
| `explicit.stat_3028809864@T1` | -2.28562 |
| `explicit.stat_3780644166@T1` | -2.23534 |
| `explicit.stat_627767961@T1` | -2.21979 |
| `explicit.stat_3485067555@T1` | 2.21330 |
| `explicit.stat_1315743832@T1` | 2.04740 |
| `explicit.stat_795138349@T1` | -1.85660 |

### accessory.ring — n=39253, R²=-1.2936

intercept: `4.2868`  ·  log_price: True  ·  ilvl: `-0.04643`  ·  n_mods: `-0.04063`  ·  n_top_tier: `0.30282`  ·  corrupted: `0.85909`  ·  n_sockets: `0.61254`  ·  quality: `0.01182`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 2.86999 |
| `explicit.stat_707457662@T2` | 2.60214 |
| `explicit.stat_2557965901@T2` | 1.20826 |
| `explicit.stat_2557965901@T1` | 1.16821 |
| `explicit.stat_1573130764@T1` | -1.07131 |
| `explicit.stat_1368271171@T1` | -1.01057 |
| `explicit.stat_1379411836@T1` | -0.99052 |
| `explicit.stat_1368271171@T2` | -0.93766 |
| `explicit.stat_3291658075@T2` | -0.88365 |
| `explicit.stat_3299347043@T1` | -0.75019 |
| `explicit.stat_3032590688@T2` | -0.72424 |
| `explicit.stat_2231156303@T1` | -0.69396 |

### accessory.amulet — n=36608, R²=-2.1096

intercept: `3.8961`  ·  log_price: True  ·  ilvl: `-0.04719`  ·  n_mods: `-0.02207`  ·  n_top_tier: `0.97454`  ·  corrupted: `0.05210`  ·  n_sockets: `-0.10666`  ·  quality: `0.00037`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T2` | -1.28946 |
| `explicit.stat_2748665614@T1` | -1.09061 |
| `explicit.stat_2748665614@T2` | -1.07954 |
| `explicit.stat_3917489142@T2` | -1.03086 |
| `explicit.stat_3299347043@T2` | -1.02893 |
| `explicit.stat_3917489142@T1` | -1.02568 |
| `explicit.stat_3299347043@T1` | -1.02560 |
| `explicit.stat_472520716@T1` | -1.01843 |
| `explicit.stat_2901986750@T1` | -1.01739 |
| `explicit.stat_1050105434@T2` | -1.01730 |
| `explicit.stat_328541901@T1` | -1.01274 |
| `explicit.stat_2974417149@T1` | -1.00936 |

### accessory.belt — n=28662, R²=-0.1785

intercept: `2.3029`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.00101`  ·  corrupted: `0.00009`  ·  n_sockets: `-0.69309`

| stat_id | coef |
|---|---|
| `explicit.stat_2639966148` | 0.13136 |
| `explicit.stat_174664100` | 0.06330 |
| `explicit.stat_3811191316` | 0.04881 |
| `pseudo.total_ele_res>=80` | 0.04385 |
| `explicit.stat_770672621` | 0.03236 |
| `explicit.stat_3742865955` | 0.02525 |
| `pseudo.total_chaos_res` | 0.02380 |
| `explicit.stat_2923486259` | -0.02379 |
| `explicit.stat_2957407601` | 0.01793 |
| `explicit.stat_1485480327` | 0.01688 |
| `explicit.stat_1389754388@T1` | -0.00105 |
| `explicit.stat_51994685@T1` | -0.00105 |

### armour.chest — n=28378, R²=-0.4337

intercept: `3.2720`  ·  log_price: True  ·  ilvl: `-0.02087`  ·  n_mods: `-0.10584`  ·  n_top_tier: `0.33121`  ·  corrupted: `0.30893`  ·  n_sockets: `0.03802`  ·  quality: `0.00979`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 0.86344 |
| `explicit.stat_4080418644@T1` | -0.67493 |
| `explicit.stat_915769802@T1` | -0.53646 |
| `explicit.stat_2451402625@T2` | -0.53507 |
| `explicit.stat_3484657501@T1` | -0.51823 |
| `explicit.stat_124859000@T2` | -0.50690 |
| `explicit.stat_3325883026@T2` | -0.47352 |
| `explicit.stat_3362812763@T1` | -0.45096 |
| `explicit.stat_915769802@T2` | -0.43677 |
| `rune.stat_836936635` | -0.43444 |
| `implicit.stat_1978899297` | -0.43073 |
| `explicit.stat_3639275092@T2` | -0.39922 |

### armour.helmet — n=27733, R²=-0.3738

intercept: `2.7658`  ·  log_price: True  ·  ilvl: `-0.01246`  ·  n_mods: `-0.05548`  ·  n_top_tier: `0.23472`  ·  corrupted: `0.65937`  ·  n_sockets: `0.03462`  ·  quality: `0.01546`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 0.84018 |
| `explicit.stat_1263695895@T1` | -0.38191 |
| `explicit.stat_53045048@T2` | -0.35931 |
| `explicit.stat_1263695895@T2` | -0.34385 |
| `explicit.stat_3362812763@T2` | -0.33135 |
| `explicit.stat_53045048@T1` | -0.30586 |
| `explicit.stat_3917489142@T2` | -0.29797 |
| `explicit.stat_3362812763@T1` | -0.28968 |
| `explicit.stat_3261801346@T2` | -0.28064 |
| `explicit.stat_328541901@T2` | -0.27672 |
| `explicit.stat_2339757871@T1` | -0.27607 |
| `explicit.stat_1999113824@T1` | -0.27249 |

### armour.boots — n=25972, R²=-0.846

intercept: `4.5335`  ·  log_price: True  ·  ilvl: `-0.04902`  ·  n_mods: `-0.12984`  ·  n_top_tier: `0.62133`  ·  corrupted: `0.34883`  ·  n_sockets: `0.10074`  ·  quality: `0.01676`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.07661 |
| `explicit.stat_2339757871@T1` | -1.83509 |
| `explicit.stat_2250533757@T1` | 1.16867 |
| `explicit.stat_1062208444@T2` | -1.12513 |
| `explicit.stat_3917489142@T2` | -0.89588 |
| `desecrated.stat_2250533757@T2` | -0.85926 |
| `explicit.stat_2451402625@T2` | -0.84009 |
| `explicit.stat_124859000@T2` | -0.83182 |
| `explicit.stat_3299347043@T1` | -0.81315 |
| `explicit.stat_3362812763@T1` | -0.79353 |
| `explicit.stat_1999113824@T2` | -0.79114 |
| `explicit.stat_2160282525@T1` | -0.78563 |

### armour.gloves — n=25309, R²=-0.8327

intercept: `3.7654`  ·  log_price: True  ·  ilvl: `-0.04709`  ·  n_mods: `-0.12484`  ·  n_top_tier: `0.42989`  ·  corrupted: `0.16087`  ·  n_sockets: `0.20623`  ·  quality: `0.02705`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 1.90488 |
| `explicit.stat_3484657501@T2` | -1.52590 |
| `explicit.stat_803737631@T2` | -1.15934 |
| `rune.stat_201332984` | 1.03173 |
| `explicit.stat_3917489142@T2` | -0.86459 |
| `explicit.stat_681332047@T2` | -0.84859 |
| `explicit.stat_3484657501@T1` | -0.84254 |
| `explicit.stat_1573130764@T1` | -0.84128 |
| `explicit.stat_3321629045@T2` | -0.76992 |
| `explicit.stat_9187492@T1` | 0.72634 |
| `explicit.stat_3321629045@T1` | -0.69531 |
| `explicit.stat_2451402625@T2` | -0.68765 |

### weapon.wand — n=16624, R²=-2.2266

intercept: `3.7865`  ·  log_price: True  ·  ilvl: `-0.04732`  ·  n_mods: `-0.00757`  ·  n_top_tier: `0.15265`  ·  corrupted: `-0.09817`  ·  n_sockets: `0.04303`  ·  quality: `-0.00211`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.61490 |
| `explicit.stat_2254480358@T1` | 2.45283 |
| `explicit.stat_591105508@T1` | 2.22806 |
| `explicit.stat_1545858329@T1` | 2.22783 |
| `explicit.stat_4226189338@T1` | 2.14212 |
| `explicit.stat_124131830@T1` | 1.97714 |
| `explicit.stat_736967255@T2` | 1.55821 |
| `explicit.stat_2768835289@T2` | 1.28364 |
| `crafted.stat_124131830` | 1.22470 |
| `explicit.stat_274716455@T1` | 0.89370 |
| `explicit.stat_2254480358@T2` | 0.75408 |
| `explicit.stat_737908626@T1` | -0.24301 |

### weapon.bow — n=13552, R²=-1.9427

intercept: `3.4871`  ·  log_price: True  ·  ilvl: `-0.04248`  ·  n_mods: `-0.03482`  ·  n_top_tier: `0.64062`  ·  corrupted: `-0.03355`  ·  n_sockets: `-0.00496`  ·  quality: `0.03425`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.37730 |
| `explicit.stat_1202301673@T1` | 1.48420 |
| `crafted.stat_3035140377` | 1.28483 |
| `explicit.stat_518292764@T2` | -0.77349 |
| `explicit.stat_1263695895@T1` | -0.77301 |
| `explicit.stat_821021828@T2` | -0.71902 |
| `explicit.stat_55876295@T1` | -0.70895 |
| `explicit.stat_2694482655@T2` | -0.70888 |
| `explicit.stat_669069897@T1` | -0.70713 |
| `explicit.stat_1368271171@T2` | -0.69954 |
| `explicit.stat_3695891184@T1` | -0.69751 |
| `explicit.stat_3695891184@T2` | -0.69738 |

### weapon.crossbow — n=12750, R²=-1.8557

intercept: `3.5190`  ·  log_price: True  ·  ilvl: `-0.04339`  ·  n_mods: `-0.02163`  ·  n_top_tier: `0.75191`  ·  corrupted: `-0.01926`  ·  n_sockets: `0.04220`  ·  quality: `0.00555`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.99508 |
| `explicit.stat_2250681686@T2` | -1.47898 |
| `explicit.stat_709508406@T1` | 1.32042 |
| `explicit.stat_1980802737` | 1.17818 |
| `explicit.stat_1202301673@T2` | -1.04873 |
| `explicit.stat_1263695895@T2` | -0.98363 |
| `explicit.stat_1202301673@T1` | 0.96372 |
| `explicit.stat_1263695895@T1` | -0.93575 |
| `explicit.stat_1509134228@T2` | -0.88318 |
| `explicit.stat_3695891184@T1` | -0.87826 |
| `explicit.stat_3695891184@T2` | -0.86398 |
| `explicit.stat_1544773869@T2` | -0.85034 |

### flask.charm — n=10672, R²=-0.482

intercept: `0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `1.59232`  ·  corrupted: `2.14419`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.32532 |
| `explicit.stat_1056492907` | 3.40145 |
| `explicit.stat_828533480@T2` | -1.59233 |
| `explicit.stat_1120862500@T2` | -1.59232 |
| `explicit.stat_3196823591@T2` | -1.59232 |
| `explicit.stat_1366840608@T2` | -1.59232 |
| `explicit.stat_1873752457@T1` | -1.59232 |
| `explicit.stat_2676834156@T2` | -1.59231 |
| `explicit.stat_1873752457@T2` | -1.59231 |
| `explicit.stat_828533480@T1` | -1.59231 |
| `explicit.stat_2541588185@T2` | -1.59230 |
| `explicit.stat_388617051@T2` | -1.59230 |

### weapon.warstaff — n=7337, R²=-0.5638

intercept: `-2.0444`  ·  log_price: True  ·  ilvl: `0.02851`  ·  n_mods: `-0.07775`  ·  n_top_tier: `0.62371`  ·  corrupted: `0.12578`  ·  n_sockets: `0.04276`  ·  quality: `0.05223`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.49259 |
| `explicit.stat_328541901@T2` | -0.77698 |
| `explicit.stat_328541901@T1` | -0.77610 |
| `explicit.stat_691932474@T2` | -0.72175 |
| `rune.stat_731403740` | 0.71105 |
| `explicit.stat_3336890334@T2` | -0.68214 |
| `explicit.stat_55876295@T1` | -0.65799 |
| `explicit.stat_55876295@T2` | -0.65319 |
| `explicit.stat_3695891184@T2` | -0.63349 |
| `explicit.stat_1940865751@T1` | -0.63121 |
| `explicit.stat_821021828@T1` | -0.62316 |
| `explicit.stat_791928121@T2` | -0.61913 |

### weapon.sceptre — n=6808, R²=-0.4858

intercept: `-11.6347`  ·  log_price: True  ·  ilvl: `0.14543`  ·  n_mods: `-0.01699`  ·  n_top_tier: `0.30313`  ·  corrupted: `0.41265`  ·  n_sockets: `0.22886`  ·  quality: `0.09207`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.27521 |
| `explicit.stat_2162097452@T2` | 1.48561 |
| `explicit.stat_4080418644@T1` | -0.86875 |
| `explicit.stat_1263695895@T2` | -0.73705 |
| `explicit.stat_1574590649@T2` | -0.68042 |
| `explicit.stat_1263695895@T1` | -0.66146 |
| `explicit.stat_2347036682@T2` | -0.61645 |
| `explicit.stat_4080418644@T2` | -0.60230 |
| `explicit.stat_2854751904@T2` | -0.48285 |
| `explicit.stat_3057012405@T1` | 0.48007 |
| `explicit.stat_289128254@T2` | -0.42791 |
| `explicit.stat_1050105434@T2` | -0.42361 |

### weapon.staff — n=6777, R²=-0.6214

intercept: `-3.7166`  ·  log_price: True  ·  ilvl: `0.04699`  ·  n_mods: `-0.02133`  ·  n_top_tier: `0.21667`  ·  corrupted: `0.05284`  ·  n_sockets: `0.09754`  ·  quality: `0.04746`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 2.50955 |
| `explicit.stat_4226189338@T1` | 2.05771 |
| `explicit.stat_1545858329@T1` | 1.80127 |
| `explicit.stat_124131830@T1` | 1.77447 |
| `explicit.stat_2254480358@T1` | 1.58517 |
| `explicit.stat_1600707273@T1` | 1.58102 |
| `explicit.stat_2768835289@T2` | 1.43662 |
| `explicit.stat_3291658075@T2` | 1.16903 |
| `explicit.stat_2254480358@T2` | 0.91799 |
| `explicit.stat_2231156303@T2` | 0.69513 |
| `explicit.stat_2891184298@T1` | 0.59686 |
| `explicit.stat_3962278098@T2` | 0.52974 |

### weapon.spear — n=5752, R²=-0.6615

intercept: `-2.3190`  ·  log_price: True  ·  ilvl: `0.03039`  ·  n_mods: `-0.01115`  ·  n_top_tier: `0.42174`  ·  corrupted: `-0.07760`  ·  n_sockets: `0.05010`  ·  quality: `0.10866`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T1` | 2.33582 |
| `explicit.stat_1202301673@T1` | 2.25676 |
| `crafted.stat_210067635@T2` | -1.44967 |
| `crafted.stat_3035140377` | 1.24536 |
| `explicit.stat_210067635@T1` | 0.68591 |
| `crafted.stat_518292764` | 0.50410 |
| `explicit.stat_55876295@T1` | -0.49833 |
| `explicit.stat_9187492@T2` | -0.47716 |
| `explicit.stat_55876295@T2` | -0.45763 |
| `explicit.stat_748522257@T1` | -0.43846 |
| `explicit.stat_1509134228@T1` | 0.43139 |
| `explicit.stat_748522257@T2` | -0.43136 |

### armour.focus — n=4705, R²=-0.4875

intercept: `-8.3907`  ·  log_price: True  ·  ilvl: `0.10359`  ·  n_mods: `-0.04099`  ·  n_top_tier: `0.90975`  ·  corrupted: `0.70623`  ·  n_sockets: `0.32742`  ·  quality: `0.08154`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 6.28787 |
| `explicit.stat_4220027924@T2` | -1.19289 |
| `explicit.stat_4220027924@T1` | -1.08987 |
| `explicit.stat_2891184298@T2` | -1.05727 |
| `explicit.stat_2923486259@T1` | -1.00738 |
| `explicit.stat_328541901@T2` | -1.00543 |
| `explicit.stat_2974417149@T1` | -0.99595 |
| `explicit.stat_736967255@T2` | -0.95983 |
| `explicit.stat_3962278098@T1` | -0.93481 |
| `explicit.stat_2891184298@T1` | -0.92337 |
| `explicit.stat_3962278098@T2` | -0.88323 |
| `explicit.stat_4015621042@T1` | -0.87947 |

### armour.quiver — n=4384, R²=-0.4669

intercept: `-7.7483`  ·  log_price: True  ·  ilvl: `0.09202`  ·  n_mods: `-0.00942`  ·  n_top_tier: `0.91959`  ·  corrupted: `0.69249`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 13.48266 |
| `explicit.stat_2463230181@T1` | 1.39248 |
| `explicit.stat_2194114101@T2` | -1.20677 |
| `explicit.stat_1573130764@T1` | -1.19131 |
| `explicit.stat_2321178454@T2` | -1.15712 |
| `explicit.stat_681332047@T2` | -1.12749 |
| `explicit.stat_1368271171@T2` | -1.05704 |
| `explicit.stat_3261801346@T1` | -1.05121 |
| `desecrated.stat_3932115504` | -1.00726 |
| `explicit.stat_1573130764@T2` | -0.99406 |
| `explicit.stat_4067062424@T1` | -0.95743 |
| `explicit.stat_1241625305@T2` | -0.91869 |

### armour.shield — n=3847, R²=-0.5781

intercept: `-6.0378`  ·  log_price: True  ·  ilvl: `0.07548`  ·  n_mods: `-0.00882`  ·  n_top_tier: `0.53970`  ·  corrupted: `0.30891`  ·  n_sockets: `0.04244`  ·  quality: `0.05438`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.65472 |
| `explicit.stat_3033371881@T1` | 1.45220 |
| `explicit.stat_2339757871@T1` | -1.09700 |
| `explicit.stat_328541901@T1` | -1.00909 |
| `explicit.stat_1011760251@T1` | -0.99920 |
| `explicit.stat_1011760251@T2` | -0.90165 |
| `explicit.stat_328541901@T2` | -0.84640 |
| `explicit.stat_2481353198@T2` | -0.84219 |
| `explicit.stat_2481353198@T1` | -0.78627 |
| `explicit.stat_1978899297@T2` | -0.74651 |
| `explicit.stat_2881298780@T1` | -0.71685 |
| `explicit.stat_1978899297@T1` | 0.71674 |

### weapon.twomace — n=3500, R²=-0.504

intercept: `-8.5922`  ·  log_price: True  ·  ilvl: `0.11207`  ·  n_mods: `-0.08990`  ·  n_top_tier: `0.35819`  ·  corrupted: `0.73161`  ·  n_sockets: `0.14640`  ·  quality: `0.04119`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.92796 |
| `desecrated.stat_1509134228@T1` | 2.65878 |
| `explicit.stat_210067635@T1` | 1.18252 |
| `crafted.stat_3035140377` | 1.09051 |
| `explicit.stat_1037193709@T1` | -1.03564 |
| `explicit.stat_1509134228@T1` | 0.78690 |
| `explicit.stat_821021828@T2` | -0.76064 |
| `explicit.stat_387439868@T2` | -0.75892 |
| `explicit.stat_709508406@T1` | -0.65634 |
| `explicit.stat_3336890334@T1` | -0.65298 |
| `explicit.stat_1037193709@T2` | -0.62275 |
| `explicit.stat_821021828@T1` | -0.58520 |

## Coverage (listings per base)

- … **Sapphire** — 19757 listings (19732 priced) [0.3–7553463.8 ex]
- … **Emerald** — 19457 listings (19435 priced) [0.3–7553463.8 ex]
- … **Ruby** — 14921 listings (14909 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 8473 listings (8464 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 6753 listings (6744 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 6593 listings (6580 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 6508 listings (6503 priced) [0.2–19945827.9 ex]
- … **Stellar Amulet** — 6239 listings (6236 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 6199 listings (6189 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 6059 listings (6050 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5272 listings (5259 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5028 listings (5022 priced) [0.2–307202867.9 ex]
- … **Ruby Ring** — 4871 listings (4869 priced) [0.2–37474957.5 ex]
- … **Topaz Ring** — 4864 listings (4861 priced) [0.3–307202867.9 ex]
- … **Plate Belt** — 4419 listings (4411 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4387 listings (4383 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4294 listings (4287 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4261 listings (4259 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4219 listings (4214 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4145 listings (4142 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4074 listings (4070 priced) [0.3–4275054.0 ex]
- … **Obliterator Bow** — 4066 listings (4054 priced) [0.3–42622633798.0 ex]
- … **Heavy Belt** — 3980 listings (3978 priced) [0.3–2608914286.6 ex]
- … **Pearl Ring** — 3890 listings (3886 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 3827 listings (3827 priced) [0.3–123132003.2 ex]

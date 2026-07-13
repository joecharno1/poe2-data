# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-13T16:47:49+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **431782** (430941 priced in exalted)
- Distinct bases: 973 · distinct mods: 3001 · mod rows: 2053026
- Sold signals: **27451** sold · 235226 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-13T16:38:15+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×21.88** (median |log error| 3.0854)
- Within ±30% of asking price: **15%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.05** · typical error ×49.93 · ±30% 8% · n=62533
- Premium segment (60ex+): skill **+0.07** · typical error ×165.16 · ±30% 0% · n=40863

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 8469 | ×55.09 | 20% | +0.03 | +0.05 |
| accessory.amulet | 7896 | ×52.32 | 21% | +0.02 | +0.02 |
| jewel | 7755 | ×8.28 | 7% | +0.02 | +0.05 |
| accessory.belt | 6120 | ×10.00 | 17% | +0.03 | +0.03 |
| armour.chest | 6042 | ×13.28 | 8% | +0.01 | +0.01 |
| armour.helmet | 5947 | ×14.12 | 9% | +0.01 | +0.03 |
| armour.boots | 5544 | ×18.83 | 5% | +0.03 | +0.06 |
| armour.gloves | 5371 | ×20.49 | 4% | +0.01 | +0.04 |
| other | 4876 | ×9.97 | 35% | +0.08 | +0.17 |
| weapon.wand | 3487 | ×37.42 | 18% | +0.07 | +0.09 |
| weapon.bow | 2856 | ×27.90 | 16% | +0.09 | +0.09 |
| weapon.crossbow | 2692 | ×22.46 | 20% | +0.10 | +0.14 |
| weapon.warstaff | 1531 | ×63.05 | 17% | +0.08 | +0.09 |
| weapon.sceptre | 1420 | ×72.34 | 14% | +0.09 | +0.09 |
| weapon.staff | 1404 | ×53.08 | 18% | +0.06 | +0.06 |
| weapon.spear | 1175 | ×49.99 | 18% | +0.08 | +0.09 |
| armour.focus | 986 | ×41.47 | 13% | +0.13 | +0.11 |
| armour.quiver | 903 | ×36.18 | 14% | +0.06 | +0.10 |
| armour.shield | 785 | ×10.97 | 16% | +0.04 | +0.05 |
| weapon.twomace | 698 | ×24.52 | 16% | +0.05 | +0.10 |
| flask.charm | 679 | ×10.00 | 35% | +0.01 | +0.02 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=42516, R²=-0.4622

intercept: `1.6052`  ·  log_price: True  ·  ilvl: `0.00005`  ·  n_mods: `0.01606`  ·  n_top_tier: `0.67678`  ·  corrupted: `0.81227`  ·  n_sockets: `-0.00008`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.22729 |
| `explicit.stat_1589917703@T1` | 2.63271 |
| `explicit.stat_2106365538@T1` | 2.03684 |
| `explicit.stat_3141070085@T1` | -1.29278 |
| `explicit.stat_3917489142@T1` | 1.08953 |
| `explicit.stat_1050105434@T1` | -1.07624 |
| `explicit.stat_789117908@T1` | -1.05381 |
| `explicit.stat_2974417149@T1` | 0.95946 |
| `explicit.stat_2891184298@T1` | 0.93689 |
| `explicit.stat_2482852589@T1` | 0.53984 |
| `implicit.stat_4041853756` | 0.22864 |
| `implicit.stat_3879011313` | 0.22864 |

### jewel — n=41320, R²=-0.7405

intercept: `-1.4255`  ·  log_price: True  ·  ilvl: `0.03331`  ·  n_mods: `0.43550`  ·  n_top_tier: `-0.16963`  ·  corrupted: `0.13043`  ·  quality: `0.23297`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -4.31918 |
| `explicit.stat_3741323227@T1` | -2.70929 |
| `explicit.stat_3780644166@T1` | -2.55690 |
| `explicit.stat_153777645@T1` | -2.27623 |
| `explicit.stat_3714003708@T1` | -2.11277 |
| `explicit.stat_1315743832@T1` | 2.06402 |
| `explicit.stat_627767961@T1` | -2.02136 |
| `explicit.stat_3485067555@T1` | 1.92432 |
| `explicit.stat_795138349@T1` | -1.91954 |
| `explicit.stat_3174700878@T1` | 1.91483 |
| `explicit.stat_1569101201@T1` | 1.87124 |
| `explicit.stat_3028809864@T1` | -1.74250 |

### accessory.ring — n=38647, R²=-1.9338

intercept: `3.8886`  ·  log_price: True  ·  ilvl: `-0.04766`  ·  n_mods: `0.00238`  ·  n_top_tier: `0.47733`  ·  corrupted: `0.28632`  ·  n_sockets: `-0.13429`  ·  quality: `0.03003`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | -0.53591 |
| `explicit.stat_1263695895@T2` | -0.51502 |
| `explicit.stat_3291658075@T2` | -0.51436 |
| `explicit.stat_4220027924@T2` | -0.50935 |
| `explicit.stat_3325883026@T1` | -0.50907 |
| `explicit.stat_2231156303@T1` | -0.50530 |
| `explicit.stat_3032590688@T2` | -0.50510 |
| `explicit.stat_3962278098@T2` | -0.50358 |
| `explicit.stat_1368271171@T2` | -0.50351 |
| `explicit.stat_1573130764@T1` | -0.50119 |
| `explicit.stat_3917489142@T2` | -0.50107 |
| `explicit.stat_4067062424@T1` | -0.50075 |

### accessory.amulet — n=36066, R²=-2.1171

intercept: `3.8055`  ·  log_price: True  ·  ilvl: `-0.04592`  ·  n_mods: `-0.02079`  ·  n_top_tier: `1.00202`  ·  corrupted: `0.04634`  ·  n_sockets: `-0.11649`  ·  quality: `0.00074`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T2` | -1.44548 |
| `explicit.stat_2748665614@T1` | -1.11828 |
| `explicit.stat_2748665614@T2` | -1.10831 |
| `explicit.stat_3917489142@T2` | -1.05562 |
| `explicit.stat_3917489142@T1` | -1.05561 |
| `explicit.stat_2901986750@T1` | -1.05418 |
| `explicit.stat_3299347043@T2` | -1.04199 |
| `explicit.stat_1050105434@T2` | -1.04154 |
| `explicit.stat_983749596@T1` | -1.03971 |
| `explicit.stat_328541901@T1` | -1.03578 |
| `explicit.stat_4220027924@T2` | -1.03535 |
| `explicit.stat_1671376347@T2` | -1.03476 |

### accessory.belt — n=28317, R²=-0.1775

intercept: `2.3030`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00005`  ·  n_top_tier: `0.00018`  ·  corrupted: `0.00012`  ·  n_sockets: `-0.69307`

| stat_id | coef |
|---|---|
| `explicit.stat_2639966148` | 0.11743 |
| `explicit.stat_174664100` | 0.05880 |
| `explicit.stat_3811191316` | 0.05072 |
| `pseudo.total_ele_res>=80` | 0.03772 |
| `explicit.stat_770672621` | 0.02926 |
| `explicit.stat_3742865955` | 0.02531 |
| `pseudo.total_chaos_res` | 0.02384 |
| `explicit.stat_2923486259` | -0.02384 |
| `explicit.stat_2957407601` | 0.01672 |
| `explicit.stat_1485480327` | 0.01619 |
| `explicit.stat_1389754388@T1` | -0.00024 |
| `explicit.stat_3299347043@T1` | -0.00023 |

### armour.chest — n=27991, R²=-0.4486

intercept: `3.4230`  ·  log_price: True  ·  ilvl: `-0.02363`  ·  n_mods: `-0.11602`  ·  n_top_tier: `0.33860`  ·  corrupted: `0.30976`  ·  n_sockets: `0.04931`  ·  quality: `0.01057`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.06373 |
| `explicit.stat_2451402625@T2` | -0.58309 |
| `explicit.stat_4080418644@T1` | -0.58266 |
| `explicit.stat_3484657501@T1` | -0.55396 |
| `explicit.stat_915769802@T1` | -0.53907 |
| `explicit.stat_124859000@T2` | -0.53670 |
| `explicit.stat_3325883026@T2` | -0.50159 |
| `explicit.stat_3261801346@T2` | -0.49078 |
| `explicit.stat_3362812763@T1` | -0.47594 |
| `explicit.stat_1062208444@T2` | -0.45836 |
| `explicit.stat_4080418644@T2` | -0.45209 |
| `explicit.stat_915769802@T2` | -0.45191 |

### armour.helmet — n=27358, R²=-0.4065

intercept: `3.0845`  ·  log_price: True  ·  ilvl: `-0.02157`  ·  n_mods: `-0.07958`  ·  n_top_tier: `0.36389`  ·  corrupted: `0.81088`  ·  n_sockets: `0.06637`  ·  quality: `0.02473`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.16695 |
| `explicit.stat_53045048@T2` | -0.55683 |
| `explicit.stat_3362812763@T2` | -0.55490 |
| `explicit.stat_1263695895@T1` | -0.54871 |
| `explicit.stat_3917489142@T2` | -0.52860 |
| `explicit.stat_1263695895@T2` | -0.51690 |
| `explicit.stat_3261801346@T2` | -0.49660 |
| `explicit.stat_53045048@T1` | -0.45832 |
| `explicit.stat_3321629045@T2` | -0.45073 |
| `explicit.stat_328541901@T2` | -0.44585 |
| `explicit.stat_1999113824@T1` | -0.44413 |
| `explicit.stat_3261801346@T1` | -0.43595 |

### armour.boots — n=25621, R²=-0.8371

intercept: `4.6260`  ·  log_price: True  ·  ilvl: `-0.04964`  ·  n_mods: `-0.14184`  ·  n_top_tier: `0.64848`  ·  corrupted: `0.37497`  ·  n_sockets: `0.08471`  ·  quality: `0.01462`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.52749 |
| `crafted.stat_3917489142@T1` | 1.36031 |
| `explicit.stat_2250533757@T1` | 1.21242 |
| `explicit.stat_1062208444@T2` | -1.14741 |
| `explicit.stat_3917489142@T2` | -0.99936 |
| `explicit.stat_124859000@T2` | -0.90479 |
| `explicit.stat_1999113824@T2` | -0.88799 |
| `explicit.stat_53045048@T1` | -0.88180 |
| `desecrated.stat_2250533757@T2` | -0.87433 |
| `explicit.stat_1999113824@T1` | -0.86645 |
| `explicit.stat_2923486259@T2` | -0.84013 |
| `explicit.stat_2160282525@T1` | -0.83386 |

### armour.gloves — n=24958, R²=-0.7997

intercept: `3.8130`  ·  log_price: True  ·  ilvl: `-0.04766`  ·  n_mods: `-0.12659`  ·  n_top_tier: `0.47222`  ·  corrupted: `0.28626`  ·  n_sockets: `0.26068`  ·  quality: `0.02526`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.67444 |
| `explicit.stat_3484657501@T2` | -1.57486 |
| `explicit.stat_803737631@T2` | -1.08885 |
| `explicit.stat_681332047@T2` | -0.88283 |
| `explicit.stat_3917489142@T2` | -0.87209 |
| `explicit.stat_3484657501@T1` | -0.86895 |
| `explicit.stat_1573130764@T1` | -0.81387 |
| `rune.stat_201332984` | 0.81260 |
| `explicit.stat_2451402625@T2` | -0.76653 |
| `explicit.stat_3695891184@T2` | -0.75421 |
| `explicit.stat_328541901@T2` | -0.73331 |
| `explicit.stat_3321629045@T2` | -0.70194 |

### weapon.wand — n=16359, R²=-2.216

intercept: `3.9340`  ·  log_price: True  ·  ilvl: `-0.04907`  ·  n_mods: `-0.01353`  ·  n_top_tier: `0.23778`  ·  corrupted: `-0.09033`  ·  n_sockets: `0.04766`  ·  quality: `-0.00050`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.18803 |
| `explicit.stat_2254480358@T1` | 2.73814 |
| `rune.stat_124131830` | -2.69492 |
| `explicit.stat_591105508@T1` | 2.14314 |
| `explicit.stat_4226189338@T1` | 2.04940 |
| `explicit.stat_124131830@T1` | 1.93863 |
| `explicit.stat_736967255@T2` | 1.47040 |
| `crafted.stat_124131830` | 1.26166 |
| `explicit.stat_2768835289@T2` | 1.06812 |
| `explicit.stat_274716455@T1` | 0.71441 |
| `explicit.stat_737908626@T1` | -0.31713 |
| `explicit.stat_3278136794@T2` | -0.29943 |

### weapon.bow — n=13359, R²=-1.9306

intercept: `3.4946`  ·  log_price: True  ·  ilvl: `-0.04249`  ·  n_mods: `-0.03927`  ·  n_top_tier: `0.61321`  ·  corrupted: `-0.03637`  ·  n_sockets: `-0.00558`  ·  quality: `0.03388`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.88427 |
| `explicit.stat_1202301673@T1` | 1.48470 |
| `crafted.stat_3035140377` | 1.33186 |
| `explicit.stat_2463230181@T1` | 1.01820 |
| `explicit.stat_1263695895@T1` | -0.77665 |
| `explicit.stat_1509134228@T1` | -0.68896 |
| `explicit.stat_821021828@T2` | -0.68807 |
| `explicit.stat_55876295@T1` | -0.68268 |
| `explicit.stat_669069897@T1` | -0.68086 |
| `explicit.stat_1037193709@T2` | -0.67731 |
| `explicit.stat_1368271171@T2` | -0.67652 |
| `explicit.stat_821021828@T1` | -0.67569 |

### weapon.crossbow — n=12602, R²=-1.8676

intercept: `3.5744`  ·  log_price: True  ·  ilvl: `-0.04386`  ·  n_mods: `-0.02301`  ·  n_top_tier: `0.69300`  ·  corrupted: `-0.03722`  ·  n_sockets: `0.04027`  ·  quality: `0.00610`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.91802 |
| `explicit.stat_2250681686@T2` | -1.46190 |
| `explicit.stat_709508406@T1` | 1.44601 |
| `explicit.stat_1202301673@T1` | 1.22348 |
| `explicit.stat_1980802737` | 1.17213 |
| `explicit.stat_1202301673@T2` | -0.94645 |
| `explicit.stat_1263695895@T2` | -0.89582 |
| `explicit.stat_1509134228@T1` | 0.87833 |
| `crafted.stat_3035140377` | 0.86397 |
| `explicit.stat_2250681686` | 0.82473 |
| `explicit.stat_1263695895@T1` | -0.80183 |
| `explicit.stat_1509134228@T2` | -0.79723 |

### flask.charm — n=10463, R²=-0.4775

intercept: `0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.75741`  ·  corrupted: `2.17821`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.29136 |
| `explicit.stat_1056492907` | 3.40058 |
| `explicit.stat_2676834156@T1` | 0.85514 |
| `explicit.stat_828533480@T2` | -0.75743 |
| `explicit.stat_1120862500@T2` | -0.75741 |
| `explicit.stat_3196823591@T2` | -0.75741 |
| `explicit.stat_2676834156@T2` | -0.75740 |
| `explicit.stat_828533480@T1` | -0.75740 |
| `explicit.stat_1873752457@T1` | -0.75740 |
| `explicit.stat_1873752457@T2` | -0.75740 |
| `explicit.stat_1366840608@T2` | -0.75740 |
| `explicit.stat_388617051@T2` | -0.75739 |

### weapon.warstaff — n=7179, R²=-0.5793

intercept: `-1.6060`  ·  log_price: True  ·  ilvl: `0.02204`  ·  n_mods: `-0.05982`  ·  n_top_tier: `0.47637`  ·  corrupted: `0.16706`  ·  n_sockets: `0.03247`  ·  quality: `0.05304`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.47673 |
| `rune.stat_731403740` | 0.81439 |
| `explicit.stat_9187492@T1` | 0.69743 |
| `explicit.stat_1037193709@T1` | 0.66845 |
| `explicit.stat_328541901@T1` | -0.59285 |
| `explicit.stat_328541901@T2` | -0.59099 |
| `explicit.stat_1509134228@T1` | 0.58715 |
| `explicit.stat_3336890334@T2` | -0.53970 |
| `explicit.stat_691932474@T2` | -0.52892 |
| `explicit.stat_55876295@T1` | -0.52071 |
| `explicit.stat_821021828@T1` | -0.50861 |
| `explicit.stat_55876295@T2` | -0.50584 |

### weapon.sceptre — n=6689, R²=-0.4997

intercept: `-10.4650`  ·  log_price: True  ·  ilvl: `0.13082`  ·  n_mods: `-0.02104`  ·  n_top_tier: `0.40405`  ·  corrupted: `0.35057`  ·  n_sockets: `0.19417`  ·  quality: `0.09506`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.29358 |
| `explicit.stat_2162097452@T2` | 1.39778 |
| `explicit.stat_4080418644@T1` | -0.77294 |
| `explicit.stat_1263695895@T2` | -0.74777 |
| `explicit.stat_1263695895@T1` | -0.71506 |
| `explicit.stat_1574590649@T2` | -0.70973 |
| `explicit.stat_2347036682@T2` | -0.64627 |
| `explicit.stat_4080418644@T2` | -0.52594 |
| `explicit.stat_2854751904@T2` | -0.49538 |
| `explicit.stat_289128254@T2` | -0.48889 |
| `explicit.stat_1050105434@T2` | -0.47329 |
| `explicit.stat_1798257884@T2` | 0.47312 |

### weapon.staff — n=6629, R²=-0.6308

intercept: `-2.5597`  ·  log_price: True  ·  ilvl: `0.03229`  ·  n_mods: `-0.01687`  ·  n_top_tier: `0.39745`  ·  corrupted: `0.03656`  ·  n_sockets: `0.07285`  ·  quality: `0.05725`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 2.31949 |
| `explicit.stat_4226189338@T1` | 1.85513 |
| `explicit.stat_1545858329@T1` | 1.58052 |
| `explicit.stat_124131830@T1` | 1.52240 |
| `explicit.stat_2254480358@T1` | 1.44581 |
| `explicit.stat_1600707273@T1` | 1.38227 |
| `explicit.stat_2768835289@T2` | 1.20152 |
| `explicit.stat_3291658075@T2` | 0.98906 |
| `explicit.stat_2254480358@T2` | 0.82853 |
| `explicit.stat_4226189338@T2` | 0.70738 |
| `explicit.stat_2231156303@T2` | 0.53780 |
| `explicit.stat_2974417149@T1` | -0.51268 |

### weapon.spear — n=5651, R²=-0.6741

intercept: `-1.4164`  ·  log_price: True  ·  ilvl: `0.01854`  ·  n_mods: `-0.00799`  ·  n_top_tier: `0.38951`  ·  corrupted: `-0.04919`  ·  n_sockets: `0.03916`  ·  quality: `0.10837`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.29415 |
| `explicit.stat_9187492@T1` | 2.05478 |
| `crafted.stat_210067635@T2` | -1.40644 |
| `crafted.stat_3035140377` | 1.23101 |
| `crafted.stat_518292764` | 0.61598 |
| `explicit.stat_210067635@T1` | 0.59800 |
| `explicit.stat_1509134228@T1` | 0.52442 |
| `explicit.stat_55876295@T1` | -0.44744 |
| `explicit.stat_55876295@T2` | -0.40967 |
| `explicit.stat_691932474@T1` | -0.40589 |
| `explicit.stat_748522257@T2` | -0.39803 |
| `explicit.stat_748522257@T1` | -0.39663 |

### armour.focus — n=4638, R²=-0.495

intercept: `-8.1697`  ·  log_price: True  ·  ilvl: `0.10086`  ·  n_mods: `-0.04741`  ·  n_top_tier: `1.03138`  ·  corrupted: `0.64957`  ·  n_sockets: `0.30825`  ·  quality: `0.07793`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 6.13997 |
| `crafted.stat_737908626@T2` | -2.63614 |
| `explicit.stat_4220027924@T2` | -1.34876 |
| `explicit.stat_4220027924@T1` | -1.23065 |
| `explicit.stat_2891184298@T2` | -1.20372 |
| `explicit.stat_2923486259@T1` | -1.16434 |
| `explicit.stat_2891184298@T1` | -1.12921 |
| `explicit.stat_328541901@T2` | -1.11871 |
| `explicit.stat_736967255@T2` | -1.06488 |
| `explicit.stat_2974417149@T1` | -1.06299 |
| `explicit.stat_3962278098@T1` | -1.03686 |
| `explicit.stat_737908626@T2` | -1.03326 |

### armour.quiver — n=4307, R²=-0.4975

intercept: `-6.6362`  ·  log_price: True  ·  ilvl: `0.07876`  ·  n_mods: `-0.00775`  ·  n_top_tier: `0.70558`  ·  corrupted: `0.61706`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 13.49422 |
| `explicit.stat_1573130764@T1` | -1.01419 |
| `explicit.stat_2321178454@T2` | -0.97683 |
| `desecrated.stat_3932115504` | -0.97234 |
| `explicit.stat_2463230181@T1` | 0.95940 |
| `explicit.stat_2194114101@T2` | -0.90946 |
| `explicit.stat_681332047@T2` | -0.88510 |
| `explicit.stat_1368271171@T2` | -0.81787 |
| `explicit.stat_3261801346@T1` | -0.81168 |
| `explicit.stat_1573130764@T2` | -0.76609 |
| `explicit.stat_4067062424@T1` | -0.74408 |
| `explicit.stat_1241625305@T2` | -0.68192 |

### armour.shield — n=3773, R²=-0.5831

intercept: `-6.1152`  ·  log_price: True  ·  ilvl: `0.07644`  ·  n_mods: `0.00544`  ·  n_top_tier: `0.39438`  ·  corrupted: `0.23763`  ·  n_sockets: `0.01077`  ·  quality: `0.05506`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.65877 |
| `explicit.stat_2339757871@T1` | -0.92433 |
| `explicit.stat_328541901@T1` | -0.91589 |
| `explicit.stat_1011760251@T1` | -0.90155 |
| `explicit.stat_1978899297@T1` | 0.85878 |
| `explicit.stat_1011760251@T2` | -0.81099 |
| `explicit.stat_3676141501@T1` | 0.75504 |
| `explicit.stat_328541901@T2` | -0.71744 |
| `explicit.stat_2481353198@T2` | -0.69636 |
| `explicit.stat_1978899297@T2` | -0.66720 |
| `explicit.stat_4095671657@T1` | 0.61474 |
| `explicit.stat_2481353198@T1` | -0.59950 |

### weapon.twomace — n=3422, R²=-0.5144

intercept: `-7.5743`  ·  log_price: True  ·  ilvl: `0.09802`  ·  n_mods: `-0.07862`  ·  n_top_tier: `0.43164`  ·  corrupted: `0.68004`  ·  n_sockets: `0.12258`  ·  quality: `0.03223`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.84274 |
| `desecrated.stat_1509134228@T1` | 2.50541 |
| `explicit.stat_1037193709@T1` | -1.14957 |
| `crafted.stat_3035140377` | 1.10873 |
| `explicit.stat_1509134228@T1` | 0.95545 |
| `explicit.stat_210067635@T1` | 0.89718 |
| `explicit.stat_3336890334@T1` | -0.84537 |
| `explicit.stat_387439868@T2` | -0.78820 |
| `explicit.stat_1037193709@T2` | -0.74865 |
| `explicit.stat_821021828@T2` | -0.69586 |
| `explicit.stat_2694482655@T1` | -0.63581 |
| `explicit.stat_3695891184@T1` | -0.63550 |

## Coverage (listings per base)

- … **Sapphire** — 19428 listings (19403 priced) [0.3–7553463.8 ex]
- … **Emerald** — 19142 listings (19120 priced) [0.3–7553463.8 ex]
- … **Ruby** — 14711 listings (14699 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 8371 listings (8362 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 6662 listings (6653 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 6490 listings (6478 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 6408 listings (6403 priced) [0.2–19945827.9 ex]
- … **Stellar Amulet** — 6152 listings (6149 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 6130 listings (6120 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 5974 listings (5966 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5189 listings (5176 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4945 listings (4939 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 4804 listings (4801 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 4795 listings (4793 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 4358 listings (4352 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4321 listings (4317 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4249 listings (4242 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4193 listings (4191 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4166 listings (4162 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4087 listings (4084 priced) [0.2–24532814.5 ex]
- … **Obliterator Bow** — 4007 listings (3995 priced) [0.3–42622633798.0 ex]
- … **Bloodstone Amulet** — 4004 listings (4000 priced) [0.3–4275054.0 ex]
- … **Heavy Belt** — 3940 listings (3938 priced) [0.3–2608914286.6 ex]
- … **Pearl Ring** — 3845 listings (3842 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 3763 listings (3763 priced) [0.3–123132003.2 ex]

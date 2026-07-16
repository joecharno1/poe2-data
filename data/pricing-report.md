# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-16T10:31:34+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **543450** (541991 priced in exalted)
- Distinct bases: 986 · distinct mods: 3174 · mod rows: 2575465
- Sold signals: **25774** sold · 305273 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-16T10:24:00+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×26.97** (median |log error| 3.2948)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×78.67 · ±30% 5% · n=78801
- Premium segment (60ex+): skill **+0.11** · typical error ×361.98 · ±30% 0% · n=53006

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 10997 | ×52.84 | 22% | +0.04 | +0.06 |
| jewel | 10308 | ×9.87 | 5% | +0.04 | +0.08 |
| accessory.amulet | 10101 | ×52.32 | 20% | +0.03 | +0.03 |
| accessory.belt | 7622 | ×26.02 | 23% | +0.04 | +0.06 |
| armour.chest | 7438 | ×30.86 | 25% | +0.06 | +0.09 |
| armour.helmet | 7247 | ×33.04 | 18% | +0.06 | +0.09 |
| armour.boots | 6742 | ×38.11 | 22% | +0.07 | +0.08 |
| armour.gloves | 6592 | ×40.62 | 18% | +0.06 | +0.09 |
| other | 6124 | ×1.95 | 43% | +0.10 | +0.17 |
| weapon.wand | 4163 | ×35.51 | 16% | +0.08 | +0.09 |
| weapon.bow | 3295 | ×30.54 | 18% | +0.10 | +0.10 |
| weapon.crossbow | 3079 | ×30.66 | 18% | +0.09 | +0.12 |
| weapon.warstaff | 1876 | ×35.21 | 12% | +0.13 | +0.12 |
| weapon.staff | 1809 | ×57.50 | 10% | +0.10 | +0.11 |
| weapon.sceptre | 1738 | ×42.37 | 5% | +0.16 | +0.15 |
| weapon.spear | 1420 | ×49.65 | 16% | +0.08 | +0.08 |
| armour.focus | 1202 | ×31.50 | 7% | +0.15 | +0.18 |
| armour.quiver | 1155 | ×29.44 | 8% | +0.11 | +0.14 |
| flask.charm | 994 | ×25.00 | 33% | +0.04 | +0.06 |
| armour.shield | 949 | ×26.61 | 10% | +0.03 | +0.05 |
| weapon.twomace | 851 | ×14.16 | 11% | +0.07 | +0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=55962, R²=-0.947

intercept: `-1.7020`  ·  log_price: True  ·  ilvl: `0.02570`  ·  n_mods: `0.68787`  ·  n_top_tier: `-0.20075`  ·  corrupted: `0.30729`  ·  quality: `0.22761`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.76502 |
| `explicit.stat_2301718443@T1` | 2.83461 |
| `explicit.stat_3780644166@T1` | -2.50474 |
| `explicit.stat_627767961@T1` | -2.30699 |
| `explicit.stat_3485067555@T1` | 2.21187 |
| `explicit.stat_1805182458@T1` | -2.01133 |
| `explicit.stat_234296660@T1` | -1.68100 |
| `explicit.stat_1697951953@T1` | -1.60684 |
| `explicit.stat_21071013@T1` | 1.60591 |
| `explicit.stat_1852872083@T1` | -1.60213 |
| `explicit.stat_3668351662@T1` | -1.57852 |
| `explicit.stat_3166958180@T1` | -1.54111 |

### other — n=52326, R²=-0.6363

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.34717`  ·  corrupted: `0.33821`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.43308 |
| `explicit.stat_2974417149@T1` | 0.42332 |
| `explicit.stat_3299347043@T1` | -0.34213 |
| `explicit.stat_2482852589@T1` | -0.28368 |
| `implicit.stat_3879011313` | 0.23468 |
| `implicit.stat_2219129443` | 0.23027 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_2968503605@T1` | 0.17727 |
| `explicit.stat_2106365538@T1` | -0.14505 |
| `explicit.stat_789117908@T1` | -0.14473 |
| `explicit.stat_1050105434@T1` | -0.12857 |
| `implicit.stat_2923486259` | -0.09289 |

### accessory.ring — n=50344, R²=-2.0094

intercept: `3.4875`  ·  log_price: True  ·  ilvl: `-0.04302`  ·  n_mods: `0.00060`  ·  n_top_tier: `0.89337`  ·  corrupted: `0.07092`  ·  n_sockets: `2.18336`  ·  quality: `0.07301`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -0.93749 |
| `explicit.stat_2557965901@T1` | -0.93385 |
| `explicit.stat_2557965901@T2` | -0.92286 |
| `explicit.stat_2231156303@T2` | -0.91841 |
| `explicit.stat_1368271171@T2` | -0.91579 |
| `explicit.stat_3291658075@T1` | -0.91529 |
| `explicit.stat_2144192055@T1` | -0.91469 |
| `explicit.stat_803737631@T1` | -0.91467 |
| `explicit.stat_3291658075@T2` | -0.91166 |
| `explicit.stat_1573130764@T1` | -0.91098 |
| `explicit.stat_3325883026@T1` | -0.90972 |
| `explicit.stat_1368271171@T1` | -0.90928 |

### accessory.amulet — n=46204, R²=-2.1463

intercept: `3.8327`  ·  log_price: True  ·  ilvl: `-0.04691`  ·  n_mods: `-0.02320`  ·  n_top_tier: `1.02545`  ·  corrupted: `0.08827`  ·  n_sockets: `-0.10812`  ·  quality: `-0.00060`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.12453 |
| `explicit.stat_587431675@T2` | -1.10346 |
| `explicit.stat_472520716@T2` | -1.10198 |
| `explicit.stat_3299347043@T2` | -1.08567 |
| `explicit.stat_803737631@T1` | -1.08383 |
| `explicit.stat_472520716@T1` | -1.08382 |
| `explicit.stat_1050105434@T2` | -1.07539 |
| `explicit.stat_2866361420@T2` | -1.06745 |
| `explicit.stat_803737631@T2` | -1.06481 |
| `explicit.stat_2901986750@T1` | -1.06267 |
| `explicit.stat_2974417149@T2` | -1.05835 |
| `explicit.stat_3489782002@T2` | -1.05671 |

### accessory.belt — n=35018, R²=-1.7405

intercept: `3.0391`  ·  log_price: True  ·  ilvl: `-0.03679`  ·  n_mods: `-0.01807`  ·  n_top_tier: `1.14705`  ·  corrupted: `0.52769`  ·  n_sockets: `0.29837`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.17589 |
| `explicit.stat_3299347043@T1` | -1.17486 |
| `explicit.stat_2881298780@T1` | -1.17266 |
| `explicit.stat_809229260@T2` | -1.16856 |
| `explicit.stat_4220027924@T2` | -1.16746 |
| `explicit.stat_3325883026@T1` | -1.16512 |
| `explicit.stat_3299347043@T2` | -1.16366 |
| `explicit.stat_644456512@T2` | -1.16096 |
| `explicit.stat_1671376347@T2` | -1.15750 |
| `explicit.stat_51994685@T1` | -1.15727 |
| `explicit.stat_809229260@T1` | -1.15400 |
| `explicit.stat_644456512@T1` | -1.15258 |

### armour.chest — n=34727, R²=-1.7491

intercept: `3.3249`  ·  log_price: True  ·  ilvl: `-0.04105`  ·  n_mods: `-0.01199`  ·  n_top_tier: `0.52908`  ·  corrupted: `0.02761`  ·  n_sockets: `0.01926`  ·  quality: `0.05525`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.93983 |
| `explicit.stat_3981240776@T1` | 1.01825 |
| `explicit.stat_986397080@T2` | -0.58638 |
| `explicit.stat_986397080@T1` | -0.56933 |
| `explicit.stat_4015621042@T1` | -0.56120 |
| `explicit.stat_4080418644@T2` | -0.55997 |
| `explicit.stat_4080418644@T1` | -0.55951 |
| `explicit.stat_2451402625@T2` | -0.55451 |
| `explicit.stat_3484657501@T1` | -0.55298 |
| `explicit.stat_915769802@T1` | -0.55226 |
| `explicit.stat_3372524247@T2` | -0.55223 |
| `explicit.stat_915769802@T2` | -0.54910 |

### armour.helmet — n=33689, R²=-1.6355

intercept: `3.7108`  ·  log_price: True  ·  ilvl: `-0.04694`  ·  n_mods: `-0.02449`  ·  n_top_tier: `0.42280`  ·  corrupted: `0.82548`  ·  n_sockets: `0.05553`  ·  quality: `0.05289`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -6.00048 |
| `crafted.stat_3917489142@T1` | 2.97267 |
| `explicit.stat_1263695895@T1` | -0.63414 |
| `explicit.stat_3917489142@T2` | -0.60747 |
| `explicit.stat_1263695895@T2` | -0.58320 |
| `explicit.stat_2162097452@T2` | -0.54695 |
| `explicit.stat_1999113824@T1` | -0.50800 |
| `explicit.stat_4052037485@T2` | -0.50292 |
| `explicit.stat_3917489142@T1` | -0.49579 |
| `explicit.stat_3321629045@T2` | -0.49542 |
| `explicit.stat_53045048@T1` | -0.48226 |
| `explicit.stat_803737631@T1` | -0.46286 |

### armour.boots — n=31534, R²=-1.7669

intercept: `3.3826`  ·  log_price: True  ·  ilvl: `-0.04156`  ·  n_mods: `-0.01379`  ·  n_top_tier: `0.66302`  ·  corrupted: `0.01350`  ·  n_sockets: `0.02165`  ·  quality: `0.04340`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.55825 |
| `explicit.stat_2250533757@T1` | 1.35979 |
| `explicit.stat_3917489142@T2` | -0.76772 |
| `explicit.stat_3299347043@T1` | -0.75884 |
| `explicit.stat_2339757871@T1` | -0.72342 |
| `explicit.stat_2923486259@T2` | -0.71924 |
| `explicit.stat_2160282525@T1` | -0.70555 |
| `explicit.stat_3917489142@T1` | -0.69416 |
| `explicit.stat_1671376347@T2` | -0.69183 |
| `explicit.stat_53045048@T1` | -0.69033 |
| `explicit.stat_1062208444@T2` | -0.68484 |
| `explicit.stat_3484657501@T2` | -0.68029 |

### armour.gloves — n=30690, R²=-1.7981

intercept: `3.7374`  ·  log_price: True  ·  ilvl: `-0.04730`  ·  n_mods: `-0.01125`  ·  n_top_tier: `0.50389`  ·  corrupted: `-0.00244`  ·  n_sockets: `0.05110`  ·  quality: `0.04153`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.20543 |
| `rune.stat_201332984` | -1.95118 |
| `explicit.stat_1671376347@T1` | 1.06750 |
| `explicit.stat_9187492@T1` | 0.88377 |
| `explicit.stat_9187492@T2` | -0.75945 |
| `explicit.stat_3484657501@T2` | -0.69109 |
| `explicit.stat_1999113824@T1` | 0.64362 |
| `explicit.stat_3321629045@T2` | -0.64039 |
| `explicit.stat_3484657501@T1` | -0.62527 |
| `explicit.stat_2923486259@T1` | -0.59176 |
| `explicit.stat_803737631@T2` | -0.59157 |
| `explicit.stat_3917489142@T2` | -0.57999 |

### weapon.wand — n=19440, R²=-2.0992

intercept: `3.7484`  ·  log_price: True  ·  ilvl: `-0.04628`  ·  n_mods: `-0.02940`  ·  n_top_tier: `0.65273`  ·  corrupted: `0.05165`  ·  n_sockets: `0.04078`  ·  quality: `0.01463`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.83713 |
| `explicit.stat_2254480358@T1` | 2.74764 |
| `explicit.stat_1545858329@T1` | 2.69440 |
| `explicit.stat_124131830@T1` | 1.77833 |
| `explicit.stat_4226189338@T1` | 1.74314 |
| `explicit.stat_591105508@T1` | 1.71904 |
| `explicit.stat_736967255@T2` | 1.57484 |
| `crafted.stat_124131830` | 1.22234 |
| `explicit.stat_1600707273@T2` | -0.88003 |
| `explicit.stat_1263695895@T2` | -0.83521 |
| `explicit.stat_2254480358@T2` | 0.81387 |
| `explicit.stat_1263695895@T1` | -0.80582 |

### weapon.bow — n=15538, R²=-2.0084

intercept: `3.5010`  ·  log_price: True  ·  ilvl: `-0.04251`  ·  n_mods: `-0.02944`  ·  n_top_tier: `0.64068`  ·  corrupted: `-0.06430`  ·  n_sockets: `0.00545`  ·  quality: `0.03593`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.01497 |
| `desecrated.stat_666077204@T1` | -1.81192 |
| `explicit.stat_1202301673@T1` | 1.60956 |
| `crafted.stat_3035140377` | 1.47662 |
| `explicit.stat_1263695895@T1` | -0.90550 |
| `explicit.stat_1263695895@T2` | -0.87604 |
| `explicit.stat_2463230181@T2` | -0.86411 |
| `explicit.stat_518292764@T2` | -0.73123 |
| `explicit.stat_3695891184@T2` | -0.72886 |
| `explicit.stat_518292764@T1` | 0.70584 |
| `explicit.stat_1037193709@T1` | -0.70242 |
| `explicit.stat_3695891184@T1` | -0.69942 |

### weapon.crossbow — n=14611, R²=-1.9144

intercept: `3.8824`  ·  log_price: True  ·  ilvl: `-0.04740`  ·  n_mods: `-0.03284`  ·  n_top_tier: `0.69937`  ·  corrupted: `0.00937`  ·  n_sockets: `0.03767`  ·  quality: `0.01904`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.87592 |
| `explicit.stat_2250681686@T2` | -1.67907 |
| `explicit.stat_1202301673@T1` | 1.40734 |
| `explicit.stat_1980802737` | 1.18695 |
| `explicit.stat_2250681686` | 1.12590 |
| `crafted.stat_3035140377` | 0.97046 |
| `explicit.stat_709508406@T1` | 0.95057 |
| `explicit.stat_1263695895@T2` | -0.89865 |
| `explicit.stat_1263695895@T1` | -0.88318 |
| `explicit.stat_2694482655@T1` | -0.78863 |
| `explicit.stat_1509134228@T2` | -0.77462 |
| `explicit.stat_3695891184@T1` | -0.77289 |

### flask.charm — n=14239, R²=-0.5659

intercept: `0.0266`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.99341`  ·  corrupted: `1.85574`  ·  quality: `0.00044`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.58948 |
| `explicit.stat_1056492907` | 3.14687 |
| `explicit.stat_828533480@T2` | -2.99343 |
| `explicit.stat_1120862500@T2` | -2.99341 |
| `explicit.stat_828533480@T1` | -2.99341 |
| `explicit.stat_388617051@T2` | -2.99340 |
| `explicit.stat_3196823591@T2` | -2.99340 |
| `explicit.stat_1873752457@T2` | -2.99340 |
| `explicit.stat_2541588185@T2` | -2.99339 |
| `explicit.stat_2676834156@T2` | -2.99339 |
| `explicit.stat_2365392475@T2` | -2.99338 |
| `explicit.stat_1873752457@T1` | -2.99337 |

### weapon.warstaff — n=9205, R²=-0.4124

intercept: `-9.2438`  ·  log_price: True  ·  ilvl: `0.12478`  ·  n_mods: `-0.18973`  ·  n_top_tier: `0.37250`  ·  corrupted: `0.18478`  ·  n_sockets: `0.18899`  ·  quality: `0.05367`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 1.44098 |
| `desecrated.stat_2231156303@T1` | 1.44098 |
| `rune.stat_243313994` | 1.06268 |
| `crafted.stat_210067635@T2` | 1.03997 |
| `explicit.stat_328541901@T1` | -0.95426 |
| `explicit.stat_328541901@T2` | -0.93143 |
| `desecrated.stat_9187492` | 0.69661 |
| `explicit.stat_1037193709@T1` | 0.64560 |
| `explicit.stat_9187492@T1` | 0.62209 |
| `explicit.stat_748522257@T2` | 0.50961 |
| `explicit.stat_518292764@T1` | -0.50566 |
| `explicit.stat_1940865751@T1` | -0.47861 |

### weapon.staff — n=8623, R²=-0.4348

intercept: `-12.8825`  ·  log_price: True  ·  ilvl: `0.16725`  ·  n_mods: `-0.12906`  ·  n_top_tier: `0.52330`  ·  corrupted: `0.35321`  ·  n_sockets: `0.21349`  ·  quality: `0.04746`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.76699 |
| `explicit.stat_591105508@T1` | 1.34663 |
| `explicit.stat_4226189338@T1` | 1.14530 |
| `explicit.stat_293638271@T2` | -1.10382 |
| `explicit.stat_124131830@T2` | 1.03720 |
| `explicit.stat_4226189338@T2` | 0.83505 |
| `explicit.stat_1263695895@T2` | -0.76434 |
| `explicit.stat_124131830@T1` | 0.75549 |
| `explicit.stat_3962278098@T2` | 0.75105 |
| `explicit.stat_2505884597@T2` | -0.72722 |
| `explicit.stat_2968503605@T1` | -0.62074 |
| `explicit.stat_3291658075@T2` | 0.61875 |

### weapon.sceptre — n=8533, R²=-0.3631

intercept: `-18.0098`  ·  log_price: True  ·  ilvl: `0.22819`  ·  n_mods: `-0.03244`  ·  n_top_tier: `0.31790`  ·  corrupted: `0.53583`  ·  n_sockets: `0.24342`  ·  quality: `0.04727`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.81140 |
| `explicit.stat_2162097452@T2` | 1.69386 |
| `explicit.stat_1250712710@T2` | 1.24926 |
| `explicit.stat_3057012405@T1` | 1.08229 |
| `explicit.stat_1263695895@T1` | -0.93818 |
| `explicit.stat_1263695895@T2` | -0.81356 |
| `explicit.stat_1574590649@T1` | -0.74603 |
| `explicit.stat_2347036682@T2` | -0.73722 |
| `explicit.stat_289128254@T2` | -0.61756 |
| `explicit.stat_2854751904@T2` | -0.58983 |
| `explicit.stat_2347036682@T1` | 0.57286 |
| `explicit.stat_101878827@T1` | 0.54870 |

### weapon.spear — n=7020, R²=-0.4764

intercept: `-10.0181`  ·  log_price: True  ·  ilvl: `0.13644`  ·  n_mods: `-0.06937`  ·  n_top_tier: `0.74795`  ·  corrupted: `-0.07424`  ·  n_sockets: `0.26889`  ·  quality: `0.07122`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -2.90456 |
| `explicit.stat_1202301673@T1` | 1.91931 |
| `explicit.stat_1509134228@T1` | 1.59402 |
| `explicit.stat_9187492@T1` | 1.53263 |
| `explicit.stat_1037193709@T1` | -1.15705 |
| `explicit.stat_1263695895@T2` | -1.03506 |
| `crafted.stat_3035140377` | 1.01380 |
| `explicit.stat_691932474@T1` | -0.92767 |
| `explicit.stat_55876295@T1` | -0.84733 |
| `explicit.stat_1940865751@T2` | -0.84591 |
| `explicit.stat_9187492@T2` | -0.74044 |
| `explicit.stat_748522257@T2` | -0.72061 |

### armour.focus — n=5742, R²=-0.3826

intercept: `-12.4690`  ·  log_price: True  ·  ilvl: `0.16070`  ·  n_mods: `-0.16689`  ·  n_top_tier: `0.80777`  ·  corrupted: `0.29799`  ·  n_sockets: `0.47944`  ·  quality: `0.08521`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 6.29184 |
| `crafted.stat_737908626@T2` | 1.64857 |
| `explicit.stat_3962278098@T1` | -1.35530 |
| `explicit.stat_3291658075@T1` | -1.32824 |
| `explicit.stat_4220027924@T2` | -1.28211 |
| `explicit.stat_2231156303@T2` | -1.05844 |
| `explicit.stat_2923486259@T1` | -1.01276 |
| `explicit.stat_2231156303@T1` | -0.97390 |
| `explicit.stat_2974417149@T1` | -0.95426 |
| `explicit.stat_2339757871@T1` | -0.92973 |
| `explicit.stat_2339757871@T2` | -0.86587 |
| `explicit.stat_2974417149@T2` | -0.86253 |

### armour.quiver — n=5388, R²=-0.3577

intercept: `-13.1146`  ·  log_price: True  ·  ilvl: `0.15900`  ·  n_mods: `-0.09770`  ·  n_top_tier: `0.90728`  ·  corrupted: `0.71204`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.30450 |
| `explicit.stat_2463230181@T1` | 1.86832 |
| `explicit.stat_2321178454@T2` | -1.31180 |
| `explicit.stat_681332047@T2` | -1.30791 |
| `explicit.stat_1573130764@T1` | -1.27713 |
| `explicit.stat_4067062424@T1` | -1.26233 |
| `explicit.stat_803737631@T2` | -1.10143 |
| `explicit.stat_2194114101@T2` | -1.06714 |
| `explicit.stat_2321178454@T1` | -1.00918 |
| `explicit.stat_1573130764@T2` | -1.00398 |
| `explicit.stat_4067062424@T2` | -0.97348 |
| `explicit.stat_803737631@T1` | -0.95897 |

### armour.shield — n=4686, R²=-0.5182

intercept: `-9.8619`  ·  log_price: True  ·  ilvl: `0.12879`  ·  n_mods: `-0.08030`  ·  n_top_tier: `0.56867`  ·  corrupted: `-0.39003`  ·  n_sockets: `0.20246`  ·  quality: `0.06308`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.55008 |
| `explicit.stat_3484657501@T2` | -1.15929 |
| `explicit.stat_2339757871@T1` | -1.12895 |
| `explicit.stat_3484657501@T1` | -1.11824 |
| `explicit.stat_2481353198@T2` | -1.10660 |
| `explicit.stat_1011760251@T2` | -1.03071 |
| `explicit.stat_2481353198@T1` | -0.99422 |
| `explicit.stat_3033371881@T2` | -0.88404 |
| `explicit.stat_3321629045@T2` | -0.88158 |
| `explicit.stat_3855016469@T1` | -0.85086 |
| `explicit.stat_2923486259@T2` | -0.84097 |
| `explicit.stat_328541901@T1` | -0.81801 |

### weapon.twomace — n=4294, R²=-0.504

intercept: `-8.9377`  ·  log_price: True  ·  ilvl: `0.12046`  ·  n_mods: `-0.17727`  ·  n_top_tier: `0.22581`  ·  corrupted: `0.06097`  ·  n_sockets: `0.13636`  ·  quality: `0.05164`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.47038 |
| `desecrated.stat_1509134228@T1` | 3.35973 |
| `explicit.stat_1037193709@T1` | -1.53418 |
| `crafted.stat_3035140377` | 0.87468 |
| `explicit.stat_3336890334@T1` | -0.78375 |
| `explicit.stat_210067635@T2` | 0.64936 |
| `explicit.stat_387439868@T2` | -0.63548 |
| `explicit.stat_1037193709@T2` | -0.61535 |
| `explicit.stat_1509134228@T1` | 0.58245 |
| `explicit.stat_210067635@T1` | 0.54354 |
| `explicit.stat_518292764@T2` | -0.52494 |
| `explicit.stat_9187492@T1` | -0.51408 |

## Coverage (listings per base)

- … **Sapphire** — 26032 listings (25986 priced) [0.3–87761642.7 ex]
- … **Emerald** — 25497 listings (25465 priced) [0.3–87761642.7 ex]
- … **Ruby** — 19523 listings (19503 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10158 listings (10143 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8591 listings (8575 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8347 listings (8326 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8221 listings (8214 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 7804 listings (7789 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 7676 listings (7658 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 7665 listings (7656 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6401 listings (6393 priced) [0.2–307202867.9 ex]
- … **Dueling Wand** — 6209 listings (6191 priced) [0.3–4297682211.9 ex]
- … **Topaz Ring** — 6128 listings (6123 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6118 listings (6112 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5452 listings (5429 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5422 listings (5417 priced) [0.3–19945827.9 ex]
- … **Amber Amulet** — 5287 listings (5281 priced) [0.3–3985176410.3 ex]
- … **Unset Ring** — 5286 listings (5272 priced) [0.2–24532814.5 ex]
- … **Jade Amulet** — 5282 listings (5273 priced) [0.3–4547453.5 ex]
- … **Ancestral Tiara** — 5270 listings (5252 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5108 listings (5100 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 4990 listings (4983 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 4851 listings (4849 priced) [0.3–123132003.2 ex]
- … **Heavy Belt** — 4837 listings (4829 priced) [0.3–398912568423.8 ex]
- … **Lunar Amulet** — 4794 listings (4783 priced) [0.3–91750808.2 ex]

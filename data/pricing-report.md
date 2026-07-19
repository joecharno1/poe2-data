# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-19T07:03:20+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **642805** (640849 priced in exalted)
- Distinct bases: 994 · distinct mods: 3270 · mod rows: 3044654
- Sold signals: **24694** sold · 365499 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-19T06:50:08+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×21.66** (median |log error| 3.0755)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.15** · typical error ×63.83 · ±30% 5% · n=93724
- Premium segment (60ex+): skill **+0.14** · typical error ×311.38 · ±30% 0% · n=63498

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 13540 | ×53.61 | 21% | +0.03 | +0.05 |
| jewel | 12794 | ×10.77 | 4% | +0.10 | +0.13 |
| accessory.amulet | 12278 | ×37.61 | 18% | +0.04 | +0.04 |
| accessory.belt | 8900 | ×21.36 | 16% | +0.07 | +0.10 |
| armour.chest | 8610 | ×15.25 | 22% | +0.08 | +0.10 |
| armour.helmet | 8408 | ×21.89 | 15% | +0.08 | +0.10 |
| armour.boots | 7788 | ×27.86 | 21% | +0.09 | +0.11 |
| armour.gloves | 7659 | ×35.48 | 15% | +0.08 | +0.11 |
| other | 7580 | ×1.91 | 44% | +0.10 | +0.18 |
| weapon.wand | 4605 | ×47.76 | 16% | +0.09 | +0.11 |
| weapon.bow | 3629 | ×30.85 | 14% | +0.13 | +0.13 |
| weapon.crossbow | 3409 | ×31.86 | 16% | +0.10 | +0.14 |
| weapon.warstaff | 2299 | ×22.54 | 6% | +0.20 | +0.21 |
| weapon.staff | 2142 | ×27.17 | 6% | +0.16 | +0.15 |
| weapon.sceptre | 2102 | ×27.75 | 5% | +0.13 | +0.12 |
| weapon.spear | 1704 | ×23.50 | 7% | +0.12 | +0.13 |
| armour.focus | 1419 | ×19.88 | 7% | +0.11 | +0.12 |
| armour.quiver | 1352 | ×23.20 | 7% | +0.16 | +0.17 |
| armour.shield | 1109 | ×17.70 | 8% | +0.08 | +0.10 |
| flask.charm | 1061 | ×13.03 | 31% | -0.00 | +0.02 |
| weapon.twomace | 1028 | ×7.58 | 9% | +0.09 | +0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=69569, R²=-0.9564

intercept: `-1.9241`  ·  log_price: True  ·  ilvl: `0.02578`  ·  n_mods: `0.88675`  ·  n_top_tier: `-0.34563`  ·  corrupted: `0.31419`  ·  quality: `-0.00265`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.41192 |
| `explicit.stat_3374165039@T1` | -2.31207 |
| `explicit.stat_3485067555@T1` | 2.22995 |
| `explicit.stat_3780644166@T1` | -1.96418 |
| `explicit.stat_2523933828@T1` | -1.76256 |
| `explicit.stat_1697447343@T1` | -1.66224 |
| `explicit.stat_4147897060@T1` | -1.60476 |
| `explicit.stat_3174700878@T1` | 1.54155 |
| `explicit.stat_1569101201@T1` | -1.46981 |
| `explicit.stat_21071013@T1` | 1.39419 |
| `explicit.stat_318953428@T1` | -1.30566 |
| `explicit.stat_1594812856@T1` | 1.29185 |

### accessory.ring — n=61626, R²=-2.022

intercept: `3.3555`  ·  log_price: True  ·  ilvl: `-0.04143`  ·  n_mods: `0.00014`  ·  n_top_tier: `1.08229`  ·  corrupted: `0.01750`  ·  n_sockets: `0.03667`  ·  quality: `0.02497`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.13744 |
| `explicit.stat_1573130764@T2` | -1.12314 |
| `explicit.stat_803737631@T1` | -1.11451 |
| `explicit.stat_4220027924@T2` | -1.10775 |
| `explicit.stat_2231156303@T1` | -1.10607 |
| `explicit.stat_3325883026@T1` | -1.09808 |
| `explicit.stat_789117908@T2` | -1.09477 |
| `explicit.stat_4080418644@T1` | -1.09472 |
| `explicit.stat_2923486259@T2` | -1.09449 |
| `explicit.stat_3032590688@T2` | -1.09307 |
| `explicit.stat_2144192055@T1` | -1.09253 |
| `explicit.stat_789117908@T1` | -1.09132 |

### other — n=61319, R²=-0.6247

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00048`  ·  n_top_tier: `0.34610`  ·  corrupted: `0.33087`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.39967 |
| `explicit.stat_3299347043@T1` | -0.25161 |
| `implicit.stat_2219129443` | 0.23021 |
| `implicit.stat_3879011313` | 0.23020 |
| `implicit.stat_4041853756` | 0.23020 |
| `explicit.stat_2968503605@T1` | -0.12368 |
| `explicit.stat_2974417149@T1` | 0.10515 |
| `explicit.stat_736967255@T1` | -0.08491 |
| `explicit.stat_3291658075@T1` | -0.07878 |
| `explicit.stat_789117908@T1` | -0.07378 |
| `explicit.stat_2106365538@T1` | -0.06551 |
| `implicit.stat_2901986750` | -0.05366 |

### accessory.amulet — n=55838, R²=-2.1527

intercept: `3.6551`  ·  log_price: True  ·  ilvl: `-0.04466`  ·  n_mods: `-0.02415`  ·  n_top_tier: `1.24496`  ·  corrupted: `0.05955`  ·  n_sockets: `-0.16638`  ·  quality: `-0.00195`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.90530 |
| `explicit.stat_3299347043@T2` | -1.66232 |
| `explicit.stat_2974417149@T1` | -1.36254 |
| `explicit.stat_587431675@T2` | -1.35306 |
| `explicit.stat_803737631@T1` | -1.33942 |
| `explicit.stat_2974417149@T2` | -1.31951 |
| `explicit.stat_2866361420@T2` | -1.31336 |
| `explicit.stat_2866361420@T1` | -1.30611 |
| `explicit.stat_1050105434@T2` | -1.30142 |
| `explicit.stat_803737631@T2` | -1.29941 |
| `explicit.stat_472520716@T2` | -1.29459 |
| `explicit.stat_1671376347@T2` | -1.28053 |

### accessory.belt — n=40906, R²=-1.541

intercept: `4.4737`  ·  log_price: True  ·  ilvl: `-0.05275`  ·  n_mods: `-0.04310`  ·  n_top_tier: `0.58457`  ·  corrupted: `1.29628`  ·  n_sockets: `1.19323`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.03454 |
| `explicit.stat_4220027924@T1` | 0.85183 |
| `explicit.stat_3299347043@T1` | -0.76563 |
| `explicit.stat_3299347043@T2` | -0.65432 |
| `explicit.stat_2881298780@T1` | -0.65217 |
| `explicit.stat_4220027924@T2` | -0.62369 |
| `explicit.stat_51994685@T1` | -0.61774 |
| `explicit.stat_1570770415@T2` | -0.60534 |
| `explicit.stat_1389754388@T1` | -0.60302 |
| `explicit.stat_3372524247@T2` | -0.60063 |
| `explicit.stat_3325883026@T1` | -0.59988 |
| `explicit.stat_1050105434@T1` | -0.58720 |

### armour.chest — n=40534, R²=-1.7581

intercept: `3.3254`  ·  log_price: True  ·  ilvl: `-0.04106`  ·  n_mods: `-0.01686`  ·  n_top_tier: `0.40437`  ·  corrupted: `0.14906`  ·  n_sockets: `0.02456`  ·  quality: `0.06436`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.81687 |
| `explicit.stat_3981240776@T1` | 0.50357 |
| `explicit.stat_986397080@T2` | -0.48448 |
| `explicit.stat_986397080@T1` | -0.47767 |
| `explicit.stat_915769802@T2` | -0.44932 |
| `explicit.stat_2339757871@T2` | -0.44873 |
| `explicit.stat_3484657501@T1` | -0.44781 |
| `explicit.stat_4080418644@T1` | -0.44044 |
| `explicit.stat_1692879867@T2` | -0.43852 |
| `explicit.stat_915769802@T1` | -0.43603 |
| `explicit.stat_3372524247@T1` | 0.43281 |
| `explicit.stat_3261801346@T2` | -0.42978 |

### armour.helmet — n=39409, R²=-1.6111

intercept: `3.3775`  ·  log_price: True  ·  ilvl: `-0.04268`  ·  n_mods: `-0.02825`  ·  n_top_tier: `0.51569`  ·  corrupted: `0.69070`  ·  n_sockets: `0.06063`  ·  quality: `0.05865`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.59137 |
| `explicit.stat_3917489142@T2` | -0.91033 |
| `explicit.stat_1263695895@T1` | -0.85026 |
| `explicit.stat_3917489142@T1` | -0.82580 |
| `explicit.stat_1263695895@T2` | -0.69352 |
| `explicit.stat_2162097452@T2` | -0.69210 |
| `explicit.stat_4052037485@T2` | -0.60774 |
| `explicit.stat_1999113824@T1` | -0.60536 |
| `explicit.stat_803737631@T1` | -0.59775 |
| `explicit.stat_803737631@T2` | -0.58551 |
| `explicit.stat_3321629045@T2` | -0.57025 |
| `explicit.stat_53045048@T1` | -0.56675 |

### armour.boots — n=36647, R²=-1.7263

intercept: `3.5252`  ·  log_price: True  ·  ilvl: `-0.04332`  ·  n_mods: `-0.02111`  ·  n_top_tier: `0.60911`  ·  corrupted: `0.02287`  ·  n_sockets: `0.02961`  ·  quality: `0.06181`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.59345 |
| `explicit.stat_2339757871@T1` | -1.07923 |
| `crafted.stat_3917489142@T1` | 1.07425 |
| `explicit.stat_3299347043@T1` | -0.78182 |
| `explicit.stat_3917489142@T2` | -0.74917 |
| `explicit.stat_2923486259@T1` | 0.73446 |
| `explicit.stat_2923486259@T2` | -0.67069 |
| `explicit.stat_1062208444@T2` | -0.66355 |
| `explicit.stat_3917489142@T1` | -0.65541 |
| `explicit.stat_2160282525@T1` | -0.65152 |
| `explicit.stat_3321629045@T1` | -0.64547 |
| `explicit.stat_1999113824@T2` | -0.64420 |

### armour.gloves — n=35668, R²=-1.6687

intercept: `3.7678`  ·  log_price: True  ·  ilvl: `-0.04826`  ·  n_mods: `-0.02871`  ·  n_top_tier: `0.71138`  ·  corrupted: `-0.02338`  ·  n_sockets: `0.12116`  ·  quality: `0.05094`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 4.85874 |
| `rune.stat_201332984` | 1.69885 |
| `explicit.stat_2923486259@T1` | -1.42122 |
| `explicit.stat_3484657501@T2` | -0.97283 |
| `explicit.stat_2923486259@T2` | -0.96229 |
| `explicit.stat_803737631@T2` | -0.91251 |
| `explicit.stat_3321629045@T2` | -0.90917 |
| `explicit.stat_803737631@T1` | -0.88757 |
| `explicit.stat_4015621042@T2` | -0.88654 |
| `explicit.stat_4052037485@T1` | -0.88286 |
| `explicit.stat_3484657501@T1` | -0.85508 |
| `explicit.stat_9187492@T2` | -0.84924 |

### weapon.wand — n=21541, R²=-2.0163

intercept: `3.8081`  ·  log_price: True  ·  ilvl: `-0.04734`  ·  n_mods: `-0.04007`  ·  n_top_tier: `0.48987`  ·  corrupted: `0.00001`  ·  n_sockets: `0.06319`  ·  quality: `0.01971`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.94349 |
| `explicit.stat_1545858329@T1` | 2.57721 |
| `explicit.stat_124131830@T1` | 2.34720 |
| `explicit.stat_2254480358@T1` | 2.31954 |
| `explicit.stat_591105508@T1` | 1.87690 |
| `explicit.stat_4226189338@T1` | 1.83232 |
| `explicit.stat_736967255@T2` | 1.62762 |
| `crafted.stat_124131830` | 1.24144 |
| `explicit.stat_2254480358@T2` | 0.95250 |
| `explicit.stat_1263695895@T2` | -0.89595 |
| `explicit.stat_4226189338@T2` | 0.84887 |
| `explicit.stat_1263695895@T1` | -0.80581 |

### flask.charm — n=17637, R²=-0.6136

intercept: `0.1001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.51145`  ·  corrupted: `1.60550`  ·  quality: `0.00095`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.73755 |
| `explicit.stat_1056492907` | 2.75485 |
| `explicit.stat_828533480@T2` | -1.51149 |
| `explicit.stat_1120862500@T2` | -1.51145 |
| `explicit.stat_1873752457@T2` | -1.51145 |
| `explicit.stat_1873752457@T1` | -1.51143 |
| `explicit.stat_3196823591@T2` | -1.51142 |
| `explicit.stat_2365392475@T2` | -1.51141 |
| `explicit.stat_2676834156@T2` | -1.51139 |
| `explicit.stat_388617051@T2` | -1.51129 |
| `explicit.stat_828533480@T1` | -1.51125 |
| `explicit.stat_1366840608@T2` | -1.50464 |

### weapon.bow — n=17201, R²=-1.9162

intercept: `3.8031`  ·  log_price: True  ·  ilvl: `-0.04473`  ·  n_mods: `-0.07907`  ·  n_top_tier: `0.70228`  ·  corrupted: `0.38577`  ·  n_sockets: `0.06565`  ·  quality: `0.03339`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.44813 |
| `explicit.stat_1263695895@T1` | -1.18630 |
| `explicit.stat_1263695895@T2` | -1.03456 |
| `desecrated.stat_666077204@T1` | -0.97936 |
| `explicit.stat_2463230181@T2` | -0.97744 |
| `explicit.stat_3336890334@T1` | 0.97519 |
| `explicit.stat_1509134228@T1` | -0.80978 |
| `explicit.stat_1037193709@T1` | -0.79829 |
| `explicit.stat_3695891184@T2` | -0.79306 |
| `explicit.stat_1037193709@T2` | -0.78870 |
| `explicit.stat_3639275092@T1` | -0.78701 |
| `explicit.stat_210067635@T2` | -0.78187 |

### weapon.crossbow — n=16151, R²=-1.7895

intercept: `3.9244`  ·  log_price: True  ·  ilvl: `-0.04743`  ·  n_mods: `-0.07696`  ·  n_top_tier: `0.47425`  ·  corrupted: `0.06933`  ·  n_sockets: `0.07081`  ·  quality: `0.02475`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.66516 |
| `explicit.stat_1980802737` | 1.31566 |
| `explicit.stat_1202301673@T1` | 1.31476 |
| `explicit.stat_2250681686@T2` | -1.24685 |
| `explicit.stat_2250681686` | 0.90737 |
| `explicit.stat_709508406@T1` | 0.87284 |
| `explicit.stat_1509134228@T1` | 0.72275 |
| `crafted.stat_3035140377` | 0.71780 |
| `explicit.stat_3336890334@T1` | -0.71624 |
| `explicit.stat_1263695895@T2` | -0.68961 |
| `explicit.stat_3336890334@T2` | -0.65261 |
| `explicit.stat_3695891184@T1` | -0.63052 |

### weapon.warstaff — n=10908, R²=-0.3502

intercept: `-10.4694`  ·  log_price: True  ·  ilvl: `0.14249`  ·  n_mods: `-0.23064`  ·  n_top_tier: `0.32562`  ·  corrupted: `0.41056`  ·  n_sockets: `0.13831`  ·  quality: `0.05681`

| stat_id | coef |
|---|---|
| `desecrated.stat_473429811@T1` | -1.95791 |
| `desecrated.stat_3291658075@T1` | -1.95791 |
| `desecrated.stat_2527686725@T1` | 1.79298 |
| `desecrated.stat_2231156303@T1` | 1.79298 |
| `crafted.stat_210067635@T2` | 1.22956 |
| `rune.stat_243313994` | 0.84172 |
| `explicit.stat_328541901@T1` | -0.82831 |
| `explicit.stat_1037193709@T1` | 0.79963 |
| `explicit.stat_328541901@T2` | -0.77034 |
| `desecrated.stat_9187492` | 0.74016 |
| `explicit.stat_1509134228@T1` | 0.71298 |
| `explicit.stat_1368271171@T1` | -0.62768 |

### weapon.staff — n=10274, R²=-0.381

intercept: `-15.7009`  ·  log_price: True  ·  ilvl: `0.20123`  ·  n_mods: `-0.07891`  ·  n_top_tier: `0.51583`  ·  corrupted: `0.68914`  ·  n_sockets: `0.19928`  ·  quality: `0.03475`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.20189 |
| `explicit.stat_591105508@T1` | 2.03205 |
| `explicit.stat_4226189338@T1` | 1.98032 |
| `explicit.stat_293638271@T2` | -1.48388 |
| `explicit.stat_124131830@T1` | 1.37863 |
| `explicit.stat_1600707273@T1` | 1.06514 |
| `explicit.stat_2254480358@T1` | 0.94785 |
| `explicit.stat_473429811@T2` | -0.69957 |
| `explicit.stat_124131830@T2` | 0.69803 |
| `explicit.stat_274716455@T1` | -0.69466 |
| `explicit.stat_3278136794@T1` | -0.65715 |
| `explicit.stat_2254480358@T2` | 0.61951 |

### weapon.sceptre — n=10088, R²=-0.3361

intercept: `-20.3713`  ·  log_price: True  ·  ilvl: `0.26175`  ·  n_mods: `0.00502`  ·  n_top_tier: `0.36014`  ·  corrupted: `-0.02424`  ·  n_sockets: `0.27378`  ·  quality: `0.02653`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.32211 |
| `explicit.stat_3057012405@T1` | 1.24692 |
| `explicit.stat_2162097452@T2` | 1.16220 |
| `explicit.stat_1250712710@T2` | 0.98743 |
| `explicit.stat_2854751904@T2` | -0.78812 |
| `explicit.stat_2347036682@T2` | -0.69960 |
| `explicit.stat_1798257884@T2` | 0.66056 |
| `explicit.stat_101878827@T1` | 0.65608 |
| `explicit.stat_101878827@T2` | 0.61268 |
| `explicit.stat_3639275092@T2` | -0.60809 |
| `explicit.stat_1263695895@T2` | -0.60458 |
| `explicit.stat_849987426@T1` | 0.55229 |

### weapon.spear — n=8167, R²=-0.3757

intercept: `-12.5085`  ·  log_price: True  ·  ilvl: `0.17541`  ·  n_mods: `-0.19800`  ·  n_top_tier: `0.74209`  ·  corrupted: `-0.14785`  ·  n_sockets: `0.23149`  ·  quality: `0.06987`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.80874 |
| `explicit.stat_1202301673@T1` | 1.64846 |
| `explicit.stat_1509134228@T1` | 1.49715 |
| `desecrated.stat_210067635@T1` | -1.34255 |
| `explicit.stat_9187492@T1` | 1.21273 |
| `explicit.stat_1940865751@T2` | -1.11550 |
| `explicit.stat_4080418644@T2` | -1.05703 |
| `explicit.stat_9187492@T2` | -1.04926 |
| `explicit.stat_691932474@T2` | -0.96842 |
| `explicit.stat_691932474@T1` | -0.95918 |
| `crafted.stat_3035140377` | 0.92171 |
| `explicit.stat_4080418644@T1` | -0.83906 |

### armour.focus — n=6672, R²=-0.3377

intercept: `-14.3813`  ·  log_price: True  ·  ilvl: `0.18548`  ·  n_mods: `-0.19032`  ·  n_top_tier: `0.92803`  ·  corrupted: `0.32233`  ·  n_sockets: `0.39017`  ·  quality: `0.04650`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | 2.74798 |
| `crafted.stat_2974417149@T1` | 2.13883 |
| `explicit.stat_2923486259@T1` | -1.64391 |
| `explicit.stat_4220027924@T1` | -1.47474 |
| `explicit.stat_4220027924@T2` | -1.45904 |
| `explicit.stat_3291658075@T1` | -1.25824 |
| `explicit.stat_2974417149@T1` | -1.25010 |
| `explicit.stat_2974417149@T2` | -1.18429 |
| `explicit.stat_2231156303@T2` | -1.08655 |
| `explicit.stat_2339757871@T2` | -1.04507 |
| `explicit.stat_737908626@T2` | -0.98758 |
| `explicit.stat_274716455@T2` | -0.95734 |

### armour.quiver — n=6265, R²=-0.305

intercept: `-15.9750`  ·  log_price: True  ·  ilvl: `0.19437`  ·  n_mods: `-0.13603`  ·  n_top_tier: `0.90943`  ·  corrupted: `0.74252`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.07905 |
| `explicit.stat_2463230181@T1` | 2.29973 |
| `explicit.stat_681332047@T2` | -1.44879 |
| `explicit.stat_1573130764@T1` | -1.41880 |
| `explicit.stat_4067062424@T1` | -1.10626 |
| `explicit.stat_803737631@T2` | -1.08715 |
| `explicit.stat_1573130764@T2` | -1.07068 |
| `explicit.stat_2463230181@T2` | 1.05098 |
| `explicit.stat_2194114101@T2` | -1.03958 |
| `explicit.stat_681332047@T1` | -1.03016 |
| `explicit.stat_4067062424@T2` | -0.99697 |
| `explicit.stat_803737631@T1` | -0.98385 |

### armour.shield — n=5387, R²=-0.4562

intercept: `-12.3554`  ·  log_price: True  ·  ilvl: `0.16293`  ·  n_mods: `-0.07624`  ·  n_top_tier: `0.54654`  ·  corrupted: `-0.27407`  ·  n_sockets: `0.34378`  ·  quality: `0.06441`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.23145 |
| `explicit.stat_1301765461@T1` | 1.19505 |
| `explicit.stat_3321629045@T2` | -1.15051 |
| `explicit.stat_3855016469@T1` | -1.00671 |
| `explicit.stat_4095671657@T1` | -0.97925 |
| `explicit.stat_3484657501@T2` | -0.95822 |
| `explicit.stat_4095671657@T2` | -0.92392 |
| `explicit.stat_3033371881@T2` | -0.91623 |
| `explicit.stat_328541901@T1` | -0.83992 |
| `explicit.stat_2901986750@T1` | -0.82657 |
| `explicit.stat_1671376347@T1` | -0.70203 |
| `explicit.stat_4220027924@T1` | -0.69464 |

### weapon.twomace — n=4978, R²=-0.4549

intercept: `-9.7160`  ·  log_price: True  ·  ilvl: `0.13499`  ·  n_mods: `-0.21848`  ·  n_top_tier: `0.33293`  ·  corrupted: `0.30014`  ·  n_sockets: `0.15250`  ·  quality: `0.06173`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.41057 |
| `desecrated.stat_1509134228@T1` | 1.71714 |
| `explicit.stat_1037193709@T1` | -1.36701 |
| `explicit.stat_3336890334@T1` | -1.11811 |
| `explicit.stat_9187492@T1` | -0.88957 |
| `explicit.stat_709508406@T1` | 0.76750 |
| `explicit.stat_1263695895@T2` | -0.74277 |
| `explicit.stat_387439868@T2` | -0.67987 |
| `explicit.stat_691932474@T1` | -0.67664 |
| `explicit.stat_210067635@T2` | 0.65832 |
| `explicit.stat_1509134228@T1` | 0.60126 |
| `explicit.stat_821021828@T2` | -0.58657 |

## Coverage (listings per base)

- … **Sapphire** — 32246 listings (32192 priced) [0.3–3985176410.3 ex]
- … **Emerald** — 31332 listings (31291 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 24055 listings (24025 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11674 listings (11659 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10449 listings (10427 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10122 listings (10098 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9972 listings (9962 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 9439 listings (9419 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9316 listings (9296 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8948 listings (8935 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7751 listings (7737 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7467 listings (7459 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7353 listings (7346 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6907 listings (6886 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6479 listings (6472 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 6387 listings (6369 priced) [0.2–39887666593.4 ex]
- … **Plate Belt** — 6383 listings (6355 priced) [0.3–398912568423.8 ex]
- … **Jade Amulet** — 6368 listings (6356 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6344 listings (6337 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6263 listings (6236 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6167 listings (6158 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 6128 listings (6121 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5803 listings (5800 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5747 listings (5734 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5648 listings (5639 priced) [0.3–398912568423.8 ex]

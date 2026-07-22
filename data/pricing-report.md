# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-22T19:08:23+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **744971** (742577 priced in exalted)
- Distinct bases: 1002 · distinct mods: 3339 · mod rows: 3520140
- Sold signals: **24011** sold · 423787 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-22T18:54:43+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×18.16** (median |log error| 2.8994)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.16** · typical error ×49.52 · ±30% 5% · n=108116
- Premium segment (60ex+): skill **+0.15** · typical error ×272.00 · ±30% 0% · n=71684

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 16158 | ×38.90 | 21% | +0.04 | +0.07 |
| jewel | 15577 | ×10.24 | 4% | +0.11 | +0.13 |
| accessory.amulet | 14456 | ×24.51 | 16% | +0.04 | +0.04 |
| accessory.belt | 10150 | ×25.86 | 17% | +0.06 | +0.09 |
| armour.chest | 9864 | ×16.48 | 22% | +0.08 | +0.11 |
| armour.helmet | 9571 | ×23.35 | 16% | +0.09 | +0.12 |
| armour.boots | 8868 | ×23.15 | 18% | +0.11 | +0.13 |
| armour.gloves | 8715 | ×30.99 | 12% | +0.09 | +0.11 |
| other | 8621 | ×1.88 | 44% | +0.12 | +0.17 |
| weapon.wand | 5088 | ×35.39 | 13% | +0.13 | +0.13 |
| weapon.bow | 3997 | ×23.43 | 9% | +0.18 | +0.21 |
| weapon.crossbow | 3767 | ×22.11 | 11% | +0.14 | +0.18 |
| weapon.warstaff | 2607 | ×13.73 | 7% | +0.15 | +0.16 |
| weapon.staff | 2518 | ×15.27 | 6% | +0.13 | +0.13 |
| weapon.sceptre | 2483 | ×17.96 | 5% | +0.06 | +0.07 |
| weapon.spear | 1960 | ×12.23 | 7% | +0.12 | +0.16 |
| armour.focus | 1640 | ×13.34 | 6% | +0.09 | +0.11 |
| armour.quiver | 1548 | ×17.71 | 7% | +0.12 | +0.14 |
| armour.shield | 1258 | ×8.05 | 8% | +0.11 | +0.11 |
| flask.charm | 1248 | ×10.00 | 27% | +0.03 | +0.03 |
| weapon.twomace | 1160 | ×8.44 | 7% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=85739, R²=-0.999

intercept: `-1.9027`  ·  log_price: True  ·  ilvl: `0.02378`  ·  n_mods: `0.71983`  ·  n_top_tier: `-0.14419`  ·  corrupted: `0.44767`  ·  quality: `-0.14842`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.35865 |
| `explicit.stat_1869147066@T1` | -3.16928 |
| `explicit.stat_3668351662@T1` | -2.02831 |
| `explicit.stat_1594812856@T1` | 1.89202 |
| `explicit.stat_239367161@T1` | -1.59019 |
| `explicit.stat_3780644166@T1` | -1.56303 |
| `explicit.stat_3485067555@T1` | 1.54782 |
| `explicit.stat_3028809864@T1` | -1.54191 |
| `explicit.stat_1697447343@T1` | -1.38853 |
| `explicit.stat_2456523742@T1` | 1.30757 |
| `explicit.stat_3374165039@T1` | -1.26658 |
| `explicit.stat_627767961@T1` | -1.25410 |

### accessory.ring — n=73556, R²=-2.0169

intercept: `3.2108`  ·  log_price: True  ·  ilvl: `-0.04030`  ·  n_mods: `0.00045`  ·  n_top_tier: `0.98139`  ·  corrupted: `-0.00564`  ·  n_sockets: `2.20008`  ·  quality: `-0.00390`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.04129 |
| `explicit.stat_1263695895@T2` | -1.01042 |
| `explicit.stat_1573130764@T2` | -1.00386 |
| `explicit.stat_3917489142@T2` | -1.00244 |
| `explicit.stat_4080418644@T1` | -1.00089 |
| `explicit.stat_1263695895@T1` | -0.99993 |
| `explicit.stat_1671376347@T2` | -0.99845 |
| `explicit.stat_2891184298@T2` | -0.99731 |
| `explicit.stat_2901986750@T2` | -0.99663 |
| `explicit.stat_2923486259@T2` | -0.99621 |
| `explicit.stat_3372524247@T2` | -0.99615 |
| `explicit.stat_3325883026@T1` | -0.99582 |

### other — n=70905, R²=-0.6838

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.05631`  ·  n_top_tier: `0.29027`  ·  corrupted: `0.00000`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.41493 |
| `explicit.stat_3299347043@T1` | -0.26055 |
| `implicit.stat_2219129443` | 0.22461 |
| `explicit.stat_3917489142@T1` | -0.16898 |
| `implicit.stat_3182714256` | 0.16895 |
| `implicit.stat_718638445` | 0.16895 |
| `explicit.stat_2974417149@T1` | 0.11894 |
| `explicit.stat_789117908@T1` | -0.07024 |
| `implicit.stat_3879011313` | 0.05688 |
| `implicit.stat_958696139` | -0.05630 |
| `explicit.stat_736967255@T1` | -0.04742 |
| `implicit.stat_1416292992` | -0.03754 |

### accessory.amulet — n=65789, R²=-2.0793

intercept: `3.0582`  ·  log_price: True  ·  ilvl: `-0.04009`  ·  n_mods: `-0.00542`  ·  n_top_tier: `0.92468`  ·  corrupted: `0.05423`  ·  n_sockets: `-0.08054`  ·  quality: `0.06868`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.57831 |
| `explicit.stat_3299347043@T2` | -1.54022 |
| `explicit.stat_2866361420@T1` | -1.05086 |
| `explicit.stat_1202301673@T2` | -1.04504 |
| `explicit.stat_2974417149@T1` | -1.04064 |
| `explicit.stat_2974417149@T2` | -1.02832 |
| `explicit.stat_2901986750@T1` | -1.02811 |
| `explicit.stat_4080418644@T1` | -1.01810 |
| `explicit.stat_2866361420@T2` | -1.01675 |
| `explicit.stat_803737631@T1` | -1.00954 |
| `explicit.stat_1050105434@T1` | -0.97487 |
| `explicit.stat_3261801346@T1` | -0.97409 |

### accessory.belt — n=46458, R²=-1.65

intercept: `4.4113`  ·  log_price: True  ·  ilvl: `-0.05345`  ·  n_mods: `-0.02627`  ·  n_top_tier: `0.83390`  ·  corrupted: `1.20834`  ·  n_sockets: `1.60045`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.22372 |
| `explicit.stat_3299347043@T2` | -0.86976 |
| `explicit.stat_915769802@T1` | -0.86810 |
| `explicit.stat_2881298780@T1` | -0.86692 |
| `explicit.stat_809229260@T2` | -0.85458 |
| `explicit.stat_51994685@T1` | -0.85372 |
| `explicit.stat_3299347043@T1` | -0.85077 |
| `explicit.stat_1570770415@T2` | -0.84659 |
| `explicit.stat_3325883026@T1` | -0.84372 |
| `explicit.stat_915769802@T2` | -0.83687 |
| `explicit.stat_3585532255@T2` | -0.83651 |
| `explicit.stat_2881298780@T2` | -0.83607 |

### armour.chest — n=46039, R²=-1.7931

intercept: `3.3024`  ·  log_price: True  ·  ilvl: `-0.04062`  ·  n_mods: `-0.01549`  ·  n_top_tier: `0.35894`  ·  corrupted: `0.33484`  ·  n_sockets: `0.02719`  ·  quality: `0.07750`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.83767 |
| `explicit.stat_986397080@T2` | -0.41689 |
| `explicit.stat_4080418644@T2` | -0.40260 |
| `explicit.stat_1692879867@T2` | -0.39389 |
| `explicit.stat_986397080@T1` | -0.39254 |
| `explicit.stat_4080418644@T1` | -0.38808 |
| `explicit.stat_915769802@T2` | -0.38307 |
| `explicit.stat_3484657501@T1` | -0.38292 |
| `explicit.stat_2451402625@T2` | -0.37772 |
| `explicit.stat_915769802@T1` | -0.37565 |
| `explicit.stat_1062208444@T2` | -0.37464 |
| `explicit.stat_1999113824@T1` | -0.36955 |

### armour.helmet — n=44813, R²=-1.6815

intercept: `3.3954`  ·  log_price: True  ·  ilvl: `-0.04247`  ·  n_mods: `-0.03040`  ·  n_top_tier: `0.52710`  ·  corrupted: `0.57200`  ·  n_sockets: `0.09455`  ·  quality: `0.07142`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.65089 |
| `crafted.stat_3917489142@T1` | 2.12725 |
| `explicit.stat_1263695895@T1` | -0.91613 |
| `explicit.stat_3917489142@T2` | -0.74683 |
| `explicit.stat_2162097452@T2` | -0.70059 |
| `explicit.stat_3917489142@T1` | -0.67322 |
| `explicit.stat_1263695895@T2` | -0.65375 |
| `explicit.stat_4052037485@T2` | -0.62974 |
| `explicit.stat_4015621042@T2` | -0.62671 |
| `explicit.stat_3321629045@T2` | -0.58301 |
| `explicit.stat_1999113824@T1` | -0.58197 |
| `explicit.stat_803737631@T1` | -0.57493 |

### armour.boots — n=41343, R²=-1.6804

intercept: `3.7398`  ·  log_price: True  ·  ilvl: `-0.04609`  ·  n_mods: `-0.03300`  ·  n_top_tier: `0.44125`  ·  corrupted: `0.09623`  ·  n_sockets: `0.06788`  ·  quality: `0.07109`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.19694 |
| `explicit.stat_2250533757@T1` | 1.75007 |
| `crafted.stat_3917489142@T1` | 1.37316 |
| `explicit.stat_2923486259@T1` | 0.64164 |
| `explicit.stat_3299347043@T1` | -0.61890 |
| `explicit.stat_2923486259@T2` | -0.55285 |
| `explicit.stat_3917489142@T2` | -0.49872 |
| `explicit.stat_1671376347@T2` | -0.49570 |
| `explicit.stat_1874553720@T1` | -0.49490 |
| `explicit.stat_99927264@T1` | -0.49463 |
| `explicit.stat_2160282525@T1` | -0.49138 |
| `explicit.stat_2451402625@T1` | -0.48026 |

### armour.gloves — n=40363, R²=-1.6382

intercept: `3.9828`  ·  log_price: True  ·  ilvl: `-0.05232`  ·  n_mods: `-0.00387`  ·  n_top_tier: `0.66633`  ·  corrupted: `-0.03729`  ·  n_sockets: `0.20277`  ·  quality: `0.05865`

| stat_id | coef |
|---|---|
| `explicit.stat_4052037485@T1` | -1.02487 |
| `explicit.stat_4052037485@T2` | -0.92960 |
| `explicit.stat_3321629045@T2` | -0.91842 |
| `explicit.stat_3917489142@T2` | -0.86125 |
| `explicit.stat_3484657501@T2` | -0.83675 |
| `explicit.stat_124859000@T1` | -0.82362 |
| `explicit.stat_2923486259@T1` | -0.82253 |
| `explicit.stat_4015621042@T2` | -0.82135 |
| `explicit.stat_9187492@T2` | -0.82061 |
| `explicit.stat_3484657501@T1` | -0.81903 |
| `explicit.stat_124859000@T2` | -0.77925 |
| `explicit.stat_803737631@T1` | -0.77818 |

### weapon.wand — n=23616, R²=-1.828

intercept: `3.9574`  ·  log_price: True  ·  ilvl: `-0.04886`  ·  n_mods: `-0.06986`  ·  n_top_tier: `0.59675`  ·  corrupted: `0.18257`  ·  n_sockets: `0.01742`  ·  quality: `0.02943`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.19832 |
| `explicit.stat_1545858329@T1` | 2.71006 |
| `explicit.stat_2254480358@T1` | 2.62309 |
| `explicit.stat_591105508@T1` | 2.18570 |
| `explicit.stat_124131830@T1` | 2.02972 |
| `explicit.stat_4226189338@T1` | 1.49700 |
| `explicit.stat_2254480358@T2` | 1.32674 |
| `crafted.stat_124131830` | 1.24052 |
| `explicit.stat_1263695895@T2` | -1.03952 |
| `explicit.stat_1600707273@T1` | 1.01382 |
| `explicit.stat_473429811@T1` | -0.88838 |
| `explicit.stat_473429811@T2` | -0.85487 |

### flask.charm — n=20931, R²=-0.667

intercept: `0.1070`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.39285`  ·  corrupted: `1.44309`  ·  quality: `0.03597`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.59506 |
| `explicit.stat_1056492907` | 2.52775 |
| `explicit.stat_3246948616` | 2.29748 |
| `explicit.stat_828533480@T2` | -1.39288 |
| `explicit.stat_1120862500@T2` | -1.39286 |
| `explicit.stat_1873752457@T2` | -1.39286 |
| `explicit.stat_388617051@T2` | -1.39284 |
| `explicit.stat_2541588185@T2` | -1.39284 |
| `explicit.stat_2365392475@T2` | -1.39279 |
| `explicit.stat_3196823591@T2` | -1.39192 |
| `explicit.stat_2676834156@T2` | -1.39086 |
| `explicit.stat_1873752457@T1` | -1.39067 |

### weapon.bow — n=18897, R²=-1.6398

intercept: `4.1374`  ·  log_price: True  ·  ilvl: `-0.04874`  ·  n_mods: `-0.12634`  ·  n_top_tier: `0.74442`  ·  corrupted: `0.55927`  ·  n_sockets: `0.07654`  ·  quality: `0.03235`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 5.24786 |
| `desecrated.stat_210067635@T1` | -1.60990 |
| `explicit.stat_1263695895@T1` | -1.51279 |
| `crafted.stat_210067635@T2` | -1.46227 |
| `explicit.stat_1263695895@T2` | -1.34593 |
| `crafted.stat_3035140377` | 1.10382 |
| `explicit.stat_1509134228@T1` | -1.04622 |
| `explicit.stat_2463230181@T2` | -1.03175 |
| `explicit.stat_3695891184@T1` | -0.98669 |
| `explicit.stat_210067635@T2` | -0.97939 |
| `explicit.stat_1368271171@T1` | -0.93538 |
| `explicit.stat_1368271171@T2` | -0.92945 |

### weapon.crossbow — n=17678, R²=-1.5503

intercept: `4.1277`  ·  log_price: True  ·  ilvl: `-0.04807`  ·  n_mods: `-0.12059`  ·  n_top_tier: `0.38627`  ·  corrupted: `-0.00929`  ·  n_sockets: `0.11028`  ·  quality: `0.01674`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.77468 |
| `explicit.stat_1980802737` | 1.47709 |
| `explicit.stat_2250681686@T2` | -1.33117 |
| `explicit.stat_1202301673@T1` | 1.25195 |
| `explicit.stat_2250681686` | 1.00820 |
| `explicit.stat_1509134228@T1` | 0.96908 |
| `crafted.stat_3035140377` | 0.83514 |
| `explicit.stat_709508406@T1` | 0.82972 |
| `explicit.stat_210067635@T2` | -0.71116 |
| `explicit.stat_3336890334@T2` | -0.70260 |
| `explicit.stat_3695891184@T1` | -0.70093 |
| `explicit.stat_3695891184@T2` | -0.66187 |

### weapon.warstaff — n=12530, R²=-0.3247

intercept: `-10.5120`  ·  log_price: True  ·  ilvl: `0.14311`  ·  n_mods: `-0.24022`  ·  n_top_tier: `0.51740`  ·  corrupted: `0.30758`  ·  n_sockets: `0.12871`  ·  quality: `0.05246`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 1.13738 |
| `desecrated.stat_2231156303@T1` | 1.13738 |
| `explicit.stat_821021828@T2` | -0.94529 |
| `crafted.stat_210067635@T2` | 0.94298 |
| `explicit.stat_328541901@T2` | -0.88430 |
| `explicit.stat_210067635@T1` | -0.85362 |
| `explicit.stat_328541901@T1` | -0.84420 |
| `desecrated.stat_9187492` | 0.80873 |
| `explicit.stat_1940865751@T1` | -0.80258 |
| `rune.stat_243313994` | 0.78879 |
| `explicit.stat_1037193709@T2` | -0.76429 |
| `explicit.stat_1940865751@T2` | -0.72719 |

### weapon.staff — n=11954, R²=-0.3449

intercept: `-16.7510`  ·  log_price: True  ·  ilvl: `0.21561`  ·  n_mods: `-0.10391`  ·  n_top_tier: `0.46745`  ·  corrupted: `1.00271`  ·  n_sockets: `0.20507`  ·  quality: `0.03289`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.22957 |
| `explicit.stat_124131830@T1` | 1.74356 |
| `explicit.stat_4226189338@T1` | 1.61037 |
| `explicit.stat_1600707273@T1` | 1.58453 |
| `explicit.stat_1545858329@T1` | 1.28827 |
| `explicit.stat_3962278098@T2` | 0.94039 |
| `explicit.stat_591105508@T2` | 0.93663 |
| `explicit.stat_473429811@T2` | -0.79661 |
| `explicit.stat_1263695895@T1` | 0.71532 |
| `explicit.stat_293638271@T2` | -0.64733 |
| `explicit.stat_4226189338@T2` | 0.57872 |
| `explicit.stat_3015669065@T2` | -0.56423 |

### weapon.sceptre — n=11588, R²=-0.3344

intercept: `-21.1961`  ·  log_price: True  ·  ilvl: `0.27044`  ·  n_mods: `-0.05208`  ·  n_top_tier: `-0.02130`  ·  corrupted: `0.25209`  ·  n_sockets: `0.22037`  ·  quality: `0.03473`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.82352 |
| `explicit.stat_2162097452@T2` | 1.33706 |
| `explicit.stat_1798257884@T2` | 1.15044 |
| `explicit.stat_3057012405@T1` | 1.02421 |
| `explicit.stat_101878827@T1` | 0.78102 |
| `explicit.stat_101878827@T2` | 0.68984 |
| `explicit.stat_4080418644@T2` | -0.68101 |
| `explicit.stat_1250712710@T2` | 0.62448 |
| `explicit.stat_2347036682@T1` | 0.58583 |
| `desecrated.stat_2162097452` | 0.57284 |
| `explicit.stat_328541901@T2` | 0.54481 |
| `explicit.stat_1998951374@T1` | 0.53640 |

### weapon.spear — n=9440, R²=-0.3865

intercept: `-14.1859`  ·  log_price: True  ·  ilvl: `0.19142`  ·  n_mods: `-0.14269`  ·  n_top_tier: `0.56520`  ·  corrupted: `-0.59909`  ·  n_sockets: `0.21668`  ·  quality: `0.06249`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.95040 |
| `desecrated.stat_666077204@T1` | -2.21093 |
| `explicit.stat_1037193709@T1` | -1.24515 |
| `crafted.stat_3035140377` | 1.13272 |
| `explicit.stat_4080418644@T2` | -1.13185 |
| `explicit.stat_9187492@T2` | -1.02157 |
| `explicit.stat_748522257@T2` | -1.00879 |
| `explicit.stat_1940865751@T2` | -0.98588 |
| `explicit.stat_4080418644@T1` | -0.95862 |
| `desecrated.stat_210067635@T1` | -0.95090 |
| `explicit.stat_3336890334@T2` | -0.93728 |
| `explicit.stat_1202301673@T1` | 0.87706 |

### armour.focus — n=7716, R²=-0.334

intercept: `-16.3471`  ·  log_price: True  ·  ilvl: `0.20859`  ·  n_mods: `-0.14377`  ·  n_top_tier: `0.98902`  ·  corrupted: `-0.14879`  ·  n_sockets: `0.40712`  ·  quality: `0.03371`

| stat_id | coef |
|---|---|
| `explicit.stat_4220027924@T1` | -1.55019 |
| `crafted.stat_737908626@T2` | 1.39777 |
| `explicit.stat_2923486259@T2` | -1.33925 |
| `explicit.stat_2923486259@T1` | -1.33432 |
| `explicit.stat_2231156303@T1` | -1.30397 |
| `explicit.stat_2768835289@T1` | -1.21684 |
| `explicit.stat_3962278098@T2` | -1.18155 |
| `explicit.stat_2339757871@T2` | -1.16654 |
| `explicit.stat_4220027924@T2` | -1.14572 |
| `explicit.stat_3291658075@T2` | -1.14021 |
| `explicit.stat_2231156303@T2` | -1.13085 |
| `explicit.stat_4015621042@T1` | -1.11836 |

### armour.quiver — n=7176, R²=-0.267

intercept: `-18.8961`  ·  log_price: True  ·  ilvl: `0.22765`  ·  n_mods: `-0.07460`  ·  n_top_tier: `0.71704`  ·  corrupted: `0.99265`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.33864 |
| `explicit.stat_681332047@T2` | -1.25692 |
| `explicit.stat_1573130764@T2` | -1.04796 |
| `explicit.stat_681332047@T1` | -1.03029 |
| `explicit.stat_1573130764@T1` | -0.99264 |
| `explicit.stat_2463230181@T1` | 0.90171 |
| `explicit.stat_2194114101@T2` | -0.89005 |
| `explicit.stat_2321178454@T2` | -0.83667 |
| `explicit.stat_4067062424@T1` | -0.71936 |
| `explicit.stat_3714003708@T2` | -0.71756 |
| `explicit.stat_803737631@T1` | -0.70166 |
| `explicit.stat_4067062424@T2` | -0.65677 |

### armour.shield — n=6181, R²=-0.4054

intercept: `-13.5293`  ·  log_price: True  ·  ilvl: `0.18284`  ·  n_mods: `-0.17732`  ·  n_top_tier: `0.65230`  ·  corrupted: `-0.45654`  ·  n_sockets: `0.34986`  ·  quality: `0.04706`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.46960 |
| `explicit.stat_2901986750@T1` | -1.41812 |
| `explicit.stat_3033371881@T2` | -1.35481 |
| `explicit.stat_328541901@T1` | -1.31904 |
| `explicit.stat_1011760251@T1` | -1.30862 |
| `explicit.stat_4095671657@T1` | -1.27784 |
| `explicit.stat_4095671657@T2` | -1.17095 |
| `explicit.stat_328541901@T2` | -1.11439 |
| `explicit.stat_2481353198@T1` | -1.05348 |
| `explicit.stat_2901986750@T2` | -1.04997 |
| `explicit.stat_2339757871@T1` | -1.00529 |
| `explicit.stat_3321629045@T2` | -0.99596 |

### weapon.twomace — n=5627, R²=-0.4317

intercept: `-11.4036`  ·  log_price: True  ·  ilvl: `0.15553`  ·  n_mods: `-0.22708`  ·  n_top_tier: `0.41445`  ·  corrupted: `0.78950`  ·  n_sockets: `0.18272`  ·  quality: `0.06206`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -6.00446 |
| `desecrated.stat_1509134228@T1` | 2.86936 |
| `explicit.stat_1037193709@T1` | -1.56010 |
| `explicit.stat_3336890334@T1` | -1.28691 |
| `explicit.stat_1263695895@T2` | -1.26421 |
| `explicit.stat_9187492@T1` | -0.93380 |
| `explicit.stat_2694482655@T1` | 0.91970 |
| `explicit.stat_210067635@T1` | -0.86380 |
| `explicit.stat_1263695895@T1` | -0.80606 |
| `explicit.stat_1037193709@T2` | -0.55521 |
| `explicit.stat_518292764@T2` | -0.53518 |
| `explicit.stat_3695891184@T2` | -0.52086 |

## Coverage (listings per base)

- … **Sapphire** — 39375 listings (39310 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 38292 listings (38239 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 29349 listings (29317 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 13258 listings (13240 priced) [0.2–398916549611043.2 ex]
- … **Prismatic Ring** — 12299 listings (12273 priced) [0.2–398916549611043.2 ex]
- … **Solar Amulet** — 11960 listings (11934 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 11822 listings (11807 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 11078 listings (11051 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 11047 listings (11024 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 10461 listings (10448 priced) [0.3–398916549611043.2 ex]
- … **Sapphire Ring** — 9155 listings (9140 priced) [0.2–398916549611043.2 ex]
- … **Topaz Ring** — 8828 listings (8818 priced) [0.3–398916549611043.2 ex]
- … **Ruby Ring** — 8740 listings (8731 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7641 listings (7617 priced) [0.3–398916553600208.8 ex]
- … **Unset Ring** — 7562 listings (7540 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7527 listings (7519 priced) [0.3–398916549611043.2 ex]
- … **Jade Amulet** — 7464 listings (7448 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 7395 listings (7387 priced) [0.3–3985176410.3 ex]
- … **Pearl Ring** — 7315 listings (7306 priced) [0.2–398916549611043.2 ex]
- … **Plate Belt** — 7254 listings (7223 priced) [0.3–398916553600208.8 ex]
- … **Ancestral Tiara** — 7208 listings (7177 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 7151 listings (7139 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6841 listings (6837 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6763 listings (6748 priced) [0.3–398916549611043.2 ex]
- … **Heavy Belt** — 6411 listings (6397 priced) [0.3–398916553600208.8 ex]

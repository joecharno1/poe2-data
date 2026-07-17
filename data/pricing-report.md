# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-17T07:44:01+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **573366** (571784 priced in exalted)
- Distinct bases: 987 · distinct mods: 3204 · mod rows: 2714246
- Sold signals: **25399** sold · 324052 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-17T07:35:39+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×26.26** (median |log error| 3.268)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 80% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×76.10 · ±30% 4% · n=83299
- Premium segment (60ex+): skill **+0.11** · typical error ×363.98 · ±30% 0% · n=56345

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 11744 | ×54.77 | 22% | +0.03 | +0.05 |
| jewel | 11023 | ×10.80 | 4% | +0.06 | +0.10 |
| accessory.amulet | 10741 | ×50.06 | 20% | +0.03 | +0.04 |
| accessory.belt | 7986 | ×25.43 | 23% | +0.03 | +0.05 |
| armour.chest | 7772 | ×19.82 | 24% | +0.06 | +0.10 |
| armour.helmet | 7593 | ×29.52 | 22% | +0.05 | +0.07 |
| armour.boots | 7052 | ×35.02 | 22% | +0.07 | +0.10 |
| armour.gloves | 6889 | ×46.44 | 18% | +0.07 | +0.09 |
| other | 6539 | ×1.92 | 44% | +0.10 | +0.18 |
| weapon.wand | 4275 | ×51.31 | 19% | +0.07 | +0.08 |
| weapon.bow | 3366 | ×31.37 | 15% | +0.13 | +0.13 |
| weapon.crossbow | 3176 | ×36.83 | 18% | +0.09 | +0.12 |
| weapon.warstaff | 2019 | ×37.76 | 8% | +0.14 | +0.12 |
| weapon.staff | 1913 | ×52.51 | 7% | +0.12 | +0.12 |
| weapon.sceptre | 1865 | ×40.33 | 4% | +0.18 | +0.20 |
| weapon.spear | 1490 | ×43.77 | 13% | +0.08 | +0.09 |
| armour.focus | 1260 | ×22.68 | 6% | +0.15 | +0.16 |
| armour.quiver | 1204 | ×25.86 | 7% | +0.14 | +0.15 |
| flask.charm | 1050 | ×32.58 | 31% | +0.05 | +0.07 |
| armour.shield | 983 | ×20.29 | 7% | +0.04 | +0.05 |
| weapon.twomace | 896 | ×8.63 | 11% | +0.07 | +0.06 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=60192, R²=-0.9448

intercept: `-1.8383`  ·  log_price: True  ·  ilvl: `0.02584`  ·  n_mods: `0.74048`  ·  n_top_tier: `-0.22225`  ·  corrupted: `0.35115`  ·  quality: `0.22687`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.40341 |
| `explicit.stat_2301718443@T1` | 2.67200 |
| `explicit.stat_3374165039@T1` | -2.17053 |
| `explicit.stat_1805182458@T1` | -2.10143 |
| `explicit.stat_3485067555@T1` | 1.95578 |
| `explicit.stat_491450213@T1` | 1.60249 |
| `explicit.stat_3166958180@T1` | -1.52139 |
| `explicit.stat_686254215@T1` | -1.46974 |
| `explicit.stat_1697951953@T1` | -1.46337 |
| `explicit.stat_2523933828@T1` | -1.45243 |
| `explicit.stat_239367161@T1` | -1.39278 |
| `explicit.stat_3119612865@T1` | -1.37631 |

### other — n=55019, R²=-0.6546

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.34725`  ·  corrupted: `0.30622`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2974417149@T1` | 0.40982 |
| `explicit.stat_3291658075@T1` | 0.30475 |
| `explicit.stat_3299347043@T1` | -0.30372 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_2106365538@T1` | -0.13935 |
| `explicit.stat_1050105434@T1` | -0.11318 |
| `explicit.stat_2482852589@T1` | -0.10469 |
| `implicit.stat_2923486259` | -0.09700 |
| `pseudo.total_chaos_res` | 0.09700 |
| `explicit.stat_789117908@T1` | -0.06447 |

### accessory.ring — n=53662, R²=-2.0256

intercept: `3.5318`  ·  log_price: True  ·  ilvl: `-0.04368`  ·  n_mods: `-0.00002`  ·  n_top_tier: `1.01428`  ·  corrupted: `0.02322`  ·  n_sockets: `2.18756`  ·  quality: `0.07388`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -1.05101 |
| `explicit.stat_3299347043@T1` | -1.04936 |
| `explicit.stat_1573130764@T1` | -1.04542 |
| `explicit.stat_1368271171@T2` | -1.03593 |
| `explicit.stat_803737631@T1` | -1.03526 |
| `explicit.stat_2231156303@T2` | -1.03458 |
| `explicit.stat_4220027924@T2` | -1.03425 |
| `explicit.stat_3325883026@T1` | -1.03408 |
| `explicit.stat_2144192055@T1` | -1.03284 |
| `explicit.stat_1263695895@T2` | -1.03214 |
| `explicit.stat_3299347043@T2` | -1.03017 |
| `explicit.stat_4067062424@T2` | -1.02982 |

### accessory.amulet — n=49104, R²=-2.1559

intercept: `3.5912`  ·  log_price: True  ·  ilvl: `-0.04387`  ·  n_mods: `-0.02536`  ·  n_top_tier: `1.03358`  ·  corrupted: `0.07149`  ·  n_sockets: `-0.10688`  ·  quality: `-0.00087`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.23530 |
| `explicit.stat_587431675@T2` | -1.11949 |
| `explicit.stat_3299347043@T2` | -1.10507 |
| `explicit.stat_2974417149@T1` | -1.10386 |
| `explicit.stat_472520716@T2` | -1.09655 |
| `explicit.stat_803737631@T1` | -1.09012 |
| `explicit.stat_1050105434@T2` | -1.08562 |
| `explicit.stat_2866361420@T2` | -1.08031 |
| `explicit.stat_2974417149@T2` | -1.07753 |
| `explicit.stat_803737631@T2` | -1.07548 |
| `explicit.stat_2866361420@T1` | -1.06870 |
| `explicit.stat_1671376347@T2` | -1.06328 |

### accessory.belt — n=36726, R²=-1.8216

intercept: `2.6189`  ·  log_price: True  ·  ilvl: `-0.03151`  ·  n_mods: `-0.01600`  ·  n_top_tier: `1.03624`  ·  corrupted: `0.77015`  ·  n_sockets: `0.64295`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.06381 |
| `explicit.stat_2881298780@T1` | -1.06109 |
| `explicit.stat_3299347043@T2` | -1.05462 |
| `explicit.stat_4220027924@T2` | -1.05314 |
| `explicit.stat_809229260@T2` | -1.05075 |
| `explicit.stat_1389754388@T1` | -1.04987 |
| `explicit.stat_3325883026@T1` | -1.04669 |
| `explicit.stat_915769802@T1` | -1.04217 |
| `explicit.stat_51994685@T1` | -1.04067 |
| `explicit.stat_3372524247@T2` | -1.04021 |
| `explicit.stat_1671376347@T2` | -1.04007 |
| `explicit.stat_915769802@T2` | -1.03967 |

### armour.chest — n=36525, R²=-1.7588

intercept: `3.2820`  ·  log_price: True  ·  ilvl: `-0.04037`  ·  n_mods: `-0.01405`  ·  n_top_tier: `0.49868`  ·  corrupted: `0.04606`  ·  n_sockets: `0.02232`  ·  quality: `0.05990`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.57068 |
| `explicit.stat_3981240776@T1` | 0.98663 |
| `explicit.stat_986397080@T2` | -0.55327 |
| `explicit.stat_4080418644@T2` | -0.53506 |
| `explicit.stat_915769802@T2` | -0.52927 |
| `explicit.stat_1692879867@T1` | -0.52916 |
| `explicit.stat_4080418644@T1` | -0.52766 |
| `explicit.stat_986397080@T1` | -0.52644 |
| `explicit.stat_2451402625@T2` | -0.52285 |
| `explicit.stat_3372524247@T2` | -0.51932 |
| `explicit.stat_915769802@T1` | -0.51909 |
| `explicit.stat_4015621042@T1` | -0.51547 |

### armour.helmet — n=35428, R²=-1.8296

intercept: `3.3580`  ·  log_price: True  ·  ilvl: `-0.04198`  ·  n_mods: `-0.01684`  ·  n_top_tier: `0.34883`  ·  corrupted: `0.75907`  ·  n_sockets: `0.03244`  ·  quality: `0.05160`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.31933 |
| `crafted.stat_3917489142@T1` | 1.02427 |
| `explicit.stat_1263695895@T1` | -0.53420 |
| `explicit.stat_2162097452@T2` | -0.46178 |
| `explicit.stat_1263695895@T2` | -0.45836 |
| `explicit.stat_3917489142@T2` | -0.45732 |
| `explicit.stat_4052037485@T2` | -0.40180 |
| `explicit.stat_1999113824@T1` | -0.39641 |
| `explicit.stat_3917489142@T1` | -0.39164 |
| `explicit.stat_3321629045@T2` | -0.38088 |
| `explicit.stat_3484657501@T1` | -0.36809 |
| `explicit.stat_803737631@T1` | -0.36369 |

### armour.boots — n=33169, R²=-1.7999

intercept: `3.3230`  ·  log_price: True  ·  ilvl: `-0.04072`  ·  n_mods: `-0.01536`  ·  n_top_tier: `0.69808`  ·  corrupted: `-0.00111`  ·  n_sockets: `0.01926`  ·  quality: `0.04899`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.56324 |
| `explicit.stat_2250533757@T1` | 1.17542 |
| `explicit.stat_2339757871@T1` | -0.85277 |
| `explicit.stat_3299347043@T1` | -0.84136 |
| `explicit.stat_3917489142@T2` | -0.83574 |
| `explicit.stat_3917489142@T1` | -0.76539 |
| `explicit.stat_2160282525@T1` | -0.73402 |
| `explicit.stat_2923486259@T2` | -0.72523 |
| `explicit.stat_3484657501@T2` | -0.72468 |
| `explicit.stat_1671376347@T2` | -0.72352 |
| `explicit.stat_3299347043@T2` | -0.71991 |
| `explicit.stat_99927264@T1` | -0.70380 |

### armour.gloves — n=32230, R²=-1.8361

intercept: `3.6798`  ·  log_price: True  ·  ilvl: `-0.04613`  ·  n_mods: `-0.01235`  ·  n_top_tier: `0.59938`  ·  corrupted: `0.03379`  ·  n_sockets: `0.04234`  ·  quality: `0.04376`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 1.04218 |
| `explicit.stat_9187492@T2` | -0.85914 |
| `explicit.stat_9187492@T1` | 0.83085 |
| `explicit.stat_1671376347@T1` | 0.81886 |
| `explicit.stat_2923486259@T1` | -0.80654 |
| `explicit.stat_3484657501@T2` | -0.71063 |
| `explicit.stat_3321629045@T2` | -0.70788 |
| `explicit.stat_803737631@T2` | -0.66675 |
| `explicit.stat_4052037485@T1` | -0.66582 |
| `explicit.stat_3484657501@T1` | -0.66231 |
| `explicit.stat_124859000@T2` | -0.65018 |
| `explicit.stat_1999113824@T2` | -0.64094 |

### weapon.wand — n=20047, R²=-2.2476

intercept: `3.6069`  ·  log_price: True  ·  ilvl: `-0.04453`  ·  n_mods: `-0.02872`  ·  n_top_tier: `0.46080`  ·  corrupted: `0.04477`  ·  n_sockets: `0.05948`  ·  quality: `0.00874`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.81971 |
| `explicit.stat_2254480358@T1` | 2.43642 |
| `explicit.stat_4226189338@T1` | 2.32803 |
| `rune.stat_124131830` | -2.32272 |
| `explicit.stat_124131830@T1` | 1.84102 |
| `explicit.stat_591105508@T1` | 1.83160 |
| `explicit.stat_736967255@T2` | 1.72395 |
| `crafted.stat_124131830` | 1.28840 |
| `explicit.stat_1600707273@T1` | 1.11545 |
| `explicit.stat_4226189338@T2` | 0.87769 |
| `explicit.stat_1263695895@T1` | -0.62689 |
| `explicit.stat_1263695895@T2` | -0.62431 |

### weapon.bow — n=16103, R²=-1.9159

intercept: `3.6352`  ·  log_price: True  ·  ilvl: `-0.04301`  ·  n_mods: `-0.06972`  ·  n_top_tier: `0.59244`  ·  corrupted: `0.19881`  ·  n_sockets: `0.03991`  ·  quality: `0.02864`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.46051 |
| `desecrated.stat_210067635@T1` | -1.61748 |
| `crafted.stat_3035140377` | 1.45541 |
| `explicit.stat_1202301673@T1` | 1.41280 |
| `explicit.stat_2463230181@T1` | -1.09193 |
| `explicit.stat_2463230181@T2` | -1.03834 |
| `explicit.stat_3336890334@T1` | 1.00095 |
| `explicit.stat_1263695895@T1` | -0.98823 |
| `explicit.stat_1263695895@T2` | -0.93852 |
| `explicit.stat_518292764@T2` | -0.86006 |
| `explicit.stat_3695891184@T2` | -0.76387 |
| `explicit.stat_3695891184@T1` | -0.73593 |

### flask.charm — n=15228, R²=-0.572

intercept: `0.0645`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `2.30468`  ·  corrupted: `1.89601`  ·  quality: `0.00008`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.57285 |
| `explicit.stat_1056492907` | 2.94547 |
| `explicit.stat_828533480@T2` | -2.30470 |
| `explicit.stat_1873752457@T2` | -2.30468 |
| `explicit.stat_388617051@T2` | -2.30467 |
| `explicit.stat_2676834156@T2` | -2.30467 |
| `explicit.stat_1120862500@T2` | -2.30466 |
| `explicit.stat_3196823591@T2` | -2.30466 |
| `explicit.stat_1873752457@T1` | -2.30466 |
| `explicit.stat_2365392475@T2` | -2.30465 |
| `explicit.stat_828533480@T1` | -2.30459 |
| `explicit.stat_1366840608@T2` | -2.30117 |

### weapon.crossbow — n=15076, R²=-1.9508

intercept: `3.7801`  ·  log_price: True  ·  ilvl: `-0.04622`  ·  n_mods: `-0.03902`  ·  n_top_tier: `0.66376`  ·  corrupted: `0.02145`  ·  n_sockets: `0.03232`  ·  quality: `0.02256`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.83573 |
| `explicit.stat_2250681686@T2` | -1.60320 |
| `explicit.stat_1202301673@T1` | 1.49182 |
| `explicit.stat_1980802737` | 1.20134 |
| `explicit.stat_2250681686` | 1.04847 |
| `explicit.stat_518292764@T1` | 0.81849 |
| `crafted.stat_3035140377` | 0.78934 |
| `explicit.stat_2694482655@T1` | -0.77408 |
| `explicit.stat_1509134228@T2` | -0.76580 |
| `explicit.stat_1940865751@T1` | -0.75835 |
| `explicit.stat_1263695895@T2` | -0.74524 |
| `explicit.stat_1940865751@T2` | -0.73947 |

### weapon.warstaff — n=9677, R²=-0.3754

intercept: `-9.5026`  ·  log_price: True  ·  ilvl: `0.13101`  ·  n_mods: `-0.21602`  ·  n_top_tier: `0.32569`  ·  corrupted: `0.20359`  ·  n_sockets: `0.18948`  ·  quality: `0.06321`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 1.59233 |
| `desecrated.stat_2527686725@T1` | 1.59233 |
| `crafted.stat_210067635@T2` | 1.18665 |
| `explicit.stat_1037193709@T1` | 1.07563 |
| `rune.stat_243313994` | 0.86219 |
| `explicit.stat_328541901@T1` | -0.79882 |
| `explicit.stat_328541901@T2` | -0.78175 |
| `desecrated.stat_9187492` | 0.73782 |
| `explicit.stat_9187492@T1` | 0.69945 |
| `explicit.stat_1509134228@T1` | 0.65640 |
| `explicit.stat_748522257@T2` | 0.53520 |
| `explicit.stat_2694482655@T2` | 0.49153 |

### weapon.staff — n=9085, R²=-0.397

intercept: `-14.3391`  ·  log_price: True  ·  ilvl: `0.18710`  ·  n_mods: `-0.15578`  ·  n_top_tier: `0.45836`  ·  corrupted: `0.42708`  ·  n_sockets: `0.27284`  ·  quality: `0.04199`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.94275 |
| `explicit.stat_4226189338@T1` | 1.76053 |
| `explicit.stat_591105508@T1` | 1.52795 |
| `explicit.stat_293638271@T2` | -1.13590 |
| `explicit.stat_124131830@T1` | 0.98043 |
| `explicit.stat_2254480358@T2` | 0.88291 |
| `explicit.stat_591105508@T2` | 0.74799 |
| `explicit.stat_2254480358@T1` | 0.74576 |
| `explicit.stat_4226189338@T2` | 0.73559 |
| `explicit.stat_2505884597@T2` | -0.73185 |
| `explicit.stat_3962278098@T2` | 0.72591 |
| `explicit.stat_124131830@T2` | 0.72512 |

### weapon.sceptre — n=8964, R²=-0.3535

intercept: `-18.5393`  ·  log_price: True  ·  ilvl: `0.23728`  ·  n_mods: `-0.08389`  ·  n_top_tier: `0.27481`  ·  corrupted: `0.34100`  ·  n_sockets: `0.28385`  ·  quality: `0.04234`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.71718 |
| `explicit.stat_2162097452@T2` | 1.57834 |
| `explicit.stat_1250712710@T2` | 1.40896 |
| `explicit.stat_3057012405@T1` | 1.07864 |
| `explicit.stat_101878827@T1` | 0.71981 |
| `explicit.stat_2347036682@T1` | 0.69449 |
| `explicit.stat_1263695895@T2` | -0.67880 |
| `explicit.stat_849987426@T1` | 0.65112 |
| `explicit.stat_2347036682@T2` | -0.57533 |
| `explicit.stat_1574590649@T1` | -0.56694 |
| `explicit.stat_1263695895@T1` | -0.52488 |
| `explicit.stat_289128254@T2` | -0.44728 |

### weapon.spear — n=7330, R²=-0.432

intercept: `-10.9742`  ·  log_price: True  ·  ilvl: `0.15549`  ·  n_mods: `-0.15689`  ·  n_top_tier: `0.82417`  ·  corrupted: `-0.32213`  ·  n_sockets: `0.26793`  ·  quality: `0.05932`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.94081 |
| `explicit.stat_1202301673@T1` | 1.51894 |
| `explicit.stat_1509134228@T1` | 1.36354 |
| `crafted.stat_3035140377` | 1.10473 |
| `explicit.stat_1037193709@T1` | -1.05415 |
| `explicit.stat_4080418644@T2` | -1.02747 |
| `explicit.stat_9187492@T1` | 0.94373 |
| `explicit.stat_3261801346@T1` | -0.91878 |
| `explicit.stat_9187492@T2` | -0.91168 |
| `explicit.stat_691932474@T1` | -0.81260 |
| `explicit.stat_691932474@T2` | -0.80005 |
| `explicit.stat_3261801346@T2` | -0.79565 |

### armour.focus — n=6020, R²=-0.3729

intercept: `-12.2685`  ·  log_price: True  ·  ilvl: `0.16202`  ·  n_mods: `-0.16191`  ·  n_top_tier: `0.79621`  ·  corrupted: `0.44831`  ·  n_sockets: `0.41340`  ·  quality: `0.06900`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 7.84398 |
| `explicit.stat_4220027924@T2` | -1.32256 |
| `explicit.stat_3962278098@T1` | -1.24435 |
| `explicit.stat_2231156303@T2` | -0.93241 |
| `explicit.stat_3291658075@T1` | -0.91610 |
| `explicit.stat_2891184298@T2` | -0.90364 |
| `explicit.stat_2339757871@T2` | -0.87483 |
| `explicit.stat_737908626@T2` | -0.84669 |
| `explicit.stat_2974417149@T1` | -0.81114 |
| `explicit.stat_4052037485@T2` | -0.80885 |
| `explicit.stat_2231156303@T1` | -0.76298 |
| `explicit.stat_2923486259@T1` | -0.74174 |

### armour.quiver — n=5647, R²=-0.3171

intercept: `-13.9254`  ·  log_price: True  ·  ilvl: `0.17192`  ·  n_mods: `-0.14564`  ·  n_top_tier: `0.86360`  ·  corrupted: `0.83965`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.73899 |
| `explicit.stat_2463230181@T1` | 3.28076 |
| `explicit.stat_2463230181@T2` | 1.62026 |
| `explicit.stat_681332047@T2` | -1.33936 |
| `explicit.stat_1573130764@T1` | -1.22075 |
| `explicit.stat_2321178454@T2` | -1.14698 |
| `explicit.stat_803737631@T2` | -1.07967 |
| `explicit.stat_1573130764@T2` | -1.00808 |
| `explicit.stat_4067062424@T1` | -1.00362 |
| `explicit.stat_2321178454@T1` | -0.93799 |
| `explicit.stat_803737631@T1` | -0.91200 |
| `explicit.stat_3261801346@T1` | -0.81408 |

### armour.shield — n=4896, R²=-0.4913

intercept: `-10.3154`  ·  log_price: True  ·  ilvl: `0.13918`  ·  n_mods: `-0.12364`  ·  n_top_tier: `0.67782`  ·  corrupted: `-0.31010`  ·  n_sockets: `0.26227`  ·  quality: `0.06749`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.38272 |
| `explicit.stat_2339757871@T1` | -1.30950 |
| `explicit.stat_328541901@T1` | -1.18293 |
| `explicit.stat_328541901@T2` | -1.12553 |
| `explicit.stat_3321629045@T2` | -1.08161 |
| `explicit.stat_3484657501@T2` | -1.07451 |
| `explicit.stat_3033371881@T2` | -1.06192 |
| `explicit.stat_2481353198@T2` | -1.02770 |
| `explicit.stat_2901986750@T1` | -1.00395 |
| `explicit.stat_4095671657@T1` | -0.95280 |
| `explicit.stat_1671376347@T1` | -0.90317 |
| `explicit.stat_2923486259@T1` | -0.88510 |

### weapon.twomace — n=4498, R²=-0.4909

intercept: `-9.6448`  ·  log_price: True  ·  ilvl: `0.13390`  ·  n_mods: `-0.19096`  ·  n_top_tier: `0.42018`  ·  corrupted: `-0.07126`  ·  n_sockets: `0.15111`  ·  quality: `0.05525`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.86577 |
| `desecrated.stat_1509134228@T1` | 1.96786 |
| `explicit.stat_1037193709@T1` | -1.55406 |
| `explicit.stat_387439868@T2` | -0.97725 |
| `crafted.stat_3035140377` | 0.92057 |
| `explicit.stat_9187492@T1` | -0.80578 |
| `explicit.stat_1037193709@T2` | -0.79139 |
| `explicit.stat_691932474@T1` | -0.75416 |
| `explicit.stat_3336890334@T1` | -0.67998 |
| `explicit.stat_1263695895@T2` | -0.65767 |
| `explicit.stat_387439868@T1` | -0.48794 |
| `explicit.stat_669069897@T2` | -0.48666 |

## Coverage (listings per base)

- … **Sapphire** — 27937 listings (27889 priced) [0.3–885594757.8 ex]
- … **Emerald** — 27368 listings (27329 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 20933 listings (20909 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10575 listings (10560 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 9152 listings (9134 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8851 listings (8832 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8742 listings (8734 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8304 listings (8288 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8164 listings (8146 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8083 listings (8072 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6788 listings (6778 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6522 listings (6516 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6488 listings (6482 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6428 listings (6409 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 5747 listings (5740 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 5726 listings (5703 priced) [0.3–398912568423.8 ex]
- … **Jade Amulet** — 5622 listings (5611 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 5612 listings (5595 priced) [0.2–24532814.5 ex]
- … **Amber Amulet** — 5595 listings (5588 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5536 listings (5515 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5436 listings (5427 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5322 listings (5315 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5121 listings (5119 priced) [0.3–3985176410.3 ex]
- … **Heavy Belt** — 5093 listings (5085 priced) [0.3–398912568423.8 ex]
- … **Lunar Amulet** — 5090 listings (5078 priced) [0.3–91750808.2 ex]

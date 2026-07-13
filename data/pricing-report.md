# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-13T01:52:33+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **401713** (400981 priced in exalted)
- Distinct bases: 969 · distinct mods: 2955 · mod rows: 1909248
- Sold signals: **28130** sold · 215170 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-13T01:43:37+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.59** (median |log error| 3.1174)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.09** · typical error ×56.62 · ±30% 6% · n=58404
- Premium segment (60ex+): skill **+0.10** · typical error ×268.35 · ±30% 0% · n=37430

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 7851 | ×53.19 | 21% | +0.03 | +0.06 |
| accessory.amulet | 7318 | ×49.09 | 20% | +0.02 | +0.02 |
| jewel | 7021 | ×7.89 | 8% | +0.01 | +0.04 |
| accessory.belt | 5722 | ×10.00 | 16% | +0.02 | +0.02 |
| armour.chest | 5612 | ×17.78 | 8% | +0.09 | +0.12 |
| armour.helmet | 5541 | ×19.62 | 6% | +0.04 | +0.07 |
| armour.boots | 5082 | ×21.06 | 16% | +0.07 | +0.10 |
| armour.gloves | 5070 | ×33.00 | 12% | +0.07 | +0.08 |
| other | 4642 | ×3.98 | 41% | +0.08 | +0.15 |
| weapon.wand | 3328 | ×45.28 | 20% | +0.06 | +0.06 |
| weapon.bow | 2689 | ×27.33 | 19% | +0.08 | +0.08 |
| weapon.crossbow | 2509 | ×22.11 | 21% | +0.10 | +0.10 |
| weapon.warstaff | 1427 | ×81.70 | 16% | +0.08 | +0.08 |
| weapon.sceptre | 1316 | ×75.76 | 12% | +0.07 | +0.08 |
| weapon.staff | 1284 | ×52.59 | 15% | +0.06 | +0.06 |
| weapon.spear | 1085 | ×40.30 | 18% | +0.06 | +0.06 |
| armour.focus | 874 | ×44.23 | 15% | +0.12 | +0.16 |
| armour.quiver | 861 | ×37.20 | 15% | +0.04 | +0.09 |
| armour.shield | 732 | ×29.24 | 14% | +0.04 | +0.09 |
| weapon.twomace | 646 | ×23.99 | 15% | +0.06 | +0.08 |
| flask.charm | 599 | ×5.00 | 40% | +0.01 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=39870, R²=-0.6241

intercept: `1.6076`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `0.00768`  ·  n_top_tier: `0.33942`  ·  corrupted: `0.45200`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.56942 |
| `explicit.stat_2974417149@T1` | 0.50679 |
| `explicit.stat_2891184298@T1` | 0.34682 |
| `explicit.stat_3917489142@T1` | 0.33502 |
| `explicit.stat_789117908@T1` | -0.33239 |
| `explicit.stat_2106365538@T1` | 0.31865 |
| `explicit.stat_1050105434@T1` | -0.30598 |
| `implicit.stat_1379411836` | -0.23102 |
| `implicit.stat_4041853756` | 0.22950 |
| `implicit.stat_3879011313` | 0.22949 |
| `explicit.stat_101878827@T1` | -0.20107 |
| `explicit.stat_1589917703@T1` | -0.19083 |

### jewel — n=37826, R²=-0.7

intercept: `-1.3774`  ·  log_price: True  ·  ilvl: `0.03539`  ·  n_mods: `0.31248`  ·  n_top_tier: `-0.10029`  ·  corrupted: `0.16894`  ·  quality: `0.23279`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -5.00081 |
| `explicit.stat_3780644166@T1` | -3.49164 |
| `explicit.stat_3741323227@T1` | -3.04098 |
| `explicit.stat_1569101201@T1` | 2.50595 |
| `explicit.stat_627767961@T1` | -2.47467 |
| `explicit.stat_234296660@T1` | -2.33994 |
| `explicit.stat_3485067555@T1` | 2.16412 |
| `explicit.stat_21071013@T1` | 2.00331 |
| `explicit.stat_1315743832@T1` | 1.90308 |
| `explicit.stat_3174700878@T1` | 1.78630 |
| `explicit.stat_1423639565@T1` | -1.71254 |
| `explicit.stat_2527686725@T1` | 1.67946 |

### accessory.ring — n=35752, R²=-1.9356

intercept: `4.1537`  ·  log_price: True  ·  ilvl: `-0.05089`  ·  n_mods: `0.00437`  ·  n_top_tier: `0.02712`  ·  corrupted: `0.77107`  ·  n_sockets: `2.05501`  ·  quality: `0.05518`

| stat_id | coef |
|---|---|
| `explicit.stat_1671376347@T1` | 1.15963 |
| `explicit.stat_3032590688@T1` | 0.24052 |
| `implicit.stat_2748665614` | -0.21199 |
| `explicit.stat_707457662@T1` | 0.20493 |
| `explicit.stat_707457662@T2` | 0.20015 |
| `explicit.stat_1967040409` | 0.15420 |
| `explicit.stat_1263695895@T1` | -0.09969 |
| `implicit.stat_2901986750` | -0.09425 |
| `explicit.stat_2901986750` | -0.09140 |
| `explicit.stat_3325883026@T1` | -0.07957 |
| `explicit.stat_1573130764@T2` | 0.07636 |
| `explicit.stat_2653231923` | 0.07573 |

### accessory.amulet — n=33466, R²=-2.1178

intercept: `4.0506`  ·  log_price: True  ·  ilvl: `-0.04901`  ·  n_mods: `-0.02461`  ·  n_top_tier: `0.68421`  ·  corrupted: `0.07886`  ·  n_sockets: `-0.10185`  ·  quality: `-0.00027`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T2` | -1.19773 |
| `explicit.stat_124131830` | 1.05075 |
| `explicit.stat_983749596@T1` | -0.98064 |
| `explicit.stat_983749596@T2` | -0.89919 |
| `explicit.stat_3981240776@T2` | 0.87081 |
| `explicit.stat_2748665614@T2` | -0.80268 |
| `explicit.stat_3299347043@T2` | -0.79678 |
| `explicit.stat_472520716@T1` | -0.77898 |
| `explicit.stat_3299347043@T1` | -0.77475 |
| `explicit.stat_2748665614@T1` | -0.76846 |
| `explicit.stat_3917489142@T2` | -0.74979 |
| `explicit.stat_472520716@T2` | -0.74638 |

### accessory.belt — n=26431, R²=-0.1908

intercept: `2.4536`  ·  log_price: True  ·  ilvl: `-0.00160`  ·  n_mods: `-0.01947`  ·  n_top_tier: `0.05478`  ·  corrupted: `0.03548`  ·  n_sockets: `-0.66384`

| stat_id | coef |
|---|---|
| `explicit.stat_2639966148` | 0.08680 |
| `explicit.stat_1389754388@T1` | -0.07757 |
| `explicit.stat_3325883026@T1` | -0.07344 |
| `explicit.stat_51994685@T1` | -0.07201 |
| `explicit.stat_2881298780@T1` | -0.06721 |
| `explicit.stat_1389754388@T2` | -0.06314 |
| `explicit.stat_2923486259@T1` | -0.06276 |
| `explicit.stat_2923486259@T2` | -0.06219 |
| `explicit.stat_1050105434@T1` | -0.05936 |
| `explicit.stat_1671376347@T2` | -0.05933 |
| `explicit.stat_644456512@T1` | -0.05931 |
| `explicit.stat_4220027924@T2` | -0.05883 |

### armour.chest — n=26127, R²=-1.1126

intercept: `4.3781`  ·  log_price: True  ·  ilvl: `-0.05262`  ·  n_mods: `-0.07479`  ·  n_top_tier: `0.48452`  ·  corrupted: `0.14581`  ·  n_sockets: `0.08056`  ·  quality: `0.02927`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.23597 |
| `explicit.stat_3981240776@T1` | 0.84727 |
| `explicit.stat_4080418644@T1` | -0.70681 |
| `explicit.stat_915769802@T1` | -0.66850 |
| `explicit.stat_4015621042@T2` | -0.66321 |
| `explicit.stat_4015621042@T1` | -0.65860 |
| `explicit.stat_3484657501@T1` | -0.65331 |
| `explicit.stat_3261801346@T2` | -0.63407 |
| `explicit.stat_3321629045@T1` | -0.61874 |
| `explicit.stat_2451402625@T2` | -0.59298 |
| `explicit.stat_986397080@T2` | -0.59115 |
| `explicit.stat_124859000@T2` | -0.57985 |

### armour.helmet — n=25524, R²=-0.959

intercept: `4.1912`  ·  log_price: True  ·  ilvl: `-0.05177`  ·  n_mods: `-0.09140`  ·  n_top_tier: `0.47713`  ·  corrupted: `0.67650`  ·  n_sockets: `0.07090`  ·  quality: `0.04023`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 5.37335 |
| `explicit.stat_2339757871@T1` | -2.31070 |
| `explicit.stat_53045048@T2` | -0.94359 |
| `explicit.stat_53045048@T1` | -0.92151 |
| `explicit.stat_3362812763@T1` | -0.91492 |
| `explicit.stat_1263695895@T1` | -0.90122 |
| `explicit.stat_587431675@T2` | -0.73438 |
| `explicit.stat_1263695895@T2` | -0.69135 |
| `explicit.stat_2162097452@T2` | -0.68793 |
| `explicit.stat_328541901@T2` | -0.67156 |
| `explicit.stat_1999113824@T1` | -0.65779 |
| `explicit.stat_1062208444@T2` | -0.63534 |

### armour.boots — n=23975, R²=-1.4634

intercept: `4.0371`  ·  log_price: True  ·  ilvl: `-0.04924`  ·  n_mods: `-0.02774`  ·  n_top_tier: `0.48958`  ·  corrupted: `0.22942`  ·  n_sockets: `0.02251`  ·  quality: `0.02324`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | -2.46845 |
| `explicit.stat_2250533757@T1` | 1.69135 |
| `desecrated.stat_2250533757@T2` | -0.84729 |
| `explicit.stat_2923486259@T2` | -0.72426 |
| `explicit.stat_2339757871@T1` | -0.65665 |
| `explicit.stat_53045048@T1` | -0.64582 |
| `explicit.stat_3917489142@T2` | -0.62824 |
| `explicit.stat_4220027924@T1` | 0.60302 |
| `explicit.stat_2160282525@T1` | -0.57963 |
| `explicit.stat_4052037485@T2` | -0.57448 |
| `explicit.stat_1062208444@T2` | -0.56569 |
| `explicit.stat_2160282525@T2` | -0.54897 |

### armour.gloves — n=23360, R²=-1.455

intercept: `4.1349`  ·  log_price: True  ·  ilvl: `-0.05421`  ·  n_mods: `-0.04381`  ·  n_top_tier: `0.47147`  ·  corrupted: `0.25790`  ·  n_sockets: `0.13453`  ·  quality: `0.03133`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T2` | -0.99201 |
| `explicit.stat_9187492@T1` | 0.79022 |
| `explicit.stat_803737631@T2` | -0.76449 |
| `explicit.stat_3484657501@T1` | -0.74126 |
| `explicit.stat_3032590688@T1` | -0.71947 |
| `explicit.stat_2339757871@T1` | 0.70218 |
| `explicit.stat_803737631@T1` | -0.69653 |
| `explicit.stat_9187492@T2` | -0.69307 |
| `explicit.stat_681332047@T2` | -0.68694 |
| `explicit.stat_3321629045@T1` | -0.66841 |
| `explicit.stat_3917489142@T2` | -0.64254 |
| `rune.stat_201332984` | 0.62583 |

### weapon.wand — n=15507, R²=-2.2021

intercept: `3.8250`  ·  log_price: True  ·  ilvl: `-0.04740`  ·  n_mods: `-0.01565`  ·  n_top_tier: `0.19974`  ·  corrupted: `-0.02061`  ·  n_sockets: `0.03979`  ·  quality: `0.00386`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 3.64037 |
| `rune.stat_124131830` | -3.10064 |
| `explicit.stat_4226189338@T1` | 2.94429 |
| `explicit.stat_1545858329@T1` | 2.18551 |
| `explicit.stat_591105508@T1` | 2.15574 |
| `explicit.stat_1600707273@T1` | 2.04444 |
| `explicit.stat_736967255@T2` | 1.62423 |
| `crafted.stat_124131830` | 1.13372 |
| `explicit.stat_124131830@T1` | 0.72804 |
| `explicit.stat_1600707273@T2` | 0.56794 |
| `explicit.stat_2974417149@T1` | 0.56506 |
| `explicit.stat_3962278098@T2` | -0.23936 |

### weapon.bow — n=12638, R²=-2.0399

intercept: `3.4057`  ·  log_price: True  ·  ilvl: `-0.04178`  ·  n_mods: `-0.01935`  ·  n_top_tier: `0.86507`  ·  corrupted: `-0.02053`  ·  n_sockets: `-0.00310`  ·  quality: `0.03018`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 4.12739 |
| `desecrated.stat_210067635@T1` | -3.31692 |
| `rune.stat_3885405204` | -2.22948 |
| `crafted.stat_3035140377` | 1.59431 |
| `explicit.stat_1202301673@T1` | 1.30385 |
| `explicit.stat_55876295@T1` | -0.92450 |
| `explicit.stat_669069897@T1` | -0.90176 |
| `explicit.stat_669069897@T2` | -0.89696 |
| `explicit.stat_3336890334@T2` | -0.89411 |
| `explicit.stat_3695891184@T1` | -0.89240 |
| `explicit.stat_2694482655@T1` | -0.89218 |
| `explicit.stat_1037193709@T2` | -0.88989 |

### weapon.crossbow — n=11914, R²=-1.9161

intercept: `3.7174`  ·  log_price: True  ·  ilvl: `-0.04591`  ·  n_mods: `-0.00754`  ·  n_top_tier: `0.70938`  ·  corrupted: `-0.03542`  ·  n_sockets: `0.01921`  ·  quality: `0.00104`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -1.96524 |
| `explicit.stat_1980802737@T2` | -1.94768 |
| `explicit.stat_1202301673@T1` | 1.46233 |
| `explicit.stat_709508406@T1` | 1.45610 |
| `explicit.stat_2250681686` | 1.28299 |
| `explicit.stat_1980802737` | 1.19944 |
| `crafted.stat_3035140377` | 0.84753 |
| `explicit.stat_1263695895@T2` | -0.84511 |
| `explicit.stat_1202301673@T2` | -0.82052 |
| `explicit.stat_1263695895@T1` | -0.79708 |
| `rune.stat_669069897` | -0.76403 |
| `explicit.stat_669069897@T1` | -0.74158 |

### flask.charm — n=9444, R²=-0.4463

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.01257`  ·  corrupted: `0.77499`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.01046 |
| `explicit.stat_1056492907` | 3.40117 |
| `explicit.stat_2676834156@T1` | 1.59804 |
| `explicit.stat_2541588185@T1` | 0.19813 |
| `explicit.stat_2678930256` | 0.03219 |
| `explicit.stat_3138344128` | 0.02047 |
| `explicit.stat_828533480@T2` | -0.01257 |
| `explicit.stat_2676834156@T2` | -0.01257 |
| `explicit.stat_1366840608@T2` | -0.01257 |
| `explicit.stat_1873752457@T2` | -0.01257 |
| `explicit.stat_388617051@T2` | -0.01256 |
| `explicit.stat_1120862500@T2` | -0.01256 |

### weapon.warstaff — n=6659, R²=-0.6117

intercept: `-0.3169`  ·  log_price: True  ·  ilvl: `0.00435`  ·  n_mods: `-0.01160`  ·  n_top_tier: `0.24398`  ·  corrupted: `0.06102`  ·  n_sockets: `0.00825`  ·  quality: `0.06417`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.44938 |
| `explicit.stat_9187492@T1` | 1.11761 |
| `rune.stat_731403740` | 0.97257 |
| `explicit.stat_1509134228@T2` | 0.80870 |
| `desecrated.stat_9187492` | 0.54131 |
| `crafted.stat_3035140377` | 0.53436 |
| `rune.stat_1712188793` | -0.43774 |
| `crafted.stat_210067635@T2` | -0.34046 |
| `desecrated.stat_518292764` | 0.31614 |
| `explicit.stat_2694482655@T1` | 0.28150 |
| `explicit.stat_328541901@T2` | -0.26760 |
| `explicit.stat_1509134228@T1` | -0.26462 |

### weapon.sceptre — n=6206, R²=-0.5493

intercept: `-7.4711`  ·  log_price: True  ·  ilvl: `0.09366`  ·  n_mods: `-0.01366`  ·  n_top_tier: `0.09730`  ·  corrupted: `0.24433`  ·  n_sockets: `0.15539`  ·  quality: `0.10269`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.86603 |
| `explicit.stat_2162097452@T2` | 1.39277 |
| `explicit.stat_3057012405@T1` | 0.66947 |
| `explicit.stat_1798257884@T2` | 0.66729 |
| `explicit.stat_4080418644@T1` | -0.66054 |
| `explicit.stat_4080418644@T2` | -0.51300 |
| `explicit.stat_2347036682@T1` | 0.39809 |
| `explicit.stat_3984865854@T2` | 0.37331 |
| `explicit.stat_328541901@T2` | 0.36696 |
| `explicit.stat_1250712710@T1` | 0.35157 |
| `explicit.stat_101878827@T2` | 0.34460 |
| `explicit.stat_1263695895@T2` | -0.33560 |

### weapon.staff — n=6115, R²=-0.6657

intercept: `-0.4449`  ·  log_price: True  ·  ilvl: `0.00556`  ·  n_mods: `-0.00057`  ·  n_top_tier: `0.29946`  ·  corrupted: `0.05196`  ·  n_sockets: `0.02336`  ·  quality: `0.03749`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 3.36156 |
| `explicit.stat_4226189338@T1` | 2.14431 |
| `explicit.stat_1600707273@T1` | 2.01273 |
| `explicit.stat_2254480358@T1` | 1.78950 |
| `explicit.stat_1545858329@T1` | 1.77333 |
| `explicit.stat_2254480358@T2` | 1.33418 |
| `explicit.stat_2231156303@T2` | 1.19442 |
| `explicit.stat_124131830@T1` | 1.19047 |
| `explicit.stat_4226189338@T2` | 1.17913 |
| `explicit.stat_3291658075@T2` | 0.61573 |
| `crafted.stat_124131830` | 0.48703 |
| `explicit.stat_3962278098@T2` | 0.40061 |

### weapon.spear — n=5205, R²=-0.6906

intercept: `-0.1306`  ·  log_price: True  ·  ilvl: `0.00176`  ·  n_mods: `-0.00150`  ·  n_top_tier: `0.27558`  ·  corrupted: `-0.00750`  ·  n_sockets: `0.00495`  ·  quality: `0.09772`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.14784 |
| `explicit.stat_9187492@T1` | 1.84880 |
| `crafted.stat_210067635@T2` | 1.58875 |
| `crafted.stat_3035140377` | 1.29128 |
| `crafted.stat_518292764` | 0.69217 |
| `explicit.stat_210067635@T1` | 0.45478 |
| `explicit.stat_3336890334@T1` | 0.34077 |
| `explicit.stat_1263695895@T1` | -0.29058 |
| `explicit.stat_1263695895@T2` | -0.29026 |
| `explicit.stat_55876295@T1` | -0.28088 |
| `explicit.stat_691932474@T1` | -0.27820 |
| `explicit.stat_4080418644@T2` | -0.27693 |

### armour.focus — n=4269, R²=-0.5348

intercept: `-6.1869`  ·  log_price: True  ·  ilvl: `0.07638`  ·  n_mods: `-0.01826`  ·  n_top_tier: `0.82861`  ·  corrupted: `0.47464`  ·  n_sockets: `0.18310`  ·  quality: `0.07272`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 7.72040 |
| `crafted.stat_737908626@T2` | -3.37199 |
| `explicit.stat_1671376347@T1` | 1.04358 |
| `explicit.stat_4220027924@T2` | -1.01580 |
| `explicit.stat_4220027924@T1` | -1.01575 |
| `explicit.stat_124131830@T2` | -1.00080 |
| `explicit.stat_736967255@T2` | -0.96209 |
| `explicit.stat_2891184298@T2` | -0.94880 |
| `explicit.stat_3962278098@T1` | -0.92714 |
| `explicit.stat_3962278098@T2` | -0.89957 |
| `explicit.stat_2923486259@T1` | -0.89414 |
| `explicit.stat_2974417149@T2` | -0.88992 |

### armour.quiver — n=3995, R²=-0.5614

intercept: `-4.4340`  ·  log_price: True  ·  ilvl: `0.05204`  ·  n_mods: `0.00737`  ·  n_top_tier: `0.99608`  ·  corrupted: `0.93317`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 9.34197 |
| `explicit.stat_2194114101@T2` | -1.18320 |
| `explicit.stat_681332047@T2` | -1.17027 |
| `explicit.stat_2321178454@T2` | -1.15139 |
| `explicit.stat_3261801346@T1` | -1.06698 |
| `explicit.stat_1573130764@T1` | -1.05885 |
| `explicit.stat_1368271171@T2` | -1.04640 |
| `explicit.stat_1573130764@T2` | -1.02186 |
| `explicit.stat_3714003708@T2` | -0.99624 |
| `explicit.stat_2321178454@T1` | -0.99040 |
| `explicit.stat_1241625305@T2` | -0.98859 |
| `explicit.stat_3261801346@T2` | -0.96618 |

### armour.shield — n=3484, R²=-0.6346

intercept: `-3.1910`  ·  log_price: True  ·  ilvl: `0.03989`  ·  n_mods: `-0.00420`  ·  n_top_tier: `0.51414`  ·  corrupted: `0.72041`  ·  n_sockets: `0.00281`  ·  quality: `0.04403`

| stat_id | coef |
|---|---|
| `explicit.stat_328541901@T1` | -1.10898 |
| `explicit.stat_1011760251@T1` | -1.05830 |
| `explicit.stat_328541901@T2` | -0.99414 |
| `explicit.stat_2339757871@T1` | -0.93294 |
| `explicit.stat_1011760251@T2` | -0.87849 |
| `explicit.stat_1978899297@T1` | 0.78323 |
| `explicit.stat_2481353198@T1` | -0.70606 |
| `explicit.stat_2481353198@T2` | -0.69621 |
| `explicit.stat_1978899297@T2` | -0.64249 |
| `explicit.stat_53045048@T2` | -0.63046 |
| `explicit.stat_3362812763@T1` | -0.62943 |
| `explicit.stat_2901986750@T1` | -0.62533 |

### weapon.twomace — n=3136, R²=-0.5726

intercept: `-3.2974`  ·  log_price: True  ·  ilvl: `0.04227`  ·  n_mods: `-0.02220`  ·  n_top_tier: `0.79279`  ·  corrupted: `0.67007`  ·  n_sockets: `0.07762`  ·  quality: `0.01952`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.58966 |
| `explicit.stat_1037193709@T1` | -1.10661 |
| `crafted.stat_3035140377` | 1.06662 |
| `explicit.stat_3336890334@T1` | -0.97854 |
| `explicit.stat_1037193709@T2` | -0.96941 |
| `explicit.stat_387439868@T2` | -0.92393 |
| `explicit.stat_821021828@T2` | -0.91071 |
| `explicit.stat_1263695895@T2` | -0.88004 |
| `explicit.stat_691932474@T1` | -0.87274 |
| `explicit.stat_210067635@T1` | 0.86730 |
| `explicit.stat_3695891184@T1` | -0.86417 |
| `explicit.stat_669069897@T1` | -0.85297 |

## Coverage (listings per base)

- … **Sapphire** — 17813 listings (17788 priced) [0.4–7553463.8 ex]
- … **Emerald** — 17585 listings (17565 priced) [0.3–7553463.8 ex]
- … **Ruby** — 13572 listings (13560 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 7734 listings (7725 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 6193 listings (6187 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 6020 listings (6009 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 5934 listings (5930 priced) [0.2–4323655.9 ex]
- … **Stellar Amulet** — 5767 listings (5764 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 5699 listings (5689 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 5528 listings (5523 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 4917 listings (4905 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4614 listings (4609 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 4488 listings (4485 priced) [1.0–307202867.9 ex]
- … **Ruby Ring** — 4469 listings (4467 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 4082 listings (4076 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4009 listings (4006 priced) [0.3–5286174.1 ex]
- … **Ancestral Tiara** — 3946 listings (3939 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3913 listings (3912 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3885 listings (3881 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 3815 listings (3814 priced) [0.2–24532814.5 ex]
- … **Obliterator Bow** — 3782 listings (3771 priced) [0.3–42622633798.0 ex]
- … **Heavy Belt** — 3708 listings (3706 priced) [0.3–4877938.3 ex]
- … **Bloodstone Amulet** — 3699 listings (3696 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 3569 listings (3566 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 3517 listings (3517 priced) [0.3–123132003.2 ex]

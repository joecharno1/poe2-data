# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-03T14:15:00+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **51878** (51878 priced in exalted)
- Distinct bases: 769 · distinct mods: 1618 · mod rows: 260703
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-03T13:59:55+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.19** (median |log error| 1.9727)
- Within ±30% of asking price: **26%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 67% of actuals above prediction (target ≈ 75%)

| group | n_test | ×err | ±30% | skill |
|---|---|---|---|---|
| accessory.belt | 828 | ×9.33 | 17% | -0.05 |
| armour.boots | 817 | ×8.29 | 14% | -0.08 |
| armour.chest | 812 | ×7.00 | 11% | -0.04 |
| armour.gloves | 804 | ×8.55 | 19% | -0.03 |
| armour.helmet | 801 | ×6.85 | 13% | +0.02 |
| accessory.amulet | 728 | ×33.75 | 12% | +0.25 |
| accessory.ring | 679 | ×6.94 | 7% | -0.03 |
| weapon.wand | 624 | ×8.89 | 32% | +0.05 |
| weapon.bow | 589 | ×8.37 | 35% | +0.05 |
| weapon.crossbow | 564 | ×7.47 | 22% | +0.06 |
| other | 466 | ×7.34 | 37% | +0.47 |
| jewel | 339 | ×9.25 | 5% | -0.20 |
| weapon.sceptre | 173 | ×1.00 | 99% | +0.00 |
| weapon.spear | 164 | ×1.00 | 99% | +0.00 |
| armour.focus | 144 | ×1.00 | 100% | n/a |
| armour.shield | 129 | ×1.00 | 99% | +0.00 |
| armour.quiver | 102 | ×1.00 | 96% | +0.00 |
| weapon.twomace | 74 | ×1.00 | 96% | +0.00 |
| weapon.warstaff | 67 | ×1.00 | 97% | -0.00 |
| weapon.staff | 59 | ×1.00 | 95% | +0.00 |
| flask.charm | 31 | ×1.34 | 39% | -0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=5059, R²=0.1059

intercept: `1.6631`  ·  log_price: True  ·  ilvl: `0.00417`  ·  n_mods: `0.03797`  ·  n_top_tier: `0.11288`  ·  corrupted: `0.22488`  ·  n_sockets: `-0.13188`  ·  quality: `-0.01686`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.86040 |
| `explicit.stat_124131830` | -0.87995 |
| `explicit.stat_124131830@T2` | 0.56162 |
| `explicit.stat_4080418644@T1` | -0.55510 |
| `implicit.stat_718638445` | 0.50097 |
| `implicit.stat_3182714256` | 0.49739 |
| `explicit.stat_4080418644@T2` | -0.34353 |
| `implicit.stat_1379411836` | -0.30756 |
| `explicit.stat_4052037485@T1` | -0.20693 |
| `explicit.stat_3299347043@T1` | -0.19977 |
| `explicit.stat_1671376347@T2` | -0.19960 |
| `explicit.stat_3372524247@T1` | -0.19507 |

### accessory.belt — n=3984, R²=-1.0238

intercept: `4.4665`  ·  log_price: True  ·  ilvl: `-0.05643`  ·  n_mods: `-0.02280`  ·  n_top_tier: `-0.10504`  ·  corrupted: `0.09276`  ·  n_sockets: `-0.01131`

| stat_id | coef |
|---|---|
| `explicit.stat_4220027924@T1` | 2.07746 |
| `explicit.stat_1836676211@T1` | 1.42082 |
| `crafted.stat_3249412463` | 1.07202 |
| `explicit.stat_2923486259@T1` | 0.98220 |
| `implicit.stat_731781020` | 0.83574 |
| `explicit.stat_3299347043@T1` | -0.43072 |
| `explicit.stat_1412217137@T2` | 0.38761 |
| `explicit.stat_3299347043@T2` | -0.36855 |
| `explicit.stat_4220027924@T2` | 0.34200 |
| `explicit.stat_3372524247@T1` | 0.26908 |
| `explicit.stat_2881298780@T2` | 0.26291 |
| `explicit.stat_1836676211@T2` | 0.20101 |

### armour.chest — n=3834, R²=-1.1509

intercept: `4.2382`  ·  log_price: True  ·  ilvl: `-0.05361`  ·  n_mods: `-0.02292`  ·  n_top_tier: `0.15892`  ·  corrupted: `0.17525`  ·  n_sockets: `0.07475`  ·  quality: `0.00739`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 3.99359 |
| `implicit.stat_2251279027` | 1.79627 |
| `explicit.stat_3981240776@T1` | 1.62058 |
| `explicit.stat_3372524247@T1` | 1.45648 |
| `explicit.stat_4015621042@T1` | 1.25772 |
| `explicit.stat_2339757871@T1` | -0.85725 |
| `explicit.stat_4052037485@T1` | -0.53569 |
| `explicit.stat_915769802@T1` | -0.45218 |
| `explicit.stat_3362812763@T1` | -0.40039 |
| `explicit.stat_1671376347@T1` | 0.37846 |
| `explicit.stat_4080418644@T2` | -0.36181 |
| `implicit.stat_1978899297` | -0.35412 |

### armour.helmet — n=3828, R²=-1.0326

intercept: `4.5629`  ·  log_price: True  ·  ilvl: `-0.05919`  ·  n_mods: `-0.02608`  ·  n_top_tier: `0.52682`  ·  corrupted: `-0.22352`  ·  n_sockets: `0.08391`  ·  quality: `0.05577`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | -1.10667 |
| `explicit.stat_3033371881@T1` | -1.01958 |
| `explicit.stat_3372524247@T1` | 0.96764 |
| `explicit.stat_3033371881@T2` | -0.94468 |
| `explicit.stat_3325883026@T1` | -0.81642 |
| `explicit.stat_2339757871@T1` | -0.80586 |
| `explicit.stat_2162097452@T2` | -0.79575 |
| `explicit.stat_3325883026@T2` | -0.79494 |
| `explicit.stat_4015621042@T2` | -0.78427 |
| `explicit.stat_2451402625@T2` | -0.78380 |
| `explicit.stat_124859000@T1` | -0.76962 |
| `explicit.stat_1263695895@T1` | -0.76912 |

### armour.boots — n=3778, R²=-0.8774

intercept: `3.8090`  ·  log_price: True  ·  ilvl: `-0.04824`  ·  n_mods: `-0.05407`  ·  n_top_tier: `0.85246`  ·  corrupted: `0.72509`  ·  n_sockets: `0.10377`  ·  quality: `0.01728`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.40154 |
| `explicit.stat_2250533757@T1` | 1.35583 |
| `explicit.stat_2923486259@T2` | -1.12990 |
| `explicit.stat_3484657501@T2` | -1.06901 |
| `explicit.stat_3639275092@T1` | -1.05178 |
| `explicit.stat_1062208444@T1` | -1.03737 |
| `explicit.stat_3484657501@T1` | -1.01938 |
| `explicit.stat_2923486259@T1` | -1.01296 |
| `explicit.stat_1062208444@T2` | -0.96102 |
| `explicit.stat_3639275092@T2` | -0.95941 |
| `explicit.stat_3033371881@T2` | -0.95242 |
| `explicit.stat_3321629045@T2` | -0.95234 |

### armour.gloves — n=3652, R²=-1.0691

intercept: `3.8495`  ·  log_price: True  ·  ilvl: `-0.05060`  ·  n_mods: `-0.00313`  ·  n_top_tier: `0.31693`  ·  corrupted: `-0.40129`  ·  n_sockets: `0.14858`  ·  quality: `0.03098`

| stat_id | coef |
|---|---|
| `explicit.stat_3362812763@T2` | 1.66142 |
| `explicit.stat_3372524247@T1` | 1.37526 |
| `explicit.stat_2451402625@T1` | 1.24820 |
| `explicit.stat_3556824919@T1` | 1.15327 |
| `explicit.stat_2339757871@T1` | -0.87270 |
| `explicit.stat_4015621042@T2` | 0.75183 |
| `explicit.stat_1573130764@T2` | 0.60116 |
| `explicit.stat_1999113824@T2` | 0.59945 |
| `explicit.stat_4015621042@T1` | -0.55675 |
| `explicit.stat_3639275092@T1` | -0.53630 |
| `explicit.stat_2557965901@T2` | -0.51879 |
| `explicit.stat_4080418644@T2` | -0.50408 |

### accessory.amulet — n=3439, R²=-2.0071

intercept: `6.7004`  ·  log_price: True  ·  ilvl: `-0.06229`  ·  n_mods: `-0.54051`  ·  n_top_tier: `1.12115`  ·  corrupted: `1.17793`  ·  n_sockets: `-0.98977`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -7.63841 |
| `explicit.stat_2923486259@T2` | -5.09705 |
| `explicit.stat_9187492@T2` | -3.09748 |
| `explicit.stat_1202301673@T2` | 2.98704 |
| `explicit.stat_2482852589@T1` | -2.71424 |
| `explicit.stat_3299347043@T1` | -2.52908 |
| `explicit.stat_2482852589@T2` | -2.48261 |
| `explicit.stat_4220027924@T1` | 2.40486 |
| `explicit.stat_2748665614@T1` | -2.27282 |
| `explicit.stat_328541901@T1` | -2.24639 |
| `explicit.stat_1671376347@T1` | 2.07647 |
| `explicit.stat_1050105434@T1` | -2.07276 |

### accessory.ring — n=3305, R²=-2.3287

intercept: `4.6893`  ·  log_price: True  ·  ilvl: `-0.04076`  ·  n_mods: `-0.19726`  ·  n_top_tier: `0.35573`  ·  corrupted: `0.51826`  ·  n_sockets: `4.79610`  ·  quality: `0.00199`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 2.71874 |
| `explicit.stat_3299347043@T1` | -2.56770 |
| `explicit.stat_1263695895@T2` | -2.12674 |
| `explicit.stat_3695891184@T1` | -1.89186 |
| `explicit.stat_4220027924@T1` | 1.66494 |
| `explicit.stat_2923486259@T2` | -1.60652 |
| `explicit.stat_1263695895@T1` | -1.54883 |
| `explicit.stat_3962278098@T2` | -1.44639 |
| `explicit.stat_4067062424@T1` | -1.24956 |
| `explicit.stat_707457662@T2` | 1.21019 |
| `explicit.stat_3291658075@T2` | 1.11459 |
| `explicit.stat_1368271171@T1` | -1.03104 |

### weapon.wand — n=3151, R²=-1.3969

intercept: `3.1641`  ·  log_price: True  ·  ilvl: `-0.03955`  ·  n_mods: `-0.01845`  ·  n_top_tier: `0.06510`  ·  corrupted: `0.04479`  ·  n_sockets: `-0.00007`  ·  quality: `0.06413`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 3.76839 |
| `explicit.stat_591105508@T1` | 2.32516 |
| `explicit.stat_1545858329@T1` | 2.28813 |
| `explicit.stat_1600707273@T1` | 2.26117 |
| `explicit.stat_4226189338@T1` | 2.23818 |
| `explicit.stat_2974417149@T1` | 2.12584 |
| `explicit.stat_736967255@T2` | 2.11716 |
| `explicit.stat_2968503605@T1` | 1.63282 |
| `crafted.stat_124131830` | 1.39347 |
| `explicit.stat_124131830@T1` | 1.35633 |
| `rune.stat_3278136794` | -0.92664 |
| `explicit.stat_591105508@T2` | 0.58386 |

### weapon.bow — n=2761, R²=-1.31

intercept: `3.3217`  ·  log_price: True  ·  ilvl: `-0.04134`  ·  n_mods: `-0.02211`  ·  n_top_tier: `0.38522`  ·  corrupted: `0.23648`  ·  n_sockets: `0.02494`  ·  quality: `-0.00984`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -7.11872 |
| `desecrated.stat_1200678966@T1` | -5.81099 |
| `rune.stat_3885405204` | -2.66142 |
| `explicit.stat_2463230181@T1` | 1.87113 |
| `explicit.stat_1202301673@T1` | 1.81590 |
| `desecrated.stat_210067635@T1` | 1.30406 |
| `explicit.stat_821021828@T1` | -0.92445 |
| `crafted.stat_3035140377` | 0.92419 |
| `explicit.stat_821021828@T2` | -0.79596 |
| `explicit.stat_1509134228@T1` | 0.59174 |
| `desecrated.stat_666077204` | 0.46805 |
| `explicit.stat_1940865751@T1` | -0.45416 |

### weapon.crossbow — n=2630, R²=-1.2127

intercept: `3.4965`  ·  log_price: True  ·  ilvl: `-0.04469`  ·  n_mods: `0.00473`  ·  n_top_tier: `0.70236`  ·  corrupted: `0.35099`  ·  n_sockets: `0.10758`  ·  quality: `-0.06981`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 4.78018 |
| `explicit.stat_709508406@T1` | 3.23044 |
| `explicit.stat_691932474@T1` | -2.32690 |
| `explicit.stat_3336890334@T1` | 1.47656 |
| `explicit.stat_1037193709@T2` | 1.01286 |
| `explicit.stat_1202301673@T2` | -0.90710 |
| `explicit.stat_1509134228@T1` | 0.90612 |
| `explicit.stat_1263695895@T1` | 0.89211 |
| `explicit.stat_691932474@T2` | -0.79701 |
| `explicit.stat_3695891184@T2` | -0.79616 |
| `explicit.stat_3261801346@T1` | -0.78913 |
| `explicit.stat_4080418644@T1` | -0.78176 |

### jewel — n=1842, R²=-0.5355

intercept: `-1.8562`  ·  log_price: True  ·  ilvl: `0.04141`  ·  n_mods: `0.19055`  ·  n_top_tier: `-0.49868`  ·  corrupted: `0.46497`

| stat_id | coef |
|---|---|
| `explicit.stat_3851254963@T1` | 8.74973 |
| `explicit.stat_1569101201@T1` | 5.81298 |
| `explicit.stat_924253255@T1` | 5.74471 |
| `explicit.stat_1310194496@T1` | 5.70446 |
| `explicit.stat_21071013@T1` | 5.65027 |
| `explicit.stat_4081947835@T1` | 5.45450 |
| `explicit.stat_318953428@T1` | 4.97196 |
| `explicit.stat_2106365538@T1` | -4.83275 |
| `explicit.stat_3714003708@T1` | -4.67178 |
| `explicit.stat_3759663284@T1` | 4.15696 |
| `explicit.stat_1459321413@T1` | 4.13006 |
| `explicit.stat_1316278494@T1` | 3.95480 |

### weapon.sceptre — n=902, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1798257884` | 0.00000 |
| `desecrated.stat_1050105434` | 0.00000 |
| `desecrated.stat_1250712710` | 0.00000 |
| `desecrated.stat_1798257884` | 0.00000 |
| `desecrated.stat_3984865854` | 0.00000 |
| `explicit.stat_101878827` | 0.00000 |
| `explicit.stat_101878827@T1` | 0.00000 |
| `explicit.stat_101878827@T2` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_1250712710` | 0.00000 |

### weapon.spear — n=824, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1202301673@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |

### armour.focus — n=754, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1671376347` | 0.00000 |
| `desecrated.stat_2891184298` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T1` | -0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |
| `explicit.stat_2231156303` | 0.00000 |

### armour.shield — n=624, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1568848828` | 0.00000 |
| `explicit.stat_1011760251` | 0.00000 |
| `explicit.stat_1011760251@T1` | -0.00000 |
| `explicit.stat_1011760251@T2` | -0.00000 |
| `explicit.stat_1062208444` | 0.00000 |
| `explicit.stat_1062208444@T1` | 0.00000 |
| `explicit.stat_1062208444@T2` | 0.00000 |
| `explicit.stat_1301765461` | 0.00000 |
| `explicit.stat_1301765461@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |

### weapon.warstaff — n=528, R²=-0.0035

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_821021828@T2` | 0.00000 |
| `explicit.stat_210067635@T2` | 0.00000 |
| `explicit.stat_821021828@T1` | 0.00000 |
| `explicit.stat_210067635@T1` | 0.00000 |
| `explicit.stat_387439868@T1` | 0.00000 |
| `explicit.stat_387439868@T2` | 0.00000 |
| `explicit.stat_3695891184@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1940865751@T2` | 0.00000 |
| `explicit.stat_748522257@T1` | 0.00000 |
| `explicit.stat_1940865751@T1` | 0.00000 |
| `explicit.stat_3695891184@T2` | 0.00000 |

### weapon.staff — n=501, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1545858329` | 0.00000 |
| `explicit.stat_1545858329@T1` | 0.00000 |

### armour.quiver — n=493, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1241625305` | 0.00000 |
| `explicit.stat_1241625305@T1` | 0.00000 |
| `explicit.stat_1241625305@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | -0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1573130764` | 0.00000 |
| `explicit.stat_1573130764@T1` | 0.00000 |
| `explicit.stat_1573130764@T2` | 0.00000 |
| `explicit.stat_1754445556` | 0.00000 |

### flask.charm — n=458, R²=-0.6111

intercept: `0.0267`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00006`  ·  n_top_tier: `-0.00005`  ·  corrupted: `-0.29250`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.80474 |
| `explicit.stat_280890192` | -0.19046 |
| `explicit.stat_2541588185@T2` | 0.17121 |
| `implicit.stat_2016937536` | 0.16398 |
| `explicit.stat_3849649145` | -0.15972 |
| `explicit.stat_1873752457@T2` | 0.10159 |
| `explicit.stat_1873752457@T1` | 0.09141 |
| `explicit.stat_828533480@T2` | -0.06097 |
| `implicit.stat_4010341289` | -0.02657 |
| `implicit.stat_1691862754` | -0.02656 |
| `implicit.stat_2778646494` | -0.02656 |
| `implicit.stat_3699444296` | -0.02656 |

### weapon.twomace — n=361, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |
| `explicit.stat_1940865751` | 0.00000 |
| `explicit.stat_1940865751@T1` | 0.00000 |

## Coverage (listings per base)

- … **Utility Belt** — 1269 listings (1269 priced) [0.3–802.8 ex]
- … **Emerald** — 1000 listings (1000 priced) [0.4–802.8 ex]
- … **Dueling Wand** — 994 listings (994 priced) [1.0–802.8 ex]
- … **Sapphire** — 905 listings (905 priced) [0.4–802.8 ex]
- … **Stellar Amulet** — 833 listings (833 priced) [0.3–802.8 ex]
- … **Obliterator Bow** — 804 listings (804 priced) [0.5–802.8 ex]
- … **Ruby** — 775 listings (775 priced) [0.3–802.8 ex]
- … **Gold Amulet** — 625 listings (625 priced) [0.3–802.8 ex]
- … **Solar Amulet** — 620 listings (620 priced) [1.0–802.8 ex]
- … **Warmonger Bow** — 578 listings (578 priced) [0.9–802.8 ex]
- … **Plate Belt** — 570 listings (570 priced) [1.0–802.8 ex]
- … **Siphoning Wand** — 569 listings (569 priced) [1.0–802.8 ex]
- … **Ancestral Tiara** — 567 listings (567 priced) [1.0–802.8 ex]
- … **Galvanic Wand** — 567 listings (567 priced) [1.0–802.8 ex]
- … **Prismatic Ring** — 553 listings (553 priced) [0.3–802.8 ex]
- … **Heavy Belt** — 549 listings (549 priced) [0.5–802.8 ex]
- … **Amethyst Ring** — 531 listings (531 priced) [1.0–802.8 ex]
- … **Attuned Wand** — 522 listings (522 priced) [0.3–802.8 ex]
- … **Gold Ring** — 493 listings (493 priced) [0.7–802.8 ex]
- … **Withered Wand** — 490 listings (490 priced) [1.0–802.8 ex]
- … **Trarthan Cannon** — 476 listings (476 priced) [0.7–802.8 ex]
- … **Sapphire Ring** — 465 listings (465 priced) [0.5–802.8 ex]
- … **Topaz Ring** — 463 listings (463 priced) [1.0–802.8 ex]
- … **Long Belt** — 458 listings (458 priced) [1.0–802.8 ex]
- … **Lapis Amulet** — 438 listings (438 priced) [0.6–802.8 ex]

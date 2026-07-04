# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-04T00:19:06+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **74190** (74190 priced in exalted)
- Distinct bases: 828 · distinct mods: 1852 · mod rows: 364673
- Sold signals: **6779** sold · 9756 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-04T00:10:33+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.50** (median |log error| 2.0154)
- Within ±30% of asking price: **29%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 66% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×32.84 · ±30% 6% · n=10548
- Premium segment (60ex+): skill **+0.11** · typical error ×183.61 · ±30% 0% · n=6027
- Sold listings (clearing prices): skill **-0.04** · typical error ×2.49 · ±30% 44% · n=3566

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.belt | 1276 | ×9.51 | 24% | +0.03 | +0.05 |
| accessory.ring | 1167 | ×6.46 | 7% | +0.03 | +0.08 |
| accessory.amulet | 1165 | ×22.92 | 4% | -0.15 | -0.12 |
| armour.helmet | 1153 | ×8.32 | 20% | +0.01 | +0.08 |
| armour.chest | 1136 | ×8.30 | 23% | +0.01 | +0.07 |
| armour.gloves | 1061 | ×8.22 | 26% | +0.02 | +0.04 |
| other | 1004 | ×9.97 | 34% | +0.42 | +0.41 |
| armour.boots | 998 | ×8.65 | 27% | +0.00 | +0.08 |
| weapon.wand | 845 | ×9.31 | 34% | +0.02 | +0.07 |
| weapon.bow | 760 | ×8.95 | 32% | +0.04 | +0.10 |
| weapon.crossbow | 717 | ×8.03 | 22% | -0.01 | +0.11 |
| jewel | 581 | ×5.87 | 9% | +0.06 | +0.27 |
| weapon.sceptre | 213 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.spear | 182 | ×1.00 | 100% | +0.00 | +0.00 |
| armour.focus | 170 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.shield | 144 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.staff | 144 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.warstaff | 143 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 116 | ×1.00 | 97% | +0.00 | +0.00 |
| weapon.twomace | 67 | ×1.00 | 99% | +0.00 | +0.00 |
| flask.charm | 19 | ×1.45 | 21% | -0.07 | -0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=8608, R²=-0.0936

intercept: `1.5270`  ·  log_price: True  ·  ilvl: `0.00513`  ·  n_mods: `0.04104`  ·  n_top_tier: `0.13919`  ·  corrupted: `0.42564`  ·  n_sockets: `-0.11266`  ·  quality: `-0.01353`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.39410 |
| `explicit.stat_124131830@T2` | 1.16424 |
| `explicit.stat_124131830` | -0.99010 |
| `implicit.stat_718638445` | 0.45069 |
| `implicit.stat_3182714256` | 0.44582 |
| `implicit.stat_1379411836` | -0.29487 |
| `explicit.stat_4052037485@T1` | -0.22896 |
| `explicit.stat_3299347043@T2` | -0.22241 |
| `explicit.stat_3299347043@T1` | -0.20986 |
| `implicit.stat_4041853756` | 0.19390 |
| `implicit.stat_3879011313` | 0.19340 |
| `implicit.stat_958696139` | -0.18904 |

### accessory.belt — n=5797, R²=-1.2113

intercept: `4.6152`  ·  log_price: True  ·  ilvl: `-0.05609`  ·  n_mods: `-0.02308`  ·  n_top_tier: `0.01860`  ·  corrupted: `0.08565`  ·  n_sockets: `-0.19058`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.75292 |
| `explicit.stat_2923486259@T2` | 1.01768 |
| `explicit.stat_1836676211@T1` | 0.87770 |
| `explicit.stat_4220027924@T1` | 0.85516 |
| `explicit.stat_3372524247@T1` | 0.53871 |
| `explicit.stat_3299347043@T1` | -0.27650 |
| `explicit.stat_2923486259@T1` | -0.20365 |
| `explicit.stat_2639966148` | 0.11840 |
| `explicit.stat_3299347043@T2` | -0.10420 |
| `explicit.stat_174664100` | 0.09811 |
| `explicit.stat_2881298780@T2` | 0.07961 |
| `explicit.stat_4080418644@T2` | -0.07604 |

### armour.chest — n=5574, R²=-1.3438

intercept: `3.4813`  ·  log_price: True  ·  ilvl: `-0.04343`  ·  n_mods: `-0.02530`  ·  n_top_tier: `0.38249`  ·  corrupted: `0.08139`  ·  n_sockets: `0.03362`  ·  quality: `0.01554`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 4.04082 |
| `explicit.stat_3981240776@T1` | 1.50728 |
| `explicit.stat_3372524247@T1` | 0.86693 |
| `explicit.stat_1671376347@T1` | 0.83318 |
| `explicit.stat_2339757871@T1` | -0.63449 |
| `explicit.stat_915769802@T1` | -0.56713 |
| `explicit.stat_4052037485@T1` | -0.56377 |
| `explicit.stat_3261801346@T2` | -0.51133 |
| `explicit.stat_3261801346@T1` | -0.50720 |
| `explicit.stat_2339757871@T2` | -0.49809 |
| `explicit.stat_3981240776@T2` | 0.48726 |
| `explicit.stat_3325883026@T2` | -0.47101 |

### armour.helmet — n=5570, R²=-1.2651

intercept: `3.9312`  ·  log_price: True  ·  ilvl: `-0.04981`  ·  n_mods: `-0.02777`  ·  n_top_tier: `0.69057`  ·  corrupted: `0.13719`  ·  n_sockets: `0.01134`  ·  quality: `0.02366`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.85943 |
| `explicit.stat_3372524247@T1` | 1.30872 |
| `explicit.stat_3325883026@T1` | -0.91814 |
| `explicit.stat_1263695895@T1` | -0.90451 |
| `explicit.stat_3362812763@T1` | -0.87302 |
| `explicit.stat_3033371881@T2` | -0.87061 |
| `explicit.stat_2923486259@T1` | -0.86339 |
| `explicit.stat_3033371881@T1` | -0.86193 |
| `explicit.stat_4052037485@T2` | -0.83806 |
| `explicit.stat_3325883026@T2` | -0.83508 |
| `explicit.stat_3362812763@T2` | -0.82286 |
| `explicit.stat_124859000@T1` | -0.82227 |

### accessory.amulet — n=5484, R²=-2.2561

intercept: `5.5531`  ·  log_price: True  ·  ilvl: `-0.05850`  ·  n_mods: `-0.18311`  ·  n_top_tier: `0.01247`  ·  corrupted: `0.01781`  ·  n_sockets: `-0.47598`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | 3.13078 |
| `explicit.stat_1444556985@T1` | 2.60640 |
| `explicit.stat_983749596@T1` | -2.15859 |
| `explicit.stat_1671376347@T1` | 1.94829 |
| `explicit.stat_9187492@T2` | -1.89912 |
| `explicit.stat_2923486259@T1` | -1.89259 |
| `explicit.stat_3981240776@T2` | 1.74430 |
| `explicit.stat_3981240776@T1` | 1.67576 |
| `explicit.stat_4220027924@T1` | 1.45637 |
| `explicit.stat_9187492` | 1.34366 |
| `explicit.stat_124131830` | 1.32436 |
| `explicit.stat_983749596@T2` | -1.30165 |

### accessory.ring — n=5420, R²=-2.0252

intercept: `4.7790`  ·  log_price: True  ·  ilvl: `-0.03802`  ·  n_mods: `-0.21497`  ·  n_top_tier: `0.55549`  ·  corrupted: `0.27530`  ·  n_sockets: `3.14250`  ·  quality: `-0.00059`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.81791 |
| `explicit.stat_1573130764@T1` | -1.77365 |
| `explicit.stat_1263695895@T2` | -1.74205 |
| `explicit.stat_2231156303@T2` | -1.38478 |
| `explicit.stat_2231156303@T1` | -1.31634 |
| `explicit.stat_1671376347@T1` | -1.30888 |
| `explicit.stat_1263695895@T1` | -1.29962 |
| `explicit.stat_2923486259@T2` | -1.19050 |
| `explicit.stat_1050105434@T2` | -1.15772 |
| `explicit.stat_1050105434@T1` | -1.09347 |
| `explicit.stat_3962278098@T2` | -1.04172 |
| `explicit.stat_1573130764@T2` | -1.03876 |

### armour.gloves — n=4992, R²=-1.3218

intercept: `3.8875`  ·  log_price: True  ·  ilvl: `-0.04919`  ·  n_mods: `0.00402`  ·  n_top_tier: `0.30540`  ·  corrupted: `-0.16332`  ·  n_sockets: `0.07456`  ·  quality: `0.00373`

| stat_id | coef |
|---|---|
| `explicit.stat_1671376347@T1` | 1.55272 |
| `explicit.stat_2339757871@T1` | -1.44723 |
| `explicit.stat_3556824919@T1` | 1.29078 |
| `explicit.stat_1573130764@T2` | 1.17443 |
| `explicit.stat_2451402625@T1` | 1.14873 |
| `explicit.stat_2557965901@T2` | -0.48155 |
| `explicit.stat_9187492@T2` | -0.47745 |
| `explicit.stat_2557965901@T1` | -0.47324 |
| `explicit.stat_3033371881@T2` | -0.41834 |
| `explicit.stat_3033371881@T1` | -0.40311 |
| `explicit.stat_681332047@T2` | -0.40064 |
| `explicit.stat_4015621042@T2` | 0.39053 |

### armour.boots — n=4956, R²=-1.0515

intercept: `3.4207`  ·  log_price: True  ·  ilvl: `-0.04313`  ·  n_mods: `-0.02236`  ·  n_top_tier: `0.50550`  ·  corrupted: `0.15070`  ·  n_sockets: `0.06969`  ·  quality: `0.04468`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.72696 |
| `explicit.stat_2923486259@T1` | 0.99651 |
| `explicit.stat_2339757871@T1` | -0.73367 |
| `explicit.stat_3639275092@T1` | -0.62053 |
| `explicit.stat_3362812763@T1` | -0.61664 |
| `explicit.stat_3362812763@T2` | -0.60765 |
| `explicit.stat_1062208444@T1` | -0.59865 |
| `explicit.stat_3033371881@T2` | -0.59522 |
| `explicit.stat_3484657501@T2` | -0.59283 |
| `explicit.stat_3261801346@T2` | -0.58415 |
| `explicit.stat_3639275092@T2` | -0.57487 |
| `explicit.stat_3321629045@T1` | -0.57306 |

### weapon.wand — n=4050, R²=-1.4877

intercept: `3.1611`  ·  log_price: True  ·  ilvl: `-0.03951`  ·  n_mods: `-0.01445`  ·  n_top_tier: `0.06504`  ·  corrupted: `0.02493`  ·  n_sockets: `0.00854`  ·  quality: `0.01624`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.34042 |
| `explicit.stat_1600707273@T1` | 2.25432 |
| `explicit.stat_4226189338@T1` | 2.23459 |
| `explicit.stat_736967255@T2` | 2.18700 |
| `explicit.stat_1545858329@T1` | 2.17901 |
| `explicit.stat_2974417149@T1` | 2.17384 |
| `explicit.stat_124131830@T1` | 2.07705 |
| `explicit.stat_1600707273@T2` | 1.69965 |
| `crafted.stat_124131830` | 0.96181 |
| `explicit.stat_2254480358@T1` | 0.86894 |
| `explicit.stat_2968503605@T1` | 0.46801 |
| `rune.stat_3278136794` | 0.25067 |

### weapon.bow — n=3486, R²=-1.379

intercept: `3.3064`  ·  log_price: True  ·  ilvl: `-0.04093`  ·  n_mods: `-0.02447`  ·  n_top_tier: `0.39710`  ·  corrupted: `0.20032`  ·  n_sockets: `0.01526`  ·  quality: `-0.00792`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -7.18776 |
| `explicit.stat_1509134228@T1` | 1.85423 |
| `explicit.stat_1202301673@T1` | 1.83353 |
| `explicit.stat_2463230181@T1` | 1.80934 |
| `desecrated.stat_210067635@T1` | -1.65792 |
| `explicit.stat_821021828@T1` | -0.70244 |
| `crafted.stat_3035140377` | 0.63206 |
| `explicit.stat_821021828@T2` | -0.61185 |
| `desecrated.stat_666077204` | 0.49808 |
| `explicit.stat_1940865751@T1` | -0.49688 |
| `explicit.stat_1263695895@T1` | -0.47372 |
| `explicit.stat_691932474@T2` | -0.47208 |

### weapon.crossbow — n=3288, R²=-1.3094

intercept: `3.3642`  ·  log_price: True  ·  ilvl: `-0.04285`  ·  n_mods: `-0.00013`  ·  n_top_tier: `0.45930`  ·  corrupted: `0.04871`  ·  n_sockets: `0.06319`  ·  quality: `-0.03406`

| stat_id | coef |
|---|---|
| `explicit.stat_709508406@T1` | 2.16505 |
| `explicit.stat_3336890334@T1` | 1.96854 |
| `explicit.stat_1037193709@T1` | 1.90477 |
| `explicit.stat_691932474@T1` | -1.86661 |
| `explicit.stat_1509134228@T1` | 0.92212 |
| `explicit.stat_1263695895@T2` | -0.80567 |
| `crafted.stat_3035140377` | 0.73195 |
| `explicit.stat_1263695895@T1` | 0.66455 |
| `explicit.stat_2694482655@T1` | -0.60983 |
| `explicit.stat_518292764@T1` | 0.60547 |
| `explicit.stat_1509134228@T2` | -0.59802 |
| `explicit.stat_3695891184@T2` | -0.56532 |

### jewel — n=3016, R²=-0.8203

intercept: `-1.5766`  ·  log_price: True  ·  ilvl: `0.03499`  ·  n_mods: `0.25245`  ·  n_top_tier: `-0.50215`  ·  corrupted: `0.87543`

| stat_id | coef |
|---|---|
| `explicit.stat_1569101201@T1` | 6.79647 |
| `explicit.stat_1594812856@T1` | 6.76572 |
| `explicit.stat_2527686725@T1` | 6.69534 |
| `explicit.stat_2301718443@T1` | -6.32414 |
| `explicit.stat_1569159338@T1` | 5.32449 |
| `explicit.stat_1459321413@T1` | 5.07031 |
| `explicit.stat_3787460122@T1` | 4.70778 |
| `explicit.stat_3851254963@T1` | 4.02667 |
| `explicit.stat_293638271@T1` | -4.00069 |
| `explicit.stat_2456523742@T1` | 3.98610 |
| `explicit.stat_2011656677@T1` | 3.82074 |
| `explicit.stat_3283482523@T1` | -3.53599 |

### weapon.sceptre — n=1043, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

### weapon.spear — n=932, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
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

### armour.focus — n=835, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

### weapon.warstaff — n=717, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_210067635` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |

### armour.shield — n=713, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1568848828` | 0.00000 |
| `explicit.stat_1011760251` | 0.00000 |
| `explicit.stat_1011760251@T1` | -0.00000 |
| `explicit.stat_1011760251@T2` | 0.00000 |
| `explicit.stat_1062208444` | 0.00000 |
| `explicit.stat_1062208444@T1` | 0.00000 |
| `explicit.stat_1062208444@T2` | 0.00000 |
| `explicit.stat_1301765461` | 0.00000 |
| `explicit.stat_1301765461@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |

### weapon.staff — n=693, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_124131830` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T1` | 0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |

### armour.quiver — n=647, R²=0.0

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

### flask.charm — n=510, R²=-0.6508

intercept: `0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `-0.00002`  ·  corrupted: `0.19462`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.61491 |
| `explicit.stat_1873752457@T1` | -0.34823 |
| `explicit.stat_3849649145` | -0.12293 |
| `explicit.stat_1873752457@T2` | -0.12290 |
| `explicit.stat_828533480@T2` | -0.06104 |
| `explicit.stat_2541588185@T2` | -0.04219 |
| `explicit.stat_3196823591@T2` | -0.00010 |
| `implicit.stat_3699444296` | -0.00005 |
| `implicit.stat_4010341289` | -0.00005 |
| `explicit.stat_2716923832` | 0.00004 |
| `explicit.stat_3891350097` | -0.00004 |
| `implicit.stat_3310778564` | -0.00003 |

### weapon.twomace — n=463, R²=0.0

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

- … **Utility Belt** — 1788 listings (1788 priced) [0.3–10711.3 ex]
- … **Emerald** — 1743 listings (1743 priced) [0.6–802.8 ex]
- … **Sapphire** — 1648 listings (1648 priced) [0.4–802.8 ex]
- … **Ruby** — 1385 listings (1385 priced) [0.3–802.8 ex]
- … **Stellar Amulet** — 1322 listings (1322 priced) [0.3–35704.5 ex]
- … **Dueling Wand** — 1277 listings (1277 priced) [0.8–802.8 ex]
- … **Solar Amulet** — 1016 listings (1016 priced) [1.0–802.8 ex]
- … **Obliterator Bow** — 1002 listings (1002 priced) [0.5–802.8 ex]
- … **Gold Amulet** — 993 listings (993 priced) [0.3–802.8 ex]
- … **Prismatic Ring** — 955 listings (955 priced) [0.3–802.8 ex]
- … **Amethyst Ring** — 933 listings (933 priced) [0.8–802.8 ex]
- … **Gold Ring** — 873 listings (873 priced) [0.7–802.8 ex]
- … **Plate Belt** — 873 listings (873 priced) [1.0–802.8 ex]
- … **Heavy Belt** — 811 listings (811 priced) [0.5–802.8 ex]
- … **Ancestral Tiara** — 808 listings (808 priced) [1.0–802.8 ex]
- … **Topaz Ring** — 771 listings (771 priced) [1.0–802.8 ex]
- … **Sapphire Ring** — 767 listings (767 priced) [0.5–802.8 ex]
- … **Galvanic Wand** — 741 listings (741 priced) [1.0–802.8 ex]
- … **Ruby Ring** — 726 listings (726 priced) [0.4–802.8 ex]
- … **Warmonger Bow** — 725 listings (725 priced) [0.9–802.8 ex]
- … **Siphoning Wand** — 717 listings (717 priced) [1.0–802.8 ex]
- … **Lapis Amulet** — 701 listings (701 priced) [0.6–802.8 ex]
- … **Jade Amulet** — 684 listings (684 priced) [0.3–802.8 ex]
- … **Attuned Wand** — 672 listings (672 priced) [0.3–802.8 ex]
- … **Amber Amulet** — 667 listings (667 priced) [0.3–802.8 ex]

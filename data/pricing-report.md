# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-04T13:15:07+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **108216** (108216 priced in exalted)
- Distinct bases: 866 · distinct mods: 2104 · mod rows: 523238
- Sold signals: **27933** sold · 30581 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-04T13:09:44+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.56** (median |log error| 2.0223)
- Within ±30% of asking price: **28%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 66% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×33.19 · ±30% 6% · n=14969
- Premium segment (60ex+): skill **+0.12** · typical error ×178.50 · ±30% 0% · n=8422
- Sold listings (clearing prices): skill **-0.01** · typical error ×2.43 · ±30% 45% · n=7258

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.amulet | 1821 | ×25.55 | 9% | -0.03 | +0.00 |
| accessory.belt | 1780 | ×9.52 | 26% | +0.01 | +0.05 |
| accessory.ring | 1779 | ×7.05 | 6% | +0.02 | +0.01 |
| armour.helmet | 1707 | ×8.75 | 22% | +0.02 | +0.03 |
| armour.chest | 1667 | ×7.77 | 22% | +0.05 | +0.11 |
| armour.gloves | 1569 | ×8.62 | 23% | +0.02 | +0.05 |
| armour.boots | 1502 | ×8.94 | 24% | +0.02 | +0.08 |
| other | 1436 | ×5.91 | 34% | +0.43 | +0.39 |
| jewel | 1276 | ×6.92 | 9% | +0.02 | +0.04 |
| weapon.wand | 1221 | ×9.25 | 34% | +0.04 | +0.07 |
| weapon.bow | 1014 | ×8.37 | 35% | +0.07 | +0.08 |
| weapon.crossbow | 950 | ×8.53 | 32% | +0.08 | +0.13 |
| weapon.sceptre | 248 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.warstaff | 229 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.spear | 220 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.staff | 193 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.focus | 184 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 178 | ×1.00 | 94% | +0.00 | +0.00 |
| armour.shield | 169 | ×1.00 | 96% | +0.00 | +0.00 |
| weapon.twomace | 131 | ×1.00 | 98% | +0.00 | +0.00 |
| flask.charm | 63 | ×1.00 | 86% | -0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=12756, R²=-0.2495

intercept: `1.5898`  ·  log_price: True  ·  ilvl: `0.00506`  ·  n_mods: `0.04646`  ·  n_top_tier: `0.10498`  ·  corrupted: `0.30772`  ·  n_sockets: `-0.14251`  ·  quality: `-0.01605`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830` | -0.64478 |
| `implicit.stat_718638445` | 0.51957 |
| `implicit.stat_3182714256` | 0.51953 |
| `implicit.stat_958696139` | -0.34957 |
| `explicit.stat_1050105434@T1` | -0.34130 |
| `implicit.stat_1379411836` | -0.31667 |
| `explicit.stat_2974417149@T1` | 0.28614 |
| `explicit.stat_2891184298@T1` | -0.22923 |
| `explicit.stat_101878827@T1` | -0.19200 |
| `implicit.stat_4041853756` | 0.18760 |
| `implicit.stat_3879011313` | 0.18710 |
| `explicit.stat_1050105434@T2` | -0.18671 |

### accessory.amulet — n=8387, R²=-2.2189

intercept: `5.2478`  ·  log_price: True  ·  ilvl: `-0.06066`  ·  n_mods: `-0.13697`  ·  n_top_tier: `-0.00541`  ·  corrupted: `-0.13423`  ·  n_sockets: `0.12796`  ·  quality: `0.16016`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | 2.98603 |
| `explicit.stat_587431675@T1` | 2.16124 |
| `explicit.stat_2162097452@T2` | -1.97978 |
| `explicit.stat_3372524247@T1` | 1.67494 |
| `explicit.stat_3981240776@T2` | -1.60026 |
| `explicit.stat_9187492` | 1.56864 |
| `explicit.stat_2162097452` | 1.26733 |
| `explicit.stat_3981240776@T1` | -1.26255 |
| `explicit.stat_1671376347@T1` | 1.24146 |
| `explicit.stat_124131830@T2` | 1.19638 |
| `explicit.stat_3261801346@T2` | 1.17950 |
| `explicit.stat_124131830` | 1.09883 |

### accessory.ring — n=8192, R²=-1.8909

intercept: `3.8709`  ·  log_price: True  ·  ilvl: `-0.02640`  ·  n_mods: `-0.23705`  ·  n_top_tier: `0.58591`  ·  corrupted: `0.53870`  ·  n_sockets: `3.17690`  ·  quality: `0.03535`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 3.48650 |
| `explicit.stat_707457662@T2` | 3.29161 |
| `explicit.stat_2557965901@T2` | 2.56338 |
| `explicit.stat_2557965901@T1` | 2.40012 |
| `explicit.stat_1573130764@T1` | -2.30499 |
| `explicit.stat_3299347043@T1` | -1.66980 |
| `explicit.stat_789117908@T1` | -1.36170 |
| `explicit.stat_2231156303@T2` | -1.30125 |
| `explicit.stat_1671376347@T1` | -1.29145 |
| `explicit.stat_1050105434@T1` | -1.27791 |
| `explicit.stat_2923486259@T1` | -1.25560 |
| `explicit.stat_1573130764@T2` | -1.21728 |

### accessory.belt — n=8102, R²=-1.2295

intercept: `4.2622`  ·  log_price: True  ·  ilvl: `-0.05185`  ·  n_mods: `-0.02777`  ·  n_top_tier: `0.05271`  ·  corrupted: `0.15498`  ·  n_sockets: `-0.10295`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.76617 |
| `crafted.stat_3249412463` | 1.67847 |
| `explicit.stat_2923486259@T2` | 0.89867 |
| `explicit.stat_1836676211@T1` | 0.88444 |
| `explicit.stat_3299347043@T1` | -0.28509 |
| `explicit.stat_3299347043@T2` | -0.23851 |
| `implicit.stat_731781020` | 0.16751 |
| `explicit.stat_1389754388@T1` | -0.13939 |
| `explicit.stat_1671376347@T1` | 0.12432 |
| `explicit.stat_2881298780@T1` | -0.09922 |
| `explicit.stat_1389754388@T2` | -0.09240 |
| `explicit.stat_809229260@T2` | -0.09234 |

### armour.chest — n=7850, R²=-1.3175

intercept: `3.7971`  ·  log_price: True  ·  ilvl: `-0.04693`  ·  n_mods: `-0.02428`  ·  n_top_tier: `0.74730`  ·  corrupted: `-0.03945`  ·  n_sockets: `-0.00610`  ·  quality: `0.01649`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 2.02522 |
| `implicit.stat_2251279027` | 1.63157 |
| `explicit.stat_3981240776@T1` | 1.18976 |
| `explicit.stat_2923486259@T1` | -1.04015 |
| `explicit.stat_2923486259@T2` | -1.00696 |
| `explicit.stat_2339757871@T1` | -0.92749 |
| `explicit.stat_3261801346@T2` | -0.90162 |
| `explicit.stat_3261801346@T1` | -0.88217 |
| `explicit.stat_3301100256@T2` | -0.84261 |
| `explicit.stat_915769802@T1` | -0.81459 |
| `explicit.stat_986397080@T2` | -0.80733 |
| `explicit.stat_4052037485@T1` | -0.80459 |

### armour.helmet — n=7819, R²=-1.2867

intercept: `4.1437`  ·  log_price: True  ·  ilvl: `-0.05244`  ·  n_mods: `-0.02056`  ·  n_top_tier: `0.74575`  ·  corrupted: `0.19317`  ·  n_sockets: `-0.02911`  ·  quality: `0.02387`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 7.34810 |
| `explicit.stat_3033371881@T1` | -1.93953 |
| `explicit.stat_3033371881@T2` | -1.79268 |
| `explicit.stat_2339757871@T1` | -1.62647 |
| `explicit.stat_803737631@T2` | -0.92294 |
| `explicit.stat_3325883026@T1` | -0.90100 |
| `explicit.stat_3362812763@T1` | -0.90047 |
| `explicit.stat_3372524247@T1` | 0.87382 |
| `explicit.stat_3362812763@T2` | -0.86759 |
| `explicit.stat_3321629045@T2` | -0.84020 |
| `explicit.stat_53045048@T1` | -0.83892 |
| `explicit.stat_3325883026@T2` | -0.83181 |

### armour.boots — n=7227, R²=-1.0883

intercept: `3.9765`  ·  log_price: True  ·  ilvl: `-0.04957`  ·  n_mods: `-0.03636`  ·  n_top_tier: `0.37737`  ·  corrupted: `0.04815`  ·  n_sockets: `0.03821`  ·  quality: `0.02629`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.78794 |
| `explicit.stat_2339757871@T1` | -1.33810 |
| `explicit.stat_4220027924@T1` | 1.19832 |
| `explicit.stat_3362812763@T1` | -0.58818 |
| `explicit.stat_3321629045@T1` | -0.56818 |
| `explicit.stat_3033371881@T2` | -0.54821 |
| `explicit.stat_3362812763@T2` | -0.53366 |
| `explicit.stat_3484657501@T2` | -0.47697 |
| `explicit.stat_2160282525@T1` | -0.46921 |
| `explicit.stat_1874553720@T2` | -0.46136 |
| `explicit.stat_99927264@T1` | -0.45796 |
| `explicit.stat_124859000@T1` | -0.45560 |

### armour.gloves — n=7173, R²=-1.3067

intercept: `4.1598`  ·  log_price: True  ·  ilvl: `-0.05282`  ·  n_mods: `0.00394`  ·  n_top_tier: `0.77621`  ·  corrupted: `0.00877`  ·  n_sockets: `0.02547`  ·  quality: `0.03633`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.85045 |
| `explicit.stat_3372524247@T1` | 1.14499 |
| `explicit.stat_1671376347@T1` | 1.07832 |
| `explicit.stat_9187492@T2` | -0.93970 |
| `explicit.stat_4015621042@T1` | -0.90202 |
| `explicit.stat_681332047@T2` | -0.88082 |
| `explicit.stat_3917489142@T1` | -0.87975 |
| `explicit.stat_2557965901@T2` | -0.86577 |
| `explicit.stat_4052037485@T2` | -0.85797 |
| `explicit.stat_803737631@T1` | -0.84726 |
| `explicit.stat_2557965901@T1` | -0.84617 |
| `explicit.stat_3917489142@T2` | -0.84346 |

### jewel — n=6258, R²=-0.9998

intercept: `-1.5385`  ·  log_price: True  ·  ilvl: `0.03926`  ·  n_mods: `0.12973`  ·  n_top_tier: `-0.38433`  ·  corrupted: `0.63170`

| stat_id | coef |
|---|---|
| `explicit.stat_2456523742@T1` | 4.87668 |
| `explicit.stat_1697447343@T1` | -4.32323 |
| `explicit.stat_1836676211@T1` | -3.78903 |
| `explicit.stat_1697951953@T1` | 3.73008 |
| `explicit.stat_2301718443@T1` | -3.72279 |
| `explicit.stat_3973629633@T1` | 3.68487 |
| `explicit.stat_293638271@T1` | -3.66109 |
| `explicit.stat_3851254963@T1` | 3.59803 |
| `explicit.stat_429143663@T1` | 3.24725 |
| `explicit.stat_924253255@T1` | 3.20289 |
| `explicit.stat_3377888098@T1` | -3.14795 |
| `explicit.stat_2106365538@T1` | -3.10738 |

### weapon.wand — n=5649, R²=-1.5982

intercept: `3.3893`  ·  log_price: True  ·  ilvl: `-0.04230`  ·  n_mods: `-0.01252`  ·  n_top_tier: `0.41727`  ·  corrupted: `0.01744`  ·  n_sockets: `0.00535`  ·  quality: `0.02636`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.10827 |
| `explicit.stat_1545858329@T1` | 1.92325 |
| `explicit.stat_591105508@T1` | 1.89487 |
| `explicit.stat_2254480358@T1` | 1.82675 |
| `explicit.stat_4226189338@T1` | 1.67688 |
| `explicit.stat_736967255@T2` | 1.61612 |
| `explicit.stat_1600707273@T2` | 1.30660 |
| `explicit.stat_1600707273@T1` | 1.16135 |
| `crafted.stat_124131830` | 1.07670 |
| `explicit.stat_124131830@T2` | -0.53561 |
| `explicit.stat_293638271@T2` | -0.50349 |
| `explicit.stat_3962278098@T2` | -0.48354 |

### weapon.bow — n=4825, R²=-1.5368

intercept: `3.3564`  ·  log_price: True  ·  ilvl: `-0.04166`  ·  n_mods: `-0.02380`  ·  n_top_tier: `0.27289`  ·  corrupted: `-0.02693`  ·  n_sockets: `0.00874`  ·  quality: `-0.00157`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -7.53518 |
| `explicit.stat_2463230181@T1` | 2.01225 |
| `explicit.stat_1509134228@T1` | 1.88196 |
| `explicit.stat_518292764@T1` | 1.81243 |
| `explicit.stat_1202301673@T1` | 1.73094 |
| `crafted.stat_3035140377` | 1.09712 |
| `desecrated.stat_210067635@T1` | 0.66678 |
| `rune.stat_3885405204` | -0.64833 |
| `desecrated.stat_666077204` | 0.46323 |
| `explicit.stat_821021828@T1` | -0.40252 |
| `explicit.stat_1940865751@T1` | -0.37277 |
| `explicit.stat_2694482655@T1` | -0.36820 |

### weapon.crossbow — n=4537, R²=-1.3952

intercept: `3.5195`  ·  log_price: True  ·  ilvl: `-0.04409`  ·  n_mods: `0.00267`  ·  n_top_tier: `0.48742`  ·  corrupted: `-0.00906`  ·  n_sockets: `0.02171`  ·  quality: `-0.00984`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -3.28696 |
| `explicit.stat_2250681686` | 2.85304 |
| `explicit.stat_709508406@T1` | 2.39988 |
| `explicit.stat_1037193709@T1` | 1.83193 |
| `explicit.stat_3336890334@T1` | 1.79365 |
| `explicit.stat_1509134228@T1` | 1.76898 |
| `explicit.stat_691932474@T1` | -1.29585 |
| `explicit.stat_1202301673@T1` | 0.94712 |
| `crafted.stat_3035140377` | 0.84382 |
| `explicit.stat_1967051901@T1` | 0.81831 |
| `explicit.stat_518292764@T1` | 0.77656 |
| `explicit.stat_1263695895@T2` | -0.57239 |

### weapon.sceptre — n=1254, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1798257884` | 0.00000 |
| `desecrated.stat_1050105434` | 0.00000 |
| `desecrated.stat_1798257884` | 0.00000 |
| `desecrated.stat_3984865854` | 0.00000 |
| `explicit.stat_101878827` | 0.00000 |
| `explicit.stat_101878827@T1` | 0.00000 |
| `explicit.stat_101878827@T2` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_1250712710` | 0.00000 |
| `explicit.stat_1250712710@T1` | 0.00000 |

### weapon.spear — n=1113, R²=0.0

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

### weapon.warstaff — n=1092, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_1037193709` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_1940865751` | 0.00000 |
| `desecrated.stat_210067635` | 0.00000 |
| `desecrated.stat_2694482655` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |
| `desecrated.stat_387439868` | 0.00000 |
| `desecrated.stat_4258524206` | 0.00000 |

### weapon.staff — n=1040, R²=0.0

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

### armour.focus — n=955, R²=0.0

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

### flask.charm — n=902, R²=-0.4096

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2541588185@T2` | 0.24984 |
| `explicit.stat_1873752457` | 0.00011 |
| `explicit.stat_1120862500@T2` | -0.00006 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_1873752457@T2` | -0.00002 |
| `explicit.stat_3849649145` | -0.00002 |
| `explicit.stat_2365392475@T2` | -0.00002 |
| `explicit.stat_2566921799` | 0.00002 |
| `implicit.stat_3676540188` | -0.00001 |
| `implicit.stat_1691862754` | -0.00001 |
| `implicit.stat_1810482573` | -0.00001 |
| `implicit.stat_585126960` | -0.00001 |

### armour.quiver — n=848, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.00000 |
| `desecrated.stat_3714003708` | 0.00000 |
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

### armour.shield — n=829, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

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

### weapon.twomace — n=604, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

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

- … **Emerald** — 3309 listings (3309 priced) [0.5–856.7 ex]
- … **Sapphire** — 3228 listings (3228 priced) [0.4–856.7 ex]
- … **Ruby** — 2603 listings (2603 priced) [0.3–856.7 ex]
- … **Utility Belt** — 2577 listings (2577 priced) [0.3–83658.4 ex]
- … **Stellar Amulet** — 1914 listings (1914 priced) [0.3–41829.2 ex]
- … **Dueling Wand** — 1787 listings (1787 priced) [0.8–856.7 ex]
- … **Solar Amulet** — 1579 listings (1579 priced) [1.0–856.7 ex]
- … **Gold Amulet** — 1541 listings (1541 priced) [0.6–856.7 ex]
- … **Prismatic Ring** — 1465 listings (1465 priced) [0.3–856.7 ex]
- … **Amethyst Ring** — 1405 listings (1405 priced) [0.8–856.7 ex]
- … **Gold Ring** — 1375 listings (1375 priced) [0.7–856.7 ex]
- … **Obliterator Bow** — 1372 listings (1372 priced) [0.6–856.7 ex]
- … **Plate Belt** — 1254 listings (1254 priced) [1.0–856.7 ex]
- … **Heavy Belt** — 1151 listings (1151 priced) [0.5–856.7 ex]
- … **Topaz Ring** — 1143 listings (1143 priced) [1.0–856.7 ex]
- … **Sapphire Ring** — 1131 listings (1131 priced) [0.5–856.7 ex]
- … **Ancestral Tiara** — 1119 listings (1119 priced) [1.0–856.7 ex]
- … **Ruby Ring** — 1078 listings (1078 priced) [0.4–856.7 ex]
- … **Lapis Amulet** — 1034 listings (1034 priced) [0.6–856.7 ex]
- … **Galvanic Wand** — 1023 listings (1023 priced) [1.0–856.7 ex]
- … **Jade Amulet** — 1006 listings (1006 priced) [0.6–856.7 ex]
- … **Amber Amulet** — 1002 listings (1002 priced) [0.6–856.7 ex]
- … **Siphoning Wand** — 993 listings (993 priced) [1.0–856.7 ex]
- … **Warmonger Bow** — 971 listings (971 priced) [1.0–856.7 ex]
- … **Attuned Wand** — 939 listings (939 priced) [0.3–856.7 ex]

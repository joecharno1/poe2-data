# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-04T19:23:33+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **123272** (123272 priced in exalted)
- Distinct bases: 882 · distinct mods: 2195 · mod rows: 593865
- Sold signals: **33686** sold · 42082 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-04T19:16:58+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.39** (median |log error| 1.9997)
- Within ±30% of asking price: **29%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 67% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×27.44 · ±30% 9% · n=17373
- Premium segment (60ex+): skill **+0.11** · typical error ×141.10 · ±30% 0% · n=9816
- Sold listings (clearing prices): skill **-0.02** · typical error ×2.76 · ±30% 46% · n=7499

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.amulet | 2068 | ×30.89 | 12% | +0.03 | -0.01 |
| accessory.ring | 2034 | ×5.66 | 9% | +0.04 | -0.03 |
| accessory.belt | 1994 | ×9.72 | 24% | -0.00 | +0.04 |
| armour.chest | 1932 | ×8.43 | 20% | +0.01 | +0.08 |
| armour.helmet | 1911 | ×8.87 | 22% | +0.01 | +0.07 |
| armour.boots | 1776 | ×8.73 | 25% | +0.03 | +0.09 |
| armour.gloves | 1748 | ×6.00 | 36% | -0.00 | -0.05 |
| other | 1677 | ×6.20 | 34% | +0.40 | +0.37 |
| jewel | 1511 | ×6.43 | 8% | +0.01 | +0.10 |
| weapon.wand | 1356 | ×9.11 | 35% | +0.05 | +0.09 |
| weapon.bow | 1154 | ×8.95 | 34% | +0.08 | +0.04 |
| weapon.crossbow | 1081 | ×8.27 | 33% | +0.08 | +0.13 |
| weapon.sceptre | 268 | ×1.00 | 97% | +0.00 | +0.00 |
| weapon.staff | 255 | ×1.00 | 97% | +0.00 | +0.00 |
| weapon.spear | 251 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.warstaff | 246 | ×1.00 | 98% | +0.00 | +0.00 |
| armour.focus | 214 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 190 | ×1.00 | 95% | +0.00 | +0.00 |
| armour.shield | 182 | ×1.00 | 95% | +0.00 | +0.00 |
| weapon.twomace | 140 | ×1.00 | 98% | +0.00 | +0.00 |
| flask.charm | 76 | ×1.22 | 51% | +0.02 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=14694, R²=-0.3058

intercept: `1.5130`  ·  log_price: True  ·  ilvl: `0.00555`  ·  n_mods: `0.06114`  ·  n_top_tier: `0.10882`  ·  corrupted: `0.34289`  ·  n_sockets: `-0.13472`  ·  quality: `-0.01449`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830` | -0.63054 |
| `implicit.stat_3182714256` | 0.52564 |
| `implicit.stat_718638445` | 0.52553 |
| `explicit.stat_4220027924@T2` | -0.38294 |
| `explicit.stat_1050105434@T1` | -0.33465 |
| `implicit.stat_1379411836` | -0.32241 |
| `explicit.stat_2974417149@T1` | 0.23537 |
| `implicit.stat_958696139` | 0.20960 |
| `explicit.stat_3917489142@T1` | -0.20852 |
| `implicit.stat_4041853756` | 0.18993 |
| `implicit.stat_3879011313` | 0.18992 |
| `explicit.stat_789117908@T1` | 0.15674 |

### accessory.amulet — n=9578, R²=-2.262

intercept: `4.9067`  ·  log_price: True  ·  ilvl: `-0.05947`  ·  n_mods: `-0.11760`  ·  n_top_tier: `0.27426`  ·  corrupted: `-0.06318`  ·  n_sockets: `0.14861`  ·  quality: `0.16423`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | 2.72676 |
| `explicit.stat_587431675@T1` | 2.43955 |
| `explicit.stat_3981240776@T2` | -2.35465 |
| `explicit.stat_2162097452@T2` | -2.26169 |
| `explicit.stat_3981240776@T1` | -2.11904 |
| `explicit.stat_1671376347@T1` | 1.66264 |
| `explicit.stat_9187492` | 1.43693 |
| `explicit.stat_4220027924@T1` | -1.39672 |
| `explicit.stat_803737631@T1` | -1.28540 |
| `explicit.stat_124131830@T2` | 1.25543 |
| `explicit.stat_2162097452` | 1.21501 |
| `explicit.stat_3556824919@T1` | -1.05907 |

### accessory.ring — n=9469, R²=-1.9144

intercept: `2.3056`  ·  log_price: True  ·  ilvl: `-0.02463`  ·  n_mods: `0.04221`  ·  n_top_tier: `0.20365`  ·  corrupted: `0.32281`  ·  n_sockets: `3.87805`  ·  quality: `0.01424`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 6.17350 |
| `explicit.stat_707457662@T2` | 5.47596 |
| `explicit.stat_2557965901@T2` | 4.38717 |
| `explicit.stat_2557965901@T1` | 4.37206 |
| `explicit.stat_1573130764@T1` | -1.69171 |
| `explicit.stat_3299347043@T1` | -1.24538 |
| `explicit.stat_3695891184@T2` | -1.20409 |
| `explicit.stat_1379411836@T1` | -1.04902 |
| `explicit.stat_707457662` | -0.95358 |
| `explicit.stat_3962278098@T2` | -0.94622 |
| `implicit.stat_958696139` | 0.93347 |
| `explicit.stat_1379411836@T2` | -0.89725 |

### accessory.belt — n=9200, R²=-1.2589

intercept: `3.8554`  ·  log_price: True  ·  ilvl: `-0.04695`  ·  n_mods: `-0.02101`  ·  n_top_tier: `-0.07756`  ·  corrupted: `0.27425`  ·  n_sockets: `-0.11495`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.99173 |
| `explicit.stat_2923486259@T1` | 1.76877 |
| `explicit.stat_1836676211@T1` | 1.19943 |
| `explicit.stat_2923486259@T2` | 0.81965 |
| `explicit.stat_4220027924@T1` | 0.23291 |
| `explicit.stat_1671376347@T1` | 0.20851 |
| `explicit.stat_3372524247@T1` | 0.20064 |
| `explicit.stat_3585532255@T1` | 0.18026 |
| `explicit.stat_3585532255@T2` | 0.15222 |
| `pseudo.total_ele_res>=80` | 0.14058 |
| `explicit.stat_1570770415@T1` | 0.12684 |
| `explicit.stat_1412217137@T2` | 0.11576 |

### armour.chest — n=8942, R²=-1.3509

intercept: `4.0195`  ·  log_price: True  ·  ilvl: `-0.04962`  ·  n_mods: `-0.02543`  ·  n_top_tier: `0.60888`  ·  corrupted: `-0.04054`  ·  n_sockets: `-0.00030`  ·  quality: `0.01451`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 1.98774 |
| `implicit.stat_2251279027` | 1.78967 |
| `explicit.stat_3981240776@T1` | 1.47647 |
| `explicit.stat_4080418644@T2` | -0.73422 |
| `explicit.stat_3261801346@T2` | -0.73197 |
| `explicit.stat_4015621042@T2` | -0.72027 |
| `explicit.stat_2923486259@T1` | -0.71674 |
| `explicit.stat_4015621042@T1` | -0.70062 |
| `explicit.stat_3261801346@T1` | -0.69998 |
| `explicit.stat_3362812763@T1` | 0.69251 |
| `explicit.stat_2339757871@T1` | -0.68933 |
| `explicit.stat_3301100256@T2` | -0.67400 |

### armour.helmet — n=8855, R²=-1.3412

intercept: `4.3477`  ·  log_price: True  ·  ilvl: `-0.05506`  ·  n_mods: `-0.02927`  ·  n_top_tier: `0.80365`  ·  corrupted: `0.09428`  ·  n_sockets: `-0.00909`  ·  quality: `0.01734`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 5.53735 |
| `explicit.stat_2339757871@T1` | -2.66430 |
| `explicit.stat_3033371881@T1` | -0.92941 |
| `explicit.stat_803737631@T2` | -0.92697 |
| `explicit.stat_3325883026@T1` | -0.92482 |
| `explicit.stat_53045048@T1` | -0.92142 |
| `explicit.stat_3639275092@T1` | -0.91034 |
| `explicit.stat_4052037485@T2` | -0.89515 |
| `explicit.stat_3321629045@T2` | -0.88545 |
| `explicit.stat_4015621042@T2` | -0.87788 |
| `explicit.stat_3033371881@T2` | -0.87077 |
| `explicit.stat_53045048@T2` | -0.87053 |

### armour.boots — n=8296, R²=-1.0958

intercept: `4.0833`  ·  log_price: True  ·  ilvl: `-0.05060`  ·  n_mods: `-0.03077`  ·  n_top_tier: `0.48203`  ·  corrupted: `-0.03102`  ·  n_sockets: `0.01557`  ·  quality: `0.01923`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.70516 |
| `crafted.stat_3917489142@T1` | 1.32313 |
| `explicit.stat_4220027924@T1` | 1.00273 |
| `explicit.stat_2339757871@T1` | -0.86501 |
| `explicit.stat_3362812763@T1` | -0.62314 |
| `explicit.stat_3321629045@T1` | -0.61884 |
| `explicit.stat_99927264@T1` | -0.59897 |
| `explicit.stat_3362812763@T2` | -0.59830 |
| `explicit.stat_1062208444@T1` | -0.57578 |
| `explicit.stat_3033371881@T2` | -0.56620 |
| `explicit.stat_2160282525@T1` | -0.56182 |
| `explicit.stat_1062208444@T2` | -0.55702 |

### armour.gloves — n=8227, R²=-0.2095

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.14000`  ·  corrupted: `0.04148`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.65173 |
| `explicit.stat_4067062424@T1` | 1.27134 |
| `explicit.stat_124859000@T1` | 0.50582 |
| `desecrated.stat_3032590688` | 0.16497 |
| `explicit.stat_2339757871@T1` | -0.14023 |
| `explicit.stat_4052037485@T1` | -0.14005 |
| `explicit.stat_1671376347@T1` | -0.14004 |
| `explicit.stat_4015621042@T1` | -0.14004 |
| `explicit.stat_3362812763@T1` | -0.14003 |
| `explicit.stat_2797971005@T2` | -0.14002 |
| `explicit.stat_3484657501@T2` | -0.14002 |
| `explicit.stat_3917489142@T2` | -0.14002 |

### jewel — n=7675, R²=-0.9619

intercept: `-1.4291`  ·  log_price: True  ·  ilvl: `0.03668`  ·  n_mods: `0.18091`  ·  n_top_tier: `-0.40677`  ·  corrupted: `0.59642`

| stat_id | coef |
|---|---|
| `explicit.stat_2301718443@T1` | -5.58326 |
| `explicit.stat_1569101201@T1` | 4.17036 |
| `explicit.stat_2456523742@T1` | 3.92783 |
| `explicit.stat_2011656677@T1` | 3.78692 |
| `explicit.stat_1869147066@T1` | 3.41916 |
| `explicit.stat_491450213@T1` | 3.20807 |
| `explicit.stat_1854213750@T1` | 3.07054 |
| `explicit.stat_3851254963@T1` | 2.90201 |
| `explicit.stat_3174700878@T1` | 2.64629 |
| `explicit.stat_1697447343@T1` | -2.52491 |
| `explicit.stat_1836676211@T1` | -2.44681 |
| `explicit.stat_1805182458@T1` | -2.41962 |

### weapon.wand — n=6295, R²=-1.6293

intercept: `3.4272`  ·  log_price: True  ·  ilvl: `-0.04237`  ·  n_mods: `-0.01644`  ·  n_top_tier: `0.61519`  ·  corrupted: `0.01296`  ·  n_sockets: `-0.00243`  ·  quality: `0.03063`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.48885 |
| `explicit.stat_1545858329@T1` | 1.71488 |
| `explicit.stat_4226189338@T1` | 1.67380 |
| `explicit.stat_2254480358@T1` | 1.63970 |
| `explicit.stat_591105508@T1` | 1.52366 |
| `explicit.stat_736967255@T2` | 1.25434 |
| `crafted.stat_124131830` | 1.09777 |
| `explicit.stat_1600707273@T2` | 1.06978 |
| `explicit.stat_3962278098@T2` | -0.74045 |
| `explicit.stat_293638271@T2` | -0.70488 |
| `explicit.stat_2768835289@T2` | -0.70075 |
| `explicit.stat_737908626@T1` | -0.66461 |

### weapon.bow — n=5327, R²=-1.5535

intercept: `3.4041`  ·  log_price: True  ·  ilvl: `-0.04209`  ·  n_mods: `-0.03217`  ·  n_top_tier: `0.34410`  ·  corrupted: `-0.03243`  ·  n_sockets: `0.00498`  ·  quality: `-0.00135`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -6.51318 |
| `explicit.stat_2463230181@T1` | 1.92442 |
| `explicit.stat_1509134228@T1` | 1.82203 |
| `explicit.stat_518292764@T1` | 1.79692 |
| `explicit.stat_1202301673@T1` | 1.52077 |
| `crafted.stat_3035140377` | 0.95779 |
| `desecrated.stat_210067635@T1` | 0.79662 |
| `rune.stat_3885405204` | -0.56542 |
| `explicit.stat_821021828@T1` | -0.56270 |
| `explicit.stat_821021828@T2` | -0.48660 |
| `explicit.stat_1263695895@T1` | -0.44536 |
| `explicit.stat_1940865751@T1` | -0.44067 |

### weapon.crossbow — n=5048, R²=-1.4407

intercept: `3.6004`  ·  log_price: True  ·  ilvl: `-0.04493`  ·  n_mods: `-0.00317`  ·  n_top_tier: `0.35398`  ·  corrupted: `-0.03011`  ·  n_sockets: `0.01807`  ·  quality: `-0.00427`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -3.32319 |
| `explicit.stat_2250681686` | 2.99846 |
| `explicit.stat_709508406@T1` | 2.55722 |
| `explicit.stat_3336890334@T1` | 1.91032 |
| `explicit.stat_1509134228@T1` | 1.89252 |
| `explicit.stat_1037193709@T1` | 1.89145 |
| `desecrated.stat_3131442032@T1` | -1.33456 |
| `desecrated.stat_1365232741@T1` | -1.33456 |
| `explicit.stat_691932474@T1` | -1.24324 |
| `explicit.stat_1202301673@T1` | 1.05846 |
| `crafted.stat_3035140377` | 0.88452 |
| `explicit.stat_1263695895@T1` | 0.71084 |

### weapon.sceptre — n=1326, R²=0.0

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

### weapon.warstaff — n=1231, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1037193709` | 0.00000 |
| `crafted.stat_1940865751` | 0.00000 |
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_1037193709` | 0.00000 |
| `desecrated.stat_1368271171` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_1940865751` | 0.00000 |
| `desecrated.stat_210067635` | 0.00000 |
| `desecrated.stat_2694482655` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |

### weapon.spear — n=1205, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1202301673@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |

### weapon.staff — n=1170, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_124131830` | 0.00000 |
| `crafted.stat_589361270` | 0.00000 |
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

### armour.focus — n=1002, R²=0.0

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

### flask.charm — n=952, R²=-0.5273

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2541588185@T2` | 0.24989 |
| `explicit.stat_1873752457` | 0.00014 |
| `explicit.stat_1120862500@T2` | -0.00007 |
| `explicit.stat_1873752457@T2` | -0.00003 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_828533480@T2` | -0.00003 |
| `explicit.stat_2566921799` | 0.00003 |
| `explicit.stat_388617051@T2` | -0.00003 |
| `explicit.stat_828533480@T1` | -0.00002 |
| `explicit.stat_2365392475@T2` | -0.00002 |
| `explicit.stat_3849649145` | -0.00002 |
| `implicit.stat_3676540188` | -0.00002 |

### armour.quiver — n=934, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1241625305` | 0.00000 |
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

### armour.shield — n=873, R²=0.0

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

### weapon.twomace — n=667, R²=0.0

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

- … **Emerald** — 3997 listings (3997 priced) [0.8–856.7 ex]
- … **Sapphire** — 3961 listings (3961 priced) [0.7–856.7 ex]
- … **Ruby** — 3209 listings (3209 priced) [0.3–856.7 ex]
- … **Utility Belt** — 2876 listings (2876 priced) [0.3–77723.4 ex]
- … **Stellar Amulet** — 2156 listings (2156 priced) [0.3–38371.8 ex]
- … **Dueling Wand** — 1981 listings (1981 priced) [1.0–856.7 ex]
- … **Solar Amulet** — 1794 listings (1794 priced) [1.0–856.7 ex]
- … **Gold Amulet** — 1770 listings (1770 priced) [0.6–856.7 ex]
- … **Prismatic Ring** — 1721 listings (1721 priced) [0.3–856.7 ex]
- … **Amethyst Ring** — 1632 listings (1632 priced) [0.8–856.7 ex]
- … **Gold Ring** — 1588 listings (1588 priced) [0.7–856.7 ex]
- … **Obliterator Bow** — 1494 listings (1494 priced) [0.9–856.7 ex]
- … **Plate Belt** — 1432 listings (1432 priced) [1.0–856.7 ex]
- … **Topaz Ring** — 1315 listings (1315 priced) [1.0–856.7 ex]
- … **Heavy Belt** — 1309 listings (1309 priced) [0.5–856.7 ex]
- … **Sapphire Ring** — 1283 listings (1283 priced) [0.9–856.7 ex]
- … **Ancestral Tiara** — 1263 listings (1263 priced) [1.0–856.7 ex]
- … **Ruby Ring** — 1246 listings (1246 priced) [0.8–856.7 ex]
- … **Lapis Amulet** — 1190 listings (1190 priced) [0.6–856.7 ex]
- … **Amber Amulet** — 1157 listings (1157 priced) [0.6–856.7 ex]
- … **Jade Amulet** — 1147 listings (1147 priced) [0.6–856.7 ex]
- … **Galvanic Wand** — 1131 listings (1131 priced) [0.8–856.7 ex]
- … **Siphoning Wand** — 1103 listings (1103 priced) [1.0–856.7 ex]
- … **Warmonger Bow** — 1069 listings (1069 priced) [1.0–856.7 ex]
- … **Attuned Wand** — 1050 listings (1050 priced) [0.3–856.7 ex]

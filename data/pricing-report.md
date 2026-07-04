# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-04T06:47:13+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **91650** (91650 priced in exalted)
- Distinct bases: 852 · distinct mods: 1979 · mod rows: 445823
- Sold signals: **19556** sold · 19046 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-04T06:42:33+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.64** (median |log error| 2.033)
- Within ±30% of asking price: **33%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 64% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.08** · typical error ×22.15 · ±30% 19% · n=12793
- Premium segment (60ex+): skill **+0.08** · typical error ×109.87 · ±30% 1% · n=7271
- Sold listings (clearing prices): skill **+0.05** · typical error ×24.62 · ±30% 25% · n=7650

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.amulet | 1498 | ×12.86 | 8% | -0.03 | -0.10 |
| accessory.belt | 1489 | ×9.18 | 27% | +0.03 | +0.06 |
| armour.chest | 1475 | ×10.00 | 42% | -0.01 | -0.05 |
| accessory.ring | 1452 | ×7.85 | 5% | -0.04 | -0.04 |
| armour.helmet | 1442 | ×10.00 | 37% | -0.03 | -0.09 |
| armour.gloves | 1320 | ×10.00 | 35% | -0.00 | -0.05 |
| armour.boots | 1283 | ×10.00 | 32% | -0.02 | -0.07 |
| other | 1156 | ×9.52 | 34% | +0.43 | +0.41 |
| weapon.wand | 1017 | ×8.22 | 36% | +0.05 | +0.11 |
| jewel | 928 | ×6.83 | 8% | +0.02 | +0.09 |
| weapon.bow | 906 | ×8.53 | 34% | +0.06 | +0.07 |
| weapon.crossbow | 870 | ×8.15 | 31% | +0.04 | +0.09 |
| weapon.sceptre | 238 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.spear | 213 | ×1.00 | 100% | n/a | - |
| armour.focus | 189 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.warstaff | 178 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.staff | 172 | ×1.00 | 95% | +0.00 | +0.00 |
| armour.shield | 165 | ×1.00 | 96% | +0.00 | +0.00 |
| armour.quiver | 144 | ×1.00 | 97% | +0.00 | +0.00 |
| weapon.twomace | 90 | ×1.00 | 97% | +0.00 | +0.00 |
| flask.charm | 69 | ×1.00 | 97% | -0.95 | -0.38 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=10724, R²=-0.1933

intercept: `1.5444`  ·  log_price: True  ·  ilvl: `0.00599`  ·  n_mods: `0.03398`  ·  n_top_tier: `0.10270`  ·  corrupted: `0.33567`  ·  n_sockets: `-0.14930`  ·  quality: `-0.01730`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830` | -0.59054 |
| `implicit.stat_718638445` | 0.51572 |
| `implicit.stat_3182714256` | 0.50986 |
| `explicit.stat_4052037485@T1` | -0.36011 |
| `implicit.stat_1379411836` | -0.29349 |
| `explicit.stat_3917489142@T1` | 0.25436 |
| `explicit.stat_2974417149@T1` | 0.22227 |
| `implicit.stat_4041853756` | 0.18608 |
| `implicit.stat_3879011313` | 0.18548 |
| `implicit.stat_958696139` | -0.16349 |
| `explicit.stat_1050105434@T1` | -0.15698 |
| `explicit.stat_1050105434@T2` | -0.14814 |

### accessory.belt — n=6963, R²=-1.257

intercept: `4.4594`  ·  log_price: True  ·  ilvl: `-0.05286`  ·  n_mods: `-0.03274`  ·  n_top_tier: `0.11375`  ·  corrupted: `0.07770`  ·  n_sockets: `-0.22689`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T2` | 1.26225 |
| `crafted.stat_3249412463` | 1.19040 |
| `explicit.stat_3299347043@T1` | -0.39706 |
| `explicit.stat_2923486259@T1` | 0.37987 |
| `implicit.stat_731781020` | -0.32800 |
| `explicit.stat_3299347043@T2` | -0.25260 |
| `explicit.stat_1389754388@T1` | -0.17897 |
| `explicit.stat_4080418644@T2` | -0.16776 |
| `explicit.stat_644456512@T2` | -0.15329 |
| `explicit.stat_2881298780@T1` | -0.14752 |
| `explicit.stat_1050105434@T1` | -0.14648 |
| `explicit.stat_809229260@T2` | -0.14629 |

### accessory.amulet — n=6940, R²=-2.4384

intercept: `5.0238`  ·  log_price: True  ·  ilvl: `-0.05586`  ·  n_mods: `-0.16425`  ·  n_top_tier: `0.32736`  ·  corrupted: `-0.28277`  ·  n_sockets: `-0.28101`  ·  quality: `0.66931`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -3.16146 |
| `explicit.stat_1202301673@T2` | 2.73599 |
| `explicit.stat_2923486259@T1` | -2.23889 |
| `explicit.stat_983749596@T2` | -2.14215 |
| `explicit.stat_2162097452@T2` | -2.12467 |
| `explicit.stat_9187492@T2` | -1.98908 |
| `explicit.stat_2923486259@T2` | -1.68632 |
| `explicit.stat_3299347043@T1` | -1.42668 |
| `explicit.stat_9187492` | 1.27092 |
| `explicit.stat_1671376347@T1` | 1.23354 |
| `explicit.stat_124131830` | 1.16501 |
| `explicit.stat_2162097452` | 1.15974 |

### accessory.ring — n=6822, R²=-1.9767

intercept: `4.9063`  ·  log_price: True  ·  ilvl: `-0.03495`  ·  n_mods: `-0.25007`  ·  n_top_tier: `0.70128`  ·  corrupted: `0.41955`  ·  n_sockets: `2.90371`  ·  quality: `0.05332`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 3.13298 |
| `explicit.stat_707457662@T2` | 2.56717 |
| `explicit.stat_1263695895@T2` | -2.56380 |
| `explicit.stat_1263695895@T1` | -2.46383 |
| `explicit.stat_3299347043@T1` | -1.92016 |
| `explicit.stat_1573130764@T1` | -1.67317 |
| `explicit.stat_1368271171@T1` | -1.60728 |
| `explicit.stat_2923486259@T2` | -1.47500 |
| `explicit.stat_1050105434@T2` | -1.35879 |
| `explicit.stat_1368271171@T2` | -1.30153 |
| `explicit.stat_1754445556@T2` | -1.25912 |
| `explicit.stat_1573130764@T2` | -1.21622 |

### armour.chest — n=6714, R²=-0.2924

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00064`  ·  corrupted: `0.00004`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3372524247` | -0.05124 |
| `desecrated.stat_4220027924` | -0.05121 |
| `implicit.stat_4220027924` | -0.05117 |
| `explicit.stat_1671376347` | -0.05117 |
| `pseudo.total_ele_res` | 0.05117 |
| `explicit.stat_3372524247` | -0.05117 |
| `explicit.stat_4220027924` | -0.05117 |
| `implicit.stat_3372524247` | -0.05117 |
| `rune.stat_4220027924` | -0.05117 |
| `rune.stat_1671376347` | -0.05117 |
| `implicit.stat_1671376347` | -0.05117 |
| `desecrated.stat_1671376347` | -0.05117 |

### armour.helmet — n=6695, R²=-0.2399

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.37928`  ·  corrupted: `0.00006`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 0.92884 |
| `explicit.stat_3321629045@T1` | -0.37931 |
| `explicit.stat_803737631@T2` | -0.37931 |
| `explicit.stat_3362812763@T2` | -0.37931 |
| `explicit.stat_803737631@T1` | -0.37930 |
| `explicit.stat_1062208444@T2` | -0.37930 |
| `explicit.stat_3484657501@T1` | -0.37930 |
| `explicit.stat_3362812763@T1` | -0.37930 |
| `explicit.stat_53045048@T2` | -0.37929 |
| `explicit.stat_2451402625@T1` | -0.37929 |
| `explicit.stat_3917489142@T2` | -0.37929 |
| `explicit.stat_328541901@T2` | -0.37929 |

### armour.boots — n=6135, R²=-0.1962

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.16665`  ·  corrupted: `0.00002`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_4080418644@T1` | -0.17222 |
| `explicit.stat_1062208444@T2` | -0.16694 |
| `explicit.stat_2339757871@T1` | -0.16679 |
| `explicit.stat_1062208444@T1` | -0.16669 |
| `explicit.stat_3484657501@T1` | -0.16669 |
| `explicit.stat_3261801346@T2` | -0.16669 |
| `explicit.stat_3639275092@T1` | -0.16669 |
| `explicit.stat_3362812763@T2` | -0.16668 |
| `explicit.stat_3484657501@T2` | -0.16668 |
| `explicit.stat_124859000@T2` | -0.16668 |
| `explicit.stat_3033371881@T2` | -0.16667 |
| `explicit.stat_3321629045@T2` | -0.16667 |

### armour.gloves — n=6103, R²=-0.2495

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00014`  ·  corrupted: `0.00003`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.19442 |
| `desecrated.stat_3299347043` | 0.01067 |
| `rune.stat_3299347043` | -0.00104 |
| `explicit.stat_3299347043` | -0.00104 |
| `pseudo.total_life` | 0.00104 |
| `explicit.stat_2339757871@T1` | -0.00070 |
| `explicit.stat_2923486259` | -0.00032 |
| `pseudo.total_chaos_res` | 0.00032 |
| `explicit.stat_4067062424@T1` | 0.00026 |
| `explicit.stat_4052037485@T1` | -0.00019 |
| `explicit.stat_3484657501@T2` | -0.00018 |
| `explicit.stat_4015621042@T1` | -0.00018 |

### weapon.wand — n=4900, R²=-1.5974

intercept: `3.3354`  ·  log_price: True  ·  ilvl: `-0.04157`  ·  n_mods: `-0.01253`  ·  n_top_tier: `0.07813`  ·  corrupted: `0.03256`  ·  n_sockets: `-0.00603`  ·  quality: `0.04631`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.28183 |
| `explicit.stat_1600707273@T1` | 2.26252 |
| `explicit.stat_1545858329@T1` | 2.19357 |
| `explicit.stat_736967255@T2` | 2.10819 |
| `explicit.stat_124131830@T1` | 2.04778 |
| `explicit.stat_1600707273@T2` | 1.74459 |
| `explicit.stat_4226189338@T1` | 1.42610 |
| `crafted.stat_124131830` | 1.24344 |
| `explicit.stat_124131830@T2` | -0.20971 |
| `explicit.stat_293638271@T2` | -0.16001 |
| `explicit.stat_2968503605@T2` | -0.15037 |
| `explicit.stat_473429811@T1` | -0.14677 |

### jewel — n=4609, R²=-1.0011

intercept: `-1.5666`  ·  log_price: True  ·  ilvl: `0.03806`  ·  n_mods: `0.18699`  ·  n_top_tier: `-0.50063`  ·  corrupted: `0.49433`

| stat_id | coef |
|---|---|
| `explicit.stat_2011656677@T1` | 7.01471 |
| `explicit.stat_1569101201@T1` | 5.89332 |
| `explicit.stat_274716455@T1` | -5.63730 |
| `explicit.stat_2456523742@T1` | 5.09761 |
| `explicit.stat_3851254963@T1` | 5.09319 |
| `explicit.stat_153777645@T1` | 4.88145 |
| `explicit.stat_2301718443@T1` | -4.70146 |
| `explicit.stat_293638271@T1` | -3.85802 |
| `explicit.stat_1459321413@T1` | 3.79518 |
| `explicit.stat_3741323227@T1` | 3.72748 |
| `explicit.stat_1805182458@T1` | -3.22366 |
| `explicit.stat_3377888098@T1` | -3.17951 |

### weapon.bow — n=4224, R²=-1.4668

intercept: `3.3467`  ·  log_price: True  ·  ilvl: `-0.04123`  ·  n_mods: `-0.02959`  ·  n_top_tier: `0.42447`  ·  corrupted: `0.06988`  ·  n_sockets: `0.01493`  ·  quality: `-0.00282`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -7.86522 |
| `explicit.stat_2463230181@T1` | 1.84031 |
| `explicit.stat_1509134228@T1` | 1.81250 |
| `explicit.stat_518292764@T1` | 1.69055 |
| `explicit.stat_1202301673@T1` | 1.49743 |
| `crafted.stat_3035140377` | 1.07898 |
| `desecrated.stat_210067635@T1` | -0.78393 |
| `explicit.stat_821021828@T1` | -0.64959 |
| `explicit.stat_821021828@T2` | -0.58782 |
| `explicit.stat_1263695895@T1` | -0.58541 |
| `explicit.stat_1940865751@T1` | -0.51667 |
| `explicit.stat_691932474@T2` | -0.48962 |

### weapon.crossbow — n=3974, R²=-1.4043

intercept: `3.4967`  ·  log_price: True  ·  ilvl: `-0.04414`  ·  n_mods: `0.00647`  ·  n_top_tier: `0.41443`  ·  corrupted: `0.01334`  ·  n_sockets: `0.03001`  ·  quality: `-0.01022`

| stat_id | coef |
|---|---|
| `desecrated.stat_1365232741@T1` | -2.24970 |
| `desecrated.stat_3131442032@T1` | -2.24970 |
| `explicit.stat_1037193709@T1` | 1.88934 |
| `explicit.stat_3336890334@T1` | 1.86789 |
| `explicit.stat_709508406@T1` | 1.84486 |
| `explicit.stat_691932474@T1` | -1.83845 |
| `explicit.stat_1509134228@T1` | 1.75228 |
| `explicit.stat_1263695895@T1` | 1.23671 |
| `crafted.stat_3035140377` | 0.92369 |
| `explicit.stat_1202301673@T1` | 0.54454 |
| `explicit.stat_1202301673@T2` | -0.50102 |
| `explicit.stat_1509134228@T2` | -0.47369 |

### weapon.sceptre — n=1155, R²=0.0

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

### weapon.spear — n=1023, R²=0.0

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

### weapon.warstaff — n=917, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_210067635` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |
| `desecrated.stat_387439868` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |

### armour.focus — n=903, R²=0.0

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

### weapon.staff — n=888, R²=0.0

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

### armour.shield — n=774, R²=0.0

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

### armour.quiver — n=759, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.00000 |
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

### flask.charm — n=747, R²=-0.422

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00018 |
| `explicit.stat_3196823591@T2` | -0.00009 |
| `explicit.stat_1873752457@T1` | -0.00008 |
| `explicit.stat_1120862500@T2` | -0.00006 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_828533480@T2` | -0.00004 |
| `explicit.stat_3849649145` | -0.00003 |
| `explicit.stat_828533480@T1` | -0.00002 |
| `explicit.stat_388617051@T2` | -0.00002 |
| `explicit.stat_2541588185@T2` | 0.00002 |
| `explicit.stat_1366840608@T2` | 0.00001 |
| `implicit.stat_3676540188` | -0.00001 |

### weapon.twomace — n=539, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

- … **Emerald** — 2551 listings (2551 priced) [0.5–856.7 ex]
- … **Sapphire** — 2440 listings (2440 priced) [0.3–856.7 ex]
- … **Utility Belt** — 2199 listings (2199 priced) [0.3–12851.0 ex]
- … **Ruby** — 1977 listings (1977 priced) [0.3–856.7 ex]
- … **Stellar Amulet** — 1637 listings (1637 priced) [0.3–37188.0 ex]
- … **Dueling Wand** — 1542 listings (1542 priced) [0.8–856.7 ex]
- … **Solar Amulet** — 1304 listings (1304 priced) [1.0–856.7 ex]
- … **Gold Amulet** — 1273 listings (1273 priced) [0.4–856.7 ex]
- … **Obliterator Bow** — 1218 listings (1218 priced) [0.4–856.7 ex]
- … **Prismatic Ring** — 1212 listings (1212 priced) [0.3–856.7 ex]
- … **Amethyst Ring** — 1169 listings (1169 priced) [0.8–856.7 ex]
- … **Gold Ring** — 1132 listings (1132 priced) [0.7–856.7 ex]
- … **Plate Belt** — 1074 listings (1074 priced) [1.0–856.7 ex]
- … **Heavy Belt** — 1000 listings (1000 priced) [0.5–856.7 ex]
- … **Ancestral Tiara** — 970 listings (970 priced) [1.0–856.7 ex]
- … **Sapphire Ring** — 949 listings (949 priced) [0.5–856.7 ex]
- … **Topaz Ring** — 944 listings (944 priced) [1.0–856.7 ex]
- … **Ruby Ring** — 904 listings (904 priced) [0.4–856.7 ex]
- … **Galvanic Wand** — 897 listings (897 priced) [1.0–856.7 ex]
- … **Lapis Amulet** — 882 listings (882 priced) [0.6–856.7 ex]
- … **Warmonger Bow** — 859 listings (859 priced) [0.9–856.7 ex]
- … **Siphoning Wand** — 853 listings (853 priced) [1.0–856.7 ex]
- … **Amber Amulet** — 846 listings (846 priced) [0.4–856.7 ex]
- … **Jade Amulet** — 845 listings (845 priced) [0.4–856.7 ex]
- … **Attuned Wand** — 824 listings (824 priced) [0.3–856.7 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-05T17:29:51+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **175351** (175351 priced in exalted)
- Distinct bases: 912 · distinct mods: 2413 · mod rows: 830400
- Sold signals: **40762** sold · 92350 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-05T17:22:24+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.16** (median |log error| 1.968)
- Within ±30% of asking price: **26%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 68% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×29.47 · ±30% 6% · n=22641
- Premium segment (60ex+): skill **+0.13** · typical error ×165.47 · ±30% 0% · n=12817
- Sold listings (clearing prices): skill **-0.01** · typical error ×24.26 · ±30% 28% · n=6647

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 3237 | ×7.40 | 5% | +0.02 | +0.03 |
| accessory.amulet | 3129 | ×7.92 | 5% | +0.02 | +0.02 |
| accessory.belt | 2789 | ×9.53 | 26% | +0.05 | +0.08 |
| jewel | 2786 | ×7.69 | 7% | +0.00 | +0.05 |
| armour.chest | 2677 | ×9.18 | 26% | +0.03 | +0.09 |
| armour.helmet | 2647 | ×9.00 | 22% | +0.03 | +0.09 |
| armour.boots | 2483 | ×9.00 | 25% | +0.03 | +0.09 |
| other | 2436 | ×6.66 | 35% | +0.17 | +0.26 |
| armour.gloves | 2414 | ×8.87 | 25% | +0.02 | +0.07 |
| weapon.wand | 1741 | ×9.20 | 32% | +0.05 | +0.11 |
| weapon.bow | 1468 | ×8.97 | 33% | +0.05 | +0.08 |
| weapon.crossbow | 1374 | ×8.71 | 28% | +0.07 | +0.08 |
| weapon.warstaff | 359 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.sceptre | 343 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.staff | 315 | ×1.00 | 100% | n/a | - |
| weapon.spear | 314 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 244 | ×1.00 | 98% | +0.00 | +0.00 |
| armour.focus | 240 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.shield | 204 | ×1.00 | 99% | +0.00 | +0.00 |
| flask.charm | 188 | ×1.00 | 99% | -0.00 | +0.00 |
| weapon.twomace | 154 | ×1.00 | 97% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=21212, R²=-0.4663

intercept: `1.5743`  ·  log_price: True  ·  ilvl: `0.00154`  ·  n_mods: `0.03446`  ·  n_top_tier: `0.26799`  ·  corrupted: `0.34392`  ·  n_sockets: `-0.03657`  ·  quality: `-0.00362`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.42921 |
| `explicit.stat_1050105434@T1` | -0.39190 |
| `explicit.stat_2974417149@T1` | 0.34734 |
| `implicit.stat_1379411836` | -0.28690 |
| `explicit.stat_2106365538@T1` | 0.24870 |
| `explicit.stat_2891184298@T1` | 0.24297 |
| `explicit.stat_124131830` | -0.23491 |
| `implicit.stat_4041853756` | 0.21814 |
| `implicit.stat_3879011313` | 0.21799 |
| `implicit.stat_3182714256` | 0.19013 |
| `implicit.stat_718638445` | 0.19006 |
| `implicit.stat_958696139` | -0.12062 |

### accessory.ring — n=14894, R²=-1.5186

intercept: `4.8632`  ·  log_price: True  ·  ilvl: `-0.04245`  ·  n_mods: `-0.26767`  ·  n_top_tier: `0.00340`  ·  corrupted: `0.86719`  ·  n_sockets: `3.51589`  ·  quality: `0.01772`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 3.95164 |
| `explicit.stat_1379411836@T1` | -3.32187 |
| `explicit.stat_707457662@T2` | 2.68648 |
| `explicit.stat_1379411836@T2` | -2.13829 |
| `explicit.stat_3299347043@T1` | -1.96290 |
| `explicit.stat_1573130764@T1` | -1.28176 |
| `explicit.stat_1754445556@T1` | 1.14967 |
| `explicit.stat_3299347043@T2` | -0.95170 |
| `explicit.stat_736967255@T1` | 0.89333 |
| `explicit.stat_1368271171@T1` | -0.88675 |
| `explicit.stat_4067062424@T2` | 0.88265 |
| `explicit.stat_3032590688@T2` | 0.79778 |

### accessory.amulet — n=14395, R²=-1.3347

intercept: `4.2126`  ·  log_price: True  ·  ilvl: `-0.04024`  ·  n_mods: `-0.19682`  ·  n_top_tier: `0.56106`  ·  corrupted: `0.48187`  ·  n_sockets: `-0.81644`  ·  quality: `-0.09134`

| stat_id | coef |
|---|---|
| `explicit.stat_2748665614@T1` | -2.94284 |
| `explicit.stat_983749596@T1` | -2.41837 |
| `explicit.stat_983749596@T2` | -1.96062 |
| `explicit.stat_2748665614@T2` | -1.80403 |
| `explicit.stat_3556824919@T1` | -1.57295 |
| `explicit.stat_3299347043@T1` | -1.51909 |
| `explicit.stat_1671376347@T2` | -1.38735 |
| `explicit.stat_803737631@T1` | -1.34300 |
| `explicit.stat_4080418644@T2` | -1.31067 |
| `explicit.stat_4080418644@T1` | -1.25672 |
| `explicit.stat_3325883026@T1` | -1.24072 |
| `explicit.stat_1444556985@T1` | -1.18035 |

### jewel — n=13969, R²=-0.8038

intercept: `-1.2209`  ·  log_price: True  ·  ilvl: `0.03414`  ·  n_mods: `0.19082`  ·  n_top_tier: `-0.40109`  ·  corrupted: `0.41054`  ·  quality: `0.22398`

| stat_id | coef |
|---|---|
| `explicit.stat_1869147066@T1` | 4.77085 |
| `explicit.stat_1405298142@T1` | 4.17364 |
| `explicit.stat_153777645@T1` | 4.16200 |
| `explicit.stat_3714003708@T1` | -3.06260 |
| `explicit.stat_1569101201@T1` | 2.97783 |
| `explicit.stat_872504239@T1` | -2.81984 |
| `explicit.stat_3146310524@T1` | 2.70112 |
| `explicit.stat_1316278494@T1` | -2.64792 |
| `explicit.stat_1829102168@T1` | -2.57357 |
| `explicit.stat_3780644166@T1` | 2.57309 |
| `explicit.stat_3192728503@T1` | 2.54488 |
| `explicit.stat_3851254963@T1` | 2.50346 |

### accessory.belt — n=12638, R²=-1.239

intercept: `3.6997`  ·  log_price: True  ·  ilvl: `-0.04445`  ·  n_mods: `-0.02864`  ·  n_top_tier: `0.08949`  ·  corrupted: `0.34922`  ·  n_sockets: `-0.11926`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.64339 |
| `explicit.stat_2923486259@T1` | 0.80687 |
| `explicit.stat_3299347043@T1` | -0.46436 |
| `explicit.stat_1836676211@T1` | 0.36029 |
| `explicit.stat_3299347043@T2` | -0.32866 |
| `explicit.stat_2923486259@T2` | 0.23399 |
| `explicit.stat_4220027924@T1` | 0.21215 |
| `pseudo.total_ele_res>=80` | 0.13844 |
| `explicit.stat_1389754388@T1` | -0.13321 |
| `explicit.stat_809229260@T2` | -0.12955 |
| `explicit.stat_915769802@T1` | -0.11958 |
| `explicit.stat_2639966148` | 0.11748 |

### armour.chest — n=12339, R²=-1.3185

intercept: `4.1325`  ·  log_price: True  ·  ilvl: `-0.05104`  ·  n_mods: `-0.02207`  ·  n_top_tier: `0.45138`  ·  corrupted: `0.18543`  ·  n_sockets: `0.00066`  ·  quality: `0.01071`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.30772 |
| `explicit.stat_3981240776@T1` | 1.63118 |
| `explicit.stat_3981240776@T2` | 1.07596 |
| `explicit.stat_4015621042@T1` | -0.61000 |
| `explicit.stat_328541901@T1` | -0.54266 |
| `explicit.stat_4080418644@T2` | -0.54227 |
| `explicit.stat_4080418644@T1` | -0.54069 |
| `explicit.stat_4015621042@T2` | -0.53206 |
| `explicit.stat_2339757871@T1` | -0.52521 |
| `explicit.stat_1999113824@T1` | -0.51638 |
| `explicit.stat_915769802@T1` | -0.50910 |
| `explicit.stat_986397080@T2` | -0.50889 |

### armour.helmet — n=12151, R²=-1.3484

intercept: `4.6882`  ·  log_price: True  ·  ilvl: `-0.05860`  ·  n_mods: `-0.02248`  ·  n_top_tier: `0.54025`  ·  corrupted: `0.62667`  ·  n_sockets: `-0.01133`  ·  quality: `0.03155`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.76380 |
| `explicit.stat_2339757871@T1` | -1.77947 |
| `explicit.stat_3033371881@T1` | -0.65373 |
| `explicit.stat_2162097452@T2` | -0.64867 |
| `explicit.stat_1263695895@T1` | -0.64728 |
| `explicit.stat_3033371881@T2` | -0.63277 |
| `explicit.stat_4015621042@T2` | -0.62712 |
| `explicit.stat_53045048@T1` | -0.62530 |
| `explicit.stat_4052037485@T2` | -0.60490 |
| `explicit.stat_4015621042@T1` | -0.59628 |
| `explicit.stat_803737631@T2` | -0.59213 |
| `explicit.stat_53045048@T2` | -0.58151 |

### armour.boots — n=11396, R²=-1.1558

intercept: `4.0191`  ·  log_price: True  ·  ilvl: `-0.04962`  ·  n_mods: `-0.02739`  ·  n_top_tier: `0.18101`  ·  corrupted: `0.13382`  ·  n_sockets: `0.01719`  ·  quality: `0.02848`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 2.07503 |
| `explicit.stat_4220027924@T1` | 1.05950 |
| `desecrated.stat_2250533757@T2` | -0.61648 |
| `explicit.stat_2339757871@T1` | -0.58283 |
| `explicit.stat_3917489142@T2` | -0.31957 |
| `rune.stat_836936635` | -0.27355 |
| `explicit.stat_99927264@T1` | -0.26995 |
| `explicit.stat_3362812763@T1` | -0.26927 |
| `explicit.stat_2923486259@T2` | -0.26054 |
| `explicit.stat_1062208444@T2` | -0.24909 |
| `explicit.stat_2160282525@T1` | -0.24492 |
| `explicit.stat_3917489142@T1` | -0.24087 |

### armour.gloves — n=11261, R²=-1.4351

intercept: `3.9895`  ·  log_price: True  ·  ilvl: `-0.05064`  ·  n_mods: `0.00228`  ·  n_top_tier: `1.05546`  ·  corrupted: `-0.08090`  ·  n_sockets: `-0.00385`  ·  quality: `0.01077`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.01152 |
| `explicit.stat_681332047@T2` | -1.26274 |
| `explicit.stat_681332047@T1` | -1.22667 |
| `explicit.stat_9187492@T2` | -1.18360 |
| `explicit.stat_2797971005@T1` | -1.17464 |
| `explicit.stat_124859000@T1` | -1.16654 |
| `explicit.stat_3032590688@T1` | -1.14754 |
| `explicit.stat_1573130764@T1` | -1.14742 |
| `explicit.stat_2557965901@T1` | -1.13580 |
| `explicit.stat_803737631@T2` | -1.13206 |
| `explicit.stat_2557965901@T2` | -1.12955 |
| `explicit.stat_2797971005@T2` | -1.12738 |

### weapon.wand — n=8070, R²=-1.6871

intercept: `3.5485`  ·  log_price: True  ·  ilvl: `-0.04429`  ·  n_mods: `-0.01197`  ·  n_top_tier: `0.29017`  ·  corrupted: `0.00280`  ·  n_sockets: `-0.00407`  ·  quality: `0.01850`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.63207 |
| `explicit.stat_4226189338@T1` | 2.08916 |
| `explicit.stat_591105508@T1` | 2.08362 |
| `explicit.stat_1545858329@T1` | 2.00358 |
| `explicit.stat_2254480358@T1` | 1.98515 |
| `explicit.stat_1600707273@T1` | 1.93034 |
| `explicit.stat_736967255@T2` | 1.56724 |
| `explicit.stat_1600707273@T2` | 1.33174 |
| `crafted.stat_124131830` | 0.91028 |
| `explicit.stat_2768835289@T2` | -0.43476 |
| `rune.stat_3278136794` | 0.36531 |
| `explicit.stat_2254480358@T2` | -0.35378 |

### weapon.bow — n=6753, R²=-1.6164

intercept: `3.5126`  ·  log_price: True  ·  ilvl: `-0.04359`  ·  n_mods: `-0.01738`  ·  n_top_tier: `0.32268`  ·  corrupted: `-0.07706`  ·  n_sockets: `0.00208`  ·  quality: `0.00325`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.07018 |
| `desecrated.stat_666077204@T1` | -2.96040 |
| `explicit.stat_2463230181@T1` | 1.98302 |
| `explicit.stat_1202301673@T1` | 1.87955 |
| `explicit.stat_1509134228@T1` | 1.82733 |
| `explicit.stat_518292764@T1` | 1.64532 |
| `crafted.stat_3035140377` | 1.61941 |
| `rune.stat_3885405204` | -0.84765 |
| `explicit.stat_55876295@T1` | -0.43288 |
| `explicit.stat_55876295@T2` | -0.39582 |
| `explicit.stat_2694482655@T1` | -0.38929 |
| `explicit.stat_3261801346@T1` | -0.38626 |

### weapon.crossbow — n=6358, R²=-1.4689

intercept: `3.5749`  ·  log_price: True  ·  ilvl: `-0.04514`  ·  n_mods: `-0.00385`  ·  n_top_tier: `0.47673`  ·  corrupted: `0.01975`  ·  n_sockets: `0.00415`  ·  quality: `-0.00232`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 2.24096 |
| `explicit.stat_709508406@T1` | 1.74210 |
| `explicit.stat_1037193709@T1` | 1.73558 |
| `explicit.stat_1202301673@T1` | 1.59994 |
| `explicit.stat_2250681686@T2` | -1.45101 |
| `crafted.stat_3035140377` | 1.12666 |
| `explicit.stat_691932474@T1` | -1.04269 |
| `explicit.stat_2250681686` | 0.99877 |
| `rune.stat_55876295` | 0.68969 |
| `rune.stat_2246411426` | -0.68474 |
| `explicit.stat_1202301673@T2` | -0.60860 |
| `explicit.stat_669069897@T2` | -0.55899 |

### flask.charm — n=2127, R²=-0.1557

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00002 |
| `explicit.stat_2541588185@T2` | 0.00001 |
| `explicit.stat_2365392475@T2` | 0.00001 |
| `explicit.stat_3196823591@T2` | 0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `explicit.stat_1366840608@T2` | 0.00001 |
| `explicit.stat_828533480@T1` | 0.00001 |
| `explicit.stat_828533480@T2` | 0.00001 |
| `explicit.stat_388617051@T2` | 0.00001 |
| `explicit.stat_1873752457@T1` | 0.00000 |
| `explicit.stat_2676834156@T2` | 0.00000 |
| `explicit.stat_3849649145` | -0.00000 |

### weapon.warstaff — n=1638, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
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
| `desecrated.stat_3261801346` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |

### weapon.sceptre — n=1586, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1798257884` | 0.00000 |
| `desecrated.stat_1050105434` | 0.00000 |
| `desecrated.stat_3984865854` | 0.00000 |
| `explicit.stat_101878827` | 0.00000 |
| `explicit.stat_101878827@T1` | 0.00000 |
| `explicit.stat_101878827@T2` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_1250712710` | 0.00000 |
| `explicit.stat_1250712710@T1` | 0.00000 |
| `explicit.stat_1250712710@T2` | 0.00000 |

### weapon.staff — n=1549, R²=0.0

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

### weapon.spear — n=1427, R²=0.0

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

### armour.focus — n=1141, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1671376347` | 0.00000 |
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
| `explicit.stat_2231156303@T1` | 0.00000 |

### armour.quiver — n=1124, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1241625305` | 0.00000 |
| `desecrated.stat_3032590688` | 0.00000 |
| `desecrated.stat_3261801346` | 0.00000 |
| `desecrated.stat_3714003708` | 0.00000 |
| `desecrated.stat_681332047` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1241625305` | 0.00000 |
| `explicit.stat_1241625305@T1` | 0.00000 |
| `explicit.stat_1241625305@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | -0.00000 |

### armour.shield — n=991, R²=0.0

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

### weapon.twomace — n=810, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |
| `explicit.stat_1940865751` | 0.00000 |

## Coverage (listings per base)

- … **Emerald** — 6988 listings (6988 priced) [0.7–856.7 ex]
- … **Sapphire** — 6941 listings (6941 priced) [0.6–856.7 ex]
- … **Ruby** — 5447 listings (5447 priced) [0.3–856.7 ex]
- … **Utility Belt** — 3886 listings (3886 priced) [0.3–4555741.7 ex]
- … **Stellar Amulet** — 2968 listings (2968 priced) [0.3–70539.4 ex]
- … **Prismatic Ring** — 2653 listings (2653 priced) [0.3–856.7 ex]
- … **Solar Amulet** — 2601 listings (2601 priced) [1.0–856.7 ex]
- … **Gold Amulet** — 2600 listings (2600 priced) [0.7–856.7 ex]
- … **Amethyst Ring** — 2533 listings (2533 priced) [0.8–856.7 ex]
- … **Dueling Wand** — 2483 listings (2483 priced) [1.0–856.7 ex]
- … **Gold Ring** — 2453 listings (2453 priced) [0.5–856.7 ex]
- … **Topaz Ring** — 2013 listings (2013 priced) [1.0–856.7 ex]
- … **Sapphire Ring** — 2011 listings (2011 priced) [0.9–856.7 ex]
- … **Ruby Ring** — 1953 listings (1953 priced) [1.0–856.7 ex]
- … **Plate Belt** — 1940 listings (1940 priced) [1.0–856.7 ex]
- … **Obliterator Bow** — 1920 listings (1920 priced) [0.7–856.7 ex]
- … **Heavy Belt** — 1848 listings (1848 priced) [0.5–856.7 ex]
- … **Lapis Amulet** — 1783 listings (1783 priced) [0.6–856.7 ex]
- … **Amber Amulet** — 1749 listings (1749 priced) [0.7–856.7 ex]
- … **Jade Amulet** — 1741 listings (1741 priced) [0.7–856.7 ex]
- … **Ancestral Tiara** — 1716 listings (1716 priced) [1.0–856.7 ex]
- … **Unset Ring** — 1601 listings (1601 priced) [1.0–856.7 ex]
- … **Bloodstone Amulet** — 1560 listings (1560 priced) [1.0–856.7 ex]
- … **Pearl Ring** — 1526 listings (1526 priced) [0.7–856.7 ex]
- … **Lunar Amulet** — 1519 listings (1519 priced) [0.7–856.7 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-05T13:06:33+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **165351** (165351 priced in exalted)
- Distinct bases: 908 · distinct mods: 2380 · mod rows: 784804
- Sold signals: **38971** sold · 83321 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-05T12:59:08+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×8.09** (median |log error| 2.0909)
- Within ±30% of asking price: **28%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 67% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×32.13 · ±30% 6% · n=21421
- Premium segment (60ex+): skill **+0.12** · typical error ×177.68 · ±30% 0% · n=12086
- Sold listings (clearing prices): skill **+0.06** · typical error ×22.11 · ±30% 31% · n=6281

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 3058 | ×7.67 | 5% | +0.01 | +0.01 |
| accessory.amulet | 2906 | ×32.82 | 13% | -0.03 | -0.06 |
| accessory.belt | 2607 | ×9.76 | 28% | +0.02 | +0.05 |
| armour.chest | 2562 | ×8.75 | 25% | +0.02 | +0.09 |
| armour.helmet | 2502 | ×8.65 | 22% | +0.03 | +0.08 |
| jewel | 2483 | ×7.43 | 8% | +0.01 | +0.06 |
| armour.boots | 2315 | ×9.15 | 25% | +0.01 | +0.09 |
| armour.gloves | 2314 | ×8.88 | 25% | +0.03 | +0.06 |
| other | 2268 | ×5.76 | 35% | +0.38 | +0.45 |
| weapon.wand | 1673 | ×9.12 | 32% | +0.04 | +0.06 |
| weapon.bow | 1422 | ×8.76 | 33% | +0.07 | +0.10 |
| weapon.crossbow | 1309 | ×8.80 | 28% | +0.08 | +0.11 |
| weapon.warstaff | 329 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.sceptre | 325 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.staff | 306 | ×1.00 | 100% | n/a | - |
| weapon.spear | 296 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.focus | 240 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 235 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.shield | 206 | ×1.00 | 99% | +0.00 | +0.00 |
| flask.charm | 155 | ×1.00 | 99% | -0.00 | +0.00 |
| weapon.twomace | 155 | ×1.00 | 97% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=19977, R²=-0.4251

intercept: `1.5536`  ·  log_price: True  ·  ilvl: `0.00293`  ·  n_mods: `0.04055`  ·  n_top_tier: `0.21678`  ·  corrupted: `0.50527`  ·  n_sockets: `-0.06590`  ·  quality: `-0.00725`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.42577 |
| `explicit.stat_2974417149@T1` | 0.32216 |
| `implicit.stat_1379411836` | -0.30043 |
| `implicit.stat_3182714256` | 0.29726 |
| `implicit.stat_718638445` | 0.29712 |
| `explicit.stat_2891184298@T1` | 0.28104 |
| `explicit.stat_2106365538@T1` | 0.27847 |
| `explicit.stat_1050105434@T1` | -0.26604 |
| `implicit.stat_958696139` | -0.21553 |
| `implicit.stat_4041853756` | 0.20865 |
| `implicit.stat_3879011313` | 0.20836 |
| `explicit.stat_124131830` | -0.20148 |

### accessory.ring — n=13841, R²=-1.5623

intercept: `4.4291`  ·  log_price: True  ·  ilvl: `-0.04263`  ·  n_mods: `-0.21751`  ·  n_top_tier: `0.10914`  ·  corrupted: `0.85235`  ·  n_sockets: `3.43328`  ·  quality: `0.03434`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.20259 |
| `explicit.stat_707457662@T2` | 3.22028 |
| `explicit.stat_3299347043@T1` | -2.58024 |
| `explicit.stat_1379411836@T1` | -2.56766 |
| `explicit.stat_1263695895@T1` | -2.41644 |
| `explicit.stat_1263695895@T2` | -2.16575 |
| `explicit.stat_1573130764@T1` | -1.63788 |
| `explicit.stat_1379411836@T2` | -1.61938 |
| `explicit.stat_3299347043@T2` | -1.35724 |
| `explicit.stat_1368271171@T2` | -1.09347 |
| `explicit.stat_2891184298@T1` | -0.98077 |
| `explicit.stat_1754445556@T1` | 0.84757 |

### accessory.amulet — n=13464, R²=-2.1775

intercept: `4.0157`  ·  log_price: True  ·  ilvl: `-0.04932`  ·  n_mods: `-0.02588`  ·  n_top_tier: `0.94054`  ·  corrupted: `0.16688`  ·  n_sockets: `-0.05040`  ·  quality: `-0.02970`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T2` | -2.50011 |
| `explicit.stat_2748665614@T1` | -1.84591 |
| `explicit.stat_2748665614@T2` | -1.55990 |
| `explicit.stat_1202301673@T2` | 1.46300 |
| `explicit.stat_3261801346@T1` | -1.11444 |
| `explicit.stat_4080418644@T1` | -1.07205 |
| `explicit.stat_1379411836@T2` | -1.05266 |
| `explicit.stat_4080418644@T2` | -1.04511 |
| `explicit.stat_983749596@T2` | -1.04091 |
| `explicit.stat_124131830@T2` | 1.03871 |
| `explicit.stat_983749596@T1` | -1.03687 |
| `explicit.stat_1671376347@T2` | -1.02798 |

### jewel — n=12737, R²=-0.8276

intercept: `-1.4032`  ·  log_price: True  ·  ilvl: `0.03661`  ·  n_mods: `0.18519`  ·  n_top_tier: `-0.41593`  ·  corrupted: `0.40680`  ·  quality: `0.22369`

| stat_id | coef |
|---|---|
| `explicit.stat_1869147066@T1` | 4.40252 |
| `explicit.stat_1697951953@T1` | -3.24359 |
| `explicit.stat_3714003708@T1` | -3.18340 |
| `explicit.stat_3192728503@T1` | 3.14660 |
| `explicit.stat_3780644166@T1` | 2.98358 |
| `explicit.stat_1697447343@T1` | 2.97548 |
| `explicit.stat_2106365538@T1` | -2.52528 |
| `explicit.stat_1405298142@T1` | 2.52171 |
| `explicit.stat_3146310524@T1` | 2.40921 |
| `explicit.stat_3851254963@T1` | 2.37134 |
| `explicit.stat_1836676211@T1` | 2.34528 |
| `explicit.stat_1238227257@T1` | -2.32328 |

### accessory.belt — n=11964, R²=-1.2684

intercept: `3.7659`  ·  log_price: True  ·  ilvl: `-0.04552`  ·  n_mods: `-0.02530`  ·  n_top_tier: `0.09733`  ·  corrupted: `0.19753`  ·  n_sockets: `-0.18223`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.61382 |
| `explicit.stat_2923486259@T1` | 1.85998 |
| `explicit.stat_2923486259@T2` | 0.84565 |
| `explicit.stat_3299347043@T1` | -0.59323 |
| `explicit.stat_3299347043@T2` | -0.30999 |
| `explicit.stat_3372524247@T1` | 0.19903 |
| `explicit.stat_3325883026@T1` | -0.13575 |
| `explicit.stat_809229260@T2` | -0.13469 |
| `explicit.stat_2881298780@T1` | -0.13250 |
| `explicit.stat_1389754388@T1` | -0.12866 |
| `explicit.stat_915769802@T2` | -0.12089 |
| `explicit.stat_915769802@T1` | -0.11999 |

### armour.chest — n=11704, R²=-1.3323

intercept: `3.9551`  ·  log_price: True  ·  ilvl: `-0.04882`  ·  n_mods: `-0.01770`  ·  n_top_tier: `0.36841`  ·  corrupted: `0.23559`  ·  n_sockets: `-0.00261`  ·  quality: `0.00798`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.26170 |
| `explicit.stat_3981240776@T1` | 1.62692 |
| `explicit.stat_3981240776@T2` | 0.88467 |
| `explicit.stat_4015621042@T1` | -0.48541 |
| `explicit.stat_328541901@T1` | -0.48489 |
| `explicit.stat_4080418644@T2` | -0.45905 |
| `explicit.stat_2339757871@T1` | -0.44544 |
| `explicit.stat_3261801346@T2` | -0.44419 |
| `explicit.stat_2339757871@T2` | -0.44049 |
| `explicit.stat_4080418644@T1` | -0.43900 |
| `explicit.stat_986397080@T2` | -0.42427 |
| `explicit.stat_915769802@T1` | -0.42389 |

### armour.helmet — n=11543, R²=-1.3674

intercept: `4.5297`  ·  log_price: True  ·  ilvl: `-0.05662`  ·  n_mods: `-0.02581`  ·  n_top_tier: `0.62057`  ·  corrupted: `0.66616`  ·  n_sockets: `-0.01146`  ·  quality: `0.02817`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.37289 |
| `crafted.stat_3917489142@T1` | 1.47111 |
| `explicit.stat_53045048@T1` | -0.72305 |
| `explicit.stat_803737631@T2` | -0.70435 |
| `explicit.stat_3033371881@T1` | -0.69504 |
| `explicit.stat_3325883026@T1` | -0.69091 |
| `explicit.stat_3325883026@T2` | -0.68321 |
| `explicit.stat_53045048@T2` | -0.68139 |
| `explicit.stat_4015621042@T2` | -0.68074 |
| `explicit.stat_4052037485@T2` | -0.67536 |
| `explicit.stat_3033371881@T2` | -0.67223 |
| `explicit.stat_1062208444@T2` | -0.66050 |

### armour.boots — n=10783, R²=-1.1521

intercept: `4.0373`  ·  log_price: True  ·  ilvl: `-0.04984`  ·  n_mods: `-0.02928`  ·  n_top_tier: `0.22569`  ·  corrupted: `0.08963`  ·  n_sockets: `0.01401`  ·  quality: `0.01851`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 2.00612 |
| `desecrated.stat_2250533757@T2` | -1.02787 |
| `explicit.stat_2339757871@T1` | -0.73476 |
| `explicit.stat_4220027924@T1` | 0.59208 |
| `explicit.stat_3362812763@T1` | -0.32054 |
| `rune.stat_836936635` | -0.31168 |
| `explicit.stat_2923486259@T2` | -0.30615 |
| `explicit.stat_3917489142@T2` | -0.30600 |
| `explicit.stat_1062208444@T2` | -0.29357 |
| `explicit.stat_1671376347@T2` | -0.28885 |
| `explicit.stat_2160282525@T1` | -0.28755 |
| `explicit.stat_3033371881@T2` | -0.28610 |

### armour.gloves — n=10676, R²=-1.4002

intercept: `4.1632`  ·  log_price: True  ·  ilvl: `-0.05286`  ·  n_mods: `0.00507`  ·  n_top_tier: `1.09325`  ·  corrupted: `-0.09786`  ·  n_sockets: `-0.00299`  ·  quality: `0.01165`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.35482 |
| `explicit.stat_2797971005@T1` | -1.30421 |
| `explicit.stat_2797971005@T2` | -1.24967 |
| `explicit.stat_9187492@T2` | -1.22906 |
| `explicit.stat_124859000@T1` | -1.22160 |
| `explicit.stat_3032590688@T1` | -1.21119 |
| `explicit.stat_803737631@T2` | -1.18992 |
| `explicit.stat_803737631@T1` | -1.18947 |
| `explicit.stat_1573130764@T1` | -1.17044 |
| `explicit.stat_681332047@T2` | -1.16931 |
| `explicit.stat_3484657501@T2` | -1.16277 |
| `explicit.stat_1754445556@T2` | -1.16022 |

### weapon.wand — n=7738, R²=-1.6636

intercept: `3.5760`  ·  log_price: True  ·  ilvl: `-0.04469`  ·  n_mods: `-0.01282`  ·  n_top_tier: `0.30205`  ·  corrupted: `0.00248`  ·  n_sockets: `-0.00043`  ·  quality: `0.02215`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.53672 |
| `explicit.stat_591105508@T1` | 2.05952 |
| `explicit.stat_4226189338@T1` | 2.03033 |
| `explicit.stat_1545858329@T1` | 1.95697 |
| `explicit.stat_2254480358@T1` | 1.93811 |
| `explicit.stat_736967255@T2` | 1.55038 |
| `explicit.stat_1600707273@T2` | 1.39162 |
| `explicit.stat_1600707273@T1` | 1.28949 |
| `crafted.stat_124131830` | 0.89947 |
| `explicit.stat_2768835289@T2` | -0.41047 |
| `explicit.stat_737908626@T1` | -0.37613 |
| `explicit.stat_293638271@T2` | -0.37043 |

### weapon.bow — n=6476, R²=-1.5873

intercept: `3.4628`  ·  log_price: True  ·  ilvl: `-0.04291`  ·  n_mods: `-0.02087`  ·  n_top_tier: `0.38957`  ·  corrupted: `-0.06723`  ·  n_sockets: `0.00470`  ·  quality: `0.00064`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -3.56439 |
| `explicit.stat_2463230181@T1` | 1.91683 |
| `explicit.stat_1202301673@T1` | 1.79152 |
| `explicit.stat_1509134228@T1` | 1.72359 |
| `crafted.stat_3035140377` | 1.64135 |
| `explicit.stat_518292764@T1` | 1.56699 |
| `desecrated.stat_210067635@T1` | -1.45608 |
| `rune.stat_3885405204` | -0.78070 |
| `explicit.stat_3261801346@T1` | -0.47566 |
| `explicit.stat_55876295@T1` | -0.45815 |
| `explicit.stat_2694482655@T1` | -0.44857 |
| `explicit.stat_669069897@T2` | -0.44591 |

### weapon.crossbow — n=6146, R²=-1.4678

intercept: `3.4793`  ·  log_price: True  ·  ilvl: `-0.04414`  ·  n_mods: `0.00133`  ·  n_top_tier: `0.52590`  ·  corrupted: `0.01258`  ·  n_sockets: `0.01023`  ·  quality: `-0.00158`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 1.84404 |
| `explicit.stat_709508406@T1` | 1.73260 |
| `explicit.stat_1037193709@T1` | 1.66295 |
| `explicit.stat_1202301673@T1` | 1.56312 |
| `explicit.stat_2250681686@T2` | -1.48546 |
| `crafted.stat_3035140377` | 1.09665 |
| `explicit.stat_691932474@T1` | -1.07949 |
| `explicit.stat_2250681686` | 0.98775 |
| `rune.stat_2246411426` | -0.68081 |
| `rune.stat_55876295` | 0.66404 |
| `explicit.stat_1202301673@T2` | -0.63572 |
| `explicit.stat_669069897@T1` | -0.63214 |

### flask.charm — n=1899, R²=-0.1871

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_2541588185@T2` | 0.00002 |
| `explicit.stat_2365392475@T2` | 0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `explicit.stat_1366840608@T2` | 0.00001 |
| `explicit.stat_3196823591@T2` | 0.00001 |
| `explicit.stat_3849649145` | -0.00001 |
| `explicit.stat_828533480@T2` | 0.00000 |
| `implicit.stat_4010341289` | -0.00000 |
| `explicit.stat_828533480@T1` | 0.00000 |
| `explicit.stat_2676834156@T2` | 0.00000 |
| `implicit.stat_2016937536` | 0.00000 |

### weapon.warstaff — n=1556, R²=0.0

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

### weapon.sceptre — n=1535, R²=0.0

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

### weapon.staff — n=1471, R²=0.0

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

### weapon.spear — n=1383, R²=0.0

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

### armour.focus — n=1113, R²=0.0

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

### armour.quiver — n=1084, R²=0.0

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

### armour.shield — n=967, R²=0.0

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

### weapon.twomace — n=780, R²=0.0

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

- … **Emerald** — 6400 listings (6400 priced) [0.7–856.7 ex]
- … **Sapphire** — 6361 listings (6361 priced) [0.6–856.7 ex]
- … **Ruby** — 5036 listings (5036 priced) [0.3–856.7 ex]
- … **Utility Belt** — 3712 listings (3712 priced) [0.3–4555741.7 ex]
- … **Stellar Amulet** — 2803 listings (2803 priced) [0.3–72137.5 ex]
- … **Prismatic Ring** — 2485 listings (2485 priced) [0.3–856.7 ex]
- … **Gold Amulet** — 2465 listings (2465 priced) [0.7–856.7 ex]
- … **Solar Amulet** — 2445 listings (2445 priced) [1.0–856.7 ex]
- … **Dueling Wand** — 2383 listings (2383 priced) [1.0–856.7 ex]
- … **Amethyst Ring** — 2367 listings (2367 priced) [0.8–856.7 ex]
- … **Gold Ring** — 2274 listings (2274 priced) [0.5–856.7 ex]
- … **Topaz Ring** — 1878 listings (1878 priced) [1.0–856.7 ex]
- … **Sapphire Ring** — 1861 listings (1861 priced) [0.9–856.7 ex]
- … **Obliterator Bow** — 1846 listings (1846 priced) [0.6–856.7 ex]
- … **Plate Belt** — 1835 listings (1835 priced) [1.0–856.7 ex]
- … **Ruby Ring** — 1817 listings (1817 priced) [0.6–856.7 ex]
- … **Heavy Belt** — 1722 listings (1722 priced) [0.5–856.7 ex]
- … **Lapis Amulet** — 1675 listings (1675 priced) [0.6–856.7 ex]
- … **Amber Amulet** — 1628 listings (1628 priced) [0.7–856.7 ex]
- … **Ancestral Tiara** — 1617 listings (1617 priced) [1.0–856.7 ex]
- … **Jade Amulet** — 1615 listings (1615 priced) [0.7–856.7 ex]
- … **Unset Ring** — 1477 listings (1477 priced) [1.0–856.7 ex]
- … **Bloodstone Amulet** — 1458 listings (1458 priced) [1.0–856.7 ex]
- … **Lunar Amulet** — 1431 listings (1431 priced) [0.8–856.7 ex]
- … **Pearl Ring** — 1430 listings (1430 priced) [0.8–856.7 ex]

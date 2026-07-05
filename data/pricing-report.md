# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-05T19:49:21+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **181582** (181573 priced in exalted)
- Distinct bases: 916 · distinct mods: 2444 · mod rows: 860303
- Sold signals: **39911** sold · 96600 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-05T19:42:33+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×8.41** (median |log error| 2.1295)
- Within ±30% of asking price: **26%**
- Skill vs constant-price guess: **+0.02** (> 0 = the mods carry signal)
- Calibration: 69% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×36.16 · ±30% 6% · n=24129
- Premium segment (60ex+): skill **+0.11** · typical error ×204.94 · ±30% 0% · n=13929
- Sold listings (clearing prices): skill **-0.03** · typical error ×21.70 · ±30% 27% · n=5418

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 3413 | ×7.27 | 5% | +0.01 | +0.01 |
| accessory.amulet | 3276 | ×41.71 | 20% | -0.03 | -0.04 |
| jewel | 2848 | ×7.71 | 6% | +0.01 | +0.05 |
| accessory.belt | 2815 | ×9.49 | 25% | +0.03 | +0.09 |
| armour.chest | 2754 | ×9.20 | 26% | +0.03 | +0.09 |
| armour.helmet | 2727 | ×9.07 | 22% | +0.03 | +0.09 |
| armour.gloves | 2542 | ×9.00 | 24% | +0.01 | +0.07 |
| armour.boots | 2537 | ×9.20 | 25% | +0.03 | +0.09 |
| other | 2432 | ×6.45 | 37% | +0.07 | +0.16 |
| weapon.wand | 1815 | ×9.35 | 31% | +0.04 | +0.12 |
| weapon.bow | 1495 | ×9.05 | 32% | +0.06 | +0.09 |
| weapon.crossbow | 1376 | ×9.09 | 30% | +0.07 | +0.09 |
| weapon.warstaff | 374 | ×1.00 | 87% | +0.00 | +0.00 |
| weapon.sceptre | 356 | ×1.00 | 75% | +0.00 | +0.00 |
| weapon.staff | 351 | ×1.00 | 74% | +0.00 | +0.00 |
| weapon.spear | 323 | ×1.00 | 72% | +0.00 | +0.00 |
| armour.focus | 267 | ×1.00 | 66% | +0.00 | +0.00 |
| armour.quiver | 266 | ×1.00 | 64% | +0.00 | +0.00 |
| armour.shield | 230 | ×1.00 | 59% | +0.00 | +0.00 |
| flask.charm | 200 | ×1.00 | 81% | -0.00 | +0.00 |
| weapon.twomace | 194 | ×1.00 | 52% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=21812, R²=-0.4752

intercept: `1.5746`  ·  log_price: True  ·  ilvl: `0.00172`  ·  n_mods: `0.03418`  ·  n_top_tier: `0.26108`  ·  corrupted: `0.36243`  ·  n_sockets: `-0.04054`  ·  quality: `-0.00423`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.41751 |
| `explicit.stat_2974417149@T1` | 0.34274 |
| `explicit.stat_1050105434@T1` | -0.34105 |
| `implicit.stat_1379411836` | -0.28847 |
| `explicit.stat_2891184298@T1` | 0.26843 |
| `explicit.stat_2106365538@T1` | 0.26655 |
| `explicit.stat_124131830` | -0.25041 |
| `implicit.stat_4041853756` | 0.21675 |
| `implicit.stat_3879011313` | 0.21658 |
| `implicit.stat_3182714256` | 0.20349 |
| `implicit.stat_718638445` | 0.20342 |
| `implicit.stat_958696139` | -0.13504 |

### accessory.ring — n=15487, R²=-1.4806

intercept: `4.9217`  ·  log_price: True  ·  ilvl: `-0.04261`  ·  n_mods: `-0.23711`  ·  n_top_tier: `-0.18461`  ·  corrupted: `0.85343`  ·  n_sockets: `2.90562`  ·  quality: `0.00961`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 5.04729 |
| `explicit.stat_707457662@T2` | 3.55139 |
| `explicit.stat_1379411836@T1` | -3.06211 |
| `explicit.stat_1379411836@T2` | -1.85131 |
| `explicit.stat_1754445556@T1` | 1.43761 |
| `explicit.stat_3299347043@T1` | -1.26427 |
| `explicit.stat_3032590688@T2` | 1.18664 |
| `explicit.stat_2923486259@T2` | 1.06497 |
| `explicit.stat_736967255@T1` | 1.03397 |
| `explicit.stat_4067062424@T2` | 0.94372 |
| `explicit.stat_1754445556@T2` | 0.91094 |
| `explicit.stat_2923486259@T1` | 0.88583 |

### accessory.amulet — n=14945, R²=-2.168

intercept: `4.3182`  ·  log_price: True  ·  ilvl: `-0.05260`  ·  n_mods: `-0.02798`  ·  n_top_tier: `0.38748`  ·  corrupted: `0.10182`  ·  n_sockets: `-0.03170`  ·  quality: `-0.04108`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.31972 |
| `explicit.stat_3981240776@T2` | 1.23602 |
| `explicit.stat_2748665614@T1` | -1.17803 |
| `explicit.stat_124131830` | 1.17709 |
| `explicit.stat_983749596@T2` | -1.05235 |
| `explicit.stat_2748665614@T2` | -0.84805 |
| `explicit.stat_1202301673@T2` | 0.54732 |
| `explicit.stat_1671376347@T2` | -0.51567 |
| `explicit.stat_4080418644@T2` | -0.51135 |
| `explicit.stat_4080418644@T1` | -0.50741 |
| `explicit.stat_3261801346@T1` | -0.48459 |
| `explicit.stat_2482852589@T1` | -0.48295 |

### jewel — n=14363, R²=-0.7856

intercept: `-1.2722`  ·  log_price: True  ·  ilvl: `0.03474`  ·  n_mods: `0.22567`  ·  n_top_tier: `-0.42955`  ·  corrupted: `0.37562`  ·  quality: `0.22414`

| stat_id | coef |
|---|---|
| `explicit.stat_1869147066@T1` | 5.36041 |
| `explicit.stat_153777645@T1` | 4.43111 |
| `explicit.stat_1405298142@T1` | 3.98846 |
| `explicit.stat_3714003708@T1` | -3.35586 |
| `explicit.stat_1569101201@T1` | 3.05063 |
| `explicit.stat_1316278494@T1` | -2.78859 |
| `explicit.stat_1829102168@T1` | -2.68206 |
| `explicit.stat_3192728503@T1` | 2.55519 |
| `explicit.stat_3146310524@T1` | 2.53611 |
| `explicit.stat_2106365538@T1` | -2.45083 |
| `explicit.stat_3780644166@T1` | 2.40847 |
| `explicit.stat_3473929743@T1` | 2.37236 |

### accessory.belt — n=13033, R²=-1.3

intercept: `3.5553`  ·  log_price: True  ·  ilvl: `-0.04270`  ·  n_mods: `-0.02547`  ·  n_top_tier: `-0.00067`  ·  corrupted: `0.18421`  ·  n_sockets: `-0.11083`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.83147 |
| `explicit.stat_2923486259@T1` | 1.04286 |
| `explicit.stat_1836676211@T1` | 0.38628 |
| `explicit.stat_2923486259@T2` | 0.37355 |
| `explicit.stat_3299347043@T1` | -0.29022 |
| `explicit.stat_3299347043@T2` | -0.15679 |
| `explicit.stat_4220027924@T1` | 0.14904 |
| `explicit.stat_3372524247@T1` | 0.13171 |
| `explicit.stat_2639966148` | 0.10037 |
| `implicit.stat_731781020` | -0.08696 |
| `explicit.stat_174664100` | 0.07735 |
| `pseudo.total_ele_res>=80` | 0.06972 |

### armour.chest — n=12761, R²=-1.3413

intercept: `4.0181`  ·  log_price: True  ·  ilvl: `-0.04967`  ·  n_mods: `-0.01960`  ·  n_top_tier: `0.33357`  ·  corrupted: `0.13101`  ·  n_sockets: `0.00261`  ·  quality: `0.00713`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.29468 |
| `explicit.stat_3981240776@T1` | 1.78075 |
| `explicit.stat_3981240776@T2` | 1.02090 |
| `explicit.stat_4015621042@T1` | -0.48494 |
| `explicit.stat_4015621042@T2` | -0.42295 |
| `explicit.stat_328541901@T1` | -0.42120 |
| `explicit.stat_4080418644@T2` | -0.40973 |
| `explicit.stat_4080418644@T1` | -0.40424 |
| `explicit.stat_1999113824@T1` | -0.39523 |
| `explicit.stat_915769802@T1` | -0.39210 |
| `explicit.stat_986397080@T2` | -0.38915 |
| `explicit.stat_3261801346@T2` | -0.38239 |

### armour.helmet — n=12558, R²=-1.3533

intercept: `4.5700`  ·  log_price: True  ·  ilvl: `-0.05712`  ·  n_mods: `-0.02208`  ·  n_top_tier: `0.53808`  ·  corrupted: `0.48029`  ·  n_sockets: `-0.01538`  ·  quality: `0.02939`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.11392 |
| `explicit.stat_2339757871@T1` | -2.88858 |
| `explicit.stat_53045048@T1` | -0.65870 |
| `explicit.stat_3033371881@T1` | -0.63379 |
| `explicit.stat_2162097452@T2` | -0.63103 |
| `explicit.stat_3033371881@T2` | -0.62712 |
| `explicit.stat_4015621042@T2` | -0.62671 |
| `explicit.stat_1263695895@T1` | -0.62467 |
| `explicit.stat_53045048@T2` | -0.60043 |
| `explicit.stat_4015621042@T1` | -0.59983 |
| `explicit.stat_4052037485@T2` | -0.59758 |
| `explicit.stat_1062208444@T2` | -0.59045 |

### armour.boots — n=11778, R²=-1.1655

intercept: `4.0021`  ·  log_price: True  ·  ilvl: `-0.04941`  ·  n_mods: `-0.02667`  ·  n_top_tier: `0.25816`  ·  corrupted: `0.21471`  ·  n_sockets: `0.01531`  ·  quality: `0.04303`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.98282 |
| `explicit.stat_2339757871@T1` | -1.49591 |
| `explicit.stat_4220027924@T1` | 0.86482 |
| `explicit.stat_3917489142@T2` | -0.39410 |
| `rune.stat_836936635` | -0.36579 |
| `explicit.stat_3362812763@T1` | -0.34776 |
| `explicit.stat_99927264@T1` | -0.33724 |
| `explicit.stat_2923486259@T2` | -0.33508 |
| `explicit.stat_3321629045@T1` | -0.33133 |
| `explicit.stat_4015621042@T2` | -0.33017 |
| `explicit.stat_1062208444@T2` | -0.32978 |
| `explicit.stat_1671376347@T2` | -0.32015 |

### armour.gloves — n=11618, R²=-1.4534

intercept: `3.9287`  ·  log_price: True  ·  ilvl: `-0.04996`  ·  n_mods: `0.00435`  ·  n_top_tier: `1.09644`  ·  corrupted: `-0.07608`  ·  n_sockets: `-0.00480`  ·  quality: `0.01136`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.00787 |
| `explicit.stat_681332047@T2` | -1.41952 |
| `explicit.stat_681332047@T1` | -1.41664 |
| `explicit.stat_2797971005@T1` | -1.24427 |
| `explicit.stat_9187492@T2` | -1.22101 |
| `explicit.stat_1573130764@T1` | -1.21399 |
| `explicit.stat_124859000@T1` | -1.19642 |
| `explicit.stat_2797971005@T2` | -1.18394 |
| `explicit.stat_3032590688@T1` | -1.18311 |
| `explicit.stat_2557965901@T1` | -1.17655 |
| `explicit.stat_803737631@T2` | -1.17021 |
| `explicit.stat_3484657501@T2` | -1.16927 |

### weapon.wand — n=8317, R²=-1.7109

intercept: `3.4490`  ·  log_price: True  ·  ilvl: `-0.04301`  ·  n_mods: `-0.01049`  ·  n_top_tier: `0.60377`  ·  corrupted: `0.02363`  ·  n_sockets: `-0.00556`  ·  quality: `0.02003`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.79079 |
| `explicit.stat_591105508@T1` | 1.77440 |
| `explicit.stat_4226189338@T1` | 1.76778 |
| `explicit.stat_2254480358@T1` | 1.68238 |
| `explicit.stat_1600707273@T1` | 1.64269 |
| `explicit.stat_1545858329@T1` | 1.49366 |
| `explicit.stat_736967255@T2` | 1.30818 |
| `crafted.stat_124131830` | 0.81318 |
| `explicit.stat_2768835289@T2` | -0.74674 |
| `explicit.stat_1600707273@T2` | 0.73433 |
| `explicit.stat_3962278098@T2` | -0.70562 |
| `explicit.stat_737908626@T1` | -0.68091 |

### weapon.bow — n=6905, R²=-1.6583

intercept: `3.4918`  ·  log_price: True  ·  ilvl: `-0.04331`  ·  n_mods: `-0.01491`  ·  n_top_tier: `0.19078`  ·  corrupted: `-0.05089`  ·  n_sockets: `0.00343`  ·  quality: `0.00401`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.84985 |
| `desecrated.stat_210067635@T1` | -2.59239 |
| `explicit.stat_2463230181@T1` | 2.11301 |
| `explicit.stat_1202301673@T1` | 2.07918 |
| `explicit.stat_1509134228@T1` | 1.96474 |
| `crafted.stat_3035140377` | 1.65226 |
| `explicit.stat_518292764@T1` | 1.61080 |
| `rune.stat_3885405204` | -0.70219 |
| `desecrated.stat_666077204` | 0.30074 |
| `explicit.stat_55876295@T1` | -0.29199 |
| `explicit.stat_55876295@T2` | -0.25630 |
| `explicit.stat_2694482655@T1` | -0.25199 |

### weapon.crossbow — n=6500, R²=-1.5268

intercept: `3.5166`  ·  log_price: True  ·  ilvl: `-0.04410`  ·  n_mods: `-0.00128`  ·  n_top_tier: `0.39383`  ·  corrupted: `0.00024`  ·  n_sockets: `0.00255`  ·  quality: `-0.00050`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 2.33093 |
| `explicit.stat_709508406@T1` | 1.86225 |
| `explicit.stat_1037193709@T1` | 1.86192 |
| `explicit.stat_1202301673@T1` | 1.72403 |
| `explicit.stat_2250681686@T2` | -1.38696 |
| `crafted.stat_3035140377` | 1.16060 |
| `explicit.stat_2250681686` | 1.02486 |
| `explicit.stat_691932474@T1` | -0.92188 |
| `rune.stat_2246411426` | -0.63742 |
| `rune.stat_55876295` | 0.62660 |
| `explicit.stat_1202301673@T2` | -0.51498 |
| `explicit.stat_669069897@T1` | -0.46477 |

### flask.charm — n=2276, R²=-0.1931

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00002 |
| `explicit.stat_2541588185@T2` | 0.00001 |
| `explicit.stat_3849649145` | -0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `explicit.stat_1873752457@T2` | -0.00001 |
| `explicit.stat_3196823591@T2` | 0.00001 |
| `implicit.stat_4010341289` | -0.00000 |
| `explicit.stat_1366840608@T2` | 0.00000 |
| `explicit.stat_1509210032` | -0.00000 |
| `implicit.stat_3676540188` | -0.00000 |
| `implicit.stat_2016937536` | 0.00000 |
| `implicit.stat_1810482573` | -0.00000 |

### weapon.warstaff — n=1736, R²=0.0

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

### weapon.sceptre — n=1692, R²=-0.022

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T2` | -0.00001 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_3057012405@T1` | -0.00000 |
| `explicit.stat_3057012405@T2` | -0.00000 |
| `explicit.stat_1250712710@T1` | -0.00000 |
| `explicit.stat_289128254@T1` | -0.00000 |
| `explicit.stat_2162097452@T1` | -0.00000 |
| `explicit.stat_3984865854@T1` | -0.00000 |
| `explicit.stat_2854751904@T1` | -0.00000 |
| `explicit.stat_3639275092@T1` | -0.00000 |
| `explicit.stat_3984865854@T2` | -0.00000 |
| `explicit.stat_289128254@T2` | -0.00000 |

### weapon.staff — n=1656, R²=-0.0268

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T2` | 0.00001 |
| `explicit.stat_1263695895@T1` | 0.00001 |
| `explicit.stat_1263695895@T2` | 0.00001 |
| `explicit.stat_2254480358@T1` | 0.00001 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_2968503605@T2` | 0.00000 |
| `explicit.stat_473429811@T1` | -0.00000 |
| `explicit.stat_1545858329@T2` | 0.00000 |
| `explicit.stat_2231156303@T2` | -0.00000 |
| `explicit.stat_2891184298@T2` | 0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_3639275092@T2` | 0.00000 |

### weapon.spear — n=1528, R²=-0.0163

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T1` | -0.00001 |
| `explicit.stat_9187492@T2` | -0.00001 |
| `explicit.stat_1202301673@T1` | -0.00001 |
| `explicit.stat_669069897@T1` | -0.00000 |
| `explicit.stat_1202301673@T2` | -0.00000 |
| `explicit.stat_55876295@T2` | -0.00000 |
| `explicit.stat_3261801346@T2` | -0.00000 |
| `explicit.stat_669069897@T2` | -0.00000 |
| `explicit.stat_3639275092@T2` | -0.00000 |
| `explicit.stat_791928121@T2` | -0.00000 |
| `explicit.stat_748522257@T2` | -0.00000 |
| `explicit.stat_210067635@T2` | -0.00000 |

### armour.focus — n=1247, R²=-0.026

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_274716455@T1` | 0.00001 |
| `explicit.stat_3962278098@T2` | 0.00001 |
| `explicit.stat_3291658075@T1` | 0.00000 |
| `explicit.stat_4052037485@T2` | -0.00000 |
| `explicit.stat_3372524247@T1` | -0.00000 |
| `explicit.stat_124131830@T2` | -0.00000 |
| `explicit.stat_2231156303@T1` | -0.00000 |
| `explicit.stat_3962278098@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | -0.00000 |
| `explicit.stat_789117908@T2` | -0.00000 |
| `explicit.stat_2768835289@T2` | -0.00000 |
| `explicit.stat_2768835289@T1` | -0.00000 |

### armour.quiver — n=1225, R²=-0.0298

intercept: `-0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | -0.00001 |
| `explicit.stat_4067062424@T1` | 0.00001 |
| `explicit.stat_1754445556@T1` | 0.00001 |
| `explicit.stat_803737631@T1` | 0.00000 |
| `explicit.stat_3695891184@T2` | 0.00000 |
| `explicit.stat_3759663284@T2` | 0.00000 |
| `explicit.stat_4067062424@T2` | 0.00000 |
| `explicit.stat_1241625305@T2` | 0.00000 |
| `explicit.stat_3759663284@T1` | 0.00000 |
| `explicit.stat_3695891184@T1` | 0.00000 |
| `explicit.stat_681332047@T2` | 0.00000 |
| `explicit.stat_3261801346@T1` | 0.00000 |

### armour.shield — n=1090, R²=-0.0415

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00002`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_4095671657@T1` | 0.00003 |
| `explicit.stat_4095671657@T2` | 0.00003 |
| `explicit.stat_3676141501@T1` | 0.00003 |
| `explicit.stat_53045048@T1` | 0.00003 |
| `explicit.stat_3033371881@T2` | 0.00003 |
| `explicit.stat_3855016469@T2` | 0.00003 |
| `explicit.stat_3676141501@T2` | 0.00003 |
| `explicit.stat_4052037485@T2` | 0.00003 |
| `explicit.stat_53045048@T2` | 0.00003 |
| `explicit.stat_4052037485@T1` | 0.00003 |
| `explicit.stat_328541901@T1` | 0.00003 |
| `explicit.stat_328541901@T2` | 0.00002 |

### weapon.twomace — n=908, R²=-0.0511

intercept: `-0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_518292764@T1` | -0.00002 |
| `explicit.stat_210067635@T1` | -0.00002 |
| `explicit.stat_1037193709@T1` | -0.00002 |
| `explicit.stat_518292764@T2` | -0.00001 |
| `explicit.stat_691932474@T1` | -0.00001 |
| `explicit.stat_3639275092@T2` | -0.00001 |
| `explicit.stat_1940865751@T2` | -0.00001 |
| `explicit.stat_709508406@T1` | -0.00001 |
| `explicit.stat_669069897@T2` | -0.00001 |
| `explicit.stat_210067635@T2` | -0.00001 |
| `explicit.stat_9187492@T1` | -0.00001 |
| `explicit.stat_3639275092@T1` | -0.00001 |

## Coverage (listings per base)

- … **Emerald** — 7185 listings (7185 priced) [0.7–2153.0 ex]
- … **Sapphire** — 7145 listings (7145 priced) [0.6–3588.3 ex]
- … **Ruby** — 5598 listings (5598 priced) [0.3–7176.6 ex]
- … **Utility Belt** — 3983 listings (3983 priced) [0.3–4555741.7 ex]
- … **Stellar Amulet** — 3037 listings (3037 priced) [0.3–4547453.5 ex]
- … **Prismatic Ring** — 2755 listings (2755 priced) [0.3–856.7 ex]
- … **Solar Amulet** — 2708 listings (2708 priced) [1.0–4547453.5 ex]
- … **Gold Amulet** — 2706 listings (2706 priced) [0.7–3588.3 ex]
- … **Amethyst Ring** — 2632 listings (2632 priced) [0.8–856.7 ex]
- … **Dueling Wand** — 2562 listings (2562 priced) [1.0–21529.8 ex]
- … **Gold Ring** — 2536 listings (2536 priced) [0.5–856.7 ex]
- … **Sapphire Ring** — 2099 listings (2099 priced) [0.9–856.7 ex]
- … **Topaz Ring** — 2081 listings (2081 priced) [1.0–2153.0 ex]
- … **Ruby Ring** — 2020 listings (2020 priced) [1.0–856.7 ex]
- … **Plate Belt** — 1986 listings (1986 priced) [1.0–4547453.5 ex]
- … **Obliterator Bow** — 1965 listings (1965 priced) [0.6–330123.7 ex]
- … **Heavy Belt** — 1909 listings (1909 priced) [0.5–856.7 ex]
- … **Lapis Amulet** — 1834 listings (1834 priced) [0.6–4547453.5 ex]
- … **Amber Amulet** — 1816 listings (1816 priced) [0.7–4547453.5 ex]
- … **Jade Amulet** — 1811 listings (1811 priced) [0.7–4547453.5 ex]
- … **Ancestral Tiara** — 1772 listings (1771 priced) [1.0–7176.6 ex]
- … **Unset Ring** — 1677 listings (1677 priced) [1.0–856.7 ex]
- … **Bloodstone Amulet** — 1633 listings (1633 priced) [1.0–1435.3 ex]
- … **Pearl Ring** — 1591 listings (1591 priced) [0.6–7176.6 ex]
- … **Azure Amulet** — 1573 listings (1573 priced) [1.0–4306.0 ex]

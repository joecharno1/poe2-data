# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-03T07:41:34+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **40036** (40036 priced in exalted)
- Distinct bases: 726 · distinct mods: 1446 · mod rows: 203814
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-03T07:28:04+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×10.21** (median |log error| 2.3232)
- Within ±30% of asking price: **29%**
- Skill vs constant-price guess: **+0.23** (> 0 = the mods carry signal)
- Calibration: 63% of actuals above prediction (target ≈ 75%)

| group | n_test | ×err | ±30% | skill |
|---|---|---|---|---|
| accessory.belt | 633 | ×55.50 | 5% | +0.10 |
| armour.boots | 615 | ×7.95 | 6% | +0.49 |
| armour.helmet | 607 | ×10.53 | 43% | +0.00 |
| armour.gloves | 607 | ×12.27 | 6% | +0.40 |
| armour.chest | 601 | ×9.54 | 7% | +0.38 |
| accessory.amulet | 533 | ×10.05 | 30% | +0.05 |
| accessory.ring | 527 | ×40.32 | 18% | -0.00 |
| weapon.wand | 519 | ×9.04 | 29% | -0.01 |
| other | 437 | ×9.95 | 36% | +0.44 |
| weapon.bow | 394 | ×9.43 | 30% | -0.02 |
| weapon.crossbow | 379 | ×8.86 | 30% | -0.01 |
| jewel | 196 | ×25.97 | 4% | +0.18 |
| armour.focus | 146 | ×1.00 | 100% | n/a |
| weapon.sceptre | 143 | ×1.00 | 99% | +0.00 |
| weapon.spear | 128 | ×1.00 | 100% | n/a |
| armour.shield | 122 | ×1.00 | 100% | n/a |
| weapon.warstaff | 65 | ×1.00 | 100% | n/a |
| weapon.staff | 64 | ×1.00 | 100% | +0.00 |
| armour.quiver | 54 | ×1.00 | 100% | n/a |
| weapon.twomace | 30 | ×1.00 | 100% | n/a |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=3795, R²=0.1152

intercept: `1.5773`  ·  log_price: True  ·  ilvl: `0.00058`  ·  n_mods: `0.01748`  ·  n_top_tier: `0.32214`  ·  corrupted: `4.46879`  ·  n_sockets: `-0.00500`  ·  quality: `-0.00060`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.14887 |
| `explicit.stat_915769802@T1` | -0.80721 |
| `explicit.stat_4080418644@T1` | -0.66354 |
| `explicit.stat_1263695895@T1` | -0.63623 |
| `explicit.stat_124131830` | -0.57775 |
| `explicit.stat_4220027924@T1` | -0.56944 |
| `explicit.stat_4080418644@T2` | -0.56169 |
| `explicit.stat_4052037485@T1` | -0.53863 |
| `explicit.stat_2891184298@T1` | -0.49208 |
| `explicit.stat_3299347043@T2` | -0.48800 |
| `explicit.stat_4052037485@T2` | -0.47999 |
| `explicit.stat_789117908@T1` | 0.46517 |

### accessory.belt — n=3182, R²=-0.1249

intercept: `4.2386`  ·  log_price: True  ·  ilvl: `0.00354`  ·  n_mods: `-0.40446`  ·  n_top_tier: `0.89109`  ·  corrupted: `0.07676`

| stat_id | coef |
|---|---|
| `implicit.stat_731781020` | -5.11316 |
| `explicit.stat_3299347043@T1` | 2.50756 |
| `crafted.stat_3249412463` | 2.09886 |
| `explicit.stat_2923486259@T1` | -2.09458 |
| `explicit.stat_1389754388@T1` | -1.84170 |
| `explicit.stat_3299347043@T2` | 1.70717 |
| `explicit.stat_3372524247@T2` | -1.65128 |
| `explicit.stat_3585532255@T1` | 1.58782 |
| `explicit.stat_809229260@T1` | -1.36108 |
| `explicit.stat_3372524247@T1` | -1.23857 |
| `explicit.stat_644456512@T1` | -1.23734 |
| `explicit.stat_1836676211@T1` | -1.17311 |

### armour.helmet — n=3048, R²=-0.1252

intercept: `3.2056`  ·  log_price: True  ·  ilvl: `-0.01527`  ·  n_mods: `-0.07219`  ·  n_top_tier: `0.41759`  ·  corrupted: `0.68471`  ·  n_sockets: `-0.02371`  ·  quality: `-0.00389`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T2` | 5.39617 |
| `explicit.stat_1263695895@T1` | 4.67464 |
| `crafted.stat_3917489142@T1` | -3.62408 |
| `desecrated.stat_3299347043@T2` | 2.96089 |
| `desecrated.stat_4015621042@T1` | -2.30806 |
| `explicit.stat_4080418644@T2` | 2.09788 |
| `explicit.stat_3033371881@T2` | -1.91105 |
| `explicit.stat_3325883026@T2` | -1.71887 |
| `explicit.stat_4080418644@T1` | 1.66591 |
| `explicit.stat_1050105434@T2` | -1.44958 |
| `explicit.stat_3639275092@T2` | -1.39226 |
| `explicit.stat_2923486259@T2` | -1.35760 |

### armour.chest — n=3045, R²=-0.159

intercept: `3.1165`  ·  log_price: True  ·  ilvl: `-0.02795`  ·  n_mods: `-0.07062`  ·  n_top_tier: `-0.04366`  ·  corrupted: `1.30627`  ·  n_sockets: `-0.28201`  ·  quality: `-0.09682`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.48806 |
| `explicit.stat_4080418644@T1` | 2.22852 |
| `explicit.stat_3362812763@T2` | -2.02743 |
| `explicit.stat_2339757871@T1` | -1.92602 |
| `explicit.stat_1999113824@T1` | 1.64865 |
| `explicit.stat_3325883026@T1` | -1.61742 |
| `rune.stat_836936635` | 1.55232 |
| `explicit.stat_986397080@T1` | 1.54747 |
| `implicit.stat_1978899297` | -1.48721 |
| `explicit.stat_2881298780@T1` | -1.45619 |
| `explicit.stat_1692879867@T1` | 1.28699 |
| `explicit.stat_2339757871@T2` | -1.19505 |

### armour.boots — n=2973, R²=-0.0774

intercept: `6.9058`  ·  log_price: True  ·  ilvl: `-0.06735`  ·  n_mods: `-0.07139`  ·  n_top_tier: `0.56642`  ·  corrupted: `1.07156`  ·  n_sockets: `0.07580`  ·  quality: `-0.03483`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 4.34546 |
| `explicit.stat_2339757871@T1` | 3.46146 |
| `explicit.stat_2923486259@T1` | 3.05705 |
| `explicit.stat_3484657501@T2` | -2.49388 |
| `explicit.stat_3325883026@T1` | 2.48537 |
| `explicit.stat_3362812763@T2` | -1.76961 |
| `explicit.stat_53045048@T2` | -1.67296 |
| `explicit.stat_3261801346@T1` | -1.58243 |
| `explicit.stat_4080418644@T1` | -1.53089 |
| `explicit.stat_3325883026@T2` | 1.38891 |
| `explicit.stat_1874553720@T1` | -1.36770 |
| `explicit.stat_3033371881@T1` | -1.31238 |

### armour.gloves — n=2874, R²=-0.2546

intercept: `3.9435`  ·  log_price: True  ·  ilvl: `-0.03729`  ·  n_mods: `-0.12246`  ·  n_top_tier: `0.71950`  ·  corrupted: `0.09359`  ·  n_sockets: `-0.29022`  ·  quality: `0.03311`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -3.57928 |
| `explicit.stat_3917489142@T2` | -3.09295 |
| `explicit.stat_2339757871@T1` | 2.68256 |
| `explicit.stat_1062208444@T2` | 2.23059 |
| `explicit.stat_4220027924@T1` | -2.16976 |
| `explicit.stat_3639275092@T1` | -1.99084 |
| `explicit.stat_2923486259@T2` | -1.97049 |
| `explicit.stat_2557965901@T2` | -1.76278 |
| `explicit.stat_3484657501@T2` | -1.67374 |
| `explicit.stat_1368271171@T2` | -1.65843 |
| `explicit.stat_681332047@T2` | -1.63364 |
| `rune.stat_201332984` | 1.62873 |

### accessory.amulet — n=2694, R²=-2.026

intercept: `5.9761`  ·  log_price: True  ·  ilvl: `-0.06484`  ·  n_mods: `-0.36463`  ·  n_top_tier: `0.70108`  ·  corrupted: `0.21712`  ·  n_sockets: `0.19425`

| stat_id | coef |
|---|---|
| `explicit.stat_4220027924@T1` | 3.57487 |
| `explicit.stat_1444556985@T1` | 2.84641 |
| `explicit.stat_2923486259@T1` | -2.60323 |
| `explicit.stat_1202301673@T2` | 2.35699 |
| `explicit.stat_124131830@T2` | -2.33358 |
| `explicit.stat_328541901@T1` | -2.31430 |
| `explicit.stat_2923486259@T2` | -2.23963 |
| `explicit.stat_9187492@T2` | -2.01567 |
| `explicit.stat_124131830` | 1.73735 |
| `explicit.stat_1671376347@T2` | -1.72167 |
| `explicit.stat_4080418644@T1` | -1.71696 |
| `explicit.stat_3372524247@T1` | 1.67980 |

### accessory.ring — n=2503, R²=-2.755

intercept: `8.8655`  ·  log_price: True  ·  ilvl: `-0.07925`  ·  n_mods: `-0.42348`  ·  n_top_tier: `0.52487`  ·  corrupted: `0.09454`  ·  n_sockets: `2.85007`  ·  quality: `0.32021`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -3.73089 |
| `explicit.stat_3291658075@T2` | 2.22032 |
| `explicit.stat_4067062424@T1` | -2.17552 |
| `explicit.stat_2144192055@T2` | -2.13394 |
| `explicit.stat_3299347043@T2` | -1.97237 |
| `explicit.stat_1263695895@T2` | -1.95967 |
| `explicit.stat_1754445556@T1` | 1.81782 |
| `explicit.stat_1368271171@T1` | -1.81352 |
| `explicit.stat_1263695895@T1` | -1.74073 |
| `explicit.stat_1671376347@T1` | 1.71887 |
| `explicit.stat_1379411836@T1` | -1.71066 |
| `explicit.stat_2144192055@T1` | -1.62203 |

### weapon.wand — n=2466, R²=-1.2927

intercept: `3.3139`  ·  log_price: True  ·  ilvl: `-0.04165`  ·  n_mods: `-0.00902`  ·  n_top_tier: `0.29036`  ·  corrupted: `-0.08811`  ·  n_sockets: `0.04300`  ·  quality: `0.20841`

| stat_id | coef |
|---|---|
| `explicit.stat_1600707273@T1` | 3.97949 |
| `explicit.stat_124131830@T1` | 3.15640 |
| `explicit.stat_2254480358@T2` | -2.44562 |
| `explicit.stat_591105508@T1` | 2.19239 |
| `explicit.stat_4226189338@T1` | 2.05829 |
| `explicit.stat_2974417149@T1` | 1.88585 |
| `explicit.stat_2231156303@T2` | 1.78392 |
| `explicit.stat_2968503605@T1` | 1.78205 |
| `explicit.stat_2254480358@T1` | 1.37093 |
| `crafted.stat_124131830` | 0.82998 |
| `explicit.stat_124131830@T2` | 0.78237 |
| `rune.stat_124131830` | 0.65619 |

### weapon.bow — n=2110, R²=-1.1417

intercept: `2.9571`  ·  log_price: True  ·  ilvl: `-0.03668`  ·  n_mods: `-0.01490`  ·  n_top_tier: `0.08129`  ·  corrupted: `0.61478`  ·  n_sockets: `0.07241`  ·  quality: `-0.00109`

| stat_id | coef |
|---|---|
| `desecrated.stat_1200678966@T1` | -8.36774 |
| `desecrated.stat_210067635@T1` | 4.42706 |
| `desecrated.stat_666077204@T1` | -3.56148 |
| `rune.stat_3885405204` | -2.47987 |
| `explicit.stat_1202301673@T1` | 2.15623 |
| `explicit.stat_518292764@T1` | 2.08809 |
| `crafted.stat_3035140377` | 1.80620 |
| `explicit.stat_1037193709@T1` | 1.39874 |
| `explicit.stat_1509134228@T1` | 1.26502 |
| `explicit.stat_821021828@T1` | -1.01334 |
| `desecrated.stat_518292764` | 0.81411 |
| `explicit.stat_821021828@T2` | -0.77452 |

### weapon.crossbow — n=2026, R²=-1.0681

intercept: `4.7745`  ·  log_price: True  ·  ilvl: `-0.06052`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.65236`  ·  corrupted: `-0.10889`  ·  n_sockets: `0.27175`  ·  quality: `-0.06911`

| stat_id | coef |
|---|---|
| `explicit.stat_709508406@T1` | 3.09823 |
| `desecrated.stat_1365232741@T1` | 2.01773 |
| `desecrated.stat_3131442032@T1` | 2.01773 |
| `explicit.stat_1037193709@T1` | 1.81492 |
| `explicit.stat_3336890334@T1` | 1.76128 |
| `explicit.stat_691932474@T1` | -1.54323 |
| `explicit.stat_1037193709@T2` | 1.20612 |
| `explicit.stat_1263695895@T2` | -1.16485 |
| `explicit.stat_4080418644@T2` | 0.99407 |
| `crafted.stat_210067635@T2` | -0.96792 |
| `explicit.stat_2694482655@T1` | -0.85682 |
| `explicit.stat_210067635@T1` | -0.85419 |

### jewel — n=926, R²=-0.1903

intercept: `-2.1895`  ·  log_price: True  ·  ilvl: `0.04643`  ·  n_mods: `-0.01055`  ·  n_top_tier: `-0.31462`  ·  corrupted: `0.75240`

| stat_id | coef |
|---|---|
| `explicit.stat_533892981@T1` | 11.37626 |
| `explicit.stat_2637470878@T1` | -10.05825 |
| `explicit.stat_1829102168@T1` | 9.72778 |
| `explicit.stat_1594812856@T1` | 9.06140 |
| `explicit.stat_3851254963@T1` | 9.05539 |
| `explicit.stat_2301718443@T1` | -8.21321 |
| `explicit.stat_1776411443@T1` | 7.46354 |
| `explicit.stat_2456523742@T1` | 7.11997 |
| `explicit.stat_169946467@T1` | 7.11431 |
| `explicit.stat_153777645@T1` | 6.64895 |
| `explicit.stat_274716455@T1` | 6.48363 |
| `explicit.stat_2011656677@T1` | 6.31757 |

### weapon.sceptre — n=822, R²=0.0

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

### weapon.spear — n=738, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

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

### armour.focus — n=691, R²=0.0

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

### armour.shield — n=567, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

### armour.quiver — n=344, R²=0.0

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

### weapon.warstaff — n=342, R²=-0.0029

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T2` | -0.00000 |
| `explicit.stat_387439868@T1` | 0.00000 |
| `explicit.stat_2694482655@T1` | -0.00000 |
| `explicit.stat_791928121@T2` | -0.00000 |
| `explicit.stat_791928121@T1` | -0.00000 |
| `explicit.stat_387439868@T2` | 0.00000 |
| `explicit.stat_1940865751@T2` | 0.00000 |
| `explicit.stat_210067635@T2` | 0.00000 |
| `explicit.stat_709508406@T2` | -0.00000 |
| `explicit.stat_3261801346@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_9187492` | 0.00000 |

### weapon.staff — n=338, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

### flask.charm — n=326, R²=-0.4813

intercept: `0.0353`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00208`  ·  n_top_tier: `-0.00285`  ·  corrupted: `-0.00402`  ·  quality: `-0.00013`

| stat_id | coef |
|---|---|
| `explicit.stat_2541588185@T2` | 0.29259 |
| `explicit.stat_280890192` | -0.25352 |
| `implicit.stat_2016937536` | 0.22457 |
| `implicit.stat_1691862754` | -0.03330 |
| `implicit.stat_4010341289` | -0.03324 |
| `implicit.stat_3699444296` | -0.03324 |
| `implicit.stat_1810482573` | -0.03323 |
| `implicit.stat_2778646494` | -0.03320 |
| `implicit.stat_3676540188` | -0.03320 |
| `implicit.stat_585126960` | -0.03301 |
| `implicit.stat_3310778564` | -0.03205 |
| `implicit.stat_3854901951` | -0.03075 |

### weapon.twomace — n=242, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |
| `explicit.stat_1940865751` | 0.00000 |
| `explicit.stat_1940865751@T1` | 0.00000 |
| `explicit.stat_1940865751@T2` | 0.00000 |
| `explicit.stat_210067635` | 0.00000 |

## Coverage (listings per base)

- … **Utility Belt** — 950 listings (950 priced) [1.0–737.3 ex]
- … **Dueling Wand** — 783 listings (783 priced) [1.0–727.0 ex]
- … **Obliterator Bow** — 629 listings (629 priced) [0.5–727.0 ex]
- … **Stellar Amulet** — 624 listings (624 priced) [0.3–737.3 ex]
- … **Emerald** — 542 listings (542 priced) [0.4–727.0 ex]
- … **Solar Amulet** — 489 listings (489 priced) [1.0–737.3 ex]
- … **Sapphire** — 478 listings (478 priced) [0.4–727.0 ex]
- … **Gold Amulet** — 476 listings (476 priced) [0.3–737.3 ex]
- … **Siphoning Wand** — 449 listings (449 priced) [1.0–727.0 ex]
- … **Warmonger Bow** — 449 listings (449 priced) [1.0–727.0 ex]
- … **Plate Belt** — 448 listings (448 priced) [1.0–737.3 ex]
- … **Ruby** — 443 listings (443 priced) [0.3–727.0 ex]
- … **Ancestral Tiara** — 440 listings (440 priced) [1.0–737.3 ex]
- … **Heavy Belt** — 440 listings (440 priced) [0.5–737.3 ex]
- … **Galvanic Wand** — 437 listings (437 priced) [1.0–727.0 ex]
- … **Attuned Wand** — 407 listings (407 priced) [0.3–727.0 ex]
- … **Amethyst Ring** — 403 listings (403 priced) [1.0–737.3 ex]
- … **Prismatic Ring** — 398 listings (398 priced) [0.3–737.3 ex]
- … **Withered Wand** — 394 listings (394 priced) [1.0–727.0 ex]
- … **Trarthan Cannon** — 369 listings (369 priced) [0.7–727.0 ex]
- … **Long Belt** — 365 listings (365 priced) [1.0–737.3 ex]
- … **Gold Ring** — 363 listings (363 priced) [0.7–737.3 ex]
- … **Lapis Amulet** — 352 listings (352 priced) [0.6–737.3 ex]
- … **Rawhide Belt** — 351 listings (351 priced) [1.0–737.3 ex]
- … **Amber Amulet** — 349 listings (349 priced) [0.3–737.3 ex]

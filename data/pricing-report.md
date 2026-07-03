# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-03T09:54:00+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **44184** (44184 priced in exalted)
- Distinct bases: 738 · distinct mods: 1511 · mod rows: 223816
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-03T09:37:49+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×9.71** (median |log error| 2.2736)
- Within ±30% of asking price: **26%**
- Skill vs constant-price guess: **+0.18** (> 0 = the mods carry signal)
- Calibration: 65% of actuals above prediction (target ≈ 75%)

| group | n_test | ×err | ±30% | skill |
|---|---|---|---|---|
| accessory.belt | 747 | ×59.99 | 2% | +0.11 |
| armour.chest | 732 | ×7.45 | 4% | +0.24 |
| armour.helmet | 717 | ×10.39 | 42% | +0.03 |
| armour.boots | 657 | ×7.06 | 6% | +0.47 |
| armour.gloves | 645 | ×7.81 | 6% | +0.32 |
| accessory.ring | 614 | ×10.00 | 7% | +0.02 |
| weapon.wand | 596 | ×9.38 | 31% | -0.06 |
| accessory.amulet | 575 | ×60.21 | 1% | +0.07 |
| weapon.crossbow | 478 | ×9.20 | 33% | +0.03 |
| other | 457 | ×10.00 | 36% | +0.44 |
| weapon.bow | 424 | ×8.48 | 33% | -0.09 |
| jewel | 191 | ×26.05 | 4% | -0.18 |
| weapon.sceptre | 169 | ×1.00 | 99% | +0.00 |
| weapon.spear | 159 | ×1.00 | 99% | +0.00 |
| armour.focus | 143 | ×1.00 | 100% | n/a |
| armour.shield | 117 | ×1.00 | 100% | n/a |
| weapon.warstaff | 72 | ×1.00 | 99% | -0.00 |
| weapon.staff | 67 | ×1.00 | 90% | +0.00 |
| armour.quiver | 63 | ×1.00 | 94% | +0.00 |
| weapon.twomace | 52 | ×1.00 | 96% | +0.00 |
| flask.charm | 50 | ×1.01 | 68% | -0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=4216, R²=0.0729

intercept: `1.5694`  ·  log_price: True  ·  ilvl: `0.00092`  ·  n_mods: `0.01449`  ·  n_top_tier: `0.31473`  ·  corrupted: `4.68185`  ·  n_sockets: `-0.01186`  ·  quality: `-0.00149`

| stat_id | coef |
|---|---|
| `explicit.stat_2968503605@T1` | 4.02255 |
| `explicit.stat_124131830@T1` | 1.14413 |
| `explicit.stat_1263695895@T1` | -0.96092 |
| `explicit.stat_4080418644@T1` | -0.68760 |
| `explicit.stat_124131830` | -0.61995 |
| `explicit.stat_2891184298@T1` | -0.61628 |
| `explicit.stat_4080418644@T2` | -0.53881 |
| `explicit.stat_789117908@T1` | 0.52129 |
| `explicit.stat_3299347043@T1` | -0.48082 |
| `explicit.stat_3299347043@T2` | -0.44980 |
| `explicit.stat_3372524247@T1` | -0.44104 |
| `explicit.stat_4052037485@T1` | -0.41878 |

### accessory.belt — n=3456, R²=-0.101

intercept: `2.6175`  ·  log_price: True  ·  ilvl: `0.00290`  ·  n_mods: `-0.04797`  ·  n_top_tier: `0.47381`  ·  corrupted: `0.15485`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 2.25113 |
| `implicit.stat_731781020` | -1.76131 |
| `explicit.stat_2923486259@T1` | -1.66267 |
| `explicit.stat_2881298780@T1` | 0.78491 |
| `explicit.stat_51994685@T1` | -0.66976 |
| `explicit.stat_51994685@T2` | -0.65061 |
| `explicit.stat_1050105434@T2` | -0.62222 |
| `explicit.stat_2923486259@T2` | -0.61691 |
| `explicit.stat_2881298780@T2` | -0.61474 |
| `explicit.stat_644456512@T1` | -0.55693 |
| `explicit.stat_4080418644@T1` | -0.54452 |
| `explicit.stat_4080418644@T2` | -0.53987 |

### armour.chest — n=3321, R²=-0.15

intercept: `2.5872`  ·  log_price: True  ·  ilvl: `-0.00629`  ·  n_mods: `-0.05899`  ·  n_top_tier: `0.13886`  ·  corrupted: `0.29677`  ·  n_sockets: `-0.24271`  ·  quality: `-0.07222`

| stat_id | coef |
|---|---|
| `desecrated.stat_3299347043@T1` | 2.45909 |
| `implicit.stat_1978899297` | -1.48750 |
| `explicit.stat_3362812763@T2` | -1.36795 |
| `rune.stat_836936635` | 1.24206 |
| `explicit.stat_3033371881@T1` | -1.23497 |
| `explicit.stat_3981240776@T2` | 1.10880 |
| `explicit.stat_2923486259@T2` | -1.08268 |
| `explicit.stat_4080418644@T1` | 1.05487 |
| `explicit.stat_4080418644@T2` | 0.91079 |
| `explicit.stat_3261801346@T2` | -0.73784 |
| `explicit.stat_2451402625@T2` | -0.71753 |
| `explicit.stat_1062208444@T2` | -0.68516 |

### armour.helmet — n=3319, R²=-0.1268

intercept: `2.1666`  ·  log_price: True  ·  ilvl: `-0.00388`  ·  n_mods: `-0.02954`  ·  n_top_tier: `0.43337`  ·  corrupted: `0.37390`  ·  n_sockets: `-0.24122`  ·  quality: `-0.00381`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.99726 |
| `explicit.stat_1263695895@T1` | 2.81876 |
| `explicit.stat_1263695895@T2` | 2.05211 |
| `explicit.stat_803737631@T1` | -1.61789 |
| `desecrated.stat_3299347043@T2` | 1.56502 |
| `explicit.stat_53045048@T2` | -1.39201 |
| `explicit.stat_3362812763@T2` | -1.30726 |
| `explicit.stat_4080418644@T1` | 1.27821 |
| `explicit.stat_2451402625@T2` | 1.19476 |
| `explicit.stat_2923486259@T1` | 1.17304 |
| `explicit.stat_328541901@T1` | -1.09877 |
| `explicit.stat_803737631@T2` | -1.08492 |

### armour.boots — n=3270, R²=-0.1242

intercept: `2.7786`  ·  log_price: True  ·  ilvl: `-0.01701`  ·  n_mods: `-0.14611`  ·  n_top_tier: `0.91977`  ·  corrupted: `0.60378`  ·  n_sockets: `0.18103`  ·  quality: `-0.02624`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 7.25555 |
| `explicit.stat_3484657501@T2` | -2.84901 |
| `explicit.stat_3362812763@T2` | -2.58436 |
| `explicit.stat_4080418644@T1` | -2.31918 |
| `explicit.stat_1062208444@T1` | -2.09744 |
| `explicit.stat_1062208444@T2` | -2.02265 |
| `explicit.stat_4080418644@T2` | -1.95594 |
| `explicit.stat_3362812763@T1` | -1.85294 |
| `explicit.stat_3484657501@T1` | -1.67093 |
| `explicit.stat_3261801346@T2` | -1.56898 |
| `explicit.stat_53045048@T2` | -1.38387 |
| `explicit.stat_2923486259@T1` | 1.35806 |

### armour.gloves — n=3150, R²=-0.173

intercept: `2.3348`  ·  log_price: True  ·  ilvl: `-0.01083`  ·  n_mods: `0.01036`  ·  n_top_tier: `0.76391`  ·  corrupted: `0.23451`  ·  n_sockets: `0.10972`  ·  quality: `0.01448`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.30612 |
| `explicit.stat_4080418644@T1` | -2.28280 |
| `explicit.stat_4220027924@T1` | -2.02961 |
| `explicit.stat_53045048@T2` | -1.83971 |
| `explicit.stat_2923486259@T1` | -1.79161 |
| `explicit.stat_2557965901@T2` | -1.74779 |
| `explicit.stat_1062208444@T2` | 1.74583 |
| `explicit.stat_1671376347@T1` | -1.66282 |
| `explicit.stat_3484657501@T2` | -1.51669 |
| `explicit.stat_2557965901@T1` | -1.42130 |
| `explicit.stat_3033371881@T2` | 1.35360 |
| `explicit.stat_3032590688@T2` | -1.34794 |

### accessory.amulet — n=2949, R²=-2.1673

intercept: `5.2186`  ·  log_price: True  ·  ilvl: `-0.05610`  ·  n_mods: `-0.28963`  ·  n_top_tier: `0.93226`  ·  corrupted: `1.66886`  ·  n_sockets: `0.12695`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T2` | -3.94863 |
| `explicit.stat_2923486259@T1` | -3.33174 |
| `explicit.stat_2923486259@T2` | -2.60497 |
| `explicit.stat_1444556985@T1` | 2.48553 |
| `explicit.stat_328541901@T1` | -1.82651 |
| `explicit.stat_4080418644@T1` | -1.79017 |
| `explicit.stat_3917489142@T2` | -1.76927 |
| `explicit.stat_4080418644@T2` | -1.76716 |
| `explicit.stat_2106365538@T1` | -1.76489 |
| `explicit.stat_2482852589@T2` | -1.71631 |
| `explicit.stat_1050105434@T2` | -1.70956 |
| `explicit.stat_124131830@T2` | -1.68034 |

### accessory.ring — n=2782, R²=-2.2923

intercept: `7.8687`  ·  log_price: True  ·  ilvl: `-0.05994`  ·  n_mods: `-0.43020`  ·  n_top_tier: `0.34123`  ·  corrupted: `0.79439`  ·  n_sockets: `5.45276`  ·  quality: `-0.07254`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -3.20347 |
| `explicit.stat_2923486259@T2` | -3.11887 |
| `explicit.stat_4220027924@T1` | 2.47420 |
| `explicit.stat_2923486259@T1` | -2.38793 |
| `explicit.stat_1379411836@T1` | -2.03979 |
| `explicit.stat_1263695895@T1` | -1.96852 |
| `explicit.stat_707457662@T1` | 1.84244 |
| `explicit.stat_1379411836@T2` | -1.72541 |
| `explicit.stat_1263695895@T2` | -1.50268 |
| `explicit.stat_707457662@T2` | 1.49275 |
| `explicit.stat_3695891184@T1` | -1.34386 |
| `explicit.stat_3032590688@T1` | -1.31827 |

### weapon.wand — n=2730, R²=-1.4099

intercept: `3.3306`  ·  log_price: True  ·  ilvl: `-0.04189`  ·  n_mods: `-0.01098`  ·  n_top_tier: `0.08234`  ·  corrupted: `0.05146`  ·  n_sockets: `0.01389`  ·  quality: `0.08401`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.80775 |
| `explicit.stat_591105508@T1` | 2.41679 |
| `explicit.stat_1545858329@T1` | 2.29223 |
| `explicit.stat_736967255@T2` | 2.19071 |
| `explicit.stat_2974417149@T1` | 2.14674 |
| `explicit.stat_1600707273@T1` | 1.92648 |
| `explicit.stat_4226189338@T1` | 1.41691 |
| `crafted.stat_124131830` | 1.24725 |
| `explicit.stat_124131830@T2` | 1.24357 |
| `explicit.stat_2254480358@T1` | 0.50735 |
| `explicit.stat_124131830` | -0.41654 |
| `rune.stat_124131830` | 0.35426 |

### weapon.bow — n=2346, R²=-1.2449

intercept: `3.3509`  ·  log_price: True  ·  ilvl: `-0.04172`  ·  n_mods: `-0.01923`  ·  n_top_tier: `0.52419`  ·  corrupted: `0.26363`  ·  n_sockets: `0.04181`  ·  quality: `-0.00703`

| stat_id | coef |
|---|---|
| `desecrated.stat_1200678966@T1` | -3.80042 |
| `rune.stat_3885405204` | -2.41458 |
| `explicit.stat_2463230181@T1` | 1.77887 |
| `explicit.stat_1202301673@T1` | 1.67548 |
| `crafted.stat_3035140377` | 1.12520 |
| `desecrated.stat_666077204@T1` | 0.94537 |
| `explicit.stat_821021828@T1` | -0.83458 |
| `explicit.stat_821021828@T2` | -0.74250 |
| `explicit.stat_1940865751@T1` | -0.60396 |
| `explicit.stat_1940865751@T2` | -0.57558 |
| `explicit.stat_1509134228@T1` | -0.56537 |
| `explicit.stat_3261801346@T1` | -0.55917 |

### weapon.crossbow — n=2226, R²=-1.2149

intercept: `4.1307`  ·  log_price: True  ·  ilvl: `-0.05213`  ·  n_mods: `-0.00395`  ·  n_top_tier: `0.74742`  ·  corrupted: `0.20187`  ·  n_sockets: `0.23616`  ·  quality: `-0.07395`

| stat_id | coef |
|---|---|
| `explicit.stat_709508406@T1` | 3.17356 |
| `explicit.stat_1037193709@T1` | 2.38387 |
| `explicit.stat_691932474@T1` | -1.87545 |
| `explicit.stat_3336890334@T1` | 1.43314 |
| `explicit.stat_1263695895@T2` | -1.26822 |
| `desecrated.stat_3131442032@T1` | 1.15832 |
| `desecrated.stat_1365232741@T1` | 1.15832 |
| `explicit.stat_1037193709@T2` | 0.95418 |
| `explicit.stat_2694482655@T1` | -0.92122 |
| `explicit.stat_1940865751@T1` | -0.88547 |
| `explicit.stat_4080418644@T1` | -0.84563 |
| `explicit.stat_3639275092@T1` | -0.83136 |

### jewel — n=1225, R²=-0.3955

intercept: `-1.8875`  ·  log_price: True  ·  ilvl: `0.04426`  ·  n_mods: `-0.00001`  ·  n_top_tier: `-0.35736`  ·  corrupted: `0.60485`

| stat_id | coef |
|---|---|
| `explicit.stat_2011656677@T1` | 8.76751 |
| `explicit.stat_1852872083@T1` | 7.68930 |
| `explicit.stat_2637470878@T1` | -7.18481 |
| `explicit.stat_318953428@T1` | 6.80444 |
| `explicit.stat_3851254963@T1` | 6.18239 |
| `explicit.stat_21071013@T1` | 6.04827 |
| `explicit.stat_3585532255@T1` | -5.99662 |
| `explicit.stat_1405298142@T1` | -5.85725 |
| `explicit.stat_3714003708@T1` | -5.41851 |
| `explicit.stat_1459321413@T1` | 5.28379 |
| `explicit.stat_1594812856@T1` | 5.27349 |
| `explicit.stat_1238227257@T1` | 5.19467 |

### weapon.sceptre — n=847, R²=0.0

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

### weapon.spear — n=765, R²=0.0

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

### armour.focus — n=712, R²=0.0

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

### armour.shield — n=582, R²=0.0

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

### weapon.warstaff — n=406, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |

### armour.quiver — n=401, R²=0.0

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

### weapon.staff — n=397, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1545858329` | 0.00000 |
| `explicit.stat_1545858329@T1` | 0.00000 |

### flask.charm — n=397, R²=-0.6126

intercept: `0.0161`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00004`  ·  n_top_tier: `-0.00005`  ·  corrupted: `-0.32736`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457@T1` | 0.32712 |
| `explicit.stat_2541588185@T2` | 0.30166 |
| `explicit.stat_280890192` | -0.12594 |
| `implicit.stat_2016937536` | 0.10994 |
| `implicit.stat_1691862754` | -0.01608 |
| `implicit.stat_1810482573` | -0.01607 |
| `implicit.stat_4010341289` | -0.01607 |
| `implicit.stat_585126960` | -0.01606 |
| `implicit.stat_2778646494` | -0.01606 |
| `implicit.stat_3699444296` | -0.01605 |
| `implicit.stat_3676540188` | -0.01605 |
| `implicit.stat_3310778564` | -0.01604 |

### weapon.twomace — n=291, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
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
| `explicit.stat_1940865751@T2` | 0.00000 |

## Coverage (listings per base)

- … **Utility Belt** — 1069 listings (1069 priced) [0.3–737.3 ex]
- … **Dueling Wand** — 861 listings (861 priced) [1.0–727.0 ex]
- … **Emerald** — 698 listings (698 priced) [0.4–727.0 ex]
- … **Obliterator Bow** — 697 listings (697 priced) [0.5–727.0 ex]
- … **Stellar Amulet** — 689 listings (689 priced) [0.3–737.3 ex]
- … **Sapphire** — 611 listings (611 priced) [0.4–727.0 ex]
- … **Ruby** — 552 listings (552 priced) [0.3–727.0 ex]
- … **Solar Amulet** — 536 listings (536 priced) [1.0–737.3 ex]
- … **Gold Amulet** — 528 listings (528 priced) [0.3–737.3 ex]
- … **Siphoning Wand** — 496 listings (496 priced) [1.0–727.0 ex]
- … **Warmonger Bow** — 490 listings (490 priced) [1.0–727.0 ex]
- … **Ancestral Tiara** — 486 listings (486 priced) [1.0–737.3 ex]
- … **Galvanic Wand** — 483 listings (483 priced) [1.0–727.0 ex]
- … **Plate Belt** — 477 listings (477 priced) [1.0–737.3 ex]
- … **Heavy Belt** — 475 listings (475 priced) [0.5–737.3 ex]
- … **Attuned Wand** — 450 listings (450 priced) [0.3–727.0 ex]
- … **Prismatic Ring** — 445 listings (445 priced) [0.3–737.3 ex]
- … **Amethyst Ring** — 441 listings (441 priced) [1.0–737.3 ex]
- … **Withered Wand** — 434 listings (434 priced) [1.0–727.0 ex]
- … **Gold Ring** — 419 listings (419 priced) [0.7–737.3 ex]
- … **Trarthan Cannon** — 395 listings (395 priced) [0.7–727.0 ex]
- … **Long Belt** — 394 listings (394 priced) [1.0–737.3 ex]
- … **Topaz Ring** — 393 listings (393 priced) [1.0–737.3 ex]
- … **Lapis Amulet** — 383 listings (383 priced) [0.6–737.3 ex]
- … **Rawhide Belt** — 378 listings (378 priced) [1.0–737.3 ex]

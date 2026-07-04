# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-04T17:36:32+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **118832** (118832 priced in exalted)
- Distinct bases: 879 · distinct mods: 2176 · mod rows: 572677
- Sold signals: **31576** sold · 39225 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-04T17:30:13+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.62** (median |log error| 2.0307)
- Within ±30% of asking price: **28%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 67% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×32.61 · ±30% 6% · n=16651
- Premium segment (60ex+): skill **+0.12** · typical error ×167.96 · ±30% 0% · n=9453
- Sold listings (clearing prices): skill **-0.09** · typical error ×1.73 · ±30% 52% · n=6839

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 1951 | ×6.03 | 7% | +0.05 | +0.03 |
| accessory.amulet | 1948 | ×29.84 | 12% | -0.01 | -0.03 |
| accessory.belt | 1931 | ×9.85 | 24% | +0.01 | +0.01 |
| armour.chest | 1869 | ×8.34 | 21% | +0.02 | +0.10 |
| armour.helmet | 1857 | ×8.89 | 21% | +0.00 | +0.06 |
| armour.gloves | 1721 | ×8.70 | 23% | +0.02 | +0.06 |
| armour.boots | 1695 | ×8.94 | 24% | +0.02 | +0.09 |
| other | 1597 | ×6.20 | 34% | +0.40 | +0.37 |
| jewel | 1416 | ×6.58 | 9% | -0.00 | +0.07 |
| weapon.wand | 1323 | ×9.39 | 33% | +0.05 | +0.09 |
| weapon.bow | 1143 | ×8.94 | 34% | +0.07 | +0.05 |
| weapon.crossbow | 1071 | ×7.97 | 32% | +0.07 | +0.13 |
| weapon.sceptre | 266 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.warstaff | 258 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.spear | 246 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.staff | 244 | ×1.00 | 97% | +0.00 | +0.00 |
| armour.focus | 195 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 187 | ×1.00 | 95% | +0.00 | +0.00 |
| armour.shield | 186 | ×1.00 | 96% | +0.00 | +0.00 |
| weapon.twomace | 134 | ×1.00 | 99% | +0.00 | +0.00 |
| flask.charm | 68 | ×1.00 | 57% | +0.03 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=14058, R²=-0.2904

intercept: `1.5475`  ·  log_price: True  ·  ilvl: `0.00503`  ·  n_mods: `0.04600`  ·  n_top_tier: `0.12798`  ·  corrupted: `0.41098`  ·  n_sockets: `-0.12848`  ·  quality: `-0.01417`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830` | -0.66332 |
| `explicit.stat_1050105434@T1` | -0.60221 |
| `implicit.stat_3182714256` | 0.47327 |
| `implicit.stat_718638445` | 0.47314 |
| `explicit.stat_4220027924@T2` | -0.36394 |
| `implicit.stat_1379411836` | -0.32124 |
| `explicit.stat_1050105434@T2` | -0.31151 |
| `implicit.stat_958696139` | 0.20885 |
| `implicit.stat_4041853756` | 0.19214 |
| `implicit.stat_3879011313` | 0.19213 |
| `explicit.stat_2891184298@T1` | -0.19119 |
| `explicit.stat_101878827@T1` | -0.19061 |

### accessory.amulet — n=9208, R²=-2.2237

intercept: `4.8713`  ·  log_price: True  ·  ilvl: `-0.05905`  ·  n_mods: `-0.11576`  ·  n_top_tier: `0.40453`  ·  corrupted: `-0.12180`  ·  n_sockets: `0.12969`  ·  quality: `0.16836`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | 2.54520 |
| `explicit.stat_3981240776@T2` | -2.42186 |
| `explicit.stat_3981240776@T1` | -2.25134 |
| `explicit.stat_2162097452@T2` | -2.03016 |
| `explicit.stat_9187492` | 1.47296 |
| `explicit.stat_4220027924@T1` | -1.36452 |
| `explicit.stat_803737631@T1` | -1.28345 |
| `explicit.stat_3556824919@T1` | -1.19600 |
| `explicit.stat_1671376347@T1` | 1.12902 |
| `explicit.stat_124131830@T2` | 1.11850 |
| `explicit.stat_803737631@T2` | -1.11503 |
| `explicit.stat_3372524247@T1` | 1.10837 |

### accessory.ring — n=9053, R²=-1.9081

intercept: `2.8853`  ·  log_price: True  ·  ilvl: `-0.02461`  ·  n_mods: `-0.03848`  ·  n_top_tier: `0.43056`  ·  corrupted: `0.19954`  ·  n_sockets: `3.52886`  ·  quality: `0.04221`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 5.76552 |
| `explicit.stat_707457662@T2` | 5.37293 |
| `explicit.stat_2557965901@T2` | 3.71270 |
| `explicit.stat_2557965901@T1` | 3.58639 |
| `explicit.stat_1379411836@T1` | -1.88553 |
| `explicit.stat_1573130764@T1` | -1.63821 |
| `explicit.stat_1379411836@T2` | -1.52741 |
| `explicit.stat_3299347043@T1` | -1.49444 |
| `explicit.stat_3695891184@T2` | -1.45029 |
| `explicit.stat_3962278098@T2` | -1.44850 |
| `explicit.stat_1671376347@T1` | -1.41903 |
| `explicit.stat_2923486259@T1` | -1.06259 |

### accessory.belt — n=8832, R²=-1.2415

intercept: `3.8882`  ·  log_price: True  ·  ilvl: `-0.04716`  ·  n_mods: `-0.02567`  ·  n_top_tier: `-0.07637`  ·  corrupted: `0.17826`  ·  n_sockets: `-0.08852`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.81839 |
| `explicit.stat_2923486259@T1` | 1.72653 |
| `explicit.stat_1836676211@T1` | 1.13044 |
| `explicit.stat_2923486259@T2` | 0.87497 |
| `explicit.stat_3372524247@T1` | 0.22342 |
| `explicit.stat_1671376347@T1` | 0.21745 |
| `explicit.stat_4220027924@T1` | 0.19053 |
| `explicit.stat_3585532255@T1` | 0.17585 |
| `explicit.stat_3585532255@T2` | 0.15580 |
| `implicit.stat_731781020` | 0.14102 |
| `pseudo.total_ele_res>=80` | 0.13984 |
| `explicit.stat_1570770415@T1` | 0.13362 |

### armour.chest — n=8587, R²=-1.353

intercept: `3.8646`  ·  log_price: True  ·  ilvl: `-0.04771`  ·  n_mods: `-0.02881`  ·  n_top_tier: `0.76411`  ·  corrupted: `-0.03877`  ·  n_sockets: `0.00066`  ·  quality: `0.01296`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 1.72835 |
| `implicit.stat_2251279027` | 1.62864 |
| `explicit.stat_3981240776@T1` | 1.32308 |
| `explicit.stat_2923486259@T1` | -0.90322 |
| `explicit.stat_3261801346@T2` | -0.89234 |
| `explicit.stat_3261801346@T1` | -0.88138 |
| `explicit.stat_2923486259@T2` | -0.87319 |
| `explicit.stat_4080418644@T2` | -0.85038 |
| `explicit.stat_2339757871@T1` | -0.83550 |
| `explicit.stat_3301100256@T2` | -0.83439 |
| `explicit.stat_986397080@T2` | -0.83423 |
| `explicit.stat_2339757871@T2` | -0.83420 |

### armour.helmet — n=8512, R²=-1.3396

intercept: `4.3420`  ·  log_price: True  ·  ilvl: `-0.05503`  ·  n_mods: `-0.02757`  ·  n_top_tier: `0.79212`  ·  corrupted: `0.11271`  ·  n_sockets: `-0.03089`  ·  quality: `0.01680`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 6.62058 |
| `explicit.stat_2339757871@T1` | -2.23807 |
| `explicit.stat_3033371881@T1` | -0.95648 |
| `explicit.stat_803737631@T2` | -0.93946 |
| `explicit.stat_3362812763@T1` | -0.92107 |
| `explicit.stat_3325883026@T1` | -0.91838 |
| `explicit.stat_53045048@T1` | -0.90808 |
| `explicit.stat_3639275092@T1` | -0.89654 |
| `explicit.stat_1263695895@T1` | -0.89604 |
| `explicit.stat_3321629045@T2` | -0.89460 |
| `explicit.stat_4015621042@T2` | -0.89096 |
| `explicit.stat_53045048@T2` | -0.88418 |

### armour.boots — n=7964, R²=-1.1011

intercept: `4.0380`  ·  log_price: True  ·  ilvl: `-0.05012`  ·  n_mods: `-0.03304`  ·  n_top_tier: `0.42402`  ·  corrupted: `0.01881`  ·  n_sockets: `0.02197`  ·  quality: `0.02353`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.06202 |
| `explicit.stat_2250533757@T1` | 1.75363 |
| `explicit.stat_4220027924@T1` | 1.04332 |
| `explicit.stat_2339757871@T1` | -0.73950 |
| `explicit.stat_3362812763@T1` | -0.61226 |
| `explicit.stat_3362812763@T2` | -0.56271 |
| `explicit.stat_3321629045@T1` | -0.55219 |
| `explicit.stat_99927264@T1` | -0.51345 |
| `explicit.stat_1062208444@T1` | -0.51248 |
| `explicit.stat_2160282525@T1` | -0.50923 |
| `explicit.stat_1062208444@T2` | -0.49501 |
| `explicit.stat_3033371881@T2` | -0.49358 |

### armour.gloves — n=7880, R²=-1.3576

intercept: `4.1125`  ·  log_price: True  ·  ilvl: `-0.05281`  ·  n_mods: `0.01834`  ·  n_top_tier: `0.82660`  ·  corrupted: `0.04491`  ·  n_sockets: `0.02706`  ·  quality: `0.01785`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.65334 |
| `explicit.stat_4015621042@T1` | -0.93250 |
| `explicit.stat_9187492@T2` | -0.92465 |
| `explicit.stat_3032590688@T1` | -0.90197 |
| `explicit.stat_3484657501@T2` | -0.89585 |
| `explicit.stat_803737631@T1` | -0.89201 |
| `explicit.stat_681332047@T2` | -0.89142 |
| `explicit.stat_2557965901@T2` | -0.89008 |
| `explicit.stat_803737631@T2` | -0.88916 |
| `explicit.stat_124859000@T1` | -0.87823 |
| `explicit.stat_3033371881@T2` | -0.87618 |
| `explicit.stat_2451402625@T2` | -0.87304 |

### jewel — n=7400, R²=-0.9837

intercept: `-1.5012`  ·  log_price: True  ·  ilvl: `0.03717`  ·  n_mods: `0.18896`  ·  n_top_tier: `-0.40657`  ·  corrupted: `0.62724`

| stat_id | coef |
|---|---|
| `explicit.stat_2301718443@T1` | -5.75266 |
| `explicit.stat_1869147066@T1` | 4.14402 |
| `explicit.stat_2011656677@T1` | 3.95041 |
| `explicit.stat_1569101201@T1` | 3.46283 |
| `explicit.stat_491450213@T1` | 3.16861 |
| `explicit.stat_2456523742@T1` | 3.07598 |
| `explicit.stat_3174700878@T1` | 2.77060 |
| `explicit.stat_3374165039@T1` | 2.74158 |
| `explicit.stat_1316278494@T1` | -2.69734 |
| `explicit.stat_3485067555@T1` | 2.67731 |
| `explicit.stat_153777645@T1` | 2.51594 |
| `explicit.stat_1805182458@T1` | -2.45030 |

### weapon.wand — n=6135, R²=-1.5862

intercept: `3.4520`  ·  log_price: True  ·  ilvl: `-0.04265`  ·  n_mods: `-0.01960`  ·  n_top_tier: `0.66988`  ·  corrupted: `-0.00555`  ·  n_sockets: `0.00348`  ·  quality: `0.03071`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.03642 |
| `explicit.stat_591105508@T1` | 1.68470 |
| `explicit.stat_1545858329@T1` | 1.65420 |
| `explicit.stat_4226189338@T1` | 1.62526 |
| `explicit.stat_2254480358@T1` | 1.56947 |
| `explicit.stat_736967255@T2` | 1.25008 |
| `explicit.stat_2968503605@T1` | 1.16729 |
| `explicit.stat_1600707273@T2` | 1.03461 |
| `crafted.stat_124131830` | 1.02791 |
| `explicit.stat_3962278098@T2` | -0.76914 |
| `explicit.stat_2768835289@T2` | -0.75835 |
| `explicit.stat_124131830@T2` | -0.74396 |

### weapon.bow — n=5221, R²=-1.5643

intercept: `3.4683`  ·  log_price: True  ·  ilvl: `-0.04284`  ·  n_mods: `-0.03123`  ·  n_top_tier: `0.22275`  ·  corrupted: `-0.06274`  ·  n_sockets: `0.00337`  ·  quality: `0.00064`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -6.40753 |
| `explicit.stat_2463230181@T1` | 2.02852 |
| `explicit.stat_1509134228@T1` | 1.94543 |
| `explicit.stat_518292764@T1` | 1.91753 |
| `explicit.stat_1202301673@T1` | 1.67080 |
| `crafted.stat_3035140377` | 1.08039 |
| `rune.stat_3885405204` | -0.72980 |
| `explicit.stat_821021828@T1` | -0.43083 |
| `desecrated.stat_666077204` | 0.40152 |
| `explicit.stat_821021828@T2` | -0.35737 |
| `desecrated.stat_518292764` | 0.33513 |
| `explicit.stat_1263695895@T1` | -0.33467 |

### weapon.crossbow — n=4950, R²=-1.4542

intercept: `3.5170`  ·  log_price: True  ·  ilvl: `-0.04388`  ·  n_mods: `-0.00020`  ·  n_top_tier: `0.24097`  ·  corrupted: `-0.02319`  ·  n_sockets: `0.01966`  ·  quality: `-0.00662`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -3.30431 |
| `explicit.stat_2250681686` | 3.09280 |
| `explicit.stat_709508406@T1` | 2.92110 |
| `explicit.stat_3336890334@T1` | 2.04879 |
| `explicit.stat_1037193709@T1` | 2.03414 |
| `explicit.stat_1509134228@T1` | 2.01784 |
| `desecrated.stat_1365232741@T1` | -1.40816 |
| `desecrated.stat_3131442032@T1` | -1.40816 |
| `explicit.stat_691932474@T1` | -1.18003 |
| `explicit.stat_1202301673@T1` | 0.97997 |
| `explicit.stat_1967051901@T1` | 0.86559 |
| `crafted.stat_3035140377` | 0.79871 |

### weapon.sceptre — n=1308, R²=0.0

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

### weapon.warstaff — n=1206, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

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
| `desecrated.stat_3336890334` | 0.00000 |
| `desecrated.stat_387439868` | 0.00000 |

### weapon.spear — n=1179, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

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
| `explicit.stat_1263695895@T2` | -0.00000 |

### weapon.staff — n=1136, R²=0.0

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

### armour.focus — n=985, R²=0.0

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

### flask.charm — n=937, R²=-0.5072

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2541588185@T2` | 0.24991 |
| `explicit.stat_1873752457` | 0.00017 |
| `explicit.stat_1120862500@T2` | -0.00005 |
| `explicit.stat_2566921799` | 0.00003 |
| `explicit.stat_1873752457@T1` | -0.00002 |
| `explicit.stat_1366840608@T2` | 0.00002 |
| `explicit.stat_3849649145` | -0.00002 |
| `explicit.stat_1873752457@T2` | -0.00002 |
| `explicit.stat_828533480@T2` | -0.00002 |
| `implicit.stat_3676540188` | -0.00002 |
| `implicit.stat_2016937536` | 0.00001 |
| `implicit.stat_4010341289` | -0.00001 |

### armour.quiver — n=918, R²=0.0

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

### armour.shield — n=856, R²=0.0

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

### weapon.twomace — n=647, R²=0.0

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

- … **Emerald** — 3833 listings (3833 priced) [0.8–856.7 ex]
- … **Sapphire** — 3804 listings (3804 priced) [0.4–856.7 ex]
- … **Ruby** — 3064 listings (3064 priced) [0.3–856.7 ex]
- … **Utility Belt** — 2785 listings (2785 priced) [0.3–77723.4 ex]
- … **Stellar Amulet** — 2080 listings (2080 priced) [0.3–38371.8 ex]
- … **Dueling Wand** — 1930 listings (1930 priced) [1.0–856.7 ex]
- … **Solar Amulet** — 1732 listings (1732 priced) [1.0–856.7 ex]
- … **Gold Amulet** — 1697 listings (1697 priced) [0.6–856.7 ex]
- … **Prismatic Ring** — 1635 listings (1635 priced) [0.3–856.7 ex]
- … **Amethyst Ring** — 1564 listings (1564 priced) [0.8–856.7 ex]
- … **Gold Ring** — 1518 listings (1518 priced) [0.8–856.7 ex]
- … **Obliterator Bow** — 1465 listings (1465 priced) [0.9–856.7 ex]
- … **Plate Belt** — 1374 listings (1374 priced) [1.0–856.7 ex]
- … **Topaz Ring** — 1262 listings (1262 priced) [1.0–856.7 ex]
- … **Heavy Belt** — 1257 listings (1257 priced) [0.5–856.7 ex]
- … **Sapphire Ring** — 1239 listings (1239 priced) [0.9–856.7 ex]
- … **Ancestral Tiara** — 1217 listings (1217 priced) [1.0–856.7 ex]
- … **Ruby Ring** — 1196 listings (1196 priced) [0.8–856.7 ex]
- … **Lapis Amulet** — 1141 listings (1141 priced) [0.6–856.7 ex]
- … **Amber Amulet** — 1107 listings (1107 priced) [0.6–856.7 ex]
- … **Jade Amulet** — 1107 listings (1107 priced) [0.6–856.7 ex]
- … **Galvanic Wand** — 1103 listings (1103 priced) [1.0–856.7 ex]
- … **Siphoning Wand** — 1080 listings (1080 priced) [1.0–856.7 ex]
- … **Warmonger Bow** — 1052 listings (1052 priced) [1.0–856.7 ex]
- … **Attuned Wand** — 1022 listings (1022 priced) [0.3–856.7 ex]

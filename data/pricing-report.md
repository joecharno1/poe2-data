# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-05T10:54:19+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **160313** (160313 priced in exalted)
- Distinct bases: 907 · distinct mods: 2364 · mod rows: 761544
- Sold signals: **36428** sold · 80360 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-05T10:47:51+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×8.15** (median |log error| 2.0976)
- Within ±30% of asking price: **30%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 65% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×25.31 · ±30% 13% · n=20656
- Premium segment (60ex+): skill **+0.12** · typical error ×138.46 · ±30% 1% · n=11778
- Sold listings (clearing prices): skill **+0.12** · typical error ×50.86 · ±30% 18% · n=5633

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 2856 | ×7.28 | 5% | +0.00 | +0.00 |
| accessory.amulet | 2842 | ×31.03 | 13% | -0.03 | -0.08 |
| accessory.belt | 2508 | ×9.65 | 27% | +0.03 | +0.06 |
| armour.chest | 2477 | ×8.65 | 25% | +0.02 | +0.08 |
| jewel | 2409 | ×7.36 | 7% | +0.00 | +0.04 |
| armour.helmet | 2389 | ×8.50 | 21% | +0.02 | +0.06 |
| armour.boots | 2294 | ×6.00 | 40% | -0.00 | -0.05 |
| armour.gloves | 2258 | ×10.00 | 36% | -0.00 | -0.01 |
| other | 2182 | ×9.99 | 35% | +0.41 | +0.37 |
| weapon.wand | 1648 | ×9.12 | 35% | +0.03 | +0.09 |
| weapon.bow | 1387 | ×8.90 | 34% | +0.07 | +0.04 |
| weapon.crossbow | 1274 | ×8.91 | 28% | +0.07 | +0.09 |
| weapon.sceptre | 315 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.warstaff | 305 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.spear | 293 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.staff | 280 | ×1.00 | 100% | n/a | - |
| armour.focus | 232 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 232 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.shield | 193 | ×1.00 | 98% | +0.00 | +0.00 |
| flask.charm | 158 | ×1.00 | 100% | n/a | - |
| weapon.twomace | 156 | ×1.00 | 97% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=19378, R²=-0.2848

intercept: `1.5728`  ·  log_price: True  ·  ilvl: `0.00087`  ·  n_mods: `0.07139`  ·  n_top_tier: `1.24885`  ·  corrupted: `2.38657`  ·  n_sockets: `-0.01574`  ·  quality: `-0.00136`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 2.77156 |
| `explicit.stat_2891184298@T1` | 2.67996 |
| `explicit.stat_1050105434@T1` | -2.65655 |
| `explicit.stat_1589917703@T1` | 2.32430 |
| `explicit.stat_3141070085@T1` | 2.30881 |
| `explicit.stat_101878827@T1` | 2.27224 |
| `explicit.stat_789117908@T1` | -2.17106 |
| `explicit.stat_3917489142@T1` | 1.93775 |
| `explicit.stat_2106365538@T1` | 1.70773 |
| `explicit.stat_2968503605@T1` | 1.36279 |
| `explicit.stat_2974417149@T1` | 1.19260 |
| `implicit.stat_1379411836` | -0.28444 |

### accessory.ring — n=13316, R²=-1.6219

intercept: `4.6277`  ·  log_price: True  ·  ilvl: `-0.04261`  ·  n_mods: `-0.24644`  ·  n_top_tier: `0.05826`  ·  corrupted: `0.85132`  ·  n_sockets: `3.28924`  ·  quality: `0.03010`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -2.84993 |
| `explicit.stat_2557965901@T1` | 2.73536 |
| `explicit.stat_1379411836@T1` | -2.72034 |
| `explicit.stat_2557965901@T2` | 1.94122 |
| `explicit.stat_1379411836@T2` | -1.67447 |
| `explicit.stat_707457662@T1` | 1.53466 |
| `explicit.stat_707457662@T2` | 1.44715 |
| `explicit.stat_3299347043@T2` | -1.35293 |
| `explicit.stat_1573130764@T1` | -1.29575 |
| `explicit.stat_1368271171@T1` | -1.15173 |
| `explicit.stat_1368271171@T2` | -1.12186 |
| `explicit.stat_2923486259@T1` | -0.94779 |

### accessory.amulet — n=12988, R²=-2.1962

intercept: `4.2076`  ·  log_price: True  ·  ilvl: `-0.05225`  ·  n_mods: `-0.03082`  ·  n_top_tier: `0.88750`  ·  corrupted: `0.11408`  ·  n_sockets: `-0.00922`  ·  quality: `-0.02525`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T2` | -1.99575 |
| `explicit.stat_983749596@T1` | -1.79551 |
| `explicit.stat_2748665614@T1` | -1.71976 |
| `explicit.stat_983749596@T2` | -1.47984 |
| `explicit.stat_2748665614@T2` | -1.43080 |
| `explicit.stat_9187492@T2` | 1.39088 |
| `explicit.stat_1202301673@T2` | 1.27116 |
| `explicit.stat_3299347043@T1` | -1.10215 |
| `explicit.stat_3261801346@T1` | -1.08532 |
| `explicit.stat_587431675@T2` | 1.02150 |
| `explicit.stat_1379411836@T2` | -1.00198 |
| `explicit.stat_2482852589@T1` | -0.99351 |

### jewel — n=12129, R²=-0.8471

intercept: `-1.3445`  ·  log_price: True  ·  ilvl: `0.03536`  ·  n_mods: `0.19566`  ·  n_top_tier: `-0.41624`  ·  corrupted: `0.42663`  ·  quality: `0.22420`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | 6.16751 |
| `explicit.stat_1869147066@T1` | 4.26993 |
| `explicit.stat_21071013@T1` | 3.73466 |
| `explicit.stat_3780644166@T1` | 3.69299 |
| `explicit.stat_1697951953@T1` | -3.31376 |
| `explicit.stat_153777645@T1` | 3.28509 |
| `explicit.stat_1836676211@T1` | 2.96766 |
| `explicit.stat_3973629633@T1` | 2.92114 |
| `explicit.stat_1062710370@T1` | -2.82507 |
| `explicit.stat_1405298142@T1` | 2.78640 |
| `explicit.stat_3851254963@T1` | 2.72806 |
| `explicit.stat_1316278494@T1` | -2.72510 |

### accessory.belt — n=11638, R²=-1.2741

intercept: `3.7362`  ·  log_price: True  ·  ilvl: `-0.04537`  ·  n_mods: `-0.02461`  ·  n_top_tier: `0.09180`  ·  corrupted: `0.09295`  ·  n_sockets: `-0.14437`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.50723 |
| `explicit.stat_2923486259@T1` | 1.27263 |
| `explicit.stat_2923486259@T2` | 0.81455 |
| `explicit.stat_3299347043@T1` | -0.46631 |
| `explicit.stat_3299347043@T2` | -0.27371 |
| `explicit.stat_3325883026@T1` | -0.13489 |
| `explicit.stat_809229260@T2` | -0.13242 |
| `explicit.stat_1389754388@T1` | -0.13220 |
| `explicit.stat_1412217137@T1` | -0.12873 |
| `explicit.stat_2881298780@T1` | -0.12741 |
| `explicit.stat_3372524247@T1` | 0.12086 |
| `explicit.stat_915769802@T2` | -0.11556 |

### armour.chest — n=11381, R²=-1.3452

intercept: `3.9975`  ·  log_price: True  ·  ilvl: `-0.04935`  ·  n_mods: `-0.01601`  ·  n_top_tier: `0.54509`  ·  corrupted: `0.15831`  ·  n_sockets: `-0.00240`  ·  quality: `0.00622`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.25994 |
| `explicit.stat_3981240776@T1` | 1.50108 |
| `explicit.stat_328541901@T1` | -0.64982 |
| `explicit.stat_3261801346@T2` | -0.64492 |
| `explicit.stat_4015621042@T1` | -0.63951 |
| `explicit.stat_4080418644@T2` | -0.63274 |
| `explicit.stat_3261801346@T1` | -0.62616 |
| `explicit.stat_986397080@T2` | -0.61797 |
| `explicit.stat_4080418644@T1` | -0.60765 |
| `explicit.stat_915769802@T1` | -0.60584 |
| `explicit.stat_328541901@T2` | -0.60304 |
| `explicit.stat_3325883026@T2` | -0.59879 |

### armour.helmet — n=11204, R²=-1.3814

intercept: `4.5056`  ·  log_price: True  ·  ilvl: `-0.05632`  ·  n_mods: `-0.02709`  ·  n_top_tier: `0.74218`  ·  corrupted: `0.56176`  ·  n_sockets: `-0.01147`  ·  quality: `0.02138`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.73247 |
| `explicit.stat_2339757871@T1` | -2.62114 |
| `explicit.stat_3033371881@T1` | -0.83813 |
| `explicit.stat_53045048@T1` | -0.83237 |
| `explicit.stat_3033371881@T2` | -0.81957 |
| `explicit.stat_803737631@T2` | -0.81602 |
| `explicit.stat_4052037485@T2` | -0.80140 |
| `explicit.stat_3325883026@T1` | -0.80053 |
| `explicit.stat_1263695895@T1` | -0.79796 |
| `explicit.stat_3321629045@T2` | -0.79566 |
| `explicit.stat_3325883026@T2` | -0.79456 |
| `explicit.stat_3321629045@T1` | -0.78901 |

### armour.boots — n=10478, R²=-0.1887

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.05983`  ·  corrupted: `0.00001`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 0.11665 |
| `pseudo.total_chaos_res` | 0.08289 |
| `explicit.stat_2923486259` | -0.08288 |
| `explicit.stat_2339757871@T1` | -0.05993 |
| `explicit.stat_3325883026@T2` | -0.05985 |
| `explicit.stat_1062208444@T1` | -0.05985 |
| `explicit.stat_3484657501@T1` | -0.05985 |
| `explicit.stat_99927264@T2` | -0.05984 |
| `explicit.stat_3325883026@T1` | -0.05984 |
| `explicit.stat_3917489142@T2` | -0.05984 |
| `explicit.stat_3362812763@T2` | -0.05984 |
| `explicit.stat_2451402625@T2` | -0.05984 |

### armour.gloves — n=10382, R²=-0.2129

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.40641`  ·  corrupted: `0.16422`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_4067062424@T1` | 0.97880 |
| `explicit.stat_2339757871@T1` | -0.40667 |
| `explicit.stat_3484657501@T2` | -0.40645 |
| `explicit.stat_3362812763@T1` | -0.40644 |
| `explicit.stat_1368271171@T1` | -0.40644 |
| `explicit.stat_4080418644@T1` | -0.40643 |
| `explicit.stat_4015621042@T1` | -0.40643 |
| `explicit.stat_2797971005@T2` | -0.40643 |
| `explicit.stat_3362812763@T2` | -0.40643 |
| `explicit.stat_3695891184@T1` | -0.40643 |
| `explicit.stat_1671376347@T1` | -0.40643 |
| `explicit.stat_4052037485@T1` | -0.40643 |

### weapon.wand — n=7579, R²=-1.6913

intercept: `3.4821`  ·  log_price: True  ·  ilvl: `-0.04352`  ·  n_mods: `-0.01347`  ·  n_top_tier: `0.13572`  ·  corrupted: `-0.00190`  ·  n_sockets: `-0.00237`  ·  quality: `0.01464`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.60689 |
| `explicit.stat_591105508@T1` | 2.23650 |
| `explicit.stat_4226189338@T1` | 2.22053 |
| `explicit.stat_1545858329@T1` | 2.15247 |
| `explicit.stat_2254480358@T1` | 2.11548 |
| `explicit.stat_1600707273@T2` | 1.23449 |
| `explicit.stat_736967255@T2` | 1.11645 |
| `crafted.stat_124131830` | 0.97788 |
| `explicit.stat_2968503605@T1` | 0.48556 |
| `rune.stat_3278136794` | 0.24828 |
| `explicit.stat_2768835289@T2` | -0.23584 |
| `explicit.stat_1600707273@T1` | 0.21870 |

### weapon.bow — n=6338, R²=-1.6111

intercept: `3.4519`  ·  log_price: True  ·  ilvl: `-0.04270`  ·  n_mods: `-0.02425`  ·  n_top_tier: `0.28016`  ·  corrupted: `-0.04520`  ·  n_sockets: `0.00595`  ·  quality: `0.00293`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -6.76485 |
| `explicit.stat_2463230181@T1` | 2.01639 |
| `explicit.stat_1202301673@T1` | 1.85760 |
| `crafted.stat_3035140377` | 1.72983 |
| `explicit.stat_518292764@T1` | 1.62006 |
| `explicit.stat_1509134228@T1` | 1.51923 |
| `desecrated.stat_210067635@T1` | -1.39055 |
| `desecrated.stat_666077204` | 0.45250 |
| `rune.stat_3885405204` | -0.44615 |
| `explicit.stat_3261801346@T1` | -0.35678 |
| `explicit.stat_2694482655@T1` | -0.34881 |
| `explicit.stat_55876295@T1` | -0.34551 |

### weapon.crossbow — n=6019, R²=-1.4428

intercept: `3.5028`  ·  log_price: True  ·  ilvl: `-0.04425`  ·  n_mods: `-0.00076`  ·  n_top_tier: `0.65191`  ·  corrupted: `0.02208`  ·  n_sockets: `0.00572`  ·  quality: `-0.00123`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 1.71461 |
| `explicit.stat_709508406@T1` | 1.60378 |
| `explicit.stat_2250681686@T2` | -1.57020 |
| `explicit.stat_1037193709@T1` | 1.54994 |
| `explicit.stat_1202301673@T1` | 1.44112 |
| `explicit.stat_691932474@T1` | -1.32306 |
| `crafted.stat_3035140377` | 1.10599 |
| `explicit.stat_3336890334@T1` | 0.97717 |
| `explicit.stat_2250681686` | 0.92561 |
| `explicit.stat_1202301673@T2` | -0.76261 |
| `explicit.stat_669069897@T2` | -0.75686 |
| `explicit.stat_669069897@T1` | -0.74850 |

### flask.charm — n=1783, R²=-0.2056

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_2541588185@T2` | 0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `explicit.stat_1366840608@T2` | 0.00001 |
| `explicit.stat_2365392475@T2` | 0.00001 |
| `explicit.stat_3849649145` | -0.00001 |
| `explicit.stat_3196823591@T2` | 0.00001 |
| `implicit.stat_4010341289` | -0.00001 |
| `explicit.stat_828533480@T2` | 0.00001 |
| `implicit.stat_2016937536` | 0.00000 |
| `implicit.stat_585126960` | -0.00000 |
| `explicit.stat_280890192` | -0.00000 |

### weapon.warstaff — n=1509, R²=0.0

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

### weapon.sceptre — n=1508, R²=0.0

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

### weapon.staff — n=1427, R²=0.0

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

### weapon.spear — n=1364, R²=0.0

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

### armour.focus — n=1097, R²=0.0

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

### armour.quiver — n=1061, R²=0.0

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

### armour.shield — n=954, R²=0.0

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

### weapon.twomace — n=770, R²=0.0

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

- … **Emerald** — 6120 listings (6120 priced) [0.7–856.7 ex]
- … **Sapphire** — 6060 listings (6060 priced) [0.7–856.7 ex]
- … **Ruby** — 4824 listings (4824 priced) [0.3–856.7 ex]
- … **Utility Belt** — 3622 listings (3622 priced) [0.3–5014962.3 ex]
- … **Stellar Amulet** — 2716 listings (2716 priced) [0.3–38371.8 ex]
- … **Prismatic Ring** — 2387 listings (2387 priced) [0.3–856.7 ex]
- … **Gold Amulet** — 2379 listings (2379 priced) [0.7–856.7 ex]
- … **Solar Amulet** — 2379 listings (2379 priced) [1.0–856.7 ex]
- … **Dueling Wand** — 2337 listings (2337 priced) [1.0–856.7 ex]
- … **Amethyst Ring** — 2268 listings (2268 priced) [0.8–856.7 ex]
- … **Gold Ring** — 2211 listings (2211 priced) [0.5–856.7 ex]
- … **Topaz Ring** — 1808 listings (1808 priced) [1.0–856.7 ex]
- … **Obliterator Bow** — 1793 listings (1793 priced) [0.6–856.7 ex]
- … **Sapphire Ring** — 1790 listings (1790 priced) [0.9–856.7 ex]
- … **Plate Belt** — 1784 listings (1784 priced) [1.0–856.7 ex]
- … **Ruby Ring** — 1749 listings (1749 priced) [0.6–856.7 ex]
- … **Heavy Belt** — 1670 listings (1670 priced) [0.5–856.7 ex]
- … **Lapis Amulet** — 1617 listings (1617 priced) [0.6–856.7 ex]
- … **Amber Amulet** — 1576 listings (1576 priced) [0.7–856.7 ex]
- … **Ancestral Tiara** — 1575 listings (1575 priced) [1.0–856.7 ex]
- … **Jade Amulet** — 1550 listings (1550 priced) [0.7–856.7 ex]
- … **Unset Ring** — 1426 listings (1426 priced) [1.0–856.7 ex]
- … **Bloodstone Amulet** — 1400 listings (1400 priced) [1.0–856.7 ex]
- … **Pearl Ring** — 1386 listings (1386 priced) [0.8–856.7 ex]
- … **Lunar Amulet** — 1384 listings (1384 priced) [0.8–856.7 ex]

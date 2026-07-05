# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-05T02:11:40+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **140036** (140036 priced in exalted)
- Distinct bases: 895 · distinct mods: 2284 · mod rows: 669140
- Sold signals: **35794** sold · 58648 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-05T02:05:50+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.56** (median |log error| 2.0225)
- Within ±30% of asking price: **34%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 63% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.08** · typical error ×16.01 · ±30% 20% · n=18902
- Premium segment (60ex+): skill **+0.08** · typical error ×108.84 · ±30% 0% · n=10736
- Sold listings (clearing prices): skill **+0.06** · typical error ×19.78 · ±30% 27% · n=6882

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 2442 | ×7.24 | 5% | -0.02 | -0.02 |
| accessory.amulet | 2342 | ×22.20 | 10% | -0.05 | -0.10 |
| accessory.belt | 2215 | ×9.35 | 27% | +0.03 | +0.06 |
| armour.chest | 2176 | ×6.00 | 42% | -0.00 | -0.03 |
| armour.helmet | 2162 | ×6.00 | 40% | -0.01 | -0.01 |
| armour.gloves | 2022 | ×10.00 | 37% | -0.00 | -0.02 |
| armour.boots | 2017 | ×10.00 | 38% | -0.01 | -0.01 |
| jewel | 1910 | ×7.82 | 7% | -0.02 | -0.00 |
| other | 1875 | ×9.94 | 36% | +0.41 | +0.38 |
| weapon.wand | 1499 | ×8.99 | 36% | +0.03 | +0.12 |
| weapon.bow | 1232 | ×8.26 | 38% | +0.07 | +0.07 |
| weapon.crossbow | 1207 | ×7.98 | 35% | +0.06 | +0.10 |
| weapon.sceptre | 297 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.staff | 281 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.warstaff | 275 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.spear | 270 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.focus | 220 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 215 | ×1.00 | 96% | +0.00 | +0.00 |
| armour.shield | 185 | ×1.00 | 95% | +0.00 | +0.00 |
| weapon.twomace | 141 | ×1.00 | 96% | +0.00 | +0.00 |
| flask.charm | 112 | ×1.00 | 100% | n/a | - |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=16940, R²=-0.4033

intercept: `1.5789`  ·  log_price: True  ·  ilvl: `0.00078`  ·  n_mods: `0.03360`  ·  n_top_tier: `0.29701`  ·  corrupted: `3.78816`  ·  n_sockets: `-0.01573`  ·  quality: `-0.00139`

| stat_id | coef |
|---|---|
| `explicit.stat_2891184298@T1` | 3.39913 |
| `explicit.stat_101878827@T1` | 3.05146 |
| `explicit.stat_1589917703@T1` | -1.19863 |
| `explicit.stat_2974417149@T1` | 1.19732 |
| `explicit.stat_3141070085@T1` | 0.71882 |
| `explicit.stat_2968503605@T1` | 0.49248 |
| `explicit.stat_3917489142@T1` | 0.41152 |
| `explicit.stat_1589917703` | 0.39136 |
| `implicit.stat_1379411836` | -0.27769 |
| `explicit.stat_789117908@T1` | -0.22833 |
| `implicit.stat_3879011313` | 0.22588 |
| `implicit.stat_4041853756` | 0.22381 |

### accessory.ring — n=11177, R²=-1.8065

intercept: `3.6257`  ·  log_price: True  ·  ilvl: `-0.03134`  ·  n_mods: `-0.10345`  ·  n_top_tier: `-0.08272`  ·  corrupted: `0.63026`  ·  n_sockets: `3.06948`  ·  quality: `0.03175`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T2` | 3.29340 |
| `explicit.stat_707457662@T1` | 3.23849 |
| `explicit.stat_1368271171@T1` | -1.23498 |
| `explicit.stat_1379411836@T1` | 1.09101 |
| `explicit.stat_1368271171@T2` | -1.02039 |
| `explicit.stat_1573130764@T1` | -1.01559 |
| `explicit.stat_736967255@T2` | 0.95154 |
| `explicit.stat_1263695895@T1` | 0.81371 |
| `explicit.stat_3962278098@T1` | -0.77626 |
| `explicit.stat_1379411836@T2` | 0.61941 |
| `explicit.stat_736967255@T1` | 0.60670 |
| `explicit.stat_2144192055@T1` | -0.59645 |

### accessory.amulet — n=11011, R²=-2.3773

intercept: `4.2381`  ·  log_price: True  ·  ilvl: `-0.05181`  ·  n_mods: `-0.07960`  ·  n_top_tier: `0.89925`  ·  corrupted: `0.03158`  ·  n_sockets: `0.07315`  ·  quality: `0.15330`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T2` | -2.54178 |
| `explicit.stat_983749596@T1` | -2.18852 |
| `explicit.stat_983749596@T2` | -1.99683 |
| `explicit.stat_1202301673@T2` | 1.93362 |
| `explicit.stat_803737631@T1` | -1.58390 |
| `explicit.stat_4080418644@T1` | -1.37849 |
| `explicit.stat_1671376347@T2` | -1.36651 |
| `explicit.stat_2923486259@T1` | -1.35273 |
| `explicit.stat_3261801346@T1` | -1.31508 |
| `explicit.stat_3325883026@T1` | -1.31296 |
| `explicit.stat_2974417149@T1` | -1.31125 |
| `explicit.stat_803737631@T2` | -1.30911 |

### accessory.belt — n=10295, R²=-1.2814

intercept: `3.6828`  ·  log_price: True  ·  ilvl: `-0.04485`  ·  n_mods: `-0.02085`  ·  n_top_tier: `-0.05587`  ·  corrupted: `0.06419`  ·  n_sockets: `-0.09616`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 2.09740 |
| `crafted.stat_3249412463` | 2.03682 |
| `explicit.stat_2923486259@T2` | 0.85224 |
| `explicit.stat_1836676211@T1` | 0.69907 |
| `explicit.stat_3372524247@T1` | 0.26453 |
| `explicit.stat_1671376347@T1` | 0.15790 |
| `explicit.stat_4220027924@T1` | 0.13907 |
| `explicit.stat_2639966148` | 0.11072 |
| `explicit.stat_3299347043@T1` | -0.10626 |
| `explicit.stat_3585532255@T2` | 0.10118 |
| `explicit.stat_3585532255@T1` | 0.09889 |
| `explicit.stat_1570770415@T1` | 0.08987 |

### armour.chest — n=10035, R²=-0.2425

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.01922`  ·  corrupted: `0.00005`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_4220027924` | -0.03185 |
| `desecrated.stat_3372524247` | -0.03074 |
| `pseudo.total_ele_res` | 0.02985 |
| `explicit.stat_1671376347` | -0.02985 |
| `explicit.stat_3372524247` | -0.02985 |
| `explicit.stat_4220027924` | -0.02985 |
| `implicit.stat_4220027924` | -0.02985 |
| `implicit.stat_3372524247` | -0.02985 |
| `implicit.stat_1671376347` | -0.02985 |
| `rune.stat_1671376347` | -0.02985 |
| `rune.stat_4220027924` | -0.02985 |
| `rune.stat_3372524247` | -0.02985 |

### armour.helmet — n=9900, R²=-0.2327

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.19306`  ·  corrupted: `0.00054`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 0.76823 |
| `explicit.stat_3321629045@T1` | -0.19309 |
| `explicit.stat_803737631@T2` | -0.19308 |
| `explicit.stat_1062208444@T2` | -0.19307 |
| `explicit.stat_3484657501@T2` | -0.19307 |
| `explicit.stat_53045048@T2` | -0.19307 |
| `explicit.stat_4220027924@T2` | -0.19307 |
| `explicit.stat_3484657501@T1` | -0.19307 |
| `explicit.stat_2451402625@T2` | -0.19307 |
| `explicit.stat_3325883026@T1` | -0.19307 |
| `explicit.stat_3325883026@T2` | -0.19307 |
| `explicit.stat_2451402625@T1` | -0.19306 |

### jewel — n=9620, R²=-0.9144

intercept: `-1.2314`  ·  log_price: True  ·  ilvl: `0.03479`  ·  n_mods: `0.17897`  ·  n_top_tier: `-0.41638`  ·  corrupted: `0.46678`

| stat_id | coef |
|---|---|
| `explicit.stat_2301718443@T1` | -4.62512 |
| `explicit.stat_2011656677@T1` | 3.79437 |
| `explicit.stat_280731498@T1` | 3.41454 |
| `explicit.stat_1062710370@T1` | -3.14936 |
| `explicit.stat_795138349@T1` | -2.88598 |
| `explicit.stat_1405298142@T1` | 2.71039 |
| `explicit.stat_1459321413@T1` | 2.60406 |
| `explicit.stat_3759663284@T1` | -2.52969 |
| `explicit.stat_3851254963@T1` | 2.40670 |
| `explicit.stat_3028809864@T1` | 2.25166 |
| `explicit.stat_1854213750@T1` | 2.22975 |
| `explicit.stat_1869147066@T1` | 2.17548 |

### armour.boots — n=9288, R²=-0.2178

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00994`  ·  corrupted: `0.00002`  ·  n_sockets: `-0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1671376347` | 0.01226 |
| `desecrated.stat_2250533757@T2` | -0.01018 |
| `explicit.stat_2339757871@T1` | -0.01014 |
| `explicit.stat_99927264@T2` | -0.00996 |
| `explicit.stat_3639275092@T1` | -0.00996 |
| `explicit.stat_2451402625@T2` | -0.00996 |
| `explicit.stat_1062208444@T2` | -0.00996 |
| `explicit.stat_1062208444@T1` | -0.00996 |
| `explicit.stat_3362812763@T2` | -0.00996 |
| `explicit.stat_3033371881@T2` | -0.00995 |
| `explicit.stat_2923486259@T2` | -0.00995 |
| `explicit.stat_53045048@T2` | -0.00995 |

### armour.gloves — n=9219, R²=-0.2454

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00586`  ·  corrupted: `0.00005`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.16921 |
| `desecrated.stat_3299347043` | 0.01071 |
| `explicit.stat_2339757871@T1` | -0.00622 |
| `explicit.stat_4015621042@T1` | -0.00589 |
| `explicit.stat_2797971005@T2` | -0.00589 |
| `explicit.stat_3484657501@T2` | -0.00588 |
| `explicit.stat_1062208444@T1` | -0.00588 |
| `explicit.stat_3695891184@T1` | -0.00588 |
| `explicit.stat_124859000@T2` | -0.00588 |
| `explicit.stat_4080418644@T1` | -0.00587 |
| `explicit.stat_3917489142@T2` | -0.00587 |
| `explicit.stat_681332047@T1` | -0.00587 |

### weapon.wand — n=6910, R²=-1.6786

intercept: `3.3687`  ·  log_price: True  ·  ilvl: `-0.04203`  ·  n_mods: `-0.00977`  ·  n_top_tier: `0.14844`  ·  corrupted: `-0.00875`  ·  n_sockets: `-0.00185`  ·  quality: `0.01844`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.99204 |
| `explicit.stat_591105508@T1` | 2.19482 |
| `explicit.stat_1545858329@T1` | 2.15446 |
| `explicit.stat_4226189338@T1` | 2.15329 |
| `explicit.stat_2254480358@T1` | 2.09678 |
| `explicit.stat_2968503605@T1` | 1.43174 |
| `crafted.stat_124131830` | 1.12809 |
| `explicit.stat_1600707273@T2` | 0.88149 |
| `explicit.stat_736967255@T2` | 0.49283 |
| `explicit.stat_2768835289@T2` | -0.25338 |
| `rune.stat_3278136794` | 0.23427 |
| `explicit.stat_3962278098@T2` | -0.21467 |

### weapon.bow — n=5809, R²=-1.6367

intercept: `3.3513`  ·  log_price: True  ·  ilvl: `-0.04179`  ·  n_mods: `-0.01937`  ·  n_top_tier: `0.26281`  ·  corrupted: `-0.05998`  ·  n_sockets: `0.00211`  ·  quality: `-0.00166`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -5.68280 |
| `explicit.stat_2463230181@T1` | 2.03995 |
| `explicit.stat_1509134228@T1` | 1.93203 |
| `explicit.stat_518292764@T1` | 1.85446 |
| `crafted.stat_3035140377` | 1.30073 |
| `rune.stat_3885405204` | -0.69320 |
| `desecrated.stat_210067635@T1` | -0.37974 |
| `explicit.stat_1202301673@T1` | 0.37962 |
| `explicit.stat_1940865751@T1` | -0.34222 |
| `desecrated.stat_666077204` | 0.33712 |
| `explicit.stat_2694482655@T1` | -0.33298 |
| `explicit.stat_3261801346@T1` | -0.31780 |

### weapon.crossbow — n=5521, R²=-1.5123

intercept: `3.4372`  ·  log_price: True  ·  ilvl: `-0.04296`  ·  n_mods: `-0.00255`  ·  n_top_tier: `0.12463`  ·  corrupted: `-0.02762`  ·  n_sockets: `0.01504`  ·  quality: `-0.00169`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -3.33758 |
| `explicit.stat_2250681686` | 3.22420 |
| `desecrated.stat_3131442032@T1` | -2.25114 |
| `desecrated.stat_1365232741@T1` | -2.25114 |
| `explicit.stat_709508406@T1` | 2.16775 |
| `explicit.stat_1037193709@T1` | 2.14025 |
| `explicit.stat_3336890334@T1` | 2.09195 |
| `explicit.stat_1509134228@T1` | 1.81538 |
| `crafted.stat_3035140377` | 1.17071 |
| `explicit.stat_691932474@T1` | -1.10895 |
| `explicit.stat_1202301673@T1` | 1.09973 |
| `explicit.stat_1263695895@T1` | 0.89434 |

### weapon.sceptre — n=1406, R²=0.0

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

### weapon.warstaff — n=1369, R²=0.0

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
| `desecrated.stat_3261801346` | 0.00000 |

### flask.charm — n=1309, R²=-0.3393

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_1120862500@T2` | -0.00002 |
| `explicit.stat_1873752457@T2` | -0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `explicit.stat_388617051@T2` | -0.00001 |
| `explicit.stat_828533480@T1` | -0.00001 |
| `implicit.stat_4010341289` | -0.00001 |
| `explicit.stat_3849649145` | -0.00001 |
| `explicit.stat_2541588185@T2` | 0.00001 |
| `explicit.stat_1873752457@T1` | -0.00001 |
| `explicit.stat_828533480@T2` | -0.00001 |
| `implicit.stat_1810482573` | -0.00001 |

### weapon.staff — n=1297, R²=0.0

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

### weapon.spear — n=1282, R²=0.0

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

### armour.focus — n=1041, R²=0.0

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

### armour.quiver — n=997, R²=0.0

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

### armour.shield — n=908, R²=0.0

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

### weapon.twomace — n=720, R²=0.0

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

- … **Emerald** — 4935 listings (4935 priced) [0.8–856.7 ex]
- … **Sapphire** — 4888 listings (4888 priced) [0.7–856.7 ex]
- … **Ruby** — 3930 listings (3930 priced) [0.3–856.7 ex]
- … **Utility Belt** — 3208 listings (3208 priced) [0.3–4682873.9 ex]
- … **Stellar Amulet** — 2410 listings (2410 priced) [0.3–38371.8 ex]
- … **Dueling Wand** — 2157 listings (2157 priced) [1.0–856.7 ex]
- … **Prismatic Ring** — 2043 listings (2043 priced) [0.3–856.7 ex]
- … **Gold Amulet** — 2041 listings (2041 priced) [0.6–856.7 ex]
- … **Solar Amulet** — 2038 listings (2038 priced) [1.0–856.7 ex]
- … **Amethyst Ring** — 1938 listings (1938 priced) [0.8–856.7 ex]
- … **Gold Ring** — 1856 listings (1856 priced) [0.8–856.7 ex]
- … **Obliterator Bow** — 1635 listings (1635 priced) [0.6–856.7 ex]
- … **Plate Belt** — 1581 listings (1581 priced) [1.0–856.7 ex]
- … **Topaz Ring** — 1543 listings (1543 priced) [1.0–856.7 ex]
- … **Sapphire Ring** — 1519 listings (1519 priced) [0.9–856.7 ex]
- … **Ruby Ring** — 1470 listings (1470 priced) [0.6–856.7 ex]
- … **Heavy Belt** — 1469 listings (1469 priced) [0.5–856.7 ex]
- … **Ancestral Tiara** — 1408 listings (1408 priced) [1.0–856.7 ex]
- … **Lapis Amulet** — 1370 listings (1370 priced) [0.6–856.7 ex]
- … **Amber Amulet** — 1326 listings (1326 priced) [0.6–856.7 ex]
- … **Jade Amulet** — 1309 listings (1309 priced) [0.6–856.7 ex]
- … **Galvanic Wand** — 1231 listings (1231 priced) [0.5–856.7 ex]
- … **Siphoning Wand** — 1227 listings (1227 priced) [1.0–856.7 ex]
- … **Unset Ring** — 1194 listings (1194 priced) [1.0–856.7 ex]
- … **Bloodstone Amulet** — 1189 listings (1189 priced) [1.0–856.7 ex]

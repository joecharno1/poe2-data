# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-05T21:43:55+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **186181** (186156 priced in exalted)
- Distinct bases: 916 · distinct mods: 2461 · mod rows: 881639
- Sold signals: **39341** sold · 97591 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-05T21:36:51+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×9.58** (median |log error| 2.2601)
- Within ±30% of asking price: **24%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 72% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×38.90 · ±30% 6% · n=25478
- Premium segment (60ex+): skill **+0.11** · typical error ×233.01 · ±30% 0% · n=14768
- Sold listings (clearing prices): skill **+0.34** · typical error ×6.70 · ±30% 0% · n=10

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 3478 | ×7.46 | 5% | +0.02 | +0.01 |
| accessory.amulet | 3355 | ×42.91 | 20% | -0.02 | -0.03 |
| jewel | 2915 | ×8.08 | 6% | +0.02 | +0.07 |
| accessory.belt | 2894 | ×9.62 | 24% | +0.03 | +0.09 |
| armour.chest | 2849 | ×9.13 | 25% | +0.04 | +0.09 |
| armour.helmet | 2773 | ×9.32 | 22% | +0.04 | +0.09 |
| armour.boots | 2603 | ×9.25 | 24% | +0.03 | +0.06 |
| armour.gloves | 2544 | ×9.32 | 23% | +0.01 | +0.05 |
| other | 2510 | ×6.40 | 37% | +0.07 | +0.16 |
| weapon.wand | 1824 | ×9.55 | 32% | +0.04 | +0.10 |
| weapon.bow | 1508 | ×9.33 | 28% | +0.06 | +0.09 |
| weapon.crossbow | 1435 | ×9.38 | 28% | +0.08 | +0.12 |
| weapon.warstaff | 394 | ×1.00 | 63% | +0.00 | +0.00 |
| weapon.sceptre | 375 | ×1.00 | 56% | +0.00 | +0.00 |
| weapon.staff | 369 | ×3.00 | 47% | +0.00 | +0.00 |
| weapon.spear | 339 | ×1.00 | 53% | +0.00 | +0.00 |
| armour.quiver | 291 | ×40.00 | 36% | +0.00 | +0.00 |
| armour.focus | 289 | ×17.00 | 36% | +0.00 | +0.00 |
| armour.shield | 246 | ×17.00 | 28% | +0.00 | +0.00 |
| weapon.twomace | 210 | ×85.50 | 18% | +0.00 | +0.00 |
| flask.charm | 202 | ×1.00 | 72% | -0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=22307, R²=-0.4767

intercept: `1.5465`  ·  log_price: True  ·  ilvl: `0.00214`  ·  n_mods: `0.04810`  ·  n_top_tier: `0.24422`  ·  corrupted: `0.33124`  ·  n_sockets: `-0.04079`  ·  quality: `-0.00448`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.41427 |
| `explicit.stat_2974417149@T1` | 0.34170 |
| `implicit.stat_1379411836` | -0.29106 |
| `explicit.stat_2106365538@T1` | 0.28497 |
| `explicit.stat_1050105434@T1` | -0.27710 |
| `explicit.stat_124131830` | -0.25571 |
| `implicit.stat_3182714256` | 0.25072 |
| `implicit.stat_718638445` | 0.25064 |
| `explicit.stat_2891184298@T1` | 0.24990 |
| `implicit.stat_4041853756` | 0.21481 |
| `implicit.stat_3879011313` | 0.21460 |
| `implicit.stat_958696139` | -0.15441 |

### accessory.ring — n=15845, R²=-1.4613

intercept: `5.2355`  ·  log_price: True  ·  ilvl: `-0.04557`  ·  n_mods: `-0.27369`  ·  n_top_tier: `-0.14782`  ·  corrupted: `0.98196`  ·  n_sockets: `2.58683`  ·  quality: `0.00842`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.61141 |
| `explicit.stat_707457662@T2` | 3.31634 |
| `explicit.stat_1379411836@T1` | -2.76848 |
| `explicit.stat_1379411836@T2` | -1.46699 |
| `explicit.stat_3299347043@T1` | -1.30909 |
| `explicit.stat_1573130764@T1` | -1.21831 |
| `explicit.stat_3032590688@T2` | 1.19252 |
| `explicit.stat_1754445556@T1` | 1.16375 |
| `explicit.stat_2557965901@T1` | 1.06168 |
| `explicit.stat_4067062424@T2` | 0.96485 |
| `explicit.stat_736967255@T1` | 0.93936 |
| `explicit.stat_789117908@T2` | 0.83905 |

### accessory.amulet — n=15265, R²=-2.1758

intercept: `4.3527`  ·  log_price: True  ·  ilvl: `-0.05279`  ·  n_mods: `-0.02681`  ·  n_top_tier: `0.21981`  ·  corrupted: `0.10183`  ·  n_sockets: `0.01963`  ·  quality: `-0.03448`

| stat_id | coef |
|---|---|
| `explicit.stat_3981240776@T2` | 1.62729 |
| `explicit.stat_983749596@T1` | -1.26048 |
| `explicit.stat_124131830` | 1.22677 |
| `explicit.stat_2748665614@T1` | -1.08046 |
| `explicit.stat_983749596@T2` | -0.98448 |
| `explicit.stat_1202301673@T2` | 0.83789 |
| `explicit.stat_2748665614@T2` | -0.78911 |
| `explicit.stat_1202301673` | 0.51601 |
| `explicit.stat_1671376347@T2` | -0.34008 |
| `explicit.stat_4080418644@T1` | -0.32985 |
| `explicit.stat_4080418644@T2` | -0.31713 |
| `explicit.stat_3261801346@T1` | -0.30038 |

### jewel — n=14759, R²=-0.765

intercept: `-1.2403`  ·  log_price: True  ·  ilvl: `0.03526`  ·  n_mods: `0.21927`  ·  n_top_tier: `-0.34344`  ·  corrupted: `0.37487`  ·  quality: `0.22081`

| stat_id | coef |
|---|---|
| `explicit.stat_1869147066@T1` | 4.51356 |
| `explicit.stat_1316278494@T1` | -3.50574 |
| `explicit.stat_3714003708@T1` | -3.34441 |
| `explicit.stat_2594634307@T1` | 3.20586 |
| `explicit.stat_2456523742@T1` | 2.82384 |
| `explicit.stat_153777645@T1` | 2.71456 |
| `explicit.stat_1569101201@T1` | 2.71329 |
| `explicit.stat_2106365538@T1` | -2.66035 |
| `explicit.stat_1569159338@T1` | 2.61740 |
| `explicit.stat_416040624@T1` | -2.22962 |
| `explicit.stat_627767961@T1` | 2.21250 |
| `explicit.stat_1829102168@T1` | -2.18692 |

### accessory.belt — n=13274, R²=-1.3225

intercept: `3.6446`  ·  log_price: True  ·  ilvl: `-0.04376`  ·  n_mods: `-0.02377`  ·  n_top_tier: `-0.04005`  ·  corrupted: `0.21204`  ·  n_sockets: `-0.11573`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.88455 |
| `explicit.stat_2923486259@T1` | 1.03495 |
| `explicit.stat_1836676211@T1` | 0.27439 |
| `explicit.stat_3299347043@T1` | -0.24280 |
| `explicit.stat_2923486259@T2` | 0.24219 |
| `explicit.stat_4220027924@T1` | 0.19367 |
| `explicit.stat_3372524247@T1` | 0.13824 |
| `implicit.stat_731781020` | -0.13255 |
| `explicit.stat_1671376347@T1` | 0.11389 |
| `explicit.stat_3299347043@T2` | -0.10689 |
| `explicit.stat_3585532255@T1` | 0.09784 |
| `explicit.stat_1570770415@T1` | 0.09170 |

### armour.chest — n=13017, R²=-1.3407

intercept: `4.0179`  ·  log_price: True  ·  ilvl: `-0.04960`  ·  n_mods: `-0.01981`  ·  n_top_tier: `0.42962`  ·  corrupted: `0.14278`  ·  n_sockets: `0.00054`  ·  quality: `0.00536`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.28693 |
| `explicit.stat_3981240776@T1` | 1.68088 |
| `explicit.stat_3981240776@T2` | 0.96774 |
| `explicit.stat_4015621042@T1` | -0.53579 |
| `explicit.stat_4080418644@T2` | -0.52251 |
| `explicit.stat_4080418644@T1` | -0.50617 |
| `explicit.stat_4015621042@T2` | -0.49835 |
| `explicit.stat_328541901@T1` | -0.49667 |
| `explicit.stat_4220027924@T2` | -0.48249 |
| `explicit.stat_3261801346@T2` | -0.48079 |
| `explicit.stat_2339757871@T1` | -0.47959 |
| `explicit.stat_3325883026@T2` | -0.47929 |

### armour.helmet — n=12805, R²=-1.3477

intercept: `4.6674`  ·  log_price: True  ·  ilvl: `-0.05834`  ·  n_mods: `-0.02415`  ·  n_top_tier: `0.55903`  ·  corrupted: `0.49040`  ·  n_sockets: `-0.00889`  ·  quality: `0.02669`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.09242 |
| `crafted.stat_3917489142@T1` | 2.13068 |
| `explicit.stat_53045048@T1` | -0.68826 |
| `explicit.stat_1263695895@T1` | -0.68283 |
| `explicit.stat_3033371881@T1` | -0.68073 |
| `explicit.stat_3033371881@T2` | -0.65575 |
| `explicit.stat_4015621042@T2` | -0.64395 |
| `explicit.stat_2162097452@T2` | -0.64331 |
| `explicit.stat_4052037485@T2` | -0.63224 |
| `explicit.stat_53045048@T2` | -0.62592 |
| `explicit.stat_1062208444@T2` | -0.60555 |
| `explicit.stat_803737631@T2` | -0.60515 |

### armour.boots — n=12025, R²=-1.1707

intercept: `4.0183`  ·  log_price: True  ·  ilvl: `-0.04961`  ·  n_mods: `-0.02860`  ·  n_top_tier: `0.25896`  ·  corrupted: `0.21998`  ·  n_sockets: `0.01285`  ·  quality: `0.04187`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.15940 |
| `explicit.stat_2250533757@T1` | 1.95396 |
| `explicit.stat_4220027924@T1` | 0.97372 |
| `explicit.stat_3917489142@T2` | -0.41526 |
| `explicit.stat_3362812763@T1` | -0.35758 |
| `explicit.stat_2160282525@T1` | -0.34548 |
| `rune.stat_836936635` | -0.34449 |
| `explicit.stat_99927264@T1` | -0.33902 |
| `explicit.stat_4015621042@T2` | -0.33761 |
| `explicit.stat_2923486259@T2` | -0.33427 |
| `explicit.stat_1062208444@T2` | -0.32895 |
| `explicit.stat_4052037485@T2` | -0.32781 |

### armour.gloves — n=11841, R²=-1.4636

intercept: `3.9842`  ·  log_price: True  ·  ilvl: `-0.05063`  ·  n_mods: `0.00104`  ·  n_top_tier: `0.93676`  ·  corrupted: `-0.08774`  ·  n_sockets: `-0.00466`  ·  quality: `0.01132`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.86955 |
| `explicit.stat_681332047@T2` | -1.22905 |
| `explicit.stat_681332047@T1` | -1.21209 |
| `explicit.stat_9187492@T2` | -1.09215 |
| `explicit.stat_2797971005@T1` | -1.06386 |
| `explicit.stat_1573130764@T1` | -1.05652 |
| `explicit.stat_124859000@T1` | -1.03186 |
| `explicit.stat_3032590688@T1` | -1.02464 |
| `explicit.stat_2557965901@T1` | -1.02303 |
| `explicit.stat_2797971005@T2` | -1.02186 |
| `explicit.stat_803737631@T2` | -1.01246 |
| `explicit.stat_3484657501@T2` | -1.01164 |

### weapon.wand — n=8479, R²=-1.789

intercept: `3.4251`  ·  log_price: True  ·  ilvl: `-0.04267`  ·  n_mods: `-0.00924`  ·  n_top_tier: `0.47132`  ·  corrupted: `0.03375`  ·  n_sockets: `-0.00501`  ·  quality: `0.01624`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.92630 |
| `explicit.stat_4226189338@T1` | 1.90491 |
| `explicit.stat_591105508@T1` | 1.90029 |
| `explicit.stat_2254480358@T1` | 1.89372 |
| `explicit.stat_1545858329@T1` | 1.63402 |
| `explicit.stat_736967255@T2` | 1.43128 |
| `crafted.stat_124131830` | 0.81158 |
| `explicit.stat_1600707273@T1` | 0.69863 |
| `explicit.stat_2768835289@T2` | -0.60931 |
| `explicit.stat_3962278098@T2` | -0.55987 |
| `explicit.stat_737908626@T1` | -0.53703 |
| `explicit.stat_2968503605@T2` | -0.52194 |

### weapon.bow — n=7040, R²=-1.6544

intercept: `3.4326`  ·  log_price: True  ·  ilvl: `-0.04255`  ·  n_mods: `-0.01846`  ·  n_top_tier: `0.35221`  ·  corrupted: `-0.05463`  ·  n_sockets: `0.00407`  ·  quality: `0.00574`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -4.89481 |
| `desecrated.stat_210067635@T1` | -2.79087 |
| `explicit.stat_2463230181@T1` | 1.92632 |
| `explicit.stat_1202301673@T1` | 1.85837 |
| `explicit.stat_1509134228@T1` | 1.80607 |
| `explicit.stat_518292764@T1` | 1.56416 |
| `crafted.stat_3035140377` | 1.55819 |
| `explicit.stat_55876295@T1` | -0.47186 |
| `explicit.stat_55876295@T2` | -0.42914 |
| `explicit.stat_821021828@T1` | -0.42439 |
| `explicit.stat_2694482655@T1` | -0.41900 |
| `desecrated.stat_666077204` | 0.41628 |

### weapon.crossbow — n=6638, R²=-1.5409

intercept: `3.4736`  ·  log_price: True  ·  ilvl: `-0.04352`  ·  n_mods: `-0.00106`  ·  n_top_tier: `0.41495`  ·  corrupted: `-0.04495`  ·  n_sockets: `0.00573`  ·  quality: `0.00073`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 2.11618 |
| `explicit.stat_709508406@T1` | 1.84589 |
| `explicit.stat_1037193709@T1` | 1.83680 |
| `explicit.stat_1202301673@T1` | 1.71553 |
| `explicit.stat_2250681686@T2` | -1.40137 |
| `crafted.stat_3035140377` | 1.15882 |
| `explicit.stat_2250681686` | 1.01780 |
| `explicit.stat_691932474@T1` | -0.76393 |
| `rune.stat_2246411426` | -0.66009 |
| `rune.stat_55876295` | 0.65263 |
| `explicit.stat_1202301673@T2` | -0.54040 |
| `explicit.stat_669069897@T1` | -0.48681 |

### flask.charm — n=2419, R²=-0.1028

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00003 |
| `explicit.stat_2566921799` | 0.00001 |
| `explicit.stat_1873752457@T2` | -0.00001 |
| `explicit.stat_3849649145` | -0.00001 |
| `explicit.stat_2541588185@T2` | 0.00001 |
| `explicit.stat_1366840608@T2` | 0.00001 |
| `implicit.stat_2016937536` | 0.00000 |
| `explicit.stat_828533480@T1` | -0.00000 |
| `explicit.stat_1873752457@T1` | -0.00000 |
| `implicit.stat_585126960` | -0.00000 |
| `explicit.stat_3246948616` | -0.00000 |
| `implicit.stat_3676540188` | -0.00000 |

### weapon.warstaff — n=1851, R²=-0.0255

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1509134228` | 0.00001 |
| `rune.stat_1039491398` | -0.00001 |
| `explicit.stat_821021828@T1` | -0.00001 |
| `explicit.stat_709508406@T1` | 0.00001 |
| `explicit.stat_1509134228@T2` | 0.00001 |
| `explicit.stat_210067635@T1` | -0.00001 |
| `explicit.stat_3695891184@T1` | -0.00000 |
| `explicit.stat_2694482655@T1` | 0.00000 |
| `explicit.stat_669069897@T2` | -0.00000 |
| `explicit.stat_328541901@T1` | -0.00000 |
| `explicit.stat_821021828@T2` | -0.00000 |
| `explicit.stat_328541901@T2` | -0.00000 |

### weapon.sceptre — n=1787, R²=-0.0413

intercept: `-0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_4080418644@T2` | -0.00001 |
| `explicit.stat_1250712710@T1` | -0.00001 |
| `explicit.stat_3057012405@T1` | -0.00001 |
| `explicit.stat_3850614073@T2` | -0.00001 |
| `explicit.stat_3639275092@T1` | -0.00001 |
| `explicit.stat_1263695895@T1` | 0.00001 |
| `explicit.stat_2162097452@T2` | -0.00001 |
| `explicit.stat_2347036682@T1` | -0.00001 |
| `explicit.stat_849987426@T1` | -0.00000 |
| `explicit.stat_789117908@T1` | -0.00000 |
| `explicit.stat_1574590649@T1` | -0.00000 |
| `explicit.stat_289128254@T1` | -0.00000 |

### weapon.staff — n=1765, R²=-0.0552

intercept: `-0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T2` | 0.00002 |
| `explicit.stat_473429811@T1` | 0.00001 |
| `explicit.stat_2254480358@T1` | 0.00001 |
| `explicit.stat_1545858329@T2` | 0.00001 |
| `explicit.stat_1545858329@T1` | 0.00001 |
| `explicit.stat_293638271@T1` | 0.00001 |
| `explicit.stat_1050105434@T2` | 0.00001 |
| `explicit.stat_3695891184@T2` | 0.00001 |
| `explicit.stat_2254480358@T2` | 0.00001 |
| `explicit.stat_2968503605@T2` | 0.00001 |
| `explicit.stat_3639275092@T2` | 0.00001 |
| `explicit.stat_1600707273@T2` | 0.00001 |

### weapon.spear — n=1604, R²=-0.0397

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | -0.00002 |
| `explicit.stat_1263695895@T2` | -0.00001 |
| `explicit.stat_210067635@T1` | 0.00001 |
| `explicit.stat_9187492@T1` | -0.00001 |
| `explicit.stat_709508406@T1` | -0.00001 |
| `explicit.stat_3639275092@T2` | -0.00000 |
| `explicit.stat_2694482655@T1` | 0.00000 |
| `explicit.stat_9187492@T2` | -0.00000 |
| `explicit.stat_3695891184@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1509134228@T1` | 0.00000 |
| `explicit.stat_691932474@T1` | 0.00000 |

### armour.focus — n=1343, R²=0.0648

intercept: `-0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_4015621042` | 0.07386 |
| `explicit.stat_328541901@T2` | -0.00001 |
| `explicit.stat_2768835289@T1` | -0.00001 |
| `explicit.stat_2768835289@T2` | -0.00001 |
| `explicit.stat_3962278098@T2` | 0.00001 |
| `explicit.stat_124131830@T2` | -0.00001 |
| `explicit.stat_3291658075@T2` | -0.00001 |
| `explicit.stat_4220027924@T2` | -0.00001 |
| `explicit.stat_1671376347@T1` | -0.00001 |
| `explicit.stat_3372524247@T1` | -0.00001 |
| `explicit.stat_2974417149@T1` | -0.00001 |
| `explicit.stat_3372524247@T2` | -0.00001 |

### armour.quiver — n=1325, R²=-0.086

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | -0.00004 |
| `explicit.stat_2463230181@T2` | -0.00002 |
| `explicit.stat_3695891184@T1` | 0.00002 |
| `explicit.stat_3695891184@T2` | 0.00001 |
| `explicit.stat_3759663284@T1` | 0.00001 |
| `explicit.stat_4067062424@T2` | 0.00001 |
| `explicit.stat_1754445556@T1` | 0.00001 |
| `explicit.stat_4067062424@T1` | 0.00001 |
| `explicit.stat_1754445556@T2` | 0.00001 |
| `explicit.stat_1241625305@T2` | 0.00001 |
| `explicit.stat_3759663284@T2` | 0.00001 |
| `explicit.stat_803737631@T1` | 0.00001 |

### armour.shield — n=1176, R²=-0.0966

intercept: `-0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00003`  ·  corrupted: `-0.00001`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_4095671657@T1` | 0.00006 |
| `explicit.stat_3676141501@T1` | 0.00006 |
| `explicit.stat_4095671657@T2` | 0.00006 |
| `explicit.stat_3033371881@T1` | 0.00005 |
| `explicit.stat_4052037485@T2` | 0.00005 |
| `explicit.stat_3676141501@T2` | 0.00005 |
| `explicit.stat_2339757871@T2` | 0.00005 |
| `explicit.stat_3033371881@T2` | 0.00005 |
| `explicit.stat_3855016469@T2` | 0.00004 |
| `explicit.stat_1978899297@T1` | 0.00004 |
| `explicit.stat_53045048@T1` | 0.00004 |
| `explicit.stat_4052037485@T1` | 0.00004 |

### weapon.twomace — n=991, R²=-0.1128

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | 0.00002 |
| `explicit.stat_1037193709@T1` | -0.00002 |
| `explicit.stat_1037193709@T2` | -0.00002 |
| `explicit.stat_691932474@T1` | -0.00001 |
| `explicit.stat_2694482655@T1` | -0.00001 |
| `explicit.stat_1940865751@T1` | -0.00001 |
| `explicit.stat_3639275092@T1` | -0.00001 |
| `explicit.stat_1263695895@T2` | 0.00001 |
| `explicit.stat_669069897@T1` | -0.00001 |
| `explicit.stat_1368271171@T1` | -0.00001 |
| `explicit.stat_691932474@T2` | -0.00001 |
| `explicit.stat_3336890334@T2` | 0.00001 |

## Coverage (listings per base)

- … **Emerald** — 7380 listings (7380 priced) [0.7–10970.3 ex]
- … **Sapphire** — 7326 listings (7326 priced) [0.6–3588.3 ex]
- … **Ruby** — 5753 listings (5753 priced) [0.3–7176.6 ex]
- … **Utility Belt** — 4046 listings (4046 priced) [0.3–4555741.7 ex]
- … **Stellar Amulet** — 3087 listings (3087 priced) [0.3–4547453.5 ex]
- … **Prismatic Ring** — 2810 listings (2810 priced) [0.3–3656.8 ex]
- … **Solar Amulet** — 2765 listings (2765 priced) [1.0–4547453.5 ex]
- … **Gold Amulet** — 2760 listings (2760 priced) [0.7–292542.5 ex]
- … **Amethyst Ring** — 2708 listings (2708 priced) [0.8–3656.8 ex]
- … **Dueling Wand** — 2614 listings (2614 priced) [1.0–138957.7 ex]
- … **Gold Ring** — 2597 listings (2597 priced) [0.5–1462.7 ex]
- … **Sapphire Ring** — 2143 listings (2143 priced) [0.9–856.7 ex]
- … **Topaz Ring** — 2127 listings (2127 priced) [1.0–2153.0 ex]
- … **Ruby Ring** — 2067 listings (2067 priced) [1.0–856.7 ex]
- … **Plate Belt** — 2024 listings (2024 priced) [0.6–4547453.5 ex]
- … **Obliterator Bow** — 2008 listings (2006 priced) [0.6–330123.7 ex]
- … **Heavy Belt** — 1950 listings (1950 priced) [0.5–1462.7 ex]
- … **Lapis Amulet** — 1874 listings (1874 priced) [0.6–4547453.5 ex]
- … **Amber Amulet** — 1861 listings (1861 priced) [0.7–4547453.5 ex]
- … **Jade Amulet** — 1842 listings (1842 priced) [0.7–4547453.5 ex]
- … **Ancestral Tiara** — 1828 listings (1826 priced) [0.6–365678.1 ex]
- … **Unset Ring** — 1721 listings (1721 priced) [1.0–856.7 ex]
- … **Bloodstone Amulet** — 1672 listings (1672 priced) [1.0–1435.3 ex]
- … **Pearl Ring** — 1626 listings (1626 priced) [0.6–7176.6 ex]
- … **Azure Amulet** — 1614 listings (1614 priced) [1.0–4306.0 ex]

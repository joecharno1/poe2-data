# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-06T00:49:13+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **194068** (194010 priced in exalted)
- Distinct bases: 918 · distinct mods: 2494 · mod rows: 919089
- Sold signals: **38331** sold · 102168 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-06T00:42:15+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×12.40** (median |log error| 2.5178)
- Within ±30% of asking price: **23%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 73% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.10** · typical error ×36.00 · ±30% 11% · n=27308
- Premium segment (60ex+): skill **+0.10** · typical error ×201.06 · ±30% 0% · n=16126
- Sold listings (clearing prices): skill **+0.34** · typical error ×6.60 · ±30% 0% · n=10

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 3631 | ×8.00 | 5% | +0.02 | +0.03 |
| accessory.amulet | 3484 | ×44.77 | 19% | -0.01 | -0.00 |
| accessory.belt | 2998 | ×9.81 | 23% | +0.04 | +0.08 |
| jewel | 2991 | ×8.31 | 7% | +0.03 | +0.07 |
| armour.chest | 2956 | ×9.18 | 26% | +0.04 | +0.09 |
| armour.helmet | 2884 | ×9.41 | 23% | +0.04 | +0.09 |
| armour.boots | 2696 | ×10.00 | 33% | +0.00 | -0.00 |
| armour.gloves | 2664 | ×10.00 | 30% | -0.00 | -0.00 |
| other | 2596 | ×10.00 | 36% | +0.09 | +0.31 |
| weapon.wand | 1899 | ×9.83 | 31% | +0.04 | +0.07 |
| weapon.bow | 1580 | ×9.61 | 29% | +0.05 | +0.08 |
| weapon.crossbow | 1467 | ×9.62 | 30% | +0.06 | +0.09 |
| weapon.warstaff | 429 | ×45.00 | 29% | +0.00 | +0.00 |
| weapon.sceptre | 413 | ×85.50 | 26% | +0.00 | +0.00 |
| weapon.staff | 402 | ×89.05 | 18% | +0.00 | +0.00 |
| weapon.spear | 375 | ×55.00 | 26% | +0.00 | +0.00 |
| armour.focus | 261 | ×170.44 | 10% | +0.00 | +0.00 |
| armour.quiver | 224 | ×50.00 | 19% | +0.00 | +0.00 |
| flask.charm | 219 | ×1.94 | 49% | -0.00 | +0.00 |
| weapon.twomace | 188 | ×25.00 | 17% | +0.00 | +0.00 |
| armour.shield | 180 | ×40.00 | 14% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=22908, R²=-0.4073

intercept: `1.6091`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00055`  ·  n_top_tier: `0.69219`  ·  corrupted: `2.92976`  ·  n_sockets: `-0.00015`  ·  quality: `-0.00002`

| stat_id | coef |
|---|---|
| `explicit.stat_3141070085@T1` | 5.17910 |
| `explicit.stat_3291658075@T1` | 3.80988 |
| `explicit.stat_1589917703@T1` | 3.52770 |
| `explicit.stat_101878827@T1` | 3.48882 |
| `explicit.stat_2106365538@T1` | 3.37910 |
| `explicit.stat_2891184298@T1` | 3.27710 |
| `explicit.stat_1050105434@T1` | -1.29630 |
| `explicit.stat_2974417149@T1` | 1.09940 |
| `explicit.stat_789117908@T1` | -0.93034 |
| `explicit.stat_3917489142@T1` | 0.72946 |
| `explicit.stat_2968503605@T1` | 0.61221 |
| `explicit.stat_3141070085` | -0.32929 |

### accessory.ring — n=16525, R²=-1.403

intercept: `4.9778`  ·  log_price: True  ·  ilvl: `-0.04266`  ·  n_mods: `-0.26504`  ·  n_top_tier: `-0.14478`  ·  corrupted: `0.90268`  ·  n_sockets: `2.67015`  ·  quality: `0.00999`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 3.19806 |
| `explicit.stat_2557965901@T1` | 2.90833 |
| `explicit.stat_2557965901@T2` | 2.46753 |
| `explicit.stat_1379411836@T1` | -2.10994 |
| `explicit.stat_707457662@T2` | 2.00591 |
| `explicit.stat_3299347043@T1` | -1.43792 |
| `explicit.stat_1573130764@T1` | -1.14808 |
| `explicit.stat_736967255@T1` | 1.06256 |
| `explicit.stat_1379411836@T2` | -1.05226 |
| `explicit.stat_3032590688@T2` | 1.00498 |
| `explicit.stat_1754445556@T1` | 0.91510 |
| `explicit.stat_2923486259@T2` | 0.83304 |

### accessory.amulet — n=15891, R²=-2.1574

intercept: `4.4493`  ·  log_price: True  ·  ilvl: `-0.05433`  ·  n_mods: `-0.02540`  ·  n_top_tier: `0.05980`  ·  corrupted: `0.13049`  ·  n_sockets: `0.43112`  ·  quality: `-0.03598`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -2.64050 |
| `explicit.stat_983749596@T2` | -1.92620 |
| `explicit.stat_3981240776@T2` | 1.83852 |
| `explicit.stat_124131830@T2` | 1.16695 |
| `explicit.stat_3981240776@T1` | 0.94904 |
| `explicit.stat_2748665614@T1` | -0.85544 |
| `explicit.stat_1202301673@T2` | 0.79173 |
| `explicit.stat_1202301673` | 0.72528 |
| `explicit.stat_124131830` | 0.71857 |
| `explicit.stat_2748665614@T2` | -0.53532 |
| `explicit.stat_1379411836@T1` | 0.39534 |
| `explicit.stat_983749596` | 0.36911 |

### jewel — n=15547, R²=-0.7329

intercept: `-1.3187`  ·  log_price: True  ·  ilvl: `0.03635`  ·  n_mods: `0.22643`  ·  n_top_tier: `-0.37888`  ·  corrupted: `0.35658`  ·  quality: `0.22094`

| stat_id | coef |
|---|---|
| `explicit.stat_1869147066@T1` | 4.24292 |
| `explicit.stat_3714003708@T1` | -3.20731 |
| `explicit.stat_3824372849@T1` | 3.18200 |
| `explicit.stat_1316278494@T1` | -3.07784 |
| `explicit.stat_2456523742@T1` | 2.88857 |
| `explicit.stat_1569101201@T1` | 2.85852 |
| `explicit.stat_153777645@T1` | 2.47803 |
| `explicit.stat_3780644166@T1` | 2.45098 |
| `explicit.stat_2594634307@T1` | 2.36208 |
| `explicit.stat_416040624@T1` | -2.34178 |
| `explicit.stat_2106365538@T1` | -2.26473 |
| `explicit.stat_1829102168@T1` | -2.25169 |

### accessory.belt — n=13746, R²=-1.3257

intercept: `3.6086`  ·  log_price: True  ·  ilvl: `-0.04289`  ·  n_mods: `-0.02789`  ·  n_top_tier: `-0.02227`  ·  corrupted: `0.37684`  ·  n_sockets: `-0.13196`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.75372 |
| `explicit.stat_2923486259@T1` | 1.00159 |
| `explicit.stat_1836676211@T1` | 0.35854 |
| `explicit.stat_2923486259@T2` | 0.23048 |
| `explicit.stat_3299347043@T1` | -0.21172 |
| `explicit.stat_4220027924@T1` | 0.20514 |
| `implicit.stat_731781020` | -0.19410 |
| `explicit.stat_3372524247@T1` | 0.15931 |
| `explicit.stat_1671376347@T1` | 0.09081 |
| `explicit.stat_2639966148` | 0.09060 |
| `explicit.stat_3299347043@T2` | -0.08292 |
| `explicit.stat_174664100` | 0.08121 |

### armour.chest — n=13495, R²=-1.4082

intercept: `3.7646`  ·  log_price: True  ·  ilvl: `-0.04649`  ·  n_mods: `-0.01392`  ·  n_top_tier: `0.26777`  ·  corrupted: `0.12618`  ·  n_sockets: `0.00392`  ·  quality: `0.00567`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.12928 |
| `explicit.stat_3981240776@T1` | 1.44147 |
| `explicit.stat_4015621042@T1` | -0.36201 |
| `explicit.stat_4080418644@T2` | -0.32906 |
| `explicit.stat_4080418644@T1` | -0.32493 |
| `explicit.stat_328541901@T1` | -0.32145 |
| `explicit.stat_3261801346@T2` | -0.31400 |
| `explicit.stat_4015621042@T2` | -0.30962 |
| `explicit.stat_4220027924@T2` | -0.30872 |
| `explicit.stat_986397080@T2` | -0.30393 |
| `explicit.stat_328541901@T2` | -0.30160 |
| `explicit.stat_3325883026@T2` | -0.29790 |

### armour.helmet — n=13277, R²=-1.4181

intercept: `4.2835`  ·  log_price: True  ·  ilvl: `-0.05354`  ·  n_mods: `-0.01774`  ·  n_top_tier: `0.55820`  ·  corrupted: `0.53506`  ·  n_sockets: `-0.00846`  ·  quality: `0.02397`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.14840 |
| `explicit.stat_2339757871@T1` | -2.74299 |
| `explicit.stat_53045048@T1` | -0.67503 |
| `explicit.stat_3033371881@T1` | -0.64837 |
| `explicit.stat_3033371881@T2` | -0.64485 |
| `explicit.stat_4052037485@T2` | -0.62445 |
| `explicit.stat_1062208444@T2` | -0.62069 |
| `explicit.stat_53045048@T2` | -0.61258 |
| `explicit.stat_4080418644@T2` | -0.61227 |
| `explicit.stat_4015621042@T2` | -0.60769 |
| `explicit.stat_1263695895@T1` | -0.59948 |
| `explicit.stat_803737631@T2` | -0.59505 |

### armour.boots — n=12477, R²=-0.2156

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.12027`  ·  corrupted: `0.00004`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2250533757@T2` | -0.34562 |
| `explicit.stat_2339757871@T1` | -0.12044 |
| `explicit.stat_3917489142@T2` | -0.12029 |
| `explicit.stat_3362812763@T2` | -0.12029 |
| `explicit.stat_3325883026@T1` | -0.12028 |
| `explicit.stat_2451402625@T2` | -0.12028 |
| `explicit.stat_99927264@T2` | -0.12028 |
| `explicit.stat_3261801346@T2` | -0.12028 |
| `explicit.stat_1062208444@T1` | -0.12028 |
| `explicit.stat_1062208444@T2` | -0.12028 |
| `explicit.stat_99927264@T1` | -0.12028 |
| `explicit.stat_3325883026@T2` | -0.12028 |

### armour.gloves — n=12275, R²=-0.2605

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.06011`  ·  corrupted: `0.00004`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.13272 |
| `explicit.stat_2339757871@T1` | -0.06043 |
| `explicit.stat_3484657501@T2` | -0.06014 |
| `explicit.stat_1368271171@T1` | -0.06013 |
| `explicit.stat_3362812763@T2` | -0.06013 |
| `explicit.stat_2797971005@T2` | -0.06012 |
| `explicit.stat_4015621042@T1` | -0.06012 |
| `explicit.stat_3362812763@T1` | -0.06012 |
| `explicit.stat_4080418644@T1` | -0.06012 |
| `explicit.stat_328541901@T2` | -0.06012 |
| `explicit.stat_1573130764@T1` | -0.06012 |
| `explicit.stat_681332047@T2` | -0.06012 |

### weapon.wand — n=8759, R²=-1.8449

intercept: `3.4343`  ·  log_price: True  ·  ilvl: `-0.04279`  ·  n_mods: `-0.00889`  ·  n_top_tier: `0.61495`  ·  corrupted: `0.04920`  ·  n_sockets: `-0.00770`  ·  quality: `0.01708`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.78510 |
| `explicit.stat_4226189338@T1` | 1.76185 |
| `explicit.stat_2254480358@T1` | 1.75110 |
| `explicit.stat_591105508@T1` | 1.63832 |
| `crafted.stat_124131830` | 0.86608 |
| `explicit.stat_2768835289@T2` | -0.75011 |
| `explicit.stat_3962278098@T2` | -0.69761 |
| `explicit.stat_737908626@T1` | -0.67639 |
| `explicit.stat_2968503605@T2` | -0.66526 |
| `explicit.stat_1545858329@T1` | 0.65746 |
| `explicit.stat_293638271@T2` | -0.64509 |
| `explicit.stat_2505884597@T2` | -0.64489 |

### weapon.bow — n=7268, R²=-1.7145

intercept: `3.4683`  ·  log_price: True  ·  ilvl: `-0.04299`  ·  n_mods: `-0.01527`  ·  n_top_tier: `0.28697`  ·  corrupted: `-0.05710`  ·  n_sockets: `0.00330`  ·  quality: `0.00594`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.37873 |
| `explicit.stat_2463230181@T1` | 2.00555 |
| `explicit.stat_1202301673@T1` | 1.97212 |
| `crafted.stat_3035140377` | 1.51434 |
| `explicit.stat_518292764@T1` | 1.20199 |
| `explicit.stat_1509134228@T1` | 0.46694 |
| `explicit.stat_55876295@T1` | -0.37546 |
| `explicit.stat_55876295@T2` | -0.34889 |
| `explicit.stat_2694482655@T1` | -0.33741 |
| `explicit.stat_821021828@T1` | -0.33363 |
| `explicit.stat_3261801346@T1` | -0.32743 |
| `explicit.stat_669069897@T2` | -0.32691 |

### weapon.crossbow — n=6847, R²=-1.5902

intercept: `3.4710`  ·  log_price: True  ·  ilvl: `-0.04338`  ·  n_mods: `0.00156`  ·  n_top_tier: `0.35285`  ·  corrupted: `-0.05400`  ·  n_sockets: `0.00306`  ·  quality: `0.00225`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 1.98834 |
| `explicit.stat_1037193709@T1` | 1.93135 |
| `explicit.stat_709508406@T1` | 1.91943 |
| `explicit.stat_1202301673@T1` | 1.87110 |
| `explicit.stat_2250681686@T2` | -1.35910 |
| `crafted.stat_3035140377` | 1.16406 |
| `explicit.stat_2250681686` | 1.03886 |
| `rune.stat_2246411426` | -0.66137 |
| `rune.stat_55876295` | 0.65661 |
| `rune.stat_669069897` | -0.45506 |
| `explicit.stat_691932474@T1` | -0.42150 |
| `explicit.stat_1202301673@T2` | -0.41912 |

### flask.charm — n=2700, R²=-0.0988

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1056492907` | 0.00052 |
| `explicit.stat_1873752457` | 0.00001 |
| `explicit.stat_1873752457@T2` | -0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `explicit.stat_388617051@T2` | -0.00001 |
| `explicit.stat_2676834156@T2` | -0.00001 |
| `explicit.stat_3849649145` | -0.00001 |
| `explicit.stat_2541588185@T2` | 0.00001 |
| `implicit.stat_3310778564` | -0.00001 |
| `explicit.stat_1366840608@T2` | 0.00000 |
| `explicit.stat_828533480@T2` | -0.00000 |
| `explicit.stat_280890192` | -0.00000 |

### weapon.warstaff — n=2035, R²=-0.0909

intercept: `-0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1509134228` | 0.00004 |
| `rune.stat_1037193709` | 0.00003 |
| `rune.stat_1039491398` | -0.00003 |
| `explicit.stat_1509134228@T2` | 0.00001 |
| `rune.stat_1817052494` | -0.00001 |
| `explicit.stat_9187492@T1` | 0.00001 |
| `explicit.stat_1037193709@T1` | -0.00001 |
| `explicit.stat_210067635@T1` | -0.00001 |
| `desecrated.stat_518292764` | -0.00001 |
| `explicit.stat_791928121@T2` | -0.00001 |
| `explicit.stat_3639275092@T1` | -0.00001 |
| `explicit.stat_1263695895@T1` | 0.00001 |

### weapon.sceptre — n=1942, R²=-0.1028

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | 0.00001 |
| `explicit.stat_1998951374@T1` | 0.00001 |
| `explicit.stat_1798257884@T2` | 0.00001 |
| `explicit.stat_1998951374@T2` | 0.00001 |
| `explicit.stat_4010677958@T1` | 0.00001 |
| `explicit.stat_3984865854@T1` | 0.00001 |
| `explicit.stat_2854751904@T2` | 0.00001 |
| `explicit.stat_101878827@T1` | 0.00001 |
| `explicit.stat_1574590649@T1` | 0.00001 |
| `explicit.stat_3057012405@T2` | 0.00001 |
| `explicit.stat_4010677958@T2` | 0.00001 |
| `explicit.stat_1250712710@T2` | 0.00001 |

### weapon.staff — n=1941, R²=-0.1155

intercept: `-0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00002`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_3990135792` | -0.00004 |
| `explicit.stat_2254480358@T1` | 0.00004 |
| `explicit.stat_3291658075@T2` | 0.00004 |
| `explicit.stat_473429811@T1` | 0.00003 |
| `explicit.stat_124131830@T1` | 0.00003 |
| `explicit.stat_2254480358@T2` | 0.00003 |
| `explicit.stat_2968503605@T2` | 0.00003 |
| `explicit.stat_1600707273@T2` | 0.00003 |
| `explicit.stat_737908626@T1` | 0.00002 |
| `explicit.stat_3639275092@T2` | 0.00002 |
| `rune.stat_2974417149` | 0.00002 |
| `explicit.stat_1050105434@T2` | 0.00002 |

### weapon.spear — n=1741, R²=-0.104

intercept: `-0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | -0.00004 |
| `explicit.stat_1263695895@T2` | -0.00002 |
| `explicit.stat_1509134228@T1` | 0.00002 |
| `explicit.stat_210067635@T1` | 0.00001 |
| `explicit.stat_1368271171@T1` | 0.00001 |
| `explicit.stat_3639275092@T1` | 0.00001 |
| `explicit.stat_1940865751@T1` | 0.00001 |
| `explicit.stat_1037193709@T1` | 0.00001 |
| `explicit.stat_1202301673@T2` | -0.00001 |
| `explicit.stat_2694482655@T1` | 0.00001 |
| `explicit.stat_3695891184@T2` | 0.00001 |
| `explicit.stat_2694482655@T2` | 0.00001 |

### armour.focus — n=1484, R²=0.3754

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00005`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -6.45689 |
| `desecrated.stat_2910761524@T1` | 0.92668 |
| `desecrated.stat_3393628375` | 0.46120 |
| `desecrated.stat_2910761524` | -0.11691 |
| `crafted.stat_4015621042` | 0.06730 |
| `desecrated.stat_4220027924` | 0.00696 |
| `desecrated.stat_737908626` | -0.00247 |
| `explicit.stat_328541901@T2` | -0.00002 |
| `explicit.stat_3372524247@T2` | -0.00001 |
| `explicit.stat_3962278098@T2` | 0.00001 |
| `explicit.stat_2339757871@T1` | 0.00001 |
| `explicit.stat_3962278098@T1` | 0.00001 |

### armour.quiver — n=1428, R²=-0.1392

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | -0.00008 |
| `explicit.stat_2463230181@T2` | -0.00004 |
| `explicit.stat_681332047@T1` | -0.00002 |
| `explicit.stat_3714003708@T1` | -0.00001 |
| `explicit.stat_681332047@T2` | -0.00001 |
| `explicit.stat_803737631@T2` | -0.00001 |
| `explicit.stat_3032590688@T1` | -0.00001 |
| `explicit.stat_2321178454@T2` | -0.00001 |
| `explicit.stat_3714003708@T2` | -0.00001 |
| `explicit.stat_1573130764@T1` | -0.00001 |
| `explicit.stat_2321178454@T1` | -0.00001 |
| `explicit.stat_3032590688@T2` | -0.00001 |

### armour.shield — n=1260, R²=-0.1417

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | -0.00010 |
| `explicit.stat_1301765461@T2` | -0.00010 |
| `explicit.stat_1011760251@T1` | -0.00008 |
| `explicit.stat_1301765461` | 0.00005 |
| `explicit.stat_1978899297@T1` | 0.00004 |
| `explicit.stat_1011760251@T2` | -0.00003 |
| `explicit.stat_3676141501@T1` | 0.00003 |
| `explicit.stat_1011760251` | 0.00003 |
| `explicit.stat_3033371881@T1` | 0.00002 |
| `explicit.stat_2339757871@T2` | 0.00002 |
| `explicit.stat_1978899297@T2` | -0.00002 |
| `explicit.stat_4095671657@T1` | 0.00002 |

### weapon.twomace — n=1086, R²=-0.175

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | -0.00002 |
| `explicit.stat_821021828@T2` | -0.00002 |
| `explicit.stat_3336890334@T1` | -0.00002 |
| `explicit.stat_1263695895@T1` | 0.00002 |
| `explicit.stat_821021828@T1` | -0.00002 |
| `explicit.stat_1037193709@T2` | -0.00002 |
| `explicit.stat_1940865751@T1` | -0.00002 |
| `explicit.stat_2694482655@T1` | -0.00002 |
| `explicit.stat_669069897@T1` | -0.00002 |
| `explicit.stat_1368271171@T1` | -0.00001 |
| `explicit.stat_691932474@T1` | -0.00001 |
| `explicit.stat_669069897@T2` | -0.00001 |

## Coverage (listings per base)

- … **Sapphire** — 7719 listings (7719 priced) [0.6–7379.9 ex]
- … **Emerald** — 7690 listings (7690 priced) [0.7–42426.8 ex]
- … **Ruby** — 6002 listings (6002 priced) [0.3–7176.6 ex]
- … **Utility Belt** — 4185 listings (4184 priced) [0.3–4555741.7 ex]
- … **Stellar Amulet** — 3177 listings (3177 priced) [0.3–4547453.5 ex]
- … **Prismatic Ring** — 2953 listings (2953 priced) [0.3–36899.4 ex]
- … **Solar Amulet** — 2871 listings (2871 priced) [0.7–4547453.5 ex]
- … **Gold Amulet** — 2834 listings (2834 priced) [0.7–292542.5 ex]
- … **Amethyst Ring** — 2826 listings (2825 priced) [0.7–17677.8 ex]
- … **Dueling Wand** — 2705 listings (2705 priced) [1.0–138957.7 ex]
- … **Gold Ring** — 2692 listings (2691 priced) [0.5–5903.9 ex]
- … **Sapphire Ring** — 2229 listings (2229 priced) [0.9–7379.9 ex]
- … **Topaz Ring** — 2210 listings (2210 priced) [1.0–3689.9 ex]
- … **Ruby Ring** — 2136 listings (2136 priced) [0.7–44279.2 ex]
- … **Plate Belt** — 2095 listings (2095 priced) [0.7–4547453.5 ex]
- … **Obliterator Bow** — 2067 listings (2065 priced) [0.7–22139622146.9 ex]
- … **Heavy Belt** — 2000 listings (2000 priced) [0.5–2121.3 ex]
- … **Lapis Amulet** — 1951 listings (1951 priced) [0.6–4547453.5 ex]
- … **Amber Amulet** — 1929 listings (1929 priced) [0.7–4547453.5 ex]
- … **Jade Amulet** — 1912 listings (1912 priced) [0.7–4547453.5 ex]
- … **Ancestral Tiara** — 1889 listings (1887 priced) [0.7–365678.1 ex]
- … **Unset Ring** — 1792 listings (1792 priced) [0.7–1476.0 ex]
- … **Bloodstone Amulet** — 1751 listings (1751 priced) [1.0–3689.9 ex]
- … **Pearl Ring** — 1718 listings (1718 priced) [0.6–7176.6 ex]
- … **Azure Amulet** — 1691 listings (1691 priced) [1.0–28284.5 ex]

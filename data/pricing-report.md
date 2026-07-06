# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-06T08:55:30+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **213124** (213020 priced in exalted)
- Distinct bases: 930 · distinct mods: 2576 · mod rows: 1010580
- Sold signals: **36584** sold · 111371 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-06T08:49:33+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×15.63** (median |log error| 2.7495)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.02** (> 0 = the mods carry signal)
- Calibration: 76% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.05** · typical error ×40.14 · ±30% 12% · n=30679
- Premium segment (60ex+): skill **+0.06** · typical error ×166.02 · ±30% 0% · n=18329
- Sold listings (clearing prices): skill **+0.34** · typical error ×6.50 · ±30% 0% · n=10

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 3964 | ×34.52 | 15% | +0.02 | +0.02 |
| accessory.amulet | 3801 | ×44.32 | 19% | +0.01 | +0.01 |
| jewel | 3387 | ×8.84 | 6% | +0.04 | +0.07 |
| accessory.belt | 3236 | ×10.00 | 22% | +0.02 | +0.00 |
| armour.chest | 3168 | ×10.00 | 23% | -0.00 | +0.00 |
| armour.helmet | 3116 | ×10.00 | 23% | +0.00 | +0.00 |
| armour.boots | 2925 | ×11.89 | 6% | +0.00 | +0.03 |
| armour.gloves | 2909 | ×16.94 | 5% | -0.01 | +0.02 |
| other | 2750 | ×9.96 | 38% | +0.05 | +0.15 |
| weapon.wand | 2053 | ×10.96 | 27% | +0.04 | +0.06 |
| weapon.bow | 1670 | ×10.29 | 25% | +0.06 | +0.09 |
| weapon.crossbow | 1565 | ×11.11 | 24% | +0.07 | +0.09 |
| weapon.warstaff | 486 | ×40.00 | 21% | +0.00 | +0.00 |
| weapon.sceptre | 460 | ×50.00 | 15% | +0.00 | +0.00 |
| weapon.staff | 457 | ×25.00 | 23% | +0.00 | +0.00 |
| weapon.spear | 413 | ×50.00 | 16% | +0.00 | +0.00 |
| armour.quiver | 341 | ×50.00 | 14% | +0.00 | +0.00 |
| armour.focus | 321 | ×77.00 | 14% | +0.03 | +0.03 |
| armour.shield | 302 | ×42.21 | 13% | +0.00 | +0.00 |
| flask.charm | 265 | ×5.00 | 42% | -0.00 | +0.00 |
| weapon.twomace | 241 | ×47.00 | 16% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=24426, R²=-0.503

intercept: `1.6090`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00223`  ·  n_top_tier: `0.37408`  ·  corrupted: `3.63496`  ·  n_sockets: `-0.00007`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_2891184298@T1` | 2.10205 |
| `explicit.stat_2974417149@T1` | 1.26692 |
| `explicit.stat_3291658075@T1` | 1.07467 |
| `explicit.stat_2106365538@T1` | 0.89495 |
| `explicit.stat_1050105434@T1` | -0.55222 |
| `explicit.stat_1589917703@T1` | -0.40496 |
| `explicit.stat_3141070085@T1` | 0.32079 |
| `explicit.stat_101878827@T1` | 0.30804 |
| `explicit.stat_2968503605@T1` | 0.30558 |
| `explicit.stat_1589917703` | 0.30474 |
| `explicit.stat_3917489142@T1` | 0.27008 |
| `implicit.stat_1379411836` | -0.26860 |

### accessory.ring — n=18167, R²=-2.1348

intercept: `5.0310`  ·  log_price: True  ·  ilvl: `-0.05899`  ·  n_mods: `-0.03397`  ·  n_top_tier: `-0.21008`  ·  corrupted: `0.66801`  ·  n_sockets: `3.68756`  ·  quality: `0.12047`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T2` | 2.14072 |
| `explicit.stat_2557965901@T1` | 1.01268 |
| `explicit.stat_3032590688@T2` | 1.00574 |
| `explicit.stat_2557965901@T2` | 0.87370 |
| `explicit.stat_1379411836@T1` | -0.70582 |
| `explicit.stat_1263695895@T1` | 0.62100 |
| `explicit.stat_2923486259@T2` | 0.47937 |
| `implicit.stat_2748665614` | 0.45780 |
| `explicit.stat_3372524247@T1` | 0.45561 |
| `explicit.stat_736967255@T1` | 0.42811 |
| `explicit.stat_1379411836@T2` | -0.40333 |
| `explicit.stat_2923486259@T1` | 0.37046 |

### jewel — n=17499, R²=-0.7094

intercept: `-1.2145`  ·  log_price: True  ·  ilvl: `0.03690`  ·  n_mods: `0.23130`  ·  n_top_tier: `-0.32701`  ·  corrupted: `0.39878`  ·  quality: `0.21117`

| stat_id | coef |
|---|---|
| `explicit.stat_3714003708@T1` | -3.50292 |
| `explicit.stat_1869147066@T1` | 3.45330 |
| `explicit.stat_1316278494@T1` | -3.11069 |
| `explicit.stat_3824372849@T1` | 2.77024 |
| `explicit.stat_1697951953@T1` | -2.72250 |
| `explicit.stat_2456523742@T1` | 2.51367 |
| `explicit.stat_293638271@T1` | 2.36474 |
| `explicit.stat_3780644166@T1` | 2.33932 |
| `explicit.stat_3192728503@T1` | -2.33017 |
| `explicit.stat_2594634307@T1` | 2.31969 |
| `explicit.stat_1569101201@T1` | 2.23536 |
| `explicit.stat_2106365538@T1` | -2.20312 |

### accessory.amulet — n=17459, R²=-2.1966

intercept: `3.8962`  ·  log_price: True  ·  ilvl: `-0.04748`  ·  n_mods: `-0.02261`  ·  n_top_tier: `0.05539`  ·  corrupted: `0.07841`  ·  n_sockets: `0.00297`  ·  quality: `-0.00527`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -2.71098 |
| `explicit.stat_983749596@T2` | -1.99561 |
| `explicit.stat_3981240776@T2` | 1.53478 |
| `explicit.stat_1202301673` | 0.75692 |
| `explicit.stat_124131830` | 0.71332 |
| `explicit.stat_124131830@T2` | 0.70970 |
| `explicit.stat_983749596` | 0.37915 |
| `explicit.stat_3299347043@T1` | -0.33814 |
| `explicit.stat_1050105434@T1` | 0.28127 |
| `explicit.stat_2106365538@T2` | 0.19488 |
| `explicit.stat_3299347043@T2` | -0.19469 |
| `explicit.stat_1379411836@T1` | 0.19416 |

### accessory.belt — n=14904, R²=-0.0848

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.04231`  ·  corrupted: `0.00004`  ·  n_sockets: `-0.00005`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.55969 |
| `explicit.stat_2639966148` | 0.12406 |
| `pseudo.total_ele_res>=80` | 0.06891 |
| `explicit.stat_174664100` | 0.04900 |
| `explicit.stat_3811191316` | 0.04283 |
| `explicit.stat_1389754388@T1` | -0.04236 |
| `explicit.stat_51994685@T1` | -0.04233 |
| `explicit.stat_644456512@T2` | -0.04233 |
| `explicit.stat_1389754388@T2` | -0.04233 |
| `explicit.stat_644456512@T1` | -0.04233 |
| `explicit.stat_3325883026@T1` | -0.04233 |
| `explicit.stat_915769802@T2` | -0.04232 |

### armour.chest — n=14696, R²=-0.2182

intercept: `2.3030`  ·  log_price: True  ·  ilvl: `-0.00001`  ·  n_mods: `-0.00005`  ·  n_top_tier: `0.10018`  ·  corrupted: `0.00025`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_1978899297` | -0.73952 |
| `explicit.stat_3261801346@T1` | -0.10029 |
| `explicit.stat_915769802@T1` | -0.10026 |
| `explicit.stat_4080418644@T2` | -0.10025 |
| `explicit.stat_915769802@T2` | -0.10023 |
| `explicit.stat_3325883026@T1` | -0.10023 |
| `explicit.stat_3301100256@T1` | -0.10022 |
| `explicit.stat_3033371881@T2` | -0.10022 |
| `explicit.stat_4015621042@T1` | -0.10021 |
| `explicit.stat_124859000@T2` | -0.10021 |
| `explicit.stat_3299347043@T2` | -0.10020 |
| `explicit.stat_3372524247@T2` | -0.10020 |

### armour.helmet — n=14392, R²=-0.2433

intercept: `2.3029`  ·  log_price: True  ·  ilvl: `-0.00001`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.03966`  ·  corrupted: `0.03196`  ·  n_sockets: `-0.00002`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_1062208444@T2` | -0.11212 |
| `explicit.stat_4080418644@T2` | -0.09213 |
| `desecrated.stat_3917489142` | 0.05085 |
| `explicit.stat_53045048@T2` | -0.03973 |
| `explicit.stat_3033371881@T1` | -0.03971 |
| `explicit.stat_3321629045@T1` | -0.03971 |
| `explicit.stat_803737631@T2` | -0.03971 |
| `explicit.stat_328541901@T2` | -0.03969 |
| `explicit.stat_3325883026@T2` | -0.03969 |
| `explicit.stat_53045048@T1` | -0.03968 |
| `explicit.stat_3362812763@T2` | -0.03968 |
| `explicit.stat_3362812763@T1` | -0.03968 |

### armour.boots — n=13516, R²=-0.5638

intercept: `4.3008`  ·  log_price: True  ·  ilvl: `-0.04785`  ·  n_mods: `-0.18791`  ·  n_top_tier: `0.60569`  ·  corrupted: `0.52993`  ·  n_sockets: `0.15925`  ·  quality: `0.01202`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.84224 |
| `rune.stat_836936635` | -1.73500 |
| `desecrated.stat_2250533757@T2` | -1.45414 |
| `explicit.stat_3362812763@T1` | -1.39478 |
| `explicit.stat_1062208444@T2` | -1.31847 |
| `explicit.stat_2923486259@T2` | -1.18889 |
| `explicit.stat_3917489142@T2` | -1.13074 |
| `explicit.stat_328541901@T1` | -1.06302 |
| `explicit.stat_2250533757@T1` | 1.01750 |
| `explicit.stat_4080418644@T1` | -1.01308 |
| `explicit.stat_3033371881@T2` | -0.99894 |
| `explicit.stat_1062208444@T1` | -0.90635 |

### armour.gloves — n=13334, R²=-0.6107

intercept: `3.2444`  ·  log_price: True  ·  ilvl: `-0.04064`  ·  n_mods: `-0.08468`  ·  n_top_tier: `0.51965`  ·  corrupted: `0.47534`  ·  n_sockets: `0.16436`  ·  quality: `0.00362`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.95452 |
| `explicit.stat_681332047@T2` | -1.38801 |
| `explicit.stat_2797971005@T1` | -1.25621 |
| `explicit.stat_2797971005@T2` | -1.15782 |
| `explicit.stat_803737631@T2` | -1.13860 |
| `explicit.stat_124859000@T1` | -1.11222 |
| `explicit.stat_1573130764@T1` | -0.93799 |
| `explicit.stat_3484657501@T2` | -0.92551 |
| `explicit.stat_1754445556@T1` | -0.85332 |
| `explicit.stat_3032590688@T1` | -0.84383 |
| `explicit.stat_1754445556@T2` | -0.80800 |
| `explicit.stat_4015621042@T1` | -0.80187 |

### weapon.wand — n=9464, R²=-1.8948

intercept: `3.6029`  ·  log_price: True  ·  ilvl: `-0.04504`  ·  n_mods: `-0.00655`  ·  n_top_tier: `0.85464`  ·  corrupted: `0.03762`  ·  n_sockets: `0.00513`  ·  quality: `0.01254`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.07545 |
| `explicit.stat_4226189338@T1` | 1.56440 |
| `explicit.stat_2254480358@T1` | 1.54476 |
| `explicit.stat_591105508@T1` | 1.45688 |
| `explicit.stat_2768835289@T2` | -0.98484 |
| `explicit.stat_3962278098@T2` | -0.93675 |
| `explicit.stat_737908626@T1` | -0.91451 |
| `explicit.stat_2968503605@T2` | -0.89736 |
| `explicit.stat_737908626@T2` | -0.89449 |
| `explicit.stat_473429811@T1` | -0.88758 |
| `explicit.stat_2231156303@T2` | -0.88195 |
| `explicit.stat_293638271@T2` | -0.87114 |

### weapon.bow — n=7786, R²=-1.7951

intercept: `3.5090`  ·  log_price: True  ·  ilvl: `-0.04348`  ·  n_mods: `-0.01451`  ·  n_top_tier: `0.39291`  ·  corrupted: `-0.02646`  ·  n_sockets: `-0.00011`  ·  quality: `0.00476`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.11374 |
| `crafted.stat_3035140377` | 1.94253 |
| `explicit.stat_1202301673@T1` | 1.88512 |
| `explicit.stat_2463230181@T1` | 1.87441 |
| `desecrated.stat_666077204@T1` | 1.72069 |
| `explicit.stat_518292764@T1` | 0.75811 |
| `explicit.stat_55876295@T1` | -0.48508 |
| `explicit.stat_55876295@T2` | -0.46001 |
| `explicit.stat_2694482655@T1` | -0.45661 |
| `explicit.stat_1037193709@T1` | -0.43320 |
| `explicit.stat_3261801346@T1` | -0.42758 |
| `explicit.stat_821021828@T2` | -0.42560 |

### weapon.crossbow — n=7374, R²=-1.6487

intercept: `3.6507`  ·  log_price: True  ·  ilvl: `-0.04566`  ·  n_mods: `-0.00181`  ·  n_top_tier: `0.32364`  ·  corrupted: `-0.08420`  ·  n_sockets: `0.00388`  ·  quality: `0.00336`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 2.00371 |
| `explicit.stat_1037193709@T1` | 1.97132 |
| `explicit.stat_709508406@T1` | 1.92384 |
| `explicit.stat_1202301673@T1` | 1.85221 |
| `explicit.stat_2250681686@T2` | -1.31534 |
| `crafted.stat_3035140377` | 1.20910 |
| `explicit.stat_2250681686` | 1.04747 |
| `rune.stat_2246411426` | -0.65444 |
| `rune.stat_55876295` | 0.64806 |
| `explicit.stat_691932474@T1` | -0.43817 |
| `rune.stat_669069897` | -0.43730 |
| `explicit.stat_1202301673@T2` | -0.40605 |

### flask.charm — n=3343, R²=-0.1338

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00004`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1056492907` | 2.63898 |
| `explicit.stat_1873752457@T2` | -0.00002 |
| `explicit.stat_828533480@T2` | -0.00001 |
| `explicit.stat_828533480@T1` | -0.00001 |
| `explicit.stat_1120862500@T2` | -0.00001 |
| `explicit.stat_1873752457@T1` | -0.00001 |
| `explicit.stat_2676834156@T2` | -0.00001 |
| `explicit.stat_388617051@T2` | -0.00001 |
| `explicit.stat_1873752457` | -0.00001 |
| `explicit.stat_3246948616` | 0.00001 |
| `implicit.stat_3310778564` | -0.00001 |
| `explicit.stat_3196823591@T2` | -0.00001 |

### weapon.warstaff — n=2478, R²=-0.226

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1037193709` | 0.26515 |
| `rune.stat_3336890334` | 0.24394 |
| `rune.stat_2430860292` | -0.12604 |
| `rune.stat_1817052494` | -0.10606 |
| `rune.stat_1509134228` | 0.00899 |
| `rune.stat_1039491398` | -0.00809 |
| `rune.stat_2077615515` | 0.00081 |
| `crafted.stat_210067635@T2` | -0.00006 |
| `explicit.stat_1509134228@T2` | 0.00002 |
| `explicit.stat_9187492@T1` | 0.00002 |
| `explicit.stat_3336890334@T2` | -0.00001 |
| `explicit.stat_210067635@T1` | -0.00001 |

### weapon.sceptre — n=2365, R²=-0.2487

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1050105434` | 0.01333 |
| `desecrated.stat_3984865854` | -0.00841 |
| `explicit.stat_2162097452@T1` | 0.00003 |
| `explicit.stat_1263695895@T1` | 0.00003 |
| `explicit.stat_3057012405@T1` | 0.00002 |
| `explicit.stat_4010677958@T1` | 0.00002 |
| `explicit.stat_101878827@T2` | 0.00002 |
| `explicit.stat_1998951374@T1` | 0.00002 |
| `explicit.stat_4010677958@T2` | 0.00001 |
| `explicit.stat_1998951374@T2` | 0.00001 |
| `explicit.stat_2162097452@T2` | 0.00001 |
| `explicit.stat_1250712710@T1` | -0.00001 |

### weapon.staff — n=2359, R²=-0.2353

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_3990135792` | -0.13412 |
| `rune.stat_2974417149` | 0.08047 |
| `explicit.stat_124131830@T1` | 0.00005 |
| `explicit.stat_473429811@T1` | 0.00004 |
| `explicit.stat_3291658075@T2` | 0.00003 |
| `explicit.stat_274716455@T1` | 0.00002 |
| `explicit.stat_2254480358@T1` | 0.00002 |
| `explicit.stat_2968503605@T2` | 0.00002 |
| `explicit.stat_124131830@T2` | 0.00002 |
| `explicit.stat_737908626@T2` | 0.00002 |
| `explicit.stat_2974417149@T2` | 0.00002 |
| `explicit.stat_591105508@T2` | 0.00001 |

### weapon.spear — n=2053, R²=-0.2301

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 0.00003 |
| `explicit.stat_1263695895@T1` | -0.00003 |
| `explicit.stat_2694482655@T1` | 0.00002 |
| `explicit.stat_1263695895@T2` | -0.00002 |
| `explicit.stat_210067635@T1` | 0.00002 |
| `explicit.stat_518292764@T1` | 0.00002 |
| `explicit.stat_3639275092@T1` | 0.00002 |
| `explicit.stat_709508406@T1` | 0.00002 |
| `explicit.stat_1037193709@T1` | 0.00002 |
| `explicit.stat_748522257@T2` | 0.00001 |
| `explicit.stat_1368271171@T1` | 0.00001 |
| `explicit.stat_2694482655@T2` | 0.00001 |

### armour.focus — n=1717, R²=0.0063

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `-0.00005`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.85525 |
| `desecrated.stat_3465022881@T1` | 1.95770 |
| `desecrated.stat_2910761524@T1` | 0.92628 |
| `desecrated.stat_3393628375` | 0.55659 |
| `desecrated.stat_3465022881` | -0.11779 |
| `desecrated.stat_2910761524` | -0.11699 |
| `crafted.stat_4015621042` | 0.06731 |
| `desecrated.stat_4220027924` | 0.00355 |
| `desecrated.stat_737908626` | -0.00141 |
| `desecrated.stat_1671376347` | -0.00006 |
| `desecrated.stat_3372524247` | -0.00006 |
| `explicit.stat_4220027924` | -0.00006 |

### armour.quiver — n=1637, R²=-0.2516

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00002`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | -0.00005 |
| `explicit.stat_2463230181@T2` | -0.00002 |
| `explicit.stat_681332047@T1` | -0.00002 |
| `explicit.stat_3714003708@T1` | -0.00002 |
| `explicit.stat_3714003708@T2` | -0.00002 |
| `explicit.stat_803737631@T2` | -0.00002 |
| `explicit.stat_681332047@T2` | -0.00002 |
| `explicit.stat_1368271171@T2` | -0.00001 |
| `explicit.stat_3032590688@T1` | -0.00001 |
| `explicit.stat_1573130764@T1` | -0.00001 |
| `explicit.stat_1573130764@T2` | -0.00001 |
| `explicit.stat_3032590688@T2` | -0.00001 |

### armour.shield — n=1502, R²=-0.2746

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00005`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 0.29507 |
| `explicit.stat_1978899297@T1` | 0.00199 |
| `explicit.stat_1978899297@T2` | -0.00054 |
| `explicit.stat_1978899297` | 0.00048 |
| `explicit.stat_1011760251@T1` | -0.00015 |
| `explicit.stat_1301765461@T2` | -0.00013 |
| `explicit.stat_1011760251@T2` | -0.00008 |
| `explicit.stat_2339757871@T1` | -0.00008 |
| `explicit.stat_3855016469@T1` | -0.00007 |
| `explicit.stat_3771516363@T1` | -0.00006 |
| `explicit.stat_3639275092@T1` | -0.00006 |
| `explicit.stat_3372524247@T2` | -0.00006 |

### weapon.twomace — n=1271, R²=-0.2701

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1039491398` | 0.07989 |
| `rune.stat_1509134228` | -0.02885 |
| `explicit.stat_1037193709@T1` | -0.00005 |
| `explicit.stat_3336890334@T1` | -0.00005 |
| `explicit.stat_821021828@T1` | -0.00005 |
| `explicit.stat_821021828@T2` | -0.00005 |
| `explicit.stat_669069897@T1` | -0.00004 |
| `explicit.stat_1037193709@T2` | -0.00004 |
| `explicit.stat_669069897@T2` | -0.00003 |
| `explicit.stat_387439868@T2` | -0.00003 |
| `explicit.stat_1368271171@T1` | -0.00003 |
| `explicit.stat_1940865751@T1` | -0.00003 |

## Coverage (listings per base)

- … **Emerald** — 8601 listings (8601 priced) [0.7–4745587.6 ex]
- … **Sapphire** — 8568 listings (8567 priced) [0.6–4745587.6 ex]
- … **Ruby** — 6648 listings (6647 priced) [0.3–28868.8 ex]
- … **Utility Belt** — 4536 listings (4534 priced) [0.3–4555741.7 ex]
- … **Stellar Amulet** — 3405 listings (3405 priced) [0.3–4547453.5 ex]
- … **Prismatic Ring** — 3209 listings (3208 priced) [0.3–36899.4 ex]
- … **Solar Amulet** — 3140 listings (3138 priced) [0.6–4547453.5 ex]
- … **Gold Amulet** — 3069 listings (3069 priced) [0.6–292542.5 ex]
- … **Amethyst Ring** — 3049 listings (3048 priced) [0.6–71450.3 ex]
- … **Gold Ring** — 2934 listings (2933 priced) [0.5–10825.8 ex]
- … **Dueling Wand** — 2925 listings (2923 priced) [1.0–4599254.4 ex]
- … **Sapphire Ring** — 2451 listings (2451 priced) [0.6–70346.0 ex]
- … **Topaz Ring** — 2413 listings (2413 priced) [1.0–44572.1 ex]
- … **Ruby Ring** — 2344 listings (2344 priced) [0.9–44279.2 ex]
- … **Plate Belt** — 2266 listings (2266 priced) [0.5–4547453.5 ex]
- … **Obliterator Bow** — 2233 listings (2230 priced) [0.3–22139622146.9 ex]
- … **Heavy Belt** — 2143 listings (2143 priced) [0.5–211038.1 ex]
- … **Lapis Amulet** — 2132 listings (2132 priced) [0.6–4547453.5 ex]
- … **Amber Amulet** — 2111 listings (2111 priced) [0.6–4547453.5 ex]
- … **Jade Amulet** — 2085 listings (2084 priced) [0.6–4547453.5 ex]
- … **Ancestral Tiara** — 2059 listings (2057 priced) [0.6–594295.2 ex]
- … **Unset Ring** — 1967 listings (1967 priced) [0.6–10551.9 ex]
- … **Bloodstone Amulet** — 1920 listings (1920 priced) [0.6–7275.7 ex]
- … **Pearl Ring** — 1888 listings (1888 priced) [0.6–7176.6 ex]
- … **Azure Amulet** — 1884 listings (1884 priced) [0.6–29714.8 ex]

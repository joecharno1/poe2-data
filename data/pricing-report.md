# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-03T05:15:46+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **34521** (34521 priced in exalted)
- Distinct bases: 701 · distinct mods: 1278 · mod rows: 178062
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-03T05:00:54+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×33.23** (median |log error| 3.5035)
- Within ±30% of asking price: **29%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 70% of actuals above prediction (target ≈ 75%)

| group | n_test | ×err | ±30% | skill |
|---|---|---|---|---|
| accessory.belt | 575 | ×37.74 | 29% | +0.08 |
| armour.boots | 575 | ×5.93 | 25% | +0.03 |
| armour.chest | 562 | ×42.06 | 13% | +0.04 |
| armour.helmet | 561 | ×122.08 | 26% | +0.05 |
| armour.gloves | 535 | ×211.14 | 24% | -0.02 |
| weapon.wand | 461 | ×230.30 | 24% | +0.12 |
| accessory.amulet | 438 | ×69.67 | 2% | +0.21 |
| accessory.ring | 415 | ×12.99 | 4% | -1.83 |
| weapon.crossbow | 349 | ×292.83 | 17% | +0.09 |
| weapon.bow | 341 | ×86.57 | 22% | +0.05 |
| other | 259 | ×3.76 | 39% | +0.46 |
| weapon.sceptre | 148 | ×1.00 | 99% | +0.00 |
| weapon.spear | 139 | ×1.00 | 100% | n/a |
| armour.focus | 133 | ×1.00 | 100% | n/a |
| armour.shield | 112 | ×1.00 | 100% | n/a |
| jewel | 100 | ×66.65 | 5% | +0.29 |
| weapon.staff | 59 | ×1.00 | 98% | +0.00 |
| armour.quiver | 48 | ×1.00 | 100% | n/a |
| weapon.twomace | 32 | ×1.00 | 97% | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=2990, R²=0.2553

intercept: `1.5554`  ·  log_price: True  ·  ilvl: `0.00276`  ·  n_mods: `-0.02382`  ·  n_top_tier: `0.28528`  ·  corrupted: `0.52600`  ·  n_sockets: `-0.05575`  ·  quality: `-0.00551`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.32981 |
| `explicit.stat_4080418644@T1` | -0.67224 |
| `explicit.stat_4052037485@T2` | -0.58880 |
| `explicit.stat_691932474@T2` | -0.53399 |
| `explicit.stat_915769802@T1` | -0.52698 |
| `explicit.stat_2901986750@T2` | -0.45489 |
| `explicit.stat_4220027924@T1` | -0.45028 |
| `explicit.stat_1671376347@T2` | -0.40503 |
| `explicit.stat_1263695895@T1` | -0.39346 |
| `explicit.stat_3299347043@T2` | -0.36211 |
| `explicit.stat_3372524247@T1` | -0.35666 |
| `explicit.stat_124131830` | -0.35655 |

### accessory.belt — n=2726, R²=-0.8826

intercept: `1.9788`  ·  log_price: True  ·  ilvl: `-0.02404`  ·  n_mods: `-0.01343`  ·  n_top_tier: `0.05034`  ·  corrupted: `0.03960`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 0.46846 |
| `pseudo.total_ele_res>=80` | 0.25952 |
| `implicit.stat_731781020` | 0.22980 |
| `explicit.stat_2639966148` | 0.22195 |
| `explicit.stat_174664100` | 0.13596 |
| `explicit.stat_3299347043@T1` | 0.10894 |
| `explicit.stat_3811191316` | 0.10409 |
| `explicit.stat_2923486259@T2` | -0.08905 |
| `explicit.stat_2923486259@T1` | -0.07581 |
| `explicit.stat_1836676211@T2` | -0.07564 |
| `explicit.stat_1050105434@T2` | -0.07200 |
| `explicit.stat_770672621` | 0.06656 |

### armour.boots — n=2672, R²=-0.7103

intercept: `7.4340`  ·  log_price: True  ·  ilvl: `-0.09211`  ·  n_mods: `-0.04480`  ·  n_top_tier: `0.70069`  ·  corrupted: `0.44228`  ·  n_sockets: `0.06290`  ·  quality: `0.01385`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 5.23986 |
| `explicit.stat_2339757871@T1` | -1.17249 |
| `explicit.stat_3261801346@T2` | -0.92331 |
| `explicit.stat_3321629045@T1` | -0.85616 |
| `explicit.stat_3484657501@T2` | -0.85440 |
| `explicit.stat_124859000@T2` | -0.84724 |
| `explicit.stat_2923486259@T2` | -0.79405 |
| `explicit.stat_1062208444@T1` | -0.78711 |
| `explicit.stat_3299347043@T1` | -0.78580 |
| `explicit.stat_3299347043@T2` | -0.78068 |
| `explicit.stat_3362812763@T2` | -0.77836 |
| `explicit.stat_3484657501@T1` | -0.77661 |

### armour.helmet — n=2628, R²=-0.9596

intercept: `7.6532`  ·  log_price: True  ·  ilvl: `-0.09760`  ·  n_mods: `-0.03591`  ·  n_top_tier: `0.67393`  ·  corrupted: `1.55947`  ·  n_sockets: `0.11122`  ·  quality: `0.01295`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 6.27083 |
| `desecrated.stat_4015621042@T1` | -5.00680 |
| `explicit.stat_2923486259@T2` | -0.96758 |
| `explicit.stat_2923486259@T1` | -0.95071 |
| `explicit.stat_3484657501@T1` | -0.89207 |
| `explicit.stat_3917489142@T2` | -0.88037 |
| `explicit.stat_3261801346@T2` | -0.84429 |
| `explicit.stat_1263695895@T1` | -0.81363 |
| `explicit.stat_1263695895@T2` | -0.75559 |
| `explicit.stat_3917489142@T1` | -0.75475 |
| `explicit.stat_1999113824@T1` | -0.75418 |
| `explicit.stat_124859000@T1` | -0.75052 |

### armour.chest — n=2618, R²=-0.845

intercept: `8.1076`  ·  log_price: True  ·  ilvl: `-0.10263`  ·  n_mods: `-0.01419`  ·  n_top_tier: `0.67850`  ·  corrupted: `-0.91172`  ·  n_sockets: `0.04077`  ·  quality: `0.05595`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 7.39803 |
| `explicit.stat_1671376347@T1` | 3.64519 |
| `explicit.stat_3981240776@T1` | 3.07501 |
| `explicit.stat_2339757871@T1` | -2.18830 |
| `explicit.stat_2339757871@T2` | -1.84325 |
| `explicit.stat_3372524247@T1` | 1.54993 |
| `explicit.stat_4220027924@T1` | 1.18835 |
| `explicit.stat_3261801346@T1` | -1.10317 |
| `explicit.stat_4052037485@T1` | -0.94920 |
| `explicit.stat_4015621042@T2` | -0.90643 |
| `explicit.stat_3301100256@T2` | -0.89310 |
| `explicit.stat_1062208444@T1` | -0.87595 |

### armour.gloves — n=2565, R²=-0.8603

intercept: `7.4527`  ·  log_price: True  ·  ilvl: `-0.09600`  ·  n_mods: `0.05105`  ·  n_top_tier: `0.10288`  ·  corrupted: `1.15609`  ·  n_sockets: `0.01314`  ·  quality: `-0.02744`

| stat_id | coef |
|---|---|
| `explicit.stat_4067062424@T2` | 3.44696 |
| `explicit.stat_3372524247@T1` | 2.94550 |
| `explicit.stat_3556824919@T1` | 2.86379 |
| `explicit.stat_4067062424@T1` | 1.54696 |
| `explicit.stat_9187492@T1` | 1.53311 |
| `explicit.stat_1671376347@T1` | 1.49473 |
| `rune.stat_201332984` | 1.37541 |
| `explicit.stat_9187492@T2` | -0.85175 |
| `explicit.stat_9187492` | 0.66694 |
| `explicit.stat_681332047@T1` | 0.49973 |
| `explicit.stat_2451402625@T2` | -0.41257 |
| `explicit.stat_4015621042@T2` | 0.35610 |

### accessory.amulet — n=2341, R²=-0.5236

intercept: `10.4737`  ·  log_price: True  ·  ilvl: `-0.09867`  ·  n_mods: `-0.67464`  ·  n_top_tier: `1.55527`  ·  corrupted: `-1.72811`  ·  n_sockets: `-1.09824`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T2` | -6.31388 |
| `explicit.stat_2923486259@T1` | -5.89854 |
| `explicit.stat_328541901@T1` | -4.51019 |
| `explicit.stat_983749596@T1` | -4.23680 |
| `explicit.stat_2482852589@T1` | -4.23586 |
| `explicit.stat_3325883026@T2` | -3.89451 |
| `explicit.stat_4220027924@T2` | -3.85141 |
| `explicit.stat_1671376347@T2` | -3.40515 |
| `explicit.stat_3325883026@T1` | -3.31445 |
| `explicit.stat_2482852589@T2` | -3.29643 |
| `explicit.stat_803737631@T2` | -3.28782 |
| `explicit.stat_4080418644@T1` | -3.27319 |

### weapon.wand — n=2187, R²=-1.0113

intercept: `7.4938`  ·  log_price: True  ·  ilvl: `-0.09268`  ·  n_mods: `-0.05381`  ·  n_top_tier: `0.26498`  ·  corrupted: `0.20207`  ·  n_sockets: `0.02383`  ·  quality: `0.01484`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 6.17801 |
| `explicit.stat_1600707273@T1` | 6.17083 |
| `explicit.stat_2254480358@T1` | 6.09341 |
| `explicit.stat_1545858329@T1` | 6.07484 |
| `explicit.stat_4226189338@T1` | 5.60939 |
| `explicit.stat_124131830@T1` | 3.64804 |
| `crafted.stat_124131830` | 1.91252 |
| `explicit.stat_124131830@T2` | -1.75174 |
| `rune.stat_3278136794` | 0.66353 |
| `explicit.stat_124131830` | 0.58196 |
| `explicit.stat_1263695895@T1` | -0.55842 |
| `explicit.stat_2974417149@T1` | 0.55348 |

### accessory.ring — n=2131, R²=-0.2867

intercept: `6.5923`  ·  log_price: True  ·  ilvl: `-0.00219`  ·  n_mods: `-0.01614`  ·  n_top_tier: `-0.00693`  ·  corrupted: `0.13656`  ·  n_sockets: `0.31935`  ·  quality: `0.01164`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T2` | -5.84710 |
| `explicit.stat_1050105434@T1` | -5.07419 |
| `explicit.stat_803737631@T2` | -3.59099 |
| `explicit.stat_3325883026@T2` | -3.23355 |
| `explicit.stat_3325883026@T1` | 3.13334 |
| `explicit.stat_707457662@T2` | 0.65766 |
| `explicit.stat_707457662@T1` | 0.65372 |
| `explicit.stat_3299347043@T1` | -0.35424 |
| `explicit.stat_2923486259@T2` | -0.32668 |
| `explicit.stat_3325883026` | -0.23675 |
| `explicit.stat_803737631@T1` | 0.16617 |
| `explicit.stat_3962278098@T2` | -0.15822 |

### weapon.bow — n=1844, R²=-0.83

intercept: `7.5798`  ·  log_price: True  ·  ilvl: `-0.09426`  ·  n_mods: `-0.04442`  ·  n_top_tier: `0.07611`  ·  corrupted: `1.58801`  ·  n_sockets: `0.10704`  ·  quality: `-0.09694`

| stat_id | coef |
|---|---|
| `desecrated.stat_1200678966@T1` | -10.00222 |
| `explicit.stat_1037193709@T1` | 5.11386 |
| `explicit.stat_2463230181@T1` | 4.60424 |
| `explicit.stat_1202301673@T1` | 4.19725 |
| `explicit.stat_518292764@T1` | 4.14573 |
| `rune.stat_3885405204` | -2.83681 |
| `desecrated.stat_210067635@T1` | 2.28557 |
| `explicit.stat_1509134228@T1` | 1.79065 |
| `explicit.stat_210067635@T2` | 1.34479 |
| `explicit.stat_1263695895@T1` | 1.11299 |
| `explicit.stat_1263695895@T2` | 1.07783 |
| `crafted.stat_3035140377` | 0.96926 |

### weapon.crossbow — n=1760, R²=-0.8797

intercept: `8.3483`  ·  log_price: True  ·  ilvl: `-0.10470`  ·  n_mods: `-0.02511`  ·  n_top_tier: `0.42424`  ·  corrupted: `-0.05010`  ·  n_sockets: `0.01741`  ·  quality: `-0.04789`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 5.82200 |
| `explicit.stat_3336890334@T1` | 5.72561 |
| `explicit.stat_709508406@T1` | 5.49485 |
| `explicit.stat_1037193709@T2` | 2.55296 |
| `desecrated.stat_1365232741@T1` | 2.52559 |
| `desecrated.stat_3131442032@T1` | 2.52559 |
| `explicit.stat_1980802737@T2` | 1.66681 |
| `explicit.stat_1980802737` | 1.66681 |
| `desecrated.stat_538981065@T1` | -1.63836 |
| `explicit.stat_691932474@T1` | -0.68223 |
| `crafted.stat_210067635@T2` | 0.65861 |
| `explicit.stat_1940865751@T1` | -0.63397 |

### weapon.sceptre — n=787, R²=0.0

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

### weapon.spear — n=703, R²=0.0

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

### armour.focus — n=679, R²=0.0

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

### jewel — n=580, R²=0.0623

intercept: `-2.2126`  ·  log_price: True  ·  ilvl: `0.03389`  ·  n_mods: `1.23371`  ·  n_top_tier: `0.26544`  ·  corrupted: `0.06710`

| stat_id | coef |
|---|---|
| `explicit.stat_1782086450@T1` | -10.98474 |
| `explicit.stat_3780644166@T1` | -10.71414 |
| `explicit.stat_3824372849@T1` | -10.21186 |
| `explicit.stat_3377888098@T1` | -7.94395 |
| `explicit.stat_680068163@T1` | 7.87398 |
| `explicit.stat_1569101201@T1` | 7.80428 |
| `explicit.stat_2456523742@T1` | 7.76398 |
| `explicit.stat_818778753@T1` | -7.67689 |
| `explicit.stat_3851254963@T1` | 7.63516 |
| `explicit.stat_3714003708@T1` | -7.36438 |
| `explicit.stat_1181419800@T1` | -7.21386 |
| `explicit.stat_1459321413@T1` | 7.11691 |

### armour.shield — n=559, R²=0.0

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

### armour.quiver — n=295, R²=0.0

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

### weapon.warstaff — n=283, R²=-0.0135

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2694482655@T1` | 0.00002 |
| `explicit.stat_387439868@T2` | 0.00001 |
| `explicit.stat_821021828@T1` | -0.00001 |
| `explicit.stat_1368271171@T1` | 0.00001 |
| `explicit.stat_1940865751@T1` | 0.00001 |
| `explicit.stat_1940865751@T2` | 0.00001 |
| `explicit.stat_387439868@T1` | 0.00001 |
| `explicit.stat_3336890334@T1` | 0.00001 |
| `explicit.stat_1368271171@T2` | 0.00001 |
| `explicit.stat_9187492@T2` | 0.00001 |
| `explicit.stat_518292764@T1` | 0.00001 |
| `explicit.stat_3639275092@T2` | -0.00001 |

### weapon.staff — n=280, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

### flask.charm — n=246, R²=-0.1094

intercept: `0.1551`  ·  log_price: True  ·  ilvl: `0.00075`  ·  n_mods: `-0.08717`  ·  n_top_tier: `-0.08237`  ·  corrupted: `-0.04007`  ·  quality: `-0.00817`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.64612 |
| `explicit.stat_280890192` | -0.21242 |
| `implicit.stat_2016937536` | 0.17342 |
| `implicit.stat_2778646494` | -0.12421 |
| `implicit.stat_4010341289` | -0.12052 |
| `implicit.stat_3699444296` | -0.10171 |
| `implicit.stat_1412682799` | -0.08597 |
| `implicit.stat_2994271459` | 0.07702 |
| `implicit.stat_3310778564` | -0.07362 |
| `implicit.stat_585126960` | -0.06936 |
| `explicit.stat_2716923832` | -0.06404 |
| `implicit.stat_1810482573` | -0.05942 |

### weapon.twomace — n=215, R²=0.0

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
| `explicit.stat_1940865751@T2` | 0.00000 |
| `explicit.stat_210067635` | 0.00000 |
| `explicit.stat_210067635@T2` | 0.00000 |

## Coverage (listings per base)

- … **Utility Belt** — 793 listings (793 priced) [1.0–737.3 ex]
- … **Dueling Wand** — 699 listings (699 priced) [1.0–726.1 ex]
- … **Obliterator Bow** — 543 listings (543 priced) [0.5–726.1 ex]
- … **Stellar Amulet** — 522 listings (522 priced) [0.3–737.3 ex]
- … **Solar Amulet** — 416 listings (416 priced) [1.0–737.3 ex]
- … **Siphoning Wand** — 403 listings (403 priced) [1.0–726.1 ex]
- … **Gold Amulet** — 402 listings (402 priced) [0.3–737.3 ex]
- … **Warmonger Bow** — 397 listings (397 priced) [1.0–726.1 ex]
- … **Galvanic Wand** — 383 listings (383 priced) [1.0–726.1 ex]
- … **Ancestral Tiara** — 381 listings (381 priced) [1.0–737.3 ex]
- … **Plate Belt** — 380 listings (380 priced) [1.0–737.3 ex]
- … **Emerald** — 376 listings (376 priced) [0.4–726.1 ex]
- … **Heavy Belt** — 362 listings (362 priced) [0.5–737.3 ex]
- … **Attuned Wand** — 357 listings (357 priced) [0.3–726.1 ex]
- … **Withered Wand** — 344 listings (344 priced) [1.0–726.1 ex]
- … **Amethyst Ring** — 337 listings (337 priced) [1.0–737.3 ex]
- … **Prismatic Ring** — 323 listings (323 priced) [0.4–737.3 ex]
- … **Trarthan Cannon** — 323 listings (323 priced) [0.7–726.1 ex]
- … **Long Belt** — 315 listings (315 priced) [1.0–737.3 ex]
- … **Lapis Amulet** — 310 listings (310 priced) [0.6–737.3 ex]
- … **Amber Amulet** — 308 listings (308 priced) [0.3–737.3 ex]
- … **Gold Ring** — 300 listings (300 priced) [0.7–737.3 ex]
- … **Rawhide Belt** — 299 listings (299 priced) [1.0–737.3 ex]
- … **Sapphire** — 299 listings (299 priced) [0.4–726.1 ex]
- … **Sapphire Ring** — 291 listings (291 priced) [0.5–737.3 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-20T14:16:13+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **683661** (681548 priced in exalted)
- Distinct bases: 998 · distinct mods: 3307 · mod rows: 3236096
- Sold signals: **24375** sold · 389039 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-20T14:01:56+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×20.74** (median |log error| 3.0319)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.15** · typical error ×57.60 · ±30% 5% · n=99518
- Premium segment (60ex+): skill **+0.15** · typical error ×300.88 · ±30% 0% · n=66607

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 14521 | ×55.28 | 21% | +0.03 | +0.05 |
| jewel | 13792 | ×10.32 | 5% | +0.11 | +0.13 |
| accessory.amulet | 13136 | ×36.34 | 18% | +0.04 | +0.04 |
| accessory.belt | 9439 | ×22.52 | 20% | +0.04 | +0.05 |
| armour.chest | 9054 | ×17.28 | 22% | +0.08 | +0.10 |
| armour.helmet | 8911 | ×24.13 | 15% | +0.09 | +0.11 |
| armour.boots | 8225 | ×26.52 | 20% | +0.10 | +0.14 |
| armour.gloves | 8030 | ×35.16 | 14% | +0.08 | +0.11 |
| other | 8002 | ×2.00 | 42% | +0.10 | +0.16 |
| weapon.wand | 4821 | ×44.55 | 15% | +0.10 | +0.11 |
| weapon.bow | 3791 | ×25.61 | 12% | +0.16 | +0.17 |
| weapon.crossbow | 3560 | ×24.23 | 14% | +0.12 | +0.17 |
| weapon.warstaff | 2412 | ×14.28 | 7% | +0.22 | +0.19 |
| weapon.staff | 2316 | ×17.23 | 6% | +0.18 | +0.17 |
| weapon.sceptre | 2303 | ×20.91 | 5% | +0.09 | +0.10 |
| weapon.spear | 1826 | ×15.27 | 7% | +0.14 | +0.14 |
| armour.focus | 1516 | ×13.73 | 7% | +0.11 | +0.12 |
| armour.quiver | 1424 | ×19.77 | 7% | +0.17 | +0.18 |
| flask.charm | 1207 | ×12.76 | 27% | -0.01 | +0.01 |
| armour.shield | 1179 | ×10.14 | 8% | +0.10 | +0.12 |
| weapon.twomace | 1092 | ×7.97 | 9% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=75648, R²=-0.985

intercept: `-1.9460`  ·  log_price: True  ·  ilvl: `0.02435`  ·  n_mods: `0.84676`  ·  n_top_tier: `-0.27158`  ·  corrupted: `0.47437`  ·  quality: `0.00031`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.33235 |
| `explicit.stat_3485067555@T1` | 2.33359 |
| `explicit.stat_1594812856@T1` | 2.07566 |
| `explicit.stat_1569101201@T1` | -1.50328 |
| `explicit.stat_1869147066@T1` | -1.45787 |
| `explicit.stat_3780644166@T1` | -1.42751 |
| `explicit.stat_4147897060@T1` | -1.37753 |
| `explicit.stat_3174700878@T1` | 1.31666 |
| `explicit.stat_3374165039@T1` | -1.25133 |
| `explicit.stat_2523933828@T1` | -1.22880 |
| `explicit.stat_318953428@T1` | -1.11297 |
| `explicit.stat_3714003708@T1` | 1.07387 |

### accessory.ring — n=66302, R²=-2.0317

intercept: `3.6923`  ·  log_price: True  ·  ilvl: `-0.04596`  ·  n_mods: `0.00042`  ·  n_top_tier: `0.98702`  ·  corrupted: `0.00821`  ·  n_sockets: `1.92253`  ·  quality: `0.02042`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.01207 |
| `explicit.stat_1573130764@T2` | -1.00819 |
| `explicit.stat_2231156303@T1` | -1.00799 |
| `explicit.stat_4220027924@T2` | -1.00701 |
| `explicit.stat_2557965901@T2` | -1.00494 |
| `explicit.stat_803737631@T1` | -1.00475 |
| `explicit.stat_4080418644@T1` | -1.00404 |
| `explicit.stat_2557965901@T1` | -1.00379 |
| `explicit.stat_2891184298@T2` | -0.99817 |
| `explicit.stat_3325883026@T1` | -0.99758 |
| `explicit.stat_789117908@T2` | -0.99749 |
| `explicit.stat_2144192055@T1` | -0.99717 |

### other — n=65146, R²=-0.6588

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.08993`  ·  n_top_tier: `0.25665`  ·  corrupted: `0.03170`  ·  n_sockets: `-0.00007`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.33218 |
| `implicit.stat_718638445` | 0.26983 |
| `implicit.stat_3182714256` | 0.26982 |
| `explicit.stat_3299347043@T1` | -0.25170 |
| `implicit.stat_2219129443` | 0.21827 |
| `explicit.stat_2974417149@T1` | 0.15073 |
| `explicit.stat_3917489142@T1` | -0.13758 |
| `implicit.stat_958696139` | -0.08991 |
| `explicit.stat_789117908@T1` | -0.06381 |
| `implicit.stat_3879011313` | 0.06014 |
| `implicit.stat_1416292992` | -0.05995 |
| `implicit.stat_1379411836` | -0.05218 |

### accessory.amulet — n=59738, R²=-2.1403

intercept: `3.4039`  ·  log_price: True  ·  ilvl: `-0.04266`  ·  n_mods: `-0.01928`  ·  n_top_tier: `1.35641`  ·  corrupted: `0.10651`  ·  n_sockets: `-0.12958`  ·  quality: `0.03860`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.91165 |
| `explicit.stat_3299347043@T2` | -1.87536 |
| `explicit.stat_587431675@T2` | -1.51392 |
| `explicit.stat_803737631@T1` | -1.47238 |
| `explicit.stat_2866361420@T2` | -1.44594 |
| `explicit.stat_2974417149@T1` | -1.43705 |
| `explicit.stat_1050105434@T2` | -1.42146 |
| `explicit.stat_2866361420@T1` | -1.41897 |
| `explicit.stat_803737631@T2` | -1.41892 |
| `explicit.stat_2974417149@T2` | -1.40007 |
| `explicit.stat_4080418644@T1` | -1.39078 |
| `explicit.stat_1050105434@T1` | -1.39076 |

### accessory.belt — n=43131, R²=-1.7901

intercept: `3.3778`  ·  log_price: True  ·  ilvl: `-0.04057`  ·  n_mods: `-0.02083`  ·  n_top_tier: `0.47319`  ·  corrupted: `1.14071`  ·  n_sockets: `1.42508`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.03827 |
| `explicit.stat_3299347043@T1` | -0.51640 |
| `explicit.stat_2881298780@T1` | -0.50857 |
| `explicit.stat_3299347043@T2` | -0.50125 |
| `explicit.stat_51994685@T1` | -0.49226 |
| `explicit.stat_809229260@T2` | -0.49049 |
| `explicit.stat_4220027924@T2` | -0.48864 |
| `explicit.stat_915769802@T1` | -0.48585 |
| `explicit.stat_3325883026@T1` | -0.48534 |
| `explicit.stat_1389754388@T1` | -0.47773 |
| `explicit.stat_2881298780@T2` | -0.47695 |
| `explicit.stat_1570770415@T2` | -0.47664 |

### armour.chest — n=42697, R²=-1.7636

intercept: `3.3056`  ·  log_price: True  ·  ilvl: `-0.04082`  ·  n_mods: `-0.01477`  ·  n_top_tier: `0.35003`  ·  corrupted: `0.18302`  ·  n_sockets: `0.02009`  ·  quality: `0.07426`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.67710 |
| `explicit.stat_3981240776@T1` | 1.03953 |
| `explicit.stat_986397080@T2` | -0.45163 |
| `explicit.stat_986397080@T1` | -0.44198 |
| `explicit.stat_3484657501@T1` | -0.38547 |
| `explicit.stat_2339757871@T2` | -0.38395 |
| `explicit.stat_1692879867@T2` | -0.38342 |
| `explicit.stat_915769802@T2` | -0.37703 |
| `explicit.stat_4080418644@T1` | -0.37384 |
| `explicit.stat_4080418644@T2` | -0.37226 |
| `explicit.stat_3301100256@T2` | -0.36346 |
| `explicit.stat_2451402625@T1` | -0.36306 |

### armour.helmet — n=41544, R²=-1.6117

intercept: `3.4200`  ·  log_price: True  ·  ilvl: `-0.04329`  ·  n_mods: `-0.02694`  ·  n_top_tier: `0.57209`  ·  corrupted: `0.64635`  ·  n_sockets: `0.07904`  ·  quality: `0.06487`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.38463 |
| `crafted.stat_3917489142@T1` | -1.08811 |
| `explicit.stat_3917489142@T2` | -0.93878 |
| `explicit.stat_1263695895@T1` | -0.92108 |
| `explicit.stat_3917489142@T1` | -0.83890 |
| `explicit.stat_2162097452@T2` | -0.72219 |
| `explicit.stat_1263695895@T2` | -0.71151 |
| `explicit.stat_53045048@T1` | -0.66045 |
| `explicit.stat_1999113824@T1` | -0.64552 |
| `explicit.stat_803737631@T1` | -0.63847 |
| `explicit.stat_803737631@T2` | -0.62380 |
| `explicit.stat_3321629045@T2` | -0.62159 |

### armour.boots — n=38562, R²=-1.6925

intercept: `3.6362`  ·  log_price: True  ·  ilvl: `-0.04489`  ·  n_mods: `-0.02197`  ·  n_top_tier: `0.47864`  ·  corrupted: `0.08037`  ·  n_sockets: `0.04824`  ·  quality: `0.06683`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.75541 |
| `crafted.stat_3917489142@T1` | 1.56136 |
| `explicit.stat_2339757871@T1` | -1.41943 |
| `explicit.stat_2923486259@T1` | 0.75011 |
| `explicit.stat_3917489142@T2` | -0.60856 |
| `explicit.stat_3299347043@T1` | -0.58154 |
| `explicit.stat_2923486259@T2` | -0.55535 |
| `explicit.stat_1874553720@T1` | -0.55408 |
| `explicit.stat_1671376347@T2` | -0.52771 |
| `explicit.stat_1999113824@T2` | -0.52169 |
| `explicit.stat_328541901@T2` | -0.52093 |
| `explicit.stat_2160282525@T1` | -0.52072 |

### armour.gloves — n=37510, R²=-1.6728

intercept: `3.7748`  ·  log_price: True  ·  ilvl: `-0.04949`  ·  n_mods: `-0.00545`  ·  n_top_tier: `0.77862`  ·  corrupted: `-0.03716`  ·  n_sockets: `0.15025`  ·  quality: `0.06111`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.71386 |
| `explicit.stat_3321629045@T2` | -1.04085 |
| `explicit.stat_4052037485@T1` | -1.03052 |
| `explicit.stat_4015621042@T2` | -1.01754 |
| `explicit.stat_3484657501@T2` | -1.00741 |
| `rune.stat_201332984` | 0.99618 |
| `explicit.stat_2923486259@T1` | -0.99198 |
| `explicit.stat_9187492@T2` | -0.98115 |
| `explicit.stat_4052037485@T2` | -0.96726 |
| `explicit.stat_3484657501@T1` | -0.90967 |
| `explicit.stat_803737631@T1` | -0.90500 |
| `explicit.stat_803737631@T2` | -0.90269 |

### weapon.wand — n=22431, R²=-1.939

intercept: `4.1520`  ·  log_price: True  ·  ilvl: `-0.05137`  ·  n_mods: `-0.06543`  ·  n_top_tier: `0.32956`  ·  corrupted: `-0.00025`  ·  n_sockets: `0.05641`  ·  quality: `0.04351`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -3.44412 |
| `explicit.stat_1545858329@T1` | 2.86857 |
| `explicit.stat_2254480358@T1` | 2.61889 |
| `explicit.stat_124131830@T1` | 2.34677 |
| `explicit.stat_591105508@T1` | 2.06626 |
| `explicit.stat_4226189338@T1` | 1.94472 |
| `explicit.stat_736967255@T2` | 1.90991 |
| `explicit.stat_2254480358@T2` | 1.24710 |
| `crafted.stat_124131830` | 1.21293 |
| `explicit.stat_4226189338@T2` | 1.08169 |
| `explicit.stat_1263695895@T2` | -0.78844 |
| `explicit.stat_1263695895@T1` | -0.67728 |

### flask.charm — n=19031, R²=-0.6538

intercept: `0.1047`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.70367`  ·  corrupted: `1.50377`  ·  quality: `0.00763`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.62529 |
| `explicit.stat_1056492907` | 2.56403 |
| `explicit.stat_828533480@T2` | -1.70370 |
| `explicit.stat_1120862500@T2` | -1.70369 |
| `explicit.stat_1873752457@T2` | -1.70367 |
| `explicit.stat_3196823591@T2` | -1.70363 |
| `explicit.stat_2365392475@T2` | -1.70362 |
| `explicit.stat_2676834156@T2` | -1.70361 |
| `explicit.stat_388617051@T2` | -1.70088 |
| `explicit.stat_828533480@T1` | -1.69971 |
| `explicit.stat_2541588185@T2` | -1.69689 |
| `explicit.stat_1873752457@T1` | -1.68462 |

### weapon.bow — n=17917, R²=-1.7694

intercept: `3.8250`  ·  log_price: True  ·  ilvl: `-0.04577`  ·  n_mods: `-0.08732`  ·  n_top_tier: `0.79631`  ·  corrupted: `0.63516`  ·  n_sockets: `0.06659`  ·  quality: `0.02746`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.74470 |
| `explicit.stat_1263695895@T1` | -1.33582 |
| `crafted.stat_3035140377` | 1.32018 |
| `explicit.stat_1263695895@T2` | -1.16472 |
| `explicit.stat_3336890334@T1` | 1.08466 |
| `explicit.stat_2463230181@T2` | -1.05085 |
| `explicit.stat_1509134228@T1` | -0.98506 |
| `explicit.stat_3695891184@T2` | -0.94647 |
| `explicit.stat_1368271171@T2` | -0.92868 |
| `explicit.stat_3695891184@T1` | -0.90638 |
| `explicit.stat_210067635@T2` | -0.89306 |
| `explicit.stat_3336890334@T2` | -0.83573 |

### weapon.crossbow — n=16789, R²=-1.7093

intercept: `3.8582`  ·  log_price: True  ·  ilvl: `-0.04664`  ·  n_mods: `-0.08399`  ·  n_top_tier: `0.42260`  ·  corrupted: `0.12554`  ·  n_sockets: `0.08834`  ·  quality: `0.02739`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.61938 |
| `explicit.stat_2250681686@T2` | -1.32720 |
| `explicit.stat_1980802737` | 1.30320 |
| `explicit.stat_1202301673@T1` | 1.30008 |
| `explicit.stat_2250681686` | 0.94343 |
| `crafted.stat_3035140377` | 0.81750 |
| `explicit.stat_1509134228@T1` | 0.73565 |
| `explicit.stat_709508406@T1` | 0.72394 |
| `explicit.stat_3695891184@T1` | -0.71540 |
| `explicit.stat_3336890334@T2` | -0.66245 |
| `explicit.stat_3695891184@T2` | -0.64492 |
| `explicit.stat_1037193709@T2` | -0.63624 |

### weapon.warstaff — n=11600, R²=-0.3439

intercept: `-10.4636`  ·  log_price: True  ·  ilvl: `0.13981`  ·  n_mods: `-0.19888`  ·  n_top_tier: `0.35854`  ·  corrupted: `0.31991`  ·  n_sockets: `0.14575`  ·  quality: `0.05870`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 1.87221 |
| `desecrated.stat_2231156303@T1` | 1.87221 |
| `crafted.stat_210067635@T2` | 1.25235 |
| `explicit.stat_328541901@T2` | -0.91264 |
| `explicit.stat_328541901@T1` | -0.89206 |
| `desecrated.stat_9187492` | 0.79532 |
| `rune.stat_243313994` | 0.68664 |
| `explicit.stat_1368271171@T1` | -0.67719 |
| `explicit.stat_691932474@T2` | -0.63072 |
| `explicit.stat_1037193709@T1` | 0.58889 |
| `explicit.stat_1509134228@T1` | 0.55765 |
| `explicit.stat_821021828@T2` | -0.55295 |

### weapon.staff — n=10981, R²=-0.3602

intercept: `-15.9445`  ·  log_price: True  ·  ilvl: `0.20466`  ·  n_mods: `-0.07566`  ·  n_top_tier: `0.35713`  ·  corrupted: `0.78659`  ·  n_sockets: `0.19179`  ·  quality: `0.03398`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.12561 |
| `explicit.stat_591105508@T1` | 2.04273 |
| `explicit.stat_1545858329@T1` | 1.85647 |
| `explicit.stat_124131830@T1` | 1.80633 |
| `explicit.stat_2254480358@T1` | 1.64101 |
| `explicit.stat_1600707273@T1` | 1.49588 |
| `explicit.stat_2254480358@T2` | 1.01415 |
| `explicit.stat_293638271@T2` | -0.99267 |
| `explicit.stat_3962278098@T2` | 0.82497 |
| `explicit.stat_4226189338@T2` | 0.71124 |
| `rune.stat_124131830` | 0.64123 |
| `explicit.stat_1600707273@T2` | 0.63200 |

### weapon.sceptre — n=10801, R²=-0.3294

intercept: `-21.7067`  ·  log_price: True  ·  ilvl: `0.27516`  ·  n_mods: `0.03121`  ·  n_top_tier: `0.09991`  ·  corrupted: `0.16588`  ·  n_sockets: `0.22605`  ·  quality: `0.03393`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.32404 |
| `explicit.stat_3057012405@T1` | 1.45931 |
| `explicit.stat_1263695895@T2` | -1.22267 |
| `explicit.stat_2162097452@T2` | 1.13420 |
| `explicit.stat_101878827@T2` | 0.99188 |
| `explicit.stat_101878827@T1` | 0.97797 |
| `explicit.stat_1263695895@T1` | -0.93360 |
| `explicit.stat_1798257884@T2` | 0.92419 |
| `explicit.stat_849987426@T1` | 0.84988 |
| `explicit.stat_2854751904@T2` | -0.80021 |
| `explicit.stat_1998951374@T1` | 0.66425 |
| `explicit.stat_1250712710@T2` | 0.51198 |

### weapon.spear — n=8754, R²=-0.372

intercept: `-13.8549`  ·  log_price: True  ·  ilvl: `0.18880`  ·  n_mods: `-0.12506`  ·  n_top_tier: `0.57263`  ·  corrupted: `-0.58479`  ·  n_sockets: `0.20511`  ·  quality: `0.07398`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -4.82957 |
| `crafted.stat_210067635@T2` | -3.02802 |
| `explicit.stat_1202301673@T1` | 1.34451 |
| `explicit.stat_1509134228@T1` | 1.25315 |
| `explicit.stat_9187492@T1` | 1.20745 |
| `explicit.stat_4080418644@T2` | -0.99674 |
| `explicit.stat_1940865751@T2` | -0.98618 |
| `explicit.stat_691932474@T1` | -0.92389 |
| `crafted.stat_3035140377` | 0.90679 |
| `explicit.stat_691932474@T2` | -0.84965 |
| `desecrated.stat_210067635@T1` | -0.83926 |
| `explicit.stat_748522257@T2` | -0.81579 |

### armour.focus — n=7148, R²=-0.3359

intercept: `-16.2750`  ·  log_price: True  ·  ilvl: `0.20674`  ·  n_mods: `-0.12561`  ·  n_top_tier: `1.04766`  ·  corrupted: `0.03693`  ·  n_sockets: `0.31999`  ·  quality: `0.02825`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 5.42076 |
| `explicit.stat_2923486259@T1` | -1.83467 |
| `explicit.stat_4220027924@T1` | -1.77147 |
| `explicit.stat_2923486259@T2` | -1.43190 |
| `explicit.stat_4220027924@T2` | -1.29027 |
| `explicit.stat_2231156303@T2` | -1.25580 |
| `explicit.stat_274716455@T1` | -1.23490 |
| `explicit.stat_2231156303@T1` | -1.20334 |
| `explicit.stat_2339757871@T2` | -1.20295 |
| `explicit.stat_2768835289@T1` | -1.17591 |
| `explicit.stat_4015621042@T1` | -1.16759 |
| `explicit.stat_737908626@T2` | -1.13206 |

### armour.quiver — n=6660, R²=-0.2938

intercept: `-16.6527`  ·  log_price: True  ·  ilvl: `0.20071`  ·  n_mods: `-0.10776`  ·  n_top_tier: `0.71829`  ·  corrupted: `0.94133`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.06573 |
| `explicit.stat_2463230181@T1` | 1.48188 |
| `explicit.stat_681332047@T2` | -1.35983 |
| `explicit.stat_1573130764@T2` | -1.08854 |
| `explicit.stat_681332047@T1` | -1.08643 |
| `explicit.stat_1573130764@T1` | -1.07463 |
| `explicit.stat_4067062424@T1` | -0.95513 |
| `explicit.stat_803737631@T1` | -0.86363 |
| `explicit.stat_2321178454@T2` | -0.84707 |
| `explicit.stat_4067062424@T2` | -0.83888 |
| `explicit.stat_2463230181@T2` | 0.70939 |
| `explicit.stat_803737631@T2` | -0.70581 |

### armour.shield — n=5761, R²=-0.4157

intercept: `-13.8406`  ·  log_price: True  ·  ilvl: `0.18288`  ·  n_mods: `-0.10186`  ·  n_top_tier: `0.54702`  ·  corrupted: `-0.38456`  ·  n_sockets: `0.45734`  ·  quality: `0.05264`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.27873 |
| `explicit.stat_3321629045@T2` | -1.07496 |
| `explicit.stat_2339757871@T1` | -0.99162 |
| `explicit.stat_4095671657@T2` | -0.94610 |
| `explicit.stat_3676141501@T1` | 0.87470 |
| `explicit.stat_1011760251@T1` | -0.87178 |
| `explicit.stat_2451402625@T1` | -0.86637 |
| `explicit.stat_2923486259@T1` | -0.84651 |
| `explicit.stat_2481353198@T1` | -0.84391 |
| `explicit.stat_2901986750@T1` | -0.83884 |
| `explicit.stat_4220027924@T1` | -0.81025 |
| `explicit.stat_3484657501@T1` | -0.78025 |

### weapon.twomace — n=5263, R²=-0.4475

intercept: `-11.2833`  ·  log_price: True  ·  ilvl: `0.15082`  ·  n_mods: `-0.19763`  ·  n_top_tier: `0.34885`  ·  corrupted: `0.58799`  ·  n_sockets: `0.12945`  ·  quality: `0.06801`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.09064 |
| `explicit.stat_1037193709@T1` | -1.34472 |
| `explicit.stat_1263695895@T2` | -1.27306 |
| `explicit.stat_3336890334@T1` | -1.13812 |
| `explicit.stat_2694482655@T1` | 1.09620 |
| `explicit.stat_9187492@T1` | -0.89334 |
| `explicit.stat_518292764@T1` | 0.85425 |
| `explicit.stat_3695891184@T1` | -0.80111 |
| `explicit.stat_3695891184@T2` | -0.72948 |
| `explicit.stat_691932474@T1` | -0.71804 |
| `explicit.stat_387439868@T2` | -0.67092 |
| `explicit.stat_1263695895@T1` | -0.62625 |

## Coverage (listings per base)

- … **Sapphire** — 34877 listings (34821 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 33950 listings (33908 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 25994 listings (25963 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 12345 listings (12327 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11199 listings (11175 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10802 listings (10777 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 10716 listings (10705 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10075 listings (10053 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10000 listings (9978 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 9559 listings (9546 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8314 listings (8299 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7995 listings (7986 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 7891 listings (7882 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7218 listings (7196 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6885 listings (6878 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 6849 listings (6830 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6814 listings (6800 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6766 listings (6759 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6725 listings (6697 priced) [0.3–398912568423.8 ex]
- … **Ancestral Tiara** — 6649 listings (6620 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6593 listings (6584 priced) [0.2–275252424.7 ex]
- … **Bloodstone Amulet** — 6555 listings (6545 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6245 listings (6242 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6117 listings (6103 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5967 listings (5957 priced) [0.3–398912568423.8 ex]

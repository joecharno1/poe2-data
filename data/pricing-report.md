# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-03T12:03:42+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **47943** (47943 priced in exalted)
- Distinct bases: 752 · distinct mods: 1570 · mod rows: 241947
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-03T11:50:11+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.57** (median |log error| 2.0246)
- Within ±30% of asking price: **27%**
- Skill vs constant-price guess: **-0.04** (> 0 = the mods carry signal)
- Calibration: 63% of actuals above prediction (target ≈ 75%)

| group | n_test | ×err | ±30% | skill |
|---|---|---|---|---|
| accessory.belt | 774 | ×7.96 | 16% | -0.01 |
| armour.chest | 765 | ×10.61 | 47% | -0.00 |
| armour.helmet | 764 | ×7.91 | 7% | -0.38 |
| armour.boots | 689 | ×8.52 | 7% | -0.38 |
| armour.gloves | 671 | ×8.96 | 10% | -0.40 |
| accessory.amulet | 650 | ×43.56 | 2% | +0.21 |
| accessory.ring | 598 | ×5.91 | 11% | -0.14 |
| weapon.wand | 592 | ×9.21 | 33% | +0.00 |
| weapon.bow | 535 | ×8.25 | 33% | -0.06 |
| weapon.crossbow | 504 | ×6.90 | 21% | -0.04 |
| other | 467 | ×9.95 | 35% | +0.44 |
| jewel | 325 | ×6.60 | 11% | -0.16 |
| weapon.sceptre | 165 | ×1.00 | 99% | +0.00 |
| weapon.spear | 161 | ×1.00 | 99% | +0.00 |
| armour.focus | 139 | ×1.00 | 100% | n/a |
| armour.shield | 115 | ×1.00 | 100% | n/a |
| weapon.warstaff | 69 | ×1.00 | 86% | +0.00 |
| flask.charm | 57 | ×1.06 | 65% | -0.16 |
| weapon.staff | 55 | ×1.00 | 100% | n/a |
| armour.quiver | 50 | ×1.00 | 96% | +0.00 |
| weapon.twomace | 35 | ×1.00 | 100% | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=4639, R²=0.0528

intercept: `1.5754`  ·  log_price: True  ·  ilvl: `0.00097`  ·  n_mods: `0.00857`  ·  n_top_tier: `0.31529`  ·  corrupted: `4.87438`  ·  n_sockets: `-0.01521`  ·  quality: `-0.00196`

| stat_id | coef |
|---|---|
| `explicit.stat_2968503605@T1` | 4.02934 |
| `explicit.stat_2974417149@T1` | 1.72272 |
| `explicit.stat_124131830@T1` | 1.25056 |
| `explicit.stat_1263695895@T1` | -0.85369 |
| `explicit.stat_4080418644@T1` | -0.70329 |
| `explicit.stat_124131830` | -0.69804 |
| `explicit.stat_4080418644@T2` | -0.55119 |
| `explicit.stat_3299347043@T1` | -0.53792 |
| `explicit.stat_4052037485@T1` | -0.47478 |
| `explicit.stat_789117908@T1` | 0.47301 |
| `explicit.stat_3299347043@T2` | -0.47047 |
| `explicit.stat_3372524247@T1` | -0.41706 |

### accessory.belt — n=3709, R²=-1.0132

intercept: `4.4165`  ·  log_price: True  ·  ilvl: `-0.05700`  ·  n_mods: `-0.01814`  ·  n_top_tier: `-0.11116`  ·  corrupted: `0.11021`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.69464 |
| `explicit.stat_1836676211@T1` | 1.36387 |
| `implicit.stat_731781020` | 0.93624 |
| `explicit.stat_4220027924@T1` | 0.71879 |
| `explicit.stat_1412217137@T2` | 0.64794 |
| `explicit.stat_3299347043@T1` | -0.37849 |
| `explicit.stat_4220027924@T2` | 0.31727 |
| `explicit.stat_3299347043@T2` | -0.29496 |
| `explicit.stat_2881298780@T2` | 0.28369 |
| `explicit.stat_2923486259@T1` | 0.23009 |
| `explicit.stat_2881298780@T1` | 0.21558 |
| `explicit.stat_1389754388@T1` | 0.21339 |

### armour.helmet — n=3577, R²=-0.1376

intercept: `2.2698`  ·  log_price: True  ·  ilvl: `0.00032`  ·  n_mods: `0.00423`  ·  n_top_tier: `0.06716`  ·  corrupted: `0.13675`  ·  n_sockets: `-0.19644`  ·  quality: `-0.00383`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 6.04414 |
| `explicit.stat_2339757871@T1` | 4.52491 |
| `desecrated.stat_3299347043@T2` | 2.78152 |
| `desecrated.stat_4015621042@T1` | 1.95887 |
| `explicit.stat_1671376347@T1` | 1.89840 |
| `explicit.stat_4080418644@T1` | 1.75677 |
| `explicit.stat_3033371881@T1` | 1.73967 |
| `explicit.stat_2451402625@T2` | 1.71670 |
| `explicit.stat_2923486259@T1` | 1.42899 |
| `explicit.stat_4052037485@T2` | 1.39021 |
| `explicit.stat_4080418644@T2` | 1.21345 |
| `explicit.stat_124859000@T1` | 0.74713 |

### armour.chest — n=3573, R²=-0.1879

intercept: `2.4271`  ·  log_price: True  ·  ilvl: `-0.00179`  ·  n_mods: `-0.03772`  ·  n_top_tier: `-0.06955`  ·  corrupted: `0.16133`  ·  n_sockets: `-0.17898`  ·  quality: `-0.03178`

| stat_id | coef |
|---|---|
| `explicit.stat_4080418644@T2` | 3.04838 |
| `explicit.stat_4080418644@T1` | 1.95949 |
| `explicit.stat_915769802@T1` | 1.38276 |
| `rune.stat_836936635` | 0.85812 |
| `explicit.stat_3981240776@T1` | 0.65429 |
| `explicit.stat_2339757871@T2` | -0.61707 |
| `explicit.stat_1692879867@T2` | 0.53505 |
| `explicit.stat_3301100256@T2` | 0.52097 |
| `explicit.stat_3362812763@T2` | -0.47317 |
| `implicit.stat_1978899297` | -0.45047 |
| `explicit.stat_2339757871@T1` | -0.44953 |
| `explicit.stat_124859000@T2` | -0.39353 |

### armour.boots — n=3522, R²=-0.1467

intercept: `2.3137`  ·  log_price: True  ·  ilvl: `-0.00018`  ·  n_mods: `-0.00318`  ·  n_top_tier: `0.77147`  ·  corrupted: `0.06131`  ·  n_sockets: `-0.01006`  ·  quality: `-0.00160`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 5.52906 |
| `explicit.stat_2923486259@T1` | 1.04613 |
| `explicit.stat_1671376347@T1` | 1.00855 |
| `explicit.stat_3362812763@T1` | -0.85117 |
| `explicit.stat_3261801346@T1` | -0.82028 |
| `explicit.stat_2451402625@T2` | -0.80861 |
| `explicit.stat_3362812763@T2` | -0.80855 |
| `explicit.stat_3261801346@T2` | -0.80305 |
| `explicit.stat_4052037485@T2` | -0.79590 |
| `explicit.stat_3321629045@T2` | -0.79258 |
| `explicit.stat_3325883026@T1` | -0.79238 |
| `explicit.stat_1062208444@T2` | -0.78450 |

### armour.gloves — n=3403, R²=-0.1533

intercept: `2.3608`  ·  log_price: True  ·  ilvl: `-0.00148`  ·  n_mods: `-0.00384`  ·  n_top_tier: `0.15431`  ·  corrupted: `-0.05519`  ·  n_sockets: `-0.04684`  ·  quality: `0.00157`

| stat_id | coef |
|---|---|
| `explicit.stat_3033371881@T2` | 1.70760 |
| `explicit.stat_4067062424@T2` | 1.55607 |
| `explicit.stat_4080418644@T1` | -1.46204 |
| `explicit.stat_4015621042@T1` | 1.24396 |
| `explicit.stat_1062208444@T1` | -1.16880 |
| `explicit.stat_1062208444@T2` | 1.13079 |
| `explicit.stat_3484657501@T2` | -1.03879 |
| `explicit.stat_4052037485@T2` | 0.97074 |
| `explicit.stat_2923486259@T1` | -0.67281 |
| `explicit.stat_3372524247@T1` | 0.66311 |
| `explicit.stat_2451402625@T1` | 0.65575 |
| `explicit.stat_2923486259@T2` | 0.63478 |

### accessory.amulet — n=3197, R²=-2.1789

intercept: `5.4736`  ·  log_price: True  ·  ilvl: `-0.05662`  ·  n_mods: `-0.34236`  ·  n_top_tier: `0.96472`  ·  corrupted: `-0.33291`  ·  n_sockets: `0.00884`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -4.62532 |
| `explicit.stat_9187492@T2` | -3.38645 |
| `explicit.stat_2923486259@T2` | -3.35115 |
| `explicit.stat_1202301673@T2` | 3.16211 |
| `explicit.stat_1444556985@T1` | 2.28864 |
| `explicit.stat_2482852589@T1` | -1.97814 |
| `explicit.stat_2482852589@T2` | -1.93324 |
| `explicit.stat_328541901@T1` | -1.90335 |
| `explicit.stat_3981240776@T1` | 1.76277 |
| `explicit.stat_2106365538@T1` | -1.73658 |
| `explicit.stat_2106365538@T2` | -1.66935 |
| `explicit.stat_1671376347@T2` | -1.60359 |

### accessory.ring — n=3042, R²=-2.2946

intercept: `6.9930`  ·  log_price: True  ·  ilvl: `-0.05480`  ·  n_mods: `-0.38758`  ·  n_top_tier: `0.34205`  ·  corrupted: `1.15491`  ·  n_sockets: `4.56806`  ·  quality: `0.00254`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -2.73442 |
| `explicit.stat_2557965901@T1` | -2.27651 |
| `explicit.stat_4067062424@T1` | -2.26001 |
| `explicit.stat_2557965901@T2` | -2.13181 |
| `explicit.stat_4220027924@T1` | 2.02330 |
| `explicit.stat_707457662@T1` | 1.83666 |
| `explicit.stat_2923486259@T2` | -1.75415 |
| `explicit.stat_1263695895@T2` | -1.60369 |
| `explicit.stat_1263695895@T1` | -1.43630 |
| `explicit.stat_707457662@T2` | 1.11794 |
| `explicit.stat_3372524247@T2` | -1.10243 |
| `explicit.stat_1368271171@T1` | -1.10243 |

### weapon.wand — n=2930, R²=-1.4458

intercept: `3.1924`  ·  log_price: True  ·  ilvl: `-0.03992`  ·  n_mods: `-0.01751`  ·  n_top_tier: `0.14242`  ·  corrupted: `0.07849`  ·  n_sockets: `0.00153`  ·  quality: `0.09168`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.23060 |
| `explicit.stat_1545858329@T1` | 2.21786 |
| `explicit.stat_736967255@T2` | 2.07540 |
| `explicit.stat_1600707273@T1` | 2.06966 |
| `explicit.stat_2974417149@T1` | 2.03212 |
| `crafted.stat_124131830` | 1.40493 |
| `explicit.stat_4226189338@T1` | 1.24715 |
| `explicit.stat_2968503605@T1` | 1.03853 |
| `explicit.stat_124131830@T1` | 0.73857 |
| `explicit.stat_2254480358@T2` | -0.54338 |
| `rune.stat_124131830` | 0.27593 |
| `explicit.stat_1263695895@T1` | 0.22612 |

### weapon.bow — n=2539, R²=-1.2638

intercept: `3.3066`  ·  log_price: True  ·  ilvl: `-0.04109`  ·  n_mods: `-0.01892`  ·  n_top_tier: `0.43938`  ·  corrupted: `0.30749`  ·  n_sockets: `0.01784`  ·  quality: `-0.00586`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -8.20766 |
| `desecrated.stat_1200678966@T1` | -8.17926 |
| `rune.stat_3885405204` | -3.49939 |
| `explicit.stat_2463230181@T1` | 1.84930 |
| `explicit.stat_1202301673@T1` | 1.82685 |
| `crafted.stat_3035140377` | 0.90002 |
| `desecrated.stat_210067635@T1` | 0.84374 |
| `explicit.stat_821021828@T1` | -0.64590 |
| `desecrated.stat_666077204` | 0.57000 |
| `explicit.stat_821021828@T2` | -0.54705 |
| `explicit.stat_1940865751@T1` | -0.50027 |
| `explicit.stat_691932474@T2` | -0.48958 |

### weapon.crossbow — n=2430, R²=-1.2312

intercept: `3.9068`  ·  log_price: True  ·  ilvl: `-0.04949`  ·  n_mods: `0.00481`  ·  n_top_tier: `0.71718`  ·  corrupted: `0.09189`  ·  n_sockets: `0.13753`  ·  quality: `-0.07000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 4.48208 |
| `explicit.stat_709508406@T1` | 3.28754 |
| `explicit.stat_691932474@T1` | -2.02111 |
| `explicit.stat_3336890334@T1` | 1.46700 |
| `explicit.stat_1037193709@T2` | 1.18484 |
| `explicit.stat_1263695895@T2` | -1.01549 |
| `explicit.stat_3695891184@T2` | -0.78969 |
| `explicit.stat_1202301673@T2` | -0.78375 |
| `explicit.stat_669069897@T2` | -0.77549 |
| `explicit.stat_518292764@T2` | -0.77529 |
| `explicit.stat_3261801346@T1` | -0.77009 |
| `explicit.stat_4080418644@T1` | -0.76635 |

### jewel — n=1523, R²=-0.5162

intercept: `-1.8027`  ·  log_price: True  ·  ilvl: `0.04281`  ·  n_mods: `-0.03160`  ·  n_top_tier: `-0.31793`  ·  corrupted: `0.72133`

| stat_id | coef |
|---|---|
| `explicit.stat_2011656677@T1` | 9.02947 |
| `explicit.stat_1594812856@T1` | 7.75295 |
| `explicit.stat_3485067555@T1` | 6.88435 |
| `explicit.stat_3851254963@T1` | 6.84167 |
| `explicit.stat_274716455@T1` | -6.45643 |
| `explicit.stat_1405298142@T1` | -6.34755 |
| `explicit.stat_293638271@T1` | -6.19963 |
| `explicit.stat_318953428@T1` | 6.02354 |
| `explicit.stat_1854213750@T1` | 5.79406 |
| `explicit.stat_2637470878@T1` | -5.61484 |
| `explicit.stat_1569101201@T1` | 5.60616 |
| `explicit.stat_2301718443@T1` | -4.90170 |

### weapon.sceptre — n=872, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

### weapon.spear — n=796, R²=0.0

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

### armour.focus — n=727, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

### armour.shield — n=596, R²=0.0

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

### weapon.warstaff — n=469, R²=-0.0103

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2694482655@T1` | 0.00001 |
| `explicit.stat_3336890334@T1` | 0.00001 |
| `explicit.stat_1940865751@T2` | 0.00001 |
| `explicit.stat_387439868@T2` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1940865751@T1` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_387439868@T1` | 0.00000 |
| `explicit.stat_9187492@T2` | 0.00000 |
| `explicit.stat_3695891184@T1` | 0.00000 |
| `explicit.stat_821021828@T1` | -0.00000 |
| `explicit.stat_3336890334@T2` | 0.00000 |

### weapon.staff — n=448, R²=0.0

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

### armour.quiver — n=447, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`

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

### flask.charm — n=408, R²=-0.5459

intercept: `0.0298`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00004`  ·  n_top_tier: `-0.00002`  ·  corrupted: `-0.30380`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.58168 |
| `explicit.stat_280890192` | -0.22389 |
| `explicit.stat_2541588185@T2` | 0.20141 |
| `implicit.stat_2016937536` | 0.19428 |
| `explicit.stat_1873752457@T1` | 0.15843 |
| `explicit.stat_3849649145` | -0.11622 |
| `explicit.stat_828533480@T2` | -0.06105 |
| `implicit.stat_1691862754` | -0.02970 |
| `implicit.stat_1810482573` | -0.02969 |
| `implicit.stat_4010341289` | -0.02968 |
| `implicit.stat_585126960` | -0.02968 |
| `implicit.stat_2778646494` | -0.02968 |

### weapon.twomace — n=324, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

- … **Utility Belt** — 1180 listings (1180 priced) [0.3–737.3 ex]
- … **Dueling Wand** — 929 listings (929 priced) [1.0–727.0 ex]
- … **Emerald** — 847 listings (847 priced) [0.4–727.0 ex]
- … **Sapphire** — 756 listings (756 priced) [0.4–727.0 ex]
- … **Stellar Amulet** — 750 listings (750 priced) [0.3–737.3 ex]
- … **Obliterator Bow** — 742 listings (742 priced) [0.5–727.0 ex]
- … **Ruby** — 662 listings (662 priced) [0.3–727.0 ex]
- … **Solar Amulet** — 575 listings (575 priced) [1.0–737.3 ex]
- … **Gold Amulet** — 572 listings (572 priced) [0.3–737.3 ex]
- … **Ancestral Tiara** — 533 listings (533 priced) [1.0–737.3 ex]
- … **Warmonger Bow** — 533 listings (533 priced) [0.9–727.0 ex]
- … **Siphoning Wand** — 527 listings (527 priced) [1.0–727.0 ex]
- … **Plate Belt** — 522 listings (522 priced) [1.0–737.3 ex]
- … **Galvanic Wand** — 521 listings (521 priced) [1.0–727.0 ex]
- … **Heavy Belt** — 510 listings (510 priced) [0.5–737.3 ex]
- … **Prismatic Ring** — 500 listings (500 priced) [0.3–737.3 ex]
- … **Amethyst Ring** — 484 listings (484 priced) [1.0–737.3 ex]
- … **Attuned Wand** — 484 listings (484 priced) [0.3–727.0 ex]
- … **Withered Wand** — 459 listings (459 priced) [1.0–727.0 ex]
- … **Gold Ring** — 454 listings (454 priced) [0.7–737.3 ex]
- … **Trarthan Cannon** — 437 listings (437 priced) [0.7–727.0 ex]
- … **Long Belt** — 424 listings (424 priced) [1.0–737.3 ex]
- … **Sapphire Ring** — 418 listings (418 priced) [0.5–737.3 ex]
- … **Topaz Ring** — 418 listings (418 priced) [1.0–737.3 ex]
- … **Lapis Amulet** — 411 listings (411 priced) [0.6–737.3 ex]

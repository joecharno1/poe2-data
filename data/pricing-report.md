# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-03T16:25:42+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **55737** (55737 priced in exalted)
- Distinct bases: 782 · distinct mods: 1660 · mod rows: 279013
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-03T16:11:16+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×6.26** (median |log error| 1.8344)
- Within ±30% of asking price: **27%**
- Skill vs constant-price guess: **+0.02** (> 0 = the mods carry signal)
- Calibration: 66% of actuals above prediction (target ≈ 75%)

| group | n_test | ×err | ±30% | skill |
|---|---|---|---|---|
| accessory.belt | 868 | ×9.90 | 20% | -0.02 |
| armour.chest | 856 | ×7.37 | 16% | +0.02 |
| armour.boots | 851 | ×8.16 | 18% | -0.01 |
| armour.gloves | 840 | ×8.97 | 15% | -0.06 |
| armour.helmet | 835 | ×7.02 | 14% | +0.01 |
| accessory.ring | 754 | ×5.22 | 3% | -0.07 |
| accessory.amulet | 718 | ×8.05 | 6% | -0.18 |
| weapon.wand | 693 | ×9.12 | 32% | +0.04 |
| weapon.bow | 638 | ×7.21 | 37% | +0.08 |
| other | 634 | ×7.15 | 37% | +0.47 |
| weapon.crossbow | 541 | ×8.13 | 28% | +0.01 |
| jewel | 426 | ×7.42 | 7% | -0.10 |
| weapon.sceptre | 185 | ×1.00 | 98% | +0.00 |
| weapon.spear | 171 | ×1.00 | 99% | +0.00 |
| armour.focus | 155 | ×1.00 | 100% | n/a |
| armour.shield | 143 | ×1.00 | 99% | +0.00 |
| armour.quiver | 106 | ×1.00 | 98% | +0.00 |
| weapon.twomace | 84 | ×1.00 | 96% | +0.00 |
| weapon.staff | 67 | ×1.00 | 100% | n/a |
| weapon.warstaff | 65 | ×1.00 | 100% | n/a |
| flask.charm | 40 | ×1.34 | 38% | -0.05 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=5469, R²=0.0887

intercept: `1.7044`  ·  log_price: True  ·  ilvl: `0.00408`  ·  n_mods: `0.03360`  ·  n_top_tier: `0.10022`  ·  corrupted: `0.26147`  ·  n_sockets: `-0.14323`  ·  quality: `-0.01790`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.96723 |
| `explicit.stat_124131830` | -0.88927 |
| `explicit.stat_124131830@T2` | 0.67227 |
| `implicit.stat_718638445` | 0.52137 |
| `implicit.stat_3182714256` | 0.51843 |
| `explicit.stat_4080418644@T1` | -0.48391 |
| `explicit.stat_4080418644@T2` | -0.37388 |
| `implicit.stat_1379411836` | -0.30969 |
| `explicit.stat_1263695895@T1` | -0.30016 |
| `implicit.stat_958696139` | -0.25847 |
| `explicit.stat_1671376347@T1` | -0.22835 |
| `explicit.stat_4052037485@T1` | -0.21123 |

### accessory.belt — n=4238, R²=-1.0608

intercept: `4.3782`  ·  log_price: True  ·  ilvl: `-0.05596`  ·  n_mods: `-0.01461`  ·  n_top_tier: `-0.05284`  ·  corrupted: `0.09285`  ·  n_sockets: `-0.02390`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 2.35977 |
| `explicit.stat_4220027924@T1` | 2.08024 |
| `explicit.stat_1836676211@T1` | 1.42803 |
| `implicit.stat_731781020` | 0.89231 |
| `explicit.stat_3299347043@T1` | -0.51324 |
| `explicit.stat_3299347043@T2` | -0.45557 |
| `explicit.stat_2923486259@T1` | 0.43579 |
| `explicit.stat_3372524247@T1` | 0.34793 |
| `explicit.stat_2881298780@T2` | 0.22064 |
| `explicit.stat_1412217137@T2` | 0.20636 |
| `explicit.stat_4220027924@T2` | 0.17446 |
| `explicit.stat_2881298780@T1` | 0.17064 |

### armour.chest — n=4097, R²=-1.153

intercept: `3.6760`  ·  log_price: True  ·  ilvl: `-0.04653`  ·  n_mods: `-0.01351`  ·  n_top_tier: `0.31510`  ·  corrupted: `0.46601`  ·  n_sockets: `0.03290`  ·  quality: `0.01599`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 4.87774 |
| `explicit.stat_3981240776@T1` | 1.49688 |
| `explicit.stat_2339757871@T1` | -0.96156 |
| `explicit.stat_4015621042@T1` | 0.72625 |
| `explicit.stat_3372524247@T1` | 0.71658 |
| `explicit.stat_4052037485@T1` | -0.68613 |
| `explicit.stat_3362812763@T1` | -0.57722 |
| `explicit.stat_915769802@T1` | -0.56319 |
| `explicit.stat_4015621042@T2` | -0.52536 |
| `explicit.stat_1671376347@T1` | 0.51909 |
| `explicit.stat_915769802@T2` | -0.49451 |
| `explicit.stat_3325883026@T2` | -0.44573 |

### armour.helmet — n=4079, R²=-1.0527

intercept: `3.9644`  ·  log_price: True  ·  ilvl: `-0.05125`  ·  n_mods: `-0.02460`  ·  n_top_tier: `0.58002`  ·  corrupted: `-0.30158`  ·  n_sockets: `0.03888`  ·  quality: `0.05050`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | -2.51600 |
| `explicit.stat_3033371881@T1` | -1.16515 |
| `explicit.stat_3033371881@T2` | -1.08749 |
| `explicit.stat_2162097452@T2` | -0.90622 |
| `explicit.stat_3917489142@T2` | -0.88012 |
| `explicit.stat_3325883026@T1` | -0.84050 |
| `explicit.stat_3917489142@T1` | -0.83135 |
| `explicit.stat_2923486259@T1` | -0.81258 |
| `explicit.stat_3639275092@T1` | -0.80555 |
| `explicit.stat_3325883026@T2` | -0.80072 |
| `explicit.stat_4052037485@T1` | -0.79472 |
| `explicit.stat_124859000@T1` | -0.79376 |

### armour.boots — n=4041, R²=-0.8903

intercept: `3.7626`  ·  log_price: True  ·  ilvl: `-0.04744`  ·  n_mods: `-0.04534`  ·  n_top_tier: `0.64228`  ·  corrupted: `0.49875`  ·  n_sockets: `0.09299`  ·  quality: `0.02803`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.54974 |
| `explicit.stat_2923486259@T1` | 0.95680 |
| `explicit.stat_2923486259@T2` | -0.83943 |
| `explicit.stat_2339757871@T1` | -0.82156 |
| `explicit.stat_3321629045@T2` | -0.80168 |
| `explicit.stat_3033371881@T2` | -0.79729 |
| `explicit.stat_3321629045@T1` | -0.78203 |
| `explicit.stat_1062208444@T1` | -0.77742 |
| `explicit.stat_3639275092@T1` | -0.76247 |
| `explicit.stat_328541901@T1` | -0.74844 |
| `explicit.stat_1874553720@T1` | -0.72453 |
| `explicit.stat_1062208444@T2` | -0.72178 |

### armour.gloves — n=3910, R²=-1.1208

intercept: `3.7506`  ·  log_price: True  ·  ilvl: `-0.04834`  ·  n_mods: `-0.00144`  ·  n_top_tier: `0.37038`  ·  corrupted: `-0.28364`  ·  n_sockets: `0.15927`  ·  quality: `0.01242`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.36039 |
| `explicit.stat_3372524247@T1` | 1.44440 |
| `explicit.stat_2451402625@T1` | 1.16763 |
| `explicit.stat_3556824919@T1` | 1.15921 |
| `explicit.stat_1671376347@T1` | 0.96812 |
| `explicit.stat_1573130764@T2` | 0.87619 |
| `explicit.stat_3362812763@T2` | 0.62109 |
| `explicit.stat_2557965901@T2` | -0.61511 |
| `explicit.stat_53045048@T1` | -0.57848 |
| `explicit.stat_4015621042@T1` | -0.55696 |
| `explicit.stat_2557965901@T1` | -0.55147 |
| `explicit.stat_3033371881@T2` | -0.53448 |

### accessory.amulet — n=3688, R²=-1.8366

intercept: `5.8298`  ·  log_price: True  ·  ilvl: `-0.04429`  ·  n_mods: `-0.49390`  ·  n_top_tier: `0.68244`  ·  corrupted: `1.44385`  ·  n_sockets: `-1.28413`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -3.17201 |
| `explicit.stat_2923486259@T2` | -2.46732 |
| `explicit.stat_2748665614@T1` | -2.13762 |
| `explicit.stat_3299347043@T1` | -1.85017 |
| `explicit.stat_803737631@T1` | -1.80775 |
| `explicit.stat_2748665614@T2` | -1.69859 |
| `explicit.stat_1202301673@T2` | 1.66441 |
| `explicit.stat_4080418644@T1` | -1.61587 |
| `explicit.stat_2901986750@T2` | -1.58745 |
| `explicit.stat_328541901@T1` | -1.48560 |
| `explicit.stat_1050105434@T2` | -1.47784 |
| `explicit.stat_9187492@T2` | -1.39672 |

### accessory.ring — n=3559, R²=-2.3606

intercept: `4.2499`  ·  log_price: True  ·  ilvl: `-0.04130`  ·  n_mods: `-0.16138`  ·  n_top_tier: `0.38357`  ·  corrupted: `0.58018`  ·  n_sockets: `5.30996`  ·  quality: `0.00006`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T2` | -2.66942 |
| `explicit.stat_3299347043@T1` | -2.59147 |
| `explicit.stat_707457662@T1` | 1.73805 |
| `explicit.stat_1263695895@T1` | -1.49097 |
| `explicit.stat_3695891184@T1` | -1.47487 |
| `explicit.stat_1573130764@T1` | -1.45230 |
| `explicit.stat_3962278098@T2` | -1.26638 |
| `implicit.stat_958696139` | 1.11945 |
| `explicit.stat_2923486259@T2` | -1.11588 |
| `explicit.stat_4067062424@T1` | -1.06739 |
| `explicit.stat_3032590688@T1` | -1.05228 |
| `explicit.stat_1573130764@T2` | -0.98669 |

### weapon.wand — n=3358, R²=-1.4298

intercept: `2.9841`  ·  log_price: True  ·  ilvl: `-0.03730`  ·  n_mods: `-0.00969`  ·  n_top_tier: `0.14189`  ·  corrupted: `0.09265`  ·  n_sockets: `-0.00040`  ·  quality: `0.01467`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.25060 |
| `explicit.stat_1600707273@T1` | 2.16598 |
| `explicit.stat_4226189338@T1` | 2.14181 |
| `explicit.stat_1545858329@T1` | 2.14112 |
| `explicit.stat_736967255@T2` | 2.06556 |
| `explicit.stat_2974417149@T1` | 2.02295 |
| `explicit.stat_124131830@T1` | 1.94987 |
| `explicit.stat_2968503605@T1` | 1.93646 |
| `crafted.stat_124131830` | 1.24207 |
| `explicit.stat_2231156303@T2` | 0.84407 |
| `rune.stat_3278136794` | -0.49552 |
| `explicit.stat_2254480358@T2` | -0.30178 |

### weapon.bow — n=2955, R²=-1.2922

intercept: `3.2586`  ·  log_price: True  ·  ilvl: `-0.04054`  ·  n_mods: `-0.02254`  ·  n_top_tier: `0.60646`  ·  corrupted: `0.34663`  ·  n_sockets: `0.01202`  ·  quality: `-0.00741`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | 1.64800 |
| `explicit.stat_1202301673@T1` | 1.62784 |
| `explicit.stat_1509134228@T1` | 1.61950 |
| `desecrated.stat_666077204@T1` | -1.50677 |
| `rune.stat_3885405204` | -1.35333 |
| `desecrated.stat_210067635@T1` | 1.21775 |
| `explicit.stat_821021828@T1` | -1.01241 |
| `explicit.stat_821021828@T2` | -0.92173 |
| `crafted.stat_3035140377` | 0.80746 |
| `explicit.stat_1940865751@T1` | -0.69122 |
| `explicit.stat_3336890334@T2` | -0.66560 |
| `explicit.stat_3639275092@T2` | -0.66333 |

### weapon.crossbow — n=2827, R²=-1.2685

intercept: `3.5390`  ·  log_price: True  ·  ilvl: `-0.04465`  ·  n_mods: `0.00947`  ·  n_top_tier: `0.50383`  ·  corrupted: `0.05161`  ·  n_sockets: `0.05204`  ·  quality: `-0.05711`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 4.82754 |
| `explicit.stat_3336890334@T1` | 1.71457 |
| `explicit.stat_691932474@T1` | -1.61058 |
| `explicit.stat_709508406@T1` | 1.25053 |
| `desecrated.stat_3131442032@T1` | -0.93990 |
| `desecrated.stat_1365232741@T1` | -0.93990 |
| `explicit.stat_1263695895@T1` | 0.78163 |
| `crafted.stat_3035140377` | 0.71756 |
| `explicit.stat_1967051901@T2` | 0.69793 |
| `explicit.stat_1263695895@T2` | -0.66276 |
| `explicit.stat_1037193709@T2` | 0.65195 |
| `explicit.stat_1509134228@T2` | -0.59815 |

### jewel — n=2151, R²=-0.572

intercept: `-1.5730`  ·  log_price: True  ·  ilvl: `0.03770`  ·  n_mods: `0.04953`  ·  n_top_tier: `-0.35425`  ·  corrupted: `0.73533`

| stat_id | coef |
|---|---|
| `explicit.stat_21071013@T1` | 7.11753 |
| `explicit.stat_924253255@T1` | 6.67425 |
| `explicit.stat_1569101201@T1` | 6.24427 |
| `explicit.stat_3473929743@T1` | 5.87607 |
| `explicit.stat_1459321413@T1` | 5.50678 |
| `explicit.stat_2456523742@T1` | 5.27209 |
| `explicit.stat_2011656677@T1` | 5.24976 |
| `explicit.stat_1310194496@T1` | 5.15373 |
| `explicit.stat_2301718443@T1` | -5.07042 |
| `explicit.stat_3851254963@T1` | 4.99263 |
| `explicit.stat_293638271@T1` | -4.92373 |
| `explicit.stat_1569159338@T1` | 4.64870 |

### weapon.sceptre — n=936, R²=0.0

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

### weapon.spear — n=861, R²=0.0

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

### armour.focus — n=783, R²=0.0

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

### armour.shield — n=656, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1568848828` | 0.00000 |
| `explicit.stat_1011760251` | 0.00000 |
| `explicit.stat_1011760251@T1` | -0.00000 |
| `explicit.stat_1011760251@T2` | -0.00000 |
| `explicit.stat_1062208444` | 0.00000 |
| `explicit.stat_1062208444@T1` | 0.00000 |
| `explicit.stat_1062208444@T2` | 0.00000 |
| `explicit.stat_1301765461` | 0.00000 |
| `explicit.stat_1301765461@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |

### weapon.warstaff — n=588, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_210067635` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |

### weapon.staff — n=560, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1545858329` | 0.00000 |
| `explicit.stat_1545858329@T1` | 0.00000 |

### armour.quiver — n=541, R²=0.0

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

### flask.charm — n=486, R²=-0.5968

intercept: `0.0373`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00009`  ·  n_top_tier: `-0.00006`  ·  corrupted: `-0.29247`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.90991 |
| `explicit.stat_3849649145` | -0.18182 |
| `explicit.stat_1873752457@T2` | -0.18181 |
| `explicit.stat_280890192` | -0.17472 |
| `explicit.stat_828533480@T2` | -0.17462 |
| `implicit.stat_2016937536` | 0.13768 |
| `implicit.stat_1412682799` | 0.13750 |
| `explicit.stat_2541588185@T2` | 0.12982 |
| `explicit.stat_1873752457@T1` | 0.06512 |
| `implicit.stat_4010341289` | -0.03717 |
| `implicit.stat_3699444296` | -0.03717 |
| `implicit.stat_2778646494` | -0.03716 |

### weapon.twomace — n=402, R²=0.0

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

- … **Utility Belt** — 1335 listings (1335 priced) [0.3–802.8 ex]
- … **Emerald** — 1152 listings (1152 priced) [0.4–802.8 ex]
- … **Sapphire** — 1053 listings (1053 priced) [0.4–802.8 ex]
- … **Dueling Wand** — 1043 listings (1043 priced) [1.0–802.8 ex]
- … **Stellar Amulet** — 913 listings (913 priced) [0.3–802.8 ex]
- … **Ruby** — 895 listings (895 priced) [0.3–802.8 ex]
- … **Obliterator Bow** — 859 listings (859 priced) [0.5–802.8 ex]
- … **Solar Amulet** — 671 listings (671 priced) [1.0–802.8 ex]
- … **Gold Amulet** — 665 listings (665 priced) [0.3–802.8 ex]
- … **Warmonger Bow** — 615 listings (615 priced) [0.9–802.8 ex]
- … **Plate Belt** — 612 listings (612 priced) [1.0–802.8 ex]
- … **Siphoning Wand** — 611 listings (611 priced) [1.0–802.8 ex]
- … **Prismatic Ring** — 604 listings (604 priced) [0.3–802.8 ex]
- … **Galvanic Wand** — 603 listings (603 priced) [1.0–802.8 ex]
- … **Ancestral Tiara** — 596 listings (596 priced) [1.0–802.8 ex]
- … **Heavy Belt** — 588 listings (588 priced) [0.5–802.8 ex]
- … **Amethyst Ring** — 571 listings (571 priced) [1.0–802.8 ex]
- … **Attuned Wand** — 560 listings (560 priced) [0.3–802.8 ex]
- … **Gold Ring** — 531 listings (531 priced) [0.7–802.8 ex]
- … **Withered Wand** — 520 listings (520 priced) [1.0–802.8 ex]
- … **Trarthan Cannon** — 516 listings (516 priced) [0.7–802.8 ex]
- … **Sapphire Ring** — 502 listings (502 priced) [0.5–802.8 ex]
- … **Topaz Ring** — 502 listings (502 priced) [1.0–802.8 ex]
- … **Long Belt** — 488 listings (488 priced) [1.0–802.8 ex]
- … **Lapis Amulet** — 477 listings (477 priced) [0.6–802.8 ex]

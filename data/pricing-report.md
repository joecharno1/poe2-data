# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-21T07:15:28+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **704031** (701796 priced in exalted)
- Distinct bases: 1001 · distinct mods: 3317 · mod rows: 3330925
- Sold signals: **24237** sold · 400736 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-21T07:01:56+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×21.50** (median |log error| 3.0679)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×64.28 · ±30% 7% · n=102362
- Premium segment (60ex+): skill **+0.12** · typical error ×294.15 · ±30% 0% · n=67972

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 15059 | ×41.46 | 21% | +0.04 | +0.06 |
| jewel | 14391 | ×55.85 | 21% | +0.02 | +0.03 |
| accessory.amulet | 13537 | ×16.16 | 23% | +0.01 | +0.01 |
| accessory.belt | 9669 | ×19.98 | 24% | +0.02 | +0.04 |
| armour.chest | 9368 | ×15.98 | 22% | +0.08 | +0.10 |
| armour.helmet | 9070 | ×26.24 | 19% | +0.08 | +0.11 |
| armour.boots | 8440 | ×21.62 | 20% | +0.10 | +0.13 |
| armour.gloves | 8298 | ×34.59 | 15% | +0.08 | +0.10 |
| other | 8224 | ×2.00 | 41% | +0.11 | +0.18 |
| weapon.wand | 4929 | ×38.03 | 15% | +0.11 | +0.11 |
| weapon.bow | 3865 | ×27.77 | 12% | +0.15 | +0.16 |
| weapon.crossbow | 3652 | ×25.24 | 15% | +0.11 | +0.15 |
| weapon.warstaff | 2509 | ×14.01 | 7% | +0.21 | +0.21 |
| weapon.staff | 2428 | ×15.71 | 6% | +0.13 | +0.13 |
| weapon.sceptre | 2382 | ×18.81 | 4% | +0.08 | +0.09 |
| weapon.spear | 1909 | ×12.95 | 7% | +0.15 | +0.15 |
| armour.focus | 1577 | ×12.65 | 7% | +0.12 | +0.13 |
| armour.quiver | 1473 | ×17.76 | 6% | +0.12 | +0.14 |
| flask.charm | 1210 | ×11.91 | 27% | -0.00 | +0.01 |
| armour.shield | 1203 | ×8.97 | 8% | +0.10 | +0.12 |
| weapon.twomace | 1114 | ×9.28 | 8% | +0.10 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=78993, R²=-1.908

intercept: `-0.0631`  ·  log_price: True  ·  ilvl: `0.00078`  ·  n_mods: `1.02337`  ·  n_top_tier: `-0.92233`  ·  corrupted: `0.92238`  ·  quality: `0.24857`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 3.45757 |
| `explicit.stat_1604736568@T1` | -2.34393 |
| `explicit.stat_1604736568` | 2.25231 |
| `explicit.stat_3174700878@T1` | 1.09736 |
| `explicit.stat_274716455@T1` | -0.97167 |
| `explicit.stat_587431675@T1` | -0.95789 |
| `explicit.stat_2194114101@T1` | -0.90954 |
| `explicit.stat_2456523742@T1` | 0.78764 |
| `explicit.stat_3473929743@T1` | -0.71967 |
| `explicit.stat_3556824919@T1` | 0.67405 |
| `explicit.stat_3714003708@T1` | 0.61796 |
| `explicit.stat_681332047@T1` | -0.60894 |

### accessory.ring — n=68613, R²=-2.0186

intercept: `3.4540`  ·  log_price: True  ·  ilvl: `-0.04312`  ·  n_mods: `0.00140`  ·  n_top_tier: `0.92520`  ·  corrupted: `0.00945`  ·  n_sockets: `2.10185`  ·  quality: `0.02076`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -0.96952 |
| `explicit.stat_4080418644@T1` | -0.95002 |
| `explicit.stat_803737631@T1` | -0.94705 |
| `explicit.stat_2231156303@T1` | -0.94519 |
| `explicit.stat_2891184298@T2` | -0.94496 |
| `explicit.stat_3325883026@T1` | -0.94333 |
| `explicit.stat_4220027924@T2` | -0.94130 |
| `explicit.stat_3291658075@T2` | -0.94065 |
| `explicit.stat_2923486259@T2` | -0.93815 |
| `explicit.stat_3261801346@T1` | -0.93582 |
| `explicit.stat_2891184298@T1` | -0.93563 |
| `explicit.stat_1263695895@T2` | -0.93387 |

### other — n=67028, R²=-0.6517

intercept: `1.6093`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.10277`  ·  n_top_tier: `0.24381`  ·  corrupted: `0.00855`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.33247 |
| `implicit.stat_718638445` | 0.30834 |
| `implicit.stat_3182714256` | 0.30833 |
| `implicit.stat_2219129443` | 0.21997 |
| `explicit.stat_3299347043@T1` | -0.20951 |
| `explicit.stat_2974417149@T1` | 0.15328 |
| `explicit.stat_3917489142@T1` | -0.12404 |
| `implicit.stat_958696139` | -0.10275 |
| `implicit.stat_3879011313` | 0.06880 |
| `implicit.stat_1416292992` | -0.06851 |
| `explicit.stat_789117908@T1` | -0.06340 |
| `implicit.stat_3032590688` | -0.04109 |

### accessory.amulet — n=61616, R²=-0.4844

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `1.09904`  ·  corrupted: `-0.00000`  ·  n_sockets: `1.79126`  ·  quality: `0.04169`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | -1.31360 |
| `explicit.stat_124131830@T2` | -1.26296 |
| `explicit.stat_2162097452@T2` | -1.13665 |
| `explicit.stat_803737631@T1` | -1.09907 |
| `explicit.stat_3299347043@T2` | -1.09906 |
| `explicit.stat_803737631@T2` | -1.09906 |
| `explicit.stat_789117908@T1` | -1.09906 |
| `explicit.stat_983749596@T2` | -1.09906 |
| `explicit.stat_789117908@T2` | -1.09906 |
| `explicit.stat_4080418644@T2` | -1.09905 |
| `explicit.stat_2891184298@T1` | -1.09905 |
| `explicit.stat_4220027924@T2` | -1.09905 |

### accessory.belt — n=44236, R²=-2.1055

intercept: `0.2503`  ·  log_price: True  ·  ilvl: `-0.00302`  ·  n_mods: `-0.00130`  ·  n_top_tier: `0.56020`  ·  corrupted: `0.87882`  ·  n_sockets: `1.60216`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -0.56243 |
| `explicit.stat_3299347043@T2` | -0.56173 |
| `explicit.stat_915769802@T1` | -0.56164 |
| `explicit.stat_51994685@T1` | -0.56152 |
| `explicit.stat_809229260@T2` | -0.56150 |
| `explicit.stat_3325883026@T1` | -0.56130 |
| `explicit.stat_2881298780@T1` | -0.56091 |
| `explicit.stat_3372524247@T2` | -0.56068 |
| `explicit.stat_4220027924@T2` | -0.56066 |
| `explicit.stat_1570770415@T2` | -0.56064 |
| `explicit.stat_1389754388@T1` | -0.56032 |
| `explicit.stat_915769802@T2` | -0.56016 |

### armour.chest — n=43902, R²=-1.789

intercept: `3.2443`  ·  log_price: True  ·  ilvl: `-0.04011`  ·  n_mods: `-0.01275`  ·  n_top_tier: `0.34827`  ·  corrupted: `0.29741`  ·  n_sockets: `0.01746`  ·  quality: `0.07406`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.68782 |
| `explicit.stat_986397080@T2` | -0.42555 |
| `explicit.stat_986397080@T1` | -0.41202 |
| `explicit.stat_1692879867@T2` | -0.38171 |
| `explicit.stat_915769802@T2` | -0.37783 |
| `explicit.stat_3484657501@T1` | -0.37430 |
| `explicit.stat_4080418644@T2` | -0.37344 |
| `explicit.stat_4080418644@T1` | -0.37008 |
| `explicit.stat_915769802@T1` | -0.36976 |
| `explicit.stat_3301100256@T2` | -0.36963 |
| `explicit.stat_2339757871@T2` | -0.36222 |
| `explicit.stat_2451402625@T2` | -0.36128 |

### armour.helmet — n=42663, R²=-1.7791

intercept: `3.2275`  ·  log_price: True  ·  ilvl: `-0.04095`  ·  n_mods: `-0.01417`  ·  n_top_tier: `0.60417`  ·  corrupted: `0.54331`  ·  n_sockets: `0.04906`  ·  quality: `0.07098`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.41745 |
| `crafted.stat_3917489142@T1` | 0.85533 |
| `explicit.stat_3917489142@T2` | -0.80169 |
| `explicit.stat_1263695895@T1` | -0.78070 |
| `explicit.stat_2162097452@T2` | -0.74315 |
| `explicit.stat_3917489142@T1` | -0.73070 |
| `explicit.stat_4015621042@T2` | -0.66844 |
| `explicit.stat_4052037485@T2` | -0.66537 |
| `explicit.stat_1263695895@T2` | -0.66363 |
| `explicit.stat_1999113824@T1` | -0.65228 |
| `explicit.stat_803737631@T1` | -0.65160 |
| `explicit.stat_53045048@T1` | -0.64544 |

### armour.boots — n=39500, R²=-1.746

intercept: `3.4359`  ·  log_price: True  ·  ilvl: `-0.04242`  ·  n_mods: `-0.01929`  ·  n_top_tier: `0.40933`  ·  corrupted: `0.02333`  ·  n_sockets: `0.05164`  ·  quality: `0.06960`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.81115 |
| `crafted.stat_3917489142@T1` | 1.60540 |
| `explicit.stat_2339757871@T1` | -1.31409 |
| `explicit.stat_2923486259@T1` | 0.78339 |
| `explicit.stat_3299347043@T1` | -0.51876 |
| `explicit.stat_3917489142@T2` | -0.48976 |
| `explicit.stat_2923486259@T2` | -0.47342 |
| `explicit.stat_1671376347@T2` | -0.46126 |
| `explicit.stat_328541901@T2` | -0.45713 |
| `explicit.stat_1999113824@T2` | -0.45509 |
| `explicit.stat_2160282525@T1` | -0.45340 |
| `explicit.stat_1874553720@T1` | -0.45271 |

### armour.gloves — n=38504, R²=-1.732

intercept: `3.8248`  ·  log_price: True  ·  ilvl: `-0.05031`  ·  n_mods: `-0.00031`  ·  n_top_tier: `0.79219`  ·  corrupted: `-0.06889`  ·  n_sockets: `0.17325`  ·  quality: `0.06125`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.28192 |
| `explicit.stat_2923486259@T2` | -1.09188 |
| `explicit.stat_3484657501@T2` | -1.02385 |
| `explicit.stat_4052037485@T2` | -0.99988 |
| `explicit.stat_4052037485@T1` | -0.99534 |
| `explicit.stat_9187492@T2` | -0.96876 |
| `explicit.stat_2923486259@T1` | -0.96132 |
| `explicit.stat_4015621042@T2` | -0.95948 |
| `explicit.stat_3484657501@T1` | -0.92191 |
| `explicit.stat_3321629045@T2` | -0.91941 |
| `explicit.stat_803737631@T2` | -0.91568 |
| `explicit.stat_803737631@T1` | -0.89297 |

### weapon.wand — n=22839, R²=-1.9114

intercept: `4.1763`  ·  log_price: True  ·  ilvl: `-0.05159`  ·  n_mods: `-0.06905`  ·  n_top_tier: `0.43087`  ·  corrupted: `0.01559`  ·  n_sockets: `0.03650`  ·  quality: `0.05023`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -3.97044 |
| `explicit.stat_1545858329@T1` | 2.86295 |
| `explicit.stat_2254480358@T1` | 2.56170 |
| `explicit.stat_124131830@T1` | 2.08329 |
| `explicit.stat_591105508@T1` | 2.01354 |
| `explicit.stat_736967255@T2` | 1.69848 |
| `explicit.stat_4226189338@T1` | 1.57518 |
| `explicit.stat_2254480358@T2` | 1.32640 |
| `crafted.stat_124131830` | 1.19975 |
| `explicit.stat_1263695895@T1` | -0.88167 |
| `explicit.stat_1263695895@T2` | -0.87456 |
| `explicit.stat_4226189338@T2` | 0.83147 |

### flask.charm — n=19679, R²=-0.6519

intercept: `0.1096`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.68057`  ·  corrupted: `1.54426`  ·  quality: `0.00915`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60537 |
| `explicit.stat_1056492907` | 2.65693 |
| `explicit.stat_1120862500@T2` | -1.68060 |
| `explicit.stat_828533480@T2` | -1.68059 |
| `explicit.stat_1873752457@T2` | -1.68057 |
| `explicit.stat_2676834156@T2` | -1.68052 |
| `explicit.stat_3196823591@T2` | -1.68052 |
| `explicit.stat_2365392475@T2` | -1.68051 |
| `explicit.stat_828533480@T1` | -1.67948 |
| `explicit.stat_388617051@T2` | -1.67897 |
| `explicit.stat_2541588185@T2` | -1.67498 |
| `explicit.stat_1873752457@T1` | -1.67118 |

### weapon.bow — n=18198, R²=-1.8026

intercept: `3.9776`  ·  log_price: True  ·  ilvl: `-0.04795`  ·  n_mods: `-0.07183`  ·  n_top_tier: `0.73535`  ·  corrupted: `0.67325`  ·  n_sockets: `0.04385`  ·  quality: `0.03343`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 3.41504 |
| `desecrated.stat_210067635@T1` | -1.74619 |
| `explicit.stat_1263695895@T1` | -1.32231 |
| `explicit.stat_1263695895@T2` | -1.23748 |
| `crafted.stat_3035140377` | 1.18099 |
| `explicit.stat_709508406@T1` | 1.14887 |
| `explicit.stat_1509134228@T1` | -0.97441 |
| `explicit.stat_3336890334@T1` | 0.86568 |
| `explicit.stat_2463230181@T2` | -0.83351 |
| `explicit.stat_3695891184@T1` | -0.82664 |
| `explicit.stat_3695891184@T2` | -0.82227 |
| `explicit.stat_1368271171@T2` | -0.80489 |

### weapon.crossbow — n=17097, R²=-1.7493

intercept: `4.0494`  ·  log_price: True  ·  ilvl: `-0.04936`  ·  n_mods: `-0.06500`  ·  n_top_tier: `0.34500`  ·  corrupted: `0.07071`  ·  n_sockets: `0.05624`  ·  quality: `0.02903`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.73396 |
| `explicit.stat_1202301673@T1` | 1.50907 |
| `explicit.stat_1980802737` | 1.37397 |
| `explicit.stat_2250681686@T2` | -1.33762 |
| `explicit.stat_1509134228@T1` | 1.09836 |
| `explicit.stat_2250681686` | 1.07253 |
| `crafted.stat_3035140377` | 0.82024 |
| `explicit.stat_709508406@T1` | 0.64876 |
| `explicit.stat_1263695895@T2` | -0.64664 |
| `explicit.stat_387439868@T1` | 0.58124 |
| `explicit.stat_3695891184@T1` | -0.54575 |
| `explicit.stat_518292764@T1` | 0.53521 |

### weapon.warstaff — n=11913, R²=-0.3394

intercept: `-10.2508`  ·  log_price: True  ·  ilvl: `0.13767`  ·  n_mods: `-0.21196`  ·  n_top_tier: `0.40119`  ·  corrupted: `0.27441`  ·  n_sockets: `0.13779`  ·  quality: `0.05666`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 1.45692 |
| `desecrated.stat_2527686725@T1` | 1.45692 |
| `crafted.stat_210067635@T2` | 1.10221 |
| `explicit.stat_328541901@T2` | -0.96901 |
| `desecrated.stat_9187492` | 0.80859 |
| `explicit.stat_328541901@T1` | -0.78560 |
| `explicit.stat_821021828@T2` | -0.77037 |
| `rune.stat_243313994` | 0.71580 |
| `explicit.stat_2694482655@T1` | 0.62440 |
| `explicit.stat_691932474@T2` | -0.59678 |
| `explicit.stat_1037193709@T2` | -0.56044 |
| `explicit.stat_1509134228@T1` | 0.50969 |

### weapon.staff — n=11312, R²=-0.3581

intercept: `-15.5472`  ·  log_price: True  ·  ilvl: `0.19774`  ·  n_mods: `-0.06589`  ·  n_top_tier: `0.47301`  ·  corrupted: `0.66986`  ·  n_sockets: `0.15961`  ·  quality: `0.03616`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.15606 |
| `explicit.stat_1600707273@T1` | 1.60909 |
| `explicit.stat_1545858329@T1` | 1.40972 |
| `explicit.stat_124131830@T1` | 1.40567 |
| `explicit.stat_591105508@T1` | 1.32335 |
| `explicit.stat_293638271@T2` | -1.07226 |
| `explicit.stat_3962278098@T2` | 0.90026 |
| `explicit.stat_2254480358@T1` | 0.82794 |
| `rune.stat_124131830` | 0.76827 |
| `explicit.stat_1263695895@T2` | -0.76602 |
| `explicit.stat_473429811@T2` | -0.72912 |
| `explicit.stat_124131830@T2` | 0.62454 |

### weapon.sceptre — n=11088, R²=-0.3443

intercept: `-21.3328`  ·  log_price: True  ·  ilvl: `0.27001`  ·  n_mods: `0.03264`  ·  n_top_tier: `0.08109`  ·  corrupted: `0.25841`  ·  n_sockets: `0.21603`  ·  quality: `0.03041`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.69647 |
| `explicit.stat_2162097452@T2` | 1.41389 |
| `explicit.stat_3057012405@T1` | 1.03578 |
| `explicit.stat_101878827@T2` | 0.98961 |
| `explicit.stat_1798257884@T2` | 0.93554 |
| `explicit.stat_101878827@T1` | 0.92592 |
| `explicit.stat_1263695895@T2` | -0.89837 |
| `explicit.stat_849987426@T1` | 0.78480 |
| `explicit.stat_2347036682@T1` | 0.70416 |
| `explicit.stat_2854751904@T2` | -0.69021 |
| `explicit.stat_1263695895@T1` | -0.63118 |
| `explicit.stat_849987426@T2` | 0.59643 |

### weapon.spear — n=8991, R²=-0.3879

intercept: `-13.4366`  ·  log_price: True  ·  ilvl: `0.18214`  ·  n_mods: `-0.12932`  ·  n_top_tier: `0.61200`  ·  corrupted: `-0.57497`  ·  n_sockets: `0.18118`  ·  quality: `0.06995`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -4.17971 |
| `crafted.stat_210067635@T2` | -3.81637 |
| `explicit.stat_1202301673@T1` | 1.14994 |
| `explicit.stat_9187492@T1` | 1.06774 |
| `explicit.stat_4080418644@T2` | -1.00382 |
| `crafted.stat_3035140377` | 0.99174 |
| `explicit.stat_1940865751@T2` | -0.98331 |
| `desecrated.stat_210067635@T1` | -0.96422 |
| `explicit.stat_3336890334@T2` | -0.90795 |
| `explicit.stat_691932474@T2` | -0.88118 |
| `explicit.stat_9187492@T2` | -0.80689 |
| `explicit.stat_3261801346@T1` | -0.78931 |

### armour.focus — n=7350, R²=-0.3358

intercept: `-16.4579`  ·  log_price: True  ·  ilvl: `0.20743`  ·  n_mods: `-0.09698`  ·  n_top_tier: `0.86180`  ·  corrupted: `-0.01807`  ·  n_sockets: `0.29776`  ·  quality: `0.02869`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.56726 |
| `explicit.stat_4220027924@T1` | -1.33328 |
| `explicit.stat_2923486259@T2` | -1.04537 |
| `explicit.stat_2231156303@T1` | -1.04192 |
| `explicit.stat_4220027924@T2` | -1.02434 |
| `explicit.stat_4015621042@T1` | -1.00632 |
| `explicit.stat_2768835289@T1` | -0.99133 |
| `explicit.stat_2231156303@T2` | -0.95066 |
| `crafted.stat_2974417149@T1` | 0.92220 |
| `explicit.stat_737908626@T2` | -0.89882 |
| `explicit.stat_2339757871@T2` | -0.89446 |
| `explicit.stat_1050105434@T2` | -0.88870 |

### armour.quiver — n=6842, R²=-0.286

intercept: `-17.8918`  ·  log_price: True  ·  ilvl: `0.21318`  ·  n_mods: `-0.04928`  ·  n_top_tier: `0.69050`  ·  corrupted: `0.96034`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.48827 |
| `explicit.stat_681332047@T2` | -1.59907 |
| `explicit.stat_681332047@T1` | -1.40593 |
| `explicit.stat_1573130764@T2` | -1.10781 |
| `explicit.stat_1573130764@T1` | -1.06485 |
| `explicit.stat_2194114101@T2` | -0.85142 |
| `explicit.stat_803737631@T1` | -0.78819 |
| `explicit.stat_4067062424@T1` | -0.74353 |
| `explicit.stat_2321178454@T2` | -0.63024 |
| `explicit.stat_803737631@T2` | -0.60902 |
| `explicit.stat_2463230181@T1` | 0.60704 |
| `explicit.stat_3261801346@T1` | -0.60144 |

### armour.shield — n=5890, R²=-0.4352

intercept: `-12.2419`  ·  log_price: True  ·  ilvl: `0.16218`  ·  n_mods: `-0.12327`  ·  n_top_tier: `0.67013`  ·  corrupted: `-0.40759`  ·  n_sockets: `0.41061`  ·  quality: `0.05879`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.49750 |
| `explicit.stat_2339757871@T1` | -1.32581 |
| `explicit.stat_328541901@T1` | -1.30959 |
| `explicit.stat_2901986750@T1` | -1.22406 |
| `explicit.stat_328541901@T2` | -1.20850 |
| `explicit.stat_1011760251@T1` | -1.13520 |
| `explicit.stat_3321629045@T2` | -1.03536 |
| `explicit.stat_2481353198@T1` | -1.02031 |
| `explicit.stat_4095671657@T2` | -0.96798 |
| `explicit.stat_2481353198@T2` | -0.95713 |
| `explicit.stat_3484657501@T1` | -0.95438 |
| `explicit.stat_4095671657@T1` | -0.94663 |

### weapon.twomace — n=5382, R²=-0.445

intercept: `-10.9325`  ·  log_price: True  ·  ilvl: `0.14517`  ·  n_mods: `-0.19541`  ·  n_top_tier: `0.42995`  ·  corrupted: `0.59480`  ·  n_sockets: `0.12681`  ·  quality: `0.06678`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.00022 |
| `explicit.stat_1037193709@T1` | -1.68057 |
| `explicit.stat_3336890334@T1` | -1.38872 |
| `explicit.stat_1263695895@T2` | -1.38458 |
| `explicit.stat_2694482655@T1` | 1.10660 |
| `explicit.stat_1263695895@T1` | -0.91848 |
| `explicit.stat_3695891184@T1` | -0.78427 |
| `explicit.stat_9187492@T1` | -0.76663 |
| `explicit.stat_518292764@T2` | -0.71626 |
| `explicit.stat_3695891184@T2` | -0.62685 |
| `explicit.stat_691932474@T1` | -0.59998 |
| `explicit.stat_387439868@T2` | -0.57399 |

## Coverage (listings per base)

- … **Sapphire** — 36319 listings (36260 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 35396 listings (35351 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 27113 listings (27082 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 12646 listings (12628 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11548 listings (11524 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 11179 listings (11153 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 11062 listings (11050 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10403 listings (10378 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10343 listings (10320 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 9837 listings (9824 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8598 listings (8583 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8242 listings (8233 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8171 listings (8162 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7355 listings (7332 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 7099 listings (7092 priced) [0.3–3985176410.3 ex]
- … **Unset Ring** — 7080 listings (7061 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 7021 listings (7006 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 6953 listings (6945 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6881 listings (6853 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6820 listings (6811 priced) [0.2–275252424.7 ex]
- … **Ancestral Tiara** — 6814 listings (6785 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6736 listings (6726 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6412 listings (6409 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6309 listings (6295 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6113 listings (6101 priced) [0.3–398912568423.8 ex]

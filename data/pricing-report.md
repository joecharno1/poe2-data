# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-09T09:05:06+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **367191** (366593 priced in exalted)
- Distinct bases: 961 · distinct mods: 2913 · mod rows: 1743086
- Sold signals: **29019** sold · 196637 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-09T08:53:36+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.28** (median |log error| 3.1036)
- Within ±30% of asking price: **15%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×56.40 · ±30% 5% · n=53714
- Premium segment (60ex+): skill **+0.07** · typical error ×269.02 · ±30% 0% · n=33746

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 7117 | ×46.01 | 21% | +0.04 | +0.05 |
| accessory.amulet | 6641 | ×25.96 | 20% | +0.02 | +0.03 |
| jewel | 6265 | ×8.22 | 7% | +0.02 | +0.04 |
| accessory.belt | 5298 | ×14.36 | 4% | +0.02 | +0.03 |
| armour.chest | 5186 | ×16.93 | 6% | +0.06 | +0.08 |
| armour.helmet | 5071 | ×17.51 | 5% | +0.02 | +0.05 |
| armour.boots | 4669 | ×24.33 | 14% | +0.09 | +0.12 |
| armour.gloves | 4622 | ×27.02 | 8% | +0.10 | +0.10 |
| other | 4408 | ×6.74 | 40% | +0.06 | +0.15 |
| weapon.wand | 3048 | ×45.75 | 20% | +0.06 | +0.06 |
| weapon.bow | 2464 | ×27.54 | 18% | +0.09 | +0.10 |
| weapon.crossbow | 2335 | ×23.59 | 21% | +0.10 | +0.10 |
| weapon.warstaff | 1283 | ×77.22 | 15% | +0.07 | +0.07 |
| weapon.staff | 1162 | ×50.00 | 15% | +0.06 | +0.05 |
| weapon.sceptre | 1119 | ×39.97 | 11% | +0.09 | +0.10 |
| weapon.spear | 965 | ×50.00 | 16% | +0.04 | +0.04 |
| armour.focus | 783 | ×62.00 | 14% | +0.06 | +0.12 |
| armour.quiver | 726 | ×60.00 | 13% | +0.03 | +0.11 |
| flask.charm | 622 | ×53.54 | 33% | +0.00 | +0.02 |
| armour.shield | 602 | ×30.00 | 14% | +0.04 | +0.10 |
| weapon.twomace | 569 | ×20.00 | 16% | +0.07 | +0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=37009, R²=-0.6088

intercept: `1.6077`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `0.00598`  ·  n_top_tier: `0.34105`  ·  corrupted: `0.56348`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.63216 |
| `explicit.stat_2974417149@T1` | 0.54506 |
| `explicit.stat_2482852589@T1` | 0.46550 |
| `explicit.stat_1050105434@T1` | -0.43565 |
| `explicit.stat_3917489142@T1` | 0.39398 |
| `explicit.stat_2106365538@T1` | 0.38234 |
| `explicit.stat_2891184298@T1` | 0.37098 |
| `explicit.stat_789117908@T1` | -0.26102 |
| `explicit.stat_101878827@T1` | -0.24430 |
| `implicit.stat_1379411836` | -0.23079 |
| `implicit.stat_4041853756` | 0.22968 |
| `implicit.stat_3879011313` | 0.22966 |

### jewel — n=34214, R²=-0.6581

intercept: `-1.1915`  ·  log_price: True  ·  ilvl: `0.03598`  ·  n_mods: `0.15503`  ·  n_top_tier: `-0.00121`  ·  corrupted: `0.30538`  ·  quality: `0.22217`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -4.51773 |
| `explicit.stat_3741323227@T1` | -3.42893 |
| `explicit.stat_3780644166@T1` | -3.28143 |
| `explicit.stat_2527686725@T1` | 3.09187 |
| `explicit.stat_1569101201@T1` | 3.08322 |
| `explicit.stat_234296660@T1` | -2.71424 |
| `explicit.stat_3174700878@T1` | 2.03856 |
| `explicit.stat_1315743832@T1` | 2.03828 |
| `explicit.stat_1697951953@T1` | -1.99243 |
| `explicit.stat_3374165039@T1` | -1.94176 |
| `explicit.stat_1316278494@T1` | -1.80729 |
| `explicit.stat_3714003708@T1` | -1.80364 |

### accessory.ring — n=32475, R²=-1.9757

intercept: `3.8045`  ·  log_price: True  ·  ilvl: `-0.04620`  ·  n_mods: `0.00278`  ·  n_top_tier: `0.05968`  ·  corrupted: `1.10353`  ·  n_sockets: `-0.03853`  ·  quality: `0.07744`

| stat_id | coef |
|---|---|
| `explicit.stat_1671376347@T1` | 0.97547 |
| `explicit.stat_707457662@T1` | 0.39821 |
| `explicit.stat_707457662@T2` | 0.34040 |
| `explicit.stat_1379411836@T1` | -0.29232 |
| `explicit.stat_3032590688@T1` | 0.26246 |
| `explicit.stat_2923486259@T1` | 0.24894 |
| `explicit.stat_1379411836@T2` | -0.20663 |
| `implicit.stat_2748665614` | -0.19891 |
| `explicit.stat_2557965901@T1` | -0.18250 |
| `explicit.stat_2557965901@T2` | -0.16401 |
| `explicit.stat_1263695895@T1` | -0.15912 |
| `explicit.stat_1967040409` | 0.12520 |

### accessory.amulet — n=30563, R²=-2.1093

intercept: `3.8849`  ·  log_price: True  ·  ilvl: `-0.04678`  ·  n_mods: `-0.02727`  ·  n_top_tier: `0.87183`  ·  corrupted: `0.08244`  ·  n_sockets: `-0.13592`  ·  quality: `-0.00248`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.43344 |
| `explicit.stat_983749596@T2` | -1.24939 |
| `explicit.stat_3299347043@T1` | -1.06528 |
| `explicit.stat_124131830` | 0.98465 |
| `explicit.stat_472520716@T1` | -0.98352 |
| `explicit.stat_2748665614@T2` | -0.97779 |
| `explicit.stat_472520716@T2` | -0.96870 |
| `explicit.stat_587431675@T1` | -0.93716 |
| `explicit.stat_3917489142@T2` | -0.93037 |
| `explicit.stat_2748665614@T1` | -0.92847 |
| `explicit.stat_124131830@T2` | -0.92387 |
| `explicit.stat_3917489142@T1` | -0.92373 |

### accessory.belt — n=24319, R²=-0.6328

intercept: `6.8323`  ·  log_price: True  ·  ilvl: `-0.05476`  ·  n_mods: `-0.40962`  ·  n_top_tier: `0.82798`  ·  corrupted: `0.88161`  ·  n_sockets: `0.06062`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.54124 |
| `explicit.stat_2881298780@T1` | -1.28872 |
| `explicit.stat_51994685@T1` | -1.28046 |
| `explicit.stat_3325883026@T1` | -1.17318 |
| `implicit.stat_731781020` | -1.12622 |
| `explicit.stat_809229260@T2` | -1.08514 |
| `explicit.stat_1389754388@T2` | -1.08402 |
| `explicit.stat_2881298780@T2` | -1.02275 |
| `explicit.stat_4220027924@T2` | -0.92447 |
| `explicit.stat_915769802@T2` | -0.89004 |
| `explicit.stat_1671376347@T2` | -0.84357 |
| `explicit.stat_2923486259@T2` | -0.84037 |

### armour.chest — n=24068, R²=-0.8971

intercept: `4.5969`  ·  log_price: True  ·  ilvl: `-0.05178`  ·  n_mods: `-0.13170`  ·  n_top_tier: `0.47504`  ·  corrupted: `0.04425`  ·  n_sockets: `0.10709`  ·  quality: `0.02680`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.12730 |
| `explicit.stat_915769802@T1` | -0.87884 |
| `explicit.stat_3325883026@T2` | -0.78967 |
| `explicit.stat_4080418644@T1` | -0.71908 |
| `explicit.stat_4080418644@T2` | -0.71859 |
| `explicit.stat_915769802@T2` | -0.71283 |
| `explicit.stat_3484657501@T1` | -0.69130 |
| `explicit.stat_3321629045@T1` | -0.64326 |
| `explicit.stat_2451402625@T2` | -0.61440 |
| `explicit.stat_2923486259@T1` | -0.61220 |
| `explicit.stat_4015621042@T2` | -0.59619 |
| `explicit.stat_986397080@T2` | -0.58859 |

### armour.helmet — n=23545, R²=-0.7854

intercept: `4.3820`  ·  log_price: True  ·  ilvl: `-0.05283`  ·  n_mods: `-0.13314`  ·  n_top_tier: `0.51417`  ·  corrupted: `0.87922`  ·  n_sockets: `0.06040`  ·  quality: `0.03703`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.73001 |
| `explicit.stat_2339757871@T1` | -1.41620 |
| `explicit.stat_1263695895@T1` | -1.11870 |
| `explicit.stat_53045048@T2` | -1.11300 |
| `explicit.stat_3362812763@T1` | -1.02513 |
| `explicit.stat_53045048@T1` | -0.89167 |
| `explicit.stat_4080418644@T2` | -0.80688 |
| `explicit.stat_3362812763@T2` | -0.74857 |
| `explicit.stat_1999113824@T1` | -0.74152 |
| `explicit.stat_1062208444@T2` | -0.73073 |
| `explicit.stat_1263695895@T2` | -0.71730 |
| `explicit.stat_587431675@T2` | -0.70653 |

### armour.boots — n=22063, R²=-1.3183

intercept: `4.3247`  ·  log_price: True  ·  ilvl: `-0.05276`  ·  n_mods: `-0.04486`  ·  n_top_tier: `0.54531`  ·  corrupted: `0.32228`  ·  n_sockets: `0.03801`  ·  quality: `0.02539`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | -7.41921 |
| `explicit.stat_2250533757@T1` | 1.67492 |
| `desecrated.stat_2250533757@T2` | -1.15416 |
| `explicit.stat_2339757871@T1` | -0.98807 |
| `explicit.stat_4220027924@T1` | 0.83447 |
| `explicit.stat_2923486259@T2` | -0.82033 |
| `explicit.stat_3917489142@T2` | -0.75411 |
| `explicit.stat_3362812763@T1` | -0.69120 |
| `explicit.stat_1062208444@T2` | -0.68759 |
| `explicit.stat_2160282525@T1` | -0.63886 |
| `explicit.stat_99927264@T1` | -0.63339 |
| `explicit.stat_3917489142@T1` | -0.61719 |

### armour.gloves — n=21494, R²=-1.2132

intercept: `4.4023`  ·  log_price: True  ·  ilvl: `-0.05872`  ·  n_mods: `-0.06398`  ·  n_top_tier: `0.56718`  ·  corrupted: `0.15666`  ·  n_sockets: `0.27937`  ·  quality: `0.02621`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.21849 |
| `explicit.stat_681332047@T2` | -1.12523 |
| `explicit.stat_3484657501@T2` | -1.05988 |
| `explicit.stat_803737631@T2` | -0.93631 |
| `explicit.stat_3484657501@T1` | -0.83827 |
| `explicit.stat_803737631@T1` | -0.80560 |
| `explicit.stat_3299347043@T2` | -0.79462 |
| `explicit.stat_3917489142@T2` | -0.78497 |
| `explicit.stat_2797971005@T2` | -0.77466 |
| `explicit.stat_9187492@T1` | 0.74584 |
| `explicit.stat_328541901@T1` | -0.74179 |
| `explicit.stat_3299347043@T1` | -0.69425 |

### weapon.wand — n=14387, R²=-2.0999

intercept: `3.9179`  ·  log_price: True  ·  ilvl: `-0.04873`  ·  n_mods: `-0.01101`  ·  n_top_tier: `0.46383`  ·  corrupted: `-0.04115`  ·  n_sockets: `0.03113`  ·  quality: `0.01084`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 3.09737 |
| `explicit.stat_4226189338@T1` | 1.99246 |
| `explicit.stat_1545858329@T1` | 1.95594 |
| `explicit.stat_591105508@T1` | 1.94073 |
| `explicit.stat_736967255@T2` | 1.72906 |
| `explicit.stat_124131830@T1` | 1.67946 |
| `explicit.stat_1600707273@T1` | 1.52819 |
| `crafted.stat_124131830` | 0.90484 |
| `explicit.stat_1600707273@T2` | 0.72716 |
| `explicit.stat_2768835289@T2` | -0.54656 |
| `explicit.stat_2974417149@T1` | 0.54436 |
| `explicit.stat_3015669065@T1` | -0.50878 |

### weapon.bow — n=11755, R²=-1.9659

intercept: `3.4856`  ·  log_price: True  ·  ilvl: `-0.04295`  ·  n_mods: `-0.01370`  ·  n_top_tier: `0.69884`  ·  corrupted: `0.30985`  ·  n_sockets: `0.00079`  ·  quality: `0.00931`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.20484 |
| `explicit.stat_2463230181@T1` | 1.56108 |
| `explicit.stat_1202301673@T1` | 1.48954 |
| `rune.stat_3885405204` | -1.43848 |
| `crafted.stat_3035140377` | 1.40617 |
| `desecrated.stat_666077204@T1` | 0.99427 |
| `explicit.stat_55876295@T1` | -0.76936 |
| `explicit.stat_518292764@T1` | 0.76043 |
| `explicit.stat_1037193709@T1` | -0.74445 |
| `explicit.stat_3336890334@T2` | -0.72849 |
| `explicit.stat_3695891184@T2` | -0.72781 |
| `explicit.stat_3261801346@T1` | -0.72748 |

### weapon.crossbow — n=11034, R²=-1.9303

intercept: `3.7672`  ·  log_price: True  ·  ilvl: `-0.04665`  ·  n_mods: `-0.00673`  ·  n_top_tier: `0.40970`  ·  corrupted: `-0.04639`  ·  n_sockets: `0.01212`  ·  quality: `0.00235`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 1.85104 |
| `explicit.stat_1980802737@T2` | -1.78606 |
| `explicit.stat_709508406@T1` | 1.70730 |
| `explicit.stat_2250681686@T2` | -1.35869 |
| `explicit.stat_1980802737` | 1.33050 |
| `explicit.stat_1509134228@T1` | 1.13280 |
| `explicit.stat_2250681686` | 0.95580 |
| `crafted.stat_3035140377` | 0.89683 |
| `rune.stat_669069897` | -0.71766 |
| `rune.stat_1586906534` | 0.58374 |
| `explicit.stat_1263695895@T2` | -0.50421 |
| `explicit.stat_1202301673@T2` | -0.49172 |

### flask.charm — n=8394, R²=-0.427

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.03380`  ·  corrupted: `0.54220`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.93355 |
| `explicit.stat_1056492907` | 3.40113 |
| `explicit.stat_2676834156@T1` | 1.57561 |
| `explicit.stat_2541588185@T1` | 0.34630 |
| `explicit.stat_828533480@T2` | -0.03380 |
| `explicit.stat_1873752457@T2` | -0.03380 |
| `explicit.stat_1120862500@T2` | -0.03380 |
| `explicit.stat_388617051@T2` | -0.03380 |
| `explicit.stat_2676834156@T2` | -0.03380 |
| `explicit.stat_828533480@T1` | -0.03380 |
| `explicit.stat_3196823591@T2` | -0.03380 |
| `explicit.stat_1873752457@T1` | -0.03380 |

### weapon.warstaff — n=5965, R²=-0.6029

intercept: `-0.0193`  ·  log_price: True  ·  ilvl: `0.00026`  ·  n_mods: `-0.00057`  ·  n_top_tier: `0.35866`  ·  corrupted: `0.51944`  ·  n_sockets: `0.00049`  ·  quality: `0.04512`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T1` | 1.24791 |
| `rune.stat_243313994` | 1.23477 |
| `rune.stat_731403740` | 1.18319 |
| `crafted.stat_210067635@T2` | -0.68097 |
| `desecrated.stat_9187492` | 0.47199 |
| `rune.stat_1712188793` | -0.44247 |
| `crafted.stat_3035140377` | 0.38378 |
| `explicit.stat_1509134228@T1` | -0.36025 |
| `explicit.stat_328541901@T1` | -0.36018 |
| `explicit.stat_328541901@T2` | -0.36005 |
| `explicit.stat_3336890334@T2` | -0.35958 |
| `explicit.stat_1940865751@T1` | -0.35939 |

### weapon.staff — n=5495, R²=-0.6389

intercept: `-0.1207`  ·  log_price: True  ·  ilvl: `0.00149`  ·  n_mods: `-0.00013`  ·  n_top_tier: `0.09672`  ·  corrupted: `0.06087`  ·  n_sockets: `0.00476`  ·  quality: `0.00414`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 4.06702 |
| `explicit.stat_4226189338@T1` | 2.33083 |
| `explicit.stat_2254480358@T1` | 1.50422 |
| `explicit.stat_1545858329@T1` | 1.49903 |
| `explicit.stat_2768835289@T2` | 1.49181 |
| `explicit.stat_2254480358@T2` | 1.48847 |
| `explicit.stat_1600707273@T1` | 1.44715 |
| `explicit.stat_4226189338@T2` | 1.41185 |
| `explicit.stat_124131830@T1` | 0.92998 |
| `explicit.stat_3962278098@T2` | 0.59755 |
| `explicit.stat_473429811@T1` | 0.59719 |
| `explicit.stat_3291658075@T2` | 0.52646 |

### weapon.sceptre — n=5479, R²=-0.5901

intercept: `-3.4760`  ·  log_price: True  ·  ilvl: `0.04369`  ·  n_mods: `-0.02765`  ·  n_top_tier: `0.48243`  ·  corrupted: `1.13261`  ·  n_sockets: `0.10309`  ·  quality: `0.08253`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.83556 |
| `explicit.stat_3984865854@T1` | 0.82885 |
| `explicit.stat_4080418644@T1` | -0.62330 |
| `explicit.stat_1263695895@T2` | -0.56864 |
| `explicit.stat_4080418644@T2` | -0.56410 |
| `explicit.stat_1263695895@T1` | -0.55427 |
| `explicit.stat_1574590649@T2` | -0.53579 |
| `explicit.stat_2347036682@T2` | -0.53046 |
| `explicit.stat_2854751904@T1` | -0.52717 |
| `explicit.stat_1574590649@T1` | -0.51881 |
| `explicit.stat_328541901@T1` | -0.50636 |
| `explicit.stat_3639275092@T2` | -0.50518 |

### weapon.spear — n=4645, R²=-0.659

intercept: `-0.0175`  ·  log_price: True  ·  ilvl: `0.00023`  ·  n_mods: `-0.00010`  ·  n_top_tier: `0.18803`  ·  corrupted: `0.00003`  ·  n_sockets: `0.00039`  ·  quality: `0.04894`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.09262 |
| `crafted.stat_3035140377` | 1.43109 |
| `explicit.stat_9187492@T1` | 1.42146 |
| `explicit.stat_210067635@T1` | 0.91232 |
| `explicit.stat_3336890334@T1` | 0.83903 |
| `crafted.stat_518292764` | 0.57395 |
| `explicit.stat_1509134228@T1` | 0.39363 |
| `rune.stat_1039491398` | 0.20919 |
| `explicit.stat_1263695895@T2` | -0.18936 |
| `explicit.stat_691932474@T1` | -0.18866 |
| `explicit.stat_55876295@T1` | -0.18857 |
| `explicit.stat_1263695895@T1` | -0.18851 |

### armour.focus — n=3719, R²=-0.6256

intercept: `-1.9562`  ·  log_price: True  ·  ilvl: `0.02415`  ·  n_mods: `-0.00423`  ·  n_top_tier: `0.71321`  ·  corrupted: `0.00167`  ·  n_sockets: `0.07136`  ·  quality: `0.07929`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -6.33534 |
| `desecrated.stat_378817135@T1` | 5.01523 |
| `crafted.stat_2974417149@T1` | -3.20480 |
| `desecrated.stat_3393628375@T1` | 2.02263 |
| `explicit.stat_4220027924@T2` | -0.77559 |
| `explicit.stat_124131830@T2` | -0.76223 |
| `explicit.stat_789117908@T2` | -0.76089 |
| `explicit.stat_2974417149@T1` | -0.74595 |
| `explicit.stat_2891184298@T2` | -0.74579 |
| `explicit.stat_4052037485@T2` | -0.74476 |
| `explicit.stat_3962278098@T2` | -0.74366 |
| `explicit.stat_2923486259@T1` | -0.73731 |

### armour.quiver — n=3541, R²=-0.6115

intercept: `-1.4935`  ·  log_price: True  ·  ilvl: `0.01738`  ·  n_mods: `0.01020`  ·  n_top_tier: `1.15475`  ·  corrupted: `0.45312`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 10.87158 |
| `explicit.stat_2463230181@T2` | -1.46820 |
| `explicit.stat_681332047@T2` | -1.28267 |
| `explicit.stat_681332047@T1` | -1.24574 |
| `explicit.stat_1573130764@T1` | -1.21423 |
| `explicit.stat_2194114101@T2` | -1.20197 |
| `explicit.stat_1573130764@T2` | -1.19844 |
| `explicit.stat_1368271171@T2` | -1.19558 |
| `explicit.stat_1368271171@T1` | -1.17032 |
| `explicit.stat_3714003708@T2` | -1.16946 |
| `explicit.stat_2321178454@T2` | -1.16615 |
| `explicit.stat_3261801346@T1` | -1.15804 |

### armour.shield — n=3035, R²=-0.6047

intercept: `-0.1568`  ·  log_price: True  ·  ilvl: `0.00196`  ·  n_mods: `-0.00010`  ·  n_top_tier: `0.41158`  ·  corrupted: `0.02679`  ·  n_sockets: `0.00153`  ·  quality: `0.07958`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.86310 |
| `explicit.stat_1978899297@T2` | -0.57596 |
| `explicit.stat_4220027924@T1` | 0.50013 |
| `explicit.stat_1011760251@T2` | -0.43138 |
| `explicit.stat_328541901@T1` | -0.42474 |
| `explicit.stat_2339757871@T1` | -0.42069 |
| `explicit.stat_328541901@T2` | -0.41966 |
| `explicit.stat_2481353198@T2` | -0.41937 |
| `explicit.stat_3484657501@T1` | -0.41877 |
| `explicit.stat_2481353198@T1` | -0.41872 |
| `explicit.stat_3372524247@T2` | -0.41678 |
| `explicit.stat_1671376347@T1` | -0.41536 |

### weapon.twomace — n=2754, R²=-0.5827

intercept: `-0.3787`  ·  log_price: True  ·  ilvl: `0.00480`  ·  n_mods: `-0.00163`  ·  n_top_tier: `0.76158`  ·  corrupted: `0.59013`  ·  n_sockets: `0.00880`  ·  quality: `0.01138`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.64389 |
| `crafted.stat_3035140377` | 1.13114 |
| `explicit.stat_1037193709@T1` | -0.78607 |
| `explicit.stat_3336890334@T1` | -0.78446 |
| `explicit.stat_387439868@T2` | -0.78151 |
| `explicit.stat_1037193709@T2` | -0.77735 |
| `explicit.stat_821021828@T2` | -0.77142 |
| `explicit.stat_691932474@T1` | -0.77035 |
| `explicit.stat_3695891184@T1` | -0.76995 |
| `explicit.stat_709508406@T1` | -0.76928 |
| `explicit.stat_3695891184@T2` | -0.76797 |
| `explicit.stat_3639275092@T1` | -0.76773 |

## Coverage (listings per base)

- … **Sapphire** — 16194 listings (16172 priced) [0.4–7553463.8 ex]
- … **Emerald** — 16022 listings (16006 priced) [0.4–7553463.8 ex]
- … **Ruby** — 12346 listings (12334 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 7090 listings (7084 priced) [0.2–5288620.9 ex]
- … **Prismatic Ring** — 5644 listings (5638 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 5497 listings (5487 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 5410 listings (5407 priced) [0.2–4323655.9 ex]
- … **Stellar Amulet** — 5338 listings (5335 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 5218 listings (5210 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 5026 listings (5022 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 4534 listings (4525 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4233 listings (4228 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 4094 listings (4091 priced) [1.0–307202867.9 ex]
- … **Ruby Ring** — 4083 listings (4081 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 3728 listings (3723 priced) [0.2–5286174.1 ex]
- … **Lapis Amulet** — 3675 listings (3673 priced) [0.2–5286174.1 ex]
- … **Ancestral Tiara** — 3626 listings (3621 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3586 listings (3585 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3577 listings (3576 priced) [0.2–4547453.5 ex]
- … **Obliterator Bow** — 3503 listings (3494 priced) [0.4–42622633798.0 ex]
- … **Unset Ring** — 3449 listings (3448 priced) [0.2–24532814.5 ex]
- … **Heavy Belt** — 3448 listings (3447 priced) [0.2–4877938.3 ex]
- … **Bloodstone Amulet** — 3357 listings (3356 priced) [0.2–4275054.0 ex]
- … **Pearl Ring** — 3278 listings (3276 priced) [0.2–24532814.5 ex]
- … **Lunar Amulet** — 3213 listings (3211 priced) [0.4–4877938.3 ex]

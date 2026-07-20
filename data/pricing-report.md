# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-20T06:24:08+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **674619** (672519 priced in exalted)
- Distinct bases: 998 · distinct mods: 3296 · mod rows: 3193635
- Sold signals: **24442** sold · 383834 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-20T06:10:18+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.05** (median |log error| 3.1801)
- Within ±30% of asking price: **21%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×68.74 · ±30% 7% · n=98356
- Premium segment (60ex+): skill **+0.12** · typical error ×306.43 · ±30% 0% · n=66018

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 14285 | ×52.10 | 21% | +0.03 | +0.06 |
| jewel | 13579 | ×56.64 | 22% | +0.03 | +0.03 |
| accessory.amulet | 12902 | ×16.34 | 26% | +0.01 | +0.01 |
| accessory.belt | 9312 | ×22.20 | 22% | +0.03 | +0.05 |
| armour.chest | 8974 | ×18.18 | 23% | +0.07 | +0.10 |
| armour.helmet | 8808 | ×29.30 | 20% | +0.07 | +0.10 |
| armour.boots | 8170 | ×27.64 | 20% | +0.09 | +0.12 |
| armour.gloves | 7956 | ×35.86 | 17% | +0.07 | +0.10 |
| other | 7903 | ×1.93 | 42% | +0.12 | +0.19 |
| weapon.wand | 4778 | ×44.53 | 17% | +0.09 | +0.11 |
| weapon.bow | 3744 | ×30.92 | 14% | +0.13 | +0.15 |
| weapon.crossbow | 3537 | ×30.78 | 17% | +0.10 | +0.14 |
| weapon.warstaff | 2419 | ×15.75 | 6% | +0.21 | +0.20 |
| weapon.staff | 2266 | ×19.33 | 6% | +0.18 | +0.17 |
| weapon.sceptre | 2260 | ×20.89 | 5% | +0.10 | +0.10 |
| weapon.spear | 1809 | ×17.47 | 7% | +0.12 | +0.13 |
| armour.focus | 1502 | ×17.78 | 6% | +0.11 | +0.12 |
| armour.quiver | 1415 | ×20.41 | 7% | +0.16 | +0.17 |
| flask.charm | 1166 | ×12.44 | 28% | -0.01 | +0.01 |
| armour.shield | 1158 | ×16.77 | 7% | +0.09 | +0.11 |
| weapon.twomace | 1069 | ×9.19 | 8% | +0.11 | +0.12 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=74162, R²=-1.8825

intercept: `-0.0716`  ·  log_price: True  ·  ilvl: `0.00088`  ·  n_mods: `1.02336`  ·  n_top_tier: `-0.87735`  ·  corrupted: `1.22077`  ·  quality: `0.25453`

| stat_id | coef |
|---|---|
| `explicit.stat_3714003708@T1` | 3.44633 |
| `explicit.stat_3485067555@T1` | 3.26440 |
| `explicit.stat_1604736568@T1` | -2.39420 |
| `explicit.stat_3473929743@T1` | -2.33601 |
| `explicit.stat_1604736568` | 2.26474 |
| `explicit.stat_1854213750@T1` | 1.47482 |
| `explicit.stat_3174700878@T1` | 1.39385 |
| `explicit.stat_587431675@T1` | -0.96932 |
| `explicit.stat_274716455@T1` | -0.90226 |
| `explicit.stat_3556824919@T1` | 0.90119 |
| `explicit.stat_2194114101@T1` | -0.65664 |
| `explicit.stat_2231156303@T1` | 0.64432 |

### accessory.ring — n=65144, R²=-2.0436

intercept: `3.4267`  ·  log_price: True  ·  ilvl: `-0.04274`  ·  n_mods: `0.00259`  ·  n_top_tier: `1.09981`  ·  corrupted: `0.01350`  ·  n_sockets: `1.99864`  ·  quality: `0.03237`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T2` | -1.12584 |
| `explicit.stat_4220027924@T2` | -1.12314 |
| `explicit.stat_2231156303@T1` | -1.11977 |
| `explicit.stat_1573130764@T1` | -1.11974 |
| `explicit.stat_803737631@T1` | -1.11888 |
| `explicit.stat_4080418644@T1` | -1.11569 |
| `explicit.stat_736967255@T2` | -1.11283 |
| `explicit.stat_2144192055@T1` | -1.11043 |
| `explicit.stat_3291658075@T2` | -1.10956 |
| `explicit.stat_2891184298@T2` | -1.10875 |
| `explicit.stat_2891184298@T1` | -1.10792 |
| `explicit.stat_2901986750@T2` | -1.10673 |

### other — n=64229, R²=-0.6069

intercept: `1.6088`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.17261`  ·  n_top_tier: `0.17382`  ·  corrupted: `0.00129`  ·  n_sockets: `-0.00017`  ·  quality: `-0.00002`

| stat_id | coef |
|---|---|
| `implicit.stat_718638445` | 0.51814 |
| `implicit.stat_3182714256` | 0.51812 |
| `explicit.stat_1050105434@T1` | -0.22126 |
| `implicit.stat_2219129443` | 0.21297 |
| `implicit.stat_4041853756` | 0.21296 |
| `implicit.stat_3879011313` | 0.21296 |
| `explicit.stat_3299347043@T1` | -0.20883 |
| `explicit.stat_2974417149@T1` | 0.19808 |
| `implicit.stat_958696139` | -0.17250 |
| `implicit.stat_1416292992` | -0.09591 |
| `implicit.stat_3032590688` | -0.06897 |
| `explicit.stat_2901986750` | 0.06151 |

### accessory.amulet — n=58824, R²=-0.4782

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `1.09828`  ·  corrupted: `-0.00001`  ·  n_sockets: `1.79001`  ·  quality: `0.04398`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T2` | -1.16464 |
| `explicit.stat_2162097452@T2` | -1.16072 |
| `explicit.stat_1202301673@T2` | -1.14710 |
| `explicit.stat_983749596@T2` | -1.09831 |
| `explicit.stat_803737631@T1` | -1.09831 |
| `explicit.stat_803737631@T2` | -1.09831 |
| `explicit.stat_789117908@T2` | -1.09830 |
| `explicit.stat_789117908@T1` | -1.09830 |
| `explicit.stat_3299347043@T2` | -1.09830 |
| `explicit.stat_328541901@T2` | -1.09829 |
| `explicit.stat_328541901@T1` | -1.09829 |
| `explicit.stat_4220027924@T2` | -1.09829 |

### accessory.belt — n=42646, R²=-1.9031

intercept: `2.3976`  ·  log_price: True  ·  ilvl: `-0.02893`  ·  n_mods: `-0.01315`  ·  n_top_tier: `0.57774`  ·  corrupted: `0.95208`  ·  n_sockets: `1.07810`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -0.60841 |
| `explicit.stat_2881298780@T1` | -0.59789 |
| `explicit.stat_3299347043@T2` | -0.59579 |
| `explicit.stat_4220027924@T2` | -0.59010 |
| `explicit.stat_51994685@T1` | -0.58991 |
| `explicit.stat_915769802@T1` | -0.58980 |
| `explicit.stat_3325883026@T1` | -0.58654 |
| `explicit.stat_3372524247@T2` | -0.58265 |
| `explicit.stat_809229260@T2` | -0.58137 |
| `explicit.stat_2881298780@T2` | -0.58112 |
| `explicit.stat_1570770415@T2` | -0.57963 |
| `explicit.stat_1389754388@T1` | -0.57874 |

### armour.chest — n=42252, R²=-1.7959

intercept: `3.1961`  ·  log_price: True  ·  ilvl: `-0.03952`  ·  n_mods: `-0.01109`  ·  n_top_tier: `0.38141`  ·  corrupted: `0.05005`  ·  n_sockets: `0.01575`  ·  quality: `0.07428`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.68649 |
| `explicit.stat_3981240776@T1` | 0.63551 |
| `explicit.stat_986397080@T2` | -0.45388 |
| `explicit.stat_986397080@T1` | -0.44223 |
| `explicit.stat_1692879867@T2` | -0.41552 |
| `explicit.stat_3484657501@T1` | -0.40427 |
| `explicit.stat_4080418644@T2` | -0.40266 |
| `explicit.stat_915769802@T2` | -0.40239 |
| `explicit.stat_4080418644@T1` | -0.40144 |
| `explicit.stat_1692879867@T1` | -0.39461 |
| `explicit.stat_915769802@T1` | -0.39214 |
| `explicit.stat_3299347043@T2` | -0.39167 |

### armour.helmet — n=41111, R²=-1.7954

intercept: `3.2410`  ·  log_price: True  ·  ilvl: `-0.04078`  ·  n_mods: `-0.01442`  ·  n_top_tier: `0.46149`  ·  corrupted: `0.63296`  ·  n_sockets: `0.03333`  ·  quality: `0.07467`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.69300 |
| `explicit.stat_1263695895@T1` | -0.65644 |
| `explicit.stat_3917489142@T2` | -0.65582 |
| `explicit.stat_2162097452@T2` | -0.63700 |
| `crafted.stat_3917489142@T1` | -0.62775 |
| `explicit.stat_3917489142@T1` | -0.57955 |
| `explicit.stat_1263695895@T2` | -0.53788 |
| `explicit.stat_4052037485@T2` | -0.50275 |
| `explicit.stat_803737631@T1` | -0.49704 |
| `explicit.stat_1999113824@T1` | -0.49321 |
| `explicit.stat_803737631@T2` | -0.49078 |
| `explicit.stat_3321629045@T2` | -0.48489 |

### armour.boots — n=38212, R²=-1.747

intercept: `3.4261`  ·  log_price: True  ·  ilvl: `-0.04227`  ·  n_mods: `-0.01711`  ·  n_top_tier: `0.49218`  ·  corrupted: `0.07891`  ·  n_sockets: `0.03969`  ·  quality: `0.06867`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.73933 |
| `crafted.stat_3917489142@T1` | 1.55173 |
| `explicit.stat_2339757871@T1` | -1.18848 |
| `explicit.stat_2923486259@T1` | 0.61599 |
| `explicit.stat_3917489142@T2` | -0.60118 |
| `explicit.stat_3299347043@T1` | -0.59614 |
| `explicit.stat_1874553720@T1` | -0.56348 |
| `explicit.stat_2923486259@T2` | -0.55402 |
| `explicit.stat_2160282525@T1` | -0.53516 |
| `explicit.stat_124859000@T1` | -0.52652 |
| `explicit.stat_1671376347@T2` | -0.52623 |
| `explicit.stat_328541901@T2` | -0.52298 |

### armour.gloves — n=37142, R²=-1.7506

intercept: `3.7862`  ·  log_price: True  ·  ilvl: `-0.04913`  ·  n_mods: `-0.01156`  ·  n_top_tier: `0.71779`  ·  corrupted: `-0.02088`  ·  n_sockets: `0.11525`  ·  quality: `0.06044`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.59267 |
| `rune.stat_201332984` | 1.28274 |
| `explicit.stat_2923486259@T1` | -1.09090 |
| `explicit.stat_4052037485@T1` | -0.93225 |
| `explicit.stat_3321629045@T2` | -0.93068 |
| `explicit.stat_4052037485@T2` | -0.92153 |
| `explicit.stat_3484657501@T2` | -0.89841 |
| `explicit.stat_4015621042@T2` | -0.89576 |
| `explicit.stat_9187492@T2` | -0.85561 |
| `explicit.stat_803737631@T2` | -0.84779 |
| `explicit.stat_2923486259@T2` | -0.84171 |
| `explicit.stat_803737631@T1` | -0.83360 |

### weapon.wand — n=22276, R²=-2.0403

intercept: `3.9583`  ·  log_price: True  ·  ilvl: `-0.04923`  ·  n_mods: `-0.04897`  ·  n_top_tier: `0.24208`  ·  corrupted: `-0.04102`  ·  n_sockets: `0.04155`  ·  quality: `0.03665`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.14123 |
| `rune.stat_124131830` | -2.81803 |
| `explicit.stat_2254480358@T1` | 2.76679 |
| `explicit.stat_124131830@T1` | 2.40447 |
| `explicit.stat_591105508@T1` | 2.11492 |
| `explicit.stat_4226189338@T1` | 2.07568 |
| `explicit.stat_736967255@T2` | 1.93738 |
| `explicit.stat_2254480358@T2` | 1.41996 |
| `explicit.stat_1600707273@T1` | 1.30423 |
| `crafted.stat_124131830` | 1.25551 |
| `explicit.stat_4226189338@T2` | 1.14493 |
| `explicit.stat_1600707273@T2` | 0.78091 |

### flask.charm — n=18688, R²=-0.6423

intercept: `0.1060`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.45640`  ·  corrupted: `1.55059`  ·  quality: `0.00511`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60517 |
| `explicit.stat_1056492907` | 2.70912 |
| `explicit.stat_1120862500@T2` | -1.45644 |
| `explicit.stat_828533480@T2` | -1.45643 |
| `explicit.stat_1873752457@T2` | -1.45639 |
| `explicit.stat_3196823591@T2` | -1.45636 |
| `explicit.stat_2365392475@T2` | -1.45634 |
| `explicit.stat_388617051@T2` | -1.45603 |
| `explicit.stat_1873752457@T1` | -1.45495 |
| `explicit.stat_2676834156@T2` | -1.45397 |
| `explicit.stat_828533480@T1` | -1.44292 |
| `explicit.stat_2541588185@T2` | -1.43541 |

### weapon.bow — n=17744, R²=-1.9498

intercept: `4.1179`  ·  log_price: True  ·  ilvl: `-0.04952`  ·  n_mods: `-0.05434`  ·  n_top_tier: `0.81293`  ·  corrupted: `0.57146`  ·  n_sockets: `0.02977`  ·  quality: `0.03352`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.75695 |
| `crafted.stat_3035140377` | 1.33548 |
| `explicit.stat_3336890334@T1` | 1.23429 |
| `explicit.stat_1263695895@T1` | -1.05254 |
| `explicit.stat_1263695895@T2` | -1.04388 |
| `explicit.stat_709508406@T1` | 0.95811 |
| `explicit.stat_1368271171@T2` | -0.85983 |
| `explicit.stat_1509134228@T1` | -0.85583 |
| `explicit.stat_210067635@T2` | -0.84903 |
| `explicit.stat_3695891184@T2` | -0.84277 |
| `explicit.stat_3639275092@T1` | -0.83958 |
| `explicit.stat_1368271171@T1` | -0.83709 |

### weapon.crossbow — n=16668, R²=-1.8679

intercept: `4.0514`  ·  log_price: True  ·  ilvl: `-0.04990`  ·  n_mods: `-0.03969`  ·  n_top_tier: `0.36541`  ·  corrupted: `0.06696`  ·  n_sockets: `0.05323`  ·  quality: `0.03377`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 1.69260 |
| `explicit.stat_1980802737@T2` | -1.67576 |
| `explicit.stat_2250681686@T2` | -1.53949 |
| `explicit.stat_1980802737` | 1.34057 |
| `explicit.stat_2250681686` | 1.24789 |
| `explicit.stat_1509134228@T1` | 0.88948 |
| `crafted.stat_3035140377` | 0.77905 |
| `explicit.stat_709508406@T1` | 0.68223 |
| `explicit.stat_1263695895@T2` | -0.56739 |
| `explicit.stat_1263695895@T1` | -0.51218 |
| `explicit.stat_3336890334@T2` | -0.49934 |
| `explicit.stat_387439868@T1` | 0.48156 |

### weapon.warstaff — n=11491, R²=-0.3469

intercept: `-10.6111`  ·  log_price: True  ·  ilvl: `0.14278`  ·  n_mods: `-0.20339`  ·  n_top_tier: `0.39538`  ·  corrupted: `0.37306`  ·  n_sockets: `0.13543`  ·  quality: `0.05623`

| stat_id | coef |
|---|---|
| `desecrated.stat_3291658075@T1` | -1.75999 |
| `desecrated.stat_473429811@T1` | -1.75999 |
| `desecrated.stat_2231156303@T1` | 1.60832 |
| `desecrated.stat_2527686725@T1` | 1.60832 |
| `crafted.stat_210067635@T2` | 1.22761 |
| `explicit.stat_1368271171@T1` | -0.82057 |
| `explicit.stat_328541901@T2` | -0.79851 |
| `desecrated.stat_9187492` | 0.78360 |
| `explicit.stat_328541901@T1` | -0.75807 |
| `explicit.stat_1037193709@T1` | 0.73937 |
| `explicit.stat_1509134228@T1` | 0.69399 |
| `rune.stat_243313994` | 0.68887 |

### weapon.staff — n=10861, R²=-0.3531

intercept: `-16.3969`  ·  log_price: True  ·  ilvl: `0.21129`  ·  n_mods: `-0.07900`  ·  n_top_tier: `0.43267`  ·  corrupted: `0.71587`  ·  n_sockets: `0.17765`  ·  quality: `0.04288`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.31591 |
| `explicit.stat_4226189338@T1` | 2.16935 |
| `explicit.stat_1545858329@T1` | 2.12890 |
| `explicit.stat_124131830@T1` | 1.60118 |
| `explicit.stat_2254480358@T1` | 1.35707 |
| `explicit.stat_1600707273@T1` | 1.35014 |
| `explicit.stat_293638271@T2` | -1.20858 |
| `explicit.stat_2254480358@T2` | 0.92718 |
| `explicit.stat_473429811@T2` | -0.73639 |
| `explicit.stat_3962278098@T2` | 0.70706 |
| `explicit.stat_591105508@T2` | 0.67511 |
| `explicit.stat_4226189338@T2` | 0.63703 |

### weapon.sceptre — n=10680, R²=-0.3297

intercept: `-22.0313`  ·  log_price: True  ·  ilvl: `0.28072`  ·  n_mods: `0.02874`  ·  n_top_tier: `0.22399`  ·  corrupted: `0.20212`  ·  n_sockets: `0.19641`  ·  quality: `0.02894`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.31803 |
| `explicit.stat_3057012405@T1` | 1.36382 |
| `explicit.stat_1263695895@T2` | -1.28468 |
| `explicit.stat_2162097452@T2` | 1.05348 |
| `explicit.stat_1263695895@T1` | -0.93961 |
| `explicit.stat_1798257884@T2` | 0.92584 |
| `explicit.stat_2854751904@T2` | -0.83121 |
| `explicit.stat_101878827@T2` | 0.81599 |
| `explicit.stat_101878827@T1` | 0.77840 |
| `explicit.stat_849987426@T1` | 0.67840 |
| `explicit.stat_289128254@T1` | 0.61435 |
| `explicit.stat_1250712710@T2` | 0.61193 |

### weapon.spear — n=8643, R²=-0.3589

intercept: `-14.0259`  ·  log_price: True  ·  ilvl: `0.19097`  ·  n_mods: `-0.13836`  ·  n_top_tier: `0.55153`  ·  corrupted: `-0.36030`  ·  n_sockets: `0.24182`  ·  quality: `0.07860`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.00400 |
| `explicit.stat_1202301673@T1` | 1.18019 |
| `explicit.stat_9187492@T1` | 1.17515 |
| `explicit.stat_1509134228@T1` | 1.10203 |
| `explicit.stat_1940865751@T2` | -1.07592 |
| `explicit.stat_4080418644@T2` | -0.92993 |
| `desecrated.stat_210067635@T1` | -0.75852 |
| `explicit.stat_691932474@T2` | -0.75739 |
| `crafted.stat_3035140377` | 0.75500 |
| `explicit.stat_748522257@T2` | -0.74408 |
| `explicit.stat_3336890334@T2` | -0.73843 |
| `explicit.stat_518292764@T2` | 0.70607 |

### armour.focus — n=7044, R²=-0.3392

intercept: `-15.2356`  ·  log_price: True  ·  ilvl: `0.19452`  ·  n_mods: `-0.14689`  ·  n_top_tier: `0.98775`  ·  corrupted: `0.11780`  ·  n_sockets: `0.30708`  ·  quality: `0.04694`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 2.82044 |
| `explicit.stat_2923486259@T1` | -1.79623 |
| `explicit.stat_4220027924@T1` | -1.56898 |
| `crafted.stat_737908626@T2` | 1.56579 |
| `explicit.stat_4220027924@T2` | -1.24454 |
| `explicit.stat_2339757871@T2` | -1.19702 |
| `explicit.stat_2231156303@T1` | -1.16027 |
| `explicit.stat_2923486259@T2` | -1.13477 |
| `explicit.stat_274716455@T1` | -1.08231 |
| `explicit.stat_2231156303@T2` | -1.05967 |
| `explicit.stat_4015621042@T1` | -1.04923 |
| `explicit.stat_2974417149@T2` | -1.00560 |

### armour.quiver — n=6589, R²=-0.2884

intercept: `-16.7030`  ·  log_price: True  ·  ilvl: `0.20408`  ·  n_mods: `-0.12825`  ·  n_top_tier: `0.71274`  ·  corrupted: `0.86994`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.06871 |
| `explicit.stat_2463230181@T1` | 1.79534 |
| `explicit.stat_681332047@T2` | -1.53358 |
| `explicit.stat_681332047@T1` | -1.29638 |
| `explicit.stat_1573130764@T1` | -1.22147 |
| `explicit.stat_1573130764@T2` | -1.08296 |
| `explicit.stat_2463230181@T2` | 0.98596 |
| `explicit.stat_4067062424@T1` | -0.89596 |
| `explicit.stat_803737631@T1` | -0.89050 |
| `explicit.stat_4067062424@T2` | -0.85228 |
| `explicit.stat_2321178454@T2` | -0.75107 |
| `explicit.stat_803737631@T2` | -0.69566 |

### armour.shield — n=5670, R²=-0.4325

intercept: `-14.0505`  ·  log_price: True  ·  ilvl: `0.18521`  ·  n_mods: `-0.08705`  ·  n_top_tier: `0.68430`  ·  corrupted: `-0.34173`  ·  n_sockets: `0.39475`  ·  quality: `0.05978`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.97562 |
| `explicit.stat_3855016469@T1` | -1.28204 |
| `explicit.stat_1011760251@T1` | -1.21984 |
| `explicit.stat_2339757871@T2` | -1.19563 |
| `explicit.stat_3321629045@T2` | -1.18624 |
| `explicit.stat_2481353198@T1` | -1.03628 |
| `explicit.stat_3484657501@T1` | -1.03246 |
| `explicit.stat_2481353198@T2` | -1.00971 |
| `explicit.stat_2451402625@T1` | -0.98385 |
| `explicit.stat_4095671657@T2` | -0.97828 |
| `explicit.stat_3033371881@T2` | -0.93938 |
| `explicit.stat_2901986750@T1` | -0.92308 |

### weapon.twomace — n=5207, R²=-0.4506

intercept: `-10.3991`  ·  log_price: True  ·  ilvl: `0.14157`  ·  n_mods: `-0.21173`  ·  n_top_tier: `0.36109`  ·  corrupted: `0.48784`  ·  n_sockets: `0.13356`  ·  quality: `0.06542`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.21914 |
| `explicit.stat_1037193709@T1` | -1.57652 |
| `explicit.stat_3336890334@T1` | -1.12355 |
| `explicit.stat_1263695895@T2` | -1.07169 |
| `explicit.stat_2694482655@T1` | 0.97577 |
| `explicit.stat_9187492@T1` | -0.80245 |
| `explicit.stat_691932474@T1` | -0.77270 |
| `explicit.stat_518292764@T1` | 0.73867 |
| `explicit.stat_3695891184@T1` | -0.72592 |
| `explicit.stat_3695891184@T2` | -0.71393 |
| `explicit.stat_1509134228@T1` | 0.66063 |
| `crafted.stat_3035140377` | 0.60054 |

## Coverage (listings per base)

- … **Sapphire** — 34198 listings (34142 priced) [0.3–3985176410.3 ex]
- … **Emerald** — 33278 listings (33236 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 25533 listings (25502 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 12184 listings (12166 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11001 listings (10977 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10626 listings (10601 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 10524 listings (10513 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 9930 listings (9908 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9831 listings (9809 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 9434 listings (9421 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8158 listings (8143 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7852 listings (7843 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 7760 listings (7751 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7153 listings (7131 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6789 listings (6782 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 6719 listings (6700 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6707 listings (6693 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6672 listings (6665 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6650 listings (6622 priced) [0.3–398912568423.8 ex]
- … **Ancestral Tiara** — 6557 listings (6528 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6472 listings (6463 priced) [0.2–275252424.7 ex]
- … **Bloodstone Amulet** — 6464 listings (6454 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6145 listings (6142 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6042 listings (6028 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5893 listings (5883 priced) [0.3–398912568423.8 ex]

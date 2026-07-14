# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-14T22:41:04+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **486274** (485280 priced in exalted)
- Distinct bases: 980 · distinct mods: 3067 · mod rows: 2308477
- Sold signals: **26560** sold · 270507 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-14T22:17:43+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.53** (median |log error| 3.115)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.08** · typical error ×52.78 · ±30% 6% · n=69561
- Premium segment (60ex+): skill **+0.10** · typical error ×189.96 · ±30% 0% · n=45976

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 9610 | ×52.35 | 21% | +0.06 | +0.08 |
| jewel | 8945 | ×9.34 | 5% | +0.02 | +0.06 |
| accessory.amulet | 8921 | ×52.19 | 21% | +0.03 | +0.03 |
| accessory.belt | 6854 | ×10.00 | 18% | +0.04 | +0.04 |
| armour.chest | 6663 | ×15.39 | 5% | +0.00 | +0.03 |
| armour.helmet | 6586 | ×15.72 | 5% | +0.02 | +0.04 |
| armour.boots | 6127 | ×23.11 | 6% | +0.10 | +0.12 |
| armour.gloves | 5996 | ×20.79 | 5% | +0.09 | +0.11 |
| other | 5283 | ×9.96 | 36% | +0.09 | +0.18 |
| weapon.wand | 3857 | ×33.63 | 18% | +0.08 | +0.09 |
| weapon.bow | 3093 | ×26.73 | 17% | +0.10 | +0.10 |
| weapon.crossbow | 2900 | ×21.75 | 18% | +0.09 | +0.14 |
| weapon.warstaff | 1706 | ×34.68 | 18% | +0.10 | +0.09 |
| weapon.sceptre | 1626 | ×42.10 | 8% | +0.12 | +0.12 |
| weapon.staff | 1609 | ×52.32 | 17% | +0.07 | +0.09 |
| weapon.spear | 1322 | ×52.00 | 18% | +0.08 | +0.07 |
| armour.focus | 1074 | ×40.12 | 8% | +0.12 | +0.13 |
| armour.quiver | 994 | ×31.41 | 11% | +0.08 | +0.11 |
| flask.charm | 865 | ×50.00 | 34% | +0.02 | +0.04 |
| armour.shield | 857 | ×15.35 | 15% | +0.01 | +0.01 |
| weapon.twomace | 785 | ×20.19 | 17% | +0.06 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=48044, R²=-0.8492

intercept: `-1.6760`  ·  log_price: True  ·  ilvl: `0.02996`  ·  n_mods: `0.53554`  ·  n_top_tier: `-0.14007`  ·  corrupted: `0.04804`  ·  quality: `0.23015`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.97434 |
| `explicit.stat_2301718443@T1` | 2.98863 |
| `explicit.stat_1697447343@T1` | -2.29606 |
| `explicit.stat_627767961@T1` | -2.17840 |
| `explicit.stat_3780644166@T1` | -2.11153 |
| `explicit.stat_3166958180@T1` | -1.94211 |
| `explicit.stat_795138349@T1` | -1.83851 |
| `explicit.stat_3473929743@T1` | -1.77906 |
| `explicit.stat_1697951953@T1` | -1.77293 |
| `explicit.stat_239367161@T1` | -1.77071 |
| `explicit.stat_234296660@T1` | -1.73122 |
| `explicit.stat_2523933828@T1` | -1.61792 |

### other — n=47172, R²=-0.4355

intercept: `1.6087`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00325`  ·  n_top_tier: `0.68982`  ·  corrupted: `0.68089`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.46465 |
| `explicit.stat_2974417149@T1` | 1.52471 |
| `explicit.stat_3141070085@T1` | -1.35170 |
| `explicit.stat_3917489142@T1` | 1.23942 |
| `explicit.stat_789117908@T1` | -0.92782 |
| `explicit.stat_2231156303@T1` | 0.76813 |
| `explicit.stat_1050105434@T1` | -0.60323 |
| `explicit.stat_2482852589@T1` | -0.40348 |
| `explicit.stat_736967255@T1` | -0.38081 |
| `explicit.stat_1589917703@T1` | 0.37271 |
| `explicit.stat_2106365538@T1` | -0.28715 |
| `explicit.stat_3299347043@T1` | -0.25752 |

### accessory.ring — n=44053, R²=-1.9719

intercept: `3.4460`  ·  log_price: True  ·  ilvl: `-0.04251`  ·  n_mods: `0.00145`  ·  n_top_tier: `0.44914`  ·  corrupted: `0.23142`  ·  n_sockets: `2.19728`  ·  quality: `0.07703`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -0.49185 |
| `explicit.stat_1573130764@T1` | -0.48952 |
| `explicit.stat_2144192055@T1` | -0.47220 |
| `explicit.stat_3325883026@T1` | -0.47136 |
| `explicit.stat_3962278098@T2` | -0.46948 |
| `explicit.stat_3291658075@T1` | -0.46900 |
| `explicit.stat_4220027924@T2` | -0.46854 |
| `explicit.stat_1368271171@T2` | -0.46772 |
| `explicit.stat_3291658075@T2` | -0.46705 |
| `explicit.stat_1263695895@T1` | -0.46430 |
| `explicit.stat_2231156303@T2` | -0.46398 |
| `explicit.stat_2891184298@T1` | -0.46238 |

### accessory.amulet — n=40825, R²=-2.1432

intercept: `3.8268`  ·  log_price: True  ·  ilvl: `-0.04659`  ·  n_mods: `-0.02181`  ·  n_top_tier: `1.03792`  ·  corrupted: `0.06328`  ·  n_sockets: `-0.12442`  ·  quality: `-0.00003`

| stat_id | coef |
|---|---|
| `explicit.stat_472520716@T2` | -1.09191 |
| `explicit.stat_2901986750@T1` | -1.09173 |
| `explicit.stat_472520716@T1` | -1.09067 |
| `explicit.stat_2748665614@T1` | -1.08802 |
| `explicit.stat_1050105434@T2` | -1.08446 |
| `explicit.stat_803737631@T1` | -1.08254 |
| `explicit.stat_3299347043@T1` | -1.08141 |
| `explicit.stat_3917489142@T2` | -1.07805 |
| `explicit.stat_2748665614@T2` | -1.07595 |
| `explicit.stat_803737631@T2` | -1.07377 |
| `explicit.stat_2974417149@T1` | -1.07214 |
| `explicit.stat_789117908@T2` | -1.07050 |

### accessory.belt — n=31609, R²=-0.188

intercept: `2.3030`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00005`  ·  n_top_tier: `0.40264`  ·  corrupted: `0.00010`  ·  n_sockets: `-0.69301`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -0.40270 |
| `explicit.stat_1389754388@T1` | -0.40269 |
| `explicit.stat_3299347043@T2` | -0.40267 |
| `explicit.stat_2923486259@T1` | -0.40266 |
| `explicit.stat_809229260@T1` | -0.40265 |
| `explicit.stat_2881298780@T1` | -0.40265 |
| `explicit.stat_51994685@T1` | -0.40265 |
| `explicit.stat_1389754388@T2` | -0.40265 |
| `explicit.stat_2923486259@T2` | -0.40265 |
| `explicit.stat_644456512@T1` | -0.40265 |
| `explicit.stat_1671376347@T2` | -0.40265 |
| `explicit.stat_4220027924@T2` | -0.40265 |

### armour.chest — n=31254, R²=-0.6687

intercept: `3.9089`  ·  log_price: True  ·  ilvl: `-0.03648`  ·  n_mods: `-0.13847`  ·  n_top_tier: `0.39481`  ·  corrupted: `0.30505`  ·  n_sockets: `0.12085`  ·  quality: `0.02371`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.49430 |
| `explicit.stat_4080418644@T1` | -0.83414 |
| `explicit.stat_2923486259@T1` | -0.82335 |
| `explicit.stat_3484657501@T1` | -0.76484 |
| `rune.stat_836936635` | -0.69227 |
| `explicit.stat_4080418644@T2` | -0.59122 |
| `explicit.stat_3261801346@T2` | -0.58111 |
| `explicit.stat_2881298780@T2` | -0.57932 |
| `explicit.stat_915769802@T2` | -0.54047 |
| `explicit.stat_2923486259@T2` | -0.53782 |
| `explicit.stat_124859000@T2` | -0.51073 |
| `explicit.stat_2451402625@T2` | -0.50207 |

### armour.helmet — n=30449, R²=-0.7059

intercept: `3.7887`  ·  log_price: True  ·  ilvl: `-0.04256`  ·  n_mods: `-0.14610`  ·  n_top_tier: `0.43543`  ·  corrupted: `0.62729`  ·  n_sockets: `0.16555`  ·  quality: `0.03518`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.79967 |
| `explicit.stat_53045048@T2` | -0.99172 |
| `explicit.stat_3917489142@T2` | -0.95524 |
| `explicit.stat_53045048@T1` | -0.69518 |
| `explicit.stat_1999113824@T1` | -0.68083 |
| `explicit.stat_3261801346@T1` | -0.67876 |
| `explicit.stat_3321629045@T2` | -0.67175 |
| `explicit.stat_1263695895@T2` | -0.64052 |
| `explicit.stat_587431675@T2` | -0.63624 |
| `explicit.stat_1263695895@T1` | -0.63469 |
| `explicit.stat_2162097452@T2` | -0.60789 |
| `explicit.stat_3261801346@T2` | -0.57292 |

### armour.boots — n=28587, R²=-1.1262

intercept: `4.4175`  ·  log_price: True  ·  ilvl: `-0.05151`  ·  n_mods: `-0.08860`  ·  n_top_tier: `0.66314`  ·  corrupted: `0.28388`  ·  n_sockets: `0.06544`  ·  quality: `0.02494`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.88159 |
| `explicit.stat_2250533757@T1` | 1.29891 |
| `explicit.stat_3917489142@T2` | -0.96540 |
| `explicit.stat_1062208444@T2` | -0.94506 |
| `explicit.stat_3299347043@T1` | -0.92506 |
| `explicit.stat_2923486259@T2` | -0.89466 |
| `explicit.stat_2160282525@T1` | -0.86914 |
| `explicit.stat_53045048@T1` | -0.86194 |
| `explicit.stat_3484657501@T2` | -0.85728 |
| `explicit.stat_1671376347@T2` | -0.84733 |
| `explicit.stat_328541901@T1` | -0.84149 |
| `explicit.stat_3917489142@T1` | -0.79429 |

### armour.gloves — n=27898, R²=-1.0397

intercept: `3.7657`  ·  log_price: True  ·  ilvl: `-0.04816`  ·  n_mods: `-0.07656`  ·  n_top_tier: `0.50896`  ·  corrupted: `0.08464`  ·  n_sockets: `0.23453`  ·  quality: `0.03710`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | -5.93151 |
| `explicit.stat_2339757871@T1` | 2.75469 |
| `explicit.stat_3484657501@T2` | -1.35750 |
| `rune.stat_836936635` | 1.07456 |
| `explicit.stat_803737631@T2` | -1.03054 |
| `explicit.stat_803737631@T1` | -0.98143 |
| `explicit.stat_3484657501@T1` | -0.87876 |
| `explicit.stat_3917489142@T2` | -0.85019 |
| `explicit.stat_1573130764@T1` | -0.84461 |
| `explicit.stat_3321629045@T2` | -0.82409 |
| `explicit.stat_9187492@T1` | 0.76743 |
| `explicit.stat_1999113824@T2` | -0.72384 |

### weapon.wand — n=18021, R²=-2.1993

intercept: `3.6054`  ·  log_price: True  ·  ilvl: `-0.04451`  ·  n_mods: `-0.01600`  ·  n_top_tier: `0.49688`  ·  corrupted: `0.00502`  ·  n_sockets: `0.03346`  ·  quality: `0.00155`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.18896 |
| `rune.stat_124131830` | -3.11385 |
| `explicit.stat_2254480358@T1` | 2.75803 |
| `explicit.stat_591105508@T1` | 1.80887 |
| `explicit.stat_4226189338@T1` | 1.80580 |
| `explicit.stat_124131830@T1` | 1.70127 |
| `explicit.stat_736967255@T2` | 1.31430 |
| `crafted.stat_124131830` | 1.13975 |
| `explicit.stat_2768835289@T2` | 0.95655 |
| `explicit.stat_2254480358@T2` | 0.84796 |
| `explicit.stat_4226189338@T2` | 0.63611 |
| `explicit.stat_737908626@T1` | -0.57623 |

### weapon.bow — n=14593, R²=-1.9579

intercept: `3.4154`  ·  log_price: True  ·  ilvl: `-0.04093`  ·  n_mods: `-0.04662`  ·  n_top_tier: `0.62357`  ·  corrupted: `-0.08998`  ·  n_sockets: `-0.00384`  ·  quality: `0.03150`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.03344 |
| `explicit.stat_1202301673@T1` | 1.53415 |
| `crafted.stat_3035140377` | 1.31976 |
| `explicit.stat_1263695895@T1` | -0.85403 |
| `explicit.stat_1263695895@T2` | -0.75548 |
| `explicit.stat_1509134228@T1` | -0.72269 |
| `explicit.stat_3695891184@T2` | -0.70325 |
| `desecrated.stat_666077204@T1` | -0.70112 |
| `explicit.stat_1368271171@T2` | -0.69694 |
| `explicit.stat_2694482655@T2` | -0.68477 |
| `explicit.stat_3695891184@T1` | -0.67778 |
| `explicit.stat_2463230181@T2` | -0.67711 |

### weapon.crossbow — n=13808, R²=-1.9091

intercept: `3.6038`  ·  log_price: True  ·  ilvl: `-0.04391`  ·  n_mods: `-0.02212`  ·  n_top_tier: `0.77026`  ·  corrupted: `0.07227`  ·  n_sockets: `0.03290`  ·  quality: `0.01040`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.98706 |
| `explicit.stat_2250681686@T2` | -1.47527 |
| `explicit.stat_709508406@T1` | 1.36353 |
| `explicit.stat_1202301673@T1` | 1.24060 |
| `explicit.stat_1980802737` | 1.15631 |
| `explicit.stat_1263695895@T2` | -0.97051 |
| `crafted.stat_3035140377` | 0.91317 |
| `explicit.stat_2694482655@T1` | -0.88847 |
| `explicit.stat_1202301673@T2` | -0.88516 |
| `explicit.stat_1263695895@T1` | -0.88196 |
| `explicit.stat_1509134228@T2` | -0.85009 |
| `explicit.stat_3695891184@T1` | -0.84307 |

### flask.charm — n=12264, R²=-0.522

intercept: `0.0026`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.80978`  ·  corrupted: `2.30242`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.16570 |
| `explicit.stat_1056492907` | 3.35295 |
| `explicit.stat_828533480@T2` | -2.80979 |
| `explicit.stat_2676834156@T2` | -2.80978 |
| `explicit.stat_1120862500@T2` | -2.80978 |
| `explicit.stat_2541588185@T2` | -2.80978 |
| `explicit.stat_3196823591@T2` | -2.80977 |
| `explicit.stat_828533480@T1` | -2.80977 |
| `explicit.stat_1873752457@T2` | -2.80977 |
| `explicit.stat_388617051@T2` | -2.80976 |
| `explicit.stat_1873752457@T1` | -2.80976 |
| `explicit.stat_1366840608@T2` | -2.80976 |

### weapon.warstaff — n=8290, R²=-0.515

intercept: `-4.6893`  ·  log_price: True  ·  ilvl: `0.06554`  ·  n_mods: `-0.14905`  ·  n_top_tier: `0.53384`  ·  corrupted: `0.20169`  ·  n_sockets: `0.07799`  ·  quality: `0.05392`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.61607 |
| `explicit.stat_1037193709@T1` | 1.24182 |
| `explicit.stat_328541901@T1` | -1.02835 |
| `explicit.stat_328541901@T2` | -0.92112 |
| `explicit.stat_55876295@T2` | -0.71972 |
| `crafted.stat_210067635@T2` | 0.71326 |
| `explicit.stat_1037193709@T2` | -0.66392 |
| `desecrated.stat_9187492` | 0.62776 |
| `explicit.stat_55876295@T1` | -0.62399 |
| `explicit.stat_791928121@T2` | -0.57764 |
| `explicit.stat_210067635@T1` | -0.56129 |
| `explicit.stat_691932474@T2` | -0.55089 |

### weapon.staff — n=7689, R²=-0.4978

intercept: `-8.4018`  ·  log_price: True  ·  ilvl: `0.10887`  ·  n_mods: `-0.09691`  ·  n_top_tier: `0.43471`  ·  corrupted: `0.02710`  ·  n_sockets: `0.20015`  ·  quality: `0.04803`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.62122 |
| `explicit.stat_4226189338@T1` | 1.53735 |
| `explicit.stat_1545858329@T1` | 1.26974 |
| `explicit.stat_1600707273@T1` | 1.11270 |
| `explicit.stat_2254480358@T1` | 0.92567 |
| `explicit.stat_2768835289@T2` | 0.91683 |
| `explicit.stat_4226189338@T2` | 0.74309 |
| `explicit.stat_124131830@T2` | 0.68746 |
| `explicit.stat_293638271@T2` | -0.67092 |
| `explicit.stat_1263695895@T2` | -0.61202 |
| `explicit.stat_2974417149@T1` | -0.55561 |
| `explicit.stat_1050105434@T2` | -0.54867 |

### weapon.sceptre — n=7661, R²=-0.435

intercept: `-13.8838`  ·  log_price: True  ·  ilvl: `0.17562`  ·  n_mods: `-0.04043`  ·  n_top_tier: `0.66525`  ·  corrupted: `0.47140`  ·  n_sockets: `0.24052`  ·  quality: `0.06942`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.99198 |
| `explicit.stat_2162097452@T2` | 1.13524 |
| `explicit.stat_1263695895@T2` | -1.10453 |
| `explicit.stat_4080418644@T1` | -1.04850 |
| `explicit.stat_1263695895@T1` | -1.00418 |
| `explicit.stat_1574590649@T2` | -0.98343 |
| `explicit.stat_289128254@T2` | -0.92852 |
| `explicit.stat_2347036682@T2` | -0.92749 |
| `explicit.stat_1050105434@T2` | -0.82347 |
| `explicit.stat_2854751904@T2` | -0.82162 |
| `explicit.stat_3984865854@T1` | -0.75546 |
| `explicit.stat_789117908@T2` | -0.70298 |

### weapon.spear — n=6358, R²=-0.5695

intercept: `-6.5743`  ·  log_price: True  ·  ilvl: `0.08848`  ·  n_mods: `-0.03561`  ·  n_top_tier: `0.70363`  ·  corrupted: `-0.14312`  ·  n_sockets: `0.18463`  ·  quality: `0.10466`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -2.92807 |
| `explicit.stat_9187492@T1` | 1.94702 |
| `explicit.stat_1202301673@T1` | 1.93729 |
| `desecrated.stat_210067635@T1` | -1.11419 |
| `crafted.stat_3035140377` | 1.04603 |
| `explicit.stat_1509134228@T1` | 1.04034 |
| `explicit.stat_1263695895@T2` | -0.97911 |
| `explicit.stat_55876295@T1` | -0.89077 |
| `explicit.stat_1037193709@T1` | -0.80774 |
| `explicit.stat_55876295@T2` | -0.79600 |
| `explicit.stat_1940865751@T2` | -0.70301 |
| `explicit.stat_3261801346@T2` | -0.70295 |

### armour.focus — n=5191, R²=-0.4495

intercept: `-10.4995`  ·  log_price: True  ·  ilvl: `0.13221`  ·  n_mods: `-0.07916`  ·  n_top_tier: `0.95042`  ·  corrupted: `0.64217`  ·  n_sockets: `0.44178`  ·  quality: `0.07074`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 7.12797 |
| `crafted.stat_737908626@T2` | -2.88555 |
| `crafted.stat_2974417149@T1` | 1.76414 |
| `explicit.stat_4220027924@T2` | -1.27824 |
| `explicit.stat_3962278098@T2` | -1.22754 |
| `explicit.stat_3291658075@T1` | -1.20131 |
| `explicit.stat_3962278098@T1` | -1.18418 |
| `explicit.stat_2923486259@T1` | -1.08568 |
| `explicit.stat_2339757871@T2` | -1.03197 |
| `explicit.stat_2231156303@T2` | -0.99384 |
| `explicit.stat_2339757871@T1` | -0.97665 |
| `explicit.stat_737908626@T2` | -0.97527 |

### armour.quiver — n=4838, R²=-0.3995

intercept: `-9.9704`  ·  log_price: True  ·  ilvl: `0.12499`  ·  n_mods: `-0.08001`  ·  n_top_tier: `0.81340`  ·  corrupted: `0.47118`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 7.18020 |
| `explicit.stat_2463230181@T1` | 2.00996 |
| `explicit.stat_2321178454@T2` | -1.30569 |
| `explicit.stat_4067062424@T1` | -1.15012 |
| `explicit.stat_681332047@T2` | -1.07929 |
| `explicit.stat_1573130764@T2` | -0.98829 |
| `explicit.stat_803737631@T2` | -0.98454 |
| `explicit.stat_2463230181@T2` | 0.98203 |
| `explicit.stat_1573130764@T1` | -0.94584 |
| `explicit.stat_3261801346@T1` | -0.92704 |
| `explicit.stat_2321178454@T1` | -0.83611 |
| `explicit.stat_803737631@T1` | -0.81389 |

### armour.shield — n=4255, R²=-0.5659

intercept: `-7.4316`  ·  log_price: True  ·  ilvl: `0.09653`  ·  n_mods: `-0.04565`  ·  n_top_tier: `0.42720`  ·  corrupted: `0.01313`  ·  n_sockets: `0.12133`  ·  quality: `0.05767`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.06102 |
| `explicit.stat_1011760251@T1` | -0.90713 |
| `explicit.stat_3676141501@T1` | 0.86273 |
| `explicit.stat_2339757871@T1` | -0.79362 |
| `explicit.stat_2923486259@T2` | -0.76535 |
| `explicit.stat_328541901@T1` | -0.75295 |
| `explicit.stat_1011760251@T2` | -0.74203 |
| `explicit.stat_1978899297@T2` | -0.73599 |
| `explicit.stat_2481353198@T2` | -0.70249 |
| `explicit.stat_2481353198@T1` | -0.66341 |
| `explicit.stat_2881298780@T1` | -0.65633 |
| `explicit.stat_1978899297@T1` | 0.65442 |

### weapon.twomace — n=3911, R²=-0.5122

intercept: `-9.1722`  ·  log_price: True  ·  ilvl: `0.12084`  ·  n_mods: `-0.12215`  ·  n_top_tier: `0.55812`  ·  corrupted: `0.68514`  ·  n_sockets: `0.14929`  ·  quality: `0.03616`

| stat_id | coef |
|---|---|
| `desecrated.stat_1509134228@T1` | 2.13479 |
| `desecrated.stat_210067635@T1` | -2.01650 |
| `explicit.stat_1037193709@T1` | -1.76044 |
| `explicit.stat_3336890334@T1` | -1.44453 |
| `crafted.stat_3035140377` | 1.11109 |
| `explicit.stat_518292764@T2` | -1.01955 |
| `explicit.stat_1037193709@T2` | -0.98308 |
| `explicit.stat_387439868@T2` | -0.97225 |
| `explicit.stat_1263695895@T2` | -0.85771 |
| `explicit.stat_3695891184@T1` | -0.79093 |
| `explicit.stat_1263695895@T1` | -0.78995 |
| `explicit.stat_3639275092@T1` | -0.76062 |

## Coverage (listings per base)

- … **Sapphire** — 22419 listings (22389 priced) [0.3–7553463.8 ex]
- … **Emerald** — 22077 listings (22049 priced) [0.3–7553463.8 ex]
- … **Ruby** — 16919 listings (16905 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 9227 listings (9218 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 7535 listings (7525 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 7376 listings (7363 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 7237 listings (7230 priced) [0.2–19945827.9 ex]
- … **Gold Amulet** — 6904 listings (6894 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 6866 listings (6862 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 6749 listings (6737 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5737 listings (5722 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5636 listings (5630 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 5422 listings (5417 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5401 listings (5398 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 4903 listings (4889 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4843 listings (4838 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4716 listings (4709 priced) [0.6–3985176410.3 ex]
- … **Amber Amulet** — 4699 listings (4696 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4687 listings (4681 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4660 listings (4653 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4529 listings (4524 priced) [0.3–4275054.0 ex]
- … **Heavy Belt** — 4388 listings (4385 priced) [0.3–2608914286.6 ex]
- … **Obliterator Bow** — 4376 listings (4363 priced) [0.3–42622633798.0 ex]
- … **Pearl Ring** — 4363 listings (4357 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 4286 listings (4286 priced) [0.3–123132003.2 ex]

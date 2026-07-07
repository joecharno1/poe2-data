# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-07T21:28:52+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **296677** (296328 priced in exalted)
- Distinct bases: 951 · distinct mods: 2786 · mod rows: 1408871
- Sold signals: **31535** sold · 158507 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-07T21:15:25+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×19.04** (median |log error| 2.9467)
- Within ±30% of asking price: **9%**
- Skill vs constant-price guess: **-0.02** (> 0 = the mods carry signal)
- Calibration: 76% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.01** · typical error ×29.50 · ±30% 8% · n=42692
- Premium segment (60ex+): skill **+0.09** · typical error ×102.22 · ±30% 1% · n=26409

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 5599 | ×19.92 | 5% | -0.04 | -0.01 |
| accessory.amulet | 5323 | ×20.61 | 5% | -0.08 | -0.04 |
| jewel | 4844 | ×14.11 | 7% | -0.08 | -0.03 |
| accessory.belt | 4352 | ×27.49 | 4% | -0.01 | +0.03 |
| armour.chest | 4270 | ×12.97 | 6% | -0.03 | +0.01 |
| armour.helmet | 4133 | ×13.07 | 6% | -0.03 | -0.00 |
| armour.boots | 3935 | ×28.40 | 5% | +0.01 | +0.05 |
| armour.gloves | 3827 | ×15.16 | 6% | -0.05 | -0.03 |
| other | 3572 | ×10.00 | 35% | +0.11 | +0.39 |
| weapon.wand | 2660 | ×17.09 | 5% | +0.06 | +0.01 |
| weapon.bow | 2159 | ×15.05 | 6% | -0.04 | +0.01 |
| weapon.crossbow | 2011 | ×10.17 | 7% | -0.03 | +0.01 |
| weapon.warstaff | 945 | ×78.63 | 18% | +0.02 | +0.02 |
| weapon.staff | 882 | ×50.00 | 19% | +0.04 | +0.06 |
| weapon.sceptre | 828 | ×57.00 | 14% | +0.07 | +0.05 |
| weapon.spear | 687 | ×40.00 | 21% | +0.02 | +0.03 |
| armour.focus | 615 | ×392.01 | 11% | +0.02 | +0.05 |
| armour.quiver | 592 | ×79.85 | 13% | +0.00 | +0.04 |
| armour.shield | 482 | ×40.00 | 18% | +0.02 | +0.03 |
| weapon.twomace | 438 | ×27.63 | 14% | +0.04 | +0.04 |
| flask.charm | 368 | ×2.13 | 47% | -0.00 | +0.02 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=31190, R²=-0.4006

intercept: `1.6031`  ·  log_price: True  ·  ilvl: `0.00009`  ·  n_mods: `0.11086`  ·  n_top_tier: `1.17695`  ·  corrupted: `2.38722`  ·  n_sockets: `-0.00022`  ·  quality: `-0.00002`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 2.86122 |
| `explicit.stat_2891184298@T1` | 2.61826 |
| `explicit.stat_1050105434@T1` | -2.61276 |
| `explicit.stat_101878827@T1` | 2.34236 |
| `explicit.stat_1589917703@T1` | 2.33972 |
| `explicit.stat_3141070085@T1` | 2.29106 |
| `explicit.stat_2106365538@T1` | 2.10447 |
| `explicit.stat_3917489142@T1` | 2.10104 |
| `explicit.stat_789117908@T1` | -1.77623 |
| `explicit.stat_2974417149@T1` | 1.32974 |
| `implicit.stat_3182714256` | 0.33298 |
| `implicit.stat_718638445` | 0.33296 |

### jewel — n=26155, R²=-0.4167

intercept: `-0.1220`  ·  log_price: True  ·  ilvl: `0.03243`  ·  n_mods: `0.28784`  ·  n_top_tier: `0.04492`  ·  corrupted: `1.46479`  ·  quality: `0.11829`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -8.76294 |
| `explicit.stat_3824372849@T1` | -6.97993 |
| `explicit.stat_2301718443@T1` | -6.81671 |
| `explicit.stat_21071013@T1` | 6.06616 |
| `explicit.stat_2456523742@T1` | 5.95101 |
| `explicit.stat_2523933828@T1` | 4.90498 |
| `explicit.stat_924253255@T1` | 4.85174 |
| `explicit.stat_3028809864@T1` | -4.80380 |
| `explicit.stat_1459321413@T1` | 4.80221 |
| `explicit.stat_3473929743@T1` | -4.41844 |
| `explicit.stat_3741323227@T1` | -4.31415 |
| `explicit.stat_491450213@T1` | -4.29593 |

### accessory.ring — n=25668, R²=-0.6848

intercept: `-8.5712`  ·  log_price: True  ·  ilvl: `0.12750`  ·  n_mods: `0.04551`  ·  n_top_tier: `0.01280`  ·  corrupted: `1.10593`  ·  n_sockets: `0.43379`  ·  quality: `0.01448`

| stat_id | coef |
|---|---|
| `explicit.stat_2557965901@T1` | -6.91048 |
| `explicit.stat_2557965901@T2` | -5.76577 |
| `explicit.stat_1263695895@T1` | 2.00944 |
| `explicit.stat_1263695895@T2` | 1.37330 |
| `explicit.stat_736967255@T1` | -1.32449 |
| `explicit.stat_736967255@T2` | -1.15817 |
| `explicit.stat_4220027924@T1` | -0.99866 |
| `explicit.stat_707457662@T1` | 0.97769 |
| `explicit.stat_2557965901` | 0.88456 |
| `explicit.stat_707457662@T2` | 0.86147 |
| `explicit.stat_3372524247@T1` | -0.84554 |
| `explicit.stat_1573130764@T1` | 0.76847 |

### accessory.amulet — n=24303, R²=-0.4567

intercept: `4.1505`  ·  log_price: True  ·  ilvl: `-0.02085`  ·  n_mods: `-0.08092`  ·  n_top_tier: `0.22100`  ·  corrupted: `0.63872`  ·  n_sockets: `3.72807`  ·  quality: `-0.00318`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -3.74772 |
| `explicit.stat_983749596@T2` | -3.15321 |
| `explicit.stat_2748665614@T1` | 2.98515 |
| `explicit.stat_587431675@T1` | -2.94549 |
| `explicit.stat_1379411836@T1` | -1.32892 |
| `explicit.stat_124131830@T2` | 1.27723 |
| `explicit.stat_3325883026@T1` | -1.17212 |
| `explicit.stat_3261801346@T1` | -1.15962 |
| `explicit.stat_587431675@T2` | -1.07031 |
| `explicit.stat_2106365538@T1` | -1.03930 |
| `explicit.stat_1050105434@T1` | -1.02157 |
| `explicit.stat_472520716@T2` | -1.00552 |

### accessory.belt — n=19961, R²=-0.8833

intercept: `-9.6884`  ·  log_price: True  ·  ilvl: `0.14893`  ·  n_mods: `-0.17340`  ·  n_top_tier: `1.35327`  ·  corrupted: `0.66819`  ·  n_sockets: `0.32653`

| stat_id | coef |
|---|---|
| `explicit.stat_51994685@T2` | -2.16720 |
| `explicit.stat_1412217137@T1` | -1.97838 |
| `explicit.stat_1412217137@T2` | -1.92903 |
| `explicit.stat_915769802@T2` | -1.85339 |
| `explicit.stat_915769802@T1` | -1.81000 |
| `explicit.stat_51994685@T1` | -1.72535 |
| `explicit.stat_2881298780@T1` | -1.53442 |
| `explicit.stat_4220027924@T2` | -1.51602 |
| `explicit.stat_809229260@T2` | -1.51240 |
| `explicit.stat_3299347043@T2` | -1.50048 |
| `explicit.stat_1836676211@T1` | -1.45064 |
| `explicit.stat_1836676211@T2` | -1.44691 |

### armour.chest — n=19716, R²=-0.4396

intercept: `3.0199`  ·  log_price: True  ·  ilvl: `-0.01663`  ·  n_mods: `-0.15162`  ·  n_top_tier: `0.09536`  ·  corrupted: `0.27106`  ·  n_sockets: `0.14031`  ·  quality: `0.01700`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | -2.16426 |
| `implicit.stat_2251279027` | 1.08234 |
| `implicit.stat_1978899297` | 1.00175 |
| `explicit.stat_2339757871@T1` | 0.91856 |
| `explicit.stat_4080418644@T1` | -0.90784 |
| `explicit.stat_3981240776@T1` | -0.81048 |
| `explicit.stat_3033371881@T1` | 0.71495 |
| `explicit.stat_915769802@T1` | -0.64195 |
| `explicit.stat_2923486259@T2` | 0.63040 |
| `explicit.stat_53045048@T1` | 0.56530 |
| `explicit.stat_328541901@T2` | 0.49981 |
| `explicit.stat_124859000@T2` | -0.49910 |

### armour.helmet — n=19318, R²=-0.4302

intercept: `3.3563`  ·  log_price: True  ·  ilvl: `-0.01623`  ·  n_mods: `-0.22644`  ·  n_top_tier: `0.42375`  ·  corrupted: `0.71261`  ·  n_sockets: `-0.14329`  ·  quality: `0.06588`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 10.07968 |
| `explicit.stat_2339757871@T1` | -3.24635 |
| `explicit.stat_3362812763@T1` | -2.03962 |
| `explicit.stat_3362812763@T2` | -1.80925 |
| `explicit.stat_2451402625@T1` | -1.14145 |
| `explicit.stat_4080418644@T2` | -1.04707 |
| `explicit.stat_4080418644@T1` | -0.98491 |
| `explicit.stat_3261801346@T2` | -0.95337 |
| `explicit.stat_3484657501@T2` | -0.92553 |
| `explicit.stat_3033371881@T2` | -0.90313 |
| `explicit.stat_4052037485@T1` | -0.89064 |
| `explicit.stat_1263695895@T1` | 0.78456 |

### armour.boots — n=18260, R²=-0.4939

intercept: `1.0226`  ·  log_price: True  ·  ilvl: `0.00733`  ·  n_mods: `-0.15816`  ·  n_top_tier: `0.09685`  ·  corrupted: `0.96332`  ·  n_sockets: `-0.04276`  ·  quality: `0.03393`

| stat_id | coef |
|---|---|
| `desecrated.stat_2250533757@T2` | -1.22601 |
| `explicit.stat_1062208444@T2` | -1.04548 |
| `explicit.stat_4080418644@T1` | -0.97176 |
| `explicit.stat_1671376347@T1` | 0.88833 |
| `explicit.stat_53045048@T2` | 0.87437 |
| `explicit.stat_3917489142@T1` | -0.84316 |
| `explicit.stat_99927264@T2` | -0.78721 |
| `explicit.stat_3372524247@T1` | 0.77931 |
| `explicit.stat_2339757871@T1` | 0.73010 |
| `explicit.stat_124859000@T2` | -0.72299 |
| `explicit.stat_3484657501@T2` | 0.69820 |
| `explicit.stat_4015621042@T2` | -0.68513 |

### armour.gloves — n=17819, R²=-0.4547

intercept: `1.8545`  ·  log_price: True  ·  ilvl: `-0.00957`  ·  n_mods: `-0.01999`  ·  n_top_tier: `-0.29818`  ·  corrupted: `1.26852`  ·  n_sockets: `0.12474`  ·  quality: `0.02267`

| stat_id | coef |
|---|---|
| `explicit.stat_681332047@T1` | 2.18256 |
| `explicit.stat_2339757871@T1` | -2.04281 |
| `explicit.stat_3321629045@T1` | 1.67352 |
| `explicit.stat_2797971005@T1` | 1.66641 |
| `explicit.stat_3033371881@T1` | -1.51664 |
| `explicit.stat_4067062424@T2` | 1.45014 |
| `explicit.stat_681332047@T2` | 1.32785 |
| `explicit.stat_3556824919@T1` | 1.29009 |
| `explicit.stat_3917489142@T2` | -1.21697 |
| `explicit.stat_53045048@T1` | -1.20867 |
| `explicit.stat_3032590688@T1` | 1.17128 |
| `explicit.stat_3033371881@T2` | -1.07420 |

### weapon.wand — n=12321, R²=-0.6462

intercept: `2.9126`  ·  log_price: True  ·  ilvl: `-0.00919`  ·  n_mods: `-0.20714`  ·  n_top_tier: `0.85097`  ·  corrupted: `0.28437`  ·  n_sockets: `0.29670`  ·  quality: `0.04571`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T2` | -1.61687 |
| `explicit.stat_3695891184@T1` | -1.52791 |
| `explicit.stat_473429811@T2` | -1.52776 |
| `explicit.stat_328541901@T1` | -1.50151 |
| `explicit.stat_3695891184@T2` | -1.47306 |
| `explicit.stat_737908626@T1` | -1.40173 |
| `explicit.stat_1600707273@T1` | 1.33932 |
| `explicit.stat_2891184298@T2` | -1.31101 |
| `explicit.stat_2891184298@T1` | -1.23253 |
| `explicit.stat_1368271171@T1` | -1.20539 |
| `explicit.stat_1368271171@T2` | -1.18361 |
| `explicit.stat_1545858329@T1` | 1.08584 |

### weapon.bow — n=10056, R²=-0.7474

intercept: `2.8575`  ·  log_price: True  ·  ilvl: `-0.01852`  ·  n_mods: `-0.15755`  ·  n_top_tier: `0.48549`  ·  corrupted: `1.12897`  ·  n_sockets: `0.00157`  ·  quality: `0.02433`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -4.78528 |
| `explicit.stat_2463230181@T2` | -1.74860 |
| `explicit.stat_1037193709@T1` | -1.56837 |
| `rune.stat_3885405204` | 1.40574 |
| `explicit.stat_3695891184@T1` | -1.37183 |
| `explicit.stat_518292764@T2` | -1.26302 |
| `explicit.stat_1509134228@T1` | -1.21767 |
| `explicit.stat_709508406@T1` | 1.21064 |
| `explicit.stat_3695891184@T2` | -1.15603 |
| `crafted.stat_3035140377` | 1.15330 |
| `explicit.stat_1368271171@T1` | -1.13750 |
| `explicit.stat_1940865751@T2` | -1.13485 |

### weapon.crossbow — n=9498, R²=-0.7329

intercept: `1.4663`  ·  log_price: True  ·  ilvl: `-0.00425`  ·  n_mods: `0.06454`  ·  n_top_tier: `1.05050`  ·  corrupted: `-0.56022`  ·  n_sockets: `0.50875`  ·  quality: `0.00452`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | 2.07556 |
| `explicit.stat_1037193709@T2` | -1.82225 |
| `explicit.stat_1037193709@T1` | -1.68497 |
| `explicit.stat_1544773869@T2` | -1.53284 |
| `explicit.stat_691932474@T1` | -1.41749 |
| `explicit.stat_1202301673@T2` | -1.35807 |
| `explicit.stat_1509134228@T1` | -1.35366 |
| `explicit.stat_1368271171@T1` | -1.34274 |
| `explicit.stat_387439868@T1` | -1.27059 |
| `explicit.stat_4080418644@T2` | -1.19553 |
| `explicit.stat_1509134228@T2` | -1.14353 |
| `explicit.stat_3261801346@T1` | -1.14009 |

### flask.charm — n=6153, R²=-0.3157

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.01755`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.76966 |
| `explicit.stat_1056492907` | 2.99578 |
| `explicit.stat_2676834156@T1` | 1.60936 |
| `explicit.stat_3138344128` | 0.02221 |
| `explicit.stat_2541588185@T1` | 0.01241 |
| `explicit.stat_2678930256` | 0.00007 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_1873752457@T1` | -0.00004 |
| `explicit.stat_828533480@T1` | -0.00003 |
| `explicit.stat_1120862500@T2` | -0.00003 |
| `explicit.stat_3246948616` | 0.00003 |
| `explicit.stat_3196823591@T2` | -0.00003 |

### weapon.warstaff — n=4421, R²=-0.511

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00001`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00003`  ·  n_sockets: `0.00001`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | -3.87451 |
| `desecrated.stat_2527686725@T1` | -3.87451 |
| `rune.stat_243313994` | 3.18676 |
| `rune.stat_731403740` | 1.53282 |
| `rune.stat_1712188793` | -1.00409 |
| `desecrated.stat_9187492` | 0.80159 |
| `desecrated.stat_2527686725` | 0.25055 |
| `explicit.stat_9187492@T1` | 0.20602 |
| `crafted.stat_210067635@T2` | 0.10579 |
| `rune.stat_3336890334` | 0.10179 |
| `desecrated.stat_669069897` | -0.08813 |
| `rune.stat_1509134228` | 0.06674 |

### weapon.staff — n=4123, R²=-0.5553

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00006`  ·  n_sockets: `0.00001`  ·  quality: `0.00044`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.63686 |
| `explicit.stat_1600707273@T1` | 0.70035 |
| `explicit.stat_2254480358@T1` | 0.69301 |
| `explicit.stat_4226189338@T1` | 0.35382 |
| `crafted.stat_124131830` | 0.32187 |
| `rune.stat_3990135792` | -0.20205 |
| `rune.stat_975988108` | -0.12292 |
| `rune.stat_2974417149` | 0.10749 |
| `explicit.stat_2254480358@T2` | 0.08187 |
| `explicit.stat_473429811@T1` | 0.07058 |
| `desecrated.stat_2974417149` | 0.01819 |
| `explicit.stat_124131830@T1` | 0.00588 |

### weapon.sceptre — n=4107, R²=-0.5325

intercept: `-0.0010`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.37185`  ·  corrupted: `1.62236`  ·  n_sockets: `0.00001`  ·  quality: `0.07480`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.93065 |
| `explicit.stat_4080418644@T2` | -0.37187 |
| `explicit.stat_2347036682@T2` | -0.37187 |
| `explicit.stat_4080418644@T1` | -0.37187 |
| `explicit.stat_1250712710@T1` | -0.37186 |
| `explicit.stat_2347036682@T1` | -0.37186 |
| `explicit.stat_3984865854@T2` | -0.37186 |
| `explicit.stat_2854751904@T1` | -0.37185 |
| `explicit.stat_1574590649@T1` | -0.37185 |
| `explicit.stat_3639275092@T2` | -0.37185 |
| `explicit.stat_328541901@T1` | -0.37185 |
| `explicit.stat_770672621@T1` | -0.37185 |

### weapon.spear — n=3573, R²=-0.5533

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00004`  ·  corrupted: `-0.00003`  ·  n_sockets: `0.00001`  ·  quality: `0.00024`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.68849 |
| `crafted.stat_518292764` | 0.80901 |
| `explicit.stat_210067635@T1` | 0.69320 |
| `explicit.stat_1202301673@T1` | 0.38017 |
| `rune.stat_1039491398` | 0.14123 |
| `rune.stat_1509134228` | -0.06778 |
| `explicit.stat_1509134228@T1` | 0.01023 |
| `crafted.stat_210067635` | 0.00946 |
| `desecrated.stat_1509134228` | 0.00394 |
| `desecrated.stat_691932474` | -0.00063 |
| `explicit.stat_3336890334@T1` | 0.00014 |
| `explicit.stat_709508406@T1` | 0.00008 |

### armour.focus — n=2922, R²=-0.5932

intercept: `-0.0007`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.18812`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00002`  ·  quality: `0.02120`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -6.70355 |
| `crafted.stat_737908626@T2` | -3.59388 |
| `desecrated.stat_378817135@T1` | -1.48116 |
| `crafted.stat_2974417149@T1` | 0.83753 |
| `desecrated.stat_3393628375` | 0.47731 |
| `explicit.stat_2891184298@T2` | -0.18815 |
| `explicit.stat_736967255@T2` | -0.18814 |
| `explicit.stat_3291658075@T1` | -0.18814 |
| `explicit.stat_789117908@T2` | -0.18814 |
| `explicit.stat_2923486259@T1` | -0.18813 |
| `explicit.stat_4052037485@T2` | -0.18813 |
| `explicit.stat_2891184298@T1` | -0.18813 |

### armour.quiver — n=2725, R²=-0.6068

intercept: `-0.0008`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.08934`  ·  corrupted: `0.00002`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.69719 |
| `explicit.stat_3759663284@T1` | 0.60366 |
| `desecrated.stat_3714003708` | 0.10502 |
| `explicit.stat_2463230181@T2` | -0.09110 |
| `explicit.stat_681332047@T2` | -0.08941 |
| `explicit.stat_681332047@T1` | -0.08940 |
| `explicit.stat_1573130764@T1` | -0.08937 |
| `explicit.stat_1368271171@T2` | -0.08937 |
| `explicit.stat_2321178454@T2` | -0.08937 |
| `explicit.stat_3714003708@T2` | -0.08936 |
| `explicit.stat_2194114101@T2` | -0.08936 |
| `explicit.stat_1573130764@T2` | -0.08936 |

### armour.shield — n=2370, R²=-0.4525

intercept: `-0.0007`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.27244`  ·  corrupted: `0.00935`  ·  n_sockets: `0.00001`  ·  quality: `0.06862`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.78041 |
| `explicit.stat_1978899297@T2` | -0.43917 |
| `explicit.stat_1011760251@T1` | -0.28069 |
| `explicit.stat_1011760251@T2` | -0.27793 |
| `explicit.stat_2481353198@T1` | -0.27250 |
| `explicit.stat_328541901@T1` | -0.27249 |
| `explicit.stat_2339757871@T1` | -0.27249 |
| `explicit.stat_2481353198@T2` | -0.27249 |
| `explicit.stat_328541901@T2` | -0.27247 |
| `explicit.stat_3372524247@T2` | -0.27246 |
| `explicit.stat_1062208444@T2` | -0.27246 |
| `explicit.stat_3484657501@T1` | -0.27245 |

### weapon.twomace — n=2057, R²=-0.509

intercept: `-0.0007`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.35384`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_709508406` | 0.66339 |
| `explicit.stat_1509134228@T1` | 0.45750 |
| `explicit.stat_3336890334@T1` | -0.35414 |
| `explicit.stat_1037193709@T1` | -0.35389 |
| `explicit.stat_1037193709@T2` | -0.35387 |
| `explicit.stat_3336890334@T2` | -0.35387 |
| `explicit.stat_387439868@T2` | -0.35387 |
| `explicit.stat_821021828@T1` | -0.35387 |
| `explicit.stat_1940865751@T1` | -0.35387 |
| `explicit.stat_9187492@T1` | -0.35386 |
| `explicit.stat_55876295@T2` | -0.35386 |
| `explicit.stat_669069897@T1` | -0.35386 |

## Coverage (listings per base)

- … **Emerald** — 12450 listings (12442 priced) [0.6–7553463.8 ex]
- … **Sapphire** — 12445 listings (12429 priced) [0.3–7553463.8 ex]
- … **Ruby** — 9643 listings (9633 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 5937 listings (5933 priced) [0.2–5288620.9 ex]
- … **Prismatic Ring** — 4498 listings (4496 priced) [0.3–24532814.5 ex]
- … **Stellar Amulet** — 4434 listings (4434 priced) [0.2–35690283.3 ex]
- … **Solar Amulet** — 4397 listings (4391 priced) [0.3–66666666.0 ex]
- … **Amethyst Ring** — 4250 listings (4249 priced) [0.3–71450.3 ex]
- … **Gold Amulet** — 4199 listings (4196 priced) [0.2–4894457.0 ex]
- … **Gold Ring** — 4060 listings (4058 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 3879 listings (3874 priced) [0.3–3736768402.2 ex]
- … **Sapphire Ring** — 3396 listings (3392 priced) [0.3–24532814.5 ex]
- … **Topaz Ring** — 3291 listings (3290 priced) [0.3–123132003.2 ex]
- … **Ruby Ring** — 3290 listings (3290 priced) [0.3–37474957.5 ex]
- … **Plate Belt** — 3020 listings (3017 priced) [0.3–5286174.1 ex]
- … **Obliterator Bow** — 2943 listings (2936 priced) [0.5–22139622146.9 ex]
- … **Ancestral Tiara** — 2915 listings (2913 priced) [0.6–41469259.3 ex]
- … **Lapis Amulet** — 2908 listings (2908 priced) [0.3–5286174.1 ex]
- … **Amber Amulet** — 2887 listings (2886 priced) [0.2–124352753.2 ex]
- … **Jade Amulet** — 2879 listings (2878 priced) [0.2–4547453.5 ex]
- … **Heavy Belt** — 2842 listings (2842 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 2747 listings (2747 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 2706 listings (2706 priced) [0.3–14638.0 ex]
- … **Pearl Ring** — 2627 listings (2627 priced) [0.3–24532814.5 ex]
- … **Azure Amulet** — 2557 listings (2557 priced) [0.2–123132003.2 ex]

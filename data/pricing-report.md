# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-18T01:39:05+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **600946** (599187 priced in exalted)
- Distinct bases: 990 · distinct mods: 3220 · mod rows: 2846797
- Sold signals: **25141** sold · 341197 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-18T01:26:45+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.84** (median |log error| 3.2126)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×67.75 · ±30% 5% · n=87448
- Premium segment (60ex+): skill **+0.13** · typical error ×327.83 · ±30% 0% · n=59345

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 12450 | ×55.05 | 21% | +0.03 | +0.05 |
| jewel | 11704 | ×10.69 | 4% | +0.08 | +0.11 |
| accessory.amulet | 11382 | ×47.25 | 20% | +0.03 | +0.03 |
| accessory.belt | 8363 | ×23.90 | 12% | +0.08 | +0.11 |
| armour.chest | 8111 | ×18.33 | 24% | +0.07 | +0.10 |
| armour.helmet | 7941 | ×24.74 | 18% | +0.07 | +0.10 |
| armour.boots | 7332 | ×35.82 | 21% | +0.08 | +0.11 |
| armour.gloves | 7188 | ×40.68 | 16% | +0.07 | +0.10 |
| other | 7019 | ×2.00 | 43% | +0.10 | +0.18 |
| weapon.wand | 4402 | ×50.89 | 15% | +0.09 | +0.11 |
| weapon.bow | 3467 | ×30.58 | 14% | +0.13 | +0.15 |
| weapon.crossbow | 3252 | ×34.91 | 16% | +0.09 | +0.14 |
| weapon.warstaff | 2111 | ×32.06 | 6% | +0.17 | +0.15 |
| weapon.staff | 1996 | ×47.32 | 6% | +0.13 | +0.12 |
| weapon.sceptre | 1952 | ×34.67 | 5% | +0.19 | +0.19 |
| weapon.spear | 1574 | ×39.33 | 12% | +0.09 | +0.09 |
| armour.focus | 1320 | ×24.89 | 6% | +0.16 | +0.17 |
| armour.quiver | 1254 | ×23.94 | 7% | +0.15 | +0.15 |
| flask.charm | 1072 | ×16.62 | 32% | +0.02 | +0.04 |
| armour.shield | 1035 | ×21.57 | 7% | +0.05 | +0.08 |
| weapon.twomace | 924 | ×12.47 | 10% | +0.09 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=63696, R²=-0.9548

intercept: `-1.9075`  ·  log_price: True  ·  ilvl: `0.02580`  ·  n_mods: `0.87026`  ·  n_top_tier: `-0.33373`  ·  corrupted: `0.26384`  ·  quality: `0.22891`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.52212 |
| `explicit.stat_2301718443@T1` | 2.23508 |
| `explicit.stat_3374165039@T1` | -2.13746 |
| `explicit.stat_3485067555@T1` | 1.90156 |
| `explicit.stat_1805182458@T1` | -1.81755 |
| `explicit.stat_2523933828@T1` | -1.58716 |
| `explicit.stat_318953428@T1` | -1.47913 |
| `explicit.stat_3787460122@T1` | 1.41785 |
| `explicit.stat_1062710370@T1` | -1.40710 |
| `explicit.stat_3166958180@T1` | -1.40346 |
| `explicit.stat_239367161@T1` | -1.32733 |
| `explicit.stat_3174700878@T1` | 1.32245 |

### other — n=57584, R²=-0.6144

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.37693`  ·  corrupted: `0.31446`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | 1.38690 |
| `explicit.stat_2974417149@T1` | 0.37645 |
| `explicit.stat_1050105434@T1` | -0.37401 |
| `explicit.stat_2106365538@T1` | -0.36238 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_3291658075@T1` | 0.22048 |
| `explicit.stat_3141070085@T1` | -0.18151 |
| `explicit.stat_789117908@T1` | -0.13128 |
| `explicit.stat_2482852589@T1` | -0.12512 |
| `explicit.stat_736967255@T1` | 0.09510 |

### accessory.ring — n=56981, R²=-2.0436

intercept: `3.5219`  ·  log_price: True  ·  ilvl: `-0.04362`  ·  n_mods: `0.00212`  ·  n_top_tier: `1.02384`  ·  corrupted: `0.01966`  ·  n_sockets: `-0.20320`  ·  quality: `0.02039`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.07212 |
| `explicit.stat_2231156303@T1` | -1.06914 |
| `explicit.stat_1573130764@T2` | -1.06185 |
| `explicit.stat_2231156303@T2` | -1.04604 |
| `explicit.stat_4220027924@T2` | -1.04432 |
| `explicit.stat_1368271171@T2` | -1.04014 |
| `explicit.stat_3032590688@T2` | -1.03945 |
| `explicit.stat_2144192055@T1` | -1.03877 |
| `explicit.stat_789117908@T2` | -1.03829 |
| `explicit.stat_789117908@T1` | -1.03822 |
| `explicit.stat_4080418644@T1` | -1.03785 |
| `explicit.stat_3291658075@T2` | -1.03705 |

### accessory.amulet — n=51904, R²=-2.1513

intercept: `3.6848`  ·  log_price: True  ·  ilvl: `-0.04471`  ·  n_mods: `-0.02224`  ·  n_top_tier: `1.15451`  ·  corrupted: `0.03967`  ·  n_sockets: `-0.13588`  ·  quality: `0.00141`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.54471 |
| `explicit.stat_3299347043@T2` | -1.34595 |
| `explicit.stat_472520716@T2` | -1.21224 |
| `explicit.stat_803737631@T1` | -1.20948 |
| `explicit.stat_2866361420@T2` | -1.20947 |
| `explicit.stat_2974417149@T1` | -1.20942 |
| `explicit.stat_2974417149@T2` | -1.20859 |
| `explicit.stat_587431675@T2` | -1.20536 |
| `explicit.stat_2866361420@T1` | -1.19812 |
| `explicit.stat_1050105434@T2` | -1.19357 |
| `explicit.stat_803737631@T2` | -1.19267 |
| `explicit.stat_789117908@T1` | -1.18297 |

### accessory.belt — n=38445, R²=-1.3226

intercept: `5.2613`  ·  log_price: True  ·  ilvl: `-0.05945`  ·  n_mods: `-0.10343`  ·  n_top_tier: `0.54467`  ·  corrupted: `1.15330`  ·  n_sockets: `0.23717`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.35505 |
| `explicit.stat_3299347043@T2` | -0.86943 |
| `explicit.stat_2923486259@T1` | 0.86784 |
| `explicit.stat_2881298780@T1` | -0.73847 |
| `explicit.stat_4220027924@T2` | -0.70339 |
| `explicit.stat_51994685@T1` | -0.64425 |
| `explicit.stat_644456512@T1` | -0.61601 |
| `explicit.stat_1389754388@T1` | -0.59200 |
| `explicit.stat_809229260@T2` | -0.58574 |
| `explicit.stat_3372524247@T2` | -0.56716 |
| `explicit.stat_2881298780@T2` | -0.56089 |
| `explicit.stat_1570770415@T1` | -0.56008 |

### armour.chest — n=38145, R²=-1.7679

intercept: `3.2077`  ·  log_price: True  ·  ilvl: `-0.03952`  ·  n_mods: `-0.01482`  ·  n_top_tier: `0.52220`  ·  corrupted: `0.27020`  ·  n_sockets: `0.01800`  ·  quality: `0.05763`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.51673 |
| `explicit.stat_3981240776@T1` | 0.95950 |
| `explicit.stat_986397080@T2` | -0.57810 |
| `explicit.stat_986397080@T1` | -0.56043 |
| `explicit.stat_915769802@T2` | -0.55498 |
| `explicit.stat_1692879867@T1` | -0.55260 |
| `explicit.stat_3484657501@T1` | -0.55153 |
| `explicit.stat_915769802@T1` | -0.55048 |
| `explicit.stat_4080418644@T2` | -0.55048 |
| `explicit.stat_4080418644@T1` | -0.54351 |
| `explicit.stat_3299347043@T2` | -0.54144 |
| `explicit.stat_1692879867@T2` | -0.53907 |

### armour.helmet — n=37044, R²=-1.6681

intercept: `3.4044`  ·  log_price: True  ·  ilvl: `-0.04299`  ·  n_mods: `-0.02302`  ·  n_top_tier: `0.47225`  ·  corrupted: `0.74208`  ·  n_sockets: `0.05581`  ·  quality: `0.05678`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.42634 |
| `crafted.stat_3917489142@T1` | -4.53022 |
| `explicit.stat_3917489142@T2` | -0.80678 |
| `explicit.stat_3917489142@T1` | -0.72644 |
| `explicit.stat_2162097452@T2` | -0.64750 |
| `explicit.stat_1263695895@T1` | -0.63373 |
| `explicit.stat_4052037485@T2` | -0.56984 |
| `explicit.stat_1999113824@T1` | -0.55029 |
| `explicit.stat_1263695895@T2` | -0.54725 |
| `explicit.stat_803737631@T2` | -0.52454 |
| `explicit.stat_803737631@T1` | -0.51673 |
| `explicit.stat_2162097452@T1` | 0.51670 |

### armour.boots — n=34482, R²=-1.7322

intercept: `3.3870`  ·  log_price: True  ·  ilvl: `-0.04164`  ·  n_mods: `-0.01770`  ·  n_top_tier: `0.64454`  ·  corrupted: `0.00616`  ·  n_sockets: `0.02497`  ·  quality: `0.05581`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.65338 |
| `explicit.stat_2250533757@T1` | 1.44984 |
| `explicit.stat_2339757871@T1` | -0.88812 |
| `explicit.stat_3917489142@T2` | -0.86743 |
| `explicit.stat_3299347043@T1` | -0.82660 |
| `explicit.stat_3917489142@T1` | -0.79959 |
| `explicit.stat_2923486259@T2` | -0.69190 |
| `explicit.stat_1062208444@T2` | -0.68672 |
| `explicit.stat_3299347043@T2` | -0.68112 |
| `explicit.stat_2160282525@T1` | -0.67387 |
| `explicit.stat_1671376347@T2` | -0.66543 |
| `explicit.stat_4052037485@T2` | -0.66435 |

### armour.gloves — n=33644, R²=-1.7843

intercept: `3.6667`  ·  log_price: True  ·  ilvl: `-0.04676`  ·  n_mods: `-0.01381`  ·  n_top_tier: `0.69042`  ·  corrupted: `-0.01594`  ·  n_sockets: `0.07253`  ·  quality: `0.04474`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 1.85773 |
| `rune.stat_201332984` | 1.81688 |
| `explicit.stat_2339757871@T1` | 1.42415 |
| `explicit.stat_2923486259@T1` | -1.05681 |
| `explicit.stat_9187492@T2` | -0.91162 |
| `explicit.stat_3484657501@T2` | -0.88628 |
| `explicit.stat_2923486259@T2` | -0.87491 |
| `explicit.stat_3321629045@T2` | -0.86636 |
| `explicit.stat_1671376347@T1` | 0.85471 |
| `explicit.stat_3484657501@T1` | -0.82513 |
| `explicit.stat_4052037485@T1` | -0.81086 |
| `explicit.stat_9187492@T1` | 0.77691 |

### weapon.wand — n=20608, R²=-1.9904

intercept: `3.7533`  ·  log_price: True  ·  ilvl: `-0.04634`  ·  n_mods: `-0.04926`  ·  n_top_tier: `0.46792`  ·  corrupted: `0.08506`  ·  n_sockets: `0.11557`  ·  quality: `0.00759`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.78634 |
| `rune.stat_124131830` | -2.54060 |
| `explicit.stat_2254480358@T1` | 2.39027 |
| `explicit.stat_4226189338@T1` | 2.24402 |
| `explicit.stat_124131830@T1` | 2.00344 |
| `explicit.stat_591105508@T1` | 1.81406 |
| `explicit.stat_736967255@T2` | 1.72484 |
| `crafted.stat_124131830` | 1.24244 |
| `explicit.stat_2254480358@T2` | 0.99010 |
| `explicit.stat_4226189338@T2` | 0.97622 |
| `explicit.stat_1600707273@T2` | -0.81513 |
| `explicit.stat_1263695895@T1` | -0.80395 |

### weapon.bow — n=16510, R²=-1.9032

intercept: `3.7001`  ·  log_price: True  ·  ilvl: `-0.04286`  ·  n_mods: `-0.09861`  ·  n_top_tier: `0.62350`  ·  corrupted: `0.25788`  ·  n_sockets: `0.05368`  ·  quality: `0.03076`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.53619 |
| `desecrated.stat_210067635@T1` | -1.28398 |
| `explicit.stat_1202301673@T1` | 1.22887 |
| `desecrated.stat_666077204@T1` | -1.18184 |
| `explicit.stat_1263695895@T1` | -1.12338 |
| `explicit.stat_2463230181@T1` | -1.05477 |
| `explicit.stat_1263695895@T2` | -1.01064 |
| `explicit.stat_2463230181@T2` | -0.85748 |
| `explicit.stat_3695891184@T2` | -0.85297 |
| `explicit.stat_3695891184@T1` | -0.83010 |
| `explicit.stat_1509134228@T1` | -0.79502 |
| `explicit.stat_518292764@T2` | -0.76316 |

### flask.charm — n=16160, R²=-0.583

intercept: `0.0788`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `2.21250`  ·  corrupted: `1.60842`  ·  quality: `0.00007`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.86049 |
| `explicit.stat_1056492907` | 2.95011 |
| `explicit.stat_828533480@T2` | -2.21252 |
| `explicit.stat_1873752457@T2` | -2.21249 |
| `explicit.stat_1120862500@T2` | -2.21248 |
| `explicit.stat_1873752457@T1` | -2.21247 |
| `explicit.stat_2676834156@T2` | -2.21247 |
| `explicit.stat_3196823591@T2` | -2.21246 |
| `explicit.stat_388617051@T2` | -2.21246 |
| `explicit.stat_2365392475@T2` | -2.21245 |
| `explicit.stat_828533480@T1` | -2.21046 |
| `explicit.stat_1366840608@T2` | -2.20940 |

### weapon.crossbow — n=15472, R²=-1.8213

intercept: `3.8603`  ·  log_price: True  ·  ilvl: `-0.04653`  ·  n_mods: `-0.07381`  ·  n_top_tier: `0.51452`  ·  corrupted: `0.03905`  ·  n_sockets: `0.05515`  ·  quality: `0.02045`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.70115 |
| `explicit.stat_1980802737` | 1.31437 |
| `explicit.stat_1202301673@T1` | 1.23605 |
| `explicit.stat_2250681686@T2` | -1.19554 |
| `explicit.stat_709508406@T1` | 0.88603 |
| `explicit.stat_2250681686` | 0.88388 |
| `crafted.stat_3035140377` | 0.77279 |
| `explicit.stat_1263695895@T2` | -0.74740 |
| `explicit.stat_1037193709@T1` | -0.69256 |
| `explicit.stat_518292764@T1` | 0.69096 |
| `explicit.stat_1263695895@T1` | -0.68611 |
| `explicit.stat_2694482655@T1` | -0.68410 |

### weapon.warstaff — n=10188, R²=-0.3548

intercept: `-10.7296`  ·  log_price: True  ·  ilvl: `0.14691`  ·  n_mods: `-0.25257`  ·  n_top_tier: `0.21023`  ·  corrupted: `0.33467`  ·  n_sockets: `0.19130`  ·  quality: `0.06358`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 1.62740 |
| `desecrated.stat_2231156303@T1` | 1.62740 |
| `crafted.stat_210067635@T2` | 1.47309 |
| `desecrated.stat_3291658075@T1` | -1.44458 |
| `desecrated.stat_473429811@T1` | -1.44458 |
| `rune.stat_243313994` | 0.89494 |
| `explicit.stat_1509134228@T1` | 0.85771 |
| `explicit.stat_328541901@T1` | -0.83952 |
| `explicit.stat_709508406@T1` | 0.75933 |
| `desecrated.stat_9187492` | 0.73302 |
| `explicit.stat_328541901@T2` | -0.71628 |
| `explicit.stat_9187492@T1` | 0.68013 |

### weapon.staff — n=9511, R²=-0.3819

intercept: `-15.4927`  ·  log_price: True  ·  ilvl: `0.20095`  ·  n_mods: `-0.15040`  ·  n_top_tier: `0.58439`  ·  corrupted: `0.52960`  ·  n_sockets: `0.24327`  ·  quality: `0.03134`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 1.86313 |
| `explicit.stat_1545858329@T1` | 1.70748 |
| `explicit.stat_591105508@T1` | 1.56944 |
| `explicit.stat_293638271@T2` | -1.50586 |
| `explicit.stat_2254480358@T2` | 1.22648 |
| `explicit.stat_124131830@T1` | 1.10985 |
| `explicit.stat_1600707273@T1` | 0.98002 |
| `explicit.stat_591105508@T2` | 0.87934 |
| `explicit.stat_2968503605@T1` | -0.82670 |
| `explicit.stat_3291658075@T2` | -0.71537 |
| `explicit.stat_3695891184@T1` | -0.70215 |
| `explicit.stat_274716455@T1` | -0.67756 |

### weapon.sceptre — n=9388, R²=-0.3349

intercept: `-20.5623`  ·  log_price: True  ·  ilvl: `0.26395`  ·  n_mods: `-0.05358`  ·  n_top_tier: `-0.09556`  ·  corrupted: `0.47705`  ·  n_sockets: `0.27179`  ·  quality: `0.02790`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 3.20362 |
| `explicit.stat_2162097452@T2` | 1.84716 |
| `explicit.stat_1250712710@T2` | 1.80325 |
| `explicit.stat_3057012405@T1` | 1.42471 |
| `explicit.stat_101878827@T1` | 0.93173 |
| `explicit.stat_2347036682@T1` | 0.88306 |
| `explicit.stat_101878827@T2` | 0.81777 |
| `explicit.stat_1250712710@T1` | 0.72392 |
| `explicit.stat_1798257884@T2` | 0.67790 |
| `explicit.stat_4010677958@T1` | 0.67001 |
| `explicit.stat_1050105434@T1` | 0.61989 |
| `explicit.stat_4010677958@T2` | 0.61813 |

### weapon.spear — n=7638, R²=-0.4169

intercept: `-12.5482`  ·  log_price: True  ·  ilvl: `0.17616`  ·  n_mods: `-0.19318`  ·  n_top_tier: `0.74304`  ·  corrupted: `0.06091`  ·  n_sockets: `0.18637`  ·  quality: `0.05585`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.48561 |
| `explicit.stat_1202301673@T1` | 1.49518 |
| `explicit.stat_9187492@T1` | 1.35878 |
| `desecrated.stat_210067635@T1` | -1.30380 |
| `crafted.stat_3035140377` | 1.16980 |
| `explicit.stat_1509134228@T1` | 1.10345 |
| `explicit.stat_4080418644@T2` | -1.03675 |
| `explicit.stat_9187492@T2` | -0.97501 |
| `explicit.stat_3261801346@T1` | -0.93593 |
| `explicit.stat_3261801346@T2` | -0.89165 |
| `explicit.stat_709508406@T1` | 0.86501 |
| `explicit.stat_748522257@T2` | -0.83743 |

### armour.focus — n=6270, R²=-0.3636

intercept: `-14.0704`  ·  log_price: True  ·  ilvl: `0.18539`  ·  n_mods: `-0.19015`  ·  n_top_tier: `0.89064`  ·  corrupted: `0.42557`  ·  n_sockets: `0.41127`  ·  quality: `0.05991`

| stat_id | coef |
|---|---|
| `explicit.stat_4220027924@T2` | -1.45528 |
| `explicit.stat_2231156303@T2` | -1.38369 |
| `explicit.stat_4220027924@T1` | -1.35638 |
| `crafted.stat_2974417149@T1` | 1.29717 |
| `explicit.stat_2231156303@T1` | -1.14939 |
| `explicit.stat_3291658075@T1` | -1.09225 |
| `crafted.stat_737908626@T2` | -1.08823 |
| `explicit.stat_2923486259@T1` | -1.08334 |
| `explicit.stat_2974417149@T1` | -0.96354 |
| `explicit.stat_2891184298@T1` | -0.85374 |
| `explicit.stat_736967255@T2` | -0.83501 |
| `explicit.stat_4052037485@T2` | -0.82219 |

### armour.quiver — n=5870, R²=-0.3112

intercept: `-13.6227`  ·  log_price: True  ·  ilvl: `0.16998`  ·  n_mods: `-0.14936`  ·  n_top_tier: `0.93419`  ·  corrupted: `0.70663`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.23490 |
| `explicit.stat_2463230181@T1` | 3.12559 |
| `explicit.stat_2463230181@T2` | 1.56726 |
| `explicit.stat_681332047@T2` | -1.41722 |
| `explicit.stat_1573130764@T1` | -1.30171 |
| `explicit.stat_803737631@T2` | -1.15476 |
| `explicit.stat_2321178454@T2` | -1.05870 |
| `explicit.stat_803737631@T1` | -1.05719 |
| `explicit.stat_4067062424@T1` | -0.98265 |
| `explicit.stat_2194114101@T2` | -0.96969 |
| `explicit.stat_1573130764@T2` | -0.95149 |
| `explicit.stat_3261801346@T1` | -0.90893 |

### armour.shield — n=5086, R²=-0.474

intercept: `-10.8405`  ·  log_price: True  ·  ilvl: `0.14568`  ·  n_mods: `-0.10906`  ·  n_top_tier: `0.81332`  ·  corrupted: `-0.33105`  ·  n_sockets: `0.28863`  ·  quality: `0.05621`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.51124 |
| `explicit.stat_3321629045@T2` | -1.36730 |
| `explicit.stat_2923486259@T2` | -1.20903 |
| `explicit.stat_2481353198@T2` | -1.19807 |
| `explicit.stat_3033371881@T2` | -1.19423 |
| `explicit.stat_3484657501@T2` | -1.18005 |
| `explicit.stat_2451402625@T1` | -1.06452 |
| `explicit.stat_2923486259@T1` | -1.05321 |
| `explicit.stat_2451402625@T2` | -1.03473 |
| `explicit.stat_3855016469@T1` | -1.01194 |
| `explicit.stat_328541901@T1` | -1.00233 |
| `explicit.stat_2481353198@T1` | -0.95417 |

### weapon.twomace — n=4663, R²=-0.4677

intercept: `-10.0450`  ·  log_price: True  ·  ilvl: `0.13885`  ·  n_mods: `-0.21322`  ·  n_top_tier: `0.38401`  ·  corrupted: `-0.02091`  ·  n_sockets: `0.15518`  ·  quality: `0.05664`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.92339 |
| `desecrated.stat_1509134228@T1` | 1.66541 |
| `explicit.stat_1037193709@T1` | -1.45288 |
| `explicit.stat_1263695895@T2` | -0.90528 |
| `crafted.stat_3035140377` | 0.79113 |
| `explicit.stat_387439868@T2` | -0.76955 |
| `explicit.stat_691932474@T1` | -0.69979 |
| `explicit.stat_3336890334@T1` | -0.60770 |
| `explicit.stat_3695891184@T1` | -0.58405 |
| `explicit.stat_210067635@T2` | 0.57066 |
| `explicit.stat_518292764@T2` | -0.57064 |
| `explicit.stat_9187492@T1` | -0.57043 |

## Coverage (listings per base)

- … **Sapphire** — 29570 listings (29520 priced) [0.3–885594757.8 ex]
- … **Emerald** — 28843 listings (28802 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 22109 listings (22083 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10988 listings (10973 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 9714 listings (9693 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 9379 listings (9356 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9257 listings (9249 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8779 listings (8762 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8643 listings (8624 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8427 listings (8415 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7190 listings (7180 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6889 listings (6883 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6861 listings (6855 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6617 listings (6596 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6057 listings (6050 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 5990 listings (5964 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 5930 listings (5913 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 5914 listings (5903 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 5892 listings (5885 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5852 listings (5826 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5764 listings (5755 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5655 listings (5648 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5410 listings (5407 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5375 listings (5363 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5318 listings (5309 priced) [0.3–398912568423.8 ex]

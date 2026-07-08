# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-08T23:08:50+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **347723** (347198 priced in exalted)
- Distinct bases: 960 · distinct mods: 2882 · mod rows: 1651243
- Sold signals: **29607** sold · 185632 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-08T22:56:06+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×16.85** (median |log error| 2.8243)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 76% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.05** · typical error ×37.37 · ±30% 12% · n=50652
- Premium segment (60ex+): skill **+0.06** · typical error ×154.90 · ±30% 0% · n=31494

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 6672 | ×11.25 | 4% | +0.04 | +0.06 |
| accessory.amulet | 6254 | ×47.08 | 21% | +0.03 | +0.03 |
| jewel | 5955 | ×8.34 | 8% | +0.02 | +0.04 |
| accessory.belt | 5038 | ×9.23 | 23% | +0.02 | +0.03 |
| armour.chest | 4883 | ×10.00 | 25% | +0.00 | +0.01 |
| armour.helmet | 4824 | ×10.00 | 22% | +0.00 | +0.02 |
| armour.boots | 4452 | ×13.62 | 7% | +0.02 | +0.02 |
| armour.gloves | 4443 | ×15.55 | 6% | +0.02 | +0.02 |
| other | 4112 | ×9.71 | 38% | +0.06 | +0.15 |
| weapon.wand | 2959 | ×36.77 | 21% | +0.05 | +0.06 |
| weapon.bow | 2416 | ×22.69 | 19% | +0.09 | +0.11 |
| weapon.crossbow | 2218 | ×19.28 | 19% | +0.10 | +0.10 |
| weapon.warstaff | 1144 | ×72.23 | 17% | +0.06 | +0.06 |
| weapon.sceptre | 1085 | ×42.28 | 12% | +0.08 | +0.10 |
| weapon.staff | 1078 | ×71.72 | 17% | +0.05 | +0.07 |
| weapon.spear | 897 | ×50.00 | 17% | +0.03 | +0.06 |
| armour.focus | 728 | ×99.99 | 13% | +0.04 | +0.13 |
| armour.quiver | 697 | ×69.22 | 13% | +0.02 | +0.08 |
| flask.charm | 614 | ×77.76 | 29% | +0.00 | +0.01 |
| armour.shield | 562 | ×28.12 | 16% | +0.04 | +0.05 |
| weapon.twomace | 520 | ×20.00 | 17% | +0.05 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=35299, R²=-0.5006

intercept: `1.6029`  ·  log_price: True  ·  ilvl: `0.00008`  ·  n_mods: `0.01956`  ·  n_top_tier: `0.51770`  ·  corrupted: `1.07490`  ·  n_sockets: `-0.00008`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.64625 |
| `explicit.stat_2106365538@T1` | 2.20160 |
| `explicit.stat_1589917703@T1` | -1.39888 |
| `explicit.stat_3141070085@T1` | -1.31101 |
| `explicit.stat_2974417149@T1` | 0.97469 |
| `explicit.stat_1050105434@T1` | -0.91260 |
| `explicit.stat_3917489142@T1` | 0.90752 |
| `explicit.stat_101878827@T1` | -0.78411 |
| `explicit.stat_2891184298@T1` | 0.74165 |
| `explicit.stat_789117908@T1` | -0.68921 |
| `explicit.stat_2482852589@T1` | 0.57502 |
| `explicit.stat_1589917703` | 0.28378 |

### jewel — n=32032, R²=-0.6284

intercept: `-1.1203`  ·  log_price: True  ·  ilvl: `0.03707`  ·  n_mods: `0.14355`  ·  n_top_tier: `-0.02924`  ·  corrupted: `0.19420`  ·  quality: `0.22040`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -4.79401 |
| `explicit.stat_3741323227@T1` | -3.44779 |
| `explicit.stat_1569101201@T1` | 2.91530 |
| `explicit.stat_3780644166@T1` | -2.64967 |
| `explicit.stat_234296660@T1` | -2.55666 |
| `explicit.stat_2527686725@T1` | 2.52004 |
| `explicit.stat_3714003708@T1` | -1.82717 |
| `explicit.stat_3374165039@T1` | -1.63694 |
| `explicit.stat_3668351662@T1` | -1.57883 |
| `explicit.stat_4147897060@T1` | -1.53588 |
| `explicit.stat_3485067555@T1` | 1.42627 |
| `explicit.stat_3291658075@T1` | -1.37476 |

### accessory.ring — n=30528, R²=-1.2032

intercept: `3.9138`  ·  log_price: True  ·  ilvl: `-0.03962`  ·  n_mods: `-0.02488`  ·  n_top_tier: `0.04400`  ·  corrupted: `0.95400`  ·  n_sockets: `0.77461`  ·  quality: `0.04434`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 5.07872 |
| `explicit.stat_707457662@T2` | 4.60868 |
| `explicit.stat_1379411836@T1` | -1.70284 |
| `explicit.stat_1379411836@T2` | -1.22880 |
| `explicit.stat_1573130764@T1` | -1.15933 |
| `explicit.stat_1368271171@T1` | -0.91796 |
| `explicit.stat_1368271171@T2` | -0.84348 |
| `explicit.stat_2923486259@T1` | 0.84207 |
| `explicit.stat_707457662` | -0.77548 |
| `explicit.stat_1263695895@T1` | -0.70249 |
| `explicit.stat_2923486259@T2` | 0.69009 |
| `explicit.stat_1671376347@T1` | 0.59424 |

### accessory.amulet — n=28737, R²=-2.0662

intercept: `3.8454`  ·  log_price: True  ·  ilvl: `-0.04639`  ·  n_mods: `-0.02399`  ·  n_top_tier: `0.96918`  ·  corrupted: `0.10949`  ·  n_sockets: `1.73266`  ·  quality: `-0.00165`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.99177 |
| `explicit.stat_983749596@T2` | -1.67811 |
| `explicit.stat_3299347043@T1` | -1.12725 |
| `explicit.stat_2748665614@T1` | -1.08636 |
| `explicit.stat_587431675@T1` | -1.08384 |
| `explicit.stat_2748665614@T2` | -1.07886 |
| `explicit.stat_472520716@T2` | -1.05501 |
| `explicit.stat_472520716@T1` | -1.04364 |
| `explicit.stat_3299347043@T2` | -1.02638 |
| `explicit.stat_328541901@T1` | -1.01368 |
| `explicit.stat_3917489142@T2` | -1.01191 |
| `explicit.stat_3489782002@T2` | -1.00647 |

### accessory.belt — n=23017, R²=-0.1358

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.10166`  ·  corrupted: `0.00004`  ·  n_sockets: `-0.69311`

| stat_id | coef |
|---|---|
| `explicit.stat_2639966148` | 0.13813 |
| `explicit.stat_1389754388@T1` | -0.10168 |
| `explicit.stat_51994685@T1` | -0.10167 |
| `explicit.stat_1570770415@T1` | -0.10167 |
| `explicit.stat_2923486259@T2` | -0.10167 |
| `explicit.stat_644456512@T1` | -0.10167 |
| `explicit.stat_1389754388@T2` | -0.10166 |
| `explicit.stat_1836676211@T2` | -0.10166 |
| `explicit.stat_3299347043@T2` | -0.10166 |
| `explicit.stat_2923486259@T1` | -0.10166 |
| `explicit.stat_1671376347@T2` | -0.10166 |
| `explicit.stat_3299347043@T1` | -0.10166 |

### armour.chest — n=22783, R²=-0.2605

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.03182`  ·  corrupted: `0.00007`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_4220027924` | -0.03511 |
| `explicit.stat_915769802@T2` | -0.03185 |
| `explicit.stat_915769802@T1` | -0.03185 |
| `explicit.stat_3484657501@T1` | -0.03184 |
| `explicit.stat_3261801346@T1` | -0.03184 |
| `explicit.stat_4080418644@T2` | -0.03184 |
| `explicit.stat_3325883026@T2` | -0.03183 |
| `explicit.stat_3261801346@T2` | -0.03183 |
| `explicit.stat_2451402625@T2` | -0.03183 |
| `explicit.stat_3321629045@T1` | -0.03182 |
| `explicit.stat_986397080@T2` | -0.03182 |
| `explicit.stat_1062208444@T1` | -0.03181 |

### armour.helmet — n=22304, R²=-0.2919

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00004`  ·  n_top_tier: `0.10231`  ·  corrupted: `1.46223`  ·  n_sockets: `0.00001`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 0.90479 |
| `explicit.stat_3362812763@T2` | -0.10236 |
| `explicit.stat_53045048@T2` | -0.10236 |
| `explicit.stat_1263695895@T1` | -0.10235 |
| `explicit.stat_2451402625@T1` | -0.10235 |
| `explicit.stat_803737631@T2` | -0.10234 |
| `explicit.stat_4080418644@T2` | -0.10234 |
| `explicit.stat_3362812763@T1` | -0.10233 |
| `explicit.stat_4080418644@T1` | -0.10233 |
| `explicit.stat_1263695895@T2` | -0.10232 |
| `explicit.stat_53045048@T1` | -0.10232 |
| `explicit.stat_3033371881@T1` | -0.10231 |

### armour.boots — n=21087, R²=-0.4377

intercept: `3.6115`  ·  log_price: True  ·  ilvl: `-0.02789`  ·  n_mods: `-0.15645`  ·  n_top_tier: `0.43523`  ·  corrupted: `0.39078`  ·  n_sockets: `0.10126`  ·  quality: `0.00902`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.60860 |
| `explicit.stat_1062208444@T2` | -1.00318 |
| `rune.stat_836936635` | -0.94775 |
| `explicit.stat_2339757871@T1` | -0.81496 |
| `explicit.stat_2451402625@T2` | -0.73058 |
| `desecrated.stat_2250533757@T2` | -0.67398 |
| `explicit.stat_3321629045@T1` | -0.65610 |
| `explicit.stat_2923486259@T2` | -0.62854 |
| `explicit.stat_328541901@T1` | -0.62619 |
| `explicit.stat_2160282525@T1` | -0.59394 |
| `explicit.stat_1671376347@T2` | -0.58938 |
| `explicit.stat_3261801346@T2` | -0.58010 |

### armour.gloves — n=20541, R²=-0.5652

intercept: `3.4554`  ·  log_price: True  ·  ilvl: `-0.03498`  ·  n_mods: `-0.16954`  ·  n_top_tier: `0.51437`  ·  corrupted: `0.31747`  ·  n_sockets: `0.22340`  ·  quality: `0.01634`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T2` | -1.13521 |
| `explicit.stat_681332047@T2` | -0.93168 |
| `explicit.stat_803737631@T2` | -0.84004 |
| `explicit.stat_2451402625@T2` | -0.77026 |
| `explicit.stat_4080418644@T1` | -0.74922 |
| `explicit.stat_3695891184@T1` | -0.74306 |
| `explicit.stat_681332047@T1` | -0.73491 |
| `explicit.stat_3695891184@T2` | -0.71232 |
| `explicit.stat_4220027924@T2` | -0.70817 |
| `explicit.stat_3033371881@T2` | -0.69673 |
| `explicit.stat_1573130764@T1` | -0.68722 |
| `explicit.stat_3299347043@T2` | -0.67045 |

### weapon.wand — n=13905, R²=-2.1432

intercept: `3.4499`  ·  log_price: True  ·  ilvl: `-0.04305`  ·  n_mods: `-0.00905`  ·  n_top_tier: `0.38929`  ·  corrupted: `-0.00552`  ·  n_sockets: `0.02631`  ·  quality: `0.01153`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.64939 |
| `explicit.stat_591105508@T1` | 1.96284 |
| `explicit.stat_1545858329@T1` | 1.94782 |
| `explicit.stat_4226189338@T1` | 1.94145 |
| `explicit.stat_124131830@T1` | 1.86225 |
| `explicit.stat_736967255@T2` | 1.74150 |
| `explicit.stat_1600707273@T1` | 0.99473 |
| `crafted.stat_124131830` | 0.82170 |
| `explicit.stat_1600707273@T2` | 0.52188 |
| `explicit.stat_2231156303@T2` | -0.42627 |
| `explicit.stat_3015669065@T1` | -0.42406 |
| `explicit.stat_2768835289@T2` | -0.42094 |

### weapon.bow — n=11331, R²=-1.9362

intercept: `3.4120`  ·  log_price: True  ·  ilvl: `-0.04224`  ·  n_mods: `-0.01136`  ·  n_top_tier: `0.71682`  ·  corrupted: `0.24577`  ·  n_sockets: `0.00221`  ·  quality: `0.00943`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.27293 |
| `explicit.stat_2463230181@T1` | 1.57074 |
| `crafted.stat_3035140377` | 1.51180 |
| `explicit.stat_1202301673@T1` | 1.42727 |
| `rune.stat_3885405204` | -0.84809 |
| `explicit.stat_55876295@T1` | -0.77438 |
| `explicit.stat_1037193709@T1` | -0.76303 |
| `explicit.stat_1037193709@T2` | -0.74997 |
| `explicit.stat_3695891184@T2` | -0.74804 |
| `explicit.stat_3336890334@T2` | -0.74743 |
| `explicit.stat_3261801346@T1` | -0.74389 |
| `explicit.stat_3695891184@T1` | -0.74288 |

### weapon.crossbow — n=10605, R²=-1.8231

intercept: `3.5871`  ·  log_price: True  ·  ilvl: `-0.04444`  ·  n_mods: `-0.01016`  ·  n_top_tier: `0.71911`  ·  corrupted: `-0.02442`  ·  n_sockets: `0.02173`  ·  quality: `0.00457`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.92978 |
| `explicit.stat_2250681686@T2` | -1.50645 |
| `explicit.stat_709508406@T1` | 1.42776 |
| `explicit.stat_1202301673@T1` | 1.37012 |
| `explicit.stat_1980802737` | 1.15714 |
| `explicit.stat_1202301673@T2` | -0.91875 |
| `explicit.stat_1509134228@T2` | -0.83363 |
| `explicit.stat_2250681686` | 0.80180 |
| `explicit.stat_669069897@T1` | -0.79767 |
| `crafted.stat_3035140377` | 0.76804 |
| `explicit.stat_1509134228@T1` | 0.76604 |
| `explicit.stat_1263695895@T2` | -0.76078 |

### flask.charm — n=7812, R²=-0.423

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00132`  ·  corrupted: `0.47260`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.35365 |
| `explicit.stat_1056492907` | 2.99849 |
| `explicit.stat_2676834156@T1` | 1.60808 |
| `explicit.stat_2541588185@T1` | 0.29868 |
| `explicit.stat_3138344128` | 0.02095 |
| `explicit.stat_2678930256` | 0.02071 |
| `explicit.stat_1120862500@T2` | -0.00133 |
| `explicit.stat_1873752457@T2` | -0.00132 |
| `explicit.stat_828533480@T2` | -0.00132 |
| `explicit.stat_2676834156@T2` | -0.00132 |
| `explicit.stat_388617051@T2` | -0.00132 |
| `explicit.stat_1873752457@T1` | -0.00132 |

### weapon.warstaff — n=5568, R²=-0.5651

intercept: `-0.0012`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `-0.00004`  ·  n_top_tier: `0.14295`  ·  corrupted: `0.60821`  ·  n_sockets: `0.00002`  ·  quality: `0.01947`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | -6.98819 |
| `desecrated.stat_2231156303@T1` | -6.98819 |
| `rune.stat_243313994` | 1.54776 |
| `explicit.stat_9187492@T1` | 1.47189 |
| `rune.stat_731403740` | 1.35895 |
| `rune.stat_1712188793` | -0.57895 |
| `crafted.stat_210067635@T2` | -0.47854 |
| `desecrated.stat_9187492` | 0.44392 |
| `desecrated.stat_518292764` | 0.30881 |
| `crafted.stat_3035140377` | 0.30121 |
| `desecrated.stat_2231156303` | 0.17271 |
| `rune.stat_1037193709` | 0.16440 |

### weapon.staff — n=5143, R²=-0.6329

intercept: `-0.0105`  ·  log_price: True  ·  ilvl: `0.00013`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.19565`  ·  corrupted: `0.32191`  ·  n_sockets: `0.00049`  ·  quality: `0.00066`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 6.85809 |
| `explicit.stat_4226189338@T1` | 2.10704 |
| `explicit.stat_2254480358@T1` | 1.41305 |
| `explicit.stat_2768835289@T2` | 1.40970 |
| `explicit.stat_2254480358@T2` | 1.39479 |
| `explicit.stat_473429811@T1` | 0.75406 |
| `explicit.stat_1600707273@T1` | 0.49762 |
| `explicit.stat_124131830@T1` | 0.49746 |
| `explicit.stat_3962278098@T2` | 0.49735 |
| `explicit.stat_3291658075@T2` | 0.45635 |
| `crafted.stat_124131830` | 0.41672 |
| `rune.stat_3909696841` | 0.31303 |

### weapon.sceptre — n=5128, R²=-0.6206

intercept: `-0.6182`  ·  log_price: True  ·  ilvl: `0.00772`  ·  n_mods: `-0.00326`  ·  n_top_tier: `0.59263`  ·  corrupted: `1.36012`  ·  n_sockets: `0.01810`  ·  quality: `0.07882`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.67753 |
| `explicit.stat_3984865854@T1` | 0.69267 |
| `explicit.stat_4080418644@T1` | -0.62890 |
| `explicit.stat_4080418644@T2` | -0.61276 |
| `explicit.stat_2854751904@T1` | -0.60068 |
| `explicit.stat_1263695895@T2` | -0.60063 |
| `explicit.stat_2347036682@T2` | -0.59901 |
| `explicit.stat_3984865854@T2` | -0.59794 |
| `explicit.stat_328541901@T1` | -0.59718 |
| `explicit.stat_3639275092@T2` | -0.59564 |
| `explicit.stat_1574590649@T2` | -0.59377 |
| `explicit.stat_1263695895@T1` | -0.59287 |

### weapon.spear — n=4372, R²=-0.6016

intercept: `-0.0013`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.01555`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00004`  ·  quality: `0.04378`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.69140 |
| `crafted.stat_3035140377` | 1.22886 |
| `explicit.stat_210067635@T1` | 1.08303 |
| `explicit.stat_1509134228@T1` | 0.67748 |
| `explicit.stat_3336890334@T1` | 0.67744 |
| `explicit.stat_709508406@T1` | 0.65589 |
| `crafted.stat_518292764` | 0.61800 |
| `explicit.stat_9187492@T1` | 0.54855 |
| `crafted.stat_210067635` | 0.14551 |
| `rune.stat_1039491398` | 0.10005 |
| `desecrated.stat_210067635` | -0.06893 |
| `rune.stat_1509134228` | 0.04308 |

### armour.focus — n=3549, R²=-0.6474

intercept: `-0.9612`  ·  log_price: True  ·  ilvl: `0.01183`  ·  n_mods: `-0.00140`  ·  n_top_tier: `0.52685`  ·  corrupted: `0.00916`  ·  n_sockets: `0.03167`  ·  quality: `0.07644`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -4.68569 |
| `explicit.stat_1671376347@T1` | 0.69072 |
| `explicit.stat_789117908@T2` | -0.56926 |
| `desecrated.stat_3393628375@T1` | -0.55604 |
| `explicit.stat_4220027924@T2` | -0.55221 |
| `explicit.stat_124131830@T2` | -0.55193 |
| `explicit.stat_2891184298@T2` | -0.54951 |
| `explicit.stat_2231156303@T2` | -0.54867 |
| `explicit.stat_2974417149@T1` | -0.54725 |
| `explicit.stat_274716455@T1` | -0.54414 |
| `explicit.stat_4052037485@T2` | -0.54030 |
| `explicit.stat_3291658075@T1` | -0.53880 |

### armour.quiver — n=3330, R²=-0.6345

intercept: `-0.2661`  ·  log_price: True  ·  ilvl: `0.00320`  ·  n_mods: `0.00045`  ·  n_top_tier: `0.81688`  ·  corrupted: `0.59604`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 11.29824 |
| `explicit.stat_2463230181@T2` | -1.26579 |
| `explicit.stat_681332047@T2` | -0.83998 |
| `explicit.stat_681332047@T1` | -0.83732 |
| `explicit.stat_1573130764@T1` | -0.82997 |
| `desecrated.stat_3932115504` | -0.82888 |
| `explicit.stat_2194114101@T2` | -0.82822 |
| `explicit.stat_1368271171@T2` | -0.82537 |
| `explicit.stat_1573130764@T2` | -0.82498 |
| `explicit.stat_3714003708@T2` | -0.82188 |
| `explicit.stat_1368271171@T1` | -0.82026 |
| `explicit.stat_2321178454@T2` | -0.81935 |

### armour.shield — n=2870, R²=-0.5885

intercept: `-0.0249`  ·  log_price: True  ·  ilvl: `0.00031`  ·  n_mods: `0.00007`  ·  n_top_tier: `0.31593`  ·  corrupted: `0.00211`  ·  n_sockets: `0.00021`  ·  quality: `0.06944`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.91267 |
| `explicit.stat_4220027924@T1` | 0.61317 |
| `explicit.stat_1978899297@T2` | -0.50605 |
| `explicit.stat_1011760251@T2` | -0.32132 |
| `explicit.stat_328541901@T1` | -0.31799 |
| `explicit.stat_2481353198@T1` | -0.31758 |
| `explicit.stat_2481353198@T2` | -0.31743 |
| `explicit.stat_2339757871@T1` | -0.31728 |
| `explicit.stat_3484657501@T1` | -0.31720 |
| `explicit.stat_328541901@T2` | -0.31720 |
| `explicit.stat_3484657501@T2` | -0.31662 |
| `explicit.stat_1671376347@T1` | -0.31660 |

### weapon.twomace — n=2553, R²=-0.5743

intercept: `-0.0389`  ·  log_price: True  ·  ilvl: `0.00049`  ·  n_mods: `-0.00018`  ·  n_top_tier: `0.72665`  ·  corrupted: `0.10550`  ·  n_sockets: `0.00060`  ·  quality: `0.00273`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.38439 |
| `crafted.stat_3035140377` | 1.22062 |
| `explicit.stat_3336890334@T1` | -0.72969 |
| `explicit.stat_1037193709@T1` | -0.72902 |
| `explicit.stat_387439868@T2` | -0.72853 |
| `explicit.stat_821021828@T2` | -0.72813 |
| `explicit.stat_821021828@T1` | -0.72792 |
| `explicit.stat_691932474@T1` | -0.72777 |
| `explicit.stat_1037193709@T2` | -0.72746 |
| `explicit.stat_3695891184@T1` | -0.72729 |
| `explicit.stat_3336890334@T2` | -0.72724 |
| `explicit.stat_55876295@T2` | -0.72717 |

## Coverage (listings per base)

- … **Sapphire** — 15183 listings (15162 priced) [0.3–7553463.8 ex]
- … **Emerald** — 15019 listings (15006 priced) [0.4–7553463.8 ex]
- … **Ruby** — 11585 listings (11573 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 6757 listings (6751 priced) [0.3–5288620.9 ex]
- … **Prismatic Ring** — 5305 listings (5300 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 5159 listings (5151 priced) [1.0–66666666.0 ex]
- … **Amethyst Ring** — 5090 listings (5089 priced) [0.3–4323655.9 ex]
- … **Stellar Amulet** — 5078 listings (5075 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 4910 listings (4903 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 4749 listings (4747 priced) [0.3–24532814.5 ex]
- … **Dueling Wand** — 4367 listings (4359 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 3970 listings (3965 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 3860 listings (3858 priced) [0.3–37474957.5 ex]
- … **Topaz Ring** — 3851 listings (3848 priced) [1.0–307202867.9 ex]
- … **Plate Belt** — 3498 listings (3493 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 3462 listings (3460 priced) [0.3–5286174.1 ex]
- … **Ancestral Tiara** — 3421 listings (3416 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3399 listings (3398 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3373 listings (3372 priced) [0.3–4547453.5 ex]
- … **Obliterator Bow** — 3364 listings (3355 priced) [0.3–22139622146.9 ex]
- … **Heavy Belt** — 3263 listings (3262 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 3250 listings (3249 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 3173 listings (3172 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 3102 listings (3100 priced) [0.3–24532814.5 ex]
- … **Lunar Amulet** — 3023 listings (3021 priced) [0.3–4877938.3 ex]

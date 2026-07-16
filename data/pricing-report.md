# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-16T13:27:48+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **547790** (546321 priced in exalted)
- Distinct bases: 986 · distinct mods: 3177 · mod rows: 2595848
- Sold signals: **25725** sold · 308257 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-16T13:19:03+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×29.39** (median |log error| 3.3805)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 80% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×78.56 · ±30% 4% · n=79563
- Premium segment (60ex+): skill **+0.13** · typical error ×321.18 · ±30% 0% · n=53555

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 11151 | ×55.22 | 22% | +0.04 | +0.05 |
| jewel | 10415 | ×9.91 | 5% | +0.06 | +0.09 |
| accessory.amulet | 10183 | ×53.39 | 20% | +0.03 | +0.04 |
| accessory.belt | 7696 | ×23.36 | 11% | +0.09 | +0.11 |
| armour.chest | 7477 | ×32.80 | 22% | +0.06 | +0.10 |
| armour.helmet | 7310 | ×30.17 | 14% | +0.08 | +0.10 |
| armour.boots | 6779 | ×40.92 | 21% | +0.07 | +0.09 |
| armour.gloves | 6647 | ×42.33 | 15% | +0.07 | +0.10 |
| other | 6168 | ×6.15 | 40% | +0.09 | +0.15 |
| weapon.wand | 4144 | ×38.08 | 18% | +0.07 | +0.09 |
| weapon.bow | 3277 | ×34.90 | 16% | +0.11 | +0.11 |
| weapon.crossbow | 3107 | ×30.35 | 16% | +0.09 | +0.13 |
| weapon.warstaff | 1948 | ×35.07 | 12% | +0.14 | +0.12 |
| weapon.staff | 1829 | ×57.01 | 10% | +0.10 | +0.11 |
| weapon.sceptre | 1801 | ×41.70 | 5% | +0.17 | +0.16 |
| weapon.spear | 1449 | ×48.83 | 16% | +0.08 | +0.08 |
| armour.focus | 1220 | ×34.48 | 6% | +0.15 | +0.18 |
| armour.quiver | 1153 | ×25.43 | 8% | +0.12 | +0.13 |
| flask.charm | 984 | ×33.49 | 32% | +0.04 | +0.07 |
| armour.shield | 950 | ×25.38 | 10% | +0.03 | +0.04 |
| weapon.twomace | 880 | ×12.65 | 11% | +0.08 | +0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=56589, R²=-0.9396

intercept: `-1.7192`  ·  log_price: True  ·  ilvl: `0.02601`  ·  n_mods: `0.69881`  ·  n_top_tier: `-0.21395`  ·  corrupted: `0.23525`  ·  quality: `0.22631`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.91492 |
| `explicit.stat_2301718443@T1` | 2.86114 |
| `explicit.stat_627767961@T1` | -2.36934 |
| `explicit.stat_3780644166@T1` | -2.28487 |
| `explicit.stat_3485067555@T1` | 2.11861 |
| `explicit.stat_1805182458@T1` | -2.11429 |
| `explicit.stat_1852872083@T1` | -1.72053 |
| `explicit.stat_234296660@T1` | -1.56206 |
| `explicit.stat_1869147066@T1` | -1.55751 |
| `explicit.stat_1569101201@T1` | 1.54423 |
| `explicit.stat_3668351662@T1` | -1.53219 |
| `explicit.stat_3166958180@T1` | -1.52305 |

### other — n=52749, R²=-0.5867

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.43117`  ·  corrupted: `0.26183`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.57980 |
| `explicit.stat_2974417149@T1` | 0.43281 |
| `explicit.stat_789117908@T1` | -0.35984 |
| `explicit.stat_2106365538@T1` | -0.34455 |
| `explicit.stat_3299347043@T1` | -0.32127 |
| `explicit.stat_3141070085@T1` | -0.28638 |
| `explicit.stat_3917489142@T1` | 0.24263 |
| `implicit.stat_3879011313` | 0.23039 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_2968503605@T1` | 0.20528 |
| `explicit.stat_736967255@T1` | -0.19111 |

### accessory.ring — n=50848, R²=-2.0228

intercept: `3.4708`  ·  log_price: True  ·  ilvl: `-0.04284`  ·  n_mods: `0.00032`  ·  n_top_tier: `0.89004`  ·  corrupted: `0.03886`  ·  n_sockets: `2.19448`  ·  quality: `0.07285`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -0.92706 |
| `explicit.stat_2144192055@T1` | -0.91399 |
| `explicit.stat_1263695895@T2` | -0.91371 |
| `explicit.stat_1368271171@T2` | -0.91212 |
| `explicit.stat_1263695895@T1` | -0.91193 |
| `explicit.stat_2231156303@T2` | -0.91064 |
| `explicit.stat_803737631@T1` | -0.90737 |
| `explicit.stat_3291658075@T1` | -0.90720 |
| `explicit.stat_3325883026@T1` | -0.90704 |
| `explicit.stat_1573130764@T1` | -0.90612 |
| `explicit.stat_3291658075@T2` | -0.90520 |
| `explicit.stat_2901986750@T1` | -0.90453 |

### accessory.amulet — n=46650, R²=-2.1411

intercept: `3.8126`  ·  log_price: True  ·  ilvl: `-0.04662`  ·  n_mods: `-0.02415`  ·  n_top_tier: `1.07157`  ·  corrupted: `0.09062`  ·  n_sockets: `-0.11405`  ·  quality: `-0.00032`

| stat_id | coef |
|---|---|
| `explicit.stat_587431675@T2` | -1.16380 |
| `explicit.stat_3299347043@T1` | -1.15162 |
| `explicit.stat_472520716@T2` | -1.13843 |
| `explicit.stat_803737631@T1` | -1.13102 |
| `explicit.stat_472520716@T1` | -1.12222 |
| `explicit.stat_2974417149@T2` | -1.12144 |
| `explicit.stat_1050105434@T2` | -1.12123 |
| `explicit.stat_2866361420@T2` | -1.11989 |
| `explicit.stat_2901986750@T1` | -1.11429 |
| `explicit.stat_3299347043@T2` | -1.10746 |
| `explicit.stat_3917489142@T2` | -1.10554 |
| `explicit.stat_803737631@T2` | -1.10486 |

### accessory.belt — n=35280, R²=-1.2501

intercept: `5.4600`  ·  log_price: True  ·  ilvl: `-0.06194`  ·  n_mods: `-0.12420`  ·  n_top_tier: `0.92533`  ·  corrupted: `1.09591`  ·  n_sockets: `-0.11956`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.43942 |
| `explicit.stat_3299347043@T2` | -1.14451 |
| `explicit.stat_1389754388@T1` | -1.10577 |
| `explicit.stat_4220027924@T2` | -1.07811 |
| `explicit.stat_2881298780@T1` | -1.06378 |
| `explicit.stat_644456512@T1` | -1.05623 |
| `explicit.stat_809229260@T2` | -1.03105 |
| `explicit.stat_1671376347@T2` | -1.02060 |
| `explicit.stat_51994685@T1` | -0.96756 |
| `explicit.stat_809229260@T1` | -0.96750 |
| `explicit.stat_3325883026@T1` | -0.96389 |
| `explicit.stat_644456512@T2` | -0.95224 |

### armour.chest — n=34998, R²=-1.7032

intercept: `3.4585`  ·  log_price: True  ·  ilvl: `-0.04259`  ·  n_mods: `-0.01778`  ·  n_top_tier: `0.53403`  ·  corrupted: `0.06833`  ·  n_sockets: `0.02955`  ·  quality: `0.06012`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.80169 |
| `explicit.stat_3981240776@T1` | 1.06383 |
| `explicit.stat_986397080@T2` | -0.60372 |
| `explicit.stat_4015621042@T1` | -0.58630 |
| `explicit.stat_3484657501@T1` | -0.56921 |
| `explicit.stat_986397080@T1` | -0.56854 |
| `explicit.stat_4080418644@T2` | -0.56555 |
| `explicit.stat_915769802@T2` | -0.56391 |
| `explicit.stat_1692879867@T1` | -0.56326 |
| `explicit.stat_3372524247@T2` | -0.56252 |
| `explicit.stat_1692879867@T2` | -0.56189 |
| `explicit.stat_4080418644@T1` | -0.56076 |

### armour.helmet — n=33959, R²=-1.4184

intercept: `3.9254`  ·  log_price: True  ·  ilvl: `-0.04980`  ·  n_mods: `-0.04895`  ·  n_top_tier: `0.43196`  ·  corrupted: `0.81259`  ·  n_sockets: `0.13344`  ·  quality: `0.04590`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.97835 |
| `crafted.stat_3917489142@T1` | 1.67824 |
| `explicit.stat_3917489142@T2` | -0.76700 |
| `explicit.stat_1263695895@T1` | -0.67909 |
| `explicit.stat_1999113824@T1` | -0.64970 |
| `explicit.stat_1263695895@T2` | -0.62940 |
| `explicit.stat_3917489142@T1` | -0.58862 |
| `explicit.stat_3321629045@T2` | -0.57238 |
| `explicit.stat_2162097452@T2` | -0.57005 |
| `explicit.stat_1999113824@T2` | -0.52881 |
| `explicit.stat_4052037485@T2` | -0.51850 |
| `explicit.stat_803737631@T1` | -0.50763 |

### armour.boots — n=31763, R²=-1.7411

intercept: `3.4542`  ·  log_price: True  ·  ilvl: `-0.04240`  ·  n_mods: `-0.01725`  ·  n_top_tier: `0.64529`  ·  corrupted: `0.00075`  ·  n_sockets: `0.02219`  ·  quality: `0.04574`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 5.48139 |
| `explicit.stat_2250533757@T1` | 1.47302 |
| `explicit.stat_3917489142@T2` | -0.77224 |
| `explicit.stat_3299347043@T1` | -0.75488 |
| `explicit.stat_2339757871@T1` | -0.73184 |
| `explicit.stat_2923486259@T2` | -0.71176 |
| `explicit.stat_2160282525@T1` | -0.69969 |
| `explicit.stat_3917489142@T1` | -0.69820 |
| `explicit.stat_1999113824@T2` | -0.68806 |
| `explicit.stat_53045048@T1` | -0.67490 |
| `explicit.stat_1671376347@T2` | -0.67387 |
| `explicit.stat_1062208444@T2` | -0.66841 |

### armour.gloves — n=30912, R²=-1.6855

intercept: `3.8710`  ·  log_price: True  ·  ilvl: `-0.04955`  ·  n_mods: `-0.01584`  ·  n_top_tier: `0.50821`  ·  corrupted: `0.02109`  ·  n_sockets: `0.06178`  ·  quality: `0.04229`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.52659 |
| `rune.stat_201332984` | -2.00248 |
| `explicit.stat_1671376347@T1` | 1.04678 |
| `explicit.stat_9187492@T1` | 0.89927 |
| `explicit.stat_3484657501@T2` | -0.78014 |
| `explicit.stat_2923486259@T1` | -0.76835 |
| `explicit.stat_9187492@T2` | -0.74688 |
| `explicit.stat_1999113824@T1` | 0.70158 |
| `explicit.stat_3484657501@T1` | -0.66627 |
| `explicit.stat_3321629045@T2` | -0.65994 |
| `explicit.stat_803737631@T2` | -0.64112 |
| `explicit.stat_3917489142@T2` | -0.62907 |

### weapon.wand — n=19516, R²=-2.2241

intercept: `3.6273`  ·  log_price: True  ·  ilvl: `-0.04478`  ·  n_mods: `-0.02252`  ·  n_top_tier: `0.40653`  ·  corrupted: `0.03642`  ·  n_sockets: `0.04013`  ·  quality: `0.00745`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.56586 |
| `rune.stat_124131830` | -2.55169 |
| `explicit.stat_1545858329@T1` | 2.29833 |
| `explicit.stat_4226189338@T1` | 2.00710 |
| `explicit.stat_591105508@T1` | 1.95716 |
| `explicit.stat_124131830@T1` | 1.94624 |
| `explicit.stat_736967255@T2` | 1.82146 |
| `crafted.stat_124131830` | 1.25322 |
| `explicit.stat_2254480358@T2` | 0.99505 |
| `explicit.stat_2768835289@T2` | 0.80277 |
| `explicit.stat_4226189338@T2` | 0.61437 |
| `explicit.stat_1600707273@T1` | 0.61077 |

### weapon.bow — n=15589, R²=-1.94

intercept: `3.6356`  ·  log_price: True  ·  ilvl: `-0.04395`  ·  n_mods: `-0.03897`  ·  n_top_tier: `0.63144`  ·  corrupted: `-0.05376`  ·  n_sockets: `0.00874`  ·  quality: `0.03761`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.05257 |
| `explicit.stat_1202301673@T1` | 1.66561 |
| `crafted.stat_3035140377` | 1.51898 |
| `explicit.stat_2463230181@T2` | -0.97140 |
| `explicit.stat_1263695895@T2` | -0.90688 |
| `explicit.stat_1263695895@T1` | -0.90676 |
| `desecrated.stat_666077204@T1` | -0.87201 |
| `explicit.stat_518292764@T2` | -0.78435 |
| `explicit.stat_3695891184@T2` | -0.74417 |
| `explicit.stat_1940865751@T1` | 0.73758 |
| `explicit.stat_1037193709@T1` | -0.71990 |
| `explicit.stat_3695891184@T1` | -0.71602 |

### weapon.crossbow — n=14676, R²=-1.8801

intercept: `3.7269`  ·  log_price: True  ·  ilvl: `-0.04535`  ·  n_mods: `-0.04137`  ·  n_top_tier: `0.78455`  ·  corrupted: `0.03509`  ·  n_sockets: `0.04367`  ·  quality: `0.01534`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.94621 |
| `explicit.stat_2250681686@T2` | -1.40451 |
| `explicit.stat_1202301673@T1` | 1.21299 |
| `explicit.stat_1980802737` | 1.16224 |
| `explicit.stat_1263695895@T2` | -0.99981 |
| `explicit.stat_1263695895@T1` | -0.97445 |
| `explicit.stat_709508406@T1` | 0.94221 |
| `crafted.stat_3035140377` | 0.94135 |
| `explicit.stat_1509134228@T2` | -0.91626 |
| `explicit.stat_2694482655@T1` | -0.91126 |
| `explicit.stat_1544773869@T2` | -0.86659 |
| `explicit.stat_709508406@T2` | -0.86582 |

### flask.charm — n=14383, R²=-0.5669

intercept: `0.0268`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.74237`  ·  corrupted: `1.86150`  ·  quality: `0.00044`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60430 |
| `explicit.stat_1056492907` | 3.20045 |
| `explicit.stat_828533480@T2` | -2.74239 |
| `explicit.stat_1120862500@T2` | -2.74237 |
| `explicit.stat_828533480@T1` | -2.74237 |
| `explicit.stat_388617051@T2` | -2.74236 |
| `explicit.stat_1873752457@T2` | -2.74236 |
| `explicit.stat_3196823591@T2` | -2.74235 |
| `explicit.stat_2676834156@T2` | -2.74235 |
| `explicit.stat_2541588185@T2` | -2.74235 |
| `explicit.stat_2365392475@T2` | -2.74234 |
| `explicit.stat_1873752457@T1` | -2.74233 |

### weapon.warstaff — n=9271, R²=-0.4123

intercept: `-9.3040`  ·  log_price: True  ·  ilvl: `0.12535`  ·  n_mods: `-0.18158`  ·  n_top_tier: `0.35542`  ·  corrupted: `0.16692`  ·  n_sockets: `0.19196`  ·  quality: `0.05824`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.11047 |
| `explicit.stat_328541901@T1` | -0.92727 |
| `rune.stat_243313994` | 0.90169 |
| `explicit.stat_328541901@T2` | -0.89704 |
| `explicit.stat_9187492@T1` | 0.82961 |
| `desecrated.stat_9187492` | 0.75911 |
| `explicit.stat_1037193709@T1` | 0.66687 |
| `explicit.stat_748522257@T2` | 0.49414 |
| `explicit.stat_1940865751@T1` | -0.47770 |
| `explicit.stat_518292764@T1` | -0.46729 |
| `explicit.stat_1368271171@T1` | -0.43552 |
| `crafted.stat_3035140377` | 0.42896 |

### weapon.staff — n=8673, R²=-0.4343

intercept: `-12.8409`  ·  log_price: True  ·  ilvl: `0.16655`  ·  n_mods: `-0.12178`  ·  n_top_tier: `0.49629`  ·  corrupted: `0.48753`  ·  n_sockets: `0.21687`  ·  quality: `0.04321`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.87564 |
| `explicit.stat_591105508@T1` | 1.32962 |
| `explicit.stat_293638271@T2` | -1.11634 |
| `explicit.stat_4226189338@T1` | 1.11389 |
| `explicit.stat_124131830@T2` | 1.03679 |
| `explicit.stat_124131830@T1` | 0.83327 |
| `explicit.stat_3962278098@T2` | 0.83183 |
| `explicit.stat_4226189338@T2` | 0.80438 |
| `explicit.stat_3291658075@T2` | 0.77325 |
| `explicit.stat_1263695895@T2` | -0.67629 |
| `explicit.stat_2505884597@T2` | -0.65962 |
| `explicit.stat_2968503605@T1` | -0.59346 |

### weapon.sceptre — n=8590, R²=-0.3619

intercept: `-17.7787`  ·  log_price: True  ·  ilvl: `0.22562`  ·  n_mods: `-0.04537`  ·  n_top_tier: `0.31969`  ·  corrupted: `0.45662`  ·  n_sockets: `0.25542`  ·  quality: `0.04648`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.87439 |
| `explicit.stat_2162097452@T2` | 1.74249 |
| `explicit.stat_1250712710@T2` | 1.16735 |
| `explicit.stat_3057012405@T1` | 1.10719 |
| `explicit.stat_1263695895@T1` | -1.01065 |
| `explicit.stat_1263695895@T2` | -0.85082 |
| `explicit.stat_1574590649@T1` | -0.80550 |
| `explicit.stat_2347036682@T2` | -0.75700 |
| `explicit.stat_289128254@T2` | -0.65227 |
| `explicit.stat_2854751904@T2` | -0.63256 |
| `explicit.stat_2347036682@T1` | 0.60744 |
| `explicit.stat_101878827@T1` | 0.58882 |

### weapon.spear — n=7045, R²=-0.4722

intercept: `-10.1597`  ·  log_price: True  ·  ilvl: `0.13893`  ·  n_mods: `-0.07957`  ·  n_top_tier: `0.73017`  ·  corrupted: `-0.04061`  ·  n_sockets: `0.26696`  ·  quality: `0.07221`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.13883 |
| `explicit.stat_1202301673@T1` | 2.03817 |
| `explicit.stat_1509134228@T1` | 1.62396 |
| `explicit.stat_9187492@T1` | 1.60068 |
| `explicit.stat_1037193709@T1` | -1.25512 |
| `explicit.stat_1263695895@T2` | -1.11857 |
| `crafted.stat_3035140377` | 0.99803 |
| `explicit.stat_691932474@T1` | -0.87971 |
| `explicit.stat_1940865751@T2` | -0.83136 |
| `explicit.stat_55876295@T1` | -0.81427 |
| `explicit.stat_748522257@T2` | -0.67802 |
| `explicit.stat_4080418644@T2` | -0.66042 |

### armour.focus — n=5773, R²=-0.3805

intercept: `-12.7878`  ·  log_price: True  ·  ilvl: `0.16556`  ·  n_mods: `-0.16853`  ·  n_top_tier: `0.69926`  ·  corrupted: `0.32881`  ·  n_sockets: `0.47957`  ·  quality: `0.08060`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 7.13056 |
| `crafted.stat_737908626@T2` | 1.73375 |
| `explicit.stat_3962278098@T1` | -1.27704 |
| `explicit.stat_4220027924@T2` | -1.21631 |
| `explicit.stat_3291658075@T1` | -1.15001 |
| `explicit.stat_2231156303@T2` | -1.01233 |
| `explicit.stat_2923486259@T1` | -0.84816 |
| `explicit.stat_2231156303@T1` | -0.84419 |
| `explicit.stat_2339757871@T1` | -0.81075 |
| `explicit.stat_2974417149@T1` | -0.80375 |
| `explicit.stat_4220027924@T1` | -0.76265 |
| `explicit.stat_2339757871@T2` | -0.75890 |

### armour.quiver — n=5421, R²=-0.3521

intercept: `-13.2247`  ·  log_price: True  ·  ilvl: `0.16064`  ·  n_mods: `-0.12152`  ·  n_top_tier: `0.76058`  ·  corrupted: `0.81794`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.24370 |
| `explicit.stat_2463230181@T1` | 1.90056 |
| `explicit.stat_1573130764@T1` | -1.24156 |
| `explicit.stat_681332047@T2` | -1.16059 |
| `explicit.stat_4067062424@T1` | -1.13061 |
| `explicit.stat_2321178454@T2` | -1.11174 |
| `explicit.stat_803737631@T2` | -1.02963 |
| `explicit.stat_1573130764@T2` | -0.93108 |
| `explicit.stat_3261801346@T1` | -0.89793 |
| `explicit.stat_2463230181@T2` | 0.88582 |
| `explicit.stat_2321178454@T1` | -0.87297 |
| `explicit.stat_803737631@T1` | -0.84971 |

### armour.shield — n=4703, R²=-0.5185

intercept: `-10.0662`  ·  log_price: True  ·  ilvl: `0.13124`  ·  n_mods: `-0.08510`  ·  n_top_tier: `0.58371`  ·  corrupted: `-0.32070`  ·  n_sockets: `0.22260`  ·  quality: `0.06688`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.42735 |
| `explicit.stat_2339757871@T1` | -1.19638 |
| `explicit.stat_3484657501@T2` | -1.16382 |
| `explicit.stat_2481353198@T2` | -1.11951 |
| `explicit.stat_3484657501@T1` | -1.10726 |
| `explicit.stat_1011760251@T2` | -1.06818 |
| `explicit.stat_2481353198@T1` | -1.04418 |
| `explicit.stat_3321629045@T2` | -0.93002 |
| `explicit.stat_328541901@T1` | -0.89250 |
| `explicit.stat_1011760251@T1` | -0.88136 |
| `explicit.stat_2923486259@T2` | -0.88012 |
| `explicit.stat_3033371881@T2` | -0.83733 |

### weapon.twomace — n=4321, R²=-0.499

intercept: `-8.5180`  ·  log_price: True  ·  ilvl: `0.11542`  ·  n_mods: `-0.18076`  ·  n_top_tier: `0.25935`  ·  corrupted: `0.05763`  ·  n_sockets: `0.15282`  ·  quality: `0.05018`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.26468 |
| `desecrated.stat_1509134228@T1` | 3.24599 |
| `explicit.stat_1037193709@T1` | -1.59026 |
| `crafted.stat_3035140377` | 0.95786 |
| `explicit.stat_3336890334@T1` | -0.77948 |
| `explicit.stat_1037193709@T2` | -0.74860 |
| `explicit.stat_387439868@T2` | -0.65858 |
| `explicit.stat_9187492@T1` | -0.61262 |
| `explicit.stat_518292764@T2` | -0.51404 |
| `explicit.stat_210067635@T2` | 0.48848 |
| `explicit.stat_691932474@T1` | -0.46810 |
| `explicit.stat_1509134228@T1` | 0.45012 |

## Coverage (listings per base)

- … **Sapphire** — 26291 listings (26245 priced) [0.3–885594757.8 ex]
- … **Emerald** — 25802 listings (25770 priced) [0.3–885594757.8 ex]
- … **Ruby** — 19746 listings (19726 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10221 listings (10206 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8680 listings (8664 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8421 listings (8400 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8291 listings (8284 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 7896 listings (7881 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 7758 listings (7740 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 7716 listings (7707 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6460 listings (6452 priced) [0.2–307202867.9 ex]
- … **Dueling Wand** — 6238 listings (6220 priced) [0.3–4297682211.9 ex]
- … **Topaz Ring** — 6182 listings (6177 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6163 listings (6157 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5502 listings (5479 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5476 listings (5471 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 5342 listings (5328 priced) [0.2–24532814.5 ex]
- … **Jade Amulet** — 5337 listings (5328 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 5334 listings (5328 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5315 listings (5296 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5154 listings (5146 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5039 listings (5032 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 4900 listings (4898 priced) [0.3–123132003.2 ex]
- … **Heavy Belt** — 4876 listings (4868 priced) [0.3–398912568423.8 ex]
- … **Lunar Amulet** — 4835 listings (4824 priced) [0.3–91750808.2 ex]

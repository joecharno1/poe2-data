# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-07T13:37:23+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **278341** (278030 priced in exalted)
- Distinct bases: 945 · distinct mods: 2745 · mod rows: 1322350
- Sold signals: **32296** sold · 146886 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-07T13:26:37+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×16.21** (median |log error| 2.7855)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 75% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×42.36 · ±30% 13% · n=40109
- Premium segment (60ex+): skill **+0.07** · typical error ×165.37 · ±30% 0% · n=25007

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 5215 | ×12.67 | 4% | +0.04 | +0.06 |
| accessory.amulet | 5015 | ×54.18 | 20% | +0.02 | +0.02 |
| jewel | 4529 | ×8.49 | 7% | +0.01 | +0.03 |
| accessory.belt | 4146 | ×10.00 | 23% | +0.04 | +0.04 |
| armour.chest | 4061 | ×10.00 | 23% | +0.01 | +0.01 |
| armour.helmet | 3934 | ×10.00 | 23% | +0.01 | +0.01 |
| armour.boots | 3678 | ×13.38 | 9% | +0.01 | +0.02 |
| armour.gloves | 3620 | ×10.15 | 19% | -0.00 | +0.02 |
| other | 3429 | ×9.96 | 36% | +0.08 | +0.27 |
| weapon.wand | 2498 | ×23.75 | 23% | +0.06 | +0.06 |
| weapon.bow | 2064 | ×20.38 | 21% | +0.08 | +0.08 |
| weapon.crossbow | 1946 | ×14.43 | 21% | +0.09 | +0.09 |
| weapon.warstaff | 801 | ×78.41 | 19% | +0.01 | +0.01 |
| weapon.sceptre | 791 | ×82.40 | 16% | +0.01 | +0.03 |
| weapon.staff | 785 | ×78.41 | 19% | +0.03 | +0.04 |
| weapon.spear | 667 | ×50.00 | 22% | +0.01 | +0.00 |
| armour.focus | 528 | ×82.40 | 14% | +0.01 | +0.03 |
| armour.quiver | 528 | ×99.99 | 16% | +0.00 | +0.04 |
| armour.shield | 472 | ×82.11 | 16% | +0.02 | +0.02 |
| weapon.twomace | 396 | ×30.00 | 18% | +0.07 | +0.01 |
| flask.charm | 370 | ×4.44 | 45% | -0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=29538, R²=-0.4604

intercept: `1.6063`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `0.04708`  ·  n_top_tier: `0.63575`  ·  corrupted: `2.51216`  ·  n_sockets: `-0.00018`  ·  quality: `-0.00002`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.73170 |
| `explicit.stat_2106365538@T1` | 3.65123 |
| `explicit.stat_101878827@T1` | 3.39771 |
| `explicit.stat_1589917703@T1` | 2.67897 |
| `explicit.stat_3141070085@T1` | -1.75965 |
| `explicit.stat_1050105434@T1` | -1.32411 |
| `explicit.stat_3917489142@T1` | 1.21203 |
| `explicit.stat_2891184298@T1` | 0.93825 |
| `explicit.stat_2974417149@T1` | 0.79576 |
| `explicit.stat_789117908@T1` | -0.69001 |
| `explicit.stat_3141070085` | 0.35402 |
| `implicit.stat_1379411836` | -0.27603 |

### jewel — n=24264, R²=-0.6524

intercept: `-1.0491`  ·  log_price: True  ·  ilvl: `0.03540`  ·  n_mods: `0.13056`  ·  n_top_tier: `-0.00063`  ·  corrupted: `0.41372`  ·  quality: `0.21320`

| stat_id | coef |
|---|---|
| `explicit.stat_1569101201@T1` | 3.69071 |
| `explicit.stat_153777645@T1` | 3.35019 |
| `explicit.stat_21071013@T1` | -3.17934 |
| `explicit.stat_3714003708@T1` | -3.08582 |
| `explicit.stat_1316278494@T1` | -2.99693 |
| `explicit.stat_1697951953@T1` | -2.75581 |
| `explicit.stat_3668351662@T1` | -2.68205 |
| `explicit.stat_1854213750@T1` | -2.60403 |
| `explicit.stat_1594812856@T1` | -2.57787 |
| `explicit.stat_3192728503@T1` | -2.30727 |
| `explicit.stat_3283482523@T1` | -2.25647 |
| `explicit.stat_3741323227@T1` | -2.15496 |

### accessory.ring — n=23979, R²=-1.2516

intercept: `4.6455`  ·  log_price: True  ·  ilvl: `-0.04281`  ·  n_mods: `-0.15979`  ·  n_top_tier: `-0.00778`  ·  corrupted: `0.78773`  ·  n_sockets: `-1.48925`  ·  quality: `0.04157`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.66781 |
| `explicit.stat_707457662@T2` | 3.45520 |
| `explicit.stat_1379411836@T1` | -2.52187 |
| `explicit.stat_1379411836@T2` | -2.06639 |
| `explicit.stat_1368271171@T2` | -1.07650 |
| `explicit.stat_1368271171@T1` | -0.86921 |
| `explicit.stat_2923486259@T2` | 0.76624 |
| `explicit.stat_2923486259@T1` | 0.66137 |
| `explicit.stat_707457662` | -0.64607 |
| `explicit.stat_736967255@T1` | 0.62534 |
| `explicit.stat_4080418644@T2` | 0.59143 |
| `explicit.stat_2557965901@T1` | -0.48059 |

### accessory.amulet — n=22841, R²=-2.1081

intercept: `4.2836`  ·  log_price: True  ·  ilvl: `-0.05191`  ·  n_mods: `-0.02851`  ·  n_top_tier: `1.11986`  ·  corrupted: `0.12333`  ·  n_sockets: `1.66243`  ·  quality: `-0.00673`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | -2.81197 |
| `explicit.stat_983749596@T1` | -1.35056 |
| `explicit.stat_983749596@T2` | -1.29537 |
| `explicit.stat_3299347043@T1` | -1.24219 |
| `explicit.stat_3325883026@T1` | -1.23886 |
| `explicit.stat_3917489142@T2` | -1.22733 |
| `explicit.stat_2748665614@T1` | -1.20702 |
| `explicit.stat_3917489142@T1` | -1.20103 |
| `explicit.stat_2748665614@T2` | -1.19973 |
| `explicit.stat_3489782002@T2` | -1.19905 |
| `explicit.stat_3325883026@T2` | -1.18623 |
| `explicit.stat_472520716@T1` | -1.17633 |

### accessory.belt — n=18915, R²=-0.1078

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.40476`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00002`

| stat_id | coef |
|---|---|
| `explicit.stat_51994685@T1` | -0.40478 |
| `explicit.stat_2923486259@T2` | -0.40478 |
| `explicit.stat_1570770415@T1` | -0.40478 |
| `explicit.stat_644456512@T2` | -0.40477 |
| `explicit.stat_1389754388@T1` | -0.40477 |
| `explicit.stat_644456512@T1` | -0.40477 |
| `explicit.stat_51994685@T2` | -0.40477 |
| `explicit.stat_1389754388@T2` | -0.40477 |
| `explicit.stat_1570770415@T2` | -0.40477 |
| `explicit.stat_1836676211@T2` | -0.40477 |
| `explicit.stat_3299347043@T2` | -0.40476 |
| `explicit.stat_3585532255@T2` | -0.40476 |

### armour.chest — n=18678, R²=-0.2143

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.20629`  ·  corrupted: `0.00900`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_4080418644@T2` | -0.20632 |
| `explicit.stat_3261801346@T1` | -0.20632 |
| `explicit.stat_915769802@T2` | -0.20632 |
| `explicit.stat_915769802@T1` | -0.20632 |
| `explicit.stat_2339757871@T2` | -0.20631 |
| `explicit.stat_3033371881@T2` | -0.20630 |
| `explicit.stat_124859000@T2` | -0.20630 |
| `explicit.stat_2923486259@T1` | -0.20630 |
| `explicit.stat_2451402625@T2` | -0.20630 |
| `explicit.stat_3261801346@T2` | -0.20630 |
| `explicit.stat_3484657501@T1` | -0.20630 |
| `explicit.stat_3372524247@T2` | -0.20629 |

### armour.helmet — n=18293, R²=-0.2361

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.48144`  ·  corrupted: `1.38121`  ·  n_sockets: `0.00000`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.22119 |
| `explicit.stat_2451402625@T1` | -0.48146 |
| `explicit.stat_3362812763@T2` | -0.48146 |
| `explicit.stat_4080418644@T2` | -0.48146 |
| `explicit.stat_1263695895@T1` | -0.48146 |
| `explicit.stat_3362812763@T1` | -0.48145 |
| `explicit.stat_53045048@T2` | -0.48145 |
| `explicit.stat_2451402625@T2` | -0.48145 |
| `explicit.stat_1263695895@T2` | -0.48145 |
| `explicit.stat_53045048@T1` | -0.48144 |
| `explicit.stat_1062208444@T2` | -0.48144 |
| `explicit.stat_3484657501@T2` | -0.48144 |

### armour.boots — n=17229, R²=-0.3399

intercept: `3.3797`  ·  log_price: True  ·  ilvl: `-0.02301`  ·  n_mods: `-0.12334`  ·  n_top_tier: `0.48014`  ·  corrupted: `0.46101`  ·  n_sockets: `0.07523`  ·  quality: `0.00692`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.31031 |
| `explicit.stat_1062208444@T2` | -1.20082 |
| `explicit.stat_2451402625@T2` | -0.88365 |
| `rune.stat_836936635` | -0.68013 |
| `explicit.stat_1062208444@T1` | -0.66905 |
| `explicit.stat_3321629045@T2` | -0.65471 |
| `desecrated.stat_2250533757@T2` | -0.65049 |
| `explicit.stat_328541901@T1` | -0.64730 |
| `explicit.stat_99927264@T2` | -0.63678 |
| `explicit.stat_3917489142@T2` | -0.60110 |
| `explicit.stat_1999113824@T1` | -0.59352 |
| `explicit.stat_3321629045@T1` | -0.58894 |

### armour.gloves — n=16865, R²=-0.3447

intercept: `2.4928`  ·  log_price: True  ·  ilvl: `-0.00992`  ·  n_mods: `-0.03180`  ·  n_top_tier: `0.14634`  ·  corrupted: `0.14709`  ·  n_sockets: `0.07151`  ·  quality: `0.00391`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -0.39242 |
| `explicit.stat_803737631@T2` | -0.35211 |
| `explicit.stat_53045048@T1` | -0.30047 |
| `explicit.stat_3362812763@T2` | -0.28995 |
| `explicit.stat_3033371881@T2` | -0.28565 |
| `explicit.stat_681332047@T2` | -0.24554 |
| `explicit.stat_3484657501@T2` | -0.23283 |
| `explicit.stat_3917489142@T2` | -0.23172 |
| `explicit.stat_1573130764@T1` | -0.21530 |
| `explicit.stat_3362812763@T1` | -0.21438 |
| `explicit.stat_3695891184@T1` | -0.20620 |
| `explicit.stat_3033371881@T1` | -0.19630 |

### weapon.wand — n=11686, R²=-2.0065

intercept: `3.4771`  ·  log_price: True  ·  ilvl: `-0.04346`  ·  n_mods: `-0.01003`  ·  n_top_tier: `0.65464`  ·  corrupted: `0.02195`  ·  n_sockets: `0.01003`  ·  quality: `0.01255`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.85057 |
| `explicit.stat_2254480358@T1` | 1.77632 |
| `explicit.stat_591105508@T1` | 1.74170 |
| `explicit.stat_4226189338@T1` | 1.72015 |
| `explicit.stat_1600707273@T1` | 1.63931 |
| `explicit.stat_1545858329@T1` | 1.16395 |
| `explicit.stat_736967255@T2` | 0.83242 |
| `crafted.stat_124131830` | 0.82779 |
| `explicit.stat_737908626@T1` | -0.72393 |
| `explicit.stat_3962278098@T2` | -0.69933 |
| `explicit.stat_2768835289@T2` | -0.69868 |
| `explicit.stat_2968503605@T2` | -0.68189 |

### weapon.bow — n=9549, R²=-1.9059

intercept: `3.5017`  ·  log_price: True  ·  ilvl: `-0.04342`  ·  n_mods: `-0.00768`  ·  n_top_tier: `0.53710`  ·  corrupted: `-0.00949`  ·  n_sockets: `0.00572`  ·  quality: `0.00436`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.89653 |
| `explicit.stat_2463230181@T1` | 1.79072 |
| `explicit.stat_1202301673@T1` | 1.69398 |
| `crafted.stat_3035140377` | 1.15246 |
| `explicit.stat_518292764@T1` | 0.69814 |
| `desecrated.stat_666077204@T1` | -0.68212 |
| `explicit.stat_2694482655@T1` | -0.58405 |
| `explicit.stat_55876295@T1` | -0.58081 |
| `explicit.stat_669069897@T2` | -0.57495 |
| `explicit.stat_3261801346@T1` | -0.56986 |
| `explicit.stat_55876295@T2` | -0.56122 |
| `explicit.stat_3695891184@T2` | -0.55843 |

### weapon.crossbow — n=9036, R²=-1.774

intercept: `3.6746`  ·  log_price: True  ·  ilvl: `-0.04580`  ·  n_mods: `-0.00267`  ·  n_top_tier: `0.59262`  ·  corrupted: `-0.04023`  ·  n_sockets: `0.01286`  ·  quality: `0.00380`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 1.62907 |
| `explicit.stat_709508406@T1` | 1.58590 |
| `explicit.stat_2250681686@T2` | -1.44535 |
| `explicit.stat_1509134228@T1` | 0.96299 |
| `explicit.stat_1037193709@T1` | 0.93858 |
| `explicit.stat_2250681686` | 0.90156 |
| `crafted.stat_3035140377` | 0.89113 |
| `explicit.stat_1202301673@T2` | -0.66439 |
| `explicit.stat_669069897@T1` | -0.66149 |
| `explicit.stat_669069897@T2` | -0.64265 |
| `explicit.stat_1940865751@T2` | -0.63085 |
| `explicit.stat_1509134228@T2` | -0.62116 |

### flask.charm — n=5564, R²=-0.2502

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00004`  ·  corrupted: `0.01597`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.01065 |
| `explicit.stat_1056492907` | 2.99575 |
| `explicit.stat_2676834156@T1` | 1.60933 |
| `explicit.stat_3138344128` | 0.02230 |
| `explicit.stat_2678930256` | 0.00416 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_828533480@T1` | -0.00004 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_828533480@T2` | -0.00003 |
| `explicit.stat_3196823591@T2` | -0.00003 |
| `explicit.stat_388617051@T2` | -0.00003 |
| `explicit.stat_1120862500@T2` | -0.00003 |

### weapon.warstaff — n=3988, R²=-0.4607

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `-0.00002`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | -5.37599 |
| `desecrated.stat_2231156303@T1` | -5.37599 |
| `rune.stat_243313994` | 3.28523 |
| `rune.stat_731403740` | 1.60169 |
| `rune.stat_1712188793` | -1.04629 |
| `desecrated.stat_9187492` | 0.84405 |
| `desecrated.stat_2527686725` | 0.24675 |
| `rune.stat_3336890334` | 0.15967 |
| `desecrated.stat_518292764` | 0.14371 |
| `desecrated.stat_2231156303` | 0.08199 |
| `desecrated.stat_55876295` | -0.07934 |
| `rune.stat_2430860292` | -0.07498 |

### weapon.staff — n=3726, R²=-0.5113

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.64564 |
| `crafted.stat_124131830` | 0.29127 |
| `rune.stat_3990135792` | -0.15556 |
| `rune.stat_975988108` | -0.11973 |
| `rune.stat_2974417149` | 0.08788 |
| `explicit.stat_2254480358@T1` | 0.01753 |
| `desecrated.stat_2974417149` | 0.01359 |
| `explicit.stat_124131830@T1` | 0.00440 |
| `explicit.stat_1600707273@T1` | 0.00093 |
| `explicit.stat_2254480358@T2` | 0.00078 |
| `explicit.stat_473429811@T1` | 0.00068 |
| `explicit.stat_3962278098@T2` | 0.00005 |

### weapon.sceptre — n=3707, R²=-0.4659

intercept: `-0.0009`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00215`  ·  corrupted: `0.92115`  ·  n_sockets: `0.00001`  ·  quality: `0.03876`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.21477 |
| `rune.stat_1611856026` | 0.07364 |
| `rune.stat_3984865854` | 0.06185 |
| `desecrated.stat_3984865854` | 0.03761 |
| `rune.stat_1798257884` | 0.02846 |
| `rune.stat_3412619569` | 0.02846 |
| `explicit.stat_1798257884@T2` | 0.01905 |
| `desecrated.stat_1798257884` | 0.01829 |
| `desecrated.stat_1050105434` | 0.01065 |
| `explicit.stat_3984865854@T2` | -0.00217 |
| `explicit.stat_2347036682@T2` | -0.00217 |
| `explicit.stat_2347036682@T1` | -0.00217 |

### weapon.spear — n=3220, R²=-0.495

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00002`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.49784 |
| `explicit.stat_210067635@T1` | 0.69359 |
| `rune.stat_1039491398` | 0.22405 |
| `explicit.stat_1202301673@T1` | 0.19333 |
| `rune.stat_1509134228` | -0.15958 |
| `crafted.stat_210067635` | 0.00965 |
| `explicit.stat_1509134228@T1` | 0.00035 |
| `explicit.stat_3639275092@T1` | 0.00004 |
| `explicit.stat_210067635@T2` | 0.00004 |
| `explicit.stat_3639275092@T2` | 0.00004 |
| `explicit.stat_709508406@T1` | 0.00004 |
| `explicit.stat_3336890334@T2` | 0.00004 |

### armour.focus — n=2611, R²=-0.4622

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.05338`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00002`  ·  quality: `0.00936`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.51369 |
| `crafted.stat_2974417149@T1` | -4.85407 |
| `crafted.stat_737908626@T2` | -4.49335 |
| `desecrated.stat_3393628375` | 0.53352 |
| `crafted.stat_737908626` | 0.15754 |
| `explicit.stat_2923486259` | -0.14063 |
| `pseudo.total_chaos_res` | 0.14063 |
| `crafted.stat_2974417149` | 0.09401 |
| `crafted.stat_4015621042` | 0.06661 |
| `explicit.stat_736967255@T2` | -0.05340 |
| `explicit.stat_2891184298@T2` | -0.05340 |
| `explicit.stat_2923486259@T1` | -0.05340 |

### armour.quiver — n=2485, R²=-0.5405

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.12163`  ·  corrupted: `0.00003`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.67017 |
| `explicit.stat_3759663284@T1` | 0.23102 |
| `desecrated.stat_2194114101` | 0.18226 |
| `explicit.stat_681332047@T2` | -0.12167 |
| `explicit.stat_681332047@T1` | -0.12166 |
| `explicit.stat_2321178454@T2` | -0.12165 |
| `explicit.stat_1573130764@T1` | -0.12165 |
| `explicit.stat_1368271171@T2` | -0.12164 |
| `explicit.stat_3714003708@T2` | -0.12164 |
| `explicit.stat_803737631@T2` | -0.12164 |
| `explicit.stat_1573130764@T2` | -0.12164 |
| `explicit.stat_2194114101@T2` | -0.12164 |

### armour.shield — n=2196, R²=-0.4218

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.34068`  ·  corrupted: `0.00013`  ·  n_sockets: `0.00001`  ·  quality: `0.02354`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.75811 |
| `explicit.stat_1978899297@T2` | -0.48442 |
| `explicit.stat_1011760251@T1` | -0.36852 |
| `explicit.stat_1011760251@T2` | -0.35923 |
| `explicit.stat_1301765461@T1` | 0.35229 |
| `explicit.stat_2481353198@T1` | -0.34075 |
| `explicit.stat_2481353198@T2` | -0.34074 |
| `explicit.stat_328541901@T1` | -0.34071 |
| `explicit.stat_1062208444@T2` | -0.34071 |
| `explicit.stat_3676141501@T1` | -0.34071 |
| `explicit.stat_3484657501@T1` | -0.34070 |
| `explicit.stat_3372524247@T2` | -0.34070 |

### weapon.twomace — n=1874, R²=-0.4323

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.01061`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_518292764@T1` | 2.29195 |
| `desecrated.stat_210067635@T1` | 1.19008 |
| `desecrated.stat_1509134228@T1` | 0.79182 |
| `explicit.stat_1509134228@T1` | 0.70325 |
| `rune.stat_1039491398` | 0.13157 |
| `desecrated.stat_210067635` | 0.05748 |
| `rune.stat_1509134228` | -0.04751 |
| `explicit.stat_3336890334@T1` | -0.01068 |
| `explicit.stat_1037193709@T1` | -0.01067 |
| `explicit.stat_1037193709@T2` | -0.01064 |
| `explicit.stat_821021828@T1` | -0.01063 |
| `explicit.stat_1940865751@T2` | -0.01063 |

## Coverage (listings per base)

- … **Sapphire** — 11576 listings (11560 priced) [0.3–7553463.8 ex]
- … **Emerald** — 11575 listings (11567 priced) [0.5–7553463.8 ex]
- … **Ruby** — 8947 listings (8937 priced) [0.2–7553463.8 ex]
- … **Utility Belt** — 5620 listings (5616 priced) [0.2–5288620.9 ex]
- … **Stellar Amulet** — 4203 listings (4203 priced) [0.2–35690283.3 ex]
- … **Prismatic Ring** — 4197 listings (4196 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 4112 listings (4106 priced) [0.3–66666666.0 ex]
- … **Amethyst Ring** — 3980 listings (3979 priced) [0.3–71450.3 ex]
- … **Gold Amulet** — 3960 listings (3960 priced) [0.2–292542.5 ex]
- … **Gold Ring** — 3805 listings (3804 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 3665 listings (3660 priced) [0.3–3736768402.2 ex]
- … **Sapphire Ring** — 3192 listings (3189 priced) [0.3–24532814.5 ex]
- … **Topaz Ring** — 3085 listings (3084 priced) [0.5–123132003.2 ex]
- … **Ruby Ring** — 3072 listings (3072 priced) [0.3–37474957.5 ex]
- … **Plate Belt** — 2860 listings (2858 priced) [0.2–4877938.3 ex]
- … **Obliterator Bow** — 2774 listings (2768 priced) [0.2–22139622146.9 ex]
- … **Lapis Amulet** — 2751 listings (2751 priced) [0.3–4547453.5 ex]
- … **Ancestral Tiara** — 2741 listings (2739 priced) [0.6–37474957.5 ex]
- … **Jade Amulet** — 2713 listings (2712 priced) [0.2–4547453.5 ex]
- … **Amber Amulet** — 2707 listings (2706 priced) [0.2–113795639.4 ex]
- … **Heavy Belt** — 2700 listings (2700 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 2581 listings (2581 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 2532 listings (2532 priced) [0.3–14638.0 ex]
- … **Pearl Ring** — 2459 listings (2459 priced) [0.3–24532814.5 ex]
- … **Azure Amulet** — 2415 listings (2415 priced) [0.2–123132003.2 ex]

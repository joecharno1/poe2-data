# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-06T13:47:19+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **224481** (224318 priced in exalted)
- Distinct bases: 932 · distinct mods: 2619 · mod rows: 1065577
- Sold signals: **35581** sold · 116881 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-06T13:40:01+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×13.74** (median |log error| 2.6202)
- Within ±30% of asking price: **21%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 73% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.08** · typical error ×36.63 · ±30% 16% · n=32486
- Premium segment (60ex+): skill **+0.09** · typical error ×156.99 · ±30% 0% · n=19682
- Sold listings (clearing prices): skill **+0.11** · typical error ×38.06 · ±30% 0% · n=5

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 4131 | ×11.78 | 4% | +0.04 | +0.07 |
| accessory.amulet | 3963 | ×51.69 | 19% | +0.02 | +0.02 |
| jewel | 3651 | ×8.47 | 7% | +0.03 | +0.07 |
| accessory.belt | 3393 | ×8.74 | 28% | +0.03 | +0.01 |
| armour.chest | 3380 | ×10.00 | 29% | +0.00 | +0.01 |
| armour.helmet | 3249 | ×10.00 | 27% | +0.01 | -0.00 |
| armour.gloves | 3043 | ×10.00 | 24% | -0.01 | +0.00 |
| armour.boots | 3041 | ×10.00 | 24% | +0.00 | +0.00 |
| other | 2817 | ×9.99 | 35% | +0.08 | +0.31 |
| weapon.wand | 2146 | ×17.76 | 24% | +0.05 | +0.07 |
| weapon.bow | 1739 | ×10.83 | 22% | +0.07 | +0.09 |
| weapon.crossbow | 1637 | ×11.27 | 21% | +0.08 | +0.10 |
| weapon.warstaff | 585 | ×40.00 | 21% | +0.00 | +0.00 |
| weapon.staff | 536 | ×30.00 | 21% | +0.00 | +0.00 |
| weapon.sceptre | 515 | ×84.43 | 14% | +0.00 | +0.00 |
| weapon.spear | 478 | ×20.00 | 19% | +0.00 | +0.00 |
| armour.quiver | 388 | ×45.73 | 14% | +0.00 | +0.00 |
| armour.focus | 366 | ×82.27 | 14% | +0.02 | +0.02 |
| armour.shield | 325 | ×25.00 | 14% | +0.00 | +0.00 |
| flask.charm | 298 | ×20.00 | 38% | -0.00 | +0.00 |
| weapon.twomace | 287 | ×30.00 | 15% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=25306, R²=-0.4283

intercept: `1.6077`  ·  log_price: True  ·  ilvl: `0.00003`  ·  n_mods: `0.02198`  ·  n_top_tier: `0.67077`  ·  corrupted: `2.65211`  ·  n_sockets: `-0.00017`  ·  quality: `-0.00002`

| stat_id | coef |
|---|---|
| `explicit.stat_3141070085@T1` | 4.29826 |
| `explicit.stat_1589917703@T1` | 3.52768 |
| `explicit.stat_2106365538@T1` | 3.50361 |
| `explicit.stat_101878827@T1` | 3.32272 |
| `explicit.stat_3291658075@T1` | 3.20168 |
| `explicit.stat_2891184298@T1` | 2.82689 |
| `explicit.stat_1050105434@T1` | -1.36204 |
| `explicit.stat_3917489142@T1` | 1.35273 |
| `explicit.stat_789117908@T1` | -0.87567 |
| `explicit.stat_2968503605@T1` | 0.78260 |
| `explicit.stat_2974417149@T1` | 0.55017 |
| `implicit.stat_1379411836` | -0.27191 |

### accessory.ring — n=19157, R²=-1.2993

intercept: `4.9259`  ·  log_price: True  ·  ilvl: `-0.04260`  ·  n_mods: `-0.19611`  ·  n_top_tier: `-0.18250`  ·  corrupted: `0.91927`  ·  n_sockets: `1.00480`  ·  quality: `0.02427`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.73261 |
| `explicit.stat_707457662@T2` | 3.32836 |
| `explicit.stat_2557965901@T1` | 2.06573 |
| `explicit.stat_2557965901@T2` | 1.78830 |
| `explicit.stat_1379411836@T1` | -1.69755 |
| `explicit.stat_736967255@T1` | 1.10397 |
| `explicit.stat_1379411836@T2` | -1.02549 |
| `explicit.stat_2923486259@T2` | 0.94339 |
| `explicit.stat_3372524247@T1` | 0.85237 |
| `explicit.stat_2923486259@T1` | 0.69374 |
| `explicit.stat_3261801346@T2` | 0.69349 |
| `explicit.stat_3032590688@T2` | 0.67698 |

### jewel — n=18630, R²=-0.6886

intercept: `-1.2723`  ·  log_price: True  ·  ilvl: `0.03736`  ·  n_mods: `0.17933`  ·  n_top_tier: `-0.11759`  ·  corrupted: `0.25673`  ·  quality: `0.22194`

| stat_id | coef |
|---|---|
| `explicit.stat_3714003708@T1` | -3.66214 |
| `explicit.stat_1869147066@T1` | 3.47674 |
| `explicit.stat_1697951953@T1` | -2.91227 |
| `explicit.stat_3824372849@T1` | 2.86064 |
| `explicit.stat_1316278494@T1` | -2.85372 |
| `explicit.stat_2594634307@T1` | 2.66110 |
| `explicit.stat_1569101201@T1` | 2.36204 |
| `explicit.stat_2106365538@T1` | -2.34793 |
| `explicit.stat_416040624@T1` | -2.22796 |
| `explicit.stat_153777645@T1` | 2.16480 |
| `explicit.stat_3780644166@T1` | 2.15951 |
| `explicit.stat_2456523742@T1` | 2.03797 |

### accessory.amulet — n=18363, R²=-2.1456

intercept: `3.9947`  ·  log_price: True  ·  ilvl: `-0.04834`  ·  n_mods: `-0.02904`  ·  n_top_tier: `0.93067`  ·  corrupted: `0.07773`  ·  n_sockets: `0.94921`  ·  quality: `-0.03497`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -2.10086 |
| `explicit.stat_983749596@T2` | -1.83994 |
| `explicit.stat_1202301673@T2` | -1.59282 |
| `explicit.stat_3299347043@T1` | -1.14883 |
| `explicit.stat_3299347043@T2` | -1.05243 |
| `explicit.stat_2748665614@T1` | -1.04237 |
| `explicit.stat_3917489142@T2` | -1.02677 |
| `explicit.stat_587431675@T1` | -1.02123 |
| `explicit.stat_803737631@T1` | -1.01882 |
| `explicit.stat_2748665614@T2` | -1.01677 |
| `explicit.stat_3917489142@T1` | -1.00771 |
| `explicit.stat_3261801346@T1` | -1.00587 |

### accessory.belt — n=15581, R²=-0.0893

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.32435`  ·  corrupted: `0.00001`  ·  n_sockets: `4.28837`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.27858 |
| `explicit.stat_1389754388@T1` | -0.32436 |
| `explicit.stat_51994685@T1` | -0.32436 |
| `explicit.stat_1389754388@T2` | -0.32436 |
| `explicit.stat_1570770415@T1` | -0.32436 |
| `explicit.stat_1570770415@T2` | -0.32436 |
| `explicit.stat_51994685@T2` | -0.32436 |
| `explicit.stat_644456512@T2` | -0.32435 |
| `explicit.stat_2923486259@T2` | -0.32435 |
| `explicit.stat_644456512@T1` | -0.32435 |
| `explicit.stat_1050105434@T2` | -0.32435 |
| `explicit.stat_3585532255@T2` | -0.32435 |

### armour.chest — n=15416, R²=-0.2275

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.04537`  ·  corrupted: `0.00006`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3261801346@T1` | -0.04538 |
| `explicit.stat_915769802@T2` | -0.04538 |
| `explicit.stat_4080418644@T2` | -0.04538 |
| `explicit.stat_2451402625@T1` | -0.04538 |
| `explicit.stat_915769802@T1` | -0.04538 |
| `explicit.stat_3033371881@T2` | -0.04537 |
| `explicit.stat_3325883026@T1` | -0.04537 |
| `explicit.stat_124859000@T2` | -0.04537 |
| `explicit.stat_2451402625@T2` | -0.04537 |
| `explicit.stat_1062208444@T2` | -0.04537 |
| `explicit.stat_3372524247@T2` | -0.04537 |
| `explicit.stat_3301100256@T1` | -0.04537 |

### armour.helmet — n=15089, R²=-0.2269

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.19569`  ·  corrupted: `0.76669`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2451402625@T1` | -0.19571 |
| `explicit.stat_1263695895@T1` | -0.19570 |
| `explicit.stat_53045048@T2` | -0.19570 |
| `explicit.stat_3321629045@T1` | -0.19570 |
| `explicit.stat_803737631@T2` | -0.19570 |
| `explicit.stat_3362812763@T2` | -0.19570 |
| `explicit.stat_3362812763@T1` | -0.19570 |
| `explicit.stat_3484657501@T2` | -0.19570 |
| `explicit.stat_3325883026@T2` | -0.19570 |
| `explicit.stat_3484657501@T1` | -0.19570 |
| `explicit.stat_1062208444@T2` | -0.19570 |
| `explicit.stat_3325883026@T1` | -0.19569 |

### armour.boots — n=14197, R²=-0.2361

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.20918`  ·  corrupted: `0.00007`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2250533757@T2` | -0.61166 |
| `explicit.stat_2339757871@T1` | -0.20931 |
| `explicit.stat_2451402625@T2` | -0.20922 |
| `explicit.stat_3917489142@T2` | -0.20921 |
| `explicit.stat_3362812763@T1` | -0.20920 |
| `explicit.stat_2923486259@T2` | -0.20920 |
| `explicit.stat_3362812763@T2` | -0.20920 |
| `explicit.stat_1062208444@T2` | -0.20920 |
| `explicit.stat_3261801346@T2` | -0.20920 |
| `explicit.stat_99927264@T1` | -0.20920 |
| `explicit.stat_99927264@T2` | -0.20919 |
| `explicit.stat_1062208444@T1` | -0.20919 |

### armour.gloves — n=13968, R²=-0.2873

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00004`  ·  corrupted: `0.00005`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.09700 |
| `desecrated.stat_4067062424` | 0.08700 |
| `pseudo.total_life` | 0.01110 |
| `explicit.stat_3299347043` | -0.01110 |
| `rune.stat_3299347043` | -0.01110 |
| `desecrated.stat_3299347043` | -0.00949 |
| `desecrated.stat_1573130764` | 0.00916 |
| `pseudo.total_ele_res>=80` | 0.00034 |
| `explicit.stat_2339757871@T1` | -0.00025 |
| `explicit.stat_3484657501@T2` | -0.00008 |
| `explicit.stat_3362812763@T2` | -0.00008 |
| `explicit.stat_1368271171@T1` | -0.00007 |

### weapon.wand — n=9882, R²=-1.9113

intercept: `3.5463`  ·  log_price: True  ·  ilvl: `-0.04433`  ·  n_mods: `-0.00756`  ·  n_top_tier: `0.17469`  ·  corrupted: `0.06104`  ·  n_sockets: `0.00629`  ·  quality: `0.02275`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.50140 |
| `explicit.stat_2254480358@T1` | 2.25427 |
| `explicit.stat_4226189338@T1` | 2.23955 |
| `explicit.stat_591105508@T1` | 2.17794 |
| `explicit.stat_1545858329@T1` | 1.33101 |
| `explicit.stat_1600707273@T2` | 1.14948 |
| `crafted.stat_124131830` | 0.75706 |
| `explicit.stat_736967255@T2` | 0.40798 |
| `explicit.stat_737908626@T1` | -0.23133 |
| `explicit.stat_737908626@T2` | -0.22765 |
| `explicit.stat_473429811@T1` | -0.20191 |
| `explicit.stat_2231156303@T2` | -0.20149 |

### weapon.bow — n=8104, R²=-1.7639

intercept: `3.4565`  ·  log_price: True  ·  ilvl: `-0.04283`  ·  n_mods: `-0.01359`  ·  n_top_tier: `0.34202`  ·  corrupted: `-0.05677`  ·  n_sockets: `-0.00279`  ·  quality: `0.00580`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -3.33694 |
| `explicit.stat_1202301673@T1` | 1.92397 |
| `explicit.stat_2463230181@T1` | 1.92382 |
| `desecrated.stat_210067635@T1` | -1.65976 |
| `crafted.stat_3035140377` | 1.60962 |
| `explicit.stat_518292764@T1` | 1.20869 |
| `rune.stat_3885405204` | -0.57831 |
| `explicit.stat_55876295@T1` | -0.42232 |
| `explicit.stat_2694482655@T1` | -0.41424 |
| `explicit.stat_1037193709@T1` | -0.39275 |
| `explicit.stat_3261801346@T1` | -0.38805 |
| `explicit.stat_55876295@T2` | -0.38590 |

### weapon.crossbow — n=7669, R²=-1.6426

intercept: `3.5177`  ·  log_price: True  ·  ilvl: `-0.04396`  ·  n_mods: `-0.00807`  ·  n_top_tier: `0.43142`  ·  corrupted: `-0.02576`  ·  n_sockets: `0.00570`  ·  quality: `0.00469`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 1.87345 |
| `explicit.stat_1037193709@T1` | 1.79665 |
| `explicit.stat_709508406@T1` | 1.75647 |
| `explicit.stat_1202301673@T1` | 1.68054 |
| `explicit.stat_2250681686@T2` | -1.38399 |
| `crafted.stat_3035140377` | 1.20909 |
| `explicit.stat_2250681686` | 1.00941 |
| `explicit.stat_691932474@T1` | -0.86999 |
| `rune.stat_55876295` | 0.69324 |
| `rune.stat_2246411426` | -0.69278 |
| `explicit.stat_1202301673@T2` | -0.57524 |
| `explicit.stat_1940865751@T1` | -0.53434 |

### flask.charm — n=3731, R²=-0.113

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00005`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60509 |
| `explicit.stat_1056492907` | 2.70838 |
| `explicit.stat_3138344128` | 0.01448 |
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_1873752457@T1` | -0.00002 |
| `explicit.stat_1873752457@T2` | -0.00002 |
| `explicit.stat_828533480@T2` | -0.00002 |
| `explicit.stat_2676834156@T2` | -0.00002 |
| `explicit.stat_828533480@T1` | -0.00002 |
| `explicit.stat_3246948616` | 0.00002 |
| `explicit.stat_388617051@T2` | -0.00001 |
| `explicit.stat_2541588185@T2` | -0.00001 |

### weapon.warstaff — n=2748, R²=-0.2894

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 2.23505 |
| `rune.stat_1037193709` | 0.25438 |
| `rune.stat_3336890334` | 0.19285 |
| `rune.stat_1817052494` | -0.10175 |
| `rune.stat_2430860292` | -0.09964 |
| `crafted.stat_210067635@T2` | 0.08284 |
| `rune.stat_1509134228` | 0.04138 |
| `rune.stat_1039491398` | -0.03724 |
| `crafted.stat_210067635` | 0.00013 |
| `rune.stat_2077615515` | 0.00004 |
| `explicit.stat_1509134228@T2` | 0.00003 |
| `explicit.stat_709508406@T1` | -0.00002 |

### weapon.staff — n=2608, R²=-0.3045

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_3990135792` | -0.13412 |
| `rune.stat_2974417149` | 0.08047 |
| `explicit.stat_473429811@T1` | 0.00004 |
| `explicit.stat_124131830@T1` | 0.00004 |
| `explicit.stat_2254480358@T1` | 0.00003 |
| `explicit.stat_3291658075@T2` | 0.00002 |
| `explicit.stat_737908626@T1` | 0.00002 |
| `explicit.stat_124131830@T2` | 0.00002 |
| `explicit.stat_274716455@T1` | 0.00002 |
| `explicit.stat_2968503605@T2` | 0.00002 |
| `explicit.stat_293638271@T1` | 0.00002 |
| `explicit.stat_2974417149@T2` | 0.00002 |

### weapon.sceptre — n=2603, R²=-0.326

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00002`

| stat_id | coef |
|---|---|
| `desecrated.stat_1050105434` | 0.01276 |
| `desecrated.stat_3984865854` | -0.00535 |
| `explicit.stat_2162097452@T1` | 0.00004 |
| `explicit.stat_1263695895@T1` | 0.00004 |
| `explicit.stat_1798257884@T2` | 0.00002 |
| `explicit.stat_3057012405@T1` | 0.00002 |
| `explicit.stat_4010677958@T1` | 0.00002 |
| `explicit.stat_849987426@T1` | 0.00002 |
| `explicit.stat_101878827@T2` | 0.00002 |
| `explicit.stat_1998951374@T1` | 0.00002 |
| `explicit.stat_2162097452@T2` | 0.00002 |
| `explicit.stat_1250712710@T1` | -0.00001 |

### weapon.spear — n=2249, R²=-0.2762

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.49786 |
| `rune.stat_1509134228` | -0.00005 |
| `rune.stat_1039491398` | 0.00005 |
| `explicit.stat_210067635@T1` | 0.00004 |
| `explicit.stat_1263695895@T1` | -0.00004 |
| `explicit.stat_1263695895@T2` | -0.00003 |
| `explicit.stat_2694482655@T1` | 0.00002 |
| `explicit.stat_1509134228@T1` | 0.00002 |
| `explicit.stat_3639275092@T1` | 0.00002 |
| `explicit.stat_1202301673@T2` | -0.00001 |
| `explicit.stat_518292764@T1` | 0.00001 |
| `explicit.stat_387439868@T1` | 0.00001 |

### armour.focus — n=1866, R²=-0.1075

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `-0.00010`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.53244 |
| `desecrated.stat_3465022881@T1` | 1.94575 |
| `desecrated.stat_2910761524@T1` | 0.96144 |
| `desecrated.stat_3393628375` | 0.53775 |
| `desecrated.stat_2910761524` | -0.11576 |
| `desecrated.stat_3465022881` | -0.11374 |
| `crafted.stat_4015621042` | 0.06673 |
| `desecrated.stat_4015621042` | 0.03537 |
| `desecrated.stat_4220027924` | 0.00465 |
| `desecrated.stat_274716455` | 0.00134 |
| `desecrated.stat_737908626` | -0.00075 |
| `rune.stat_3523867985` | 0.00028 |

### armour.quiver — n=1781, R²=-0.326

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00003`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | -0.00009 |
| `explicit.stat_2463230181@T2` | -0.00004 |
| `explicit.stat_3714003708@T2` | -0.00003 |
| `explicit.stat_3032590688@T1` | -0.00003 |
| `explicit.stat_1573130764@T1` | -0.00003 |
| `explicit.stat_803737631@T2` | -0.00003 |
| `explicit.stat_3714003708@T1` | -0.00003 |
| `explicit.stat_1368271171@T2` | -0.00002 |
| `explicit.stat_2321178454@T2` | -0.00002 |
| `explicit.stat_681332047@T1` | -0.00002 |
| `explicit.stat_3032590688@T2` | -0.00002 |
| `explicit.stat_681332047@T2` | -0.00002 |

### armour.shield — n=1602, R²=-0.2874

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.23817`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.47402 |
| `explicit.stat_1978899297@T2` | -0.30182 |
| `explicit.stat_1011760251@T1` | -0.23825 |
| `explicit.stat_1301765461@T2` | -0.23822 |
| `explicit.stat_2339757871@T1` | -0.23821 |
| `explicit.stat_2481353198@T1` | -0.23820 |
| `explicit.stat_2481353198@T2` | -0.23819 |
| `explicit.stat_1011760251@T2` | -0.23819 |
| `explicit.stat_3639275092@T1` | -0.23819 |
| `explicit.stat_3771516363@T1` | -0.23819 |
| `explicit.stat_3639275092@T2` | -0.23819 |
| `explicit.stat_3484657501@T1` | -0.23818 |

### weapon.twomace — n=1360, R²=-0.3049

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1039491398` | 0.11095 |
| `rune.stat_1509134228` | -0.04007 |
| `explicit.stat_1037193709@T1` | -0.00006 |
| `explicit.stat_3336890334@T1` | -0.00005 |
| `explicit.stat_669069897@T1` | -0.00005 |
| `explicit.stat_821021828@T1` | -0.00005 |
| `explicit.stat_1037193709@T2` | -0.00005 |
| `explicit.stat_821021828@T2` | -0.00005 |
| `explicit.stat_669069897@T2` | -0.00004 |
| `explicit.stat_387439868@T2` | -0.00004 |
| `explicit.stat_1368271171@T1` | -0.00003 |
| `explicit.stat_1940865751@T2` | -0.00003 |

## Coverage (listings per base)

- … **Emerald** — 9083 listings (9083 priced) [0.7–7553463.8 ex]
- … **Sapphire** — 9056 listings (9055 priced) [0.6–7553463.8 ex]
- … **Ruby** — 7016 listings (7015 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 4744 listings (4742 priced) [0.3–4877938.3 ex]
- … **Stellar Amulet** — 3540 listings (3540 priced) [0.3–4547453.5 ex]
- … **Prismatic Ring** — 3358 listings (3357 priced) [0.3–36899.4 ex]
- … **Solar Amulet** — 3285 listings (3280 priced) [0.4–4547453.5 ex]
- … **Gold Amulet** — 3210 listings (3210 priced) [0.5–292542.5 ex]
- … **Amethyst Ring** — 3208 listings (3207 priced) [0.4–71450.3 ex]
- … **Gold Ring** — 3091 listings (3090 priced) [0.4–10825.8 ex]
- … **Dueling Wand** — 3048 listings (3045 priced) [1.0–4877938.3 ex]
- … **Sapphire Ring** — 2550 listings (2550 priced) [0.4–70346.0 ex]
- … **Topaz Ring** — 2531 listings (2531 priced) [1.0–44572.1 ex]
- … **Ruby Ring** — 2464 listings (2464 priced) [0.8–44279.2 ex]
- … **Plate Belt** — 2368 listings (2368 priced) [0.4–4877938.3 ex]
- … **Obliterator Bow** — 2342 listings (2338 priced) [0.3–22139622146.9 ex]
- … **Lapis Amulet** — 2240 listings (2240 priced) [0.4–4547453.5 ex]
- … **Heavy Belt** — 2234 listings (2234 priced) [0.4–4877938.3 ex]
- … **Ancestral Tiara** — 2224 listings (2222 priced) [0.6–5018207.5 ex]
- … **Amber Amulet** — 2222 listings (2222 priced) [0.5–4547453.5 ex]
- … **Jade Amulet** — 2178 listings (2177 priced) [0.4–4547453.5 ex]
- … **Unset Ring** — 2060 listings (2060 priced) [0.4–348686.5 ex]
- … **Bloodstone Amulet** — 2026 listings (2026 priced) [0.4–7275.7 ex]
- … **Pearl Ring** — 1993 listings (1993 priced) [0.4–14467.7 ex]
- … **Azure Amulet** — 1981 listings (1981 priced) [0.4–4877938.3 ex]

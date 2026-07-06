# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-06T23:13:23+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **248209** (248011 priced in exalted)
- Distinct bases: 937 · distinct mods: 2660 · mod rows: 1179527
- Sold signals: **33957** sold · 130347 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-06T23:06:54+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×14.42** (median |log error| 2.6685)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 77% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.09** · typical error ×42.64 · ±30% 9% · n=35651
- Premium segment (60ex+): skill **+0.09** · typical error ×257.31 · ±30% 0% · n=21405

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 4635 | ×13.70 | 4% | +0.03 | +0.06 |
| accessory.amulet | 4434 | ×57.63 | 21% | +0.02 | +0.03 |
| jewel | 3985 | ×8.88 | 6% | +0.03 | +0.06 |
| accessory.belt | 3712 | ×11.25 | 21% | +0.05 | +0.08 |
| armour.chest | 3639 | ×10.26 | 22% | +0.04 | +0.08 |
| armour.helmet | 3554 | ×10.75 | 20% | +0.05 | +0.08 |
| armour.boots | 3357 | ×10.00 | 27% | +0.00 | -0.00 |
| armour.gloves | 3306 | ×10.00 | 26% | -0.00 | -0.00 |
| other | 3079 | ×10.00 | 38% | +0.06 | +0.22 |
| weapon.wand | 2350 | ×20.57 | 19% | +0.07 | +0.05 |
| weapon.bow | 1878 | ×11.39 | 19% | +0.09 | +0.10 |
| weapon.crossbow | 1806 | ×11.24 | 18% | +0.08 | +0.10 |
| weapon.warstaff | 663 | ×40.00 | 26% | +0.01 | -0.00 |
| weapon.sceptre | 625 | ×50.00 | 21% | -0.00 | +0.02 |
| weapon.staff | 604 | ×53.00 | 21% | +0.01 | -0.00 |
| weapon.spear | 563 | ×50.00 | 19% | +0.01 | +0.00 |
| armour.focus | 451 | ×50.00 | 17% | +0.00 | +0.00 |
| armour.quiver | 440 | ×50.00 | 17% | +0.00 | +0.01 |
| armour.shield | 408 | ×10.00 | 20% | +0.00 | +0.01 |
| flask.charm | 348 | ×1.00 | 53% | -0.00 | -0.00 |
| weapon.twomace | 333 | ×10.00 | 23% | +0.07 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=27037, R²=-0.4672

intercept: `1.6064`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `0.04232`  ·  n_top_tier: `0.51919`  ·  corrupted: `2.07196`  ·  n_sockets: `-0.00014`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_2106365538@T1` | 3.90704 |
| `explicit.stat_3291658075@T1` | 3.63199 |
| `explicit.stat_1589917703@T1` | 3.03901 |
| `explicit.stat_101878827@T1` | 1.60697 |
| `explicit.stat_3141070085@T1` | -1.54038 |
| `explicit.stat_2891184298@T1` | 1.20926 |
| `explicit.stat_3917489142@T1` | 1.01348 |
| `explicit.stat_1050105434@T1` | -0.94114 |
| `explicit.stat_2974417149@T1` | 0.82604 |
| `explicit.stat_789117908@T1` | -0.46392 |
| `explicit.stat_2968503605@T1` | 0.38223 |
| `explicit.stat_3141070085` | 0.33454 |

### accessory.ring — n=21168, R²=-1.2544

intercept: `4.7947`  ·  log_price: True  ·  ilvl: `-0.04163`  ·  n_mods: `-0.18709`  ·  n_top_tier: `-0.11848`  ·  corrupted: `0.67953`  ·  n_sockets: `0.58107`  ·  quality: `0.03964`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 5.91090 |
| `explicit.stat_707457662@T2` | 4.47572 |
| `explicit.stat_1379411836@T1` | -2.08187 |
| `explicit.stat_1379411836@T2` | -1.58651 |
| `explicit.stat_2557965901@T2` | 1.04273 |
| `explicit.stat_2923486259@T2` | 0.93144 |
| `explicit.stat_2557965901@T1` | 0.90934 |
| `explicit.stat_707457662` | -0.83109 |
| `explicit.stat_736967255@T1` | 0.79767 |
| `explicit.stat_1368271171@T2` | -0.76938 |
| `explicit.stat_328541901@T1` | 0.67609 |
| `explicit.stat_1754445556@T1` | 0.66038 |

### jewel — n=20899, R²=-0.6111

intercept: `-1.1236`  ·  log_price: True  ·  ilvl: `0.03851`  ·  n_mods: `0.12689`  ·  n_top_tier: `-0.05420`  ·  corrupted: `0.28280`  ·  quality: `0.21121`

| stat_id | coef |
|---|---|
| `explicit.stat_3714003708@T1` | -3.31780 |
| `explicit.stat_1316278494@T1` | -3.29079 |
| `explicit.stat_1569101201@T1` | 3.14521 |
| `explicit.stat_3473929743@T1` | 2.95373 |
| `explicit.stat_1697951953@T1` | -2.83684 |
| `explicit.stat_1869147066@T1` | 2.55452 |
| `explicit.stat_3283482523@T1` | -2.19250 |
| `explicit.stat_3192728503@T1` | -1.91452 |
| `explicit.stat_1405298142@T1` | 1.89061 |
| `explicit.stat_21071013@T1` | -1.74352 |
| `explicit.stat_3780644166@T1` | 1.70026 |
| `explicit.stat_2456523742@T1` | 1.65052 |

### accessory.amulet — n=20239, R²=-2.0824

intercept: `4.1886`  ·  log_price: True  ·  ilvl: `-0.05091`  ·  n_mods: `-0.02503`  ·  n_top_tier: `1.10276`  ·  corrupted: `0.09401`  ·  n_sockets: `2.08614`  ·  quality: `-0.01200`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.88778 |
| `explicit.stat_983749596@T2` | -1.73877 |
| `explicit.stat_3299347043@T1` | -1.56191 |
| `explicit.stat_1202301673@T2` | -1.50618 |
| `explicit.stat_3299347043@T2` | -1.28008 |
| `explicit.stat_2748665614@T1` | -1.22538 |
| `explicit.stat_2748665614@T2` | -1.22526 |
| `explicit.stat_3325883026@T1` | -1.18431 |
| `explicit.stat_3917489142@T1` | -1.17900 |
| `explicit.stat_3917489142@T2` | -1.17725 |
| `explicit.stat_1671376347@T2` | -1.17597 |
| `explicit.stat_3325883026@T2` | -1.17098 |

### accessory.belt — n=16997, R²=-1.3919

intercept: `3.5603`  ·  log_price: True  ·  ilvl: `-0.04300`  ·  n_mods: `-0.01881`  ·  n_top_tier: `0.32508`  ·  corrupted: `0.30892`  ·  n_sockets: `-0.10579`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.19076 |
| `explicit.stat_809229260@T2` | -0.37001 |
| `explicit.stat_1389754388@T1` | -0.36975 |
| `explicit.stat_2881298780@T1` | -0.36173 |
| `explicit.stat_3325883026@T1` | -0.35721 |
| `explicit.stat_4220027924@T2` | -0.34672 |
| `explicit.stat_644456512@T2` | -0.34627 |
| `explicit.stat_3299347043@T2` | -0.34418 |
| `explicit.stat_915769802@T2` | -0.34394 |
| `explicit.stat_915769802@T1` | -0.34148 |
| `explicit.stat_3299347043@T1` | -0.33912 |
| `explicit.stat_51994685@T1` | -0.33345 |

### armour.chest — n=16825, R²=-1.43

intercept: `3.6644`  ·  log_price: True  ·  ilvl: `-0.04524`  ·  n_mods: `-0.01815`  ·  n_top_tier: `0.50347`  ·  corrupted: `0.05290`  ·  n_sockets: `0.01200`  ·  quality: `0.01687`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.82338 |
| `explicit.stat_4015621042@T1` | -0.61397 |
| `explicit.stat_4080418644@T2` | -0.57178 |
| `explicit.stat_915769802@T1` | -0.56089 |
| `explicit.stat_1692879867@T1` | -0.54736 |
| `explicit.stat_3325883026@T2` | -0.54661 |
| `explicit.stat_3261801346@T2` | -0.54652 |
| `explicit.stat_2451402625@T1` | -0.54234 |
| `explicit.stat_986397080@T2` | -0.54158 |
| `explicit.stat_4220027924@T2` | -0.53506 |
| `explicit.stat_4080418644@T1` | -0.52848 |
| `explicit.stat_3321629045@T1` | -0.52618 |

### armour.helmet — n=16460, R²=-1.4343

intercept: `4.3143`  ·  log_price: True  ·  ilvl: `-0.05393`  ·  n_mods: `-0.02472`  ·  n_top_tier: `0.53763`  ·  corrupted: `0.55750`  ·  n_sockets: `0.01027`  ·  quality: `0.01494`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 5.27543 |
| `explicit.stat_2339757871@T1` | -2.92863 |
| `explicit.stat_53045048@T1` | -0.76742 |
| `explicit.stat_4015621042@T2` | -0.66307 |
| `explicit.stat_53045048@T2` | -0.63416 |
| `explicit.stat_1263695895@T1` | -0.61545 |
| `explicit.stat_2162097452@T2` | -0.59708 |
| `explicit.stat_328541901@T2` | -0.59619 |
| `explicit.stat_1062208444@T2` | -0.59180 |
| `explicit.stat_803737631@T2` | -0.58937 |
| `explicit.stat_4080418644@T2` | -0.58584 |
| `explicit.stat_4052037485@T2` | -0.57133 |

### armour.boots — n=15500, R²=-0.253

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.14494`  ·  corrupted: `0.00005`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -0.14503 |
| `desecrated.stat_2250533757@T2` | -0.14501 |
| `explicit.stat_1062208444@T2` | -0.14497 |
| `explicit.stat_3261801346@T2` | -0.14497 |
| `explicit.stat_2451402625@T2` | -0.14497 |
| `explicit.stat_3362812763@T1` | -0.14497 |
| `explicit.stat_3362812763@T2` | -0.14496 |
| `explicit.stat_2923486259@T2` | -0.14496 |
| `explicit.stat_3917489142@T2` | -0.14496 |
| `explicit.stat_99927264@T1` | -0.14495 |
| `explicit.stat_2923486259@T1` | -0.14495 |
| `explicit.stat_1671376347@T2` | -0.14495 |

### armour.gloves — n=15250, R²=-0.2986

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00003`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.09685 |
| `desecrated.stat_4067062424` | 0.04030 |
| `desecrated.stat_3299347043` | 0.00079 |
| `explicit.stat_2339757871@T1` | -0.00022 |
| `explicit.stat_3484657501@T2` | -0.00007 |
| `explicit.stat_2797971005@T2` | -0.00005 |
| `explicit.stat_3362812763@T2` | -0.00004 |
| `explicit.stat_1368271171@T1` | -0.00004 |
| `explicit.stat_681332047@T2` | -0.00004 |
| `explicit.stat_3917489142@T2` | -0.00004 |
| `explicit.stat_4080418644@T1` | -0.00004 |
| `explicit.stat_4015621042@T1` | -0.00004 |

### weapon.wand — n=10761, R²=-1.9038

intercept: `3.5006`  ·  log_price: True  ·  ilvl: `-0.04376`  ·  n_mods: `-0.00839`  ·  n_top_tier: `0.44734`  ·  corrupted: `0.24856`  ·  n_sockets: `-0.00172`  ·  quality: `0.01580`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.58065 |
| `explicit.stat_2254480358@T1` | 1.99016 |
| `explicit.stat_591105508@T1` | 1.93844 |
| `explicit.stat_4226189338@T1` | 1.91951 |
| `explicit.stat_1600707273@T1` | 1.75504 |
| `explicit.stat_1545858329@T1` | 1.36443 |
| `explicit.stat_736967255@T2` | 1.10585 |
| `crafted.stat_124131830` | 0.75585 |
| `explicit.stat_1600707273@T2` | 0.73586 |
| `explicit.stat_737908626@T1` | -0.52197 |
| `explicit.stat_3962278098@T2` | -0.50367 |
| `explicit.stat_737908626@T2` | -0.49096 |

### weapon.bow — n=8822, R²=-1.8262

intercept: `3.4157`  ·  log_price: True  ·  ilvl: `-0.04240`  ·  n_mods: `-0.01263`  ·  n_top_tier: `0.40157`  ·  corrupted: `-0.03448`  ·  n_sockets: `0.00413`  ·  quality: `0.00402`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | 1.86260 |
| `explicit.stat_1202301673@T1` | 1.80298 |
| `desecrated.stat_210067635@T1` | -1.50865 |
| `explicit.stat_518292764@T1` | 1.25161 |
| `crafted.stat_3035140377` | 1.15375 |
| `explicit.stat_55876295@T1` | -0.48858 |
| `explicit.stat_2694482655@T1` | -0.47129 |
| `explicit.stat_1037193709@T1` | -0.46136 |
| `explicit.stat_55876295@T2` | -0.45802 |
| `explicit.stat_3261801346@T1` | -0.45622 |
| `explicit.stat_669069897@T2` | -0.45427 |
| `explicit.stat_3695891184@T2` | -0.44212 |

### weapon.crossbow — n=8379, R²=-1.6525

intercept: `3.5069`  ·  log_price: True  ·  ilvl: `-0.04374`  ·  n_mods: `-0.00931`  ·  n_top_tier: `0.66818`  ·  corrupted: `-0.05528`  ·  n_sockets: `0.01411`  ·  quality: `0.00567`

| stat_id | coef |
|---|---|
| `explicit.stat_709508406@T1` | 1.56607 |
| `explicit.stat_1037193709@T1` | 1.55471 |
| `explicit.stat_2250681686@T2` | -1.46565 |
| `explicit.stat_1202301673@T1` | 1.44178 |
| `rune.stat_55876295` | 1.24611 |
| `rune.stat_2246411426` | -1.12105 |
| `crafted.stat_3035140377` | 1.10802 |
| `explicit.stat_1509134228@T1` | 1.07197 |
| `explicit.stat_2250681686` | 0.88866 |
| `explicit.stat_1202301673@T2` | -0.81154 |
| `explicit.stat_691932474@T1` | -0.78226 |
| `explicit.stat_669069897@T2` | -0.76768 |

### flask.charm — n=4512, R²=-0.1666

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00004`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.04207 |
| `explicit.stat_1056492907` | 2.99567 |
| `explicit.stat_3138344128` | 0.01956 |
| `explicit.stat_1873752457@T2` | -0.00003 |
| `explicit.stat_3196823591@T2` | -0.00003 |
| `explicit.stat_388617051@T2` | -0.00003 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_2541588185@T2` | -0.00003 |
| `explicit.stat_828533480@T1` | -0.00003 |
| `explicit.stat_1873752457` | 0.00003 |
| `explicit.stat_2676834156@T2` | -0.00002 |
| `explicit.stat_828533480@T2` | -0.00002 |

### weapon.warstaff — n=3363, R²=-0.4148

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | -3.41174 |
| `desecrated.stat_2231156303@T1` | -3.41174 |
| `rune.stat_243313994` | 3.29644 |
| `rune.stat_1037193709` | 0.29122 |
| `desecrated.stat_2527686725` | 0.27186 |
| `rune.stat_3336890334` | 0.23018 |
| `rune.stat_2430860292` | -0.11893 |
| `rune.stat_1817052494` | -0.11649 |
| `desecrated.stat_2231156303` | 0.03192 |
| `rune.stat_2077615515` | -0.02033 |
| `desecrated.stat_9187492` | 0.01937 |
| `rune.stat_1509134228` | 0.00183 |

### weapon.sceptre — n=3175, R²=-0.4419

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00711`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 0.50955 |
| `rune.stat_1611856026` | 0.08662 |
| `rune.stat_3984865854` | 0.07621 |
| `desecrated.stat_1050105434` | 0.00887 |
| `desecrated.stat_3984865854` | -0.00376 |
| `explicit.stat_1798257884@T2` | 0.00329 |
| `explicit.stat_1263695895@T1` | 0.00006 |
| `explicit.stat_1250712710@T1` | -0.00003 |
| `explicit.stat_3984865854@T2` | -0.00003 |
| `explicit.stat_101878827@T1` | -0.00002 |
| `explicit.stat_2347036682@T2` | -0.00002 |
| `explicit.stat_3057012405@T1` | 0.00002 |

### weapon.staff — n=3170, R²=-0.4208

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.64582 |
| `rune.stat_3990135792` | -0.12451 |
| `rune.stat_975988108` | -0.11659 |
| `rune.stat_2974417149` | 0.07470 |
| `crafted.stat_124131830` | 0.02313 |
| `explicit.stat_2254480358@T1` | 0.01046 |
| `explicit.stat_3962278098@T2` | 0.00134 |
| `explicit.stat_473429811@T1` | 0.00011 |
| `explicit.stat_124131830@T1` | 0.00004 |
| `explicit.stat_1600707273@T1` | 0.00004 |
| `explicit.stat_124131830@T2` | 0.00004 |
| `explicit.stat_2891184298@T2` | 0.00003 |

### weapon.spear — n=2770, R²=-0.418

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.71687 |
| `crafted.stat_518292764` | 0.88669 |
| `rune.stat_1039491398` | 0.14198 |
| `rune.stat_1509134228` | -0.14158 |
| `explicit.stat_210067635@T1` | 0.01321 |
| `desecrated.stat_1509134228` | 0.00146 |
| `desecrated.stat_691932474` | -0.00123 |
| `crafted.stat_210067635` | 0.00016 |
| `explicit.stat_1263695895@T2` | -0.00004 |
| `explicit.stat_709508406@T1` | 0.00004 |
| `explicit.stat_2694482655@T1` | 0.00004 |
| `explicit.stat_1263695895@T1` | -0.00004 |

### armour.focus — n=2229, R²=-0.2982

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00172`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00001`  ·  quality: `0.00003`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | -4.18330 |
| `desecrated.stat_2910761524@T1` | 0.95969 |
| `desecrated.stat_2910761524` | -0.11547 |
| `crafted.stat_2974417149` | 0.08973 |
| `crafted.stat_4015621042` | 0.06671 |
| `desecrated.stat_4015621042` | 0.02037 |
| `rune.stat_3523867985` | 0.02022 |
| `pseudo.total_chaos_res` | 0.00561 |
| `explicit.stat_2923486259` | -0.00561 |
| `desecrated.stat_274716455` | 0.00513 |
| `desecrated.stat_1671376347` | -0.00470 |
| `desecrated.stat_3372524247` | -0.00469 |

### armour.quiver — n=2115, R²=-0.4631

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00004`

| stat_id | coef |
|---|---|
| `desecrated.stat_3714003708` | 0.00121 |
| `explicit.stat_3759663284@T1` | 0.00015 |
| `explicit.stat_2463230181@T1` | -0.00007 |
| `explicit.stat_681332047@T1` | -0.00004 |
| `explicit.stat_681332047@T2` | -0.00004 |
| `explicit.stat_2321178454@T2` | -0.00004 |
| `explicit.stat_803737631@T2` | -0.00004 |
| `explicit.stat_2463230181@T2` | -0.00003 |
| `explicit.stat_1573130764@T1` | -0.00003 |
| `explicit.stat_1368271171@T2` | -0.00003 |
| `explicit.stat_3714003708@T2` | -0.00003 |
| `explicit.stat_3714003708@T1` | -0.00003 |

### armour.shield — n=1915, R²=-0.3904

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.16283`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.85016 |
| `explicit.stat_1978899297@T2` | -0.34950 |
| `explicit.stat_1978899297` | 0.18665 |
| `explicit.stat_1011760251@T1` | -0.16291 |
| `explicit.stat_2481353198@T1` | -0.16288 |
| `explicit.stat_1011760251@T2` | -0.16287 |
| `explicit.stat_1301765461@T2` | -0.16287 |
| `explicit.stat_2481353198@T2` | -0.16286 |
| `explicit.stat_3484657501@T1` | -0.16285 |
| `explicit.stat_2339757871@T1` | -0.16285 |
| `explicit.stat_3639275092@T1` | -0.16284 |
| `explicit.stat_3639275092@T2` | -0.16284 |

### weapon.twomace — n=1643, R²=-0.3969

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00019`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_518292764@T1` | 0.36961 |
| `rune.stat_1039491398` | 0.11921 |
| `rune.stat_1509134228` | -0.04305 |
| `desecrated.stat_1509134228` | 0.02236 |
| `explicit.stat_1037193709@T1` | -0.00023 |
| `explicit.stat_3336890334@T1` | -0.00023 |
| `explicit.stat_387439868@T2` | -0.00021 |
| `explicit.stat_1037193709@T2` | -0.00021 |
| `explicit.stat_1940865751@T2` | -0.00021 |
| `explicit.stat_669069897@T2` | -0.00021 |
| `explicit.stat_691932474@T2` | -0.00021 |
| `explicit.stat_669069897@T1` | -0.00021 |

## Coverage (listings per base)

- … **Emerald** — 10089 listings (10089 priced) [0.7–7553463.8 ex]
- … **Sapphire** — 10022 listings (10020 priced) [0.4–7553463.8 ex]
- … **Ruby** — 7836 listings (7835 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 5120 listings (5118 priced) [0.3–4877938.3 ex]
- … **Stellar Amulet** — 3836 listings (3836 priced) [0.3–35690283.3 ex]
- … **Prismatic Ring** — 3714 listings (3713 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 3628 listings (3623 priced) [0.4–66666666.0 ex]
- … **Amethyst Ring** — 3545 listings (3544 priced) [0.4–71450.3 ex]
- … **Gold Amulet** — 3502 listings (3502 priced) [0.4–292542.5 ex]
- … **Gold Ring** — 3379 listings (3378 priced) [0.4–24532814.5 ex]
- … **Dueling Wand** — 3346 listings (3343 priced) [0.9–3736768402.2 ex]
- … **Sapphire Ring** — 2800 listings (2799 priced) [0.4–24532814.5 ex]
- … **Topaz Ring** — 2764 listings (2764 priced) [1.0–24532814.5 ex]
- … **Ruby Ring** — 2701 listings (2701 priced) [0.6–146119.1 ex]
- … **Plate Belt** — 2582 listings (2581 priced) [0.4–4877938.3 ex]
- … **Obliterator Bow** — 2542 listings (2536 priced) [0.4–22139622146.9 ex]
- … **Lapis Amulet** — 2468 listings (2468 priced) [0.4–4547453.5 ex]
- … **Ancestral Tiara** — 2435 listings (2433 priced) [0.6–5125681.0 ex]
- … **Heavy Belt** — 2424 listings (2424 priced) [0.4–4877938.3 ex]
- … **Amber Amulet** — 2420 listings (2420 priced) [0.4–4547453.5 ex]
- … **Jade Amulet** — 2404 listings (2403 priced) [0.4–4547453.5 ex]
- … **Unset Ring** — 2268 listings (2268 priced) [0.4–24532814.5 ex]
- … **Bloodstone Amulet** — 2246 listings (2246 priced) [0.4–7275.7 ex]
- … **Pearl Ring** — 2203 listings (2203 priced) [0.4–24532814.5 ex]
- … **Azure Amulet** — 2172 listings (2172 priced) [0.4–4877938.3 ex]

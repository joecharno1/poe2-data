# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-07T00:54:40+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **251730** (251497 priced in exalted)
- Distinct bases: 937 · distinct mods: 2666 · mod rows: 1196079
- Sold signals: **33741** sold · 131826 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-07T00:47:50+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×14.75** (median |log error| 2.6913)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 76% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.08** · typical error ×32.18 · ±30% 13% · n=36037
- Premium segment (60ex+): skill **+0.08** · typical error ×185.71 · ±30% 0% · n=21736

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 4697 | ×13.45 | 4% | +0.03 | +0.06 |
| accessory.amulet | 4503 | ×56.22 | 20% | +0.02 | +0.02 |
| jewel | 4047 | ×8.67 | 6% | +0.05 | +0.07 |
| accessory.belt | 3762 | ×14.45 | 20% | +0.05 | +0.08 |
| armour.chest | 3681 | ×10.00 | 28% | +0.01 | +0.00 |
| armour.helmet | 3508 | ×10.00 | 26% | +0.00 | +0.01 |
| armour.boots | 3380 | ×10.00 | 24% | +0.00 | +0.01 |
| armour.gloves | 3327 | ×10.00 | 23% | -0.00 | +0.01 |
| other | 3078 | ×10.00 | 37% | +0.06 | +0.18 |
| weapon.wand | 2366 | ×21.31 | 20% | +0.07 | +0.04 |
| weapon.bow | 1924 | ×15.06 | 20% | +0.09 | +0.10 |
| weapon.crossbow | 1806 | ×11.05 | 20% | +0.08 | +0.09 |
| weapon.warstaff | 726 | ×45.57 | 25% | +0.01 | -0.00 |
| weapon.sceptre | 701 | ×50.00 | 20% | +0.00 | +0.02 |
| weapon.staff | 671 | ×53.00 | 23% | +0.01 | -0.00 |
| weapon.spear | 540 | ×27.04 | 21% | +0.01 | +0.00 |
| armour.focus | 443 | ×50.00 | 16% | +0.01 | +0.02 |
| armour.quiver | 438 | ×57.00 | 18% | +0.00 | +0.02 |
| armour.shield | 416 | ×10.00 | 19% | +0.00 | +0.01 |
| flask.charm | 350 | ×1.00 | 57% | -0.00 | -0.00 |
| weapon.twomace | 337 | ×13.19 | 23% | +0.09 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=27307, R²=-0.4962

intercept: `1.6065`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `0.03227`  ·  n_top_tier: `0.44218`  ·  corrupted: `2.07086`  ·  n_sockets: `-0.00009`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_2106365538@T1` | 4.06966 |
| `explicit.stat_3291658075@T1` | 2.99338 |
| `explicit.stat_101878827@T1` | 2.32018 |
| `explicit.stat_2891184298@T1` | 1.69671 |
| `explicit.stat_1589917703@T1` | 1.51536 |
| `explicit.stat_2974417149@T1` | 0.97967 |
| `explicit.stat_3917489142@T1` | 0.80187 |
| `explicit.stat_1050105434@T1` | -0.75954 |
| `implicit.stat_1379411836` | -0.27356 |
| `explicit.stat_789117908@T1` | -0.26113 |
| `implicit.stat_4041853756` | 0.22703 |
| `implicit.stat_3879011313` | 0.22702 |

### accessory.ring — n=21486, R²=-1.2482

intercept: `4.8168`  ·  log_price: True  ·  ilvl: `-0.04113`  ·  n_mods: `-0.19447`  ·  n_top_tier: `-0.13861`  ·  corrupted: `0.71162`  ·  n_sockets: `0.58535`  ·  quality: `0.05327`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 5.04221 |
| `explicit.stat_707457662@T2` | 3.74779 |
| `explicit.stat_1379411836@T1` | -2.11904 |
| `explicit.stat_1379411836@T2` | -1.67283 |
| `explicit.stat_2923486259@T2` | 0.97921 |
| `explicit.stat_736967255@T1` | 0.77828 |
| `explicit.stat_1368271171@T2` | -0.75195 |
| `explicit.stat_328541901@T1` | 0.73918 |
| `explicit.stat_2557965901@T2` | 0.70046 |
| `explicit.stat_707457662` | -0.69612 |
| `explicit.stat_4080418644@T2` | 0.61406 |
| `explicit.stat_3372524247@T2` | 0.55832 |

### jewel — n=21259, R²=-0.6038

intercept: `-1.1181`  ·  log_price: True  ·  ilvl: `0.03911`  ·  n_mods: `0.08668`  ·  n_top_tier: `-0.01832`  ·  corrupted: `0.31749`  ·  quality: `0.20880`

| stat_id | coef |
|---|---|
| `explicit.stat_1569101201@T1` | 3.64412 |
| `explicit.stat_3714003708@T1` | -3.52729 |
| `explicit.stat_1316278494@T1` | -3.29426 |
| `explicit.stat_1697951953@T1` | -2.90720 |
| `explicit.stat_3473929743@T1` | 2.80751 |
| `explicit.stat_21071013@T1` | -2.70138 |
| `explicit.stat_153777645@T1` | 2.55685 |
| `explicit.stat_1869147066@T1` | 2.35929 |
| `explicit.stat_3544800472@T1` | -2.03980 |
| `explicit.stat_3192728503@T1` | -1.98762 |
| `explicit.stat_3283482523@T1` | -1.95257 |
| `explicit.stat_293638271@T1` | 1.75023 |

### accessory.amulet — n=20539, R²=-2.06

intercept: `4.3022`  ·  log_price: True  ·  ilvl: `-0.05253`  ·  n_mods: `-0.02316`  ·  n_top_tier: `1.10464`  ·  corrupted: `0.22009`  ·  n_sockets: `2.05750`  ·  quality: `-0.02025`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.70112 |
| `explicit.stat_983749596@T1` | -1.60318 |
| `explicit.stat_983749596@T2` | -1.54180 |
| `explicit.stat_3299347043@T2` | -1.37577 |
| `explicit.stat_2748665614@T2` | -1.23522 |
| `explicit.stat_2748665614@T1` | -1.22683 |
| `explicit.stat_3917489142@T1` | -1.20932 |
| `explicit.stat_3917489142@T2` | -1.19830 |
| `explicit.stat_3325883026@T1` | -1.18895 |
| `explicit.stat_1671376347@T2` | -1.18742 |
| `explicit.stat_3489782002@T2` | -1.16452 |
| `explicit.stat_4080418644@T1` | -1.16133 |

### accessory.belt — n=17200, R²=-1.3914

intercept: `3.6489`  ·  log_price: True  ·  ilvl: `-0.04386`  ·  n_mods: `-0.01986`  ·  n_top_tier: `0.42757`  ·  corrupted: `0.41920`  ·  n_sockets: `-0.11785`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.17725 |
| `explicit.stat_809229260@T2` | -0.47412 |
| `explicit.stat_1389754388@T1` | -0.46530 |
| `explicit.stat_2881298780@T1` | -0.45933 |
| `explicit.stat_3299347043@T2` | -0.45703 |
| `explicit.stat_3325883026@T1` | -0.45062 |
| `explicit.stat_4220027924@T2` | -0.45007 |
| `explicit.stat_3299347043@T1` | -0.44959 |
| `explicit.stat_644456512@T2` | -0.44518 |
| `explicit.stat_51994685@T1` | -0.44223 |
| `explicit.stat_915769802@T1` | -0.44043 |
| `explicit.stat_915769802@T2` | -0.43987 |

### armour.chest — n=17036, R²=-0.2301

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.06784`  ·  corrupted: `0.00006`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_4080418644@T2` | -0.06787 |
| `explicit.stat_3261801346@T1` | -0.06786 |
| `explicit.stat_915769802@T1` | -0.06786 |
| `explicit.stat_915769802@T2` | -0.06786 |
| `explicit.stat_2451402625@T1` | -0.06786 |
| `explicit.stat_3261801346@T2` | -0.06785 |
| `explicit.stat_124859000@T2` | -0.06785 |
| `explicit.stat_2923486259@T1` | -0.06785 |
| `explicit.stat_3033371881@T2` | -0.06785 |
| `explicit.stat_2339757871@T2` | -0.06785 |
| `explicit.stat_3484657501@T2` | -0.06785 |
| `explicit.stat_2451402625@T2` | -0.06784 |

### armour.helmet — n=16662, R²=-0.238

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.15106`  ·  corrupted: `1.01795`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T2` | -0.15108 |
| `explicit.stat_1263695895@T1` | -0.15108 |
| `explicit.stat_3362812763@T1` | -0.15108 |
| `explicit.stat_2451402625@T1` | -0.15108 |
| `explicit.stat_53045048@T2` | -0.15107 |
| `explicit.stat_3362812763@T2` | -0.15107 |
| `explicit.stat_4080418644@T2` | -0.15107 |
| `explicit.stat_3484657501@T2` | -0.15107 |
| `explicit.stat_1062208444@T2` | -0.15107 |
| `explicit.stat_53045048@T1` | -0.15107 |
| `explicit.stat_328541901@T2` | -0.15107 |
| `explicit.stat_803737631@T2` | -0.15107 |

### armour.boots — n=15696, R²=-0.2591

intercept: `2.3032`  ·  log_price: True  ·  ilvl: `-0.00001`  ·  n_mods: `-0.00009`  ·  n_top_tier: `0.12112`  ·  corrupted: `0.00028`  ·  n_sockets: `0.00002`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1062208444@T2` | -0.12163 |
| `desecrated.stat_2250533757@T2` | -0.12150 |
| `explicit.stat_2339757871@T1` | -0.12136 |
| `explicit.stat_2451402625@T2` | -0.12130 |
| `explicit.stat_3362812763@T1` | -0.12130 |
| `explicit.stat_3261801346@T2` | -0.12126 |
| `explicit.stat_3362812763@T2` | -0.12122 |
| `explicit.stat_2923486259@T2` | -0.12121 |
| `explicit.stat_2923486259@T1` | -0.12121 |
| `explicit.stat_3033371881@T2` | -0.12120 |
| `explicit.stat_3917489142@T2` | -0.12119 |
| `explicit.stat_328541901@T1` | -0.12118 |

### armour.gloves — n=15442, R²=-0.3025

intercept: `2.3078`  ·  log_price: True  ·  ilvl: `-0.00023`  ·  n_mods: `-0.00085`  ·  n_top_tier: `0.00218`  ·  corrupted: `0.00146`  ·  n_sockets: `0.00135`  ·  quality: `0.00005`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.09659 |
| `desecrated.stat_4067062424` | 0.05533 |
| `explicit.stat_2339757871@T1` | -0.02593 |
| `desecrated.stat_3299347043` | 0.01067 |
| `explicit.stat_3299347043` | 0.01058 |
| `rune.stat_3299347043` | 0.01057 |
| `pseudo.total_life` | -0.01054 |
| `explicit.stat_3484657501@T2` | -0.00671 |
| `explicit.stat_2797971005@T2` | -0.00630 |
| `explicit.stat_803737631@T2` | -0.00627 |
| `rune.stat_789117908` | -0.00572 |
| `explicit.stat_681332047@T2` | -0.00505 |

### weapon.wand — n=10881, R²=-1.9049

intercept: `3.6236`  ·  log_price: True  ·  ilvl: `-0.04529`  ·  n_mods: `-0.00537`  ·  n_top_tier: `0.42626`  ·  corrupted: `0.18154`  ·  n_sockets: `0.00002`  ·  quality: `0.01508`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.60641 |
| `explicit.stat_2254480358@T1` | 2.02087 |
| `explicit.stat_591105508@T1` | 1.98260 |
| `explicit.stat_4226189338@T1` | 1.95638 |
| `explicit.stat_1600707273@T1` | 1.80455 |
| `explicit.stat_1545858329@T1` | 1.39954 |
| `explicit.stat_736967255@T2` | 1.30261 |
| `explicit.stat_1600707273@T2` | 0.80868 |
| `crafted.stat_124131830` | 0.76531 |
| `explicit.stat_3962278098@T2` | -0.49893 |
| `explicit.stat_737908626@T1` | -0.49318 |
| `explicit.stat_737908626@T2` | -0.46061 |

### weapon.bow — n=8926, R²=-1.8609

intercept: `3.4905`  ·  log_price: True  ·  ilvl: `-0.04314`  ·  n_mods: `-0.01249`  ·  n_top_tier: `0.38833`  ·  corrupted: `-0.04206`  ·  n_sockets: `0.00115`  ·  quality: `0.00339`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | 1.90981 |
| `explicit.stat_1202301673@T1` | 1.85766 |
| `desecrated.stat_210067635@T1` | -1.83023 |
| `explicit.stat_518292764@T1` | 1.36843 |
| `crafted.stat_3035140377` | 1.15885 |
| `explicit.stat_55876295@T1` | -0.45202 |
| `explicit.stat_2694482655@T1` | -0.44499 |
| `explicit.stat_55876295@T2` | -0.43011 |
| `explicit.stat_3261801346@T1` | -0.42940 |
| `explicit.stat_669069897@T2` | -0.42311 |
| `explicit.stat_3695891184@T2` | -0.41479 |
| `explicit.stat_1940865751@T2` | -0.41474 |

### weapon.crossbow — n=8469, R²=-1.712

intercept: `3.5641`  ·  log_price: True  ·  ilvl: `-0.04448`  ·  n_mods: `-0.00132`  ·  n_top_tier: `0.38216`  ·  corrupted: `-0.04967`  ·  n_sockets: `0.00970`  ·  quality: `0.00498`

| stat_id | coef |
|---|---|
| `explicit.stat_709508406@T1` | 1.90126 |
| `explicit.stat_1202301673@T1` | 1.81358 |
| `explicit.stat_1037193709@T1` | 1.80787 |
| `explicit.stat_2250681686@T2` | -1.33281 |
| `rune.stat_55876295` | 1.26244 |
| `explicit.stat_1509134228@T1` | 1.19328 |
| `crafted.stat_3035140377` | 1.16074 |
| `rune.stat_2246411426` | -1.13598 |
| `explicit.stat_2250681686` | 1.01273 |
| `explicit.stat_1202301673@T2` | -0.46581 |
| `explicit.stat_669069897@T1` | -0.43625 |
| `explicit.stat_669069897@T2` | -0.43593 |

### flask.charm — n=4628, R²=-0.1699

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00017`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.04340 |
| `explicit.stat_1056492907` | 2.99555 |
| `explicit.stat_3138344128` | 0.01985 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_3196823591@T2` | -0.00003 |
| `explicit.stat_828533480@T1` | -0.00003 |
| `explicit.stat_388617051@T2` | -0.00003 |
| `explicit.stat_828533480@T2` | -0.00003 |
| `explicit.stat_2541588185@T2` | -0.00003 |
| `explicit.stat_2676834156@T2` | -0.00003 |
| `explicit.stat_1873752457` | 0.00003 |

### weapon.warstaff — n=3423, R²=-0.4214

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | -3.86208 |
| `desecrated.stat_2231156303@T1` | -3.86208 |
| `rune.stat_243313994` | 3.29627 |
| `desecrated.stat_9187492` | 0.52413 |
| `rune.stat_1037193709` | 0.26913 |
| `desecrated.stat_2527686725` | 0.26639 |
| `rune.stat_3336890334` | 0.22995 |
| `rune.stat_2430860292` | -0.11881 |
| `rune.stat_1817052494` | -0.10765 |
| `desecrated.stat_2231156303` | 0.04335 |
| `rune.stat_2077615515` | -0.01998 |
| `rune.stat_1509134228` | 0.00217 |

### weapon.sceptre — n=3248, R²=-0.4497

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00647`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 0.80882 |
| `rune.stat_1611856026` | 0.07984 |
| `rune.stat_3984865854` | 0.06008 |
| `desecrated.stat_1050105434` | 0.01126 |
| `explicit.stat_1798257884@T2` | 0.00341 |
| `desecrated.stat_3984865854` | -0.00091 |
| `explicit.stat_1250712710@T1` | -0.00005 |
| `explicit.stat_3984865854@T2` | -0.00005 |
| `explicit.stat_101878827@T1` | -0.00005 |
| `explicit.stat_1263695895@T1` | 0.00004 |
| `explicit.stat_2347036682@T2` | -0.00004 |
| `explicit.stat_3639275092@T2` | -0.00004 |

### weapon.staff — n=3238, R²=-0.4331

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.64581 |
| `rune.stat_3990135792` | -0.13073 |
| `rune.stat_975988108` | -0.11533 |
| `rune.stat_2974417149` | 0.07843 |
| `explicit.stat_2254480358@T1` | 0.01491 |
| `crafted.stat_124131830` | 0.00820 |
| `explicit.stat_473429811@T1` | 0.00037 |
| `explicit.stat_124131830@T1` | 0.00005 |
| `explicit.stat_3962278098@T2` | 0.00004 |
| `explicit.stat_1600707273@T1` | 0.00004 |
| `explicit.stat_124131830@T2` | 0.00004 |
| `explicit.stat_2891184298@T2` | 0.00003 |

### weapon.spear — n=2844, R²=-0.4628

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1039491398` | 0.13375 |
| `rune.stat_1509134228` | -0.13363 |
| `explicit.stat_210067635@T1` | 0.06539 |
| `explicit.stat_1263695895@T2` | -0.00004 |
| `explicit.stat_1263695895@T1` | -0.00003 |
| `explicit.stat_2694482655@T1` | 0.00003 |
| `explicit.stat_709508406@T1` | 0.00003 |
| `explicit.stat_3639275092@T1` | 0.00002 |
| `explicit.stat_1509134228@T1` | 0.00002 |
| `explicit.stat_691932474@T1` | -0.00002 |
| `explicit.stat_4080418644@T1` | -0.00002 |
| `explicit.stat_3639275092@T2` | 0.00002 |

### armour.focus — n=2278, R²=-0.3241

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00014`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00001`  ·  quality: `0.00007`

| stat_id | coef |
|---|---|
| `desecrated.stat_2910761524@T1` | 0.95283 |
| `crafted.stat_2974417149@T1` | -0.56362 |
| `desecrated.stat_378817135@T1` | -0.26470 |
| `desecrated.stat_2910761524` | -0.11407 |
| `crafted.stat_4015621042` | 0.06671 |
| `desecrated.stat_378817135` | 0.05973 |
| `crafted.stat_2974417149` | 0.04065 |
| `desecrated.stat_4015621042` | 0.02037 |
| `rune.stat_3523867985` | 0.01858 |
| `pseudo.total_chaos_res` | 0.00557 |
| `explicit.stat_2923486259` | -0.00557 |
| `desecrated.stat_274716455` | 0.00519 |

### armour.quiver — n=2178, R²=-0.4705

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00004`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.90399 |
| `desecrated.stat_3932115504` | 0.13610 |
| `desecrated.stat_2194114101` | 0.01720 |
| `explicit.stat_3759663284@T1` | 0.00053 |
| `explicit.stat_2463230181@T1` | -0.00009 |
| `desecrated.stat_3714003708` | 0.00007 |
| `desecrated.stat_1754445556` | 0.00006 |
| `explicit.stat_681332047@T1` | -0.00005 |
| `explicit.stat_681332047@T2` | -0.00005 |
| `explicit.stat_2463230181@T2` | -0.00005 |
| `explicit.stat_803737631@T2` | -0.00005 |
| `explicit.stat_2321178454@T2` | -0.00005 |

### armour.shield — n=1952, R²=-0.4039

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.17885`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00001`  ·  quality: `0.00017`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.84576 |
| `explicit.stat_1978899297@T2` | -0.35987 |
| `explicit.stat_1978899297` | 0.18100 |
| `explicit.stat_1011760251@T1` | -0.17894 |
| `explicit.stat_2481353198@T1` | -0.17890 |
| `explicit.stat_1011760251@T2` | -0.17889 |
| `explicit.stat_1301765461@T2` | -0.17889 |
| `explicit.stat_2481353198@T2` | -0.17889 |
| `explicit.stat_2339757871@T1` | -0.17887 |
| `explicit.stat_3484657501@T1` | -0.17887 |
| `explicit.stat_3639275092@T1` | -0.17887 |
| `explicit.stat_328541901@T1` | -0.17886 |

### weapon.twomace — n=1675, R²=-0.4089

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00786`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_518292764@T1` | 0.44118 |
| `rune.stat_1039491398` | 0.13225 |
| `rune.stat_1509134228` | -0.04776 |
| `desecrated.stat_1509134228` | 0.01986 |
| `explicit.stat_1509134228@T1` | 0.01400 |
| `explicit.stat_3336890334@T1` | -0.00791 |
| `explicit.stat_1037193709@T1` | -0.00791 |
| `explicit.stat_1037193709@T2` | -0.00789 |
| `explicit.stat_387439868@T2` | -0.00789 |
| `explicit.stat_1940865751@T2` | -0.00788 |
| `explicit.stat_691932474@T2` | -0.00788 |
| `explicit.stat_9187492@T1` | -0.00787 |

## Coverage (listings per base)

- … **Emerald** — 10259 listings (10252 priced) [0.7–7553463.8 ex]
- … **Sapphire** — 10199 listings (10187 priced) [0.4–7553463.8 ex]
- … **Ruby** — 7969 listings (7959 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 5165 listings (5162 priced) [0.3–4877938.3 ex]
- … **Stellar Amulet** — 3877 listings (3877 priced) [0.3–35690283.3 ex]
- … **Prismatic Ring** — 3762 listings (3761 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 3690 listings (3685 priced) [0.4–66666666.0 ex]
- … **Amethyst Ring** — 3602 listings (3601 priced) [0.4–71450.3 ex]
- … **Gold Amulet** — 3549 listings (3549 priced) [0.4–292542.5 ex]
- … **Gold Ring** — 3422 listings (3421 priced) [0.4–24532814.5 ex]
- … **Dueling Wand** — 3385 listings (3382 priced) [0.8–3736768402.2 ex]
- … **Sapphire Ring** — 2844 listings (2843 priced) [0.4–24532814.5 ex]
- … **Topaz Ring** — 2810 listings (2810 priced) [1.0–24532814.5 ex]
- … **Ruby Ring** — 2743 listings (2743 priced) [0.4–146119.1 ex]
- … **Plate Belt** — 2615 listings (2613 priced) [0.4–4877938.3 ex]
- … **Obliterator Bow** — 2571 listings (2565 priced) [0.4–22139622146.9 ex]
- … **Lapis Amulet** — 2506 listings (2506 priced) [0.4–4547453.5 ex]
- … **Ancestral Tiara** — 2487 listings (2485 priced) [0.6–5125681.0 ex]
- … **Heavy Belt** — 2459 listings (2459 priced) [0.4–4877938.3 ex]
- … **Amber Amulet** — 2452 listings (2452 priced) [0.4–4547453.5 ex]
- … **Jade Amulet** — 2434 listings (2433 priced) [0.4–4547453.5 ex]
- … **Unset Ring** — 2296 listings (2296 priced) [0.4–24532814.5 ex]
- … **Bloodstone Amulet** — 2276 listings (2276 priced) [0.4–7275.7 ex]
- … **Pearl Ring** — 2230 listings (2230 priced) [0.4–24532814.5 ex]
- … **Azure Amulet** — 2199 listings (2199 priced) [0.4–4877938.3 ex]

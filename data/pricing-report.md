# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-06T18:32:27+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **236485** (236304 priced in exalted)
- Distinct bases: 934 · distinct mods: 2636 · mod rows: 1123062
- Sold signals: **34615** sold · 123572 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-06T18:25:12+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×15.12** (median |log error| 2.7157)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 76% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.10** · typical error ×51.46 · ±30% 9% · n=33889
- Premium segment (60ex+): skill **+0.10** · typical error ×248.39 · ±30% 0% · n=20467

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 4370 | ×13.01 | 4% | +0.04 | +0.07 |
| accessory.amulet | 4207 | ×56.51 | 19% | +0.02 | +0.03 |
| jewel | 3738 | ×8.45 | 6% | +0.05 | +0.07 |
| accessory.belt | 3569 | ×15.03 | 20% | +0.04 | +0.08 |
| armour.chest | 3490 | ×10.31 | 21% | +0.05 | +0.08 |
| armour.helmet | 3336 | ×10.84 | 19% | +0.05 | +0.07 |
| armour.boots | 3215 | ×10.00 | 26% | +0.01 | +0.01 |
| armour.gloves | 3137 | ×10.82 | 26% | +0.00 | +0.01 |
| other | 2940 | ×10.00 | 34% | +0.21 | +0.12 |
| weapon.wand | 2243 | ×23.34 | 21% | +0.06 | +0.06 |
| weapon.bow | 1778 | ×11.29 | 19% | +0.08 | +0.09 |
| weapon.crossbow | 1711 | ×13.23 | 20% | +0.08 | +0.10 |
| weapon.warstaff | 624 | ×40.00 | 24% | +0.00 | +0.00 |
| weapon.sceptre | 564 | ×50.00 | 18% | +0.00 | +0.01 |
| weapon.staff | 561 | ×50.00 | 20% | +0.00 | +0.00 |
| weapon.spear | 540 | ×40.00 | 20% | +0.00 | +0.00 |
| armour.focus | 431 | ×40.00 | 16% | -0.00 | -0.00 |
| armour.quiver | 411 | ×40.00 | 18% | +0.00 | +0.00 |
| armour.shield | 378 | ×10.00 | 16% | +0.00 | +0.00 |
| flask.charm | 302 | ×20.00 | 44% | -0.00 | +0.00 |
| weapon.twomace | 285 | ×10.00 | 19% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=26160, R²=-0.3695

intercept: `1.6065`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `0.06586`  ·  n_top_tier: `1.23195`  ·  corrupted: `2.95513`  ·  n_sockets: `-0.00028`  ·  quality: `-0.00003`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 2.75715 |
| `explicit.stat_2891184298@T1` | 2.67865 |
| `explicit.stat_1050105434@T1` | -2.62441 |
| `explicit.stat_3141070085@T1` | 2.37664 |
| `explicit.stat_101878827@T1` | 2.32226 |
| `explicit.stat_1589917703@T1` | 2.32011 |
| `explicit.stat_3917489142@T1` | 2.26410 |
| `explicit.stat_2106365538@T1` | 2.09147 |
| `explicit.stat_789117908@T1` | -1.85435 |
| `explicit.stat_2974417149@T1` | 1.09856 |
| `explicit.stat_2968503605@T1` | 0.29821 |
| `implicit.stat_1379411836` | -0.27925 |

### accessory.ring — n=20169, R²=-1.2857

intercept: `4.3530`  ·  log_price: True  ·  ilvl: `-0.03831`  ·  n_mods: `-0.13697`  ·  n_top_tier: `-0.25621`  ·  corrupted: `0.82283`  ·  n_sockets: `1.05139`  ·  quality: `0.03966`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 5.19789 |
| `explicit.stat_707457662@T2` | 3.73265 |
| `explicit.stat_2557965901@T1` | 3.48424 |
| `explicit.stat_2557965901@T2` | 2.99905 |
| `explicit.stat_1379411836@T1` | -1.95351 |
| `explicit.stat_2923486259@T2` | 1.43013 |
| `explicit.stat_2923486259@T1` | 1.16864 |
| `explicit.stat_1379411836@T2` | -1.15453 |
| `explicit.stat_736967255@T1` | 1.04095 |
| `explicit.stat_1754445556@T1` | 0.86539 |
| `explicit.stat_3032590688@T2` | 0.83812 |
| `explicit.stat_3372524247@T2` | 0.78131 |

### jewel — n=19757, R²=-0.6364

intercept: `-1.1795`  ·  log_price: True  ·  ilvl: `0.03932`  ·  n_mods: `0.14243`  ·  n_top_tier: `-0.11668`  ·  corrupted: `0.12547`  ·  quality: `0.21785`

| stat_id | coef |
|---|---|
| `explicit.stat_3824372849@T1` | 3.83452 |
| `explicit.stat_3714003708@T1` | -3.68736 |
| `explicit.stat_1316278494@T1` | -3.38860 |
| `explicit.stat_1697951953@T1` | -3.14052 |
| `explicit.stat_1569101201@T1` | 2.56691 |
| `explicit.stat_3473929743@T1` | 2.35328 |
| `explicit.stat_2456523742@T1` | 2.08872 |
| `explicit.stat_21071013@T1` | -2.03476 |
| `explicit.stat_416040624@T1` | -1.96997 |
| `explicit.stat_2106365538@T1` | -1.75612 |
| `explicit.stat_293638271@T1` | 1.67916 |
| `explicit.stat_2594634307@T1` | 1.66642 |

### accessory.amulet — n=19311, R²=-2.0786

intercept: `4.0320`  ·  log_price: True  ·  ilvl: `-0.04912`  ·  n_mods: `-0.02317`  ·  n_top_tier: `0.40867`  ·  corrupted: `0.06712`  ·  n_sockets: `1.90933`  ·  quality: `-0.05903`

| stat_id | coef |
|---|---|
| `explicit.stat_3981240776@T2` | 1.64544 |
| `explicit.stat_3981240776@T1` | 1.43970 |
| `explicit.stat_983749596@T1` | -1.37618 |
| `explicit.stat_983749596@T2` | -1.17593 |
| `explicit.stat_124131830` | 1.16222 |
| `explicit.stat_1202301673` | 0.89437 |
| `explicit.stat_1202301673@T2` | -0.84255 |
| `explicit.stat_3372524247@T1` | 0.80964 |
| `explicit.stat_3299347043@T1` | -0.63383 |
| `explicit.stat_3299347043@T2` | -0.52117 |
| `explicit.stat_3917489142@T1` | -0.49537 |
| `explicit.stat_3917489142@T2` | -0.49526 |

### accessory.belt — n=16301, R²=-1.3671

intercept: `3.4660`  ·  log_price: True  ·  ilvl: `-0.04170`  ·  n_mods: `-0.02011`  ·  n_top_tier: `0.05011`  ·  corrupted: `0.84042`  ·  n_sockets: `-0.10253`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.17561 |
| `explicit.stat_1836676211@T1` | 0.17730 |
| `explicit.stat_3372524247@T1` | 0.13271 |
| `pseudo.total_ele_res>=80` | 0.12756 |
| `explicit.stat_3299347043@T1` | -0.12073 |
| `explicit.stat_2923486259@T1` | 0.09721 |
| `explicit.stat_2923486259@T2` | 0.08990 |
| `explicit.stat_809229260@T2` | -0.08703 |
| `explicit.stat_2881298780@T1` | -0.08370 |
| `explicit.stat_3299347043@T2` | -0.08283 |
| `explicit.stat_1389754388@T1` | -0.08061 |
| `explicit.stat_174664100` | 0.08057 |

### armour.chest — n=16147, R²=-1.3594

intercept: `3.8473`  ·  log_price: True  ·  ilvl: `-0.04749`  ·  n_mods: `-0.02319`  ·  n_top_tier: `0.51651`  ·  corrupted: `0.16230`  ·  n_sockets: `0.01964`  ·  quality: `0.02131`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.86229 |
| `explicit.stat_3981240776@T1` | 1.14862 |
| `explicit.stat_4015621042@T1` | -0.70551 |
| `explicit.stat_4080418644@T2` | -0.60764 |
| `explicit.stat_3261801346@T2` | -0.56887 |
| `explicit.stat_915769802@T1` | -0.56267 |
| `explicit.stat_1692879867@T1` | -0.55965 |
| `explicit.stat_3321629045@T1` | -0.55674 |
| `explicit.stat_3325883026@T2` | -0.55336 |
| `explicit.stat_3981240776@T2` | 0.55180 |
| `explicit.stat_986397080@T2` | -0.55103 |
| `explicit.stat_4220027924@T2` | -0.54776 |

### armour.helmet — n=15774, R²=-1.4092

intercept: `4.3216`  ·  log_price: True  ·  ilvl: `-0.05402`  ·  n_mods: `-0.02222`  ·  n_top_tier: `0.57734`  ·  corrupted: `0.36111`  ·  n_sockets: `0.00019`  ·  quality: `0.01493`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.57285 |
| `explicit.stat_2339757871@T1` | -3.66049 |
| `explicit.stat_53045048@T1` | -0.77991 |
| `explicit.stat_2162097452@T2` | -0.68951 |
| `explicit.stat_1263695895@T1` | -0.67596 |
| `explicit.stat_53045048@T2` | -0.66715 |
| `explicit.stat_4015621042@T2` | -0.65697 |
| `explicit.stat_1062208444@T2` | -0.64870 |
| `explicit.stat_803737631@T2` | -0.64802 |
| `explicit.stat_4080418644@T2` | -0.63392 |
| `explicit.stat_328541901@T2` | -0.62584 |
| `explicit.stat_3033371881@T1` | -0.61976 |

### armour.boots — n=14868, R²=-0.2079

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.39066`  ·  corrupted: `0.00079`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2250533757@T2` | -0.60524 |
| `explicit.stat_2339757871@T1` | -0.39070 |
| `explicit.stat_3362812763@T2` | -0.39067 |
| `explicit.stat_2923486259@T2` | -0.39067 |
| `explicit.stat_2451402625@T2` | -0.39067 |
| `explicit.stat_3917489142@T2` | -0.39067 |
| `explicit.stat_3261801346@T2` | -0.39067 |
| `explicit.stat_124859000@T1` | -0.39067 |
| `explicit.stat_3362812763@T1` | -0.39066 |
| `explicit.stat_99927264@T2` | -0.39066 |
| `explicit.stat_3325883026@T1` | -0.39066 |
| `explicit.stat_1062208444@T1` | -0.39066 |

### armour.gloves — n=14621, R²=-0.285

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00163`  ·  corrupted: `0.06948`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.09452 |
| `desecrated.stat_4067062424` | 0.08565 |
| `desecrated.stat_1573130764` | 0.04149 |
| `explicit.stat_3372524247@T1` | 0.03716 |
| `pseudo.total_ele_res>=80` | 0.01990 |
| `explicit.stat_4067062424@T1` | 0.01611 |
| `pseudo.total_life` | 0.01155 |
| `explicit.stat_3299347043` | -0.01155 |
| `rune.stat_3299347043` | -0.01155 |
| `desecrated.stat_3299347043` | -0.00799 |
| `explicit.stat_9187492@T2` | -0.00235 |
| `explicit.stat_9187492@T1` | 0.00202 |

### weapon.wand — n=10336, R²=-1.9024

intercept: `3.5707`  ·  log_price: True  ·  ilvl: `-0.04463`  ·  n_mods: `-0.00712`  ·  n_top_tier: `0.34387`  ·  corrupted: `0.04314`  ·  n_sockets: `0.00039`  ·  quality: `0.02254`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.72522 |
| `explicit.stat_2254480358@T1` | 2.06939 |
| `explicit.stat_4226189338@T1` | 2.04660 |
| `explicit.stat_591105508@T1` | 2.04553 |
| `explicit.stat_1600707273@T1` | 1.60737 |
| `explicit.stat_736967255@T2` | 1.04975 |
| `explicit.stat_1600707273@T2` | 0.86822 |
| `crafted.stat_124131830` | 0.76651 |
| `explicit.stat_1545858329@T1` | 0.46861 |
| `explicit.stat_3962278098@T2` | -0.41786 |
| `explicit.stat_737908626@T2` | -0.40769 |
| `explicit.stat_737908626@T1` | -0.39902 |

### weapon.bow — n=8483, R²=-1.7893

intercept: `3.4810`  ·  log_price: True  ·  ilvl: `-0.04318`  ·  n_mods: `-0.01347`  ·  n_top_tier: `0.44908`  ·  corrupted: `-0.03111`  ·  n_sockets: `0.00119`  ·  quality: `0.00482`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 1.80550 |
| `explicit.stat_2463230181@T1` | 1.76087 |
| `desecrated.stat_210067635@T1` | -1.62469 |
| `crafted.stat_3035140377` | 1.36963 |
| `explicit.stat_518292764@T1` | 1.34178 |
| `desecrated.stat_666077204@T1` | -0.98393 |
| `rune.stat_3885405204` | -0.62603 |
| `explicit.stat_55876295@T1` | -0.53067 |
| `explicit.stat_2694482655@T1` | -0.51630 |
| `explicit.stat_1037193709@T1` | -0.51560 |
| `explicit.stat_3261801346@T1` | -0.50411 |
| `explicit.stat_669069897@T2` | -0.49303 |

### weapon.crossbow — n=8033, R²=-1.668

intercept: `3.5586`  ·  log_price: True  ·  ilvl: `-0.04450`  ·  n_mods: `-0.00565`  ·  n_top_tier: `0.49162`  ·  corrupted: `-0.05087`  ·  n_sockets: `0.01224`  ·  quality: `0.00315`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 1.74407 |
| `explicit.stat_709508406@T1` | 1.68313 |
| `explicit.stat_1202301673@T1` | 1.67404 |
| `explicit.stat_1509134228@T1` | 1.61603 |
| `explicit.stat_2250681686@T2` | -1.38107 |
| `crafted.stat_3035140377` | 1.12140 |
| `explicit.stat_2250681686` | 0.97259 |
| `explicit.stat_691932474@T1` | -0.72078 |
| `rune.stat_2246411426` | -0.65885 |
| `rune.stat_55876295` | 0.65431 |
| `explicit.stat_1202301673@T2` | -0.60571 |
| `explicit.stat_669069897@T2` | -0.58351 |

### flask.charm — n=4122, R²=-0.141

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00016`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60502 |
| `explicit.stat_1056492907` | 2.99557 |
| `explicit.stat_3138344128` | 0.01956 |
| `explicit.stat_1873752457` | 0.00003 |
| `explicit.stat_1873752457@T2` | -0.00003 |
| `explicit.stat_828533480@T2` | -0.00003 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_828533480@T1` | -0.00003 |
| `explicit.stat_2541588185@T2` | -0.00002 |
| `explicit.stat_388617051@T2` | -0.00002 |
| `explicit.stat_3196823591@T2` | -0.00002 |
| `explicit.stat_2676834156@T2` | -0.00002 |

### weapon.warstaff — n=3054, R²=-0.3684

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 0.83896 |
| `rune.stat_1037193709` | 0.27625 |
| `rune.stat_3336890334` | 0.16819 |
| `rune.stat_1817052494` | -0.11050 |
| `rune.stat_2430860292` | -0.08690 |
| `rune.stat_1509134228` | 0.00149 |
| `rune.stat_1039491398` | -0.00134 |
| `desecrated.stat_9187492` | 0.00053 |
| `crafted.stat_210067635@T2` | 0.00029 |
| `explicit.stat_1509134228@T2` | 0.00004 |
| `desecrated.stat_518292764` | -0.00003 |
| `explicit.stat_9187492@T1` | 0.00002 |

### weapon.sceptre — n=2888, R²=-0.3969

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00001`  ·  quality: `0.00004`

| stat_id | coef |
|---|---|
| `rune.stat_3984865854` | 0.04853 |
| `rune.stat_1611856026` | 0.02427 |
| `explicit.stat_2162097452@T1` | 0.02003 |
| `desecrated.stat_1050105434` | 0.01276 |
| `desecrated.stat_3984865854` | -0.00541 |
| `explicit.stat_1263695895@T1` | 0.00008 |
| `explicit.stat_1263695895@T2` | 0.00004 |
| `explicit.stat_1798257884@T2` | 0.00004 |
| `explicit.stat_3057012405@T1` | 0.00003 |
| `explicit.stat_2162097452@T2` | 0.00003 |
| `explicit.stat_4010677958@T1` | 0.00003 |
| `explicit.stat_101878827@T2` | 0.00002 |

### weapon.staff — n=2882, R²=-0.3568

intercept: `-0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.64584 |
| `rune.stat_3990135792` | -0.13414 |
| `rune.stat_975988108` | -0.11467 |
| `rune.stat_2974417149` | 0.08048 |
| `explicit.stat_473429811@T1` | 0.00079 |
| `explicit.stat_3962278098@T2` | 0.00005 |
| `explicit.stat_124131830@T1` | 0.00004 |
| `explicit.stat_2254480358@T1` | 0.00004 |
| `crafted.stat_124131830` | 0.00003 |
| `explicit.stat_124131830@T2` | 0.00003 |
| `explicit.stat_3278136794@T2` | 0.00003 |
| `explicit.stat_1545858329@T1` | 0.00003 |

### weapon.spear — n=2510, R²=-0.3502

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.49787 |
| `crafted.stat_518292764` | 0.72874 |
| `rune.stat_1509134228` | -0.00633 |
| `rune.stat_1039491398` | 0.00632 |
| `explicit.stat_210067635@T1` | 0.00006 |
| `explicit.stat_1263695895@T2` | -0.00004 |
| `explicit.stat_1263695895@T1` | -0.00004 |
| `explicit.stat_2694482655@T1` | 0.00003 |
| `explicit.stat_1940865751@T1` | 0.00003 |
| `explicit.stat_709508406@T1` | 0.00002 |
| `explicit.stat_3639275092@T1` | 0.00002 |
| `explicit.stat_1509134228@T1` | 0.00002 |

### armour.focus — n=2069, R²=-0.2129

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00004`  ·  corrupted: `-0.00006`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -7.53290 |
| `crafted.stat_2974417149@T1` | -3.46081 |
| `desecrated.stat_2910761524@T1` | 0.93304 |
| `desecrated.stat_3393628375` | 0.53778 |
| `desecrated.stat_2910761524` | -0.11103 |
| `crafted.stat_4015621042` | 0.06673 |
| `crafted.stat_2974417149` | 0.06403 |
| `desecrated.stat_4015621042` | 0.03537 |
| `desecrated.stat_274716455` | 0.00513 |
| `desecrated.stat_1671376347` | -0.00465 |
| `desecrated.stat_3372524247` | -0.00465 |
| `explicit.stat_4220027924` | -0.00465 |

### armour.quiver — n=1959, R²=-0.3968

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00003`

| stat_id | coef |
|---|---|
| `desecrated.stat_3759663284` | 0.00033 |
| `explicit.stat_2463230181@T1` | -0.00008 |
| `explicit.stat_2463230181@T2` | -0.00004 |
| `explicit.stat_681332047@T1` | -0.00004 |
| `explicit.stat_681332047@T2` | -0.00004 |
| `explicit.stat_803737631@T2` | -0.00004 |
| `explicit.stat_3714003708@T2` | -0.00004 |
| `explicit.stat_3714003708@T1` | -0.00004 |
| `explicit.stat_1368271171@T2` | -0.00004 |
| `explicit.stat_1573130764@T1` | -0.00003 |
| `explicit.stat_2321178454@T2` | -0.00003 |
| `explicit.stat_3032590688@T2` | -0.00003 |

### armour.shield — n=1754, R²=-0.3283

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.10882`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.67496 |
| `explicit.stat_1978899297@T2` | -0.26625 |
| `explicit.stat_1301765461@T1` | 0.21711 |
| `explicit.stat_1978899297` | 0.15741 |
| `explicit.stat_1011760251@T1` | -0.10888 |
| `explicit.stat_2481353198@T1` | -0.10885 |
| `explicit.stat_1301765461@T2` | -0.10884 |
| `explicit.stat_2481353198@T2` | -0.10884 |
| `explicit.stat_3639275092@T1` | -0.10884 |
| `explicit.stat_3639275092@T2` | -0.10883 |
| `explicit.stat_2339757871@T1` | -0.10883 |
| `explicit.stat_3771516363@T1` | -0.10883 |

### weapon.twomace — n=1494, R²=-0.3666

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00004`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1039491398` | 0.11922 |
| `rune.stat_1509134228` | -0.04305 |
| `explicit.stat_518292764@T1` | 0.00229 |
| `explicit.stat_1037193709@T1` | -0.00008 |
| `explicit.stat_3336890334@T1` | -0.00008 |
| `explicit.stat_1037193709@T2` | -0.00007 |
| `explicit.stat_669069897@T1` | -0.00006 |
| `explicit.stat_669069897@T2` | -0.00006 |
| `explicit.stat_387439868@T2` | -0.00006 |
| `explicit.stat_691932474@T1` | -0.00005 |
| `explicit.stat_821021828@T1` | -0.00005 |
| `explicit.stat_1940865751@T2` | -0.00005 |

## Coverage (listings per base)

- … **Emerald** — 9595 listings (9595 priced) [0.7–7553463.8 ex]
- … **Sapphire** — 9506 listings (9505 priced) [0.6–7553463.8 ex]
- … **Ruby** — 7444 listings (7443 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 4944 listings (4942 priced) [0.3–4877938.3 ex]
- … **Stellar Amulet** — 3698 listings (3698 priced) [0.3–4547453.5 ex]
- … **Prismatic Ring** — 3548 listings (3547 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 3465 listings (3460 priced) [0.4–4906562.9 ex]
- … **Amethyst Ring** — 3375 listings (3374 priced) [0.4–71450.3 ex]
- … **Gold Amulet** — 3355 listings (3355 priced) [0.5–292542.5 ex]
- … **Gold Ring** — 3217 listings (3216 priced) [0.4–24532814.5 ex]
- … **Dueling Wand** — 3209 listings (3206 priced) [1.0–3736768402.2 ex]
- … **Sapphire Ring** — 2684 listings (2684 priced) [0.4–24532814.5 ex]
- … **Topaz Ring** — 2655 listings (2655 priced) [1.0–24532814.5 ex]
- … **Ruby Ring** — 2580 listings (2580 priced) [0.6–146119.1 ex]
- … **Plate Belt** — 2473 listings (2473 priced) [0.4–4877938.3 ex]
- … **Obliterator Bow** — 2449 listings (2444 priced) [0.3–22139622146.9 ex]
- … **Lapis Amulet** — 2357 listings (2357 priced) [0.4–4547453.5 ex]
- … **Ancestral Tiara** — 2332 listings (2330 priced) [0.6–5018207.5 ex]
- … **Heavy Belt** — 2329 listings (2329 priced) [0.4–4877938.3 ex]
- … **Amber Amulet** — 2317 listings (2317 priced) [0.5–4547453.5 ex]
- … **Jade Amulet** — 2303 listings (2302 priced) [0.4–4547453.5 ex]
- … **Unset Ring** — 2150 listings (2150 priced) [0.4–24532814.5 ex]
- … **Bloodstone Amulet** — 2130 listings (2130 priced) [0.4–7275.7 ex]
- … **Pearl Ring** — 2096 listings (2096 priced) [0.4–24532814.5 ex]
- … **Azure Amulet** — 2064 listings (2064 priced) [0.4–4877938.3 ex]

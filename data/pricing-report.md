# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-19T10:10:00+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **647250** (645242 priced in exalted)
- Distinct bases: 995 · distinct mods: 3274 · mod rows: 3065866
- Sold signals: **24643** sold · 368118 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-19T09:55:44+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×21.48** (median |log error| 3.0672)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.15** · typical error ×61.84 · ±30% 5% · n=94362
- Premium segment (60ex+): skill **+0.15** · typical error ×306.89 · ±30% 0% · n=63843

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 13582 | ×53.42 | 21% | +0.03 | +0.05 |
| jewel | 12956 | ×10.46 | 4% | +0.10 | +0.13 |
| accessory.amulet | 12292 | ×38.44 | 18% | +0.04 | +0.03 |
| accessory.belt | 8970 | ×21.00 | 19% | +0.06 | +0.08 |
| armour.chest | 8622 | ×16.06 | 21% | +0.08 | +0.10 |
| armour.helmet | 8510 | ×20.84 | 12% | +0.10 | +0.11 |
| armour.boots | 7894 | ×25.92 | 21% | +0.09 | +0.11 |
| armour.gloves | 7722 | ×33.97 | 16% | +0.08 | +0.10 |
| other | 7599 | ×2.00 | 43% | +0.10 | +0.17 |
| weapon.wand | 4635 | ×49.12 | 17% | +0.09 | +0.11 |
| weapon.bow | 3650 | ×28.41 | 13% | +0.14 | +0.14 |
| weapon.crossbow | 3421 | ×29.95 | 16% | +0.10 | +0.14 |
| weapon.warstaff | 2248 | ×23.17 | 7% | +0.20 | +0.21 |
| weapon.staff | 2153 | ×29.65 | 5% | +0.17 | +0.15 |
| weapon.sceptre | 2144 | ×26.85 | 5% | +0.13 | +0.13 |
| weapon.spear | 1713 | ×23.03 | 8% | +0.12 | +0.13 |
| armour.focus | 1433 | ×20.54 | 6% | +0.11 | +0.13 |
| armour.quiver | 1362 | ×25.46 | 7% | +0.16 | +0.17 |
| armour.shield | 1119 | ×17.88 | 8% | +0.08 | +0.10 |
| flask.charm | 1081 | ×13.28 | 30% | -0.00 | +0.03 |
| weapon.twomace | 1033 | ×7.33 | 9% | +0.09 | +0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=70183, R²=-0.9556

intercept: `-1.9025`  ·  log_price: True  ·  ilvl: `0.02565`  ·  n_mods: `0.88314`  ·  n_top_tier: `-0.34479`  ·  corrupted: `0.36154`  ·  quality: `-0.00286`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.45059 |
| `explicit.stat_3485067555@T1` | 2.38209 |
| `explicit.stat_3374165039@T1` | -2.24392 |
| `explicit.stat_3780644166@T1` | -1.89335 |
| `explicit.stat_2523933828@T1` | -1.64518 |
| `explicit.stat_1569101201@T1` | -1.61025 |
| `explicit.stat_4147897060@T1` | -1.55547 |
| `explicit.stat_1594812856@T1` | 1.42932 |
| `explicit.stat_3166958180@T1` | -1.34933 |
| `explicit.stat_3174700878@T1` | 1.34450 |
| `explicit.stat_318953428@T1` | -1.33043 |
| `explicit.stat_1697447343@T1` | -1.31457 |

### accessory.ring — n=62102, R²=-2.0216

intercept: `3.3599`  ·  log_price: True  ·  ilvl: `-0.04152`  ·  n_mods: `0.00169`  ·  n_top_tier: `1.11029`  ·  corrupted: `0.01381`  ·  n_sockets: `0.23714`  ·  quality: `0.02663`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.14760 |
| `explicit.stat_803737631@T1` | -1.14047 |
| `explicit.stat_1573130764@T2` | -1.13985 |
| `explicit.stat_2231156303@T1` | -1.13796 |
| `explicit.stat_4220027924@T2` | -1.13343 |
| `explicit.stat_4080418644@T1` | -1.12666 |
| `explicit.stat_3325883026@T1` | -1.12272 |
| `explicit.stat_2923486259@T2` | -1.12006 |
| `explicit.stat_789117908@T2` | -1.11836 |
| `explicit.stat_2901986750@T2` | -1.11799 |
| `explicit.stat_2144192055@T1` | -1.11788 |
| `explicit.stat_3261801346@T1` | -1.11709 |

### other — n=61702, R²=-0.6409

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00005`  ·  n_top_tier: `0.34659`  ·  corrupted: `0.33309`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.42786 |
| `implicit.stat_2219129443` | 0.41644 |
| `explicit.stat_3299347043@T1` | -0.27905 |
| `implicit.stat_3879011313` | 0.23005 |
| `explicit.stat_2968503605@T1` | -0.11328 |
| `explicit.stat_2974417149@T1` | 0.10543 |
| `explicit.stat_736967255@T1` | -0.08571 |
| `explicit.stat_3291658075@T1` | -0.07909 |
| `implicit.stat_1379411836` | -0.07299 |
| `explicit.stat_789117908@T1` | -0.07203 |
| `explicit.stat_2106365538@T1` | -0.06570 |
| `implicit.stat_2901986750` | -0.05744 |

### accessory.amulet — n=56246, R²=-2.1492

intercept: `3.7722`  ·  log_price: True  ·  ilvl: `-0.04609`  ·  n_mods: `-0.02500`  ·  n_top_tier: `1.28429`  ·  corrupted: `0.06058`  ·  n_sockets: `-0.18199`  ·  quality: `-0.00142`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.87089 |
| `explicit.stat_3299347043@T2` | -1.67043 |
| `explicit.stat_587431675@T2` | -1.42815 |
| `explicit.stat_2974417149@T1` | -1.40228 |
| `explicit.stat_803737631@T1` | -1.37572 |
| `explicit.stat_2974417149@T2` | -1.36405 |
| `explicit.stat_2866361420@T2` | -1.35394 |
| `explicit.stat_2866361420@T1` | -1.35239 |
| `explicit.stat_1050105434@T2` | -1.33511 |
| `explicit.stat_803737631@T2` | -1.33464 |
| `explicit.stat_472520716@T2` | -1.33049 |
| `explicit.stat_1671376347@T2` | -1.31899 |

### accessory.belt — n=41187, R²=-1.6378

intercept: `4.0502`  ·  log_price: True  ·  ilvl: `-0.04843`  ·  n_mods: `-0.03051`  ·  n_top_tier: `0.56914`  ·  corrupted: `1.20252`  ·  n_sockets: `1.18108`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.00138 |
| `explicit.stat_4220027924@T1` | 0.82519 |
| `explicit.stat_3299347043@T1` | -0.63146 |
| `explicit.stat_2881298780@T1` | -0.60732 |
| `explicit.stat_3299347043@T2` | -0.60410 |
| `explicit.stat_4220027924@T2` | -0.59956 |
| `explicit.stat_51994685@T1` | -0.59731 |
| `explicit.stat_1570770415@T2` | -0.58732 |
| `explicit.stat_3372524247@T2` | -0.58611 |
| `explicit.stat_3325883026@T1` | -0.58451 |
| `explicit.stat_1389754388@T1` | -0.58068 |
| `explicit.stat_1570770415@T1` | -0.57614 |

### armour.chest — n=40798, R²=-1.7076

intercept: `3.4600`  ·  log_price: True  ·  ilvl: `-0.04267`  ·  n_mods: `-0.02330`  ·  n_top_tier: `0.41656`  ·  corrupted: `0.12999`  ·  n_sockets: `0.02993`  ·  quality: `0.06791`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.92266 |
| `explicit.stat_3981240776@T1` | 0.66364 |
| `explicit.stat_986397080@T2` | -0.51647 |
| `explicit.stat_2339757871@T2` | -0.51004 |
| `explicit.stat_986397080@T1` | -0.50326 |
| `explicit.stat_2339757871@T1` | -0.48340 |
| `explicit.stat_3484657501@T1` | -0.48200 |
| `explicit.stat_1692879867@T2` | -0.46156 |
| `explicit.stat_915769802@T2` | -0.46004 |
| `explicit.stat_4080418644@T1` | -0.45700 |
| `explicit.stat_3261801346@T2` | -0.44964 |
| `explicit.stat_4080418644@T2` | -0.44547 |

### armour.helmet — n=39648, R²=-1.4358

intercept: `3.6028`  ·  log_price: True  ·  ilvl: `-0.04518`  ·  n_mods: `-0.05218`  ·  n_top_tier: `0.48029`  ·  corrupted: `0.63863`  ·  n_sockets: `0.10755`  ·  quality: `0.05654`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.01931 |
| `crafted.stat_3917489142@T1` | -1.29589 |
| `explicit.stat_3917489142@T2` | -1.01236 |
| `explicit.stat_3917489142@T1` | -0.85357 |
| `explicit.stat_1263695895@T1` | -0.83794 |
| `explicit.stat_2162097452@T2` | -0.68092 |
| `explicit.stat_1999113824@T1` | -0.67783 |
| `explicit.stat_1263695895@T2` | -0.63248 |
| `explicit.stat_2923486259@T1` | 0.60695 |
| `explicit.stat_3321629045@T2` | -0.58303 |
| `explicit.stat_803737631@T1` | -0.57821 |
| `explicit.stat_803737631@T2` | -0.56404 |

### armour.boots — n=36866, R²=-1.7591

intercept: `3.3925`  ·  log_price: True  ·  ilvl: `-0.04177`  ·  n_mods: `-0.01968`  ·  n_top_tier: `0.51013`  ·  corrupted: `0.00874`  ·  n_sockets: `0.02647`  ·  quality: `0.06212`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.65044 |
| `crafted.stat_3917489142@T1` | 1.24524 |
| `explicit.stat_2923486259@T1` | 0.84267 |
| `explicit.stat_2339757871@T1` | -0.81520 |
| `explicit.stat_3299347043@T1` | -0.65879 |
| `explicit.stat_3917489142@T2` | -0.63624 |
| `explicit.stat_2923486259@T2` | -0.57243 |
| `explicit.stat_1062208444@T2` | -0.56066 |
| `explicit.stat_2160282525@T1` | -0.55739 |
| `explicit.stat_3917489142@T1` | -0.55142 |
| `explicit.stat_1999113824@T2` | -0.54809 |
| `explicit.stat_3321629045@T1` | -0.54682 |

### armour.gloves — n=35893, R²=-1.7275

intercept: `3.6572`  ·  log_price: True  ·  ilvl: `-0.04682`  ·  n_mods: `-0.02872`  ·  n_top_tier: `0.71817`  ·  corrupted: `-0.03308`  ·  n_sockets: `0.11172`  ·  quality: `0.05154`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.67278 |
| `rune.stat_201332984` | 1.55737 |
| `explicit.stat_2923486259@T1` | -1.44343 |
| `explicit.stat_2923486259@T2` | -1.09345 |
| `explicit.stat_3484657501@T2` | -0.96680 |
| `explicit.stat_3321629045@T2` | -0.92922 |
| `explicit.stat_803737631@T2` | -0.89543 |
| `explicit.stat_9187492@T2` | -0.88540 |
| `explicit.stat_4052037485@T1` | -0.88455 |
| `explicit.stat_803737631@T1` | -0.85531 |
| `explicit.stat_3484657501@T1` | -0.83111 |
| `explicit.stat_4015621042@T2` | -0.81791 |

### weapon.wand — n=21649, R²=-2.0708

intercept: `3.7586`  ·  log_price: True  ·  ilvl: `-0.04695`  ·  n_mods: `-0.03703`  ·  n_top_tier: `0.49927`  ·  corrupted: `0.00054`  ·  n_sockets: `0.05737`  ·  quality: `0.02007`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.98052 |
| `explicit.stat_1545858329@T1` | 2.57244 |
| `explicit.stat_2254480358@T1` | 2.37604 |
| `explicit.stat_124131830@T1` | 2.33789 |
| `explicit.stat_591105508@T1` | 1.86337 |
| `explicit.stat_4226189338@T1` | 1.82282 |
| `explicit.stat_736967255@T2` | 1.67357 |
| `crafted.stat_124131830` | 1.20054 |
| `explicit.stat_1263695895@T2` | -0.88758 |
| `explicit.stat_2254480358@T2` | 0.84723 |
| `explicit.stat_4226189338@T2` | 0.82870 |
| `explicit.stat_1263695895@T1` | -0.77508 |

### flask.charm — n=17772, R²=-0.6147

intercept: `0.1062`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.32277`  ·  corrupted: `1.60223`  ·  quality: `0.00128`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.77909 |
| `explicit.stat_1056492907` | 2.69616 |
| `explicit.stat_828533480@T2` | -1.32280 |
| `explicit.stat_1873752457@T2` | -1.32277 |
| `explicit.stat_1120862500@T2` | -1.32277 |
| `explicit.stat_1873752457@T1` | -1.32274 |
| `explicit.stat_3196823591@T2` | -1.32273 |
| `explicit.stat_2365392475@T2` | -1.32272 |
| `explicit.stat_2676834156@T2` | -1.32272 |
| `explicit.stat_828533480@T1` | -1.32271 |
| `explicit.stat_388617051@T2` | -1.32260 |
| `explicit.stat_1366840608@T2` | -1.31318 |

### weapon.bow — n=17280, R²=-1.8248

intercept: `3.8540`  ·  log_price: True  ·  ilvl: `-0.04518`  ·  n_mods: `-0.09138`  ·  n_top_tier: `0.64812`  ·  corrupted: `0.54552`  ·  n_sockets: `0.08353`  ·  quality: `0.03423`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.33593 |
| `explicit.stat_3336890334@T1` | 1.24319 |
| `explicit.stat_1263695895@T1` | -0.95727 |
| `explicit.stat_2463230181@T2` | -0.95017 |
| `explicit.stat_1263695895@T2` | -0.86513 |
| `explicit.stat_709508406@T1` | 0.85719 |
| `explicit.stat_210067635@T2` | -0.82089 |
| `explicit.stat_1509134228@T1` | -0.75610 |
| `explicit.stat_3639275092@T1` | -0.75223 |
| `explicit.stat_3695891184@T2` | -0.73931 |
| `explicit.stat_3639275092@T2` | -0.73022 |
| `explicit.stat_709508406@T2` | -0.72315 |

### weapon.crossbow — n=16223, R²=-1.8405

intercept: `3.8669`  ·  log_price: True  ·  ilvl: `-0.04710`  ·  n_mods: `-0.06601`  ·  n_top_tier: `0.43927`  ·  corrupted: `0.04136`  ·  n_sockets: `0.07027`  ·  quality: `0.02176`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.67158 |
| `explicit.stat_1202301673@T1` | 1.41500 |
| `explicit.stat_1980802737` | 1.32923 |
| `explicit.stat_2250681686@T2` | -1.23604 |
| `explicit.stat_709508406@T1` | 0.92999 |
| `explicit.stat_2250681686` | 0.91899 |
| `crafted.stat_3035140377` | 0.76670 |
| `explicit.stat_1509134228@T1` | 0.72144 |
| `explicit.stat_1263695895@T2` | -0.63581 |
| `explicit.stat_3336890334@T1` | -0.59211 |
| `explicit.stat_3336890334@T2` | -0.58779 |
| `explicit.stat_1509134228@T2` | -0.58208 |

### weapon.warstaff — n=10978, R²=-0.3474

intercept: `-10.6193`  ·  log_price: True  ·  ilvl: `0.14407`  ·  n_mods: `-0.23388`  ·  n_top_tier: `0.35099`  ·  corrupted: `0.45087`  ·  n_sockets: `0.14228`  ·  quality: `0.06218`

| stat_id | coef |
|---|---|
| `desecrated.stat_473429811@T1` | -2.32406 |
| `desecrated.stat_3291658075@T1` | -2.32406 |
| `desecrated.stat_2231156303@T1` | 1.89201 |
| `desecrated.stat_2527686725@T1` | 1.89201 |
| `crafted.stat_210067635@T2` | 1.24165 |
| `explicit.stat_328541901@T1` | -0.79922 |
| `explicit.stat_1037193709@T1` | 0.77009 |
| `rune.stat_243313994` | 0.73304 |
| `desecrated.stat_9187492` | 0.72015 |
| `explicit.stat_328541901@T2` | -0.71772 |
| `explicit.stat_1509134228@T1` | 0.70251 |
| `explicit.stat_691932474@T2` | -0.64384 |

### weapon.staff — n=10345, R²=-0.3749

intercept: `-16.0507`  ·  log_price: True  ·  ilvl: `0.20548`  ·  n_mods: `-0.08814`  ·  n_top_tier: `0.45177`  ·  corrupted: `0.78632`  ·  n_sockets: `0.19905`  ·  quality: `0.03246`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.30908 |
| `explicit.stat_4226189338@T1` | 2.08325 |
| `explicit.stat_591105508@T1` | 2.04443 |
| `explicit.stat_124131830@T1` | 1.71419 |
| `explicit.stat_293638271@T2` | -1.39304 |
| `explicit.stat_1600707273@T1` | 1.28513 |
| `explicit.stat_2254480358@T1` | 1.23331 |
| `explicit.stat_2254480358@T2` | 0.76986 |
| `explicit.stat_124131830@T2` | 0.70840 |
| `explicit.stat_2768835289@T2` | 0.67325 |
| `explicit.stat_591105508@T2` | 0.64885 |
| `explicit.stat_3278136794@T1` | -0.59685 |

### weapon.sceptre — n=10191, R²=-0.3331

intercept: `-20.9265`  ·  log_price: True  ·  ilvl: `0.26784`  ·  n_mods: `0.02343`  ·  n_top_tier: `0.51445`  ·  corrupted: `-0.10467`  ·  n_sockets: `0.23886`  ·  quality: `0.02778`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.15536 |
| `explicit.stat_3057012405@T1` | 1.16837 |
| `explicit.stat_2854751904@T2` | -1.01157 |
| `explicit.stat_2162097452@T2` | 1.00057 |
| `explicit.stat_2347036682@T2` | -0.73424 |
| `explicit.stat_1250712710@T2` | 0.72218 |
| `explicit.stat_3639275092@T2` | -0.66557 |
| `explicit.stat_1574590649@T2` | -0.58447 |
| `explicit.stat_770672621@T1` | -0.57695 |
| `explicit.stat_789117908@T2` | -0.57126 |
| `explicit.stat_4080418644@T2` | -0.54163 |
| `explicit.stat_3639275092@T1` | -0.47479 |

### weapon.spear — n=8226, R²=-0.3772

intercept: `-12.5235`  ·  log_price: True  ·  ilvl: `0.17512`  ·  n_mods: `-0.19771`  ·  n_top_tier: `0.72762`  ·  corrupted: `-0.09597`  ·  n_sockets: `0.17320`  ·  quality: `0.07369`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.75396 |
| `explicit.stat_1202301673@T1` | 1.67001 |
| `desecrated.stat_210067635@T1` | -1.46351 |
| `explicit.stat_1509134228@T1` | 1.40912 |
| `explicit.stat_9187492@T1` | 1.13367 |
| `explicit.stat_1940865751@T2` | -1.10338 |
| `explicit.stat_691932474@T2` | -1.08927 |
| `explicit.stat_9187492@T2` | -1.08509 |
| `explicit.stat_691932474@T1` | -0.99553 |
| `explicit.stat_4080418644@T2` | -0.96989 |
| `crafted.stat_3035140377` | 0.90866 |
| `explicit.stat_3261801346@T1` | -0.80170 |

### armour.focus — n=6718, R²=-0.3331

intercept: `-14.7178`  ·  log_price: True  ·  ilvl: `0.18875`  ·  n_mods: `-0.18816`  ·  n_top_tier: `0.97183`  ·  corrupted: `0.21067`  ·  n_sockets: `0.36229`  ·  quality: `0.05241`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 3.18771 |
| `explicit.stat_2923486259@T1` | -1.61861 |
| `explicit.stat_4220027924@T1` | -1.50807 |
| `crafted.stat_737908626@T2` | 1.39884 |
| `explicit.stat_4220027924@T2` | -1.37566 |
| `explicit.stat_2974417149@T1` | -1.35078 |
| `explicit.stat_2974417149@T2` | -1.26646 |
| `explicit.stat_3291658075@T1` | -1.14323 |
| `explicit.stat_2231156303@T2` | -1.08818 |
| `explicit.stat_2339757871@T2` | -1.08614 |
| `explicit.stat_737908626@T2` | -1.05597 |
| `explicit.stat_274716455@T2` | -1.03823 |

### armour.quiver — n=6314, R²=-0.2993

intercept: `-15.7901`  ·  log_price: True  ·  ilvl: `0.19457`  ·  n_mods: `-0.15026`  ·  n_top_tier: `0.90595`  ·  corrupted: `0.79594`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.64904 |
| `explicit.stat_2463230181@T1` | 2.39375 |
| `explicit.stat_681332047@T2` | -1.46843 |
| `explicit.stat_1573130764@T1` | -1.38160 |
| `explicit.stat_2463230181@T2` | 1.19436 |
| `explicit.stat_1573130764@T2` | -1.18314 |
| `explicit.stat_681332047@T1` | -1.07803 |
| `explicit.stat_803737631@T2` | -1.07725 |
| `explicit.stat_4067062424@T1` | -1.06243 |
| `explicit.stat_2194114101@T2` | -1.03451 |
| `explicit.stat_803737631@T1` | -1.01275 |
| `explicit.stat_2321178454@T2` | -0.92331 |

### armour.shield — n=5415, R²=-0.454

intercept: `-12.7214`  ·  log_price: True  ·  ilvl: `0.16766`  ·  n_mods: `-0.07291`  ·  n_top_tier: `0.68993`  ·  corrupted: `-0.25751`  ·  n_sockets: `0.35405`  ·  quality: `0.06817`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.36427 |
| `explicit.stat_3321629045@T2` | -1.25894 |
| `explicit.stat_2901986750@T1` | -1.12946 |
| `explicit.stat_3484657501@T2` | -1.11649 |
| `explicit.stat_3855016469@T1` | -1.08014 |
| `explicit.stat_4095671657@T2` | -1.04132 |
| `explicit.stat_4095671657@T1` | -1.00264 |
| `explicit.stat_3033371881@T2` | -1.00009 |
| `explicit.stat_328541901@T1` | -0.94894 |
| `explicit.stat_1671376347@T1` | -0.93771 |
| `explicit.stat_1301765461@T1` | 0.82451 |
| `explicit.stat_1011760251@T2` | -0.81187 |

### weapon.twomace — n=5004, R²=-0.4483

intercept: `-10.0128`  ·  log_price: True  ·  ilvl: `0.13816`  ·  n_mods: `-0.22392`  ·  n_top_tier: `0.40258`  ·  corrupted: `0.29846`  ·  n_sockets: `0.16860`  ·  quality: `0.05897`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.19511 |
| `desecrated.stat_1509134228@T1` | 1.53457 |
| `explicit.stat_1037193709@T1` | -1.41424 |
| `explicit.stat_3336890334@T1` | -1.23968 |
| `explicit.stat_9187492@T1` | -0.95896 |
| `explicit.stat_1263695895@T2` | -0.94384 |
| `explicit.stat_387439868@T2` | -0.78700 |
| `explicit.stat_691932474@T1` | -0.72469 |
| `explicit.stat_709508406@T1` | 0.71439 |
| `explicit.stat_821021828@T2` | -0.65139 |
| `explicit.stat_3695891184@T1` | -0.62316 |
| `explicit.stat_210067635@T2` | 0.58512 |

## Coverage (listings per base)

- … **Sapphire** — 32495 listings (32441 priced) [0.3–3985176410.3 ex]
- … **Emerald** — 31589 listings (31548 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 24229 listings (24199 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11751 listings (11735 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10515 listings (10492 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10178 listings (10154 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 10053 listings (10042 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 9508 listings (9487 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9389 listings (9367 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 9007 listings (8994 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7810 listings (7796 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7519 listings (7511 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7403 listings (7395 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6952 listings (6931 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6520 listings (6513 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 6434 listings (6415 priced) [0.2–39887666593.4 ex]
- … **Plate Belt** — 6429 listings (6401 priced) [0.3–398912568423.8 ex]
- … **Jade Amulet** — 6426 listings (6414 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6386 listings (6379 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6311 listings (6283 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6220 listings (6211 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 6171 listings (6163 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5846 listings (5843 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5788 listings (5775 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5688 listings (5679 priced) [0.3–398912568423.8 ex]

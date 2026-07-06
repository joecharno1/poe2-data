# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-06T02:29:40+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **198086** (198008 priced in exalted)
- Distinct bases: 922 · distinct mods: 2507 · mod rows: 938531
- Sold signals: **37976** sold · 104021 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-06T02:23:18+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×12.01** (median |log error| 2.4856)
- Within ±30% of asking price: **24%**
- Skill vs constant-price guess: **+0.01** (> 0 = the mods carry signal)
- Calibration: 73% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.07** · typical error ×29.54 · ±30% 18% · n=27947
- Premium segment (60ex+): skill **+0.08** · typical error ×138.32 · ±30% 0% · n=16321
- Sold listings (clearing prices): skill **+0.34** · typical error ×6.58 · ±30% 0% · n=10

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 3640 | ×7.47 | 5% | +0.02 | +0.04 |
| accessory.amulet | 3567 | ×39.32 | 19% | -0.01 | -0.01 |
| accessory.belt | 3071 | ×6.87 | 32% | +0.02 | -0.02 |
| jewel | 3068 | ×8.06 | 7% | +0.03 | +0.06 |
| armour.chest | 2976 | ×10.00 | 32% | -0.01 | +0.00 |
| armour.helmet | 2948 | ×10.00 | 30% | +0.00 | +0.01 |
| armour.gloves | 2711 | ×9.99 | 27% | -0.00 | -0.00 |
| armour.boots | 2708 | ×9.96 | 28% | +0.00 | +0.02 |
| other | 2674 | ×10.00 | 37% | +0.06 | +0.18 |
| weapon.wand | 1905 | ×10.21 | 31% | +0.03 | +0.08 |
| weapon.bow | 1594 | ×9.72 | 29% | +0.05 | +0.08 |
| weapon.crossbow | 1495 | ×9.69 | 32% | +0.05 | +0.09 |
| weapon.warstaff | 422 | ×82.00 | 19% | +0.00 | +0.00 |
| weapon.staff | 411 | ×55.00 | 23% | -0.00 | +0.00 |
| weapon.sceptre | 411 | ×90.00 | 18% | -0.00 | +0.00 |
| armour.focus | 312 | ×170.44 | 11% | +0.00 | +0.00 |
| weapon.spear | 302 | ×50.00 | 19% | -0.00 | +0.00 |
| armour.quiver | 274 | ×50.00 | 18% | +0.00 | +0.00 |
| armour.shield | 230 | ×44.00 | 15% | +0.00 | +0.00 |
| weapon.twomace | 227 | ×47.00 | 18% | -0.00 | +0.00 |
| flask.charm | 217 | ×1.00 | 59% | -0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=23216, R²=-0.5123

intercept: `1.6080`  ·  log_price: True  ·  ilvl: `0.00005`  ·  n_mods: `0.00087`  ·  n_top_tier: `0.34880`  ·  corrupted: `3.90476`  ·  n_sockets: `-0.00102`  ·  quality: `-0.00009`

| stat_id | coef |
|---|---|
| `explicit.stat_2106365538@T1` | 4.24785 |
| `explicit.stat_1589917703@T1` | 4.16942 |
| `explicit.stat_3291658075@T1` | 4.10043 |
| `explicit.stat_101878827@T1` | 3.66014 |
| `explicit.stat_2891184298@T1` | 2.14192 |
| `explicit.stat_2974417149@T1` | 1.17406 |
| `explicit.stat_1050105434@T1` | -0.62189 |
| `explicit.stat_789117908@T1` | -0.42634 |
| `explicit.stat_3141070085@T1` | 0.34370 |
| `explicit.stat_2968503605@T1` | 0.31262 |
| `implicit.stat_1379411836` | -0.26866 |
| `implicit.stat_4041853756` | 0.22996 |

### accessory.ring — n=16881, R²=-1.3611

intercept: `5.2522`  ·  log_price: True  ·  ilvl: `-0.04479`  ·  n_mods: `-0.26890`  ·  n_top_tier: `-0.02026`  ·  corrupted: `0.81065`  ·  n_sockets: `2.39927`  ·  quality: `0.00775`

| stat_id | coef |
|---|---|
| `explicit.stat_2557965901@T1` | 2.59759 |
| `explicit.stat_707457662@T1` | 2.50394 |
| `explicit.stat_2557965901@T2` | 2.30827 |
| `explicit.stat_1379411836@T1` | -2.18541 |
| `explicit.stat_3299347043@T1` | -1.38017 |
| `explicit.stat_707457662@T2` | 1.35095 |
| `explicit.stat_1379411836@T2` | -1.19355 |
| `explicit.stat_1573130764@T1` | -1.06901 |
| `explicit.stat_3032590688@T2` | 0.90107 |
| `explicit.stat_2923486259@T2` | 0.78666 |
| `explicit.stat_1263695895@T2` | -0.78411 |
| `explicit.stat_736967255@T1` | 0.72822 |

### accessory.amulet — n=16218, R²=-2.1871

intercept: `4.2445`  ·  log_price: True  ·  ilvl: `-0.05197`  ·  n_mods: `-0.02274`  ·  n_top_tier: `0.00864`  ·  corrupted: `0.08152`  ·  n_sockets: `0.11412`  ·  quality: `-0.01424`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -3.27982 |
| `explicit.stat_983749596@T2` | -2.38025 |
| `explicit.stat_3981240776@T2` | 1.87681 |
| `explicit.stat_1202301673@T2` | 1.06475 |
| `explicit.stat_124131830@T2` | 0.91733 |
| `explicit.stat_124131830` | 0.68179 |
| `explicit.stat_2748665614@T1` | -0.60539 |
| `explicit.stat_1202301673` | 0.58522 |
| `explicit.stat_983749596` | 0.46303 |
| `explicit.stat_2748665614@T2` | -0.37145 |
| `explicit.stat_3981240776@T1` | 0.26214 |
| `explicit.stat_4220027924@T1` | 0.20268 |

### jewel — n=15932, R²=-0.7407

intercept: `-1.2586`  ·  log_price: True  ·  ilvl: `0.03646`  ·  n_mods: `0.20958`  ·  n_top_tier: `-0.43076`  ·  corrupted: `0.44685`  ·  quality: `0.21381`

| stat_id | coef |
|---|---|
| `explicit.stat_1869147066@T1` | 4.91026 |
| `explicit.stat_3714003708@T1` | -3.48176 |
| `explicit.stat_3824372849@T1` | 3.08120 |
| `explicit.stat_1569101201@T1` | 2.88205 |
| `explicit.stat_2456523742@T1` | 2.66806 |
| `explicit.stat_153777645@T1` | 2.63169 |
| `explicit.stat_1316278494@T1` | -2.56361 |
| `explicit.stat_1829102168@T1` | -2.48891 |
| `explicit.stat_1697447343@T1` | 2.27429 |
| `explicit.stat_293638271@T1` | 2.26038 |
| `explicit.stat_2106365538@T1` | -2.13308 |
| `explicit.stat_3377888098@T1` | -2.13109 |

### accessory.belt — n=13969, R²=-0.0872

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.52968`  ·  corrupted: `0.00001`  ·  n_sockets: `4.28836`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 1.39632 |
| `explicit.stat_51994685@T1` | -0.52970 |
| `explicit.stat_1389754388@T1` | -0.52970 |
| `explicit.stat_51994685@T2` | -0.52970 |
| `explicit.stat_1389754388@T2` | -0.52970 |
| `explicit.stat_644456512@T2` | -0.52969 |
| `explicit.stat_1570770415@T2` | -0.52969 |
| `explicit.stat_1570770415@T1` | -0.52969 |
| `explicit.stat_3325883026@T1` | -0.52969 |
| `explicit.stat_1050105434@T2` | -0.52969 |
| `explicit.stat_1836676211@T2` | -0.52969 |
| `explicit.stat_2881298780@T2` | -0.52969 |

### armour.chest — n=13753, R²=-0.2162

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.09078`  ·  corrupted: `0.00008`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3261801346@T1` | -0.09081 |
| `explicit.stat_4080418644@T2` | -0.09080 |
| `explicit.stat_915769802@T2` | -0.09080 |
| `explicit.stat_3033371881@T2` | -0.09080 |
| `explicit.stat_3325883026@T1` | -0.09080 |
| `explicit.stat_915769802@T1` | -0.09080 |
| `explicit.stat_4080418644@T1` | -0.09079 |
| `explicit.stat_124859000@T2` | -0.09079 |
| `explicit.stat_2881298780@T1` | -0.09079 |
| `explicit.stat_3301100256@T1` | -0.09079 |
| `explicit.stat_3372524247@T2` | -0.09079 |
| `explicit.stat_3261801346@T2` | -0.09079 |

### armour.helmet — n=13502, R²=-0.2267

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.03387`  ·  corrupted: `0.03661`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3917489142` | 0.05074 |
| `rune.stat_3523867985` | 0.04969 |
| `crafted.stat_3917489142@T1` | -0.03400 |
| `explicit.stat_3321629045@T1` | -0.03389 |
| `explicit.stat_1062208444@T2` | -0.03388 |
| `explicit.stat_53045048@T2` | -0.03388 |
| `explicit.stat_4080418644@T2` | -0.03388 |
| `explicit.stat_2451402625@T1` | -0.03388 |
| `explicit.stat_803737631@T2` | -0.03388 |
| `explicit.stat_3033371881@T1` | -0.03388 |
| `explicit.stat_4220027924@T2` | -0.03387 |
| `explicit.stat_3325883026@T2` | -0.03387 |

### armour.boots — n=12706, R²=-0.2376

intercept: `2.3265`  ·  log_price: True  ·  ilvl: `-0.00049`  ·  n_mods: `-0.00332`  ·  n_top_tier: `0.02846`  ·  corrupted: `0.00575`  ·  n_sockets: `0.00070`  ·  quality: `0.00015`

| stat_id | coef |
|---|---|
| `explicit.stat_1062208444@T2` | -1.16543 |
| `explicit.stat_4080418644@T1` | -1.03854 |
| `desecrated.stat_2250533757@T2` | -0.10111 |
| `pseudo.total_chaos_res` | 0.09535 |
| `explicit.stat_2923486259` | -0.09476 |
| `explicit.stat_2339757871@T1` | -0.06453 |
| `desecrated.stat_3917489142` | 0.06350 |
| `explicit.stat_3362812763@T1` | -0.03788 |
| `explicit.stat_3261801346@T2` | -0.03422 |
| `explicit.stat_3917489142@T2` | -0.03405 |
| `explicit.stat_328541901@T1` | -0.03377 |
| `explicit.stat_3362812763@T2` | -0.03285 |

### armour.gloves — n=12503, R²=-0.2677

intercept: `2.3037`  ·  log_price: True  ·  ilvl: `-0.00005`  ·  n_mods: `-0.00013`  ·  n_top_tier: `0.00134`  ·  corrupted: `0.00046`  ·  n_sockets: `0.00020`  ·  quality: `0.00002`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.10782 |
| `desecrated.stat_1573130764` | 0.05849 |
| `pseudo.total_life` | 0.01018 |
| `rune.stat_3299347043` | -0.01018 |
| `explicit.stat_3299347043` | -0.01018 |
| `desecrated.stat_3299347043` | -0.01017 |
| `explicit.stat_2339757871@T1` | -0.00691 |
| `explicit.stat_803737631@T2` | -0.00239 |
| `explicit.stat_681332047@T2` | -0.00234 |
| `explicit.stat_2797971005@T2` | -0.00223 |
| `explicit.stat_2797971005@T1` | -0.00215 |
| `explicit.stat_3484657501@T2` | -0.00206 |

### weapon.wand — n=8927, R²=-1.9054

intercept: `3.5016`  ·  log_price: True  ·  ilvl: `-0.04368`  ·  n_mods: `-0.01049`  ·  n_top_tier: `0.54615`  ·  corrupted: `0.05008`  ·  n_sockets: `-0.00678`  ·  quality: `0.00950`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.96313 |
| `explicit.stat_4226189338@T1` | 1.83830 |
| `explicit.stat_2254480358@T1` | 1.82062 |
| `explicit.stat_591105508@T1` | 1.67347 |
| `crafted.stat_124131830` | 0.91153 |
| `explicit.stat_2768835289@T2` | -0.67921 |
| `explicit.stat_3962278098@T2` | -0.62904 |
| `explicit.stat_737908626@T1` | -0.60085 |
| `explicit.stat_2968503605@T2` | -0.59812 |
| `explicit.stat_293638271@T2` | -0.58170 |
| `explicit.stat_2505884597@T2` | -0.56994 |
| `explicit.stat_473429811@T1` | -0.56443 |

### weapon.bow — n=7384, R²=-1.7471

intercept: `3.4372`  ·  log_price: True  ·  ilvl: `-0.04261`  ·  n_mods: `-0.01547`  ·  n_top_tier: `0.23374`  ·  corrupted: `-0.03915`  ·  n_sockets: `0.00514`  ·  quality: `0.00454`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.16289 |
| `explicit.stat_2463230181@T1` | 2.06377 |
| `explicit.stat_1202301673@T1` | 2.03041 |
| `crafted.stat_3035140377` | 1.60620 |
| `explicit.stat_518292764@T1` | 1.09911 |
| `desecrated.stat_666077204@T1` | 0.88507 |
| `explicit.stat_1509134228@T1` | 0.69127 |
| `explicit.stat_55876295@T1` | -0.31117 |
| `explicit.stat_821021828@T1` | -0.29689 |
| `explicit.stat_821021828@T2` | -0.29415 |
| `explicit.stat_55876295@T2` | -0.28613 |
| `explicit.stat_2694482655@T1` | -0.28557 |

### weapon.crossbow — n=6957, R²=-1.6278

intercept: `3.4603`  ·  log_price: True  ·  ilvl: `-0.04321`  ·  n_mods: `-0.00030`  ·  n_top_tier: `0.15817`  ·  corrupted: `-0.06145`  ·  n_sockets: `0.00318`  ·  quality: `0.00126`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 2.18177 |
| `explicit.stat_1037193709@T1` | 2.14350 |
| `explicit.stat_709508406@T1` | 2.12073 |
| `explicit.stat_1202301673@T1` | 2.08134 |
| `explicit.stat_2250681686@T2` | -1.26563 |
| `crafted.stat_3035140377` | 1.23627 |
| `explicit.stat_2250681686` | 1.13875 |
| `rune.stat_669069897` | -0.57654 |
| `rune.stat_55876295` | 0.46346 |
| `rune.stat_2246411426` | -0.45759 |
| `rune.stat_1586906534` | 0.45159 |
| `rune.stat_1509134228` | 0.22694 |

### flask.charm — n=2842, R²=-0.0942

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00002`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1056492907` | 0.53870 |
| `explicit.stat_1873752457@T2` | -0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `explicit.stat_1120862500@T2` | -0.00001 |
| `explicit.stat_2676834156@T2` | -0.00001 |
| `explicit.stat_828533480@T1` | -0.00001 |
| `explicit.stat_828533480@T2` | -0.00001 |
| `explicit.stat_1873752457@T1` | -0.00001 |
| `explicit.stat_388617051@T2` | -0.00001 |
| `explicit.stat_1873752457` | 0.00001 |
| `explicit.stat_3849649145` | -0.00001 |
| `explicit.stat_3196823591@T2` | -0.00000 |

### weapon.warstaff — n=2125, R²=-0.1237

intercept: `-0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_1509134228` | 0.00004 |
| `rune.stat_1039491398` | -0.00003 |
| `rune.stat_1037193709` | 0.00003 |
| `explicit.stat_9187492@T1` | 0.00002 |
| `explicit.stat_1509134228@T2` | 0.00002 |
| `rune.stat_1817052494` | -0.00001 |
| `explicit.stat_709508406@T1` | -0.00001 |
| `explicit.stat_210067635@T1` | -0.00001 |
| `explicit.stat_3336890334@T2` | -0.00001 |
| `desecrated.stat_518292764` | -0.00001 |
| `explicit.stat_1037193709@T1` | -0.00001 |
| `explicit.stat_791928121@T2` | -0.00001 |

### weapon.staff — n=2037, R²=-0.1479

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00002`  ·  corrupted: `-0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_3990135792` | -0.00101 |
| `rune.stat_2974417149` | 0.00059 |
| `explicit.stat_124131830@T1` | 0.00004 |
| `explicit.stat_473429811@T1` | 0.00004 |
| `explicit.stat_3291658075@T2` | 0.00004 |
| `explicit.stat_2254480358@T1` | 0.00003 |
| `explicit.stat_737908626@T1` | 0.00002 |
| `explicit.stat_591105508@T2` | 0.00002 |
| `explicit.stat_2968503605@T2` | 0.00002 |
| `explicit.stat_591105508@T1` | 0.00002 |
| `explicit.stat_1600707273@T2` | 0.00002 |
| `explicit.stat_274716455@T1` | 0.00002 |

### weapon.sceptre — n=2035, R²=-0.1381

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1998951374@T1` | 0.00001 |
| `explicit.stat_1998951374@T2` | 0.00001 |
| `explicit.stat_4010677958@T1` | 0.00001 |
| `explicit.stat_1263695895@T1` | 0.00001 |
| `explicit.stat_2854751904@T2` | 0.00001 |
| `explicit.stat_1798257884@T2` | 0.00001 |
| `explicit.stat_3057012405@T1` | 0.00001 |
| `explicit.stat_1250712710@T2` | 0.00001 |
| `explicit.stat_4010677958@T2` | 0.00001 |
| `explicit.stat_3984865854@T1` | 0.00001 |
| `explicit.stat_3984865854@T2` | -0.00001 |
| `explicit.stat_289128254@T1` | 0.00001 |

### weapon.spear — n=1808, R²=-0.1312

intercept: `-0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | -0.00004 |
| `explicit.stat_1509134228@T1` | 0.00003 |
| `explicit.stat_1263695895@T2` | -0.00003 |
| `explicit.stat_210067635@T1` | 0.00001 |
| `explicit.stat_1368271171@T1` | 0.00001 |
| `explicit.stat_1037193709@T1` | 0.00001 |
| `explicit.stat_1509134228@T2` | 0.00001 |
| `explicit.stat_3639275092@T1` | 0.00001 |
| `explicit.stat_2694482655@T1` | 0.00001 |
| `explicit.stat_2694482655@T2` | 0.00001 |
| `explicit.stat_1940865751@T1` | 0.00001 |
| `explicit.stat_518292764@T1` | 0.00001 |

### armour.focus — n=1531, R²=0.2876

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00005`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -6.32034 |
| `desecrated.stat_2910761524@T1` | 0.90836 |
| `desecrated.stat_3393628375` | 0.45142 |
| `desecrated.stat_2910761524` | -0.11758 |
| `crafted.stat_4015621042` | 0.06761 |
| `desecrated.stat_4220027924` | 0.00644 |
| `desecrated.stat_737908626` | -0.00300 |
| `explicit.stat_3962278098@T1` | 0.00001 |
| `explicit.stat_328541901@T2` | -0.00001 |
| `explicit.stat_3962278098@T2` | 0.00001 |
| `explicit.stat_2339757871@T1` | 0.00001 |
| `explicit.stat_737908626@T1` | 0.00001 |

### armour.quiver — n=1474, R²=-0.1659

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | -0.00007 |
| `explicit.stat_2463230181@T2` | -0.00004 |
| `explicit.stat_803737631@T2` | -0.00001 |
| `explicit.stat_2321178454@T2` | -0.00001 |
| `explicit.stat_3032590688@T1` | -0.00001 |
| `explicit.stat_3714003708@T1` | -0.00001 |
| `explicit.stat_803737631@T1` | -0.00001 |
| `explicit.stat_1368271171@T2` | -0.00001 |
| `explicit.stat_1368271171@T1` | -0.00001 |
| `explicit.stat_3714003708@T2` | -0.00001 |
| `explicit.stat_681332047@T1` | -0.00001 |
| `explicit.stat_1573130764@T1` | -0.00001 |

### armour.shield — n=1306, R²=-0.1658

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 0.00020 |
| `explicit.stat_1011760251@T1` | -0.00008 |
| `explicit.stat_1301765461@T2` | -0.00008 |
| `explicit.stat_1301765461` | 0.00004 |
| `explicit.stat_1978899297@T1` | 0.00004 |
| `explicit.stat_4095671657@T1` | 0.00004 |
| `explicit.stat_3676141501@T1` | 0.00003 |
| `explicit.stat_3033371881@T1` | 0.00003 |
| `explicit.stat_2339757871@T1` | -0.00003 |
| `explicit.stat_4052037485@T2` | 0.00003 |
| `explicit.stat_53045048@T1` | 0.00003 |
| `explicit.stat_2339757871@T2` | 0.00003 |

### weapon.twomace — n=1122, R²=-0.1957

intercept: `-0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | 0.00003 |
| `explicit.stat_821021828@T2` | -0.00003 |
| `explicit.stat_821021828@T1` | -0.00003 |
| `explicit.stat_1037193709@T1` | -0.00002 |
| `explicit.stat_1263695895@T2` | 0.00002 |
| `explicit.stat_518292764@T1` | 0.00001 |
| `explicit.stat_3336890334@T2` | 0.00001 |
| `explicit.stat_1509134228@T1` | 0.00001 |
| `explicit.stat_3336890334@T1` | -0.00001 |
| `explicit.stat_1368271171@T2` | 0.00001 |
| `explicit.stat_387439868@T1` | 0.00001 |
| `explicit.stat_1037193709@T2` | -0.00001 |

## Coverage (listings per base)

- … **Emerald** — 7882 listings (7882 priced) [0.7–42426.8 ex]
- … **Sapphire** — 7859 listings (7859 priced) [0.6–7379.9 ex]
- … **Ruby** — 6138 listings (6138 priced) [0.3–7176.6 ex]
- … **Utility Belt** — 4257 listings (4255 priced) [0.3–4555741.7 ex]
- … **Stellar Amulet** — 3221 listings (3221 priced) [0.3–4547453.5 ex]
- … **Prismatic Ring** — 3019 listings (3019 priced) [0.3–36899.4 ex]
- … **Solar Amulet** — 2923 listings (2923 priced) [0.6–4547453.5 ex]
- … **Gold Amulet** — 2882 listings (2882 priced) [0.7–292542.5 ex]
- … **Amethyst Ring** — 2874 listings (2873 priced) [0.6–17677.8 ex]
- … **Dueling Wand** — 2765 listings (2765 priced) [1.0–138957.7 ex]
- … **Gold Ring** — 2746 listings (2745 priced) [0.5–5903.9 ex]
- … **Sapphire Ring** — 2278 listings (2278 priced) [0.9–7379.9 ex]
- … **Topaz Ring** — 2255 listings (2255 priced) [1.0–3689.9 ex]
- … **Ruby Ring** — 2182 listings (2182 priced) [0.6–44279.2 ex]
- … **Plate Belt** — 2137 listings (2137 priced) [0.6–4547453.5 ex]
- … **Obliterator Bow** — 2107 listings (2104 priced) [0.6–22139622146.9 ex]
- … **Heavy Belt** — 2030 listings (2030 priced) [0.5–2121.3 ex]
- … **Lapis Amulet** — 1990 listings (1990 priced) [0.6–4547453.5 ex]
- … **Amber Amulet** — 1972 listings (1972 priced) [0.7–4547453.5 ex]
- … **Jade Amulet** — 1951 listings (1951 priced) [0.6–4547453.5 ex]
- … **Ancestral Tiara** — 1930 listings (1928 priced) [0.6–365678.1 ex]
- … **Unset Ring** — 1831 listings (1831 priced) [0.6–1476.0 ex]
- … **Bloodstone Amulet** — 1784 listings (1784 priced) [1.0–4675.3 ex]
- … **Pearl Ring** — 1756 listings (1756 priced) [0.6–7176.6 ex]
- … **Azure Amulet** — 1735 listings (1735 priced) [1.0–28284.5 ex]

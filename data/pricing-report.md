# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-22T08:09:57+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **732302** (729941 priced in exalted)
- Distinct bases: 1002 · distinct mods: 3330 · mod rows: 3460484
- Sold signals: **24073** sold · 416741 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-22T07:56:04+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×20.03** (median |log error| 2.9974)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×71.07 · ±30% 6% · n=106272
- Premium segment (60ex+): skill **+0.11** · typical error ×293.54 · ±30% 0% · n=70625

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 15816 | ×28.32 | 21% | +0.04 | +0.07 |
| jewel | 15236 | ×50.76 | 21% | +0.02 | +0.03 |
| accessory.amulet | 14118 | ×10.00 | 20% | +0.01 | +0.00 |
| accessory.belt | 9960 | ×24.99 | 24% | +0.02 | +0.04 |
| armour.chest | 9706 | ×18.28 | 23% | +0.08 | +0.11 |
| armour.helmet | 9441 | ×28.52 | 19% | +0.08 | +0.10 |
| armour.boots | 8724 | ×24.08 | 19% | +0.10 | +0.12 |
| armour.gloves | 8589 | ×33.42 | 13% | +0.08 | +0.11 |
| other | 8565 | ×1.99 | 38% | +0.12 | +0.19 |
| weapon.wand | 5012 | ×43.71 | 16% | +0.10 | +0.12 |
| weapon.bow | 3948 | ×25.67 | 13% | +0.16 | +0.15 |
| weapon.crossbow | 3725 | ×23.58 | 16% | +0.11 | +0.15 |
| weapon.warstaff | 2574 | ×14.72 | 7% | +0.16 | +0.15 |
| weapon.staff | 2476 | ×15.92 | 6% | +0.13 | +0.13 |
| weapon.sceptre | 2436 | ×18.43 | 5% | +0.06 | +0.07 |
| weapon.spear | 1952 | ×13.70 | 7% | +0.11 | +0.14 |
| armour.focus | 1612 | ×12.83 | 7% | +0.09 | +0.10 |
| armour.quiver | 1525 | ×16.81 | 7% | +0.12 | +0.13 |
| flask.charm | 1248 | ×9.97 | 28% | +0.03 | +0.03 |
| armour.shield | 1237 | ×8.10 | 9% | +0.10 | +0.11 |
| weapon.twomace | 1148 | ×9.11 | 7% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=83685, R²=-1.8821

intercept: `-0.0917`  ·  log_price: True  ·  ilvl: `0.00113`  ·  n_mods: `0.95199`  ·  n_top_tier: `-0.85686`  ·  corrupted: `1.15351`  ·  quality: `-0.06644`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 3.31193 |
| `explicit.stat_1604736568@T1` | -2.17233 |
| `explicit.stat_1604736568` | 2.08173 |
| `explicit.stat_2194114101@T1` | -1.09601 |
| `explicit.stat_3714003708@T1` | 0.80538 |
| `explicit.stat_274716455@T1` | -0.78502 |
| `explicit.stat_681332047@T1` | -0.76686 |
| `explicit.stat_3473929743@T1` | -0.49982 |
| `explicit.stat_3556824919@T1` | 0.45576 |
| `explicit.stat_681332047` | 0.33660 |
| `explicit.stat_737908626@T1` | -0.30154 |
| `explicit.stat_3668351662@T1` | -0.26268 |

### accessory.ring — n=72047, R²=-2.0089

intercept: `3.3137`  ·  log_price: True  ·  ilvl: `-0.04166`  ·  n_mods: `0.00089`  ·  n_top_tier: `0.96874`  ·  corrupted: `-0.00356`  ·  n_sockets: `2.19364`  ·  quality: `0.02059`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.03414 |
| `explicit.stat_1573130764@T2` | -1.00681 |
| `explicit.stat_1263695895@T2` | -0.99626 |
| `explicit.stat_2891184298@T2` | -0.99552 |
| `explicit.stat_2891184298@T1` | -0.99356 |
| `explicit.stat_3032590688@T1` | -0.99258 |
| `explicit.stat_3325883026@T1` | -0.99209 |
| `explicit.stat_4080418644@T1` | -0.99154 |
| `explicit.stat_2231156303@T1` | -0.98945 |
| `explicit.stat_3917489142@T2` | -0.98854 |
| `explicit.stat_2923486259@T2` | -0.98833 |
| `explicit.stat_4220027924@T2` | -0.98561 |

### other — n=69731, R²=-0.6475

intercept: `1.6093`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.17271`  ·  n_top_tier: `0.17385`  ·  corrupted: `0.00005`  ·  n_sockets: `-0.00005`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_718638445` | 0.51820 |
| `implicit.stat_3182714256` | 0.51818 |
| `explicit.stat_1050105434@T1` | -0.26520 |
| `implicit.stat_2219129443` | 0.21298 |
| `explicit.stat_2974417149@T1` | 0.18809 |
| `implicit.stat_958696139` | -0.17271 |
| `explicit.stat_3299347043@T1` | -0.16933 |
| `implicit.stat_1416292992` | -0.11514 |
| `explicit.stat_3917489142@T1` | -0.11501 |
| `implicit.stat_3879011313` | 0.10634 |
| `implicit.stat_3032590688` | -0.06908 |
| `explicit.stat_2901986750` | 0.05515 |

### accessory.amulet — n=64529, R²=-0.4992

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `1.04453`  ·  corrupted: `0.00000`  ·  n_sockets: `1.78905`  ·  quality: `0.04048`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | -1.40168 |
| `explicit.stat_124131830@T2` | -1.10378 |
| `explicit.stat_2162097452@T2` | -1.04462 |
| `explicit.stat_803737631@T1` | -1.04456 |
| `explicit.stat_803737631@T2` | -1.04456 |
| `explicit.stat_3299347043@T2` | -1.04456 |
| `explicit.stat_3299347043@T1` | -1.04455 |
| `explicit.stat_4080418644@T2` | -1.04455 |
| `explicit.stat_983749596@T2` | -1.04455 |
| `explicit.stat_983749596@T1` | -1.04455 |
| `explicit.stat_3372524247@T1` | -1.04455 |
| `explicit.stat_789117908@T2` | -1.04454 |

### accessory.belt — n=45721, R²=-2.1384

intercept: `0.1804`  ·  log_price: True  ·  ilvl: `-0.00218`  ·  n_mods: `-0.00096`  ·  n_top_tier: `0.79791`  ·  corrupted: `0.62904`  ·  n_sockets: `1.62256`

| stat_id | coef |
|---|---|
| `explicit.stat_2881298780@T1` | -0.79924 |
| `explicit.stat_3299347043@T2` | -0.79915 |
| `explicit.stat_809229260@T2` | -0.79910 |
| `explicit.stat_51994685@T1` | -0.79906 |
| `explicit.stat_915769802@T1` | -0.79900 |
| `explicit.stat_1570770415@T2` | -0.79868 |
| `explicit.stat_3325883026@T1` | -0.79863 |
| `explicit.stat_3372524247@T2` | -0.79845 |
| `explicit.stat_3299347043@T1` | -0.79820 |
| `explicit.stat_1570770415@T1` | -0.79815 |
| `explicit.stat_2881298780@T2` | -0.79813 |
| `explicit.stat_1389754388@T1` | -0.79801 |

### armour.chest — n=45347, R²=-1.8231

intercept: `3.2813`  ·  log_price: True  ·  ilvl: `-0.04044`  ·  n_mods: `-0.01338`  ·  n_top_tier: `0.35614`  ·  corrupted: `0.20254`  ·  n_sockets: `0.01878`  ·  quality: `0.07892`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.20343 |
| `explicit.stat_986397080@T2` | -0.40514 |
| `explicit.stat_986397080@T1` | -0.38898 |
| `explicit.stat_1692879867@T2` | -0.38480 |
| `explicit.stat_4080418644@T2` | -0.38341 |
| `explicit.stat_915769802@T2` | -0.38099 |
| `explicit.stat_2339757871@T2` | -0.37417 |
| `explicit.stat_915769802@T1` | -0.37387 |
| `explicit.stat_1062208444@T2` | -0.37375 |
| `explicit.stat_2451402625@T2` | -0.37013 |
| `explicit.stat_4015621042@T2` | -0.36796 |
| `explicit.stat_3484657501@T1` | -0.36773 |

### armour.helmet — n=44130, R²=-1.8012

intercept: `3.2980`  ·  log_price: True  ·  ilvl: `-0.04122`  ·  n_mods: `-0.01727`  ·  n_top_tier: `0.52258`  ·  corrupted: `0.54321`  ·  n_sockets: `0.05605`  ·  quality: `0.07766`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.30251 |
| `crafted.stat_3917489142@T1` | 2.05068 |
| `explicit.stat_1263695895@T1` | -0.70391 |
| `explicit.stat_2162097452@T2` | -0.69432 |
| `explicit.stat_3917489142@T2` | -0.65850 |
| `explicit.stat_3917489142@T1` | -0.60218 |
| `explicit.stat_4052037485@T2` | -0.58056 |
| `explicit.stat_4015621042@T2` | -0.57838 |
| `explicit.stat_1263695895@T2` | -0.56293 |
| `explicit.stat_3321629045@T2` | -0.55260 |
| `explicit.stat_1999113824@T1` | -0.54994 |
| `explicit.stat_4052037485@T1` | -0.53853 |

### armour.boots — n=40784, R²=-1.733

intercept: `3.6032`  ·  log_price: True  ·  ilvl: `-0.04448`  ·  n_mods: `-0.02334`  ·  n_top_tier: `0.38674`  ·  corrupted: `0.03895`  ·  n_sockets: `0.05251`  ·  quality: `0.07444`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.19464 |
| `explicit.stat_2250533757@T1` | 1.79597 |
| `crafted.stat_3917489142@T1` | 1.46158 |
| `explicit.stat_2923486259@T1` | 0.87401 |
| `explicit.stat_3299347043@T1` | -0.52356 |
| `explicit.stat_2923486259@T2` | -0.46901 |
| `explicit.stat_3917489142@T2` | -0.44086 |
| `explicit.stat_2160282525@T1` | -0.43587 |
| `explicit.stat_328541901@T2` | -0.43188 |
| `explicit.stat_1874553720@T1` | -0.43096 |
| `explicit.stat_1671376347@T2` | -0.42932 |
| `explicit.stat_99927264@T1` | -0.42473 |

### armour.gloves — n=39780, R²=-1.6748

intercept: `3.9067`  ·  log_price: True  ·  ilvl: `-0.05137`  ·  n_mods: `-0.00641`  ·  n_top_tier: `0.69593`  ·  corrupted: `-0.04852`  ·  n_sockets: `0.18661`  ·  quality: `0.05858`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.04611 |
| `explicit.stat_4052037485@T1` | -0.98320 |
| `explicit.stat_3484657501@T2` | -0.93609 |
| `explicit.stat_4052037485@T2` | -0.89700 |
| `explicit.stat_4015621042@T2` | -0.89306 |
| `explicit.stat_3321629045@T2` | -0.88125 |
| `explicit.stat_2923486259@T2` | -0.87286 |
| `explicit.stat_3484657501@T1` | -0.86448 |
| `explicit.stat_124859000@T1` | -0.83079 |
| `explicit.stat_9187492@T2` | -0.82571 |
| `explicit.stat_3917489142@T2` | -0.79112 |
| `explicit.stat_803737631@T2` | -0.77601 |

### weapon.wand — n=23368, R²=-2.028

intercept: `4.2694`  ·  log_price: True  ·  ilvl: `-0.05298`  ·  n_mods: `-0.05138`  ·  n_top_tier: `0.57142`  ·  corrupted: `-0.01215`  ·  n_sockets: `0.02096`  ·  quality: `0.04663`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.12925 |
| `explicit.stat_1545858329@T1` | 3.03051 |
| `explicit.stat_2254480358@T1` | 2.55229 |
| `explicit.stat_4226189338@T1` | 2.42189 |
| `explicit.stat_124131830@T1` | 2.33067 |
| `explicit.stat_591105508@T1` | 2.24389 |
| `explicit.stat_1600707273@T1` | 1.40698 |
| `crafted.stat_124131830` | 1.20404 |
| `explicit.stat_2254480358@T2` | 1.13976 |
| `explicit.stat_1263695895@T2` | -0.97425 |
| `explicit.stat_1263695895@T1` | -0.93509 |
| `explicit.stat_4226189338@T2` | 0.87593 |

### flask.charm — n=20521, R²=-0.6624

intercept: `0.1060`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.60922`  ·  corrupted: `1.53796`  ·  quality: `0.01419`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60507 |
| `explicit.stat_1056492907` | 2.54123 |
| `explicit.stat_3246948616` | 2.30245 |
| `explicit.stat_1120862500@T2` | -1.60925 |
| `explicit.stat_828533480@T2` | -1.60925 |
| `explicit.stat_1873752457@T2` | -1.60922 |
| `explicit.stat_2541588185@T2` | -1.60921 |
| `explicit.stat_388617051@T2` | -1.60919 |
| `explicit.stat_2365392475@T2` | -1.60914 |
| `explicit.stat_3196823591@T2` | -1.60880 |
| `explicit.stat_2676834156@T2` | -1.60858 |
| `explicit.stat_828533480@T1` | -1.60423 |

### weapon.bow — n=18679, R²=-1.8197

intercept: `4.0671`  ·  log_price: True  ·  ilvl: `-0.04798`  ·  n_mods: `-0.09539`  ·  n_top_tier: `0.76321`  ·  corrupted: `0.72392`  ·  n_sockets: `0.04142`  ·  quality: `0.03276`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 5.17482 |
| `desecrated.stat_210067635@T1` | -1.82562 |
| `explicit.stat_1263695895@T1` | -1.30532 |
| `crafted.stat_210067635@T2` | -1.25480 |
| `explicit.stat_1263695895@T2` | -1.21081 |
| `crafted.stat_3035140377` | 1.15753 |
| `explicit.stat_1509134228@T1` | -0.96915 |
| `explicit.stat_210067635@T2` | -0.92875 |
| `explicit.stat_2463230181@T2` | -0.91872 |
| `explicit.stat_3695891184@T1` | -0.86527 |
| `explicit.stat_1368271171@T2` | -0.86342 |
| `explicit.stat_1368271171@T1` | -0.85117 |

### weapon.crossbow — n=17501, R²=-1.8009

intercept: `4.3871`  ·  log_price: True  ·  ilvl: `-0.05311`  ·  n_mods: `-0.06316`  ·  n_top_tier: `0.46654`  ·  corrupted: `-0.12694`  ·  n_sockets: `0.04632`  ·  quality: `0.01945`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.94125 |
| `explicit.stat_2250681686@T2` | -1.90810 |
| `explicit.stat_2250681686` | 1.52034 |
| `explicit.stat_1202301673@T1` | 1.45677 |
| `explicit.stat_1980802737` | 1.36734 |
| `explicit.stat_1509134228@T1` | 0.95952 |
| `crafted.stat_3035140377` | 0.89663 |
| `explicit.stat_709508406@T1` | 0.69994 |
| `explicit.stat_3695891184@T1` | -0.66091 |
| `explicit.stat_3336890334@T2` | -0.64807 |
| `explicit.stat_3695891184@T2` | -0.60542 |
| `explicit.stat_691932474@T1` | -0.58727 |

### weapon.warstaff — n=12331, R²=-0.3234

intercept: `-11.1156`  ·  log_price: True  ·  ilvl: `0.15143`  ·  n_mods: `-0.23746`  ·  n_top_tier: `0.48660`  ·  corrupted: `0.28984`  ·  n_sockets: `0.12138`  ·  quality: `0.05154`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 0.97351 |
| `desecrated.stat_2231156303@T1` | 0.93970 |
| `desecrated.stat_2527686725@T1` | 0.93970 |
| `explicit.stat_821021828@T2` | -0.88458 |
| `explicit.stat_328541901@T2` | -0.86182 |
| `explicit.stat_1037193709@T2` | -0.83638 |
| `desecrated.stat_9187492` | 0.80581 |
| `rune.stat_243313994` | 0.75298 |
| `explicit.stat_210067635@T1` | -0.73177 |
| `desecrated.stat_3291658075@T1` | -0.72228 |
| `desecrated.stat_473429811@T1` | -0.72228 |
| `explicit.stat_328541901@T1` | -0.70431 |

### weapon.staff — n=11758, R²=-0.3518

intercept: `-15.9843`  ·  log_price: True  ·  ilvl: `0.20570`  ·  n_mods: `-0.12784`  ·  n_top_tier: `0.50343`  ·  corrupted: `0.86861`  ·  n_sockets: `0.19457`  ·  quality: `0.03924`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.01507 |
| `explicit.stat_124131830@T1` | 1.76852 |
| `explicit.stat_4226189338@T1` | 1.58112 |
| `explicit.stat_1600707273@T1` | 1.44400 |
| `explicit.stat_1545858329@T1` | 0.94592 |
| `explicit.stat_3962278098@T2` | 0.90102 |
| `explicit.stat_473429811@T2` | -0.88154 |
| `explicit.stat_293638271@T2` | -0.84510 |
| `explicit.stat_591105508@T2` | 0.81245 |
| `explicit.stat_124131830@T2` | 0.60614 |
| `explicit.stat_4226189338@T2` | 0.54920 |
| `explicit.stat_1050105434@T2` | -0.53528 |

### weapon.sceptre — n=11428, R²=-0.3296

intercept: `-21.7119`  ·  log_price: True  ·  ilvl: `0.27589`  ·  n_mods: `-0.01785`  ·  n_top_tier: `0.15525`  ·  corrupted: `0.20168`  ·  n_sockets: `0.19976`  ·  quality: `0.03655`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.58960 |
| `explicit.stat_2162097452@T2` | 1.33567 |
| `explicit.stat_3057012405@T1` | 1.04532 |
| `explicit.stat_1263695895@T1` | -0.98035 |
| `explicit.stat_1798257884@T2` | 0.95957 |
| `explicit.stat_101878827@T2` | 0.76924 |
| `explicit.stat_1263695895@T2` | -0.74195 |
| `explicit.stat_101878827@T1` | 0.70891 |
| `explicit.stat_2854751904@T2` | -0.64743 |
| `explicit.stat_4080418644@T2` | -0.58052 |
| `explicit.stat_328541901@T2` | 0.43348 |
| `explicit.stat_2347036682@T1` | 0.43323 |

### weapon.spear — n=9306, R²=-0.3803

intercept: `-13.2996`  ·  log_price: True  ·  ilvl: `0.18421`  ·  n_mods: `-0.18928`  ·  n_top_tier: `0.57225`  ·  corrupted: `-0.52175`  ·  n_sockets: `0.22345`  ·  quality: `0.07328`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -3.28757 |
| `crafted.stat_210067635@T2` | -3.23167 |
| `crafted.stat_3035140377` | 0.97921 |
| `explicit.stat_1037193709@T1` | -0.96409 |
| `explicit.stat_748522257@T2` | -0.94717 |
| `explicit.stat_9187492@T2` | -0.94347 |
| `explicit.stat_4080418644@T2` | -0.91968 |
| `explicit.stat_4080418644@T1` | -0.88654 |
| `explicit.stat_1940865751@T2` | -0.87880 |
| `explicit.stat_3336890334@T2` | -0.86143 |
| `explicit.stat_9187492@T1` | 0.82620 |
| `explicit.stat_3261801346@T1` | -0.82165 |

### armour.focus — n=7601, R²=-0.3304

intercept: `-16.5723`  ·  log_price: True  ·  ilvl: `0.21127`  ·  n_mods: `-0.15921`  ·  n_top_tier: `0.95674`  ·  corrupted: `-0.25724`  ·  n_sockets: `0.40610`  ·  quality: `0.03432`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 2.13084 |
| `explicit.stat_4220027924@T1` | -1.46332 |
| `explicit.stat_2923486259@T1` | -1.43312 |
| `explicit.stat_2339757871@T2` | -1.22750 |
| `explicit.stat_2923486259@T2` | -1.16119 |
| `explicit.stat_4220027924@T2` | -1.15907 |
| `explicit.stat_2768835289@T1` | -1.14233 |
| `explicit.stat_3962278098@T2` | -1.10234 |
| `explicit.stat_274716455@T2` | -1.09209 |
| `explicit.stat_4015621042@T1` | -1.08446 |
| `explicit.stat_2231156303@T1` | -1.06881 |
| `explicit.stat_1050105434@T2` | -1.04796 |

### armour.quiver — n=7079, R²=-0.2759

intercept: `-18.3650`  ·  log_price: True  ·  ilvl: `0.22123`  ·  n_mods: `-0.07649`  ·  n_top_tier: `0.70111`  ·  corrupted: `0.97658`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.16272 |
| `explicit.stat_681332047@T2` | -1.36390 |
| `explicit.stat_681332047@T1` | -1.11236 |
| `explicit.stat_1573130764@T2` | -0.99728 |
| `explicit.stat_1573130764@T1` | -0.89840 |
| `explicit.stat_2321178454@T2` | -0.86886 |
| `explicit.stat_2194114101@T2` | -0.82033 |
| `explicit.stat_4067062424@T1` | -0.73880 |
| `explicit.stat_3714003708@T2` | -0.60844 |
| `explicit.stat_4067062424@T2` | -0.60228 |
| `explicit.stat_803737631@T2` | -0.59463 |
| `explicit.stat_3261801346@T1` | -0.59301 |

### armour.shield — n=6084, R²=-0.4138

intercept: `-13.7851`  ·  log_price: True  ·  ilvl: `0.18605`  ·  n_mods: `-0.18805`  ·  n_top_tier: `0.62421`  ·  corrupted: `-0.52244`  ·  n_sockets: `0.33689`  ·  quality: `0.04844`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.48052 |
| `explicit.stat_1011760251@T1` | -1.45635 |
| `explicit.stat_328541901@T1` | -1.22012 |
| `explicit.stat_3033371881@T2` | -1.16625 |
| `explicit.stat_4095671657@T2` | -1.13423 |
| `explicit.stat_2339757871@T1` | -1.09838 |
| `explicit.stat_2901986750@T1` | -1.07498 |
| `explicit.stat_4095671657@T1` | -1.03756 |
| `explicit.stat_2923486259@T1` | -1.03614 |
| `explicit.stat_3321629045@T2` | -1.02298 |
| `explicit.stat_2339757871@T2` | -0.99399 |
| `explicit.stat_2481353198@T1` | -0.92316 |

### weapon.twomace — n=5559, R²=-0.4257

intercept: `-11.1065`  ·  log_price: True  ·  ilvl: `0.15378`  ·  n_mods: `-0.24832`  ·  n_top_tier: `0.49263`  ·  corrupted: `0.48496`  ·  n_sockets: `0.18988`  ·  quality: `0.05733`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.89058 |
| `explicit.stat_1037193709@T1` | -1.57533 |
| `explicit.stat_3336890334@T1` | -1.42925 |
| `explicit.stat_1263695895@T2` | -1.24730 |
| `explicit.stat_9187492@T1` | -1.22035 |
| `explicit.stat_2694482655@T1` | 0.93118 |
| `explicit.stat_1263695895@T1` | -0.68934 |
| `explicit.stat_210067635@T1` | -0.68864 |
| `explicit.stat_3695891184@T2` | -0.67724 |
| `explicit.stat_3695891184@T1` | -0.67570 |
| `explicit.stat_518292764@T2` | -0.66261 |
| `explicit.stat_55876295@T1` | -0.60559 |

## Coverage (listings per base)

- … **Sapphire** — 38409 listings (38344 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 37431 listings (37379 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 28649 listings (28617 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 13073 listings (13055 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 12048 listings (12022 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 11737 listings (11711 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 11607 listings (11594 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10857 listings (10830 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10821 listings (10798 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 10281 listings (10268 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8993 listings (8978 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8638 listings (8628 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8556 listings (8547 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7552 listings (7528 priced) [0.3–398916553600208.8 ex]
- … **Unset Ring** — 7429 listings (7407 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7401 listings (7393 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 7334 listings (7319 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 7241 listings (7233 priced) [0.3–3985176410.3 ex]
- … **Pearl Ring** — 7183 listings (7174 priced) [0.2–275252424.7 ex]
- … **Plate Belt** — 7131 listings (7100 priced) [0.3–398916553600208.8 ex]
- … **Ancestral Tiara** — 7074 listings (7045 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 7024 listings (7012 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6725 listings (6721 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6623 listings (6608 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6318 listings (6304 priced) [0.3–398916553600208.8 ex]

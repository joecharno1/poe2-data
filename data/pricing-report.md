# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-08T11:43:17+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **324884** (324453 priced in exalted)
- Distinct bases: 956 · distinct mods: 2836 · mod rows: 1542001
- Sold signals: **30432** sold · 173253 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-08T11:32:14+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×17.26** (median |log error| 2.8486)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.02** · typical error ×43.55 · ±30% 8% · n=47003
- Premium segment (60ex+): skill **+0.05** · typical error ×188.09 · ±30% 0% · n=29325

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 6220 | ×11.23 | 4% | +0.03 | +0.05 |
| accessory.amulet | 5797 | ×48.36 | 21% | +0.03 | +0.03 |
| jewel | 5433 | ×8.54 | 6% | +0.02 | +0.05 |
| accessory.belt | 4692 | ×10.00 | 21% | +0.01 | +0.02 |
| armour.chest | 4640 | ×11.62 | 6% | +0.05 | +0.06 |
| armour.helmet | 4519 | ×11.73 | 7% | +0.01 | +0.02 |
| armour.boots | 4301 | ×16.64 | 6% | +0.05 | +0.07 |
| armour.gloves | 4152 | ×18.06 | 5% | +0.02 | +0.04 |
| other | 3936 | ×9.75 | 38% | +0.06 | +0.16 |
| weapon.wand | 2781 | ×32.56 | 22% | +0.06 | +0.07 |
| weapon.bow | 2286 | ×20.31 | 21% | +0.09 | +0.08 |
| weapon.crossbow | 2092 | ×15.85 | 21% | +0.09 | +0.10 |
| weapon.warstaff | 1009 | ×50.00 | 18% | +0.03 | +0.04 |
| weapon.sceptre | 977 | ×50.00 | 13% | +0.09 | +0.06 |
| weapon.staff | 975 | ×49.00 | 19% | +0.04 | +0.05 |
| weapon.spear | 806 | ×40.00 | 18% | +0.03 | +0.04 |
| armour.focus | 660 | ×454.05 | 12% | +0.02 | +0.09 |
| armour.quiver | 641 | ×77.82 | 12% | +0.00 | +0.04 |
| armour.shield | 533 | ×25.00 | 19% | +0.02 | +0.04 |
| flask.charm | 471 | ×10.00 | 37% | +0.00 | -0.00 |
| weapon.twomace | 469 | ×19.99 | 16% | +0.00 | +0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=33522, R²=-0.4918

intercept: `1.6031`  ·  log_price: True  ·  ilvl: `0.00008`  ·  n_mods: `0.02059`  ·  n_top_tier: `0.51534`  ·  corrupted: `1.09856`  ·  n_sockets: `-0.00009`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.32577 |
| `explicit.stat_2106365538@T1` | 2.53263 |
| `explicit.stat_3141070085@T1` | -1.78825 |
| `explicit.stat_1589917703@T1` | -1.64930 |
| `explicit.stat_2891184298@T1` | 1.55844 |
| `explicit.stat_3917489142@T1` | 0.94545 |
| `explicit.stat_2974417149@T1` | 0.94402 |
| `explicit.stat_1050105434@T1` | -0.92105 |
| `explicit.stat_101878827@T1` | -0.90333 |
| `explicit.stat_789117908@T1` | -0.69464 |
| `explicit.stat_1589917703` | 0.36634 |
| `explicit.stat_3141070085` | 0.28203 |

### jewel — n=29488, R²=-0.6235

intercept: `-1.1173`  ·  log_price: True  ·  ilvl: `0.03692`  ·  n_mods: `0.18965`  ·  n_top_tier: `-0.07992`  ·  corrupted: `0.26231`  ·  quality: `0.21511`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.77157 |
| `explicit.stat_1569159338@T1` | -3.32045 |
| `explicit.stat_1569101201@T1` | 3.29416 |
| `explicit.stat_3741323227@T1` | -3.20986 |
| `explicit.stat_1854213750@T1` | -2.26796 |
| `explicit.stat_1316278494@T1` | -2.26469 |
| `explicit.stat_1062710370@T1` | -2.14082 |
| `explicit.stat_234296660@T1` | -2.10211 |
| `explicit.stat_3714003708@T1` | -2.04177 |
| `explicit.stat_2527686725@T1` | 1.99636 |
| `explicit.stat_1697951953@T1` | -1.96118 |
| `explicit.stat_440490623@T1` | -1.86853 |

### accessory.ring — n=28362, R²=-1.2084

intercept: `3.8082`  ·  log_price: True  ·  ilvl: `-0.03848`  ·  n_mods: `-0.02520`  ·  n_top_tier: `0.24101`  ·  corrupted: `0.96628`  ·  n_sockets: `0.75953`  ·  quality: `0.04590`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 5.96358 |
| `explicit.stat_707457662@T2` | 4.96532 |
| `explicit.stat_1379411836@T1` | -2.39975 |
| `explicit.stat_1379411836@T2` | -1.93638 |
| `explicit.stat_1368271171@T1` | -1.19501 |
| `explicit.stat_1368271171@T2` | -0.98600 |
| `explicit.stat_707457662` | -0.92814 |
| `explicit.stat_1263695895@T1` | -0.79823 |
| `explicit.stat_1263695895@T2` | -0.74725 |
| `explicit.stat_3291658075@T2` | -0.72465 |
| `explicit.stat_3291658075@T1` | -0.71930 |
| `explicit.stat_3695891184@T1` | -0.69797 |

### accessory.amulet — n=26805, R²=-2.067

intercept: `4.0522`  ·  log_price: True  ·  ilvl: `-0.04884`  ·  n_mods: `-0.02944`  ·  n_top_tier: `1.08099`  ·  corrupted: `0.07434`  ·  n_sockets: `1.69850`  ·  quality: `-0.00177`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.40562 |
| `explicit.stat_983749596@T2` | -1.35640 |
| `explicit.stat_3299347043@T1` | -1.33732 |
| `explicit.stat_587431675@T1` | -1.19517 |
| `explicit.stat_2748665614@T1` | -1.16806 |
| `explicit.stat_3325883026@T1` | -1.15865 |
| `explicit.stat_472520716@T2` | -1.15210 |
| `explicit.stat_472520716@T1` | -1.14768 |
| `explicit.stat_2748665614@T2` | -1.14692 |
| `explicit.stat_3325883026@T2` | -1.13955 |
| `explicit.stat_3917489142@T2` | -1.13843 |
| `explicit.stat_3917489142@T1` | -1.13207 |

### accessory.belt — n=21650, R²=-0.1367

intercept: `2.3029`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00004`  ·  n_top_tier: `0.07544`  ·  corrupted: `0.00007`  ·  n_sockets: `-0.65925`

| stat_id | coef |
|---|---|
| `explicit.stat_2639966148` | 0.08431 |
| `explicit.stat_1389754388@T1` | -0.07551 |
| `explicit.stat_51994685@T1` | -0.07548 |
| `explicit.stat_1570770415@T1` | -0.07547 |
| `explicit.stat_644456512@T1` | -0.07547 |
| `explicit.stat_2923486259@T2` | -0.07547 |
| `explicit.stat_2881298780@T1` | -0.07546 |
| `explicit.stat_4220027924@T2` | -0.07546 |
| `explicit.stat_1836676211@T2` | -0.07546 |
| `explicit.stat_2881298780@T2` | -0.07546 |
| `explicit.stat_1671376347@T2` | -0.07546 |
| `explicit.stat_1389754388@T2` | -0.07545 |

### armour.chest — n=21472, R²=-0.8013

intercept: `4.3883`  ·  log_price: True  ·  ilvl: `-0.04899`  ·  n_mods: `-0.13109`  ·  n_top_tier: `0.54451`  ·  corrupted: `0.16244`  ·  n_sockets: `0.05761`  ·  quality: `0.02272`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.93503 |
| `explicit.stat_915769802@T1` | -1.14709 |
| `explicit.stat_915769802@T2` | -0.89850 |
| `explicit.stat_3321629045@T1` | -0.87986 |
| `explicit.stat_3261801346@T1` | -0.83567 |
| `explicit.stat_4015621042@T1` | -0.83241 |
| `explicit.stat_3325883026@T2` | -0.79741 |
| `explicit.stat_4080418644@T2` | -0.77175 |
| `explicit.stat_3261801346@T2` | -0.75648 |
| `explicit.stat_3362812763@T2` | -0.73117 |
| `explicit.stat_3484657501@T1` | -0.72783 |
| `explicit.stat_986397080@T2` | -0.71928 |

### armour.helmet — n=21036, R²=-0.4249

intercept: `3.4681`  ·  log_price: True  ·  ilvl: `-0.02782`  ·  n_mods: `-0.11421`  ·  n_top_tier: `0.42165`  ·  corrupted: `0.75615`  ·  n_sockets: `0.01722`  ·  quality: `0.02536`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.50715 |
| `explicit.stat_1062208444@T2` | -1.04752 |
| `explicit.stat_4080418644@T2` | -0.99982 |
| `explicit.stat_53045048@T2` | -0.78866 |
| `explicit.stat_3362812763@T2` | -0.68170 |
| `explicit.stat_53045048@T1` | -0.62202 |
| `explicit.stat_3362812763@T1` | -0.61877 |
| `explicit.stat_4080418644@T1` | -0.52375 |
| `explicit.stat_587431675@T2` | -0.50523 |
| `explicit.stat_1999113824@T1` | -0.50169 |
| `explicit.stat_803737631@T2` | -0.49404 |
| `explicit.stat_2162097452@T2` | -0.49073 |

### armour.boots — n=19857, R²=-0.8489

intercept: `4.3518`  ·  log_price: True  ·  ilvl: `-0.05157`  ·  n_mods: `-0.11658`  ·  n_top_tier: `0.58731`  ·  corrupted: `0.41626`  ·  n_sockets: `0.12492`  ·  quality: `0.01472`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.28077 |
| `explicit.stat_2339757871@T1` | -1.19640 |
| `explicit.stat_2923486259@T2` | -1.10977 |
| `rune.stat_836936635` | -0.99522 |
| `explicit.stat_3362812763@T1` | -0.99105 |
| `explicit.stat_1062208444@T2` | -0.93094 |
| `explicit.stat_328541901@T1` | -0.86878 |
| `explicit.stat_3321629045@T1` | -0.86295 |
| `explicit.stat_3484657501@T2` | -0.77926 |
| `explicit.stat_2160282525@T1` | -0.77880 |
| `explicit.stat_1999113824@T2` | -0.75082 |
| `explicit.stat_1999113824@T1` | -0.74638 |

### armour.gloves — n=19336, R²=-0.8049

intercept: `3.5983`  ·  log_price: True  ·  ilvl: `-0.04558`  ·  n_mods: `-0.12743`  ·  n_top_tier: `0.51446`  ·  corrupted: `0.40074`  ·  n_sockets: `0.31208`  ·  quality: `0.01285`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.42432 |
| `explicit.stat_803737631@T2` | -1.05056 |
| `explicit.stat_3484657501@T2` | -1.03592 |
| `explicit.stat_681332047@T2` | -0.99498 |
| `explicit.stat_328541901@T1` | -0.93875 |
| `explicit.stat_2797971005@T2` | -0.77141 |
| `explicit.stat_1754445556@T1` | -0.75659 |
| `explicit.stat_3695891184@T1` | -0.75653 |
| `explicit.stat_124859000@T2` | -0.73609 |
| `explicit.stat_4220027924@T2` | -0.73357 |
| `explicit.stat_4080418644@T1` | -0.72016 |
| `explicit.stat_3033371881@T2` | -0.71621 |

### weapon.wand — n=13141, R²=-2.0528

intercept: `3.5853`  ·  log_price: True  ·  ilvl: `-0.04475`  ·  n_mods: `-0.00646`  ·  n_top_tier: `0.59703`  ·  corrupted: `-0.00455`  ·  n_sockets: `0.02165`  ·  quality: `0.02095`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.15549 |
| `explicit.stat_591105508@T1` | 1.78436 |
| `explicit.stat_1545858329@T1` | 1.75325 |
| `explicit.stat_4226189338@T1` | 1.74304 |
| `explicit.stat_1600707273@T1` | 1.69217 |
| `explicit.stat_124131830@T1` | 1.63829 |
| `explicit.stat_736967255@T2` | 1.16522 |
| `crafted.stat_124131830` | 0.76202 |
| `explicit.stat_2768835289@T2` | -0.64424 |
| `explicit.stat_737908626@T1` | -0.62918 |
| `explicit.stat_2231156303@T2` | -0.62529 |
| `explicit.stat_473429811@T1` | -0.62291 |

### weapon.bow — n=10758, R²=-1.9813

intercept: `3.3983`  ·  log_price: True  ·  ilvl: `-0.04212`  ·  n_mods: `-0.01033`  ·  n_top_tier: `0.49001`  ·  corrupted: `0.08687`  ·  n_sockets: `0.00182`  ·  quality: `0.00648`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.94265 |
| `explicit.stat_2463230181@T1` | 1.79022 |
| `explicit.stat_1202301673@T1` | 1.66151 |
| `desecrated.stat_666077204@T1` | 1.64346 |
| `crafted.stat_3035140377` | 1.48475 |
| `rune.stat_3885405204` | -0.81299 |
| `explicit.stat_55876295@T1` | -0.54443 |
| `explicit.stat_2694482655@T1` | -0.53502 |
| `explicit.stat_3336890334@T2` | -0.53259 |
| `explicit.stat_3695891184@T2` | -0.52538 |
| `explicit.stat_3261801346@T1` | -0.51504 |
| `explicit.stat_55876295@T2` | -0.51103 |

### weapon.crossbow — n=10090, R²=-1.8265

intercept: `3.6340`  ·  log_price: True  ·  ilvl: `-0.04505`  ·  n_mods: `-0.00665`  ·  n_top_tier: `0.59851`  ·  corrupted: `-0.04168`  ·  n_sockets: `0.01443`  ·  quality: `0.00288`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -2.72676 |
| `explicit.stat_1980802737` | 2.08391 |
| `explicit.stat_709508406@T1` | 1.61347 |
| `explicit.stat_1202301673@T1` | 1.56504 |
| `explicit.stat_2250681686@T2` | -1.45239 |
| `explicit.stat_1509134228@T1` | 0.97354 |
| `explicit.stat_2250681686` | 0.86849 |
| `crafted.stat_3035140377` | 0.81604 |
| `explicit.stat_1037193709@T1` | 0.81039 |
| `rune.stat_669069897` | -0.75895 |
| `explicit.stat_1202301673@T2` | -0.72133 |
| `explicit.stat_1509134228@T2` | -0.68531 |

### flask.charm — n=7077, R²=-0.3692

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00004`  ·  corrupted: `0.28813`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60453 |
| `explicit.stat_1056492907` | 2.99576 |
| `explicit.stat_2676834156@T1` | 1.60873 |
| `explicit.stat_2541588185@T1` | 0.48291 |
| `explicit.stat_3138344128` | 0.02159 |
| `explicit.stat_2678930256` | 0.00722 |
| `explicit.stat_3246948616` | 0.00013 |
| `explicit.stat_1120862500@T2` | -0.00005 |
| `explicit.stat_1873752457@T2` | -0.00005 |
| `explicit.stat_2676834156@T2` | -0.00004 |
| `explicit.stat_1873752457@T1` | -0.00004 |
| `explicit.stat_828533480@T1` | -0.00004 |

### weapon.warstaff — n=5002, R²=-0.5544

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.00004`  ·  corrupted: `0.03069`  ·  n_sockets: `0.00001`  ·  quality: `0.00392`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 2.17670 |
| `rune.stat_731403740` | 1.54687 |
| `explicit.stat_9187492@T1` | 1.38582 |
| `rune.stat_1712188793` | -0.76950 |
| `desecrated.stat_9187492` | 0.63856 |
| `desecrated.stat_518292764` | 0.38020 |
| `crafted.stat_210067635@T2` | -0.22554 |
| `explicit.stat_2694482655@T1` | 0.16380 |
| `crafted.stat_3035140377` | 0.11807 |
| `desecrated.stat_669069897` | -0.11470 |
| `rune.stat_1509134228` | 0.08892 |
| `rune.stat_3336890334` | 0.07182 |

### weapon.staff — n=4644, R²=-0.5984

intercept: `-0.0007`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00028`  ·  n_sockets: `0.00001`  ·  quality: `0.00473`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.02436 |
| `explicit.stat_4226189338@T1` | 2.30250 |
| `explicit.stat_1600707273@T1` | 1.60938 |
| `explicit.stat_2254480358@T1` | 1.60931 |
| `explicit.stat_2254480358@T2` | 1.09790 |
| `explicit.stat_3962278098@T2` | 0.69266 |
| `explicit.stat_473429811@T1` | 0.66455 |
| `explicit.stat_124131830@T1` | 0.48656 |
| `crafted.stat_124131830` | 0.44522 |
| `explicit.stat_3291658075@T2` | 0.32497 |
| `rune.stat_3990135792` | -0.15314 |
| `rune.stat_975988108` | -0.11554 |

### weapon.sceptre — n=4620, R²=-0.6011

intercept: `-0.0263`  ·  log_price: True  ·  ilvl: `0.00033`  ·  n_mods: `-0.00008`  ·  n_top_tier: `0.54031`  ·  corrupted: `1.79100`  ·  n_sockets: `0.00074`  ·  quality: `0.07896`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.76138 |
| `explicit.stat_4080418644@T1` | -0.54123 |
| `explicit.stat_4080418644@T2` | -0.54110 |
| `explicit.stat_2347036682@T2` | -0.54097 |
| `explicit.stat_1263695895@T2` | -0.54092 |
| `explicit.stat_1250712710@T1` | -0.54061 |
| `explicit.stat_328541901@T1` | -0.54050 |
| `explicit.stat_2347036682@T1` | -0.54040 |
| `explicit.stat_789117908@T1` | -0.54032 |
| `explicit.stat_3984865854@T2` | -0.54028 |
| `explicit.stat_101878827@T1` | -0.54025 |
| `explicit.stat_1263695895@T1` | -0.54025 |

### weapon.spear — n=3997, R²=-0.5897

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00002`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00002`  ·  quality: `0.00561`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.30137 |
| `crafted.stat_3035140377` | 1.89991 |
| `crafted.stat_518292764` | 0.80844 |
| `explicit.stat_210067635@T1` | 0.69307 |
| `explicit.stat_1509134228@T1` | 0.49598 |
| `crafted.stat_210067635` | 0.19136 |
| `explicit.stat_9187492@T1` | 0.17111 |
| `explicit.stat_3336890334@T1` | 0.10783 |
| `rune.stat_1039491398` | 0.08025 |
| `explicit.stat_709508406@T1` | 0.01310 |
| `desecrated.stat_210067635` | -0.00914 |
| `desecrated.stat_1509134228` | 0.00739 |

### armour.focus — n=3223, R²=-0.6309

intercept: `-0.0271`  ·  log_price: True  ·  ilvl: `0.00033`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.55745`  ·  corrupted: `0.00098`  ·  n_sockets: `0.00080`  ·  quality: `0.05384`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -4.75557 |
| `desecrated.stat_3393628375@T1` | -2.52446 |
| `desecrated.stat_378817135@T1` | 2.12168 |
| `crafted.stat_2974417149@T1` | -1.23305 |
| `explicit.stat_789117908@T2` | -0.55826 |
| `explicit.stat_2231156303@T2` | -0.55822 |
| `explicit.stat_4052037485@T2` | -0.55803 |
| `explicit.stat_736967255@T2` | -0.55801 |
| `explicit.stat_2891184298@T2` | -0.55787 |
| `explicit.stat_2891184298@T1` | -0.55786 |
| `explicit.stat_789117908@T1` | -0.55786 |
| `explicit.stat_274716455@T1` | -0.55784 |

### armour.quiver — n=3024, R²=-0.6407

intercept: `-0.0144`  ·  log_price: True  ·  ilvl: `0.00017`  ·  n_mods: `0.00006`  ·  n_top_tier: `0.49905`  ·  corrupted: `0.00113`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.50379 |
| `explicit.stat_2463230181@T1` | 1.10830 |
| `explicit.stat_681332047@T2` | -0.50058 |
| `explicit.stat_681332047@T1` | -0.50036 |
| `explicit.stat_1573130764@T1` | -0.49984 |
| `explicit.stat_2194114101@T2` | -0.49955 |
| `explicit.stat_1368271171@T2` | -0.49951 |
| `explicit.stat_1573130764@T2` | -0.49947 |
| `explicit.stat_2321178454@T2` | -0.49939 |
| `explicit.stat_3714003708@T2` | -0.49932 |
| `explicit.stat_803737631@T2` | -0.49914 |
| `explicit.stat_1368271171@T1` | -0.49907 |

### armour.shield — n=2615, R²=-0.5154

intercept: `-0.0010`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.43209`  ·  corrupted: `0.20666`  ·  n_sockets: `0.00000`  ·  quality: `0.06870`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.74788 |
| `explicit.stat_1978899297@T2` | -0.55683 |
| `explicit.stat_1011760251@T1` | -0.43264 |
| `explicit.stat_1011760251@T2` | -0.43245 |
| `explicit.stat_328541901@T1` | -0.43217 |
| `explicit.stat_2339757871@T1` | -0.43215 |
| `explicit.stat_328541901@T2` | -0.43214 |
| `explicit.stat_3484657501@T1` | -0.43214 |
| `explicit.stat_2481353198@T1` | -0.43214 |
| `explicit.stat_3484657501@T2` | -0.43213 |
| `explicit.stat_3372524247@T2` | -0.43212 |
| `explicit.stat_2481353198@T2` | -0.43212 |

### weapon.twomace — n=2310, R²=-0.5636

intercept: `-0.0011`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.33448`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00002`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.29221 |
| `crafted.stat_3035140377` | 1.33925 |
| `desecrated.stat_1509134228@T1` | 0.80408 |
| `explicit.stat_1037193709@T1` | -0.33461 |
| `explicit.stat_3336890334@T1` | -0.33457 |
| `explicit.stat_387439868@T2` | -0.33453 |
| `explicit.stat_1263695895@T1` | -0.33453 |
| `explicit.stat_821021828@T2` | -0.33452 |
| `explicit.stat_1037193709@T2` | -0.33452 |
| `explicit.stat_821021828@T1` | -0.33451 |
| `explicit.stat_1263695895@T2` | -0.33451 |
| `explicit.stat_3695891184@T1` | -0.33451 |

## Coverage (listings per base)

- … **Sapphire** — 14032 listings (14014 priced) [0.3–7553463.8 ex]
- … **Emerald** — 13915 listings (13903 priced) [0.4–7553463.8 ex]
- … **Ruby** — 10671 listings (10661 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 6396 listings (6392 priced) [0.3–5288620.9 ex]
- … **Prismatic Ring** — 4914 listings (4912 priced) [0.3–24532814.5 ex]
- … **Stellar Amulet** — 4826 listings (4826 priced) [0.3–35690283.3 ex]
- … **Solar Amulet** — 4807 listings (4799 priced) [1.0–66666666.0 ex]
- … **Amethyst Ring** — 4716 listings (4715 priced) [0.3–4323655.9 ex]
- … **Gold Amulet** — 4588 listings (4583 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 4446 listings (4444 priced) [0.3–24532814.5 ex]
- … **Dueling Wand** — 4140 listings (4135 priced) [0.3–3736768402.2 ex]
- … **Sapphire Ring** — 3719 listings (3715 priced) [0.3–24532814.5 ex]
- … **Topaz Ring** — 3605 listings (3604 priced) [1.0–123132003.2 ex]
- … **Ruby Ring** — 3602 listings (3602 priced) [0.3–37474957.5 ex]
- … **Plate Belt** — 3273 listings (3270 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 3249 listings (3248 priced) [0.3–5286174.1 ex]
- … **Ancestral Tiara** — 3213 listings (3210 priced) [0.6–41469259.3 ex]
- … **Obliterator Bow** — 3167 listings (3159 priced) [0.4–22139622146.9 ex]
- … **Amber Amulet** — 3164 listings (3163 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3145 listings (3144 priced) [0.3–4547453.5 ex]
- … **Heavy Belt** — 3079 listings (3079 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 3010 listings (3010 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 2976 listings (2976 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 2893 listings (2893 priced) [0.3–24532814.5 ex]
- … **Lunar Amulet** — 2823 listings (2821 priced) [0.3–4877938.3 ex]

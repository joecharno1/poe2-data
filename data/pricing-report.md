# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-09T02:48:39+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **355197** (354653 priced in exalted)
- Distinct bases: 960 · distinct mods: 2895 · mod rows: 1686821
- Sold signals: **29347** sold · 190169 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-09T02:35:50+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×17.49** (median |log error| 2.8616)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.05** · typical error ×40.35 · ±30% 8% · n=51995
- Premium segment (60ex+): skill **+0.07** · typical error ×179.49 · ±30% 0% · n=32381

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 6849 | ×11.19 | 4% | +0.04 | +0.05 |
| accessory.amulet | 6485 | ×48.11 | 22% | +0.03 | +0.03 |
| jewel | 6055 | ×8.46 | 7% | +0.02 | +0.04 |
| accessory.belt | 5109 | ×10.00 | 21% | +0.02 | +0.02 |
| armour.chest | 5002 | ×8.58 | 11% | +0.01 | +0.03 |
| armour.helmet | 4930 | ×10.90 | 6% | +0.01 | +0.02 |
| armour.boots | 4596 | ×14.92 | 7% | +0.09 | +0.12 |
| armour.gloves | 4521 | ×17.27 | 6% | +0.05 | +0.07 |
| other | 4235 | ×9.99 | 37% | +0.06 | +0.14 |
| weapon.wand | 3039 | ×41.85 | 21% | +0.06 | +0.06 |
| weapon.bow | 2448 | ×24.03 | 19% | +0.09 | +0.10 |
| weapon.crossbow | 2266 | ×19.79 | 19% | +0.10 | +0.12 |
| weapon.warstaff | 1226 | ×74.99 | 17% | +0.07 | +0.06 |
| weapon.staff | 1068 | ×74.69 | 16% | +0.05 | +0.06 |
| weapon.sceptre | 1061 | ×49.99 | 12% | +0.08 | +0.10 |
| weapon.spear | 921 | ×50.00 | 18% | +0.03 | +0.04 |
| armour.focus | 739 | ×99.99 | 13% | +0.03 | +0.12 |
| armour.quiver | 731 | ×75.81 | 13% | +0.02 | +0.07 |
| flask.charm | 622 | ×77.76 | 32% | +0.00 | +0.02 |
| armour.shield | 588 | ×30.00 | 16% | +0.04 | +0.05 |
| weapon.twomace | 536 | ×20.00 | 18% | +0.05 | +0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=36055, R²=-0.5131

intercept: `1.6062`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `0.00810`  ·  n_top_tier: `0.48446`  ·  corrupted: `0.98112`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.28361 |
| `explicit.stat_1589917703@T1` | -1.12222 |
| `explicit.stat_2891184298@T1` | 1.01362 |
| `explicit.stat_101878827@T1` | -0.98839 |
| `explicit.stat_2106365538@T1` | 0.96662 |
| `explicit.stat_2974417149@T1` | 0.92217 |
| `explicit.stat_3917489142@T1` | 0.86222 |
| `explicit.stat_3141070085@T1` | -0.83040 |
| `explicit.stat_1050105434@T1` | -0.77273 |
| `explicit.stat_789117908@T1` | -0.57541 |
| `explicit.stat_2482852589@T1` | 0.53845 |
| `implicit.stat_1379411836` | -0.25919 |

### jewel — n=32759, R²=-0.6455

intercept: `-1.1941`  ·  log_price: True  ·  ilvl: `0.03674`  ·  n_mods: `0.21030`  ·  n_top_tier: `-0.07097`  ·  corrupted: `0.15698`  ·  quality: `0.22393`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -4.40455 |
| `explicit.stat_3741323227@T1` | -3.29377 |
| `explicit.stat_1569101201@T1` | 2.80463 |
| `explicit.stat_3780644166@T1` | -2.78570 |
| `explicit.stat_2527686725@T1` | 2.59245 |
| `explicit.stat_234296660@T1` | -2.53957 |
| `explicit.stat_3374165039@T1` | -1.95214 |
| `explicit.stat_3714003708@T1` | -1.71542 |
| `explicit.stat_293638271@T1` | -1.63630 |
| `explicit.stat_1316278494@T1` | -1.44186 |
| `explicit.stat_3485067555@T1` | 1.44147 |
| `explicit.stat_3668351662@T1` | -1.43957 |

### accessory.ring — n=31354, R²=-1.2075

intercept: `3.7767`  ·  log_price: True  ·  ilvl: `-0.03935`  ·  n_mods: `-0.01892`  ·  n_top_tier: `-0.01229`  ·  corrupted: `0.98144`  ·  n_sockets: `0.77114`  ·  quality: `0.02907`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.73019 |
| `explicit.stat_707457662@T2` | 4.32002 |
| `explicit.stat_1379411836@T1` | -1.60897 |
| `explicit.stat_1573130764@T1` | -1.09868 |
| `explicit.stat_1379411836@T2` | -1.03020 |
| `explicit.stat_2923486259@T1` | 0.88132 |
| `explicit.stat_1368271171@T1` | -0.77305 |
| `explicit.stat_1368271171@T2` | -0.75032 |
| `explicit.stat_707457662` | -0.70836 |
| `explicit.stat_2923486259@T2` | 0.70364 |
| `explicit.stat_1263695895@T1` | -0.64609 |
| `explicit.stat_4080418644@T2` | 0.60377 |

### accessory.amulet — n=29529, R²=-2.0825

intercept: `3.8549`  ·  log_price: True  ·  ilvl: `-0.04640`  ·  n_mods: `-0.02437`  ·  n_top_tier: `0.56972`  ·  corrupted: `0.16244`  ·  n_sockets: `1.71293`  ·  quality: `-0.00356`

| stat_id | coef |
|---|---|
| `explicit.stat_3981240776@T2` | 1.32065 |
| `explicit.stat_3981240776@T1` | 1.26516 |
| `explicit.stat_983749596@T1` | -1.21748 |
| `explicit.stat_124131830` | 1.10093 |
| `explicit.stat_983749596@T2` | -1.03294 |
| `explicit.stat_1202301673@T2` | 0.76101 |
| `explicit.stat_9187492@T2` | 0.75237 |
| `explicit.stat_2748665614@T2` | -0.67724 |
| `explicit.stat_3299347043@T1` | -0.65939 |
| `explicit.stat_2748665614@T1` | -0.64648 |
| `explicit.stat_472520716@T2` | -0.64309 |
| `explicit.stat_472520716@T1` | -0.64061 |

### accessory.belt — n=23582, R²=-0.1492

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.14021`  ·  corrupted: `0.00006`  ·  n_sockets: `-0.69309`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -0.14027 |
| `explicit.stat_51994685@T1` | -0.14024 |
| `explicit.stat_1570770415@T1` | -0.14023 |
| `explicit.stat_644456512@T1` | -0.14023 |
| `explicit.stat_1389754388@T2` | -0.14023 |
| `explicit.stat_1671376347@T2` | -0.14022 |
| `explicit.stat_2923486259@T2` | -0.14022 |
| `explicit.stat_2881298780@T1` | -0.14022 |
| `explicit.stat_4220027924@T2` | -0.14022 |
| `explicit.stat_3325883026@T1` | -0.14022 |
| `explicit.stat_1836676211@T2` | -0.14022 |
| `explicit.stat_3299347043@T2` | -0.14022 |

### armour.chest — n=23316, R²=-0.4283

intercept: `3.0576`  ·  log_price: True  ·  ilvl: `-0.01743`  ·  n_mods: `-0.07587`  ·  n_top_tier: `0.24186`  ·  corrupted: `0.10275`  ·  n_sockets: `0.02405`  ·  quality: `0.00583`

| stat_id | coef |
|---|---|
| `implicit.stat_1978899297` | -1.14684 |
| `implicit.stat_2251279027` | 0.68082 |
| `explicit.stat_915769802@T1` | -0.52274 |
| `explicit.stat_3484657501@T1` | -0.50256 |
| `explicit.stat_3325883026@T2` | -0.48910 |
| `explicit.stat_915769802@T2` | -0.40869 |
| `explicit.stat_3261801346@T1` | -0.39134 |
| `explicit.stat_2451402625@T2` | -0.35550 |
| `explicit.stat_4080418644@T1` | -0.35264 |
| `explicit.stat_986397080@T2` | -0.31185 |
| `explicit.stat_3301100256@T2` | -0.29960 |
| `explicit.stat_2451402625@T1` | -0.27809 |

### armour.helmet — n=22827, R²=-0.4783

intercept: `3.4440`  ·  log_price: True  ·  ilvl: `-0.02929`  ·  n_mods: `-0.10984`  ·  n_top_tier: `0.38488`  ·  corrupted: `0.70258`  ·  n_sockets: `0.03599`  ·  quality: `0.02682`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.53128 |
| `explicit.stat_4080418644@T2` | -0.91023 |
| `explicit.stat_53045048@T2` | -0.74746 |
| `explicit.stat_4080418644@T1` | -0.69224 |
| `explicit.stat_3362812763@T2` | -0.68283 |
| `explicit.stat_53045048@T1` | -0.57925 |
| `explicit.stat_2339757871@T1` | -0.55425 |
| `explicit.stat_3362812763@T1` | -0.53977 |
| `explicit.stat_1999113824@T1` | -0.52615 |
| `explicit.stat_2451402625@T1` | -0.49617 |
| `explicit.stat_3261801346@T1` | -0.49009 |
| `explicit.stat_803737631@T2` | -0.48264 |

### armour.boots — n=21405, R²=-0.9731

intercept: `4.3950`  ·  log_price: True  ·  ilvl: `-0.05214`  ·  n_mods: `-0.11211`  ·  n_top_tier: `0.54070`  ·  corrupted: `0.31758`  ·  n_sockets: `0.13554`  ·  quality: `0.01824`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.83826 |
| `explicit.stat_2250533757@T1` | 1.36596 |
| `crafted.stat_3917489142@T1` | -1.19639 |
| `explicit.stat_2923486259@T2` | -0.96178 |
| `explicit.stat_3362812763@T1` | -0.89446 |
| `explicit.stat_1062208444@T2` | -0.88912 |
| `desecrated.stat_2250533757@T2` | -0.87748 |
| `rune.stat_836936635` | -0.82244 |
| `explicit.stat_3321629045@T1` | -0.80075 |
| `explicit.stat_2160282525@T1` | -0.75406 |
| `explicit.stat_1999113824@T1` | -0.74852 |
| `explicit.stat_328541901@T1` | -0.73057 |

### armour.gloves — n=20862, R²=-0.936

intercept: `3.8211`  ·  log_price: True  ·  ilvl: `-0.04955`  ·  n_mods: `-0.12546`  ·  n_top_tier: `0.52238`  ·  corrupted: `0.30278`  ·  n_sockets: `0.34733`  ·  quality: `0.01452`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.42271 |
| `explicit.stat_681332047@T2` | -1.00870 |
| `explicit.stat_3484657501@T2` | -0.95651 |
| `explicit.stat_803737631@T2` | -0.93512 |
| `explicit.stat_3299347043@T2` | -0.83109 |
| `explicit.stat_328541901@T1` | -0.79176 |
| `explicit.stat_4220027924@T2` | -0.75345 |
| `explicit.stat_3321629045@T1` | -0.69264 |
| `explicit.stat_681332047@T1` | -0.67160 |
| `explicit.stat_2797971005@T2` | -0.65460 |
| `explicit.stat_3695891184@T2` | -0.65291 |
| `explicit.stat_1754445556@T1` | -0.64666 |

### weapon.wand — n=14073, R²=-2.1239

intercept: `3.6590`  ·  log_price: True  ·  ilvl: `-0.04566`  ·  n_mods: `-0.00976`  ·  n_top_tier: `0.34045`  ·  corrupted: `-0.01152`  ·  n_sockets: `0.03347`  ·  quality: `0.01575`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 3.14035 |
| `explicit.stat_4226189338@T1` | 2.05780 |
| `explicit.stat_591105508@T1` | 2.04490 |
| `explicit.stat_1545858329@T1` | 2.03156 |
| `explicit.stat_124131830@T1` | 1.92874 |
| `explicit.stat_736967255@T2` | 1.81670 |
| `explicit.stat_1600707273@T1` | 1.11378 |
| `crafted.stat_124131830` | 0.84075 |
| `explicit.stat_1600707273@T2` | 0.63030 |
| `explicit.stat_2974417149@T1` | 0.47486 |
| `explicit.stat_2768835289@T2` | -0.39405 |
| `explicit.stat_2231156303@T2` | -0.38303 |

### weapon.bow — n=11473, R²=-1.9531

intercept: `3.4262`  ·  log_price: True  ·  ilvl: `-0.04237`  ·  n_mods: `-0.01121`  ·  n_top_tier: `0.73581`  ·  corrupted: `0.27956`  ·  n_sockets: `0.00264`  ·  quality: `0.00967`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.27068 |
| `desecrated.stat_666077204@T1` | 1.57614 |
| `explicit.stat_2463230181@T1` | 1.53314 |
| `crafted.stat_3035140377` | 1.49559 |
| `explicit.stat_1202301673@T1` | 1.43135 |
| `rune.stat_3885405204` | -0.93544 |
| `explicit.stat_55876295@T1` | -0.79417 |
| `explicit.stat_1037193709@T1` | -0.78049 |
| `explicit.stat_3695891184@T2` | -0.76723 |
| `explicit.stat_3336890334@T2` | -0.76312 |
| `explicit.stat_3695891184@T1` | -0.76231 |
| `explicit.stat_3261801346@T1` | -0.76129 |

### weapon.crossbow — n=10737, R²=-1.8302

intercept: `3.6592`  ·  log_price: True  ·  ilvl: `-0.04522`  ·  n_mods: `-0.01160`  ·  n_top_tier: `0.69279`  ·  corrupted: `-0.02137`  ·  n_sockets: `0.02371`  ·  quality: `0.00474`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.90185 |
| `explicit.stat_2250681686@T2` | -1.49359 |
| `explicit.stat_1202301673@T1` | 1.39532 |
| `explicit.stat_709508406@T1` | 1.35480 |
| `explicit.stat_1980802737` | 1.15749 |
| `explicit.stat_1202301673@T2` | -0.88655 |
| `crafted.stat_3035140377` | 0.82868 |
| `explicit.stat_1509134228@T2` | -0.82683 |
| `explicit.stat_2250681686` | 0.80072 |
| `explicit.stat_1509134228@T1` | 0.78837 |
| `explicit.stat_1263695895@T2` | -0.78162 |
| `explicit.stat_669069897@T1` | -0.74536 |

### flask.charm — n=8026, R²=-0.4252

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00111`  ·  corrupted: `0.52940`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.35360 |
| `explicit.stat_1056492907` | 3.12477 |
| `explicit.stat_2676834156@T1` | 1.60827 |
| `explicit.stat_2541588185@T1` | 0.21598 |
| `explicit.stat_3138344128` | 0.02095 |
| `explicit.stat_2678930256` | 0.01656 |
| `explicit.stat_1120862500@T2` | -0.00112 |
| `explicit.stat_1873752457@T2` | -0.00112 |
| `explicit.stat_388617051@T2` | -0.00111 |
| `explicit.stat_828533480@T2` | -0.00111 |
| `explicit.stat_3196823591@T2` | -0.00111 |
| `explicit.stat_2676834156@T2` | -0.00111 |

### weapon.warstaff — n=5701, R²=-0.5628

intercept: `-0.0031`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `-0.00008`  ·  n_top_tier: `0.20151`  ·  corrupted: `0.68802`  ·  n_sockets: `0.00006`  ·  quality: `0.04238`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T1` | 1.40752 |
| `rune.stat_243313994` | 1.25375 |
| `rune.stat_731403740` | 1.24632 |
| `crafted.stat_210067635@T2` | -0.54338 |
| `rune.stat_1712188793` | -0.48535 |
| `desecrated.stat_9187492` | 0.47056 |
| `crafted.stat_3035140377` | 0.34592 |
| `desecrated.stat_518292764` | 0.28464 |
| `rune.stat_1037193709` | 0.27263 |
| `rune.stat_3336890334` | 0.25769 |
| `explicit.stat_691932474@T1` | -0.20168 |
| `explicit.stat_709508406@T1` | -0.20167 |

### weapon.staff — n=5274, R²=-0.6152

intercept: `-0.0217`  ·  log_price: True  ·  ilvl: `0.00027`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.32270`  ·  corrupted: `0.04706`  ·  n_sockets: `0.00081`  ·  quality: `0.00044`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 4.24605 |
| `explicit.stat_4226189338@T1` | 2.13429 |
| `explicit.stat_2254480358@T1` | 1.28518 |
| `explicit.stat_2254480358@T2` | 1.28452 |
| `explicit.stat_2768835289@T2` | 1.26465 |
| `explicit.stat_4226189338@T2` | 1.07260 |
| `explicit.stat_1545858329@T1` | 1.05801 |
| `explicit.stat_3291658075@T2` | 0.82271 |
| `explicit.stat_1600707273@T1` | 0.77451 |
| `explicit.stat_124131830@T1` | 0.75184 |
| `crafted.stat_124131830` | 0.37783 |
| `explicit.stat_3962278098@T2` | 0.37096 |

### weapon.sceptre — n=5238, R²=-0.6089

intercept: `-1.2968`  ·  log_price: True  ·  ilvl: `0.01617`  ·  n_mods: `-0.00924`  ·  n_top_tier: `0.51927`  ·  corrupted: `1.23825`  ·  n_sockets: `0.03543`  ·  quality: `0.08206`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.82160 |
| `explicit.stat_3984865854@T1` | 0.99580 |
| `explicit.stat_4080418644@T1` | -0.58777 |
| `explicit.stat_4080418644@T2` | -0.55398 |
| `explicit.stat_1263695895@T1` | -0.54805 |
| `explicit.stat_1263695895@T2` | -0.54618 |
| `explicit.stat_1574590649@T2` | -0.53938 |
| `explicit.stat_2854751904@T1` | -0.53485 |
| `explicit.stat_1574590649@T1` | -0.53177 |
| `explicit.stat_2347036682@T2` | -0.53000 |
| `explicit.stat_1998951374@T1` | -0.52616 |
| `explicit.stat_328541901@T1` | -0.52582 |

### weapon.spear — n=4447, R²=-0.6042

intercept: `-0.0025`  ·  log_price: True  ·  ilvl: `0.00003`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.16831`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00007`  ·  quality: `0.04620`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.53769 |
| `crafted.stat_3035140377` | 1.25490 |
| `explicit.stat_9187492@T1` | 1.16991 |
| `explicit.stat_210067635@T1` | 0.93040 |
| `explicit.stat_3336890334@T1` | 0.64187 |
| `crafted.stat_518292764` | 0.57668 |
| `explicit.stat_1509134228@T1` | 0.52466 |
| `explicit.stat_709508406@T1` | 0.52406 |
| `explicit.stat_691932474@T1` | -0.16839 |
| `explicit.stat_1263695895@T2` | -0.16838 |
| `explicit.stat_709508406@T2` | -0.16838 |
| `explicit.stat_55876295@T1` | -0.16838 |

### armour.focus — n=3606, R²=-0.6333

intercept: `-1.3726`  ·  log_price: True  ·  ilvl: `0.01695`  ·  n_mods: `-0.00548`  ·  n_top_tier: `0.57385`  ·  corrupted: `0.00205`  ·  n_sockets: `0.04241`  ·  quality: `0.07920`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -5.07611 |
| `crafted.stat_2974417149@T1` | -4.15806 |
| `desecrated.stat_378817135@T1` | -0.86382 |
| `explicit.stat_124131830@T2` | -0.65045 |
| `explicit.stat_1671376347@T1` | 0.63274 |
| `explicit.stat_4220027924@T2` | -0.61627 |
| `explicit.stat_274716455@T1` | -0.61337 |
| `explicit.stat_789117908@T2` | -0.61335 |
| `explicit.stat_2974417149@T1` | -0.60375 |
| `explicit.stat_2891184298@T2` | -0.60291 |
| `explicit.stat_736967255@T2` | -0.60242 |
| `explicit.stat_3291658075@T1` | -0.59285 |

### armour.quiver — n=3403, R²=-0.6368

intercept: `-0.7786`  ·  log_price: True  ·  ilvl: `0.00930`  ·  n_mods: `0.00207`  ·  n_top_tier: `0.83798`  ·  corrupted: `0.54714`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 13.56493 |
| `explicit.stat_2463230181@T2` | -1.41044 |
| `desecrated.stat_3932115504` | -1.03780 |
| `explicit.stat_681332047@T2` | -0.90991 |
| `explicit.stat_681332047@T1` | -0.89504 |
| `explicit.stat_1573130764@T1` | -0.87580 |
| `explicit.stat_2194114101@T2` | -0.86548 |
| `explicit.stat_1573130764@T2` | -0.86388 |
| `explicit.stat_1368271171@T2` | -0.86188 |
| `explicit.stat_3714003708@T2` | -0.85025 |
| `explicit.stat_1368271171@T1` | -0.84525 |
| `explicit.stat_2321178454@T2` | -0.84355 |

### armour.shield — n=2932, R²=-0.5846

intercept: `-0.0438`  ·  log_price: True  ·  ilvl: `0.00054`  ·  n_mods: `0.00009`  ·  n_top_tier: `0.44642`  ·  corrupted: `0.03758`  ·  n_sockets: `0.00026`  ·  quality: `0.07548`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.85836 |
| `explicit.stat_1978899297@T2` | -0.59851 |
| `explicit.stat_3855016469@T1` | 0.48588 |
| `explicit.stat_1011760251@T2` | -0.45755 |
| `explicit.stat_328541901@T1` | -0.45067 |
| `explicit.stat_2481353198@T1` | -0.44989 |
| `explicit.stat_2481353198@T2` | -0.44969 |
| `explicit.stat_3484657501@T1` | -0.44919 |
| `explicit.stat_2339757871@T1` | -0.44876 |
| `explicit.stat_3484657501@T2` | -0.44820 |
| `explicit.stat_328541901@T2` | -0.44794 |
| `explicit.stat_3372524247@T2` | -0.44770 |

### weapon.twomace — n=2608, R²=-0.5975

intercept: `-0.0748`  ·  log_price: True  ·  ilvl: `0.00094`  ·  n_mods: `0.00008`  ·  n_top_tier: `0.67801`  ·  corrupted: `0.03767`  ·  n_sockets: `0.00203`  ·  quality: `0.00188`

| stat_id | coef |
|---|---|
| `desecrated.stat_1509134228@T1` | -1.80324 |
| `crafted.stat_3035140377` | 1.21870 |
| `explicit.stat_210067635@T1` | 0.93317 |
| `explicit.stat_3336890334@T1` | -0.68605 |
| `explicit.stat_387439868@T2` | -0.68293 |
| `explicit.stat_1037193709@T1` | -0.68240 |
| `explicit.stat_821021828@T2` | -0.68069 |
| `explicit.stat_1037193709@T2` | -0.67966 |
| `explicit.stat_821021828@T1` | -0.67955 |
| `explicit.stat_2694482655@T1` | -0.67931 |
| `explicit.stat_3695891184@T1` | -0.67907 |
| `explicit.stat_3639275092@T2` | -0.67871 |

## Coverage (listings per base)

- … **Sapphire** — 15528 listings (15506 priced) [0.4–7553463.8 ex]
- … **Emerald** — 15385 listings (15371 priced) [0.4–7553463.8 ex]
- … **Ruby** — 11874 listings (11862 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 6904 listings (6898 priced) [0.3–5288620.9 ex]
- … **Prismatic Ring** — 5459 listings (5454 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 5312 listings (5303 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 5229 listings (5227 priced) [0.4–4323655.9 ex]
- … **Stellar Amulet** — 5193 listings (5190 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 5051 listings (5044 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 4850 listings (4848 priced) [0.4–24532814.5 ex]
- … **Dueling Wand** — 4432 listings (4424 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4080 listings (4075 priced) [0.4–307202867.9 ex]
- … **Ruby Ring** — 3958 listings (3956 priced) [0.4–37474957.5 ex]
- … **Topaz Ring** — 3943 listings (3940 priced) [1.0–307202867.9 ex]
- … **Plate Belt** — 3595 listings (3590 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 3558 listings (3556 priced) [0.4–5286174.1 ex]
- … **Ancestral Tiara** — 3514 listings (3509 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3484 listings (3483 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3468 listings (3467 priced) [0.3–4547453.5 ex]
- … **Obliterator Bow** — 3406 listings (3397 priced) [0.4–22139622146.9 ex]
- … **Heavy Belt** — 3351 listings (3350 priced) [0.4–4877938.3 ex]
- … **Unset Ring** — 3346 listings (3345 priced) [0.4–24532814.5 ex]
- … **Bloodstone Amulet** — 3251 listings (3250 priced) [0.4–4275054.0 ex]
- … **Pearl Ring** — 3174 listings (3172 priced) [0.4–24532814.5 ex]
- … **Azure Amulet** — 3095 listings (3095 priced) [0.4–123132003.2 ex]

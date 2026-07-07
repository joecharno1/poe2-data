# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-07T18:17:03+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **289004** (288677 priced in exalted)
- Distinct bases: 950 · distinct mods: 2775 · mod rows: 1373562
- Sold signals: **31802** sold · 153386 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-07T18:07:47+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×16.82** (median |log error| 2.8224)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 75% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×43.45 · ±30% 13% · n=41714
- Premium segment (60ex+): skill **+0.07** · typical error ×188.05 · ±30% 0% · n=26072

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 5453 | ×11.30 | 4% | +0.03 | +0.05 |
| accessory.amulet | 5175 | ×55.24 | 20% | +0.02 | +0.02 |
| jewel | 4703 | ×8.22 | 8% | +0.01 | +0.04 |
| accessory.belt | 4219 | ×18.25 | 20% | +0.05 | +0.08 |
| armour.chest | 4182 | ×10.00 | 27% | +0.01 | +0.01 |
| armour.helmet | 4020 | ×10.00 | 26% | +0.01 | +0.01 |
| armour.boots | 3831 | ×10.00 | 26% | +0.00 | +0.00 |
| armour.gloves | 3773 | ×10.00 | 24% | +0.00 | +0.01 |
| other | 3523 | ×10.00 | 35% | +0.09 | +0.34 |
| weapon.wand | 2599 | ×23.96 | 22% | +0.06 | +0.06 |
| weapon.bow | 2118 | ×19.73 | 20% | +0.09 | +0.09 |
| weapon.crossbow | 1998 | ×17.75 | 20% | +0.09 | +0.11 |
| weapon.warstaff | 886 | ×78.63 | 19% | +0.02 | +0.01 |
| weapon.staff | 844 | ×50.00 | 20% | +0.04 | +0.05 |
| weapon.sceptre | 842 | ×99.00 | 13% | +0.04 | +0.03 |
| weapon.spear | 708 | ×50.00 | 23% | +0.02 | +0.02 |
| armour.focus | 573 | ×659.97 | 11% | +0.00 | +0.03 |
| armour.quiver | 562 | ×99.00 | 14% | +0.00 | +0.03 |
| armour.shield | 436 | ×50.00 | 18% | +0.01 | +0.02 |
| weapon.twomace | 419 | ×20.00 | 19% | +0.07 | +0.03 |
| flask.charm | 395 | ×5.00 | 45% | -0.00 | +0.02 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=30359, R²=-0.4332

intercept: `1.6035`  ·  log_price: True  ·  ilvl: `0.00008`  ·  n_mods: `0.05566`  ·  n_top_tier: `0.78356`  ·  corrupted: `1.44371`  ·  n_sockets: `-0.00011`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.58460 |
| `explicit.stat_2106365538@T1` | 3.26212 |
| `explicit.stat_1589917703@T1` | 3.23726 |
| `explicit.stat_101878827@T1` | 3.23657 |
| `explicit.stat_3141070085@T1` | 2.53819 |
| `explicit.stat_2891184298@T1` | 2.11213 |
| `explicit.stat_1050105434@T1` | -1.73081 |
| `explicit.stat_3917489142@T1` | 1.46865 |
| `explicit.stat_789117908@T1` | -0.96382 |
| `explicit.stat_2974417149@T1` | 0.81246 |
| `implicit.stat_1379411836` | -0.27731 |
| `implicit.stat_2901986750` | 0.22874 |

### jewel — n=25395, R²=-0.6275

intercept: `-1.1467`  ·  log_price: True  ·  ilvl: `0.03711`  ·  n_mods: `0.12672`  ·  n_top_tier: `-0.00743`  ·  corrupted: `0.46397`  ·  quality: `0.20892`

| stat_id | coef |
|---|---|
| `explicit.stat_3714003708@T1` | -3.82824 |
| `explicit.stat_1569101201@T1` | 3.52567 |
| `explicit.stat_1316278494@T1` | -3.31406 |
| `explicit.stat_3192728503@T1` | -3.21465 |
| `explicit.stat_21071013@T1` | -3.20237 |
| `explicit.stat_3668351662@T1` | -3.14721 |
| `explicit.stat_1854213750@T1` | -2.85136 |
| `explicit.stat_1594812856@T1` | -2.55926 |
| `explicit.stat_3741323227@T1` | -2.48391 |
| `explicit.stat_153777645@T1` | 2.40044 |
| `explicit.stat_2527686725@T1` | 2.09434 |
| `explicit.stat_1697951953@T1` | -2.09084 |

### accessory.ring — n=24955, R²=-1.2381

intercept: `4.5630`  ·  log_price: True  ·  ilvl: `-0.04301`  ·  n_mods: `-0.13080`  ·  n_top_tier: `0.11598`  ·  corrupted: `0.83826`  ·  n_sockets: `-1.46544`  ·  quality: `0.03002`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.12326 |
| `explicit.stat_707457662@T2` | 2.96719 |
| `explicit.stat_1379411836@T1` | -2.44081 |
| `explicit.stat_1379411836@T2` | -1.98338 |
| `explicit.stat_1368271171@T2` | -1.10164 |
| `explicit.stat_1368271171@T1` | -0.90317 |
| `explicit.stat_2923486259@T2` | 0.74547 |
| `explicit.stat_1573130764@T1` | -0.65374 |
| `explicit.stat_707457662` | -0.58968 |
| `explicit.stat_4080418644@T2` | 0.58143 |
| `explicit.stat_3299347043@T1` | -0.51892 |
| `explicit.stat_3291658075@T1` | -0.50943 |

### accessory.amulet — n=23716, R²=-2.1072

intercept: `4.1481`  ·  log_price: True  ·  ilvl: `-0.05027`  ·  n_mods: `-0.02667`  ·  n_top_tier: `1.10725`  ·  corrupted: `0.10367`  ·  n_sockets: `1.30392`  ·  quality: `-0.00296`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | -2.84566 |
| `explicit.stat_983749596@T1` | -1.49974 |
| `explicit.stat_983749596@T2` | -1.39268 |
| `explicit.stat_3299347043@T1` | -1.26821 |
| `explicit.stat_3917489142@T2` | -1.21733 |
| `explicit.stat_3917489142@T1` | -1.20987 |
| `explicit.stat_2748665614@T1` | -1.20487 |
| `explicit.stat_3325883026@T1` | -1.19932 |
| `explicit.stat_472520716@T1` | -1.18280 |
| `explicit.stat_2748665614@T2` | -1.18222 |
| `explicit.stat_3489782002@T2` | -1.17683 |
| `explicit.stat_472520716@T2` | -1.15768 |

### accessory.belt — n=19549, R²=-1.4214

intercept: `3.7079`  ·  log_price: True  ·  ilvl: `-0.04417`  ·  n_mods: `-0.02207`  ·  n_top_tier: `0.77916`  ·  corrupted: `0.53315`  ·  n_sockets: `-0.13420`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.00780 |
| `explicit.stat_1389754388@T1` | -0.82738 |
| `explicit.stat_2881298780@T1` | -0.82717 |
| `explicit.stat_809229260@T2` | -0.82173 |
| `explicit.stat_51994685@T1` | -0.81180 |
| `explicit.stat_4220027924@T2` | -0.80745 |
| `explicit.stat_3299347043@T1` | -0.79953 |
| `explicit.stat_3299347043@T2` | -0.79728 |
| `explicit.stat_1671376347@T2` | -0.79604 |
| `explicit.stat_2923486259@T2` | -0.79504 |
| `explicit.stat_3325883026@T1` | -0.79291 |
| `explicit.stat_915769802@T2` | -0.79267 |

### armour.chest — n=19315, R²=-0.2206

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.13928`  ·  corrupted: `0.01477`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 0.18901 |
| `explicit.stat_915769802@T2` | -0.13930 |
| `explicit.stat_915769802@T1` | -0.13930 |
| `explicit.stat_4080418644@T2` | -0.13929 |
| `explicit.stat_3261801346@T1` | -0.13929 |
| `explicit.stat_2339757871@T2` | -0.13929 |
| `explicit.stat_3261801346@T2` | -0.13928 |
| `explicit.stat_2451402625@T2` | -0.13928 |
| `explicit.stat_124859000@T2` | -0.13928 |
| `explicit.stat_3484657501@T1` | -0.13928 |
| `explicit.stat_53045048@T2` | -0.13928 |
| `explicit.stat_1062208444@T2` | -0.13928 |

### armour.helmet — n=18929, R²=-0.2454

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.43392`  ·  corrupted: `1.48938`  ·  n_sockets: `0.00000`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.02591 |
| `explicit.stat_1263695895@T2` | -0.43394 |
| `explicit.stat_1263695895@T1` | -0.43394 |
| `explicit.stat_3362812763@T2` | -0.43394 |
| `explicit.stat_2451402625@T1` | -0.43394 |
| `explicit.stat_3362812763@T1` | -0.43393 |
| `explicit.stat_53045048@T2` | -0.43392 |
| `explicit.stat_4080418644@T2` | -0.43392 |
| `explicit.stat_2451402625@T2` | -0.43392 |
| `explicit.stat_3325883026@T1` | -0.43392 |
| `explicit.stat_53045048@T1` | -0.43392 |
| `explicit.stat_3917489142@T2` | -0.43392 |

### armour.boots — n=17833, R²=-0.2842

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.18552`  ·  corrupted: `0.00825`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2250533757@T2` | -0.18554 |
| `explicit.stat_3917489142@T2` | -0.18554 |
| `explicit.stat_2339757871@T1` | -0.18553 |
| `explicit.stat_2451402625@T2` | -0.18553 |
| `explicit.stat_3261801346@T2` | -0.18553 |
| `explicit.stat_2923486259@T2` | -0.18553 |
| `explicit.stat_1062208444@T2` | -0.18553 |
| `explicit.stat_99927264@T2` | -0.18553 |
| `explicit.stat_1999113824@T1` | -0.18552 |
| `explicit.stat_3917489142@T1` | -0.18552 |
| `explicit.stat_1062208444@T1` | -0.18552 |
| `explicit.stat_53045048@T1` | -0.18552 |

### armour.gloves — n=17429, R²=-0.3261

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00012`  ·  corrupted: `0.00780`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.09691 |
| `desecrated.stat_4067062424` | 0.08704 |
| `pseudo.total_ele_res>=80` | 0.02876 |
| `desecrated.stat_1573130764` | 0.02148 |
| `desecrated.stat_3299347043` | 0.00318 |
| `explicit.stat_9187492@T1` | 0.00159 |
| `explicit.stat_9187492@T2` | -0.00077 |
| `explicit.stat_9187492` | 0.00067 |
| `explicit.stat_2339757871@T1` | -0.00021 |
| `explicit.stat_2923486259@T1` | 0.00020 |
| `explicit.stat_3484657501@T2` | -0.00018 |
| `explicit.stat_2797971005@T2` | -0.00015 |

### weapon.wand — n=12058, R²=-2.0191

intercept: `3.4156`  ·  log_price: True  ·  ilvl: `-0.04269`  ·  n_mods: `-0.01041`  ·  n_top_tier: `0.84292`  ·  corrupted: `0.03954`  ·  n_sockets: `0.00875`  ·  quality: `0.01559`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 1.59139 |
| `explicit.stat_124131830@T1` | 1.58659 |
| `explicit.stat_591105508@T1` | 1.52845 |
| `explicit.stat_4226189338@T1` | 1.52312 |
| `explicit.stat_1600707273@T1` | 1.43071 |
| `explicit.stat_1545858329@T1` | 1.38948 |
| `explicit.stat_737908626@T1` | -0.90082 |
| `explicit.stat_473429811@T2` | -0.88113 |
| `explicit.stat_3962278098@T2` | -0.87717 |
| `explicit.stat_2768835289@T2` | -0.87354 |
| `explicit.stat_3639275092@T1` | -0.87021 |
| `explicit.stat_473429811@T1` | -0.86848 |

### weapon.bow — n=9821, R²=-1.9033

intercept: `3.4247`  ·  log_price: True  ·  ilvl: `-0.04253`  ·  n_mods: `-0.01095`  ·  n_top_tier: `0.53026`  ·  corrupted: `-0.00734`  ·  n_sockets: `0.00355`  ·  quality: `0.00568`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | 1.78542 |
| `desecrated.stat_210067635@T1` | -1.76235 |
| `explicit.stat_1202301673@T1` | 1.60440 |
| `crafted.stat_3035140377` | 1.19112 |
| `explicit.stat_518292764@T1` | 1.05861 |
| `explicit.stat_55876295@T1` | -0.58458 |
| `explicit.stat_3336890334@T2` | -0.57443 |
| `explicit.stat_3261801346@T1` | -0.57303 |
| `explicit.stat_2694482655@T1` | -0.56696 |
| `explicit.stat_3695891184@T2` | -0.56640 |
| `explicit.stat_1037193709@T1` | -0.56449 |
| `explicit.stat_1368271171@T2` | -0.56389 |

### weapon.crossbow — n=9289, R²=-1.7496

intercept: `3.6309`  ·  log_price: True  ·  ilvl: `-0.04539`  ·  n_mods: `-0.00148`  ·  n_top_tier: `0.70164`  ·  corrupted: `-0.01772`  ·  n_sockets: `0.01637`  ·  quality: `0.00510`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -2.78167 |
| `explicit.stat_1980802737` | 2.03039 |
| `explicit.stat_2250681686@T2` | -1.54781 |
| `explicit.stat_709508406@T1` | 1.48287 |
| `explicit.stat_1202301673@T1` | 1.46582 |
| `explicit.stat_1037193709@T1` | 1.20046 |
| `rune.stat_55876295` | 0.98473 |
| `explicit.stat_1509134228@T1` | 0.94892 |
| `rune.stat_2246411426` | -0.91375 |
| `crafted.stat_3035140377` | 0.89367 |
| `explicit.stat_2250681686` | 0.84750 |
| `explicit.stat_1202301673@T2` | -0.82896 |

### flask.charm — n=5929, R²=-0.292

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00004`  ·  corrupted: `0.04990`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.01283 |
| `explicit.stat_1056492907` | 2.99629 |
| `explicit.stat_2676834156@T1` | 1.60936 |
| `explicit.stat_3138344128` | 0.02221 |
| `explicit.stat_2678930256` | 0.00181 |
| `explicit.stat_2541588185@T1` | 0.00090 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_3196823591@T2` | -0.00004 |
| `explicit.stat_1873752457@T1` | -0.00004 |
| `explicit.stat_828533480@T1` | -0.00004 |
| `explicit.stat_1120862500@T2` | -0.00003 |
| `explicit.stat_828533480@T2` | -0.00003 |

### weapon.warstaff — n=4234, R²=-0.4957

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00001`  ·  n_top_tier: `-0.00002`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | -3.71000 |
| `desecrated.stat_2231156303@T1` | -3.71000 |
| `rune.stat_243313994` | 3.21593 |
| `rune.stat_731403740` | 1.55437 |
| `rune.stat_1712188793` | -1.04360 |
| `desecrated.stat_9187492` | 0.70329 |
| `crafted.stat_210067635@T2` | 0.37582 |
| `desecrated.stat_2527686725` | 0.25098 |
| `explicit.stat_9187492@T1` | 0.15735 |
| `rune.stat_3336890334` | 0.14026 |
| `desecrated.stat_55876295` | -0.07133 |
| `rune.stat_1509134228` | 0.06449 |

### weapon.staff — n=3956, R²=-0.5378

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00003`  ·  n_sockets: `0.00001`  ·  quality: `0.00008`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.64416 |
| `explicit.stat_2254480358@T1` | 0.32708 |
| `crafted.stat_124131830` | 0.32188 |
| `rune.stat_3990135792` | -0.19595 |
| `explicit.stat_1600707273@T1` | 0.13371 |
| `rune.stat_975988108` | -0.12316 |
| `rune.stat_2974417149` | 0.10518 |
| `explicit.stat_4226189338@T1` | 0.05829 |
| `desecrated.stat_2974417149` | 0.01816 |
| `explicit.stat_473429811@T1` | 0.01114 |
| `explicit.stat_2254480358@T2` | 0.00347 |
| `explicit.stat_3962278098@T2` | 0.00094 |

### weapon.sceptre — n=3953, R²=-0.51

intercept: `-0.0009`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.17319`  ·  corrupted: `1.35305`  ·  n_sockets: `0.00001`  ·  quality: `0.05470`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.12932 |
| `explicit.stat_2347036682@T2` | -0.17321 |
| `explicit.stat_4080418644@T2` | -0.17321 |
| `explicit.stat_3984865854@T2` | -0.17321 |
| `explicit.stat_4080418644@T1` | -0.17321 |
| `explicit.stat_2347036682@T1` | -0.17320 |
| `explicit.stat_1250712710@T1` | -0.17320 |
| `explicit.stat_1574590649@T1` | -0.17320 |
| `explicit.stat_328541901@T1` | -0.17320 |
| `explicit.stat_3639275092@T2` | -0.17319 |
| `explicit.stat_1574590649@T2` | -0.17319 |
| `explicit.stat_2854751904@T1` | -0.17319 |

### weapon.spear — n=3425, R²=-0.5339

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00010`  ·  corrupted: `-0.00004`  ·  n_sockets: `0.00001`  ·  quality: `0.00003`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.50279 |
| `explicit.stat_210067635@T1` | 1.09727 |
| `rune.stat_1039491398` | 0.19874 |
| `rune.stat_1509134228` | -0.12925 |
| `explicit.stat_1202301673@T1` | 0.12197 |
| `crafted.stat_210067635` | 0.00963 |
| `explicit.stat_1509134228@T1` | 0.00532 |
| `explicit.stat_3336890334@T1` | 0.00033 |
| `explicit.stat_709508406@T1` | 0.00024 |
| `explicit.stat_210067635@T2` | 0.00014 |
| `explicit.stat_3639275092@T1` | 0.00014 |
| `explicit.stat_3336890334@T2` | 0.00013 |

### armour.focus — n=2805, R²=-0.5648

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.11434`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00002`  ·  quality: `0.00966`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -6.65809 |
| `crafted.stat_737908626@T2` | -4.67119 |
| `crafted.stat_2974417149@T1` | -3.21736 |
| `desecrated.stat_3393628375` | 0.47960 |
| `crafted.stat_737908626` | 0.15963 |
| `explicit.stat_2923486259` | -0.13752 |
| `pseudo.total_chaos_res` | 0.13752 |
| `explicit.stat_2891184298@T2` | -0.11437 |
| `explicit.stat_736967255@T2` | -0.11436 |
| `explicit.stat_2923486259@T1` | -0.11436 |
| `explicit.stat_3291658075@T1` | -0.11436 |
| `explicit.stat_4052037485@T2` | -0.11436 |

### armour.quiver — n=2629, R²=-0.5873

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.11889`  ·  corrupted: `0.00002`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.67219 |
| `explicit.stat_3759663284@T1` | 0.57411 |
| `explicit.stat_681332047@T2` | -0.11895 |
| `explicit.stat_681332047@T1` | -0.11894 |
| `explicit.stat_1368271171@T2` | -0.11891 |
| `explicit.stat_1573130764@T1` | -0.11891 |
| `explicit.stat_2321178454@T2` | -0.11891 |
| `explicit.stat_2194114101@T2` | -0.11890 |
| `explicit.stat_3714003708@T2` | -0.11890 |
| `explicit.stat_803737631@T2` | -0.11890 |
| `explicit.stat_1573130764@T2` | -0.11890 |
| `explicit.stat_2194114101@T1` | -0.11890 |

### armour.shield — n=2276, R²=-0.437

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.28827`  ·  corrupted: `0.00231`  ·  n_sockets: `0.00000`  ·  quality: `0.05478`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.77701 |
| `explicit.stat_1978899297@T2` | -0.44875 |
| `explicit.stat_1011760251@T1` | -0.29700 |
| `explicit.stat_1011760251@T2` | -0.29408 |
| `explicit.stat_2481353198@T1` | -0.28831 |
| `explicit.stat_328541901@T1` | -0.28831 |
| `explicit.stat_2481353198@T2` | -0.28830 |
| `explicit.stat_2339757871@T1` | -0.28830 |
| `explicit.stat_328541901@T2` | -0.28829 |
| `explicit.stat_1062208444@T2` | -0.28829 |
| `explicit.stat_3372524247@T2` | -0.28829 |
| `explicit.stat_3639275092@T1` | -0.28828 |

### weapon.twomace — n=1976, R²=-0.4721

intercept: `-0.0007`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.15804`  ·  corrupted: `-0.00003`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_669069897` | -3.24089 |
| `rune.stat_1586906534` | 2.29309 |
| `explicit.stat_1509134228@T1` | 2.03318 |
| `desecrated.stat_210067635@T1` | 0.84943 |
| `rune.stat_709508406` | 0.66768 |
| `rune.stat_1857162058` | -0.28613 |
| `desecrated.stat_1509134228@T1` | -0.24091 |
| `explicit.stat_3336890334@T1` | -0.15814 |
| `explicit.stat_1037193709@T1` | -0.15809 |
| `explicit.stat_1037193709@T2` | -0.15807 |
| `explicit.stat_3336890334@T2` | -0.15807 |
| `explicit.stat_387439868@T2` | -0.15807 |

## Coverage (listings per base)

- … **Emerald** — 12105 listings (12097 priced) [0.6–7553463.8 ex]
- … **Sapphire** — 12065 listings (12049 priced) [0.3–7553463.8 ex]
- … **Ruby** — 9333 listings (9323 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 5792 listings (5788 priced) [0.2–5288620.9 ex]
- … **Prismatic Ring** — 4357 listings (4355 priced) [0.3–24532814.5 ex]
- … **Stellar Amulet** — 4340 listings (4340 priced) [0.2–35690283.3 ex]
- … **Solar Amulet** — 4282 listings (4276 priced) [0.3–66666666.0 ex]
- … **Amethyst Ring** — 4120 listings (4119 priced) [0.3–71450.3 ex]
- … **Gold Amulet** — 4094 listings (4094 priced) [0.2–292542.5 ex]
- … **Gold Ring** — 3961 listings (3960 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 3800 listings (3795 priced) [0.3–3736768402.2 ex]
- … **Sapphire Ring** — 3302 listings (3298 priced) [0.3–24532814.5 ex]
- … **Topaz Ring** — 3214 listings (3213 priced) [0.3–123132003.2 ex]
- … **Ruby Ring** — 3186 listings (3186 priced) [0.3–37474957.5 ex]
- … **Plate Belt** — 2958 listings (2956 priced) [0.3–5286174.1 ex]
- … **Obliterator Bow** — 2870 listings (2863 priced) [0.5–22139622146.9 ex]
- … **Lapis Amulet** — 2854 listings (2854 priced) [0.3–5286174.1 ex]
- … **Ancestral Tiara** — 2850 listings (2848 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 2820 listings (2819 priced) [0.2–124352753.2 ex]
- … **Jade Amulet** — 2803 listings (2802 priced) [0.2–4547453.5 ex]
- … **Heavy Belt** — 2779 listings (2779 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 2675 listings (2675 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 2632 listings (2632 priced) [0.3–14638.0 ex]
- … **Pearl Ring** — 2557 listings (2557 priced) [0.3–24532814.5 ex]
- … **Azure Amulet** — 2494 listings (2494 priced) [0.2–123132003.2 ex]

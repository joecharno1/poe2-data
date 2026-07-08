# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-08T18:17:28+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **337889** (337408 priced in exalted)
- Distinct bases: 958 · distinct mods: 2860 · mod rows: 1604382
- Sold signals: **29934** sold · 180221 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-08T18:00:38+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×16.79** (median |log error| 2.8205)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 75% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×40.48 · ±30% 14% · n=49080
- Premium segment (60ex+): skill **+0.08** · typical error ×140.12 · ±30% 1% · n=30503

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 6465 | ×11.58 | 4% | +0.04 | +0.06 |
| accessory.amulet | 6053 | ×50.90 | 21% | +0.03 | +0.03 |
| jewel | 5780 | ×8.36 | 7% | +0.01 | +0.04 |
| accessory.belt | 4899 | ×7.91 | 25% | +0.02 | +0.03 |
| armour.chest | 4781 | ×10.00 | 24% | +0.01 | +0.01 |
| armour.helmet | 4718 | ×10.00 | 22% | +0.01 | +0.02 |
| armour.boots | 4421 | ×14.34 | 20% | +0.01 | +0.03 |
| armour.gloves | 4285 | ×17.88 | 20% | +0.00 | +0.02 |
| other | 4066 | ×10.00 | 35% | +0.14 | +0.40 |
| weapon.wand | 2929 | ×45.24 | 21% | +0.05 | +0.06 |
| weapon.bow | 2336 | ×19.66 | 20% | +0.09 | +0.09 |
| weapon.crossbow | 2161 | ×14.96 | 20% | +0.10 | +0.12 |
| weapon.warstaff | 1072 | ×72.28 | 17% | +0.04 | +0.05 |
| weapon.staff | 1023 | ×50.00 | 19% | +0.04 | +0.08 |
| weapon.sceptre | 990 | ×49.00 | 14% | +0.07 | +0.08 |
| weapon.spear | 858 | ×39.00 | 18% | +0.04 | +0.03 |
| armour.focus | 719 | ×99.99 | 13% | +0.03 | +0.11 |
| armour.quiver | 682 | ×74.93 | 13% | +0.02 | +0.07 |
| flask.charm | 569 | ×77.76 | 28% | +0.00 | +0.02 |
| armour.shield | 559 | ×20.00 | 17% | +0.03 | +0.05 |
| weapon.twomace | 489 | ×20.00 | 14% | +0.04 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=34569, R²=-0.3799

intercept: `1.5955`  ·  log_price: True  ·  ilvl: `0.00019`  ·  n_mods: `0.11215`  ·  n_top_tier: `1.20495`  ·  corrupted: `2.11902`  ·  n_sockets: `-0.00059`  ·  quality: `-0.00006`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 2.77514 |
| `explicit.stat_1050105434@T1` | -2.70196 |
| `explicit.stat_2482852589@T1` | 2.66868 |
| `explicit.stat_1589917703@T1` | 2.26184 |
| `explicit.stat_101878827@T1` | 2.19876 |
| `explicit.stat_3141070085@T1` | 2.14263 |
| `explicit.stat_2106365538@T1` | 2.09172 |
| `explicit.stat_3917489142@T1` | 2.03504 |
| `explicit.stat_789117908@T1` | -1.85256 |
| `explicit.stat_2974417149@T1` | 1.51528 |
| `explicit.stat_2891184298@T1` | 1.43769 |
| `implicit.stat_3182714256` | 0.33754 |

### jewel — n=30936, R²=-0.6442

intercept: `-1.1181`  ·  log_price: True  ·  ilvl: `0.03553`  ·  n_mods: `0.23456`  ·  n_top_tier: `-0.09010`  ·  corrupted: `0.34974`  ·  quality: `0.21410`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.72551 |
| `explicit.stat_3741323227@T1` | -3.55713 |
| `explicit.stat_1569101201@T1` | 3.31560 |
| `explicit.stat_1569159338@T1` | -3.28798 |
| `explicit.stat_3780644166@T1` | -2.40361 |
| `explicit.stat_234296660@T1` | -2.20830 |
| `explicit.stat_3714003708@T1` | -1.86284 |
| `explicit.stat_2527686725@T1` | 1.61757 |
| `explicit.stat_1316278494@T1` | -1.60753 |
| `explicit.stat_1697951953@T1` | -1.52793 |
| `explicit.stat_21071013@T1` | -1.41580 |
| `explicit.stat_3374165039@T1` | -1.41189 |

### accessory.ring — n=29614, R²=-1.2073

intercept: `3.8088`  ·  log_price: True  ·  ilvl: `-0.03896`  ·  n_mods: `-0.02569`  ·  n_top_tier: `0.11145`  ·  corrupted: `0.94512`  ·  n_sockets: `0.87358`  ·  quality: `0.04617`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 5.42472 |
| `explicit.stat_707457662@T2` | 4.86253 |
| `explicit.stat_1379411836@T1` | -2.24789 |
| `explicit.stat_1379411836@T2` | -1.73350 |
| `explicit.stat_1368271171@T1` | -1.07301 |
| `explicit.stat_1573130764@T1` | -1.00492 |
| `explicit.stat_2923486259@T1` | 0.95605 |
| `explicit.stat_1368271171@T2` | -0.91332 |
| `explicit.stat_2923486259@T2` | 0.85059 |
| `explicit.stat_707457662` | -0.83565 |
| `explicit.stat_1671376347@T1` | 0.70203 |
| `explicit.stat_1263695895@T1` | -0.63719 |

### accessory.amulet — n=27904, R²=-2.0453

intercept: `4.1288`  ·  log_price: True  ·  ilvl: `-0.04988`  ·  n_mods: `-0.02521`  ·  n_top_tier: `1.02056`  ·  corrupted: `0.13135`  ·  n_sockets: `1.85277`  ·  quality: `-0.00209`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.62091 |
| `explicit.stat_983749596@T2` | -1.43397 |
| `explicit.stat_3299347043@T1` | -1.23108 |
| `explicit.stat_587431675@T1` | -1.12243 |
| `explicit.stat_3299347043@T2` | -1.11641 |
| `explicit.stat_2748665614@T1` | -1.10215 |
| `explicit.stat_2748665614@T2` | -1.09451 |
| `explicit.stat_472520716@T2` | -1.09405 |
| `explicit.stat_3917489142@T2` | -1.09016 |
| `explicit.stat_3917489142@T1` | -1.09002 |
| `explicit.stat_472520716@T1` | -1.08430 |
| `explicit.stat_3325883026@T1` | -1.06737 |

### accessory.belt — n=22427, R²=-0.1286

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.12981`  ·  corrupted: `0.00003`  ·  n_sockets: `-0.69310`

| stat_id | coef |
|---|---|
| `explicit.stat_2639966148` | 0.14829 |
| `explicit.stat_1570770415@T1` | -0.12982 |
| `explicit.stat_1389754388@T1` | -0.12982 |
| `explicit.stat_2923486259@T2` | -0.12982 |
| `explicit.stat_51994685@T1` | -0.12981 |
| `explicit.stat_644456512@T1` | -0.12981 |
| `explicit.stat_1836676211@T2` | -0.12981 |
| `explicit.stat_3585532255@T2` | -0.12981 |
| `explicit.stat_1570770415@T2` | -0.12981 |
| `explicit.stat_1671376347@T2` | -0.12981 |
| `explicit.stat_1389754388@T2` | -0.12981 |
| `explicit.stat_3299347043@T2` | -0.12981 |

### armour.chest — n=22228, R²=-0.2393

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.09984`  ·  corrupted: `0.00008`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_915769802@T2` | -0.09987 |
| `explicit.stat_915769802@T1` | -0.09987 |
| `explicit.stat_4080418644@T2` | -0.09986 |
| `explicit.stat_3261801346@T1` | -0.09985 |
| `explicit.stat_3484657501@T1` | -0.09985 |
| `explicit.stat_3261801346@T2` | -0.09985 |
| `explicit.stat_3325883026@T2` | -0.09985 |
| `explicit.stat_2451402625@T2` | -0.09985 |
| `explicit.stat_3484657501@T2` | -0.09984 |
| `explicit.stat_124859000@T2` | -0.09984 |
| `explicit.stat_2923486259@T2` | -0.09984 |
| `explicit.stat_986397080@T2` | -0.09984 |

### armour.helmet — n=21774, R²=-0.2701

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.25381`  ·  corrupted: `1.59408`  ·  n_sockets: `0.00001`  ·  quality: `0.00002`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 0.75339 |
| `explicit.stat_3362812763@T2` | -0.25385 |
| `explicit.stat_2451402625@T1` | -0.25384 |
| `explicit.stat_53045048@T2` | -0.25383 |
| `explicit.stat_803737631@T2` | -0.25383 |
| `explicit.stat_1263695895@T1` | -0.25382 |
| `explicit.stat_4080418644@T2` | -0.25382 |
| `explicit.stat_3362812763@T1` | -0.25382 |
| `explicit.stat_1263695895@T2` | -0.25381 |
| `explicit.stat_53045048@T1` | -0.25381 |
| `explicit.stat_1062208444@T2` | -0.25381 |
| `explicit.stat_3261801346@T2` | -0.25381 |

### armour.boots — n=20556, R²=-0.2626

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00004`  ·  n_top_tier: `0.31134`  ·  corrupted: `0.17671`  ·  n_sockets: `-0.00000`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `desecrated.stat_2250533757@T2` | -0.31147 |
| `explicit.stat_1999113824@T1` | -0.31139 |
| `explicit.stat_3261801346@T2` | -0.31138 |
| `explicit.stat_2451402625@T2` | -0.31137 |
| `explicit.stat_3484657501@T2` | -0.31136 |
| `explicit.stat_2923486259@T2` | -0.31136 |
| `explicit.stat_1062208444@T1` | -0.31136 |
| `explicit.stat_1062208444@T2` | -0.31136 |
| `explicit.stat_328541901@T1` | -0.31135 |
| `explicit.stat_1671376347@T2` | -0.31135 |
| `explicit.stat_3639275092@T2` | -0.31135 |
| `explicit.stat_3033371881@T2` | -0.31135 |

### armour.gloves — n=20014, R²=-0.3526

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00001`  ·  n_mods: `-0.00005`  ·  n_top_tier: `0.02188`  ·  corrupted: `0.02432`  ·  n_sockets: `0.00004`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.11093 |
| `desecrated.stat_4067062424` | 0.09119 |
| `pseudo.total_ele_res>=80` | 0.03245 |
| `explicit.stat_9187492@T2` | -0.02837 |
| `explicit.stat_3484657501@T2` | -0.02200 |
| `explicit.stat_803737631@T2` | -0.02196 |
| `explicit.stat_3362812763@T2` | -0.02195 |
| `explicit.stat_2797971005@T2` | -0.02194 |
| `explicit.stat_4080418644@T1` | -0.02193 |
| `explicit.stat_328541901@T1` | -0.02192 |
| `explicit.stat_4220027924@T2` | -0.02192 |
| `explicit.stat_4052037485@T1` | -0.02192 |

### weapon.wand — n=13595, R²=-2.1221

intercept: `3.5161`  ·  log_price: True  ·  ilvl: `-0.04391`  ·  n_mods: `-0.00919`  ·  n_top_tier: `0.25845`  ·  corrupted: `-0.00846`  ·  n_sockets: `0.02585`  ·  quality: `0.01834`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.83831 |
| `explicit.stat_591105508@T1` | 2.12448 |
| `explicit.stat_4226189338@T1` | 2.10297 |
| `explicit.stat_1545858329@T1` | 2.10000 |
| `explicit.stat_124131830@T1` | 1.94991 |
| `explicit.stat_1600707273@T1` | 1.86029 |
| `explicit.stat_736967255@T2` | 1.84841 |
| `crafted.stat_124131830` | 0.85023 |
| `explicit.stat_1600707273@T2` | 0.42062 |
| `explicit.stat_2974417149@T1` | 0.36672 |
| `explicit.stat_3015669065@T1` | -0.28771 |
| `explicit.stat_1368271171@T2` | -0.28078 |

### weapon.bow — n=11074, R²=-1.9508

intercept: `3.3951`  ·  log_price: True  ·  ilvl: `-0.04205`  ·  n_mods: `-0.01092`  ·  n_top_tier: `0.66043`  ·  corrupted: `0.12523`  ·  n_sockets: `0.00178`  ·  quality: `0.00906`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.06511 |
| `explicit.stat_2463230181@T1` | 1.65080 |
| `crafted.stat_3035140377` | 1.55297 |
| `explicit.stat_1202301673@T1` | 1.46077 |
| `rune.stat_3885405204` | -1.27160 |
| `explicit.stat_518292764@T1` | 0.86120 |
| `explicit.stat_55876295@T1` | -0.72187 |
| `explicit.stat_2694482655@T1` | -0.70252 |
| `explicit.stat_3695891184@T2` | -0.69864 |
| `explicit.stat_3336890334@T2` | -0.69657 |
| `explicit.stat_1037193709@T1` | -0.68949 |
| `explicit.stat_3261801346@T1` | -0.68796 |

### weapon.crossbow — n=10368, R²=-1.8172

intercept: `3.5620`  ·  log_price: True  ·  ilvl: `-0.04408`  ·  n_mods: `-0.00859`  ·  n_top_tier: `0.64836`  ·  corrupted: `-0.02104`  ·  n_sockets: `0.01534`  ·  quality: `0.00159`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -2.75506 |
| `explicit.stat_1980802737` | 2.05213 |
| `explicit.stat_709508406@T1` | 1.56526 |
| `explicit.stat_2250681686@T2` | -1.46764 |
| `explicit.stat_1202301673@T1` | 1.35669 |
| `explicit.stat_1509134228@T1` | 0.94632 |
| `explicit.stat_1202301673@T2` | -0.88453 |
| `explicit.stat_2250681686` | 0.83522 |
| `crafted.stat_3035140377` | 0.81845 |
| `explicit.stat_1037193709@T1` | 0.77154 |
| `explicit.stat_1509134228@T2` | -0.75968 |
| `rune.stat_669069897` | -0.69879 |

### flask.charm — n=7497, R²=-0.3996

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.55945`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60516 |
| `explicit.stat_1056492907` | 2.99571 |
| `explicit.stat_2676834156@T1` | 1.60935 |
| `explicit.stat_2541588185@T1` | 0.54017 |
| `explicit.stat_3138344128` | 0.02023 |
| `explicit.stat_2678930256` | 0.02020 |
| `explicit.stat_3246948616` | 0.00005 |
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_1120862500@T2` | -0.00004 |
| `explicit.stat_1873752457@T2` | -0.00003 |
| `explicit.stat_828533480@T2` | -0.00003 |
| `explicit.stat_1873752457@T1` | -0.00003 |

### weapon.warstaff — n=5324, R²=-0.5548

intercept: `-0.0008`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.05896`  ·  corrupted: `0.63427`  ·  n_sockets: `0.00001`  ·  quality: `0.01528`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.86483 |
| `rune.stat_731403740` | 1.51165 |
| `explicit.stat_9187492@T1` | 1.07148 |
| `rune.stat_1712188793` | -0.62795 |
| `desecrated.stat_9187492` | 0.58862 |
| `crafted.stat_210067635@T2` | -0.49697 |
| `desecrated.stat_518292764` | 0.38480 |
| `crafted.stat_3035140377` | 0.37669 |
| `rune.stat_1037193709` | 0.20327 |
| `desecrated.stat_669069897` | -0.13929 |
| `rune.stat_1509134228` | 0.09624 |
| `desecrated.stat_55876295` | -0.08284 |

### weapon.staff — n=4932, R²=-0.6238

intercept: `-0.0011`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00048`  ·  corrupted: `0.05270`  ·  n_sockets: `0.00004`  ·  quality: `0.00003`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 6.95524 |
| `explicit.stat_2254480358@T1` | 1.60885 |
| `explicit.stat_4226189338@T1` | 1.54408 |
| `explicit.stat_2254480358@T2` | 1.30720 |
| `explicit.stat_124131830@T1` | 1.13818 |
| `explicit.stat_3962278098@T2` | 1.11663 |
| `explicit.stat_2768835289@T2` | 1.03927 |
| `explicit.stat_473429811@T1` | 0.69266 |
| `explicit.stat_1600707273@T1` | 0.69254 |
| `explicit.stat_3291658075@T2` | 0.49364 |
| `crafted.stat_124131830` | 0.41447 |
| `rune.stat_3909696841` | 0.30932 |

### weapon.sceptre — n=4892, R²=-0.6139

intercept: `-0.1246`  ·  log_price: True  ·  ilvl: `0.00155`  ·  n_mods: `-0.00065`  ·  n_top_tier: `0.54351`  ·  corrupted: `1.07928`  ·  n_sockets: `0.00253`  ·  quality: `0.07959`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.75575 |
| `explicit.stat_3984865854@T1` | 0.69516 |
| `explicit.stat_4080418644@T1` | -0.54862 |
| `explicit.stat_4080418644@T2` | -0.54668 |
| `explicit.stat_2347036682@T2` | -0.54606 |
| `explicit.stat_1263695895@T2` | -0.54528 |
| `explicit.stat_1250712710@T1` | -0.54490 |
| `explicit.stat_3639275092@T2` | -0.54423 |
| `explicit.stat_328541901@T1` | -0.54410 |
| `explicit.stat_1574590649@T1` | -0.54380 |
| `explicit.stat_2854751904@T1` | -0.54378 |
| `explicit.stat_789117908@T1` | -0.54327 |

### weapon.spear — n=4184, R²=-0.5696

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.01784`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00002`  ·  quality: `0.04013`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 3.40716 |
| `explicit.stat_1202301673@T1` | 2.34022 |
| `crafted.stat_3035140377` | 1.30350 |
| `explicit.stat_210067635@T1` | 0.87547 |
| `explicit.stat_3336890334@T1` | 0.70208 |
| `crafted.stat_518292764` | 0.63754 |
| `explicit.stat_1509134228@T1` | 0.62786 |
| `explicit.stat_709508406@T1` | 0.21128 |
| `explicit.stat_9187492@T1` | 0.11926 |
| `rune.stat_1039491398` | 0.10220 |
| `desecrated.stat_210067635` | -0.04823 |
| `rune.stat_1509134228` | 0.04679 |

### armour.focus — n=3403, R²=-0.6413

intercept: `-0.2828`  ·  log_price: True  ·  ilvl: `0.00349`  ·  n_mods: `-0.00061`  ·  n_top_tier: `1.03884`  ·  corrupted: `0.00030`  ·  n_sockets: `0.00902`  ·  quality: `0.05354`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -1.27942 |
| `explicit.stat_789117908@T2` | -1.04998 |
| `explicit.stat_2891184298@T2` | -1.04725 |
| `explicit.stat_3291658075@T1` | -1.04658 |
| `explicit.stat_4052037485@T2` | -1.04446 |
| `explicit.stat_4220027924@T2` | -1.04419 |
| `explicit.stat_736967255@T2` | -1.04373 |
| `explicit.stat_2231156303@T2` | -1.04368 |
| `explicit.stat_2923486259@T1` | -1.04336 |
| `explicit.stat_2974417149@T1` | -1.04203 |
| `explicit.stat_4015621042@T2` | -1.04185 |
| `explicit.stat_789117908@T1` | -1.04158 |

### armour.quiver — n=3198, R²=-0.6477

intercept: `-0.0886`  ·  log_price: True  ·  ilvl: `0.00105`  ·  n_mods: `0.00022`  ·  n_top_tier: `0.80364`  ·  corrupted: `0.07399`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 12.41338 |
| `desecrated.stat_3932115504` | -0.89217 |
| `explicit.stat_2463230181@T2` | -0.83359 |
| `explicit.stat_681332047@T2` | -0.81000 |
| `explicit.stat_681332047@T1` | -0.80930 |
| `explicit.stat_1573130764@T1` | -0.80807 |
| `explicit.stat_2194114101@T2` | -0.80674 |
| `explicit.stat_1368271171@T2` | -0.80603 |
| `explicit.stat_3714003708@T2` | -0.80573 |
| `explicit.stat_1573130764@T2` | -0.80552 |
| `explicit.stat_2321178454@T2` | -0.80522 |
| `explicit.stat_3261801346@T1` | -0.80383 |

### armour.shield — n=2759, R²=-0.5676

intercept: `-0.0038`  ·  log_price: True  ·  ilvl: `0.00005`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.29884`  ·  corrupted: `0.00241`  ·  n_sockets: `0.00003`  ·  quality: `0.06844`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.92100 |
| `explicit.stat_4220027924@T1` | 0.57868 |
| `explicit.stat_1978899297@T2` | -0.49293 |
| `explicit.stat_1011760251@T2` | -0.30097 |
| `explicit.stat_1011760251@T1` | -0.30073 |
| `explicit.stat_328541901@T1` | -0.29926 |
| `explicit.stat_328541901@T2` | -0.29921 |
| `explicit.stat_2339757871@T1` | -0.29915 |
| `explicit.stat_3484657501@T1` | -0.29909 |
| `explicit.stat_3484657501@T2` | -0.29901 |
| `explicit.stat_2481353198@T1` | -0.29899 |
| `explicit.stat_1671376347@T1` | -0.29897 |

### weapon.twomace — n=2440, R²=-0.565

intercept: `-0.0076`  ·  log_price: True  ·  ilvl: `0.00010`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.68709`  ·  corrupted: `0.01242`  ·  n_sockets: `0.00016`  ·  quality: `0.00085`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.58506 |
| `crafted.stat_3035140377` | 1.24770 |
| `explicit.stat_3336890334@T1` | -0.68769 |
| `explicit.stat_1037193709@T1` | -0.68767 |
| `explicit.stat_387439868@T2` | -0.68752 |
| `explicit.stat_821021828@T2` | -0.68735 |
| `explicit.stat_1263695895@T2` | -0.68734 |
| `explicit.stat_1263695895@T1` | -0.68726 |
| `explicit.stat_821021828@T1` | -0.68726 |
| `explicit.stat_669069897@T1` | -0.68722 |
| `explicit.stat_691932474@T1` | -0.68721 |
| `explicit.stat_1037193709@T2` | -0.68721 |

## Coverage (listings per base)

- … **Sapphire** — 14698 listings (14677 priced) [0.3–7553463.8 ex]
- … **Emerald** — 14566 listings (14553 priced) [0.4–7553463.8 ex]
- … **Ruby** — 11179 listings (11167 priced) [0.2–308559482.1 ex]
- … **Utility Belt** — 6597 listings (6592 priced) [0.3–5288620.9 ex]
- … **Prismatic Ring** — 5149 listings (5144 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 5018 listings (5010 priced) [1.0–66666666.0 ex]
- … **Stellar Amulet** — 4965 listings (4963 priced) [0.2–35690283.3 ex]
- … **Amethyst Ring** — 4928 listings (4927 priced) [0.3–4323655.9 ex]
- … **Gold Amulet** — 4771 listings (4765 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 4626 listings (4624 priced) [0.3–24532814.5 ex]
- … **Dueling Wand** — 4269 listings (4264 priced) [0.3–3956304924.1 ex]
- … **Sapphire Ring** — 3874 listings (3869 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 3758 listings (3757 priced) [0.3–37474957.5 ex]
- … **Topaz Ring** — 3736 listings (3733 priced) [1.0–307202867.9 ex]
- … **Plate Belt** — 3391 listings (3386 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 3360 listings (3358 priced) [0.3–5286174.1 ex]
- … **Ancestral Tiara** — 3344 listings (3340 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3307 listings (3306 priced) [0.3–124352753.2 ex]
- … **Obliterator Bow** — 3280 listings (3271 priced) [0.4–22139622146.9 ex]
- … **Jade Amulet** — 3273 listings (3272 priced) [0.3–4547453.5 ex]
- … **Heavy Belt** — 3187 listings (3187 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 3139 listings (3139 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 3083 listings (3083 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 3009 listings (3007 priced) [0.3–24532814.5 ex]
- … **Azure Amulet** — 2932 listings (2932 priced) [0.3–123132003.2 ex]

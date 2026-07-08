# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-08T16:26:53+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **334554** (334100 priced in exalted)
- Distinct bases: 958 · distinct mods: 2857 · mod rows: 1588077
- Sold signals: **30043** sold · 179088 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-08T16:13:13+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×16.28** (median |log error| 2.7899)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 75% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×39.15 · ±30% 14% · n=48481
- Premium segment (60ex+): skill **+0.08** · typical error ×137.81 · ±30% 1% · n=30250

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 6386 | ×11.15 | 4% | +0.03 | +0.05 |
| accessory.amulet | 6070 | ×49.97 | 20% | +0.03 | +0.03 |
| jewel | 5689 | ×8.54 | 7% | +0.02 | +0.05 |
| accessory.belt | 4835 | ×9.86 | 23% | +0.02 | +0.03 |
| armour.chest | 4735 | ×10.00 | 24% | +0.01 | +0.01 |
| armour.helmet | 4657 | ×10.27 | 22% | +0.01 | +0.02 |
| armour.boots | 4321 | ×11.32 | 20% | +0.01 | +0.02 |
| armour.gloves | 4294 | ×15.68 | 20% | +0.00 | +0.02 |
| other | 4004 | ×9.83 | 35% | +0.15 | +0.40 |
| weapon.wand | 2862 | ×40.30 | 21% | +0.06 | +0.06 |
| weapon.bow | 2344 | ×19.55 | 21% | +0.09 | +0.08 |
| weapon.crossbow | 2174 | ×14.51 | 20% | +0.09 | +0.11 |
| weapon.warstaff | 1073 | ×52.00 | 18% | +0.04 | +0.04 |
| weapon.sceptre | 1018 | ×42.85 | 14% | +0.08 | +0.08 |
| weapon.staff | 938 | ×50.00 | 19% | +0.04 | +0.08 |
| weapon.spear | 800 | ×40.00 | 17% | +0.04 | +0.03 |
| armour.focus | 694 | ×88.26 | 13% | +0.03 | +0.10 |
| armour.quiver | 673 | ×60.56 | 13% | +0.01 | +0.07 |
| flask.charm | 579 | ×77.76 | 28% | +0.00 | +0.01 |
| armour.shield | 540 | ×18.67 | 19% | +0.03 | +0.05 |
| weapon.twomace | 489 | ×20.00 | 14% | +0.04 | +0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=34318, R²=-0.3859

intercept: `1.5883`  ·  log_price: True  ·  ilvl: `0.00031`  ·  n_mods: `0.12327`  ·  n_top_tier: `1.20808`  ·  corrupted: `2.14706`  ·  n_sockets: `-0.00144`  ·  quality: `-0.00016`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 2.76539 |
| `explicit.stat_1050105434@T1` | -2.70735 |
| `explicit.stat_2482852589@T1` | 2.57446 |
| `explicit.stat_1589917703@T1` | 2.25313 |
| `explicit.stat_101878827@T1` | 2.18294 |
| `explicit.stat_3917489142@T1` | 2.10937 |
| `explicit.stat_3141070085@T1` | 2.09920 |
| `explicit.stat_2106365538@T1` | 2.03842 |
| `explicit.stat_2891184298@T1` | 1.93016 |
| `explicit.stat_789117908@T1` | -1.82657 |
| `explicit.stat_2974417149@T1` | 1.54938 |
| `implicit.stat_3182714256` | 0.37284 |

### jewel — n=30576, R²=-0.6334

intercept: `-1.1295`  ·  log_price: True  ·  ilvl: `0.03627`  ·  n_mods: `0.22601`  ·  n_top_tier: `-0.09349`  ·  corrupted: `0.28554`  ·  quality: `0.21535`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -4.00851 |
| `explicit.stat_3741323227@T1` | -3.55210 |
| `explicit.stat_1569101201@T1` | 3.20755 |
| `explicit.stat_1569159338@T1` | -2.87638 |
| `explicit.stat_234296660@T1` | -2.48549 |
| `explicit.stat_3780644166@T1` | -2.25275 |
| `explicit.stat_3473929743@T1` | -2.08982 |
| `explicit.stat_1316278494@T1` | -1.97057 |
| `explicit.stat_2527686725@T1` | 1.96113 |
| `explicit.stat_3374165039@T1` | -1.62481 |
| `explicit.stat_1062710370@T1` | -1.48634 |
| `explicit.stat_1697951953@T1` | -1.43180 |

### accessory.ring — n=29310, R²=-1.2021

intercept: `3.8589`  ·  log_price: True  ·  ilvl: `-0.03897`  ·  n_mods: `-0.02695`  ·  n_top_tier: `0.11892`  ·  corrupted: `0.95863`  ·  n_sockets: `0.79626`  ·  quality: `0.04488`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.65372 |
| `explicit.stat_707457662@T2` | 4.15679 |
| `explicit.stat_1379411836@T1` | -2.28778 |
| `explicit.stat_1379411836@T2` | -1.81293 |
| `explicit.stat_1368271171@T1` | -1.02309 |
| `explicit.stat_2923486259@T1` | 1.01761 |
| `explicit.stat_1368271171@T2` | -0.94028 |
| `explicit.stat_2923486259@T2` | 0.84659 |
| `explicit.stat_1573130764@T1` | -0.75205 |
| `explicit.stat_707457662` | -0.72311 |
| `explicit.stat_1671376347@T1` | 0.67373 |
| `explicit.stat_2557965901@T1` | 0.57218 |

### accessory.amulet — n=27630, R²=-2.0618

intercept: `3.8951`  ·  log_price: True  ·  ilvl: `-0.04696`  ·  n_mods: `-0.02308`  ·  n_top_tier: `0.58274`  ·  corrupted: `0.11335`  ·  n_sockets: `1.68135`  ·  quality: `-0.00180`

| stat_id | coef |
|---|---|
| `explicit.stat_3981240776@T2` | 1.47196 |
| `explicit.stat_3981240776@T1` | 1.19992 |
| `explicit.stat_983749596@T1` | -1.18265 |
| `explicit.stat_124131830` | 1.10260 |
| `explicit.stat_983749596@T2` | -1.01057 |
| `explicit.stat_3299347043@T1` | -0.76210 |
| `explicit.stat_9187492@T2` | 0.75093 |
| `explicit.stat_2748665614@T1` | -0.67609 |
| `explicit.stat_3299347043@T2` | -0.65896 |
| `explicit.stat_2748665614@T2` | -0.65216 |
| `explicit.stat_3917489142@T2` | -0.64362 |
| `explicit.stat_472520716@T1` | -0.63952 |

### accessory.belt — n=22212, R²=-0.1298

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.25887`  ·  corrupted: `0.00003`  ·  n_sockets: `-0.69310`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -0.25889 |
| `explicit.stat_2923486259@T2` | -0.25888 |
| `explicit.stat_1570770415@T1` | -0.25888 |
| `explicit.stat_51994685@T1` | -0.25888 |
| `explicit.stat_1836676211@T2` | -0.25888 |
| `explicit.stat_644456512@T1` | -0.25888 |
| `explicit.stat_3585532255@T2` | -0.25888 |
| `explicit.stat_1671376347@T2` | -0.25888 |
| `explicit.stat_3299347043@T2` | -0.25888 |
| `explicit.stat_4220027924@T2` | -0.25888 |
| `explicit.stat_1389754388@T2` | -0.25887 |
| `explicit.stat_1570770415@T2` | -0.25887 |

### armour.chest — n=22045, R²=-0.2361

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.09760`  ·  corrupted: `0.00007`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_915769802@T2` | -0.09764 |
| `explicit.stat_915769802@T1` | -0.09763 |
| `explicit.stat_3261801346@T1` | -0.09762 |
| `explicit.stat_4080418644@T2` | -0.09762 |
| `explicit.stat_3484657501@T1` | -0.09762 |
| `explicit.stat_3261801346@T2` | -0.09762 |
| `explicit.stat_2451402625@T2` | -0.09761 |
| `explicit.stat_3325883026@T2` | -0.09761 |
| `explicit.stat_124859000@T2` | -0.09761 |
| `explicit.stat_1062208444@T1` | -0.09761 |
| `explicit.stat_2923486259@T2` | -0.09761 |
| `explicit.stat_3484657501@T2` | -0.09760 |

### armour.helmet — n=21573, R²=-0.2696

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.23038`  ·  corrupted: `1.60115`  ·  n_sockets: `0.00001`  ·  quality: `0.00002`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 0.49564 |
| `explicit.stat_3362812763@T2` | -0.23042 |
| `explicit.stat_2451402625@T1` | -0.23040 |
| `explicit.stat_53045048@T2` | -0.23039 |
| `explicit.stat_1263695895@T1` | -0.23039 |
| `explicit.stat_803737631@T2` | -0.23039 |
| `explicit.stat_4080418644@T2` | -0.23039 |
| `explicit.stat_1263695895@T2` | -0.23039 |
| `explicit.stat_3362812763@T1` | -0.23039 |
| `explicit.stat_3261801346@T2` | -0.23038 |
| `explicit.stat_3917489142@T2` | -0.23038 |
| `explicit.stat_53045048@T1` | -0.23038 |

### armour.boots — n=20373, R²=-0.2691

intercept: `2.3030`  ·  log_price: True  ·  ilvl: `-0.00001`  ·  n_mods: `-0.00006`  ·  n_top_tier: `0.26379`  ·  corrupted: `0.12120`  ·  n_sockets: `0.00000`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `desecrated.stat_2250533757@T2` | -0.26398 |
| `explicit.stat_2451402625@T2` | -0.26388 |
| `explicit.stat_1999113824@T1` | -0.26385 |
| `explicit.stat_3261801346@T2` | -0.26385 |
| `explicit.stat_1062208444@T1` | -0.26384 |
| `explicit.stat_2923486259@T2` | -0.26384 |
| `explicit.stat_3484657501@T2` | -0.26382 |
| `explicit.stat_3917489142@T2` | -0.26382 |
| `explicit.stat_1671376347@T2` | -0.26382 |
| `explicit.stat_3639275092@T2` | -0.26381 |
| `explicit.stat_1062208444@T2` | -0.26381 |
| `explicit.stat_3362812763@T1` | -0.26381 |

### armour.gloves — n=19844, R²=-0.3474

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00001`  ·  n_mods: `-0.00004`  ·  n_top_tier: `0.02826`  ·  corrupted: `0.03764`  ·  n_sockets: `0.00004`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.10373 |
| `desecrated.stat_4067062424` | 0.09126 |
| `explicit.stat_9187492@T2` | -0.04237 |
| `explicit.stat_9187492@T1` | 0.03840 |
| `pseudo.total_ele_res>=80` | 0.03655 |
| `explicit.stat_3484657501@T2` | -0.02836 |
| `explicit.stat_2797971005@T2` | -0.02834 |
| `explicit.stat_803737631@T2` | -0.02833 |
| `explicit.stat_3362812763@T2` | -0.02831 |
| `explicit.stat_328541901@T1` | -0.02831 |
| `explicit.stat_4052037485@T1` | -0.02830 |
| `explicit.stat_4080418644@T1` | -0.02830 |

### weapon.wand — n=13482, R²=-2.0946

intercept: `3.5123`  ·  log_price: True  ·  ilvl: `-0.04381`  ·  n_mods: `-0.00851`  ·  n_top_tier: `0.25304`  ·  corrupted: `-0.03958`  ·  n_sockets: `0.02653`  ·  quality: `0.02014`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.75896 |
| `explicit.stat_591105508@T1` | 2.12231 |
| `explicit.stat_1545858329@T1` | 2.10224 |
| `explicit.stat_4226189338@T1` | 2.09904 |
| `explicit.stat_124131830@T1` | 1.96640 |
| `explicit.stat_1600707273@T1` | 1.86289 |
| `explicit.stat_736967255@T2` | 1.85165 |
| `crafted.stat_124131830` | 0.84131 |
| `explicit.stat_1600707273@T2` | 0.51734 |
| `explicit.stat_2974417149@T2` | 0.38695 |
| `explicit.stat_2974417149@T1` | 0.35207 |
| `explicit.stat_3015669065@T1` | -0.28578 |

### weapon.bow — n=10991, R²=-1.9645

intercept: `3.4343`  ·  log_price: True  ·  ilvl: `-0.04260`  ·  n_mods: `-0.01012`  ·  n_top_tier: `0.57364`  ·  corrupted: `0.15732`  ·  n_sockets: `0.00057`  ·  quality: `0.00885`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.05783 |
| `explicit.stat_2463230181@T1` | 1.74400 |
| `explicit.stat_1202301673@T1` | 1.58995 |
| `crafted.stat_3035140377` | 1.58169 |
| `desecrated.stat_666077204@T1` | 1.54078 |
| `rune.stat_3885405204` | -0.94645 |
| `explicit.stat_518292764@T1` | 0.77271 |
| `explicit.stat_55876295@T1` | -0.63679 |
| `explicit.stat_3695891184@T2` | -0.62231 |
| `explicit.stat_3336890334@T2` | -0.61093 |
| `explicit.stat_2694482655@T1` | -0.61043 |
| `explicit.stat_3261801346@T1` | -0.60273 |

### weapon.crossbow — n=10291, R²=-1.8321

intercept: `3.5562`  ·  log_price: True  ·  ilvl: `-0.04405`  ·  n_mods: `-0.00828`  ·  n_top_tier: `0.60426`  ·  corrupted: `-0.03026`  ·  n_sockets: `0.01510`  ·  quality: `0.00327`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -2.72691 |
| `explicit.stat_1980802737` | 2.07984 |
| `explicit.stat_709508406@T1` | 1.60665 |
| `explicit.stat_1202301673@T1` | 1.50983 |
| `explicit.stat_2250681686@T2` | -1.44281 |
| `explicit.stat_1509134228@T1` | 1.05360 |
| `explicit.stat_2250681686` | 0.85964 |
| `crafted.stat_3035140377` | 0.84846 |
| `explicit.stat_1037193709@T1` | 0.78018 |
| `explicit.stat_1202301673@T2` | -0.76092 |
| `rune.stat_669069897` | -0.72416 |
| `explicit.stat_1509134228@T2` | -0.70059 |

### flask.charm — n=7394, R²=-0.395

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00012`  ·  corrupted: `0.53995`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.59788 |
| `explicit.stat_1056492907` | 2.99572 |
| `explicit.stat_2676834156@T1` | 1.60922 |
| `explicit.stat_2541588185@T1` | 0.54310 |
| `explicit.stat_3138344128` | 0.02053 |
| `explicit.stat_2678930256` | 0.01366 |
| `explicit.stat_3246948616` | 0.00055 |
| `explicit.stat_1120862500@T2` | -0.00013 |
| `explicit.stat_1873752457@T2` | -0.00013 |
| `explicit.stat_2676834156@T2` | -0.00012 |
| `explicit.stat_1873752457@T1` | -0.00012 |
| `explicit.stat_828533480@T1` | -0.00012 |

### weapon.warstaff — n=5237, R²=-0.5559

intercept: `-0.0008`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.00206`  ·  corrupted: `0.27376`  ·  n_sockets: `0.00001`  ·  quality: `0.01631`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.93929 |
| `rune.stat_731403740` | 1.47945 |
| `explicit.stat_9187492@T1` | 1.38417 |
| `rune.stat_1712188793` | -0.58110 |
| `desecrated.stat_9187492` | 0.56197 |
| `crafted.stat_210067635@T2` | -0.45554 |
| `crafted.stat_3035140377` | 0.34622 |
| `desecrated.stat_518292764` | 0.34173 |
| `desecrated.stat_669069897` | -0.10686 |
| `rune.stat_1509134228` | 0.09534 |
| `desecrated.stat_55876295` | -0.07764 |
| `rune.stat_3336890334` | 0.05933 |

### weapon.staff — n=4854, R²=-0.6196

intercept: `-0.0008`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00008`  ·  corrupted: `0.00733`  ·  n_sockets: `0.00002`  ·  quality: `0.00049`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.03878 |
| `explicit.stat_4226189338@T1` | 2.30250 |
| `explicit.stat_2254480358@T1` | 1.60928 |
| `explicit.stat_2254480358@T2` | 1.42667 |
| `explicit.stat_124131830@T1` | 1.22847 |
| `explicit.stat_3962278098@T2` | 0.84594 |
| `explicit.stat_473429811@T1` | 0.69300 |
| `explicit.stat_1600707273@T1` | 0.69296 |
| `explicit.stat_3291658075@T2` | 0.50387 |
| `crafted.stat_124131830` | 0.44695 |
| `rune.stat_3909696841` | 0.25185 |
| `rune.stat_975988108` | -0.15358 |

### weapon.sceptre — n=4825, R²=-0.6163

intercept: `-0.0864`  ·  log_price: True  ·  ilvl: `0.00108`  ·  n_mods: `-0.00045`  ·  n_top_tier: `0.44235`  ·  corrupted: `1.08715`  ·  n_sockets: `0.00203`  ·  quality: `0.08034`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.75550 |
| `explicit.stat_3984865854@T1` | 0.65172 |
| `explicit.stat_1798257884@T2` | 0.51531 |
| `explicit.stat_4080418644@T1` | -0.44584 |
| `explicit.stat_4080418644@T2` | -0.44518 |
| `explicit.stat_2347036682@T2` | -0.44419 |
| `explicit.stat_1263695895@T2` | -0.44413 |
| `explicit.stat_1574590649@T1` | -0.44396 |
| `explicit.stat_1250712710@T1` | -0.44363 |
| `explicit.stat_328541901@T1` | -0.44316 |
| `explicit.stat_3639275092@T2` | -0.44303 |
| `explicit.stat_3984865854@T2` | -0.44226 |

### weapon.spear — n=4131, R²=-0.5821

intercept: `-0.0006`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00221`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00002`  ·  quality: `0.01799`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 3.18559 |
| `explicit.stat_1202301673@T1` | 2.30484 |
| `crafted.stat_3035140377` | 1.53709 |
| `crafted.stat_518292764` | 0.71856 |
| `explicit.stat_210067635@T1` | 0.69795 |
| `explicit.stat_1509134228@T1` | 0.55842 |
| `explicit.stat_9187492@T1` | 0.25286 |
| `explicit.stat_3336890334@T1` | 0.19722 |
| `rune.stat_1039491398` | 0.10704 |
| `explicit.stat_709508406@T1` | 0.06760 |
| `desecrated.stat_210067635` | -0.06454 |
| `rune.stat_1509134228` | 0.05107 |

### armour.focus — n=3348, R²=-0.6343

intercept: `-0.2958`  ·  log_price: True  ·  ilvl: `0.00365`  ·  n_mods: `-0.00033`  ·  n_top_tier: `0.75627`  ·  corrupted: `0.00449`  ·  n_sockets: `0.01127`  ·  quality: `0.06099`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -3.56058 |
| `desecrated.stat_378817135@T1` | 2.70955 |
| `desecrated.stat_3393628375@T1` | -1.19875 |
| `explicit.stat_789117908@T2` | -0.76765 |
| `explicit.stat_736967255@T2` | -0.76552 |
| `explicit.stat_2891184298@T2` | -0.76470 |
| `explicit.stat_4052037485@T2` | -0.76332 |
| `explicit.stat_2231156303@T2` | -0.76159 |
| `explicit.stat_4220027924@T2` | -0.76147 |
| `explicit.stat_2923486259@T1` | -0.76038 |
| `explicit.stat_3291658075@T1` | -0.76010 |
| `explicit.stat_789117908@T1` | -0.75979 |

### armour.quiver — n=3157, R²=-0.6448

intercept: `-0.0724`  ·  log_price: True  ·  ilvl: `0.00087`  ·  n_mods: `0.00017`  ·  n_top_tier: `0.84451`  ·  corrupted: `0.03646`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.04241 |
| `explicit.stat_2463230181@T2` | -0.85602 |
| `explicit.stat_681332047@T2` | -0.85018 |
| `explicit.stat_681332047@T1` | -0.84941 |
| `explicit.stat_1573130764@T1` | -0.84826 |
| `explicit.stat_2194114101@T2` | -0.84719 |
| `explicit.stat_1368271171@T2` | -0.84675 |
| `explicit.stat_1573130764@T2` | -0.84632 |
| `explicit.stat_2321178454@T2` | -0.84628 |
| `explicit.stat_3714003708@T2` | -0.84558 |
| `explicit.stat_803737631@T2` | -0.84467 |
| `explicit.stat_3261801346@T1` | -0.84464 |

### armour.shield — n=2722, R²=-0.5499

intercept: `-0.0028`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.39251`  ·  corrupted: `0.02747`  ·  n_sockets: `0.00002`  ·  quality: `0.06867`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.87819 |
| `explicit.stat_1978899297@T2` | -0.56149 |
| `explicit.stat_4220027924@T1` | 0.47985 |
| `explicit.stat_328541901@T1` | -0.39286 |
| `explicit.stat_1011760251@T2` | -0.39278 |
| `explicit.stat_328541901@T2` | -0.39274 |
| `explicit.stat_2481353198@T1` | -0.39271 |
| `explicit.stat_2339757871@T1` | -0.39271 |
| `explicit.stat_3484657501@T1` | -0.39270 |
| `explicit.stat_2481353198@T2` | -0.39266 |
| `explicit.stat_3484657501@T2` | -0.39265 |
| `explicit.stat_3372524247@T2` | -0.39261 |

### weapon.twomace — n=2399, R²=-0.5688

intercept: `-0.0047`  ·  log_price: True  ·  ilvl: `0.00006`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.33316`  ·  corrupted: `0.00040`  ·  n_sockets: `0.00009`  ·  quality: `0.00190`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.13812 |
| `crafted.stat_3035140377` | 1.33076 |
| `desecrated.stat_1509134228@T1` | -0.60982 |
| `rune.stat_709508406` | 0.56033 |
| `explicit.stat_1037193709@T1` | -0.33375 |
| `explicit.stat_3336890334@T1` | -0.33353 |
| `explicit.stat_387439868@T2` | -0.33347 |
| `explicit.stat_1263695895@T1` | -0.33341 |
| `explicit.stat_1263695895@T2` | -0.33338 |
| `explicit.stat_821021828@T2` | -0.33338 |
| `explicit.stat_821021828@T1` | -0.33335 |
| `explicit.stat_1037193709@T2` | -0.33332 |

## Coverage (listings per base)

- … **Sapphire** — 14534 listings (14513 priced) [0.2–7553463.8 ex]
- … **Emerald** — 14424 listings (14411 priced) [0.4–7553463.8 ex]
- … **Ruby** — 11043 listings (11031 priced) [0.2–308559482.1 ex]
- … **Utility Belt** — 6542 listings (6537 priced) [0.3–5288620.9 ex]
- … **Prismatic Ring** — 5097 listings (5095 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 4962 listings (4954 priced) [1.0–66666666.0 ex]
- … **Stellar Amulet** — 4928 listings (4927 priced) [0.2–35690283.3 ex]
- … **Amethyst Ring** — 4876 listings (4875 priced) [0.3–4323655.9 ex]
- … **Gold Amulet** — 4722 listings (4716 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 4588 listings (4586 priced) [0.3–24532814.5 ex]
- … **Dueling Wand** — 4232 listings (4227 priced) [0.3–3956304924.1 ex]
- … **Sapphire Ring** — 3825 listings (3821 priced) [0.3–24532814.5 ex]
- … **Ruby Ring** — 3716 listings (3716 priced) [0.3–37474957.5 ex]
- … **Topaz Ring** — 3709 listings (3708 priced) [1.0–123132003.2 ex]
- … **Plate Belt** — 3359 listings (3356 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 3333 listings (3332 priced) [0.3–5286174.1 ex]
- … **Ancestral Tiara** — 3302 listings (3298 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3272 listings (3271 priced) [0.3–124352753.2 ex]
- … **Obliterator Bow** — 3253 listings (3245 priced) [0.3–22139622146.9 ex]
- … **Jade Amulet** — 3247 listings (3246 priced) [0.3–4547453.5 ex]
- … **Heavy Belt** — 3164 listings (3164 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 3101 listings (3101 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 3061 listings (3061 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 2982 listings (2982 priced) [0.3–24532814.5 ex]
- … **Lunar Amulet** — 2906 listings (2904 priced) [0.3–4877938.3 ex]

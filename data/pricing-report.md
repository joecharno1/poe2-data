# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-14T01:37:27+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **449828** (448941 priced in exalted)
- Distinct bases: 978 · distinct mods: 3022 · mod rows: 2137188
- Sold signals: **27136** sold · 246956 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-14T01:28:50+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×25.56** (median |log error| 3.2412)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.09** · typical error ×73.16 · ±30% 5% · n=64696
- Premium segment (60ex+): skill **+0.09** · typical error ×310.85 · ±30% 0% · n=42509

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 8881 | ×50.69 | 20% | +0.04 | +0.05 |
| accessory.amulet | 8264 | ×49.63 | 21% | +0.03 | +0.02 |
| jewel | 8105 | ×8.56 | 7% | +0.02 | +0.05 |
| accessory.belt | 6415 | ×22.55 | 4% | +0.02 | +0.04 |
| armour.chest | 6238 | ×23.31 | 15% | +0.07 | +0.09 |
| armour.helmet | 6109 | ×22.75 | 11% | +0.08 | +0.10 |
| armour.boots | 5726 | ×23.35 | 21% | +0.06 | +0.08 |
| armour.gloves | 5565 | ×33.26 | 18% | +0.05 | +0.08 |
| other | 4958 | ×6.15 | 41% | +0.08 | +0.15 |
| weapon.wand | 3649 | ×33.62 | 19% | +0.07 | +0.07 |
| weapon.bow | 2954 | ×27.73 | 19% | +0.08 | +0.08 |
| weapon.crossbow | 2761 | ×18.92 | 21% | +0.10 | +0.13 |
| weapon.warstaff | 1563 | ×49.68 | 18% | +0.09 | +0.11 |
| weapon.sceptre | 1448 | ×56.07 | 11% | +0.09 | +0.10 |
| weapon.staff | 1430 | ×62.87 | 18% | +0.06 | +0.07 |
| weapon.spear | 1220 | ×49.87 | 20% | +0.08 | +0.06 |
| armour.focus | 1021 | ×45.03 | 10% | +0.13 | +0.12 |
| armour.quiver | 947 | ×28.74 | 14% | +0.06 | +0.10 |
| armour.shield | 774 | ×17.92 | 19% | +0.03 | +0.04 |
| weapon.twomace | 732 | ×46.51 | 15% | +0.06 | +0.08 |
| flask.charm | 730 | ×24.99 | 35% | +0.01 | +0.02 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=44010, R²=-0.6177

intercept: `1.6044`  ·  log_price: True  ·  ilvl: `0.00006`  ·  n_mods: `0.01369`  ·  n_top_tier: `0.35405`  ·  corrupted: `0.32481`  ·  n_sockets: `-0.00009`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.58970 |
| `explicit.stat_2974417149@T1` | 0.50482 |
| `explicit.stat_789117908@T1` | -0.39587 |
| `explicit.stat_2891184298@T1` | 0.32510 |
| `explicit.stat_1050105434@T1` | -0.29232 |
| `explicit.stat_3299347043@T1` | -0.28338 |
| `implicit.stat_4041853756` | 0.22888 |
| `implicit.stat_3879011313` | 0.22888 |
| `explicit.stat_3141070085@T1` | -0.22628 |
| `explicit.stat_3917489142@T1` | 0.21919 |
| `explicit.stat_1589917703@T1` | -0.21173 |
| `implicit.stat_1379411836` | -0.18602 |

### jewel — n=43295, R²=-0.7823

intercept: `-1.4773`  ·  log_price: True  ·  ilvl: `0.03142`  ·  n_mods: `0.42742`  ·  n_top_tier: `-0.11094`  ·  corrupted: `0.17137`  ·  quality: `0.23311`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.37288 |
| `explicit.stat_3780644166@T1` | -2.81257 |
| `explicit.stat_1697447343@T1` | -2.79303 |
| `explicit.stat_627767961@T1` | -2.60626 |
| `explicit.stat_2301718443@T1` | 2.45744 |
| `explicit.stat_1315743832@T1` | 2.35716 |
| `explicit.stat_153777645@T1` | -2.31355 |
| `explicit.stat_3174700878@T1` | 1.97252 |
| `explicit.stat_3485067555@T1` | 1.94779 |
| `explicit.stat_795138349@T1` | -1.94363 |
| `explicit.stat_3473929743@T1` | -1.92605 |
| `explicit.stat_3028809864@T1` | -1.81521 |

### accessory.ring — n=40411, R²=-1.9775

intercept: `3.5123`  ·  log_price: True  ·  ilvl: `-0.04324`  ·  n_mods: `-0.00049`  ·  n_top_tier: `0.52764`  ·  corrupted: `0.11182`  ·  n_sockets: `-0.08274`  ·  quality: `0.07365`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -0.57164 |
| `explicit.stat_3325883026@T1` | -0.56615 |
| `explicit.stat_1573130764@T1` | -0.55759 |
| `explicit.stat_3962278098@T2` | -0.55393 |
| `explicit.stat_1263695895@T1` | -0.55224 |
| `explicit.stat_3917489142@T2` | -0.54880 |
| `explicit.stat_1368271171@T2` | -0.54849 |
| `explicit.stat_2144192055@T1` | -0.54714 |
| `explicit.stat_3032590688@T2` | -0.54611 |
| `explicit.stat_3291658075@T2` | -0.54575 |
| `explicit.stat_4220027924@T2` | -0.54535 |
| `explicit.stat_803737631@T2` | -0.54525 |

### accessory.amulet — n=37601, R²=-2.1247

intercept: `3.9586`  ·  log_price: True  ·  ilvl: `-0.04808`  ·  n_mods: `-0.02501`  ·  n_top_tier: `0.89738`  ·  corrupted: `0.04070`  ·  n_sockets: `-0.04016`  ·  quality: `0.00110`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T2` | -1.07221 |
| `explicit.stat_2748665614@T1` | -1.00484 |
| `explicit.stat_2748665614@T2` | -0.99232 |
| `explicit.stat_472520716@T1` | -0.96180 |
| `explicit.stat_3299347043@T2` | -0.95320 |
| `explicit.stat_3917489142@T2` | -0.94985 |
| `explicit.stat_1050105434@T2` | -0.94762 |
| `explicit.stat_472520716@T2` | -0.94572 |
| `explicit.stat_2901986750@T1` | -0.94522 |
| `explicit.stat_3917489142@T1` | -0.94091 |
| `explicit.stat_2974417149@T1` | -0.93656 |
| `explicit.stat_983749596@T1` | -0.93350 |

### accessory.belt — n=29380, R²=-0.7351

intercept: `6.9596`  ·  log_price: True  ·  ilvl: `-0.05984`  ·  n_mods: `-0.41392`  ·  n_top_tier: `1.09548`  ·  corrupted: `1.14010`  ·  n_sockets: `0.73985`

| stat_id | coef |
|---|---|
| `explicit.stat_2881298780@T1` | -1.71258 |
| `explicit.stat_1389754388@T1` | -1.65424 |
| `explicit.stat_51994685@T1` | -1.58612 |
| `explicit.stat_3299347043@T1` | -1.49206 |
| `explicit.stat_809229260@T2` | -1.31641 |
| `explicit.stat_3299347043@T2` | -1.29492 |
| `explicit.stat_644456512@T1` | -1.28406 |
| `explicit.stat_1671376347@T2` | -1.27066 |
| `explicit.stat_1389754388@T2` | -1.23434 |
| `explicit.stat_2881298780@T2` | -1.20919 |
| `explicit.stat_4220027924@T2` | -1.14741 |
| `explicit.stat_3585532255@T2` | -1.14727 |

### armour.chest — n=29059, R²=-1.4789

intercept: `4.0877`  ·  log_price: True  ·  ilvl: `-0.04988`  ·  n_mods: `-0.03573`  ·  n_top_tier: `0.47070`  ·  corrupted: `0.35725`  ·  n_sockets: `0.03883`  ·  quality: `0.03835`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.16075 |
| `explicit.stat_3981240776@T1` | 1.23651 |
| `explicit.stat_3033371881@T1` | 0.57199 |
| `explicit.stat_3484657501@T1` | -0.56839 |
| `explicit.stat_915769802@T2` | -0.54614 |
| `explicit.stat_4015621042@T1` | -0.54070 |
| `explicit.stat_986397080@T2` | -0.53356 |
| `explicit.stat_4080418644@T2` | -0.52129 |
| `explicit.stat_4080418644@T1` | -0.52097 |
| `explicit.stat_1999113824@T1` | -0.51471 |
| `explicit.stat_124859000@T2` | -0.50547 |
| `explicit.stat_915769802@T1` | -0.50025 |

### armour.helmet — n=28403, R²=-1.3485

intercept: `3.9934`  ·  log_price: True  ·  ilvl: `-0.05092`  ·  n_mods: `-0.03984`  ·  n_top_tier: `0.45605`  ·  corrupted: `0.74439`  ·  n_sockets: `0.07949`  ·  quality: `0.04943`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.32623 |
| `explicit.stat_2339757871@T1` | -3.25703 |
| `explicit.stat_1263695895@T1` | -0.82493 |
| `explicit.stat_53045048@T1` | -0.75875 |
| `explicit.stat_53045048@T2` | -0.71834 |
| `explicit.stat_1263695895@T2` | -0.63021 |
| `explicit.stat_1999113824@T1` | -0.62455 |
| `explicit.stat_3917489142@T2` | -0.62101 |
| `explicit.stat_587431675@T2` | -0.60270 |
| `explicit.stat_2162097452@T2` | -0.56936 |
| `explicit.stat_803737631@T2` | -0.56465 |
| `explicit.stat_1999113824@T2` | -0.54832 |

### armour.boots — n=26644, R²=-1.6533

intercept: `3.6316`  ·  log_price: True  ·  ilvl: `-0.04465`  ·  n_mods: `-0.01229`  ·  n_top_tier: `0.61338`  ·  corrupted: `0.08521`  ·  n_sockets: `0.00332`  ·  quality: `0.02654`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.51978 |
| `desecrated.stat_2250533757@T2` | -0.85483 |
| `explicit.stat_3917489142@T2` | -0.78305 |
| `explicit.stat_3917489142@T1` | -0.76153 |
| `explicit.stat_2339757871@T1` | -0.74086 |
| `explicit.stat_53045048@T1` | -0.66095 |
| `explicit.stat_4052037485@T2` | -0.65621 |
| `explicit.stat_2923486259@T2` | -0.65604 |
| `explicit.stat_3362812763@T1` | -0.64820 |
| `explicit.stat_2160282525@T1` | -0.64583 |
| `explicit.stat_1062208444@T2` | -0.64374 |
| `explicit.stat_2160282525@T2` | -0.64099 |

### armour.gloves — n=25968, R²=-1.717

intercept: `3.8455`  ·  log_price: True  ·  ilvl: `-0.04876`  ·  n_mods: `-0.01528`  ·  n_top_tier: `0.47455`  ·  corrupted: `-0.01738`  ·  n_sockets: `0.04180`  ·  quality: `0.04486`

| stat_id | coef |
|---|---|
| `explicit.stat_1671376347@T1` | 0.87199 |
| `explicit.stat_2339757871@T1` | 0.82765 |
| `explicit.stat_9187492@T1` | 0.81894 |
| `explicit.stat_9187492@T2` | -0.75956 |
| `explicit.stat_3484657501@T2` | -0.73575 |
| `explicit.stat_3917489142@T2` | -0.60142 |
| `explicit.stat_803737631@T2` | -0.59083 |
| `rune.stat_201332984` | 0.58768 |
| `explicit.stat_3484657501@T1` | -0.58272 |
| `explicit.stat_3032590688@T1` | -0.56044 |
| `explicit.stat_3917489142@T1` | -0.54626 |
| `explicit.stat_2923486259@T2` | -0.54295 |

### weapon.wand — n=17007, R²=-2.251

intercept: `3.7471`  ·  log_price: True  ·  ilvl: `-0.04650`  ·  n_mods: `-0.01040`  ·  n_top_tier: `0.05819`  ·  corrupted: `-0.06833`  ·  n_sockets: `0.03397`  ·  quality: `-0.00170`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.11286 |
| `rune.stat_124131830` | -2.67646 |
| `explicit.stat_2254480358@T1` | 2.56118 |
| `explicit.stat_591105508@T1` | 2.30297 |
| `explicit.stat_124131830@T1` | 2.25121 |
| `explicit.stat_4226189338@T1` | 2.20490 |
| `explicit.stat_736967255@T2` | 1.77885 |
| `explicit.stat_2768835289@T2` | 1.41504 |
| `crafted.stat_124131830` | 1.16147 |
| `explicit.stat_2254480358@T2` | 0.93372 |
| `explicit.stat_2974417149@T1` | 0.36593 |
| `explicit.stat_1600707273@T1` | 0.17472 |

### weapon.bow — n=13824, R²=-2.0942

intercept: `3.2760`  ·  log_price: True  ·  ilvl: `-0.03995`  ·  n_mods: `-0.01977`  ·  n_top_tier: `0.75072`  ·  corrupted: `-0.04088`  ·  n_sockets: `-0.00723`  ·  quality: `0.03033`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.86620 |
| `explicit.stat_1202301673@T1` | 1.44911 |
| `crafted.stat_3035140377` | 1.25814 |
| `explicit.stat_1263695895@T1` | -0.86740 |
| `explicit.stat_1509134228@T1` | -0.82238 |
| `explicit.stat_3695891184@T1` | -0.79861 |
| `explicit.stat_3695891184@T2` | -0.79475 |
| `explicit.stat_669069897@T1` | -0.79471 |
| `explicit.stat_55876295@T1` | -0.79168 |
| `explicit.stat_1263695895@T2` | -0.78841 |
| `explicit.stat_2694482655@T2` | -0.78345 |
| `explicit.stat_1368271171@T2` | -0.77707 |

### weapon.crossbow — n=13035, R²=-1.9391

intercept: `3.5085`  ·  log_price: True  ·  ilvl: `-0.04310`  ·  n_mods: `-0.01643`  ·  n_top_tier: `0.75230`  ·  corrupted: `-0.01496`  ·  n_sockets: `0.02914`  ·  quality: `0.00988`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.94435 |
| `explicit.stat_2250681686@T2` | -1.47106 |
| `explicit.stat_709508406@T1` | 1.39636 |
| `explicit.stat_1980802737` | 1.12608 |
| `explicit.stat_1202301673@T1` | 1.04446 |
| `explicit.stat_1202301673@T2` | -1.03972 |
| `explicit.stat_1263695895@T2` | -0.92250 |
| `explicit.stat_1263695895@T1` | -0.88003 |
| `crafted.stat_3035140377` | 0.85127 |
| `explicit.stat_3695891184@T1` | -0.83936 |
| `explicit.stat_3695891184@T2` | -0.82274 |
| `explicit.stat_1509134228@T2` | -0.81175 |

### flask.charm — n=10999, R²=-0.4983

intercept: `0.0002`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `1.58384`  ·  corrupted: `2.04708`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.36197 |
| `explicit.stat_1056492907` | 3.45199 |
| `explicit.stat_828533480@T2` | -1.58385 |
| `explicit.stat_3196823591@T2` | -1.58384 |
| `explicit.stat_1120862500@T2` | -1.58384 |
| `explicit.stat_1366840608@T2` | -1.58383 |
| `explicit.stat_1873752457@T1` | -1.58383 |
| `explicit.stat_1873752457@T2` | -1.58383 |
| `explicit.stat_2676834156@T2` | -1.58383 |
| `explicit.stat_2541588185@T2` | -1.58382 |
| `explicit.stat_388617051@T2` | -1.58382 |
| `explicit.stat_828533480@T1` | -1.58382 |

### weapon.warstaff — n=7615, R²=-0.512

intercept: `-3.9298`  ·  log_price: True  ·  ilvl: `0.05573`  ·  n_mods: `-0.15161`  ·  n_top_tier: `0.70237`  ·  corrupted: `0.16598`  ·  n_sockets: `0.08764`  ·  quality: `0.06524`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.38480 |
| `explicit.stat_328541901@T1` | -1.08600 |
| `explicit.stat_1037193709@T1` | 1.06112 |
| `explicit.stat_328541901@T2` | -1.05411 |
| `explicit.stat_691932474@T2` | -0.88242 |
| `explicit.stat_55876295@T1` | -0.80534 |
| `explicit.stat_55876295@T2` | -0.79083 |
| `explicit.stat_3336890334@T2` | -0.77531 |
| `explicit.stat_210067635@T1` | -0.77423 |
| `explicit.stat_3695891184@T2` | -0.75285 |
| `explicit.stat_1940865751@T1` | -0.74027 |
| `explicit.stat_1037193709@T2` | -0.73188 |

### weapon.sceptre — n=7020, R²=-0.4744

intercept: `-12.1214`  ·  log_price: True  ·  ilvl: `0.15274`  ·  n_mods: `-0.03144`  ·  n_top_tier: `0.43164`  ·  corrupted: `0.35857`  ·  n_sockets: `0.27577`  ·  quality: `0.09423`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.12914 |
| `explicit.stat_2162097452@T2` | 1.33312 |
| `explicit.stat_4080418644@T1` | -1.00006 |
| `explicit.stat_1574590649@T2` | -0.84271 |
| `explicit.stat_1263695895@T1` | -0.75084 |
| `explicit.stat_1263695895@T2` | -0.72821 |
| `explicit.stat_2347036682@T2` | -0.72023 |
| `explicit.stat_4080418644@T2` | -0.71428 |
| `explicit.stat_2854751904@T2` | -0.65610 |
| `explicit.stat_1050105434@T2` | -0.63699 |
| `explicit.stat_289128254@T2` | -0.59045 |
| `explicit.stat_3639275092@T2` | -0.45330 |

### weapon.staff — n=7002, R²=-0.5998

intercept: `-5.4862`  ·  log_price: True  ·  ilvl: `0.06984`  ·  n_mods: `-0.03062`  ·  n_top_tier: `0.39686`  ·  corrupted: `0.07379`  ·  n_sockets: `0.15244`  ·  quality: `0.04756`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.04746 |
| `rune.stat_124131830` | 2.04131 |
| `explicit.stat_124131830@T1` | 1.66924 |
| `explicit.stat_1545858329@T1` | 1.56124 |
| `explicit.stat_2768835289@T2` | 1.45274 |
| `explicit.stat_2254480358@T1` | 1.29064 |
| `explicit.stat_1600707273@T1` | 1.04715 |
| `explicit.stat_3291658075@T2` | 0.85270 |
| `explicit.stat_2254480358@T2` | 0.69727 |
| `explicit.stat_2974417149@T1` | -0.66026 |
| `explicit.stat_293638271@T2` | -0.50542 |
| `crafted.stat_124131830` | 0.47230 |

### weapon.spear — n=5918, R²=-0.6484

intercept: `-4.0272`  ·  log_price: True  ·  ilvl: `0.05312`  ·  n_mods: `-0.02030`  ·  n_top_tier: `0.42318`  ·  corrupted: `-0.09405`  ·  n_sockets: `0.08673`  ·  quality: `0.10165`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.05177 |
| `explicit.stat_9187492@T1` | 2.58243 |
| `explicit.stat_1202301673@T1` | 2.40471 |
| `crafted.stat_3035140377` | 1.13942 |
| `explicit.stat_210067635@T1` | 1.00941 |
| `explicit.stat_1509134228@T1` | 0.61963 |
| `explicit.stat_55876295@T1` | -0.54508 |
| `explicit.stat_1263695895@T2` | -0.52380 |
| `explicit.stat_55876295@T2` | -0.48574 |
| `explicit.stat_1509134228@T2` | -0.46880 |
| `explicit.stat_1940865751@T2` | -0.42852 |
| `explicit.stat_748522257@T1` | -0.41920 |

### armour.focus — n=4826, R²=-0.4644

intercept: `-9.0519`  ·  log_price: True  ·  ilvl: `0.11224`  ·  n_mods: `-0.05815`  ·  n_top_tier: `0.90636`  ·  corrupted: `0.67250`  ·  n_sockets: `0.44544`  ·  quality: `0.07297`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 4.81272 |
| `explicit.stat_4220027924@T2` | -1.28321 |
| `crafted.stat_737908626@T2` | -1.22276 |
| `explicit.stat_4220027924@T1` | -1.17451 |
| `explicit.stat_2923486259@T1` | -1.15102 |
| `explicit.stat_3962278098@T1` | -1.07947 |
| `explicit.stat_737908626@T2` | -1.04183 |
| `explicit.stat_2891184298@T2` | -1.00968 |
| `explicit.stat_328541901@T2` | -1.00362 |
| `explicit.stat_736967255@T2` | -0.98568 |
| `explicit.stat_2974417149@T1` | -0.96409 |
| `explicit.stat_3962278098@T2` | -0.93929 |

### armour.quiver — n=4503, R²=-0.4571

intercept: `-8.6677`  ·  log_price: True  ·  ilvl: `0.10580`  ·  n_mods: `-0.02332`  ·  n_top_tier: `0.77621`  ·  corrupted: `0.72456`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 7.27519 |
| `explicit.stat_2463230181@T1` | 2.71876 |
| `explicit.stat_2463230181@T2` | 1.34971 |
| `explicit.stat_2321178454@T2` | -1.15448 |
| `explicit.stat_2194114101@T2` | -1.01957 |
| `explicit.stat_1573130764@T1` | -0.95757 |
| `explicit.stat_681332047@T2` | -0.94691 |
| `explicit.stat_3261801346@T1` | -0.91151 |
| `explicit.stat_1573130764@T2` | -0.85455 |
| `explicit.stat_4067062424@T1` | -0.82314 |
| `explicit.stat_1368271171@T2` | -0.81267 |
| `explicit.stat_2321178454@T1` | -0.80081 |

### armour.shield — n=3952, R²=-0.562

intercept: `-7.3684`  ·  log_price: True  ·  ilvl: `0.09500`  ·  n_mods: `-0.05096`  ·  n_top_tier: `0.64458`  ·  corrupted: `0.32873`  ·  n_sockets: `0.04885`  ·  quality: `0.05080`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.64129 |
| `explicit.stat_2339757871@T1` | -1.31052 |
| `explicit.stat_1011760251@T1` | -1.26252 |
| `explicit.stat_1011760251@T2` | -1.05516 |
| `explicit.stat_328541901@T1` | -1.04392 |
| `explicit.stat_2481353198@T2` | -0.99722 |
| `explicit.stat_2481353198@T1` | -0.98966 |
| `explicit.stat_3033371881@T1` | 0.98748 |
| `explicit.stat_2881298780@T1` | -0.98301 |
| `explicit.stat_2881298780@T2` | -0.85033 |
| `explicit.stat_328541901@T2` | -0.82205 |
| `explicit.stat_3372524247@T2` | -0.80764 |

### weapon.twomace — n=3593, R²=-0.4927

intercept: `-10.0214`  ·  log_price: True  ·  ilvl: `0.13193`  ·  n_mods: `-0.12116`  ·  n_top_tier: `0.30967`  ·  corrupted: `0.74999`  ·  n_sockets: `0.14395`  ·  quality: `0.03924`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.64377 |
| `desecrated.stat_1509134228@T1` | 2.60326 |
| `explicit.stat_1037193709@T1` | -1.14113 |
| `explicit.stat_210067635@T1` | 1.13581 |
| `crafted.stat_3035140377` | 1.10026 |
| `explicit.stat_387439868@T2` | -0.81701 |
| `explicit.stat_3336890334@T1` | -0.78533 |
| `explicit.stat_821021828@T2` | -0.72933 |
| `explicit.stat_210067635@T2` | 0.62341 |
| `explicit.stat_2694482655@T1` | -0.57001 |
| `explicit.stat_518292764@T1` | 0.55898 |
| `explicit.stat_821021828@T1` | -0.54746 |

## Coverage (listings per base)

- … **Sapphire** — 20292 listings (20264 priced) [0.3–7553463.8 ex]
- … **Emerald** — 20063 listings (20038 priced) [0.3–7553463.8 ex]
- … **Ruby** — 15354 listings (15341 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 8636 listings (8627 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 6953 listings (6944 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 6788 listings (6775 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 6668 listings (6663 priced) [0.2–19945827.9 ex]
- … **Stellar Amulet** — 6402 listings (6398 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 6357 listings (6347 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 6216 listings (6207 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5392 listings (5378 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5191 listings (5185 priced) [0.2–307202867.9 ex]
- … **Ruby Ring** — 5006 listings (5004 priced) [0.2–37474957.5 ex]
- … **Topaz Ring** — 4992 listings (4988 priced) [0.3–307202867.9 ex]
- … **Plate Belt** — 4552 listings (4538 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4506 listings (4502 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4392 listings (4385 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4360 listings (4358 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4322 listings (4317 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4272 listings (4267 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4187 listings (4183 priced) [0.3–4275054.0 ex]
- … **Obliterator Bow** — 4155 listings (4143 priced) [0.3–42622633798.0 ex]
- … **Heavy Belt** — 4074 listings (4072 priced) [0.3–2608914286.6 ex]
- … **Pearl Ring** — 4004 listings (4000 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 3943 listings (3943 priced) [0.3–123132003.2 ex]

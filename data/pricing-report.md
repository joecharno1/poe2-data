# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-08T20:04:17+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **341264** (340766 priced in exalted)
- Distinct bases: 958 · distinct mods: 2869 · mod rows: 1620581
- Sold signals: **29841** sold · 181352 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-08T19:50:58+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×16.72** (median |log error| 2.8167)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 77% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×47.48 · ±30% 12% · n=49550
- Premium segment (60ex+): skill **+0.07** · typical error ×174.34 · ±30% 0% · n=30787

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 6530 | ×11.28 | 4% | +0.03 | +0.05 |
| accessory.amulet | 6184 | ×50.70 | 21% | +0.03 | +0.03 |
| jewel | 5812 | ×8.34 | 7% | +0.02 | +0.04 |
| accessory.belt | 4884 | ×10.26 | 20% | +0.04 | +0.07 |
| armour.chest | 4813 | ×10.00 | 26% | +0.00 | +0.01 |
| armour.helmet | 4714 | ×10.00 | 24% | +0.01 | +0.01 |
| armour.boots | 4432 | ×10.71 | 21% | +0.00 | +0.03 |
| armour.gloves | 4389 | ×14.94 | 20% | +0.00 | +0.02 |
| other | 4076 | ×10.00 | 35% | +0.09 | +0.29 |
| weapon.wand | 2939 | ×41.80 | 20% | +0.06 | +0.07 |
| weapon.bow | 2381 | ×20.89 | 19% | +0.09 | +0.11 |
| weapon.crossbow | 2217 | ×18.40 | 19% | +0.10 | +0.09 |
| weapon.warstaff | 1073 | ×74.69 | 17% | +0.05 | +0.05 |
| weapon.staff | 1036 | ×64.75 | 18% | +0.05 | +0.08 |
| weapon.sceptre | 1010 | ×50.00 | 13% | +0.07 | +0.06 |
| weapon.spear | 870 | ×45.00 | 17% | +0.03 | +0.04 |
| armour.focus | 701 | ×84.32 | 13% | +0.04 | +0.12 |
| armour.quiver | 659 | ×75.93 | 14% | +0.02 | +0.06 |
| armour.shield | 567 | ×20.00 | 17% | +0.03 | +0.07 |
| flask.charm | 564 | ×77.76 | 29% | +0.00 | +0.01 |
| weapon.twomace | 522 | ×20.00 | 14% | +0.04 | +0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=34818, R²=-0.4346

intercept: `1.5993`  ·  log_price: True  ·  ilvl: `0.00013`  ·  n_mods: `0.03806`  ·  n_top_tier: `0.77962`  ·  corrupted: `1.40214`  ·  n_sockets: `-0.00010`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.61032 |
| `explicit.stat_2482852589@T1` | 3.52551 |
| `explicit.stat_101878827@T1` | 3.19252 |
| `explicit.stat_1589917703@T1` | 3.16228 |
| `explicit.stat_2106365538@T1` | 3.13599 |
| `explicit.stat_3141070085@T1` | 2.51975 |
| `explicit.stat_1050105434@T1` | -1.67383 |
| `explicit.stat_3917489142@T1` | 1.50993 |
| `explicit.stat_789117908@T1` | -1.25899 |
| `explicit.stat_2974417149@T1` | 1.16749 |
| `explicit.stat_2891184298@T1` | 0.44972 |
| `implicit.stat_1379411836` | -0.27374 |

### jewel — n=31301, R²=-0.634

intercept: `-1.1132`  ·  log_price: True  ·  ilvl: `0.03582`  ·  n_mods: `0.25002`  ·  n_top_tier: `-0.11248`  ·  corrupted: `0.31104`  ·  quality: `0.21388`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.84975 |
| `explicit.stat_3741323227@T1` | -3.53938 |
| `explicit.stat_1569101201@T1` | 3.11540 |
| `explicit.stat_1569159338@T1` | -2.77803 |
| `explicit.stat_3780644166@T1` | -2.49071 |
| `explicit.stat_234296660@T1` | -2.12293 |
| `explicit.stat_3714003708@T1` | -2.00408 |
| `explicit.stat_1316278494@T1` | -1.74993 |
| `explicit.stat_2527686725@T1` | 1.56808 |
| `explicit.stat_1869147066@T1` | 1.47475 |
| `explicit.stat_3485067555@T1` | 1.42324 |
| `explicit.stat_1697951953@T1` | -1.42000 |

### accessory.ring — n=29922, R²=-1.1917

intercept: `3.7523`  ·  log_price: True  ·  ilvl: `-0.03848`  ·  n_mods: `-0.01911`  ·  n_top_tier: `0.10732`  ·  corrupted: `0.89785`  ·  n_sockets: `0.89303`  ·  quality: `0.04446`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 5.13433 |
| `explicit.stat_707457662@T2` | 4.51772 |
| `explicit.stat_1379411836@T1` | -1.95699 |
| `explicit.stat_1379411836@T2` | -1.45430 |
| `explicit.stat_1368271171@T1` | -1.18785 |
| `explicit.stat_1368271171@T2` | -1.06849 |
| `explicit.stat_1573130764@T1` | -0.97459 |
| `explicit.stat_707457662` | -0.79205 |
| `explicit.stat_2923486259@T1` | 0.79011 |
| `explicit.stat_2923486259@T2` | 0.78054 |
| `explicit.stat_1263695895@T1` | -0.74812 |
| `explicit.stat_2557965901@T1` | 0.63335 |

### accessory.amulet — n=28177, R²=-2.0539

intercept: `3.9427`  ·  log_price: True  ·  ilvl: `-0.04766`  ·  n_mods: `-0.02518`  ·  n_top_tier: `1.04657`  ·  corrupted: `0.11957`  ·  n_sockets: `1.73111`  ·  quality: `-0.00212`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.62209 |
| `explicit.stat_983749596@T2` | -1.43889 |
| `explicit.stat_3299347043@T1` | -1.26117 |
| `explicit.stat_2748665614@T1` | -1.15116 |
| `explicit.stat_587431675@T1` | -1.14514 |
| `explicit.stat_3299347043@T2` | -1.13375 |
| `explicit.stat_2748665614@T2` | -1.12738 |
| `explicit.stat_472520716@T2` | -1.12657 |
| `explicit.stat_472520716@T1` | -1.11845 |
| `explicit.stat_3917489142@T2` | -1.09884 |
| `explicit.stat_3917489142@T1` | -1.09823 |
| `explicit.stat_2106365538@T1` | -1.08860 |

### accessory.belt — n=22625, R²=-1.4528

intercept: `3.8725`  ·  log_price: True  ·  ilvl: `-0.04569`  ·  n_mods: `-0.03088`  ·  n_top_tier: `0.81720`  ·  corrupted: `0.80201`  ·  n_sockets: `-0.12173`

| stat_id | coef |
|---|---|
| `explicit.stat_2881298780@T1` | -0.91146 |
| `explicit.stat_1389754388@T1` | -0.87989 |
| `explicit.stat_809229260@T2` | -0.87208 |
| `explicit.stat_2881298780@T2` | -0.86084 |
| `explicit.stat_4220027924@T2` | -0.85087 |
| `explicit.stat_51994685@T1` | -0.84379 |
| `explicit.stat_1671376347@T2` | -0.83367 |
| `explicit.stat_3325883026@T1` | -0.83298 |
| `explicit.stat_915769802@T2` | -0.82033 |
| `explicit.stat_1389754388@T2` | -0.81557 |
| `explicit.stat_3299347043@T2` | -0.81414 |
| `explicit.stat_3585532255@T2` | -0.80979 |

### armour.chest — n=22412, R²=-0.2509

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.05410`  ·  corrupted: `0.00008`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_915769802@T2` | -0.05413 |
| `explicit.stat_915769802@T1` | -0.05412 |
| `explicit.stat_4080418644@T2` | -0.05412 |
| `explicit.stat_3484657501@T1` | -0.05412 |
| `explicit.stat_3261801346@T1` | -0.05412 |
| `explicit.stat_3261801346@T2` | -0.05411 |
| `explicit.stat_3325883026@T2` | -0.05411 |
| `explicit.stat_1062208444@T1` | -0.05411 |
| `explicit.stat_3484657501@T2` | -0.05411 |
| `explicit.stat_2451402625@T2` | -0.05411 |
| `explicit.stat_2923486259@T2` | -0.05411 |
| `explicit.stat_124859000@T2` | -0.05411 |

### armour.helmet — n=21945, R²=-0.2782

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.14979`  ·  corrupted: `1.60336`  ·  n_sockets: `0.00001`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 0.28959 |
| `explicit.stat_3362812763@T2` | -0.14982 |
| `explicit.stat_2451402625@T1` | -0.14981 |
| `explicit.stat_53045048@T2` | -0.14981 |
| `explicit.stat_803737631@T2` | -0.14980 |
| `explicit.stat_1263695895@T1` | -0.14980 |
| `explicit.stat_4080418644@T2` | -0.14980 |
| `explicit.stat_1263695895@T2` | -0.14980 |
| `explicit.stat_3362812763@T1` | -0.14980 |
| `explicit.stat_3917489142@T2` | -0.14979 |
| `explicit.stat_53045048@T1` | -0.14979 |
| `explicit.stat_3261801346@T2` | -0.14979 |

### armour.boots — n=20737, R²=-0.3054

intercept: `2.3402`  ·  log_price: True  ·  ilvl: `-0.00075`  ·  n_mods: `-0.00562`  ·  n_top_tier: `0.12222`  ·  corrupted: `0.02873`  ·  n_sockets: `0.00063`  ·  quality: `0.00052`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 1.41030 |
| `explicit.stat_2339757871@T1` | -0.14594 |
| `rune.stat_232299587` | 0.14216 |
| `desecrated.stat_2250533757@T2` | -0.14124 |
| `explicit.stat_1062208444@T2` | -0.13699 |
| `explicit.stat_2451402625@T2` | -0.13353 |
| `explicit.stat_2923486259@T2` | -0.12804 |
| `explicit.stat_3261801346@T2` | -0.12760 |
| `explicit.stat_1062208444@T1` | -0.12688 |
| `explicit.stat_1671376347@T2` | -0.12612 |
| `explicit.stat_1999113824@T1` | -0.12612 |
| `explicit.stat_3033371881@T2` | -0.12534 |

### armour.gloves — n=20191, R²=-0.3627

intercept: `2.3036`  ·  log_price: True  ·  ilvl: `-0.00003`  ·  n_mods: `-0.00019`  ·  n_top_tier: `0.00277`  ·  corrupted: `0.00237`  ·  n_sockets: `0.00017`  ·  quality: `0.00003`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.10594 |
| `desecrated.stat_4067062424` | 0.09551 |
| `pseudo.total_ele_res>=80` | 0.01770 |
| `desecrated.stat_3299347043` | 0.01598 |
| `rune.stat_789117908` | -0.01484 |
| `explicit.stat_3299347043` | 0.00737 |
| `pseudo.total_life` | -0.00737 |
| `rune.stat_3299347043` | 0.00734 |
| `explicit.stat_3484657501@T2` | -0.00329 |
| `explicit.stat_3362812763@T2` | -0.00321 |
| `explicit.stat_803737631@T2` | -0.00314 |
| `explicit.stat_9187492@T2` | -0.00310 |

### weapon.wand — n=13716, R²=-2.0854

intercept: `3.4987`  ·  log_price: True  ·  ilvl: `-0.04352`  ·  n_mods: `-0.01227`  ·  n_top_tier: `0.41515`  ·  corrupted: `-0.00349`  ·  n_sockets: `0.02672`  ·  quality: `0.01449`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.65828 |
| `explicit.stat_591105508@T1` | 1.94445 |
| `explicit.stat_1545858329@T1` | 1.93436 |
| `explicit.stat_4226189338@T1` | 1.93109 |
| `explicit.stat_124131830@T1` | 1.89176 |
| `explicit.stat_736967255@T2` | 1.72797 |
| `explicit.stat_1600707273@T1` | 1.71443 |
| `crafted.stat_124131830` | 0.79705 |
| `explicit.stat_1600707273@T2` | 0.60725 |
| `explicit.stat_2231156303@T2` | -0.45156 |
| `explicit.stat_3015669065@T1` | -0.44922 |
| `explicit.stat_3015669065@T2` | -0.44275 |

### weapon.bow — n=11159, R²=-1.9306

intercept: `3.3885`  ·  log_price: True  ·  ilvl: `-0.04196`  ·  n_mods: `-0.01154`  ·  n_top_tier: `0.65599`  ·  corrupted: `0.20556`  ·  n_sockets: `0.00263`  ·  quality: `0.00707`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.27809 |
| `desecrated.stat_210067635@T1` | -2.06092 |
| `explicit.stat_2463230181@T1` | 1.64119 |
| `crafted.stat_3035140377` | 1.55739 |
| `explicit.stat_1202301673@T1` | 1.43116 |
| `rune.stat_3885405204` | -1.01116 |
| `explicit.stat_518292764@T1` | 0.91668 |
| `explicit.stat_55876295@T1` | -0.72262 |
| `explicit.stat_1037193709@T1` | -0.69435 |
| `explicit.stat_3695891184@T2` | -0.69398 |
| `explicit.stat_2694482655@T1` | -0.69133 |
| `explicit.stat_3336890334@T2` | -0.69117 |

### weapon.crossbow — n=10477, R²=-1.8084

intercept: `3.5539`  ·  log_price: True  ·  ilvl: `-0.04398`  ·  n_mods: `-0.01205`  ·  n_top_tier: `0.72440`  ·  corrupted: `-0.01482`  ·  n_sockets: `0.02025`  ·  quality: `0.00364`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -2.78367 |
| `explicit.stat_1980802737` | 2.00861 |
| `explicit.stat_2250681686@T2` | -1.50443 |
| `explicit.stat_709508406@T1` | 1.44563 |
| `explicit.stat_1202301673@T1` | 1.23159 |
| `explicit.stat_1202301673@T2` | -1.00032 |
| `explicit.stat_1509134228@T2` | -0.88231 |
| `explicit.stat_2250681686` | 0.78869 |
| `explicit.stat_669069897@T1` | -0.78763 |
| `explicit.stat_1940865751@T2` | -0.76150 |
| `explicit.stat_691932474@T1` | -0.75804 |
| `explicit.stat_669069897@T2` | -0.75563 |

### flask.charm — n=7597, R²=-0.4088

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.41018`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.35363 |
| `explicit.stat_1056492907` | 2.99570 |
| `explicit.stat_2676834156@T1` | 1.60935 |
| `explicit.stat_2541588185@T1` | 0.48153 |
| `explicit.stat_2678930256` | 0.02127 |
| `explicit.stat_3138344128` | 0.02097 |
| `explicit.stat_3246948616` | 0.00005 |
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_1120862500@T2` | -0.00004 |
| `explicit.stat_1873752457@T2` | -0.00003 |
| `explicit.stat_828533480@T2` | -0.00003 |
| `explicit.stat_1873752457@T1` | -0.00003 |

### weapon.warstaff — n=5419, R²=-0.5534

intercept: `-0.0008`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.16193`  ·  corrupted: `0.59209`  ·  n_sockets: `0.00001`  ·  quality: `0.01906`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.55293 |
| `explicit.stat_9187492@T1` | 1.44741 |
| `rune.stat_731403740` | 1.38271 |
| `rune.stat_1712188793` | -0.61209 |
| `crafted.stat_210067635@T2` | -0.57862 |
| `desecrated.stat_9187492` | 0.47661 |
| `crafted.stat_3035140377` | 0.31653 |
| `desecrated.stat_518292764` | 0.26625 |
| `rune.stat_1037193709` | 0.18455 |
| `explicit.stat_1509134228@T1` | -0.16198 |
| `explicit.stat_328541901@T1` | -0.16196 |
| `explicit.stat_821021828@T1` | -0.16196 |

### weapon.staff — n=5017, R²=-0.627

intercept: `-0.0021`  ·  log_price: True  ·  ilvl: `0.00003`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.02781`  ·  corrupted: `0.23858`  ·  n_sockets: `0.00010`  ·  quality: `0.00009`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 6.90622 |
| `explicit.stat_4226189338@T1` | 2.25251 |
| `explicit.stat_2254480358@T1` | 1.58147 |
| `explicit.stat_2768835289@T2` | 1.58098 |
| `explicit.stat_124131830@T1` | 1.21535 |
| `explicit.stat_2254480358@T2` | 1.07081 |
| `explicit.stat_3291658075@T2` | 1.03108 |
| `explicit.stat_473429811@T1` | 0.66611 |
| `explicit.stat_1600707273@T1` | 0.66512 |
| `explicit.stat_3962278098@T2` | 0.66505 |
| `crafted.stat_124131830` | 0.41520 |
| `rune.stat_3909696841` | 0.23018 |

### weapon.sceptre — n=4977, R²=-0.619

intercept: `-0.3294`  ·  log_price: True  ·  ilvl: `0.00409`  ·  n_mods: `-0.00129`  ·  n_top_tier: `0.61877`  ·  corrupted: `1.09832`  ·  n_sockets: `0.00831`  ·  quality: `0.07646`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.69178 |
| `explicit.stat_4080418644@T1` | -0.63576 |
| `explicit.stat_4080418644@T2` | -0.62892 |
| `explicit.stat_2347036682@T2` | -0.62475 |
| `explicit.stat_1263695895@T2` | -0.62240 |
| `explicit.stat_1250712710@T1` | -0.62227 |
| `explicit.stat_3639275092@T2` | -0.61948 |
| `explicit.stat_1574590649@T1` | -0.61943 |
| `explicit.stat_328541901@T1` | -0.61899 |
| `explicit.stat_2854751904@T1` | -0.61808 |
| `explicit.stat_1574590649@T2` | -0.61802 |
| `explicit.stat_770672621@T2` | -0.61785 |

### weapon.spear — n=4264, R²=-0.5812

intercept: `-0.0008`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00142`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00002`  ·  quality: `0.05378`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 2.78029 |
| `explicit.stat_1202301673@T1` | 2.54364 |
| `crafted.stat_3035140377` | 1.17919 |
| `explicit.stat_210067635@T1` | 1.09295 |
| `explicit.stat_3336890334@T1` | 0.69447 |
| `explicit.stat_1509134228@T1` | 0.63198 |
| `crafted.stat_518292764` | 0.60940 |
| `explicit.stat_709508406@T1` | 0.43648 |
| `rune.stat_1039491398` | 0.09883 |
| `desecrated.stat_210067635` | -0.09370 |
| `explicit.stat_9187492@T1` | 0.08373 |
| `rune.stat_1509134228` | 0.04360 |

### armour.focus — n=3456, R²=-0.6555

intercept: `-0.4446`  ·  log_price: True  ·  ilvl: `0.00549`  ·  n_mods: `-0.00231`  ·  n_top_tier: `0.52536`  ·  corrupted: `0.00020`  ·  n_sockets: `0.01409`  ·  quality: `0.06989`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -5.40681 |
| `desecrated.stat_378817135@T1` | 0.90129 |
| `explicit.stat_1671376347@T1` | 0.78292 |
| `desecrated.stat_3393628375@T1` | -0.73554 |
| `explicit.stat_789117908@T2` | -0.54485 |
| `explicit.stat_3291658075@T1` | -0.54220 |
| `explicit.stat_2891184298@T2` | -0.53704 |
| `explicit.stat_4220027924@T2` | -0.53648 |
| `explicit.stat_4052037485@T2` | -0.53625 |
| `explicit.stat_2923486259@T1` | -0.53313 |
| `explicit.stat_736967255@T2` | -0.53290 |
| `explicit.stat_2231156303@T2` | -0.53098 |

### armour.quiver — n=3243, R²=-0.6579

intercept: `-0.1125`  ·  log_price: True  ·  ilvl: `0.00133`  ·  n_mods: `0.00023`  ·  n_top_tier: `0.67938`  ·  corrupted: `0.31390`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 12.30513 |
| `desecrated.stat_3932115504` | -0.87097 |
| `explicit.stat_2463230181@T1` | 0.81201 |
| `explicit.stat_2463230181@T2` | -0.71336 |
| `explicit.stat_1241625305@T1` | 0.69889 |
| `explicit.stat_681332047@T2` | -0.68757 |
| `explicit.stat_681332047@T1` | -0.68641 |
| `explicit.stat_1573130764@T1` | -0.68402 |
| `explicit.stat_1368271171@T2` | -0.68249 |
| `explicit.stat_2194114101@T2` | -0.68232 |
| `explicit.stat_1573130764@T2` | -0.68190 |
| `explicit.stat_3714003708@T2` | -0.68172 |

### armour.shield — n=2786, R²=-0.575

intercept: `-0.0069`  ·  log_price: True  ·  ilvl: `0.00009`  ·  n_mods: `0.00002`  ·  n_top_tier: `0.27097`  ·  corrupted: `0.00118`  ·  n_sockets: `0.00006`  ·  quality: `0.06867`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.92457 |
| `explicit.stat_4220027924@T1` | 0.61525 |
| `explicit.stat_1978899297@T2` | -0.47781 |
| `explicit.stat_1011760251@T1` | -0.27740 |
| `explicit.stat_1011760251@T2` | -0.27551 |
| `explicit.stat_328541901@T1` | -0.27250 |
| `explicit.stat_328541901@T2` | -0.27230 |
| `explicit.stat_2339757871@T1` | -0.27147 |
| `explicit.stat_3484657501@T1` | -0.27137 |
| `explicit.stat_2481353198@T1` | -0.27124 |
| `explicit.stat_3484657501@T2` | -0.27120 |
| `explicit.stat_1671376347@T1` | -0.27119 |

### weapon.twomace — n=2473, R²=-0.5679

intercept: `-0.0106`  ·  log_price: True  ·  ilvl: `0.00014`  ·  n_mods: `-0.00004`  ·  n_top_tier: `0.68918`  ·  corrupted: `0.01084`  ·  n_sockets: `0.00022`  ·  quality: `0.00164`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.34236 |
| `crafted.stat_3035140377` | 1.22548 |
| `desecrated.stat_1509134228@T1` | -0.72475 |
| `explicit.stat_3336890334@T1` | -0.69014 |
| `explicit.stat_1037193709@T1` | -0.68995 |
| `explicit.stat_387439868@T2` | -0.68972 |
| `explicit.stat_821021828@T2` | -0.68958 |
| `explicit.stat_821021828@T1` | -0.68953 |
| `explicit.stat_1263695895@T2` | -0.68951 |
| `explicit.stat_1263695895@T1` | -0.68943 |
| `explicit.stat_1037193709@T2` | -0.68937 |
| `explicit.stat_669069897@T1` | -0.68935 |

## Coverage (listings per base)

- … **Sapphire** — 14859 listings (14838 priced) [0.3–7553463.8 ex]
- … **Emerald** — 14719 listings (14706 priced) [0.4–7553463.8 ex]
- … **Ruby** — 11326 listings (11314 priced) [0.2–308559482.1 ex]
- … **Utility Belt** — 6644 listings (6639 priced) [0.3–5288620.9 ex]
- … **Prismatic Ring** — 5198 listings (5193 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 5056 listings (5048 priced) [1.0–66666666.0 ex]
- … **Stellar Amulet** — 5000 listings (4997 priced) [0.3–35690283.3 ex]
- … **Amethyst Ring** — 4982 listings (4981 priced) [0.3–4323655.9 ex]
- … **Gold Amulet** — 4814 listings (4808 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 4672 listings (4670 priced) [0.3–24532814.5 ex]
- … **Dueling Wand** — 4297 listings (4292 priced) [0.3–3956304924.1 ex]
- … **Sapphire Ring** — 3910 listings (3905 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 3791 listings (3790 priced) [0.3–37474957.5 ex]
- … **Topaz Ring** — 3775 listings (3772 priced) [1.0–307202867.9 ex]
- … **Plate Belt** — 3429 listings (3424 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 3389 listings (3387 priced) [0.3–5286174.1 ex]
- … **Ancestral Tiara** — 3364 listings (3359 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3334 listings (3333 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3312 listings (3311 priced) [0.3–4547453.5 ex]
- … **Obliterator Bow** — 3308 listings (3299 priced) [0.3–22139622146.9 ex]
- … **Heavy Belt** — 3212 listings (3212 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 3169 listings (3169 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 3110 listings (3110 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 3045 listings (3043 priced) [0.3–24532814.5 ex]
- … **Lunar Amulet** — 2968 listings (2966 priced) [0.3–4877938.3 ex]

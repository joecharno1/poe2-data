# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-15T01:37:21+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **491580** (490567 priced in exalted)
- Distinct bases: 980 · distinct mods: 3074 · mod rows: 2333768
- Sold signals: **26472** sold · 273890 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-15T01:28:57+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.15** (median |log error| 3.1844)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.09** · typical error ×64.76 · ±30% 5% · n=70563
- Premium segment (60ex+): skill **+0.10** · typical error ×291.87 · ±30% 0% · n=46835

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 9714 | ×52.67 | 20% | +0.06 | +0.08 |
| jewel | 9055 | ×9.41 | 5% | +0.02 | +0.05 |
| accessory.amulet | 9031 | ×50.23 | 21% | +0.03 | +0.03 |
| accessory.belt | 6973 | ×16.72 | 4% | +0.02 | +0.04 |
| armour.chest | 6789 | ×20.05 | 19% | +0.07 | +0.09 |
| armour.helmet | 6579 | ×21.33 | 14% | +0.08 | +0.10 |
| armour.boots | 6144 | ×24.94 | 21% | +0.06 | +0.08 |
| armour.gloves | 6052 | ×31.60 | 17% | +0.06 | +0.08 |
| other | 5317 | ×3.98 | 41% | +0.09 | +0.16 |
| weapon.wand | 3886 | ×34.44 | 18% | +0.07 | +0.09 |
| weapon.bow | 3113 | ×24.58 | 17% | +0.10 | +0.11 |
| weapon.crossbow | 2917 | ×21.18 | 21% | +0.08 | +0.12 |
| weapon.warstaff | 1746 | ×34.75 | 17% | +0.10 | +0.09 |
| weapon.staff | 1642 | ×53.61 | 15% | +0.08 | +0.09 |
| weapon.sceptre | 1642 | ×44.63 | 7% | +0.13 | +0.13 |
| weapon.spear | 1330 | ×69.31 | 16% | +0.09 | +0.07 |
| armour.focus | 1106 | ×44.07 | 8% | +0.12 | +0.14 |
| armour.quiver | 1047 | ×35.75 | 11% | +0.09 | +0.12 |
| flask.charm | 886 | ×50.00 | 34% | +0.02 | +0.05 |
| armour.shield | 872 | ×17.36 | 16% | +0.02 | +0.01 |
| weapon.twomace | 786 | ×22.12 | 17% | +0.06 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=48724, R²=-0.8657

intercept: `-1.6738`  ·  log_price: True  ·  ilvl: `0.02985`  ·  n_mods: `0.47983`  ·  n_top_tier: `-0.08266`  ·  corrupted: `0.08837`  ·  quality: `0.22875`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.90723 |
| `explicit.stat_2301718443@T1` | 3.20630 |
| `explicit.stat_1697447343@T1` | -2.38762 |
| `explicit.stat_3780644166@T1` | -2.29077 |
| `explicit.stat_627767961@T1` | -2.17850 |
| `explicit.stat_2594634307@T1` | 1.92870 |
| `explicit.stat_3166958180@T1` | -1.92104 |
| `explicit.stat_234296660@T1` | -1.91618 |
| `explicit.stat_239367161@T1` | -1.78357 |
| `explicit.stat_3091578504@T1` | -1.74958 |
| `explicit.stat_3485067555@T1` | 1.70669 |
| `explicit.stat_1697951953@T1` | -1.67765 |

### other — n=47628, R²=-0.5962

intercept: `1.6050`  ·  log_price: True  ·  ilvl: `0.00006`  ·  n_mods: `0.01394`  ·  n_top_tier: `0.36348`  ·  corrupted: `0.33601`  ·  n_sockets: `-0.00006`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.52588 |
| `explicit.stat_2974417149@T1` | 0.52192 |
| `explicit.stat_2482852589@T1` | -0.40303 |
| `explicit.stat_3299347043@T1` | -0.35930 |
| `explicit.stat_789117908@T1` | -0.32709 |
| `explicit.stat_3917489142@T1` | 0.28266 |
| `explicit.stat_2968503605@T1` | 0.27622 |
| `implicit.stat_3879011313` | 0.22907 |
| `implicit.stat_2219129443` | 0.22886 |
| `implicit.stat_4041853756` | 0.22886 |
| `explicit.stat_2106365538@T1` | -0.22712 |
| `explicit.stat_1589917703@T1` | -0.19089 |

### accessory.ring — n=44605, R²=-1.975

intercept: `3.5365`  ·  log_price: True  ·  ilvl: `-0.04364`  ·  n_mods: `0.00010`  ·  n_top_tier: `0.45155`  ·  corrupted: `0.19107`  ·  n_sockets: `2.18916`  ·  quality: `0.07415`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -0.49584 |
| `explicit.stat_1573130764@T1` | -0.49519 |
| `explicit.stat_3325883026@T1` | -0.49275 |
| `explicit.stat_1263695895@T1` | -0.48455 |
| `explicit.stat_2144192055@T1` | -0.47703 |
| `explicit.stat_3291658075@T1` | -0.47664 |
| `explicit.stat_1368271171@T2` | -0.47401 |
| `explicit.stat_3962278098@T2` | -0.47332 |
| `explicit.stat_3291658075@T2` | -0.47205 |
| `explicit.stat_803737631@T1` | -0.47177 |
| `explicit.stat_1263695895@T2` | -0.47168 |
| `explicit.stat_4220027924@T2` | -0.47058 |

### accessory.amulet — n=41284, R²=-2.1365

intercept: `3.8230`  ·  log_price: True  ·  ilvl: `-0.04673`  ·  n_mods: `-0.02435`  ·  n_top_tier: `1.00029`  ·  corrupted: `0.06078`  ·  n_sockets: `-0.11167`  ·  quality: `-0.00095`

| stat_id | coef |
|---|---|
| `explicit.stat_472520716@T1` | -1.07205 |
| `explicit.stat_472520716@T2` | -1.07179 |
| `explicit.stat_1050105434@T2` | -1.05160 |
| `explicit.stat_2901986750@T1` | -1.04999 |
| `explicit.stat_2748665614@T1` | -1.04800 |
| `explicit.stat_3917489142@T2` | -1.04446 |
| `explicit.stat_803737631@T1` | -1.04204 |
| `explicit.stat_2974417149@T1` | -1.03874 |
| `explicit.stat_2866361420@T2` | -1.03718 |
| `explicit.stat_2748665614@T2` | -1.03678 |
| `explicit.stat_2866361420@T1` | -1.03124 |
| `explicit.stat_789117908@T2` | -1.03118 |

### accessory.belt — n=31946, R²=-0.7514

intercept: `6.3571`  ·  log_price: True  ·  ilvl: `-0.05758`  ·  n_mods: `-0.37705`  ·  n_top_tier: `1.17120`  ·  corrupted: `0.70476`  ·  n_sockets: `0.58174`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.76886 |
| `explicit.stat_2881298780@T1` | -1.68912 |
| `explicit.stat_3299347043@T1` | -1.68878 |
| `explicit.stat_51994685@T1` | -1.46162 |
| `explicit.stat_809229260@T2` | -1.43196 |
| `explicit.stat_644456512@T1` | -1.41223 |
| `explicit.stat_3299347043@T2` | -1.38880 |
| `explicit.stat_809229260@T1` | -1.30213 |
| `explicit.stat_1389754388@T2` | -1.28371 |
| `explicit.stat_4080418644@T2` | -1.27583 |
| `explicit.stat_3585532255@T2` | -1.25332 |
| `explicit.stat_3325883026@T1` | -1.24608 |

### armour.chest — n=31586, R²=-1.5666

intercept: `3.7774`  ·  log_price: True  ·  ilvl: `-0.04622`  ·  n_mods: `-0.03510`  ·  n_top_tier: `0.47750`  ·  corrupted: `0.39299`  ·  n_sockets: `0.04318`  ·  quality: `0.03901`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.89507 |
| `explicit.stat_3981240776@T1` | 1.06455 |
| `explicit.stat_3033371881@T1` | 0.71385 |
| `explicit.stat_2923486259@T1` | -0.61435 |
| `explicit.stat_3484657501@T1` | -0.59126 |
| `explicit.stat_2923486259@T2` | -0.58106 |
| `explicit.stat_4015621042@T1` | -0.56070 |
| `explicit.stat_986397080@T2` | -0.55046 |
| `explicit.stat_4080418644@T2` | -0.53145 |
| `explicit.stat_4080418644@T1` | -0.52402 |
| `explicit.stat_1692879867@T1` | -0.51841 |
| `explicit.stat_915769802@T2` | -0.51485 |

### armour.helmet — n=30773, R²=-1.433

intercept: `3.8169`  ·  log_price: True  ·  ilvl: `-0.04832`  ·  n_mods: `-0.04657`  ·  n_top_tier: `0.46205`  ·  corrupted: `0.64553`  ·  n_sockets: `0.06164`  ·  quality: `0.05002`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.03809 |
| `crafted.stat_3917489142@T1` | 2.11087 |
| `explicit.stat_1263695895@T1` | -0.87513 |
| `explicit.stat_3917489142@T2` | -0.77915 |
| `explicit.stat_1263695895@T2` | -0.70074 |
| `explicit.stat_53045048@T1` | -0.64529 |
| `explicit.stat_53045048@T2` | -0.63389 |
| `explicit.stat_3917489142@T1` | -0.60091 |
| `explicit.stat_3261801346@T2` | -0.58091 |
| `explicit.stat_587431675@T2` | -0.57277 |
| `explicit.stat_3261801346@T1` | -0.56546 |
| `explicit.stat_1999113824@T1` | -0.55396 |

### armour.boots — n=28895, R²=-1.7137

intercept: `3.5673`  ·  log_price: True  ·  ilvl: `-0.04404`  ·  n_mods: `-0.01358`  ·  n_top_tier: `0.73734`  ·  corrupted: `0.00640`  ·  n_sockets: `0.00508`  ·  quality: `0.02363`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.40372 |
| `explicit.stat_3917489142@T2` | -0.86107 |
| `explicit.stat_2339757871@T1` | -0.82858 |
| `explicit.stat_3917489142@T1` | -0.81145 |
| `explicit.stat_53045048@T1` | -0.79513 |
| `explicit.stat_3299347043@T1` | -0.78890 |
| `explicit.stat_2160282525@T1` | -0.78359 |
| `explicit.stat_2923486259@T2` | -0.76868 |
| `explicit.stat_3362812763@T1` | -0.76660 |
| `explicit.stat_1671376347@T2` | -0.76561 |
| `explicit.stat_2160282525@T2` | -0.75812 |
| `explicit.stat_4052037485@T2` | -0.75796 |

### armour.gloves — n=28169, R²=-1.7474

intercept: `3.5949`  ·  log_price: True  ·  ilvl: `-0.04570`  ·  n_mods: `-0.00990`  ·  n_top_tier: `0.58825`  ·  corrupted: `-0.05901`  ·  n_sockets: `0.05300`  ·  quality: `0.05020`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | -6.54359 |
| `explicit.stat_9187492@T2` | -0.88671 |
| `explicit.stat_3484657501@T2` | -0.85862 |
| `explicit.stat_9187492@T1` | 0.82686 |
| `explicit.stat_1671376347@T1` | 0.78416 |
| `explicit.stat_3484657501@T1` | -0.73980 |
| `explicit.stat_4052037485@T1` | -0.70981 |
| `explicit.stat_803737631@T2` | -0.69731 |
| `explicit.stat_3321629045@T2` | -0.69081 |
| `explicit.stat_3917489142@T2` | -0.67824 |
| `explicit.stat_803737631@T1` | -0.64536 |
| `explicit.stat_1573130764@T1` | -0.63193 |

### weapon.wand — n=18179, R²=-2.2161

intercept: `3.5761`  ·  log_price: True  ·  ilvl: `-0.04415`  ·  n_mods: `-0.01470`  ·  n_top_tier: `0.59409`  ·  corrupted: `-0.01455`  ·  n_sockets: `0.03624`  ·  quality: `0.00297`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.92008 |
| `explicit.stat_1545858329@T1` | 2.88514 |
| `explicit.stat_2254480358@T1` | 2.36577 |
| `explicit.stat_4226189338@T1` | 1.73362 |
| `explicit.stat_591105508@T1` | 1.69976 |
| `explicit.stat_124131830@T1` | 1.56582 |
| `explicit.stat_736967255@T2` | 1.28321 |
| `crafted.stat_124131830` | 1.15502 |
| `explicit.stat_2768835289@T2` | 0.85911 |
| `explicit.stat_2254480358@T2` | 0.78736 |
| `explicit.stat_737908626@T1` | -0.67528 |
| `explicit.stat_1263695895@T2` | -0.67285 |

### weapon.bow — n=14675, R²=-1.9539

intercept: `3.4078`  ·  log_price: True  ·  ilvl: `-0.04073`  ·  n_mods: `-0.04674`  ·  n_top_tier: `0.64614`  ·  corrupted: `-0.06162`  ·  n_sockets: `0.00242`  ·  quality: `0.03137`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.00178 |
| `explicit.stat_1202301673@T1` | 1.47367 |
| `crafted.stat_3035140377` | 1.28652 |
| `desecrated.stat_666077204@T1` | 1.00970 |
| `explicit.stat_1263695895@T1` | -0.89574 |
| `explicit.stat_1263695895@T2` | -0.79490 |
| `explicit.stat_1509134228@T1` | -0.73620 |
| `explicit.stat_3695891184@T2` | -0.73372 |
| `explicit.stat_1368271171@T2` | -0.72984 |
| `explicit.stat_2463230181@T2` | -0.72359 |
| `explicit.stat_518292764@T2` | -0.71477 |
| `explicit.stat_2694482655@T2` | -0.70495 |

### weapon.crossbow — n=13882, R²=-2.001

intercept: `3.5902`  ·  log_price: True  ·  ilvl: `-0.04391`  ·  n_mods: `-0.01467`  ·  n_top_tier: `0.72792`  ·  corrupted: `0.02124`  ·  n_sockets: `0.01705`  ·  quality: `0.00825`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -2.01187 |
| `explicit.stat_709508406@T1` | 1.49611 |
| `explicit.stat_2250681686@T2` | -1.49310 |
| `explicit.stat_1202301673@T1` | 1.43632 |
| `explicit.stat_1980802737` | 1.20779 |
| `crafted.stat_3035140377` | 0.92888 |
| `explicit.stat_1263695895@T2` | -0.87780 |
| `explicit.stat_1263695895@T1` | -0.85067 |
| `explicit.stat_2250681686` | 0.84175 |
| `explicit.stat_669069897@T1` | -0.78946 |
| `explicit.stat_1202301673@T2` | -0.78312 |
| `explicit.stat_2694482655@T1` | -0.78296 |

### flask.charm — n=12472, R²=-0.5302

intercept: `0.0036`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.61727`  ·  corrupted: `2.30243`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.16584 |
| `explicit.stat_1056492907` | 3.36219 |
| `explicit.stat_828533480@T2` | -2.61728 |
| `explicit.stat_2541588185@T2` | -2.61727 |
| `explicit.stat_828533480@T1` | -2.61727 |
| `explicit.stat_1120862500@T2` | -2.61727 |
| `explicit.stat_2676834156@T2` | -2.61726 |
| `explicit.stat_1873752457@T2` | -2.61726 |
| `explicit.stat_3196823591@T2` | -2.61726 |
| `explicit.stat_1873752457@T1` | -2.61725 |
| `explicit.stat_388617051@T2` | -2.61725 |
| `explicit.stat_1366840608@T2` | -2.61725 |

### weapon.warstaff — n=8378, R²=-0.5019

intercept: `-5.2989`  ·  log_price: True  ·  ilvl: `0.07260`  ·  n_mods: `-0.14391`  ·  n_top_tier: `0.56956`  ·  corrupted: `0.20556`  ·  n_sockets: `0.10406`  ·  quality: `0.05501`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.42500 |
| `explicit.stat_1037193709@T1` | 1.11532 |
| `explicit.stat_328541901@T1` | -1.01171 |
| `explicit.stat_328541901@T2` | -0.97366 |
| `explicit.stat_55876295@T2` | -0.76427 |
| `explicit.stat_1037193709@T2` | -0.70343 |
| `desecrated.stat_9187492` | 0.66664 |
| `explicit.stat_55876295@T1` | -0.61950 |
| `explicit.stat_791928121@T2` | -0.59126 |
| `explicit.stat_3695891184@T2` | -0.57718 |
| `explicit.stat_1368271171@T1` | -0.56172 |
| `explicit.stat_691932474@T2` | -0.55863 |

### weapon.staff — n=7796, R²=-0.5036

intercept: `-8.1846`  ·  log_price: True  ·  ilvl: `0.10609`  ·  n_mods: `-0.09739`  ·  n_top_tier: `0.46901`  ·  corrupted: `-0.01067`  ·  n_sockets: `0.19638`  ·  quality: `0.04344`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.45823 |
| `explicit.stat_4226189338@T1` | 1.41620 |
| `explicit.stat_1545858329@T1` | 1.37540 |
| `explicit.stat_1600707273@T1` | 1.12523 |
| `explicit.stat_2768835289@T2` | 0.95428 |
| `explicit.stat_124131830@T2` | 0.90397 |
| `explicit.stat_2254480358@T1` | 0.86892 |
| `explicit.stat_4226189338@T2` | 0.85687 |
| `explicit.stat_293638271@T2` | -0.73871 |
| `explicit.stat_1263695895@T2` | -0.67573 |
| `explicit.stat_1050105434@T2` | -0.57818 |
| `explicit.stat_274716455@T1` | -0.56669 |

### weapon.sceptre — n=7759, R²=-0.4282

intercept: `-14.1429`  ·  log_price: True  ·  ilvl: `0.17856`  ·  n_mods: `-0.02875`  ·  n_top_tier: `0.43223`  ·  corrupted: `0.43051`  ·  n_sockets: `0.20675`  ·  quality: `0.06945`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.24866 |
| `explicit.stat_2162097452@T2` | 1.41907 |
| `explicit.stat_1263695895@T2` | -0.79420 |
| `explicit.stat_1574590649@T2` | -0.78424 |
| `explicit.stat_2347036682@T1` | 0.75857 |
| `explicit.stat_1250712710@T2` | 0.71391 |
| `explicit.stat_2347036682@T2` | -0.70294 |
| `explicit.stat_289128254@T2` | -0.70074 |
| `explicit.stat_3057012405@T1` | 0.66542 |
| `explicit.stat_4080418644@T1` | -0.64902 |
| `explicit.stat_2854751904@T2` | -0.63883 |
| `explicit.stat_1263695895@T1` | -0.63416 |

### weapon.spear — n=6433, R²=-0.5576

intercept: `-7.0518`  ·  log_price: True  ·  ilvl: `0.09436`  ·  n_mods: `-0.04181`  ·  n_top_tier: `0.70881`  ·  corrupted: `-0.16910`  ·  n_sockets: `0.18139`  ·  quality: `0.10366`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -2.80318 |
| `explicit.stat_1202301673@T1` | 1.99271 |
| `explicit.stat_9187492@T1` | 1.78023 |
| `desecrated.stat_210067635@T1` | -1.07894 |
| `crafted.stat_3035140377` | 1.05944 |
| `explicit.stat_1509134228@T1` | 1.03622 |
| `explicit.stat_1263695895@T2` | -0.98535 |
| `explicit.stat_55876295@T1` | -0.89608 |
| `explicit.stat_1037193709@T1` | -0.82531 |
| `explicit.stat_55876295@T2` | -0.79677 |
| `explicit.stat_1940865751@T2` | -0.75013 |
| `explicit.stat_3261801346@T2` | -0.71750 |

### armour.focus — n=5235, R²=-0.4489

intercept: `-10.7899`  ·  log_price: True  ·  ilvl: `0.13555`  ·  n_mods: `-0.08522`  ·  n_top_tier: `0.89072`  ·  corrupted: `0.61634`  ·  n_sockets: `0.41821`  ·  quality: `0.06983`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -2.01234 |
| `crafted.stat_2974417149@T1` | 1.53970 |
| `explicit.stat_4220027924@T2` | -1.30711 |
| `explicit.stat_3962278098@T2` | -1.08100 |
| `explicit.stat_3962278098@T1` | -1.04113 |
| `explicit.stat_2339757871@T1` | -1.02083 |
| `explicit.stat_2339757871@T2` | -1.01110 |
| `explicit.stat_3291658075@T1` | -0.98777 |
| `explicit.stat_736967255@T2` | -0.97627 |
| `explicit.stat_737908626@T2` | -0.96237 |
| `explicit.stat_2974417149@T1` | -0.95978 |
| `explicit.stat_2923486259@T1` | -0.92488 |

### armour.quiver — n=4885, R²=-0.3882

intercept: `-10.3339`  ·  log_price: True  ·  ilvl: `0.12980`  ·  n_mods: `-0.07529`  ·  n_top_tier: `0.73995`  ·  corrupted: `0.50030`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 7.08005 |
| `explicit.stat_2463230181@T1` | 1.75318 |
| `explicit.stat_2321178454@T2` | -1.17285 |
| `explicit.stat_4067062424@T1` | -1.10536 |
| `explicit.stat_681332047@T2` | -0.99543 |
| `explicit.stat_803737631@T2` | -0.98530 |
| `explicit.stat_1573130764@T2` | -0.89374 |
| `explicit.stat_2463230181@T2` | 0.88257 |
| `explicit.stat_1573130764@T1` | -0.85360 |
| `explicit.stat_3261801346@T1` | -0.79020 |
| `explicit.stat_2194114101@T2` | -0.76356 |
| `explicit.stat_803737631@T1` | -0.71004 |

### armour.shield — n=4284, R²=-0.5717

intercept: `-7.3449`  ·  log_price: True  ·  ilvl: `0.09536`  ·  n_mods: `-0.05320`  ·  n_top_tier: `0.45384`  ·  corrupted: `-0.00234`  ·  n_sockets: `0.08224`  ·  quality: `0.06144`

| stat_id | coef |
|---|---|
| `explicit.stat_3676141501@T1` | 1.04467 |
| `explicit.stat_1301765461@T1` | 0.87124 |
| `explicit.stat_2339757871@T1` | -0.83887 |
| `explicit.stat_2923486259@T2` | -0.81705 |
| `explicit.stat_2481353198@T2` | -0.79679 |
| `explicit.stat_2481353198@T1` | -0.75723 |
| `explicit.stat_328541901@T1` | -0.73951 |
| `explicit.stat_1011760251@T2` | -0.71141 |
| `explicit.stat_1978899297@T2` | -0.71120 |
| `explicit.stat_1011760251@T1` | -0.70845 |
| `explicit.stat_2881298780@T1` | -0.70024 |
| `explicit.stat_3321629045@T2` | -0.65579 |

### weapon.twomace — n=3945, R²=-0.5229

intercept: `-8.9348`  ·  log_price: True  ·  ilvl: `0.11791`  ·  n_mods: `-0.12386`  ·  n_top_tier: `0.50744`  ·  corrupted: `0.69739`  ·  n_sockets: `0.15598`  ·  quality: `0.03611`

| stat_id | coef |
|---|---|
| `desecrated.stat_1509134228@T1` | 2.25071 |
| `desecrated.stat_210067635@T1` | -2.13898 |
| `explicit.stat_1037193709@T1` | -1.69229 |
| `explicit.stat_3336890334@T1` | -1.31016 |
| `crafted.stat_3035140377` | 1.12504 |
| `explicit.stat_518292764@T2` | -0.95106 |
| `explicit.stat_387439868@T2` | -0.89091 |
| `explicit.stat_1263695895@T1` | -0.87984 |
| `explicit.stat_1037193709@T2` | -0.85179 |
| `explicit.stat_1263695895@T2` | -0.84929 |
| `explicit.stat_3639275092@T1` | -0.74753 |
| `explicit.stat_3695891184@T1` | -0.67160 |

## Coverage (listings per base)

- … **Sapphire** — 22711 listings (22680 priced) [0.3–7553463.8 ex]
- … **Emerald** — 22395 listings (22366 priced) [0.3–7553463.8 ex]
- … **Ruby** — 17135 listings (17120 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 9323 listings (9314 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 7624 listings (7614 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 7469 listings (7456 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 7331 listings (7324 priced) [0.2–19945827.9 ex]
- … **Gold Amulet** — 6994 listings (6984 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 6928 listings (6924 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 6854 listings (6842 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5794 listings (5778 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5705 listings (5699 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 5473 listings (5468 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5448 listings (5445 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 4948 listings (4933 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 4879 listings (4874 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4790 listings (4779 priced) [0.6–398912568423.8 ex]
- … **Jade Amulet** — 4749 listings (4743 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 4741 listings (4738 priced) [0.3–3985176410.3 ex]
- … **Unset Ring** — 4705 listings (4698 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4578 listings (4573 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 4429 listings (4423 priced) [0.2–275252424.7 ex]
- … **Heavy Belt** — 4427 listings (4424 priced) [0.3–398912568423.8 ex]
- … **Obliterator Bow** — 4396 listings (4383 priced) [0.3–42622633798.0 ex]
- … **Azure Amulet** — 4337 listings (4337 priced) [0.3–123132003.2 ex]

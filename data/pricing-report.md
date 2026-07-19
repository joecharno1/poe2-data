# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-19T02:15:14+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **636602** (634654 priced in exalted)
- Distinct bases: 994 · distinct mods: 3263 · mod rows: 3015139
- Sold signals: **24776** sold · 362187 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-19T02:02:53+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×21.89** (median |log error| 3.0859)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×66.20 · ±30% 5% · n=92863
- Premium segment (60ex+): skill **+0.14** · typical error ×316.37 · ±30% 0% · n=62917

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 13376 | ×50.50 | 21% | +0.03 | +0.05 |
| jewel | 12647 | ×10.73 | 4% | +0.09 | +0.12 |
| accessory.amulet | 12144 | ×33.34 | 18% | +0.04 | +0.04 |
| accessory.belt | 8793 | ×20.03 | 13% | +0.08 | +0.10 |
| armour.chest | 8550 | ×17.12 | 22% | +0.08 | +0.09 |
| armour.helmet | 8332 | ×24.33 | 17% | +0.08 | +0.10 |
| armour.boots | 7749 | ×31.31 | 21% | +0.08 | +0.11 |
| armour.gloves | 7620 | ×38.99 | 17% | +0.07 | +0.09 |
| other | 7473 | ×1.96 | 43% | +0.10 | +0.18 |
| weapon.wand | 4579 | ×45.97 | 16% | +0.09 | +0.11 |
| weapon.bow | 3609 | ×30.64 | 14% | +0.13 | +0.13 |
| weapon.crossbow | 3387 | ×33.16 | 17% | +0.09 | +0.14 |
| weapon.warstaff | 2275 | ×22.35 | 6% | +0.20 | +0.20 |
| weapon.staff | 2151 | ×29.36 | 5% | +0.16 | +0.15 |
| weapon.sceptre | 2101 | ×27.36 | 5% | +0.13 | +0.13 |
| weapon.spear | 1681 | ×26.66 | 8% | +0.12 | +0.13 |
| armour.focus | 1410 | ×17.93 | 7% | +0.11 | +0.12 |
| armour.quiver | 1339 | ×23.86 | 8% | +0.16 | +0.18 |
| armour.shield | 1106 | ×17.73 | 9% | +0.08 | +0.10 |
| flask.charm | 1078 | ×15.00 | 31% | -0.00 | +0.02 |
| weapon.twomace | 1008 | ×7.32 | 9% | +0.10 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=68683, R²=-0.9511

intercept: `-1.9275`  ·  log_price: True  ·  ilvl: `0.02608`  ·  n_mods: `0.86378`  ·  n_top_tier: `-0.32786`  ·  corrupted: `0.28520`  ·  quality: `-0.00551`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.22412 |
| `explicit.stat_3374165039@T1` | -2.21404 |
| `explicit.stat_3485067555@T1` | 2.01828 |
| `explicit.stat_3780644166@T1` | -1.96329 |
| `explicit.stat_2523933828@T1` | -1.72673 |
| `explicit.stat_4147897060@T1` | -1.62384 |
| `explicit.stat_318953428@T1` | -1.59688 |
| `explicit.stat_1697447343@T1` | -1.37550 |
| `explicit.stat_3174700878@T1` | 1.34262 |
| `explicit.stat_1805182458@T1` | -1.32852 |
| `explicit.stat_3787460122@T1` | 1.31198 |
| `explicit.stat_686254215@T1` | -1.30555 |

### accessory.ring — n=60921, R²=-2.0254

intercept: `3.4921`  ·  log_price: True  ·  ilvl: `-0.04315`  ·  n_mods: `-0.00025`  ·  n_top_tier: `1.11185`  ·  corrupted: `0.01923`  ·  n_sockets: `0.31614`  ·  quality: `0.02337`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.16862 |
| `explicit.stat_1573130764@T2` | -1.16124 |
| `explicit.stat_2231156303@T1` | -1.14663 |
| `explicit.stat_803737631@T1` | -1.13899 |
| `explicit.stat_4220027924@T2` | -1.13640 |
| `explicit.stat_789117908@T2` | -1.12918 |
| `explicit.stat_3325883026@T1` | -1.12859 |
| `explicit.stat_2144192055@T1` | -1.12664 |
| `explicit.stat_4080418644@T1` | -1.12641 |
| `explicit.stat_3032590688@T2` | -1.12628 |
| `explicit.stat_2923486259@T2` | -1.12487 |
| `explicit.stat_789117908@T1` | -1.12165 |

### other — n=60750, R²=-0.6261

intercept: `1.6093`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00081`  ·  n_top_tier: `0.34577`  ·  corrupted: `0.23606`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.40818 |
| `explicit.stat_3299347043@T1` | -0.23336 |
| `implicit.stat_2219129443` | 0.23017 |
| `implicit.stat_3879011313` | 0.23017 |
| `implicit.stat_4041853756` | 0.23017 |
| `explicit.stat_2968503605@T1` | -0.12333 |
| `explicit.stat_2974417149@T1` | 0.10573 |
| `explicit.stat_3291658075@T1` | -0.08669 |
| `explicit.stat_789117908@T1` | -0.07181 |
| `explicit.stat_2106365538@T1` | -0.06632 |
| `explicit.stat_736967255@T1` | -0.06256 |
| `implicit.stat_2901986750` | -0.05437 |

### accessory.amulet — n=55254, R²=-2.15

intercept: `3.7713`  ·  log_price: True  ·  ilvl: `-0.04585`  ·  n_mods: `-0.02621`  ·  n_top_tier: `1.16969`  ·  corrupted: `0.05158`  ·  n_sockets: `-0.18158`  ·  quality: `-0.00244`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.77060 |
| `explicit.stat_3299347043@T2` | -1.52305 |
| `explicit.stat_2974417149@T1` | -1.28934 |
| `explicit.stat_587431675@T2` | -1.27113 |
| `explicit.stat_803737631@T1` | -1.25116 |
| `explicit.stat_2974417149@T2` | -1.24599 |
| `explicit.stat_2866361420@T2` | -1.24030 |
| `explicit.stat_2866361420@T1` | -1.23856 |
| `explicit.stat_803737631@T2` | -1.22900 |
| `explicit.stat_1050105434@T2` | -1.22398 |
| `explicit.stat_472520716@T2` | -1.21998 |
| `explicit.stat_1671376347@T2` | -1.20263 |

### accessory.belt — n=40535, R²=-1.4655

intercept: `4.7745`  ·  log_price: True  ·  ilvl: `-0.05558`  ·  n_mods: `-0.05542`  ·  n_top_tier: `0.51552`  ·  corrupted: `1.23588`  ·  n_sockets: `0.78924`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.06703 |
| `explicit.stat_3299347043@T1` | -0.97468 |
| `explicit.stat_4220027924@T1` | 0.65384 |
| `explicit.stat_3299347043@T2` | -0.64041 |
| `explicit.stat_2881298780@T1` | -0.61717 |
| `explicit.stat_51994685@T1` | -0.56040 |
| `explicit.stat_4220027924@T2` | -0.55795 |
| `explicit.stat_3325883026@T1` | -0.54201 |
| `explicit.stat_1389754388@T1` | -0.54161 |
| `explicit.stat_1570770415@T2` | -0.53863 |
| `explicit.stat_3372524247@T2` | -0.53214 |
| `explicit.stat_1050105434@T1` | -0.52319 |

### armour.chest — n=40139, R²=-1.7492

intercept: `3.3885`  ·  log_price: True  ·  ilvl: `-0.04184`  ·  n_mods: `-0.01714`  ·  n_top_tier: `0.37216`  ·  corrupted: `0.13606`  ·  n_sockets: `0.02809`  ·  quality: `0.06575`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.68429 |
| `explicit.stat_3981240776@T1` | 0.70241 |
| `explicit.stat_986397080@T2` | -0.43479 |
| `explicit.stat_986397080@T1` | -0.43102 |
| `explicit.stat_915769802@T2` | -0.41004 |
| `explicit.stat_1692879867@T2` | -0.40732 |
| `explicit.stat_4080418644@T1` | -0.40613 |
| `explicit.stat_915769802@T1` | -0.40434 |
| `explicit.stat_2339757871@T2` | -0.40401 |
| `explicit.stat_3484657501@T1` | -0.40344 |
| `explicit.stat_1692879867@T1` | -0.39513 |
| `explicit.stat_3299347043@T2` | -0.39132 |

### armour.helmet — n=39057, R²=-1.684

intercept: `3.3237`  ·  log_price: True  ·  ilvl: `-0.04185`  ·  n_mods: `-0.02354`  ·  n_top_tier: `0.54142`  ·  corrupted: `0.71909`  ·  n_sockets: `0.04251`  ·  quality: `0.06339`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.10024 |
| `crafted.stat_3917489142@T1` | -0.95435 |
| `explicit.stat_3917489142@T2` | -0.86072 |
| `explicit.stat_1263695895@T1` | -0.82785 |
| `explicit.stat_3917489142@T1` | -0.77621 |
| `explicit.stat_1263695895@T2` | -0.70113 |
| `explicit.stat_2162097452@T2` | -0.69855 |
| `explicit.stat_1999113824@T1` | -0.61946 |
| `explicit.stat_803737631@T1` | -0.60603 |
| `explicit.stat_4052037485@T2` | -0.59904 |
| `explicit.stat_803737631@T2` | -0.58574 |
| `explicit.stat_53045048@T1` | -0.58355 |

### armour.boots — n=36330, R²=-1.773

intercept: `3.3164`  ·  log_price: True  ·  ilvl: `-0.04078`  ·  n_mods: `-0.01711`  ·  n_top_tier: `0.63241`  ·  corrupted: `-0.01070`  ·  n_sockets: `0.02252`  ·  quality: `0.06016`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.57377 |
| `crafted.stat_3917489142@T1` | 1.07053 |
| `explicit.stat_2339757871@T1` | -1.04089 |
| `explicit.stat_3299347043@T1` | -0.75852 |
| `explicit.stat_3917489142@T2` | -0.74456 |
| `explicit.stat_2923486259@T2` | -0.68305 |
| `explicit.stat_1062208444@T2` | -0.66612 |
| `explicit.stat_1874553720@T1` | -0.66343 |
| `explicit.stat_3917489142@T1` | -0.66199 |
| `explicit.stat_2160282525@T1` | -0.65754 |
| `explicit.stat_3321629045@T1` | -0.65156 |
| `explicit.stat_3484657501@T2` | -0.64876 |

### armour.gloves — n=35370, R²=-1.7968

intercept: `3.6946`  ·  log_price: True  ·  ilvl: `-0.04700`  ·  n_mods: `-0.01678`  ·  n_top_tier: `0.65611`  ·  corrupted: `-0.00458`  ·  n_sockets: `0.06594`  ·  quality: `0.05280`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 4.84996 |
| `explicit.stat_2923486259@T1` | -1.33291 |
| `rune.stat_201332984` | 1.10016 |
| `explicit.stat_3484657501@T2` | -0.90677 |
| `explicit.stat_1671376347@T1` | 0.90510 |
| `explicit.stat_9187492@T2` | -0.84040 |
| `explicit.stat_2923486259@T2` | -0.81633 |
| `explicit.stat_3321629045@T2` | -0.80852 |
| `explicit.stat_3484657501@T1` | -0.79539 |
| `explicit.stat_803737631@T2` | -0.77800 |
| `explicit.stat_9187492@T1` | 0.77216 |
| `explicit.stat_803737631@T1` | -0.75416 |

### weapon.wand — n=21392, R²=-2.0204

intercept: `3.8155`  ·  log_price: True  ·  ilvl: `-0.04734`  ·  n_mods: `-0.04139`  ·  n_top_tier: `0.31743`  ·  corrupted: `-0.00335`  ·  n_sockets: `0.05426`  ·  quality: `0.02282`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.12009 |
| `rune.stat_124131830` | -2.68139 |
| `explicit.stat_2254480358@T1` | 2.50183 |
| `explicit.stat_124131830@T1` | 2.45559 |
| `explicit.stat_591105508@T1` | 2.03273 |
| `explicit.stat_4226189338@T1` | 2.00382 |
| `explicit.stat_736967255@T2` | 1.76142 |
| `crafted.stat_124131830` | 1.22393 |
| `explicit.stat_2254480358@T2` | 1.08607 |
| `explicit.stat_4226189338@T2` | 1.01866 |
| `explicit.stat_1263695895@T2` | -0.72502 |
| `explicit.stat_1545858329@T2` | 0.71038 |

### flask.charm — n=17424, R²=-0.6109

intercept: `0.0981`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.06132`  ·  corrupted: `1.60581`  ·  quality: `0.00077`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.77901 |
| `explicit.stat_1056492907` | 2.77395 |
| `explicit.stat_3246948616` | 1.09852 |
| `explicit.stat_828533480@T2` | -1.06136 |
| `explicit.stat_1120862500@T2` | -1.06132 |
| `explicit.stat_1873752457@T2` | -1.06132 |
| `explicit.stat_1873752457@T1` | -1.06130 |
| `explicit.stat_388617051@T2` | -1.06129 |
| `explicit.stat_3196823591@T2` | -1.06128 |
| `explicit.stat_828533480@T1` | -1.06128 |
| `explicit.stat_2365392475@T2` | -1.06127 |
| `explicit.stat_2676834156@T2` | -1.06126 |

### weapon.bow — n=17112, R²=-1.91

intercept: `3.8853`  ·  log_price: True  ·  ilvl: `-0.04562`  ·  n_mods: `-0.08213`  ·  n_top_tier: `0.76076`  ·  corrupted: `0.35987`  ·  n_sockets: `0.06155`  ·  quality: `0.03351`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.44381 |
| `desecrated.stat_666077204@T1` | -1.43201 |
| `explicit.stat_1263695895@T1` | -1.26231 |
| `explicit.stat_1263695895@T2` | -1.12069 |
| `explicit.stat_2463230181@T2` | -1.03756 |
| `explicit.stat_1509134228@T1` | -0.90843 |
| `explicit.stat_3695891184@T2` | -0.89226 |
| `explicit.stat_1037193709@T2` | -0.85047 |
| `explicit.stat_3639275092@T1` | -0.84622 |
| `explicit.stat_3695891184@T1` | -0.84161 |
| `explicit.stat_1037193709@T1` | -0.84052 |
| `explicit.stat_3639275092@T2` | -0.83139 |

### weapon.crossbow — n=16044, R²=-1.8834

intercept: `3.8942`  ·  log_price: True  ·  ilvl: `-0.04758`  ·  n_mods: `-0.05180`  ·  n_top_tier: `0.45304`  ·  corrupted: `0.06676`  ·  n_sockets: `0.05332`  ·  quality: `0.02633`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.71701 |
| `explicit.stat_1202301673@T1` | 1.37347 |
| `explicit.stat_1980802737` | 1.31865 |
| `explicit.stat_2250681686@T2` | -1.28591 |
| `explicit.stat_709508406@T1` | 0.96566 |
| `explicit.stat_2250681686` | 0.93792 |
| `explicit.stat_1509134228@T1` | 0.76910 |
| `crafted.stat_3035140377` | 0.73266 |
| `explicit.stat_1263695895@T2` | -0.59725 |
| `explicit.stat_3336890334@T1` | -0.58390 |
| `explicit.stat_3336890334@T2` | -0.58358 |
| `explicit.stat_1509134228@T2` | -0.57401 |

### weapon.warstaff — n=10808, R²=-0.3505

intercept: `-10.2507`  ·  log_price: True  ·  ilvl: `0.13978`  ·  n_mods: `-0.24226`  ·  n_top_tier: `0.32787`  ·  corrupted: `0.41375`  ·  n_sockets: `0.14747`  ·  quality: `0.05832`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 2.29864 |
| `desecrated.stat_2527686725@T1` | 2.29864 |
| `desecrated.stat_473429811@T1` | -2.00616 |
| `desecrated.stat_3291658075@T1` | -2.00616 |
| `crafted.stat_210067635@T2` | 1.26479 |
| `rune.stat_243313994` | 0.88303 |
| `explicit.stat_1037193709@T1` | 0.76686 |
| `explicit.stat_328541901@T2` | -0.75046 |
| `desecrated.stat_9187492` | 0.74348 |
| `explicit.stat_328541901@T1` | -0.74102 |
| `explicit.stat_1368271171@T1` | -0.65098 |
| `explicit.stat_1509134228@T1` | 0.64762 |

### weapon.staff — n=10181, R²=-0.3793

intercept: `-16.0531`  ·  log_price: True  ·  ilvl: `0.20579`  ·  n_mods: `-0.09036`  ·  n_top_tier: `0.54567`  ·  corrupted: `0.59616`  ·  n_sockets: `0.20692`  ·  quality: `0.03436`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.13850 |
| `explicit.stat_591105508@T1` | 2.05346 |
| `explicit.stat_4226189338@T1` | 2.00453 |
| `explicit.stat_293638271@T2` | -1.47465 |
| `explicit.stat_124131830@T1` | 1.17918 |
| `explicit.stat_1600707273@T1` | 1.06470 |
| `explicit.stat_274716455@T1` | -0.77857 |
| `explicit.stat_124131830@T2` | 0.71809 |
| `explicit.stat_3278136794@T1` | -0.70861 |
| `explicit.stat_2254480358@T1` | 0.70292 |
| `explicit.stat_2254480358@T2` | 0.69484 |
| `explicit.stat_473429811@T2` | -0.67500 |

### weapon.sceptre — n=10008, R²=-0.335

intercept: `-19.9135`  ·  log_price: True  ·  ilvl: `0.25634`  ·  n_mods: `0.00357`  ·  n_top_tier: `0.39537`  ·  corrupted: `0.01423`  ·  n_sockets: `0.24538`  ·  quality: `0.03122`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.28651 |
| `explicit.stat_1250712710@T2` | 1.19757 |
| `explicit.stat_2162097452@T2` | 1.16387 |
| `explicit.stat_3057012405@T1` | 1.10058 |
| `explicit.stat_2347036682@T2` | -0.79839 |
| `explicit.stat_2854751904@T2` | -0.78410 |
| `explicit.stat_3639275092@T2` | -0.72920 |
| `explicit.stat_101878827@T1` | 0.65958 |
| `explicit.stat_101878827@T2` | 0.62902 |
| `explicit.stat_1263695895@T2` | -0.60354 |
| `explicit.stat_1798257884@T2` | 0.59116 |
| `explicit.stat_4080418644@T2` | -0.54591 |

### weapon.spear — n=8084, R²=-0.3759

intercept: `-12.3181`  ·  log_price: True  ·  ilvl: `0.17448`  ·  n_mods: `-0.22911`  ·  n_top_tier: `0.72127`  ·  corrupted: `-0.06757`  ·  n_sockets: `0.24037`  ·  quality: `0.07875`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.63191 |
| `explicit.stat_9187492@T1` | 1.48529 |
| `explicit.stat_1202301673@T1` | 1.46642 |
| `explicit.stat_1509134228@T1` | 1.44594 |
| `desecrated.stat_210067635@T1` | -1.22368 |
| `explicit.stat_1940865751@T2` | -1.13761 |
| `explicit.stat_4080418644@T2` | -1.12761 |
| `crafted.stat_3035140377` | 1.01209 |
| `explicit.stat_691932474@T1` | -0.96603 |
| `explicit.stat_691932474@T2` | -0.89260 |
| `explicit.stat_4080418644@T1` | -0.85703 |
| `explicit.stat_3261801346@T1` | -0.82492 |

### armour.focus — n=6617, R²=-0.3346

intercept: `-14.2932`  ·  log_price: True  ·  ilvl: `0.18531`  ·  n_mods: `-0.21927`  ·  n_top_tier: `0.92533`  ·  corrupted: `0.30407`  ·  n_sockets: `0.34154`  ·  quality: `0.04880`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 3.95274 |
| `explicit.stat_2923486259@T1` | -1.55941 |
| `explicit.stat_4220027924@T1` | -1.55574 |
| `explicit.stat_4220027924@T2` | -1.43788 |
| `explicit.stat_3291658075@T1` | -1.28050 |
| `explicit.stat_2231156303@T2` | -1.19069 |
| `explicit.stat_2231156303@T1` | -1.12345 |
| `explicit.stat_2974417149@T1` | -1.12134 |
| `explicit.stat_2974417149@T2` | -1.09373 |
| `explicit.stat_2339757871@T2` | -0.98346 |
| `explicit.stat_4052037485@T2` | -0.93328 |
| `explicit.stat_737908626@T2` | -0.87705 |

### armour.quiver — n=6213, R²=-0.3022

intercept: `-15.5449`  ·  log_price: True  ·  ilvl: `0.18892`  ·  n_mods: `-0.13817`  ·  n_top_tier: `0.80844`  ·  corrupted: `0.75468`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.32987 |
| `explicit.stat_2463230181@T1` | 2.69375 |
| `explicit.stat_1573130764@T1` | -1.31011 |
| `explicit.stat_2463230181@T2` | 1.28411 |
| `explicit.stat_681332047@T2` | -1.28004 |
| `explicit.stat_803737631@T2` | -0.96133 |
| `explicit.stat_1573130764@T2` | -0.94621 |
| `explicit.stat_4067062424@T2` | -0.92061 |
| `explicit.stat_2194114101@T2` | -0.92037 |
| `explicit.stat_803737631@T1` | -0.91343 |
| `explicit.stat_4067062424@T1` | -0.90501 |
| `explicit.stat_2321178454@T2` | -0.85612 |

### armour.shield — n=5353, R²=-0.4604

intercept: `-12.2736`  ·  log_price: True  ·  ilvl: `0.16274`  ·  n_mods: `-0.08102`  ·  n_top_tier: `0.58037`  ·  corrupted: `-0.26834`  ·  n_sockets: `0.33236`  ·  quality: `0.06223`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.49599 |
| `explicit.stat_3484657501@T1` | -1.24800 |
| `explicit.stat_3321629045@T2` | -1.23317 |
| `explicit.stat_3484657501@T2` | -0.98381 |
| `explicit.stat_3855016469@T1` | -0.97945 |
| `explicit.stat_3033371881@T2` | -0.95342 |
| `explicit.stat_4095671657@T1` | -0.94328 |
| `explicit.stat_328541901@T1` | -0.88254 |
| `explicit.stat_2901986750@T1` | -0.85943 |
| `explicit.stat_4095671657@T2` | -0.76088 |
| `explicit.stat_1671376347@T1` | -0.72134 |
| `explicit.stat_2923486259@T2` | -0.71682 |

### weapon.twomace — n=4935, R²=-0.4578

intercept: `-9.8813`  ·  log_price: True  ·  ilvl: `0.13721`  ·  n_mods: `-0.21968`  ·  n_top_tier: `0.27034`  ·  corrupted: `0.30979`  ·  n_sockets: `0.14661`  ·  quality: `0.06195`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.67614 |
| `desecrated.stat_1509134228@T1` | 1.79237 |
| `explicit.stat_1037193709@T1` | -1.36907 |
| `explicit.stat_3336890334@T1` | -1.11226 |
| `explicit.stat_709508406@T1` | 0.94912 |
| `explicit.stat_2694482655@T1` | 0.80495 |
| `explicit.stat_9187492@T1` | -0.78070 |
| `explicit.stat_210067635@T2` | 0.75392 |
| `explicit.stat_1509134228@T1` | 0.73238 |
| `explicit.stat_1263695895@T2` | -0.66568 |
| `explicit.stat_387439868@T2` | -0.64582 |
| `explicit.stat_691932474@T1` | -0.63259 |

## Coverage (listings per base)

- … **Sapphire** — 31862 listings (31808 priced) [0.3–885594757.8 ex]
- … **Emerald** — 30981 listings (30940 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 23723 listings (23693 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11537 listings (11522 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10333 listings (10311 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10005 listings (9981 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9866 listings (9856 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 9332 listings (9313 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9214 listings (9194 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8872 listings (8859 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7670 listings (7656 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7394 listings (7386 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7274 listings (7267 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6860 listings (6839 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6416 listings (6409 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 6325 listings (6297 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 6310 listings (6293 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6305 listings (6293 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6280 listings (6273 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6209 listings (6182 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6117 listings (6108 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 6050 listings (6043 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5748 listings (5745 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5682 listings (5669 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5595 listings (5586 priced) [0.3–398912568423.8 ex]

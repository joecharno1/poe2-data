# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-19T22:30:22+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **664749** (662669 priced in exalted)
- Distinct bases: 996 · distinct mods: 3289 · mod rows: 3147906
- Sold signals: **24510** sold · 378554 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-19T22:17:27+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×20.37** (median |log error| 3.0142)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.16** · typical error ×57.05 · ±30% 5% · n=96926
- Premium segment (60ex+): skill **+0.15** · typical error ×276.66 · ±30% 0% · n=65243

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 14037 | ×55.61 | 21% | +0.03 | +0.06 |
| jewel | 13382 | ×10.23 | 5% | +0.11 | +0.12 |
| accessory.amulet | 12657 | ×35.90 | 18% | +0.04 | +0.04 |
| accessory.belt | 9181 | ×16.07 | 6% | +0.06 | +0.08 |
| armour.chest | 8896 | ×16.03 | 20% | +0.08 | +0.10 |
| armour.helmet | 8679 | ×20.84 | 14% | +0.09 | +0.10 |
| armour.boots | 8011 | ×25.76 | 20% | +0.10 | +0.12 |
| armour.gloves | 7885 | ×33.79 | 15% | +0.08 | +0.11 |
| other | 7769 | ×2.00 | 43% | +0.10 | +0.17 |
| weapon.wand | 4734 | ×44.14 | 15% | +0.09 | +0.11 |
| weapon.bow | 3709 | ×26.84 | 11% | +0.15 | +0.17 |
| weapon.crossbow | 3513 | ×29.62 | 16% | +0.11 | +0.13 |
| weapon.warstaff | 2392 | ×17.33 | 7% | +0.20 | +0.21 |
| weapon.staff | 2254 | ×21.12 | 6% | +0.17 | +0.16 |
| weapon.sceptre | 2243 | ×21.17 | 5% | +0.13 | +0.13 |
| weapon.spear | 1749 | ×18.74 | 7% | +0.12 | +0.13 |
| armour.focus | 1483 | ×19.21 | 6% | +0.11 | +0.12 |
| armour.quiver | 1392 | ×21.19 | 7% | +0.16 | +0.17 |
| flask.charm | 1141 | ×14.25 | 29% | -0.00 | +0.03 |
| armour.shield | 1110 | ×18.58 | 7% | +0.09 | +0.11 |
| weapon.twomace | 1054 | ×8.99 | 8% | +0.11 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=72665, R²=-0.9707

intercept: `-1.9190`  ·  log_price: True  ·  ilvl: `0.02493`  ·  n_mods: `0.91260`  ·  n_top_tier: `-0.35577`  ·  corrupted: `0.31206`  ·  quality: `-0.00389`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.56428 |
| `explicit.stat_3485067555@T1` | 2.48606 |
| `explicit.stat_3374165039@T1` | -1.92251 |
| `explicit.stat_1594812856@T1` | 1.76912 |
| `explicit.stat_1569101201@T1` | -1.68886 |
| `explicit.stat_2523933828@T1` | -1.53920 |
| `explicit.stat_4147897060@T1` | -1.51703 |
| `explicit.stat_3473929743@T1` | -1.31466 |
| `explicit.stat_3780644166@T1` | -1.25186 |
| `explicit.stat_1697447343@T1` | -1.22837 |
| `explicit.stat_3824372849@T1` | -1.22547 |
| `explicit.stat_2301718443@T1` | 1.22544 |

### accessory.ring — n=64009, R²=-2.0337

intercept: `3.2963`  ·  log_price: True  ·  ilvl: `-0.04086`  ·  n_mods: `0.00082`  ·  n_top_tier: `1.16795`  ·  corrupted: `0.01225`  ·  n_sockets: `1.88234`  ·  quality: `0.02539`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.20192 |
| `explicit.stat_1573130764@T2` | -1.19260 |
| `explicit.stat_803737631@T1` | -1.19064 |
| `explicit.stat_4220027924@T2` | -1.18936 |
| `explicit.stat_2231156303@T1` | -1.18868 |
| `explicit.stat_4080418644@T1` | -1.18397 |
| `explicit.stat_789117908@T2` | -1.17846 |
| `explicit.stat_789117908@T1` | -1.17821 |
| `explicit.stat_736967255@T2` | -1.17799 |
| `explicit.stat_2891184298@T1` | -1.17660 |
| `explicit.stat_3261801346@T1` | -1.17545 |
| `explicit.stat_2923486259@T2` | -1.17518 |

### other — n=63265, R²=-0.6344

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00105`  ·  n_top_tier: `0.34562`  ·  corrupted: `0.25235`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_2219129443` | 0.41656 |
| `explicit.stat_1050105434@T1` | -0.38346 |
| `explicit.stat_3299347043@T1` | -0.28668 |
| `implicit.stat_3879011313` | 0.26187 |
| `explicit.stat_2974417149@T1` | 0.13399 |
| `explicit.stat_736967255@T1` | -0.09396 |
| `explicit.stat_789117908@T1` | -0.07525 |
| `explicit.stat_3291658075@T1` | -0.07412 |
| `explicit.stat_2106365538@T1` | -0.06029 |
| `implicit.stat_2901986750` | -0.05998 |
| `implicit.stat_1379411836` | -0.05934 |
| `pseudo.total_ele_res>=40` | -0.05155 |

### accessory.amulet — n=57833, R²=-2.1492

intercept: `3.5392`  ·  log_price: True  ·  ilvl: `-0.04387`  ·  n_mods: `-0.01929`  ·  n_top_tier: `1.42519`  ·  corrupted: `0.05551`  ·  n_sockets: `-0.13146`  ·  quality: `0.03009`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -2.07600 |
| `explicit.stat_3299347043@T2` | -1.86509 |
| `explicit.stat_587431675@T2` | -1.59128 |
| `explicit.stat_803737631@T1` | -1.51966 |
| `explicit.stat_2974417149@T1` | -1.51148 |
| `explicit.stat_2866361420@T2` | -1.49855 |
| `explicit.stat_1050105434@T2` | -1.48184 |
| `explicit.stat_2866361420@T1` | -1.47731 |
| `explicit.stat_803737631@T2` | -1.46927 |
| `explicit.stat_2748665614@T1` | -1.46610 |
| `explicit.stat_1671376347@T2` | -1.46277 |
| `explicit.stat_2974417149@T2` | -1.45903 |

### accessory.belt — n=42087, R²=-1.1707

intercept: `6.1040`  ·  log_price: True  ·  ilvl: `-0.06217`  ·  n_mods: `-0.20202`  ·  n_top_tier: `0.65475`  ·  corrupted: `0.92547`  ·  n_sockets: `0.66934`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.26598 |
| `implicit.stat_731781020` | -1.11966 |
| `explicit.stat_3299347043@T2` | -0.95878 |
| `explicit.stat_2881298780@T1` | -0.88407 |
| `explicit.stat_1570770415@T2` | -0.78965 |
| `explicit.stat_51994685@T1` | -0.78403 |
| `explicit.stat_4220027924@T2` | -0.77998 |
| `explicit.stat_1570770415@T1` | -0.71995 |
| `explicit.stat_3372524247@T2` | -0.71726 |
| `explicit.stat_644456512@T1` | -0.67250 |
| `explicit.stat_4080418644@T2` | -0.66958 |
| `explicit.stat_1389754388@T1` | -0.66604 |

### armour.chest — n=41712, R²=-1.6887

intercept: `3.5243`  ·  log_price: True  ·  ilvl: `-0.04326`  ·  n_mods: `-0.02346`  ·  n_top_tier: `0.40134`  ·  corrupted: `0.14732`  ·  n_sockets: `0.02652`  ·  quality: `0.06970`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.71925 |
| `explicit.stat_3981240776@T1` | 0.98985 |
| `explicit.stat_986397080@T2` | -0.54960 |
| `explicit.stat_986397080@T1` | -0.52760 |
| `explicit.stat_2339757871@T2` | -0.49726 |
| `explicit.stat_1692879867@T2` | -0.46387 |
| `explicit.stat_3484657501@T1` | -0.46256 |
| `explicit.stat_3033371881@T1` | 0.45932 |
| `explicit.stat_2339757871@T1` | -0.45223 |
| `explicit.stat_4080418644@T1` | -0.44472 |
| `explicit.stat_915769802@T2` | -0.44304 |
| `explicit.stat_4080418644@T2` | -0.44217 |

### armour.helmet — n=40578, R²=-1.5552

intercept: `3.4365`  ·  log_price: True  ·  ilvl: `-0.04335`  ·  n_mods: `-0.03251`  ·  n_top_tier: `0.48881`  ·  corrupted: `0.68657`  ·  n_sockets: `0.08002`  ·  quality: `0.06198`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.63007 |
| `explicit.stat_3917489142@T2` | -0.88054 |
| `explicit.stat_1263695895@T1` | -0.79564 |
| `explicit.stat_3917489142@T1` | -0.77460 |
| `explicit.stat_2162097452@T2` | -0.68691 |
| `explicit.stat_1263695895@T2` | -0.61151 |
| `explicit.stat_1999113824@T1` | -0.58568 |
| `explicit.stat_803737631@T1` | -0.55729 |
| `explicit.stat_2923486259@T1` | 0.55601 |
| `explicit.stat_3321629045@T2` | -0.55277 |
| `explicit.stat_1999113824@T2` | -0.54087 |
| `explicit.stat_53045048@T1` | -0.54032 |

### armour.boots — n=37712, R²=-1.7055

intercept: `3.5569`  ·  log_price: True  ·  ilvl: `-0.04383`  ·  n_mods: `-0.02104`  ·  n_top_tier: `0.52557`  ·  corrupted: `0.08030`  ·  n_sockets: `0.03974`  ·  quality: `0.06452`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.70659 |
| `crafted.stat_3917489142@T1` | 1.51705 |
| `explicit.stat_2339757871@T1` | -1.08022 |
| `explicit.stat_2923486259@T1` | 0.73822 |
| `explicit.stat_3917489142@T2` | -0.63631 |
| `explicit.stat_3299347043@T1` | -0.62755 |
| `explicit.stat_2923486259@T2` | -0.61530 |
| `explicit.stat_1874553720@T1` | -0.58194 |
| `explicit.stat_2160282525@T1` | -0.57650 |
| `explicit.stat_1062208444@T2` | -0.57569 |
| `explicit.stat_1999113824@T2` | -0.56491 |
| `explicit.stat_3321629045@T1` | -0.55906 |

### armour.gloves — n=36662, R²=-1.6698

intercept: `3.7831`  ·  log_price: True  ·  ilvl: `-0.04912`  ·  n_mods: `-0.01369`  ·  n_top_tier: `0.68106`  ·  corrupted: `-0.00293`  ·  n_sockets: `0.12119`  ·  quality: `0.05636`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 6.18677 |
| `explicit.stat_2923486259@T1` | -1.18047 |
| `explicit.stat_3484657501@T2` | -0.94485 |
| `explicit.stat_3321629045@T2` | -0.90811 |
| `explicit.stat_4015621042@T2` | -0.86001 |
| `explicit.stat_803737631@T2` | -0.85953 |
| `explicit.stat_3484657501@T1` | -0.83936 |
| `rune.stat_201332984` | 0.82902 |
| `explicit.stat_3639275092@T1` | -0.82226 |
| `explicit.stat_4052037485@T1` | -0.82186 |
| `explicit.stat_803737631@T1` | -0.80822 |
| `explicit.stat_9187492@T2` | -0.80821 |

### weapon.wand — n=22104, R²=-1.9816

intercept: `3.9177`  ·  log_price: True  ·  ilvl: `-0.04866`  ·  n_mods: `-0.05312`  ·  n_top_tier: `0.26625`  ·  corrupted: `-0.04960`  ·  n_sockets: `0.04244`  ·  quality: `0.03196`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.05017 |
| `rune.stat_124131830` | -2.86290 |
| `explicit.stat_2254480358@T1` | 2.60947 |
| `explicit.stat_124131830@T1` | 2.30494 |
| `explicit.stat_591105508@T1` | 2.11974 |
| `explicit.stat_4226189338@T1` | 2.08746 |
| `explicit.stat_736967255@T2` | 1.93896 |
| `explicit.stat_2254480358@T2` | 1.30626 |
| `crafted.stat_124131830` | 1.24661 |
| `explicit.stat_1600707273@T1` | 1.20863 |
| `explicit.stat_4226189338@T2` | 1.08573 |
| `explicit.stat_2505884597@T1` | 0.70473 |

### flask.charm — n=18406, R²=-0.6325

intercept: `0.1052`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.37427`  ·  corrupted: `1.59075`  ·  quality: `0.00452`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.61739 |
| `explicit.stat_1056492907` | 2.71300 |
| `explicit.stat_3246948616` | 1.60930 |
| `explicit.stat_828533480@T2` | -1.37430 |
| `explicit.stat_1120862500@T2` | -1.37429 |
| `explicit.stat_1873752457@T2` | -1.37426 |
| `explicit.stat_3196823591@T2` | -1.37422 |
| `explicit.stat_2365392475@T2` | -1.37422 |
| `explicit.stat_388617051@T2` | -1.37422 |
| `explicit.stat_2676834156@T2` | -1.37319 |
| `explicit.stat_828533480@T1` | -1.37195 |
| `explicit.stat_1873752457@T1` | -1.37173 |

### weapon.bow — n=17596, R²=-1.7121

intercept: `3.9308`  ·  log_price: True  ·  ilvl: `-0.04547`  ·  n_mods: `-0.11049`  ·  n_top_tier: `0.65899`  ·  corrupted: `0.47327`  ·  n_sockets: `0.09253`  ·  quality: `0.02947`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.87379 |
| `explicit.stat_3336890334@T1` | 1.26767 |
| `crafted.stat_3035140377` | 1.25140 |
| `explicit.stat_1263695895@T1` | -1.03320 |
| `explicit.stat_2463230181@T2` | -0.95113 |
| `explicit.stat_1263695895@T2` | -0.94707 |
| `explicit.stat_709508406@T1` | 0.89672 |
| `explicit.stat_3695891184@T2` | -0.80591 |
| `explicit.stat_210067635@T2` | -0.79759 |
| `explicit.stat_3639275092@T1` | -0.77821 |
| `explicit.stat_1368271171@T2` | -0.76697 |
| `explicit.stat_3639275092@T2` | -0.75508 |

### weapon.crossbow — n=16525, R²=-1.8022

intercept: `4.0505`  ·  log_price: True  ·  ilvl: `-0.04941`  ·  n_mods: `-0.06114`  ·  n_top_tier: `0.38027`  ·  corrupted: `0.07087`  ·  n_sockets: `0.08031`  ·  quality: `0.02953`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 1.62015 |
| `explicit.stat_1980802737@T2` | -1.51781 |
| `explicit.stat_2250681686@T2` | -1.35008 |
| `explicit.stat_1980802737` | 1.34115 |
| `explicit.stat_2250681686` | 1.17038 |
| `explicit.stat_709508406@T1` | 0.90223 |
| `crafted.stat_3035140377` | 0.80481 |
| `explicit.stat_1509134228@T1` | 0.73739 |
| `explicit.stat_3336890334@T2` | -0.56244 |
| `explicit.stat_387439868@T1` | 0.56208 |
| `explicit.stat_1263695895@T2` | -0.55190 |
| `explicit.stat_3336890334@T1` | -0.54206 |

### weapon.warstaff — n=11335, R²=-0.3398

intercept: `-11.1534`  ·  log_price: True  ·  ilvl: `0.14903`  ·  n_mods: `-0.19421`  ·  n_top_tier: `0.33432`  ·  corrupted: `0.36561`  ·  n_sockets: `0.15590`  ·  quality: `0.05804`

| stat_id | coef |
|---|---|
| `desecrated.stat_3291658075@T1` | -1.72479 |
| `desecrated.stat_473429811@T1` | -1.72479 |
| `crafted.stat_210067635@T2` | 1.23678 |
| `desecrated.stat_2527686725@T1` | 1.08946 |
| `desecrated.stat_2231156303@T1` | 1.08946 |
| `explicit.stat_328541901@T1` | -0.92606 |
| `explicit.stat_328541901@T2` | -0.83978 |
| `explicit.stat_1368271171@T1` | -0.77773 |
| `desecrated.stat_9187492` | 0.77408 |
| `explicit.stat_1037193709@T1` | 0.76198 |
| `explicit.stat_1509134228@T1` | 0.67777 |
| `explicit.stat_691932474@T2` | -0.67058 |

### weapon.staff — n=10718, R²=-0.372

intercept: `-15.2092`  ·  log_price: True  ·  ilvl: `0.19523`  ·  n_mods: `-0.07567`  ·  n_top_tier: `0.41903`  ·  corrupted: `0.81720`  ·  n_sockets: `0.18810`  ·  quality: `0.03997`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.12659 |
| `explicit.stat_591105508@T1` | 2.10437 |
| `explicit.stat_4226189338@T1` | 2.06022 |
| `explicit.stat_2254480358@T1` | 1.28245 |
| `explicit.stat_124131830@T1` | 1.17602 |
| `explicit.stat_1600707273@T1` | 1.13946 |
| `explicit.stat_293638271@T2` | -1.11958 |
| `explicit.stat_2254480358@T2` | 0.86598 |
| `explicit.stat_3962278098@T2` | 0.81120 |
| `explicit.stat_1263695895@T1` | 0.71810 |
| `explicit.stat_591105508@T2` | 0.66226 |
| `explicit.stat_4226189338@T2` | 0.64737 |

### weapon.sceptre — n=10539, R²=-0.3379

intercept: `-21.3496`  ·  log_price: True  ·  ilvl: `0.27238`  ·  n_mods: `0.03055`  ·  n_top_tier: `0.24834`  ·  corrupted: `0.04466`  ·  n_sockets: `0.20170`  ·  quality: `0.02743`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.28384 |
| `explicit.stat_3057012405@T1` | 1.42595 |
| `explicit.stat_1263695895@T2` | -1.09842 |
| `explicit.stat_2162097452@T2` | 1.06214 |
| `explicit.stat_1263695895@T1` | -0.91349 |
| `explicit.stat_1798257884@T2` | 0.81644 |
| `explicit.stat_1250712710@T2` | 0.74061 |
| `explicit.stat_2854751904@T2` | -0.73170 |
| `explicit.stat_101878827@T1` | 0.71984 |
| `explicit.stat_101878827@T2` | 0.71777 |
| `explicit.stat_849987426@T1` | 0.60952 |
| `explicit.stat_289128254@T1` | 0.54028 |

### weapon.spear — n=8496, R²=-0.3711

intercept: `-13.8585`  ·  log_price: True  ·  ilvl: `0.19037`  ·  n_mods: `-0.16335`  ·  n_top_tier: `0.68174`  ·  corrupted: `-0.34489`  ·  n_sockets: `0.22684`  ·  quality: `0.07167`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.72847 |
| `explicit.stat_1202301673@T1` | 1.49004 |
| `explicit.stat_1509134228@T1` | 1.36922 |
| `explicit.stat_4080418644@T2` | -1.05823 |
| `explicit.stat_1940865751@T2` | -1.05318 |
| `explicit.stat_691932474@T1` | -0.99447 |
| `explicit.stat_9187492@T1` | 0.97762 |
| `explicit.stat_691932474@T2` | -0.90147 |
| `explicit.stat_3336890334@T2` | -0.86473 |
| `explicit.stat_748522257@T2` | -0.78876 |
| `crafted.stat_3035140377` | 0.78110 |
| `explicit.stat_3261801346@T1` | -0.75066 |

### armour.focus — n=6936, R²=-0.3382

intercept: `-15.7253`  ·  log_price: True  ·  ilvl: `0.20046`  ·  n_mods: `-0.17777`  ·  n_top_tier: `0.93245`  ·  corrupted: `0.16302`  ·  n_sockets: `0.24564`  ·  quality: `0.05097`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 2.34474 |
| `crafted.stat_737908626@T2` | 2.25018 |
| `explicit.stat_2923486259@T1` | -1.78770 |
| `explicit.stat_4220027924@T1` | -1.51991 |
| `explicit.stat_4220027924@T2` | -1.34460 |
| `explicit.stat_2231156303@T1` | -1.33859 |
| `explicit.stat_2231156303@T2` | -1.24591 |
| `explicit.stat_274716455@T2` | -1.18623 |
| `explicit.stat_2923486259@T2` | -1.06010 |
| `explicit.stat_2974417149@T1` | -1.04983 |
| `explicit.stat_2339757871@T2` | -1.04729 |
| `explicit.stat_2974417149@T2` | -0.98058 |

### armour.quiver — n=6515, R²=-0.2956

intercept: `-16.4391`  ·  log_price: True  ·  ilvl: `0.20241`  ·  n_mods: `-0.11561`  ·  n_top_tier: `0.82404`  ·  corrupted: `0.85672`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.02491 |
| `explicit.stat_2463230181@T1` | 1.68425 |
| `explicit.stat_681332047@T2` | -1.43371 |
| `explicit.stat_1573130764@T1` | -1.35353 |
| `explicit.stat_681332047@T1` | -1.20475 |
| `explicit.stat_1573130764@T2` | -1.19670 |
| `explicit.stat_4067062424@T1` | -1.05184 |
| `explicit.stat_803737631@T1` | -0.97638 |
| `explicit.stat_2463230181@T2` | 0.94893 |
| `explicit.stat_2321178454@T2` | -0.90473 |
| `explicit.stat_803737631@T2` | -0.90311 |
| `explicit.stat_4067062424@T2` | -0.82015 |

### armour.shield — n=5581, R²=-0.4195

intercept: `-13.3520`  ·  log_price: True  ·  ilvl: `0.17645`  ·  n_mods: `-0.11958`  ·  n_top_tier: `0.67598`  ·  corrupted: `-0.37863`  ·  n_sockets: `0.38929`  ·  quality: `0.06152`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.84699 |
| `explicit.stat_3321629045@T2` | -1.19488 |
| `explicit.stat_2901986750@T1` | -1.06631 |
| `explicit.stat_3484657501@T1` | -1.06043 |
| `explicit.stat_3855016469@T1` | -1.05518 |
| `explicit.stat_328541901@T1` | -0.98870 |
| `explicit.stat_3033371881@T2` | -0.98809 |
| `explicit.stat_2451402625@T1` | -0.96002 |
| `explicit.stat_4095671657@T2` | -0.93117 |
| `explicit.stat_3484657501@T2` | -0.92231 |
| `explicit.stat_4220027924@T1` | -0.89121 |
| `explicit.stat_2339757871@T2` | -0.87022 |

### weapon.twomace — n=5149, R²=-0.4452

intercept: `-10.8564`  ·  log_price: True  ·  ilvl: `0.14792`  ·  n_mods: `-0.22139`  ·  n_top_tier: `0.38013`  ·  corrupted: `0.62910`  ·  n_sockets: `0.15284`  ·  quality: `0.06238`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.41088 |
| `explicit.stat_1037193709@T1` | -1.78498 |
| `explicit.stat_3336890334@T1` | -1.24259 |
| `explicit.stat_1263695895@T2` | -1.12980 |
| `explicit.stat_2694482655@T1` | 0.90966 |
| `explicit.stat_9187492@T1` | -0.88586 |
| `explicit.stat_691932474@T1` | -0.79638 |
| `explicit.stat_387439868@T2` | -0.74647 |
| `explicit.stat_518292764@T1` | 0.71235 |
| `explicit.stat_3695891184@T1` | -0.64183 |
| `explicit.stat_3695891184@T2` | -0.61284 |
| `explicit.stat_210067635@T2` | 0.59626 |

## Coverage (listings per base)

- … **Sapphire** — 33505 listings (33450 priced) [0.3–3985176410.3 ex]
- … **Emerald** — 32668 listings (32627 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 25092 listings (25062 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 12024 listings (12006 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10813 listings (10789 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10468 listings (10444 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 10351 listings (10340 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 9759 listings (9737 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9680 listings (9658 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 9255 listings (9242 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8023 listings (8008 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7728 listings (7719 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7624 listings (7615 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 7106 listings (7084 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6686 listings (6679 priced) [0.3–19945827.9 ex]
- … **Jade Amulet** — 6608 listings (6594 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 6602 listings (6583 priced) [0.2–39887666593.4 ex]
- … **Plate Belt** — 6576 listings (6548 priced) [0.3–398912568423.8 ex]
- … **Amber Amulet** — 6556 listings (6549 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6463 listings (6434 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6366 listings (6358 priced) [0.2–275252424.7 ex]
- … **Bloodstone Amulet** — 6356 listings (6346 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6046 listings (6043 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5944 listings (5930 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5817 listings (5807 priced) [0.3–398912568423.8 ex]

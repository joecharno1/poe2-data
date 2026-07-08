# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-08T00:36:30+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **303335** (302973 priced in exalted)
- Distinct bases: 953 · distinct mods: 2795 · mod rows: 1440359
- Sold signals: **31278** sold · 162213 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-08T00:26:04+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×16.52** (median |log error| 2.8047)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 77% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×42.71 · ±30% 12% · n=43882
- Premium segment (60ex+): skill **+0.07** · typical error ×191.66 · ±30% 0% · n=27208

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 5729 | ×11.74 | 4% | +0.04 | +0.05 |
| accessory.amulet | 5431 | ×52.19 | 19% | +0.02 | +0.03 |
| jewel | 4998 | ×8.27 | 8% | +0.00 | +0.03 |
| accessory.belt | 4444 | ×15.28 | 21% | +0.04 | +0.07 |
| armour.chest | 4328 | ×10.00 | 26% | +0.00 | +0.01 |
| armour.helmet | 4267 | ×10.00 | 25% | +0.00 | +0.01 |
| armour.boots | 4027 | ×10.92 | 14% | +0.00 | +0.02 |
| armour.gloves | 3945 | ×9.93 | 21% | +0.00 | +0.01 |
| other | 3701 | ×10.00 | 35% | +0.06 | +0.22 |
| weapon.wand | 2709 | ×31.96 | 22% | +0.05 | +0.05 |
| weapon.bow | 2181 | ×20.10 | 20% | +0.08 | +0.10 |
| weapon.crossbow | 2030 | ×15.30 | 22% | +0.08 | +0.09 |
| weapon.warstaff | 987 | ×74.94 | 17% | +0.02 | +0.02 |
| weapon.sceptre | 899 | ×59.48 | 13% | +0.07 | +0.03 |
| weapon.staff | 897 | ×49.99 | 19% | +0.04 | +0.07 |
| weapon.spear | 745 | ×45.00 | 20% | +0.02 | +0.02 |
| armour.focus | 623 | ×618.93 | 11% | +0.01 | +0.07 |
| armour.quiver | 609 | ×79.79 | 13% | -0.00 | +0.04 |
| armour.shield | 496 | ×30.00 | 17% | +0.02 | +0.03 |
| weapon.twomace | 444 | ×20.00 | 13% | +0.02 | +0.05 |
| flask.charm | 395 | ×3.00 | 46% | -0.00 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=31716, R²=-0.4813

intercept: `1.6040`  ·  log_price: True  ·  ilvl: `0.00007`  ·  n_mods: `0.04630`  ·  n_top_tier: `0.60219`  ·  corrupted: `1.75325`  ·  n_sockets: `-0.00015`  ·  quality: `-0.00002`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.87601 |
| `explicit.stat_2106365538@T1` | 3.66224 |
| `explicit.stat_3141070085@T1` | -1.75359 |
| `explicit.stat_101878827@T1` | 1.67756 |
| `explicit.stat_2891184298@T1` | 1.52314 |
| `explicit.stat_1589917703@T1` | 1.44924 |
| `explicit.stat_1050105434@T1` | -1.18692 |
| `explicit.stat_3917489142@T1` | 1.09106 |
| `explicit.stat_2974417149@T1` | 1.00429 |
| `explicit.stat_789117908@T1` | -0.79598 |
| `explicit.stat_3141070085` | 0.35962 |
| `implicit.stat_1379411836` | -0.27582 |

### jewel — n=26909, R²=-0.6082

intercept: `-1.0102`  ·  log_price: True  ·  ilvl: `0.03622`  ·  n_mods: `0.12518`  ·  n_top_tier: `-0.02149`  ·  corrupted: `0.23642`  ·  quality: `0.21711`

| stat_id | coef |
|---|---|
| `explicit.stat_1569101201@T1` | 4.02529 |
| `explicit.stat_3714003708@T1` | -3.81664 |
| `explicit.stat_3192728503@T1` | -3.26870 |
| `explicit.stat_1316278494@T1` | -2.97721 |
| `explicit.stat_3741323227@T1` | -2.78766 |
| `explicit.stat_1854213750@T1` | -2.74577 |
| `explicit.stat_3668351662@T1` | -2.27651 |
| `explicit.stat_1569159338@T1` | -2.14080 |
| `explicit.stat_153777645@T1` | 2.09379 |
| `explicit.stat_1697951953@T1` | -1.86824 |
| `explicit.stat_4045894391@T1` | -1.75630 |
| `explicit.stat_1062710370@T1` | -1.43722 |

### accessory.ring — n=26281, R²=-1.2199

intercept: `4.1957`  ·  log_price: True  ·  ilvl: `-0.04101`  ·  n_mods: `-0.08099`  ·  n_top_tier: `0.15108`  ·  corrupted: `0.96680`  ·  n_sockets: `-1.26774`  ·  quality: `0.02903`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 3.60360 |
| `explicit.stat_707457662@T2` | 2.62576 |
| `explicit.stat_1379411836@T1` | -2.31151 |
| `explicit.stat_1379411836@T2` | -1.91821 |
| `explicit.stat_1368271171@T2` | -0.93423 |
| `explicit.stat_2231156303@T1` | -0.85095 |
| `explicit.stat_1368271171@T1` | -0.77787 |
| `explicit.stat_2231156303@T2` | -0.76714 |
| `explicit.stat_3695891184@T1` | -0.71454 |
| `explicit.stat_1263695895@T1` | -0.69044 |
| `explicit.stat_3695891184@T2` | -0.67515 |
| `explicit.stat_3291658075@T1` | -0.65489 |

### accessory.amulet — n=24876, R²=-2.093

intercept: `4.1187`  ·  log_price: True  ·  ilvl: `-0.04976`  ·  n_mods: `-0.02946`  ·  n_top_tier: `0.98768`  ·  corrupted: `0.11885`  ·  n_sockets: `1.49315`  ·  quality: `-0.00276`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | -1.18052 |
| `explicit.stat_3299347043@T1` | -1.15147 |
| `explicit.stat_983749596@T1` | -1.12442 |
| `explicit.stat_3917489142@T2` | -1.12286 |
| `explicit.stat_3917489142@T1` | -1.11069 |
| `explicit.stat_3325883026@T1` | -1.10137 |
| `explicit.stat_983749596@T2` | -1.09563 |
| `explicit.stat_587431675@T1` | -1.08105 |
| `explicit.stat_3325883026@T2` | -1.08009 |
| `explicit.stat_472520716@T1` | -1.07381 |
| `explicit.stat_2748665614@T1` | -1.06738 |
| `explicit.stat_3489782002@T2` | -1.06124 |

### accessory.belt — n=20363, R²=-1.4494

intercept: `3.6226`  ·  log_price: True  ·  ilvl: `-0.04316`  ·  n_mods: `-0.02045`  ·  n_top_tier: `0.85831`  ·  corrupted: `0.50996`  ·  n_sockets: `-0.12331`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -0.91858 |
| `explicit.stat_2881298780@T1` | -0.90705 |
| `explicit.stat_809229260@T2` | -0.90570 |
| `explicit.stat_4220027924@T2` | -0.88227 |
| `explicit.stat_51994685@T1` | -0.87708 |
| `explicit.stat_3299347043@T2` | -0.87339 |
| `explicit.stat_1671376347@T2` | -0.87041 |
| `explicit.stat_915769802@T2` | -0.86898 |
| `explicit.stat_3325883026@T1` | -0.86735 |
| `explicit.stat_2881298780@T2` | -0.86529 |
| `explicit.stat_3299347043@T1` | -0.86142 |
| `explicit.stat_1412217137@T2` | -0.85853 |

### armour.chest — n=20124, R²=-0.2416

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.04710`  ·  corrupted: `0.00009`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_915769802@T1` | -0.04715 |
| `explicit.stat_915769802@T2` | -0.04714 |
| `explicit.stat_3261801346@T1` | -0.04714 |
| `explicit.stat_3261801346@T2` | -0.04713 |
| `explicit.stat_4080418644@T2` | -0.04712 |
| `explicit.stat_2451402625@T2` | -0.04712 |
| `explicit.stat_124859000@T2` | -0.04711 |
| `explicit.stat_3321629045@T1` | -0.04711 |
| `explicit.stat_3484657501@T1` | -0.04711 |
| `explicit.stat_4015621042@T1` | -0.04711 |
| `explicit.stat_3325883026@T2` | -0.04711 |
| `explicit.stat_53045048@T2` | -0.04711 |

### armour.helmet — n=19717, R²=-0.2703

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.20264`  ·  corrupted: `1.04805`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 1.18015 |
| `explicit.stat_3362812763@T2` | -0.20267 |
| `explicit.stat_4080418644@T2` | -0.20266 |
| `explicit.stat_53045048@T2` | -0.20266 |
| `explicit.stat_2451402625@T1` | -0.20266 |
| `explicit.stat_1263695895@T1` | -0.20266 |
| `explicit.stat_3362812763@T1` | -0.20266 |
| `explicit.stat_1062208444@T2` | -0.20266 |
| `explicit.stat_1263695895@T2` | -0.20265 |
| `explicit.stat_803737631@T2` | -0.20265 |
| `explicit.stat_53045048@T1` | -0.20265 |
| `explicit.stat_3321629045@T2` | -0.20265 |

### armour.boots — n=18612, R²=-0.3671

intercept: `3.1419`  ·  log_price: True  ·  ilvl: `-0.01911`  ·  n_mods: `-0.09543`  ·  n_top_tier: `0.32036`  ·  corrupted: `0.25908`  ·  n_sockets: `0.06172`  ·  quality: `0.00513`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -0.74235 |
| `explicit.stat_1062208444@T2` | -0.74012 |
| `explicit.stat_2451402625@T2` | -0.54264 |
| `explicit.stat_328541901@T1` | -0.49703 |
| `explicit.stat_3321629045@T1` | -0.47731 |
| `explicit.stat_3321629045@T2` | -0.44467 |
| `desecrated.stat_2250533757@T2` | -0.42846 |
| `explicit.stat_2923486259@T2` | -0.42839 |
| `explicit.stat_1999113824@T1` | -0.41898 |
| `explicit.stat_3917489142@T2` | -0.41864 |
| `explicit.stat_1062208444@T1` | -0.40145 |
| `explicit.stat_3639275092@T1` | -0.39791 |

### armour.gloves — n=18180, R²=-0.3736

intercept: `2.5274`  ·  log_price: True  ·  ilvl: `-0.00921`  ·  n_mods: `-0.04062`  ·  n_top_tier: `0.14542`  ·  corrupted: `0.14801`  ·  n_sockets: `0.06230`  ·  quality: `0.00336`

| stat_id | coef |
|---|---|
| `explicit.stat_53045048@T1` | -0.46950 |
| `explicit.stat_3484657501@T2` | -0.41983 |
| `explicit.stat_803737631@T2` | -0.30859 |
| `explicit.stat_3362812763@T2` | -0.28780 |
| `explicit.stat_3033371881@T2` | -0.27879 |
| `explicit.stat_2797971005@T2` | -0.25496 |
| `explicit.stat_3695891184@T1` | -0.24423 |
| `explicit.stat_3033371881@T1` | -0.23223 |
| `explicit.stat_4080418644@T1` | -0.22395 |
| `explicit.stat_328541901@T1` | -0.22362 |
| `explicit.stat_2451402625@T2` | -0.21520 |
| `explicit.stat_4220027924@T2` | -0.20807 |

### weapon.wand — n=12525, R²=-2.0611

intercept: `3.5757`  ·  log_price: True  ·  ilvl: `-0.04469`  ·  n_mods: `-0.00892`  ·  n_top_tier: `0.66177`  ·  corrupted: `0.04318`  ·  n_sockets: `0.01354`  ·  quality: `0.01439`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 1.82199 |
| `explicit.stat_124131830@T1` | 1.72141 |
| `explicit.stat_4226189338@T1` | 1.71862 |
| `explicit.stat_591105508@T1` | 1.70180 |
| `explicit.stat_1545858329@T1` | 1.67855 |
| `explicit.stat_1600707273@T1` | 1.67092 |
| `explicit.stat_736967255@T2` | 0.88388 |
| `crafted.stat_124131830` | 0.73838 |
| `explicit.stat_737908626@T1` | -0.71639 |
| `explicit.stat_2768835289@T2` | -0.68993 |
| `explicit.stat_473429811@T2` | -0.68573 |
| `explicit.stat_2231156303@T2` | -0.68234 |

### weapon.bow — n=10232, R²=-1.9503

intercept: `3.3067`  ·  log_price: True  ·  ilvl: `-0.04105`  ·  n_mods: `-0.00840`  ·  n_top_tier: `0.46892`  ·  corrupted: `-0.00131`  ·  n_sockets: `0.00082`  ·  quality: `0.00812`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | 1.81763 |
| `desecrated.stat_210067635@T1` | -1.75764 |
| `explicit.stat_1202301673@T1` | 1.60368 |
| `crafted.stat_3035140377` | 1.37100 |
| `desecrated.stat_666077204@T1` | 1.12352 |
| `explicit.stat_518292764@T1` | 0.91186 |
| `explicit.stat_55876295@T1` | -0.53031 |
| `explicit.stat_3261801346@T1` | -0.50920 |
| `explicit.stat_3336890334@T2` | -0.50737 |
| `explicit.stat_3695891184@T2` | -0.50616 |
| `explicit.stat_2694482655@T1` | -0.50323 |
| `explicit.stat_3695891184@T1` | -0.49740 |

### weapon.crossbow — n=9655, R²=-1.8357

intercept: `3.4922`  ·  log_price: True  ·  ilvl: `-0.04360`  ·  n_mods: `-0.00157`  ·  n_top_tier: `0.40002`  ·  corrupted: `-0.04593`  ·  n_sockets: `0.00916`  ·  quality: `0.00403`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -2.62122 |
| `explicit.stat_1980802737` | 2.19627 |
| `explicit.stat_709508406@T1` | 1.81379 |
| `explicit.stat_1202301673@T1` | 1.79934 |
| `explicit.stat_1509134228@T1` | 1.54899 |
| `explicit.stat_2250681686@T2` | -1.36176 |
| `explicit.stat_2250681686` | 0.98807 |
| `explicit.stat_1037193709@T1` | 0.98084 |
| `crafted.stat_3035140377` | 0.84931 |
| `explicit.stat_1202301673@T2` | -0.49751 |
| `explicit.stat_1509134228@T2` | -0.46025 |
| `explicit.stat_691932474@T1` | -0.45236 |

### flask.charm — n=6371, R²=-0.3364

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.03225`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.00499 |
| `explicit.stat_1056492907` | 2.99572 |
| `explicit.stat_2676834156@T1` | 1.25328 |
| `explicit.stat_3138344128` | 0.02221 |
| `explicit.stat_2541588185@T1` | 0.01139 |
| `explicit.stat_2678930256` | 0.00422 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_3246948616` | 0.00004 |
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_1873752457@T1` | -0.00004 |
| `explicit.stat_3196823591@T2` | -0.00004 |
| `explicit.stat_828533480@T1` | -0.00003 |

### weapon.warstaff — n=4566, R²=-0.5209

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00001`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00005`  ·  n_sockets: `0.00001`  ·  quality: `0.00044`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | -4.02314 |
| `desecrated.stat_2231156303@T1` | -4.02314 |
| `rune.stat_243313994` | 3.08546 |
| `rune.stat_731403740` | 1.52422 |
| `crafted.stat_210067635@T2` | -0.70425 |
| `desecrated.stat_9187492` | 0.64775 |
| `rune.stat_1712188793` | -0.58334 |
| `explicit.stat_9187492@T1` | 0.41478 |
| `desecrated.stat_2527686725` | 0.25018 |
| `desecrated.stat_518292764` | 0.22930 |
| `desecrated.stat_55876295` | -0.10687 |
| `desecrated.stat_669069897` | -0.09863 |

### weapon.staff — n=4268, R²=-0.5707

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.00048`  ·  n_sockets: `0.00001`  ·  quality: `0.00323`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.58066 |
| `explicit.stat_4226189338@T1` | 1.38620 |
| `explicit.stat_2254480358@T1` | 0.79526 |
| `explicit.stat_1600707273@T1` | 0.71715 |
| `explicit.stat_3291658075@T2` | 0.38563 |
| `explicit.stat_3962278098@T2` | 0.32614 |
| `crafted.stat_124131830` | 0.32187 |
| `explicit.stat_473429811@T1` | 0.31034 |
| `explicit.stat_2254480358@T2` | 0.21092 |
| `rune.stat_3990135792` | -0.19702 |
| `rune.stat_975988108` | -0.12130 |
| `rune.stat_2974417149` | 0.10455 |

### weapon.sceptre — n=4239, R²=-0.5432

intercept: `-0.0013`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.25257`  ·  corrupted: `1.63220`  ·  n_sockets: `0.00002`  ·  quality: `0.09062`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.04999 |
| `explicit.stat_3984865854@T1` | 0.37964 |
| `explicit.stat_4080418644@T2` | -0.25261 |
| `explicit.stat_2347036682@T2` | -0.25261 |
| `explicit.stat_4080418644@T1` | -0.25260 |
| `explicit.stat_1250712710@T1` | -0.25259 |
| `explicit.stat_3984865854@T2` | -0.25258 |
| `explicit.stat_2347036682@T1` | -0.25258 |
| `explicit.stat_328541901@T1` | -0.25258 |
| `explicit.stat_1263695895@T2` | -0.25258 |
| `explicit.stat_1574590649@T1` | -0.25258 |
| `explicit.stat_3639275092@T2` | -0.25257 |

### weapon.spear — n=3683, R²=-0.5722

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00003`  ·  corrupted: `-0.00003`  ·  n_sockets: `0.00001`  ·  quality: `0.00015`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.71304 |
| `explicit.stat_1202301673@T1` | 1.58860 |
| `explicit.stat_210067635@T1` | 0.82568 |
| `crafted.stat_518292764` | 0.80837 |
| `rune.stat_1039491398` | 0.14078 |
| `rune.stat_1509134228` | -0.06718 |
| `explicit.stat_1509134228@T1` | 0.01110 |
| `crafted.stat_210067635` | 0.00953 |
| `desecrated.stat_1509134228` | 0.00300 |
| `desecrated.stat_691932474` | -0.00062 |
| `explicit.stat_210067635@T2` | 0.00006 |
| `explicit.stat_1263695895@T1` | 0.00006 |

### armour.focus — n=2995, R²=-0.5983

intercept: `-0.0009`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.43323`  ·  corrupted: `0.00004`  ·  n_sockets: `0.00003`  ·  quality: `0.03469`

| stat_id | coef |
|---|---|
| `desecrated.stat_3393628375@T1` | -5.48532 |
| `crafted.stat_737908626@T2` | -3.98380 |
| `desecrated.stat_378817135@T1` | -1.16270 |
| `explicit.stat_789117908@T2` | -0.43325 |
| `explicit.stat_3291658075@T1` | -0.43325 |
| `explicit.stat_2339757871@T2` | -0.43325 |
| `explicit.stat_2891184298@T2` | -0.43325 |
| `explicit.stat_736967255@T2` | -0.43324 |
| `explicit.stat_274716455@T1` | -0.43324 |
| `explicit.stat_4015621042@T2` | -0.43324 |
| `explicit.stat_2923486259@T1` | -0.43324 |
| `explicit.stat_3372524247@T2` | -0.43324 |

### armour.quiver — n=2820, R²=-0.6354

intercept: `-0.0025`  ·  log_price: True  ·  ilvl: `0.00003`  ·  n_mods: `0.00002`  ·  n_top_tier: `0.32273`  ·  corrupted: `0.00009`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.58324 |
| `explicit.stat_3759663284@T1` | 0.35897 |
| `explicit.stat_681332047@T2` | -0.32302 |
| `explicit.stat_681332047@T1` | -0.32300 |
| `explicit.stat_1573130764@T1` | -0.32282 |
| `explicit.stat_2194114101@T2` | -0.32281 |
| `explicit.stat_1368271171@T2` | -0.32280 |
| `explicit.stat_2321178454@T2` | -0.32280 |
| `explicit.stat_1573130764@T2` | -0.32277 |
| `explicit.stat_3714003708@T2` | -0.32275 |
| `explicit.stat_803737631@T2` | -0.32273 |
| `explicit.stat_2194114101@T1` | -0.32272 |

### armour.shield — n=2421, R²=-0.4745

intercept: `-0.0007`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.31131`  ·  corrupted: `0.00526`  ·  n_sockets: `0.00000`  ·  quality: `0.06490`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.76645 |
| `explicit.stat_1978899297@T2` | -0.46558 |
| `explicit.stat_1011760251@T1` | -0.33220 |
| `explicit.stat_1011760251@T2` | -0.32522 |
| `explicit.stat_2481353198@T1` | -0.31136 |
| `explicit.stat_328541901@T1` | -0.31136 |
| `explicit.stat_2339757871@T1` | -0.31136 |
| `explicit.stat_2481353198@T2` | -0.31135 |
| `explicit.stat_328541901@T2` | -0.31135 |
| `explicit.stat_3372524247@T2` | -0.31133 |
| `explicit.stat_3484657501@T1` | -0.31133 |
| `explicit.stat_1062208444@T2` | -0.31132 |

### weapon.twomace — n=2140, R²=-0.518

intercept: `-0.0008`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.30597`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.45597 |
| `crafted.stat_3035140377` | 1.34591 |
| `explicit.stat_1509134228@T1` | 0.71756 |
| `rune.stat_709508406` | 0.67011 |
| `desecrated.stat_1509134228@T1` | -0.59109 |
| `explicit.stat_3336890334@T1` | -0.30768 |
| `explicit.stat_1037193709@T1` | -0.30606 |
| `explicit.stat_1263695895@T1` | -0.30601 |
| `explicit.stat_1037193709@T2` | -0.30601 |
| `explicit.stat_387439868@T2` | -0.30600 |
| `explicit.stat_1263695895@T2` | -0.30600 |
| `explicit.stat_821021828@T1` | -0.30600 |

## Coverage (listings per base)

- … **Sapphire** — 12773 listings (12756 priced) [0.4–7553463.8 ex]
- … **Emerald** — 12766 listings (12758 priced) [0.4–7553463.8 ex]
- … **Ruby** — 9887 listings (9877 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 6036 listings (6032 priced) [0.3–5288620.9 ex]
- … **Prismatic Ring** — 4595 listings (4593 priced) [0.3–24532814.5 ex]
- … **Stellar Amulet** — 4525 listings (4525 priced) [0.2–35690283.3 ex]
- … **Solar Amulet** — 4473 listings (4467 priced) [0.5–66666666.0 ex]
- … **Amethyst Ring** — 4363 listings (4362 priced) [0.4–71450.3 ex]
- … **Gold Amulet** — 4277 listings (4274 priced) [0.2–4894457.0 ex]
- … **Gold Ring** — 4145 listings (4143 priced) [0.5–24532814.5 ex]
- … **Dueling Wand** — 3943 listings (3938 priced) [0.3–3736768402.2 ex]
- … **Sapphire Ring** — 3471 listings (3467 priced) [0.4–24532814.5 ex]
- … **Ruby Ring** — 3368 listings (3368 priced) [0.4–37474957.5 ex]
- … **Topaz Ring** — 3343 listings (3342 priced) [0.5–123132003.2 ex]
- … **Plate Belt** — 3087 listings (3084 priced) [0.3–5286174.1 ex]
- … **Obliterator Bow** — 2997 listings (2990 priced) [0.4–22139622146.9 ex]
- … **Ancestral Tiara** — 2989 listings (2986 priced) [0.6–41469259.3 ex]
- … **Lapis Amulet** — 2983 listings (2982 priced) [0.5–5286174.1 ex]
- … **Jade Amulet** — 2958 listings (2957 priced) [0.2–4547453.5 ex]
- … **Amber Amulet** — 2955 listings (2954 priced) [0.2–124352753.2 ex]
- … **Heavy Belt** — 2887 listings (2887 priced) [0.5–4877938.3 ex]
- … **Unset Ring** — 2803 listings (2803 priced) [0.5–24532814.5 ex]
- … **Bloodstone Amulet** — 2768 listings (2768 priced) [0.5–329628.5 ex]
- … **Pearl Ring** — 2694 listings (2694 priced) [0.4–24532814.5 ex]
- … **Azure Amulet** — 2621 listings (2621 priced) [0.5–123132003.2 ex]

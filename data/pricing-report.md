# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-14T19:27:56+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **480721** (479745 priced in exalted)
- Distinct bases: 979 · distinct mods: 3057 · mod rows: 2282876
- Sold signals: **26631** sold · 267191 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-14T19:18:04+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×23.40** (median |log error| 3.1527)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.08** · typical error ×55.82 · ±30% 5% · n=68599
- Premium segment (60ex+): skill **+0.09** · typical error ×187.45 · ±30% 0% · n=45518

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 9516 | ×53.72 | 21% | +0.06 | +0.08 |
| jewel | 8829 | ×9.41 | 5% | +0.02 | +0.06 |
| accessory.amulet | 8822 | ×52.02 | 21% | +0.03 | +0.03 |
| accessory.belt | 6823 | ×12.13 | 6% | +0.03 | +0.04 |
| armour.chest | 6656 | ×15.07 | 6% | +0.00 | +0.03 |
| armour.helmet | 6512 | ×17.56 | 5% | +0.02 | +0.05 |
| armour.boots | 6042 | ×23.96 | 7% | +0.11 | +0.12 |
| armour.gloves | 5908 | ×20.97 | 5% | +0.07 | +0.08 |
| other | 5207 | ×9.92 | 36% | +0.09 | +0.19 |
| weapon.wand | 3809 | ×35.55 | 20% | +0.07 | +0.08 |
| weapon.bow | 3072 | ×31.28 | 19% | +0.09 | +0.08 |
| weapon.crossbow | 2903 | ×20.07 | 20% | +0.09 | +0.13 |
| weapon.warstaff | 1671 | ×32.40 | 18% | +0.10 | +0.09 |
| weapon.sceptre | 1596 | ×48.83 | 8% | +0.12 | +0.10 |
| weapon.staff | 1572 | ×52.73 | 17% | +0.07 | +0.08 |
| weapon.spear | 1251 | ×64.20 | 18% | +0.08 | +0.07 |
| armour.quiver | 1022 | ×39.39 | 12% | +0.07 | +0.12 |
| armour.focus | 1019 | ×40.83 | 8% | +0.12 | +0.14 |
| flask.charm | 863 | ×40.00 | 36% | +0.02 | +0.03 |
| armour.shield | 805 | ×14.87 | 15% | +0.01 | +0.01 |
| weapon.twomace | 768 | ×19.24 | 18% | +0.06 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=47337, R²=-0.8584

intercept: `-1.6716`  ·  log_price: True  ·  ilvl: `0.02959`  ·  n_mods: `0.57847`  ·  n_top_tier: `-0.17665`  ·  corrupted: `0.08657`  ·  quality: `0.22507`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -4.00748 |
| `explicit.stat_2301718443@T1` | 3.24970 |
| `explicit.stat_1697447343@T1` | -2.35724 |
| `explicit.stat_3780644166@T1` | -2.25466 |
| `explicit.stat_3473929743@T1` | -1.98804 |
| `explicit.stat_627767961@T1` | -1.86793 |
| `explicit.stat_795138349@T1` | -1.77778 |
| `explicit.stat_3166958180@T1` | -1.73538 |
| `explicit.stat_3485067555@T1` | 1.70514 |
| `explicit.stat_239367161@T1` | -1.68654 |
| `explicit.stat_234296660@T1` | -1.64654 |
| `explicit.stat_1697951953@T1` | -1.56476 |

### other — n=46683, R²=-0.4509

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00005`  ·  n_top_tier: `0.69313`  ·  corrupted: `0.77765`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1589917703@T1` | 3.08525 |
| `explicit.stat_3291658075@T1` | 3.06143 |
| `explicit.stat_2231156303@T1` | 1.97794 |
| `explicit.stat_3141070085@T1` | -1.43566 |
| `explicit.stat_1050105434@T1` | -1.13876 |
| `explicit.stat_789117908@T1` | -1.04029 |
| `explicit.stat_2974417149@T1` | 1.01607 |
| `explicit.stat_3917489142@T1` | 1.01404 |
| `explicit.stat_2482852589@T1` | 0.90780 |
| `explicit.stat_2891184298@T1` | 0.81608 |
| `explicit.stat_2968503605@T1` | 0.65535 |
| `explicit.stat_736967255@T1` | -0.32593 |

### accessory.ring — n=43492, R²=-1.9728

intercept: `3.4734`  ·  log_price: True  ·  ilvl: `-0.04283`  ·  n_mods: `0.00130`  ·  n_top_tier: `0.47212`  ·  corrupted: `0.15127`  ·  n_sockets: `2.19816`  ·  quality: `0.07357`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -0.51434 |
| `explicit.stat_1573130764@T1` | -0.51181 |
| `explicit.stat_1263695895@T1` | -0.49570 |
| `explicit.stat_3291658075@T2` | -0.49533 |
| `explicit.stat_2144192055@T1` | -0.49447 |
| `explicit.stat_4220027924@T2` | -0.49445 |
| `explicit.stat_1368271171@T2` | -0.49430 |
| `explicit.stat_3291658075@T1` | -0.49347 |
| `explicit.stat_3325883026@T1` | -0.48966 |
| `explicit.stat_3962278098@T2` | -0.48877 |
| `explicit.stat_2231156303@T2` | -0.48841 |
| `explicit.stat_3032590688@T2` | -0.48748 |

### accessory.amulet — n=40334, R²=-2.1459

intercept: `3.8233`  ·  log_price: True  ·  ilvl: `-0.04661`  ·  n_mods: `-0.02029`  ·  n_top_tier: `1.14857`  ·  corrupted: `0.04965`  ·  n_sockets: `-0.11341`  ·  quality: `0.00003`

| stat_id | coef |
|---|---|
| `explicit.stat_2748665614@T1` | -1.22342 |
| `explicit.stat_2748665614@T2` | -1.20778 |
| `explicit.stat_2901986750@T1` | -1.20084 |
| `explicit.stat_472520716@T1` | -1.19988 |
| `explicit.stat_472520716@T2` | -1.19817 |
| `explicit.stat_1050105434@T2` | -1.19337 |
| `explicit.stat_803737631@T1` | -1.18829 |
| `explicit.stat_3917489142@T2` | -1.18692 |
| `explicit.stat_3299347043@T1` | -1.18564 |
| `explicit.stat_2974417149@T1` | -1.18044 |
| `explicit.stat_2162097452@T2` | -1.17846 |
| `explicit.stat_2866361420@T1` | -1.17624 |

### accessory.belt — n=31272, R²=-0.4345

intercept: `5.7846`  ·  log_price: True  ·  ilvl: `-0.03957`  ·  n_mods: `-0.41773`  ·  n_top_tier: `0.90993`  ·  corrupted: `0.62489`  ·  n_sockets: `0.18347`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.39082 |
| `explicit.stat_2881298780@T1` | -1.30653 |
| `explicit.stat_3299347043@T1` | -1.24532 |
| `explicit.stat_51994685@T1` | -1.15435 |
| `explicit.stat_3299347043@T2` | -1.11459 |
| `explicit.stat_3325883026@T1` | -1.11242 |
| `explicit.stat_809229260@T2` | -1.06545 |
| `explicit.stat_2923486259@T1` | -1.06479 |
| `explicit.stat_1389754388@T2` | -1.05947 |
| `explicit.stat_809229260@T1` | -1.02209 |
| `explicit.stat_2923486259@T2` | -1.00675 |
| `explicit.stat_1671376347@T2` | -1.00531 |

### armour.chest — n=30902, R²=-0.5842

intercept: `3.7642`  ·  log_price: True  ·  ilvl: `-0.03191`  ·  n_mods: `-0.13884`  ·  n_top_tier: `0.39947`  ·  corrupted: `0.31729`  ·  n_sockets: `0.09755`  ·  quality: `0.02020`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.39466 |
| `explicit.stat_4080418644@T1` | -0.88338 |
| `explicit.stat_2923486259@T1` | -0.73661 |
| `explicit.stat_3484657501@T1` | -0.66573 |
| `explicit.stat_4080418644@T2` | -0.61955 |
| `explicit.stat_3261801346@T2` | -0.57679 |
| `explicit.stat_124859000@T2` | -0.56554 |
| `explicit.stat_915769802@T2` | -0.56496 |
| `explicit.stat_2451402625@T2` | -0.54857 |
| `explicit.stat_2881298780@T2` | -0.51256 |
| `explicit.stat_2923486259@T2` | -0.50197 |
| `explicit.stat_3325883026@T2` | -0.49845 |

### armour.helmet — n=30163, R²=-0.7173

intercept: `3.8999`  ·  log_price: True  ·  ilvl: `-0.04466`  ·  n_mods: `-0.14037`  ·  n_top_tier: `0.48630`  ·  corrupted: `0.73865`  ·  n_sockets: `0.14311`  ·  quality: `0.03592`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.17313 |
| `explicit.stat_53045048@T2` | -1.05137 |
| `explicit.stat_3917489142@T2` | -1.03701 |
| `explicit.stat_2339757871@T1` | -0.90577 |
| `explicit.stat_53045048@T1` | -0.81129 |
| `explicit.stat_3321629045@T2` | -0.78169 |
| `explicit.stat_3261801346@T1` | -0.75783 |
| `explicit.stat_1999113824@T1` | -0.74544 |
| `explicit.stat_587431675@T2` | -0.66095 |
| `explicit.stat_1263695895@T2` | -0.65826 |
| `explicit.stat_3261801346@T2` | -0.64914 |
| `explicit.stat_2162097452@T2` | -0.64805 |

### armour.boots — n=28312, R²=-1.1644

intercept: `4.3388`  ·  log_price: True  ·  ilvl: `-0.05102`  ·  n_mods: `-0.07593`  ·  n_top_tier: `0.67996`  ·  corrupted: `0.31148`  ·  n_sockets: `0.05659`  ·  quality: `0.02576`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.68631 |
| `explicit.stat_2250533757@T1` | 1.30724 |
| `explicit.stat_2923486259@T2` | -1.05837 |
| `explicit.stat_3917489142@T2` | -1.04778 |
| `explicit.stat_3299347043@T1` | -1.02111 |
| `explicit.stat_3917489142@T1` | -0.95133 |
| `explicit.stat_1062208444@T2` | -0.92626 |
| `explicit.stat_4052037485@T2` | -0.86402 |
| `explicit.stat_53045048@T1` | -0.85163 |
| `explicit.stat_328541901@T1` | -0.84736 |
| `explicit.stat_3484657501@T2` | -0.84404 |
| `explicit.stat_1671376347@T2` | -0.84018 |

### armour.gloves — n=27619, R²=-1.0251

intercept: `3.8053`  ·  log_price: True  ·  ilvl: `-0.04866`  ·  n_mods: `-0.08706`  ·  n_top_tier: `0.47375`  ·  corrupted: `0.15068`  ·  n_sockets: `0.25383`  ·  quality: `0.03486`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | -5.60168 |
| `explicit.stat_2339757871@T1` | 2.24542 |
| `explicit.stat_3484657501@T2` | -1.34949 |
| `explicit.stat_803737631@T2` | -1.00365 |
| `rune.stat_836936635` | 0.92416 |
| `explicit.stat_3484657501@T1` | -0.91750 |
| `explicit.stat_3917489142@T2` | -0.84317 |
| `explicit.stat_803737631@T1` | -0.81589 |
| `explicit.stat_9187492@T1` | 0.79003 |
| `explicit.stat_1573130764@T1` | -0.76661 |
| `explicit.stat_3321629045@T2` | -0.75823 |
| `explicit.stat_3917489142@T1` | -0.73605 |

### weapon.wand — n=17863, R²=-2.2484

intercept: `3.5531`  ·  log_price: True  ·  ilvl: `-0.04387`  ·  n_mods: `-0.01426`  ·  n_top_tier: `0.36946`  ·  corrupted: `0.01589`  ·  n_sockets: `0.03198`  ·  quality: `0.00061`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.19895 |
| `rune.stat_124131830` | -3.00980 |
| `explicit.stat_2254480358@T1` | 2.63333 |
| `explicit.stat_4226189338@T1` | 1.93959 |
| `explicit.stat_591105508@T1` | 1.90723 |
| `explicit.stat_124131830@T1` | 1.83224 |
| `explicit.stat_736967255@T2` | 1.25202 |
| `crafted.stat_124131830` | 1.13934 |
| `explicit.stat_2768835289@T2` | 0.91892 |
| `explicit.stat_2254480358@T2` | 0.87148 |
| `explicit.stat_4226189338@T2` | 0.58950 |
| `explicit.stat_737908626@T1` | -0.44657 |

### weapon.bow — n=14472, R²=-1.9952

intercept: `3.4702`  ·  log_price: True  ·  ilvl: `-0.04184`  ·  n_mods: `-0.03680`  ·  n_top_tier: `0.65567`  ·  corrupted: `-0.08673`  ·  n_sockets: `-0.00645`  ·  quality: `0.03194`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.35193 |
| `explicit.stat_1202301673@T1` | 1.57883 |
| `crafted.stat_3035140377` | 1.27358 |
| `explicit.stat_1263695895@T1` | -0.83496 |
| `explicit.stat_3695891184@T2` | -0.74216 |
| `explicit.stat_1263695895@T2` | -0.73471 |
| `explicit.stat_1509134228@T1` | -0.72797 |
| `explicit.stat_3695891184@T1` | -0.72764 |
| `explicit.stat_1368271171@T2` | -0.72117 |
| `explicit.stat_1037193709@T2` | -0.69964 |
| `explicit.stat_2694482655@T2` | -0.69769 |
| `explicit.stat_1368271171@T1` | -0.69342 |

### weapon.crossbow — n=13703, R²=-1.9816

intercept: `3.5662`  ·  log_price: True  ·  ilvl: `-0.04371`  ·  n_mods: `-0.01612`  ·  n_top_tier: `0.70646`  ·  corrupted: `0.00763`  ·  n_sockets: `0.01494`  ·  quality: `0.00935`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.95341 |
| `explicit.stat_709508406@T1` | 1.55296 |
| `explicit.stat_2250681686@T2` | -1.47208 |
| `explicit.stat_1202301673@T1` | 1.32238 |
| `explicit.stat_1980802737` | 1.19286 |
| `crafted.stat_3035140377` | 0.91918 |
| `explicit.stat_1202301673@T2` | -0.87197 |
| `explicit.stat_1263695895@T2` | -0.86009 |
| `explicit.stat_1263695895@T1` | -0.83470 |
| `explicit.stat_2250681686` | 0.82942 |
| `explicit.stat_2694482655@T1` | -0.77613 |
| `explicit.stat_1037193709@T1` | -0.77271 |

### flask.charm — n=12062, R²=-0.5217

intercept: `0.0010`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.99560`  ·  corrupted: `2.18247`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.28697 |
| `explicit.stat_1056492907` | 3.42451 |
| `explicit.stat_828533480@T2` | -2.99561 |
| `explicit.stat_2676834156@T2` | -2.99560 |
| `explicit.stat_1120862500@T2` | -2.99560 |
| `explicit.stat_3196823591@T2` | -2.99560 |
| `explicit.stat_828533480@T1` | -2.99560 |
| `explicit.stat_2541588185@T2` | -2.99560 |
| `explicit.stat_1873752457@T2` | -2.99559 |
| `explicit.stat_1366840608@T2` | -2.99559 |
| `explicit.stat_388617051@T2` | -2.99559 |
| `explicit.stat_1873752457@T1` | -2.99558 |

### weapon.warstaff — n=8196, R²=-0.5286

intercept: `-4.2627`  ·  log_price: True  ·  ilvl: `0.05945`  ·  n_mods: `-0.14108`  ·  n_top_tier: `0.54461`  ·  corrupted: `0.15146`  ·  n_sockets: `0.07426`  ·  quality: `0.05408`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.56997 |
| `explicit.stat_1037193709@T1` | 1.26743 |
| `explicit.stat_328541901@T1` | -1.00339 |
| `explicit.stat_328541901@T2` | -0.90450 |
| `explicit.stat_55876295@T2` | -0.72046 |
| `explicit.stat_1037193709@T2` | -0.69339 |
| `desecrated.stat_9187492` | 0.63114 |
| `crafted.stat_210067635@T2` | 0.62651 |
| `explicit.stat_55876295@T1` | -0.59152 |
| `explicit.stat_1940865751@T1` | -0.59056 |
| `explicit.stat_210067635@T1` | -0.57993 |
| `explicit.stat_791928121@T2` | -0.57917 |

### weapon.staff — n=7563, R²=-0.5143

intercept: `-7.9876`  ·  log_price: True  ·  ilvl: `0.10324`  ·  n_mods: `-0.09334`  ·  n_top_tier: `0.33790`  ·  corrupted: `0.02627`  ·  n_sockets: `0.19398`  ·  quality: `0.05571`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 1.96907 |
| `explicit.stat_124131830@T1` | 1.65448 |
| `explicit.stat_1545858329@T1` | 1.45936 |
| `explicit.stat_2768835289@T2` | 1.05151 |
| `explicit.stat_2254480358@T1` | 1.04795 |
| `explicit.stat_1600707273@T1` | 0.99105 |
| `explicit.stat_4226189338@T2` | 0.92481 |
| `explicit.stat_3962278098@T2` | 0.73478 |
| `explicit.stat_124131830@T2` | 0.68655 |
| `explicit.stat_2231156303@T2` | 0.68054 |
| `explicit.stat_591105508@T1` | 0.65633 |
| `explicit.stat_1263695895@T2` | -0.60944 |

### weapon.sceptre — n=7543, R²=-0.4481

intercept: `-13.0321`  ·  log_price: True  ·  ilvl: `0.16520`  ·  n_mods: `-0.05460`  ·  n_top_tier: `0.66006`  ·  corrupted: `0.45190`  ·  n_sockets: `0.19651`  ·  quality: `0.06495`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.10325 |
| `explicit.stat_2162097452@T2` | 1.21549 |
| `explicit.stat_1263695895@T1` | -1.14481 |
| `explicit.stat_4080418644@T1` | -1.07594 |
| `explicit.stat_1574590649@T2` | -1.07004 |
| `explicit.stat_1263695895@T2` | -1.05744 |
| `explicit.stat_2347036682@T2` | -0.97490 |
| `explicit.stat_289128254@T2` | -0.88197 |
| `explicit.stat_1050105434@T2` | -0.81578 |
| `explicit.stat_2854751904@T2` | -0.78965 |
| `explicit.stat_3639275092@T2` | -0.65464 |
| `explicit.stat_789117908@T2` | -0.62499 |

### weapon.spear — n=6283, R²=-0.5816

intercept: `-6.0935`  ·  log_price: True  ·  ilvl: `0.08161`  ·  n_mods: `-0.03154`  ·  n_top_tier: `0.72699`  ·  corrupted: `-0.17034`  ·  n_sockets: `0.15469`  ·  quality: `0.10217`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.91384 |
| `explicit.stat_1202301673@T1` | 2.07862 |
| `explicit.stat_9187492@T1` | 1.85228 |
| `desecrated.stat_210067635@T1` | -1.16696 |
| `crafted.stat_3035140377` | 1.08127 |
| `explicit.stat_1263695895@T2` | -0.97640 |
| `explicit.stat_1509134228@T1` | 0.97310 |
| `explicit.stat_55876295@T1` | -0.92194 |
| `explicit.stat_55876295@T2` | -0.87108 |
| `explicit.stat_1037193709@T1` | -0.77210 |
| `explicit.stat_791928121@T2` | -0.72380 |
| `explicit.stat_1940865751@T2` | -0.71744 |

### armour.focus — n=5138, R²=-0.4529

intercept: `-10.2505`  ·  log_price: True  ·  ilvl: `0.12836`  ·  n_mods: `-0.07719`  ·  n_top_tier: `0.86212`  ·  corrupted: `0.70578`  ·  n_sockets: `0.38410`  ·  quality: `0.06928`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -3.77512 |
| `explicit.stat_4220027924@T2` | -1.20841 |
| `crafted.stat_2974417149@T1` | 1.17429 |
| `explicit.stat_3291658075@T1` | -1.09221 |
| `explicit.stat_736967255@T2` | -1.07912 |
| `explicit.stat_3962278098@T2` | -1.04816 |
| `explicit.stat_2923486259@T1` | -1.00885 |
| `explicit.stat_3962278098@T1` | -0.96922 |
| `explicit.stat_2974417149@T1` | -0.93821 |
| `explicit.stat_2231156303@T2` | -0.89087 |
| `explicit.stat_3372524247@T2` | -0.88330 |
| `explicit.stat_2339757871@T2` | -0.88139 |

### armour.quiver — n=4787, R²=-0.4087

intercept: `-9.8508`  ·  log_price: True  ·  ilvl: `0.12135`  ·  n_mods: `-0.06668`  ·  n_top_tier: `0.81578`  ·  corrupted: `0.37448`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 7.54274 |
| `explicit.stat_2463230181@T1` | 2.43378 |
| `explicit.stat_2463230181@T2` | 1.32778 |
| `explicit.stat_2321178454@T2` | -1.32748 |
| `explicit.stat_681332047@T2` | -1.18436 |
| `explicit.stat_4067062424@T1` | -1.16615 |
| `explicit.stat_1573130764@T2` | -1.02858 |
| `explicit.stat_3261801346@T1` | -0.95773 |
| `explicit.stat_1573130764@T1` | -0.90633 |
| `explicit.stat_803737631@T2` | -0.89099 |
| `explicit.stat_2321178454@T1` | -0.84204 |
| `explicit.stat_681332047@T1` | -0.82051 |

### armour.shield — n=4206, R²=-0.5797

intercept: `-7.0875`  ·  log_price: True  ·  ilvl: `0.09269`  ·  n_mods: `-0.05355`  ·  n_top_tier: `0.53381`  ·  corrupted: `0.10887`  ·  n_sockets: `0.09691`  ·  quality: `0.05016`

| stat_id | coef |
|---|---|
| `explicit.stat_1011760251@T1` | -1.19201 |
| `explicit.stat_2339757871@T1` | -1.09710 |
| `explicit.stat_1011760251@T2` | -0.95479 |
| `explicit.stat_1301765461@T1` | 0.92864 |
| `explicit.stat_328541901@T1` | -0.90127 |
| `explicit.stat_2923486259@T2` | -0.81964 |
| `explicit.stat_3676141501@T1` | 0.79503 |
| `explicit.stat_1978899297@T2` | -0.77295 |
| `explicit.stat_2481353198@T2` | -0.75207 |
| `explicit.stat_3321629045@T2` | -0.69898 |
| `explicit.stat_53045048@T1` | -0.67989 |
| `explicit.stat_2481353198@T1` | -0.67410 |

### weapon.twomace — n=3861, R²=-0.5296

intercept: `-8.4407`  ·  log_price: True  ·  ilvl: `0.11089`  ·  n_mods: `-0.10131`  ·  n_top_tier: `0.54593`  ·  corrupted: `0.69317`  ·  n_sockets: `0.13845`  ·  quality: `0.03728`

| stat_id | coef |
|---|---|
| `desecrated.stat_1509134228@T1` | 2.32978 |
| `desecrated.stat_210067635@T1` | -2.22845 |
| `explicit.stat_1037193709@T1` | -1.62801 |
| `explicit.stat_3336890334@T1` | -1.32398 |
| `crafted.stat_3035140377` | 1.10914 |
| `explicit.stat_387439868@T2` | -0.93396 |
| `explicit.stat_518292764@T2` | -0.93154 |
| `explicit.stat_1037193709@T2` | -0.90946 |
| `explicit.stat_1263695895@T1` | -0.84449 |
| `explicit.stat_1263695895@T2` | -0.83265 |
| `explicit.stat_3695891184@T1` | -0.72396 |
| `explicit.stat_3639275092@T1` | -0.71256 |

## Coverage (listings per base)

- … **Sapphire** — 22108 listings (22078 priced) [0.3–7553463.8 ex]
- … **Emerald** — 21806 listings (21778 priced) [0.3–7553463.8 ex]
- … **Ruby** — 16676 listings (16662 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 9136 listings (9127 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 7431 listings (7421 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 7288 listings (7275 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 7153 listings (7146 priced) [0.2–19945827.9 ex]
- … **Gold Amulet** — 6816 listings (6806 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 6796 listings (6792 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 6674 listings (6663 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5682 listings (5667 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5576 listings (5570 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 5354 listings (5350 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5330 listings (5327 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 4845 listings (4831 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4789 listings (4784 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4682 listings (4675 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4645 listings (4642 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4632 listings (4626 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4595 listings (4588 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4478 listings (4473 priced) [0.3–4275054.0 ex]
- … **Heavy Belt** — 4341 listings (4338 priced) [0.3–2608914286.6 ex]
- … **Obliterator Bow** — 4339 listings (4326 priced) [0.3–42622633798.0 ex]
- … **Pearl Ring** — 4310 listings (4305 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 4222 listings (4222 priced) [0.3–123132003.2 ex]

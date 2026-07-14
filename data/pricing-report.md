# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-14T13:31:35+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **469177** (468233 priced in exalted)
- Distinct bases: 979 · distinct mods: 3048 · mod rows: 2228660
- Sold signals: **26820** sold · 259557 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-14T13:22:55+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.91** (median |log error| 3.2153)
- Within ±30% of asking price: **15%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.10** · typical error ×65.26 · ±30% 5% · n=66977
- Premium segment (60ex+): skill **+0.11** · typical error ×241.58 · ±30% 0% · n=44298

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 9220 | ×49.98 | 21% | +0.05 | +0.06 |
| accessory.amulet | 8621 | ×50.16 | 21% | +0.03 | +0.02 |
| jewel | 8598 | ×9.02 | 5% | +0.02 | +0.05 |
| accessory.belt | 6652 | ×17.34 | 4% | +0.04 | +0.05 |
| armour.chest | 6521 | ×21.79 | 11% | +0.09 | +0.11 |
| armour.helmet | 6379 | ×20.84 | 5% | +0.04 | +0.07 |
| armour.boots | 5944 | ×27.77 | 13% | +0.09 | +0.10 |
| armour.gloves | 5815 | ×24.47 | 6% | +0.11 | +0.12 |
| other | 5124 | ×8.73 | 40% | +0.09 | +0.15 |
| weapon.wand | 3750 | ×33.47 | 19% | +0.07 | +0.08 |
| weapon.bow | 3031 | ×29.61 | 17% | +0.09 | +0.09 |
| weapon.crossbow | 2846 | ×24.76 | 20% | +0.09 | +0.12 |
| weapon.warstaff | 1624 | ×34.44 | 20% | +0.09 | +0.10 |
| weapon.staff | 1507 | ×51.04 | 16% | +0.07 | +0.07 |
| weapon.sceptre | 1491 | ×39.18 | 7% | +0.12 | +0.10 |
| weapon.spear | 1288 | ×49.60 | 20% | +0.08 | +0.07 |
| armour.focus | 1038 | ×46.25 | 10% | +0.13 | +0.13 |
| armour.quiver | 979 | ×33.51 | 13% | +0.07 | +0.11 |
| armour.shield | 825 | ×17.98 | 19% | +0.03 | +0.02 |
| flask.charm | 777 | ×50.00 | 35% | +0.02 | +0.03 |
| weapon.twomace | 710 | ×13.15 | 18% | +0.06 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=45979, R²=-0.8352

intercept: `-1.5126`  ·  log_price: True  ·  ilvl: `0.02994`  ·  n_mods: `0.53130`  ·  n_top_tier: `-0.17636`  ·  corrupted: `0.14667`  ·  quality: `0.23513`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.47750 |
| `explicit.stat_2301718443@T1` | 3.20909 |
| `explicit.stat_3780644166@T1` | -2.75043 |
| `explicit.stat_1697447343@T1` | -2.45180 |
| `explicit.stat_795138349@T1` | -2.07874 |
| `explicit.stat_2594634307@T1` | 1.91638 |
| `explicit.stat_169946467@T1` | -1.86216 |
| `explicit.stat_1315743832@T1` | 1.85492 |
| `explicit.stat_21071013@T1` | 1.84382 |
| `explicit.stat_627767961@T1` | -1.72416 |
| `explicit.stat_1805182458@T1` | -1.72346 |
| `explicit.stat_3485067555@T1` | 1.72273 |

### other — n=45692, R²=-0.5787

intercept: `1.6093`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00011`  ·  n_top_tier: `0.45261`  ·  corrupted: `0.53381`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.67884 |
| `explicit.stat_1050105434@T1` | -0.50726 |
| `explicit.stat_789117908@T1` | -0.50003 |
| `explicit.stat_2974417149@T1` | 0.45525 |
| `explicit.stat_1589917703@T1` | -0.44530 |
| `explicit.stat_3299347043@T1` | -0.39058 |
| `explicit.stat_3917489142@T1` | 0.28431 |
| `explicit.stat_2891184298@T1` | 0.24048 |
| `explicit.stat_101878827@T1` | 0.24038 |
| `implicit.stat_3879011313` | 0.23028 |
| `implicit.stat_4041853756` | 0.23026 |
| `explicit.stat_2968503605@T1` | 0.22245 |

### accessory.ring — n=42354, R²=-1.9847

intercept: `3.4453`  ·  log_price: True  ·  ilvl: `-0.04252`  ·  n_mods: `0.00016`  ·  n_top_tier: `0.50774`  ·  corrupted: `0.03450`  ·  n_sockets: `1.31451`  ·  quality: `0.07373`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -0.55085 |
| `explicit.stat_1573130764@T1` | -0.54890 |
| `explicit.stat_1263695895@T1` | -0.54491 |
| `explicit.stat_3325883026@T1` | -0.54126 |
| `explicit.stat_803737631@T1` | -0.53747 |
| `explicit.stat_3291658075@T1` | -0.53184 |
| `explicit.stat_3962278098@T2` | -0.53109 |
| `explicit.stat_1368271171@T2` | -0.52968 |
| `explicit.stat_2144192055@T1` | -0.52728 |
| `explicit.stat_3291658075@T2` | -0.52682 |
| `explicit.stat_2231156303@T2` | -0.52651 |
| `explicit.stat_1263695895@T2` | -0.52541 |

### accessory.amulet — n=39320, R²=-2.1282

intercept: `3.7951`  ·  log_price: True  ·  ilvl: `-0.04622`  ·  n_mods: `-0.02112`  ·  n_top_tier: `1.02404`  ·  corrupted: `0.03681`  ·  n_sockets: `-0.12493`  ·  quality: `0.00147`

| stat_id | coef |
|---|---|
| `explicit.stat_2748665614@T1` | -1.11363 |
| `explicit.stat_2748665614@T2` | -1.10564 |
| `explicit.stat_2901986750@T1` | -1.07773 |
| `explicit.stat_472520716@T1` | -1.07734 |
| `explicit.stat_803737631@T1` | -1.06873 |
| `explicit.stat_1050105434@T2` | -1.06847 |
| `explicit.stat_3917489142@T2` | -1.06728 |
| `explicit.stat_3917489142@T1` | -1.06139 |
| `explicit.stat_2974417149@T1` | -1.06071 |
| `explicit.stat_472520716@T2` | -1.05966 |
| `explicit.stat_803737631@T2` | -1.05427 |
| `explicit.stat_2866361420@T2` | -1.05421 |

### accessory.belt — n=30579, R²=-0.6578

intercept: `6.7757`  ·  log_price: True  ·  ilvl: `-0.05706`  ·  n_mods: `-0.43104`  ·  n_top_tier: `0.97546`  ·  corrupted: `0.94136`  ·  n_sockets: `0.50604`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.65602 |
| `explicit.stat_2881298780@T1` | -1.52644 |
| `explicit.stat_3299347043@T1` | -1.30584 |
| `explicit.stat_51994685@T1` | -1.30550 |
| `explicit.stat_809229260@T2` | -1.19817 |
| `explicit.stat_1389754388@T2` | -1.18660 |
| `explicit.stat_3299347043@T2` | -1.12388 |
| `explicit.stat_1671376347@T2` | -1.07473 |
| `explicit.stat_4080418644@T2` | -1.05073 |
| `explicit.stat_4220027924@T2` | -1.03463 |
| `explicit.stat_1050105434@T2` | -1.01936 |
| `explicit.stat_3325883026@T1` | -1.01319 |

### armour.chest — n=30230, R²=-1.2857

intercept: `4.4440`  ·  log_price: True  ·  ilvl: `-0.05328`  ·  n_mods: `-0.06765`  ·  n_top_tier: `0.52576`  ·  corrupted: `0.39117`  ·  n_sockets: `0.08931`  ·  quality: `0.03792`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.20307 |
| `explicit.stat_3981240776@T1` | 1.08458 |
| `explicit.stat_3033371881@T1` | 0.86756 |
| `explicit.stat_3484657501@T1` | -0.71342 |
| `explicit.stat_986397080@T2` | -0.67375 |
| `explicit.stat_4080418644@T1` | -0.65635 |
| `explicit.stat_2923486259@T1` | -0.63163 |
| `explicit.stat_915769802@T2` | -0.62243 |
| `explicit.stat_124859000@T2` | -0.61265 |
| `explicit.stat_4080418644@T2` | -0.61145 |
| `explicit.stat_3301100256@T1` | -0.60959 |
| `explicit.stat_3299347043@T2` | -0.56614 |

### armour.helmet — n=29518, R²=-0.9103

intercept: `4.0121`  ·  log_price: True  ·  ilvl: `-0.04958`  ·  n_mods: `-0.10209`  ·  n_top_tier: `0.47108`  ·  corrupted: `0.66044`  ·  n_sockets: `0.13658`  ·  quality: `0.04146`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.75944 |
| `explicit.stat_2339757871@T1` | -1.74400 |
| `explicit.stat_53045048@T2` | -1.01103 |
| `explicit.stat_3917489142@T2` | -0.83403 |
| `explicit.stat_3261801346@T1` | -0.82791 |
| `explicit.stat_53045048@T1` | -0.82352 |
| `explicit.stat_1999113824@T1` | -0.81263 |
| `explicit.stat_3321629045@T2` | -0.73034 |
| `explicit.stat_1263695895@T1` | -0.71719 |
| `explicit.stat_3261801346@T2` | -0.67304 |
| `explicit.stat_1263695895@T2` | -0.65560 |
| `explicit.stat_2162097452@T2` | -0.61843 |

### armour.boots — n=27682, R²=-1.3922

intercept: `4.2063`  ·  log_price: True  ·  ilvl: `-0.05110`  ·  n_mods: `-0.04143`  ·  n_top_tier: `0.66530`  ·  corrupted: `0.14206`  ·  n_sockets: `0.00826`  ·  quality: `0.03075`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.49391 |
| `explicit.stat_3299347043@T1` | -0.94656 |
| `explicit.stat_2923486259@T2` | -0.90128 |
| `explicit.stat_3917489142@T2` | -0.89858 |
| `explicit.stat_2339757871@T1` | -0.89831 |
| `explicit.stat_4052037485@T2` | -0.86015 |
| `explicit.stat_3917489142@T1` | -0.81102 |
| `explicit.stat_53045048@T1` | -0.79275 |
| `explicit.stat_1062208444@T2` | -0.78061 |
| `explicit.stat_2160282525@T1` | -0.77417 |
| `explicit.stat_4080418644@T1` | -0.75528 |
| `explicit.stat_3362812763@T1` | -0.74869 |

### armour.gloves — n=27000, R²=-1.1805

intercept: `3.9291`  ·  log_price: True  ·  ilvl: `-0.05235`  ·  n_mods: `-0.04952`  ·  n_top_tier: `0.50884`  ·  corrupted: `0.08854`  ·  n_sockets: `0.24835`  ·  quality: `0.03639`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.26416 |
| `explicit.stat_3484657501@T2` | -1.36420 |
| `rune.stat_836936635` | 1.15007 |
| `explicit.stat_803737631@T2` | -1.00827 |
| `explicit.stat_3484657501@T1` | -0.91020 |
| `explicit.stat_9187492@T1` | 0.87945 |
| `explicit.stat_803737631@T1` | -0.84442 |
| `explicit.stat_3321629045@T2` | -0.79620 |
| `explicit.stat_3917489142@T2` | -0.79416 |
| `explicit.stat_9187492@T2` | -0.78181 |
| `explicit.stat_2923486259@T1` | -0.78105 |
| `explicit.stat_3032590688@T1` | -0.77413 |

### weapon.wand — n=17535, R²=-2.2178

intercept: `3.7827`  ·  log_price: True  ·  ilvl: `-0.04682`  ·  n_mods: `-0.01683`  ·  n_top_tier: `0.19931`  ·  corrupted: `0.00103`  ·  n_sockets: `0.03092`  ·  quality: `0.00094`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.19508 |
| `rune.stat_124131830` | -3.08923 |
| `explicit.stat_2254480358@T1` | 3.07744 |
| `explicit.stat_591105508@T1` | 2.12939 |
| `explicit.stat_124131830@T1` | 2.11850 |
| `explicit.stat_4226189338@T1` | 2.09601 |
| `explicit.stat_736967255@T2` | 1.34581 |
| `crafted.stat_124131830` | 1.18392 |
| `explicit.stat_2254480358@T2` | 1.14317 |
| `explicit.stat_2768835289@T2` | 1.06921 |
| `explicit.stat_4226189338@T2` | 0.58408 |
| `explicit.stat_737908626@T1` | -0.29663 |

### weapon.bow — n=14222, R²=-1.9572

intercept: `3.4805`  ·  log_price: True  ·  ilvl: `-0.04196`  ·  n_mods: `-0.03427`  ·  n_top_tier: `0.63644`  ·  corrupted: `-0.07273`  ·  n_sockets: `-0.00913`  ·  quality: `0.03204`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.10020 |
| `explicit.stat_1202301673@T1` | 1.57903 |
| `crafted.stat_3035140377` | 1.30973 |
| `explicit.stat_1263695895@T1` | -0.74622 |
| `explicit.stat_1509134228@T1` | -0.72316 |
| `explicit.stat_1037193709@T1` | -0.70603 |
| `explicit.stat_1263695895@T2` | -0.70494 |
| `explicit.stat_1368271171@T2` | -0.70388 |
| `explicit.stat_3695891184@T2` | -0.69214 |
| `explicit.stat_3695891184@T1` | -0.68195 |
| `explicit.stat_2694482655@T2` | -0.67930 |
| `explicit.stat_821021828@T2` | -0.67835 |

### weapon.crossbow — n=13447, R²=-1.9839

intercept: `3.6037`  ·  log_price: True  ·  ilvl: `-0.04433`  ·  n_mods: `-0.01132`  ·  n_top_tier: `0.77612`  ·  corrupted: `-0.01874`  ·  n_sockets: `0.01548`  ·  quality: `0.01042`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -2.04424 |
| `explicit.stat_1980802737@T2` | -1.97954 |
| `explicit.stat_709508406@T1` | 1.48449 |
| `explicit.stat_2250681686` | 1.33480 |
| `explicit.stat_1202301673@T1` | 1.18943 |
| `explicit.stat_1980802737` | 1.17967 |
| `explicit.stat_1202301673@T2` | -0.97906 |
| `explicit.stat_1263695895@T2` | -0.93087 |
| `explicit.stat_1263695895@T1` | -0.89100 |
| `crafted.stat_3035140377` | 0.89021 |
| `explicit.stat_669069897@T1` | -0.83779 |
| `explicit.stat_1037193709@T2` | -0.83115 |

### flask.charm — n=11673, R²=-0.5205

intercept: `0.0005`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.30255`  ·  corrupted: `2.08720`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.36181 |
| `explicit.stat_1056492907` | 3.52783 |
| `explicit.stat_828533480@T2` | -2.30256 |
| `explicit.stat_1120862500@T2` | -2.30255 |
| `explicit.stat_3196823591@T2` | -2.30254 |
| `explicit.stat_1873752457@T2` | -2.30254 |
| `explicit.stat_2676834156@T2` | -2.30254 |
| `explicit.stat_1366840608@T2` | -2.30254 |
| `explicit.stat_2541588185@T2` | -2.30254 |
| `explicit.stat_388617051@T2` | -2.30254 |
| `explicit.stat_828533480@T1` | -2.30253 |
| `explicit.stat_1873752457@T1` | -2.30253 |

### weapon.warstaff — n=7955, R²=-0.5316

intercept: `-3.5729`  ·  log_price: True  ·  ilvl: `0.04995`  ·  n_mods: `-0.12253`  ·  n_top_tier: `0.59404`  ·  corrupted: `0.23615`  ·  n_sockets: `0.07935`  ·  quality: `0.06151`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.28111 |
| `explicit.stat_1037193709@T1` | 1.21416 |
| `explicit.stat_328541901@T1` | -0.97927 |
| `explicit.stat_328541901@T2` | -0.93107 |
| `crafted.stat_210067635@T2` | 0.85942 |
| `explicit.stat_55876295@T2` | -0.75150 |
| `explicit.stat_55876295@T1` | -0.68939 |
| `explicit.stat_691932474@T2` | -0.67897 |
| `explicit.stat_1037193709@T2` | -0.67255 |
| `explicit.stat_3336890334@T2` | -0.65150 |
| `explicit.stat_791928121@T2` | -0.62870 |
| `desecrated.stat_9187492` | 0.62424 |

### weapon.sceptre — n=7319, R²=-0.4547

intercept: `-11.7115`  ·  log_price: True  ·  ilvl: `0.14796`  ·  n_mods: `-0.06025`  ·  n_top_tier: `0.55697`  ·  corrupted: `0.39155`  ·  n_sockets: `0.19807`  ·  quality: `0.07141`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.33360 |
| `explicit.stat_2162097452@T2` | 1.31411 |
| `explicit.stat_4080418644@T1` | -1.22937 |
| `explicit.stat_1263695895@T1` | -1.07272 |
| `explicit.stat_1263695895@T2` | -1.02806 |
| `explicit.stat_1574590649@T2` | -0.95860 |
| `explicit.stat_2347036682@T2` | -0.79602 |
| `explicit.stat_289128254@T2` | -0.73380 |
| `explicit.stat_1050105434@T2` | -0.65845 |
| `explicit.stat_4080418644@T2` | -0.65701 |
| `explicit.stat_3639275092@T2` | -0.58199 |
| `explicit.stat_2854751904@T2` | -0.57563 |

### weapon.staff — n=7310, R²=-0.5379

intercept: `-6.6988`  ·  log_price: True  ·  ilvl: `0.08565`  ·  n_mods: `-0.05762`  ·  n_top_tier: `0.36181`  ·  corrupted: `-0.02346`  ·  n_sockets: `0.20048`  ·  quality: `0.06237`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 1.92727 |
| `explicit.stat_124131830@T1` | 1.85489 |
| `rune.stat_124131830` | 1.51494 |
| `explicit.stat_1545858329@T1` | 1.41834 |
| `explicit.stat_1600707273@T1` | 1.26389 |
| `explicit.stat_2254480358@T1` | 1.15692 |
| `explicit.stat_591105508@T1` | 1.01179 |
| `explicit.stat_4226189338@T2` | 0.95970 |
| `explicit.stat_2768835289@T2` | 0.88077 |
| `explicit.stat_3962278098@T2` | 0.76057 |
| `explicit.stat_2231156303@T2` | 0.73206 |
| `explicit.stat_3291658075@T2` | 0.68719 |

### weapon.spear — n=6108, R²=-0.6479

intercept: `-3.9176`  ·  log_price: True  ·  ilvl: `0.05162`  ·  n_mods: `-0.01654`  ·  n_top_tier: `0.53727`  ·  corrupted: `-0.05247`  ·  n_sockets: `0.09390`  ·  quality: `0.09328`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.97267 |
| `explicit.stat_1202301673@T1` | 2.53447 |
| `explicit.stat_9187492@T1` | 2.32989 |
| `crafted.stat_3035140377` | 1.26278 |
| `explicit.stat_1509134228@T1` | 0.85152 |
| `explicit.stat_210067635@T1` | 0.80839 |
| `explicit.stat_1263695895@T2` | -0.75288 |
| `crafted.stat_518292764` | 0.72095 |
| `explicit.stat_55876295@T1` | -0.65912 |
| `explicit.stat_55876295@T2` | -0.61112 |
| `explicit.stat_1509134228@T2` | -0.53845 |
| `explicit.stat_791928121@T2` | -0.52672 |

### armour.focus — n=4986, R²=-0.4616

intercept: `-9.7586`  ·  log_price: True  ·  ilvl: `0.12190`  ·  n_mods: `-0.05416`  ·  n_top_tier: `0.90812`  ·  corrupted: `0.72838`  ·  n_sockets: `0.39327`  ·  quality: `0.07337`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 4.62500 |
| `crafted.stat_2974417149@T1` | 1.44408 |
| `explicit.stat_4220027924@T2` | -1.30716 |
| `crafted.stat_737908626@T2` | -1.25810 |
| `explicit.stat_3962278098@T2` | -1.07231 |
| `explicit.stat_4220027924@T1` | -1.07078 |
| `explicit.stat_2923486259@T1` | -1.03861 |
| `explicit.stat_3291658075@T1` | -1.02904 |
| `explicit.stat_736967255@T2` | -1.02335 |
| `explicit.stat_2974417149@T1` | -0.96616 |
| `explicit.stat_737908626@T2` | -0.95677 |
| `explicit.stat_3962278098@T1` | -0.94667 |

### armour.quiver — n=4669, R²=-0.4293

intercept: `-9.5758`  ·  log_price: True  ·  ilvl: `0.11740`  ·  n_mods: `-0.02982`  ·  n_top_tier: `0.79586`  ·  corrupted: `0.76737`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.21999 |
| `explicit.stat_2463230181@T1` | 2.45319 |
| `explicit.stat_2321178454@T2` | -1.25375 |
| `explicit.stat_2463230181@T2` | 1.18816 |
| `explicit.stat_681332047@T2` | -1.10866 |
| `explicit.stat_1573130764@T1` | -1.02274 |
| `explicit.stat_1573130764@T2` | -1.01333 |
| `explicit.stat_4067062424@T1` | -0.99660 |
| `explicit.stat_3261801346@T1` | -0.99374 |
| `explicit.stat_2194114101@T2` | -0.89866 |
| `explicit.stat_2321178454@T1` | -0.82597 |
| `explicit.stat_1368271171@T2` | -0.81412 |

### armour.shield — n=4083, R²=-0.5684

intercept: `-7.5264`  ·  log_price: True  ·  ilvl: `0.09741`  ·  n_mods: `-0.05434`  ·  n_top_tier: `0.62819`  ·  corrupted: `0.16871`  ·  n_sockets: `0.09560`  ·  quality: `0.04930`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.99578 |
| `explicit.stat_1011760251@T1` | -1.54132 |
| `explicit.stat_2339757871@T1` | -1.22581 |
| `explicit.stat_1011760251@T2` | -1.14061 |
| `explicit.stat_328541901@T1` | -0.92146 |
| `explicit.stat_2481353198@T2` | -0.91628 |
| `explicit.stat_2481353198@T1` | -0.85304 |
| `explicit.stat_4095671657@T1` | -0.83767 |
| `explicit.stat_3321629045@T2` | -0.82677 |
| `explicit.stat_2881298780@T1` | -0.82316 |
| `explicit.stat_328541901@T2` | -0.79739 |
| `explicit.stat_3771516363@T1` | -0.78095 |

### weapon.twomace — n=3766, R²=-0.5157

intercept: `-8.5228`  ·  log_price: True  ·  ilvl: `0.11103`  ·  n_mods: `-0.09578`  ·  n_top_tier: `0.42350`  ·  corrupted: `0.75547`  ·  n_sockets: `0.13785`  ·  quality: `0.04022`

| stat_id | coef |
|---|---|
| `desecrated.stat_1509134228@T1` | 2.22398 |
| `desecrated.stat_210067635@T1` | -1.92864 |
| `explicit.stat_1037193709@T1` | -1.42424 |
| `explicit.stat_3336890334@T1` | -1.20118 |
| `crafted.stat_3035140377` | 1.10553 |
| `explicit.stat_1263695895@T1` | -0.76914 |
| `explicit.stat_387439868@T2` | -0.76610 |
| `explicit.stat_1037193709@T2` | -0.73870 |
| `explicit.stat_1263695895@T2` | -0.71356 |
| `explicit.stat_3695891184@T1` | -0.67634 |
| `explicit.stat_210067635@T2` | 0.65622 |
| `explicit.stat_518292764@T2` | -0.64907 |

## Coverage (listings per base)

- … **Sapphire** — 21487 listings (21457 priced) [0.3–7553463.8 ex]
- … **Emerald** — 21228 listings (21200 priced) [0.3–7553463.8 ex]
- … **Ruby** — 16227 listings (16213 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 8970 listings (8961 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 7261 listings (7251 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 7102 listings (7089 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 6955 listings (6948 priced) [0.2–19945827.9 ex]
- … **Stellar Amulet** — 6651 listings (6647 priced) [0.3–91750808.2 ex]
- … **Gold Amulet** — 6647 listings (6637 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 6500 listings (6489 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5580 listings (5565 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5437 listings (5431 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 5217 listings (5213 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5208 listings (5205 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 4738 listings (4724 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4671 listings (4666 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4576 listings (4569 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4526 listings (4524 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4522 listings (4516 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4481 listings (4475 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4370 listings (4365 priced) [0.3–4275054.0 ex]
- … **Obliterator Bow** — 4268 listings (4255 priced) [0.3–42622633798.0 ex]
- … **Heavy Belt** — 4227 listings (4225 priced) [0.3–2608914286.6 ex]
- … **Pearl Ring** — 4190 listings (4185 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 4120 listings (4120 priced) [0.3–123132003.2 ex]

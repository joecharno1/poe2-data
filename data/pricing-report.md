# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-17T00:07:02+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **562778** (561239 priced in exalted)
- Distinct bases: 987 · distinct mods: 3187 · mod rows: 2664672
- Sold signals: **25527** sold · 317870 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-16T23:58:29+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.54** (median |log error| 3.2003)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×63.47 · ±30% 5% · n=81452
- Premium segment (60ex+): skill **+0.13** · typical error ×306.71 · ±30% 0% · n=55008

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 11496 | ×54.52 | 22% | +0.03 | +0.05 |
| jewel | 10696 | ×10.66 | 4% | +0.07 | +0.10 |
| accessory.amulet | 10484 | ×43.25 | 20% | +0.03 | +0.04 |
| accessory.belt | 7808 | ×20.33 | 17% | +0.05 | +0.08 |
| armour.chest | 7629 | ×22.32 | 18% | +0.08 | +0.10 |
| armour.helmet | 7423 | ×25.19 | 14% | +0.08 | +0.10 |
| armour.boots | 6934 | ×35.74 | 20% | +0.08 | +0.11 |
| armour.gloves | 6776 | ×33.06 | 13% | +0.09 | +0.12 |
| other | 6346 | ×1.92 | 43% | +0.10 | +0.17 |
| weapon.wand | 4231 | ×36.95 | 15% | +0.09 | +0.10 |
| weapon.bow | 3329 | ×34.40 | 15% | +0.12 | +0.14 |
| weapon.crossbow | 3141 | ×34.06 | 15% | +0.10 | +0.13 |
| weapon.warstaff | 2005 | ×32.24 | 8% | +0.14 | +0.13 |
| weapon.staff | 1879 | ×52.72 | 8% | +0.11 | +0.11 |
| weapon.sceptre | 1851 | ×39.94 | 4% | +0.17 | +0.17 |
| weapon.spear | 1460 | ×45.04 | 15% | +0.08 | +0.10 |
| armour.focus | 1242 | ×26.62 | 6% | +0.15 | +0.16 |
| armour.quiver | 1185 | ×29.08 | 7% | +0.12 | +0.13 |
| flask.charm | 1012 | ×30.00 | 32% | +0.05 | +0.07 |
| armour.shield | 961 | ×22.74 | 8% | +0.04 | +0.05 |
| weapon.twomace | 886 | ×10.40 | 11% | +0.07 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=58579, R²=-0.9157

intercept: `-1.8216`  ·  log_price: True  ·  ilvl: `0.02694`  ·  n_mods: `0.75116`  ·  n_top_tier: `-0.25916`  ·  corrupted: `0.27465`  ·  quality: `0.22190`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.81475 |
| `explicit.stat_2301718443@T1` | 3.19246 |
| `explicit.stat_627767961@T1` | -2.11505 |
| `explicit.stat_1805182458@T1` | -1.90289 |
| `explicit.stat_1697951953@T1` | -1.75647 |
| `explicit.stat_491450213@T1` | 1.72221 |
| `explicit.stat_3166958180@T1` | -1.70976 |
| `explicit.stat_3780644166@T1` | -1.69207 |
| `explicit.stat_3485067555@T1` | 1.58202 |
| `explicit.stat_239367161@T1` | -1.52996 |
| `explicit.stat_3668351662@T1` | -1.46613 |
| `explicit.stat_1315743832@T1` | -1.41122 |

### other — n=54030, R²=-0.6498

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.34734`  ·  corrupted: `0.29401`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.37468 |
| `explicit.stat_2974417149@T1` | 0.34498 |
| `explicit.stat_3299347043@T1` | -0.30354 |
| `implicit.stat_3879011313` | 0.23030 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_2106365538@T1` | -0.15086 |
| `explicit.stat_2482852589@T1` | -0.13790 |
| `explicit.stat_1050105434@T1` | -0.12411 |
| `explicit.stat_2968503605@T1` | 0.10948 |
| `implicit.stat_2923486259` | -0.09138 |
| `pseudo.total_chaos_res` | 0.09138 |

### accessory.ring — n=52409, R²=-2.0357

intercept: `3.4749`  ·  log_price: True  ·  ilvl: `-0.04304`  ·  n_mods: `-0.00004`  ·  n_top_tier: `1.07644`  ·  corrupted: `0.02264`  ·  n_sockets: `2.18724`  ·  quality: `0.07141`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -1.11339 |
| `explicit.stat_1368271171@T2` | -1.10465 |
| `explicit.stat_1573130764@T1` | -1.10447 |
| `explicit.stat_803737631@T1` | -1.10183 |
| `explicit.stat_3325883026@T1` | -1.10026 |
| `explicit.stat_4220027924@T2` | -1.09853 |
| `explicit.stat_2231156303@T2` | -1.09849 |
| `explicit.stat_2144192055@T1` | -1.09740 |
| `explicit.stat_1263695895@T2` | -1.09689 |
| `explicit.stat_4067062424@T2` | -1.09602 |
| `explicit.stat_3291658075@T2` | -1.09549 |
| `explicit.stat_1263695895@T1` | -1.09464 |

### accessory.amulet — n=48025, R²=-2.1408

intercept: `3.6411`  ·  log_price: True  ·  ilvl: `-0.04457`  ·  n_mods: `-0.02708`  ·  n_top_tier: `1.09106`  ·  corrupted: `0.05987`  ·  n_sockets: `-0.11784`  ·  quality: `-0.00108`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.24233 |
| `explicit.stat_587431675@T2` | -1.17972 |
| `explicit.stat_2974417149@T1` | -1.17285 |
| `explicit.stat_472520716@T2` | -1.16076 |
| `explicit.stat_2974417149@T2` | -1.15577 |
| `explicit.stat_803737631@T1` | -1.15152 |
| `explicit.stat_803737631@T2` | -1.14577 |
| `explicit.stat_1050105434@T2` | -1.14024 |
| `explicit.stat_2866361420@T2` | -1.13805 |
| `explicit.stat_2901986750@T1` | -1.13041 |
| `explicit.stat_3917489142@T2` | -1.12432 |
| `explicit.stat_2866361420@T1` | -1.12418 |

### accessory.belt — n=36110, R²=-1.5371

intercept: `4.6728`  ·  log_price: True  ·  ilvl: `-0.05493`  ·  n_mods: `-0.05985`  ·  n_top_tier: `0.69035`  ·  corrupted: `1.21002`  ·  n_sockets: `0.42467`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -0.95972 |
| `explicit.stat_3299347043@T2` | -0.80436 |
| `explicit.stat_2881298780@T1` | -0.78380 |
| `explicit.stat_4220027924@T2` | -0.76837 |
| `explicit.stat_1389754388@T1` | -0.76167 |
| `explicit.stat_809229260@T2` | -0.74924 |
| `explicit.stat_51994685@T1` | -0.74247 |
| `explicit.stat_644456512@T1` | -0.71218 |
| `explicit.stat_915769802@T2` | -0.70998 |
| `explicit.stat_1671376347@T2` | -0.70937 |
| `explicit.stat_51994685@T2` | -0.69549 |
| `explicit.stat_3372524247@T2` | -0.69505 |

### armour.chest — n=35910, R²=-1.6314

intercept: `3.6996`  ·  log_price: True  ·  ilvl: `-0.04498`  ·  n_mods: `-0.03120`  ·  n_top_tier: `0.48684`  ·  corrupted: `0.09827`  ·  n_sockets: `0.05573`  ·  quality: `0.05840`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.67412 |
| `explicit.stat_3981240776@T1` | 1.03504 |
| `explicit.stat_3033371881@T1` | 0.88927 |
| `explicit.stat_986397080@T2` | -0.64326 |
| `explicit.stat_986397080@T1` | -0.61071 |
| `explicit.stat_4015621042@T1` | -0.56152 |
| `explicit.stat_2339757871@T2` | -0.55938 |
| `explicit.stat_3484657501@T1` | -0.55503 |
| `explicit.stat_4080418644@T2` | -0.53206 |
| `explicit.stat_915769802@T2` | -0.52943 |
| `explicit.stat_2451402625@T2` | -0.52920 |
| `explicit.stat_4080418644@T1` | -0.52814 |

### armour.helmet — n=34851, R²=-1.4439

intercept: `3.6867`  ·  log_price: True  ·  ilvl: `-0.04620`  ·  n_mods: `-0.05314`  ·  n_top_tier: `0.37329`  ·  corrupted: `0.71032`  ·  n_sockets: `0.14659`  ·  quality: `0.04461`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.93877 |
| `crafted.stat_3917489142@T1` | 1.03448 |
| `explicit.stat_1263695895@T1` | -0.74178 |
| `explicit.stat_3917489142@T2` | -0.69718 |
| `explicit.stat_1263695895@T2` | -0.58575 |
| `explicit.stat_1999113824@T1` | -0.56121 |
| `explicit.stat_2162097452@T2` | -0.55494 |
| `explicit.stat_3321629045@T2` | -0.51382 |
| `explicit.stat_3917489142@T1` | -0.51148 |
| `explicit.stat_1999113824@T2` | -0.49507 |
| `explicit.stat_2162097452@T1` | 0.47999 |
| `explicit.stat_587431675@T2` | -0.45687 |

### armour.boots — n=32650, R²=-1.7259

intercept: `3.5212`  ·  log_price: True  ·  ilvl: `-0.04305`  ·  n_mods: `-0.02284`  ·  n_top_tier: `0.66831`  ·  corrupted: `0.00675`  ·  n_sockets: `0.02195`  ·  quality: `0.04838`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.25621 |
| `explicit.stat_2250533757@T1` | 1.39065 |
| `explicit.stat_3299347043@T1` | -0.85218 |
| `explicit.stat_3917489142@T2` | -0.82766 |
| `explicit.stat_2339757871@T1` | -0.80081 |
| `explicit.stat_3917489142@T1` | -0.74230 |
| `explicit.stat_2160282525@T1` | -0.72117 |
| `explicit.stat_2923486259@T2` | -0.71966 |
| `explicit.stat_53045048@T1` | -0.70862 |
| `explicit.stat_1671376347@T2` | -0.70554 |
| `explicit.stat_3484657501@T2` | -0.70019 |
| `explicit.stat_4052037485@T2` | -0.69314 |

### armour.gloves — n=31729, R²=-1.6198

intercept: `3.6317`  ·  log_price: True  ·  ilvl: `-0.04592`  ·  n_mods: `-0.02454`  ·  n_top_tier: `0.54586`  ·  corrupted: `0.01185`  ·  n_sockets: `0.08476`  ·  quality: `0.04206`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | -1.05499 |
| `explicit.stat_2923486259@T1` | -0.96448 |
| `rune.stat_836936635` | 0.92808 |
| `explicit.stat_1671376347@T1` | 0.90314 |
| `explicit.stat_9187492@T1` | 0.86761 |
| `explicit.stat_9187492@T2` | -0.80368 |
| `explicit.stat_2339757871@T1` | 0.80139 |
| `explicit.stat_4052037485@T1` | -0.80026 |
| `explicit.stat_3321629045@T2` | -0.79939 |
| `explicit.stat_3484657501@T2` | -0.70564 |
| `explicit.stat_803737631@T2` | -0.69180 |
| `explicit.stat_1999113824@T2` | -0.67287 |

### weapon.wand — n=19848, R²=-2.0495

intercept: `3.5706`  ·  log_price: True  ·  ilvl: `-0.04408`  ·  n_mods: `-0.04326`  ·  n_top_tier: `0.51427`  ·  corrupted: `0.00228`  ·  n_sockets: `0.11753`  ·  quality: `0.01102`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.61237 |
| `explicit.stat_2254480358@T1` | 2.27884 |
| `explicit.stat_1545858329@T1` | 2.21960 |
| `explicit.stat_4226189338@T1` | 1.89221 |
| `explicit.stat_591105508@T1` | 1.82240 |
| `explicit.stat_124131830@T1` | 1.75028 |
| `explicit.stat_736967255@T2` | 1.58290 |
| `crafted.stat_124131830` | 1.18205 |
| `explicit.stat_1600707273@T1` | 0.92771 |
| `explicit.stat_4226189338@T2` | 0.88913 |
| `explicit.stat_2254480358@T2` | 0.86986 |
| `explicit.stat_1263695895@T1` | -0.72255 |

### weapon.bow — n=15903, R²=-1.8587

intercept: `3.6734`  ·  log_price: True  ·  ilvl: `-0.04340`  ·  n_mods: `-0.07184`  ·  n_top_tier: `0.61109`  ·  corrupted: `0.23650`  ·  n_sockets: `0.02865`  ·  quality: `0.03416`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.04085 |
| `desecrated.stat_210067635@T1` | -1.67063 |
| `crafted.stat_3035140377` | 1.48600 |
| `explicit.stat_1202301673@T1` | 1.44575 |
| `explicit.stat_2463230181@T2` | -1.16301 |
| `explicit.stat_1263695895@T1` | -0.99062 |
| `explicit.stat_1263695895@T2` | -0.98413 |
| `explicit.stat_518292764@T2` | -0.94141 |
| `explicit.stat_2463230181@T1` | -0.80393 |
| `explicit.stat_1940865751@T1` | 0.78455 |
| `explicit.stat_3695891184@T2` | -0.77239 |
| `explicit.stat_1037193709@T1` | -0.73714 |

### weapon.crossbow — n=14930, R²=-1.7798

intercept: `3.8335`  ·  log_price: True  ·  ilvl: `-0.04628`  ·  n_mods: `-0.06874`  ·  n_top_tier: `0.73587`  ·  corrupted: `0.04254`  ·  n_sockets: `0.05881`  ·  quality: `0.01780`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.88426 |
| `explicit.stat_2250681686@T2` | -1.33353 |
| `explicit.stat_1202301673@T1` | 1.20420 |
| `explicit.stat_1980802737` | 1.19004 |
| `explicit.stat_1509134228@T2` | -0.93062 |
| `explicit.stat_1263695895@T2` | -0.92071 |
| `explicit.stat_1263695895@T1` | -0.91725 |
| `explicit.stat_2694482655@T1` | -0.88242 |
| `crafted.stat_3035140377` | 0.87041 |
| `explicit.stat_709508406@T2` | -0.85310 |
| `explicit.stat_1940865751@T2` | -0.84471 |
| `explicit.stat_2250681686` | 0.82990 |

### flask.charm — n=14859, R²=-0.559

intercept: `0.0545`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `2.42857`  ·  corrupted: `1.75430`  ·  quality: `0.00024`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.71325 |
| `explicit.stat_1056492907` | 3.11909 |
| `explicit.stat_828533480@T2` | -2.42860 |
| `explicit.stat_1873752457@T2` | -2.42857 |
| `explicit.stat_1120862500@T2` | -2.42856 |
| `explicit.stat_828533480@T1` | -2.42856 |
| `explicit.stat_388617051@T2` | -2.42856 |
| `explicit.stat_3196823591@T2` | -2.42856 |
| `explicit.stat_2676834156@T2` | -2.42855 |
| `explicit.stat_2365392475@T2` | -2.42855 |
| `explicit.stat_1873752457@T1` | -2.42854 |
| `explicit.stat_1366840608@T2` | -2.42852 |

### weapon.warstaff — n=9559, R²=-0.3859

intercept: `-9.2915`  ·  log_price: True  ·  ilvl: `0.12691`  ·  n_mods: `-0.19737`  ·  n_top_tier: `0.39668`  ·  corrupted: `0.16832`  ·  n_sockets: `0.17840`  ·  quality: `0.06062`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.06833 |
| `explicit.stat_1037193709@T1` | 1.04043 |
| `rune.stat_243313994` | 0.96076 |
| `explicit.stat_328541901@T1` | -0.90296 |
| `explicit.stat_328541901@T2` | -0.89160 |
| `desecrated.stat_9187492` | 0.72936 |
| `explicit.stat_9187492@T1` | 0.71698 |
| `explicit.stat_1940865751@T1` | -0.49913 |
| `explicit.stat_748522257@T2` | 0.49256 |
| `explicit.stat_691932474@T2` | -0.48979 |
| `explicit.stat_1368271171@T1` | -0.47481 |
| `explicit.stat_1037193709@T2` | -0.44753 |

### weapon.staff — n=8919, R²=-0.4145

intercept: `-13.1612`  ·  log_price: True  ·  ilvl: `0.17229`  ·  n_mods: `-0.15044`  ·  n_top_tier: `0.47085`  ·  corrupted: `0.43901`  ·  n_sockets: `0.25084`  ·  quality: `0.04245`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.03819 |
| `explicit.stat_4226189338@T1` | 1.62007 |
| `explicit.stat_591105508@T1` | 1.33013 |
| `rune.stat_124131830` | 1.01423 |
| `explicit.stat_293638271@T2` | -1.00786 |
| `explicit.stat_124131830@T2` | 0.88836 |
| `explicit.stat_2254480358@T2` | 0.88632 |
| `explicit.stat_3962278098@T2` | 0.86949 |
| `explicit.stat_124131830@T1` | 0.83274 |
| `explicit.stat_2505884597@T2` | -0.62430 |
| `explicit.stat_2231156303@T2` | 0.60310 |
| `explicit.stat_2968503605@T1` | -0.58829 |

### weapon.sceptre — n=8823, R²=-0.3598

intercept: `-17.9877`  ·  log_price: True  ·  ilvl: `0.23040`  ·  n_mods: `-0.08777`  ·  n_top_tier: `0.32902`  ·  corrupted: `0.46156`  ·  n_sockets: `0.29407`  ·  quality: `0.04228`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.87882 |
| `explicit.stat_2162097452@T2` | 1.70079 |
| `explicit.stat_1250712710@T2` | 1.21890 |
| `explicit.stat_3057012405@T1` | 0.99630 |
| `explicit.stat_1263695895@T1` | -0.95633 |
| `explicit.stat_1263695895@T2` | -0.88871 |
| `explicit.stat_1574590649@T1` | -0.80310 |
| `explicit.stat_2347036682@T1` | 0.71807 |
| `explicit.stat_849987426@T1` | 0.68750 |
| `explicit.stat_2347036682@T2` | -0.64694 |
| `explicit.stat_101878827@T1` | 0.64273 |
| `explicit.stat_289128254@T2` | -0.61074 |

### weapon.spear — n=7224, R²=-0.4385

intercept: `-11.0033`  ·  log_price: True  ·  ilvl: `0.15583`  ·  n_mods: `-0.14375`  ·  n_top_tier: `0.74823`  ·  corrupted: `-0.26929`  ·  n_sockets: `0.27311`  ·  quality: `0.06890`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.77532 |
| `explicit.stat_1202301673@T1` | 1.69820 |
| `explicit.stat_1509134228@T1` | 1.67193 |
| `explicit.stat_9187492@T1` | 1.39006 |
| `crafted.stat_3035140377` | 1.11212 |
| `explicit.stat_1037193709@T1` | -1.09408 |
| `explicit.stat_1263695895@T2` | -0.85536 |
| `explicit.stat_4080418644@T2` | -0.84138 |
| `explicit.stat_691932474@T1` | -0.82389 |
| `explicit.stat_1940865751@T2` | -0.82222 |
| `explicit.stat_55876295@T1` | -0.77633 |
| `explicit.stat_3261801346@T1` | -0.77554 |

### armour.focus — n=5936, R²=-0.3868

intercept: `-11.8916`  ·  log_price: True  ·  ilvl: `0.15647`  ·  n_mods: `-0.17898`  ·  n_top_tier: `0.82796`  ·  corrupted: `0.48164`  ·  n_sockets: `0.45224`  ·  quality: `0.07224`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 9.42247 |
| `explicit.stat_4220027924@T2` | -1.36394 |
| `explicit.stat_3962278098@T1` | -1.29945 |
| `explicit.stat_3291658075@T1` | -1.03588 |
| `explicit.stat_2231156303@T2` | -0.97799 |
| `explicit.stat_2891184298@T2` | -0.91182 |
| `explicit.stat_2339757871@T2` | -0.90802 |
| `explicit.stat_4052037485@T2` | -0.86052 |
| `explicit.stat_4220027924@T1` | -0.84193 |
| `explicit.stat_2339757871@T1` | -0.84137 |
| `explicit.stat_737908626@T2` | -0.82755 |
| `explicit.stat_736967255@T2` | -0.78710 |

### armour.quiver — n=5561, R²=-0.3306

intercept: `-14.2203`  ·  log_price: True  ·  ilvl: `0.17477`  ·  n_mods: `-0.12954`  ·  n_top_tier: `0.76422`  ·  corrupted: `0.83989`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.16880 |
| `explicit.stat_2463230181@T1` | 2.93230 |
| `explicit.stat_2463230181@T2` | 1.40531 |
| `explicit.stat_1573130764@T1` | -1.20767 |
| `explicit.stat_681332047@T2` | -1.19499 |
| `explicit.stat_4067062424@T1` | -1.01574 |
| `explicit.stat_2321178454@T2` | -1.00217 |
| `explicit.stat_803737631@T2` | -0.96714 |
| `explicit.stat_3261801346@T1` | -0.85855 |
| `explicit.stat_2194114101@T2` | -0.80132 |
| `explicit.stat_1573130764@T2` | -0.80097 |
| `explicit.stat_2321178454@T1` | -0.76187 |

### armour.shield — n=4840, R²=-0.5062

intercept: `-10.1766`  ·  log_price: True  ·  ilvl: `0.13718`  ·  n_mods: `-0.10542`  ·  n_top_tier: `0.72603`  ·  corrupted: `-0.30313`  ·  n_sockets: `0.27295`  ·  quality: `0.06284`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.36006 |
| `explicit.stat_2481353198@T2` | -1.26112 |
| `explicit.stat_2339757871@T1` | -1.24623 |
| `explicit.stat_328541901@T1` | -1.21075 |
| `explicit.stat_3033371881@T2` | -1.12929 |
| `explicit.stat_3484657501@T2` | -1.10759 |
| `explicit.stat_328541901@T2` | -1.09035 |
| `explicit.stat_3321629045@T2` | -1.08103 |
| `explicit.stat_2481353198@T1` | -1.03433 |
| `explicit.stat_4095671657@T1` | -0.98917 |
| `explicit.stat_2901986750@T1` | -0.96122 |
| `explicit.stat_2923486259@T2` | -0.95617 |

### weapon.twomace — n=4442, R²=-0.4921

intercept: `-9.5194`  ·  log_price: True  ·  ilvl: `0.13078`  ·  n_mods: `-0.18619`  ·  n_top_tier: `0.38606`  ·  corrupted: `-0.07172`  ·  n_sockets: `0.18768`  ·  quality: `0.05763`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.95920 |
| `desecrated.stat_1509134228@T1` | 2.68207 |
| `explicit.stat_1037193709@T1` | -1.67285 |
| `explicit.stat_3336890334@T1` | -0.97286 |
| `crafted.stat_3035140377` | 0.92185 |
| `explicit.stat_1037193709@T2` | -0.88102 |
| `explicit.stat_387439868@T2` | -0.80254 |
| `explicit.stat_9187492@T1` | -0.69638 |
| `explicit.stat_691932474@T1` | -0.66154 |
| `explicit.stat_1263695895@T2` | -0.65133 |
| `explicit.stat_210067635@T1` | 0.61911 |
| `explicit.stat_1509134228@T1` | 0.61121 |

## Coverage (listings per base)

- … **Sapphire** — 27213 listings (27166 priced) [0.3–885594757.8 ex]
- … **Emerald** — 26666 listings (26632 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 20417 listings (20395 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10429 listings (10414 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8942 listings (8926 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8659 listings (8640 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8537 listings (8529 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8130 listings (8115 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 7959 listings (7941 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 7925 listings (7915 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6651 listings (6641 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6386 listings (6380 priced) [0.3–307202867.9 ex]
- … **Dueling Wand** — 6353 listings (6334 priced) [0.3–4297682211.9 ex]
- … **Ruby Ring** — 6334 listings (6328 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5635 listings (5612 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5619 listings (5612 priced) [0.3–19945827.9 ex]
- … **Jade Amulet** — 5500 listings (5489 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 5479 listings (5463 priced) [0.2–24532814.5 ex]
- … **Amber Amulet** — 5478 listings (5471 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5440 listings (5419 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5304 listings (5295 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5209 listings (5202 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5027 listings (5025 priced) [0.3–3985176410.3 ex]
- … **Heavy Belt** — 4999 listings (4991 priced) [0.3–398912568423.8 ex]
- … **Lunar Amulet** — 4986 listings (4974 priced) [0.3–91750808.2 ex]

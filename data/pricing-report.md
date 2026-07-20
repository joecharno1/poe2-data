# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-20T08:05:51+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **676371** (674263 priced in exalted)
- Distinct bases: 998 · distinct mods: 3299 · mod rows: 3201992
- Sold signals: **24432** sold · 384417 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-20T07:52:31+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.08** (median |log error| 3.1812)
- Within ±30% of asking price: **21%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×74.72 · ±30% 7% · n=98693
- Premium segment (60ex+): skill **+0.11** · typical error ×310.26 · ±30% 0% · n=66325

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 14342 | ×51.14 | 21% | +0.03 | +0.06 |
| jewel | 13689 | ×57.25 | 22% | +0.03 | +0.03 |
| accessory.amulet | 12964 | ×16.34 | 25% | +0.01 | +0.01 |
| accessory.belt | 9345 | ×24.88 | 23% | +0.02 | +0.04 |
| armour.chest | 8974 | ×18.24 | 24% | +0.07 | +0.10 |
| armour.helmet | 8820 | ×27.82 | 21% | +0.07 | +0.10 |
| armour.boots | 8184 | ×28.16 | 21% | +0.09 | +0.11 |
| armour.gloves | 7997 | ×35.78 | 16% | +0.07 | +0.10 |
| other | 7926 | ×1.85 | 42% | +0.12 | +0.20 |
| weapon.wand | 4795 | ×46.56 | 18% | +0.09 | +0.11 |
| weapon.bow | 3760 | ×32.41 | 15% | +0.12 | +0.12 |
| weapon.crossbow | 3533 | ×28.35 | 14% | +0.12 | +0.16 |
| weapon.warstaff | 2435 | ×15.57 | 7% | +0.21 | +0.20 |
| weapon.staff | 2290 | ×19.56 | 6% | +0.18 | +0.17 |
| weapon.sceptre | 2247 | ×20.43 | 5% | +0.09 | +0.09 |
| weapon.spear | 1801 | ×17.50 | 7% | +0.13 | +0.13 |
| armour.focus | 1513 | ×15.97 | 7% | +0.11 | +0.12 |
| armour.quiver | 1412 | ×20.08 | 7% | +0.17 | +0.18 |
| flask.charm | 1183 | ×13.01 | 27% | -0.00 | +0.02 |
| armour.shield | 1154 | ×15.01 | 7% | +0.09 | +0.11 |
| weapon.twomace | 1080 | ×9.13 | 8% | +0.11 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=74457, R²=-1.8912

intercept: `-0.0601`  ·  log_price: True  ·  ilvl: `0.00074`  ·  n_mods: `1.02339`  ·  n_top_tier: `-0.85004`  ·  corrupted: `1.27701`  ·  quality: `0.31232`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 3.57600 |
| `explicit.stat_3714003708@T1` | 3.44678 |
| `explicit.stat_1604736568@T1` | -2.46956 |
| `explicit.stat_1604736568` | 2.30530 |
| `explicit.stat_3473929743@T1` | -2.13458 |
| `explicit.stat_3174700878@T1` | 1.03297 |
| `explicit.stat_587431675@T1` | -1.02427 |
| `explicit.stat_274716455@T1` | -0.86727 |
| `explicit.stat_2194114101@T1` | -0.74506 |
| `explicit.stat_2231156303@T1` | 0.49868 |
| `explicit.stat_491450213@T1` | 0.49564 |
| `explicit.stat_3556824919@T1` | 0.48353 |

### accessory.ring — n=65376, R²=-2.0415

intercept: `3.5042`  ·  log_price: True  ·  ilvl: `-0.04367`  ·  n_mods: `0.00129`  ·  n_top_tier: `1.01038`  ·  corrupted: `0.01110`  ·  n_sockets: `2.00281`  ·  quality: `0.02428`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.05056 |
| `explicit.stat_1573130764@T2` | -1.04394 |
| `explicit.stat_4220027924@T2` | -1.03503 |
| `explicit.stat_4080418644@T1` | -1.03299 |
| `explicit.stat_2231156303@T1` | -1.03233 |
| `explicit.stat_803737631@T1` | -1.02717 |
| `explicit.stat_2891184298@T2` | -1.02557 |
| `explicit.stat_736967255@T2` | -1.02192 |
| `explicit.stat_2144192055@T1` | -1.02153 |
| `explicit.stat_2923486259@T2` | -1.02054 |
| `explicit.stat_789117908@T2` | -1.02034 |
| `explicit.stat_2891184298@T1` | -1.01929 |

### other — n=64399, R²=-0.607

intercept: `1.6073`  ·  log_price: True  ·  ilvl: `0.00005`  ·  n_mods: `0.17488`  ·  n_top_tier: `0.17094`  ·  corrupted: `0.00130`  ·  n_sockets: `-0.00082`  ·  quality: `-0.00010`

| stat_id | coef |
|---|---|
| `implicit.stat_718638445` | 0.52618 |
| `implicit.stat_3182714256` | 0.52615 |
| `explicit.stat_1050105434@T1` | -0.21923 |
| `explicit.stat_3299347043@T1` | -0.21643 |
| `explicit.stat_2974417149@T1` | 0.21439 |
| `implicit.stat_2219129443` | 0.21262 |
| `implicit.stat_3879011313` | 0.21261 |
| `implicit.stat_4041853756` | 0.21258 |
| `implicit.stat_958696139` | -0.17500 |
| `implicit.stat_1416292992` | -0.10812 |
| `implicit.stat_3032590688` | -0.06977 |
| `explicit.stat_2901986750` | 0.06118 |

### accessory.amulet — n=59008, R²=-0.4828

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `1.05111`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.79936`  ·  quality: `0.04944`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | -1.09185 |
| `explicit.stat_2162097452@T2` | -1.07281 |
| `explicit.stat_124131830@T2` | -1.06760 |
| `explicit.stat_803737631@T1` | -1.05114 |
| `explicit.stat_803737631@T2` | -1.05113 |
| `explicit.stat_983749596@T2` | -1.05113 |
| `explicit.stat_3299347043@T2` | -1.05113 |
| `explicit.stat_789117908@T2` | -1.05113 |
| `explicit.stat_789117908@T1` | -1.05112 |
| `explicit.stat_328541901@T2` | -1.05112 |
| `explicit.stat_328541901@T1` | -1.05112 |
| `explicit.stat_1050105434@T2` | -1.05112 |

### accessory.belt — n=42737, R²=-2.008

intercept: `0.5988`  ·  log_price: True  ·  ilvl: `-0.00722`  ·  n_mods: `-0.00336`  ·  n_top_tier: `0.69347`  ·  corrupted: `0.71090`  ·  n_sockets: `1.36320`

| stat_id | coef |
|---|---|
| `explicit.stat_2881298780@T1` | -0.69786 |
| `explicit.stat_3299347043@T1` | -0.69743 |
| `explicit.stat_3299347043@T2` | -0.69673 |
| `explicit.stat_4220027924@T2` | -0.69648 |
| `explicit.stat_915769802@T1` | -0.69638 |
| `explicit.stat_51994685@T1` | -0.69615 |
| `explicit.stat_3325883026@T1` | -0.69574 |
| `explicit.stat_809229260@T2` | -0.69514 |
| `explicit.stat_3372524247@T2` | -0.69452 |
| `explicit.stat_1389754388@T1` | -0.69452 |
| `explicit.stat_1570770415@T2` | -0.69422 |
| `explicit.stat_2881298780@T2` | -0.69397 |

### armour.chest — n=42338, R²=-1.8125

intercept: `3.1131`  ·  log_price: True  ·  ilvl: `-0.03850`  ·  n_mods: `-0.00999`  ·  n_top_tier: `0.30077`  ·  corrupted: `0.06581`  ·  n_sockets: `0.01459`  ·  quality: `0.07483`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.66730 |
| `explicit.stat_3981240776@T1` | 0.67099 |
| `explicit.stat_986397080@T2` | -0.36878 |
| `explicit.stat_986397080@T1` | -0.35565 |
| `explicit.stat_1692879867@T2` | -0.32963 |
| `explicit.stat_4080418644@T1` | -0.32287 |
| `explicit.stat_915769802@T2` | -0.32210 |
| `explicit.stat_3484657501@T1` | -0.32097 |
| `explicit.stat_4080418644@T2` | -0.32068 |
| `explicit.stat_1692879867@T1` | -0.31409 |
| `explicit.stat_915769802@T1` | -0.31231 |
| `explicit.stat_3301100256@T2` | -0.31217 |

### armour.helmet — n=41187, R²=-1.8325

intercept: `3.1220`  ·  log_price: True  ·  ilvl: `-0.03929`  ·  n_mods: `-0.01373`  ·  n_top_tier: `0.45790`  ·  corrupted: `0.65002`  ·  n_sockets: `0.02969`  ·  quality: `0.07388`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.27038 |
| `explicit.stat_2162097452@T2` | -0.62907 |
| `explicit.stat_3917489142@T2` | -0.62375 |
| `explicit.stat_1263695895@T1` | -0.61697 |
| `explicit.stat_3917489142@T1` | -0.55539 |
| `explicit.stat_1263695895@T2` | -0.51564 |
| `explicit.stat_4052037485@T2` | -0.49664 |
| `explicit.stat_803737631@T1` | -0.48910 |
| `explicit.stat_1999113824@T1` | -0.48687 |
| `explicit.stat_803737631@T2` | -0.48448 |
| `explicit.stat_53045048@T1` | -0.47959 |
| `explicit.stat_3321629045@T2` | -0.47803 |

### armour.boots — n=38270, R²=-1.7691

intercept: `3.3184`  ·  log_price: True  ·  ilvl: `-0.04097`  ·  n_mods: `-0.01581`  ·  n_top_tier: `0.47991`  ·  corrupted: `0.06520`  ·  n_sockets: `0.03364`  ·  quality: `0.06671`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.76813 |
| `crafted.stat_3917489142@T1` | 1.45966 |
| `explicit.stat_2339757871@T1` | -1.12079 |
| `explicit.stat_2923486259@T1` | 0.66611 |
| `explicit.stat_3917489142@T2` | -0.55768 |
| `explicit.stat_3299347043@T1` | -0.55473 |
| `explicit.stat_1874553720@T1` | -0.53327 |
| `explicit.stat_2923486259@T2` | -0.53262 |
| `explicit.stat_2160282525@T1` | -0.51884 |
| `explicit.stat_124859000@T1` | -0.51052 |
| `explicit.stat_1671376347@T2` | -0.51004 |
| `explicit.stat_3321629045@T2` | -0.50556 |

### armour.gloves — n=37198, R²=-1.7521

intercept: `3.7509`  ·  log_price: True  ·  ilvl: `-0.04868`  ·  n_mods: `-0.01220`  ·  n_top_tier: `0.73220`  ·  corrupted: `-0.01521`  ·  n_sockets: `0.11632`  ·  quality: `0.05982`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.66303 |
| `rune.stat_201332984` | 1.28649 |
| `explicit.stat_2923486259@T1` | -1.04886 |
| `explicit.stat_3321629045@T2` | -0.94451 |
| `explicit.stat_4052037485@T1` | -0.93794 |
| `explicit.stat_4052037485@T2` | -0.92050 |
| `explicit.stat_3484657501@T2` | -0.91668 |
| `explicit.stat_4015621042@T2` | -0.88848 |
| `explicit.stat_9187492@T2` | -0.87682 |
| `explicit.stat_803737631@T2` | -0.85780 |
| `explicit.stat_803737631@T1` | -0.83638 |
| `explicit.stat_3639275092@T1` | -0.82305 |

### weapon.wand — n=22302, R²=-2.0559

intercept: `4.0019`  ·  log_price: True  ·  ilvl: `-0.04985`  ·  n_mods: `-0.04788`  ·  n_top_tier: `0.23750`  ·  corrupted: `-0.00815`  ·  n_sockets: `0.03579`  ·  quality: `0.04093`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.15237 |
| `rune.stat_124131830` | -2.97287 |
| `explicit.stat_2254480358@T1` | 2.75264 |
| `explicit.stat_124131830@T1` | 2.55179 |
| `explicit.stat_591105508@T1` | 2.13510 |
| `explicit.stat_4226189338@T1` | 2.08037 |
| `explicit.stat_736967255@T2` | 1.96791 |
| `explicit.stat_2254480358@T2` | 1.44591 |
| `crafted.stat_124131830` | 1.30344 |
| `explicit.stat_1600707273@T1` | 1.19070 |
| `explicit.stat_4226189338@T2` | 1.16604 |
| `explicit.stat_1545858329@T2` | 0.73774 |

### flask.charm — n=18753, R²=-0.6426

intercept: `0.1059`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.60926`  ·  corrupted: `1.52377`  ·  quality: `0.00406`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60583 |
| `explicit.stat_1056492907` | 2.70738 |
| `explicit.stat_1120862500@T2` | -1.60929 |
| `explicit.stat_828533480@T2` | -1.60929 |
| `explicit.stat_1873752457@T2` | -1.60925 |
| `explicit.stat_3196823591@T2` | -1.60922 |
| `explicit.stat_2365392475@T2` | -1.60921 |
| `explicit.stat_2676834156@T2` | -1.60908 |
| `explicit.stat_388617051@T2` | -1.60889 |
| `explicit.stat_1873752457@T1` | -1.60479 |
| `explicit.stat_828533480@T1` | -1.60294 |
| `explicit.stat_1366840608@T2` | -1.58900 |

### weapon.bow — n=17778, R²=-2.0217

intercept: `3.9660`  ·  log_price: True  ·  ilvl: `-0.04790`  ·  n_mods: `-0.04283`  ·  n_top_tier: `0.85030`  ·  corrupted: `0.61013`  ·  n_sockets: `0.01925`  ·  quality: `0.03004`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 2.27394 |
| `desecrated.stat_210067635@T1` | -1.93359 |
| `crafted.stat_3035140377` | 1.43095 |
| `explicit.stat_1263695895@T1` | -1.06140 |
| `explicit.stat_3336890334@T1` | 1.03978 |
| `explicit.stat_1263695895@T2` | -1.03214 |
| `explicit.stat_1368271171@T2` | -0.89716 |
| `explicit.stat_1509134228@T1` | -0.88050 |
| `explicit.stat_669069897@T1` | -0.87786 |
| `explicit.stat_210067635@T2` | -0.87450 |
| `explicit.stat_1368271171@T1` | -0.87254 |
| `explicit.stat_3695891184@T1` | -0.86950 |

### weapon.crossbow — n=16704, R²=-1.7218

intercept: `4.0394`  ·  log_price: True  ·  ilvl: `-0.04933`  ·  n_mods: `-0.07055`  ·  n_top_tier: `0.37697`  ·  corrupted: `0.13537`  ·  n_sockets: `0.08161`  ·  quality: `0.03189`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.63828 |
| `explicit.stat_1202301673@T1` | 1.51302 |
| `explicit.stat_2250681686@T2` | -1.34647 |
| `explicit.stat_1980802737` | 1.34062 |
| `explicit.stat_2250681686` | 1.01333 |
| `crafted.stat_3035140377` | 0.80234 |
| `explicit.stat_709508406@T1` | 0.78103 |
| `explicit.stat_1509134228@T1` | 0.77170 |
| `explicit.stat_3336890334@T2` | -0.61884 |
| `explicit.stat_3695891184@T1` | -0.58421 |
| `explicit.stat_1037193709@T1` | -0.55510 |
| `explicit.stat_1263695895@T2` | -0.55309 |

### weapon.warstaff — n=11505, R²=-0.3472

intercept: `-10.6634`  ·  log_price: True  ·  ilvl: `0.14330`  ·  n_mods: `-0.21233`  ·  n_top_tier: `0.38287`  ·  corrupted: `0.40446`  ·  n_sockets: `0.12853`  ·  quality: `0.05787`

| stat_id | coef |
|---|---|
| `desecrated.stat_3291658075@T1` | -1.75339 |
| `desecrated.stat_473429811@T1` | -1.75339 |
| `desecrated.stat_2231156303@T1` | 1.70164 |
| `desecrated.stat_2527686725@T1` | 1.70164 |
| `crafted.stat_210067635@T2` | 1.26211 |
| `explicit.stat_328541901@T2` | -0.86028 |
| `explicit.stat_328541901@T1` | -0.82783 |
| `explicit.stat_1368271171@T1` | -0.81578 |
| `desecrated.stat_9187492` | 0.77866 |
| `explicit.stat_1509134228@T1` | 0.71703 |
| `rune.stat_243313994` | 0.71444 |
| `explicit.stat_1037193709@T1` | 0.71156 |

### weapon.staff — n=10883, R²=-0.3543

intercept: `-16.1920`  ·  log_price: True  ·  ilvl: `0.20854`  ·  n_mods: `-0.08537`  ·  n_top_tier: `0.35332`  ·  corrupted: `0.65098`  ·  n_sockets: `0.19152`  ·  quality: `0.04530`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.17450 |
| `explicit.stat_4226189338@T1` | 2.17302 |
| `explicit.stat_1545858329@T1` | 2.14511 |
| `explicit.stat_124131830@T1` | 1.57475 |
| `explicit.stat_2254480358@T1` | 1.53791 |
| `explicit.stat_1600707273@T1` | 1.50306 |
| `explicit.stat_293638271@T2` | -1.17537 |
| `explicit.stat_2254480358@T2` | 1.06500 |
| `explicit.stat_3962278098@T2` | 0.87773 |
| `explicit.stat_4226189338@T2` | 0.70251 |
| `explicit.stat_1600707273@T2` | 0.65514 |
| `explicit.stat_591105508@T2` | 0.61930 |

### weapon.sceptre — n=10702, R²=-0.3264

intercept: `-21.9324`  ·  log_price: True  ·  ilvl: `0.27981`  ·  n_mods: `0.02049`  ·  n_top_tier: `0.22514`  ·  corrupted: `0.18951`  ·  n_sockets: `0.20965`  ·  quality: `0.03024`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.35458 |
| `explicit.stat_3057012405@T1` | 1.32237 |
| `explicit.stat_1263695895@T2` | -1.30123 |
| `explicit.stat_2162097452@T2` | 1.04980 |
| `explicit.stat_1263695895@T1` | -0.94060 |
| `explicit.stat_1798257884@T2` | 0.92049 |
| `explicit.stat_101878827@T2` | 0.83838 |
| `explicit.stat_2854751904@T2` | -0.83378 |
| `explicit.stat_101878827@T1` | 0.79184 |
| `explicit.stat_849987426@T1` | 0.70048 |
| `explicit.stat_289128254@T1` | 0.57932 |
| `explicit.stat_1998951374@T1` | 0.54567 |

### weapon.spear — n=8659, R²=-0.357

intercept: `-13.7833`  ·  log_price: True  ·  ilvl: `0.18783`  ·  n_mods: `-0.13481`  ·  n_top_tier: `0.58891`  ·  corrupted: `-0.44810`  ·  n_sockets: `0.24783`  ·  quality: `0.07941`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.04347 |
| `desecrated.stat_666077204@T1` | -3.11513 |
| `explicit.stat_9187492@T1` | 1.29483 |
| `explicit.stat_1940865751@T2` | -1.13021 |
| `explicit.stat_1202301673@T1` | 1.11830 |
| `desecrated.stat_210067635@T1` | -1.09092 |
| `explicit.stat_1509134228@T1` | 0.99340 |
| `explicit.stat_4080418644@T2` | -0.96999 |
| `explicit.stat_691932474@T2` | -0.79419 |
| `explicit.stat_3336890334@T2` | -0.78176 |
| `explicit.stat_748522257@T2` | -0.73870 |
| `explicit.stat_1037193709@T2` | -0.73732 |

### armour.focus — n=7083, R²=-0.3458

intercept: `-15.7762`  ·  log_price: True  ·  ilvl: `0.19958`  ·  n_mods: `-0.12586`  ·  n_top_tier: `1.08019`  ·  corrupted: `0.19102`  ·  n_sockets: `0.34473`  ·  quality: `0.02956`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 4.98200 |
| `explicit.stat_2923486259@T1` | -1.85549 |
| `explicit.stat_4220027924@T1` | -1.77638 |
| `explicit.stat_2923486259@T2` | -1.36457 |
| `explicit.stat_4220027924@T2` | -1.34016 |
| `explicit.stat_2231156303@T1` | -1.32390 |
| `explicit.stat_2231156303@T2` | -1.23723 |
| `explicit.stat_274716455@T1` | -1.20478 |
| `explicit.stat_4015621042@T1` | -1.17346 |
| `explicit.stat_2768835289@T1` | -1.15285 |
| `explicit.stat_737908626@T2` | -1.13388 |
| `explicit.stat_2339757871@T2` | -1.13021 |

### armour.quiver — n=6609, R²=-0.2895

intercept: `-17.0764`  ·  log_price: True  ·  ilvl: `0.20726`  ·  n_mods: `-0.12531`  ·  n_top_tier: `0.70919`  ·  corrupted: `0.86627`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.93965 |
| `explicit.stat_2463230181@T1` | 1.88870 |
| `explicit.stat_681332047@T2` | -1.39724 |
| `explicit.stat_1573130764@T1` | -1.21935 |
| `explicit.stat_681332047@T1` | -1.11115 |
| `explicit.stat_1573130764@T2` | -1.07653 |
| `explicit.stat_2463230181@T2` | 0.99123 |
| `explicit.stat_803737631@T1` | -0.93816 |
| `explicit.stat_4067062424@T1` | -0.91538 |
| `explicit.stat_4067062424@T2` | -0.83719 |
| `explicit.stat_803737631@T2` | -0.80540 |
| `explicit.stat_2321178454@T2` | -0.78413 |

### armour.shield — n=5685, R²=-0.4221

intercept: `-14.2263`  ·  log_price: True  ·  ilvl: `0.18796`  ·  n_mods: `-0.10081`  ·  n_top_tier: `0.70817`  ·  corrupted: `-0.37713`  ·  n_sockets: `0.39514`  ·  quality: `0.06053`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.99774 |
| `explicit.stat_3855016469@T1` | -1.42628 |
| `explicit.stat_1011760251@T1` | -1.21198 |
| `explicit.stat_2339757871@T2` | -1.17485 |
| `explicit.stat_3321629045@T2` | -1.13558 |
| `explicit.stat_2481353198@T1` | -1.08636 |
| `explicit.stat_1301765461@T2` | -1.04174 |
| `explicit.stat_3484657501@T1` | -1.03041 |
| `explicit.stat_2901986750@T1` | -1.03032 |
| `explicit.stat_2451402625@T1` | -1.01357 |
| `explicit.stat_2481353198@T2` | -1.01290 |
| `explicit.stat_4095671657@T2` | -0.96520 |

### weapon.twomace — n=5220, R²=-0.4495

intercept: `-10.5051`  ·  log_price: True  ·  ilvl: `0.14156`  ·  n_mods: `-0.20155`  ·  n_top_tier: `0.38421`  ·  corrupted: `0.52748`  ·  n_sockets: `0.13755`  ·  quality: `0.06601`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.14769 |
| `explicit.stat_1037193709@T1` | -1.55246 |
| `explicit.stat_1263695895@T2` | -1.29407 |
| `explicit.stat_3336890334@T1` | -1.13240 |
| `explicit.stat_2694482655@T1` | 0.93293 |
| `explicit.stat_9187492@T1` | -0.92019 |
| `explicit.stat_691932474@T1` | -0.77615 |
| `explicit.stat_3695891184@T2` | -0.74849 |
| `explicit.stat_1263695895@T1` | -0.74450 |
| `explicit.stat_3695891184@T1` | -0.74081 |
| `explicit.stat_518292764@T1` | 0.70813 |
| `explicit.stat_387439868@T2` | -0.64680 |

## Coverage (listings per base)

- … **Sapphire** — 34323 listings (34267 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 33419 listings (33377 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 25627 listings (25596 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 12210 listings (12192 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11058 listings (11034 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10658 listings (10633 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 10563 listings (10552 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 9975 listings (9953 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9853 listings (9831 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 9464 listings (9451 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8187 listings (8172 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7879 listings (7870 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 7790 listings (7781 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7167 listings (7145 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6808 listings (6801 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 6746 listings (6727 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6728 listings (6714 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6689 listings (6682 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6661 listings (6633 priced) [0.3–398912568423.8 ex]
- … **Ancestral Tiara** — 6578 listings (6549 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6494 listings (6485 priced) [0.2–275252424.7 ex]
- … **Bloodstone Amulet** — 6475 listings (6465 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6165 listings (6162 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6053 listings (6039 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5911 listings (5901 priced) [0.3–398912568423.8 ex]

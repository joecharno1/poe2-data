# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-14T04:28:45+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **453216** (452305 priced in exalted)
- Distinct bases: 978 · distinct mods: 3029 · mod rows: 2152558
- Sold signals: **27087** sold · 249018 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-14T04:20:52+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×31.13** (median |log error| 3.4383)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×95.34 · ±30% 4% · n=64869
- Premium segment (60ex+): skill **+0.11** · typical error ×370.78 · ±30% 0% · n=42647

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 8869 | ×50.54 | 20% | +0.04 | +0.04 |
| accessory.amulet | 8294 | ×41.62 | 21% | +0.03 | +0.02 |
| jewel | 8230 | ×44.29 | 14% | +0.02 | +0.03 |
| accessory.belt | 6408 | ×29.62 | 6% | +0.07 | +0.10 |
| armour.chest | 6249 | ×22.07 | 20% | +0.06 | +0.08 |
| armour.helmet | 6108 | ×28.41 | 17% | +0.06 | +0.09 |
| armour.boots | 5700 | ×23.53 | 22% | +0.05 | +0.08 |
| armour.gloves | 5557 | ×36.15 | 21% | +0.04 | +0.06 |
| other | 5022 | ×6.20 | 41% | +0.08 | +0.15 |
| weapon.wand | 3668 | ×34.69 | 21% | +0.06 | +0.07 |
| weapon.bow | 2966 | ×29.62 | 17% | +0.08 | +0.09 |
| weapon.crossbow | 2790 | ×25.11 | 20% | +0.09 | +0.13 |
| weapon.warstaff | 1553 | ×49.13 | 19% | +0.08 | +0.10 |
| weapon.staff | 1434 | ×56.19 | 18% | +0.06 | +0.07 |
| weapon.sceptre | 1415 | ×50.61 | 10% | +0.09 | +0.09 |
| weapon.spear | 1245 | ×49.82 | 20% | +0.08 | +0.07 |
| armour.focus | 991 | ×47.08 | 10% | +0.13 | +0.13 |
| armour.quiver | 976 | ×29.18 | 14% | +0.06 | +0.11 |
| armour.shield | 793 | ×19.22 | 18% | +0.04 | +0.05 |
| weapon.twomace | 738 | ×31.67 | 15% | +0.06 | +0.09 |
| flask.charm | 724 | ×25.00 | 34% | +0.01 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=44242, R²=-0.6188

intercept: `1.6033`  ·  log_price: True  ·  ilvl: `0.00008`  ·  n_mods: `0.01789`  ·  n_top_tier: `0.34627`  ·  corrupted: `0.32835`  ·  n_sockets: `-0.00010`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.54691 |
| `explicit.stat_2974417149@T1` | 0.51536 |
| `explicit.stat_789117908@T1` | -0.36796 |
| `explicit.stat_2891184298@T1` | 0.32861 |
| `explicit.stat_1050105434@T1` | -0.29980 |
| `explicit.stat_3917489142@T1` | 0.23501 |
| `implicit.stat_4041853756` | 0.22846 |
| `implicit.stat_3879011313` | 0.22846 |
| `explicit.stat_3141070085@T1` | -0.21718 |
| `explicit.stat_3299347043@T1` | -0.21450 |
| `implicit.stat_1379411836` | -0.18687 |
| `explicit.stat_101878827@T1` | 0.16476 |

### jewel — n=44007, R²=-1.7581

intercept: `-0.3165`  ·  log_price: True  ·  ilvl: `0.00412`  ·  n_mods: `1.01834`  ·  n_top_tier: `-0.79599`  ·  corrupted: `0.24848`  ·  quality: `0.30044`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 3.69354 |
| `explicit.stat_3596695232@T1` | 3.45937 |
| `explicit.stat_1604736568@T1` | -3.24790 |
| `explicit.stat_1604736568` | 3.03957 |
| `explicit.stat_1829102168@T1` | 2.60134 |
| `explicit.stat_3741323227@T1` | -2.25910 |
| `explicit.stat_3759663284@T1` | -2.23728 |
| `explicit.stat_3556824919@T1` | -1.87702 |
| `explicit.stat_1697447343@T1` | -1.75394 |
| `explicit.stat_2011656677@T1` | 1.62609 |
| `explicit.stat_737908626@T1` | 1.47451 |
| `explicit.stat_1714971114@T1` | 1.34465 |

### accessory.ring — n=40696, R²=-1.9858

intercept: `3.3997`  ·  log_price: True  ·  ilvl: `-0.04184`  ·  n_mods: `-0.00108`  ·  n_top_tier: `0.51308`  ·  corrupted: `0.13317`  ·  n_sockets: `-0.07558`  ·  quality: `0.07606`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | -0.55956 |
| `explicit.stat_2231156303@T1` | -0.55315 |
| `explicit.stat_3325883026@T1` | -0.54605 |
| `explicit.stat_1573130764@T1` | -0.54106 |
| `explicit.stat_3917489142@T2` | -0.53878 |
| `explicit.stat_3962278098@T2` | -0.53678 |
| `explicit.stat_1368271171@T2` | -0.53565 |
| `explicit.stat_3291658075@T1` | -0.53532 |
| `explicit.stat_3032590688@T2` | -0.53400 |
| `explicit.stat_4220027924@T2` | -0.53285 |
| `explicit.stat_3291658075@T2` | -0.53266 |
| `explicit.stat_2144192055@T1` | -0.53163 |

### accessory.amulet — n=37845, R²=-2.1267

intercept: `3.9686`  ·  log_price: True  ·  ilvl: `-0.04819`  ·  n_mods: `-0.02514`  ·  n_top_tier: `0.77972`  ·  corrupted: `0.02774`  ·  n_sockets: `-0.04033`  ·  quality: `0.00134`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T2` | -0.89614 |
| `explicit.stat_2748665614@T1` | -0.88670 |
| `explicit.stat_2748665614@T2` | -0.87257 |
| `explicit.stat_472520716@T1` | -0.83711 |
| `explicit.stat_2901986750@T1` | -0.83703 |
| `explicit.stat_3299347043@T2` | -0.83584 |
| `explicit.stat_3917489142@T2` | -0.83426 |
| `explicit.stat_3917489142@T1` | -0.83062 |
| `explicit.stat_1050105434@T2` | -0.82869 |
| `explicit.stat_2974417149@T1` | -0.82019 |
| `explicit.stat_3325883026@T1` | -0.81854 |
| `explicit.stat_472520716@T2` | -0.81570 |

### accessory.belt — n=29547, R²=-1.0122

intercept: `6.1480`  ·  log_price: True  ·  ilvl: `-0.06249`  ·  n_mods: `-0.24088`  ·  n_top_tier: `0.98075`  ·  corrupted: `1.16774`  ·  n_sockets: `1.08117`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.38932 |
| `explicit.stat_1389754388@T1` | -1.37039 |
| `explicit.stat_51994685@T1` | -1.33184 |
| `explicit.stat_2881298780@T1` | -1.25343 |
| `explicit.stat_809229260@T2` | -1.21774 |
| `explicit.stat_1671376347@T2` | -1.10765 |
| `explicit.stat_644456512@T1` | -1.08471 |
| `explicit.stat_1389754388@T2` | -1.04569 |
| `explicit.stat_3299347043@T2` | -1.04087 |
| `explicit.stat_4220027924@T2` | -1.03814 |
| `explicit.stat_3585532255@T2` | -1.01332 |
| `explicit.stat_4080418644@T2` | -0.99226 |

### armour.chest — n=29214, R²=-1.59

intercept: `3.8158`  ·  log_price: True  ·  ilvl: `-0.04687`  ·  n_mods: `-0.02179`  ·  n_top_tier: `0.37559`  ·  corrupted: `0.32619`  ·  n_sockets: `0.02054`  ·  quality: `0.03903`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.26315 |
| `explicit.stat_3981240776@T1` | 1.30104 |
| `explicit.stat_3033371881@T1` | 0.54405 |
| `explicit.stat_4015621042@T1` | -0.42491 |
| `explicit.stat_4080418644@T2` | -0.42201 |
| `explicit.stat_915769802@T2` | -0.41969 |
| `explicit.stat_3484657501@T1` | -0.41413 |
| `explicit.stat_986397080@T2` | -0.41255 |
| `explicit.stat_4080418644@T1` | -0.40357 |
| `explicit.stat_1999113824@T1` | -0.40316 |
| `explicit.stat_915769802@T1` | -0.40052 |
| `explicit.stat_2923486259@T2` | -0.39432 |

### armour.helmet — n=28567, R²=-1.5748

intercept: `3.8800`  ·  log_price: True  ·  ilvl: `-0.04901`  ·  n_mods: `-0.02463`  ·  n_top_tier: `0.49440`  ·  corrupted: `0.74998`  ·  n_sockets: `0.02714`  ·  quality: `0.05841`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.65207 |
| `explicit.stat_2339757871@T1` | -2.22297 |
| `explicit.stat_1263695895@T1` | -0.87246 |
| `explicit.stat_1263695895@T2` | -0.73470 |
| `explicit.stat_53045048@T1` | -0.64545 |
| `explicit.stat_2162097452@T2` | -0.59306 |
| `explicit.stat_3917489142@T2` | -0.58320 |
| `explicit.stat_1999113824@T1` | -0.58308 |
| `explicit.stat_53045048@T2` | -0.58285 |
| `explicit.stat_3261801346@T2` | -0.55254 |
| `explicit.stat_328541901@T2` | -0.54875 |
| `explicit.stat_803737631@T2` | -0.54370 |

### armour.boots — n=26793, R²=-1.688

intercept: `3.5004`  ·  log_price: True  ·  ilvl: `-0.04308`  ·  n_mods: `-0.01033`  ·  n_top_tier: `0.58470`  ·  corrupted: `0.08910`  ·  n_sockets: `0.00459`  ·  quality: `0.02698`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.48290 |
| `desecrated.stat_2250533757@T2` | -0.71555 |
| `explicit.stat_3917489142@T2` | -0.69230 |
| `explicit.stat_3917489142@T1` | -0.65920 |
| `explicit.stat_2923486259@T2` | -0.62466 |
| `explicit.stat_53045048@T1` | -0.62019 |
| `explicit.stat_3362812763@T1` | -0.61907 |
| `explicit.stat_3299347043@T1` | -0.61871 |
| `explicit.stat_2160282525@T1` | -0.61247 |
| `explicit.stat_1062208444@T2` | -0.61087 |
| `explicit.stat_4052037485@T2` | -0.60980 |
| `explicit.stat_2160282525@T2` | -0.60937 |

### armour.gloves — n=26118, R²=-1.8914

intercept: `3.7054`  ·  log_price: True  ·  ilvl: `-0.04651`  ·  n_mods: `-0.00882`  ·  n_top_tier: `0.50968`  ·  corrupted: `-0.01077`  ·  n_sockets: `0.02520`  ·  quality: `0.03514`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T1` | 0.82473 |
| `explicit.stat_9187492@T2` | -0.80927 |
| `explicit.stat_1671376347@T1` | 0.77849 |
| `explicit.stat_3484657501@T2` | -0.65330 |
| `explicit.stat_3917489142@T2` | -0.59323 |
| `rune.stat_201332984` | 0.58960 |
| `explicit.stat_803737631@T2` | -0.58035 |
| `explicit.stat_2923486259@T2` | -0.57338 |
| `explicit.stat_3032590688@T1` | -0.54944 |
| `explicit.stat_3484657501@T1` | -0.54939 |
| `explicit.stat_328541901@T2` | -0.54821 |
| `explicit.stat_3321629045@T2` | -0.54273 |

### weapon.wand — n=17133, R²=-2.2869

intercept: `3.7178`  ·  log_price: True  ·  ilvl: `-0.04619`  ·  n_mods: `-0.01217`  ·  n_top_tier: `0.05418`  ·  corrupted: `-0.06365`  ·  n_sockets: `0.02777`  ·  quality: `-0.00016`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.13674 |
| `rune.stat_124131830` | -2.77012 |
| `explicit.stat_2254480358@T1` | 2.74533 |
| `explicit.stat_591105508@T1` | 2.31242 |
| `explicit.stat_124131830@T1` | 2.25882 |
| `explicit.stat_4226189338@T1` | 2.25324 |
| `explicit.stat_736967255@T2` | 1.54595 |
| `explicit.stat_2768835289@T2` | 1.46488 |
| `crafted.stat_124131830` | 1.23902 |
| `explicit.stat_2254480358@T2` | 0.95023 |
| `explicit.stat_1600707273@T1` | 0.15869 |
| `explicit.stat_2974417149@T1` | 0.14179 |

### weapon.bow — n=13906, R²=-1.9741

intercept: `3.4260`  ·  log_price: True  ·  ilvl: `-0.04165`  ·  n_mods: `-0.03207`  ·  n_top_tier: `0.75039`  ·  corrupted: `-0.06150`  ·  n_sockets: `-0.00835`  ·  quality: `0.03496`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.53429 |
| `explicit.stat_1202301673@T1` | 1.44103 |
| `crafted.stat_3035140377` | 1.21760 |
| `explicit.stat_1263695895@T1` | -0.87593 |
| `explicit.stat_1509134228@T1` | -0.82222 |
| `explicit.stat_2694482655@T2` | -0.80966 |
| `explicit.stat_1368271171@T2` | -0.80962 |
| `explicit.stat_55876295@T1` | -0.80905 |
| `explicit.stat_669069897@T1` | -0.80802 |
| `explicit.stat_3695891184@T1` | -0.80631 |
| `explicit.stat_3695891184@T2` | -0.80450 |
| `explicit.stat_821021828@T2` | -0.80292 |

### weapon.crossbow — n=13155, R²=-1.9229

intercept: `3.6502`  ·  log_price: True  ·  ilvl: `-0.04487`  ·  n_mods: `-0.01594`  ·  n_top_tier: `0.70531`  ·  corrupted: `-0.01978`  ·  n_sockets: `0.03448`  ·  quality: `0.00996`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.94078 |
| `explicit.stat_2250681686@T2` | -1.60501 |
| `explicit.stat_709508406@T1` | 1.50597 |
| `explicit.stat_1980802737` | 1.18217 |
| `explicit.stat_1202301673@T1` | 1.06785 |
| `explicit.stat_1202301673@T2` | -0.98720 |
| `explicit.stat_2250681686` | 0.98705 |
| `explicit.stat_1263695895@T2` | -0.92675 |
| `explicit.stat_1263695895@T1` | -0.87547 |
| `crafted.stat_3035140377` | 0.81590 |
| `explicit.stat_3695891184@T1` | -0.79619 |
| `explicit.stat_3695891184@T2` | -0.77979 |

### flask.charm — n=11097, R²=-0.5008

intercept: `0.0005`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `1.55061`  ·  corrupted: `2.09061`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.33413 |
| `explicit.stat_1056492907` | 3.39916 |
| `explicit.stat_828533480@T2` | -1.55062 |
| `explicit.stat_3196823591@T2` | -1.55061 |
| `explicit.stat_1120862500@T2` | -1.55061 |
| `explicit.stat_1366840608@T2` | -1.55060 |
| `explicit.stat_2676834156@T2` | -1.55060 |
| `explicit.stat_1873752457@T2` | -1.55060 |
| `explicit.stat_1873752457@T1` | -1.55060 |
| `explicit.stat_2541588185@T2` | -1.55059 |
| `explicit.stat_388617051@T2` | -1.55059 |
| `explicit.stat_828533480@T1` | -1.55059 |

### weapon.warstaff — n=7683, R²=-0.5182

intercept: `-3.9542`  ·  log_price: True  ·  ilvl: `0.05619`  ·  n_mods: `-0.15295`  ·  n_top_tier: `0.81711`  ·  corrupted: `0.19098`  ·  n_sockets: `0.08748`  ·  quality: `0.06114`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.35621 |
| `explicit.stat_328541901@T1` | -1.10851 |
| `explicit.stat_328541901@T2` | -1.06450 |
| `explicit.stat_691932474@T2` | -0.93074 |
| `explicit.stat_55876295@T2` | -0.92546 |
| `explicit.stat_55876295@T1` | -0.92130 |
| `explicit.stat_1037193709@T2` | -0.88570 |
| `explicit.stat_3336890334@T2` | -0.87405 |
| `explicit.stat_1037193709@T1` | 0.86662 |
| `explicit.stat_210067635@T1` | -0.86481 |
| `explicit.stat_1940865751@T1` | -0.85217 |
| `explicit.stat_791928121@T2` | -0.84161 |

### weapon.staff — n=7078, R²=-0.5728

intercept: `-6.2797`  ·  log_price: True  ·  ilvl: `0.07945`  ·  n_mods: `-0.03911`  ·  n_top_tier: `0.40113`  ·  corrupted: `0.10855`  ·  n_sockets: `0.17378`  ·  quality: `0.05340`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 1.97812 |
| `explicit.stat_124131830@T1` | 1.80774 |
| `rune.stat_124131830` | 1.78387 |
| `explicit.stat_1545858329@T1` | 1.47764 |
| `explicit.stat_2768835289@T2` | 1.38532 |
| `explicit.stat_2254480358@T1` | 1.14338 |
| `explicit.stat_1600707273@T1` | 1.11124 |
| `explicit.stat_3291658075@T2` | 0.86342 |
| `explicit.stat_4226189338@T2` | 0.84680 |
| `explicit.stat_2974417149@T1` | -0.65394 |
| `explicit.stat_2254480358@T2` | 0.61371 |
| `explicit.stat_293638271@T2` | -0.51856 |

### weapon.sceptre — n=7075, R²=-0.4801

intercept: `-11.4143`  ·  log_price: True  ·  ilvl: `0.14407`  ·  n_mods: `-0.04051`  ·  n_top_tier: `0.55485`  ·  corrupted: `0.31282`  ·  n_sockets: `0.25264`  ·  quality: `0.09152`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.15443 |
| `explicit.stat_2162097452@T2` | 1.32093 |
| `explicit.stat_4080418644@T1` | -1.16018 |
| `explicit.stat_1574590649@T2` | -0.98250 |
| `explicit.stat_4080418644@T2` | -0.93170 |
| `explicit.stat_1263695895@T1` | -0.93037 |
| `explicit.stat_1263695895@T2` | -0.84238 |
| `explicit.stat_289128254@T2` | -0.79168 |
| `explicit.stat_2347036682@T2` | -0.76128 |
| `explicit.stat_1050105434@T2` | -0.72680 |
| `explicit.stat_2854751904@T2` | -0.67118 |
| `explicit.stat_3639275092@T2` | -0.61022 |

### weapon.spear — n=5943, R²=-0.6571

intercept: `-3.4611`  ·  log_price: True  ·  ilvl: `0.04566`  ·  n_mods: `-0.01513`  ·  n_top_tier: `0.44953`  ·  corrupted: `-0.09266`  ·  n_sockets: `0.07890`  ·  quality: `0.10375`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.37733 |
| `explicit.stat_9187492@T1` | 2.43900 |
| `explicit.stat_1202301673@T1` | 2.39323 |
| `crafted.stat_3035140377` | 1.28932 |
| `explicit.stat_210067635@T1` | 1.04927 |
| `explicit.stat_1509134228@T1` | 0.71377 |
| `explicit.stat_1263695895@T2` | -0.59466 |
| `explicit.stat_55876295@T1` | -0.55154 |
| `explicit.stat_55876295@T2` | -0.50704 |
| `explicit.stat_1509134228@T2` | -0.48369 |
| `explicit.stat_1940865751@T2` | -0.45177 |
| `explicit.stat_1940865751@T1` | -0.43820 |

### armour.focus — n=4856, R²=-0.4621

intercept: `-9.3222`  ·  log_price: True  ·  ilvl: `0.11643`  ·  n_mods: `-0.06206`  ·  n_top_tier: `0.88366`  ·  corrupted: `0.73220`  ·  n_sockets: `0.47131`  ·  quality: `0.07365`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 5.59477 |
| `explicit.stat_4220027924@T2` | -1.31470 |
| `crafted.stat_737908626@T2` | -1.20299 |
| `explicit.stat_4220027924@T1` | -1.15515 |
| `explicit.stat_736967255@T2` | -1.07137 |
| `explicit.stat_2923486259@T1` | -1.05292 |
| `explicit.stat_3962278098@T1` | -1.05064 |
| `explicit.stat_737908626@T2` | -0.97322 |
| `explicit.stat_2891184298@T2` | -0.95979 |
| `explicit.stat_328541901@T2` | -0.94860 |
| `explicit.stat_3962278098@T2` | -0.94291 |
| `explicit.stat_2974417149@T1` | -0.88625 |

### armour.quiver — n=4537, R²=-0.4377

intercept: `-9.1422`  ·  log_price: True  ·  ilvl: `0.11272`  ·  n_mods: `-0.05118`  ·  n_top_tier: `0.72829`  ·  corrupted: `0.70540`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 7.28677 |
| `explicit.stat_2463230181@T1` | 1.94260 |
| `explicit.stat_2321178454@T2` | -1.15732 |
| `explicit.stat_1573130764@T1` | -0.99241 |
| `explicit.stat_2194114101@T2` | -0.93509 |
| `explicit.stat_681332047@T2` | -0.92063 |
| `explicit.stat_2463230181@T2` | 0.87650 |
| `explicit.stat_1573130764@T2` | -0.87265 |
| `explicit.stat_4067062424@T1` | -0.87264 |
| `explicit.stat_3261801346@T1` | -0.86859 |
| `explicit.stat_1368271171@T2` | -0.81452 |
| `explicit.stat_2321178454@T1` | -0.80266 |

### armour.shield — n=3969, R²=-0.55

intercept: `-8.0669`  ·  log_price: True  ·  ilvl: `0.10414`  ·  n_mods: `-0.05516`  ·  n_top_tier: `0.60494`  ·  corrupted: `0.23878`  ·  n_sockets: `0.08657`  ·  quality: `0.05516`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.72904 |
| `explicit.stat_1011760251@T1` | -1.36743 |
| `explicit.stat_2339757871@T1` | -1.23236 |
| `explicit.stat_1011760251@T2` | -1.08385 |
| `explicit.stat_2881298780@T1` | -0.96021 |
| `explicit.stat_2481353198@T2` | -0.93675 |
| `explicit.stat_2481353198@T1` | -0.91714 |
| `explicit.stat_328541901@T1` | -0.82916 |
| `explicit.stat_2881298780@T2` | -0.81698 |
| `explicit.stat_3372524247@T2` | -0.78112 |
| `explicit.stat_3261801346@T1` | -0.77831 |
| `explicit.stat_3321629045@T2` | -0.75847 |

### weapon.twomace — n=3636, R²=-0.4949

intercept: `-9.8943`  ·  log_price: True  ·  ilvl: `0.13000`  ·  n_mods: `-0.12440`  ·  n_top_tier: `0.29506`  ·  corrupted: `0.66730`  ·  n_sockets: `0.14665`  ·  quality: `0.04051`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.59044 |
| `desecrated.stat_1509134228@T1` | 2.57672 |
| `explicit.stat_1037193709@T1` | -1.26102 |
| `explicit.stat_210067635@T1` | 1.15366 |
| `crafted.stat_3035140377` | 1.09267 |
| `explicit.stat_387439868@T2` | -0.87637 |
| `explicit.stat_3336890334@T1` | -0.76993 |
| `explicit.stat_821021828@T2` | -0.63670 |
| `explicit.stat_2694482655@T1` | -0.57365 |
| `explicit.stat_210067635@T2` | 0.54275 |
| `explicit.stat_3695891184@T1` | -0.53929 |
| `explicit.stat_1037193709@T2` | -0.53469 |

## Coverage (listings per base)

- … **Sapphire** — 20589 listings (20559 priced) [0.3–7553463.8 ex]
- … **Emerald** — 20359 listings (20331 priced) [0.3–7553463.8 ex]
- … **Ruby** — 15565 listings (15551 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 8681 listings (8672 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 6989 listings (6980 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 6834 listings (6821 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 6706 listings (6701 priced) [0.2–19945827.9 ex]
- … **Stellar Amulet** — 6432 listings (6428 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 6396 listings (6386 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 6254 listings (6245 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5438 listings (5424 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5230 listings (5224 priced) [0.2–307202867.9 ex]
- … **Ruby Ring** — 5038 listings (5036 priced) [0.2–37474957.5 ex]
- … **Topaz Ring** — 5023 listings (5019 priced) [0.3–307202867.9 ex]
- … **Plate Belt** — 4579 listings (4565 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4530 listings (4526 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4425 listings (4418 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4387 listings (4385 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4354 listings (4349 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4303 listings (4298 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4216 listings (4212 priced) [0.3–4275054.0 ex]
- … **Obliterator Bow** — 4178 listings (4166 priced) [0.3–42622633798.0 ex]
- … **Heavy Belt** — 4095 listings (4093 priced) [0.3–2608914286.6 ex]
- … **Pearl Ring** — 4036 listings (4032 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 3973 listings (3973 priced) [0.3–123132003.2 ex]

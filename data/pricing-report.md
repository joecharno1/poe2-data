# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-14T10:36:32+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **463850** (462914 priced in exalted)
- Distinct bases: 978 · distinct mods: 3044 · mod rows: 2203485
- Sold signals: **26924** sold · 255771 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-14T10:27:47+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.38** (median |log error| 3.1081)
- Within ±30% of asking price: **21%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.10** · typical error ×82.32 · ±30% 5% · n=66289
- Premium segment (60ex+): skill **+0.10** · typical error ×380.89 · ±30% 0% · n=43611

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 9103 | ×49.66 | 21% | +0.04 | +0.05 |
| accessory.amulet | 8523 | ×38.00 | 21% | +0.03 | +0.03 |
| jewel | 8459 | ×8.67 | 6% | +0.02 | +0.05 |
| accessory.belt | 6619 | ×37.57 | 20% | +0.07 | +0.09 |
| armour.chest | 6422 | ×11.84 | 27% | +0.05 | +0.07 |
| armour.helmet | 6326 | ×27.17 | 20% | +0.05 | +0.09 |
| armour.boots | 5885 | ×19.62 | 25% | +0.04 | +0.06 |
| armour.gloves | 5717 | ×29.51 | 21% | +0.04 | +0.05 |
| other | 5064 | ×1.99 | 43% | +0.09 | +0.17 |
| weapon.wand | 3693 | ×33.67 | 20% | +0.07 | +0.07 |
| weapon.bow | 2993 | ×28.00 | 19% | +0.08 | +0.09 |
| weapon.crossbow | 2797 | ×23.91 | 22% | +0.09 | +0.11 |
| weapon.warstaff | 1641 | ×36.55 | 20% | +0.09 | +0.10 |
| weapon.sceptre | 1507 | ×40.43 | 8% | +0.10 | +0.10 |
| weapon.staff | 1498 | ×51.95 | 17% | +0.06 | +0.07 |
| weapon.spear | 1223 | ×44.79 | 20% | +0.08 | +0.07 |
| armour.focus | 1027 | ×47.51 | 10% | +0.12 | +0.13 |
| armour.quiver | 973 | ×24.59 | 14% | +0.06 | +0.10 |
| armour.shield | 817 | ×19.38 | 19% | +0.03 | +0.04 |
| flask.charm | 742 | ×40.00 | 34% | +0.02 | +0.03 |
| weapon.twomace | 739 | ×16.74 | 16% | +0.07 | +0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=45309, R²=-0.7882

intercept: `-1.4850`  ·  log_price: True  ·  ilvl: `0.03113`  ·  n_mods: `0.48255`  ·  n_top_tier: `-0.15828`  ·  corrupted: `0.13442`  ·  quality: `0.23196`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.54816 |
| `explicit.stat_2301718443@T1` | 3.32501 |
| `explicit.stat_1697447343@T1` | -2.54802 |
| `explicit.stat_3780644166@T1` | -2.38165 |
| `explicit.stat_627767961@T1` | -2.31290 |
| `explicit.stat_21071013@T1` | 2.00976 |
| `explicit.stat_795138349@T1` | -1.95649 |
| `explicit.stat_153777645@T1` | -1.82476 |
| `explicit.stat_3485067555@T1` | 1.81876 |
| `explicit.stat_2523933828@T1` | -1.78894 |
| `explicit.stat_1315743832@T1` | 1.77940 |
| `explicit.stat_1805182458@T1` | -1.73639 |

### other — n=45199, R²=-0.6347

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00005`  ·  n_top_tier: `0.34690`  ·  corrupted: `0.34629`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.50859 |
| `explicit.stat_2974417149@T1` | 0.44964 |
| `explicit.stat_789117908@T1` | -0.36144 |
| `explicit.stat_2891184298@T1` | 0.29999 |
| `explicit.stat_1050105434@T1` | -0.28775 |
| `explicit.stat_3299347043@T1` | -0.23957 |
| `explicit.stat_3917489142@T1` | 0.23126 |
| `implicit.stat_3879011313` | 0.23035 |
| `implicit.stat_4041853756` | 0.23026 |
| `implicit.stat_1379411836` | -0.16096 |
| `explicit.stat_2482852589@T1` | -0.09772 |
| `explicit.stat_101878827@T1` | -0.05857 |

### accessory.ring — n=41804, R²=-1.9907

intercept: `3.3797`  ·  log_price: True  ·  ilvl: `-0.04171`  ·  n_mods: `0.00034`  ·  n_top_tier: `0.77922`  ·  corrupted: `0.05086`  ·  n_sockets: `1.02135`  ·  quality: `0.07638`

| stat_id | coef |
|---|---|
| `explicit.stat_2557965901@T1` | -0.85742 |
| `explicit.stat_2557965901@T2` | -0.84409 |
| `explicit.stat_2231156303@T1` | -0.81979 |
| `explicit.stat_3325883026@T1` | -0.81786 |
| `explicit.stat_1263695895@T1` | -0.81655 |
| `explicit.stat_1573130764@T1` | -0.80833 |
| `explicit.stat_3291658075@T1` | -0.80332 |
| `explicit.stat_3962278098@T2` | -0.80166 |
| `explicit.stat_4220027924@T2` | -0.80052 |
| `explicit.stat_1368271171@T2` | -0.80020 |
| `explicit.stat_3325883026@T2` | -0.79788 |
| `explicit.stat_2144192055@T1` | -0.79780 |

### accessory.amulet — n=38836, R²=-2.1367

intercept: `3.8711`  ·  log_price: True  ·  ilvl: `-0.04698`  ·  n_mods: `-0.02473`  ·  n_top_tier: `0.91000`  ·  corrupted: `0.02858`  ·  n_sockets: `-0.12849`  ·  quality: `0.00027`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T2` | -1.09734 |
| `explicit.stat_2748665614@T1` | -1.01746 |
| `explicit.stat_2748665614@T2` | -1.00130 |
| `explicit.stat_472520716@T1` | -0.97928 |
| `explicit.stat_2901986750@T1` | -0.97690 |
| `explicit.stat_1050105434@T2` | -0.96132 |
| `explicit.stat_3299347043@T2` | -0.96082 |
| `explicit.stat_3917489142@T2` | -0.96001 |
| `explicit.stat_472520716@T2` | -0.95462 |
| `explicit.stat_2974417149@T1` | -0.95331 |
| `explicit.stat_3917489142@T1` | -0.95152 |
| `explicit.stat_3299347043@T1` | -0.94866 |

### accessory.belt — n=30288, R²=-1.4964

intercept: `4.2688`  ·  log_price: True  ·  ilvl: `-0.05062`  ·  n_mods: `-0.04131`  ·  n_top_tier: `1.05887`  ·  corrupted: `1.24529`  ·  n_sockets: `1.47683`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.17723 |
| `explicit.stat_1389754388@T1` | -1.11695 |
| `explicit.stat_51994685@T1` | -1.11311 |
| `explicit.stat_2881298780@T1` | -1.11027 |
| `explicit.stat_809229260@T2` | -1.10951 |
| `explicit.stat_4220027924@T2` | -1.08673 |
| `explicit.stat_3325883026@T1` | -1.08327 |
| `explicit.stat_1671376347@T2` | -1.06969 |
| `explicit.stat_1389754388@T2` | -1.06029 |
| `explicit.stat_644456512@T1` | -1.05299 |
| `explicit.stat_915769802@T2` | -1.05175 |
| `explicit.stat_3299347043@T2` | -1.05108 |

### armour.chest — n=29930, R²=-1.7702

intercept: `3.2325`  ·  log_price: True  ·  ilvl: `-0.03992`  ·  n_mods: `-0.00944`  ·  n_top_tier: `0.18854`  ·  corrupted: `0.23701`  ·  n_sockets: `0.00924`  ·  quality: `0.02432`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.19432 |
| `explicit.stat_3981240776@T1` | 0.70256 |
| `explicit.stat_4080418644@T2` | -0.22336 |
| `explicit.stat_4080418644@T1` | -0.21558 |
| `explicit.stat_915769802@T1` | -0.20520 |
| `explicit.stat_4015621042@T1` | -0.20349 |
| `explicit.stat_986397080@T2` | -0.20136 |
| `explicit.stat_915769802@T2` | -0.20032 |
| `explicit.stat_3484657501@T1` | -0.19940 |
| `explicit.stat_4220027924@T2` | -0.19576 |
| `explicit.stat_124859000@T2` | -0.19516 |
| `explicit.stat_2451402625@T2` | -0.19465 |

### armour.helmet — n=29214, R²=-1.6735

intercept: `3.7085`  ·  log_price: True  ·  ilvl: `-0.04657`  ·  n_mods: `-0.01831`  ·  n_top_tier: `0.46930`  ·  corrupted: `0.51083`  ·  n_sockets: `0.01854`  ·  quality: `0.06238`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.30409 |
| `explicit.stat_2339757871@T1` | -2.50822 |
| `explicit.stat_1263695895@T1` | -0.73179 |
| `explicit.stat_1263695895@T2` | -0.64880 |
| `explicit.stat_53045048@T1` | -0.56908 |
| `explicit.stat_2162097452@T2` | -0.56634 |
| `explicit.stat_3917489142@T2` | -0.56399 |
| `explicit.stat_1999113824@T1` | -0.53045 |
| `explicit.stat_3261801346@T2` | -0.52390 |
| `explicit.stat_53045048@T2` | -0.51470 |
| `explicit.stat_3261801346@T1` | -0.50489 |
| `explicit.stat_328541901@T2` | -0.50261 |

### armour.boots — n=27382, R²=-1.8034

intercept: `3.2514`  ·  log_price: True  ·  ilvl: `-0.04014`  ·  n_mods: `-0.00674`  ·  n_top_tier: `0.64898`  ·  corrupted: `0.03241`  ·  n_sockets: `0.00101`  ·  quality: `0.01903`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.02118 |
| `crafted.stat_3917489142@T1` | -0.89943 |
| `desecrated.stat_2250533757@T2` | -0.72834 |
| `explicit.stat_3917489142@T2` | -0.71994 |
| `explicit.stat_3917489142@T1` | -0.69440 |
| `explicit.stat_3362812763@T1` | -0.68072 |
| `explicit.stat_1062208444@T2` | -0.67073 |
| `explicit.stat_3299347043@T1` | -0.67054 |
| `explicit.stat_3362812763@T2` | -0.66531 |
| `explicit.stat_2923486259@T2` | -0.66450 |
| `explicit.stat_2160282525@T2` | -0.66364 |
| `explicit.stat_2160282525@T1` | -0.66279 |

### armour.gloves — n=26739, R²=-1.896

intercept: `3.6190`  ·  log_price: True  ·  ilvl: `-0.04577`  ·  n_mods: `-0.00430`  ·  n_top_tier: `0.49013`  ·  corrupted: `-0.01333`  ·  n_sockets: `0.02592`  ·  quality: `0.04155`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T1` | 0.86629 |
| `explicit.stat_1671376347@T1` | 0.83266 |
| `rune.stat_201332984` | 0.82887 |
| `explicit.stat_9187492@T2` | -0.82237 |
| `explicit.stat_3484657501@T2` | -0.66279 |
| `explicit.stat_803737631@T2` | -0.57900 |
| `explicit.stat_3917489142@T2` | -0.57435 |
| `explicit.stat_3484657501@T1` | -0.56214 |
| `explicit.stat_3321629045@T2` | -0.54204 |
| `explicit.stat_2923486259@T2` | -0.53514 |
| `explicit.stat_3917489142@T1` | -0.52275 |
| `explicit.stat_3321629045@T1` | -0.51863 |

### weapon.wand — n=17395, R²=-2.2411

intercept: `3.6631`  ·  log_price: True  ·  ilvl: `-0.04533`  ·  n_mods: `-0.01798`  ·  n_top_tier: `0.08754`  ·  corrupted: `-0.04123`  ·  n_sockets: `0.03510`  ·  quality: `0.00093`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.31312 |
| `explicit.stat_2254480358@T1` | 2.93012 |
| `rune.stat_124131830` | -2.78757 |
| `explicit.stat_591105508@T1` | 2.24959 |
| `explicit.stat_4226189338@T1` | 2.19098 |
| `explicit.stat_124131830@T1` | 2.14704 |
| `explicit.stat_736967255@T2` | 1.45879 |
| `crafted.stat_124131830` | 1.24569 |
| `explicit.stat_2254480358@T2` | 1.17389 |
| `explicit.stat_2768835289@T2` | 1.16329 |
| `explicit.stat_1600707273@T1` | 0.69471 |
| `explicit.stat_4226189338@T2` | 0.50658 |

### weapon.bow — n=14113, R²=-2.0676

intercept: `3.3780`  ·  log_price: True  ·  ilvl: `-0.04105`  ·  n_mods: `-0.02346`  ·  n_top_tier: `0.70975`  ·  corrupted: `-0.06876`  ·  n_sockets: `-0.00530`  ·  quality: `0.02644`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.06276 |
| `explicit.stat_1202301673@T1` | 1.53558 |
| `crafted.stat_3035140377` | 1.31437 |
| `explicit.stat_1263695895@T1` | -0.80758 |
| `explicit.stat_1509134228@T1` | -0.76320 |
| `explicit.stat_669069897@T1` | -0.75899 |
| `explicit.stat_1263695895@T2` | -0.75888 |
| `explicit.stat_3695891184@T1` | -0.75236 |
| `explicit.stat_3695891184@T2` | -0.75011 |
| `explicit.stat_55876295@T1` | -0.74173 |
| `explicit.stat_1368271171@T2` | -0.73910 |
| `explicit.stat_3336890334@T2` | -0.73884 |

### weapon.crossbow — n=13339, R²=-1.9755

intercept: `3.7212`  ·  log_price: True  ·  ilvl: `-0.04587`  ·  n_mods: `-0.00996`  ·  n_top_tier: `0.72336`  ·  corrupted: `-0.01244`  ·  n_sockets: `0.01744`  ·  quality: `0.00997`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -3.08076 |
| `explicit.stat_2250681686` | 2.42651 |
| `explicit.stat_1980802737@T2` | -1.95099 |
| `explicit.stat_709508406@T1` | 1.49809 |
| `explicit.stat_1202301673@T1` | 1.37436 |
| `explicit.stat_1980802737` | 1.18533 |
| `explicit.stat_1263695895@T1` | -0.90887 |
| `explicit.stat_1263695895@T2` | -0.90834 |
| `crafted.stat_3035140377` | 0.88932 |
| `explicit.stat_1202301673@T2` | -0.84409 |
| `explicit.stat_669069897@T1` | -0.79622 |
| `explicit.stat_1037193709@T2` | -0.77022 |

### flask.charm — n=11454, R²=-0.516

intercept: `0.0007`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.03208`  ·  corrupted: `1.92922`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.51780 |
| `explicit.stat_1056492907` | 3.40538 |
| `explicit.stat_828533480@T2` | -2.03209 |
| `explicit.stat_3196823591@T2` | -2.03208 |
| `explicit.stat_1873752457@T2` | -2.03208 |
| `explicit.stat_1120862500@T2` | -2.03208 |
| `explicit.stat_2676834156@T2` | -2.03208 |
| `explicit.stat_1366840608@T2` | -2.03207 |
| `explicit.stat_388617051@T2` | -2.03207 |
| `explicit.stat_1873752457@T1` | -2.03207 |
| `explicit.stat_2541588185@T2` | -2.03207 |
| `explicit.stat_828533480@T1` | -2.03206 |

### weapon.warstaff — n=7843, R²=-0.5355

intercept: `-3.5681`  ·  log_price: True  ·  ilvl: `0.04998`  ·  n_mods: `-0.11536`  ·  n_top_tier: `0.66853`  ·  corrupted: `0.19988`  ·  n_sockets: `0.07376`  ·  quality: `0.05934`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.30590 |
| `explicit.stat_328541901@T1` | -1.01034 |
| `explicit.stat_328541901@T2` | -0.99605 |
| `explicit.stat_1037193709@T1` | 0.92872 |
| `explicit.stat_55876295@T2` | -0.81712 |
| `crafted.stat_210067635@T2` | 0.80760 |
| `explicit.stat_55876295@T1` | -0.77212 |
| `explicit.stat_1037193709@T2` | -0.73402 |
| `explicit.stat_691932474@T2` | -0.72683 |
| `explicit.stat_3336890334@T2` | -0.71076 |
| `explicit.stat_791928121@T2` | -0.68121 |
| `explicit.stat_210067635@T1` | -0.67392 |

### weapon.sceptre — n=7232, R²=-0.4695

intercept: `-11.1706`  ·  log_price: True  ·  ilvl: `0.14093`  ·  n_mods: `-0.05310`  ·  n_top_tier: `0.57003`  ·  corrupted: `0.39295`  ·  n_sockets: `0.19684`  ·  quality: `0.07831`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.28456 |
| `explicit.stat_2162097452@T2` | 1.34097 |
| `explicit.stat_1263695895@T1` | -1.04575 |
| `explicit.stat_4080418644@T1` | -1.02521 |
| `explicit.stat_1574590649@T2` | -0.97445 |
| `explicit.stat_1263695895@T2` | -0.85603 |
| `explicit.stat_2347036682@T2` | -0.80210 |
| `explicit.stat_289128254@T2` | -0.79009 |
| `explicit.stat_4080418644@T2` | -0.73430 |
| `explicit.stat_1050105434@T2` | -0.65368 |
| `explicit.stat_2854751904@T2` | -0.62024 |
| `explicit.stat_3639275092@T2` | -0.61445 |

### weapon.staff — n=7217, R²=-0.5616

intercept: `-6.6213`  ·  log_price: True  ·  ilvl: `0.08404`  ·  n_mods: `-0.04801`  ·  n_top_tier: `0.30627`  ·  corrupted: `0.02768`  ·  n_sockets: `0.18456`  ·  quality: `0.05872`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.03482 |
| `explicit.stat_124131830@T1` | 1.94681 |
| `explicit.stat_1545858329@T1` | 1.52179 |
| `explicit.stat_2768835289@T2` | 1.23298 |
| `explicit.stat_2254480358@T1` | 1.21063 |
| `explicit.stat_4226189338@T2` | 0.94322 |
| `explicit.stat_1600707273@T1` | 0.92689 |
| `explicit.stat_3962278098@T2` | 0.69926 |
| `rune.stat_124131830` | 0.69471 |
| `explicit.stat_2254480358@T2` | 0.64609 |
| `explicit.stat_2974417149@T1` | -0.58997 |
| `explicit.stat_473429811@T1` | 0.48240 |

### weapon.spear — n=6049, R²=-0.6423

intercept: `-4.0248`  ·  log_price: True  ·  ilvl: `0.05340`  ·  n_mods: `-0.02025`  ·  n_top_tier: `0.51430`  ·  corrupted: `-0.06862`  ·  n_sockets: `0.10060`  ·  quality: `0.09520`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.96604 |
| `explicit.stat_1202301673@T1` | 2.38111 |
| `explicit.stat_9187492@T1` | 2.37296 |
| `crafted.stat_3035140377` | 1.26781 |
| `explicit.stat_210067635@T1` | 0.80561 |
| `explicit.stat_1509134228@T1` | 0.77181 |
| `explicit.stat_1263695895@T2` | -0.72835 |
| `explicit.stat_55876295@T1` | -0.61814 |
| `explicit.stat_55876295@T2` | -0.58169 |
| `explicit.stat_1940865751@T2` | -0.51526 |
| `explicit.stat_1509134228@T2` | -0.50181 |
| `explicit.stat_4080418644@T2` | -0.49925 |

### armour.focus — n=4941, R²=-0.4651

intercept: `-9.6419`  ·  log_price: True  ·  ilvl: `0.12003`  ·  n_mods: `-0.05199`  ·  n_top_tier: `0.83897`  ·  corrupted: `0.76532`  ·  n_sockets: `0.41612`  ·  quality: `0.07274`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 5.69120 |
| `crafted.stat_737908626@T2` | -2.57611 |
| `explicit.stat_4220027924@T2` | -1.24815 |
| `explicit.stat_3962278098@T2` | -1.00407 |
| `explicit.stat_736967255@T2` | -0.99324 |
| `explicit.stat_328541901@T2` | -0.93970 |
| `explicit.stat_2339757871@T2` | -0.92525 |
| `explicit.stat_3291658075@T1` | -0.91399 |
| `explicit.stat_2923486259@T1` | -0.91037 |
| `explicit.stat_3962278098@T1` | -0.89718 |
| `explicit.stat_737908626@T2` | -0.89229 |
| `explicit.stat_4220027924@T1` | -0.89205 |

### armour.quiver — n=4608, R²=-0.4404

intercept: `-9.3356`  ·  log_price: True  ·  ilvl: `0.11535`  ·  n_mods: `-0.03599`  ·  n_top_tier: `0.77126`  ·  corrupted: `0.76196`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 7.22186 |
| `explicit.stat_2463230181@T1` | 2.19757 |
| `explicit.stat_2321178454@T2` | -1.21873 |
| `explicit.stat_681332047@T2` | -1.10335 |
| `explicit.stat_2463230181@T2` | 1.04495 |
| `explicit.stat_3261801346@T1` | -0.98205 |
| `explicit.stat_2194114101@T2` | -0.95597 |
| `explicit.stat_1573130764@T1` | -0.92497 |
| `explicit.stat_1573130764@T2` | -0.89989 |
| `explicit.stat_4067062424@T1` | -0.86337 |
| `explicit.stat_1368271171@T2` | -0.84105 |
| `explicit.stat_2321178454@T1` | -0.80688 |

### armour.shield — n=4043, R²=-0.5628

intercept: `-8.4075`  ·  log_price: True  ·  ilvl: `0.10918`  ·  n_mods: `-0.05541`  ·  n_top_tier: `0.66329`  ·  corrupted: `0.15558`  ·  n_sockets: `0.06632`  ·  quality: `0.05391`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.98962 |
| `explicit.stat_1011760251@T1` | -1.33206 |
| `explicit.stat_2339757871@T1` | -1.24597 |
| `explicit.stat_1011760251@T2` | -1.01783 |
| `explicit.stat_328541901@T1` | -1.00936 |
| `explicit.stat_2481353198@T1` | -0.98914 |
| `explicit.stat_2481353198@T2` | -0.98801 |
| `explicit.stat_328541901@T2` | -0.87512 |
| `explicit.stat_2881298780@T1` | -0.85873 |
| `explicit.stat_3321629045@T2` | -0.84509 |
| `explicit.stat_1978899297@T2` | -0.81328 |
| `explicit.stat_4095671657@T1` | -0.79087 |

### weapon.twomace — n=3709, R²=-0.4849

intercept: `-10.0083`  ·  log_price: True  ·  ilvl: `0.13154`  ·  n_mods: `-0.11593`  ·  n_top_tier: `0.40168`  ·  corrupted: `0.69428`  ·  n_sockets: `0.13099`  ·  quality: `0.04585`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.52725 |
| `desecrated.stat_1509134228@T1` | 2.33471 |
| `explicit.stat_1037193709@T1` | -1.47955 |
| `crafted.stat_3035140377` | 1.10801 |
| `explicit.stat_3336890334@T1` | -0.95851 |
| `explicit.stat_387439868@T2` | -0.93925 |
| `explicit.stat_821021828@T2` | -0.76012 |
| `explicit.stat_1037193709@T2` | -0.72406 |
| `explicit.stat_3695891184@T1` | -0.67691 |
| `explicit.stat_1263695895@T1` | -0.65297 |
| `explicit.stat_518292764@T2` | -0.64872 |
| `explicit.stat_3695891184@T2` | -0.62740 |

## Coverage (listings per base)

- … **Sapphire** — 21179 listings (21149 priced) [0.3–7553463.8 ex]
- … **Emerald** — 20912 listings (20884 priced) [0.3–7553463.8 ex]
- … **Ruby** — 16004 listings (15990 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 8877 listings (8868 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 7166 listings (7156 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 7011 listings (6998 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 6876 listings (6870 priced) [0.2–19945827.9 ex]
- … **Stellar Amulet** — 6584 listings (6580 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 6565 listings (6555 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 6413 listings (6402 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5533 listings (5518 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5366 listings (5360 priced) [0.2–307202867.9 ex]
- … **Ruby Ring** — 5159 listings (5156 priced) [0.2–37474957.5 ex]
- … **Topaz Ring** — 5153 listings (5149 priced) [0.3–307202867.9 ex]
- … **Plate Belt** — 4703 listings (4689 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4634 listings (4629 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4528 listings (4521 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4479 listings (4477 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4464 listings (4459 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4432 listings (4426 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4317 listings (4313 priced) [0.3–4275054.0 ex]
- … **Obliterator Bow** — 4227 listings (4214 priced) [0.3–42622633798.0 ex]
- … **Heavy Belt** — 4195 listings (4193 priced) [0.3–2608914286.6 ex]
- … **Pearl Ring** — 4149 listings (4144 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 4068 listings (4068 priced) [0.3–123132003.2 ex]

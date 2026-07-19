# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-19T13:14:45+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **651682** (649646 priced in exalted)
- Distinct bases: 996 · distinct mods: 3280 · mod rows: 3087122
- Sold signals: **24605** sold · 370812 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-19T13:01:49+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×21.73** (median |log error| 3.0788)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.16** · typical error ×59.28 · ±30% 5% · n=94916
- Premium segment (60ex+): skill **+0.16** · typical error ×278.49 · ±30% 0% · n=64111

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 13710 | ×55.48 | 21% | +0.03 | +0.05 |
| jewel | 13078 | ×10.51 | 4% | +0.10 | +0.12 |
| accessory.amulet | 12405 | ×40.35 | 18% | +0.04 | +0.03 |
| accessory.belt | 8992 | ×20.35 | 14% | +0.07 | +0.10 |
| armour.chest | 8713 | ×17.80 | 20% | +0.09 | +0.11 |
| armour.helmet | 8495 | ×20.63 | 10% | +0.11 | +0.13 |
| armour.boots | 7902 | ×27.32 | 19% | +0.10 | +0.13 |
| armour.gloves | 7768 | ×34.81 | 13% | +0.10 | +0.11 |
| other | 7652 | ×2.26 | 42% | +0.10 | +0.16 |
| weapon.wand | 4661 | ×45.77 | 15% | +0.09 | +0.11 |
| weapon.bow | 3671 | ×26.72 | 12% | +0.15 | +0.15 |
| weapon.crossbow | 3391 | ×26.44 | 15% | +0.11 | +0.16 |
| weapon.warstaff | 2287 | ×19.37 | 6% | +0.21 | +0.21 |
| weapon.staff | 2212 | ×26.39 | 6% | +0.17 | +0.15 |
| weapon.sceptre | 2165 | ×26.04 | 5% | +0.13 | +0.13 |
| weapon.spear | 1712 | ×21.53 | 8% | +0.12 | +0.12 |
| armour.focus | 1423 | ×19.73 | 6% | +0.10 | +0.12 |
| armour.quiver | 1366 | ×24.54 | 7% | +0.16 | +0.17 |
| flask.charm | 1115 | ×13.92 | 30% | -0.00 | +0.01 |
| armour.shield | 1113 | ×16.22 | 8% | +0.08 | +0.10 |
| weapon.twomace | 1037 | ×7.91 | 8% | +0.10 | +0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=70807, R²=-0.9636

intercept: `-1.9062`  ·  log_price: True  ·  ilvl: `0.02526`  ·  n_mods: `0.90086`  ·  n_top_tier: `-0.35385`  ·  corrupted: `0.32645`  ·  quality: `-0.00434`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.61096 |
| `explicit.stat_3374165039@T1` | -2.39855 |
| `explicit.stat_3485067555@T1` | 2.23445 |
| `explicit.stat_1569101201@T1` | -1.68836 |
| `explicit.stat_3780644166@T1` | -1.65328 |
| `explicit.stat_4147897060@T1` | -1.59151 |
| `explicit.stat_1594812856@T1` | 1.40733 |
| `explicit.stat_2523933828@T1` | -1.35337 |
| `explicit.stat_1697447343@T1` | -1.30015 |
| `explicit.stat_318953428@T1` | -1.27738 |
| `explicit.stat_1805182458@T1` | -1.21682 |
| `explicit.stat_3166958180@T1` | -1.20279 |

### accessory.ring — n=62566, R²=-2.0286

intercept: `3.2240`  ·  log_price: True  ·  ilvl: `-0.03987`  ·  n_mods: `0.00099`  ·  n_top_tier: `1.10025`  ·  corrupted: `0.01367`  ·  n_sockets: `0.33628`  ·  quality: `0.02431`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.13800 |
| `explicit.stat_1573130764@T2` | -1.12663 |
| `explicit.stat_4220027924@T2` | -1.12483 |
| `explicit.stat_803737631@T1` | -1.12481 |
| `explicit.stat_2231156303@T1` | -1.11959 |
| `explicit.stat_4080418644@T1` | -1.11629 |
| `explicit.stat_2901986750@T2` | -1.11338 |
| `explicit.stat_3325883026@T1` | -1.11107 |
| `explicit.stat_789117908@T2` | -1.10943 |
| `explicit.stat_789117908@T1` | -1.10854 |
| `explicit.stat_3032590688@T2` | -1.10749 |
| `explicit.stat_3962278098@T1` | -1.10701 |

### other — n=62092, R²=-0.626

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00005`  ·  n_top_tier: `0.34706`  ·  corrupted: `0.31873`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.50899 |
| `implicit.stat_2219129443` | 0.41464 |
| `explicit.stat_3299347043@T1` | -0.25801 |
| `implicit.stat_3879011313` | 0.23142 |
| `implicit.stat_4041853756` | 0.12452 |
| `explicit.stat_2968503605@T1` | -0.11637 |
| `explicit.stat_2974417149@T1` | 0.11085 |
| `explicit.stat_3917489142@T1` | 0.10252 |
| `explicit.stat_3291658075@T1` | -0.09960 |
| `explicit.stat_2482852589@T1` | 0.09097 |
| `explicit.stat_789117908@T1` | -0.07422 |
| `implicit.stat_1379411836` | -0.07298 |

### accessory.amulet — n=56662, R²=-2.1547

intercept: `3.7451`  ·  log_price: True  ·  ilvl: `-0.04583`  ·  n_mods: `-0.02429`  ·  n_top_tier: `1.36681`  ·  corrupted: `0.05853`  ·  n_sockets: `-0.16737`  ·  quality: `-0.00043`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -2.03853 |
| `explicit.stat_3299347043@T2` | -1.77295 |
| `explicit.stat_587431675@T2` | -1.49679 |
| `explicit.stat_2974417149@T1` | -1.47728 |
| `explicit.stat_803737631@T1` | -1.45832 |
| `explicit.stat_2866361420@T2` | -1.44812 |
| `explicit.stat_2866361420@T1` | -1.43637 |
| `explicit.stat_2974417149@T2` | -1.43123 |
| `explicit.stat_1050105434@T2` | -1.42026 |
| `explicit.stat_803737631@T2` | -1.41802 |
| `explicit.stat_472520716@T2` | -1.40949 |
| `explicit.stat_1671376347@T2` | -1.40097 |

### accessory.belt — n=41428, R²=-1.481

intercept: `4.8179`  ·  log_price: True  ·  ilvl: `-0.05624`  ·  n_mods: `-0.05389`  ·  n_top_tier: `0.60213`  ·  corrupted: `1.18127`  ·  n_sockets: `0.94042`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.03083 |
| `explicit.stat_3299347043@T1` | -0.92543 |
| `explicit.stat_3299347043@T2` | -0.71636 |
| `explicit.stat_2881298780@T1` | -0.67450 |
| `explicit.stat_51994685@T1` | -0.64827 |
| `explicit.stat_4220027924@T2` | -0.64539 |
| `explicit.stat_1570770415@T2` | -0.63483 |
| `explicit.stat_3325883026@T1` | -0.62762 |
| `explicit.stat_3372524247@T2` | -0.62295 |
| `explicit.stat_1389754388@T1` | -0.62182 |
| `explicit.stat_1570770415@T1` | -0.61979 |
| `explicit.stat_4220027924@T1` | 0.60991 |

### armour.chest — n=41035, R²=-1.6771

intercept: `3.6401`  ·  log_price: True  ·  ilvl: `-0.04489`  ·  n_mods: `-0.02486`  ·  n_top_tier: `0.39780`  ·  corrupted: `0.17360`  ·  n_sockets: `0.03165`  ·  quality: `0.07338`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.88269 |
| `explicit.stat_3981240776@T1` | 0.91236 |
| `explicit.stat_986397080@T2` | -0.51538 |
| `explicit.stat_986397080@T1` | -0.50289 |
| `explicit.stat_3372524247@T1` | 0.49819 |
| `explicit.stat_2339757871@T2` | -0.49412 |
| `explicit.stat_3484657501@T1` | -0.46406 |
| `explicit.stat_2339757871@T1` | -0.44980 |
| `explicit.stat_1692879867@T2` | -0.44958 |
| `explicit.stat_4080418644@T1` | -0.44555 |
| `explicit.stat_915769802@T2` | -0.44033 |
| `explicit.stat_2451402625@T1` | -0.43111 |

### armour.helmet — n=39924, R²=-1.378

intercept: `3.6808`  ·  log_price: True  ·  ilvl: `-0.04601`  ·  n_mods: `-0.06078`  ·  n_top_tier: `0.47114`  ·  corrupted: `0.69051`  ·  n_sockets: `0.11641`  ·  quality: `0.05676`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.08595 |
| `explicit.stat_3917489142@T2` | -1.02291 |
| `crafted.stat_3917489142@T1` | -0.95207 |
| `explicit.stat_3917489142@T1` | -0.81324 |
| `explicit.stat_1263695895@T1` | -0.75971 |
| `explicit.stat_2162097452@T2` | -0.68716 |
| `explicit.stat_1999113824@T1` | -0.67599 |
| `explicit.stat_2923486259@T1` | 0.65733 |
| `explicit.stat_3321629045@T2` | -0.62747 |
| `explicit.stat_803737631@T1` | -0.62231 |
| `explicit.stat_1263695895@T2` | -0.58639 |
| `explicit.stat_2162097452@T1` | 0.57385 |

### armour.boots — n=37081, R²=-1.6737

intercept: `3.7427`  ·  log_price: True  ·  ilvl: `-0.04606`  ·  n_mods: `-0.02502`  ·  n_top_tier: `0.54949`  ·  corrupted: `0.04875`  ·  n_sockets: `0.04016`  ·  quality: `0.06386`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.66513 |
| `crafted.stat_3917489142@T1` | 1.32889 |
| `explicit.stat_2339757871@T1` | -1.18607 |
| `explicit.stat_2923486259@T1` | 0.82459 |
| `explicit.stat_3299347043@T1` | -0.74280 |
| `explicit.stat_3917489142@T2` | -0.72192 |
| `explicit.stat_2923486259@T2` | -0.64963 |
| `explicit.stat_1062208444@T2` | -0.61160 |
| `explicit.stat_3917489142@T1` | -0.60388 |
| `explicit.stat_2160282525@T1` | -0.60324 |
| `explicit.stat_1874553720@T1` | -0.60201 |
| `explicit.stat_1999113824@T2` | -0.59877 |

### armour.gloves — n=36100, R²=-1.5309

intercept: `3.9019`  ·  log_price: True  ·  ilvl: `-0.05066`  ·  n_mods: `-0.03335`  ·  n_top_tier: `0.78037`  ·  corrupted: `-0.03485`  ·  n_sockets: `0.17620`  ·  quality: `0.05033`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.11593 |
| `explicit.stat_2923486259@T1` | -1.55847 |
| `explicit.stat_3484657501@T2` | -1.10267 |
| `explicit.stat_3321629045@T2` | -1.09948 |
| `explicit.stat_2923486259@T2` | -1.09419 |
| `rune.stat_836936635` | 1.09383 |
| `explicit.stat_803737631@T2` | -1.03556 |
| `explicit.stat_4015621042@T2` | -0.99716 |
| `explicit.stat_3484657501@T1` | -0.99643 |
| `explicit.stat_803737631@T1` | -0.97730 |
| `explicit.stat_4052037485@T1` | -0.95882 |
| `explicit.stat_3321629045@T1` | -0.93037 |

### weapon.wand — n=21746, R²=-1.9688

intercept: `3.7908`  ·  log_price: True  ·  ilvl: `-0.04712`  ·  n_mods: `-0.05324`  ·  n_top_tier: `0.48451`  ·  corrupted: `-0.01079`  ·  n_sockets: `0.07011`  ·  quality: `0.02558`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.80522 |
| `explicit.stat_1545858329@T1` | 2.54184 |
| `explicit.stat_2254480358@T1` | 2.29642 |
| `explicit.stat_124131830@T1` | 2.26861 |
| `explicit.stat_591105508@T1` | 1.86720 |
| `explicit.stat_4226189338@T1` | 1.80598 |
| `explicit.stat_736967255@T2` | 1.74113 |
| `crafted.stat_124131830` | 1.17924 |
| `explicit.stat_1600707273@T1` | 0.96055 |
| `explicit.stat_2254480358@T2` | 0.94434 |
| `explicit.stat_1263695895@T2` | -0.92321 |
| `explicit.stat_4226189338@T2` | 0.83720 |

### flask.charm — n=17928, R²=-0.6163

intercept: `0.1062`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.60826`  ·  corrupted: `1.60049`  ·  quality: `0.00127`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.74155 |
| `explicit.stat_1056492907` | 2.69655 |
| `explicit.stat_828533480@T2` | -1.60829 |
| `explicit.stat_1120862500@T2` | -1.60826 |
| `explicit.stat_1873752457@T2` | -1.60826 |
| `explicit.stat_388617051@T2` | -1.60825 |
| `explicit.stat_3196823591@T2` | -1.60823 |
| `explicit.stat_2365392475@T2` | -1.60823 |
| `explicit.stat_828533480@T1` | -1.60822 |
| `explicit.stat_1873752457@T1` | -1.60816 |
| `explicit.stat_2676834156@T2` | -1.60738 |
| `explicit.stat_1366840608@T2` | -1.59537 |

### weapon.bow — n=17362, R²=-1.7795

intercept: `3.9483`  ·  log_price: True  ·  ilvl: `-0.04638`  ·  n_mods: `-0.08732`  ·  n_top_tier: `0.67036`  ·  corrupted: `0.45818`  ·  n_sockets: `0.09129`  ·  quality: `0.03253`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.72883 |
| `crafted.stat_3035140377` | 1.34680 |
| `explicit.stat_3336890334@T1` | 1.32139 |
| `desecrated.stat_666077204@T1` | 1.24718 |
| `explicit.stat_1263695895@T1` | -1.02643 |
| `explicit.stat_1263695895@T2` | -0.91268 |
| `explicit.stat_2463230181@T2` | -0.83725 |
| `explicit.stat_709508406@T1` | 0.82805 |
| `explicit.stat_1509134228@T1` | -0.78745 |
| `explicit.stat_3695891184@T2` | -0.76598 |
| `explicit.stat_3639275092@T1` | -0.76353 |
| `explicit.stat_210067635@T2` | -0.75328 |

### weapon.crossbow — n=16297, R²=-1.761

intercept: `3.9293`  ·  log_price: True  ·  ilvl: `-0.04726`  ·  n_mods: `-0.08311`  ·  n_top_tier: `0.44449`  ·  corrupted: `0.06490`  ·  n_sockets: `0.08896`  ·  quality: `0.02418`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.48859 |
| `explicit.stat_1202301673@T1` | 1.44517 |
| `explicit.stat_1980802737` | 1.30964 |
| `explicit.stat_2250681686@T2` | -1.14714 |
| `explicit.stat_709508406@T1` | 0.85797 |
| `explicit.stat_2250681686` | 0.84630 |
| `crafted.stat_3035140377` | 0.72981 |
| `explicit.stat_1509134228@T1` | 0.70351 |
| `explicit.stat_1263695895@T2` | -0.65304 |
| `explicit.stat_1509134228@T2` | -0.64873 |
| `explicit.stat_3336890334@T1` | -0.63894 |
| `explicit.stat_3336890334@T2` | -0.62734 |

### weapon.warstaff — n=11075, R²=-0.3437

intercept: `-10.7800`  ·  log_price: True  ·  ilvl: `0.14425`  ·  n_mods: `-0.20148`  ·  n_top_tier: `0.29171`  ·  corrupted: `0.39622`  ·  n_sockets: `0.15638`  ·  quality: `0.06111`

| stat_id | coef |
|---|---|
| `desecrated.stat_3291658075@T1` | -1.44728 |
| `desecrated.stat_473429811@T1` | -1.44728 |
| `crafted.stat_210067635@T2` | 1.29002 |
| `desecrated.stat_2231156303@T1` | 1.09754 |
| `desecrated.stat_2527686725@T1` | 1.09754 |
| `explicit.stat_1037193709@T1` | 0.82613 |
| `explicit.stat_1509134228@T1` | 0.79193 |
| `explicit.stat_328541901@T2` | -0.76994 |
| `explicit.stat_328541901@T1` | -0.76961 |
| `desecrated.stat_9187492` | 0.74100 |
| `explicit.stat_9187492@T1` | 0.69299 |
| `explicit.stat_518292764@T1` | 0.65743 |

### weapon.staff — n=10434, R²=-0.3787

intercept: `-16.1586`  ·  log_price: True  ·  ilvl: `0.20716`  ·  n_mods: `-0.06130`  ·  n_top_tier: `0.44387`  ·  corrupted: `0.74858`  ·  n_sockets: `0.18382`  ·  quality: `0.03558`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.20425 |
| `explicit.stat_591105508@T1` | 2.06054 |
| `explicit.stat_1545858329@T1` | 1.92614 |
| `explicit.stat_124131830@T1` | 1.74461 |
| `explicit.stat_293638271@T2` | -1.36463 |
| `explicit.stat_2254480358@T1` | 1.31058 |
| `explicit.stat_1600707273@T1` | 1.06745 |
| `explicit.stat_2254480358@T2` | 0.91662 |
| `explicit.stat_124131830@T2` | 0.65734 |
| `explicit.stat_591105508@T2` | 0.63445 |
| `explicit.stat_4226189338@T2` | 0.61040 |
| `explicit.stat_3291658075@T2` | -0.60151 |

### weapon.sceptre — n=10272, R²=-0.3402

intercept: `-21.6923`  ·  log_price: True  ·  ilvl: `0.27727`  ·  n_mods: `0.03266`  ·  n_top_tier: `0.36365`  ·  corrupted: `-0.09806`  ·  n_sockets: `0.23218`  ·  quality: `0.02790`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.24193 |
| `explicit.stat_3057012405@T1` | 1.27179 |
| `explicit.stat_2162097452@T2` | 1.11125 |
| `explicit.stat_2854751904@T2` | -0.78283 |
| `explicit.stat_1250712710@T2` | 0.70691 |
| `explicit.stat_101878827@T2` | 0.61984 |
| `explicit.stat_770672621@T1` | -0.61217 |
| `explicit.stat_849987426@T1` | 0.59723 |
| `explicit.stat_1798257884@T2` | 0.58483 |
| `explicit.stat_101878827@T1` | 0.56854 |
| `explicit.stat_2347036682@T2` | -0.55178 |
| `explicit.stat_1250712710@T1` | 0.51540 |

### weapon.spear — n=8282, R²=-0.3924

intercept: `-12.2027`  ·  log_price: True  ·  ilvl: `0.17036`  ·  n_mods: `-0.19842`  ·  n_top_tier: `0.75434`  ·  corrupted: `-0.05741`  ·  n_sockets: `0.15730`  ·  quality: `0.07045`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -5.02820 |
| `explicit.stat_1202301673@T1` | 1.56604 |
| `explicit.stat_1509134228@T1` | 1.40946 |
| `desecrated.stat_210067635@T1` | -1.32716 |
| `explicit.stat_9187492@T1` | 1.18253 |
| `explicit.stat_1940865751@T2` | -1.13398 |
| `explicit.stat_9187492@T2` | -1.06945 |
| `explicit.stat_691932474@T1` | -1.05704 |
| `explicit.stat_691932474@T2` | -1.01548 |
| `crafted.stat_3035140377` | 1.00811 |
| `explicit.stat_4080418644@T2` | -0.99944 |
| `explicit.stat_3261801346@T1` | -0.86240 |

### armour.focus — n=6762, R²=-0.3328

intercept: `-14.9618`  ·  log_price: True  ·  ilvl: `0.19183`  ·  n_mods: `-0.16345`  ·  n_top_tier: `0.95505`  ·  corrupted: `0.10485`  ·  n_sockets: `0.34561`  ·  quality: `0.05385`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 1.68526 |
| `explicit.stat_2923486259@T1` | -1.58278 |
| `explicit.stat_4220027924@T1` | -1.48550 |
| `explicit.stat_4220027924@T2` | -1.30134 |
| `explicit.stat_2974417149@T1` | -1.23833 |
| `explicit.stat_2339757871@T2` | -1.16266 |
| `explicit.stat_2974417149@T2` | -1.15953 |
| `explicit.stat_2231156303@T2` | -1.07870 |
| `explicit.stat_274716455@T2` | -1.07547 |
| `explicit.stat_2231156303@T1` | -1.04117 |
| `explicit.stat_1050105434@T2` | -1.00105 |
| `explicit.stat_3291658075@T1` | -0.98298 |

### armour.quiver — n=6358, R²=-0.2981

intercept: `-15.9207`  ·  log_price: True  ·  ilvl: `0.19491`  ·  n_mods: `-0.13439`  ·  n_top_tier: `0.89833`  ·  corrupted: `0.72931`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.02824 |
| `explicit.stat_2463230181@T1` | 1.74695 |
| `explicit.stat_1573130764@T1` | -1.42312 |
| `explicit.stat_681332047@T2` | -1.40370 |
| `explicit.stat_1573130764@T2` | -1.21711 |
| `explicit.stat_803737631@T2` | -1.09755 |
| `explicit.stat_803737631@T1` | -1.00837 |
| `explicit.stat_681332047@T1` | -0.97043 |
| `explicit.stat_2194114101@T2` | -0.93433 |
| `explicit.stat_4067062424@T1` | -0.92803 |
| `explicit.stat_2321178454@T2` | -0.89747 |
| `explicit.stat_4067062424@T2` | -0.89050 |

### armour.shield — n=5455, R²=-0.4457

intercept: `-13.4563`  ·  log_price: True  ·  ilvl: `0.17706`  ·  n_mods: `-0.06923`  ·  n_top_tier: `0.65874`  ·  corrupted: `-0.30753`  ·  n_sockets: `0.37914`  ·  quality: `0.06749`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.36667 |
| `explicit.stat_3321629045@T2` | -1.23395 |
| `explicit.stat_3484657501@T1` | -1.19910 |
| `explicit.stat_3855016469@T1` | -1.08306 |
| `explicit.stat_2901986750@T1` | -1.03918 |
| `explicit.stat_3033371881@T2` | -1.02269 |
| `explicit.stat_3484657501@T2` | -1.01215 |
| `explicit.stat_1671376347@T1` | -0.94540 |
| `explicit.stat_1301765461@T1` | 0.90671 |
| `explicit.stat_4095671657@T2` | -0.87585 |
| `explicit.stat_2451402625@T1` | -0.87161 |
| `explicit.stat_328541901@T1` | -0.82497 |

### weapon.twomace — n=5036, R²=-0.4451

intercept: `-10.3301`  ·  log_price: True  ·  ilvl: `0.14199`  ·  n_mods: `-0.21330`  ·  n_top_tier: `0.46988`  ·  corrupted: `0.20938`  ·  n_sockets: `0.17548`  ·  quality: `0.06185`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.24557 |
| `desecrated.stat_1509134228@T1` | 1.87702 |
| `explicit.stat_1037193709@T1` | -1.58270 |
| `explicit.stat_3336890334@T1` | -1.22803 |
| `explicit.stat_9187492@T1` | -1.02789 |
| `explicit.stat_1263695895@T2` | -0.97672 |
| `explicit.stat_691932474@T1` | -0.96912 |
| `explicit.stat_387439868@T2` | -0.92320 |
| `explicit.stat_3695891184@T1` | -0.72625 |
| `explicit.stat_709508406@T1` | 0.69423 |
| `explicit.stat_821021828@T2` | -0.65514 |
| `crafted.stat_3035140377` | 0.62712 |

## Coverage (listings per base)

- … **Sapphire** — 32762 listings (32708 priced) [0.3–3985176410.3 ex]
- … **Emerald** — 31856 listings (31815 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 24431 listings (24401 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11826 listings (11808 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10583 listings (10560 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10256 listings (10232 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 10121 listings (10110 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 9580 listings (9558 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9469 listings (9447 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 9068 listings (9055 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7861 listings (7846 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7567 listings (7558 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7460 listings (7451 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6988 listings (6967 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6564 listings (6557 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 6477 listings (6458 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6470 listings (6456 priced) [0.3–4547453.5 ex]
- … **Plate Belt** — 6468 listings (6440 priced) [0.3–398912568423.8 ex]
- … **Amber Amulet** — 6432 listings (6425 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6356 listings (6327 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6254 listings (6245 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 6215 listings (6207 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5896 listings (5893 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5831 listings (5817 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5722 listings (5712 priced) [0.3–398912568423.8 ex]

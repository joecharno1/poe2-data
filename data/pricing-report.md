# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-22T04:59:20+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **729109** (726757 priced in exalted)
- Distinct bases: 1002 · distinct mods: 3329 · mod rows: 3445715
- Sold signals: **24084** sold · 415360 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-22T04:47:30+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.89** (median |log error| 3.1308)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×71.49 · ±30% 4% · n=105944
- Premium segment (60ex+): skill **+0.12** · typical error ×366.28 · ±30% 0% · n=70366

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 15705 | ×44.51 | 21% | +0.04 | +0.07 |
| jewel | 15151 | ×52.61 | 21% | +0.02 | +0.03 |
| accessory.amulet | 14103 | ×24.87 | 17% | +0.04 | +0.04 |
| accessory.belt | 9902 | ×20.09 | 23% | +0.02 | +0.05 |
| armour.chest | 9672 | ×18.02 | 21% | +0.08 | +0.11 |
| armour.helmet | 9397 | ×27.19 | 18% | +0.08 | +0.11 |
| armour.boots | 8656 | ×22.44 | 19% | +0.10 | +0.13 |
| other | 8538 | ×2.00 | 41% | +0.11 | +0.18 |
| armour.gloves | 8513 | ×34.94 | 15% | +0.07 | +0.10 |
| weapon.wand | 4989 | ×40.04 | 14% | +0.11 | +0.11 |
| weapon.bow | 3944 | ×25.62 | 13% | +0.16 | +0.16 |
| weapon.crossbow | 3711 | ×22.89 | 13% | +0.13 | +0.17 |
| weapon.warstaff | 2561 | ×14.32 | 7% | +0.16 | +0.16 |
| weapon.staff | 2495 | ×16.84 | 6% | +0.12 | +0.12 |
| weapon.sceptre | 2430 | ×18.64 | 5% | +0.07 | +0.08 |
| weapon.spear | 1950 | ×13.52 | 7% | +0.11 | +0.14 |
| armour.focus | 1623 | ×13.36 | 7% | +0.09 | +0.10 |
| armour.quiver | 1514 | ×16.92 | 7% | +0.12 | +0.13 |
| flask.charm | 1242 | ×9.97 | 29% | +0.02 | +0.02 |
| armour.shield | 1234 | ×8.65 | 8% | +0.10 | +0.11 |
| weapon.twomace | 1132 | ×9.39 | 7% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=83116, R²=-1.8736

intercept: `-0.0951`  ·  log_price: True  ·  ilvl: `0.00117`  ·  n_mods: `0.97780`  ·  n_top_tier: `-0.89520`  ·  corrupted: `1.18758`  ·  quality: `-0.06520`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 3.30689 |
| `explicit.stat_1604736568@T1` | -2.20965 |
| `explicit.stat_1604736568` | 2.12922 |
| `explicit.stat_3556824919@T1` | 1.25250 |
| `explicit.stat_681332047@T1` | -0.90489 |
| `explicit.stat_2194114101@T1` | -0.89514 |
| `explicit.stat_3714003708@T1` | 0.83807 |
| `explicit.stat_274716455@T1` | -0.83623 |
| `explicit.stat_3473929743@T1` | -0.47718 |
| `explicit.stat_681332047` | 0.41149 |
| `explicit.stat_4045894391@T1` | -0.36353 |
| `explicit.stat_3596695232@T1` | -0.33250 |

### accessory.ring — n=71648, R²=-2.019

intercept: `3.3373`  ·  log_price: True  ·  ilvl: `-0.04167`  ·  n_mods: `0.00036`  ·  n_top_tier: `0.99301`  ·  corrupted: `0.00169`  ·  n_sockets: `2.19826`  ·  quality: `0.02173`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.04062 |
| `explicit.stat_1263695895@T2` | -1.02417 |
| `explicit.stat_3032590688@T1` | -1.01369 |
| `explicit.stat_4080418644@T1` | -1.01318 |
| `explicit.stat_2891184298@T1` | -1.01295 |
| `explicit.stat_3325883026@T1` | -1.01241 |
| `explicit.stat_2891184298@T2` | -1.01207 |
| `explicit.stat_1263695895@T1` | -1.00795 |
| `explicit.stat_2923486259@T2` | -1.00706 |
| `explicit.stat_3291658075@T2` | -1.00699 |
| `explicit.stat_1573130764@T2` | -1.00654 |
| `explicit.stat_803737631@T1` | -1.00524 |

### other — n=69385, R²=-0.6658

intercept: `1.6093`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.09734`  ·  n_top_tier: `0.24923`  ·  corrupted: `0.00420`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.36331 |
| `implicit.stat_718638445` | 0.29207 |
| `implicit.stat_3182714256` | 0.29206 |
| `explicit.stat_3299347043@T1` | -0.22552 |
| `implicit.stat_2219129443` | 0.22051 |
| `explicit.stat_3917489142@T1` | -0.16154 |
| `explicit.stat_2974417149@T1` | 0.14892 |
| `implicit.stat_958696139` | -0.09733 |
| `implicit.stat_1416292992` | -0.06489 |
| `explicit.stat_789117908@T1` | -0.06164 |
| `implicit.stat_3879011313` | 0.05957 |
| `explicit.stat_736967255@T1` | -0.04060 |

### accessory.amulet — n=64203, R²=-2.0854

intercept: `3.2066`  ·  log_price: True  ·  ilvl: `-0.04147`  ·  n_mods: `-0.00929`  ·  n_top_tier: `1.00598`  ·  corrupted: `0.03287`  ·  n_sockets: `-0.02842`  ·  quality: `0.00902`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T2` | -1.53503 |
| `explicit.stat_3299347043@T1` | -1.52217 |
| `explicit.stat_2901986750@T1` | -1.16215 |
| `explicit.stat_1202301673@T2` | -1.13100 |
| `explicit.stat_2866361420@T1` | -1.12517 |
| `explicit.stat_2866361420@T2` | -1.10266 |
| `explicit.stat_2974417149@T1` | -1.09219 |
| `explicit.stat_803737631@T1` | -1.08064 |
| `explicit.stat_4080418644@T1` | -1.07831 |
| `explicit.stat_2974417149@T2` | -1.07309 |
| `explicit.stat_1050105434@T2` | -1.05509 |
| `explicit.stat_803737631@T2` | -1.05396 |

### accessory.belt — n=45541, R²=-2.0502

intercept: `1.5146`  ·  log_price: True  ·  ilvl: `-0.01828`  ·  n_mods: `-0.00780`  ·  n_top_tier: `0.78565`  ·  corrupted: `0.77632`  ·  n_sockets: `1.56153`

| stat_id | coef |
|---|---|
| `explicit.stat_51994685@T1` | -0.79737 |
| `explicit.stat_2881298780@T1` | -0.79513 |
| `explicit.stat_3299347043@T2` | -0.79493 |
| `explicit.stat_809229260@T2` | -0.79415 |
| `explicit.stat_915769802@T1` | -0.79380 |
| `explicit.stat_3325883026@T1` | -0.79144 |
| `explicit.stat_3372524247@T2` | -0.79050 |
| `explicit.stat_1570770415@T2` | -0.79027 |
| `explicit.stat_2881298780@T2` | -0.78794 |
| `explicit.stat_3299347043@T1` | -0.78757 |
| `explicit.stat_915769802@T2` | -0.78701 |
| `explicit.stat_4220027924@T2` | -0.78639 |

### armour.chest — n=45181, R²=-1.7704

intercept: `3.4254`  ·  log_price: True  ·  ilvl: `-0.04213`  ·  n_mods: `-0.01632`  ·  n_top_tier: `0.39066`  ·  corrupted: `0.25594`  ·  n_sockets: `0.02570`  ·  quality: `0.07747`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.23536 |
| `explicit.stat_986397080@T2` | -0.45507 |
| `explicit.stat_986397080@T1` | -0.44216 |
| `explicit.stat_4080418644@T2` | -0.42935 |
| `explicit.stat_3484657501@T1` | -0.42476 |
| `explicit.stat_1692879867@T2` | -0.42338 |
| `explicit.stat_915769802@T2` | -0.41653 |
| `explicit.stat_2451402625@T2` | -0.41511 |
| `explicit.stat_2339757871@T2` | -0.40923 |
| `explicit.stat_915769802@T1` | -0.40817 |
| `explicit.stat_1999113824@T2` | -0.40606 |
| `explicit.stat_1062208444@T2` | -0.40405 |

### armour.helmet — n=43947, R²=-1.7755

intercept: `3.2528`  ·  log_price: True  ·  ilvl: `-0.04066`  ·  n_mods: `-0.02044`  ·  n_top_tier: `0.49670`  ·  corrupted: `0.48066`  ·  n_sockets: `0.05678`  ·  quality: `0.07819`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.52604 |
| `crafted.stat_3917489142@T1` | 2.60520 |
| `explicit.stat_1263695895@T1` | -0.72859 |
| `explicit.stat_2162097452@T2` | -0.67428 |
| `explicit.stat_3917489142@T2` | -0.65270 |
| `explicit.stat_3917489142@T1` | -0.59269 |
| `explicit.stat_4052037485@T2` | -0.56196 |
| `explicit.stat_1263695895@T2` | -0.55269 |
| `explicit.stat_4015621042@T2` | -0.54787 |
| `explicit.stat_1999113824@T1` | -0.53146 |
| `explicit.stat_3321629045@T2` | -0.52822 |
| `explicit.stat_803737631@T2` | -0.52030 |

### armour.boots — n=40679, R²=-1.7532

intercept: `3.4546`  ·  log_price: True  ·  ilvl: `-0.04265`  ·  n_mods: `-0.02197`  ·  n_top_tier: `0.37675`  ·  corrupted: `0.03402`  ·  n_sockets: `0.04515`  ·  quality: `0.07308`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.03037 |
| `explicit.stat_2250533757@T1` | 1.79876 |
| `crafted.stat_3917489142@T1` | 1.55078 |
| `explicit.stat_2923486259@T1` | 0.98118 |
| `explicit.stat_3299347043@T1` | -0.48625 |
| `explicit.stat_2923486259@T2` | -0.45486 |
| `explicit.stat_1671376347@T2` | -0.42558 |
| `explicit.stat_3917489142@T2` | -0.42556 |
| `explicit.stat_2160282525@T1` | -0.42296 |
| `explicit.stat_328541901@T2` | -0.41886 |
| `explicit.stat_1874553720@T1` | -0.41514 |
| `explicit.stat_99927264@T1` | -0.41016 |

### armour.gloves — n=39681, R²=-1.8066

intercept: `3.7914`  ·  log_price: True  ·  ilvl: `-0.04923`  ·  n_mods: `-0.00693`  ·  n_top_tier: `0.66963`  ·  corrupted: `-0.03652`  ·  n_sockets: `0.13100`  ·  quality: `0.05731`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -0.95600 |
| `explicit.stat_4052037485@T1` | -0.91481 |
| `explicit.stat_3484657501@T2` | -0.86178 |
| `explicit.stat_4052037485@T2` | -0.83962 |
| `explicit.stat_2923486259@T2` | -0.83004 |
| `explicit.stat_9187492@T2` | -0.82989 |
| `explicit.stat_4015621042@T2` | -0.81852 |
| `explicit.stat_3321629045@T2` | -0.80359 |
| `explicit.stat_3484657501@T1` | -0.77366 |
| `explicit.stat_124859000@T1` | -0.73712 |
| `explicit.stat_3917489142@T2` | -0.72927 |
| `explicit.stat_4080418644@T2` | -0.72753 |

### weapon.wand — n=23302, R²=-1.9117

intercept: `4.1588`  ·  log_price: True  ·  ilvl: `-0.05140`  ·  n_mods: `-0.07129`  ·  n_top_tier: `0.59787`  ·  corrupted: `0.00518`  ·  n_sockets: `0.01571`  ·  quality: `0.04210`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.09338 |
| `explicit.stat_1545858329@T1` | 2.84338 |
| `explicit.stat_2254480358@T1` | 2.57678 |
| `explicit.stat_124131830@T1` | 2.14629 |
| `explicit.stat_591105508@T1` | 2.07315 |
| `explicit.stat_4226189338@T1` | 1.90404 |
| `explicit.stat_1600707273@T1` | 1.26567 |
| `explicit.stat_2254480358@T2` | 1.22017 |
| `crafted.stat_124131830` | 1.14787 |
| `explicit.stat_1263695895@T2` | -1.11152 |
| `explicit.stat_1263695895@T1` | -1.10224 |
| `explicit.stat_473429811@T2` | -0.82217 |

### flask.charm — n=20431, R²=-0.6645

intercept: `0.1043`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.60914`  ·  corrupted: `1.55445`  ·  quality: `0.00955`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60508 |
| `explicit.stat_1056492907` | 2.54583 |
| `explicit.stat_3246948616` | 2.06524 |
| `explicit.stat_1120862500@T2` | -1.60917 |
| `explicit.stat_828533480@T2` | -1.60917 |
| `explicit.stat_1873752457@T2` | -1.60914 |
| `explicit.stat_2541588185@T2` | -1.60913 |
| `explicit.stat_388617051@T2` | -1.60912 |
| `explicit.stat_2365392475@T2` | -1.60906 |
| `explicit.stat_3196823591@T2` | -1.60900 |
| `explicit.stat_2676834156@T2` | -1.60854 |
| `explicit.stat_828533480@T1` | -1.60384 |

### weapon.bow — n=18631, R²=-1.8476

intercept: `3.9792`  ·  log_price: True  ·  ilvl: `-0.04724`  ·  n_mods: `-0.08892`  ·  n_top_tier: `0.76931`  ·  corrupted: `0.62796`  ·  n_sockets: `0.04348`  ·  quality: `0.03413`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 4.64359 |
| `desecrated.stat_210067635@T1` | -2.03526 |
| `explicit.stat_1263695895@T1` | -1.30993 |
| `explicit.stat_1263695895@T2` | -1.22712 |
| `crafted.stat_3035140377` | 1.19764 |
| `explicit.stat_1509134228@T1` | -0.98564 |
| `explicit.stat_2463230181@T2` | -0.94601 |
| `explicit.stat_709508406@T1` | 0.90874 |
| `explicit.stat_210067635@T2` | -0.90259 |
| `explicit.stat_1368271171@T1` | -0.89646 |
| `explicit.stat_1368271171@T2` | -0.87587 |
| `explicit.stat_3695891184@T1` | -0.87574 |

### weapon.crossbow — n=17443, R²=-1.6368

intercept: `4.0977`  ·  log_price: True  ·  ilvl: `-0.04821`  ·  n_mods: `-0.11361`  ·  n_top_tier: `0.43292`  ·  corrupted: `-0.02808`  ·  n_sockets: `0.10338`  ·  quality: `0.01896`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.88652 |
| `explicit.stat_2250681686@T2` | -1.43929 |
| `explicit.stat_1980802737` | 1.40360 |
| `explicit.stat_1202301673@T1` | 1.17735 |
| `explicit.stat_2250681686` | 1.06497 |
| `explicit.stat_1509134228@T1` | 0.99991 |
| `explicit.stat_709508406@T1` | 0.87338 |
| `crafted.stat_3035140377` | 0.84494 |
| `explicit.stat_3695891184@T1` | -0.80162 |
| `explicit.stat_3695891184@T2` | -0.75778 |
| `explicit.stat_3336890334@T2` | -0.67217 |
| `explicit.stat_210067635@T2` | -0.67026 |

### weapon.warstaff — n=12290, R²=-0.3244

intercept: `-10.9590`  ·  log_price: True  ·  ilvl: `0.14938`  ·  n_mods: `-0.23389`  ·  n_top_tier: `0.50426`  ·  corrupted: `0.25332`  ·  n_sockets: `0.12155`  ·  quality: `0.05247`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 1.19862 |
| `desecrated.stat_2527686725@T1` | 1.19862 |
| `explicit.stat_328541901@T2` | -1.04978 |
| `explicit.stat_821021828@T2` | -1.00970 |
| `crafted.stat_210067635@T2` | 0.95252 |
| `explicit.stat_1037193709@T2` | -0.89837 |
| `explicit.stat_328541901@T1` | -0.84791 |
| `desecrated.stat_9187492` | 0.82135 |
| `rune.stat_243313994` | 0.74560 |
| `explicit.stat_821021828@T1` | -0.70523 |
| `explicit.stat_1940865751@T2` | -0.70487 |
| `explicit.stat_691932474@T2` | -0.59403 |

### weapon.staff — n=11725, R²=-0.3584

intercept: `-16.2401`  ·  log_price: True  ·  ilvl: `0.20863`  ·  n_mods: `-0.11192`  ·  n_top_tier: `0.50120`  ·  corrupted: `0.92702`  ·  n_sockets: `0.20139`  ·  quality: `0.04276`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.93796 |
| `explicit.stat_591105508@T1` | 1.81725 |
| `explicit.stat_4226189338@T1` | 1.61998 |
| `explicit.stat_1600707273@T1` | 1.46389 |
| `explicit.stat_1545858329@T1` | 1.02981 |
| `explicit.stat_3962278098@T2` | 0.95894 |
| `explicit.stat_473429811@T2` | -0.95677 |
| `explicit.stat_293638271@T2` | -0.89273 |
| `explicit.stat_2254480358@T1` | 0.85373 |
| `explicit.stat_591105508@T2` | 0.78461 |
| `explicit.stat_124131830@T2` | 0.58711 |
| `explicit.stat_3015669065@T2` | -0.55168 |

### weapon.sceptre — n=11397, R²=-0.3325

intercept: `-21.4560`  ·  log_price: True  ·  ilvl: `0.27298`  ·  n_mods: `-0.01881`  ·  n_top_tier: `0.02518`  ·  corrupted: `0.13102`  ·  n_sockets: `0.21100`  ·  quality: `0.03691`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.81582 |
| `explicit.stat_2162097452@T2` | 1.51026 |
| `explicit.stat_3057012405@T1` | 1.27871 |
| `explicit.stat_1798257884@T2` | 1.22111 |
| `explicit.stat_101878827@T2` | 0.97897 |
| `explicit.stat_101878827@T1` | 0.97270 |
| `explicit.stat_1263695895@T1` | -0.62471 |
| `explicit.stat_4080418644@T2` | -0.59210 |
| `explicit.stat_2347036682@T1` | 0.56491 |
| `explicit.stat_1250712710@T2` | 0.52802 |
| `explicit.stat_1263695895@T2` | -0.52770 |
| `explicit.stat_1998951374@T1` | 0.52137 |

### weapon.spear — n=9261, R²=-0.3805

intercept: `-13.6107`  ·  log_price: True  ·  ilvl: `0.18839`  ·  n_mods: `-0.18610`  ·  n_top_tier: `0.59942`  ·  corrupted: `-0.56402`  ·  n_sockets: `0.23676`  ·  quality: `0.07160`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -4.72313 |
| `crafted.stat_210067635@T2` | -3.35781 |
| `explicit.stat_9187492@T1` | 1.16077 |
| `explicit.stat_748522257@T2` | -1.02500 |
| `explicit.stat_4080418644@T2` | -0.97999 |
| `crafted.stat_3035140377` | 0.95079 |
| `explicit.stat_1940865751@T2` | -0.89623 |
| `explicit.stat_3336890334@T2` | -0.87917 |
| `explicit.stat_9187492@T2` | -0.87438 |
| `explicit.stat_1037193709@T1` | -0.86872 |
| `explicit.stat_4080418644@T1` | -0.86035 |
| `explicit.stat_3261801346@T1` | -0.77092 |

### armour.focus — n=7585, R²=-0.3323

intercept: `-16.2596`  ·  log_price: True  ·  ilvl: `0.20756`  ·  n_mods: `-0.15334`  ·  n_top_tier: `0.96665`  ·  corrupted: `-0.10092`  ·  n_sockets: `0.41051`  ·  quality: `0.02866`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | 2.27490 |
| `crafted.stat_2974417149@T1` | 2.17553 |
| `explicit.stat_4220027924@T1` | -1.48557 |
| `explicit.stat_2923486259@T1` | -1.47521 |
| `explicit.stat_2339757871@T2` | -1.23512 |
| `explicit.stat_2923486259@T2` | -1.20876 |
| `explicit.stat_2768835289@T1` | -1.18468 |
| `explicit.stat_4220027924@T2` | -1.18433 |
| `explicit.stat_3962278098@T2` | -1.13147 |
| `explicit.stat_4015621042@T1` | -1.08788 |
| `explicit.stat_1050105434@T2` | -1.02146 |
| `explicit.stat_274716455@T1` | -1.00276 |

### armour.quiver — n=7063, R²=-0.2748

intercept: `-18.3802`  ·  log_price: True  ·  ilvl: `0.22258`  ·  n_mods: `-0.08794`  ·  n_top_tier: `0.72338`  ·  corrupted: `1.02039`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.22560 |
| `explicit.stat_681332047@T2` | -1.45051 |
| `explicit.stat_681332047@T1` | -1.19740 |
| `explicit.stat_1573130764@T2` | -0.99603 |
| `explicit.stat_2321178454@T2` | -0.87897 |
| `explicit.stat_2194114101@T2` | -0.76960 |
| `explicit.stat_1573130764@T1` | -0.75938 |
| `explicit.stat_4067062424@T1` | -0.69344 |
| `explicit.stat_3714003708@T2` | -0.65193 |
| `explicit.stat_3261801346@T1` | -0.61592 |
| `explicit.stat_803737631@T1` | -0.61365 |
| `explicit.stat_803737631@T2` | -0.60772 |

### armour.shield — n=6062, R²=-0.4153

intercept: `-13.4519`  ·  log_price: True  ·  ilvl: `0.18188`  ·  n_mods: `-0.19587`  ·  n_top_tier: `0.64069`  ·  corrupted: `-0.38471`  ·  n_sockets: `0.38805`  ·  quality: `0.04885`

| stat_id | coef |
|---|---|
| `explicit.stat_1011760251@T1` | -2.12590 |
| `explicit.stat_3855016469@T1` | -1.34954 |
| `explicit.stat_4095671657@T2` | -1.26657 |
| `explicit.stat_4095671657@T1` | -1.19007 |
| `explicit.stat_2901986750@T1` | -1.18302 |
| `explicit.stat_1011760251@T2` | -1.17386 |
| `explicit.stat_3321629045@T2` | -1.10786 |
| `explicit.stat_2481353198@T1` | -1.03856 |
| `explicit.stat_3033371881@T2` | -1.00807 |
| `explicit.stat_4052037485@T1` | -1.00619 |
| `explicit.stat_2923486259@T1` | -0.97691 |
| `explicit.stat_328541901@T1` | -0.94128 |

### weapon.twomace — n=5532, R²=-0.4307

intercept: `-11.0848`  ·  log_price: True  ·  ilvl: `0.15356`  ·  n_mods: `-0.24945`  ·  n_top_tier: `0.49994`  ·  corrupted: `0.48948`  ·  n_sockets: `0.19622`  ·  quality: `0.05590`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.82914 |
| `explicit.stat_3336890334@T1` | -1.67180 |
| `explicit.stat_1037193709@T1` | -1.60172 |
| `explicit.stat_1263695895@T2` | -1.27088 |
| `explicit.stat_9187492@T1` | -1.06787 |
| `explicit.stat_2694482655@T1` | 0.95439 |
| `explicit.stat_3695891184@T2` | -0.76693 |
| `explicit.stat_3695891184@T1` | -0.75906 |
| `explicit.stat_1263695895@T1` | -0.75820 |
| `explicit.stat_210067635@T1` | -0.60668 |
| `explicit.stat_518292764@T2` | -0.60028 |
| `explicit.stat_691932474@T1` | -0.59107 |

## Coverage (listings per base)

- … **Sapphire** — 38170 listings (38105 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 37196 listings (37144 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 28432 listings (28400 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 13010 listings (12992 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11994 listings (11968 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 11678 listings (11652 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 11537 listings (11525 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10796 listings (10769 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10763 listings (10740 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 10219 listings (10206 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8945 listings (8930 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8583 listings (8574 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8512 listings (8503 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7525 listings (7501 priced) [0.3–4297682211.9 ex]
- … **Unset Ring** — 7397 listings (7377 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7363 listings (7355 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 7306 listings (7291 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 7209 listings (7201 priced) [0.3–3985176410.3 ex]
- … **Pearl Ring** — 7149 listings (7140 priced) [0.2–275252424.7 ex]
- … **Plate Belt** — 7104 listings (7073 priced) [0.3–398912568423.8 ex]
- … **Ancestral Tiara** — 7046 listings (7017 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6987 listings (6977 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6691 listings (6687 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6587 listings (6572 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6287 listings (6273 priced) [0.3–398912568423.8 ex]

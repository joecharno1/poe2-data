# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-22T01:49:59+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **725936** (723593 priced in exalted)
- Distinct bases: 1001 · distinct mods: 3327 · mod rows: 3431061
- Sold signals: **24101** sold · 413932 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-22T01:38:04+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.84** (median |log error| 3.1284)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×66.61 · ±30% 4% · n=105468
- Premium segment (60ex+): skill **+0.13** · typical error ×347.16 · ±30% 0% · n=70026

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 15620 | ×50.24 | 21% | +0.04 | +0.07 |
| jewel | 15107 | ×54.88 | 21% | +0.02 | +0.03 |
| accessory.amulet | 13992 | ×26.50 | 17% | +0.04 | +0.04 |
| accessory.belt | 9868 | ×21.42 | 20% | +0.04 | +0.06 |
| armour.chest | 9620 | ×16.71 | 22% | +0.08 | +0.11 |
| armour.helmet | 9385 | ×24.67 | 17% | +0.09 | +0.11 |
| armour.boots | 8602 | ×21.39 | 18% | +0.11 | +0.13 |
| armour.gloves | 8493 | ×31.86 | 13% | +0.08 | +0.11 |
| other | 8492 | ×1.84 | 43% | +0.11 | +0.18 |
| weapon.wand | 5002 | ×36.13 | 13% | +0.12 | +0.12 |
| weapon.bow | 3937 | ×24.77 | 13% | +0.16 | +0.16 |
| weapon.crossbow | 3693 | ×22.08 | 15% | +0.12 | +0.15 |
| weapon.warstaff | 2561 | ×14.67 | 7% | +0.16 | +0.16 |
| weapon.staff | 2444 | ×16.97 | 6% | +0.12 | +0.13 |
| weapon.sceptre | 2412 | ×18.10 | 5% | +0.06 | +0.06 |
| weapon.spear | 1935 | ×12.96 | 7% | +0.11 | +0.14 |
| armour.focus | 1614 | ×13.34 | 7% | +0.09 | +0.10 |
| armour.quiver | 1506 | ×16.73 | 7% | +0.12 | +0.13 |
| flask.charm | 1241 | ×10.00 | 28% | +0.02 | +0.03 |
| armour.shield | 1237 | ×8.80 | 8% | +0.10 | +0.12 |
| weapon.twomace | 1124 | ×9.27 | 7% | +0.10 | +0.12 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=82554, R²=-1.8941

intercept: `-0.0734`  ·  log_price: True  ·  ilvl: `0.00090`  ·  n_mods: `1.01875`  ·  n_top_tier: `-0.94727`  ·  corrupted: `1.28115`  ·  quality: `-0.06509`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 4.20771 |
| `explicit.stat_1604736568@T1` | -2.28107 |
| `explicit.stat_1604736568` | 2.21066 |
| `explicit.stat_3714003708@T1` | 1.17839 |
| `explicit.stat_3556824919@T1` | 1.05406 |
| `explicit.stat_2194114101@T1` | -0.92480 |
| `explicit.stat_681332047@T1` | -0.72176 |
| `explicit.stat_274716455@T1` | -0.50716 |
| `explicit.stat_3473929743@T1` | -0.36126 |
| `explicit.stat_4045894391@T1` | -0.36057 |
| `explicit.stat_681332047` | 0.32501 |
| `explicit.stat_737908626@T1` | -0.29373 |

### accessory.ring — n=71243, R²=-2.0084

intercept: `3.3092`  ·  log_price: True  ·  ilvl: `-0.04123`  ·  n_mods: `0.00076`  ·  n_top_tier: `1.05541`  ·  corrupted: `0.00639`  ·  n_sockets: `2.19539`  ·  quality: `0.02120`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.08912 |
| `explicit.stat_1263695895@T2` | -1.08213 |
| `explicit.stat_3032590688@T1` | -1.07246 |
| `explicit.stat_3325883026@T1` | -1.07168 |
| `explicit.stat_4080418644@T1` | -1.07096 |
| `explicit.stat_2891184298@T2` | -1.07087 |
| `explicit.stat_803737631@T1` | -1.06877 |
| `explicit.stat_2923486259@T2` | -1.06871 |
| `explicit.stat_3695891184@T1` | -1.06788 |
| `explicit.stat_1671376347@T2` | -1.06710 |
| `explicit.stat_3962278098@T1` | -1.06638 |
| `explicit.stat_1754445556@T1` | -1.06572 |

### other — n=69040, R²=-0.6707

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.06671`  ·  n_top_tier: `0.27987`  ·  corrupted: `0.01599`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.38605 |
| `explicit.stat_3299347043@T1` | -0.24536 |
| `implicit.stat_2219129443` | 0.22333 |
| `implicit.stat_718638445` | 0.20015 |
| `implicit.stat_3182714256` | 0.20014 |
| `explicit.stat_3917489142@T1` | -0.16226 |
| `explicit.stat_2974417149@T1` | 0.12068 |
| `explicit.stat_789117908@T1` | -0.06835 |
| `implicit.stat_958696139` | -0.06669 |
| `implicit.stat_3879011313` | 0.06048 |
| `explicit.stat_736967255@T1` | -0.04576 |
| `implicit.stat_1416292992` | -0.04447 |

### accessory.amulet — n=63858, R²=-2.0931

intercept: `3.1233`  ·  log_price: True  ·  ilvl: `-0.04050`  ·  n_mods: `-0.00658`  ·  n_top_tier: `1.02582`  ·  corrupted: `0.06043`  ·  n_sockets: `-0.02570`  ·  quality: `0.01812`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.69861 |
| `explicit.stat_3299347043@T2` | -1.62033 |
| `explicit.stat_2901986750@T1` | -1.16148 |
| `explicit.stat_2866361420@T1` | -1.12591 |
| `explicit.stat_1202301673@T2` | -1.12556 |
| `explicit.stat_2866361420@T2` | -1.11705 |
| `explicit.stat_803737631@T1` | -1.11136 |
| `explicit.stat_124131830@T2` | -1.10758 |
| `explicit.stat_2974417149@T1` | -1.10717 |
| `explicit.stat_4080418644@T1` | -1.08911 |
| `explicit.stat_2974417149@T2` | -1.07661 |
| `explicit.stat_1050105434@T2` | -1.07525 |

### accessory.belt — n=45364, R²=-1.8373

intercept: `3.6750`  ·  log_price: True  ·  ilvl: `-0.04423`  ·  n_mods: `-0.02232`  ·  n_top_tier: `0.72892`  ·  corrupted: `1.12978`  ·  n_sockets: `1.44760`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 0.86351 |
| `explicit.stat_2881298780@T1` | -0.76762 |
| `explicit.stat_51994685@T1` | -0.76427 |
| `explicit.stat_809229260@T2` | -0.75588 |
| `explicit.stat_3299347043@T2` | -0.74996 |
| `explicit.stat_915769802@T1` | -0.74445 |
| `explicit.stat_1570770415@T2` | -0.74413 |
| `explicit.stat_2881298780@T2` | -0.74336 |
| `explicit.stat_3325883026@T1` | -0.74294 |
| `explicit.stat_3372524247@T2` | -0.73812 |
| `explicit.stat_1836676211@T2` | -0.73397 |
| `explicit.stat_915769802@T2` | -0.73181 |

### armour.chest — n=45011, R²=-1.7945

intercept: `3.3055`  ·  log_price: True  ·  ilvl: `-0.04067`  ·  n_mods: `-0.01462`  ·  n_top_tier: `0.36125`  ·  corrupted: `0.31749`  ·  n_sockets: `0.02139`  ·  quality: `0.07401`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.96282 |
| `explicit.stat_986397080@T2` | -0.41571 |
| `explicit.stat_986397080@T1` | -0.40621 |
| `explicit.stat_1692879867@T2` | -0.38954 |
| `explicit.stat_4080418644@T2` | -0.38824 |
| `explicit.stat_3484657501@T1` | -0.38456 |
| `explicit.stat_915769802@T2` | -0.38415 |
| `explicit.stat_1062208444@T2` | -0.37899 |
| `explicit.stat_2339757871@T2` | -0.37823 |
| `explicit.stat_915769802@T1` | -0.37636 |
| `explicit.stat_2451402625@T2` | -0.37442 |
| `explicit.stat_1999113824@T2` | -0.37201 |

### armour.helmet — n=43805, R²=-1.7341

intercept: `3.2584`  ·  log_price: True  ·  ilvl: `-0.04073`  ·  n_mods: `-0.02491`  ·  n_top_tier: `0.55288`  ·  corrupted: `0.60090`  ·  n_sockets: `0.07723`  ·  quality: `0.06941`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.92582 |
| `crafted.stat_3917489142@T1` | 1.31460 |
| `explicit.stat_1263695895@T1` | -0.83777 |
| `explicit.stat_3917489142@T2` | -0.71961 |
| `explicit.stat_2162097452@T2` | -0.71138 |
| `explicit.stat_3917489142@T1` | -0.65524 |
| `explicit.stat_1263695895@T2` | -0.64582 |
| `explicit.stat_4052037485@T2` | -0.63780 |
| `explicit.stat_4015621042@T2` | -0.63266 |
| `explicit.stat_1999113824@T1` | -0.60587 |
| `explicit.stat_587431675@T2` | -0.59186 |
| `explicit.stat_3321629045@T2` | -0.59012 |

### armour.boots — n=40527, R²=-1.7033

intercept: `3.6047`  ·  log_price: True  ·  ilvl: `-0.04432`  ·  n_mods: `-0.02707`  ·  n_top_tier: `0.38168`  ·  corrupted: `0.07769`  ·  n_sockets: `0.05483`  ·  quality: `0.07119`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.22957 |
| `explicit.stat_2250533757@T1` | 1.78065 |
| `crafted.stat_3917489142@T1` | 1.48031 |
| `explicit.stat_2923486259@T1` | 0.98923 |
| `explicit.stat_3299347043@T1` | -0.52289 |
| `explicit.stat_2923486259@T2` | -0.47844 |
| `explicit.stat_328541901@T2` | -0.45018 |
| `explicit.stat_1874553720@T1` | -0.43981 |
| `explicit.stat_1671376347@T2` | -0.43911 |
| `explicit.stat_2160282525@T1` | -0.43875 |
| `explicit.stat_3917489142@T2` | -0.43608 |
| `explicit.stat_1999113824@T2` | -0.42037 |

### armour.gloves — n=39531, R²=-1.6607

intercept: `3.8230`  ·  log_price: True  ·  ilvl: `-0.04963`  ·  n_mods: `-0.01615`  ·  n_top_tier: `0.69984`  ·  corrupted: `-0.05345`  ·  n_sockets: `0.18514`  ·  quality: `0.05925`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.19998 |
| `explicit.stat_2923486259@T2` | -1.01883 |
| `explicit.stat_4052037485@T1` | -0.98735 |
| `explicit.stat_3484657501@T2` | -0.97091 |
| `explicit.stat_3321629045@T2` | -0.91869 |
| `explicit.stat_4052037485@T2` | -0.89082 |
| `explicit.stat_3484657501@T1` | -0.85100 |
| `explicit.stat_4015621042@T2` | -0.84453 |
| `explicit.stat_124859000@T1` | -0.84406 |
| `explicit.stat_9187492@T2` | -0.83567 |
| `rune.stat_201332984` | -0.81865 |
| `explicit.stat_803737631@T2` | -0.80389 |

### weapon.wand — n=23260, R²=-1.8741

intercept: `3.8870`  ·  log_price: True  ·  ilvl: `-0.04799`  ·  n_mods: `-0.08034`  ·  n_top_tier: `0.63114`  ·  corrupted: `0.07380`  ·  n_sockets: `0.01813`  ·  quality: `0.03983`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.36369 |
| `explicit.stat_1545858329@T1` | 2.58384 |
| `explicit.stat_2254480358@T1` | 2.45525 |
| `explicit.stat_124131830@T1` | 2.06750 |
| `explicit.stat_591105508@T1` | 1.86962 |
| `explicit.stat_4226189338@T1` | 1.34937 |
| `explicit.stat_2254480358@T2` | 1.19551 |
| `explicit.stat_1263695895@T2` | -1.17206 |
| `explicit.stat_1263695895@T1` | -1.14207 |
| `crafted.stat_124131830` | 1.10528 |
| `explicit.stat_1600707273@T1` | 1.04979 |
| `explicit.stat_473429811@T2` | -0.88833 |

### flask.charm — n=20347, R²=-0.6642

intercept: `0.1066`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.60924`  ·  corrupted: `1.54373`  ·  quality: `0.01163`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60506 |
| `explicit.stat_1056492907` | 2.52702 |
| `explicit.stat_3246948616` | 2.01120 |
| `explicit.stat_828533480@T2` | -1.60927 |
| `explicit.stat_1120862500@T2` | -1.60926 |
| `explicit.stat_1873752457@T2` | -1.60924 |
| `explicit.stat_2541588185@T2` | -1.60923 |
| `explicit.stat_388617051@T2` | -1.60922 |
| `explicit.stat_3196823591@T2` | -1.60918 |
| `explicit.stat_2365392475@T2` | -1.60916 |
| `explicit.stat_2676834156@T2` | -1.60831 |
| `explicit.stat_828533480@T1` | -1.60674 |

### weapon.bow — n=18592, R²=-1.8515

intercept: `3.8967`  ·  log_price: True  ·  ilvl: `-0.04587`  ·  n_mods: `-0.09428`  ·  n_top_tier: `0.77831`  ·  corrupted: `0.62668`  ·  n_sockets: `0.04128`  ·  quality: `0.02940`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 4.80640 |
| `desecrated.stat_210067635@T1` | -1.97873 |
| `explicit.stat_1263695895@T1` | -1.27812 |
| `crafted.stat_3035140377` | 1.24504 |
| `explicit.stat_1263695895@T2` | -1.19259 |
| `explicit.stat_2463230181@T2` | -1.01994 |
| `explicit.stat_1509134228@T1` | -0.99203 |
| `explicit.stat_210067635@T2` | -0.92062 |
| `explicit.stat_3695891184@T1` | -0.89485 |
| `explicit.stat_709508406@T1` | 0.89013 |
| `explicit.stat_1368271171@T2` | -0.88023 |
| `explicit.stat_3695891184@T2` | -0.87558 |

### weapon.crossbow — n=17402, R²=-1.7686

intercept: `4.0273`  ·  log_price: True  ·  ilvl: `-0.04818`  ·  n_mods: `-0.07906`  ·  n_top_tier: `0.34325`  ·  corrupted: `-0.01675`  ·  n_sockets: `0.06010`  ·  quality: `0.01888`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.85034 |
| `explicit.stat_1202301673@T1` | 1.47580 |
| `explicit.stat_1980802737` | 1.42161 |
| `explicit.stat_2250681686@T2` | -1.37165 |
| `explicit.stat_1509134228@T1` | 1.27200 |
| `explicit.stat_2250681686` | 1.10078 |
| `explicit.stat_709508406@T1` | 0.90588 |
| `crafted.stat_3035140377` | 0.88297 |
| `explicit.stat_1263695895@T2` | -0.57902 |
| `explicit.stat_3695891184@T1` | -0.57686 |
| `explicit.stat_3336890334@T2` | -0.52254 |
| `explicit.stat_3695891184@T2` | -0.51292 |

### weapon.warstaff — n=12258, R²=-0.3291

intercept: `-10.9331`  ·  log_price: True  ·  ilvl: `0.14873`  ·  n_mods: `-0.23708`  ·  n_top_tier: `0.53399`  ·  corrupted: `0.26076`  ·  n_sockets: `0.11454`  ·  quality: `0.05231`

| stat_id | coef |
|---|---|
| `explicit.stat_821021828@T2` | -1.04717 |
| `explicit.stat_328541901@T2` | -0.99010 |
| `explicit.stat_1037193709@T2` | -0.96526 |
| `crafted.stat_210067635@T2` | 0.94729 |
| `explicit.stat_328541901@T1` | -0.84777 |
| `desecrated.stat_9187492` | 0.80034 |
| `rune.stat_243313994` | 0.77554 |
| `explicit.stat_1940865751@T2` | -0.76142 |
| `explicit.stat_821021828@T1` | -0.75032 |
| `explicit.stat_9187492@T2` | -0.74033 |
| `desecrated.stat_2527686725@T1` | 0.73620 |
| `desecrated.stat_2231156303@T1` | 0.73620 |

### weapon.staff — n=11676, R²=-0.3521

intercept: `-16.5704`  ·  log_price: True  ·  ilvl: `0.21274`  ·  n_mods: `-0.08024`  ·  n_top_tier: `0.47034`  ·  corrupted: `0.81004`  ·  n_sockets: `0.21595`  ·  quality: `0.03386`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.09096 |
| `explicit.stat_591105508@T1` | 1.94587 |
| `explicit.stat_4226189338@T1` | 1.82154 |
| `explicit.stat_1600707273@T1` | 1.40885 |
| `explicit.stat_1545858329@T1` | 1.19960 |
| `explicit.stat_3962278098@T2` | 0.91953 |
| `explicit.stat_293638271@T2` | -0.90195 |
| `explicit.stat_473429811@T2` | -0.87243 |
| `explicit.stat_591105508@T2` | 0.81633 |
| `explicit.stat_2254480358@T1` | 0.69110 |
| `explicit.stat_124131830@T2` | 0.67860 |
| `explicit.stat_4226189338@T2` | 0.64051 |

### weapon.sceptre — n=11373, R²=-0.3306

intercept: `-21.6511`  ·  log_price: True  ·  ilvl: `0.27616`  ·  n_mods: `-0.01960`  ·  n_top_tier: `0.07598`  ·  corrupted: `0.13252`  ·  n_sockets: `0.17852`  ·  quality: `0.03595`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.78878 |
| `explicit.stat_2162097452@T2` | 1.49612 |
| `explicit.stat_3057012405@T1` | 1.26181 |
| `explicit.stat_1798257884@T2` | 1.10745 |
| `explicit.stat_101878827@T1` | 0.91447 |
| `explicit.stat_101878827@T2` | 0.91200 |
| `explicit.stat_1263695895@T1` | -0.80563 |
| `explicit.stat_1263695895@T2` | -0.74246 |
| `explicit.stat_2854751904@T2` | -0.61939 |
| `explicit.stat_4080418644@T2` | -0.60751 |
| `explicit.stat_1250712710@T2` | 0.53094 |
| `explicit.stat_1998951374@T1` | 0.50550 |

### weapon.spear — n=9242, R²=-0.3821

intercept: `-13.5245`  ·  log_price: True  ·  ilvl: `0.18714`  ·  n_mods: `-0.18524`  ·  n_top_tier: `0.56947`  ·  corrupted: `-0.52260`  ·  n_sockets: `0.22317`  ·  quality: `0.07429`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -3.90145 |
| `crafted.stat_210067635@T2` | -3.27705 |
| `explicit.stat_9187492@T1` | 1.12471 |
| `explicit.stat_748522257@T2` | -1.01970 |
| `explicit.stat_4080418644@T2` | -0.97284 |
| `crafted.stat_3035140377` | 0.91673 |
| `explicit.stat_1940865751@T2` | -0.91529 |
| `explicit.stat_9187492@T2` | -0.87988 |
| `explicit.stat_3336890334@T2` | -0.84925 |
| `explicit.stat_1037193709@T1` | -0.83746 |
| `explicit.stat_4080418644@T1` | -0.82957 |
| `desecrated.stat_210067635@T1` | -0.78198 |

### armour.focus — n=7560, R²=-0.3216

intercept: `-16.4396`  ·  log_price: True  ·  ilvl: `0.21047`  ·  n_mods: `-0.17280`  ·  n_top_tier: `1.02122`  ·  corrupted: `-0.07821`  ·  n_sockets: `0.38670`  ·  quality: `0.02792`

| stat_id | coef |
|---|---|
| `explicit.stat_4220027924@T1` | -1.62155 |
| `crafted.stat_2974417149@T1` | 1.54693 |
| `explicit.stat_2923486259@T1` | -1.47487 |
| `explicit.stat_4220027924@T2` | -1.24866 |
| `explicit.stat_2768835289@T1` | -1.20258 |
| `explicit.stat_2923486259@T2` | -1.16896 |
| `explicit.stat_2339757871@T2` | -1.15347 |
| `explicit.stat_4015621042@T1` | -1.12470 |
| `explicit.stat_3962278098@T2` | -1.12450 |
| `explicit.stat_1050105434@T2` | -1.08774 |
| `explicit.stat_3291658075@T2` | -1.08649 |
| `explicit.stat_274716455@T2` | -1.07494 |

### armour.quiver — n=7040, R²=-0.2768

intercept: `-18.5001`  ·  log_price: True  ·  ilvl: `0.22261`  ·  n_mods: `-0.07652`  ·  n_top_tier: `0.68322`  ·  corrupted: `1.02039`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.10612 |
| `explicit.stat_681332047@T2` | -1.38587 |
| `explicit.stat_681332047@T1` | -1.13901 |
| `explicit.stat_1573130764@T2` | -0.94313 |
| `explicit.stat_2321178454@T2` | -0.84904 |
| `explicit.stat_2194114101@T2` | -0.78339 |
| `explicit.stat_1573130764@T1` | -0.74850 |
| `explicit.stat_4067062424@T1` | -0.66802 |
| `explicit.stat_3714003708@T2` | -0.60258 |
| `explicit.stat_4067062424@T2` | -0.57285 |
| `explicit.stat_3261801346@T1` | -0.57157 |
| `explicit.stat_803737631@T1` | -0.56151 |

### armour.shield — n=6048, R²=-0.4092

intercept: `-13.2800`  ·  log_price: True  ·  ilvl: `0.17970`  ·  n_mods: `-0.19187`  ·  n_top_tier: `0.69387`  ·  corrupted: `-0.39361`  ·  n_sockets: `0.42551`  ·  quality: `0.04721`

| stat_id | coef |
|---|---|
| `explicit.stat_1011760251@T1` | -1.60142 |
| `explicit.stat_3855016469@T1` | -1.32727 |
| `explicit.stat_4095671657@T2` | -1.31016 |
| `explicit.stat_1011760251@T2` | -1.29534 |
| `explicit.stat_2901986750@T1` | -1.24985 |
| `explicit.stat_4095671657@T1` | -1.20937 |
| `explicit.stat_4052037485@T1` | -1.18812 |
| `explicit.stat_3321629045@T2` | -1.13961 |
| `explicit.stat_2481353198@T1` | -1.13433 |
| `explicit.stat_2923486259@T1` | -1.05570 |
| `explicit.stat_2481353198@T2` | -0.97618 |
| `explicit.stat_3033371881@T2` | -0.96615 |

### weapon.twomace — n=5524, R²=-0.4267

intercept: `-11.1437`  ·  log_price: True  ·  ilvl: `0.15568`  ·  n_mods: `-0.26706`  ·  n_top_tier: `0.47208`  ·  corrupted: `0.50563`  ·  n_sockets: `0.19451`  ·  quality: `0.05671`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.92209 |
| `explicit.stat_1037193709@T1` | -1.41881 |
| `explicit.stat_3336890334@T1` | -1.33581 |
| `explicit.stat_1263695895@T2` | -1.19344 |
| `explicit.stat_9187492@T1` | -1.08360 |
| `explicit.stat_2694482655@T1` | 0.98395 |
| `explicit.stat_3695891184@T2` | -0.74391 |
| `explicit.stat_3695891184@T1` | -0.73529 |
| `explicit.stat_1263695895@T1` | -0.69001 |
| `explicit.stat_55876295@T1` | -0.62182 |
| `explicit.stat_518292764@T2` | -0.59400 |
| `explicit.stat_691932474@T1` | -0.57756 |

## Coverage (listings per base)

- … **Sapphire** — 37916 listings (37851 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 36952 listings (36900 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 28247 listings (28215 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 12937 listings (12919 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11924 listings (11899 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 11600 listings (11574 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 11478 listings (11466 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10748 listings (10721 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10701 listings (10678 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 10161 listings (10148 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8904 listings (8889 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8531 listings (8522 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8463 listings (8454 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7511 listings (7487 priced) [0.3–4297682211.9 ex]
- … **Unset Ring** — 7353 listings (7333 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7331 listings (7324 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 7273 listings (7258 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 7179 listings (7171 priced) [0.3–3985176410.3 ex]
- … **Pearl Ring** — 7094 listings (7085 priced) [0.2–275252424.7 ex]
- … **Plate Belt** — 7072 listings (7041 priced) [0.3–398912568423.8 ex]
- … **Ancestral Tiara** — 7016 listings (6987 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6952 listings (6942 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6663 listings (6659 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6543 listings (6528 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6264 listings (6251 priced) [0.3–398912568423.8 ex]

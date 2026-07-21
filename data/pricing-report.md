# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-21T19:41:13+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **718666** (716379 priced in exalted)
- Distinct bases: 1001 · distinct mods: 3325 · mod rows: 3398830
- Sold signals: **24155** sold · 409193 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-21T19:27:30+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×18.80** (median |log error| 2.934)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.16** · typical error ×51.11 · ±30% 5% · n=104478
- Premium segment (60ex+): skill **+0.16** · typical error ×267.44 · ±30% 0% · n=69263

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 15469 | ×49.54 | 21% | +0.04 | +0.07 |
| jewel | 14888 | ×9.99 | 5% | +0.11 | +0.13 |
| accessory.amulet | 13833 | ×34.15 | 17% | +0.05 | +0.04 |
| accessory.belt | 9784 | ×22.37 | 13% | +0.08 | +0.10 |
| armour.chest | 9565 | ×15.28 | 20% | +0.09 | +0.11 |
| armour.helmet | 9289 | ×20.79 | 12% | +0.11 | +0.12 |
| armour.boots | 8613 | ×20.26 | 19% | +0.10 | +0.13 |
| armour.gloves | 8461 | ×30.17 | 13% | +0.09 | +0.11 |
| other | 8420 | ×2.00 | 42% | +0.11 | +0.16 |
| weapon.wand | 4972 | ×36.12 | 15% | +0.11 | +0.12 |
| weapon.bow | 3926 | ×22.07 | 12% | +0.16 | +0.17 |
| weapon.crossbow | 3692 | ×25.45 | 14% | +0.12 | +0.15 |
| weapon.warstaff | 2503 | ×14.01 | 7% | +0.16 | +0.16 |
| weapon.staff | 2452 | ×15.56 | 6% | +0.12 | +0.13 |
| weapon.sceptre | 2396 | ×19.79 | 5% | +0.06 | +0.07 |
| weapon.spear | 1926 | ×12.37 | 7% | +0.11 | +0.14 |
| armour.focus | 1604 | ×13.33 | 7% | +0.12 | +0.13 |
| armour.quiver | 1493 | ×15.66 | 7% | +0.12 | +0.13 |
| armour.shield | 1233 | ×8.48 | 8% | +0.10 | +0.11 |
| flask.charm | 1203 | ×10.00 | 27% | +0.02 | +0.04 |
| weapon.twomace | 1118 | ×9.17 | 7% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=81378, R²=-0.9728

intercept: `-1.9143`  ·  log_price: True  ·  ilvl: `0.02393`  ·  n_mods: `0.86361`  ·  n_top_tier: `-0.28793`  ·  corrupted: `0.36398`  ·  quality: `-0.04316`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -2.91626 |
| `explicit.stat_1869147066@T1` | -1.95252 |
| `explicit.stat_1594812856@T1` | 1.88043 |
| `explicit.stat_3668351662@T1` | -1.83149 |
| `explicit.stat_3485067555@T1` | 1.80859 |
| `explicit.stat_239367161@T1` | -1.66689 |
| `explicit.stat_627767961@T1` | -1.52024 |
| `explicit.stat_3028809864@T1` | -1.41242 |
| `explicit.stat_1697447343@T1` | -1.34853 |
| `explicit.stat_2456523742@T1` | 1.26630 |
| `explicit.stat_429143663@T1` | 1.22792 |
| `explicit.stat_234296660@T1` | -1.15421 |

### accessory.ring — n=70413, R²=-2.0038

intercept: `3.1406`  ·  log_price: True  ·  ilvl: `-0.03917`  ·  n_mods: `0.00055`  ·  n_top_tier: `1.07364`  ·  corrupted: `0.00706`  ·  n_sockets: `2.21027`  ·  quality: `0.02567`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.10672 |
| `explicit.stat_2891184298@T2` | -1.09296 |
| `explicit.stat_2231156303@T1` | -1.09053 |
| `explicit.stat_2923486259@T2` | -1.09024 |
| `explicit.stat_4080418644@T1` | -1.08955 |
| `explicit.stat_4220027924@T2` | -1.08821 |
| `explicit.stat_803737631@T1` | -1.08676 |
| `explicit.stat_1263695895@T2` | -1.08660 |
| `explicit.stat_2891184298@T1` | -1.08565 |
| `explicit.stat_3962278098@T1` | -1.08378 |
| `explicit.stat_3032590688@T1` | -1.08357 |
| `explicit.stat_3962278098@T2` | -1.08323 |

### other — n=68334, R²=-0.6941

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.02624`  ·  n_top_tier: `0.32034`  ·  corrupted: `0.05181`  ·  n_sockets: `-0.00005`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.41890 |
| `explicit.stat_3299347043@T1` | -0.23810 |
| `explicit.stat_3917489142@T1` | -0.18568 |
| `explicit.stat_2974417149@T1` | 0.10479 |
| `implicit.stat_3182714256` | 0.07875 |
| `implicit.stat_718638445` | 0.07875 |
| `explicit.stat_789117908@T1` | -0.07530 |
| `implicit.stat_2219129443` | 0.05432 |
| `explicit.stat_736967255@T1` | -0.05234 |
| `explicit.stat_2106365538@T1` | -0.04548 |
| `implicit.stat_2901986750` | -0.03589 |
| `implicit.stat_3879011313` | 0.03203 |

### accessory.amulet — n=63138, R²=-2.1375

intercept: `3.2615`  ·  log_price: True  ·  ilvl: `-0.04163`  ·  n_mods: `-0.01323`  ·  n_top_tier: `1.20783`  ·  corrupted: `0.09985`  ·  n_sockets: `-0.00556`  ·  quality: `0.03245`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.82153 |
| `explicit.stat_3299347043@T2` | -1.72862 |
| `explicit.stat_124131830@T2` | -1.36816 |
| `explicit.stat_2866361420@T2` | -1.28868 |
| `explicit.stat_2866361420@T1` | -1.28351 |
| `explicit.stat_587431675@T2` | -1.28276 |
| `explicit.stat_803737631@T1` | -1.27935 |
| `explicit.stat_2974417149@T1` | -1.27802 |
| `explicit.stat_2901986750@T1` | -1.27526 |
| `explicit.stat_2974417149@T2` | -1.26576 |
| `explicit.stat_4080418644@T1` | -1.25143 |
| `explicit.stat_803737631@T2` | -1.24992 |

### accessory.belt — n=45010, R²=-1.494

intercept: `5.1778`  ·  log_price: True  ·  ilvl: `-0.06042`  ·  n_mods: `-0.05668`  ·  n_top_tier: `0.53392`  ·  corrupted: `1.25867`  ·  n_sockets: `1.13321`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.33761 |
| `explicit.stat_2923486259@T2` | 0.76808 |
| `explicit.stat_3299347043@T2` | -0.66333 |
| `explicit.stat_2881298780@T1` | -0.61470 |
| `explicit.stat_3299347043@T1` | -0.60870 |
| `explicit.stat_51994685@T1` | -0.59681 |
| `explicit.stat_1570770415@T2` | -0.57418 |
| `explicit.stat_3325883026@T1` | -0.56093 |
| `explicit.stat_809229260@T2` | -0.55633 |
| `explicit.stat_2881298780@T2` | -0.55326 |
| `explicit.stat_915769802@T1` | -0.54875 |
| `explicit.stat_4080418644@T2` | -0.54750 |

### armour.chest — n=44634, R²=-1.7042

intercept: `3.5641`  ·  log_price: True  ·  ilvl: `-0.04393`  ·  n_mods: `-0.02061`  ·  n_top_tier: `0.36197`  ·  corrupted: `0.39296`  ·  n_sockets: `0.03440`  ·  quality: `0.07222`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.91621 |
| `explicit.stat_3372524247@T1` | 0.46701 |
| `explicit.stat_986397080@T2` | -0.45456 |
| `explicit.stat_986397080@T1` | -0.45219 |
| `explicit.stat_3484657501@T1` | -0.45150 |
| `explicit.stat_4080418644@T2` | -0.41925 |
| `explicit.stat_1692879867@T2` | -0.41171 |
| `explicit.stat_2339757871@T2` | -0.40754 |
| `explicit.stat_915769802@T2` | -0.39845 |
| `explicit.stat_3301100256@T2` | -0.38876 |
| `explicit.stat_1999113824@T2` | -0.38635 |
| `explicit.stat_915769802@T1` | -0.38291 |

### armour.helmet — n=43424, R²=-1.4961

intercept: `3.4838`  ·  log_price: True  ·  ilvl: `-0.04390`  ·  n_mods: `-0.04402`  ·  n_top_tier: `0.62189`  ·  corrupted: `0.51055`  ·  n_sockets: `0.16930`  ·  quality: `0.06300`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.51686 |
| `crafted.stat_3917489142@T1` | 2.21781 |
| `explicit.stat_1263695895@T1` | -1.03154 |
| `explicit.stat_3917489142@T2` | -0.99030 |
| `explicit.stat_3917489142@T1` | -0.85068 |
| `explicit.stat_1999113824@T1` | -0.79594 |
| `explicit.stat_2162097452@T2` | -0.76449 |
| `explicit.stat_1263695895@T2` | -0.73802 |
| `explicit.stat_3321629045@T2` | -0.73473 |
| `explicit.stat_803737631@T1` | -0.72807 |
| `explicit.stat_1999113824@T2` | -0.70470 |
| `explicit.stat_4052037485@T2` | -0.70370 |

### armour.boots — n=40164, R²=-1.7227

intercept: `3.4997`  ·  log_price: True  ·  ilvl: `-0.04321`  ·  n_mods: `-0.02160`  ·  n_top_tier: `0.40925`  ·  corrupted: `0.03910`  ·  n_sockets: `0.05986`  ·  quality: `0.06986`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.74736 |
| `explicit.stat_2339757871@T1` | -1.50710 |
| `crafted.stat_3917489142@T1` | 1.38192 |
| `explicit.stat_2923486259@T1` | 0.79355 |
| `explicit.stat_3299347043@T1` | -0.52938 |
| `explicit.stat_2923486259@T2` | -0.48086 |
| `explicit.stat_3917489142@T2` | -0.47174 |
| `explicit.stat_2160282525@T1` | -0.46846 |
| `explicit.stat_1671376347@T2` | -0.46493 |
| `explicit.stat_328541901@T2` | -0.46153 |
| `explicit.stat_99927264@T1` | -0.44194 |
| `explicit.stat_1874553720@T1` | -0.43575 |

### armour.gloves — n=39192, R²=-1.6317

intercept: `3.8229`  ·  log_price: True  ·  ilvl: `-0.04992`  ·  n_mods: `-0.01017`  ·  n_top_tier: `0.83107`  ·  corrupted: `-0.04781`  ·  n_sockets: `0.20172`  ·  quality: `0.05973`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.51804 |
| `explicit.stat_2923486259@T2` | -1.26570 |
| `explicit.stat_4052037485@T1` | -1.10456 |
| `explicit.stat_3484657501@T2` | -1.07981 |
| `explicit.stat_4052037485@T2` | -1.05744 |
| `explicit.stat_3321629045@T2` | -1.03461 |
| `explicit.stat_124859000@T1` | -1.00287 |
| `explicit.stat_3484657501@T1` | -0.99576 |
| `explicit.stat_803737631@T2` | -0.95250 |
| `explicit.stat_9187492@T2` | -0.94907 |
| `explicit.stat_3639275092@T1` | -0.92804 |
| `explicit.stat_681332047@T2` | -0.92701 |

### weapon.wand — n=23129, R²=-1.8861

intercept: `4.0507`  ·  log_price: True  ·  ilvl: `-0.05001`  ·  n_mods: `-0.07196`  ·  n_top_tier: `0.62326`  ·  corrupted: `-0.00770`  ·  n_sockets: `0.01810`  ·  quality: `0.04172`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.55442 |
| `explicit.stat_1545858329@T1` | 2.67672 |
| `explicit.stat_2254480358@T1` | 2.35259 |
| `explicit.stat_591105508@T1` | 2.11935 |
| `explicit.stat_124131830@T1` | 2.10224 |
| `explicit.stat_736967255@T2` | 1.58689 |
| `explicit.stat_4226189338@T1` | 1.57188 |
| `explicit.stat_2254480358@T2` | 1.17777 |
| `explicit.stat_1263695895@T2` | -1.12246 |
| `crafted.stat_124131830` | 1.11593 |
| `explicit.stat_1263695895@T1` | -1.08084 |
| `explicit.stat_3962278098@T2` | -1.06413 |

### flask.charm — n=20135, R²=-0.6612

intercept: `0.1069`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.75643`  ·  corrupted: `1.56650`  ·  quality: `0.00641`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.59505 |
| `explicit.stat_1056492907` | 2.60080 |
| `explicit.stat_3246948616` | 2.07828 |
| `explicit.stat_1120862500@T2` | -1.75648 |
| `explicit.stat_828533480@T2` | -1.75646 |
| `explicit.stat_1873752457@T2` | -1.75643 |
| `explicit.stat_2676834156@T2` | -1.75638 |
| `explicit.stat_2365392475@T2` | -1.75635 |
| `explicit.stat_3196823591@T2` | -1.75632 |
| `explicit.stat_2541588185@T2` | -1.75545 |
| `explicit.stat_388617051@T2` | -1.75489 |
| `explicit.stat_828533480@T1` | -1.75114 |

### weapon.bow — n=18469, R²=-1.7761

intercept: `3.9381`  ·  log_price: True  ·  ilvl: `-0.04666`  ·  n_mods: `-0.09834`  ·  n_top_tier: `0.72022`  ·  corrupted: `0.77342`  ·  n_sockets: `0.05853`  ·  quality: `0.02799`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 4.60287 |
| `desecrated.stat_210067635@T1` | -1.73525 |
| `explicit.stat_1263695895@T1` | -1.36422 |
| `explicit.stat_1263695895@T2` | -1.21495 |
| `crafted.stat_3035140377` | 1.19138 |
| `explicit.stat_1509134228@T1` | -1.04668 |
| `explicit.stat_709508406@T1` | 1.02466 |
| `explicit.stat_2463230181@T2` | -0.91557 |
| `explicit.stat_3695891184@T1` | -0.86844 |
| `crafted.stat_210067635@T2` | -0.86684 |
| `explicit.stat_210067635@T2` | -0.86091 |
| `explicit.stat_1368271171@T2` | -0.84735 |

### weapon.crossbow — n=17290, R²=-1.6872

intercept: `4.2637`  ·  log_price: True  ·  ilvl: `-0.05119`  ·  n_mods: `-0.08198`  ·  n_top_tier: `0.29110`  ·  corrupted: `-0.06708`  ·  n_sockets: `0.06343`  ·  quality: `0.02058`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.84161 |
| `explicit.stat_1202301673@T1` | 1.53254 |
| `explicit.stat_1980802737` | 1.47529 |
| `explicit.stat_2250681686@T2` | -1.44052 |
| `explicit.stat_1509134228@T1` | 1.23596 |
| `explicit.stat_2250681686` | 1.22120 |
| `explicit.stat_709508406@T1` | 0.90008 |
| `crafted.stat_3035140377` | 0.84172 |
| `explicit.stat_387439868@T1` | 0.60326 |
| `explicit.stat_3695891184@T1` | -0.57505 |
| `explicit.stat_1263695895@T2` | -0.50962 |
| `explicit.stat_3336890334@T2` | -0.50731 |

### weapon.warstaff — n=12131, R²=-0.3358

intercept: `-10.4859`  ·  log_price: True  ·  ilvl: `0.14251`  ·  n_mods: `-0.23971`  ·  n_top_tier: `0.53420`  ·  corrupted: `0.23838`  ·  n_sockets: `0.12520`  ·  quality: `0.05497`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 1.42305 |
| `desecrated.stat_2527686725@T1` | 1.42305 |
| `explicit.stat_821021828@T2` | -0.97450 |
| `crafted.stat_210067635@T2` | 0.93405 |
| `explicit.stat_1037193709@T2` | -0.90854 |
| `explicit.stat_328541901@T2` | -0.89751 |
| `desecrated.stat_9187492` | 0.79686 |
| `rune.stat_243313994` | 0.77478 |
| `explicit.stat_328541901@T1` | -0.76943 |
| `explicit.stat_691932474@T2` | -0.68313 |
| `explicit.stat_1940865751@T2` | -0.64958 |
| `explicit.stat_821021828@T1` | -0.63972 |

### weapon.staff — n=11545, R²=-0.3564

intercept: `-16.0882`  ·  log_price: True  ·  ilvl: `0.20510`  ·  n_mods: `-0.06726`  ·  n_top_tier: `0.51117`  ·  corrupted: `0.79987`  ·  n_sockets: `0.19110`  ·  quality: `0.03164`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.88755 |
| `explicit.stat_4226189338@T1` | 1.77040 |
| `explicit.stat_591105508@T1` | 1.68419 |
| `explicit.stat_1600707273@T1` | 1.47398 |
| `explicit.stat_1545858329@T1` | 1.14485 |
| `explicit.stat_293638271@T2` | -1.01018 |
| `explicit.stat_473429811@T2` | -0.90534 |
| `explicit.stat_3962278098@T2` | 0.83510 |
| `explicit.stat_124131830@T2` | 0.72771 |
| `explicit.stat_4226189338@T2` | 0.67114 |
| `rune.stat_124131830` | 0.61799 |
| `crafted.stat_124131830` | 0.61535 |

### weapon.sceptre — n=11284, R²=-0.3373

intercept: `-21.1207`  ·  log_price: True  ·  ilvl: `0.26794`  ·  n_mods: `-0.02532`  ·  n_top_tier: `0.08821`  ·  corrupted: `0.24820`  ·  n_sockets: `0.17959`  ·  quality: `0.03499`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.89143 |
| `explicit.stat_2162097452@T2` | 1.62324 |
| `explicit.stat_3057012405@T1` | 1.34172 |
| `explicit.stat_1263695895@T1` | -1.07339 |
| `explicit.stat_1263695895@T2` | -1.01633 |
| `explicit.stat_1798257884@T2` | 0.91378 |
| `explicit.stat_101878827@T1` | 0.88890 |
| `explicit.stat_101878827@T2` | 0.85868 |
| `explicit.stat_4080418644@T2` | -0.62721 |
| `explicit.stat_2854751904@T2` | -0.61610 |
| `explicit.stat_4080418644@T1` | -0.51803 |
| `explicit.stat_849987426@T2` | 0.50430 |

### weapon.spear — n=9164, R²=-0.3837

intercept: `-13.3351`  ·  log_price: True  ·  ilvl: `0.18313`  ·  n_mods: `-0.14239`  ·  n_top_tier: `0.57824`  ·  corrupted: `-0.50910`  ·  n_sockets: `0.18126`  ·  quality: `0.07147`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -4.93893 |
| `crafted.stat_210067635@T2` | -3.10555 |
| `explicit.stat_1202301673@T1` | 1.18779 |
| `explicit.stat_9187492@T1` | 1.07948 |
| `explicit.stat_1940865751@T2` | -0.96631 |
| `crafted.stat_3035140377` | 0.95875 |
| `explicit.stat_748522257@T2` | -0.95832 |
| `explicit.stat_4080418644@T2` | -0.94491 |
| `explicit.stat_3336890334@T2` | -0.91523 |
| `explicit.stat_1037193709@T1` | -0.84126 |
| `explicit.stat_691932474@T2` | -0.83681 |
| `desecrated.stat_210067635@T1` | -0.83537 |

### armour.focus — n=7490, R²=-0.3235

intercept: `-15.7833`  ·  log_price: True  ·  ilvl: `0.20158`  ·  n_mods: `-0.16236`  ·  n_top_tier: `0.94073`  ·  corrupted: `0.01241`  ·  n_sockets: `0.30164`  ·  quality: `0.03265`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 2.40762 |
| `explicit.stat_4220027924@T1` | -1.43306 |
| `explicit.stat_2923486259@T1` | -1.35679 |
| `explicit.stat_4220027924@T2` | -1.12873 |
| `explicit.stat_2923486259@T2` | -1.11414 |
| `explicit.stat_2231156303@T2` | -1.06808 |
| `explicit.stat_2768835289@T1` | -1.06158 |
| `explicit.stat_2339757871@T2` | -1.05364 |
| `explicit.stat_4015621042@T1` | -1.02864 |
| `explicit.stat_1050105434@T2` | -1.00955 |
| `explicit.stat_2231156303@T1` | -1.00417 |
| `explicit.stat_3291658075@T2` | -0.96921 |

### armour.quiver — n=6985, R²=-0.2811

intercept: `-18.1754`  ·  log_price: True  ·  ilvl: `0.21953`  ·  n_mods: `-0.05593`  ·  n_top_tier: `0.64666`  ·  corrupted: `0.97287`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.36136 |
| `explicit.stat_681332047@T2` | -1.50292 |
| `explicit.stat_681332047@T1` | -1.24018 |
| `explicit.stat_1573130764@T2` | -0.97106 |
| `explicit.stat_1573130764@T1` | -0.85221 |
| `explicit.stat_2321178454@T2` | -0.76527 |
| `explicit.stat_2194114101@T2` | -0.72509 |
| `explicit.stat_4067062424@T1` | -0.64086 |
| `explicit.stat_803737631@T1` | -0.58010 |
| `explicit.stat_3261801346@T1` | -0.51958 |
| `explicit.stat_3714003708@T2` | -0.51665 |
| `explicit.stat_4067062424@T2` | -0.49246 |

### armour.shield — n=5990, R²=-0.4241

intercept: `-12.4171`  ·  log_price: True  ·  ilvl: `0.16577`  ·  n_mods: `-0.16441`  ·  n_top_tier: `0.70170`  ·  corrupted: `-0.32953`  ·  n_sockets: `0.41192`  ·  quality: `0.03960`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.44078 |
| `explicit.stat_2901986750@T1` | -1.26870 |
| `explicit.stat_4095671657@T1` | -1.12333 |
| `explicit.stat_4095671657@T2` | -1.12178 |
| `explicit.stat_2481353198@T1` | -1.11840 |
| `explicit.stat_3321629045@T2` | -1.09742 |
| `explicit.stat_1011760251@T1` | -1.09563 |
| `explicit.stat_4052037485@T1` | -1.08211 |
| `explicit.stat_2481353198@T2` | -1.03890 |
| `explicit.stat_328541901@T1` | -1.03308 |
| `explicit.stat_328541901@T2` | -0.96541 |
| `explicit.stat_3362812763@T1` | -0.95413 |

### weapon.twomace — n=5464, R²=-0.4469

intercept: `-11.1434`  ·  log_price: True  ·  ilvl: `0.15022`  ·  n_mods: `-0.22568`  ·  n_top_tier: `0.52123`  ·  corrupted: `0.56948`  ·  n_sockets: `0.13865`  ·  quality: `0.06007`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.93788 |
| `explicit.stat_1037193709@T1` | -1.65818 |
| `explicit.stat_3336890334@T1` | -1.45863 |
| `explicit.stat_1263695895@T2` | -1.29734 |
| `explicit.stat_9187492@T1` | -1.13908 |
| `explicit.stat_2694482655@T1` | 0.85325 |
| `explicit.stat_3695891184@T1` | -0.83798 |
| `explicit.stat_3695891184@T2` | -0.79352 |
| `explicit.stat_518292764@T2` | -0.75448 |
| `explicit.stat_1263695895@T1` | -0.68056 |
| `explicit.stat_691932474@T1` | -0.66576 |
| `explicit.stat_210067635@T1` | -0.65181 |

## Coverage (listings per base)

- … **Sapphire** — 37389 listings (37330 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 36436 listings (36390 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 27871 listings (27840 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 12835 listings (12817 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11797 listings (11773 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 11479 listings (11453 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 11340 listings (11328 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10639 listings (10612 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10584 listings (10561 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 10038 listings (10025 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8796 listings (8781 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8427 listings (8418 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8369 listings (8360 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7467 listings (7444 priced) [0.3–4297682211.9 ex]
- … **Unset Ring** — 7277 listings (7258 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7257 listings (7250 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 7195 listings (7180 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 7109 listings (7101 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 7012 listings (6982 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6995 listings (6986 priced) [0.2–275252424.7 ex]
- … **Ancestral Tiara** — 6958 listings (6929 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6875 listings (6865 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6574 listings (6570 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6456 listings (6442 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6215 listings (6202 priced) [0.3–398912568423.8 ex]

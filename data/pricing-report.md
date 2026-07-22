# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-22T12:58:18+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **737455** (735084 priced in exalted)
- Distinct bases: 1002 · distinct mods: 3332 · mod rows: 3484842
- Sold signals: **24047** sold · 419304 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-22T12:45:45+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×16.73** (median |log error| 2.8171)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.15** · typical error ×44.51 · ±30% 8% · n=107059
- Premium segment (60ex+): skill **+0.14** · typical error ×226.60 · ±30% 0% · n=71075

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 15933 | ×45.13 | 21% | +0.04 | +0.07 |
| jewel | 15407 | ×10.08 | 5% | +0.11 | +0.13 |
| accessory.amulet | 14280 | ×10.00 | 25% | +0.02 | +0.01 |
| accessory.belt | 10042 | ×24.85 | 23% | +0.02 | +0.05 |
| armour.chest | 9786 | ×17.10 | 21% | +0.08 | +0.11 |
| armour.helmet | 9524 | ×23.20 | 16% | +0.09 | +0.11 |
| armour.boots | 8773 | ×21.69 | 17% | +0.11 | +0.13 |
| armour.gloves | 8659 | ×30.27 | 13% | +0.09 | +0.11 |
| other | 8575 | ×2.00 | 42% | +0.12 | +0.18 |
| weapon.wand | 5015 | ×35.31 | 14% | +0.12 | +0.12 |
| weapon.bow | 3961 | ×24.38 | 11% | +0.17 | +0.18 |
| weapon.crossbow | 3747 | ×23.16 | 13% | +0.12 | +0.16 |
| weapon.warstaff | 2573 | ×14.14 | 7% | +0.15 | +0.16 |
| weapon.staff | 2503 | ×15.39 | 6% | +0.13 | +0.13 |
| weapon.sceptre | 2447 | ×18.10 | 5% | +0.06 | +0.07 |
| weapon.spear | 1974 | ×13.59 | 7% | +0.11 | +0.15 |
| armour.focus | 1631 | ×12.58 | 7% | +0.09 | +0.10 |
| armour.quiver | 1537 | ×17.17 | 7% | +0.12 | +0.13 |
| armour.shield | 1248 | ×7.84 | 8% | +0.10 | +0.11 |
| flask.charm | 1241 | ×10.00 | 27% | +0.03 | +0.02 |
| weapon.twomace | 1148 | ×8.75 | 6% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=84563, R²=-0.9941

intercept: `-1.9145`  ·  log_price: True  ·  ilvl: `0.02393`  ·  n_mods: `0.74216`  ·  n_top_tier: `-0.16682`  ·  corrupted: `0.46163`  ·  quality: `-0.14956`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.28762 |
| `explicit.stat_1869147066@T1` | -3.17711 |
| `explicit.stat_3668351662@T1` | -2.03032 |
| `explicit.stat_1594812856@T1` | 1.74675 |
| `explicit.stat_3780644166@T1` | -1.60693 |
| `explicit.stat_3485067555@T1` | 1.58460 |
| `explicit.stat_239367161@T1` | -1.52695 |
| `explicit.stat_2527686725@T1` | 1.48880 |
| `explicit.stat_1697447343@T1` | -1.43122 |
| `explicit.stat_3028809864@T1` | -1.38480 |
| `explicit.stat_3374165039@T1` | -1.29397 |
| `explicit.stat_429143663@T1` | 1.26943 |

### accessory.ring — n=72684, R²=-2.009

intercept: `3.3242`  ·  log_price: True  ·  ilvl: `-0.04166`  ·  n_mods: `0.00171`  ·  n_top_tier: `0.94004`  ·  corrupted: `-0.00447`  ·  n_sockets: `2.20277`  ·  quality: `-0.00269`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -0.98471 |
| `explicit.stat_1263695895@T2` | -0.96398 |
| `explicit.stat_1573130764@T2` | -0.96095 |
| `explicit.stat_3917489142@T2` | -0.95993 |
| `explicit.stat_2891184298@T2` | -0.95961 |
| `explicit.stat_3372524247@T2` | -0.95789 |
| `explicit.stat_2891184298@T1` | -0.95685 |
| `explicit.stat_4080418644@T1` | -0.95674 |
| `explicit.stat_3695891184@T1` | -0.95617 |
| `explicit.stat_2923486259@T2` | -0.95604 |
| `explicit.stat_1671376347@T2` | -0.95577 |
| `explicit.stat_3325883026@T1` | -0.95558 |

### other — n=70226, R²=-0.6735

intercept: `1.6093`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.08559`  ·  n_top_tier: `0.26098`  ·  corrupted: `0.00040`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.37438 |
| `implicit.stat_718638445` | 0.25682 |
| `implicit.stat_3182714256` | 0.25681 |
| `explicit.stat_3299347043@T1` | -0.24062 |
| `implicit.stat_2219129443` | 0.22169 |
| `explicit.stat_3917489142@T1` | -0.16983 |
| `explicit.stat_2974417149@T1` | 0.14146 |
| `implicit.stat_958696139` | -0.08558 |
| `explicit.stat_789117908@T1` | -0.06466 |
| `implicit.stat_3879011313` | 0.06002 |
| `implicit.stat_1416292992` | -0.05705 |
| `explicit.stat_736967255@T1` | -0.04265 |

### accessory.amulet — n=65062, R²=-0.4937

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `1.30414`  ·  corrupted: `0.00000`  ·  n_sockets: `1.79169`  ·  quality: `0.03549`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T2` | -1.52061 |
| `explicit.stat_1202301673@T2` | -1.45595 |
| `explicit.stat_2162097452@T2` | -1.32911 |
| `explicit.stat_789117908@T1` | -1.30417 |
| `explicit.stat_803737631@T2` | -1.30417 |
| `explicit.stat_803737631@T1` | -1.30417 |
| `explicit.stat_983749596@T2` | -1.30417 |
| `explicit.stat_4080418644@T2` | -1.30417 |
| `explicit.stat_789117908@T2` | -1.30416 |
| `explicit.stat_3299347043@T2` | -1.30416 |
| `explicit.stat_2891184298@T1` | -1.30416 |
| `explicit.stat_3981240776@T2` | -1.30416 |

### accessory.belt — n=45981, R²=-2.1135

intercept: `0.4383`  ·  log_price: True  ·  ilvl: `-0.00529`  ·  n_mods: `-0.00223`  ·  n_top_tier: `0.73283`  ·  corrupted: `0.74154`  ·  n_sockets: `1.59680`

| stat_id | coef |
|---|---|
| `explicit.stat_915769802@T1` | -0.73617 |
| `explicit.stat_2881298780@T1` | -0.73576 |
| `explicit.stat_3299347043@T2` | -0.73564 |
| `explicit.stat_809229260@T2` | -0.73551 |
| `explicit.stat_3299347043@T1` | -0.73530 |
| `explicit.stat_51994685@T1` | -0.73528 |
| `explicit.stat_1570770415@T2` | -0.73461 |
| `explicit.stat_3325883026@T1` | -0.73430 |
| `explicit.stat_3372524247@T2` | -0.73423 |
| `explicit.stat_915769802@T2` | -0.73378 |
| `explicit.stat_1570770415@T1` | -0.73326 |
| `explicit.stat_2881298780@T2` | -0.73318 |

### armour.chest — n=45622, R²=-1.7919

intercept: `3.3539`  ·  log_price: True  ·  ilvl: `-0.04128`  ·  n_mods: `-0.01564`  ·  n_top_tier: `0.30696`  ·  corrupted: `0.27412`  ·  n_sockets: `0.02616`  ·  quality: `0.07901`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.14027 |
| `explicit.stat_986397080@T2` | -0.36688 |
| `explicit.stat_986397080@T1` | -0.34731 |
| `explicit.stat_4080418644@T2` | -0.34600 |
| `explicit.stat_1692879867@T2` | -0.34402 |
| `explicit.stat_915769802@T2` | -0.33345 |
| `explicit.stat_2451402625@T2` | -0.33107 |
| `explicit.stat_3484657501@T1` | -0.32814 |
| `explicit.stat_1062208444@T2` | -0.32701 |
| `explicit.stat_915769802@T1` | -0.32483 |
| `explicit.stat_4080418644@T1` | -0.32285 |
| `explicit.stat_1999113824@T1` | -0.31870 |

### armour.helmet — n=44413, R²=-1.6963

intercept: `3.4147`  ·  log_price: True  ·  ilvl: `-0.04268`  ·  n_mods: `-0.02835`  ·  n_top_tier: `0.49740`  ·  corrupted: `0.59493`  ·  n_sockets: `0.08449`  ·  quality: `0.07041`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.29771 |
| `crafted.stat_3917489142@T1` | 1.01675 |
| `explicit.stat_1263695895@T1` | -0.80839 |
| `explicit.stat_3917489142@T2` | -0.71870 |
| `explicit.stat_2162097452@T2` | -0.69168 |
| `explicit.stat_3917489142@T1` | -0.64553 |
| `explicit.stat_4052037485@T2` | -0.62995 |
| `explicit.stat_1263695895@T2` | -0.59623 |
| `explicit.stat_4015621042@T2` | -0.58662 |
| `explicit.stat_4052037485@T1` | -0.56831 |
| `explicit.stat_803737631@T1` | -0.54053 |
| `explicit.stat_1999113824@T1` | -0.53908 |

### armour.boots — n=41004, R²=-1.647

intercept: `3.8039`  ·  log_price: True  ·  ilvl: `-0.04686`  ·  n_mods: `-0.03433`  ·  n_top_tier: `0.45399`  ·  corrupted: `0.10394`  ·  n_sockets: `0.07497`  ·  quality: `0.07082`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.05030 |
| `explicit.stat_2250533757@T1` | 1.71127 |
| `crafted.stat_3917489142@T1` | 1.41447 |
| `explicit.stat_3299347043@T1` | -0.65800 |
| `explicit.stat_2923486259@T2` | -0.62814 |
| `explicit.stat_2923486259@T1` | 0.61259 |
| `explicit.stat_3917489142@T2` | -0.54279 |
| `explicit.stat_1874553720@T1` | -0.53354 |
| `explicit.stat_1062208444@T2` | -0.51948 |
| `explicit.stat_2160282525@T1` | -0.51753 |
| `explicit.stat_328541901@T2` | -0.50964 |
| `explicit.stat_99927264@T1` | -0.50752 |

### armour.gloves — n=39996, R²=-1.64

intercept: `3.8700`  ·  log_price: True  ·  ilvl: `-0.05092`  ·  n_mods: `-0.00926`  ·  n_top_tier: `0.72073`  ·  corrupted: `-0.07017`  ·  n_sockets: `0.20119`  ·  quality: `0.05544`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.10620 |
| `explicit.stat_4052037485@T1` | -1.01466 |
| `explicit.stat_4052037485@T2` | -1.01319 |
| `explicit.stat_3484657501@T2` | -1.00420 |
| `explicit.stat_3484657501@T1` | -0.94601 |
| `explicit.stat_3321629045@T2` | -0.94531 |
| `explicit.stat_4015621042@T2` | -0.93684 |
| `explicit.stat_2923486259@T2` | -0.89816 |
| `explicit.stat_124859000@T1` | -0.85163 |
| `explicit.stat_9187492@T2` | -0.85049 |
| `explicit.stat_3639275092@T1` | -0.82133 |
| `explicit.stat_3917489142@T2` | -0.81250 |

### weapon.wand — n=23466, R²=-1.8842

intercept: `3.8255`  ·  log_price: True  ·  ilvl: `-0.04723`  ·  n_mods: `-0.07163`  ·  n_top_tier: `0.57850`  ·  corrupted: `0.11795`  ·  n_sockets: `0.02813`  ·  quality: `0.03588`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.21972 |
| `explicit.stat_1545858329@T1` | 2.74202 |
| `explicit.stat_2254480358@T1` | 2.59149 |
| `explicit.stat_591105508@T1` | 2.16791 |
| `explicit.stat_124131830@T1` | 2.14073 |
| `crafted.stat_124131830` | 1.25147 |
| `explicit.stat_2254480358@T2` | 1.24901 |
| `explicit.stat_4226189338@T1` | 1.22159 |
| `explicit.stat_1600707273@T1` | 1.11536 |
| `explicit.stat_1263695895@T2` | -1.07207 |
| `explicit.stat_1263695895@T1` | -0.88447 |
| `explicit.stat_473429811@T1` | -0.84586 |

### flask.charm — n=20686, R²=-0.6657

intercept: `0.1068`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.60899`  ·  corrupted: `1.50712`  ·  quality: `0.02484`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60513 |
| `explicit.stat_1056492907` | 2.52874 |
| `explicit.stat_3246948616` | 2.01535 |
| `explicit.stat_828533480@T2` | -1.60903 |
| `explicit.stat_1120862500@T2` | -1.60901 |
| `explicit.stat_1873752457@T2` | -1.60900 |
| `explicit.stat_2541588185@T2` | -1.60899 |
| `explicit.stat_388617051@T2` | -1.60897 |
| `explicit.stat_2365392475@T2` | -1.60892 |
| `explicit.stat_3196823591@T2` | -1.60760 |
| `explicit.stat_2676834156@T2` | -1.60690 |
| `explicit.stat_1873752457@T1` | -1.60595 |

### weapon.bow — n=18776, R²=-1.7255

intercept: `4.1358`  ·  log_price: True  ·  ilvl: `-0.04862`  ·  n_mods: `-0.10953`  ·  n_top_tier: `0.73675`  ·  corrupted: `0.56626`  ·  n_sockets: `0.05410`  ·  quality: `0.03642`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 3.73166 |
| `desecrated.stat_210067635@T1` | -1.71929 |
| `explicit.stat_1263695895@T1` | -1.42831 |
| `crafted.stat_210067635@T2` | -1.28106 |
| `explicit.stat_1263695895@T2` | -1.26106 |
| `crafted.stat_3035140377` | 1.17474 |
| `explicit.stat_1509134228@T1` | -0.98183 |
| `explicit.stat_210067635@T2` | -0.93767 |
| `explicit.stat_1368271171@T2` | -0.87865 |
| `explicit.stat_3695891184@T1` | -0.85814 |
| `explicit.stat_821021828@T2` | -0.81955 |
| `explicit.stat_1368271171@T1` | -0.78895 |

### weapon.crossbow — n=17587, R²=-1.6638

intercept: `4.1937`  ·  log_price: True  ·  ilvl: `-0.05000`  ·  n_mods: `-0.10039`  ·  n_top_tier: `0.42998`  ·  corrupted: `-0.06290`  ·  n_sockets: `0.07500`  ·  quality: `0.01410`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.95577 |
| `explicit.stat_2250681686@T2` | -1.44906 |
| `explicit.stat_1980802737` | 1.44767 |
| `explicit.stat_1202301673@T1` | 1.26543 |
| `explicit.stat_2250681686` | 1.08513 |
| `explicit.stat_1509134228@T1` | 0.90995 |
| `crafted.stat_3035140377` | 0.88639 |
| `explicit.stat_3695891184@T1` | -0.78139 |
| `explicit.stat_709508406@T1` | 0.74584 |
| `explicit.stat_3336890334@T2` | -0.70053 |
| `explicit.stat_3695891184@T2` | -0.69636 |
| `explicit.stat_210067635@T2` | -0.62232 |

### weapon.warstaff — n=12389, R²=-0.3242

intercept: `-11.0480`  ·  log_price: True  ·  ilvl: `0.15075`  ·  n_mods: `-0.24210`  ·  n_top_tier: `0.50331`  ·  corrupted: `0.25932`  ·  n_sockets: `0.11960`  ·  quality: `0.05246`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 1.09425 |
| `desecrated.stat_2231156303@T1` | 1.09425 |
| `crafted.stat_210067635@T2` | 0.94714 |
| `explicit.stat_821021828@T2` | -0.88593 |
| `explicit.stat_328541901@T2` | -0.88385 |
| `explicit.stat_1037193709@T2` | -0.83529 |
| `explicit.stat_210067635@T1` | -0.83383 |
| `explicit.stat_328541901@T1` | -0.80963 |
| `desecrated.stat_9187492` | 0.78482 |
| `rune.stat_243313994` | 0.78292 |
| `explicit.stat_1940865751@T2` | -0.70272 |
| `desecrated.stat_473429811@T1` | -0.62230 |

### weapon.staff — n=11827, R²=-0.3514

intercept: `-16.4934`  ·  log_price: True  ·  ilvl: `0.21152`  ·  n_mods: `-0.09241`  ·  n_top_tier: `0.37651`  ·  corrupted: `0.94515`  ·  n_sockets: `0.19720`  ·  quality: `0.04178`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.27785 |
| `explicit.stat_124131830@T1` | 2.14753 |
| `explicit.stat_4226189338@T1` | 1.72948 |
| `explicit.stat_1600707273@T1` | 1.41376 |
| `explicit.stat_1545858329@T1` | 1.29873 |
| `explicit.stat_3962278098@T2` | 1.13375 |
| `explicit.stat_591105508@T2` | 1.02851 |
| `explicit.stat_124131830@T2` | 0.83344 |
| `explicit.stat_4226189338@T2` | 0.81441 |
| `explicit.stat_473429811@T2` | -0.77860 |
| `explicit.stat_293638271@T2` | -0.68122 |
| `explicit.stat_1263695895@T1` | 0.64354 |

### weapon.sceptre — n=11498, R²=-0.3292

intercept: `-21.6995`  ·  log_price: True  ·  ilvl: `0.27624`  ·  n_mods: `-0.01085`  ·  n_top_tier: `0.17299`  ·  corrupted: `0.26129`  ·  n_sockets: `0.19436`  ·  quality: `0.03483`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.59105 |
| `explicit.stat_2162097452@T2` | 1.23683 |
| `explicit.stat_3057012405@T1` | 1.03894 |
| `explicit.stat_1798257884@T2` | 0.90919 |
| `explicit.stat_4080418644@T2` | -0.76002 |
| `explicit.stat_101878827@T2` | 0.72703 |
| `explicit.stat_101878827@T1` | 0.69561 |
| `explicit.stat_1263695895@T1` | -0.63154 |
| `explicit.stat_1263695895@T2` | -0.58972 |
| `explicit.stat_2854751904@T2` | -0.56736 |
| `explicit.stat_2347036682@T1` | 0.45245 |
| `explicit.stat_1250712710@T2` | 0.38408 |

### weapon.spear — n=9353, R²=-0.3783

intercept: `-13.6666`  ·  log_price: True  ·  ilvl: `0.18840`  ·  n_mods: `-0.18665`  ·  n_top_tier: `0.60000`  ·  corrupted: `-0.55336`  ·  n_sockets: `0.24186`  ·  quality: `0.07059`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.18572 |
| `desecrated.stat_666077204@T1` | -3.08755 |
| `explicit.stat_1037193709@T1` | -1.18546 |
| `explicit.stat_4080418644@T2` | -1.06693 |
| `explicit.stat_9187492@T2` | -1.02881 |
| `crafted.stat_3035140377` | 1.02130 |
| `explicit.stat_748522257@T2` | -0.98004 |
| `explicit.stat_4080418644@T1` | -0.91511 |
| `explicit.stat_3336890334@T2` | -0.91140 |
| `explicit.stat_3261801346@T1` | -0.87632 |
| `explicit.stat_1940865751@T2` | -0.87361 |
| `explicit.stat_3261801346@T2` | -0.85902 |

### armour.focus — n=7636, R²=-0.3412

intercept: `-16.0454`  ·  log_price: True  ·  ilvl: `0.20497`  ·  n_mods: `-0.15734`  ·  n_top_tier: `1.01502`  ·  corrupted: `-0.31999`  ·  n_sockets: `0.41202`  ·  quality: `0.02878`

| stat_id | coef |
|---|---|
| `explicit.stat_4220027924@T1` | -1.62744 |
| `explicit.stat_2923486259@T1` | -1.54341 |
| `explicit.stat_2923486259@T2` | -1.41467 |
| `crafted.stat_737908626@T2` | 1.40264 |
| `crafted.stat_2974417149@T1` | 1.34620 |
| `explicit.stat_2768835289@T1` | -1.31312 |
| `explicit.stat_2339757871@T2` | -1.28224 |
| `explicit.stat_3962278098@T2` | -1.27252 |
| `explicit.stat_2231156303@T1` | -1.23400 |
| `explicit.stat_4220027924@T2` | -1.17432 |
| `explicit.stat_274716455@T2` | -1.16032 |
| `explicit.stat_4015621042@T1` | -1.15653 |

### armour.quiver — n=7112, R²=-0.2748

intercept: `-18.7981`  ·  log_price: True  ·  ilvl: `0.22606`  ·  n_mods: `-0.05378`  ·  n_top_tier: `0.70884`  ·  corrupted: `0.98586`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 4.98083 |
| `explicit.stat_681332047@T2` | -1.26800 |
| `explicit.stat_681332047@T1` | -1.09388 |
| `explicit.stat_1573130764@T2` | -0.98846 |
| `explicit.stat_2321178454@T2` | -0.87480 |
| `explicit.stat_1573130764@T1` | -0.86019 |
| `explicit.stat_2194114101@T2` | -0.84223 |
| `explicit.stat_4067062424@T1` | -0.64223 |
| `explicit.stat_3714003708@T2` | -0.63018 |
| `explicit.stat_803737631@T2` | -0.60416 |
| `explicit.stat_4067062424@T2` | -0.59453 |
| `explicit.stat_803737631@T1` | -0.59219 |

### armour.shield — n=6127, R²=-0.4038

intercept: `-13.4833`  ·  log_price: True  ·  ilvl: `0.18180`  ·  n_mods: `-0.18679`  ·  n_top_tier: `0.61961`  ·  corrupted: `-0.52318`  ·  n_sockets: `0.35888`  ·  quality: `0.04804`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.70635 |
| `explicit.stat_3033371881@T2` | -1.37117 |
| `explicit.stat_1011760251@T1` | -1.36293 |
| `explicit.stat_2339757871@T1` | -1.19487 |
| `explicit.stat_2901986750@T1` | -1.18920 |
| `explicit.stat_328541901@T2` | -1.09000 |
| `explicit.stat_2481353198@T1` | -1.08160 |
| `explicit.stat_328541901@T1` | -1.06725 |
| `explicit.stat_4095671657@T2` | -1.05988 |
| `explicit.stat_4095671657@T1` | -1.02972 |
| `explicit.stat_3321629045@T2` | -0.97503 |
| `explicit.stat_4052037485@T1` | -0.96532 |

### weapon.twomace — n=5586, R²=-0.422

intercept: `-11.0659`  ·  log_price: True  ·  ilvl: `0.15270`  ·  n_mods: `-0.24318`  ·  n_top_tier: `0.45585`  ·  corrupted: `0.71565`  ·  n_sockets: `0.21012`  ·  quality: `0.06467`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.44974 |
| `explicit.stat_1037193709@T1` | -1.69982 |
| `explicit.stat_3336890334@T1` | -1.48692 |
| `explicit.stat_1263695895@T2` | -1.20303 |
| `explicit.stat_9187492@T1` | -1.04566 |
| `explicit.stat_2694482655@T1` | 0.86000 |
| `explicit.stat_1263695895@T1` | -0.77579 |
| `explicit.stat_210067635@T1` | -0.73754 |
| `explicit.stat_3695891184@T1` | -0.63501 |
| `explicit.stat_3695891184@T2` | -0.63488 |
| `explicit.stat_1037193709@T2` | -0.62716 |
| `explicit.stat_518292764@T2` | -0.57969 |

## Coverage (listings per base)

- … **Sapphire** — 38821 listings (38756 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 37787 listings (37735 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 28961 listings (28929 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 13141 listings (13123 priced) [0.2–398916549611043.2 ex]
- … **Prismatic Ring** — 12148 listings (12122 priced) [0.2–398916549611043.2 ex]
- … **Solar Amulet** — 11836 listings (11810 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 11697 listings (11683 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10950 listings (10923 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10919 listings (10896 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 10372 listings (10359 priced) [0.3–398916549611043.2 ex]
- … **Sapphire Ring** — 9060 listings (9045 priced) [0.2–398916549611043.2 ex]
- … **Topaz Ring** — 8723 listings (8713 priced) [0.3–398916549611043.2 ex]
- … **Ruby Ring** — 8624 listings (8615 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7589 listings (7565 priced) [0.3–398916553600208.8 ex]
- … **Unset Ring** — 7483 listings (7461 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7449 listings (7441 priced) [0.3–398916549611043.2 ex]
- … **Jade Amulet** — 7387 listings (7371 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 7307 listings (7299 priced) [0.3–3985176410.3 ex]
- … **Pearl Ring** — 7245 listings (7236 priced) [0.2–398916549611043.2 ex]
- … **Plate Belt** — 7174 listings (7143 priced) [0.3–398916553600208.8 ex]
- … **Ancestral Tiara** — 7131 listings (7102 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 7083 listings (7071 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6773 listings (6769 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6683 listings (6668 priced) [0.3–398916549611043.2 ex]
- … **Heavy Belt** — 6358 listings (6344 priced) [0.3–398916553600208.8 ex]

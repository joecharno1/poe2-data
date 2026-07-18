# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-18T07:48:12+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **609696** (607873 priced in exalted)
- Distinct bases: 991 · distinct mods: 3236 · mod rows: 2887714
- Sold signals: **25032** sold · 346325 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-18T07:36:10+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×25.65** (median |log error| 3.2445)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 80% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×71.29 · ±30% 5% · n=88822
- Premium segment (60ex+): skill **+0.13** · typical error ×325.41 · ±30% 0% · n=60580

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 12714 | ×56.66 | 21% | +0.02 | +0.04 |
| jewel | 11912 | ×11.01 | 5% | +0.08 | +0.11 |
| accessory.amulet | 11576 | ×45.94 | 19% | +0.04 | +0.03 |
| accessory.belt | 8441 | ×24.75 | 13% | +0.09 | +0.12 |
| armour.chest | 8151 | ×18.76 | 21% | +0.08 | +0.10 |
| armour.helmet | 8007 | ×25.57 | 16% | +0.08 | +0.10 |
| armour.boots | 7447 | ×41.33 | 21% | +0.08 | +0.11 |
| armour.gloves | 7319 | ×43.72 | 17% | +0.07 | +0.10 |
| other | 7129 | ×2.00 | 43% | +0.10 | +0.17 |
| weapon.wand | 4430 | ×55.70 | 18% | +0.07 | +0.09 |
| weapon.bow | 3485 | ×32.10 | 13% | +0.14 | +0.15 |
| weapon.crossbow | 3251 | ×36.60 | 16% | +0.10 | +0.14 |
| weapon.warstaff | 2185 | ×32.05 | 7% | +0.17 | +0.14 |
| weapon.staff | 2041 | ×46.50 | 5% | +0.14 | +0.13 |
| weapon.sceptre | 2006 | ×34.01 | 5% | +0.20 | +0.19 |
| weapon.spear | 1592 | ×37.77 | 10% | +0.09 | +0.10 |
| armour.focus | 1323 | ×19.73 | 7% | +0.16 | +0.18 |
| armour.quiver | 1279 | ×26.21 | 6% | +0.15 | +0.15 |
| flask.charm | 1059 | ×22.00 | 31% | +0.01 | +0.04 |
| armour.shield | 1048 | ×25.53 | 8% | +0.07 | +0.10 |
| weapon.twomace | 939 | ×9.68 | 9% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=64940, R²=-0.945

intercept: `-1.8544`  ·  log_price: True  ·  ilvl: `0.02568`  ·  n_mods: `0.87488`  ·  n_top_tier: `-0.34922`  ·  corrupted: `0.24723`  ·  quality: `0.22442`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.45419 |
| `explicit.stat_3374165039@T1` | -2.20462 |
| `explicit.stat_2523933828@T1` | -1.83664 |
| `explicit.stat_3485067555@T1` | 1.78941 |
| `explicit.stat_318953428@T1` | -1.59374 |
| `explicit.stat_1805182458@T1` | -1.52187 |
| `explicit.stat_3166958180@T1` | -1.42275 |
| `explicit.stat_4147897060@T1` | -1.38697 |
| `explicit.stat_3174700878@T1` | 1.37636 |
| `explicit.stat_627767961@T1` | -1.36075 |
| `explicit.stat_239367161@T1` | -1.35164 |
| `explicit.stat_1062710370@T1` | -1.31443 |

### other — n=58366, R²=-0.5888

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `0.40730`  ·  corrupted: `0.28469`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | 1.33005 |
| `explicit.stat_1050105434@T1` | -0.36740 |
| `explicit.stat_2106365538@T1` | -0.35775 |
| `explicit.stat_3141070085@T1` | -0.29156 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_3917489142@T1` | -0.21433 |
| `explicit.stat_2974417149@T1` | 0.20222 |
| `explicit.stat_3291658075@T1` | 0.19939 |
| `explicit.stat_789117908@T1` | -0.17798 |
| `explicit.stat_2482852589@T1` | -0.16234 |

### accessory.ring — n=57939, R²=-2.0428

intercept: `3.3672`  ·  log_price: True  ·  ilvl: `-0.04159`  ·  n_mods: `0.00049`  ·  n_top_tier: `1.08014`  ·  corrupted: `0.01746`  ·  n_sockets: `-0.05950`  ·  quality: `0.00325`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.11935 |
| `explicit.stat_1573130764@T2` | -1.11748 |
| `explicit.stat_2231156303@T1` | -1.11394 |
| `explicit.stat_4220027924@T2` | -1.10364 |
| `explicit.stat_789117908@T1` | -1.09806 |
| `explicit.stat_789117908@T2` | -1.09792 |
| `explicit.stat_803737631@T1` | -1.09628 |
| `explicit.stat_4080418644@T1` | -1.09374 |
| `explicit.stat_2923486259@T2` | -1.09361 |
| `explicit.stat_2144192055@T1` | -1.09357 |
| `explicit.stat_3291658075@T2` | -1.09261 |
| `explicit.stat_3032590688@T2` | -1.09256 |

### accessory.amulet — n=52726, R²=-2.1647

intercept: `3.7007`  ·  log_price: True  ·  ilvl: `-0.04526`  ·  n_mods: `-0.01952`  ·  n_top_tier: `1.18134`  ·  corrupted: `0.03197`  ·  n_sockets: `-0.12827`  ·  quality: `0.00720`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.53709 |
| `explicit.stat_3299347043@T2` | -1.34901 |
| `explicit.stat_2974417149@T2` | -1.24459 |
| `explicit.stat_587431675@T2` | -1.24296 |
| `explicit.stat_2974417149@T1` | -1.23892 |
| `explicit.stat_472520716@T2` | -1.23713 |
| `explicit.stat_803737631@T1` | -1.23556 |
| `explicit.stat_2866361420@T2` | -1.23395 |
| `explicit.stat_1050105434@T2` | -1.21877 |
| `explicit.stat_2866361420@T1` | -1.21863 |
| `explicit.stat_803737631@T2` | -1.21635 |
| `explicit.stat_1671376347@T2` | -1.21413 |

### accessory.belt — n=38940, R²=-1.3527

intercept: `5.1382`  ·  log_price: True  ·  ilvl: `-0.05847`  ·  n_mods: `-0.08150`  ·  n_top_tier: `0.68670`  ·  corrupted: `1.27786`  ·  n_sockets: `-0.00480`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.55931 |
| `explicit.stat_2923486259@T1` | 0.93835 |
| `explicit.stat_3299347043@T2` | -0.91988 |
| `explicit.stat_2881298780@T1` | -0.82189 |
| `explicit.stat_4220027924@T2` | -0.76647 |
| `explicit.stat_51994685@T1` | -0.74581 |
| `explicit.stat_644456512@T1` | -0.72236 |
| `explicit.stat_809229260@T2` | -0.71920 |
| `explicit.stat_3325883026@T1` | -0.71908 |
| `explicit.stat_1570770415@T2` | -0.71658 |
| `explicit.stat_1389754388@T1` | -0.71273 |
| `explicit.stat_915769802@T2` | -0.69294 |

### armour.chest — n=38661, R²=-1.7042

intercept: `3.3874`  ·  log_price: True  ·  ilvl: `-0.04155`  ·  n_mods: `-0.02485`  ·  n_top_tier: `0.50522`  ·  corrupted: `0.17300`  ·  n_sockets: `0.03096`  ·  quality: `0.06091`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.66479 |
| `explicit.stat_3981240776@T1` | 0.62906 |
| `explicit.stat_986397080@T2` | -0.60809 |
| `explicit.stat_986397080@T1` | -0.56962 |
| `explicit.stat_3484657501@T1` | -0.55259 |
| `explicit.stat_2339757871@T2` | -0.54917 |
| `explicit.stat_915769802@T2` | -0.54683 |
| `explicit.stat_3299347043@T2` | -0.54178 |
| `explicit.stat_4080418644@T1` | -0.53838 |
| `explicit.stat_1692879867@T2` | -0.53813 |
| `explicit.stat_915769802@T1` | -0.53560 |
| `explicit.stat_124859000@T1` | -0.53558 |

### armour.helmet — n=37565, R²=-1.5855

intercept: `3.4303`  ·  log_price: True  ·  ilvl: `-0.04342`  ·  n_mods: `-0.02833`  ·  n_top_tier: `0.45618`  ·  corrupted: `0.70211`  ·  n_sockets: `0.07368`  ·  quality: `0.05663`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.01584 |
| `crafted.stat_3917489142@T1` | -2.25815 |
| `explicit.stat_3917489142@T2` | -0.92245 |
| `explicit.stat_3917489142@T1` | -0.83031 |
| `explicit.stat_1263695895@T1` | -0.62646 |
| `explicit.stat_2162097452@T2` | -0.62210 |
| `explicit.stat_4052037485@T2` | -0.58828 |
| `explicit.stat_1999113824@T1` | -0.58227 |
| `explicit.stat_2162097452@T1` | 0.53663 |
| `explicit.stat_803737631@T1` | -0.53584 |
| `explicit.stat_1263695895@T2` | -0.53402 |
| `explicit.stat_803737631@T2` | -0.52965 |

### armour.boots — n=34944, R²=-1.7364

intercept: `3.3161`  ·  log_price: True  ·  ilvl: `-0.04078`  ·  n_mods: `-0.01766`  ·  n_top_tier: `0.70053`  ·  corrupted: `-0.00475`  ·  n_sockets: `0.02072`  ·  quality: `0.06306`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.47365 |
| `crafted.stat_3917489142@T1` | 1.24816 |
| `explicit.stat_3917489142@T2` | -0.87202 |
| `explicit.stat_2339757871@T1` | -0.86774 |
| `explicit.stat_3299347043@T1` | -0.84568 |
| `explicit.stat_3917489142@T1` | -0.78779 |
| `explicit.stat_2923486259@T2` | -0.74264 |
| `explicit.stat_1062208444@T2` | -0.73878 |
| `explicit.stat_2160282525@T1` | -0.73727 |
| `explicit.stat_1874553720@T1` | -0.72988 |
| `explicit.stat_3299347043@T2` | -0.72874 |
| `explicit.stat_4052037485@T2` | -0.72230 |

### armour.gloves — n=34085, R²=-1.8131

intercept: `3.7346`  ·  log_price: True  ·  ilvl: `-0.04725`  ·  n_mods: `-0.01929`  ·  n_top_tier: `0.59441`  ·  corrupted: `-0.00359`  ·  n_sockets: `0.06329`  ·  quality: `0.05049`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.96552 |
| `rune.stat_201332984` | 1.61421 |
| `rune.stat_836936635` | 1.20629 |
| `explicit.stat_1671376347@T1` | 1.00048 |
| `explicit.stat_2923486259@T1` | -0.88150 |
| `explicit.stat_9187492@T2` | -0.85794 |
| `explicit.stat_9187492@T1` | 0.82578 |
| `explicit.stat_3484657501@T2` | -0.80112 |
| `explicit.stat_3484657501@T1` | -0.73321 |
| `explicit.stat_3321629045@T2` | -0.73298 |
| `explicit.stat_2923486259@T2` | -0.69724 |
| `explicit.stat_803737631@T2` | -0.69406 |

### weapon.wand — n=20787, R²=-2.1632

intercept: `3.9134`  ·  log_price: True  ·  ilvl: `-0.04848`  ·  n_mods: `-0.02790`  ·  n_top_tier: `0.52463`  ·  corrupted: `-0.01288`  ·  n_sockets: `0.05019`  ·  quality: `0.00741`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.15959 |
| `rune.stat_124131830` | -2.81009 |
| `explicit.stat_2254480358@T1` | 2.49750 |
| `explicit.stat_124131830@T1` | 2.01731 |
| `explicit.stat_4226189338@T1` | 1.83910 |
| `explicit.stat_591105508@T1` | 1.82167 |
| `explicit.stat_736967255@T2` | 1.69272 |
| `crafted.stat_124131830` | 1.30691 |
| `explicit.stat_2254480358@T2` | 0.88672 |
| `explicit.stat_2768835289@T2` | -0.83070 |
| `explicit.stat_1263695895@T1` | -0.82369 |
| `explicit.stat_1263695895@T2` | -0.80025 |

### weapon.bow — n=16649, R²=-1.811

intercept: `3.9882`  ·  log_price: True  ·  ilvl: `-0.04584`  ·  n_mods: `-0.11711`  ·  n_top_tier: `0.62706`  ·  corrupted: `0.25058`  ·  n_sockets: `0.06724`  ·  quality: `0.03272`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.35465 |
| `desecrated.stat_666077204@T1` | -1.34287 |
| `desecrated.stat_210067635@T1` | -1.27540 |
| `explicit.stat_1202301673@T1` | 1.12021 |
| `explicit.stat_2463230181@T1` | -1.04962 |
| `explicit.stat_1263695895@T1` | -1.00583 |
| `explicit.stat_518292764@T2` | -0.96564 |
| `explicit.stat_1263695895@T2` | -0.91719 |
| `explicit.stat_3695891184@T2` | -0.86064 |
| `explicit.stat_3695891184@T1` | -0.82682 |
| `explicit.stat_3336890334@T1` | 0.80340 |
| `explicit.stat_1509134228@T1` | -0.78424 |

### flask.charm — n=16453, R²=-0.5934

intercept: `0.0850`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.80501`  ·  corrupted: `1.60838`  ·  quality: `0.00012`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.86006 |
| `explicit.stat_1056492907` | 2.98248 |
| `explicit.stat_828533480@T2` | -1.80504 |
| `explicit.stat_1873752457@T2` | -1.80500 |
| `explicit.stat_1120862500@T2` | -1.80500 |
| `explicit.stat_1873752457@T1` | -1.80498 |
| `explicit.stat_2676834156@T2` | -1.80497 |
| `explicit.stat_3196823591@T2` | -1.80497 |
| `explicit.stat_2365392475@T2` | -1.80496 |
| `explicit.stat_388617051@T2` | -1.80487 |
| `explicit.stat_828533480@T1` | -1.80408 |
| `explicit.stat_1366840608@T2` | -1.80404 |

### weapon.crossbow — n=15609, R²=-1.8147

intercept: `3.8685`  ·  log_price: True  ·  ilvl: `-0.04671`  ·  n_mods: `-0.06622`  ·  n_top_tier: `0.65503`  ·  corrupted: `0.04509`  ·  n_sockets: `0.05794`  ·  quality: `0.02229`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.78622 |
| `explicit.stat_2250681686@T2` | -1.30348 |
| `explicit.stat_1980802737` | 1.24886 |
| `explicit.stat_1202301673@T1` | 1.10542 |
| `explicit.stat_2250681686` | 0.84175 |
| `explicit.stat_1509134228@T2` | -0.83560 |
| `explicit.stat_2694482655@T1` | -0.82064 |
| `explicit.stat_1263695895@T2` | -0.81968 |
| `explicit.stat_1037193709@T1` | -0.80539 |
| `crafted.stat_3035140377` | 0.78953 |
| `explicit.stat_1202301673@T2` | -0.78070 |
| `explicit.stat_1940865751@T2` | -0.77300 |

### weapon.warstaff — n=10310, R²=-0.3479

intercept: `-10.7726`  ·  log_price: True  ·  ilvl: `0.14788`  ·  n_mods: `-0.25834`  ·  n_top_tier: `0.20426`  ·  corrupted: `0.30080`  ·  n_sockets: `0.18620`  ·  quality: `0.06079`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 1.84653 |
| `desecrated.stat_2231156303@T1` | 1.84653 |
| `desecrated.stat_3291658075@T1` | -1.64119 |
| `desecrated.stat_473429811@T1` | -1.64119 |
| `crafted.stat_210067635@T2` | 1.42633 |
| `rune.stat_243313994` | 0.94764 |
| `explicit.stat_1509134228@T1` | 0.87963 |
| `explicit.stat_328541901@T1` | -0.80304 |
| `explicit.stat_328541901@T2` | -0.75570 |
| `desecrated.stat_9187492` | 0.73108 |
| `explicit.stat_9187492@T1` | 0.66591 |
| `explicit.stat_748522257@T2` | 0.63170 |

### weapon.staff — n=9656, R²=-0.3745

intercept: `-15.7046`  ·  log_price: True  ·  ilvl: `0.20387`  ·  n_mods: `-0.16396`  ·  n_top_tier: `0.61939`  ·  corrupted: `0.57849`  ·  n_sockets: `0.22497`  ·  quality: `0.03699`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.09957 |
| `explicit.stat_1545858329@T1` | 1.97935 |
| `explicit.stat_293638271@T2` | -1.59869 |
| `explicit.stat_591105508@T1` | 1.40300 |
| `explicit.stat_124131830@T1` | 1.22507 |
| `explicit.stat_2254480358@T2` | 1.08436 |
| `explicit.stat_1600707273@T1` | 0.87430 |
| `explicit.stat_274716455@T1` | -0.85387 |
| `explicit.stat_3695891184@T1` | -0.81571 |
| `explicit.stat_2968503605@T1` | -0.77905 |
| `explicit.stat_293638271@T1` | -0.75647 |
| `rune.stat_124131830` | 0.71455 |

### weapon.sceptre — n=9529, R²=-0.3268

intercept: `-21.0636`  ·  log_price: True  ·  ilvl: `0.27124`  ·  n_mods: `-0.02734`  ·  n_top_tier: `-0.01023`  ·  corrupted: `0.39734`  ·  n_sockets: `0.28626`  ·  quality: `0.02868`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.95448 |
| `explicit.stat_1250712710@T2` | 1.77527 |
| `explicit.stat_2162097452@T2` | 1.70488 |
| `explicit.stat_3057012405@T1` | 1.48341 |
| `explicit.stat_101878827@T1` | 1.06301 |
| `explicit.stat_101878827@T2` | 0.90382 |
| `explicit.stat_1798257884@T2` | 0.79305 |
| `explicit.stat_2347036682@T1` | 0.67062 |
| `explicit.stat_849987426@T1` | 0.65266 |
| `explicit.stat_1250712710@T1` | 0.64604 |
| `explicit.stat_1998951374@T2` | 0.59062 |
| `explicit.stat_4080418644@T1` | 0.59006 |

### weapon.spear — n=7739, R²=-0.4043

intercept: `-12.6054`  ·  log_price: True  ·  ilvl: `0.17576`  ·  n_mods: `-0.18456`  ·  n_top_tier: `0.64281`  ·  corrupted: `0.01156`  ·  n_sockets: `0.20497`  ·  quality: `0.05422`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.41442 |
| `explicit.stat_1202301673@T1` | 1.47819 |
| `explicit.stat_9187492@T1` | 1.41686 |
| `crafted.stat_3035140377` | 1.09129 |
| `desecrated.stat_210067635@T1` | -1.08433 |
| `explicit.stat_4080418644@T2` | -0.99264 |
| `explicit.stat_1509134228@T1` | 0.93666 |
| `explicit.stat_709508406@T1` | 0.89036 |
| `explicit.stat_3261801346@T1` | -0.82561 |
| `explicit.stat_9187492@T2` | -0.82547 |
| `explicit.stat_3695891184@T2` | -0.76088 |
| `explicit.stat_748522257@T2` | -0.75968 |

### armour.focus — n=6351, R²=-0.3544

intercept: `-14.3449`  ·  log_price: True  ·  ilvl: `0.18681`  ·  n_mods: `-0.15843`  ·  n_top_tier: `0.85274`  ·  corrupted: `0.40640`  ·  n_sockets: `0.47713`  ·  quality: `0.05768`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 1.45839 |
| `explicit.stat_4220027924@T2` | -1.38866 |
| `explicit.stat_4220027924@T1` | -1.32445 |
| `explicit.stat_2231156303@T2` | -1.27697 |
| `explicit.stat_2923486259@T1` | -1.16299 |
| `explicit.stat_2891184298@T1` | -0.98420 |
| `explicit.stat_2231156303@T1` | -0.96833 |
| `explicit.stat_736967255@T2` | -0.93563 |
| `explicit.stat_2974417149@T1` | -0.86651 |
| `explicit.stat_737908626@T2` | -0.86581 |
| `explicit.stat_2339757871@T2` | -0.82639 |
| `explicit.stat_2974417149@T2` | -0.80516 |

### armour.quiver — n=5953, R²=-0.3083

intercept: `-14.6540`  ·  log_price: True  ·  ilvl: `0.18130`  ·  n_mods: `-0.11458`  ·  n_top_tier: `0.81296`  ·  corrupted: `0.64581`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.18862 |
| `explicit.stat_2463230181@T1` | 3.15652 |
| `explicit.stat_2463230181@T2` | 1.61659 |
| `explicit.stat_1573130764@T1` | -1.31801 |
| `explicit.stat_681332047@T2` | -1.21529 |
| `explicit.stat_2321178454@T2` | -0.94345 |
| `explicit.stat_803737631@T2` | -0.93157 |
| `explicit.stat_4067062424@T1` | -0.89668 |
| `explicit.stat_803737631@T1` | -0.86523 |
| `explicit.stat_2194114101@T2` | -0.80300 |
| `explicit.stat_1573130764@T2` | -0.78049 |
| `explicit.stat_4067062424@T2` | -0.74889 |

### armour.shield — n=5174, R²=-0.4453

intercept: `-12.4914`  ·  log_price: True  ·  ilvl: `0.16607`  ·  n_mods: `-0.09722`  ·  n_top_tier: `0.63002`  ·  corrupted: `-0.32636`  ·  n_sockets: `0.32700`  ·  quality: `0.06830`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.35208 |
| `explicit.stat_3321629045@T2` | -1.27434 |
| `explicit.stat_4095671657@T1` | -1.17031 |
| `explicit.stat_2923486259@T2` | -1.06136 |
| `explicit.stat_4095671657@T2` | -1.03788 |
| `explicit.stat_2923486259@T1` | -0.99255 |
| `explicit.stat_1301765461@T1` | 0.94045 |
| `explicit.stat_3484657501@T2` | -0.93203 |
| `explicit.stat_3855016469@T1` | -0.92958 |
| `explicit.stat_328541901@T1` | -0.84802 |
| `explicit.stat_3033371881@T2` | -0.83426 |
| `explicit.stat_3261801346@T1` | -0.83047 |

### weapon.twomace — n=4735, R²=-0.4525

intercept: `-9.7556`  ·  log_price: True  ·  ilvl: `0.13697`  ·  n_mods: `-0.24386`  ·  n_top_tier: `0.27546`  ·  corrupted: `-0.01970`  ·  n_sockets: `0.16735`  ·  quality: `0.05572`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.47404 |
| `desecrated.stat_1509134228@T1` | 1.90518 |
| `explicit.stat_1037193709@T1` | -1.42555 |
| `explicit.stat_3336890334@T1` | -1.00401 |
| `explicit.stat_9187492@T1` | -0.76743 |
| `crafted.stat_3035140377` | 0.76701 |
| `explicit.stat_387439868@T2` | -0.72388 |
| `explicit.stat_1263695895@T2` | -0.67939 |
| `explicit.stat_210067635@T2` | 0.60001 |
| `explicit.stat_3695891184@T1` | -0.56121 |
| `explicit.stat_691932474@T1` | -0.54894 |
| `explicit.stat_1037193709@T2` | -0.52803 |

## Coverage (listings per base)

- … **Sapphire** — 30125 listings (30074 priced) [0.3–885594757.8 ex]
- … **Emerald** — 29395 listings (29354 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 22491 listings (22464 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11132 listings (11117 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 9873 listings (9852 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 9539 listings (9516 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9405 listings (9397 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8907 listings (8890 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8770 listings (8751 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8540 listings (8528 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7304 listings (7293 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7019 listings (7013 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6956 listings (6950 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6665 listings (6644 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6141 listings (6134 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 6065 listings (6038 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 6032 listings (6015 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6010 listings (5999 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 5989 listings (5982 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5924 listings (5898 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5844 listings (5835 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5763 listings (5756 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5485 listings (5482 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5463 listings (5451 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5371 listings (5362 priced) [0.3–398912568423.8 ex]

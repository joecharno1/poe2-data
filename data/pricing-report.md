# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-18T20:05:57+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **627793** (625884 priced in exalted)
- Distinct bases: 993 · distinct mods: 3256 · mod rows: 2973109
- Sold signals: **24848** sold · 357361 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-18T19:53:44+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.36** (median |log error| 3.1071)
- Within ±30% of asking price: **13%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×54.21 · ±30% 5% · n=91312
- Premium segment (60ex+): skill **+0.13** · typical error ×203.22 · ±30% 0% · n=62066

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 13134 | ×56.99 | 21% | +0.03 | +0.05 |
| jewel | 12365 | ×10.94 | 4% | +0.09 | +0.12 |
| accessory.amulet | 11950 | ×50.44 | 19% | +0.04 | +0.04 |
| accessory.belt | 8692 | ×14.04 | 5% | +0.02 | +0.04 |
| armour.chest | 8419 | ×13.42 | 5% | +0.05 | +0.08 |
| armour.helmet | 8276 | ×15.23 | 5% | +0.06 | +0.09 |
| armour.boots | 7636 | ×29.36 | 12% | +0.13 | +0.14 |
| armour.gloves | 7506 | ×27.85 | 8% | +0.13 | +0.14 |
| other | 7320 | ×5.30 | 41% | +0.09 | +0.15 |
| weapon.wand | 4538 | ×45.53 | 15% | +0.09 | +0.11 |
| weapon.bow | 3538 | ×28.14 | 13% | +0.14 | +0.15 |
| weapon.crossbow | 3344 | ×31.03 | 13% | +0.11 | +0.15 |
| weapon.warstaff | 2242 | ×22.27 | 6% | +0.19 | +0.19 |
| weapon.staff | 2083 | ×30.90 | 5% | +0.16 | +0.14 |
| weapon.sceptre | 2083 | ×28.81 | 5% | +0.16 | +0.16 |
| weapon.spear | 1631 | ×29.84 | 9% | +0.10 | +0.11 |
| armour.focus | 1375 | ×17.43 | 7% | +0.11 | +0.11 |
| armour.quiver | 1311 | ×23.01 | 8% | +0.16 | +0.17 |
| armour.shield | 1082 | ×18.94 | 8% | +0.08 | +0.10 |
| flask.charm | 1060 | ×19.98 | 29% | +0.00 | +0.03 |
| weapon.twomace | 997 | ×7.73 | 9% | +0.09 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=67420, R²=-0.9433

intercept: `-1.9177`  ·  log_price: True  ·  ilvl: `0.02582`  ·  n_mods: `0.87069`  ·  n_top_tier: `-0.33193`  ·  corrupted: `0.30171`  ·  quality: `-0.00241`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.15093 |
| `explicit.stat_3374165039@T1` | -2.32577 |
| `explicit.stat_3485067555@T1` | 2.00630 |
| `explicit.stat_3780644166@T1` | -1.76721 |
| `explicit.stat_2523933828@T1` | -1.65670 |
| `explicit.stat_21071013@T1` | 1.64293 |
| `explicit.stat_4147897060@T1` | -1.62947 |
| `explicit.stat_1805182458@T1` | -1.55485 |
| `explicit.stat_318953428@T1` | -1.44037 |
| `explicit.stat_1697447343@T1` | -1.41278 |
| `explicit.stat_1315743832@T1` | -1.29387 |
| `explicit.stat_239367161@T1` | -1.29328 |

### other — n=59976, R²=-0.5866

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.41145`  ·  corrupted: `0.30414`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.42791 |
| `explicit.stat_3299347043@T1` | -0.38874 |
| `explicit.stat_3291658075@T1` | -0.24667 |
| `explicit.stat_3141070085@T1` | -0.24469 |
| `implicit.stat_2219129443` | 0.23041 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_2106365538@T1` | -0.22442 |
| `explicit.stat_3917489142@T1` | 0.20157 |
| `explicit.stat_736967255@T1` | 0.16660 |
| `explicit.stat_789117908@T1` | -0.16302 |
| `explicit.stat_2231156303@T1` | -0.13150 |

### accessory.ring — n=59951, R²=-2.0346

intercept: `3.4054`  ·  log_price: True  ·  ilvl: `-0.04200`  ·  n_mods: `-0.00057`  ·  n_top_tier: `1.08886`  ·  corrupted: `0.02248`  ·  n_sockets: `0.16652`  ·  quality: `0.01698`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -1.12082 |
| `explicit.stat_1573130764@T1` | -1.11944 |
| `explicit.stat_1573130764@T2` | -1.11896 |
| `explicit.stat_803737631@T1` | -1.11384 |
| `explicit.stat_3325883026@T1` | -1.11209 |
| `explicit.stat_1263695895@T2` | -1.11138 |
| `explicit.stat_4220027924@T2` | -1.11050 |
| `explicit.stat_1263695895@T1` | -1.11024 |
| `explicit.stat_2923486259@T2` | -1.10248 |
| `explicit.stat_4080418644@T1` | -1.10241 |
| `explicit.stat_789117908@T2` | -1.10175 |
| `explicit.stat_2144192055@T1` | -1.09957 |

### accessory.amulet — n=54422, R²=-2.1724

intercept: `3.7971`  ·  log_price: True  ·  ilvl: `-0.04642`  ·  n_mods: `-0.01871`  ·  n_top_tier: `1.38850`  ·  corrupted: `0.05197`  ·  n_sockets: `-0.15235`  ·  quality: `0.00593`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.82889 |
| `explicit.stat_3299347043@T2` | -1.61804 |
| `explicit.stat_2974417149@T1` | -1.47054 |
| `explicit.stat_587431675@T2` | -1.45963 |
| `explicit.stat_2974417149@T2` | -1.45121 |
| `explicit.stat_803737631@T1` | -1.44082 |
| `explicit.stat_2866361420@T1` | -1.43282 |
| `explicit.stat_2866361420@T2` | -1.43267 |
| `explicit.stat_472520716@T2` | -1.42928 |
| `explicit.stat_1050105434@T2` | -1.42913 |
| `explicit.stat_803737631@T2` | -1.42364 |
| `explicit.stat_1671376347@T2` | -1.42085 |

### accessory.belt — n=39984, R²=-0.5953

intercept: `6.8044`  ·  log_price: True  ·  ilvl: `-0.05281`  ·  n_mods: `-0.43517`  ·  n_top_tier: `0.77672`  ·  corrupted: `0.99448`  ·  n_sockets: `0.03192`

| stat_id | coef |
|---|---|
| `explicit.stat_2881298780@T1` | -1.17903 |
| `explicit.stat_3299347043@T1` | -1.03530 |
| `explicit.stat_51994685@T1` | -1.01526 |
| `explicit.stat_644456512@T1` | -1.01422 |
| `explicit.stat_1389754388@T1` | -0.93316 |
| `explicit.stat_3299347043@T2` | -0.92436 |
| `explicit.stat_3325883026@T1` | -0.91134 |
| `explicit.stat_3372524247@T2` | -0.89214 |
| `explicit.stat_1570770415@T2` | -0.89020 |
| `explicit.stat_809229260@T1` | -0.87636 |
| `explicit.stat_809229260@T2` | -0.87232 |
| `explicit.stat_2923486259@T1` | -0.83254 |

### armour.chest — n=39637, R²=-1.0014

intercept: `4.0768`  ·  log_price: True  ·  ilvl: `-0.04436`  ·  n_mods: `-0.14809`  ·  n_top_tier: `0.37923`  ·  corrupted: `0.19757`  ·  n_sockets: `0.18510`  ·  quality: `0.03932`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.81961 |
| `explicit.stat_986397080@T2` | -0.70260 |
| `explicit.stat_2339757871@T2` | -0.66275 |
| `explicit.stat_1692879867@T2` | -0.65972 |
| `explicit.stat_3484657501@T1` | -0.61673 |
| `explicit.stat_3301100256@T2` | -0.61615 |
| `explicit.stat_915769802@T2` | -0.58514 |
| `explicit.stat_3299347043@T2` | -0.58355 |
| `explicit.stat_986397080@T1` | -0.55732 |
| `explicit.stat_4080418644@T2` | -0.55260 |
| `explicit.stat_915769802@T1` | -0.52885 |
| `explicit.stat_1692879867@T1` | -0.51733 |

### armour.helmet — n=38581, R²=-0.8945

intercept: `3.5711`  ·  log_price: True  ·  ilvl: `-0.04351`  ·  n_mods: `-0.10551`  ·  n_top_tier: `0.46428`  ·  corrupted: `0.69394`  ·  n_sockets: `0.14821`  ·  quality: `0.04051`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | -3.23884 |
| `explicit.stat_2339757871@T1` | -1.84068 |
| `explicit.stat_3917489142@T2` | -1.21529 |
| `explicit.stat_1999113824@T1` | -0.94821 |
| `explicit.stat_3321629045@T2` | -0.75491 |
| `explicit.stat_2451402625@T2` | -0.73735 |
| `explicit.stat_3917489142@T1` | -0.73639 |
| `explicit.stat_803737631@T2` | -0.72581 |
| `explicit.stat_1263695895@T1` | -0.71546 |
| `explicit.stat_1999113824@T2` | -0.64880 |
| `explicit.stat_2162097452@T2` | -0.64264 |
| `explicit.stat_4052037485@T2` | -0.60000 |

### armour.boots — n=35870, R²=-1.3544

intercept: `4.2546`  ·  log_price: True  ·  ilvl: `-0.05124`  ·  n_mods: `-0.07132`  ·  n_top_tier: `0.58914`  ·  corrupted: `-0.01581`  ·  n_sockets: `0.11241`  ·  quality: `0.05470`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.54970 |
| `explicit.stat_2339757871@T1` | -1.48219 |
| `crafted.stat_3917489142@T1` | 1.28913 |
| `explicit.stat_3299347043@T1` | -0.93578 |
| `explicit.stat_3917489142@T2` | -0.89633 |
| `explicit.stat_2923486259@T2` | -0.84996 |
| `explicit.stat_3484657501@T2` | -0.73612 |
| `explicit.stat_2160282525@T1` | -0.72242 |
| `explicit.stat_1062208444@T2` | -0.72098 |
| `explicit.stat_1999113824@T2` | -0.71508 |
| `explicit.stat_1874553720@T1` | -0.71439 |
| `explicit.stat_4052037485@T2` | -0.67925 |

### armour.gloves — n=34948, R²=-1.2828

intercept: `3.8629`  ·  log_price: True  ·  ilvl: `-0.04906`  ·  n_mods: `-0.07671`  ·  n_top_tier: `0.64162`  ·  corrupted: `0.05936`  ·  n_sockets: `0.22500`  ·  quality: `0.03951`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.78910 |
| `explicit.stat_2923486259@T1` | -1.28368 |
| `explicit.stat_3484657501@T2` | -1.20704 |
| `explicit.stat_3484657501@T1` | -1.10562 |
| `explicit.stat_3321629045@T2` | -0.99428 |
| `explicit.stat_803737631@T2` | -0.92110 |
| `explicit.stat_803737631@T1` | -0.87148 |
| `explicit.stat_2797971005@T2` | -0.79813 |
| `explicit.stat_3917489142@T2` | -0.79245 |
| `explicit.stat_9187492@T2` | -0.77846 |
| `explicit.stat_124859000@T2` | -0.76712 |
| `explicit.stat_9187492@T1` | 0.76697 |

### weapon.wand — n=21228, R²=-1.9842

intercept: `3.8312`  ·  log_price: True  ·  ilvl: `-0.04741`  ·  n_mods: `-0.04824`  ·  n_top_tier: `0.44922`  ·  corrupted: `-0.00378`  ·  n_sockets: `0.06524`  ·  quality: `0.01591`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.02399 |
| `rune.stat_124131830` | -2.45812 |
| `explicit.stat_2254480358@T1` | 2.40754 |
| `explicit.stat_124131830@T1` | 2.12929 |
| `explicit.stat_4226189338@T1` | 1.98352 |
| `explicit.stat_591105508@T1` | 1.87602 |
| `explicit.stat_736967255@T2` | 1.61935 |
| `explicit.stat_1600707273@T1` | 1.26924 |
| `crafted.stat_124131830` | 1.22620 |
| `explicit.stat_2768835289@T2` | -1.01706 |
| `explicit.stat_2254480358@T2` | 0.97072 |
| `explicit.stat_4226189338@T2` | 0.96844 |

### flask.charm — n=17149, R²=-0.6067

intercept: `0.1016`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.60944`  ·  corrupted: `1.60594`  ·  quality: `0.00085`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.77929 |
| `explicit.stat_1056492907` | 2.71902 |
| `explicit.stat_828533480@T2` | -1.60948 |
| `explicit.stat_1120862500@T2` | -1.60945 |
| `explicit.stat_1873752457@T2` | -1.60944 |
| `explicit.stat_388617051@T2` | -1.60943 |
| `explicit.stat_1873752457@T1` | -1.60942 |
| `explicit.stat_3196823591@T2` | -1.60941 |
| `explicit.stat_2365392475@T2` | -1.60940 |
| `explicit.stat_2676834156@T2` | -1.60939 |
| `explicit.stat_828533480@T1` | -1.60834 |
| `explicit.stat_1366840608@T2` | -1.60553 |

### weapon.bow — n=16970, R²=-1.7921

intercept: `3.9102`  ·  log_price: True  ·  ilvl: `-0.04422`  ·  n_mods: `-0.12844`  ·  n_top_tier: `0.67775`  ·  corrupted: `0.43269`  ·  n_sockets: `0.09575`  ·  quality: `0.03311`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.36899 |
| `desecrated.stat_666077204@T1` | -1.33482 |
| `desecrated.stat_210067635@T1` | -1.30593 |
| `explicit.stat_1263695895@T1` | -1.25313 |
| `explicit.stat_2463230181@T2` | -1.13969 |
| `explicit.stat_3336890334@T1` | 1.02117 |
| `explicit.stat_1263695895@T2` | -0.98978 |
| `explicit.stat_2463230181@T1` | -0.90830 |
| `explicit.stat_3695891184@T2` | -0.90560 |
| `explicit.stat_1509134228@T1` | -0.90409 |
| `explicit.stat_3695891184@T1` | -0.83569 |
| `explicit.stat_1037193709@T2` | -0.79888 |

### weapon.crossbow — n=15898, R²=-1.6828

intercept: `3.9505`  ·  log_price: True  ·  ilvl: `-0.04644`  ·  n_mods: `-0.10110`  ·  n_top_tier: `0.51390`  ·  corrupted: `0.04141`  ·  n_sockets: `0.09935`  ·  quality: `0.01866`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.67573 |
| `explicit.stat_1980802737` | 1.30478 |
| `explicit.stat_1202301673@T1` | 1.00271 |
| `explicit.stat_2250681686@T2` | -0.99914 |
| `explicit.stat_2250681686` | 0.85192 |
| `explicit.stat_709508406@T1` | 0.79934 |
| `rune.stat_731403740` | 0.78150 |
| `explicit.stat_1509134228@T2` | -0.72319 |
| `explicit.stat_3336890334@T2` | -0.71680 |
| `crafted.stat_3035140377` | 0.71544 |
| `explicit.stat_1940865751@T2` | -0.68954 |
| `explicit.stat_1263695895@T2` | -0.68218 |

### weapon.warstaff — n=10633, R²=-0.3581

intercept: `-10.0556`  ·  log_price: True  ·  ilvl: `0.13740`  ·  n_mods: `-0.23798`  ·  n_top_tier: `0.29120`  ·  corrupted: `0.39548`  ·  n_sockets: `0.16347`  ·  quality: `0.05655`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 2.86699 |
| `desecrated.stat_2527686725@T1` | 2.86699 |
| `desecrated.stat_3291658075@T1` | -1.79558 |
| `desecrated.stat_473429811@T1` | -1.79558 |
| `crafted.stat_210067635@T2` | 1.41080 |
| `rune.stat_243313994` | 0.83717 |
| `desecrated.stat_9187492` | 0.76780 |
| `explicit.stat_328541901@T1` | -0.69888 |
| `explicit.stat_328541901@T2` | -0.68235 |
| `explicit.stat_1509134228@T1` | 0.67170 |
| `explicit.stat_9187492@T1` | 0.66350 |
| `explicit.stat_1037193709@T1` | 0.61703 |

### weapon.staff — n=9992, R²=-0.388

intercept: `-15.8017`  ·  log_price: True  ·  ilvl: `0.20316`  ·  n_mods: `-0.13154`  ·  n_top_tier: `0.60140`  ·  corrupted: `0.55647`  ·  n_sockets: `0.19602`  ·  quality: `0.03572`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.92916 |
| `explicit.stat_591105508@T1` | 1.83109 |
| `explicit.stat_4226189338@T1` | 1.71899 |
| `explicit.stat_293638271@T2` | -1.54316 |
| `explicit.stat_124131830@T1` | 1.28798 |
| `explicit.stat_1600707273@T1` | 1.07962 |
| `explicit.stat_274716455@T1` | -0.88365 |
| `explicit.stat_3278136794@T1` | -0.71039 |
| `explicit.stat_2968503605@T1` | -0.69664 |
| `explicit.stat_1050105434@T2` | -0.67061 |
| `explicit.stat_591105508@T2` | 0.67041 |
| `explicit.stat_2505884597@T2` | -0.60949 |

### weapon.sceptre — n=9858, R²=-0.331

intercept: `-20.7855`  ·  log_price: True  ·  ilvl: `0.27012`  ·  n_mods: `-0.04309`  ·  n_top_tier: `0.16712`  ·  corrupted: `0.25766`  ·  n_sockets: `0.26463`  ·  quality: `0.02925`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.38612 |
| `explicit.stat_1250712710@T2` | 1.42529 |
| `explicit.stat_3057012405@T1` | 1.39227 |
| `explicit.stat_2162097452@T2` | 1.30197 |
| `explicit.stat_101878827@T1` | 0.77573 |
| `explicit.stat_101878827@T2` | 0.77315 |
| `explicit.stat_849987426@T1` | 0.73084 |
| `explicit.stat_1263695895@T2` | -0.65712 |
| `explicit.stat_2347036682@T2` | -0.57656 |
| `explicit.stat_289128254@T1` | 0.57441 |
| `explicit.stat_1798257884@T2` | 0.51252 |
| `explicit.stat_3850614073@T1` | 0.49642 |

### weapon.spear — n=7967, R²=-0.391

intercept: `-12.4216`  ·  log_price: True  ·  ilvl: `0.17421`  ·  n_mods: `-0.21873`  ·  n_top_tier: `0.63535`  ·  corrupted: `0.00837`  ·  n_sockets: `0.21645`  ·  quality: `0.08293`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.98724 |
| `explicit.stat_1202301673@T1` | 1.61508 |
| `explicit.stat_1509134228@T1` | 1.45453 |
| `explicit.stat_9187492@T1` | 1.27402 |
| `explicit.stat_4080418644@T2` | -1.18191 |
| `explicit.stat_1940865751@T2` | -1.01489 |
| `desecrated.stat_210067635@T1` | -1.00298 |
| `explicit.stat_4080418644@T1` | -0.95230 |
| `explicit.stat_709508406@T1` | 0.91003 |
| `explicit.stat_9187492@T2` | -0.89735 |
| `crafted.stat_3035140377` | 0.86362 |
| `explicit.stat_691932474@T2` | -0.84084 |

### armour.focus — n=6527, R²=-0.3502

intercept: `-13.7298`  ·  log_price: True  ·  ilvl: `0.17796`  ·  n_mods: `-0.20299`  ·  n_top_tier: `0.88403`  ·  corrupted: `0.45674`  ·  n_sockets: `0.41632`  ·  quality: `0.04814`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 1.76144 |
| `explicit.stat_4220027924@T1` | -1.48530 |
| `explicit.stat_2923486259@T1` | -1.47929 |
| `explicit.stat_4220027924@T2` | -1.35604 |
| `explicit.stat_2231156303@T2` | -1.19696 |
| `explicit.stat_2974417149@T1` | -1.17901 |
| `explicit.stat_2231156303@T1` | -1.12832 |
| `explicit.stat_2974417149@T2` | -1.11857 |
| `explicit.stat_3291658075@T1` | -0.99316 |
| `explicit.stat_2339757871@T2` | -0.89852 |
| `explicit.stat_737908626@T2` | -0.85594 |
| `explicit.stat_736967255@T2` | -0.84218 |

### armour.quiver — n=6120, R²=-0.3054

intercept: `-15.1621`  ·  log_price: True  ·  ilvl: `0.18477`  ·  n_mods: `-0.12550`  ·  n_top_tier: `0.83422`  ·  corrupted: `0.70816`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.02367 |
| `explicit.stat_2463230181@T1` | 2.57213 |
| `explicit.stat_681332047@T2` | -1.38468 |
| `explicit.stat_1573130764@T1` | -1.30930 |
| `explicit.stat_2463230181@T2` | 1.19836 |
| `explicit.stat_4067062424@T1` | -0.96379 |
| `explicit.stat_681332047@T1` | -0.93471 |
| `explicit.stat_2194114101@T2` | -0.92179 |
| `explicit.stat_803737631@T2` | -0.91909 |
| `explicit.stat_803737631@T1` | -0.91685 |
| `explicit.stat_1573130764@T2` | -0.89879 |
| `explicit.stat_4067062424@T2` | -0.88651 |

### armour.shield — n=5302, R²=-0.4545

intercept: `-12.7310`  ·  log_price: True  ·  ilvl: `0.16795`  ·  n_mods: `-0.06353`  ·  n_top_tier: `0.64543`  ·  corrupted: `-0.33054`  ·  n_sockets: `0.38690`  ·  quality: `0.07125`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.37416 |
| `explicit.stat_3321629045@T2` | -1.36917 |
| `explicit.stat_1301765461@T1` | 1.33352 |
| `explicit.stat_3855016469@T1` | -1.04472 |
| `explicit.stat_328541901@T1` | -1.00293 |
| `explicit.stat_3484657501@T2` | -0.99283 |
| `explicit.stat_3033371881@T2` | -0.97380 |
| `explicit.stat_4095671657@T1` | -0.89865 |
| `explicit.stat_2901986750@T1` | -0.89053 |
| `explicit.stat_2451402625@T1` | -0.81191 |
| `explicit.stat_2451402625@T2` | -0.78344 |
| `explicit.stat_3321629045@T1` | -0.77754 |

### weapon.twomace — n=4881, R²=-0.4491

intercept: `-10.5405`  ·  log_price: True  ·  ilvl: `0.14577`  ·  n_mods: `-0.20993`  ·  n_top_tier: `0.33125`  ·  corrupted: `0.09459`  ·  n_sockets: `0.13528`  ·  quality: `0.05797`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.09307 |
| `desecrated.stat_1509134228@T1` | 1.70065 |
| `explicit.stat_1037193709@T1` | -1.39839 |
| `explicit.stat_3336890334@T1` | -1.10359 |
| `explicit.stat_9187492@T1` | -0.80562 |
| `crafted.stat_3035140377` | 0.69155 |
| `explicit.stat_387439868@T2` | -0.67337 |
| `explicit.stat_1263695895@T2` | -0.66810 |
| `explicit.stat_1509134228@T1` | 0.65766 |
| `explicit.stat_210067635@T2` | 0.61876 |
| `explicit.stat_691932474@T1` | -0.60206 |
| `explicit.stat_3695891184@T1` | -0.54134 |

## Coverage (listings per base)

- … **Sapphire** — 31301 listings (31247 priced) [0.3–885594757.8 ex]
- … **Emerald** — 30443 listings (30402 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 23274 listings (23244 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11401 listings (11386 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10194 listings (10172 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 9864 listings (9840 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9713 listings (9703 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 9188 listings (9169 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9080 listings (9060 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8761 listings (8748 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7549 listings (7535 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7287 listings (7279 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7179 listings (7172 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6805 listings (6784 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6323 listings (6316 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 6242 listings (6214 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 6223 listings (6206 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6208 listings (6196 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6176 listings (6169 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6127 listings (6100 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6037 listings (6028 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5950 listings (5943 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5663 listings (5660 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5604 listings (5591 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5510 listings (5501 priced) [0.3–398912568423.8 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-18T13:58:35+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **618339** (616483 priced in exalted)
- Distinct bases: 992 · distinct mods: 3241 · mod rows: 2928120
- Sold signals: **24934** sold · 351608 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-18T13:46:00+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×23.89** (median |log error| 3.1733)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.15** · typical error ×67.53 · ±30% 5% · n=90053
- Premium segment (60ex+): skill **+0.15** · typical error ×296.04 · ±30% 0% · n=61360

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 12891 | ×54.23 | 21% | +0.03 | +0.05 |
| jewel | 12087 | ×10.53 | 5% | +0.08 | +0.11 |
| accessory.amulet | 11751 | ×45.60 | 19% | +0.04 | +0.04 |
| accessory.belt | 8591 | ×20.77 | 8% | +0.11 | +0.13 |
| armour.chest | 8282 | ×19.34 | 18% | +0.09 | +0.10 |
| armour.helmet | 8166 | ×23.45 | 11% | +0.10 | +0.12 |
| armour.boots | 7575 | ×38.28 | 20% | +0.10 | +0.12 |
| armour.gloves | 7419 | ×39.47 | 15% | +0.08 | +0.12 |
| other | 7217 | ×1.95 | 43% | +0.10 | +0.17 |
| weapon.wand | 4465 | ×46.31 | 15% | +0.09 | +0.11 |
| weapon.bow | 3530 | ×29.81 | 13% | +0.14 | +0.15 |
| weapon.crossbow | 3304 | ×34.53 | 14% | +0.10 | +0.15 |
| weapon.warstaff | 2208 | ×27.85 | 6% | +0.18 | +0.16 |
| weapon.staff | 2042 | ×40.23 | 5% | +0.14 | +0.14 |
| weapon.sceptre | 2028 | ×30.05 | 5% | +0.20 | +0.21 |
| weapon.spear | 1620 | ×31.79 | 9% | +0.10 | +0.11 |
| armour.focus | 1353 | ×17.89 | 7% | +0.16 | +0.17 |
| armour.quiver | 1296 | ×26.21 | 7% | +0.16 | +0.17 |
| armour.shield | 1062 | ×22.34 | 8% | +0.07 | +0.10 |
| flask.charm | 1057 | ×18.03 | 30% | +0.01 | +0.03 |
| weapon.twomace | 976 | ×8.40 | 10% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=66161, R²=-0.9557

intercept: `-1.8488`  ·  log_price: True  ·  ilvl: `0.02506`  ·  n_mods: `0.87459`  ·  n_top_tier: `-0.33789`  ·  corrupted: `0.25934`  ·  quality: `-0.00236`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.37219 |
| `explicit.stat_3374165039@T1` | -2.39113 |
| `explicit.stat_3485067555@T1` | 1.95858 |
| `explicit.stat_3780644166@T1` | -1.94548 |
| `explicit.stat_318953428@T1` | -1.64843 |
| `explicit.stat_4147897060@T1` | -1.60187 |
| `explicit.stat_1805182458@T1` | -1.42974 |
| `explicit.stat_21071013@T1` | 1.42802 |
| `explicit.stat_2523933828@T1` | -1.41554 |
| `explicit.stat_1697447343@T1` | -1.35066 |
| `explicit.stat_3166958180@T1` | -1.34514 |
| `explicit.stat_627767961@T1` | -1.31222 |

### other — n=59162, R²=-0.6256

intercept: `1.6093`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00030`  ·  n_top_tier: `0.34634`  ·  corrupted: `0.33877`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.31370 |
| `implicit.stat_2219129443` | 0.23023 |
| `implicit.stat_3879011313` | 0.23022 |
| `implicit.stat_4041853756` | 0.23022 |
| `explicit.stat_3299347043@T1` | -0.18964 |
| `explicit.stat_2974417149@T1` | 0.13120 |
| `explicit.stat_3917489142@T1` | 0.09559 |
| `implicit.stat_1379411836` | -0.07709 |
| `explicit.stat_2106365538@T1` | -0.07108 |
| `explicit.stat_2482852589@T1` | 0.07053 |
| `explicit.stat_789117908@T1` | -0.06787 |
| `implicit.stat_2901986750` | -0.04721 |

### accessory.ring — n=58917, R²=-2.0346

intercept: `3.4484`  ·  log_price: True  ·  ilvl: `-0.04263`  ·  n_mods: `-0.00075`  ·  n_top_tier: `1.08816`  ·  corrupted: `0.02290`  ·  n_sockets: `0.54677`  ·  quality: `0.00427`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.14357 |
| `explicit.stat_1573130764@T2` | -1.13711 |
| `explicit.stat_2231156303@T1` | -1.13170 |
| `explicit.stat_4220027924@T2` | -1.11366 |
| `explicit.stat_2923486259@T2` | -1.10880 |
| `explicit.stat_803737631@T1` | -1.10810 |
| `explicit.stat_789117908@T2` | -1.10766 |
| `explicit.stat_3325883026@T1` | -1.10643 |
| `explicit.stat_789117908@T1` | -1.10642 |
| `explicit.stat_4080418644@T1` | -1.10624 |
| `explicit.stat_3032590688@T2` | -1.10380 |
| `explicit.stat_2144192055@T1` | -1.10115 |

### accessory.amulet — n=53552, R²=-2.1611

intercept: `3.7009`  ·  log_price: True  ·  ilvl: `-0.04515`  ·  n_mods: `-0.02048`  ·  n_top_tier: `1.17538`  ·  corrupted: `0.04110`  ·  n_sockets: `-0.15181`  ·  quality: `0.00059`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.61501 |
| `explicit.stat_3299347043@T2` | -1.38793 |
| `explicit.stat_587431675@T2` | -1.24769 |
| `explicit.stat_2974417149@T1` | -1.24096 |
| `explicit.stat_472520716@T2` | -1.23844 |
| `explicit.stat_2866361420@T2` | -1.23785 |
| `explicit.stat_2974417149@T2` | -1.23737 |
| `explicit.stat_2866361420@T1` | -1.22969 |
| `explicit.stat_803737631@T1` | -1.22297 |
| `explicit.stat_1050105434@T2` | -1.21855 |
| `explicit.stat_803737631@T2` | -1.21118 |
| `explicit.stat_1671376347@T2` | -1.20831 |

### accessory.belt — n=39409, R²=-1.1506

intercept: `6.0071`  ·  log_price: True  ·  ilvl: `-0.06382`  ·  n_mods: `-0.17118`  ·  n_top_tier: `0.77710`  ·  corrupted: `1.18783`  ·  n_sockets: `0.37831`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.85265 |
| `explicit.stat_3299347043@T2` | -1.21725 |
| `explicit.stat_2881298780@T1` | -0.99598 |
| `explicit.stat_51994685@T1` | -0.89232 |
| `explicit.stat_4220027924@T2` | -0.85721 |
| `explicit.stat_1389754388@T1` | -0.85380 |
| `explicit.stat_1570770415@T1` | -0.84476 |
| `explicit.stat_809229260@T2` | -0.83862 |
| `explicit.stat_644456512@T1` | -0.83670 |
| `explicit.stat_3372524247@T2` | -0.81875 |
| `explicit.stat_1570770415@T2` | -0.80344 |
| `explicit.stat_3325883026@T1` | -0.79616 |

### armour.chest — n=39132, R²=-1.6337

intercept: `3.6168`  ·  log_price: True  ·  ilvl: `-0.04415`  ·  n_mods: `-0.03515`  ·  n_top_tier: `0.46383`  ·  corrupted: `0.18324`  ·  n_sockets: `0.05760`  ·  quality: `0.06101`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.77878 |
| `explicit.stat_3981240776@T1` | 0.84210 |
| `explicit.stat_986397080@T2` | -0.58580 |
| `explicit.stat_986397080@T1` | -0.56153 |
| `explicit.stat_3484657501@T1` | -0.55254 |
| `explicit.stat_3372524247@T1` | 0.54744 |
| `explicit.stat_2339757871@T2` | -0.54725 |
| `explicit.stat_915769802@T2` | -0.52958 |
| `explicit.stat_3033371881@T1` | 0.51491 |
| `explicit.stat_124859000@T1` | -0.51172 |
| `explicit.stat_915769802@T1` | -0.50814 |
| `explicit.stat_3299347043@T2` | -0.50423 |

### armour.helmet — n=38071, R²=-1.4026

intercept: `3.6391`  ·  log_price: True  ·  ilvl: `-0.04567`  ·  n_mods: `-0.05467`  ·  n_top_tier: `0.47297`  ·  corrupted: `0.70873`  ·  n_sockets: `0.11305`  ·  quality: `0.05516`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.89559 |
| `crafted.stat_3917489142@T1` | -1.98882 |
| `explicit.stat_3917489142@T2` | -1.15508 |
| `explicit.stat_3917489142@T1` | -1.01086 |
| `explicit.stat_1999113824@T1` | -0.70527 |
| `explicit.stat_1263695895@T1` | -0.70383 |
| `explicit.stat_2162097452@T2` | -0.63075 |
| `explicit.stat_803737631@T1` | -0.61126 |
| `explicit.stat_4052037485@T2` | -0.59131 |
| `explicit.stat_2162097452@T1` | 0.58956 |
| `explicit.stat_803737631@T2` | -0.57971 |
| `explicit.stat_1263695895@T2` | -0.57705 |

### armour.boots — n=35381, R²=-1.6706

intercept: `3.5760`  ·  log_price: True  ·  ilvl: `-0.04377`  ·  n_mods: `-0.02382`  ·  n_top_tier: `0.66049`  ·  corrupted: `-0.00136`  ·  n_sockets: `0.02722`  ·  quality: `0.06694`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.56519 |
| `crafted.stat_3917489142@T1` | 1.39142 |
| `explicit.stat_2339757871@T1` | -1.02538 |
| `explicit.stat_3299347043@T1` | -0.86780 |
| `explicit.stat_3917489142@T2` | -0.79652 |
| `explicit.stat_2923486259@T1` | 0.75271 |
| `explicit.stat_1062208444@T2` | -0.71964 |
| `explicit.stat_2923486259@T2` | -0.71661 |
| `explicit.stat_2160282525@T1` | -0.70255 |
| `explicit.stat_1874553720@T1` | -0.70215 |
| `explicit.stat_3299347043@T2` | -0.69759 |
| `explicit.stat_4052037485@T2` | -0.68778 |

### armour.gloves — n=34472, R²=-1.6767

intercept: `3.7612`  ·  log_price: True  ·  ilvl: `-0.04783`  ·  n_mods: `-0.02853`  ·  n_top_tier: `0.61843`  ·  corrupted: `0.03070`  ·  n_sockets: `0.09904`  ·  quality: `0.04950`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 3.15914 |
| `rune.stat_201332984` | 1.76721 |
| `rune.stat_836936635` | 1.08273 |
| `explicit.stat_2923486259@T1` | -1.01533 |
| `explicit.stat_1671376347@T1` | 0.91027 |
| `explicit.stat_2923486259@T2` | -0.85255 |
| `explicit.stat_3484657501@T2` | -0.85104 |
| `explicit.stat_9187492@T2` | -0.84553 |
| `explicit.stat_9187492@T1` | 0.81487 |
| `explicit.stat_3321629045@T2` | -0.81051 |
| `explicit.stat_803737631@T1` | -0.79508 |
| `explicit.stat_3484657501@T1` | -0.78047 |

### weapon.wand — n=20990, R²=-2.0157

intercept: `3.8157`  ·  log_price: True  ·  ilvl: `-0.04713`  ·  n_mods: `-0.04842`  ·  n_top_tier: `0.41177`  ·  corrupted: `-0.03864`  ·  n_sockets: `0.07917`  ·  quality: `0.01572`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.14622 |
| `rune.stat_124131830` | -2.62676 |
| `explicit.stat_2254480358@T1` | 2.53957 |
| `explicit.stat_124131830@T1` | 2.19170 |
| `explicit.stat_4226189338@T1` | 1.93849 |
| `explicit.stat_591105508@T1` | 1.85884 |
| `explicit.stat_736967255@T2` | 1.77228 |
| `crafted.stat_124131830` | 1.29097 |
| `explicit.stat_1600707273@T1` | 1.18059 |
| `explicit.stat_4226189338@T2` | 1.00225 |
| `explicit.stat_2254480358@T2` | 0.95115 |
| `explicit.stat_2768835289@T2` | -0.90830 |

### weapon.bow — n=16791, R²=-1.8223

intercept: `3.9931`  ·  log_price: True  ·  ilvl: `-0.04584`  ·  n_mods: `-0.11183`  ·  n_top_tier: `0.65199`  ·  corrupted: `0.25757`  ·  n_sockets: `0.06846`  ·  quality: `0.03720`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -1.98004 |
| `desecrated.stat_210067635@T1` | -1.50607 |
| `crafted.stat_3035140377` | 1.39286 |
| `explicit.stat_2463230181@T2` | -1.06936 |
| `explicit.stat_1263695895@T1` | -1.06840 |
| `explicit.stat_1263695895@T2` | -0.93689 |
| `explicit.stat_2463230181@T1` | -0.92735 |
| `explicit.stat_3336890334@T1` | 0.88079 |
| `explicit.stat_3695891184@T2` | -0.87864 |
| `explicit.stat_518292764@T2` | -0.85137 |
| `explicit.stat_3695891184@T1` | -0.84368 |
| `explicit.stat_1509134228@T1` | -0.83762 |

### flask.charm — n=16780, R²=-0.6075

intercept: `0.0736`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.93433`  ·  corrupted: `1.60907`  ·  quality: `0.00027`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.78373 |
| `explicit.stat_1056492907` | 2.90637 |
| `explicit.stat_828533480@T2` | -1.93436 |
| `explicit.stat_1873752457@T2` | -1.93432 |
| `explicit.stat_1120862500@T2` | -1.93432 |
| `explicit.stat_388617051@T2` | -1.93431 |
| `explicit.stat_1873752457@T1` | -1.93430 |
| `explicit.stat_3196823591@T2` | -1.93429 |
| `explicit.stat_2676834156@T2` | -1.93429 |
| `explicit.stat_2365392475@T2` | -1.93428 |
| `explicit.stat_828533480@T1` | -1.93048 |
| `explicit.stat_1366840608@T2` | -1.92866 |

### weapon.crossbow — n=15738, R²=-1.7343

intercept: `3.9644`  ·  log_price: True  ·  ilvl: `-0.04668`  ·  n_mods: `-0.09954`  ·  n_top_tier: `0.56226`  ·  corrupted: `0.05618`  ·  n_sockets: `0.08400`  ·  quality: `0.02130`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.61332 |
| `explicit.stat_1980802737` | 1.29511 |
| `explicit.stat_2250681686@T2` | -1.12937 |
| `explicit.stat_1202301673@T1` | 1.00155 |
| `explicit.stat_1263695895@T2` | -0.81343 |
| `explicit.stat_2250681686` | 0.80808 |
| `explicit.stat_1509134228@T2` | -0.79366 |
| `crafted.stat_3035140377` | 0.77105 |
| `explicit.stat_709508406@T1` | 0.75547 |
| `explicit.stat_1940865751@T2` | -0.72764 |
| `explicit.stat_3695891184@T1` | -0.72421 |
| `explicit.stat_2694482655@T1` | -0.70640 |

### weapon.warstaff — n=10459, R²=-0.354

intercept: `-10.4389`  ·  log_price: True  ·  ilvl: `0.14341`  ·  n_mods: `-0.24652`  ·  n_top_tier: `0.25542`  ·  corrupted: `0.29052`  ·  n_sockets: `0.18941`  ·  quality: `0.05663`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 2.01088 |
| `desecrated.stat_2231156303@T1` | 2.01088 |
| `crafted.stat_210067635@T2` | 1.38273 |
| `desecrated.stat_473429811@T1` | -1.17632 |
| `desecrated.stat_3291658075@T1` | -1.17632 |
| `rune.stat_243313994` | 0.90558 |
| `explicit.stat_328541901@T1` | -0.79176 |
| `desecrated.stat_9187492` | 0.78070 |
| `explicit.stat_1509134228@T1` | 0.70857 |
| `explicit.stat_328541901@T2` | -0.68518 |
| `explicit.stat_1037193709@T1` | 0.68369 |
| `explicit.stat_9187492@T1` | 0.66633 |

### weapon.staff — n=9805, R²=-0.3838

intercept: `-15.9353`  ·  log_price: True  ·  ilvl: `0.20600`  ·  n_mods: `-0.15170`  ·  n_top_tier: `0.54222`  ·  corrupted: `0.61904`  ·  n_sockets: `0.21978`  ·  quality: `0.03953`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.27151 |
| `explicit.stat_1545858329@T1` | 1.66894 |
| `explicit.stat_293638271@T2` | -1.60703 |
| `explicit.stat_591105508@T1` | 1.52680 |
| `explicit.stat_124131830@T1` | 1.11052 |
| `explicit.stat_1600707273@T1` | 0.94952 |
| `explicit.stat_274716455@T1` | -0.91985 |
| `rune.stat_124131830` | 0.77167 |
| `explicit.stat_591105508@T2` | 0.73763 |
| `explicit.stat_2254480358@T2` | 0.72079 |
| `explicit.stat_2968503605@T1` | -0.71304 |
| `explicit.stat_293638271@T1` | -0.67447 |

### weapon.sceptre — n=9678, R²=-0.3255

intercept: `-20.8397`  ·  log_price: True  ·  ilvl: `0.26925`  ·  n_mods: `-0.02097`  ·  n_top_tier: `0.01039`  ·  corrupted: `0.37241`  ·  n_sockets: `0.22636`  ·  quality: `0.03160`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.84397 |
| `explicit.stat_1250712710@T2` | 1.70270 |
| `explicit.stat_2162097452@T2` | 1.66917 |
| `explicit.stat_3057012405@T1` | 1.52605 |
| `explicit.stat_101878827@T1` | 0.96511 |
| `explicit.stat_101878827@T2` | 0.92272 |
| `explicit.stat_849987426@T1` | 0.87844 |
| `explicit.stat_1250712710@T1` | 0.80591 |
| `explicit.stat_1798257884@T2` | 0.77568 |
| `explicit.stat_1998951374@T1` | 0.66516 |
| `explicit.stat_2347036682@T1` | 0.59066 |
| `explicit.stat_1050105434@T1` | 0.58018 |

### weapon.spear — n=7851, R²=-0.4028

intercept: `-12.8018`  ·  log_price: True  ·  ilvl: `0.17840`  ·  n_mods: `-0.19841`  ·  n_top_tier: `0.79089`  ·  corrupted: `0.04945`  ·  n_sockets: `0.19453`  ·  quality: `0.06903`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -5.12166 |
| `explicit.stat_1202301673@T1` | 1.42126 |
| `desecrated.stat_210067635@T1` | -1.33807 |
| `explicit.stat_4080418644@T2` | -1.31191 |
| `explicit.stat_1509134228@T1` | 1.15470 |
| `explicit.stat_9187492@T2` | -1.06049 |
| `explicit.stat_4080418644@T1` | -1.05683 |
| `explicit.stat_1940865751@T2` | -1.03665 |
| `explicit.stat_3261801346@T1` | -1.01116 |
| `explicit.stat_691932474@T2` | -0.97014 |
| `explicit.stat_9187492@T1` | 0.96025 |
| `explicit.stat_748522257@T2` | -0.95725 |

### armour.focus — n=6412, R²=-0.3578

intercept: `-14.2626`  ·  log_price: True  ·  ilvl: `0.18471`  ·  n_mods: `-0.15195`  ·  n_top_tier: `0.90088`  ·  corrupted: `0.40815`  ·  n_sockets: `0.48003`  ·  quality: `0.05721`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 3.36954 |
| `explicit.stat_4220027924@T2` | -1.46328 |
| `explicit.stat_2923486259@T1` | -1.40370 |
| `explicit.stat_2231156303@T2` | -1.24188 |
| `explicit.stat_4220027924@T1` | -1.23073 |
| `explicit.stat_736967255@T2` | -1.00793 |
| `explicit.stat_2974417149@T2` | -0.98939 |
| `explicit.stat_2974417149@T1` | -0.98425 |
| `explicit.stat_2891184298@T1` | -0.96671 |
| `explicit.stat_2231156303@T1` | -0.92286 |
| `explicit.stat_1050105434@T2` | -0.91736 |
| `explicit.stat_737908626@T2` | -0.88175 |

### armour.quiver — n=6037, R²=-0.3009

intercept: `-15.5141`  ·  log_price: True  ·  ilvl: `0.19041`  ·  n_mods: `-0.11582`  ·  n_top_tier: `0.74925`  ·  corrupted: `0.73286`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.91737 |
| `explicit.stat_2463230181@T1` | 3.09366 |
| `explicit.stat_2463230181@T2` | 1.57673 |
| `explicit.stat_681332047@T2` | -1.36617 |
| `explicit.stat_1573130764@T1` | -1.21021 |
| `explicit.stat_4067062424@T1` | -0.89871 |
| `explicit.stat_2321178454@T2` | -0.88773 |
| `explicit.stat_803737631@T2` | -0.85035 |
| `explicit.stat_1573130764@T2` | -0.83527 |
| `explicit.stat_681332047@T1` | -0.81202 |
| `explicit.stat_4067062424@T2` | -0.77506 |
| `explicit.stat_2194114101@T2` | -0.72878 |

### armour.shield — n=5237, R²=-0.4583

intercept: `-12.9706`  ·  log_price: True  ·  ilvl: `0.17152`  ·  n_mods: `-0.08104`  ·  n_top_tier: `0.60517`  ·  corrupted: `-0.30340`  ·  n_sockets: `0.31784`  ·  quality: `0.06738`

| stat_id | coef |
|---|---|
| `explicit.stat_3321629045@T2` | -1.26248 |
| `explicit.stat_1301765461@T1` | 1.25473 |
| `explicit.stat_3484657501@T1` | -1.25309 |
| `explicit.stat_3855016469@T1` | -1.02427 |
| `explicit.stat_4095671657@T1` | -1.02141 |
| `explicit.stat_328541901@T1` | -0.92946 |
| `explicit.stat_2901986750@T1` | -0.91977 |
| `explicit.stat_3033371881@T2` | -0.91927 |
| `explicit.stat_3261801346@T1` | -0.90345 |
| `explicit.stat_3484657501@T2` | -0.88379 |
| `explicit.stat_2451402625@T1` | -0.84292 |
| `explicit.stat_2451402625@T2` | -0.81932 |

### weapon.twomace — n=4816, R²=-0.4507

intercept: `-10.5602`  ·  log_price: True  ·  ilvl: `0.14687`  ·  n_mods: `-0.22340`  ·  n_top_tier: `0.33389`  ·  corrupted: `-0.05348`  ·  n_sockets: `0.14869`  ·  quality: `0.05891`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.11722 |
| `explicit.stat_1037193709@T1` | -1.45954 |
| `desecrated.stat_1509134228@T1` | 1.43954 |
| `explicit.stat_3336890334@T1` | -1.07732 |
| `explicit.stat_387439868@T2` | -0.77905 |
| `crafted.stat_3035140377` | 0.74677 |
| `explicit.stat_9187492@T1` | -0.72151 |
| `explicit.stat_1263695895@T2` | -0.69801 |
| `explicit.stat_691932474@T1` | -0.59951 |
| `explicit.stat_3695891184@T1` | -0.57706 |
| `explicit.stat_210067635@T2` | 0.54531 |
| `explicit.stat_3695891184@T2` | -0.52907 |

## Coverage (listings per base)

- … **Sapphire** — 30711 listings (30657 priced) [0.3–885594757.8 ex]
- … **Emerald** — 29880 listings (29839 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 22875 listings (22848 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11258 listings (11243 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10021 listings (10000 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 9702 listings (9678 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9567 listings (9559 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 9043 listings (9025 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8915 listings (8896 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8634 listings (8622 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7418 listings (7406 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7161 listings (7154 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7055 listings (7049 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6723 listings (6702 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6238 listings (6231 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 6155 listings (6127 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 6116 listings (6099 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6107 listings (6095 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6072 listings (6065 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6019 listings (5993 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 5942 listings (5933 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5846 listings (5839 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5560 listings (5557 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5535 listings (5523 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5433 listings (5424 priced) [0.3–398912568423.8 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-19T03:55:59+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **638757** (636808 priced in exalted)
- Distinct bases: 994 · distinct mods: 3264 · mod rows: 3025454
- Sold signals: **24750** sold · 363128 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-19T03:43:19+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.40** (median |log error| 3.1091)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.15** · typical error ×66.72 · ±30% 5% · n=93073
- Premium segment (60ex+): skill **+0.14** · typical error ×312.03 · ±30% 0% · n=63029

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 13364 | ×51.96 | 21% | +0.03 | +0.05 |
| jewel | 12713 | ×10.73 | 4% | +0.09 | +0.12 |
| accessory.amulet | 12172 | ×35.80 | 19% | +0.04 | +0.03 |
| accessory.belt | 8866 | ×22.94 | 14% | +0.08 | +0.10 |
| armour.chest | 8547 | ×17.97 | 23% | +0.08 | +0.11 |
| armour.helmet | 8337 | ×25.13 | 18% | +0.08 | +0.10 |
| armour.boots | 7815 | ×32.99 | 21% | +0.09 | +0.11 |
| armour.gloves | 7638 | ×38.13 | 16% | +0.08 | +0.10 |
| other | 7519 | ×1.96 | 43% | +0.10 | +0.18 |
| weapon.wand | 4585 | ×45.92 | 16% | +0.09 | +0.10 |
| weapon.bow | 3591 | ×30.37 | 13% | +0.14 | +0.14 |
| weapon.crossbow | 3379 | ×29.81 | 12% | +0.11 | +0.15 |
| weapon.warstaff | 2240 | ×21.31 | 6% | +0.20 | +0.21 |
| weapon.staff | 2138 | ×28.71 | 6% | +0.16 | +0.15 |
| weapon.sceptre | 2092 | ×26.88 | 5% | +0.13 | +0.13 |
| weapon.spear | 1667 | ×23.97 | 7% | +0.12 | +0.13 |
| armour.focus | 1415 | ×18.84 | 7% | +0.11 | +0.12 |
| armour.quiver | 1338 | ×23.83 | 7% | +0.16 | +0.17 |
| flask.charm | 1104 | ×15.00 | 30% | -0.00 | +0.02 |
| armour.shield | 1103 | ×18.38 | 9% | +0.08 | +0.10 |
| weapon.twomace | 1021 | ×7.77 | 9% | +0.10 | +0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=68975, R²=-0.956

intercept: `-1.9329`  ·  log_price: True  ·  ilvl: `0.02584`  ·  n_mods: `0.87240`  ·  n_top_tier: `-0.33031`  ·  corrupted: `0.26447`  ·  quality: `-0.00239`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.26461 |
| `explicit.stat_3374165039@T1` | -2.26563 |
| `explicit.stat_3485067555@T1` | 1.99643 |
| `explicit.stat_3780644166@T1` | -1.90247 |
| `explicit.stat_2523933828@T1` | -1.76803 |
| `explicit.stat_4147897060@T1` | -1.64416 |
| `explicit.stat_1697447343@T1` | -1.64119 |
| `explicit.stat_3174700878@T1` | 1.38369 |
| `explicit.stat_318953428@T1` | -1.32288 |
| `explicit.stat_686254215@T1` | -1.29740 |
| `explicit.stat_3166958180@T1` | -1.27568 |
| `explicit.stat_21071013@T1` | 1.27087 |

### accessory.ring — n=61165, R²=-2.0285

intercept: `3.4496`  ·  log_price: True  ·  ilvl: `-0.04263`  ·  n_mods: `0.00034`  ·  n_top_tier: `1.09598`  ·  corrupted: `0.02001`  ·  n_sockets: `0.16860`  ·  quality: `0.02401`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.14912 |
| `explicit.stat_1573130764@T2` | -1.13896 |
| `explicit.stat_2231156303@T1` | -1.12742 |
| `explicit.stat_803737631@T1` | -1.12348 |
| `explicit.stat_4220027924@T2` | -1.11886 |
| `explicit.stat_3325883026@T1` | -1.11128 |
| `explicit.stat_4080418644@T1` | -1.11014 |
| `explicit.stat_2923486259@T2` | -1.10853 |
| `explicit.stat_789117908@T2` | -1.10843 |
| `explicit.stat_3032590688@T2` | -1.10841 |
| `explicit.stat_2144192055@T1` | -1.10746 |
| `explicit.stat_2901986750@T2` | -1.10498 |

### other — n=60931, R²=-0.6226

intercept: `1.6093`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00244`  ·  n_top_tier: `0.34414`  ·  corrupted: `0.32112`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.34672 |
| `explicit.stat_3299347043@T1` | -0.23517 |
| `implicit.stat_2219129443` | 0.23001 |
| `implicit.stat_3879011313` | 0.23001 |
| `implicit.stat_4041853756` | 0.23001 |
| `explicit.stat_2974417149@T1` | 0.13242 |
| `explicit.stat_736967255@T1` | -0.09058 |
| `explicit.stat_3291658075@T1` | -0.08010 |
| `explicit.stat_789117908@T1` | -0.07500 |
| `explicit.stat_2106365538@T1` | -0.06070 |
| `implicit.stat_2901986750` | -0.05251 |
| `explicit.stat_2968503605@T1` | -0.04974 |

### accessory.amulet — n=55455, R²=-2.1573

intercept: `3.6608`  ·  log_price: True  ·  ilvl: `-0.04464`  ·  n_mods: `-0.02383`  ·  n_top_tier: `1.19996`  ·  corrupted: `0.03716`  ·  n_sockets: `-0.17138`  ·  quality: `-0.00073`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.84417 |
| `explicit.stat_3299347043@T2` | -1.59614 |
| `explicit.stat_2974417149@T1` | -1.31372 |
| `explicit.stat_587431675@T2` | -1.29751 |
| `explicit.stat_2974417149@T2` | -1.28853 |
| `explicit.stat_803737631@T1` | -1.28264 |
| `explicit.stat_2866361420@T2` | -1.26929 |
| `explicit.stat_2866361420@T1` | -1.26111 |
| `explicit.stat_1050105434@T2` | -1.25322 |
| `explicit.stat_472520716@T2` | -1.25223 |
| `explicit.stat_803737631@T2` | -1.24671 |
| `explicit.stat_3261801346@T1` | -1.23434 |

### accessory.belt — n=40667, R²=-1.4727

intercept: `4.8046`  ·  log_price: True  ·  ilvl: `-0.05591`  ·  n_mods: `-0.05558`  ·  n_top_tier: `0.58465`  ·  corrupted: `1.29812`  ·  n_sockets: `1.07668`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.03625 |
| `explicit.stat_3299347043@T1` | -0.90109 |
| `explicit.stat_4220027924@T1` | 0.72145 |
| `explicit.stat_3299347043@T2` | -0.69223 |
| `explicit.stat_2881298780@T1` | -0.66276 |
| `explicit.stat_4220027924@T2` | -0.63734 |
| `explicit.stat_51994685@T1` | -0.62303 |
| `explicit.stat_1389754388@T1` | -0.61242 |
| `explicit.stat_3372524247@T2` | -0.61193 |
| `explicit.stat_1570770415@T2` | -0.60957 |
| `explicit.stat_3325883026@T1` | -0.59496 |
| `explicit.stat_1570770415@T1` | -0.59055 |

### armour.chest — n=40275, R²=-1.7543

intercept: `3.3601`  ·  log_price: True  ·  ilvl: `-0.04148`  ·  n_mods: `-0.01668`  ·  n_top_tier: `0.37704`  ·  corrupted: `0.10530`  ·  n_sockets: `0.02483`  ·  quality: `0.06730`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.70861 |
| `explicit.stat_3981240776@T1` | 0.59872 |
| `explicit.stat_986397080@T2` | -0.44434 |
| `explicit.stat_3372524247@T1` | 0.43756 |
| `explicit.stat_986397080@T1` | -0.43132 |
| `explicit.stat_915769802@T2` | -0.41489 |
| `explicit.stat_4080418644@T1` | -0.41255 |
| `explicit.stat_2339757871@T2` | -0.40755 |
| `explicit.stat_3484657501@T1` | -0.40670 |
| `explicit.stat_915769802@T1` | -0.40531 |
| `explicit.stat_1692879867@T2` | -0.40128 |
| `explicit.stat_2923486259@T2` | -0.40094 |

### armour.helmet — n=39188, R²=-1.6965

intercept: `3.3530`  ·  log_price: True  ·  ilvl: `-0.04210`  ·  n_mods: `-0.02340`  ·  n_top_tier: `0.53303`  ·  corrupted: `0.70544`  ·  n_sockets: `0.04187`  ·  quality: `0.06561`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.85231 |
| `explicit.stat_3917489142@T2` | -0.88437 |
| `explicit.stat_3917489142@T1` | -0.81575 |
| `explicit.stat_1263695895@T1` | -0.79828 |
| `explicit.stat_2162097452@T2` | -0.69687 |
| `explicit.stat_1263695895@T2` | -0.69083 |
| `crafted.stat_3917489142@T1` | -0.68906 |
| `explicit.stat_1999113824@T1` | -0.59427 |
| `explicit.stat_4052037485@T2` | -0.59161 |
| `explicit.stat_803737631@T1` | -0.58953 |
| `explicit.stat_53045048@T1` | -0.58292 |
| `explicit.stat_803737631@T2` | -0.57364 |

### armour.boots — n=36441, R²=-1.7368

intercept: `3.5311`  ·  log_price: True  ·  ilvl: `-0.04338`  ·  n_mods: `-0.02142`  ·  n_top_tier: `0.60666`  ·  corrupted: `0.00456`  ·  n_sockets: `0.02723`  ·  quality: `0.06527`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.63476 |
| `crafted.stat_3917489142@T1` | 1.12215 |
| `explicit.stat_2339757871@T1` | -0.97068 |
| `explicit.stat_3299347043@T1` | -0.77591 |
| `explicit.stat_3917489142@T2` | -0.76283 |
| `explicit.stat_3917489142@T1` | -0.67248 |
| `explicit.stat_2923486259@T2` | -0.66595 |
| `explicit.stat_2923486259@T1` | 0.65770 |
| `explicit.stat_1062208444@T2` | -0.65699 |
| `explicit.stat_2160282525@T1` | -0.64785 |
| `explicit.stat_1874553720@T1` | -0.64156 |
| `explicit.stat_3321629045@T1` | -0.63435 |

### armour.gloves — n=35475, R²=-1.727

intercept: `3.8073`  ·  log_price: True  ·  ilvl: `-0.04873`  ·  n_mods: `-0.02225`  ·  n_top_tier: `0.69960`  ·  corrupted: `-0.01215`  ·  n_sockets: `0.09803`  ·  quality: `0.04910`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.06949 |
| `rune.stat_201332984` | 1.43425 |
| `explicit.stat_2923486259@T1` | -1.39195 |
| `explicit.stat_3484657501@T2` | -0.97384 |
| `explicit.stat_3321629045@T2` | -0.87297 |
| `explicit.stat_803737631@T2` | -0.85785 |
| `explicit.stat_9187492@T2` | -0.85357 |
| `explicit.stat_3484657501@T1` | -0.84724 |
| `explicit.stat_4015621042@T2` | -0.84414 |
| `explicit.stat_1671376347@T1` | 0.82901 |
| `explicit.stat_803737631@T1` | -0.81341 |
| `explicit.stat_2923486259@T2` | -0.80693 |

### weapon.wand — n=21452, R²=-2.0027

intercept: `3.8615`  ·  log_price: True  ·  ilvl: `-0.04797`  ·  n_mods: `-0.04105`  ·  n_top_tier: `0.32568`  ·  corrupted: `0.00506`  ·  n_sockets: `0.05398`  ·  quality: `0.02482`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.09266 |
| `rune.stat_124131830` | -2.72735 |
| `explicit.stat_2254480358@T1` | 2.50917 |
| `explicit.stat_124131830@T1` | 2.44492 |
| `explicit.stat_591105508@T1` | 2.03614 |
| `explicit.stat_4226189338@T1` | 1.99357 |
| `explicit.stat_736967255@T2` | 1.76572 |
| `crafted.stat_124131830` | 1.25333 |
| `explicit.stat_2254480358@T2` | 1.10983 |
| `explicit.stat_4226189338@T2` | 0.98882 |
| `explicit.stat_1600707273@T1` | 0.78979 |
| `explicit.stat_1263695895@T2` | -0.73224 |

### flask.charm — n=17491, R²=-0.6095

intercept: `0.0959`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.08335`  ·  corrupted: `1.60321`  ·  quality: `0.00121`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.77908 |
| `explicit.stat_1056492907` | 2.82691 |
| `explicit.stat_3246948616` | 1.09868 |
| `explicit.stat_828533480@T2` | -1.08339 |
| `explicit.stat_1120862500@T2` | -1.08335 |
| `explicit.stat_1873752457@T2` | -1.08335 |
| `explicit.stat_1873752457@T1` | -1.08333 |
| `explicit.stat_3196823591@T2` | -1.08332 |
| `explicit.stat_828533480@T1` | -1.08332 |
| `explicit.stat_2365392475@T2` | -1.08331 |
| `explicit.stat_2676834156@T2` | -1.08329 |
| `explicit.stat_388617051@T2` | -1.08317 |

### weapon.bow — n=17145, R²=-1.852

intercept: `3.8950`  ·  log_price: True  ·  ilvl: `-0.04551`  ·  n_mods: `-0.09379`  ·  n_top_tier: `0.67626`  ·  corrupted: `0.45026`  ·  n_sockets: `0.07834`  ·  quality: `0.03274`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.41421 |
| `explicit.stat_1263695895@T1` | -1.23139 |
| `explicit.stat_3336890334@T1` | 1.09622 |
| `explicit.stat_1263695895@T2` | -1.04481 |
| `explicit.stat_2463230181@T2` | -1.01036 |
| `explicit.stat_1509134228@T1` | -0.85973 |
| `explicit.stat_3695891184@T2` | -0.80830 |
| `explicit.stat_1037193709@T1` | -0.77833 |
| `explicit.stat_3639275092@T1` | -0.77751 |
| `explicit.stat_3639275092@T2` | -0.76623 |
| `explicit.stat_1037193709@T2` | -0.76017 |
| `explicit.stat_709508406@T2` | -0.75023 |

### weapon.crossbow — n=16076, R²=-1.6602

intercept: `4.0002`  ·  log_price: True  ·  ilvl: `-0.04762`  ·  n_mods: `-0.10442`  ·  n_top_tier: `0.44993`  ·  corrupted: `0.08197`  ·  n_sockets: `0.10559`  ·  quality: `0.02521`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.47326 |
| `explicit.stat_1980802737` | 1.33564 |
| `explicit.stat_1202301673@T1` | 1.19636 |
| `explicit.stat_2250681686@T2` | -1.17572 |
| `explicit.stat_709508406@T1` | 0.84804 |
| `explicit.stat_2250681686` | 0.83464 |
| `explicit.stat_1263695895@T2` | -0.73941 |
| `explicit.stat_3336890334@T1` | -0.72421 |
| `crafted.stat_3035140377` | 0.71108 |
| `explicit.stat_3336890334@T2` | -0.69526 |
| `explicit.stat_3695891184@T2` | -0.65126 |
| `explicit.stat_1940865751@T2` | -0.62187 |

### weapon.warstaff — n=10851, R²=-0.3531

intercept: `-10.0433`  ·  log_price: True  ·  ilvl: `0.13724`  ·  n_mods: `-0.24958`  ·  n_top_tier: `0.31912`  ·  corrupted: `0.41495`  ·  n_sockets: `0.15118`  ·  quality: `0.05698`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 2.37860 |
| `desecrated.stat_2231156303@T1` | 2.37860 |
| `desecrated.stat_473429811@T1` | -1.57970 |
| `desecrated.stat_3291658075@T1` | -1.57970 |
| `crafted.stat_210067635@T2` | 1.30009 |
| `rune.stat_243313994` | 0.97037 |
| `explicit.stat_1037193709@T1` | 0.78717 |
| `explicit.stat_328541901@T1` | -0.75853 |
| `desecrated.stat_9187492` | 0.74663 |
| `explicit.stat_328541901@T2` | -0.70574 |
| `explicit.stat_1509134228@T1` | 0.69548 |
| `explicit.stat_1368271171@T1` | -0.62437 |

### weapon.staff — n=10213, R²=-0.3835

intercept: `-15.7387`  ·  log_price: True  ·  ilvl: `0.20178`  ·  n_mods: `-0.07004`  ·  n_top_tier: `0.52412`  ·  corrupted: `0.63238`  ·  n_sockets: `0.19765`  ·  quality: `0.03456`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.13314 |
| `explicit.stat_1545858329@T1` | 2.11289 |
| `explicit.stat_4226189338@T1` | 2.09166 |
| `explicit.stat_293638271@T2` | -1.49750 |
| `explicit.stat_124131830@T1` | 1.24460 |
| `explicit.stat_1600707273@T1` | 1.08812 |
| `explicit.stat_2254480358@T2` | 0.78819 |
| `explicit.stat_2254480358@T1` | 0.75244 |
| `explicit.stat_124131830@T2` | 0.74854 |
| `explicit.stat_274716455@T1` | -0.68843 |
| `explicit.stat_473429811@T2` | -0.67579 |
| `explicit.stat_3278136794@T1` | -0.65863 |

### weapon.sceptre — n=10041, R²=-0.3379

intercept: `-20.0110`  ·  log_price: True  ·  ilvl: `0.25726`  ·  n_mods: `0.01184`  ·  n_top_tier: `0.38048`  ·  corrupted: `0.05444`  ·  n_sockets: `0.22987`  ·  quality: `0.02972`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.34890 |
| `explicit.stat_2162097452@T2` | 1.18046 |
| `explicit.stat_3057012405@T1` | 1.16525 |
| `explicit.stat_1250712710@T2` | 1.10055 |
| `explicit.stat_2854751904@T2` | -0.86625 |
| `explicit.stat_2347036682@T2` | -0.78569 |
| `explicit.stat_3639275092@T2` | -0.72538 |
| `explicit.stat_1798257884@T2` | 0.71919 |
| `explicit.stat_101878827@T1` | 0.70106 |
| `explicit.stat_101878827@T2` | 0.66767 |
| `explicit.stat_1574590649@T2` | -0.59962 |
| `explicit.stat_1263695895@T2` | -0.53542 |

### weapon.spear — n=8118, R²=-0.3755

intercept: `-12.2822`  ·  log_price: True  ·  ilvl: `0.17427`  ·  n_mods: `-0.22272`  ·  n_top_tier: `0.77503`  ·  corrupted: `-0.06344`  ·  n_sockets: `0.22079`  ·  quality: `0.07630`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.79289 |
| `explicit.stat_1202301673@T1` | 1.45187 |
| `explicit.stat_1509134228@T1` | 1.41932 |
| `desecrated.stat_210067635@T1` | -1.35763 |
| `explicit.stat_9187492@T1` | 1.32922 |
| `explicit.stat_1940865751@T2` | -1.13701 |
| `explicit.stat_4080418644@T2` | -1.09563 |
| `explicit.stat_691932474@T1` | -1.02119 |
| `explicit.stat_691932474@T2` | -0.99656 |
| `crafted.stat_3035140377` | 0.95253 |
| `explicit.stat_9187492@T2` | -0.90993 |
| `explicit.stat_4080418644@T1` | -0.90196 |

### armour.focus — n=6635, R²=-0.3328

intercept: `-14.4157`  ·  log_price: True  ·  ilvl: `0.18694`  ·  n_mods: `-0.21111`  ·  n_top_tier: `0.91554`  ·  corrupted: `0.28916`  ·  n_sockets: `0.35006`  ·  quality: `0.04927`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 3.31049 |
| `explicit.stat_4220027924@T1` | -1.57924 |
| `explicit.stat_2923486259@T1` | -1.53755 |
| `explicit.stat_4220027924@T2` | -1.42907 |
| `explicit.stat_3291658075@T1` | -1.26411 |
| `explicit.stat_2231156303@T2` | -1.17278 |
| `explicit.stat_2974417149@T1` | -1.16285 |
| `explicit.stat_2974417149@T2` | -1.11963 |
| `explicit.stat_2231156303@T1` | -1.05976 |
| `explicit.stat_2339757871@T2` | -0.94905 |
| `explicit.stat_4052037485@T2` | -0.91824 |
| `explicit.stat_737908626@T2` | -0.87329 |

### armour.quiver — n=6234, R²=-0.3011

intercept: `-15.4731`  ·  log_price: True  ·  ilvl: `0.18855`  ·  n_mods: `-0.13560`  ·  n_top_tier: `0.82215`  ·  corrupted: `0.75576`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.91932 |
| `explicit.stat_2463230181@T1` | 2.56409 |
| `explicit.stat_1573130764@T1` | -1.32711 |
| `explicit.stat_681332047@T2` | -1.32164 |
| `explicit.stat_2463230181@T2` | 1.23317 |
| `explicit.stat_1573130764@T2` | -0.96296 |
| `explicit.stat_2194114101@T2` | -0.94784 |
| `explicit.stat_803737631@T2` | -0.94642 |
| `explicit.stat_4067062424@T2` | -0.90261 |
| `explicit.stat_803737631@T1` | -0.89392 |
| `explicit.stat_4067062424@T1` | -0.87583 |
| `explicit.stat_2321178454@T2` | -0.86351 |

### armour.shield — n=5361, R²=-0.4604

intercept: `-12.1221`  ·  log_price: True  ·  ilvl: `0.16078`  ·  n_mods: `-0.07985`  ·  n_top_tier: `0.60016`  ·  corrupted: `-0.25646`  ·  n_sockets: `0.33209`  ·  quality: `0.06338`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.27841 |
| `explicit.stat_3321629045@T2` | -1.25655 |
| `explicit.stat_3855016469@T1` | -1.04896 |
| `explicit.stat_3484657501@T2` | -1.02682 |
| `explicit.stat_3033371881@T2` | -0.95535 |
| `explicit.stat_1301765461@T1` | 0.92343 |
| `explicit.stat_4095671657@T1` | -0.89688 |
| `explicit.stat_328541901@T1` | -0.89157 |
| `explicit.stat_4095671657@T2` | -0.88967 |
| `explicit.stat_2901986750@T1` | -0.80510 |
| `explicit.stat_1671376347@T1` | -0.75822 |
| `explicit.stat_2923486259@T2` | -0.75485 |

### weapon.twomace — n=4959, R²=-0.4596

intercept: `-9.4679`  ·  log_price: True  ·  ilvl: `0.13199`  ·  n_mods: `-0.21805`  ·  n_top_tier: `0.29440`  ·  corrupted: `0.30351`  ·  n_sockets: `0.15105`  ·  quality: `0.06075`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.67553 |
| `desecrated.stat_1509134228@T1` | 1.77580 |
| `explicit.stat_1037193709@T1` | -1.31888 |
| `explicit.stat_3336890334@T1` | -1.06565 |
| `explicit.stat_709508406@T1` | 0.92914 |
| `explicit.stat_9187492@T1` | -0.83329 |
| `explicit.stat_1263695895@T2` | -0.75033 |
| `explicit.stat_1509134228@T1` | 0.72389 |
| `explicit.stat_210067635@T2` | 0.71895 |
| `explicit.stat_691932474@T1` | -0.67288 |
| `explicit.stat_387439868@T2` | -0.64442 |
| `crafted.stat_3035140377` | 0.58465 |

## Coverage (listings per base)

- … **Sapphire** — 31992 listings (31938 priced) [0.3–885594757.8 ex]
- … **Emerald** — 31096 listings (31055 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 23838 listings (23808 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11574 listings (11559 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10371 listings (10349 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10039 listings (10015 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9903 listings (9893 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 9371 listings (9352 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9246 listings (9226 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8894 listings (8881 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7694 listings (7680 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7424 listings (7416 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7304 listings (7297 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6878 listings (6857 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6438 listings (6431 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 6350 listings (6322 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 6345 listings (6328 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6327 listings (6315 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6304 listings (6297 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6226 listings (6199 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6138 listings (6129 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 6073 listings (6066 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5770 listings (5767 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5701 listings (5688 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5622 listings (5613 priced) [0.3–398912568423.8 ex]

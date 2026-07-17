# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-17T22:32:44+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **596477** (594731 priced in exalted)
- Distinct bases: 990 · distinct mods: 3218 · mod rows: 2825704
- Sold signals: **25190** sold · 338728 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-17T22:21:43+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.18** (median |log error| 3.1854)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×58.57 · ±30% 5% · n=86785
- Premium segment (60ex+): skill **+0.14** · typical error ×251.94 · ±30% 0% · n=58654

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 12322 | ×54.20 | 21% | +0.03 | +0.04 |
| jewel | 11619 | ×11.01 | 4% | +0.08 | +0.11 |
| accessory.amulet | 11278 | ×49.94 | 19% | +0.03 | +0.04 |
| accessory.belt | 8292 | ×16.68 | 4% | +0.01 | +0.03 |
| armour.chest | 8062 | ×18.25 | 11% | +0.10 | +0.13 |
| armour.helmet | 7879 | ×19.11 | 7% | +0.13 | +0.15 |
| armour.boots | 7256 | ×34.59 | 17% | +0.11 | +0.13 |
| armour.gloves | 7174 | ×37.26 | 10% | +0.10 | +0.13 |
| other | 6954 | ×3.16 | 41% | +0.09 | +0.16 |
| weapon.wand | 4362 | ×52.19 | 17% | +0.08 | +0.10 |
| weapon.bow | 3426 | ×27.09 | 12% | +0.15 | +0.17 |
| weapon.crossbow | 3239 | ×34.22 | 14% | +0.10 | +0.14 |
| weapon.warstaff | 2105 | ×29.97 | 7% | +0.16 | +0.14 |
| weapon.staff | 1980 | ×44.75 | 6% | +0.13 | +0.13 |
| weapon.sceptre | 1939 | ×33.17 | 5% | +0.19 | +0.19 |
| weapon.spear | 1556 | ×40.92 | 12% | +0.09 | +0.09 |
| armour.focus | 1303 | ×23.15 | 6% | +0.16 | +0.16 |
| armour.quiver | 1244 | ×25.26 | 7% | +0.15 | +0.15 |
| flask.charm | 1090 | ×18.18 | 31% | +0.02 | +0.06 |
| armour.shield | 1013 | ×19.60 | 7% | +0.05 | +0.07 |
| weapon.twomace | 935 | ×10.31 | 10% | +0.09 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=63069, R²=-0.9453

intercept: `-1.8569`  ·  log_price: True  ·  ilvl: `0.02571`  ·  n_mods: `0.85753`  ·  n_top_tier: `-0.33191`  ·  corrupted: `0.28114`  ·  quality: `0.22692`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.53275 |
| `explicit.stat_3374165039@T1` | -2.23751 |
| `explicit.stat_1805182458@T1` | -2.14483 |
| `explicit.stat_3485067555@T1` | 2.00147 |
| `explicit.stat_1062710370@T1` | -1.55830 |
| `explicit.stat_2523933828@T1` | -1.51379 |
| `explicit.stat_2301718443@T1` | 1.45245 |
| `explicit.stat_239367161@T1` | -1.45226 |
| `explicit.stat_3166958180@T1` | -1.44697 |
| `explicit.stat_3174700878@T1` | 1.37251 |
| `explicit.stat_1315743832@T1` | -1.32528 |
| `explicit.stat_1869147066@T1` | -1.32482 |

### other — n=57167, R²=-0.4883

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.64043`  ·  corrupted: `0.18403`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2106365538@T1` | -1.04798 |
| `explicit.stat_3299347043@T1` | 0.96457 |
| `explicit.stat_3141070085@T1` | -0.91876 |
| `explicit.stat_1050105434@T1` | -0.69043 |
| `explicit.stat_789117908@T1` | -0.64718 |
| `explicit.stat_2974417149@T1` | 0.23247 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_1589917703@T1` | -0.12957 |
| `explicit.stat_2231156303@T1` | -0.11285 |
| `explicit.stat_3917489142@T1` | 0.09632 |

### accessory.ring — n=56460, R²=-2.0424

intercept: `3.3421`  ·  log_price: True  ·  ilvl: `-0.04137`  ·  n_mods: `0.00096`  ·  n_top_tier: `1.02732`  ·  corrupted: `0.02066`  ·  n_sockets: `-0.18422`  ·  quality: `0.02090`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -1.07007 |
| `explicit.stat_1573130764@T1` | -1.06906 |
| `explicit.stat_1573130764@T2` | -1.05604 |
| `explicit.stat_1368271171@T2` | -1.04980 |
| `explicit.stat_2231156303@T2` | -1.04976 |
| `explicit.stat_4220027924@T2` | -1.04873 |
| `explicit.stat_2144192055@T1` | -1.04366 |
| `explicit.stat_1368271171@T1` | -1.04363 |
| `explicit.stat_789117908@T1` | -1.04288 |
| `explicit.stat_4080418644@T1` | -1.04225 |
| `explicit.stat_3291658075@T2` | -1.04186 |
| `explicit.stat_789117908@T2` | -1.04185 |

### accessory.amulet — n=51479, R²=-2.1528

intercept: `3.7679`  ·  log_price: True  ·  ilvl: `-0.04587`  ·  n_mods: `-0.01977`  ·  n_top_tier: `1.11276`  ·  corrupted: `0.03637`  ·  n_sockets: `-0.13442`  ·  quality: `0.00177`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.43704 |
| `explicit.stat_3299347043@T2` | -1.25224 |
| `explicit.stat_2974417149@T2` | -1.17821 |
| `explicit.stat_2974417149@T1` | -1.17184 |
| `explicit.stat_2866361420@T2` | -1.17065 |
| `explicit.stat_472520716@T2` | -1.17050 |
| `explicit.stat_803737631@T1` | -1.16189 |
| `explicit.stat_587431675@T2` | -1.16041 |
| `explicit.stat_2866361420@T1` | -1.15316 |
| `explicit.stat_1050105434@T2` | -1.15238 |
| `explicit.stat_803737631@T2` | -1.14419 |
| `explicit.stat_1671376347@T2` | -1.14036 |

### accessory.belt — n=38187, R²=-0.7379

intercept: `6.9599`  ·  log_price: True  ·  ilvl: `-0.05945`  ·  n_mods: `-0.41187`  ·  n_top_tier: `0.69413`  ·  corrupted: `0.90370`  ·  n_sockets: `0.09431`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.67268 |
| `implicit.stat_731781020` | -1.35791 |
| `explicit.stat_3299347043@T2` | -1.30998 |
| `explicit.stat_2881298780@T1` | -1.17504 |
| `explicit.stat_644456512@T1` | -1.08454 |
| `explicit.stat_51994685@T1` | -1.03404 |
| `explicit.stat_1389754388@T1` | -0.89895 |
| `explicit.stat_809229260@T2` | -0.86282 |
| `explicit.stat_4220027924@T2` | -0.84457 |
| `explicit.stat_809229260@T1` | -0.77070 |
| `explicit.stat_3372524247@T2` | -0.73151 |
| `explicit.stat_1671376347@T2` | -0.69341 |

### armour.chest — n=37908, R²=-1.4175

intercept: `4.2008`  ·  log_price: True  ·  ilvl: `-0.05005`  ·  n_mods: `-0.07050`  ·  n_top_tier: `0.52013`  ·  corrupted: `0.22773`  ·  n_sockets: `0.12544`  ·  quality: `0.06036`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.73985 |
| `explicit.stat_3981240776@T1` | 0.97545 |
| `explicit.stat_986397080@T2` | -0.81270 |
| `explicit.stat_986397080@T1` | -0.72598 |
| `explicit.stat_3484657501@T1` | -0.71588 |
| `explicit.stat_3033371881@T1` | 0.71377 |
| `explicit.stat_124859000@T1` | -0.63077 |
| `explicit.stat_915769802@T2` | -0.61097 |
| `explicit.stat_2339757871@T2` | -0.60616 |
| `explicit.stat_3299347043@T2` | -0.60151 |
| `explicit.stat_1692879867@T2` | -0.59677 |
| `explicit.stat_1692879867@T1` | -0.58934 |

### armour.helmet — n=36802, R²=-1.1485

intercept: `3.8918`  ·  log_price: True  ·  ilvl: `-0.04863`  ·  n_mods: `-0.08901`  ·  n_top_tier: `0.51524`  ·  corrupted: `0.70808`  ·  n_sockets: `0.22582`  ·  quality: `0.04560`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | -3.94043 |
| `explicit.stat_2339757871@T1` | -2.62928 |
| `explicit.stat_3917489142@T2` | -1.16190 |
| `explicit.stat_1999113824@T1` | -0.90407 |
| `explicit.stat_3917489142@T1` | -0.83350 |
| `explicit.stat_1263695895@T1` | -0.83260 |
| `explicit.stat_4052037485@T2` | -0.72524 |
| `explicit.stat_2162097452@T2` | -0.71332 |
| `explicit.stat_803737631@T2` | -0.67158 |
| `explicit.stat_3321629045@T2` | -0.66467 |
| `explicit.stat_803737631@T1` | -0.65640 |
| `explicit.stat_1050105434@T2` | -0.65170 |

### armour.boots — n=34249, R²=-1.534

intercept: `3.8609`  ·  log_price: True  ·  ilvl: `-0.04708`  ·  n_mods: `-0.03822`  ·  n_top_tier: `0.63373`  ·  corrupted: `0.03310`  ·  n_sockets: `0.06773`  ·  quality: `0.05513`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.43081 |
| `explicit.stat_2250533757@T1` | 1.45571 |
| `explicit.stat_2339757871@T1` | -1.13581 |
| `explicit.stat_3917489142@T2` | -1.00926 |
| `explicit.stat_3299347043@T1` | -0.96440 |
| `explicit.stat_3917489142@T1` | -0.87954 |
| `explicit.stat_2923486259@T2` | -0.80374 |
| `explicit.stat_1062208444@T2` | -0.72937 |
| `explicit.stat_3484657501@T2` | -0.71434 |
| `explicit.stat_2160282525@T1` | -0.71067 |
| `explicit.stat_4052037485@T2` | -0.69594 |
| `explicit.stat_3299347043@T2` | -0.69215 |

### armour.gloves — n=33414, R²=-1.4656

intercept: `3.9812`  ·  log_price: True  ·  ilvl: `-0.05122`  ·  n_mods: `-0.03930`  ·  n_top_tier: `0.71414`  ·  corrupted: `-0.01884`  ·  n_sockets: `0.16968`  ·  quality: `0.04105`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.95237 |
| `rune.stat_201332984` | 1.46316 |
| `rune.stat_836936635` | 1.43160 |
| `explicit.stat_2923486259@T1` | -1.17797 |
| `explicit.stat_3484657501@T2` | -1.15726 |
| `explicit.stat_3321629045@T2` | -1.07199 |
| `explicit.stat_3484657501@T1` | -0.99120 |
| `explicit.stat_803737631@T2` | -0.88859 |
| `explicit.stat_4052037485@T1` | -0.86847 |
| `explicit.stat_3321629045@T1` | -0.86836 |
| `explicit.stat_803737631@T1` | -0.86390 |
| `explicit.stat_9187492@T2` | -0.85900 |

### weapon.wand — n=20523, R²=-2.0929

intercept: `3.6652`  ·  log_price: True  ·  ilvl: `-0.04525`  ·  n_mods: `-0.04036`  ·  n_top_tier: `0.40284`  ·  corrupted: `0.11789`  ·  n_sockets: `0.10173`  ·  quality: `0.00476`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.75583 |
| `rune.stat_124131830` | -2.59487 |
| `explicit.stat_2254480358@T1` | 2.39334 |
| `explicit.stat_4226189338@T1` | 2.05796 |
| `explicit.stat_124131830@T1` | 1.86381 |
| `explicit.stat_591105508@T1` | 1.85179 |
| `explicit.stat_736967255@T2` | 1.74325 |
| `crafted.stat_124131830` | 1.25264 |
| `explicit.stat_4226189338@T2` | 1.04615 |
| `explicit.stat_2254480358@T2` | 1.01111 |
| `explicit.stat_1600707273@T2` | -0.70933 |
| `explicit.stat_3962278098@T2` | -0.70164 |

### weapon.bow — n=16435, R²=-1.7093

intercept: `3.7617`  ·  log_price: True  ·  ilvl: `-0.04212`  ·  n_mods: `-0.13915`  ·  n_top_tier: `0.56077`  ·  corrupted: `0.30349`  ·  n_sockets: `0.08345`  ·  quality: `0.02721`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.48418 |
| `desecrated.stat_210067635@T1` | -1.30905 |
| `explicit.stat_2463230181@T1` | -1.27063 |
| `explicit.stat_1263695895@T1` | -1.14260 |
| `explicit.stat_1263695895@T2` | -0.98468 |
| `explicit.stat_1202301673@T1` | 0.94139 |
| `explicit.stat_3336890334@T1` | 0.91028 |
| `explicit.stat_1509134228@T1` | -0.90235 |
| `explicit.stat_3695891184@T2` | -0.84555 |
| `explicit.stat_518292764@T2` | -0.82947 |
| `explicit.stat_3695891184@T1` | -0.82155 |
| `explicit.stat_2463230181@T2` | -0.79323 |

### flask.charm — n=16000, R²=-0.5834

intercept: `0.0730`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `2.27582`  ·  corrupted: `1.60850`  ·  quality: `0.00004`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.86068 |
| `explicit.stat_1056492907` | 2.96896 |
| `explicit.stat_828533480@T2` | -2.27585 |
| `explicit.stat_1873752457@T2` | -2.27582 |
| `explicit.stat_1120862500@T2` | -2.27581 |
| `explicit.stat_388617051@T2` | -2.27580 |
| `explicit.stat_2676834156@T2` | -2.27580 |
| `explicit.stat_1873752457@T1` | -2.27580 |
| `explicit.stat_3196823591@T2` | -2.27579 |
| `explicit.stat_2365392475@T2` | -2.27578 |
| `explicit.stat_1366840608@T2` | -2.27491 |
| `explicit.stat_828533480@T1` | -2.27440 |

### weapon.crossbow — n=15407, R²=-1.7012

intercept: `3.9167`  ·  log_price: True  ·  ilvl: `-0.04618`  ·  n_mods: `-0.10127`  ·  n_top_tier: `0.59550`  ·  corrupted: `0.03422`  ·  n_sockets: `0.08414`  ·  quality: `0.02177`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.75041 |
| `explicit.stat_1980802737` | 1.34088 |
| `explicit.stat_2250681686@T2` | -1.20218 |
| `explicit.stat_1202301673@T1` | 1.00376 |
| `explicit.stat_1263695895@T2` | -0.85909 |
| `explicit.stat_2250681686` | 0.85619 |
| `explicit.stat_1940865751@T2` | -0.81265 |
| `explicit.stat_1263695895@T1` | -0.79572 |
| `explicit.stat_709508406@T1` | 0.78849 |
| `explicit.stat_1037193709@T1` | -0.77465 |
| `explicit.stat_2694482655@T1` | -0.76982 |
| `explicit.stat_3695891184@T2` | -0.73969 |

### weapon.warstaff — n=10117, R²=-0.3584

intercept: `-10.6806`  ·  log_price: True  ·  ilvl: `0.14617`  ·  n_mods: `-0.25048`  ·  n_top_tier: `0.24312`  ·  corrupted: `0.38956`  ·  n_sockets: `0.18305`  ·  quality: `0.06376`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 2.61674 |
| `desecrated.stat_2527686725@T1` | 2.61674 |
| `desecrated.stat_473429811@T1` | -1.87724 |
| `desecrated.stat_3291658075@T1` | -1.87724 |
| `crafted.stat_210067635@T2` | 1.45270 |
| `rune.stat_243313994` | 0.96330 |
| `explicit.stat_1037193709@T1` | 0.88202 |
| `explicit.stat_328541901@T1` | -0.83788 |
| `explicit.stat_328541901@T2` | -0.78466 |
| `explicit.stat_709508406@T1` | 0.74068 |
| `desecrated.stat_9187492` | 0.72741 |
| `explicit.stat_1509134228@T1` | 0.70513 |

### weapon.staff — n=9432, R²=-0.3757

intercept: `-14.9920`  ·  log_price: True  ·  ilvl: `0.19470`  ·  n_mods: `-0.13704`  ·  n_top_tier: `0.51784`  ·  corrupted: `0.40224`  ·  n_sockets: `0.27941`  ·  quality: `0.03342`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.08288 |
| `explicit.stat_1545858329@T1` | 1.90890 |
| `explicit.stat_591105508@T1` | 1.56129 |
| `explicit.stat_124131830@T1` | 1.30442 |
| `explicit.stat_293638271@T2` | -1.26822 |
| `explicit.stat_2254480358@T2` | 1.13729 |
| `explicit.stat_591105508@T2` | 0.92184 |
| `explicit.stat_124131830@T2` | 0.90588 |
| `explicit.stat_1600707273@T1` | 0.73693 |
| `explicit.stat_274716455@T1` | -0.64500 |
| `explicit.stat_2254480358@T1` | 0.64468 |
| `explicit.stat_4226189338@T2` | 0.63139 |

### weapon.sceptre — n=9326, R²=-0.3353

intercept: `-20.4809`  ·  log_price: True  ·  ilvl: `0.26303`  ·  n_mods: `-0.05917`  ·  n_top_tier: `0.11067`  ·  corrupted: `0.43268`  ·  n_sockets: `0.29595`  ·  quality: `0.03320`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 3.00013 |
| `explicit.stat_2162097452@T2` | 1.66621 |
| `explicit.stat_1250712710@T2` | 1.64648 |
| `explicit.stat_3057012405@T1` | 1.16534 |
| `explicit.stat_2347036682@T1` | 0.81155 |
| `explicit.stat_101878827@T1` | 0.75280 |
| `explicit.stat_101878827@T2` | 0.58403 |
| `explicit.stat_1798257884@T2` | 0.49509 |
| `explicit.stat_849987426@T1` | 0.48196 |
| `explicit.stat_4010677958@T1` | 0.45787 |
| `explicit.stat_1250712710@T1` | 0.44718 |
| `explicit.stat_2347036682@T2` | -0.43554 |

### weapon.spear — n=7584, R²=-0.4196

intercept: `-12.0534`  ·  log_price: True  ·  ilvl: `0.16897`  ·  n_mods: `-0.17715`  ·  n_top_tier: `0.81949`  ·  corrupted: `0.04502`  ·  n_sockets: `0.18735`  ·  quality: `0.06023`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -5.40326 |
| `explicit.stat_1202301673@T1` | 1.55083 |
| `desecrated.stat_210067635@T1` | -1.17600 |
| `explicit.stat_9187492@T1` | 1.15770 |
| `explicit.stat_9187492@T2` | -1.09092 |
| `crafted.stat_3035140377` | 1.08186 |
| `explicit.stat_4080418644@T2` | -1.07510 |
| `explicit.stat_3261801346@T1` | -1.00720 |
| `explicit.stat_1509134228@T1` | 1.00640 |
| `explicit.stat_1940865751@T2` | -0.92759 |
| `explicit.stat_691932474@T1` | -0.92687 |
| `explicit.stat_3261801346@T2` | -0.90888 |

### armour.focus — n=6222, R²=-0.3658

intercept: `-13.4901`  ·  log_price: True  ·  ilvl: `0.17745`  ·  n_mods: `-0.18566`  ·  n_top_tier: `0.83336`  ·  corrupted: `0.32628`  ·  n_sockets: `0.40753`  ·  quality: `0.06403`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 1.62592 |
| `explicit.stat_4220027924@T2` | -1.41191 |
| `explicit.stat_4220027924@T1` | -1.24705 |
| `explicit.stat_2231156303@T2` | -1.24289 |
| `explicit.stat_2231156303@T1` | -1.13843 |
| `explicit.stat_3291658075@T1` | -0.99330 |
| `explicit.stat_2974417149@T1` | -0.98211 |
| `explicit.stat_2923486259@T1` | -0.96195 |
| `explicit.stat_2339757871@T2` | -0.86492 |
| `explicit.stat_737908626@T2` | -0.79407 |
| `explicit.stat_2974417149@T2` | -0.79280 |
| `crafted.stat_737908626@T2` | -0.77307 |

### armour.quiver — n=5828, R²=-0.3165

intercept: `-13.6163`  ·  log_price: True  ·  ilvl: `0.17058`  ·  n_mods: `-0.15586`  ·  n_top_tier: `0.86627`  ·  corrupted: `0.74763`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.86876 |
| `explicit.stat_2463230181@T1` | 3.33193 |
| `explicit.stat_2463230181@T2` | 1.72587 |
| `explicit.stat_681332047@T2` | -1.35384 |
| `explicit.stat_1573130764@T1` | -1.25085 |
| `explicit.stat_803737631@T2` | -1.12733 |
| `explicit.stat_2321178454@T2` | -1.05312 |
| `explicit.stat_803737631@T1` | -0.97420 |
| `explicit.stat_4067062424@T1` | -0.91503 |
| `explicit.stat_1573130764@T2` | -0.91204 |
| `explicit.stat_3261801346@T1` | -0.86505 |
| `explicit.stat_2194114101@T2` | -0.84856 |

### armour.shield — n=5039, R²=-0.4879

intercept: `-11.0356`  ·  log_price: True  ·  ilvl: `0.14777`  ·  n_mods: `-0.10282`  ·  n_top_tier: `0.78622`  ·  corrupted: `-0.32789`  ·  n_sockets: `0.32070`  ·  quality: `0.05954`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.43006 |
| `explicit.stat_3321629045@T2` | -1.34457 |
| `explicit.stat_3033371881@T2` | -1.16839 |
| `explicit.stat_2481353198@T2` | -1.15473 |
| `explicit.stat_3484657501@T2` | -1.09078 |
| `explicit.stat_2923486259@T2` | -1.07779 |
| `explicit.stat_3855016469@T1` | -1.02769 |
| `explicit.stat_2451402625@T1` | -1.02394 |
| `explicit.stat_2451402625@T2` | -0.96841 |
| `explicit.stat_2923486259@T1` | -0.94718 |
| `explicit.stat_2481353198@T1` | -0.92619 |
| `explicit.stat_3372524247@T2` | -0.87920 |

### weapon.twomace — n=4631, R²=-0.4793

intercept: `-8.9698`  ·  log_price: True  ·  ilvl: `0.12445`  ·  n_mods: `-0.20315`  ·  n_top_tier: `0.34114`  ·  corrupted: `-0.14349`  ·  n_sockets: `0.15536`  ·  quality: `0.06634`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.91952 |
| `desecrated.stat_1509134228@T1` | 1.55373 |
| `explicit.stat_1037193709@T1` | -1.41283 |
| `explicit.stat_1263695895@T2` | -0.86475 |
| `crafted.stat_3035140377` | 0.78136 |
| `explicit.stat_387439868@T2` | -0.71646 |
| `explicit.stat_691932474@T1` | -0.63530 |
| `explicit.stat_210067635@T2` | 0.57262 |
| `explicit.stat_1037193709@T2` | -0.56922 |
| `explicit.stat_3336890334@T1` | -0.56537 |
| `explicit.stat_518292764@T2` | -0.54135 |
| `explicit.stat_1509134228@T1` | 0.53445 |

## Coverage (listings per base)

- … **Sapphire** — 29262 listings (29212 priced) [0.3–885594757.8 ex]
- … **Emerald** — 28602 listings (28561 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 21921 listings (21895 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10911 listings (10896 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 9628 listings (9607 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 9296 listings (9275 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9181 listings (9173 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8706 listings (8690 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8561 listings (8542 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8364 listings (8352 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7131 listings (7121 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6822 listings (6816 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6800 listings (6794 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6583 listings (6562 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6005 listings (5998 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 5954 listings (5928 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 5888 listings (5871 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 5877 listings (5866 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 5850 listings (5843 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5807 listings (5781 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5709 listings (5700 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5606 listings (5599 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5365 listings (5362 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5327 listings (5315 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5284 listings (5275 priced) [0.3–398912568423.8 ex]

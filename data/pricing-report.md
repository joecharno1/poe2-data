# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-18T23:09:40+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **632322** (630405 priced in exalted)
- Distinct bases: 993 · distinct mods: 3260 · mod rows: 2995068
- Sold signals: **24806** sold · 359961 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-18T22:56:46+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.57** (median |log error| 3.1168)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.15** · typical error ×59.40 · ±30% 5% · n=92252
- Premium segment (60ex+): skill **+0.15** · typical error ×258.76 · ±30% 0% · n=62631

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 13268 | ×56.49 | 21% | +0.03 | +0.05 |
| jewel | 12525 | ×10.95 | 4% | +0.09 | +0.12 |
| accessory.amulet | 12045 | ×48.34 | 19% | +0.04 | +0.04 |
| accessory.belt | 8783 | ×17.63 | 5% | +0.05 | +0.08 |
| armour.chest | 8503 | ×16.86 | 12% | +0.10 | +0.12 |
| armour.helmet | 8330 | ×21.60 | 9% | +0.12 | +0.14 |
| armour.boots | 7732 | ×33.51 | 19% | +0.10 | +0.13 |
| armour.gloves | 7549 | ×36.22 | 14% | +0.09 | +0.12 |
| other | 7430 | ×2.01 | 42% | +0.10 | +0.16 |
| weapon.wand | 4565 | ×41.49 | 14% | +0.10 | +0.11 |
| weapon.bow | 3591 | ×26.89 | 12% | +0.15 | +0.15 |
| weapon.crossbow | 3362 | ×31.65 | 14% | +0.10 | +0.15 |
| weapon.warstaff | 2246 | ×23.17 | 6% | +0.20 | +0.18 |
| weapon.staff | 2117 | ×29.19 | 6% | +0.16 | +0.14 |
| weapon.sceptre | 2081 | ×28.82 | 5% | +0.13 | +0.13 |
| weapon.spear | 1650 | ×27.96 | 8% | +0.11 | +0.13 |
| armour.focus | 1383 | ×17.79 | 7% | +0.11 | +0.11 |
| armour.quiver | 1321 | ×25.72 | 7% | +0.16 | +0.18 |
| armour.shield | 1095 | ×17.66 | 9% | +0.08 | +0.10 |
| flask.charm | 1062 | ×16.34 | 30% | +0.00 | +0.03 |
| weapon.twomace | 1012 | ×7.21 | 9% | +0.09 | +0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=68059, R²=-0.9523

intercept: `-1.9057`  ·  log_price: True  ·  ilvl: `0.02576`  ·  n_mods: `0.89124`  ·  n_top_tier: `-0.35438`  ·  corrupted: `0.32705`  ·  quality: `-0.00511`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.02414 |
| `explicit.stat_3374165039@T1` | -2.14762 |
| `explicit.stat_3485067555@T1` | 2.06673 |
| `explicit.stat_3780644166@T1` | -1.96878 |
| `explicit.stat_2523933828@T1` | -1.77852 |
| `explicit.stat_4147897060@T1` | -1.64497 |
| `explicit.stat_1697447343@T1` | -1.55308 |
| `explicit.stat_318953428@T1` | -1.55154 |
| `explicit.stat_21071013@T1` | 1.44535 |
| `explicit.stat_1805182458@T1` | -1.42358 |
| `explicit.stat_3174700878@T1` | 1.35464 |
| `explicit.stat_3787460122@T1` | 1.25246 |

### accessory.ring — n=60459, R²=-2.0246

intercept: `3.4255`  ·  log_price: True  ·  ilvl: `-0.04233`  ·  n_mods: `-0.00005`  ·  n_top_tier: `1.12787`  ·  corrupted: `0.02512`  ·  n_sockets: `0.29711`  ·  quality: `0.02022`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.17520 |
| `explicit.stat_1573130764@T2` | -1.16837 |
| `explicit.stat_2231156303@T1` | -1.16289 |
| `explicit.stat_803737631@T1` | -1.15745 |
| `explicit.stat_3325883026@T1` | -1.15015 |
| `explicit.stat_4220027924@T2` | -1.14810 |
| `explicit.stat_789117908@T2` | -1.14441 |
| `explicit.stat_2144192055@T1` | -1.14181 |
| `explicit.stat_4080418644@T1` | -1.14179 |
| `explicit.stat_2923486259@T2` | -1.14080 |
| `explicit.stat_1263695895@T1` | -1.13985 |
| `explicit.stat_3325883026@T2` | -1.13963 |

### other — n=60372, R²=-0.6259

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00003`  ·  n_top_tier: `0.34788`  ·  corrupted: `0.32241`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.41287 |
| `implicit.stat_2219129443` | 0.41239 |
| `explicit.stat_3299347043@T1` | -0.24898 |
| `implicit.stat_3879011313` | 0.24130 |
| `explicit.stat_2974417149@T1` | 0.13703 |
| `implicit.stat_4041853756` | 0.13257 |
| `explicit.stat_3917489142@T1` | 0.09571 |
| `explicit.stat_3291658075@T1` | -0.09527 |
| `explicit.stat_2482852589@T1` | 0.08706 |
| `implicit.stat_1379411836` | -0.08399 |
| `explicit.stat_789117908@T1` | -0.07398 |
| `explicit.stat_736967255@T1` | 0.07206 |

### accessory.amulet — n=54872, R²=-2.1648

intercept: `3.6917`  ·  log_price: True  ·  ilvl: `-0.04509`  ·  n_mods: `-0.02056`  ·  n_top_tier: `1.36882`  ·  corrupted: `0.05238`  ·  n_sockets: `-0.15690`  ·  quality: `0.00477`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.93926 |
| `explicit.stat_3299347043@T2` | -1.70150 |
| `explicit.stat_2974417149@T1` | -1.44975 |
| `explicit.stat_587431675@T2` | -1.44010 |
| `explicit.stat_803737631@T1` | -1.43230 |
| `explicit.stat_2974417149@T2` | -1.42869 |
| `explicit.stat_2866361420@T2` | -1.42522 |
| `explicit.stat_1050105434@T2` | -1.41771 |
| `explicit.stat_2866361420@T1` | -1.41670 |
| `explicit.stat_472520716@T2` | -1.41001 |
| `explicit.stat_803737631@T2` | -1.40369 |
| `explicit.stat_3261801346@T1` | -1.39988 |

### accessory.belt — n=40272, R²=-0.9783

intercept: `6.4930`  ·  log_price: True  ·  ilvl: `-0.06251`  ·  n_mods: `-0.25674`  ·  n_top_tier: `0.70178`  ·  corrupted: `1.10914`  ·  n_sockets: `0.44792`

| stat_id | coef |
|---|---|
| `implicit.stat_731781020` | -1.71249 |
| `explicit.stat_3299347043@T1` | -1.35095 |
| `explicit.stat_2881298780@T1` | -1.00372 |
| `explicit.stat_3299347043@T2` | -0.98759 |
| `explicit.stat_644456512@T1` | -0.84299 |
| `explicit.stat_51994685@T1` | -0.84121 |
| `explicit.stat_1570770415@T2` | -0.83778 |
| `explicit.stat_1389754388@T1` | -0.83361 |
| `explicit.stat_3372524247@T2` | -0.82309 |
| `explicit.stat_809229260@T2` | -0.75824 |
| `explicit.stat_1570770415@T1` | -0.73535 |
| `explicit.stat_4220027924@T2` | -0.73495 |

### armour.chest — n=39870, R²=-1.4688

intercept: `3.9030`  ·  log_price: True  ·  ilvl: `-0.04751`  ·  n_mods: `-0.05677`  ·  n_top_tier: `0.38976`  ·  corrupted: `0.17118`  ·  n_sockets: `0.10443`  ·  quality: `0.05817`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.96002 |
| `explicit.stat_3981240776@T1` | 0.92077 |
| `explicit.stat_3484657501@T1` | -0.64698 |
| `explicit.stat_3372524247@T1` | 0.59878 |
| `explicit.stat_986397080@T2` | -0.58839 |
| `explicit.stat_3033371881@T1` | 0.54544 |
| `explicit.stat_986397080@T1` | -0.53418 |
| `explicit.stat_1692879867@T2` | -0.50204 |
| `explicit.stat_2339757871@T2` | -0.48923 |
| `explicit.stat_3299347043@T2` | -0.47319 |
| `explicit.stat_915769802@T2` | -0.47286 |
| `explicit.stat_3301100256@T2` | -0.45479 |

### armour.helmet — n=38813, R²=-1.2886

intercept: `3.8374`  ·  log_price: True  ·  ilvl: `-0.04798`  ·  n_mods: `-0.07294`  ·  n_top_tier: `0.51742`  ·  corrupted: `0.68609`  ·  n_sockets: `0.12371`  ·  quality: `0.05583`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.07426 |
| `crafted.stat_3917489142@T1` | -2.39032 |
| `explicit.stat_3917489142@T2` | -1.21994 |
| `explicit.stat_3917489142@T1` | -0.96994 |
| `explicit.stat_1999113824@T1` | -0.78777 |
| `explicit.stat_1263695895@T1` | -0.77534 |
| `explicit.stat_803737631@T1` | -0.74129 |
| `explicit.stat_803737631@T2` | -0.68682 |
| `explicit.stat_2162097452@T2` | -0.67298 |
| `explicit.stat_1263695895@T2` | -0.67087 |
| `explicit.stat_3321629045@T2` | -0.65678 |
| `explicit.stat_4052037485@T2` | -0.61264 |

### armour.boots — n=36108, R²=-1.661

intercept: `3.7164`  ·  log_price: True  ·  ilvl: `-0.04545`  ·  n_mods: `-0.02847`  ·  n_top_tier: `0.65700`  ·  corrupted: `-0.01221`  ·  n_sockets: `0.03790`  ·  quality: `0.06145`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.56457 |
| `explicit.stat_2339757871@T1` | -1.14781 |
| `crafted.stat_3917489142@T1` | 1.11162 |
| `explicit.stat_3299347043@T1` | -0.85429 |
| `explicit.stat_3917489142@T2` | -0.83860 |
| `explicit.stat_2923486259@T2` | -0.74861 |
| `explicit.stat_3917489142@T1` | -0.72840 |
| `explicit.stat_1062208444@T2` | -0.71562 |
| `explicit.stat_2160282525@T1` | -0.71538 |
| `explicit.stat_1874553720@T1` | -0.69817 |
| `explicit.stat_4052037485@T2` | -0.68532 |
| `explicit.stat_3484657501@T2` | -0.68434 |

### armour.gloves — n=35174, R²=-1.6051

intercept: `3.8364`  ·  log_price: True  ·  ilvl: `-0.04913`  ·  n_mods: `-0.03400`  ·  n_top_tier: `0.69885`  ·  corrupted: `0.00966`  ·  n_sockets: `0.11462`  ·  quality: `0.04671`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 4.41846 |
| `explicit.stat_2923486259@T1` | -1.38124 |
| `rune.stat_201332984` | 1.08310 |
| `explicit.stat_3484657501@T2` | -0.98409 |
| `explicit.stat_3321629045@T2` | -0.95048 |
| `explicit.stat_803737631@T1` | -0.90284 |
| `explicit.stat_3484657501@T1` | -0.90031 |
| `explicit.stat_803737631@T2` | -0.87833 |
| `explicit.stat_9187492@T2` | -0.82306 |
| `explicit.stat_3917489142@T2` | -0.80285 |
| `explicit.stat_2923486259@T2` | -0.80146 |
| `explicit.stat_1062208444@T2` | -0.78507 |

### weapon.wand — n=21306, R²=-1.9256

intercept: `3.7945`  ·  log_price: True  ·  ilvl: `-0.04685`  ·  n_mods: `-0.05733`  ·  n_top_tier: `0.56872`  ·  corrupted: `-0.00014`  ·  n_sockets: `0.06308`  ·  quality: `0.01620`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.77004 |
| `rune.stat_124131830` | -2.57057 |
| `explicit.stat_2254480358@T1` | 2.20106 |
| `explicit.stat_124131830@T1` | 2.12633 |
| `explicit.stat_591105508@T1` | 1.75698 |
| `explicit.stat_4226189338@T1` | 1.73794 |
| `explicit.stat_736967255@T2` | 1.46649 |
| `crafted.stat_124131830` | 1.11666 |
| `explicit.stat_1263695895@T2` | -1.01842 |
| `explicit.stat_1263695895@T1` | -0.97535 |
| `explicit.stat_1600707273@T1` | 0.88170 |
| `explicit.stat_2254480358@T2` | 0.87025 |

### flask.charm — n=17270, R²=-0.6101

intercept: `0.0920`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.44199`  ·  corrupted: `1.60512`  ·  quality: `0.00086`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.71116 |
| `explicit.stat_1056492907` | 2.81607 |
| `explicit.stat_828533480@T2` | -1.44202 |
| `explicit.stat_1873752457@T2` | -1.44198 |
| `explicit.stat_1120862500@T2` | -1.44198 |
| `explicit.stat_388617051@T2` | -1.44196 |
| `explicit.stat_1873752457@T1` | -1.44196 |
| `explicit.stat_3196823591@T2` | -1.44195 |
| `explicit.stat_2365392475@T2` | -1.44194 |
| `explicit.stat_2676834156@T2` | -1.44193 |
| `explicit.stat_828533480@T1` | -1.44107 |
| `explicit.stat_1366840608@T2` | -1.43662 |

### weapon.bow — n=17045, R²=-1.7384

intercept: `3.8025`  ·  log_price: True  ·  ilvl: `-0.04355`  ·  n_mods: `-0.12045`  ·  n_top_tier: `0.68305`  ·  corrupted: `0.39501`  ·  n_sockets: `0.12201`  ·  quality: `0.03046`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.25392 |
| `crafted.stat_3035140377` | 1.34254 |
| `explicit.stat_1263695895@T1` | -1.27574 |
| `explicit.stat_2463230181@T2` | -1.23001 |
| `explicit.stat_2463230181@T1` | -1.03677 |
| `explicit.stat_3336890334@T1` | 1.03319 |
| `explicit.stat_1263695895@T2` | -0.99518 |
| `explicit.stat_1509134228@T1` | -0.92790 |
| `desecrated.stat_210067635@T1` | -0.86219 |
| `explicit.stat_3695891184@T2` | -0.85576 |
| `explicit.stat_3639275092@T1` | -0.83343 |
| `explicit.stat_3639275092@T2` | -0.80993 |

### weapon.crossbow — n=15982, R²=-1.7125

intercept: `3.8534`  ·  log_price: True  ·  ilvl: `-0.04637`  ·  n_mods: `-0.08626`  ·  n_top_tier: `0.47013`  ·  corrupted: `0.06732`  ·  n_sockets: `0.08206`  ·  quality: `0.02292`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.64366 |
| `explicit.stat_1980802737` | 1.32354 |
| `explicit.stat_1202301673@T1` | 1.11041 |
| `explicit.stat_2250681686@T2` | -1.00844 |
| `explicit.stat_2250681686` | 0.88237 |
| `explicit.stat_709508406@T1` | 0.80452 |
| `crafted.stat_3035140377` | 0.71789 |
| `explicit.stat_3336890334@T2` | -0.68779 |
| `explicit.stat_1263695895@T2` | -0.67718 |
| `explicit.stat_1509134228@T2` | -0.65718 |
| `explicit.stat_3336890334@T1` | -0.65612 |
| `explicit.stat_3695891184@T2` | -0.61957 |

### weapon.warstaff — n=10744, R²=-0.3552

intercept: `-10.3248`  ·  log_price: True  ·  ilvl: `0.14056`  ·  n_mods: `-0.23735`  ·  n_top_tier: `0.34609`  ·  corrupted: `0.42606`  ·  n_sockets: `0.15818`  ·  quality: `0.05759`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 2.77646 |
| `desecrated.stat_2527686725@T1` | 2.77646 |
| `crafted.stat_210067635@T2` | 1.28256 |
| `rune.stat_243313994` | 0.88330 |
| `explicit.stat_328541901@T1` | -0.81244 |
| `explicit.stat_328541901@T2` | -0.79973 |
| `desecrated.stat_9187492` | 0.75636 |
| `desecrated.stat_473429811@T1` | -0.75290 |
| `desecrated.stat_3291658075@T1` | -0.75290 |
| `explicit.stat_1509134228@T1` | 0.59860 |
| `explicit.stat_1368271171@T1` | -0.59042 |
| `explicit.stat_691932474@T2` | -0.54455 |

### weapon.staff — n=10091, R²=-0.3869

intercept: `-16.0861`  ·  log_price: True  ·  ilvl: `0.20581`  ·  n_mods: `-0.08474`  ·  n_top_tier: `0.54417`  ·  corrupted: `0.60155`  ·  n_sockets: `0.19985`  ·  quality: `0.03168`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.16178 |
| `explicit.stat_591105508@T1` | 2.09849 |
| `explicit.stat_4226189338@T1` | 1.88326 |
| `explicit.stat_293638271@T2` | -1.47545 |
| `explicit.stat_124131830@T1` | 1.12468 |
| `explicit.stat_1600707273@T1` | 1.04444 |
| `explicit.stat_274716455@T1` | -0.78318 |
| `explicit.stat_591105508@T2` | 0.75930 |
| `explicit.stat_4226189338@T2` | 0.70455 |
| `explicit.stat_2254480358@T2` | 0.68294 |
| `explicit.stat_2254480358@T1` | 0.67354 |
| `explicit.stat_3278136794@T1` | -0.67082 |

### weapon.sceptre — n=9946, R²=-0.3384

intercept: `-20.2072`  ·  log_price: True  ·  ilvl: `0.25977`  ·  n_mods: `-0.00035`  ·  n_top_tier: `0.36758`  ·  corrupted: `-0.00240`  ·  n_sockets: `0.26691`  ·  quality: `0.02978`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.19627 |
| `explicit.stat_1250712710@T2` | 1.28557 |
| `explicit.stat_2162097452@T2` | 1.16280 |
| `explicit.stat_3057012405@T1` | 1.03949 |
| `explicit.stat_2854751904@T2` | -0.77286 |
| `explicit.stat_2347036682@T2` | -0.74743 |
| `explicit.stat_1263695895@T2` | -0.72625 |
| `explicit.stat_3639275092@T2` | -0.69045 |
| `explicit.stat_1798257884@T2` | 0.65536 |
| `explicit.stat_101878827@T2` | 0.62397 |
| `explicit.stat_101878827@T1` | 0.60215 |
| `explicit.stat_849987426@T1` | 0.53754 |

### weapon.spear — n=8018, R²=-0.3773

intercept: `-12.2172`  ·  log_price: True  ·  ilvl: `0.17289`  ·  n_mods: `-0.24029`  ·  n_top_tier: `0.76624`  ·  corrupted: `0.01511`  ·  n_sockets: `0.20602`  ·  quality: `0.07315`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -5.07263 |
| `explicit.stat_1202301673@T1` | 1.45416 |
| `explicit.stat_4080418644@T2` | -1.29475 |
| `explicit.stat_1509134228@T1` | 1.29105 |
| `desecrated.stat_210067635@T1` | -1.29001 |
| `explicit.stat_1940865751@T2` | -1.13738 |
| `explicit.stat_9187492@T1` | 1.10552 |
| `explicit.stat_4080418644@T1` | -1.10136 |
| `explicit.stat_691932474@T1` | -1.03114 |
| `explicit.stat_691932474@T2` | -1.02245 |
| `explicit.stat_9187492@T2` | -1.01134 |
| `crafted.stat_3035140377` | 0.98915 |

### armour.focus — n=6568, R²=-0.3526

intercept: `-14.1137`  ·  log_price: True  ·  ilvl: `0.18293`  ·  n_mods: `-0.20717`  ·  n_top_tier: `0.87887`  ·  corrupted: `0.42737`  ·  n_sockets: `0.41894`  ·  quality: `0.04413`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 1.87283 |
| `explicit.stat_4220027924@T1` | -1.51016 |
| `crafted.stat_737908626@T2` | 1.44800 |
| `explicit.stat_2923486259@T1` | -1.44503 |
| `explicit.stat_4220027924@T2` | -1.35399 |
| `explicit.stat_3291658075@T1` | -1.16233 |
| `explicit.stat_2231156303@T2` | -1.11779 |
| `explicit.stat_2974417149@T2` | -1.03986 |
| `explicit.stat_2974417149@T1` | -1.01897 |
| `explicit.stat_2231156303@T1` | -0.99034 |
| `explicit.stat_736967255@T2` | -0.97268 |
| `explicit.stat_2339757871@T2` | -0.92327 |

### armour.quiver — n=6175, R²=-0.2981

intercept: `-16.1641`  ·  log_price: True  ·  ilvl: `0.19796`  ·  n_mods: `-0.14732`  ·  n_top_tier: `0.83006`  ·  corrupted: `0.75599`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.59122 |
| `explicit.stat_2463230181@T1` | 2.21714 |
| `explicit.stat_681332047@T2` | -1.50028 |
| `explicit.stat_1573130764@T1` | -1.38346 |
| `explicit.stat_681332047@T1` | -1.13144 |
| `explicit.stat_4067062424@T1` | -1.00735 |
| `explicit.stat_803737631@T2` | -0.98975 |
| `explicit.stat_2463230181@T2` | 0.97033 |
| `explicit.stat_803737631@T1` | -0.95689 |
| `explicit.stat_4067062424@T2` | -0.92403 |
| `explicit.stat_1573130764@T2` | -0.92320 |
| `explicit.stat_2194114101@T2` | -0.88154 |

### armour.shield — n=5331, R²=-0.4546

intercept: `-12.3376`  ·  log_price: True  ·  ilvl: `0.16335`  ·  n_mods: `-0.07936`  ·  n_top_tier: `0.57467`  ·  corrupted: `-0.34425`  ·  n_sockets: `0.36861`  ·  quality: `0.06405`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.44119 |
| `explicit.stat_3321629045@T2` | -1.27238 |
| `explicit.stat_3484657501@T1` | -1.26400 |
| `explicit.stat_4095671657@T1` | -1.19160 |
| `explicit.stat_3855016469@T1` | -0.99445 |
| `explicit.stat_3033371881@T2` | -0.97428 |
| `explicit.stat_3484657501@T2` | -0.96652 |
| `explicit.stat_328541901@T1` | -0.88292 |
| `explicit.stat_2901986750@T1` | -0.83977 |
| `explicit.stat_4095671657@T2` | -0.80275 |
| `explicit.stat_2451402625@T1` | -0.73733 |
| `explicit.stat_2881298780@T1` | -0.67481 |

### weapon.twomace — n=4912, R²=-0.4573

intercept: `-10.0553`  ·  log_price: True  ·  ilvl: `0.13882`  ·  n_mods: `-0.20598`  ·  n_top_tier: `0.34809`  ·  corrupted: `0.13274`  ·  n_sockets: `0.13105`  ·  quality: `0.06216`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.97727 |
| `desecrated.stat_1509134228@T1` | 1.67399 |
| `explicit.stat_1037193709@T1` | -1.51538 |
| `explicit.stat_3336890334@T1` | -1.09927 |
| `explicit.stat_9187492@T1` | -0.82169 |
| `explicit.stat_387439868@T2` | -0.72300 |
| `explicit.stat_691932474@T1` | -0.69740 |
| `explicit.stat_1263695895@T2` | -0.68137 |
| `explicit.stat_210067635@T2` | 0.67875 |
| `explicit.stat_2694482655@T1` | 0.67401 |
| `crafted.stat_3035140377` | 0.66965 |
| `explicit.stat_1509134228@T1` | 0.61834 |

## Coverage (listings per base)

- … **Sapphire** — 31572 listings (31518 priced) [0.3–885594757.8 ex]
- … **Emerald** — 30731 listings (30690 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 23488 listings (23458 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 11469 listings (11454 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10263 listings (10241 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 9942 listings (9918 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 9809 listings (9799 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 9264 listings (9245 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9139 listings (9119 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8820 listings (8807 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 7622 listings (7608 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7338 listings (7330 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 7235 listings (7228 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6835 listings (6814 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6376 listings (6369 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 6287 listings (6259 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 6273 listings (6256 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6260 listings (6248 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6238 listings (6231 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6157 listings (6130 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6072 listings (6063 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 6005 listings (5998 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5708 listings (5705 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5655 listings (5642 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5556 listings (5547 priced) [0.3–398912568423.8 ex]

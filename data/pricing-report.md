# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-08T13:27:04+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **328106** (327668 priced in exalted)
- Distinct bases: 956 · distinct mods: 2843 · mod rows: 1557613
- Sold signals: **30303** sold · 174404 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-08T13:17:29+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×15.67** (median |log error| 2.752)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 76% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.05** · typical error ×40.86 · ±30% 13% · n=47626
- Premium segment (60ex+): skill **+0.07** · typical error ×150.45 · ±30% 0% · n=29566

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 6227 | ×11.58 | 4% | +0.03 | +0.04 |
| accessory.amulet | 5895 | ×50.62 | 20% | +0.03 | +0.03 |
| jewel | 5589 | ×8.53 | 6% | +0.02 | +0.05 |
| accessory.belt | 4711 | ×10.00 | 24% | +0.02 | +0.03 |
| armour.chest | 4676 | ×9.96 | 23% | +0.00 | +0.02 |
| armour.helmet | 4613 | ×10.00 | 22% | +0.00 | +0.02 |
| armour.boots | 4315 | ×10.59 | 16% | +0.01 | +0.03 |
| armour.gloves | 4233 | ×10.02 | 20% | +0.00 | +0.01 |
| other | 3942 | ×10.00 | 35% | +0.08 | +0.27 |
| weapon.wand | 2866 | ×32.50 | 22% | +0.06 | +0.07 |
| weapon.bow | 2308 | ×19.77 | 21% | +0.09 | +0.09 |
| weapon.crossbow | 2147 | ×15.15 | 20% | +0.09 | +0.10 |
| weapon.warstaff | 1094 | ×50.00 | 18% | +0.03 | +0.04 |
| weapon.staff | 986 | ×49.00 | 19% | +0.04 | +0.06 |
| weapon.sceptre | 952 | ×46.97 | 13% | +0.07 | +0.05 |
| weapon.spear | 812 | ×34.92 | 19% | +0.03 | +0.04 |
| armour.focus | 702 | ×343.33 | 12% | +0.02 | +0.09 |
| armour.quiver | 624 | ×50.00 | 12% | +0.01 | +0.07 |
| flask.charm | 526 | ×25.00 | 33% | +0.00 | +0.01 |
| armour.shield | 524 | ×21.97 | 19% | +0.02 | +0.03 |
| weapon.twomace | 502 | ×18.77 | 15% | +0.01 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=33779, R²=-0.4546

intercept: `1.6033`  ·  log_price: True  ·  ilvl: `0.00008`  ·  n_mods: `0.02896`  ·  n_top_tier: `0.66398`  ·  corrupted: `1.29733`  ·  n_sockets: `-0.00008`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.82024 |
| `explicit.stat_2106365538@T1` | 3.42488 |
| `explicit.stat_101878827@T1` | 3.09400 |
| `explicit.stat_1589917703@T1` | 2.68449 |
| `explicit.stat_2482852589@T1` | 2.64135 |
| `explicit.stat_1050105434@T1` | -1.37957 |
| `explicit.stat_3917489142@T1` | 1.30078 |
| `explicit.stat_2974417149@T1` | 1.10203 |
| `explicit.stat_789117908@T1` | -1.01720 |
| `explicit.stat_3141070085@T1` | 0.77997 |
| `explicit.stat_2891184298@T1` | 0.65934 |
| `implicit.stat_1379411836` | -0.25442 |

### jewel — n=29853, R²=-0.6307

intercept: `-1.1195`  ·  log_price: True  ·  ilvl: `0.03665`  ·  n_mods: `0.20553`  ·  n_top_tier: `-0.08784`  ·  corrupted: `0.27582`  ·  quality: `0.21486`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.88004 |
| `explicit.stat_1569101201@T1` | 3.25436 |
| `explicit.stat_3741323227@T1` | -3.06390 |
| `explicit.stat_234296660@T1` | -2.22178 |
| `explicit.stat_1316278494@T1` | -2.11833 |
| `explicit.stat_1569159338@T1` | -2.08992 |
| `explicit.stat_1062710370@T1` | -1.97292 |
| `explicit.stat_440490623@T1` | -1.95643 |
| `explicit.stat_1854213750@T1` | -1.93845 |
| `explicit.stat_1697951953@T1` | -1.84400 |
| `explicit.stat_3714003708@T1` | -1.73433 |
| `explicit.stat_21071013@T1` | 1.66847 |

### accessory.ring — n=28689, R²=-1.2085

intercept: `3.7724`  ·  log_price: True  ·  ilvl: `-0.03866`  ·  n_mods: `-0.02016`  ·  n_top_tier: `0.16063`  ·  corrupted: `0.95819`  ·  n_sockets: `0.97932`  ·  quality: `0.05211`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 4.83771 |
| `explicit.stat_707457662@T2` | 4.16774 |
| `explicit.stat_1379411836@T1` | -2.32405 |
| `explicit.stat_1379411836@T2` | -1.87551 |
| `explicit.stat_1368271171@T1` | -1.06758 |
| `explicit.stat_1368271171@T2` | -0.93115 |
| `explicit.stat_707457662` | -0.75809 |
| `explicit.stat_2923486259@T1` | 0.75372 |
| `explicit.stat_2923486259@T2` | 0.74045 |
| `explicit.stat_1671376347@T1` | 0.62951 |
| `explicit.stat_1263695895@T1` | -0.60700 |
| `explicit.stat_2557965901@T1` | 0.56563 |

### accessory.amulet — n=27092, R²=-2.0549

intercept: `4.0838`  ·  log_price: True  ·  ilvl: `-0.04929`  ·  n_mods: `-0.02640`  ·  n_top_tier: `1.10835`  ·  corrupted: `0.07803`  ·  n_sockets: `1.65601`  ·  quality: `-0.00111`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.53177 |
| `explicit.stat_983749596@T2` | -1.43580 |
| `explicit.stat_3299347043@T1` | -1.33483 |
| `explicit.stat_587431675@T1` | -1.22560 |
| `explicit.stat_2748665614@T1` | -1.20719 |
| `explicit.stat_3299347043@T2` | -1.20280 |
| `explicit.stat_3325883026@T1` | -1.17684 |
| `explicit.stat_2748665614@T2` | -1.17619 |
| `explicit.stat_472520716@T2` | -1.17550 |
| `explicit.stat_472520716@T1` | -1.17229 |
| `explicit.stat_3917489142@T2` | -1.16636 |
| `explicit.stat_3917489142@T1` | -1.15646 |

### accessory.belt — n=21847, R²=-0.1306

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.22365`  ·  corrupted: `0.00003`  ·  n_sockets: `-0.00002`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -0.22367 |
| `explicit.stat_51994685@T1` | -0.22366 |
| `explicit.stat_1570770415@T1` | -0.22366 |
| `explicit.stat_1836676211@T2` | -0.22366 |
| `explicit.stat_2923486259@T2` | -0.22366 |
| `explicit.stat_3585532255@T2` | -0.22366 |
| `explicit.stat_644456512@T1` | -0.22366 |
| `explicit.stat_1389754388@T2` | -0.22366 |
| `explicit.stat_1671376347@T2` | -0.22366 |
| `explicit.stat_644456512@T2` | -0.22366 |
| `explicit.stat_4220027924@T2` | -0.22366 |
| `explicit.stat_3299347043@T2` | -0.22365 |

### armour.chest — n=21676, R²=-0.2724

intercept: `2.4119`  ·  log_price: True  ·  ilvl: `-0.00203`  ·  n_mods: `-0.01286`  ·  n_top_tier: `0.10155`  ·  corrupted: `0.03104`  ·  n_sockets: `-0.00028`  ·  quality: `0.00084`

| stat_id | coef |
|---|---|
| `implicit.stat_1978899297` | -0.91824 |
| `rune.stat_836936635` | -0.28470 |
| `explicit.stat_915769802@T1` | -0.13743 |
| `explicit.stat_915769802@T2` | -0.12901 |
| `explicit.stat_3484657501@T1` | -0.12268 |
| `explicit.stat_3325883026@T2` | -0.11887 |
| `explicit.stat_4080418644@T2` | -0.11837 |
| `explicit.stat_3321629045@T1` | -0.11352 |
| `explicit.stat_3261801346@T1` | -0.11315 |
| `explicit.stat_986397080@T2` | -0.11293 |
| `explicit.stat_4015621042@T1` | -0.11086 |
| `explicit.stat_3261801346@T2` | -0.10953 |

### armour.helmet — n=21218, R²=-0.2822

intercept: `2.3029`  ·  log_price: True  ·  ilvl: `-0.00001`  ·  n_mods: `-0.00005`  ·  n_top_tier: `0.11113`  ·  corrupted: `1.38653`  ·  n_sockets: `0.00001`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 0.16835 |
| `explicit.stat_3362812763@T2` | -0.11121 |
| `explicit.stat_4080418644@T2` | -0.11120 |
| `explicit.stat_53045048@T2` | -0.11119 |
| `explicit.stat_3362812763@T1` | -0.11117 |
| `explicit.stat_2451402625@T1` | -0.11116 |
| `explicit.stat_803737631@T2` | -0.11116 |
| `explicit.stat_1062208444@T2` | -0.11116 |
| `explicit.stat_4080418644@T1` | -0.11115 |
| `explicit.stat_4052037485@T2` | -0.11115 |
| `explicit.stat_53045048@T1` | -0.11114 |
| `explicit.stat_3033371881@T1` | -0.11113 |

### armour.boots — n=20048, R²=-0.3664

intercept: `3.1436`  ·  log_price: True  ·  ilvl: `-0.01929`  ·  n_mods: `-0.10142`  ·  n_top_tier: `0.38042`  ·  corrupted: `0.29533`  ·  n_sockets: `0.04626`  ·  quality: `0.00823`

| stat_id | coef |
|---|---|
| `explicit.stat_1062208444@T2` | -0.68936 |
| `explicit.stat_2451402625@T2` | -0.63759 |
| `explicit.stat_328541901@T1` | -0.55285 |
| `explicit.stat_3321629045@T1` | -0.55095 |
| `explicit.stat_1062208444@T1` | -0.54663 |
| `explicit.stat_3362812763@T1` | -0.52244 |
| `desecrated.stat_2250533757@T2` | -0.52049 |
| `explicit.stat_2923486259@T2` | -0.51604 |
| `explicit.stat_1999113824@T1` | -0.48829 |
| `explicit.stat_3321629045@T2` | -0.48553 |
| `explicit.stat_1671376347@T2` | -0.47416 |
| `explicit.stat_2160282525@T1` | -0.43494 |

### armour.gloves — n=19509, R²=-0.3566

intercept: `2.3442`  ·  log_price: True  ·  ilvl: `-0.00135`  ·  n_mods: `-0.00738`  ·  n_top_tier: `0.03070`  ·  corrupted: `0.03030`  ·  n_sockets: `0.00836`  ·  quality: `0.00084`

| stat_id | coef |
|---|---|
| `desecrated.stat_4067062424` | 0.09746 |
| `desecrated.stat_3032590688` | 0.09421 |
| `explicit.stat_3484657501@T2` | -0.06750 |
| `explicit.stat_803737631@T2` | -0.05512 |
| `explicit.stat_2451402625@T2` | -0.05115 |
| `explicit.stat_4080418644@T1` | -0.04943 |
| `explicit.stat_3362812763@T2` | -0.04891 |
| `explicit.stat_2797971005@T2` | -0.04218 |
| `explicit.stat_1573130764@T1` | -0.04074 |
| `explicit.stat_681332047@T2` | -0.04017 |
| `explicit.stat_328541901@T1` | -0.03935 |
| `explicit.stat_4220027924@T2` | -0.03900 |

### weapon.wand — n=13238, R²=-2.0798

intercept: `3.5287`  ·  log_price: True  ·  ilvl: `-0.04407`  ·  n_mods: `-0.00778`  ·  n_top_tier: `0.44443`  ·  corrupted: `-0.00348`  ·  n_sockets: `0.02228`  ·  quality: `0.01536`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.28948 |
| `explicit.stat_591105508@T1` | 1.92910 |
| `explicit.stat_1545858329@T1` | 1.89795 |
| `explicit.stat_4226189338@T1` | 1.89647 |
| `explicit.stat_124131830@T1` | 1.69680 |
| `explicit.stat_1600707273@T1` | 1.45280 |
| `explicit.stat_736967255@T2` | 1.36675 |
| `crafted.stat_124131830` | 0.74351 |
| `explicit.stat_2768835289@T2` | -0.49029 |
| `explicit.stat_2231156303@T2` | -0.47967 |
| `explicit.stat_473429811@T1` | -0.47874 |
| `explicit.stat_737908626@T1` | -0.47608 |

### weapon.bow — n=10849, R²=-1.964

intercept: `3.4089`  ·  log_price: True  ·  ilvl: `-0.04224`  ·  n_mods: `-0.00941`  ·  n_top_tier: `0.53738`  ·  corrupted: `0.09169`  ·  n_sockets: `0.00051`  ·  quality: `0.00732`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | 1.75153 |
| `desecrated.stat_210067635@T1` | -1.74767 |
| `desecrated.stat_666077204@T1` | 1.65030 |
| `explicit.stat_1202301673@T1` | 1.61410 |
| `crafted.stat_3035140377` | 1.54373 |
| `rune.stat_3885405204` | -0.99232 |
| `explicit.stat_518292764@T1` | 0.74863 |
| `explicit.stat_55876295@T1` | -0.59899 |
| `explicit.stat_2694482655@T1` | -0.57854 |
| `explicit.stat_3336890334@T2` | -0.57731 |
| `explicit.stat_3695891184@T2` | -0.57454 |
| `explicit.stat_55876295@T2` | -0.56519 |

### weapon.crossbow — n=10155, R²=-1.8098

intercept: `3.6313`  ·  log_price: True  ·  ilvl: `-0.04501`  ·  n_mods: `-0.00790`  ·  n_top_tier: `0.65985`  ·  corrupted: `-0.03422`  ·  n_sockets: `0.01412`  ·  quality: `0.00187`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -2.75955 |
| `explicit.stat_1980802737` | 2.05670 |
| `explicit.stat_709508406@T1` | 1.55286 |
| `explicit.stat_2250681686@T2` | -1.47404 |
| `explicit.stat_1202301673@T1` | 1.42376 |
| `explicit.stat_1509134228@T1` | 0.87936 |
| `explicit.stat_1202301673@T2` | -0.84102 |
| `explicit.stat_2250681686` | 0.83239 |
| `crafted.stat_3035140377` | 0.79546 |
| `explicit.stat_1037193709@T1` | 0.76669 |
| `explicit.stat_1509134228@T2` | -0.75997 |
| `rune.stat_669069897` | -0.72468 |

### flask.charm — n=7171, R²=-0.3802

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.35674`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60507 |
| `explicit.stat_1056492907` | 2.99605 |
| `explicit.stat_2676834156@T1` | 1.60931 |
| `explicit.stat_2541588185@T1` | 0.56071 |
| `explicit.stat_3138344128` | 0.02124 |
| `explicit.stat_2678930256` | 0.00648 |
| `explicit.stat_3246948616` | 0.00013 |
| `explicit.stat_1120862500@T2` | -0.00004 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_1873752457` | 0.00004 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_828533480@T1` | -0.00003 |

### weapon.warstaff — n=5079, R²=-0.5548

intercept: `-0.0007`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.00008`  ·  corrupted: `0.19815`  ·  n_sockets: `0.00001`  ·  quality: `0.00366`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 2.13066 |
| `rune.stat_731403740` | 1.53181 |
| `explicit.stat_9187492@T1` | 1.32039 |
| `desecrated.stat_9187492` | 0.66560 |
| `rune.stat_1712188793` | -0.64910 |
| `crafted.stat_210067635@T2` | -0.47477 |
| `desecrated.stat_518292764` | 0.29582 |
| `crafted.stat_3035140377` | 0.23256 |
| `desecrated.stat_669069897` | -0.11897 |
| `desecrated.stat_55876295` | -0.10200 |
| `rune.stat_1509134228` | 0.08568 |
| `rune.stat_3336890334` | 0.04415 |

### weapon.staff — n=4731, R²=-0.6046

intercept: `-0.0007`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00003`  ·  n_sockets: `0.00002`  ·  quality: `0.00008`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.12230 |
| `explicit.stat_4226189338@T1` | 2.30250 |
| `explicit.stat_2254480358@T1` | 1.60913 |
| `explicit.stat_2254480358@T2` | 1.27721 |
| `explicit.stat_3962278098@T2` | 0.69316 |
| `explicit.stat_473429811@T1` | 0.69312 |
| `explicit.stat_124131830@T1` | 0.69307 |
| `explicit.stat_1600707273@T1` | 0.68702 |
| `crafted.stat_124131830` | 0.45555 |
| `rune.stat_3909696841` | 0.33385 |
| `explicit.stat_3291658075@T2` | 0.31566 |
| `rune.stat_975988108` | -0.15688 |

### weapon.sceptre — n=4680, R²=-0.6089

intercept: `-0.0407`  ·  log_price: True  ·  ilvl: `0.00050`  ·  n_mods: `-0.00013`  ·  n_top_tier: `0.55333`  ·  corrupted: `1.68594`  ·  n_sockets: `0.00088`  ·  quality: `0.08258`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.74794 |
| `explicit.stat_4080418644@T1` | -0.55480 |
| `explicit.stat_2347036682@T2` | -0.55431 |
| `explicit.stat_4080418644@T2` | -0.55427 |
| `explicit.stat_1250712710@T1` | -0.55387 |
| `explicit.stat_1263695895@T2` | -0.55387 |
| `explicit.stat_328541901@T1` | -0.55352 |
| `explicit.stat_3984865854@T2` | -0.55349 |
| `explicit.stat_2347036682@T1` | -0.55330 |
| `explicit.stat_789117908@T1` | -0.55327 |
| `explicit.stat_3639275092@T2` | -0.55326 |
| `explicit.stat_1050105434@T2` | -0.55306 |

### weapon.spear — n=4001, R²=-0.5919

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00002`  ·  quality: `0.00340`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.30218 |
| `crafted.stat_3035140377` | 1.92198 |
| `crafted.stat_518292764` | 0.80846 |
| `explicit.stat_210067635@T1` | 0.69305 |
| `explicit.stat_1509134228@T1` | 0.57342 |
| `explicit.stat_9187492@T1` | 0.21390 |
| `crafted.stat_210067635` | 0.19224 |
| `explicit.stat_3336890334@T1` | 0.09784 |
| `rune.stat_1039491398` | 0.08025 |
| `explicit.stat_709508406@T1` | 0.01589 |
| `desecrated.stat_210067635` | -0.00400 |
| `desecrated.stat_1509134228` | 0.00380 |

### armour.focus — n=3259, R²=-0.6307

intercept: `-0.0720`  ·  log_price: True  ·  ilvl: `0.00089`  ·  n_mods: `0.00017`  ·  n_top_tier: `0.69692`  ·  corrupted: `0.00111`  ·  n_sockets: `0.00224`  ·  quality: `0.06239`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -4.31246 |
| `desecrated.stat_378817135@T1` | 3.22755 |
| `desecrated.stat_3393628375@T1` | -1.47012 |
| `crafted.stat_2974417149@T1` | -1.15225 |
| `explicit.stat_2231156303@T2` | -0.69896 |
| `explicit.stat_789117908@T2` | -0.69895 |
| `explicit.stat_274716455@T1` | -0.69860 |
| `explicit.stat_2891184298@T2` | -0.69824 |
| `explicit.stat_4052037485@T2` | -0.69817 |
| `explicit.stat_3291658075@T1` | -0.69787 |
| `explicit.stat_3372524247@T2` | -0.69780 |
| `explicit.stat_274716455@T2` | -0.69763 |

### armour.quiver — n=3060, R²=-0.6384

intercept: `-0.0302`  ·  log_price: True  ·  ilvl: `0.00036`  ·  n_mods: `0.00016`  ·  n_top_tier: `0.77361`  ·  corrupted: `0.00413`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.35168 |
| `explicit.stat_2463230181@T1` | 0.83170 |
| `explicit.stat_681332047@T2` | -0.77599 |
| `explicit.stat_681332047@T1` | -0.77553 |
| `explicit.stat_1573130764@T1` | -0.77497 |
| `explicit.stat_2194114101@T2` | -0.77462 |
| `explicit.stat_1573130764@T2` | -0.77434 |
| `explicit.stat_3714003708@T2` | -0.77421 |
| `explicit.stat_2321178454@T2` | -0.77417 |
| `explicit.stat_1368271171@T2` | -0.77413 |
| `explicit.stat_803737631@T2` | -0.77360 |
| `explicit.stat_3261801346@T1` | -0.77359 |

### armour.shield — n=2647, R²=-0.5157

intercept: `-0.0012`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.40132`  ·  corrupted: `0.17854`  ·  n_sockets: `0.00001`  ·  quality: `0.06867`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.86970 |
| `explicit.stat_1978899297@T2` | -0.56999 |
| `explicit.stat_4220027924@T1` | 0.40193 |
| `explicit.stat_1011760251@T1` | -0.40157 |
| `explicit.stat_1011760251@T2` | -0.40147 |
| `explicit.stat_328541901@T1` | -0.40145 |
| `explicit.stat_2339757871@T1` | -0.40140 |
| `explicit.stat_328541901@T2` | -0.40139 |
| `explicit.stat_2481353198@T1` | -0.40138 |
| `explicit.stat_3484657501@T1` | -0.40138 |
| `explicit.stat_3484657501@T2` | -0.40137 |
| `explicit.stat_3372524247@T2` | -0.40136 |

### weapon.twomace — n=2341, R²=-0.5686

intercept: `-0.0018`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.31031`  ·  corrupted: `0.00003`  ·  n_sockets: `0.00003`  ·  quality: `0.00004`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.34300 |
| `crafted.stat_3035140377` | 1.36919 |
| `desecrated.stat_1509134228@T1` | -0.49799 |
| `explicit.stat_1037193709@T1` | -0.31054 |
| `explicit.stat_1263695895@T1` | -0.31049 |
| `explicit.stat_3336890334@T1` | -0.31048 |
| `explicit.stat_1263695895@T2` | -0.31045 |
| `explicit.stat_387439868@T2` | -0.31042 |
| `explicit.stat_821021828@T2` | -0.31039 |
| `explicit.stat_1037193709@T2` | -0.31039 |
| `explicit.stat_821021828@T1` | -0.31038 |
| `explicit.stat_3695891184@T1` | -0.31036 |

## Coverage (listings per base)

- … **Sapphire** — 14214 listings (14195 priced) [0.3–7553463.8 ex]
- … **Emerald** — 14074 listings (14061 priced) [0.4–7553463.8 ex]
- … **Ruby** — 10790 listings (10780 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 6450 listings (6446 priced) [0.3–5288620.9 ex]
- … **Prismatic Ring** — 4961 listings (4959 priced) [0.3–24532814.5 ex]
- … **Stellar Amulet** — 4870 listings (4869 priced) [0.3–35690283.3 ex]
- … **Solar Amulet** — 4857 listings (4849 priced) [1.0–66666666.0 ex]
- … **Amethyst Ring** — 4782 listings (4781 priced) [0.3–4323655.9 ex]
- … **Gold Amulet** — 4627 listings (4622 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 4494 listings (4492 priced) [0.3–24532814.5 ex]
- … **Dueling Wand** — 4176 listings (4171 priced) [0.3–3736768402.2 ex]
- … **Sapphire Ring** — 3754 listings (3750 priced) [0.3–24532814.5 ex]
- … **Topaz Ring** — 3642 listings (3641 priced) [1.0–123132003.2 ex]
- … **Ruby Ring** — 3641 listings (3641 priced) [0.3–37474957.5 ex]
- … **Plate Belt** — 3302 listings (3299 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 3279 listings (3278 priced) [0.3–5286174.1 ex]
- … **Ancestral Tiara** — 3245 listings (3241 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3204 listings (3203 priced) [0.3–124352753.2 ex]
- … **Obliterator Bow** — 3201 listings (3193 priced) [0.4–22139622146.9 ex]
- … **Jade Amulet** — 3184 listings (3183 priced) [0.3–4547453.5 ex]
- … **Heavy Belt** — 3104 listings (3104 priced) [0.3–4877938.3 ex]
- … **Unset Ring** — 3040 listings (3040 priced) [0.3–24532814.5 ex]
- … **Bloodstone Amulet** — 3000 listings (3000 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 2925 listings (2925 priced) [0.3–24532814.5 ex]
- … **Lunar Amulet** — 2844 listings (2842 priced) [0.3–4877938.3 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-12T22:54:06+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **394982** (394270 priced in exalted)
- Distinct bases: 967 · distinct mods: 2945 · mod rows: 1876818
- Sold signals: **28268** sold · 210773 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-12T22:44:16+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.93** (median |log error| 3.1326)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×50.36 · ±30% 8% · n=57582
- Premium segment (60ex+): skill **+0.08** · typical error ×195.45 · ±30% 0% · n=36942

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 7633 | ×55.49 | 20% | +0.03 | +0.06 |
| accessory.amulet | 7173 | ×50.93 | 20% | +0.02 | +0.02 |
| jewel | 6839 | ×7.91 | 8% | +0.01 | +0.03 |
| accessory.belt | 5691 | ×10.00 | 18% | +0.02 | +0.02 |
| armour.chest | 5520 | ×13.54 | 5% | +0.01 | +0.03 |
| armour.helmet | 5373 | ×13.78 | 13% | +0.01 | +0.03 |
| armour.boots | 5053 | ×23.06 | 7% | +0.10 | +0.12 |
| armour.gloves | 4940 | ×24.28 | 5% | +0.04 | +0.06 |
| other | 4656 | ×9.81 | 39% | +0.07 | +0.15 |
| weapon.wand | 3207 | ×46.07 | 20% | +0.06 | +0.06 |
| weapon.bow | 2605 | ×28.08 | 18% | +0.08 | +0.10 |
| weapon.crossbow | 2487 | ×22.34 | 19% | +0.10 | +0.13 |
| weapon.warstaff | 1386 | ×93.73 | 15% | +0.08 | +0.09 |
| weapon.staff | 1294 | ×65.33 | 14% | +0.06 | +0.09 |
| weapon.sceptre | 1278 | ×59.84 | 11% | +0.08 | +0.11 |
| weapon.spear | 1080 | ×50.00 | 17% | +0.05 | +0.06 |
| armour.focus | 887 | ×59.18 | 14% | +0.11 | +0.15 |
| armour.quiver | 818 | ×48.58 | 13% | +0.04 | +0.09 |
| armour.shield | 693 | ×29.99 | 13% | +0.04 | +0.08 |
| weapon.twomace | 630 | ×22.99 | 14% | +0.06 | +0.10 |
| flask.charm | 588 | ×5.00 | 40% | +0.01 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=39317, R²=-0.5959

intercept: `1.6080`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `0.00329`  ·  n_top_tier: `0.36587`  ·  corrupted: `0.69029`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.81439 |
| `explicit.stat_2974417149@T1` | 0.75495 |
| `explicit.stat_1050105434@T1` | -0.44453 |
| `explicit.stat_3917489142@T1` | 0.41001 |
| `explicit.stat_2482852589@T1` | 0.35830 |
| `explicit.stat_789117908@T1` | -0.35272 |
| `explicit.stat_2891184298@T1` | 0.33454 |
| `explicit.stat_2106365538@T1` | 0.32069 |
| `implicit.stat_1379411836` | -0.23144 |
| `implicit.stat_4041853756` | 0.22993 |
| `implicit.stat_3879011313` | 0.22993 |
| `explicit.stat_2968503605@T1` | 0.22254 |

### jewel — n=37093, R²=-0.6905

intercept: `-1.2625`  ·  log_price: True  ·  ilvl: `0.03501`  ·  n_mods: `0.26086`  ·  n_top_tier: `-0.06975`  ·  corrupted: `0.25845`  ·  quality: `0.22668`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -5.23845 |
| `explicit.stat_3741323227@T1` | -3.48087 |
| `explicit.stat_3780644166@T1` | -3.21061 |
| `explicit.stat_1569101201@T1` | 2.57655 |
| `explicit.stat_3485067555@T1` | 2.45263 |
| `explicit.stat_234296660@T1` | -2.32182 |
| `explicit.stat_627767961@T1` | -2.07415 |
| `explicit.stat_1315743832@T1` | 2.02797 |
| `explicit.stat_153777645@T1` | -2.00120 |
| `explicit.stat_1316278494@T1` | -1.90053 |
| `explicit.stat_3119612865@T1` | -1.82125 |
| `explicit.stat_4236566306@T1` | 1.67455 |

### accessory.ring — n=35148, R²=-1.9305

intercept: `4.5806`  ·  log_price: True  ·  ilvl: `-0.05595`  ·  n_mods: `0.00172`  ·  n_top_tier: `0.03886`  ·  corrupted: `0.78376`  ·  n_sockets: `2.12876`  ·  quality: `0.05849`

| stat_id | coef |
|---|---|
| `explicit.stat_1671376347@T1` | 0.79975 |
| `implicit.stat_2748665614` | -0.29488 |
| `explicit.stat_707457662@T1` | 0.27419 |
| `explicit.stat_707457662@T2` | 0.24845 |
| `explicit.stat_1967040409` | 0.17842 |
| `explicit.stat_2557965901@T2` | -0.11277 |
| `explicit.stat_2557965901@T1` | -0.10362 |
| `explicit.stat_3325883026@T1` | -0.09876 |
| `explicit.stat_3032590688@T1` | 0.09511 |
| `explicit.stat_1263695895@T1` | -0.09193 |
| `implicit.stat_2901986750` | -0.08630 |
| `implicit.stat_2039822488` | 0.08517 |

### accessory.amulet — n=32917, R²=-2.1198

intercept: `4.0791`  ·  log_price: True  ·  ilvl: `-0.04924`  ·  n_mods: `-0.02769`  ·  n_top_tier: `1.13196`  ·  corrupted: `0.07112`  ·  n_sockets: `0.14608`  ·  quality: `-0.00099`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.35073 |
| `explicit.stat_983749596@T2` | -1.28127 |
| `explicit.stat_2748665614@T2` | -1.26740 |
| `explicit.stat_2748665614@T1` | -1.25740 |
| `explicit.stat_587431675@T1` | -1.24225 |
| `explicit.stat_3299347043@T1` | -1.22905 |
| `explicit.stat_3299347043@T2` | -1.22038 |
| `explicit.stat_3917489142@T2` | -1.21432 |
| `explicit.stat_472520716@T1` | -1.21063 |
| `explicit.stat_3917489142@T1` | -1.19922 |
| `explicit.stat_2106365538@T1` | -1.19318 |
| `explicit.stat_472520716@T2` | -1.18229 |

### accessory.belt — n=26032, R²=-0.1684

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.00558`  ·  corrupted: `0.00008`  ·  n_sockets: `-0.69311`

| stat_id | coef |
|---|---|
| `explicit.stat_2639966148` | 0.13784 |
| `pseudo.total_ele_res>=80` | 0.06399 |
| `explicit.stat_174664100` | 0.05656 |
| `pseudo.total_chaos_res` | 0.04381 |
| `explicit.stat_2923486259` | -0.04381 |
| `explicit.stat_3811191316` | 0.04255 |
| `explicit.stat_770672621` | 0.03054 |
| `explicit.stat_3742865955` | 0.02315 |
| `explicit.stat_2957407601` | 0.01775 |
| `explicit.stat_1485480327` | 0.01775 |
| `explicit.stat_1389754388@T1` | -0.00561 |
| `explicit.stat_51994685@T1` | -0.00560 |

### armour.chest — n=25740, R²=-0.5838

intercept: `3.8341`  ·  log_price: True  ·  ilvl: `-0.03410`  ·  n_mods: `-0.13857`  ·  n_top_tier: `0.42410`  ·  corrupted: `0.21905`  ·  n_sockets: `0.07562`  ·  quality: `0.01441`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.45581 |
| `explicit.stat_3325883026@T2` | -0.79971 |
| `explicit.stat_915769802@T1` | -0.76527 |
| `explicit.stat_4080418644@T1` | -0.67899 |
| `explicit.stat_3484657501@T1` | -0.64675 |
| `explicit.stat_2451402625@T2` | -0.63912 |
| `explicit.stat_3261801346@T1` | -0.61665 |
| `explicit.stat_4080418644@T2` | -0.60183 |
| `explicit.stat_3325883026@T1` | -0.59336 |
| `explicit.stat_3321629045@T1` | -0.59269 |
| `explicit.stat_3261801346@T2` | -0.59120 |
| `explicit.stat_915769802@T2` | -0.57883 |

### armour.helmet — n=25140, R²=-0.3636

intercept: `2.8767`  ·  log_price: True  ·  ilvl: `-0.01315`  ·  n_mods: `-0.06789`  ·  n_top_tier: `0.32464`  ·  corrupted: `0.78927`  ·  n_sockets: `0.03782`  ·  quality: `0.01572`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.83999 |
| `explicit.stat_3362812763@T2` | -0.46627 |
| `explicit.stat_53045048@T2` | -0.44578 |
| `explicit.stat_1263695895@T1` | -0.40337 |
| `explicit.stat_4080418644@T1` | -0.39876 |
| `explicit.stat_53045048@T1` | -0.38631 |
| `explicit.stat_803737631@T2` | -0.38261 |
| `explicit.stat_1263695895@T2` | -0.37744 |
| `explicit.stat_3362812763@T1` | -0.37498 |
| `explicit.stat_328541901@T2` | -0.36487 |
| `explicit.stat_3917489142@T2` | -0.34760 |
| `explicit.stat_3261801346@T1` | -0.34627 |

### armour.boots — n=23602, R²=-1.0655

intercept: `4.4862`  ·  log_price: True  ·  ilvl: `-0.05264`  ·  n_mods: `-0.09814`  ·  n_top_tier: `0.57145`  ·  corrupted: `0.42839`  ·  n_sockets: `0.11885`  ·  quality: `0.01683`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | -1.91215 |
| `explicit.stat_2339757871@T1` | -1.46770 |
| `explicit.stat_2250533757@T1` | 1.43807 |
| `explicit.stat_2923486259@T2` | -1.24915 |
| `explicit.stat_1999113824@T2` | -0.96932 |
| `explicit.stat_1062208444@T2` | -0.92635 |
| `desecrated.stat_2250533757@T2` | -0.86937 |
| `explicit.stat_2160282525@T1` | -0.84968 |
| `explicit.stat_1999113824@T1` | -0.83496 |
| `explicit.stat_3917489142@T2` | -0.83168 |
| `explicit.stat_53045048@T1` | -0.79362 |
| `explicit.stat_4052037485@T2` | -0.75270 |

### armour.gloves — n=22985, R²=-0.9285

intercept: `4.0748`  ·  log_price: True  ·  ilvl: `-0.05241`  ·  n_mods: `-0.12558`  ·  n_top_tier: `0.50574`  ·  corrupted: `0.45668`  ·  n_sockets: `0.31020`  ·  quality: `0.01892`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T2` | -1.39428 |
| `explicit.stat_803737631@T2` | -0.98170 |
| `explicit.stat_2339757871@T1` | 0.95770 |
| `explicit.stat_3484657501@T1` | -0.95760 |
| `explicit.stat_681332047@T2` | -0.94538 |
| `explicit.stat_3321629045@T1` | -0.87486 |
| `explicit.stat_2797971005@T2` | -0.79269 |
| `explicit.stat_3299347043@T2` | -0.75322 |
| `explicit.stat_3917489142@T2` | -0.69693 |
| `explicit.stat_3695891184@T1` | -0.69622 |
| `explicit.stat_3032590688@T1` | -0.69155 |
| `explicit.stat_3695891184@T2` | -0.66093 |

### weapon.wand — n=15265, R²=-2.1352

intercept: `4.0050`  ·  log_price: True  ·  ilvl: `-0.04957`  ·  n_mods: `-0.01206`  ·  n_top_tier: `0.39105`  ·  corrupted: `-0.03910`  ·  n_sockets: `0.04331`  ·  quality: `0.00612`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 3.16290 |
| `explicit.stat_1545858329@T1` | 3.01451 |
| `explicit.stat_4226189338@T1` | 2.52812 |
| `explicit.stat_591105508@T1` | 1.99810 |
| `explicit.stat_1600707273@T1` | 1.86947 |
| `crafted.stat_124131830` | 1.13650 |
| `explicit.stat_736967255@T2` | 1.12016 |
| `explicit.stat_1600707273@T2` | 0.71928 |
| `explicit.stat_4226189338@T2` | 0.48667 |
| `explicit.stat_3962278098@T2` | -0.43943 |
| `explicit.stat_3015669065@T1` | -0.43815 |
| `explicit.stat_473429811@T2` | -0.43360 |

### weapon.bow — n=12451, R²=-1.9622

intercept: `3.4471`  ·  log_price: True  ·  ilvl: `-0.04219`  ·  n_mods: `-0.02521`  ·  n_top_tier: `0.75927`  ·  corrupted: `0.29728`  ·  n_sockets: `-0.00135`  ·  quality: `0.01959`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 3.99202 |
| `desecrated.stat_210067635@T1` | -2.58581 |
| `rune.stat_3885405204` | -1.94164 |
| `crafted.stat_3035140377` | 1.65275 |
| `explicit.stat_1202301673@T1` | 1.37035 |
| `explicit.stat_2463230181@T1` | 1.03665 |
| `explicit.stat_55876295@T1` | -0.83959 |
| `explicit.stat_1037193709@T1` | -0.82808 |
| `explicit.stat_669069897@T1` | -0.80417 |
| `explicit.stat_669069897@T2` | -0.79816 |
| `explicit.stat_1037193709@T2` | -0.79743 |
| `explicit.stat_2463230181@T2` | -0.79392 |

### weapon.crossbow — n=11729, R²=-1.8657

intercept: `3.7124`  ·  log_price: True  ·  ilvl: `-0.04583`  ·  n_mods: `-0.01296`  ·  n_top_tier: `0.74690`  ·  corrupted: `-0.04156`  ·  n_sockets: `0.03182`  ·  quality: `0.00105`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.88606 |
| `explicit.stat_2250681686@T2` | -1.52513 |
| `explicit.stat_709508406@T1` | 1.38397 |
| `explicit.stat_1202301673@T1` | 1.25849 |
| `explicit.stat_1980802737` | 1.12042 |
| `explicit.stat_1263695895@T2` | -1.02848 |
| `explicit.stat_1202301673@T2` | -0.93568 |
| `explicit.stat_1509134228@T2` | -0.89001 |
| `crafted.stat_3035140377` | 0.86626 |
| `explicit.stat_1263695895@T1` | -0.82803 |
| `explicit.stat_2250681686` | 0.80549 |
| `explicit.stat_669069897@T1` | -0.79993 |

### flask.charm — n=9227, R²=-0.4382

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00884`  ·  corrupted: `0.87047`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.00992 |
| `explicit.stat_1056492907` | 3.55530 |
| `explicit.stat_2676834156@T1` | 1.60068 |
| `explicit.stat_2541588185@T1` | 0.53457 |
| `explicit.stat_2678930256` | 0.03219 |
| `explicit.stat_3138344128` | 0.02056 |
| `explicit.stat_828533480@T2` | -0.00885 |
| `explicit.stat_2676834156@T2` | -0.00884 |
| `explicit.stat_388617051@T2` | -0.00884 |
| `explicit.stat_1120862500@T2` | -0.00884 |
| `explicit.stat_1873752457@T2` | -0.00884 |
| `explicit.stat_828533480@T1` | -0.00884 |

### weapon.warstaff — n=6521, R²=-0.6141

intercept: `-0.3498`  ·  log_price: True  ·  ilvl: `0.00475`  ·  n_mods: `-0.01113`  ·  n_top_tier: `0.25770`  ·  corrupted: `0.06619`  ·  n_sockets: `0.00908`  ·  quality: `0.07703`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T1` | 1.30733 |
| `rune.stat_243313994` | 1.21191 |
| `rune.stat_731403740` | 1.03135 |
| `crafted.stat_210067635@T2` | -0.63752 |
| `explicit.stat_1509134228@T2` | 0.56858 |
| `desecrated.stat_9187492` | 0.53994 |
| `crafted.stat_3035140377` | 0.47343 |
| `rune.stat_1712188793` | -0.42424 |
| `explicit.stat_1037193709@T1` | 0.39441 |
| `desecrated.stat_518292764` | 0.30633 |
| `explicit.stat_1509134228@T1` | -0.28996 |
| `explicit.stat_328541901@T2` | -0.28245 |

### weapon.sceptre — n=6019, R²=-0.5161

intercept: `-8.1893`  ·  log_price: True  ·  ilvl: `0.10366`  ·  n_mods: `-0.05911`  ·  n_top_tier: `0.27315`  ·  corrupted: `0.64697`  ·  n_sockets: `0.23711`  ·  quality: `0.09748`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.52881 |
| `explicit.stat_2162097452@T2` | 0.92439 |
| `explicit.stat_4080418644@T1` | -0.85441 |
| `explicit.stat_1798257884@T2` | 0.60292 |
| `explicit.stat_4080418644@T2` | -0.60274 |
| `explicit.stat_2347036682@T2` | -0.47634 |
| `explicit.stat_1574590649@T2` | -0.44980 |
| `explicit.stat_2347036682@T1` | 0.43203 |
| `explicit.stat_3057012405@T1` | 0.43109 |
| `explicit.stat_1263695895@T2` | -0.39923 |
| `explicit.stat_1250712710@T2` | 0.36162 |
| `explicit.stat_1263695895@T1` | -0.34365 |

### weapon.staff — n=6000, R²=-0.6383

intercept: `-0.8745`  ·  log_price: True  ·  ilvl: `0.01093`  ·  n_mods: `-0.00160`  ·  n_top_tier: `0.35630`  ·  corrupted: `0.20616`  ·  n_sockets: `0.04150`  ·  quality: `0.03021`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 3.67636 |
| `explicit.stat_4226189338@T1` | 2.07285 |
| `explicit.stat_1600707273@T1` | 1.66374 |
| `explicit.stat_2254480358@T1` | 1.66235 |
| `explicit.stat_1545858329@T1` | 1.61456 |
| `explicit.stat_2254480358@T2` | 1.25104 |
| `explicit.stat_124131830@T1` | 1.07983 |
| `explicit.stat_4226189338@T2` | 0.96857 |
| `explicit.stat_2231156303@T2` | 0.49676 |
| `crafted.stat_124131830` | 0.48866 |
| `explicit.stat_1263695895@T2` | -0.38994 |
| `explicit.stat_591105508@T1` | -0.38651 |

### weapon.spear — n=5092, R²=-0.6895

intercept: `-0.0969`  ·  log_price: True  ·  ilvl: `0.00127`  ·  n_mods: `-0.00035`  ·  n_top_tier: `0.30022`  ·  corrupted: `-0.00380`  ·  n_sockets: `0.00339`  ·  quality: `0.09139`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.02138 |
| `explicit.stat_9187492@T1` | 1.30329 |
| `explicit.stat_3336890334@T1` | 0.79853 |
| `crafted.stat_3035140377` | 0.66594 |
| `crafted.stat_518292764` | 0.53666 |
| `explicit.stat_210067635@T1` | 0.48444 |
| `explicit.stat_1940865751@T1` | 0.36744 |
| `explicit.stat_1509134228@T1` | 0.34435 |
| `explicit.stat_1037193709@T1` | 0.32131 |
| `explicit.stat_9187492@T2` | -0.30411 |
| `explicit.stat_55876295@T1` | -0.30348 |
| `explicit.stat_4080418644@T2` | -0.30225 |

### armour.focus — n=4178, R²=-0.5164

intercept: `-6.4348`  ·  log_price: True  ·  ilvl: `0.07944`  ·  n_mods: `-0.01861`  ·  n_top_tier: `0.66882`  ·  corrupted: `0.45158`  ·  n_sockets: `0.15892`  ·  quality: `0.07695`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 7.64738 |
| `crafted.stat_737908626@T2` | -2.18658 |
| `explicit.stat_1671376347@T1` | 1.09573 |
| `explicit.stat_4220027924@T2` | -0.88303 |
| `explicit.stat_736967255@T2` | -0.85883 |
| `explicit.stat_3962278098@T2` | -0.84911 |
| `explicit.stat_2923486259@T1` | -0.84585 |
| `explicit.stat_2891184298@T2` | -0.83855 |
| `explicit.stat_124131830@T2` | -0.81393 |
| `explicit.stat_737908626@T1` | -0.73907 |
| `explicit.stat_3962278098@T1` | -0.73870 |
| `explicit.stat_3291658075@T1` | -0.73723 |

### armour.quiver — n=3914, R²=-0.5703

intercept: `-4.5841`  ·  log_price: True  ·  ilvl: `0.05379`  ·  n_mods: `0.02087`  ·  n_top_tier: `0.96754`  ·  corrupted: `0.88735`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 9.49873 |
| `explicit.stat_681332047@T2` | -1.20202 |
| `explicit.stat_2194114101@T2` | -1.12476 |
| `explicit.stat_2321178454@T2` | -1.09733 |
| `explicit.stat_1368271171@T2` | -1.06913 |
| `explicit.stat_1573130764@T1` | -1.06890 |
| `explicit.stat_681332047@T1` | -1.03353 |
| `explicit.stat_1573130764@T2` | -1.02691 |
| `explicit.stat_3714003708@T2` | -0.99718 |
| `explicit.stat_3261801346@T1` | -0.97831 |
| `explicit.stat_1368271171@T1` | -0.95261 |
| `explicit.stat_3261801346@T2` | -0.93820 |

### armour.shield — n=3418, R²=-0.5919

intercept: `-4.0446`  ·  log_price: True  ·  ilvl: `0.05064`  ·  n_mods: `0.00080`  ·  n_top_tier: `0.51297`  ·  corrupted: `0.38830`  ·  n_sockets: `-0.00160`  ·  quality: `0.06956`

| stat_id | coef |
|---|---|
| `explicit.stat_328541901@T1` | -0.92411 |
| `explicit.stat_1978899297@T1` | 0.77642 |
| `explicit.stat_328541901@T2` | -0.74990 |
| `explicit.stat_2481353198@T1` | -0.74844 |
| `explicit.stat_1011760251@T2` | -0.73476 |
| `explicit.stat_2481353198@T2` | -0.72072 |
| `explicit.stat_2339757871@T1` | -0.71579 |
| `explicit.stat_1978899297@T2` | -0.67431 |
| `explicit.stat_53045048@T2` | -0.66840 |
| `explicit.stat_2901986750@T1` | -0.60532 |
| `explicit.stat_3362812763@T1` | -0.59893 |
| `explicit.stat_1671376347@T1` | -0.58518 |

### weapon.twomace — n=3076, R²=-0.5692

intercept: `-2.9955`  ·  log_price: True  ·  ilvl: `0.03832`  ·  n_mods: `-0.01707`  ·  n_top_tier: `0.84205`  ·  corrupted: `0.57868`  ·  n_sockets: `0.07100`  ·  quality: `0.01634`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.82166 |
| `explicit.stat_1037193709@T1` | -1.10912 |
| `crafted.stat_3035140377` | 1.04793 |
| `explicit.stat_3336890334@T1` | -1.03510 |
| `explicit.stat_821021828@T2` | -1.02242 |
| `explicit.stat_387439868@T2` | -1.02110 |
| `explicit.stat_1037193709@T2` | -0.99695 |
| `explicit.stat_709508406@T1` | -0.92008 |
| `explicit.stat_821021828@T1` | -0.91609 |
| `explicit.stat_691932474@T1` | -0.90070 |
| `explicit.stat_2694482655@T1` | -0.88742 |
| `explicit.stat_669069897@T1` | -0.88565 |

## Coverage (listings per base)

- … **Sapphire** — 17491 listings (17466 priced) [0.4–7553463.8 ex]
- … **Emerald** — 17266 listings (17246 priced) [0.3–7553463.8 ex]
- … **Ruby** — 13311 listings (13299 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 7575 listings (7566 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 6084 listings (6078 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 5923 listings (5913 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 5827 listings (5824 priced) [0.2–4323655.9 ex]
- … **Stellar Amulet** — 5659 listings (5656 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 5606 listings (5597 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 5433 listings (5429 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 4831 listings (4820 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4552 listings (4547 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 4421 listings (4418 priced) [1.0–307202867.9 ex]
- … **Ruby Ring** — 4394 listings (4392 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 4019 listings (4014 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 3951 listings (3949 priced) [0.3–5286174.1 ex]
- … **Ancestral Tiara** — 3894 listings (3887 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3851 listings (3850 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3827 listings (3823 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 3741 listings (3740 priced) [0.2–24532814.5 ex]
- … **Obliterator Bow** — 3709 listings (3699 priced) [0.3–42622633798.0 ex]
- … **Heavy Belt** — 3665 listings (3663 priced) [0.3–4877938.3 ex]
- … **Bloodstone Amulet** — 3642 listings (3639 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 3523 listings (3521 priced) [0.2–24532814.5 ex]
- … **Azure Amulet** — 3462 listings (3462 priced) [0.3–123132003.2 ex]

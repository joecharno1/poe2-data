# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-21T22:45:55+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **722270** (719939 priced in exalted)
- Distinct bases: 1001 · distinct mods: 3325 · mod rows: 3415488
- Sold signals: **24127** sold · 411572 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-21T22:33:19+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×23.24** (median |log error| 3.146)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×63.77 · ±30% 5% · n=105072
- Premium segment (60ex+): skill **+0.14** · typical error ×309.82 · ±30% 0% · n=69678

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 15481 | ×52.16 | 21% | +0.04 | +0.07 |
| jewel | 14978 | ×57.14 | 22% | +0.03 | +0.03 |
| accessory.amulet | 13974 | ×31.98 | 17% | +0.04 | +0.04 |
| accessory.belt | 9853 | ×19.77 | 9% | +0.09 | +0.11 |
| armour.chest | 9606 | ×17.03 | 21% | +0.08 | +0.11 |
| armour.helmet | 9336 | ×23.61 | 16% | +0.09 | +0.11 |
| armour.boots | 8653 | ×21.65 | 18% | +0.11 | +0.13 |
| armour.gloves | 8506 | ×29.39 | 12% | +0.09 | +0.12 |
| other | 8406 | ×2.00 | 43% | +0.11 | +0.17 |
| weapon.wand | 4969 | ×33.19 | 13% | +0.12 | +0.13 |
| weapon.bow | 3939 | ×22.92 | 10% | +0.17 | +0.18 |
| weapon.crossbow | 3702 | ×24.79 | 14% | +0.12 | +0.17 |
| weapon.warstaff | 2568 | ×13.92 | 7% | +0.16 | +0.16 |
| weapon.staff | 2481 | ×15.88 | 6% | +0.12 | +0.13 |
| weapon.sceptre | 2372 | ×17.81 | 5% | +0.06 | +0.07 |
| weapon.spear | 1945 | ×12.85 | 7% | +0.10 | +0.14 |
| armour.focus | 1608 | ×13.36 | 7% | +0.09 | +0.11 |
| armour.quiver | 1506 | ×16.64 | 8% | +0.12 | +0.13 |
| flask.charm | 1226 | ×10.00 | 28% | +0.02 | +0.04 |
| armour.shield | 1226 | ×9.02 | 8% | +0.10 | +0.12 |
| weapon.twomace | 1123 | ×8.84 | 7% | +0.09 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=81957, R²=-1.9022

intercept: `-0.0487`  ·  log_price: True  ·  ilvl: `0.00060`  ·  n_mods: `1.02346`  ·  n_top_tier: `-0.91106`  ·  corrupted: `1.55769`  ·  quality: `0.31284`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 4.29018 |
| `explicit.stat_1604736568@T1` | -2.38374 |
| `explicit.stat_1604736568` | 2.27207 |
| `explicit.stat_3556824919@T1` | 1.19614 |
| `explicit.stat_3714003708@T1` | 1.03428 |
| `explicit.stat_2194114101@T1` | -0.82136 |
| `explicit.stat_274716455@T1` | -0.66543 |
| `explicit.stat_681332047@T1` | -0.51737 |
| `explicit.stat_587431675@T1` | -0.42398 |
| `explicit.stat_3473929743@T1` | -0.39073 |
| `explicit.stat_737908626@T1` | -0.29895 |
| `explicit.stat_4045894391@T1` | -0.29523 |

### accessory.ring — n=70822, R²=-2.0023

intercept: `3.2097`  ·  log_price: True  ·  ilvl: `-0.03993`  ·  n_mods: `0.00030`  ·  n_top_tier: `1.08104`  ·  corrupted: `0.00699`  ·  n_sockets: `2.20151`  ·  quality: `0.02484`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.11695 |
| `explicit.stat_1263695895@T2` | -1.10113 |
| `explicit.stat_3325883026@T1` | -1.09701 |
| `explicit.stat_4080418644@T1` | -1.09667 |
| `explicit.stat_2923486259@T2` | -1.09609 |
| `explicit.stat_2891184298@T2` | -1.09607 |
| `explicit.stat_3962278098@T1` | -1.09384 |
| `explicit.stat_3032590688@T1` | -1.09380 |
| `explicit.stat_803737631@T1` | -1.09343 |
| `explicit.stat_3962278098@T2` | -1.09330 |
| `explicit.stat_2231156303@T1` | -1.09327 |
| `explicit.stat_4220027924@T2` | -1.09215 |

### other — n=68679, R²=-0.6711

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.05602`  ·  n_top_tier: `0.29056`  ·  corrupted: `0.01281`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.38656 |
| `explicit.stat_3299347043@T1` | -0.24018 |
| `implicit.stat_2219129443` | 0.22465 |
| `implicit.stat_3182714256` | 0.16809 |
| `implicit.stat_718638445` | 0.16809 |
| `explicit.stat_3917489142@T1` | -0.15604 |
| `explicit.stat_2974417149@T1` | 0.11585 |
| `explicit.stat_789117908@T1` | -0.07031 |
| `implicit.stat_3879011313` | 0.06295 |
| `implicit.stat_958696139` | -0.05601 |
| `explicit.stat_736967255@T1` | -0.04753 |
| `implicit.stat_1416292992` | -0.03735 |

### accessory.amulet — n=63510, R²=-2.1269

intercept: `3.1625`  ·  log_price: True  ·  ilvl: `-0.04077`  ·  n_mods: `-0.00560`  ·  n_top_tier: `1.07493`  ·  corrupted: `0.05746`  ·  n_sockets: `-0.00233`  ·  quality: `0.01857`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.67121 |
| `explicit.stat_3299347043@T2` | -1.58662 |
| `explicit.stat_124131830@T2` | -1.28842 |
| `explicit.stat_1202301673@T2` | -1.21306 |
| `explicit.stat_2901986750@T1` | -1.16044 |
| `explicit.stat_803737631@T1` | -1.15243 |
| `explicit.stat_2866361420@T1` | -1.15112 |
| `explicit.stat_2974417149@T1` | -1.15084 |
| `explicit.stat_2866361420@T2` | -1.14652 |
| `explicit.stat_2974417149@T2` | -1.12655 |
| `explicit.stat_587431675@T2` | -1.12578 |
| `explicit.stat_4080418644@T1` | -1.11841 |

### accessory.belt — n=45204, R²=-1.3586

intercept: `5.6865`  ·  log_price: True  ·  ilvl: `-0.06456`  ·  n_mods: `-0.08731`  ·  n_top_tier: `0.79475`  ·  corrupted: `1.14220`  ·  n_sockets: `1.00455`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T2` | -1.06378 |
| `explicit.stat_3299347043@T1` | -0.97517 |
| `explicit.stat_51994685@T1` | -0.89829 |
| `explicit.stat_2923486259@T1` | 0.89494 |
| `explicit.stat_2881298780@T1` | -0.88558 |
| `explicit.stat_1570770415@T2` | -0.85025 |
| `explicit.stat_4080418644@T2` | -0.83554 |
| `explicit.stat_4080418644@T1` | -0.82203 |
| `explicit.stat_915769802@T2` | -0.81979 |
| `explicit.stat_3372524247@T2` | -0.81507 |
| `explicit.stat_809229260@T2` | -0.79666 |
| `explicit.stat_2881298780@T2` | -0.79133 |

### armour.chest — n=44784, R²=-1.7764

intercept: `3.3391`  ·  log_price: True  ·  ilvl: `-0.04122`  ·  n_mods: `-0.01360`  ·  n_top_tier: `0.37477`  ·  corrupted: `0.42416`  ·  n_sockets: `0.02351`  ·  quality: `0.07404`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.77700 |
| `explicit.stat_986397080@T2` | -0.43376 |
| `explicit.stat_986397080@T1` | -0.43111 |
| `explicit.stat_3484657501@T1` | -0.41061 |
| `explicit.stat_1692879867@T2` | -0.40765 |
| `explicit.stat_4080418644@T2` | -0.40737 |
| `explicit.stat_915769802@T2` | -0.40152 |
| `explicit.stat_2339757871@T2` | -0.39800 |
| `explicit.stat_915769802@T1` | -0.39379 |
| `explicit.stat_2451402625@T2` | -0.39346 |
| `explicit.stat_1062208444@T2` | -0.39193 |
| `explicit.stat_4080418644@T1` | -0.38725 |

### armour.helmet — n=43588, R²=-1.6538

intercept: `3.3674`  ·  log_price: True  ·  ilvl: `-0.04241`  ·  n_mods: `-0.02480`  ·  n_top_tier: `0.55540`  ·  corrupted: `0.57364`  ·  n_sockets: `0.08923`  ·  quality: `0.06879`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.88738 |
| `crafted.stat_3917489142@T1` | 1.15415 |
| `explicit.stat_1263695895@T1` | -0.84640 |
| `explicit.stat_3917489142@T2` | -0.78313 |
| `explicit.stat_2162097452@T2` | -0.72297 |
| `explicit.stat_3917489142@T1` | -0.70265 |
| `explicit.stat_4015621042@T2` | -0.64622 |
| `explicit.stat_1263695895@T2` | -0.64545 |
| `explicit.stat_4052037485@T2` | -0.63543 |
| `explicit.stat_1999113824@T1` | -0.63282 |
| `explicit.stat_587431675@T2` | -0.60124 |
| `explicit.stat_3321629045@T2` | -0.59996 |

### armour.boots — n=40352, R²=-1.6683

intercept: `3.7388`  ·  log_price: True  ·  ilvl: `-0.04616`  ·  n_mods: `-0.02827`  ·  n_top_tier: `0.40336`  ·  corrupted: `0.08812`  ·  n_sockets: `0.06696`  ·  quality: `0.06916`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.13791 |
| `explicit.stat_2250533757@T1` | 1.76721 |
| `crafted.stat_3917489142@T1` | 1.40150 |
| `explicit.stat_2923486259@T1` | 0.84405 |
| `explicit.stat_3299347043@T1` | -0.55684 |
| `explicit.stat_2923486259@T2` | -0.49847 |
| `explicit.stat_3917489142@T2` | -0.47602 |
| `explicit.stat_2160282525@T1` | -0.47456 |
| `explicit.stat_328541901@T2` | -0.46686 |
| `explicit.stat_1671376347@T2` | -0.46257 |
| `explicit.stat_1874553720@T1` | -0.46006 |
| `explicit.stat_1999113824@T2` | -0.45188 |

### armour.gloves — n=39354, R²=-1.5478

intercept: `3.9162`  ·  log_price: True  ·  ilvl: `-0.05152`  ·  n_mods: `-0.01470`  ·  n_top_tier: `0.66881`  ·  corrupted: `-0.05428`  ·  n_sockets: `0.19601`  ·  quality: `0.05645`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.25492 |
| `explicit.stat_3484657501@T2` | -1.03157 |
| `explicit.stat_4052037485@T1` | -0.98608 |
| `explicit.stat_2923486259@T2` | -0.97757 |
| `explicit.stat_3321629045@T2` | -0.97122 |
| `explicit.stat_3484657501@T1` | -0.92297 |
| `explicit.stat_4052037485@T2` | -0.89997 |
| `explicit.stat_124859000@T1` | -0.88119 |
| `explicit.stat_4015621042@T2` | -0.85254 |
| `explicit.stat_9187492@T2` | -0.83038 |
| `explicit.stat_124859000@T2` | -0.80050 |
| `explicit.stat_3639275092@T1` | -0.79774 |

### weapon.wand — n=23194, R²=-1.8311

intercept: `3.7661`  ·  log_price: True  ·  ilvl: `-0.04649`  ·  n_mods: `-0.08802`  ·  n_top_tier: `0.62611`  ·  corrupted: `0.00234`  ·  n_sockets: `0.02961`  ·  quality: `0.03959`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.02635 |
| `explicit.stat_1545858329@T1` | 2.45456 |
| `explicit.stat_2254480358@T1` | 2.19362 |
| `explicit.stat_124131830@T1` | 1.98396 |
| `explicit.stat_591105508@T1` | 1.88565 |
| `explicit.stat_1263695895@T2` | -1.18703 |
| `explicit.stat_1263695895@T1` | -1.15672 |
| `explicit.stat_2254480358@T2` | 1.15571 |
| `explicit.stat_736967255@T2` | 1.09612 |
| `crafted.stat_124131830` | 1.07522 |
| `explicit.stat_4226189338@T1` | 1.05975 |
| `explicit.stat_473429811@T2` | -0.90994 |

### flask.charm — n=20256, R²=-0.663

intercept: `0.1063`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.61738`  ·  corrupted: `1.57297`  ·  quality: `0.00841`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60502 |
| `explicit.stat_1056492907` | 2.56177 |
| `explicit.stat_3246948616` | 1.95147 |
| `explicit.stat_1120862500@T2` | -1.61743 |
| `explicit.stat_828533480@T2` | -1.61742 |
| `explicit.stat_1873752457@T2` | -1.61739 |
| `explicit.stat_2365392475@T2` | -1.61731 |
| `explicit.stat_2541588185@T2` | -1.61730 |
| `explicit.stat_3196823591@T2` | -1.61723 |
| `explicit.stat_388617051@T2` | -1.61646 |
| `explicit.stat_2676834156@T2` | -1.61617 |
| `explicit.stat_828533480@T1` | -1.61264 |

### weapon.bow — n=18540, R²=-1.6975

intercept: `3.9853`  ·  log_price: True  ·  ilvl: `-0.04657`  ·  n_mods: `-0.11524`  ·  n_top_tier: `0.74330`  ·  corrupted: `0.84195`  ·  n_sockets: `0.07958`  ·  quality: `0.02616`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 4.47100 |
| `desecrated.stat_210067635@T1` | -1.78176 |
| `explicit.stat_1263695895@T1` | -1.46843 |
| `explicit.stat_1263695895@T2` | -1.28255 |
| `crafted.stat_210067635@T2` | -1.20945 |
| `crafted.stat_3035140377` | 1.13030 |
| `explicit.stat_1509134228@T1` | -1.08474 |
| `explicit.stat_2463230181@T2` | -1.03118 |
| `explicit.stat_210067635@T2` | -0.93106 |
| `explicit.stat_709508406@T1` | 0.91535 |
| `explicit.stat_3695891184@T1` | -0.89213 |
| `explicit.stat_1368271171@T2` | -0.86897 |

### weapon.crossbow — n=17340, R²=-1.7019

intercept: `4.0385`  ·  log_price: True  ·  ilvl: `-0.04863`  ·  n_mods: `-0.07991`  ·  n_top_tier: `0.31965`  ·  corrupted: `-0.06651`  ·  n_sockets: `0.07078`  ·  quality: `0.01854`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.83154 |
| `explicit.stat_1980802737` | 1.44734 |
| `explicit.stat_1202301673@T1` | 1.36651 |
| `explicit.stat_2250681686@T2` | -1.32713 |
| `explicit.stat_1509134228@T1` | 1.15034 |
| `explicit.stat_2250681686` | 1.08158 |
| `explicit.stat_709508406@T1` | 0.89485 |
| `crafted.stat_3035140377` | 0.85397 |
| `explicit.stat_3695891184@T1` | -0.56438 |
| `explicit.stat_1263695895@T2` | -0.54983 |
| `explicit.stat_387439868@T1` | 0.53703 |
| `explicit.stat_3336890334@T2` | -0.52717 |

### weapon.warstaff — n=12191, R²=-0.3324

intercept: `-10.8360`  ·  log_price: True  ·  ilvl: `0.14669`  ·  n_mods: `-0.23905`  ·  n_top_tier: `0.56652`  ·  corrupted: `0.25032`  ·  n_sockets: `0.11597`  ·  quality: `0.05362`

| stat_id | coef |
|---|---|
| `explicit.stat_821021828@T2` | -1.05743 |
| `explicit.stat_1037193709@T2` | -0.99333 |
| `explicit.stat_328541901@T2` | -0.97741 |
| `crafted.stat_210067635@T2` | 0.92786 |
| `desecrated.stat_9187492` | 0.80576 |
| `explicit.stat_821021828@T1` | -0.79536 |
| `explicit.stat_1940865751@T2` | -0.77373 |
| `rune.stat_243313994` | 0.76755 |
| `desecrated.stat_2231156303@T1` | 0.72962 |
| `desecrated.stat_2527686725@T1` | 0.72962 |
| `explicit.stat_328541901@T1` | -0.72018 |
| `explicit.stat_691932474@T2` | -0.69275 |

### weapon.staff — n=11610, R²=-0.3587

intercept: `-15.9862`  ·  log_price: True  ·  ilvl: `0.20404`  ·  n_mods: `-0.07472`  ·  n_top_tier: `0.49433`  ·  corrupted: `0.85884`  ·  n_sockets: `0.20310`  ·  quality: `0.03305`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.14251 |
| `explicit.stat_591105508@T1` | 1.98744 |
| `explicit.stat_4226189338@T1` | 1.71771 |
| `explicit.stat_1600707273@T1` | 1.43190 |
| `explicit.stat_1545858329@T1` | 1.10906 |
| `explicit.stat_293638271@T2` | -0.98545 |
| `explicit.stat_2254480358@T1` | 0.89774 |
| `explicit.stat_3962278098@T2` | 0.84366 |
| `explicit.stat_473429811@T2` | -0.83352 |
| `explicit.stat_124131830@T2` | 0.70590 |
| `explicit.stat_591105508@T2` | 0.64856 |
| `crafted.stat_124131830` | 0.61890 |

### weapon.sceptre — n=11331, R²=-0.3359

intercept: `-21.7347`  ·  log_price: True  ·  ilvl: `0.27614`  ·  n_mods: `-0.00034`  ·  n_top_tier: `0.10603`  ·  corrupted: `0.17655`  ·  n_sockets: `0.18933`  ·  quality: `0.03207`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.64743 |
| `explicit.stat_2162097452@T2` | 1.41046 |
| `explicit.stat_3057012405@T1` | 1.27936 |
| `explicit.stat_1798257884@T2` | 1.03630 |
| `explicit.stat_101878827@T2` | 0.89580 |
| `explicit.stat_101878827@T1` | 0.89283 |
| `explicit.stat_1263695895@T2` | -0.85067 |
| `explicit.stat_1263695895@T1` | -0.76466 |
| `explicit.stat_4080418644@T2` | -0.67616 |
| `explicit.stat_849987426@T2` | 0.56450 |
| `explicit.stat_2854751904@T2` | -0.54274 |
| `explicit.stat_1998951374@T1` | 0.45579 |

### weapon.spear — n=9209, R²=-0.3835

intercept: `-13.5824`  ·  log_price: True  ·  ilvl: `0.18687`  ·  n_mods: `-0.16849`  ·  n_top_tier: `0.64990`  ·  corrupted: `-0.46025`  ·  n_sockets: `0.18197`  ·  quality: `0.06881`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -4.00510 |
| `crafted.stat_210067635@T2` | -3.36793 |
| `desecrated.stat_210067635@T1` | -1.08491 |
| `explicit.stat_748522257@T2` | -1.02825 |
| `explicit.stat_4080418644@T2` | -1.01972 |
| `explicit.stat_9187492@T1` | 0.96837 |
| `explicit.stat_1940865751@T2` | -0.96447 |
| `explicit.stat_3336890334@T2` | -0.94665 |
| `crafted.stat_3035140377` | 0.93973 |
| `explicit.stat_9187492@T2` | -0.93227 |
| `explicit.stat_1037193709@T1` | -0.89083 |
| `explicit.stat_4080418644@T1` | -0.85974 |

### armour.focus — n=7529, R²=-0.3229

intercept: `-16.1551`  ·  log_price: True  ·  ilvl: `0.20659`  ·  n_mods: `-0.16494`  ·  n_top_tier: `1.00747`  ·  corrupted: `-0.05399`  ·  n_sockets: `0.36286`  ·  quality: `0.02975`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 1.71287 |
| `explicit.stat_4220027924@T1` | -1.52165 |
| `explicit.stat_2923486259@T1` | -1.41907 |
| `explicit.stat_4220027924@T2` | -1.18835 |
| `explicit.stat_2923486259@T2` | -1.16872 |
| `explicit.stat_2339757871@T2` | -1.15363 |
| `explicit.stat_2768835289@T1` | -1.13158 |
| `explicit.stat_4015621042@T1` | -1.13140 |
| `explicit.stat_2231156303@T2` | -1.11834 |
| `explicit.stat_1050105434@T2` | -1.10289 |
| `explicit.stat_3962278098@T2` | -1.07980 |
| `explicit.stat_3291658075@T2` | -1.07564 |

### armour.quiver — n=7014, R²=-0.2753

intercept: `-18.5103`  ·  log_price: True  ·  ilvl: `0.22254`  ·  n_mods: `-0.06468`  ·  n_top_tier: `0.68293`  ·  corrupted: `0.99234`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.06097 |
| `explicit.stat_681332047@T2` | -1.54992 |
| `explicit.stat_681332047@T1` | -1.33578 |
| `explicit.stat_1573130764@T2` | -0.99381 |
| `explicit.stat_2321178454@T2` | -0.83609 |
| `explicit.stat_2194114101@T2` | -0.82993 |
| `explicit.stat_1573130764@T1` | -0.80694 |
| `explicit.stat_4067062424@T1` | -0.66758 |
| `explicit.stat_3714003708@T2` | -0.58570 |
| `explicit.stat_3261801346@T1` | -0.57760 |
| `explicit.stat_4067062424@T2` | -0.56461 |
| `explicit.stat_803737631@T1` | -0.55304 |

### armour.shield — n=6014, R²=-0.414

intercept: `-12.9866`  ·  log_price: True  ·  ilvl: `0.17385`  ·  n_mods: `-0.18022`  ·  n_top_tier: `0.69601`  ·  corrupted: `-0.33061`  ·  n_sockets: `0.40756`  ·  quality: `0.04547`

| stat_id | coef |
|---|---|
| `explicit.stat_1011760251@T1` | -1.53352 |
| `explicit.stat_3855016469@T1` | -1.34958 |
| `explicit.stat_2901986750@T1` | -1.31048 |
| `explicit.stat_4095671657@T2` | -1.21270 |
| `explicit.stat_1011760251@T2` | -1.20531 |
| `explicit.stat_4052037485@T1` | -1.16618 |
| `explicit.stat_2481353198@T1` | -1.16333 |
| `explicit.stat_3321629045@T2` | -1.14838 |
| `explicit.stat_4095671657@T1` | -1.07971 |
| `explicit.stat_2481353198@T2` | -1.02444 |
| `explicit.stat_3362812763@T1` | -0.98665 |
| `explicit.stat_2923486259@T1` | -0.97313 |

### weapon.twomace — n=5487, R²=-0.4449

intercept: `-10.5991`  ·  log_price: True  ·  ilvl: `0.14431`  ·  n_mods: `-0.21231`  ·  n_top_tier: `0.51681`  ·  corrupted: `0.36065`  ·  n_sockets: `0.17876`  ·  quality: `0.05878`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.85836 |
| `explicit.stat_3336890334@T1` | -1.56487 |
| `explicit.stat_1037193709@T1` | -1.38817 |
| `explicit.stat_1263695895@T2` | -1.23991 |
| `explicit.stat_9187492@T1` | -1.13655 |
| `explicit.stat_2694482655@T1` | 0.95506 |
| `explicit.stat_3695891184@T2` | -0.88020 |
| `explicit.stat_3695891184@T1` | -0.79700 |
| `explicit.stat_518292764@T2` | -0.67277 |
| `explicit.stat_1263695895@T1` | -0.66973 |
| `explicit.stat_210067635@T1` | -0.62763 |
| `explicit.stat_691932474@T1` | -0.60704 |

## Coverage (listings per base)

- … **Sapphire** — 37652 listings (37587 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 36707 listings (36655 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 28061 listings (28029 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 12887 listings (12869 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11860 listings (11836 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 11530 listings (11504 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 11411 listings (11399 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10698 listings (10671 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10635 listings (10612 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 10095 listings (10082 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8845 listings (8830 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8485 listings (8476 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8410 listings (8401 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7486 listings (7462 priced) [0.3–4297682211.9 ex]
- … **Unset Ring** — 7310 listings (7291 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7299 listings (7292 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 7235 listings (7220 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 7144 listings (7136 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 7051 listings (7021 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 7039 listings (7030 priced) [0.2–275252424.7 ex]
- … **Ancestral Tiara** — 6983 listings (6954 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6923 listings (6913 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6621 listings (6617 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6500 listings (6486 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6235 listings (6222 priced) [0.3–398912568423.8 ex]

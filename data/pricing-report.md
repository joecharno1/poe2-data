# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-22T22:14:05+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **748597** (746187 priced in exalted)
- Distinct bases: 1002 · distinct mods: 3343 · mod rows: 3536972
- Sold signals: **23993** sold · 426166 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-22T22:01:48+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×21.88** (median |log error| 3.0858)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×59.88 · ±30% 5% · n=108550
- Premium segment (60ex+): skill **+0.14** · typical error ×298.90 · ±30% 0% · n=71910

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 16219 | ×45.35 | 21% | +0.04 | +0.06 |
| jewel | 15622 | ×56.50 | 21% | +0.02 | +0.03 |
| accessory.amulet | 14500 | ×23.51 | 16% | +0.04 | +0.04 |
| accessory.belt | 10178 | ×23.75 | 12% | +0.09 | +0.11 |
| armour.chest | 9903 | ×15.78 | 20% | +0.08 | +0.11 |
| armour.helmet | 9634 | ×22.71 | 14% | +0.10 | +0.12 |
| armour.boots | 8875 | ×21.22 | 17% | +0.12 | +0.14 |
| armour.gloves | 8772 | ×27.80 | 11% | +0.10 | +0.12 |
| other | 8709 | ×1.92 | 43% | +0.12 | +0.17 |
| weapon.wand | 5105 | ×32.11 | 12% | +0.13 | +0.14 |
| weapon.bow | 3984 | ×21.47 | 9% | +0.19 | +0.20 |
| weapon.crossbow | 3773 | ×22.85 | 12% | +0.13 | +0.17 |
| weapon.warstaff | 2611 | ×13.72 | 7% | +0.15 | +0.15 |
| weapon.staff | 2537 | ×15.29 | 6% | +0.13 | +0.13 |
| weapon.sceptre | 2481 | ×17.12 | 5% | +0.07 | +0.07 |
| weapon.spear | 1972 | ×12.57 | 7% | +0.13 | +0.17 |
| armour.focus | 1642 | ×12.93 | 6% | +0.09 | +0.11 |
| armour.quiver | 1560 | ×18.26 | 7% | +0.12 | +0.13 |
| armour.shield | 1264 | ×8.09 | 8% | +0.11 | +0.11 |
| flask.charm | 1251 | ×10.00 | 27% | +0.03 | +0.03 |
| weapon.twomace | 1168 | ×8.75 | 6% | +0.09 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=86315, R²=-1.9292

intercept: `-0.0409`  ·  log_price: True  ·  ilvl: `0.00051`  ·  n_mods: `1.02333`  ·  n_top_tier: `-0.93492`  ·  corrupted: `0.96527`  ·  quality: `-0.06877`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 4.55277 |
| `explicit.stat_1604736568@T1` | -1.99373 |
| `explicit.stat_1604736568` | 1.90954 |
| `explicit.stat_3556824919@T1` | 1.25800 |
| `explicit.stat_274716455@T1` | -0.95921 |
| `explicit.stat_2194114101@T1` | -0.56228 |
| `explicit.stat_3174700878@T1` | 0.53273 |
| `explicit.stat_681332047@T1` | -0.41512 |
| `explicit.stat_587431675@T1` | -0.40990 |
| `explicit.stat_3714003708@T1` | 0.33927 |
| `explicit.stat_2023107756@T1` | -0.30881 |
| `pseudo.weapon_spell_power` | 0.29808 |

### accessory.ring — n=73978, R²=-2.0221

intercept: `3.2248`  ·  log_price: True  ·  ilvl: `-0.04043`  ·  n_mods: `0.00163`  ·  n_top_tier: `0.95588`  ·  corrupted: `-0.00313`  ·  n_sockets: `2.21607`  ·  quality: `0.00382`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.00398 |
| `explicit.stat_1263695895@T2` | -0.99550 |
| `explicit.stat_1263695895@T1` | -0.98643 |
| `explicit.stat_1573130764@T2` | -0.98092 |
| `explicit.stat_4080418644@T1` | -0.97586 |
| `explicit.stat_2923486259@T2` | -0.97166 |
| `explicit.stat_2891184298@T1` | -0.97165 |
| `explicit.stat_3917489142@T2` | -0.97073 |
| `explicit.stat_2901986750@T2` | -0.97052 |
| `explicit.stat_1671376347@T2` | -0.97043 |
| `explicit.stat_2144192055@T1` | -0.96796 |
| `explicit.stat_2891184298@T2` | -0.96761 |

### other — n=71255, R²=-0.6839

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.07175`  ·  n_top_tier: `0.27483`  ·  corrupted: `0.00001`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.40761 |
| `explicit.stat_3299347043@T1` | -0.24826 |
| `implicit.stat_2219129443` | 0.22307 |
| `implicit.stat_718638445` | 0.21528 |
| `implicit.stat_3182714256` | 0.21527 |
| `explicit.stat_3917489142@T1` | -0.19936 |
| `explicit.stat_2974417149@T1` | 0.13204 |
| `implicit.stat_958696139` | -0.07174 |
| `explicit.stat_789117908@T1` | -0.06305 |
| `implicit.stat_1416292992` | -0.04784 |
| `explicit.stat_736967255@T1` | -0.04492 |
| `implicit.stat_3879011313` | 0.04432 |

### accessory.amulet — n=66115, R²=-2.0755

intercept: `3.0490`  ·  log_price: True  ·  ilvl: `-0.04040`  ·  n_mods: `-0.00212`  ·  n_top_tier: `0.93903`  ·  corrupted: `0.05952`  ·  n_sockets: `-0.05511`  ·  quality: `0.06793`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.64952 |
| `explicit.stat_3299347043@T2` | -1.61728 |
| `explicit.stat_2866361420@T1` | -1.06412 |
| `explicit.stat_1202301673@T2` | -1.04889 |
| `explicit.stat_4080418644@T1` | -1.04194 |
| `explicit.stat_2974417149@T1` | -1.04139 |
| `explicit.stat_2866361420@T2` | -1.03002 |
| `explicit.stat_803737631@T1` | -1.02302 |
| `explicit.stat_2974417149@T2` | -1.02230 |
| `explicit.stat_2901986750@T1` | -1.01894 |
| `explicit.stat_4080418644@T2` | -0.99897 |
| `explicit.stat_3261801346@T1` | -0.99642 |

### accessory.belt — n=46676, R²=-1.4136

intercept: `5.4233`  ·  log_price: True  ·  ilvl: `-0.06471`  ·  n_mods: `-0.04953`  ·  n_top_tier: `0.92938`  ·  corrupted: `1.13819`  ·  n_sockets: `1.29782`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T2` | -1.10342 |
| `explicit.stat_3299347043@T1` | -1.02309 |
| `explicit.stat_2881298780@T1` | -0.97499 |
| `explicit.stat_51994685@T1` | -0.96529 |
| `explicit.stat_1570770415@T2` | -0.95918 |
| `explicit.stat_2923486259@T1` | 0.94972 |
| `explicit.stat_4080418644@T2` | -0.93947 |
| `explicit.stat_3372524247@T2` | -0.93758 |
| `explicit.stat_809229260@T2` | -0.93521 |
| `explicit.stat_4080418644@T1` | -0.92961 |
| `explicit.stat_915769802@T1` | -0.92324 |
| `explicit.stat_3585532255@T2` | -0.91025 |

### armour.chest — n=46236, R²=-1.7412

intercept: `3.5021`  ·  log_price: True  ·  ilvl: `-0.04288`  ·  n_mods: `-0.02054`  ·  n_top_tier: `0.38154`  ·  corrupted: `0.33219`  ·  n_sockets: `0.04042`  ·  quality: `0.07198`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.00194 |
| `explicit.stat_3981240776@T1` | 0.55879 |
| `explicit.stat_986397080@T2` | -0.45520 |
| `explicit.stat_3484657501@T1` | -0.44472 |
| `explicit.stat_4080418644@T2` | -0.43998 |
| `explicit.stat_986397080@T1` | -0.41670 |
| `explicit.stat_1692879867@T2` | -0.41637 |
| `explicit.stat_1062208444@T2` | -0.41397 |
| `explicit.stat_915769802@T2` | -0.41393 |
| `explicit.stat_1999113824@T1` | -0.40756 |
| `explicit.stat_2451402625@T2` | -0.40677 |
| `explicit.stat_4080418644@T1` | -0.40455 |

### armour.helmet — n=45004, R²=-1.6249

intercept: `3.4533`  ·  log_price: True  ·  ilvl: `-0.04325`  ·  n_mods: `-0.03844`  ·  n_top_tier: `0.53325`  ·  corrupted: `0.57503`  ·  n_sockets: `0.11190`  ·  quality: `0.06581`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.11677 |
| `explicit.stat_1263695895@T1` | -0.96414 |
| `explicit.stat_3917489142@T2` | -0.81547 |
| `explicit.stat_3917489142@T1` | -0.73214 |
| `explicit.stat_2162097452@T2` | -0.68249 |
| `explicit.stat_1263695895@T2` | -0.65811 |
| `crafted.stat_3917489142@T1` | 0.64536 |
| `explicit.stat_4052037485@T2` | -0.63737 |
| `explicit.stat_3321629045@T2` | -0.61756 |
| `explicit.stat_4015621042@T2` | -0.61509 |
| `explicit.stat_1999113824@T1` | -0.61316 |
| `explicit.stat_803737631@T1` | -0.59904 |

### armour.boots — n=41503, R²=-1.6157

intercept: `3.8820`  ·  log_price: True  ·  ilvl: `-0.04759`  ·  n_mods: `-0.04875`  ·  n_top_tier: `0.43501`  ·  corrupted: `0.12045`  ·  n_sockets: `0.07332`  ·  quality: `0.06981`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.16267 |
| `explicit.stat_2250533757@T1` | 1.69699 |
| `crafted.stat_3917489142@T1` | 1.38967 |
| `explicit.stat_3299347043@T1` | -0.62323 |
| `explicit.stat_2923486259@T2` | -0.56514 |
| `explicit.stat_2923486259@T1` | 0.55616 |
| `explicit.stat_1062208444@T2` | -0.50928 |
| `explicit.stat_1874553720@T1` | -0.50924 |
| `explicit.stat_1671376347@T2` | -0.50800 |
| `explicit.stat_2160282525@T1` | -0.50338 |
| `explicit.stat_99927264@T1` | -0.50119 |
| `explicit.stat_2451402625@T1` | -0.49517 |

### armour.gloves — n=40511, R²=-1.5585

intercept: `3.8221`  ·  log_price: True  ·  ilvl: `-0.05035`  ·  n_mods: `-0.00805`  ·  n_top_tier: `0.69829`  ·  corrupted: `-0.00297`  ·  n_sockets: `0.22299`  ·  quality: `0.05553`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.06612 |
| `explicit.stat_4052037485@T1` | -1.01478 |
| `explicit.stat_3321629045@T2` | -0.95614 |
| `explicit.stat_4052037485@T2` | -0.95071 |
| `explicit.stat_3917489142@T2` | -0.93077 |
| `explicit.stat_2339757871@T1` | 0.91089 |
| `explicit.stat_124859000@T1` | -0.90219 |
| `explicit.stat_4015621042@T2` | -0.89589 |
| `explicit.stat_3484657501@T1` | -0.89411 |
| `explicit.stat_3484657501@T2` | -0.88476 |
| `explicit.stat_803737631@T2` | -0.85038 |
| `explicit.stat_2923486259@T2` | -0.83327 |

### weapon.wand — n=23707, R²=-1.7758

intercept: `3.7560`  ·  log_price: True  ·  ilvl: `-0.04637`  ·  n_mods: `-0.07897`  ·  n_top_tier: `0.63928`  ·  corrupted: `0.33944`  ·  n_sockets: `0.02359`  ·  quality: `0.02659`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.07661 |
| `explicit.stat_2254480358@T1` | 2.57325 |
| `explicit.stat_1545858329@T1` | 2.40034 |
| `explicit.stat_124131830@T1` | 1.84035 |
| `explicit.stat_591105508@T1` | 1.80548 |
| `explicit.stat_4226189338@T1` | 1.55857 |
| `explicit.stat_2254480358@T2` | 1.26974 |
| `crafted.stat_124131830` | 1.23536 |
| `explicit.stat_1263695895@T2` | -1.03700 |
| `explicit.stat_473429811@T1` | -1.02737 |
| `explicit.stat_473429811@T2` | -0.98908 |
| `explicit.stat_3962278098@T2` | -0.89404 |

### flask.charm — n=21067, R²=-0.6738

intercept: `0.1059`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.20854`  ·  corrupted: `1.53242`  ·  quality: `0.01710`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.59516 |
| `explicit.stat_1056492907` | 2.53281 |
| `explicit.stat_3246948616` | 2.29331 |
| `explicit.stat_828533480@T2` | -1.20857 |
| `explicit.stat_1120862500@T2` | -1.20855 |
| `explicit.stat_1873752457@T2` | -1.20854 |
| `explicit.stat_2541588185@T2` | -1.20853 |
| `explicit.stat_2365392475@T2` | -1.20847 |
| `explicit.stat_388617051@T2` | -1.20845 |
| `explicit.stat_3196823591@T2` | -1.20827 |
| `explicit.stat_1873752457@T1` | -1.20691 |
| `explicit.stat_2676834156@T2` | -1.20323 |

### weapon.bow — n=18945, R²=-1.6004

intercept: `4.0197`  ·  log_price: True  ·  ilvl: `-0.04678`  ·  n_mods: `-0.12810`  ·  n_top_tier: `0.71602`  ·  corrupted: `0.54728`  ·  n_sockets: `0.07771`  ·  quality: `0.02831`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 5.40651 |
| `explicit.stat_1263695895@T1` | -1.56174 |
| `desecrated.stat_210067635@T1` | -1.47895 |
| `crafted.stat_210067635@T2` | -1.38357 |
| `explicit.stat_1263695895@T2` | -1.31274 |
| `crafted.stat_3035140377` | 1.12422 |
| `explicit.stat_2463230181@T2` | -1.07833 |
| `explicit.stat_1509134228@T1` | -1.04529 |
| `explicit.stat_3695891184@T1` | -0.97059 |
| `explicit.stat_210067635@T2` | -0.94170 |
| `explicit.stat_2463230181@T1` | -0.92757 |
| `explicit.stat_821021828@T2` | -0.87206 |

### weapon.crossbow — n=17729, R²=-1.588

intercept: `4.0693`  ·  log_price: True  ·  ilvl: `-0.04722`  ·  n_mods: `-0.12389`  ·  n_top_tier: `0.31779`  ·  corrupted: `-0.04027`  ·  n_sockets: `0.11356`  ·  quality: `0.01283`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.74000 |
| `explicit.stat_1980802737` | 1.49468 |
| `explicit.stat_1202301673@T1` | 1.36116 |
| `explicit.stat_2250681686@T2` | -1.26374 |
| `explicit.stat_2250681686` | 1.03613 |
| `explicit.stat_1509134228@T1` | 0.99017 |
| `explicit.stat_709508406@T1` | 0.88021 |
| `crafted.stat_3035140377` | 0.85604 |
| `rune.stat_731403740` | 0.69061 |
| `explicit.stat_210067635@T2` | -0.63601 |
| `explicit.stat_3336890334@T2` | -0.61426 |
| `explicit.stat_3695891184@T1` | -0.55166 |

### weapon.warstaff — n=12588, R²=-0.3276

intercept: `-10.8528`  ·  log_price: True  ·  ilvl: `0.14715`  ·  n_mods: `-0.22922`  ·  n_top_tier: `0.53849`  ·  corrupted: `0.38712`  ·  n_sockets: `0.11812`  ·  quality: `0.05249`

| stat_id | coef |
|---|---|
| `desecrated.stat_473429811@T1` | -1.04716 |
| `desecrated.stat_3291658075@T1` | -1.04716 |
| `explicit.stat_328541901@T1` | -0.99308 |
| `explicit.stat_210067635@T1` | -0.96595 |
| `explicit.stat_328541901@T2` | -0.95972 |
| `crafted.stat_210067635@T2` | 0.94908 |
| `explicit.stat_821021828@T2` | -0.93054 |
| `explicit.stat_1037193709@T2` | -0.80339 |
| `desecrated.stat_9187492` | 0.78575 |
| `rune.stat_243313994` | 0.78317 |
| `explicit.stat_1940865751@T1` | -0.76474 |
| `explicit.stat_1940865751@T2` | -0.74394 |

### weapon.staff — n=12002, R²=-0.3477

intercept: `-16.7172`  ·  log_price: True  ·  ilvl: `0.21550`  ·  n_mods: `-0.10865`  ·  n_top_tier: `0.56073`  ·  corrupted: `0.93695`  ·  n_sockets: `0.18353`  ·  quality: `0.03156`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 1.91184 |
| `explicit.stat_4226189338@T1` | 1.57119 |
| `explicit.stat_124131830@T1` | 1.55148 |
| `explicit.stat_1600707273@T1` | 1.49170 |
| `rune.stat_124131830` | 1.25648 |
| `explicit.stat_1545858329@T1` | 1.13321 |
| `explicit.stat_3962278098@T2` | 1.05210 |
| `explicit.stat_473429811@T2` | -0.88609 |
| `explicit.stat_3015669065@T2` | -0.71443 |
| `explicit.stat_591105508@T2` | 0.69934 |
| `explicit.stat_293638271@T2` | -0.65361 |
| `explicit.stat_1050105434@T2` | -0.57801 |

### weapon.sceptre — n=11639, R²=-0.3291

intercept: `-21.5606`  ·  log_price: True  ·  ilvl: `0.27486`  ·  n_mods: `-0.04340`  ·  n_top_tier: `0.21651`  ·  corrupted: `0.24692`  ·  n_sockets: `0.21274`  ·  quality: `0.03374`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.44075 |
| `explicit.stat_2162097452@T2` | 1.00182 |
| `explicit.stat_4080418644@T2` | -0.96992 |
| `explicit.stat_1798257884@T2` | 0.87479 |
| `explicit.stat_3057012405@T1` | 0.83982 |
| `explicit.stat_2854751904@T2` | -0.58635 |
| `explicit.stat_101878827@T1` | 0.58530 |
| `explicit.stat_1574590649@T2` | -0.48393 |
| `explicit.stat_101878827@T2` | 0.41655 |
| `explicit.stat_849987426@T1` | 0.41440 |
| `explicit.stat_1998951374@T1` | 0.40708 |
| `explicit.stat_2347036682@T1` | 0.39041 |

### weapon.spear — n=9486, R²=-0.3793

intercept: `-14.4071`  ·  log_price: True  ·  ilvl: `0.19461`  ·  n_mods: `-0.14951`  ·  n_top_tier: `0.55285`  ·  corrupted: `-0.54816`  ·  n_sockets: `0.23130`  ·  quality: `0.06557`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.59749 |
| `desecrated.stat_666077204@T1` | -1.43509 |
| `explicit.stat_1037193709@T1` | -1.28473 |
| `crafted.stat_3035140377` | 1.11094 |
| `desecrated.stat_210067635@T1` | -1.07182 |
| `explicit.stat_4080418644@T2` | -1.01663 |
| `explicit.stat_9187492@T2` | -0.93445 |
| `explicit.stat_4080418644@T1` | -0.92993 |
| `explicit.stat_1940865751@T2` | -0.91660 |
| `explicit.stat_3336890334@T2` | -0.89228 |
| `explicit.stat_748522257@T2` | -0.87572 |
| `explicit.stat_1202301673@T1` | 0.87372 |

### armour.focus — n=7753, R²=-0.34

intercept: `-16.1654`  ·  log_price: True  ·  ilvl: `0.20511`  ·  n_mods: `-0.15540`  ·  n_top_tier: `0.96999`  ·  corrupted: `-0.10480`  ·  n_sockets: `0.42243`  ·  quality: `0.02917`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.79167 |
| `explicit.stat_4220027924@T1` | -1.46894 |
| `crafted.stat_737908626@T2` | 1.37672 |
| `explicit.stat_2923486259@T2` | -1.31573 |
| `explicit.stat_3962278098@T2` | -1.26315 |
| `explicit.stat_2231156303@T1` | -1.20735 |
| `explicit.stat_2768835289@T1` | -1.16203 |
| `explicit.stat_2339757871@T2` | -1.15368 |
| `explicit.stat_4220027924@T2` | -1.10691 |
| `explicit.stat_4015621042@T1` | -1.09949 |
| `explicit.stat_3291658075@T2` | -1.09840 |
| `explicit.stat_737908626@T2` | -1.07609 |

### armour.quiver — n=7216, R²=-0.2653

intercept: `-18.6553`  ·  log_price: True  ·  ilvl: `0.22499`  ·  n_mods: `-0.05718`  ·  n_top_tier: `0.71874`  ·  corrupted: `0.96373`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.65540 |
| `explicit.stat_681332047@T2` | -1.31441 |
| `explicit.stat_681332047@T1` | -1.10161 |
| `explicit.stat_1573130764@T2` | -1.00715 |
| `explicit.stat_2194114101@T2` | -0.91661 |
| `explicit.stat_1573130764@T1` | -0.82477 |
| `explicit.stat_2321178454@T2` | -0.82168 |
| `explicit.stat_3714003708@T2` | -0.71473 |
| `explicit.stat_4067062424@T1` | -0.71265 |
| `explicit.stat_803737631@T1` | -0.69463 |
| `explicit.stat_3261801346@T1` | -0.64977 |
| `explicit.stat_4067062424@T2` | -0.62983 |

### armour.shield — n=6204, R²=-0.4016

intercept: `-13.5716`  ·  log_price: True  ·  ilvl: `0.18334`  ·  n_mods: `-0.17419`  ·  n_top_tier: `0.69127`  ·  corrupted: `-0.57580`  ·  n_sockets: `0.35855`  ·  quality: `0.04436`

| stat_id | coef |
|---|---|
| `explicit.stat_4095671657@T1` | -1.60563 |
| `explicit.stat_3855016469@T1` | -1.56882 |
| `explicit.stat_2901986750@T1` | -1.33448 |
| `explicit.stat_4095671657@T2` | -1.33269 |
| `explicit.stat_1011760251@T1` | -1.30734 |
| `explicit.stat_328541901@T1` | -1.29690 |
| `explicit.stat_3033371881@T2` | -1.28234 |
| `explicit.stat_2923486259@T1` | -1.22722 |
| `explicit.stat_328541901@T2` | -1.11184 |
| `explicit.stat_2481353198@T1` | -1.06305 |
| `explicit.stat_2339757871@T1` | -1.05787 |
| `explicit.stat_2901986750@T2` | -1.04877 |

### weapon.twomace — n=5662, R²=-0.4289

intercept: `-11.2563`  ·  log_price: True  ·  ilvl: `0.15395`  ·  n_mods: `-0.21183`  ·  n_top_tier: `0.42040`  ·  corrupted: `0.83482`  ·  n_sockets: `0.17063`  ·  quality: `0.06112`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -5.40412 |
| `desecrated.stat_1509134228@T1` | 2.54561 |
| `explicit.stat_1037193709@T1` | -1.52084 |
| `explicit.stat_3336890334@T1` | -1.32582 |
| `explicit.stat_9187492@T1` | -1.02021 |
| `explicit.stat_1263695895@T2` | -0.97145 |
| `explicit.stat_2694482655@T1` | 0.95066 |
| `explicit.stat_210067635@T1` | -0.81219 |
| `explicit.stat_3695891184@T2` | -0.57453 |
| `explicit.stat_1037193709@T2` | -0.55083 |
| `explicit.stat_709508406@T1` | 0.54781 |
| `explicit.stat_518292764@T2` | -0.54239 |

## Coverage (listings per base)

- … **Sapphire** — 39657 listings (39591 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 38547 listings (38494 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 29515 listings (29483 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 13316 listings (13297 priced) [0.2–398916549611043.2 ex]
- … **Prismatic Ring** — 12359 listings (12332 priced) [0.2–398916549611043.2 ex]
- … **Solar Amulet** — 12001 listings (11975 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 11882 listings (11867 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 11133 listings (11106 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 11114 listings (11091 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 10509 listings (10496 priced) [0.3–398916549611043.2 ex]
- … **Sapphire Ring** — 9211 listings (9196 priced) [0.2–398916549611043.2 ex]
- … **Topaz Ring** — 8878 listings (8867 priced) [0.3–398916549611043.2 ex]
- … **Ruby Ring** — 8782 listings (8773 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7678 listings (7654 priced) [0.3–398916553600208.8 ex]
- … **Unset Ring** — 7610 listings (7588 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7557 listings (7549 priced) [0.3–398916549611043.2 ex]
- … **Jade Amulet** — 7510 listings (7494 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 7440 listings (7432 priced) [0.3–3985176410.3 ex]
- … **Pearl Ring** — 7357 listings (7348 priced) [0.2–398916549611043.2 ex]
- … **Plate Belt** — 7291 listings (7259 priced) [0.3–398916553600208.8 ex]
- … **Ancestral Tiara** — 7235 listings (7204 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 7197 listings (7185 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6873 listings (6869 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6804 listings (6789 priced) [0.3–398916549611043.2 ex]
- … **Heavy Belt** — 6437 listings (6421 priced) [0.3–398916553600208.8 ex]

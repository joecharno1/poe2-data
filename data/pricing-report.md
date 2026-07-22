# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-22T16:00:09+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **741166** (738779 priced in exalted)
- Distinct bases: 1002 · distinct mods: 3336 · mod rows: 3502228
- Sold signals: **24021** sold · 421729 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-22T15:47:02+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×18.70** (median |log error| 2.9284)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.15** · typical error ×50.26 · ±30% 5% · n=107447
- Premium segment (60ex+): skill **+0.15** · typical error ×277.77 · ±30% 0% · n=71326

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 16009 | ×45.65 | 21% | +0.04 | +0.07 |
| jewel | 15431 | ×10.28 | 5% | +0.11 | +0.13 |
| accessory.amulet | 14357 | ×28.14 | 17% | +0.04 | +0.04 |
| accessory.belt | 10051 | ×24.62 | 18% | +0.06 | +0.08 |
| armour.chest | 9803 | ×15.61 | 22% | +0.08 | +0.11 |
| armour.helmet | 9496 | ×23.18 | 17% | +0.09 | +0.11 |
| armour.boots | 8798 | ×22.00 | 18% | +0.11 | +0.13 |
| armour.gloves | 8692 | ×31.78 | 13% | +0.08 | +0.11 |
| other | 8605 | ×2.00 | 43% | +0.11 | +0.17 |
| weapon.wand | 5067 | ×38.85 | 14% | +0.11 | +0.13 |
| weapon.bow | 3995 | ×21.74 | 8% | +0.19 | +0.22 |
| weapon.crossbow | 3757 | ×21.39 | 10% | +0.15 | +0.17 |
| weapon.warstaff | 2594 | ×13.73 | 7% | +0.16 | +0.16 |
| weapon.staff | 2502 | ×15.38 | 6% | +0.13 | +0.13 |
| weapon.sceptre | 2432 | ×17.95 | 5% | +0.06 | +0.07 |
| weapon.spear | 1981 | ×12.98 | 7% | +0.12 | +0.15 |
| armour.focus | 1625 | ×13.16 | 6% | +0.09 | +0.10 |
| armour.quiver | 1539 | ×17.06 | 7% | +0.12 | +0.13 |
| armour.shield | 1256 | ×7.87 | 8% | +0.11 | +0.11 |
| flask.charm | 1251 | ×10.00 | 27% | +0.03 | +0.03 |
| weapon.twomace | 1159 | ×8.70 | 6% | +0.10 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=85162, R²=-0.9961

intercept: `-1.8949`  ·  log_price: True  ·  ilvl: `0.02369`  ·  n_mods: `0.72300`  ·  n_top_tier: `-0.14742`  ·  corrupted: `0.46249`  ·  quality: `-0.14865`

| stat_id | coef |
|---|---|
| `explicit.stat_1869147066@T1` | -3.40276 |
| `explicit.stat_3192728503@T1` | -3.04148 |
| `explicit.stat_3668351662@T1` | -2.05607 |
| `explicit.stat_1594812856@T1` | 1.93938 |
| `explicit.stat_3485067555@T1` | 1.75505 |
| `explicit.stat_239367161@T1` | -1.62034 |
| `explicit.stat_1697447343@T1` | -1.42653 |
| `explicit.stat_3028809864@T1` | -1.41514 |
| `explicit.stat_2456523742@T1` | 1.30637 |
| `explicit.stat_3780644166@T1` | -1.25569 |
| `explicit.stat_3377888098@T1` | -1.21635 |
| `explicit.stat_429143663@T1` | 1.17540 |

### accessory.ring — n=73129, R²=-2.0178

intercept: `3.1347`  ·  log_price: True  ·  ilvl: `-0.03930`  ·  n_mods: `0.00080`  ·  n_top_tier: `0.97727`  ·  corrupted: `-0.00542`  ·  n_sockets: `2.20944`  ·  quality: `-0.00006`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.01613 |
| `explicit.stat_1263695895@T2` | -1.00823 |
| `explicit.stat_1573130764@T2` | -1.00030 |
| `explicit.stat_1263695895@T1` | -0.99658 |
| `explicit.stat_3917489142@T2` | -0.99593 |
| `explicit.stat_4080418644@T1` | -0.99531 |
| `explicit.stat_2923486259@T2` | -0.99466 |
| `explicit.stat_2891184298@T2` | -0.99398 |
| `explicit.stat_3325883026@T1` | -0.99368 |
| `explicit.stat_1671376347@T2` | -0.99277 |
| `explicit.stat_2891184298@T1` | -0.99267 |
| `explicit.stat_3372524247@T2` | -0.99182 |

### other — n=70561, R²=-0.6861

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.04079`  ·  n_top_tier: `0.30579`  ·  corrupted: `0.00001`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.40569 |
| `explicit.stat_3299347043@T1` | -0.24593 |
| `implicit.stat_2219129443` | 0.22617 |
| `explicit.stat_3917489142@T1` | -0.18157 |
| `implicit.stat_718638445` | 0.12240 |
| `implicit.stat_3182714256` | 0.12240 |
| `explicit.stat_2974417149@T1` | 0.10957 |
| `explicit.stat_789117908@T1` | -0.07399 |
| `implicit.stat_3879011313` | 0.05500 |
| `explicit.stat_736967255@T1` | -0.04983 |
| `implicit.stat_958696139` | -0.04078 |
| `explicit.stat_2106365538@T1` | -0.03272 |

### accessory.amulet — n=65409, R²=-2.1008

intercept: `3.1266`  ·  log_price: True  ·  ilvl: `-0.04081`  ·  n_mods: `-0.00440`  ·  n_top_tier: `0.94020`  ·  corrupted: `0.06596`  ·  n_sockets: `-0.10905`  ·  quality: `0.06706`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.67292 |
| `explicit.stat_3299347043@T2` | -1.54212 |
| `explicit.stat_1202301673@T2` | -1.07162 |
| `explicit.stat_2866361420@T1` | -1.06289 |
| `explicit.stat_2901986750@T1` | -1.04339 |
| `explicit.stat_2974417149@T1` | -1.03761 |
| `explicit.stat_2974417149@T2` | -1.02791 |
| `explicit.stat_4080418644@T1` | -1.02596 |
| `explicit.stat_2866361420@T2` | -1.02376 |
| `explicit.stat_803737631@T1` | -1.01894 |
| `explicit.stat_803737631@T2` | -0.99247 |
| `explicit.stat_1050105434@T2` | -0.98581 |

### accessory.belt — n=46218, R²=-1.7308

intercept: `4.2835`  ·  log_price: True  ·  ilvl: `-0.05176`  ·  n_mods: `-0.02433`  ·  n_top_tier: `0.69389`  ·  corrupted: `1.14587`  ·  n_sockets: `1.53150`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.00423 |
| `explicit.stat_3299347043@T2` | -0.73284 |
| `explicit.stat_2881298780@T1` | -0.72853 |
| `explicit.stat_51994685@T1` | -0.72280 |
| `explicit.stat_915769802@T1` | -0.72087 |
| `explicit.stat_3299347043@T1` | -0.71422 |
| `explicit.stat_809229260@T2` | -0.71421 |
| `explicit.stat_1570770415@T2` | -0.70466 |
| `explicit.stat_3325883026@T1` | -0.70273 |
| `explicit.stat_915769802@T2` | -0.70094 |
| `explicit.stat_3372524247@T2` | -0.69900 |
| `explicit.stat_1570770415@T1` | -0.69729 |

### armour.chest — n=45833, R²=-1.8219

intercept: `3.1943`  ·  log_price: True  ·  ilvl: `-0.03934`  ·  n_mods: `-0.01360`  ·  n_top_tier: `0.31879`  ·  corrupted: `0.27549`  ·  n_sockets: `0.02142`  ·  quality: `0.07755`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.99405 |
| `explicit.stat_986397080@T2` | -0.36601 |
| `explicit.stat_4080418644@T2` | -0.35537 |
| `explicit.stat_1692879867@T2` | -0.34949 |
| `explicit.stat_986397080@T1` | -0.34730 |
| `explicit.stat_915769802@T2` | -0.34477 |
| `explicit.stat_4080418644@T1` | -0.34259 |
| `explicit.stat_3484657501@T1` | -0.33661 |
| `explicit.stat_915769802@T1` | -0.33496 |
| `explicit.stat_1062208444@T2` | -0.33454 |
| `explicit.stat_2451402625@T2` | -0.33418 |
| `explicit.stat_2339757871@T2` | -0.32909 |

### armour.helmet — n=44617, R²=-1.7477

intercept: `3.2726`  ·  log_price: True  ·  ilvl: `-0.04091`  ·  n_mods: `-0.02416`  ·  n_top_tier: `0.52079`  ·  corrupted: `0.60996`  ·  n_sockets: `0.07921`  ·  quality: `0.06926`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.60279 |
| `crafted.stat_3917489142@T1` | 1.62512 |
| `explicit.stat_1263695895@T1` | -0.84107 |
| `explicit.stat_3917489142@T2` | -0.70232 |
| `explicit.stat_2162097452@T2` | -0.69826 |
| `explicit.stat_3917489142@T1` | -0.64484 |
| `explicit.stat_4052037485@T2` | -0.63700 |
| `explicit.stat_1263695895@T2` | -0.62065 |
| `explicit.stat_4052037485@T1` | -0.58661 |
| `explicit.stat_4015621042@T2` | -0.56544 |
| `explicit.stat_3321629045@T2` | -0.56145 |
| `explicit.stat_1999113824@T1` | -0.55273 |

### armour.boots — n=41156, R²=-1.6935

intercept: `3.7196`  ·  log_price: True  ·  ilvl: `-0.04592`  ·  n_mods: `-0.03010`  ·  n_top_tier: `0.42235`  ·  corrupted: `0.07522`  ·  n_sockets: `0.06507`  ·  quality: `0.07221`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.97277 |
| `explicit.stat_2250533757@T1` | 1.78036 |
| `crafted.stat_3917489142@T1` | 1.41728 |
| `explicit.stat_2923486259@T1` | 0.65788 |
| `explicit.stat_3299347043@T1` | -0.56937 |
| `explicit.stat_2923486259@T2` | -0.55587 |
| `explicit.stat_1671376347@T2` | -0.48474 |
| `explicit.stat_99927264@T1` | -0.48194 |
| `explicit.stat_328541901@T2` | -0.48142 |
| `explicit.stat_1874553720@T1` | -0.48034 |
| `explicit.stat_2160282525@T1` | -0.47964 |
| `explicit.stat_2451402625@T1` | -0.46329 |

### armour.gloves — n=40169, R²=-1.6913

intercept: `3.7610`  ·  log_price: True  ·  ilvl: `-0.04943`  ·  n_mods: `-0.00501`  ·  n_top_tier: `0.69478`  ·  corrupted: `-0.05185`  ·  n_sockets: `0.18475`  ·  quality: `0.05786`

| stat_id | coef |
|---|---|
| `explicit.stat_4052037485@T1` | -1.05438 |
| `explicit.stat_4052037485@T2` | -1.00456 |
| `explicit.stat_3484657501@T2` | -0.92032 |
| `explicit.stat_3321629045@T2` | -0.89976 |
| `explicit.stat_3484657501@T1` | -0.88816 |
| `explicit.stat_4015621042@T2` | -0.86328 |
| `explicit.stat_9187492@T2` | -0.84886 |
| `explicit.stat_803737631@T1` | -0.81438 |
| `explicit.stat_124859000@T1` | -0.80935 |
| `explicit.stat_3917489142@T2` | -0.80892 |
| `explicit.stat_2923486259@T1` | -0.80142 |
| `explicit.stat_328541901@T2` | -0.77497 |

### weapon.wand — n=23542, R²=-1.9361

intercept: `3.9133`  ·  log_price: True  ·  ilvl: `-0.04832`  ·  n_mods: `-0.06698`  ·  n_top_tier: `0.55952`  ·  corrupted: `0.10676`  ·  n_sockets: `0.01609`  ·  quality: `0.03713`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.34740 |
| `explicit.stat_1545858329@T1` | 2.96608 |
| `explicit.stat_2254480358@T1` | 2.52925 |
| `explicit.stat_591105508@T1` | 2.21111 |
| `explicit.stat_124131830@T1` | 1.98317 |
| `explicit.stat_4226189338@T1` | 1.53529 |
| `crafted.stat_124131830` | 1.26960 |
| `explicit.stat_2254480358@T2` | 1.23325 |
| `explicit.stat_1600707273@T1` | 1.16279 |
| `explicit.stat_1263695895@T2` | -0.99548 |
| `explicit.stat_1263695895@T1` | -0.87498 |
| `explicit.stat_2768835289@T2` | 0.79101 |

### flask.charm — n=20809, R²=-0.6674

intercept: `0.1075`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.60976`  ·  corrupted: `1.50754`  ·  quality: `0.02545`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60512 |
| `explicit.stat_1056492907` | 2.52614 |
| `explicit.stat_3246948616` | 2.07433 |
| `explicit.stat_828533480@T2` | -1.60979 |
| `explicit.stat_1120862500@T2` | -1.60977 |
| `explicit.stat_1873752457@T2` | -1.60976 |
| `explicit.stat_2541588185@T2` | -1.60975 |
| `explicit.stat_388617051@T2` | -1.60973 |
| `explicit.stat_2365392475@T2` | -1.60969 |
| `explicit.stat_3196823591@T2` | -1.60883 |
| `explicit.stat_1873752457@T1` | -1.60862 |
| `explicit.stat_2676834156@T2` | -1.60687 |

### weapon.bow — n=18826, R²=-1.5654

intercept: `4.0077`  ·  log_price: True  ·  ilvl: `-0.04609`  ·  n_mods: `-0.13964`  ·  n_top_tier: `0.70487`  ·  corrupted: `0.55021`  ·  n_sockets: `0.10383`  ·  quality: `0.03008`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 3.85275 |
| `explicit.stat_1263695895@T1` | -1.61760 |
| `crafted.stat_210067635@T2` | -1.52973 |
| `explicit.stat_1263695895@T2` | -1.44117 |
| `desecrated.stat_210067635@T1` | -1.40635 |
| `crafted.stat_3035140377` | 1.10208 |
| `explicit.stat_1509134228@T1` | -1.03175 |
| `explicit.stat_210067635@T2` | -0.92894 |
| `explicit.stat_3695891184@T1` | -0.91044 |
| `explicit.stat_2463230181@T2` | -0.90784 |
| `explicit.stat_1368271171@T2` | -0.89515 |
| `explicit.stat_2463230181@T1` | -0.81430 |

### weapon.crossbow — n=17630, R²=-1.5038

intercept: `4.1061`  ·  log_price: True  ·  ilvl: `-0.04703`  ·  n_mods: `-0.15023`  ·  n_top_tier: `0.40066`  ·  corrupted: `-0.01741`  ·  n_sockets: `0.11428`  ·  quality: `0.01576`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.92705 |
| `explicit.stat_1980802737` | 1.44941 |
| `explicit.stat_2250681686@T2` | -1.38357 |
| `explicit.stat_1202301673@T1` | 1.08099 |
| `explicit.stat_2250681686` | 1.06874 |
| `explicit.stat_1509134228@T1` | 0.87300 |
| `explicit.stat_3695891184@T1` | -0.83870 |
| `crafted.stat_3035140377` | 0.82420 |
| `explicit.stat_709508406@T1` | 0.78076 |
| `explicit.stat_3695891184@T2` | -0.76923 |
| `explicit.stat_3336890334@T2` | -0.75876 |
| `explicit.stat_210067635@T2` | -0.71577 |

### weapon.warstaff — n=12457, R²=-0.3279

intercept: `-10.7071`  ·  log_price: True  ·  ilvl: `0.14589`  ·  n_mods: `-0.23083`  ·  n_top_tier: `0.52445`  ·  corrupted: `0.31110`  ·  n_sockets: `0.11489`  ·  quality: `0.05139`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 1.09026 |
| `desecrated.stat_2527686725@T1` | 1.09026 |
| `explicit.stat_821021828@T2` | -0.96709 |
| `explicit.stat_210067635@T1` | -0.96291 |
| `crafted.stat_210067635@T2` | 0.95942 |
| `explicit.stat_1037193709@T2` | -0.85136 |
| `explicit.stat_328541901@T2` | -0.81535 |
| `explicit.stat_328541901@T1` | -0.80096 |
| `rune.stat_243313994` | 0.79258 |
| `desecrated.stat_9187492` | 0.78939 |
| `explicit.stat_1940865751@T2` | -0.72097 |
| `explicit.stat_1940865751@T1` | -0.70045 |

### weapon.staff — n=11896, R²=-0.3486

intercept: `-16.6873`  ·  log_price: True  ·  ilvl: `0.21423`  ·  n_mods: `-0.10751`  ·  n_top_tier: `0.49129`  ·  corrupted: `0.90625`  ·  n_sockets: `0.20052`  ·  quality: `0.03952`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.07221 |
| `explicit.stat_124131830@T1` | 1.87949 |
| `explicit.stat_4226189338@T1` | 1.45479 |
| `explicit.stat_1600707273@T1` | 1.42854 |
| `explicit.stat_1545858329@T1` | 1.20996 |
| `explicit.stat_3962278098@T2` | 0.89194 |
| `explicit.stat_591105508@T2` | 0.88920 |
| `explicit.stat_293638271@T2` | -0.86947 |
| `explicit.stat_473429811@T2` | -0.72934 |
| `explicit.stat_124131830@T2` | 0.64528 |
| `explicit.stat_1263695895@T1` | 0.58890 |
| `rune.stat_124131830` | 0.56487 |

### weapon.sceptre — n=11541, R²=-0.3345

intercept: `-21.4329`  ·  log_price: True  ·  ilvl: `0.27314`  ·  n_mods: `-0.02008`  ·  n_top_tier: `0.16552`  ·  corrupted: `0.27626`  ·  n_sockets: `0.21081`  ·  quality: `0.03368`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.56733 |
| `explicit.stat_2162097452@T2` | 1.15229 |
| `explicit.stat_1798257884@T2` | 0.99978 |
| `explicit.stat_3057012405@T1` | 0.83757 |
| `explicit.stat_4080418644@T2` | -0.75805 |
| `explicit.stat_101878827@T1` | 0.66858 |
| `explicit.stat_101878827@T2` | 0.66590 |
| `explicit.stat_2854751904@T2` | -0.51782 |
| `explicit.stat_2347036682@T1` | 0.47925 |
| `explicit.stat_1250712710@T2` | 0.41670 |
| `explicit.stat_1263695895@T2` | -0.40824 |
| `explicit.stat_849987426@T1` | 0.39431 |

### weapon.spear — n=9384, R²=-0.3819

intercept: `-13.7926`  ·  log_price: True  ·  ilvl: `0.18911`  ·  n_mods: `-0.17482`  ·  n_top_tier: `0.54237`  ·  corrupted: `-0.46980`  ·  n_sockets: `0.21542`  ·  quality: `0.06756`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.32022 |
| `desecrated.stat_666077204@T1` | -2.10839 |
| `explicit.stat_1037193709@T1` | -1.12658 |
| `crafted.stat_3035140377` | 1.09332 |
| `explicit.stat_4080418644@T2` | -1.03492 |
| `desecrated.stat_210067635@T1` | -1.00369 |
| `explicit.stat_9187492@T2` | -0.97123 |
| `explicit.stat_1202301673@T1` | 0.96004 |
| `explicit.stat_748522257@T2` | -0.93468 |
| `explicit.stat_1940865751@T2` | -0.93003 |
| `explicit.stat_4080418644@T1` | -0.89885 |
| `explicit.stat_3336890334@T2` | -0.85491 |

### armour.focus — n=7675, R²=-0.3383

intercept: `-16.4757`  ·  log_price: True  ·  ilvl: `0.20954`  ·  n_mods: `-0.13995`  ·  n_top_tier: `0.93864`  ·  corrupted: `-0.16990`  ·  n_sockets: `0.44699`  ·  quality: `0.03009`

| stat_id | coef |
|---|---|
| `explicit.stat_4220027924@T1` | -1.62556 |
| `crafted.stat_737908626@T2` | 1.49542 |
| `explicit.stat_2923486259@T1` | -1.39784 |
| `explicit.stat_2923486259@T2` | -1.38668 |
| `explicit.stat_2768835289@T1` | -1.28963 |
| `explicit.stat_2231156303@T1` | -1.23120 |
| `explicit.stat_3962278098@T2` | -1.20856 |
| `explicit.stat_2339757871@T2` | -1.19304 |
| `crafted.stat_2974417149@T1` | 1.19222 |
| `explicit.stat_4220027924@T2` | -1.11836 |
| `explicit.stat_3291658075@T2` | -1.06878 |
| `explicit.stat_2231156303@T2` | -1.06392 |

### armour.quiver — n=7140, R²=-0.2705

intercept: `-18.5932`  ·  log_price: True  ·  ilvl: `0.22412`  ·  n_mods: `-0.08057`  ·  n_top_tier: `0.73536`  ·  corrupted: `1.01884`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.08214 |
| `explicit.stat_681332047@T2` | -1.27162 |
| `explicit.stat_681332047@T1` | -1.05647 |
| `explicit.stat_1573130764@T2` | -1.05028 |
| `explicit.stat_1573130764@T1` | -0.95949 |
| `explicit.stat_2194114101@T2` | -0.89591 |
| `explicit.stat_2321178454@T2` | -0.84600 |
| `explicit.stat_2463230181@T1` | 0.83686 |
| `explicit.stat_803737631@T1` | -0.78352 |
| `explicit.stat_3714003708@T2` | -0.76549 |
| `explicit.stat_4067062424@T1` | -0.67612 |
| `explicit.stat_4067062424@T2` | -0.63930 |

### armour.shield — n=6157, R²=-0.4104

intercept: `-13.2106`  ·  log_price: True  ·  ilvl: `0.17879`  ·  n_mods: `-0.18094`  ·  n_top_tier: `0.63608`  ·  corrupted: `-0.46597`  ·  n_sockets: `0.34713`  ·  quality: `0.04564`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.54104 |
| `explicit.stat_4095671657@T1` | -1.45664 |
| `explicit.stat_3033371881@T2` | -1.33789 |
| `explicit.stat_1011760251@T1` | -1.28381 |
| `explicit.stat_2901986750@T1` | -1.27482 |
| `explicit.stat_328541901@T1` | -1.23348 |
| `explicit.stat_4095671657@T2` | -1.18729 |
| `explicit.stat_328541901@T2` | -1.10487 |
| `explicit.stat_2339757871@T1` | -1.02439 |
| `explicit.stat_2481353198@T1` | -1.01180 |
| `explicit.stat_4052037485@T1` | -0.99157 |
| `explicit.stat_3321629045@T2` | -0.98229 |

### weapon.twomace — n=5610, R²=-0.4278

intercept: `-11.0103`  ·  log_price: True  ·  ilvl: `0.15085`  ·  n_mods: `-0.22396`  ·  n_top_tier: `0.52410`  ·  corrupted: `0.70514`  ·  n_sockets: `0.19144`  ·  quality: `0.05908`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -5.82632 |
| `desecrated.stat_1509134228@T1` | 2.56272 |
| `explicit.stat_1037193709@T1` | -1.71288 |
| `explicit.stat_3336890334@T1` | -1.42231 |
| `explicit.stat_1263695895@T2` | -1.25628 |
| `explicit.stat_9187492@T1` | -0.97650 |
| `explicit.stat_210067635@T1` | -0.86168 |
| `explicit.stat_1263695895@T1` | -0.80989 |
| `explicit.stat_2694482655@T1` | 0.80459 |
| `explicit.stat_1037193709@T2` | -0.68948 |
| `explicit.stat_691932474@T2` | -0.66634 |
| `explicit.stat_3695891184@T2` | -0.66116 |

## Coverage (listings per base)

- … **Sapphire** — 39112 listings (39047 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 38039 listings (37987 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 29157 listings (29125 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 13188 listings (13170 priced) [0.2–398916549611043.2 ex]
- … **Prismatic Ring** — 12223 listings (12197 priced) [0.2–398916549611043.2 ex]
- … **Solar Amulet** — 11900 listings (11874 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 11759 listings (11744 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 11003 listings (10976 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10984 listings (10961 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 10412 listings (10399 priced) [0.3–398916549611043.2 ex]
- … **Sapphire Ring** — 9111 listings (9096 priced) [0.2–398916549611043.2 ex]
- … **Topaz Ring** — 8775 listings (8765 priced) [0.3–398916549611043.2 ex]
- … **Ruby Ring** — 8682 listings (8673 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7617 listings (7593 priced) [0.3–398916553600208.8 ex]
- … **Unset Ring** — 7520 listings (7498 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7490 listings (7482 priced) [0.3–398916549611043.2 ex]
- … **Jade Amulet** — 7425 listings (7409 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 7355 listings (7347 priced) [0.3–3985176410.3 ex]
- … **Pearl Ring** — 7292 listings (7283 priced) [0.2–398916549611043.2 ex]
- … **Plate Belt** — 7207 listings (7176 priced) [0.3–398916553600208.8 ex]
- … **Ancestral Tiara** — 7172 listings (7141 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 7118 listings (7106 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6801 listings (6797 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6722 listings (6707 priced) [0.3–398916549611043.2 ex]
- … **Heavy Belt** — 6383 listings (6369 priced) [0.3–398916553600208.8 ex]

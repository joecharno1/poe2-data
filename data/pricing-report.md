# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-22T09:52:50+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **734105** (731742 priced in exalted)
- Distinct bases: 1002 · distinct mods: 3330 · mod rows: 3469345
- Sold signals: **24062** sold · 417327 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-22T09:40:16+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×20.55** (median |log error| 3.023)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×74.42 · ±30% 6% · n=106685
- Premium segment (60ex+): skill **+0.11** · typical error ×294.18 · ±30% 0% · n=70825

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 15846 | ×36.78 | 21% | +0.04 | +0.07 |
| jewel | 15358 | ×56.15 | 22% | +0.02 | +0.04 |
| accessory.amulet | 14196 | ×10.00 | 17% | +0.01 | +0.00 |
| accessory.belt | 9958 | ×22.98 | 25% | +0.01 | +0.04 |
| armour.chest | 9751 | ×16.25 | 23% | +0.07 | +0.10 |
| armour.helmet | 9487 | ×25.93 | 18% | +0.08 | +0.10 |
| armour.boots | 8728 | ×23.45 | 20% | +0.10 | +0.12 |
| armour.gloves | 8626 | ×35.67 | 16% | +0.07 | +0.10 |
| other | 8522 | ×2.00 | 39% | +0.12 | +0.19 |
| weapon.wand | 5042 | ×42.06 | 15% | +0.11 | +0.12 |
| weapon.bow | 3943 | ×25.43 | 13% | +0.16 | +0.16 |
| weapon.crossbow | 3732 | ×25.34 | 15% | +0.11 | +0.14 |
| weapon.warstaff | 2599 | ×14.62 | 7% | +0.16 | +0.16 |
| weapon.staff | 2499 | ×16.17 | 6% | +0.13 | +0.12 |
| weapon.sceptre | 2432 | ×18.60 | 5% | +0.06 | +0.07 |
| weapon.spear | 1940 | ×13.25 | 7% | +0.11 | +0.13 |
| armour.focus | 1623 | ×12.95 | 7% | +0.09 | +0.11 |
| armour.quiver | 1513 | ×16.67 | 7% | +0.12 | +0.13 |
| flask.charm | 1252 | ×9.97 | 28% | +0.03 | +0.02 |
| armour.shield | 1247 | ×8.06 | 8% | +0.10 | +0.12 |
| weapon.twomace | 1152 | ×8.46 | 7% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=83963, R²=-1.9114

intercept: `-0.0624`  ·  log_price: True  ·  ilvl: `0.00076`  ·  n_mods: `1.02333`  ·  n_top_tier: `-0.95131`  ·  corrupted: `1.23186`  ·  quality: `-0.06543`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 3.19080 |
| `explicit.stat_1604736568@T1` | -2.25825 |
| `explicit.stat_1604736568` | 2.19768 |
| `explicit.stat_2194114101@T1` | -0.96907 |
| `explicit.stat_274716455@T1` | -0.77435 |
| `explicit.stat_3714003708@T1` | 0.75103 |
| `explicit.stat_681332047@T1` | -0.51727 |
| `explicit.stat_3473929743@T1` | -0.34496 |
| `explicit.stat_3556824919@T1` | -0.31897 |
| `pseudo.weapon_spell_power` | 0.25588 |
| `explicit.stat_2974417149` | -0.25250 |
| `explicit.stat_681332047` | 0.22329 |

### accessory.ring — n=72264, R²=-2.0093

intercept: `3.3020`  ·  log_price: True  ·  ilvl: `-0.04149`  ·  n_mods: `0.00128`  ·  n_top_tier: `1.00323`  ·  corrupted: `-0.00758`  ·  n_sockets: `2.19712`  ·  quality: `0.01812`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.05055 |
| `explicit.stat_1573130764@T2` | -1.03055 |
| `explicit.stat_2891184298@T2` | -1.02765 |
| `explicit.stat_1263695895@T2` | -1.02675 |
| `explicit.stat_2923486259@T2` | -1.02594 |
| `explicit.stat_4080418644@T1` | -1.02330 |
| `explicit.stat_1671376347@T2` | -1.02238 |
| `explicit.stat_3917489142@T2` | -1.02164 |
| `explicit.stat_2891184298@T1` | -1.02093 |
| `explicit.stat_4220027924@T2` | -1.01927 |
| `explicit.stat_3032590688@T1` | -1.01904 |
| `explicit.stat_3325883026@T1` | -1.01765 |

### other — n=69908, R²=-0.6587

intercept: `1.6093`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.15566`  ·  n_top_tier: `0.19091`  ·  corrupted: `0.00005`  ·  n_sockets: `-0.00005`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_718638445` | 0.46703 |
| `implicit.stat_3182714256` | 0.46702 |
| `explicit.stat_1050105434@T1` | -0.29858 |
| `implicit.stat_2219129443` | 0.21469 |
| `explicit.stat_3299347043@T1` | -0.18942 |
| `explicit.stat_2974417149@T1` | 0.17695 |
| `implicit.stat_958696139` | -0.15565 |
| `explicit.stat_3917489142@T1` | -0.13069 |
| `implicit.stat_1416292992` | -0.10378 |
| `implicit.stat_3032590688` | -0.06226 |
| `implicit.stat_3879011313` | 0.05376 |
| `explicit.stat_2901986750` | 0.04542 |

### accessory.amulet — n=64711, R²=-0.5001

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `1.05109`  ·  corrupted: `0.00001`  ·  n_sockets: `1.42364`  ·  quality: `0.03743`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | -1.42206 |
| `explicit.stat_124131830@T2` | -1.16358 |
| `explicit.stat_2162097452@T2` | -1.05122 |
| `explicit.stat_803737631@T1` | -1.05115 |
| `explicit.stat_803737631@T2` | -1.05114 |
| `explicit.stat_3299347043@T2` | -1.05113 |
| `explicit.stat_3299347043@T1` | -1.05113 |
| `explicit.stat_3372524247@T1` | -1.05112 |
| `explicit.stat_4080418644@T2` | -1.05112 |
| `explicit.stat_983749596@T1` | -1.05112 |
| `explicit.stat_2866361420@T1` | -1.05111 |
| `explicit.stat_2866361420@T2` | -1.05111 |

### accessory.belt — n=45795, R²=-2.1629

intercept: `0.0976`  ·  log_price: True  ·  ilvl: `-0.00118`  ·  n_mods: `-0.00053`  ·  n_top_tier: `0.82998`  ·  corrupted: `0.44315`  ·  n_sockets: `1.62557`

| stat_id | coef |
|---|---|
| `explicit.stat_2881298780@T1` | -0.83069 |
| `explicit.stat_3299347043@T2` | -0.83062 |
| `explicit.stat_915769802@T1` | -0.83061 |
| `explicit.stat_809229260@T2` | -0.83060 |
| `explicit.stat_51994685@T1` | -0.83059 |
| `explicit.stat_1570770415@T2` | -0.83041 |
| `explicit.stat_3325883026@T1` | -0.83030 |
| `explicit.stat_3372524247@T2` | -0.83029 |
| `explicit.stat_1570770415@T1` | -0.83018 |
| `explicit.stat_2881298780@T2` | -0.83013 |
| `explicit.stat_3299347043@T1` | -0.83012 |
| `explicit.stat_915769802@T2` | -0.83007 |

### armour.chest — n=45463, R²=-1.8393

intercept: `3.1242`  ·  log_price: True  ·  ilvl: `-0.03856`  ·  n_mods: `-0.01164`  ·  n_top_tier: `0.31877`  ·  corrupted: `0.21443`  ·  n_sockets: `0.01759`  ·  quality: `0.07764`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.07952 |
| `explicit.stat_986397080@T2` | -0.35763 |
| `explicit.stat_1692879867@T2` | -0.34773 |
| `explicit.stat_4080418644@T2` | -0.34508 |
| `explicit.stat_986397080@T1` | -0.34485 |
| `explicit.stat_915769802@T2` | -0.34279 |
| `explicit.stat_915769802@T1` | -0.33748 |
| `explicit.stat_1062208444@T2` | -0.33538 |
| `explicit.stat_4080418644@T1` | -0.33442 |
| `explicit.stat_2451402625@T2` | -0.33300 |
| `explicit.stat_1692879867@T1` | -0.33257 |
| `explicit.stat_2339757871@T2` | -0.33125 |

### armour.helmet — n=44250, R²=-1.7975

intercept: `3.2604`  ·  log_price: True  ·  ilvl: `-0.04075`  ·  n_mods: `-0.01956`  ·  n_top_tier: `0.54016`  ·  corrupted: `0.55499`  ·  n_sockets: `0.05432`  ·  quality: `0.07599`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.61767 |
| `crafted.stat_3917489142@T1` | 2.23520 |
| `explicit.stat_1263695895@T1` | -0.77765 |
| `explicit.stat_2162097452@T2` | -0.69562 |
| `explicit.stat_3917489142@T2` | -0.67976 |
| `explicit.stat_3917489142@T1` | -0.62085 |
| `explicit.stat_1263695895@T2` | -0.61702 |
| `explicit.stat_4052037485@T2` | -0.61645 |
| `explicit.stat_4015621042@T2` | -0.60876 |
| `explicit.stat_3321629045@T2` | -0.57697 |
| `explicit.stat_803737631@T1` | -0.57224 |
| `explicit.stat_1999113824@T1` | -0.57064 |

### armour.boots — n=40870, R²=-1.7654

intercept: `3.4333`  ·  log_price: True  ·  ilvl: `-0.04239`  ·  n_mods: `-0.02089`  ·  n_top_tier: `0.39559`  ·  corrupted: `0.02809`  ·  n_sockets: `0.04608`  ·  quality: `0.07499`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.05418 |
| `explicit.stat_2250533757@T1` | 1.78019 |
| `crafted.stat_3917489142@T1` | 1.44139 |
| `explicit.stat_2923486259@T1` | 0.69243 |
| `explicit.stat_3299347043@T1` | -0.51478 |
| `explicit.stat_2923486259@T2` | -0.47330 |
| `explicit.stat_2160282525@T1` | -0.44102 |
| `explicit.stat_3917489142@T2` | -0.44082 |
| `explicit.stat_1671376347@T2` | -0.43911 |
| `explicit.stat_328541901@T2` | -0.43629 |
| `explicit.stat_1874553720@T1` | -0.43000 |
| `explicit.stat_99927264@T1` | -0.42834 |

### armour.gloves — n=39868, R²=-1.8093

intercept: `3.8545`  ·  log_price: True  ·  ilvl: `-0.05010`  ·  n_mods: `-0.00518`  ·  n_top_tier: `0.68478`  ·  corrupted: `-0.04314`  ·  n_sockets: `0.13632`  ·  quality: `0.05943`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -0.99689 |
| `explicit.stat_4052037485@T1` | -0.90353 |
| `explicit.stat_3484657501@T2` | -0.88225 |
| `explicit.stat_2923486259@T2` | -0.85708 |
| `explicit.stat_9187492@T2` | -0.84785 |
| `explicit.stat_4052037485@T2` | -0.84490 |
| `explicit.stat_4015621042@T2` | -0.83234 |
| `explicit.stat_3484657501@T1` | -0.81599 |
| `explicit.stat_3321629045@T2` | -0.81057 |
| `explicit.stat_3917489142@T2` | -0.76326 |
| `explicit.stat_328541901@T2` | -0.75998 |
| `explicit.stat_124859000@T1` | -0.75807 |

### weapon.wand — n=23408, R²=-1.9946

intercept: `4.0785`  ·  log_price: True  ·  ilvl: `-0.05051`  ·  n_mods: `-0.05796`  ·  n_top_tier: `0.55673`  ·  corrupted: `-0.00003`  ·  n_sockets: `0.01287`  ·  quality: `0.04108`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.23565 |
| `explicit.stat_1545858329@T1` | 2.96781 |
| `explicit.stat_2254480358@T1` | 2.54043 |
| `explicit.stat_124131830@T1` | 2.28216 |
| `explicit.stat_591105508@T1` | 2.23034 |
| `explicit.stat_4226189338@T1` | 2.02371 |
| `explicit.stat_1600707273@T1` | 1.30611 |
| `crafted.stat_124131830` | 1.25129 |
| `explicit.stat_2254480358@T2` | 1.17659 |
| `explicit.stat_1263695895@T2` | -0.96805 |
| `explicit.stat_1263695895@T1` | -0.95407 |
| `explicit.stat_4226189338@T2` | 0.80140 |

### flask.charm — n=20556, R²=-0.6623

intercept: `0.1053`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.60888`  ·  corrupted: `1.51501`  ·  quality: `0.01784`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60509 |
| `explicit.stat_1056492907` | 2.54600 |
| `explicit.stat_3246948616` | 2.30246 |
| `explicit.stat_828533480@T2` | -1.60891 |
| `explicit.stat_1120862500@T2` | -1.60891 |
| `explicit.stat_1873752457@T2` | -1.60889 |
| `explicit.stat_2541588185@T2` | -1.60888 |
| `explicit.stat_388617051@T2` | -1.60887 |
| `explicit.stat_2365392475@T2` | -1.60880 |
| `explicit.stat_3196823591@T2` | -1.60840 |
| `explicit.stat_2676834156@T2` | -1.60731 |
| `explicit.stat_828533480@T1` | -1.60369 |

### weapon.bow — n=18722, R²=-1.7976

intercept: `4.1250`  ·  log_price: True  ·  ilvl: `-0.04889`  ·  n_mods: `-0.09537`  ·  n_top_tier: `0.79491`  ·  corrupted: `0.69672`  ·  n_sockets: `0.04448`  ·  quality: `0.03196`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 5.03332 |
| `desecrated.stat_210067635@T1` | -1.88304 |
| `explicit.stat_1263695895@T1` | -1.46398 |
| `crafted.stat_210067635@T2` | -1.37724 |
| `explicit.stat_1263695895@T2` | -1.31771 |
| `crafted.stat_3035140377` | 1.14561 |
| `explicit.stat_1509134228@T1` | -1.02736 |
| `explicit.stat_210067635@T2` | -0.96373 |
| `explicit.stat_1368271171@T2` | -0.90591 |
| `explicit.stat_1368271171@T1` | -0.90265 |
| `explicit.stat_3695891184@T1` | -0.88058 |
| `explicit.stat_2463230181@T2` | -0.84752 |

### weapon.crossbow — n=17539, R²=-1.7814

intercept: `4.3780`  ·  log_price: True  ·  ilvl: `-0.05306`  ·  n_mods: `-0.06583`  ·  n_top_tier: `0.44396`  ·  corrupted: `-0.12503`  ·  n_sockets: `0.04920`  ·  quality: `0.02019`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.94789 |
| `explicit.stat_2250681686@T2` | -1.90831 |
| `explicit.stat_2250681686` | 1.55579 |
| `explicit.stat_1202301673@T1` | 1.47362 |
| `explicit.stat_1980802737` | 1.39872 |
| `explicit.stat_1509134228@T1` | 0.96018 |
| `crafted.stat_3035140377` | 0.89544 |
| `explicit.stat_709508406@T1` | 0.74122 |
| `explicit.stat_3695891184@T1` | -0.65054 |
| `explicit.stat_3336890334@T2` | -0.64217 |
| `explicit.stat_3695891184@T2` | -0.58452 |
| `explicit.stat_691932474@T1` | -0.56899 |

### weapon.warstaff — n=12354, R²=-0.3239

intercept: `-11.1184`  ·  log_price: True  ·  ilvl: `0.15135`  ·  n_mods: `-0.23339`  ·  n_top_tier: `0.49764`  ·  corrupted: `0.29526`  ·  n_sockets: `0.10453`  ·  quality: `0.05292`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 0.96058 |
| `desecrated.stat_2231156303@T1` | 0.96058 |
| `crafted.stat_210067635@T2` | 0.95903 |
| `explicit.stat_821021828@T2` | -0.88678 |
| `explicit.stat_210067635@T1` | -0.86929 |
| `explicit.stat_1037193709@T2` | -0.85198 |
| `explicit.stat_328541901@T2` | -0.81878 |
| `desecrated.stat_9187492` | 0.78855 |
| `rune.stat_243313994` | 0.72994 |
| `explicit.stat_328541901@T1` | -0.71843 |
| `explicit.stat_1940865751@T2` | -0.70802 |
| `explicit.stat_210067635@T2` | -0.61547 |

### weapon.staff — n=11779, R²=-0.3532

intercept: `-15.8958`  ·  log_price: True  ·  ilvl: `0.20411`  ·  n_mods: `-0.11630`  ·  n_top_tier: `0.47702`  ·  corrupted: `0.87200`  ·  n_sockets: `0.19111`  ·  quality: `0.03965`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 1.98304 |
| `explicit.stat_124131830@T1` | 1.95994 |
| `explicit.stat_4226189338@T1` | 1.62325 |
| `explicit.stat_1600707273@T1` | 1.52176 |
| `explicit.stat_1545858329@T1` | 1.05781 |
| `explicit.stat_3962278098@T2` | 0.92585 |
| `explicit.stat_473429811@T2` | -0.86968 |
| `explicit.stat_591105508@T2` | 0.81019 |
| `explicit.stat_293638271@T2` | -0.78683 |
| `rune.stat_124131830` | 0.70343 |
| `explicit.stat_124131830@T2` | 0.69918 |
| `explicit.stat_4226189338@T2` | 0.62121 |

### weapon.sceptre — n=11448, R²=-0.3301

intercept: `-21.2767`  ·  log_price: True  ·  ilvl: `0.27131`  ·  n_mods: `-0.02366`  ·  n_top_tier: `0.19988`  ·  corrupted: `0.21242`  ·  n_sockets: `0.21245`  ·  quality: `0.03525`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.62842 |
| `explicit.stat_2162097452@T2` | 1.31832 |
| `explicit.stat_3057012405@T1` | 1.08882 |
| `explicit.stat_1263695895@T1` | -0.98180 |
| `explicit.stat_1798257884@T2` | 0.90006 |
| `explicit.stat_1263695895@T2` | -0.84784 |
| `explicit.stat_101878827@T2` | 0.75286 |
| `explicit.stat_101878827@T1` | 0.73249 |
| `explicit.stat_4080418644@T2` | -0.65377 |
| `explicit.stat_2854751904@T2` | -0.63791 |
| `explicit.stat_2347036682@T2` | -0.39777 |
| `explicit.stat_789117908@T2` | -0.37354 |

### weapon.spear — n=9320, R²=-0.3757

intercept: `-13.6391`  ·  log_price: True  ·  ilvl: `0.18826`  ·  n_mods: `-0.18446`  ·  n_top_tier: `0.57151`  ·  corrupted: `-0.52677`  ·  n_sockets: `0.21988`  ·  quality: `0.07282`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.19632 |
| `desecrated.stat_666077204@T1` | -3.10197 |
| `explicit.stat_1037193709@T1` | -1.11498 |
| `crafted.stat_3035140377` | 0.98633 |
| `explicit.stat_9187492@T2` | -0.95293 |
| `explicit.stat_748522257@T2` | -0.94035 |
| `explicit.stat_1940865751@T2` | -0.91034 |
| `explicit.stat_4080418644@T2` | -0.90012 |
| `explicit.stat_3336890334@T2` | -0.87818 |
| `explicit.stat_4080418644@T1` | -0.85787 |
| `explicit.stat_9187492@T1` | 0.84568 |
| `explicit.stat_3261801346@T1` | -0.80676 |

### armour.focus — n=7612, R²=-0.3332

intercept: `-16.2031`  ·  log_price: True  ·  ilvl: `0.20681`  ·  n_mods: `-0.15750`  ·  n_top_tier: `0.96924`  ·  corrupted: `-0.22268`  ·  n_sockets: `0.39657`  ·  quality: `0.03366`

| stat_id | coef |
|---|---|
| `explicit.stat_4220027924@T1` | -1.62859 |
| `explicit.stat_2923486259@T1` | -1.53206 |
| `explicit.stat_2923486259@T2` | -1.32734 |
| `explicit.stat_2339757871@T2` | -1.22429 |
| `explicit.stat_2768835289@T1` | -1.19752 |
| `explicit.stat_4220027924@T2` | -1.18093 |
| `explicit.stat_3962278098@T2` | -1.17684 |
| `explicit.stat_2231156303@T1` | -1.15233 |
| `explicit.stat_1050105434@T2` | -1.10438 |
| `crafted.stat_737908626@T2` | 1.07745 |
| `explicit.stat_4015621042@T1` | -1.06297 |
| `explicit.stat_274716455@T2` | -1.04730 |

### armour.quiver — n=7088, R²=-0.2751

intercept: `-18.3639`  ·  log_price: True  ·  ilvl: `0.22136`  ·  n_mods: `-0.08050`  ·  n_top_tier: `0.67075`  ·  corrupted: `0.96865`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.17808 |
| `explicit.stat_681332047@T2` | -1.33176 |
| `explicit.stat_681332047@T1` | -1.05967 |
| `explicit.stat_1573130764@T2` | -0.94990 |
| `explicit.stat_1573130764@T1` | -0.85551 |
| `explicit.stat_2194114101@T2` | -0.82064 |
| `explicit.stat_2321178454@T2` | -0.81005 |
| `explicit.stat_4067062424@T1` | -0.66347 |
| `explicit.stat_3714003708@T2` | -0.61891 |
| `explicit.stat_803737631@T1` | -0.57610 |
| `explicit.stat_4067062424@T2` | -0.54207 |
| `explicit.stat_803737631@T2` | -0.53773 |

### armour.shield — n=6099, R²=-0.4096

intercept: `-13.5632`  ·  log_price: True  ·  ilvl: `0.18323`  ·  n_mods: `-0.18811`  ·  n_top_tier: `0.59142`  ·  corrupted: `-0.50695`  ·  n_sockets: `0.35328`  ·  quality: `0.04587`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.57010 |
| `explicit.stat_3033371881@T2` | -1.20903 |
| `explicit.stat_1011760251@T1` | -1.20835 |
| `explicit.stat_328541901@T1` | -1.14616 |
| `explicit.stat_2901986750@T1` | -1.10761 |
| `explicit.stat_2481353198@T1` | -1.10062 |
| `explicit.stat_2339757871@T1` | -1.01511 |
| `explicit.stat_4095671657@T2` | -1.00742 |
| `explicit.stat_3321629045@T2` | -0.96302 |
| `explicit.stat_2923486259@T1` | -0.95633 |
| `explicit.stat_2481353198@T2` | -0.94650 |
| `explicit.stat_2339757871@T2` | -0.92674 |

### weapon.twomace — n=5573, R²=-0.4229

intercept: `-10.6808`  ·  log_price: True  ·  ilvl: `0.14889`  ·  n_mods: `-0.24808`  ·  n_top_tier: `0.47805`  ·  corrupted: `0.52195`  ·  n_sockets: `0.19739`  ·  quality: `0.05849`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.77756 |
| `explicit.stat_1037193709@T1` | -1.49343 |
| `explicit.stat_3336890334@T1` | -1.43573 |
| `explicit.stat_1263695895@T2` | -1.24326 |
| `explicit.stat_9187492@T1` | -1.08251 |
| `explicit.stat_2694482655@T1` | 0.90140 |
| `explicit.stat_1263695895@T1` | -0.72127 |
| `explicit.stat_3695891184@T2` | -0.69628 |
| `explicit.stat_3695891184@T1` | -0.68314 |
| `explicit.stat_518292764@T2` | -0.66596 |
| `explicit.stat_210067635@T1` | -0.65515 |
| `explicit.stat_1037193709@T2` | -0.53451 |

## Coverage (listings per base)

- … **Sapphire** — 38551 listings (38486 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 37533 listings (37481 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 28756 listings (28724 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 13093 listings (13075 priced) [0.2–398916549611043.2 ex]
- … **Prismatic Ring** — 12077 listings (12051 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 11765 listings (11739 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 11636 listings (11623 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10891 listings (10864 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10851 listings (10828 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 10316 listings (10303 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 9008 listings (8993 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8670 listings (8660 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8578 listings (8569 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7568 listings (7544 priced) [0.3–398916553600208.8 ex]
- … **Unset Ring** — 7448 listings (7426 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7417 listings (7409 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 7354 listings (7339 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 7261 listings (7253 priced) [0.3–3985176410.3 ex]
- … **Pearl Ring** — 7203 listings (7194 priced) [0.2–275252424.7 ex]
- … **Plate Belt** — 7142 listings (7111 priced) [0.3–398916553600208.8 ex]
- … **Ancestral Tiara** — 7103 listings (7074 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 7042 listings (7030 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6749 listings (6745 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6644 listings (6629 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6333 listings (6319 priced) [0.3–398916553600208.8 ex]

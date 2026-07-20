# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-20T23:20:48+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **695034** (692868 priced in exalted)
- Distinct bases: 999 · distinct mods: 3313 · mod rows: 3289492
- Sold signals: **24305** sold · 395733 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-20T23:07:01+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×19.39** (median |log error| 2.9645)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.16** · typical error ×54.89 · ±30% 5% · n=100746
- Premium segment (60ex+): skill **+0.15** · typical error ×286.15 · ±30% 0% · n=67396

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 14793 | ×52.89 | 21% | +0.04 | +0.06 |
| jewel | 14106 | ×10.00 | 4% | +0.11 | +0.13 |
| accessory.amulet | 13312 | ×35.87 | 18% | +0.04 | +0.05 |
| accessory.belt | 9553 | ×20.08 | 15% | +0.06 | +0.08 |
| armour.chest | 9245 | ×14.52 | 23% | +0.08 | +0.10 |
| armour.helmet | 9028 | ×23.45 | 18% | +0.08 | +0.11 |
| armour.boots | 8376 | ×24.07 | 19% | +0.10 | +0.13 |
| armour.gloves | 8157 | ×29.13 | 12% | +0.09 | +0.11 |
| other | 8034 | ×1.94 | 43% | +0.11 | +0.17 |
| weapon.wand | 4854 | ×35.13 | 14% | +0.11 | +0.12 |
| weapon.bow | 3838 | ×26.42 | 10% | +0.17 | +0.16 |
| weapon.crossbow | 3595 | ×26.42 | 17% | +0.11 | +0.14 |
| weapon.warstaff | 2481 | ×14.32 | 7% | +0.22 | +0.22 |
| weapon.staff | 2354 | ×15.97 | 6% | +0.14 | +0.13 |
| weapon.sceptre | 2342 | ×20.42 | 4% | +0.09 | +0.10 |
| weapon.spear | 1848 | ×13.51 | 7% | +0.15 | +0.15 |
| armour.focus | 1542 | ×13.04 | 7% | +0.12 | +0.12 |
| armour.quiver | 1450 | ×18.69 | 7% | +0.12 | +0.13 |
| flask.charm | 1195 | ×10.00 | 28% | -0.02 | +0.00 |
| armour.shield | 1190 | ×9.69 | 8% | +0.10 | +0.11 |
| weapon.twomace | 1106 | ×8.80 | 8% | +0.10 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=77477, R²=-0.9834

intercept: `-1.8925`  ·  log_price: True  ·  ilvl: `0.02377`  ·  n_mods: `0.84779`  ·  n_top_tier: `-0.27446`  ·  corrupted: `0.42323`  ·  quality: `-0.00647`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.20228 |
| `explicit.stat_3485067555@T1` | 2.23413 |
| `explicit.stat_1869147066@T1` | -1.93784 |
| `explicit.stat_1594812856@T1` | 1.71491 |
| `explicit.stat_1569101201@T1` | -1.63142 |
| `explicit.stat_3668351662@T1` | -1.52840 |
| `explicit.stat_3174700878@T1` | 1.49627 |
| `explicit.stat_3780644166@T1` | -1.43184 |
| `explicit.stat_4147897060@T1` | -1.29136 |
| `explicit.stat_239367161@T1` | -1.21352 |
| `explicit.stat_234296660@T1` | -1.18160 |
| `explicit.stat_1852872083@T1` | -1.16796 |

### accessory.ring — n=67489, R²=-2.0213

intercept: `3.3991`  ·  log_price: True  ·  ilvl: `-0.04238`  ·  n_mods: `0.00044`  ·  n_top_tier: `0.97521`  ·  corrupted: `0.00903`  ·  n_sockets: `2.10767`  ·  quality: `0.01851`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.00639 |
| `explicit.stat_803737631@T1` | -0.99803 |
| `explicit.stat_2231156303@T1` | -0.99335 |
| `explicit.stat_4080418644@T1` | -0.99252 |
| `explicit.stat_3325883026@T1` | -0.99193 |
| `explicit.stat_2891184298@T2` | -0.98764 |
| `explicit.stat_4220027924@T2` | -0.98732 |
| `explicit.stat_2923486259@T2` | -0.98712 |
| `explicit.stat_2891184298@T1` | -0.98409 |
| `explicit.stat_1573130764@T2` | -0.98374 |
| `explicit.stat_3291658075@T2` | -0.98328 |
| `explicit.stat_3325883026@T2` | -0.98246 |

### other — n=66120, R²=-0.668

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.02422`  ·  n_top_tier: `0.32236`  ·  corrupted: `0.07325`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.38315 |
| `explicit.stat_3299347043@T1` | -0.23532 |
| `explicit.stat_3917489142@T1` | -0.22949 |
| `implicit.stat_2219129443` | 0.22783 |
| `explicit.stat_2974417149@T1` | 0.10978 |
| `explicit.stat_789117908@T1` | -0.07679 |
| `implicit.stat_3879011313` | 0.07514 |
| `implicit.stat_3182714256` | 0.07268 |
| `implicit.stat_718638445` | 0.07267 |
| `explicit.stat_736967255@T1` | -0.05550 |
| `explicit.stat_2106365538@T1` | -0.05011 |
| `pseudo.total_ele_res>=40` | -0.04148 |

### accessory.amulet — n=60704, R²=-2.1427

intercept: `3.4386`  ·  log_price: True  ·  ilvl: `-0.04330`  ·  n_mods: `-0.02135`  ·  n_top_tier: `1.29111`  ·  corrupted: `0.11341`  ·  n_sockets: `-0.07537`  ·  quality: `0.05146`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.71255 |
| `explicit.stat_3299347043@T2` | -1.69232 |
| `explicit.stat_803737631@T1` | -1.43073 |
| `explicit.stat_587431675@T2` | -1.43035 |
| `explicit.stat_2866361420@T2` | -1.39798 |
| `explicit.stat_2974417149@T1` | -1.39719 |
| `explicit.stat_2866361420@T1` | -1.37907 |
| `explicit.stat_2974417149@T2` | -1.37174 |
| `explicit.stat_803737631@T2` | -1.36102 |
| `explicit.stat_1050105434@T2` | -1.34947 |
| `explicit.stat_4080418644@T1` | -1.33208 |
| `explicit.stat_2901986750@T1` | -1.33092 |

### accessory.belt — n=43750, R²=-1.5881

intercept: `4.7585`  ·  log_price: True  ·  ilvl: `-0.05623`  ·  n_mods: `-0.03991`  ·  n_top_tier: `0.33475`  ·  corrupted: `1.23976`  ·  n_sockets: `1.11797`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.35117 |
| `explicit.stat_2923486259@T2` | 0.89627 |
| `explicit.stat_4220027924@T1` | 0.60119 |
| `explicit.stat_3299347043@T1` | -0.53192 |
| `explicit.stat_3299347043@T2` | -0.43801 |
| `explicit.stat_2881298780@T1` | -0.40539 |
| `explicit.stat_51994685@T1` | -0.37959 |
| `explicit.stat_809229260@T2` | -0.35607 |
| `explicit.stat_1570770415@T2` | -0.35163 |
| `explicit.stat_3372524247@T2` | -0.35045 |
| `explicit.stat_3325883026@T1` | -0.34448 |
| `explicit.stat_4220027924@T2` | -0.34168 |

### armour.chest — n=43400, R²=-1.7902

intercept: `3.1808`  ·  log_price: True  ·  ilvl: `-0.03941`  ·  n_mods: `-0.01088`  ·  n_top_tier: `0.41498`  ·  corrupted: `0.32940`  ·  n_sockets: `0.01785`  ·  quality: `0.06955`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.67806 |
| `explicit.stat_986397080@T2` | -0.49847 |
| `explicit.stat_986397080@T1` | -0.48999 |
| `explicit.stat_4080418644@T2` | -0.44665 |
| `explicit.stat_4080418644@T1` | -0.44651 |
| `explicit.stat_915769802@T2` | -0.44565 |
| `explicit.stat_1692879867@T2` | -0.44317 |
| `explicit.stat_3484657501@T1` | -0.44120 |
| `explicit.stat_915769802@T1` | -0.43557 |
| `explicit.stat_3301100256@T2` | -0.42691 |
| `explicit.stat_3372524247@T2` | -0.42564 |
| `explicit.stat_2339757871@T2` | -0.42375 |

### armour.helmet — n=42200, R²=-1.7278

intercept: `3.2534`  ·  log_price: True  ·  ilvl: `-0.04120`  ·  n_mods: `-0.01957`  ·  n_top_tier: `0.62518`  ·  corrupted: `0.66051`  ·  n_sockets: `0.05420`  ·  quality: `0.06604`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.05040 |
| `explicit.stat_1263695895@T1` | -0.94123 |
| `explicit.stat_3917489142@T2` | -0.85127 |
| `explicit.stat_1263695895@T2` | -0.77410 |
| `explicit.stat_3917489142@T1` | -0.76825 |
| `explicit.stat_2162097452@T2` | -0.75427 |
| `explicit.stat_4052037485@T2` | -0.69974 |
| `explicit.stat_53045048@T1` | -0.68820 |
| `explicit.stat_803737631@T1` | -0.68402 |
| `explicit.stat_4015621042@T2` | -0.67320 |
| `explicit.stat_1999113824@T1` | -0.67250 |
| `explicit.stat_803737631@T2` | -0.66769 |

### armour.boots — n=39122, R²=-1.6764

intercept: `3.6694`  ·  log_price: True  ·  ilvl: `-0.04530`  ·  n_mods: `-0.02236`  ·  n_top_tier: `0.47009`  ·  corrupted: `0.14055`  ·  n_sockets: `0.06577`  ·  quality: `0.06598`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.74169 |
| `crafted.stat_3917489142@T1` | 1.52631 |
| `explicit.stat_2339757871@T1` | -1.48910 |
| `explicit.stat_2923486259@T1` | 0.79669 |
| `explicit.stat_3917489142@T2` | -0.62174 |
| `explicit.stat_3299347043@T1` | -0.58721 |
| `explicit.stat_2923486259@T2` | -0.54746 |
| `explicit.stat_1999113824@T2` | -0.53650 |
| `explicit.stat_328541901@T2` | -0.53626 |
| `explicit.stat_1874553720@T1` | -0.52514 |
| `explicit.stat_2160282525@T1` | -0.52004 |
| `explicit.stat_1671376347@T2` | -0.51893 |

### armour.gloves — n=38114, R²=-1.5722

intercept: `3.6791`  ·  log_price: True  ·  ilvl: `-0.04898`  ·  n_mods: `-0.00008`  ·  n_top_tier: `0.70778`  ·  corrupted: `-0.01542`  ·  n_sockets: `0.20585`  ·  quality: `0.05442`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.95243 |
| `explicit.stat_2923486259@T1` | -1.13097 |
| `explicit.stat_2923486259@T2` | -1.07764 |
| `explicit.stat_3321629045@T2` | -1.03298 |
| `explicit.stat_3484657501@T2` | -1.01552 |
| `explicit.stat_4052037485@T1` | -0.96089 |
| `explicit.stat_3484657501@T1` | -0.93392 |
| `explicit.stat_4015621042@T2` | -0.92944 |
| `explicit.stat_4052037485@T2` | -0.91044 |
| `explicit.stat_9187492@T2` | -0.90809 |
| `explicit.stat_124859000@T1` | -0.85995 |
| `explicit.stat_803737631@T2` | -0.85542 |

### weapon.wand — n=22668, R²=-1.9065

intercept: `3.8364`  ·  log_price: True  ·  ilvl: `-0.04736`  ·  n_mods: `-0.06933`  ·  n_top_tier: `0.40262`  ·  corrupted: `0.04435`  ·  n_sockets: `0.05677`  ·  quality: `0.03879`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -3.79443 |
| `explicit.stat_1545858329@T1` | 2.75414 |
| `explicit.stat_2254480358@T1` | 2.45905 |
| `explicit.stat_124131830@T1` | 2.08499 |
| `explicit.stat_591105508@T1` | 1.99070 |
| `explicit.stat_736967255@T2` | 1.65763 |
| `explicit.stat_4226189338@T1` | 1.57498 |
| `explicit.stat_2254480358@T2` | 1.24276 |
| `crafted.stat_124131830` | 1.15088 |
| `explicit.stat_4226189338@T2` | 0.88246 |
| `explicit.stat_1263695895@T2` | -0.76840 |
| `explicit.stat_1263695895@T1` | -0.70250 |

### flask.charm — n=19426, R²=-0.6564

intercept: `0.1021`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.60912`  ·  corrupted: `1.40251`  ·  quality: `0.00414`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.78724 |
| `explicit.stat_1056492907` | 2.70570 |
| `explicit.stat_3246948616` | 1.60938 |
| `explicit.stat_1120862500@T2` | -1.60915 |
| `explicit.stat_828533480@T2` | -1.60915 |
| `explicit.stat_1873752457@T2` | -1.60912 |
| `explicit.stat_3196823591@T2` | -1.60907 |
| `explicit.stat_2676834156@T2` | -1.60906 |
| `explicit.stat_2365392475@T2` | -1.60905 |
| `explicit.stat_388617051@T2` | -1.60837 |
| `explicit.stat_2541588185@T2` | -1.60431 |
| `explicit.stat_1873752457@T1` | -1.60409 |

### weapon.bow — n=18086, R²=-1.7139

intercept: `4.0608`  ·  log_price: True  ·  ilvl: `-0.04862`  ·  n_mods: `-0.08772`  ·  n_top_tier: `0.73671`  ·  corrupted: `0.81966`  ·  n_sockets: `0.05795`  ·  quality: `0.02717`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 3.11931 |
| `desecrated.stat_210067635@T1` | -1.89333 |
| `explicit.stat_1263695895@T1` | -1.30513 |
| `crafted.stat_3035140377` | 1.17917 |
| `explicit.stat_1263695895@T2` | -1.17635 |
| `explicit.stat_3336890334@T1` | 1.17210 |
| `explicit.stat_709508406@T1` | 1.12199 |
| `explicit.stat_2463230181@T2` | -0.93950 |
| `explicit.stat_3695891184@T2` | -0.84807 |
| `explicit.stat_210067635@T2` | -0.84043 |
| `explicit.stat_1368271171@T2` | -0.83481 |
| `explicit.stat_3695891184@T1` | -0.79965 |

### weapon.crossbow — n=16975, R²=-1.8096

intercept: `4.0836`  ·  log_price: True  ·  ilvl: `-0.05001`  ·  n_mods: `-0.05556`  ·  n_top_tier: `0.37339`  ·  corrupted: `0.04591`  ·  n_sockets: `0.04718`  ·  quality: `0.02993`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.70316 |
| `explicit.stat_2250681686@T2` | -1.53285 |
| `explicit.stat_1202301673@T1` | 1.49213 |
| `explicit.stat_1980802737` | 1.35360 |
| `explicit.stat_2250681686` | 1.22329 |
| `explicit.stat_1509134228@T1` | 1.01610 |
| `crafted.stat_3035140377` | 0.89147 |
| `explicit.stat_1263695895@T2` | -0.62522 |
| `explicit.stat_3336890334@T2` | -0.54590 |
| `explicit.stat_387439868@T1` | 0.54322 |
| `explicit.stat_3695891184@T1` | -0.49820 |
| `explicit.stat_691932474@T1` | -0.46601 |

### weapon.warstaff — n=11789, R²=-0.3444

intercept: `-10.3231`  ·  log_price: True  ·  ilvl: `0.13871`  ·  n_mods: `-0.21101`  ·  n_top_tier: `0.37944`  ·  corrupted: `0.24571`  ·  n_sockets: `0.10525`  ·  quality: `0.05871`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.17975 |
| `desecrated.stat_2231156303@T1` | 1.09366 |
| `desecrated.stat_2527686725@T1` | 1.09366 |
| `explicit.stat_328541901@T2` | -0.97961 |
| `rune.stat_243313994` | 0.92200 |
| `desecrated.stat_9187492` | 0.80732 |
| `explicit.stat_328541901@T1` | -0.78327 |
| `explicit.stat_1037193709@T1` | 0.73256 |
| `explicit.stat_2694482655@T1` | 0.63752 |
| `explicit.stat_691932474@T2` | -0.57144 |
| `explicit.stat_1368271171@T1` | -0.55095 |
| `explicit.stat_821021828@T2` | -0.55035 |

### weapon.staff — n=11191, R²=-0.3606

intercept: `-15.7420`  ·  log_price: True  ·  ilvl: `0.20182`  ·  n_mods: `-0.09362`  ·  n_top_tier: `0.53730`  ·  corrupted: `0.72943`  ·  n_sockets: `0.17263`  ·  quality: `0.03346`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.06204 |
| `explicit.stat_591105508@T1` | 1.41115 |
| `explicit.stat_124131830@T1` | 1.34497 |
| `explicit.stat_1600707273@T1` | 1.33374 |
| `explicit.stat_1545858329@T1` | 1.30634 |
| `explicit.stat_293638271@T2` | -1.13788 |
| `rune.stat_124131830` | 1.03914 |
| `explicit.stat_2254480358@T1` | 0.96852 |
| `explicit.stat_1263695895@T2` | -0.87352 |
| `explicit.stat_3962278098@T2` | 0.69968 |
| `explicit.stat_473429811@T2` | -0.66725 |
| `crafted.stat_124131830` | 0.59259 |

### weapon.sceptre — n=10979, R²=-0.3401

intercept: `-21.3828`  ·  log_price: True  ·  ilvl: `0.27066`  ·  n_mods: `0.02357`  ·  n_top_tier: `0.16372`  ·  corrupted: `0.15074`  ·  n_sockets: `0.23559`  ·  quality: `0.02765`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.62443 |
| `explicit.stat_2162097452@T2` | 1.37801 |
| `explicit.stat_3057012405@T1` | 1.16309 |
| `explicit.stat_1263695895@T2` | -1.09469 |
| `explicit.stat_101878827@T2` | 0.90383 |
| `explicit.stat_1263695895@T1` | -0.89321 |
| `explicit.stat_1798257884@T2` | 0.85432 |
| `explicit.stat_2854751904@T2` | -0.82548 |
| `explicit.stat_849987426@T1` | 0.80800 |
| `explicit.stat_101878827@T1` | 0.79970 |
| `explicit.stat_1998951374@T1` | 0.52876 |
| `explicit.stat_4080418644@T2` | -0.51959 |

### weapon.spear — n=8898, R²=-0.3878

intercept: `-13.1522`  ·  log_price: True  ·  ilvl: `0.17946`  ·  n_mods: `-0.13296`  ·  n_top_tier: `0.60879`  ·  corrupted: `-0.53257`  ·  n_sockets: `0.17674`  ·  quality: `0.07497`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -3.90657 |
| `crafted.stat_210067635@T2` | -3.07633 |
| `explicit.stat_1202301673@T1` | 1.15943 |
| `explicit.stat_1940865751@T2` | -1.01899 |
| `crafted.stat_3035140377` | 0.97393 |
| `explicit.stat_9187492@T1` | 0.95112 |
| `desecrated.stat_210067635@T1` | -0.91718 |
| `explicit.stat_4080418644@T2` | -0.84047 |
| `explicit.stat_3336890334@T2` | -0.82834 |
| `explicit.stat_3261801346@T1` | -0.79036 |
| `explicit.stat_748522257@T2` | -0.74073 |
| `explicit.stat_691932474@T2` | -0.73026 |

### armour.focus — n=7273, R²=-0.3322

intercept: `-16.1446`  ·  log_price: True  ·  ilvl: `0.20414`  ·  n_mods: `-0.10455`  ·  n_top_tier: `0.90646`  ·  corrupted: `0.01750`  ·  n_sockets: `0.33679`  ·  quality: `0.02959`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 1.69337 |
| `explicit.stat_2923486259@T1` | -1.59725 |
| `explicit.stat_4220027924@T1` | -1.39288 |
| `explicit.stat_2923486259@T2` | -1.11365 |
| `explicit.stat_4220027924@T2` | -1.11251 |
| `explicit.stat_4015621042@T1` | -1.09197 |
| `crafted.stat_737908626@T2` | 1.08716 |
| `explicit.stat_2768835289@T1` | -1.06960 |
| `explicit.stat_3291658075@T1` | -1.01159 |
| `explicit.stat_2231156303@T2` | -1.00914 |
| `explicit.stat_2231156303@T1` | -1.00807 |
| `explicit.stat_737908626@T2` | -0.96259 |

### armour.quiver — n=6769, R²=-0.292

intercept: `-17.0031`  ·  log_price: True  ·  ilvl: `0.20257`  ·  n_mods: `-0.06165`  ·  n_top_tier: `0.76265`  ·  corrupted: `1.03068`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.11490 |
| `explicit.stat_681332047@T2` | -1.65200 |
| `explicit.stat_681332047@T1` | -1.43065 |
| `explicit.stat_2463230181@T1` | 1.32542 |
| `explicit.stat_1573130764@T2` | -1.10162 |
| `explicit.stat_1573130764@T1` | -0.92335 |
| `explicit.stat_2194114101@T2` | -0.76755 |
| `explicit.stat_803737631@T1` | -0.76420 |
| `explicit.stat_4067062424@T1` | -0.74008 |
| `explicit.stat_803737631@T2` | -0.68180 |
| `explicit.stat_2321178454@T2` | -0.67734 |
| `explicit.stat_3261801346@T1` | -0.59239 |

### armour.shield — n=5835, R²=-0.4388

intercept: `-12.7403`  ·  log_price: True  ·  ilvl: `0.16858`  ·  n_mods: `-0.09252`  ·  n_top_tier: `0.56122`  ·  corrupted: `-0.35929`  ·  n_sockets: `0.42081`  ·  quality: `0.05512`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.20269 |
| `explicit.stat_4095671657@T1` | -1.10956 |
| `explicit.stat_2339757871@T1` | -1.09535 |
| `explicit.stat_4095671657@T2` | -1.08287 |
| `explicit.stat_3321629045@T2` | -0.98054 |
| `explicit.stat_2901986750@T1` | -0.86684 |
| `explicit.stat_328541901@T1` | -0.85526 |
| `explicit.stat_2481353198@T2` | -0.84056 |
| `explicit.stat_3676141501@T1` | 0.80934 |
| `explicit.stat_2481353198@T1` | -0.80932 |
| `explicit.stat_3484657501@T1` | -0.78586 |
| `explicit.stat_4220027924@T1` | -0.76127 |

### weapon.twomace — n=5337, R²=-0.4551

intercept: `-10.2778`  ·  log_price: True  ·  ilvl: `0.13816`  ·  n_mods: `-0.20018`  ·  n_top_tier: `0.39846`  ·  corrupted: `0.53697`  ·  n_sockets: `0.11742`  ·  quality: `0.06546`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.40844 |
| `explicit.stat_1037193709@T1` | -1.55110 |
| `explicit.stat_3336890334@T1` | -1.26704 |
| `explicit.stat_2694482655@T1` | 1.14265 |
| `explicit.stat_1263695895@T2` | -1.08731 |
| `explicit.stat_9187492@T1` | -0.85128 |
| `explicit.stat_3695891184@T1` | -0.79547 |
| `explicit.stat_3695891184@T2` | -0.71902 |
| `explicit.stat_518292764@T1` | 0.64414 |
| `explicit.stat_691932474@T1` | -0.61589 |
| `explicit.stat_1509134228@T1` | 0.57474 |
| `explicit.stat_387439868@T2` | -0.55649 |

## Coverage (listings per base)

- … **Sapphire** — 35644 listings (35588 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 34738 listings (34696 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 26602 listings (26571 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 12492 listings (12474 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11369 listings (11345 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10994 listings (10969 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 10889 listings (10877 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10249 listings (10226 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10186 listings (10163 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 9680 listings (9667 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8466 listings (8451 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8132 listings (8123 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8047 listings (8038 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7299 listings (7277 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6992 listings (6985 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 6974 listings (6955 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6922 listings (6908 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6865 listings (6858 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6822 listings (6794 priced) [0.3–398912568423.8 ex]
- … **Ancestral Tiara** — 6748 listings (6719 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6704 listings (6695 priced) [0.2–275252424.7 ex]
- … **Bloodstone Amulet** — 6662 listings (6652 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6318 listings (6315 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6210 listings (6196 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6059 listings (6049 priced) [0.3–398912568423.8 ex]

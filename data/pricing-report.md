# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-17T03:03:39+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **567163** (565600 priced in exalted)
- Distinct bases: 987 · distinct mods: 3192 · mod rows: 2685113
- Sold signals: **25481** sold · 320813 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-17T02:55:24+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×26.77** (median |log error| 3.2872)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×68.61 · ±30% 4% · n=82246
- Premium segment (60ex+): skill **+0.13** · typical error ×322.27 · ±30% 0% · n=55547

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 11590 | ×55.39 | 21% | +0.03 | +0.05 |
| jewel | 10837 | ×10.73 | 4% | +0.06 | +0.10 |
| accessory.amulet | 10585 | ×49.20 | 20% | +0.03 | +0.04 |
| accessory.belt | 7917 | ×27.21 | 14% | +0.07 | +0.10 |
| armour.chest | 7708 | ×24.24 | 23% | +0.07 | +0.10 |
| armour.helmet | 7497 | ×30.51 | 18% | +0.06 | +0.09 |
| armour.boots | 6988 | ×39.37 | 21% | +0.08 | +0.10 |
| armour.gloves | 6820 | ×42.83 | 17% | +0.08 | +0.10 |
| other | 6448 | ×1.98 | 42% | +0.10 | +0.17 |
| weapon.wand | 4262 | ×45.62 | 17% | +0.07 | +0.09 |
| weapon.bow | 3352 | ×31.72 | 13% | +0.14 | +0.15 |
| weapon.crossbow | 3157 | ×32.74 | 13% | +0.10 | +0.15 |
| weapon.warstaff | 2018 | ×34.29 | 8% | +0.14 | +0.13 |
| weapon.staff | 1881 | ×49.69 | 8% | +0.11 | +0.11 |
| weapon.sceptre | 1872 | ×41.40 | 4% | +0.18 | +0.18 |
| weapon.spear | 1490 | ×46.08 | 14% | +0.08 | +0.09 |
| armour.focus | 1251 | ×25.71 | 6% | +0.15 | +0.17 |
| armour.quiver | 1174 | ×28.43 | 7% | +0.13 | +0.15 |
| flask.charm | 1000 | ×25.00 | 31% | +0.05 | +0.07 |
| armour.shield | 960 | ×20.16 | 8% | +0.04 | +0.06 |
| weapon.twomace | 890 | ×10.16 | 10% | +0.07 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=59256, R²=-0.9399

intercept: `-1.8185`  ·  log_price: True  ·  ilvl: `0.02602`  ·  n_mods: `0.76539`  ·  n_top_tier: `-0.25638`  ·  corrupted: `0.35858`  ·  quality: `0.22654`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.62636 |
| `explicit.stat_2301718443@T1` | 2.99335 |
| `explicit.stat_1805182458@T1` | -2.07588 |
| `explicit.stat_1697951953@T1` | -1.82877 |
| `explicit.stat_3780644166@T1` | -1.78265 |
| `explicit.stat_627767961@T1` | -1.70269 |
| `explicit.stat_3485067555@T1` | 1.69075 |
| `explicit.stat_3374165039@T1` | -1.67784 |
| `explicit.stat_3668351662@T1` | -1.64121 |
| `explicit.stat_3166958180@T1` | -1.53156 |
| `explicit.stat_239367161@T1` | -1.52742 |
| `explicit.stat_491450213@T1` | 1.51026 |

### other — n=54446, R²=-0.6416

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.35255`  ·  corrupted: `0.29804`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2974417149@T1` | 0.43687 |
| `explicit.stat_3291658075@T1` | 0.38545 |
| `explicit.stat_2968503605@T1` | 0.29063 |
| `explicit.stat_3299347043@T1` | -0.28812 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_2482852589@T1` | -0.17563 |
| `explicit.stat_2106365538@T1` | -0.16254 |
| `explicit.stat_1050105434@T1` | -0.13780 |
| `implicit.stat_2923486259` | -0.11395 |
| `pseudo.total_chaos_res` | 0.11394 |

### accessory.ring — n=52911, R²=-2.0226

intercept: `3.4246`  ·  log_price: True  ·  ilvl: `-0.04236`  ·  n_mods: `-0.00012`  ·  n_top_tier: `1.06421`  ·  corrupted: `0.02346`  ·  n_sockets: `2.18732`  ·  quality: `0.07105`

| stat_id | coef |
|---|---|
| `explicit.stat_2557965901@T1` | -1.10186 |
| `explicit.stat_1263695895@T2` | -1.09978 |
| `explicit.stat_2231156303@T1` | -1.09967 |
| `explicit.stat_1263695895@T1` | -1.09478 |
| `explicit.stat_2557965901@T2` | -1.09314 |
| `explicit.stat_1573130764@T1` | -1.09198 |
| `explicit.stat_1368271171@T2` | -1.08896 |
| `explicit.stat_3299347043@T1` | -1.08822 |
| `explicit.stat_803737631@T1` | -1.08804 |
| `explicit.stat_3325883026@T1` | -1.08560 |
| `explicit.stat_4220027924@T2` | -1.08517 |
| `explicit.stat_2231156303@T2` | -1.08379 |

### accessory.amulet — n=48489, R²=-2.1547

intercept: `3.6175`  ·  log_price: True  ·  ilvl: `-0.04430`  ·  n_mods: `-0.02474`  ·  n_top_tier: `1.11812`  ·  corrupted: `0.08519`  ·  n_sockets: `-0.09871`  ·  quality: `-0.00111`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.24260 |
| `explicit.stat_587431675@T2` | -1.19474 |
| `explicit.stat_2974417149@T1` | -1.18978 |
| `explicit.stat_803737631@T1` | -1.18151 |
| `explicit.stat_472520716@T2` | -1.18057 |
| `explicit.stat_2974417149@T2` | -1.17988 |
| `explicit.stat_1050105434@T2` | -1.16432 |
| `explicit.stat_803737631@T2` | -1.16254 |
| `explicit.stat_2866361420@T2` | -1.16209 |
| `explicit.stat_3299347043@T2` | -1.15813 |
| `explicit.stat_3917489142@T2` | -1.15057 |
| `explicit.stat_2866361420@T1` | -1.15042 |

### accessory.belt — n=36390, R²=-1.3701

intercept: `5.3733`  ·  log_price: True  ·  ilvl: `-0.06116`  ·  n_mods: `-0.09519`  ·  n_top_tier: `0.85526`  ·  corrupted: `1.28226`  ·  n_sockets: `-0.02561`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.24246 |
| `explicit.stat_3299347043@T2` | -1.03434 |
| `explicit.stat_2881298780@T1` | -0.99696 |
| `explicit.stat_4220027924@T2` | -0.95598 |
| `explicit.stat_1389754388@T1` | -0.95008 |
| `explicit.stat_51994685@T1` | -0.92972 |
| `explicit.stat_809229260@T2` | -0.91681 |
| `explicit.stat_1671376347@T2` | -0.88337 |
| `explicit.stat_644456512@T1` | -0.88198 |
| `explicit.stat_3372524247@T2` | -0.86321 |
| `explicit.stat_915769802@T2` | -0.85382 |
| `explicit.stat_2881298780@T2` | -0.84117 |

### armour.chest — n=36165, R²=-1.7181

intercept: `3.5127`  ·  log_price: True  ·  ilvl: `-0.04299`  ·  n_mods: `-0.01994`  ·  n_top_tier: `0.49173`  ·  corrupted: `0.08012`  ·  n_sockets: `0.02782`  ·  quality: `0.06310`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.62789 |
| `explicit.stat_3981240776@T1` | 1.05007 |
| `explicit.stat_986397080@T2` | -0.56245 |
| `explicit.stat_1692879867@T1` | -0.53203 |
| `explicit.stat_4080418644@T2` | -0.53139 |
| `explicit.stat_2451402625@T2` | -0.52590 |
| `explicit.stat_915769802@T2` | -0.52415 |
| `explicit.stat_986397080@T1` | -0.52360 |
| `explicit.stat_4080418644@T1` | -0.51887 |
| `explicit.stat_4015621042@T1` | -0.51851 |
| `explicit.stat_2339757871@T2` | -0.51693 |
| `explicit.stat_3372524247@T2` | -0.51573 |

### armour.helmet — n=35087, R²=-1.6313

intercept: `3.6835`  ·  log_price: True  ·  ilvl: `-0.04611`  ·  n_mods: `-0.03315`  ·  n_top_tier: `0.39845`  ·  corrupted: `0.74418`  ·  n_sockets: `0.06773`  ·  quality: `0.04864`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -6.26144 |
| `crafted.stat_3917489142@T1` | 1.14618 |
| `explicit.stat_1263695895@T1` | -0.64837 |
| `explicit.stat_3917489142@T2` | -0.63667 |
| `explicit.stat_2162097452@T2` | -0.55767 |
| `explicit.stat_1263695895@T2` | -0.54197 |
| `explicit.stat_3917489142@T1` | -0.51916 |
| `explicit.stat_1999113824@T1` | -0.49215 |
| `explicit.stat_4052037485@T2` | -0.48611 |
| `explicit.stat_3321629045@T2` | -0.46869 |
| `explicit.stat_2162097452@T1` | 0.45564 |
| `explicit.stat_1999113824@T2` | -0.43878 |

### armour.boots — n=32877, R²=-1.7489

intercept: `3.4208`  ·  log_price: True  ·  ilvl: `-0.04180`  ·  n_mods: `-0.02010`  ·  n_top_tier: `0.66964`  ·  corrupted: `-0.00505`  ·  n_sockets: `0.02027`  ·  quality: `0.05042`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.98677 |
| `explicit.stat_2250533757@T1` | 1.42399 |
| `explicit.stat_3299347043@T1` | -0.84240 |
| `explicit.stat_3917489142@T2` | -0.81562 |
| `explicit.stat_2339757871@T1` | -0.73915 |
| `explicit.stat_3917489142@T1` | -0.73584 |
| `explicit.stat_2160282525@T1` | -0.71353 |
| `explicit.stat_2923486259@T2` | -0.70741 |
| `explicit.stat_1671376347@T2` | -0.70306 |
| `explicit.stat_3299347043@T2` | -0.69897 |
| `explicit.stat_3484657501@T2` | -0.69631 |
| `explicit.stat_53045048@T1` | -0.68651 |

### armour.gloves — n=31943, R²=-1.7524

intercept: `3.7654`  ·  log_price: True  ·  ilvl: `-0.04720`  ·  n_mods: `-0.01671`  ·  n_top_tier: `0.55141`  ·  corrupted: `0.01572`  ·  n_sockets: `0.05160`  ·  quality: `0.04739`

| stat_id | coef |
|---|---|
| `explicit.stat_1671376347@T1` | 0.92043 |
| `explicit.stat_9187492@T1` | 0.88952 |
| `explicit.stat_9187492@T2` | -0.83355 |
| `rune.stat_836936635` | 0.78182 |
| `explicit.stat_2923486259@T1` | -0.77560 |
| `explicit.stat_3321629045@T2` | -0.68661 |
| `rune.stat_201332984` | -0.68601 |
| `explicit.stat_4052037485@T1` | -0.68506 |
| `explicit.stat_1999113824@T1` | 0.67690 |
| `explicit.stat_3484657501@T2` | -0.67035 |
| `explicit.stat_3917489142@T2` | -0.64302 |
| `explicit.stat_803737631@T2` | -0.63489 |

### weapon.wand — n=19929, R²=-2.2025

intercept: `3.7305`  ·  log_price: True  ·  ilvl: `-0.04606`  ·  n_mods: `-0.02752`  ·  n_top_tier: `0.45454`  ·  corrupted: `0.01083`  ·  n_sockets: `0.06216`  ·  quality: `0.00899`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.55762 |
| `explicit.stat_1545858329@T1` | 2.55707 |
| `rune.stat_124131830` | -2.48791 |
| `explicit.stat_4226189338@T1` | 2.27868 |
| `explicit.stat_124131830@T1` | 1.85590 |
| `explicit.stat_591105508@T1` | 1.84179 |
| `explicit.stat_736967255@T2` | 1.73842 |
| `crafted.stat_124131830` | 1.25824 |
| `explicit.stat_1600707273@T1` | 0.91093 |
| `explicit.stat_4226189338@T2` | 0.90221 |
| `explicit.stat_2254480358@T2` | 0.73216 |
| `explicit.stat_1600707273@T2` | -0.62014 |

### weapon.bow — n=15966, R²=-1.7442

intercept: `3.8545`  ·  log_price: True  ·  ilvl: `-0.04460`  ·  n_mods: `-0.09723`  ·  n_top_tier: `0.61953`  ·  corrupted: `0.38466`  ·  n_sockets: `0.03551`  ·  quality: `0.03403`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.50243 |
| `explicit.stat_1202301673@T1` | 1.35354 |
| `crafted.stat_3035140377` | 1.32396 |
| `explicit.stat_2463230181@T2` | -1.25683 |
| `explicit.stat_518292764@T2` | -1.11996 |
| `explicit.stat_1263695895@T1` | -1.07990 |
| `explicit.stat_2463230181@T1` | -1.04309 |
| `explicit.stat_3336890334@T1` | 1.04283 |
| `explicit.stat_1263695895@T2` | -1.00424 |
| `explicit.stat_1509134228@T1` | -0.84372 |
| `explicit.stat_3695891184@T2` | -0.81068 |
| `explicit.stat_1037193709@T1` | -0.79254 |

### weapon.crossbow — n=14992, R²=-1.6939

intercept: `3.8900`  ·  log_price: True  ·  ilvl: `-0.04668`  ·  n_mods: `-0.08305`  ·  n_top_tier: `0.70081`  ·  corrupted: `0.01367`  ·  n_sockets: `0.08514`  ·  quality: `0.02051`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.81864 |
| `explicit.stat_2250681686@T2` | -1.32589 |
| `explicit.stat_1980802737` | 1.21519 |
| `explicit.stat_1202301673@T1` | 1.15808 |
| `explicit.stat_1940865751@T2` | -0.91421 |
| `explicit.stat_1263695895@T2` | -0.91329 |
| `explicit.stat_1263695895@T1` | -0.88975 |
| `explicit.stat_1037193709@T1` | -0.87033 |
| `explicit.stat_1509134228@T2` | -0.86149 |
| `explicit.stat_2694482655@T1` | -0.85493 |
| `explicit.stat_210067635@T2` | -0.85309 |
| `explicit.stat_2250681686` | 0.84682 |

### flask.charm — n=14982, R²=-0.5655

intercept: `0.0527`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `2.45940`  ·  corrupted: `1.75491`  ·  quality: `0.00029`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.71213 |
| `explicit.stat_1056492907` | 3.13752 |
| `explicit.stat_828533480@T2` | -2.45943 |
| `explicit.stat_1873752457@T2` | -2.45939 |
| `explicit.stat_1120862500@T2` | -2.45939 |
| `explicit.stat_2676834156@T2` | -2.45939 |
| `explicit.stat_388617051@T2` | -2.45939 |
| `explicit.stat_828533480@T1` | -2.45938 |
| `explicit.stat_3196823591@T2` | -2.45938 |
| `explicit.stat_2365392475@T2` | -2.45937 |
| `explicit.stat_1873752457@T1` | -2.45936 |
| `explicit.stat_1366840608@T2` | -2.45925 |

### weapon.warstaff — n=9605, R²=-0.3787

intercept: `-9.7226`  ·  log_price: True  ·  ilvl: `0.13263`  ·  n_mods: `-0.20304`  ·  n_top_tier: `0.35199`  ·  corrupted: `0.23966`  ·  n_sockets: `0.19559`  ·  quality: `0.05934`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 1.15261 |
| `crafted.stat_210067635@T2` | 1.11827 |
| `explicit.stat_328541901@T1` | -0.97624 |
| `desecrated.stat_2231156303@T1` | 0.95738 |
| `desecrated.stat_2527686725@T1` | 0.95738 |
| `explicit.stat_328541901@T2` | -0.94140 |
| `rune.stat_243313994` | 0.89958 |
| `desecrated.stat_9187492` | 0.73807 |
| `explicit.stat_9187492@T1` | 0.69071 |
| `explicit.stat_748522257@T2` | 0.55411 |
| `explicit.stat_691932474@T2` | -0.49330 |
| `crafted.stat_3035140377` | 0.44782 |

### weapon.staff — n=8995, R²=-0.404

intercept: `-13.5958`  ·  log_price: True  ·  ilvl: `0.17777`  ·  n_mods: `-0.15237`  ·  n_top_tier: `0.47860`  ·  corrupted: `0.30509`  ·  n_sockets: `0.27659`  ·  quality: `0.04757`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.91884 |
| `explicit.stat_4226189338@T1` | 1.82303 |
| `explicit.stat_591105508@T1` | 1.35908 |
| `explicit.stat_293638271@T2` | -1.07254 |
| `explicit.stat_2254480358@T2` | 1.00489 |
| `explicit.stat_3962278098@T2` | 0.91784 |
| `explicit.stat_124131830@T1` | 0.89068 |
| `explicit.stat_124131830@T2` | 0.80201 |
| `explicit.stat_2254480358@T1` | 0.75842 |
| `rune.stat_124131830` | 0.75647 |
| `explicit.stat_2231156303@T2` | 0.72330 |
| `explicit.stat_2505884597@T2` | -0.71242 |

### weapon.sceptre — n=8877, R²=-0.3508

intercept: `-18.7643`  ·  log_price: True  ·  ilvl: `0.24054`  ·  n_mods: `-0.08586`  ·  n_top_tier: `0.30797`  ·  corrupted: `0.46460`  ·  n_sockets: `0.30115`  ·  quality: `0.04025`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.89600 |
| `explicit.stat_2162097452@T2` | 1.65408 |
| `explicit.stat_1250712710@T2` | 1.23129 |
| `explicit.stat_1263695895@T1` | -1.06195 |
| `explicit.stat_3057012405@T1` | 1.01207 |
| `explicit.stat_1263695895@T2` | -0.97358 |
| `explicit.stat_101878827@T1` | 0.76038 |
| `explicit.stat_1574590649@T1` | -0.72865 |
| `explicit.stat_2347036682@T1` | 0.67884 |
| `explicit.stat_849987426@T1` | 0.63785 |
| `explicit.stat_2347036682@T2` | -0.62535 |
| `explicit.stat_1574590649@T2` | -0.54255 |

### weapon.spear — n=7266, R²=-0.4359

intercept: `-11.1272`  ·  log_price: True  ·  ilvl: `0.15737`  ·  n_mods: `-0.14668`  ·  n_top_tier: `0.78308`  ·  corrupted: `-0.37626`  ·  n_sockets: `0.26585`  ·  quality: `0.06624`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.62291 |
| `explicit.stat_1509134228@T1` | 1.70402 |
| `explicit.stat_1202301673@T1` | 1.51185 |
| `explicit.stat_9187492@T1` | 1.20005 |
| `explicit.stat_1037193709@T1` | -1.17538 |
| `crafted.stat_3035140377` | 1.05212 |
| `explicit.stat_1263695895@T2` | -0.92324 |
| `explicit.stat_4080418644@T2` | -0.91850 |
| `explicit.stat_3261801346@T1` | -0.87154 |
| `explicit.stat_691932474@T1` | -0.85119 |
| `explicit.stat_1940865751@T2` | -0.83781 |
| `explicit.stat_3261801346@T2` | -0.82533 |

### armour.focus — n=5977, R²=-0.3728

intercept: `-12.5281`  ·  log_price: True  ·  ilvl: `0.16513`  ·  n_mods: `-0.18317`  ·  n_top_tier: `0.81847`  ·  corrupted: `0.47367`  ·  n_sockets: `0.39918`  ·  quality: `0.07298`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 8.86730 |
| `explicit.stat_4220027924@T2` | -1.34841 |
| `explicit.stat_3962278098@T1` | -1.32505 |
| `explicit.stat_2231156303@T2` | -0.95704 |
| `explicit.stat_3291658075@T1` | -0.95650 |
| `explicit.stat_2339757871@T2` | -0.93917 |
| `explicit.stat_2891184298@T2` | -0.89807 |
| `explicit.stat_4052037485@T2` | -0.88192 |
| `explicit.stat_2339757871@T1` | -0.82980 |
| `explicit.stat_2231156303@T1` | -0.82218 |
| `explicit.stat_737908626@T2` | -0.81466 |
| `explicit.stat_2974417149@T2` | -0.78443 |

### armour.quiver — n=5584, R²=-0.3189

intercept: `-14.3690`  ·  log_price: True  ·  ilvl: `0.17765`  ·  n_mods: `-0.12989`  ·  n_top_tier: `0.73594`  ·  corrupted: `0.80445`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.37911 |
| `explicit.stat_2463230181@T1` | 2.99878 |
| `explicit.stat_2463230181@T2` | 1.47050 |
| `explicit.stat_681332047@T2` | -1.20274 |
| `explicit.stat_1573130764@T1` | -1.11802 |
| `explicit.stat_2321178454@T2` | -1.06394 |
| `explicit.stat_803737631@T2` | -0.96836 |
| `explicit.stat_4067062424@T1` | -0.96150 |
| `explicit.stat_2321178454@T1` | -0.79286 |
| `explicit.stat_3261801346@T1` | -0.78655 |
| `explicit.stat_1573130764@T2` | -0.74811 |
| `explicit.stat_2194114101@T2` | -0.68792 |

### armour.shield — n=4862, R²=-0.4982

intercept: `-10.2416`  ·  log_price: True  ·  ilvl: `0.13811`  ·  n_mods: `-0.11401`  ·  n_top_tier: `0.70544`  ·  corrupted: `-0.29872`  ·  n_sockets: `0.28095`  ·  quality: `0.06325`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.41482 |
| `explicit.stat_328541901@T1` | -1.31197 |
| `explicit.stat_2481353198@T2` | -1.21711 |
| `explicit.stat_2339757871@T1` | -1.18733 |
| `explicit.stat_4095671657@T1` | -1.15885 |
| `explicit.stat_328541901@T2` | -1.13432 |
| `explicit.stat_3484657501@T2` | -1.10470 |
| `explicit.stat_3321629045@T2` | -1.07093 |
| `explicit.stat_3033371881@T2` | -1.05582 |
| `explicit.stat_2901986750@T1` | -0.99344 |
| `explicit.stat_2481353198@T1` | -0.93805 |
| `explicit.stat_1671376347@T1` | -0.91542 |

### weapon.twomace — n=4461, R²=-0.4947

intercept: `-9.3352`  ·  log_price: True  ·  ilvl: `0.12911`  ·  n_mods: `-0.18776`  ·  n_top_tier: `0.39012`  ·  corrupted: `-0.06098`  ·  n_sockets: `0.16199`  ·  quality: `0.05834`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.69143 |
| `desecrated.stat_1509134228@T1` | 2.42681 |
| `explicit.stat_1037193709@T1` | -1.63403 |
| `crafted.stat_3035140377` | 0.94957 |
| `explicit.stat_3336890334@T1` | -0.93388 |
| `explicit.stat_1037193709@T2` | -0.85187 |
| `explicit.stat_387439868@T2` | -0.83654 |
| `explicit.stat_1263695895@T2` | -0.69451 |
| `explicit.stat_691932474@T1` | -0.66041 |
| `explicit.stat_9187492@T1` | -0.65665 |
| `explicit.stat_210067635@T1` | 0.59288 |
| `explicit.stat_3639275092@T1` | -0.47236 |

## Coverage (listings per base)

- … **Sapphire** — 27505 listings (27458 priced) [0.3–885594757.8 ex]
- … **Emerald** — 26984 listings (26948 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 20645 listings (20623 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10494 listings (10479 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 9019 listings (9002 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8734 listings (8715 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8623 listings (8615 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8187 listings (8172 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8043 listings (8025 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 7983 listings (7972 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6700 listings (6690 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6443 listings (6437 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6396 listings (6390 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6378 listings (6359 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 5685 listings (5678 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 5676 listings (5653 priced) [0.3–398912568423.8 ex]
- … **Jade Amulet** — 5558 listings (5547 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 5530 listings (5513 priced) [0.2–24532814.5 ex]
- … **Amber Amulet** — 5527 listings (5520 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5471 listings (5450 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5366 listings (5357 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5252 listings (5245 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5067 listings (5065 priced) [0.3–3985176410.3 ex]
- … **Heavy Belt** — 5045 listings (5037 priced) [0.3–398912568423.8 ex]
- … **Lunar Amulet** — 5037 listings (5025 priced) [0.3–91750808.2 ex]

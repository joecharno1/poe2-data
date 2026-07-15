# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-15T16:34:09+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **515805** (514689 priced in exalted)
- Distinct bases: 983 · distinct mods: 3120 · mod rows: 2447487
- Sold signals: **26122** sold · 288536 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-15T16:24:54+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×26.12** (median |log error| 3.2627)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×61.25 · ±30% 5% · n=74477
- Premium segment (60ex+): skill **+0.11** · typical error ×220.94 · ±30% 0% · n=49755

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 10334 | ×55.18 | 21% | +0.07 | +0.09 |
| jewel | 9646 | ×9.73 | 5% | +0.03 | +0.06 |
| accessory.amulet | 9498 | ×53.50 | 20% | +0.03 | +0.03 |
| accessory.belt | 7296 | ×15.56 | 4% | +0.03 | +0.05 |
| armour.chest | 7099 | ×22.11 | 6% | +0.10 | +0.13 |
| armour.helmet | 6954 | ×20.39 | 5% | +0.05 | +0.06 |
| armour.boots | 6445 | ×35.34 | 13% | +0.10 | +0.12 |
| armour.gloves | 6332 | ×27.00 | 6% | +0.13 | +0.14 |
| other | 5665 | ×8.79 | 39% | +0.09 | +0.15 |
| weapon.wand | 4000 | ×35.44 | 18% | +0.07 | +0.08 |
| weapon.bow | 3193 | ×30.46 | 16% | +0.10 | +0.11 |
| weapon.crossbow | 2990 | ×23.08 | 19% | +0.09 | +0.12 |
| weapon.warstaff | 1839 | ×32.82 | 15% | +0.12 | +0.10 |
| weapon.staff | 1709 | ×57.47 | 12% | +0.09 | +0.10 |
| weapon.sceptre | 1705 | ×43.35 | 6% | +0.14 | +0.14 |
| weapon.spear | 1318 | ×62.80 | 15% | +0.09 | +0.09 |
| armour.focus | 1135 | ×45.01 | 8% | +0.13 | +0.17 |
| armour.quiver | 1094 | ×28.71 | 9% | +0.10 | +0.13 |
| flask.charm | 932 | ×49.99 | 34% | +0.03 | +0.06 |
| armour.shield | 906 | ×18.62 | 15% | +0.03 | +0.04 |
| weapon.twomace | 828 | ×14.67 | 13% | +0.06 | +0.06 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=52063, R²=-0.9161

intercept: `-1.7150`  ·  log_price: True  ·  ilvl: `0.02683`  ·  n_mods: `0.64657`  ·  n_top_tier: `-0.17876`  ·  corrupted: `0.28446`  ·  quality: `0.23809`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.33510 |
| `explicit.stat_2301718443@T1` | 2.90210 |
| `explicit.stat_627767961@T1` | -2.33446 |
| `explicit.stat_3485067555@T1` | 2.15210 |
| `explicit.stat_3780644166@T1` | -2.12585 |
| `explicit.stat_239367161@T1` | -1.89822 |
| `explicit.stat_1805182458@T1` | -1.84082 |
| `explicit.stat_924253255@T1` | -1.67836 |
| `explicit.stat_3091578504@T1` | -1.65937 |
| `explicit.stat_2653955271@T1` | -1.62435 |
| `explicit.stat_3166958180@T1` | -1.58054 |
| `explicit.stat_2594634307@T1` | 1.56283 |

### other — n=49824, R²=-0.5432

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00004`  ·  n_top_tier: `0.50663`  ·  corrupted: `0.43460`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 1.02304 |
| `explicit.stat_1589917703@T1` | -0.55373 |
| `explicit.stat_789117908@T1` | -0.51989 |
| `explicit.stat_2974417149@T1` | 0.41414 |
| `explicit.stat_3917489142@T1` | 0.33364 |
| `explicit.stat_736967255@T1` | -0.31739 |
| `explicit.stat_3299347043@T1` | -0.30813 |
| `explicit.stat_2482852589@T1` | -0.27330 |
| `implicit.stat_3879011313` | 0.23046 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23026 |
| `explicit.stat_2106365538@T1` | -0.19386 |

### accessory.ring — n=47246, R²=-1.984

intercept: `3.5043`  ·  log_price: True  ·  ilvl: `-0.04331`  ·  n_mods: `0.00135`  ·  n_top_tier: `0.98674`  ·  corrupted: `0.02917`  ·  n_sockets: `1.59359`  ·  quality: `0.06048`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -1.01965 |
| `explicit.stat_1573130764@T1` | -1.01559 |
| `explicit.stat_803737631@T1` | -1.01425 |
| `explicit.stat_1368271171@T2` | -1.01376 |
| `explicit.stat_2144192055@T1` | -1.01368 |
| `explicit.stat_3325883026@T1` | -1.01227 |
| `explicit.stat_3291658075@T2` | -1.01105 |
| `explicit.stat_1263695895@T1` | -1.01065 |
| `explicit.stat_3291658075@T1` | -1.00564 |
| `explicit.stat_3962278098@T2` | -1.00515 |
| `explicit.stat_1263695895@T2` | -1.00186 |
| `explicit.stat_2231156303@T2` | -1.00166 |

### accessory.amulet — n=43556, R²=-2.1336

intercept: `3.8437`  ·  log_price: True  ·  ilvl: `-0.04713`  ·  n_mods: `-0.02091`  ·  n_top_tier: `0.99914`  ·  corrupted: `0.03251`  ·  n_sockets: `-0.10237`  ·  quality: `0.00043`

| stat_id | coef |
|---|---|
| `explicit.stat_803737631@T1` | -1.07316 |
| `explicit.stat_472520716@T2` | -1.05555 |
| `explicit.stat_2901986750@T1` | -1.05371 |
| `explicit.stat_1050105434@T2` | -1.04804 |
| `explicit.stat_803737631@T2` | -1.04660 |
| `explicit.stat_472520716@T1` | -1.04114 |
| `explicit.stat_2974417149@T2` | -1.03373 |
| `explicit.stat_1444556985@T1` | -1.03282 |
| `explicit.stat_2866361420@T2` | -1.03055 |
| `explicit.stat_2866361420@T1` | -1.03037 |
| `explicit.stat_3917489142@T2` | -1.03030 |
| `explicit.stat_2974417149@T1` | -1.02764 |

### accessory.belt — n=33438, R²=-0.6217

intercept: `6.6647`  ·  log_price: True  ·  ilvl: `-0.05542`  ·  n_mods: `-0.42148`  ·  n_top_tier: `1.07738`  ·  corrupted: `0.92068`  ·  n_sockets: `0.39347`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.71033 |
| `explicit.stat_1389754388@T1` | -1.68608 |
| `explicit.stat_2881298780@T1` | -1.62053 |
| `explicit.stat_644456512@T1` | -1.36126 |
| `explicit.stat_3299347043@T2` | -1.34270 |
| `explicit.stat_809229260@T1` | -1.32490 |
| `explicit.stat_809229260@T2` | -1.28191 |
| `explicit.stat_2923486259@T1` | -1.25851 |
| `explicit.stat_51994685@T1` | -1.23228 |
| `explicit.stat_4220027924@T2` | -1.19208 |
| `explicit.stat_1389754388@T2` | -1.19181 |
| `explicit.stat_4080418644@T2` | -1.18324 |

### armour.chest — n=33089, R²=-1.0805

intercept: `4.1955`  ·  log_price: True  ·  ilvl: `-0.04862`  ·  n_mods: `-0.11203`  ·  n_top_tier: `0.56149`  ·  corrupted: `0.20888`  ·  n_sockets: `0.13659`  ·  quality: `0.03573`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.94036 |
| `explicit.stat_4080418644@T1` | -0.95717 |
| `explicit.stat_3484657501@T1` | -0.95612 |
| `explicit.stat_1692879867@T1` | -0.78004 |
| `explicit.stat_986397080@T2` | -0.77201 |
| `explicit.stat_2451402625@T1` | -0.76994 |
| `explicit.stat_2451402625@T2` | -0.75312 |
| `explicit.stat_1692879867@T2` | -0.74368 |
| `explicit.stat_1999113824@T1` | -0.72848 |
| `explicit.stat_986397080@T1` | -0.71065 |
| `explicit.stat_4080418644@T2` | -0.70007 |
| `explicit.stat_915769802@T2` | -0.69170 |

### armour.helmet — n=32220, R²=-0.888

intercept: `3.8996`  ·  log_price: True  ·  ilvl: `-0.04807`  ·  n_mods: `-0.12628`  ·  n_top_tier: `0.44010`  ·  corrupted: `0.73057`  ·  n_sockets: `0.16933`  ·  quality: `0.03909`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.80668 |
| `explicit.stat_3917489142@T2` | -1.06880 |
| `explicit.stat_53045048@T2` | -0.87025 |
| `explicit.stat_1999113824@T1` | -0.83351 |
| `explicit.stat_1263695895@T1` | -0.82423 |
| `explicit.stat_3261801346@T1` | -0.72082 |
| `explicit.stat_3917489142@T1` | -0.62412 |
| `explicit.stat_1263695895@T2` | -0.61656 |
| `explicit.stat_1050105434@T2` | -0.60450 |
| `explicit.stat_3321629045@T2` | -0.59944 |
| `explicit.stat_2162097452@T2` | -0.55822 |
| `explicit.stat_587431675@T2` | -0.55331 |

### armour.boots — n=30150, R²=-1.3442

intercept: `4.2503`  ·  log_price: True  ·  ilvl: `-0.05118`  ·  n_mods: `-0.06623`  ·  n_top_tier: `0.68473`  ·  corrupted: `0.14811`  ·  n_sockets: `0.09791`  ·  quality: `0.02987`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 1.58606 |
| `explicit.stat_2250533757@T1` | 1.38885 |
| `explicit.stat_3299347043@T1` | -1.10624 |
| `explicit.stat_2339757871@T1` | -1.07785 |
| `explicit.stat_2923486259@T2` | -0.91198 |
| `explicit.stat_3917489142@T2` | -0.90402 |
| `desecrated.stat_2250533757@T2` | -0.84345 |
| `explicit.stat_1999113824@T2` | -0.84180 |
| `explicit.stat_2160282525@T1` | -0.83449 |
| `explicit.stat_1062208444@T2` | -0.80227 |
| `explicit.stat_53045048@T1` | -0.79107 |
| `explicit.stat_1671376347@T2` | -0.77664 |

### armour.gloves — n=29398, R²=-1.1565

intercept: `3.8142`  ·  log_price: True  ·  ilvl: `-0.04964`  ·  n_mods: `-0.05015`  ·  n_top_tier: `0.50888`  ·  corrupted: `0.15825`  ·  n_sockets: `0.20530`  ·  quality: `0.03904`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | -6.11500 |
| `explicit.stat_2339757871@T1` | 3.97781 |
| `explicit.stat_3484657501@T2` | -1.11610 |
| `explicit.stat_3484657501@T1` | -0.99846 |
| `explicit.stat_2923486259@T1` | -0.90355 |
| `explicit.stat_803737631@T2` | -0.86735 |
| `explicit.stat_3321629045@T2` | -0.86472 |
| `explicit.stat_9187492@T1` | 0.83550 |
| `rune.stat_836936635` | 0.81467 |
| `explicit.stat_803737631@T1` | -0.79548 |
| `explicit.stat_4052037485@T1` | -0.74846 |
| `explicit.stat_1999113824@T2` | -0.70222 |

### weapon.wand — n=18744, R²=-2.2409

intercept: `3.6954`  ·  log_price: True  ·  ilvl: `-0.04562`  ·  n_mods: `-0.01643`  ·  n_top_tier: `0.58456`  ·  corrupted: `0.02650`  ·  n_sockets: `0.03688`  ·  quality: `0.00127`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.68428 |
| `explicit.stat_1545858329@T1` | 2.67711 |
| `explicit.stat_2254480358@T1` | 2.21827 |
| `explicit.stat_4226189338@T1` | 1.83589 |
| `explicit.stat_591105508@T1` | 1.75861 |
| `explicit.stat_736967255@T2` | 1.64123 |
| `explicit.stat_124131830@T1` | 1.63349 |
| `crafted.stat_124131830` | 1.14232 |
| `explicit.stat_2254480358@T2` | 0.82171 |
| `explicit.stat_737908626@T1` | -0.66607 |
| `explicit.stat_2768835289@T2` | 0.66194 |
| `explicit.stat_1263695895@T2` | -0.65191 |

### weapon.bow — n=15077, R²=-1.9472

intercept: `3.6750`  ·  log_price: True  ·  ilvl: `-0.04388`  ·  n_mods: `-0.04961`  ·  n_top_tier: `0.58596`  ·  corrupted: `-0.08884`  ·  n_sockets: `0.01457`  ·  quality: `0.03453`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.94513 |
| `explicit.stat_1202301673@T1` | 1.61396 |
| `desecrated.stat_666077204@T1` | 1.61090 |
| `crafted.stat_3035140377` | 1.42402 |
| `explicit.stat_2463230181@T2` | -0.92901 |
| `explicit.stat_1263695895@T1` | -0.86547 |
| `explicit.stat_1263695895@T2` | -0.83227 |
| `explicit.stat_3695891184@T2` | -0.69686 |
| `explicit.stat_3695891184@T1` | -0.67498 |
| `explicit.stat_518292764@T2` | -0.66398 |
| `explicit.stat_1509134228@T1` | -0.66006 |
| `explicit.stat_1368271171@T2` | -0.65198 |

### weapon.crossbow — n=14207, R²=-1.9305

intercept: `3.6977`  ·  log_price: True  ·  ilvl: `-0.04496`  ·  n_mods: `-0.02617`  ·  n_top_tier: `0.67007`  ·  corrupted: `0.07040`  ·  n_sockets: `0.02805`  ·  quality: `0.00997`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.93043 |
| `explicit.stat_709508406@T1` | 1.45827 |
| `explicit.stat_2250681686@T2` | -1.42173 |
| `explicit.stat_1202301673@T1` | 1.37141 |
| `explicit.stat_1980802737` | 1.21279 |
| `crafted.stat_3035140377` | 0.93016 |
| `explicit.stat_2250681686` | 0.84855 |
| `explicit.stat_1263695895@T2` | -0.79557 |
| `explicit.stat_1509134228@T2` | -0.77377 |
| `explicit.stat_210067635@T1` | -0.76116 |
| `explicit.stat_210067635@T2` | -0.75989 |
| `explicit.stat_2694482655@T1` | -0.75376 |

### flask.charm — n=13342, R²=-0.5481

intercept: `0.0086`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.71225`  ·  corrupted: `2.14872`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.32075 |
| `explicit.stat_1056492907` | 3.32891 |
| `explicit.stat_828533480@T2` | -2.71226 |
| `explicit.stat_828533480@T1` | -2.71225 |
| `explicit.stat_2541588185@T2` | -2.71225 |
| `explicit.stat_2676834156@T2` | -2.71224 |
| `explicit.stat_1120862500@T2` | -2.71224 |
| `explicit.stat_3196823591@T2` | -2.71224 |
| `explicit.stat_1873752457@T2` | -2.71223 |
| `explicit.stat_388617051@T2` | -2.71222 |
| `explicit.stat_2365392475@T2` | -2.71222 |
| `explicit.stat_1366840608@T2` | -2.71221 |

### weapon.warstaff — n=8771, R²=-0.4587

intercept: `-7.0292`  ·  log_price: True  ·  ilvl: `0.09557`  ·  n_mods: `-0.16795`  ·  n_top_tier: `0.58247`  ·  corrupted: `0.28750`  ·  n_sockets: `0.12065`  ·  quality: `0.06470`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.24366 |
| `explicit.stat_328541901@T2` | -1.01820 |
| `explicit.stat_328541901@T1` | -0.99197 |
| `explicit.stat_1037193709@T1` | 0.87837 |
| `explicit.stat_1037193709@T2` | -0.79032 |
| `desecrated.stat_9187492` | 0.68659 |
| `explicit.stat_55876295@T2` | -0.63598 |
| `explicit.stat_1368271171@T1` | -0.60757 |
| `explicit.stat_3695891184@T2` | -0.57529 |
| `explicit.stat_1940865751@T1` | -0.56134 |
| `explicit.stat_210067635@T1` | -0.54634 |
| `crafted.stat_210067635@T2` | 0.53935 |

### weapon.staff — n=8192, R²=-0.4432

intercept: `-11.1369`  ·  log_price: True  ·  ilvl: `0.14334`  ·  n_mods: `-0.09926`  ·  n_top_tier: `0.62997`  ·  corrupted: `0.19710`  ·  n_sockets: `0.22635`  ·  quality: `0.04447`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T2` | 1.12281 |
| `explicit.stat_293638271@T2` | -1.05109 |
| `explicit.stat_4226189338@T1` | 1.05055 |
| `explicit.stat_3962278098@T2` | 1.00648 |
| `explicit.stat_124131830@T1` | 0.99853 |
| `explicit.stat_1545858329@T1` | 0.99204 |
| `explicit.stat_2768835289@T2` | 0.87555 |
| `explicit.stat_2974417149@T1` | -0.78450 |
| `explicit.stat_2505884597@T2` | -0.74656 |
| `explicit.stat_591105508@T1` | 0.74073 |
| `explicit.stat_1263695895@T2` | -0.71180 |
| `explicit.stat_274716455@T1` | -0.68178 |

### weapon.sceptre — n=8097, R²=-0.3971

intercept: `-16.6558`  ·  log_price: True  ·  ilvl: `0.21057`  ·  n_mods: `-0.03232`  ·  n_top_tier: `0.29330`  ·  corrupted: `0.61323`  ·  n_sockets: `0.21402`  ·  quality: `0.05352`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.50997 |
| `explicit.stat_2162097452@T2` | 1.52027 |
| `explicit.stat_3057012405@T1` | 1.16858 |
| `explicit.stat_1250712710@T2` | 0.94926 |
| `explicit.stat_849987426@T1` | 0.80135 |
| `explicit.stat_101878827@T1` | 0.76614 |
| `explicit.stat_2347036682@T2` | -0.75233 |
| `explicit.stat_1263695895@T1` | -0.65894 |
| `explicit.stat_1263695895@T2` | -0.63238 |
| `explicit.stat_2347036682@T1` | 0.62968 |
| `explicit.stat_2854751904@T2` | -0.52328 |
| `explicit.stat_1574590649@T2` | -0.51914 |

### weapon.spear — n=6676, R²=-0.5285

intercept: `-8.2762`  ·  log_price: True  ·  ilvl: `0.11124`  ·  n_mods: `-0.03519`  ·  n_top_tier: `0.75617`  ·  corrupted: `-0.11869`  ·  n_sockets: `0.19161`  ·  quality: `0.10003`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.05106 |
| `explicit.stat_1202301673@T1` | 1.88600 |
| `explicit.stat_9187492@T1` | 1.68601 |
| `desecrated.stat_210067635@T1` | -1.13879 |
| `explicit.stat_1263695895@T2` | -1.05754 |
| `explicit.stat_210067635@T1` | 1.02926 |
| `explicit.stat_1509134228@T1` | 0.97374 |
| `explicit.stat_55876295@T1` | -0.97323 |
| `crafted.stat_3035140377` | 0.95850 |
| `explicit.stat_1037193709@T1` | -0.94378 |
| `explicit.stat_55876295@T2` | -0.77305 |
| `explicit.stat_1940865751@T2` | -0.76136 |

### armour.focus — n=5486, R²=-0.4251

intercept: `-11.6406`  ·  log_price: True  ·  ilvl: `0.14845`  ·  n_mods: `-0.13207`  ·  n_top_tier: `0.83727`  ·  corrupted: `0.71365`  ·  n_sockets: `0.43652`  ·  quality: `0.07555`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 4.31213 |
| `explicit.stat_4220027924@T2` | -1.34593 |
| `explicit.stat_3962278098@T1` | -1.29764 |
| `explicit.stat_736967255@T2` | -1.10731 |
| `explicit.stat_2923486259@T1` | -1.04995 |
| `explicit.stat_3962278098@T2` | -1.00992 |
| `explicit.stat_2231156303@T1` | -0.98649 |
| `explicit.stat_2231156303@T2` | -0.98204 |
| `explicit.stat_2974417149@T2` | -0.97450 |
| `explicit.stat_124131830@T2` | -0.89471 |
| `explicit.stat_2339757871@T2` | -0.88119 |
| `explicit.stat_737908626@T2` | -0.87517 |

### armour.quiver — n=5122, R²=-0.3854

intercept: `-12.5256`  ·  log_price: True  ·  ilvl: `0.15216`  ·  n_mods: `-0.07247`  ·  n_top_tier: `0.87410`  ·  corrupted: `0.42002`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | 1.87792 |
| `desecrated.stat_3932115504@T1` | 1.35966 |
| `explicit.stat_4067062424@T1` | -1.29257 |
| `explicit.stat_681332047@T2` | -1.28842 |
| `explicit.stat_2321178454@T2` | -1.18076 |
| `explicit.stat_803737631@T2` | -1.12724 |
| `explicit.stat_1573130764@T1` | -1.09485 |
| `explicit.stat_4067062424@T2` | -1.00938 |
| `explicit.stat_1573130764@T2` | -0.98275 |
| `explicit.stat_2194114101@T2` | -0.95673 |
| `explicit.stat_3261801346@T1` | -0.94665 |
| `explicit.stat_2321178454@T1` | -0.86230 |

### armour.shield — n=4446, R²=-0.5498

intercept: `-8.7908`  ·  log_price: True  ·  ilvl: `0.11416`  ·  n_mods: `-0.07060`  ·  n_top_tier: `0.53059`  ·  corrupted: `-0.14506`  ·  n_sockets: `0.11788`  ·  quality: `0.06769`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.12443 |
| `explicit.stat_1011760251@T1` | -1.08656 |
| `explicit.stat_2481353198@T2` | -0.98690 |
| `explicit.stat_4095671657@T1` | -0.97542 |
| `explicit.stat_2481353198@T1` | -0.97298 |
| `explicit.stat_1011760251@T2` | -0.96020 |
| `explicit.stat_3484657501@T2` | -0.91569 |
| `explicit.stat_3484657501@T1` | -0.90883 |
| `explicit.stat_3033371881@T2` | -0.88764 |
| `explicit.stat_3321629045@T2` | -0.79596 |
| `explicit.stat_328541901@T1` | -0.77693 |
| `explicit.stat_3372524247@T2` | -0.72838 |

### weapon.twomace — n=4095, R²=-0.5188

intercept: `-9.9742`  ·  log_price: True  ·  ilvl: `0.13076`  ·  n_mods: `-0.13271`  ·  n_top_tier: `0.43234`  ·  corrupted: `0.35710`  ·  n_sockets: `0.15661`  ·  quality: `0.05679`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.85146 |
| `desecrated.stat_1509134228@T1` | 2.70911 |
| `explicit.stat_1037193709@T1` | -1.64639 |
| `explicit.stat_3336890334@T1` | -1.06697 |
| `crafted.stat_3035140377` | 0.91116 |
| `explicit.stat_518292764@T2` | -0.85643 |
| `explicit.stat_387439868@T2` | -0.79622 |
| `explicit.stat_1037193709@T2` | -0.77859 |
| `explicit.stat_210067635@T1` | 0.67302 |
| `explicit.stat_3639275092@T1` | -0.63443 |
| `explicit.stat_9187492@T1` | -0.56678 |
| `explicit.stat_2694482655@T1` | -0.55464 |

## Coverage (listings per base)

- … **Sapphire** — 24272 listings (24235 priced) [0.3–7553463.8 ex]
- … **Emerald** — 23838 listings (23808 priced) [0.3–7553463.8 ex]
- … **Ruby** — 18244 listings (18228 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 9746 listings (9737 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8102 listings (8091 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 7840 listings (7823 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 7738 listings (7731 priced) [0.2–19945827.9 ex]
- … **Gold Amulet** — 7378 listings (7367 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 7263 listings (7259 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 7224 listings (7210 priced) [0.2–91750808.2 ex]
- … **Sapphire Ring** — 6054 listings (6048 priced) [0.2–307202867.9 ex]
- … **Dueling Wand** — 5970 listings (5954 priced) [0.3–4297682211.9 ex]
- … **Topaz Ring** — 5773 listings (5768 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5749 listings (5746 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5177 listings (5160 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5151 listings (5146 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 5040 listings (5026 priced) [0.6–398912568423.8 ex]
- … **Amber Amulet** — 5002 listings (4998 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 4998 listings (4991 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4953 listings (4946 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4831 listings (4825 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 4658 listings (4652 priced) [0.2–275252424.7 ex]
- … **Heavy Belt** — 4642 listings (4638 priced) [0.3–398912568423.8 ex]
- … **Azure Amulet** — 4571 listings (4571 priced) [0.3–123132003.2 ex]
- … **Obliterator Bow** — 4531 listings (4516 priced) [0.3–42622633798.0 ex]

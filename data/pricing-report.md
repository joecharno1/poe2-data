# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-16T16:25:37+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **552699** (551220 priced in exalted)
- Distinct bases: 986 · distinct mods: 3181 · mod rows: 2619174
- Sold signals: **25672** sold · 311370 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-16T16:16:47+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×27.33** (median |log error| 3.3079)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×63.47 · ±30% 4% · n=80321
- Premium segment (60ex+): skill **+0.12** · typical error ×235.80 · ±30% 0% · n=54075

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 11253 | ×55.35 | 22% | +0.04 | +0.06 |
| jewel | 10519 | ×10.54 | 5% | +0.07 | +0.10 |
| accessory.amulet | 10278 | ×53.52 | 20% | +0.03 | +0.03 |
| accessory.belt | 7767 | ×15.22 | 4% | +0.02 | +0.04 |
| armour.chest | 7505 | ×21.93 | 8% | +0.11 | +0.13 |
| armour.helmet | 7309 | ×19.24 | 6% | +0.05 | +0.07 |
| armour.boots | 6853 | ×43.57 | 16% | +0.09 | +0.12 |
| armour.gloves | 6677 | ×35.24 | 8% | +0.11 | +0.12 |
| other | 6266 | ×9.84 | 36% | +0.09 | +0.16 |
| weapon.wand | 4186 | ×41.40 | 17% | +0.08 | +0.08 |
| weapon.bow | 3324 | ×33.78 | 16% | +0.11 | +0.11 |
| weapon.crossbow | 3132 | ×30.05 | 15% | +0.09 | +0.13 |
| weapon.warstaff | 1978 | ×33.48 | 11% | +0.14 | +0.12 |
| weapon.staff | 1828 | ×53.41 | 9% | +0.10 | +0.10 |
| weapon.sceptre | 1804 | ×42.94 | 4% | +0.17 | +0.17 |
| weapon.spear | 1469 | ×48.71 | 16% | +0.08 | +0.09 |
| armour.focus | 1208 | ×30.98 | 6% | +0.14 | +0.17 |
| armour.quiver | 1157 | ×28.08 | 8% | +0.12 | +0.14 |
| flask.charm | 1018 | ×30.00 | 32% | +0.04 | +0.07 |
| armour.shield | 950 | ×24.62 | 10% | +0.03 | +0.05 |
| weapon.twomace | 878 | ×11.35 | 11% | +0.08 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=57253, R²=-0.9202

intercept: `-1.7487`  ·  log_price: True  ·  ilvl: `0.02656`  ·  n_mods: `0.72705`  ·  n_top_tier: `-0.24577`  ·  corrupted: `0.24168`  ·  quality: `0.22537`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.81550 |
| `explicit.stat_2301718443@T1` | 2.90851 |
| `explicit.stat_627767961@T1` | -2.17145 |
| `explicit.stat_1805182458@T1` | -1.98691 |
| `explicit.stat_3780644166@T1` | -1.94039 |
| `explicit.stat_3485067555@T1` | 1.90010 |
| `explicit.stat_1852872083@T1` | -1.61546 |
| `explicit.stat_2523933828@T1` | -1.57698 |
| `explicit.stat_3166958180@T1` | -1.55423 |
| `explicit.stat_3668351662@T1` | -1.46704 |
| `explicit.stat_1697951953@T1` | -1.41650 |
| `explicit.stat_2653955271@T1` | -1.36938 |

### other — n=53172, R²=-0.4649

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.69306`  ·  corrupted: `0.29857`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.22194 |
| `explicit.stat_2482852589@T1` | 0.92857 |
| `explicit.stat_789117908@T1` | -0.76999 |
| `explicit.stat_3917489142@T1` | 0.58522 |
| `explicit.stat_2974417149@T1` | 0.56003 |
| `explicit.stat_2106365538@T1` | -0.42076 |
| `explicit.stat_3299347043@T1` | -0.32517 |
| `explicit.stat_736967255@T1` | -0.28842 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23026 |
| `explicit.stat_3141070085@T1` | -0.17603 |

### accessory.ring — n=51365, R²=-2.0241

intercept: `3.4929`  ·  log_price: True  ·  ilvl: `-0.04316`  ·  n_mods: `0.00051`  ·  n_top_tier: `0.97577`  ·  corrupted: `0.02924`  ·  n_sockets: `2.19318`  ·  quality: `0.07032`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -1.01287 |
| `explicit.stat_1263695895@T1` | -1.01259 |
| `explicit.stat_1263695895@T2` | -1.00709 |
| `explicit.stat_1368271171@T2` | -0.99814 |
| `explicit.stat_2144192055@T1` | -0.99530 |
| `explicit.stat_2231156303@T2` | -0.99444 |
| `explicit.stat_3291658075@T2` | -0.99312 |
| `explicit.stat_803737631@T1` | -0.99241 |
| `explicit.stat_4220027924@T2` | -0.99143 |
| `explicit.stat_3325883026@T1` | -0.98994 |
| `explicit.stat_1573130764@T1` | -0.98966 |
| `explicit.stat_1368271171@T1` | -0.98933 |

### accessory.amulet — n=47095, R²=-2.1524

intercept: `3.7678`  ·  log_price: True  ·  ilvl: `-0.04608`  ·  n_mods: `-0.02203`  ·  n_top_tier: `1.15146`  ·  corrupted: `0.09751`  ·  n_sockets: `-0.10941`  ·  quality: `-0.00181`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.23893 |
| `explicit.stat_587431675@T2` | -1.22598 |
| `explicit.stat_472520716@T2` | -1.21269 |
| `explicit.stat_1050105434@T2` | -1.20543 |
| `explicit.stat_803737631@T1` | -1.20358 |
| `explicit.stat_2866361420@T2` | -1.19615 |
| `explicit.stat_803737631@T2` | -1.19139 |
| `explicit.stat_2901986750@T1` | -1.19036 |
| `explicit.stat_472520716@T1` | -1.18757 |
| `explicit.stat_1671376347@T2` | -1.18467 |
| `explicit.stat_3489782002@T2` | -1.18219 |
| `explicit.stat_3917489142@T2` | -1.18175 |

### accessory.belt — n=35565, R²=-0.7517

intercept: `6.6797`  ·  log_price: True  ·  ilvl: `-0.06042`  ·  n_mods: `-0.40320`  ·  n_top_tier: `0.98800`  ·  corrupted: `0.98282`  ·  n_sockets: `-0.48992`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.49458 |
| `explicit.stat_3299347043@T1` | -1.42663 |
| `explicit.stat_3299347043@T2` | -1.36038 |
| `explicit.stat_2881298780@T1` | -1.35784 |
| `explicit.stat_4220027924@T2` | -1.23710 |
| `explicit.stat_644456512@T1` | -1.20889 |
| `explicit.stat_809229260@T2` | -1.20464 |
| `explicit.stat_51994685@T1` | -1.19155 |
| `explicit.stat_809229260@T1` | -1.15716 |
| `explicit.stat_2923486259@T1` | -1.14174 |
| `explicit.stat_1671376347@T2` | -1.12175 |
| `explicit.stat_2923486259@T2` | -1.08343 |

### armour.chest — n=35297, R²=-1.205

intercept: `4.2352`  ·  log_price: True  ·  ilvl: `-0.04948`  ·  n_mods: `-0.09458`  ·  n_top_tier: `0.54422`  ·  corrupted: `0.18715`  ·  n_sockets: `0.16316`  ·  quality: `0.04906`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.89806 |
| `explicit.stat_986397080@T2` | -0.94030 |
| `explicit.stat_3981240776@T1` | 0.85841 |
| `explicit.stat_986397080@T1` | -0.85371 |
| `explicit.stat_3484657501@T1` | -0.84821 |
| `explicit.stat_1692879867@T2` | -0.74978 |
| `explicit.stat_1999113824@T1` | -0.73019 |
| `explicit.stat_4080418644@T1` | -0.69801 |
| `explicit.stat_1692879867@T1` | -0.67251 |
| `explicit.stat_915769802@T2` | -0.66973 |
| `explicit.stat_4015621042@T1` | -0.65690 |
| `explicit.stat_2923486259@T2` | -0.65409 |

### armour.helmet — n=34252, R²=-0.9591

intercept: `3.9471`  ·  log_price: True  ·  ilvl: `-0.04873`  ·  n_mods: `-0.10547`  ·  n_top_tier: `0.40288`  ·  corrupted: `0.65621`  ·  n_sockets: `0.19393`  ·  quality: `0.03602`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.68219 |
| `explicit.stat_3917489142@T2` | -0.88830 |
| `explicit.stat_1999113824@T1` | -0.83684 |
| `explicit.stat_3321629045@T2` | -0.77806 |
| `explicit.stat_53045048@T2` | -0.65846 |
| `explicit.stat_2162097452@T2` | -0.64099 |
| `explicit.stat_1999113824@T2` | -0.59310 |
| `explicit.stat_1263695895@T2` | -0.56235 |
| `explicit.stat_1050105434@T2` | -0.56210 |
| `explicit.stat_3261801346@T1` | -0.54001 |
| `explicit.stat_4052037485@T2` | -0.49294 |
| `explicit.stat_2162097452@T1` | 0.49157 |

### armour.boots — n=32040, R²=-1.4813

intercept: `4.0544`  ·  log_price: True  ·  ilvl: `-0.04927`  ·  n_mods: `-0.04785`  ·  n_top_tier: `0.61900`  ·  corrupted: `0.04474`  ·  n_sockets: `0.05047`  ·  quality: `0.04545`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.52883 |
| `explicit.stat_2250533757@T1` | 1.46431 |
| `explicit.stat_3299347043@T1` | -0.98544 |
| `explicit.stat_3917489142@T2` | -0.88628 |
| `explicit.stat_2339757871@T1` | -0.85255 |
| `explicit.stat_2923486259@T2` | -0.85072 |
| `explicit.stat_1999113824@T2` | -0.78833 |
| `explicit.stat_2160282525@T1` | -0.76431 |
| `explicit.stat_3917489142@T1` | -0.72909 |
| `explicit.stat_1062208444@T2` | -0.70558 |
| `explicit.stat_4052037485@T2` | -0.69252 |
| `explicit.stat_3484657501@T2` | -0.68867 |

### armour.gloves — n=31156, R²=-1.3065

intercept: `4.0347`  ·  log_price: True  ·  ilvl: `-0.05224`  ·  n_mods: `-0.04974`  ·  n_top_tier: `0.52247`  ·  corrupted: `0.08062`  ·  n_sockets: `0.17925`  ·  quality: `0.03733`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.07013 |
| `rune.stat_201332984` | -2.07637 |
| `explicit.stat_2923486259@T1` | -1.05110 |
| `explicit.stat_3484657501@T2` | -0.94755 |
| `explicit.stat_9187492@T1` | 0.88168 |
| `explicit.stat_3321629045@T2` | -0.86110 |
| `explicit.stat_1671376347@T1` | 0.81379 |
| `explicit.stat_803737631@T2` | -0.80705 |
| `explicit.stat_3484657501@T1` | -0.80555 |
| `explicit.stat_4052037485@T1` | -0.74324 |
| `explicit.stat_1754445556@T2` | -0.71387 |
| `explicit.stat_803737631@T1` | -0.65479 |

### weapon.wand — n=19628, R²=-2.1785

intercept: `3.6642`  ·  log_price: True  ·  ilvl: `-0.04524`  ·  n_mods: `-0.02491`  ·  n_top_tier: `0.36873`  ·  corrupted: `0.00957`  ·  n_sockets: `0.05441`  ·  quality: `0.00882`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.64062 |
| `explicit.stat_2254480358@T1` | 2.45555 |
| `rune.stat_124131830` | -2.42124 |
| `explicit.stat_4226189338@T1` | 2.08862 |
| `explicit.stat_591105508@T1` | 1.98699 |
| `explicit.stat_124131830@T1` | 1.92544 |
| `explicit.stat_736967255@T2` | 1.81905 |
| `explicit.stat_1600707273@T1` | 1.32329 |
| `crafted.stat_124131830` | 1.26811 |
| `explicit.stat_2254480358@T2` | 1.07793 |
| `explicit.stat_4226189338@T2` | 0.85750 |
| `explicit.stat_1263695895@T2` | -0.53285 |

### weapon.bow — n=15673, R²=-1.9196

intercept: `3.7246`  ·  log_price: True  ·  ilvl: `-0.04502`  ·  n_mods: `-0.04306`  ·  n_top_tier: `0.65373`  ·  corrupted: `-0.00548`  ·  n_sockets: `0.00706`  ·  quality: `0.03804`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.09181 |
| `desecrated.stat_210067635@T1` | -1.83774 |
| `explicit.stat_1202301673@T1` | 1.54644 |
| `crafted.stat_3035140377` | 1.45438 |
| `explicit.stat_2463230181@T2` | -1.00059 |
| `explicit.stat_1263695895@T2` | -0.95357 |
| `explicit.stat_1263695895@T1` | -0.94347 |
| `explicit.stat_518292764@T2` | -0.86613 |
| `explicit.stat_3695891184@T2` | -0.76438 |
| `explicit.stat_3695891184@T1` | -0.74917 |
| `explicit.stat_1037193709@T1` | -0.73773 |
| `explicit.stat_1509134228@T1` | -0.73126 |

### weapon.crossbow — n=14766, R²=-1.8267

intercept: `3.7188`  ·  log_price: True  ·  ilvl: `-0.04537`  ·  n_mods: `-0.04793`  ·  n_top_tier: `0.76635`  ·  corrupted: `0.05732`  ·  n_sockets: `0.05373`  ·  quality: `0.01695`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.91809 |
| `explicit.stat_2250681686@T2` | -1.39769 |
| `explicit.stat_1202301673@T1` | 1.17066 |
| `explicit.stat_1980802737` | 1.14895 |
| `explicit.stat_1263695895@T2` | -0.98280 |
| `explicit.stat_709508406@T1` | 0.97236 |
| `crafted.stat_3035140377` | 0.95765 |
| `explicit.stat_1544773869@T2` | -0.95354 |
| `explicit.stat_2694482655@T1` | -0.94419 |
| `explicit.stat_1509134228@T2` | -0.93376 |
| `explicit.stat_1263695895@T1` | -0.91171 |
| `explicit.stat_3695891184@T1` | -0.86666 |

### flask.charm — n=14567, R²=-0.5549

intercept: `0.0417`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.36660`  ·  corrupted: `1.90007`  ·  quality: `0.00051`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.56486 |
| `explicit.stat_1056492907` | 3.23961 |
| `explicit.stat_828533480@T2` | -2.36662 |
| `explicit.stat_828533480@T1` | -2.36660 |
| `explicit.stat_1120862500@T2` | -2.36659 |
| `explicit.stat_388617051@T2` | -2.36659 |
| `explicit.stat_1873752457@T2` | -2.36659 |
| `explicit.stat_3196823591@T2` | -2.36658 |
| `explicit.stat_2676834156@T2` | -2.36658 |
| `explicit.stat_2365392475@T2` | -2.36657 |
| `explicit.stat_1873752457@T1` | -2.36656 |
| `explicit.stat_2541588185@T2` | -2.36655 |

### weapon.warstaff — n=9365, R²=-0.4031

intercept: `-9.2219`  ·  log_price: True  ·  ilvl: `0.12442`  ·  n_mods: `-0.18967`  ·  n_top_tier: `0.30547`  ·  corrupted: `0.05833`  ·  n_sockets: `0.18448`  ·  quality: `0.06087`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.10825 |
| `rune.stat_243313994` | 1.00559 |
| `explicit.stat_328541901@T1` | -0.85398 |
| `explicit.stat_328541901@T2` | -0.79674 |
| `explicit.stat_9187492@T1` | 0.75863 |
| `explicit.stat_1037193709@T1` | 0.73416 |
| `desecrated.stat_9187492` | 0.72981 |
| `explicit.stat_1940865751@T1` | -0.53874 |
| `explicit.stat_518292764@T1` | -0.52019 |
| `explicit.stat_748522257@T2` | 0.49240 |
| `crafted.stat_3035140377` | 0.43512 |
| `explicit.stat_1368271171@T1` | -0.43369 |

### weapon.staff — n=8762, R²=-0.4295

intercept: `-13.1580`  ·  log_price: True  ·  ilvl: `0.17062`  ·  n_mods: `-0.13206`  ·  n_top_tier: `0.51310`  ·  corrupted: `0.42880`  ·  n_sockets: `0.22260`  ·  quality: `0.03936`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.72435 |
| `explicit.stat_591105508@T1` | 1.45582 |
| `explicit.stat_4226189338@T1` | 1.44577 |
| `explicit.stat_293638271@T2` | -1.14912 |
| `explicit.stat_3962278098@T2` | 0.92933 |
| `rune.stat_124131830` | 0.89618 |
| `explicit.stat_124131830@T2` | 0.84103 |
| `explicit.stat_2505884597@T2` | -0.71022 |
| `explicit.stat_124131830@T1` | 0.67013 |
| `explicit.stat_1263695895@T2` | -0.66497 |
| `explicit.stat_2968503605@T1` | -0.63333 |
| `explicit.stat_2974417149@T1` | -0.58268 |

### weapon.sceptre — n=8678, R²=-0.3596

intercept: `-18.0425`  ·  log_price: True  ·  ilvl: `0.22886`  ·  n_mods: `-0.06349`  ·  n_top_tier: `0.33470`  ·  corrupted: `0.41667`  ·  n_sockets: `0.29134`  ·  quality: `0.04607`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.83522 |
| `explicit.stat_2162097452@T2` | 1.63081 |
| `explicit.stat_1250712710@T2` | 1.34051 |
| `explicit.stat_3057012405@T1` | 1.04865 |
| `explicit.stat_1263695895@T1` | -0.95234 |
| `explicit.stat_1574590649@T1` | -0.89366 |
| `explicit.stat_2347036682@T2` | -0.82459 |
| `explicit.stat_1263695895@T2` | -0.77710 |
| `explicit.stat_2347036682@T1` | 0.68978 |
| `explicit.stat_289128254@T2` | -0.66754 |
| `explicit.stat_2854751904@T2` | -0.65759 |
| `explicit.stat_101878827@T1` | 0.50799 |

### weapon.spear — n=7111, R²=-0.475

intercept: `-10.2216`  ·  log_price: True  ·  ilvl: `0.13975`  ·  n_mods: `-0.08029`  ·  n_top_tier: `0.78488`  ·  corrupted: `-0.11566`  ·  n_sockets: `0.26324`  ·  quality: `0.06307`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.20092 |
| `explicit.stat_1202301673@T1` | 1.70053 |
| `explicit.stat_1509134228@T1` | 1.58918 |
| `explicit.stat_9187492@T1` | 1.51102 |
| `explicit.stat_1037193709@T1` | -1.30260 |
| `crafted.stat_3035140377` | 1.08072 |
| `explicit.stat_1263695895@T2` | -1.01570 |
| `explicit.stat_691932474@T1` | -0.90340 |
| `explicit.stat_55876295@T1` | -0.88158 |
| `explicit.stat_4080418644@T2` | -0.83640 |
| `explicit.stat_1940865751@T2` | -0.82885 |
| `explicit.stat_3261801346@T1` | -0.80922 |

### armour.focus — n=5812, R²=-0.3718

intercept: `-13.0738`  ·  log_price: True  ·  ilvl: `0.16956`  ·  n_mods: `-0.17777`  ·  n_top_tier: `0.75818`  ·  corrupted: `0.28221`  ·  n_sockets: `0.49494`  ·  quality: `0.07503`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 7.56523 |
| `explicit.stat_3962278098@T1` | -1.31709 |
| `explicit.stat_4220027924@T2` | -1.25714 |
| `crafted.stat_737908626@T2` | 1.25387 |
| `explicit.stat_3291658075@T1` | -1.21813 |
| `explicit.stat_2231156303@T2` | -1.04200 |
| `explicit.stat_2231156303@T1` | -0.99269 |
| `explicit.stat_2339757871@T1` | -0.87504 |
| `explicit.stat_2923486259@T1` | -0.86629 |
| `explicit.stat_736967255@T2` | -0.86201 |
| `explicit.stat_2974417149@T1` | -0.84396 |
| `explicit.stat_2339757871@T2` | -0.81921 |

### armour.quiver — n=5461, R²=-0.3504

intercept: `-13.3429`  ·  log_price: True  ·  ilvl: `0.16256`  ·  n_mods: `-0.12360`  ·  n_top_tier: `0.75186`  ·  corrupted: `0.84235`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.29163 |
| `explicit.stat_2463230181@T1` | 1.75939 |
| `explicit.stat_1573130764@T1` | -1.18792 |
| `explicit.stat_681332047@T2` | -1.15039 |
| `explicit.stat_4067062424@T1` | -1.14057 |
| `explicit.stat_2321178454@T2` | -1.05316 |
| `explicit.stat_803737631@T2` | -1.02212 |
| `explicit.stat_2194114101@T2` | -0.93049 |
| `explicit.stat_3261801346@T1` | -0.90984 |
| `explicit.stat_4067062424@T2` | -0.87984 |
| `explicit.stat_803737631@T1` | -0.86384 |
| `explicit.stat_2321178454@T1` | -0.86191 |

### armour.shield — n=4742, R²=-0.5097

intercept: `-10.7371`  ·  log_price: True  ·  ilvl: `0.14019`  ·  n_mods: `-0.09014`  ·  n_top_tier: `0.64990`  ·  corrupted: `-0.32614`  ·  n_sockets: `0.25257`  ·  quality: `0.06702`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.25009 |
| `explicit.stat_2481353198@T2` | -1.20599 |
| `explicit.stat_3484657501@T1` | -1.20382 |
| `explicit.stat_3484657501@T2` | -1.19690 |
| `explicit.stat_328541901@T1` | -1.14289 |
| `explicit.stat_2481353198@T1` | -1.09975 |
| `explicit.stat_2923486259@T1` | -1.09903 |
| `explicit.stat_2923486259@T2` | -1.09071 |
| `explicit.stat_3321629045@T2` | -1.02161 |
| `explicit.stat_1011760251@T2` | -0.98921 |
| `explicit.stat_3033371881@T2` | -0.96625 |
| `explicit.stat_4095671657@T1` | -0.88783 |

### weapon.twomace — n=4358, R²=-0.4955

intercept: `-8.7923`  ·  log_price: True  ·  ilvl: `0.11747`  ·  n_mods: `-0.16365`  ·  n_top_tier: `0.36133`  ·  corrupted: `-0.02682`  ·  n_sockets: `0.17649`  ·  quality: `0.05720`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -5.20258 |
| `desecrated.stat_1509134228@T1` | 3.13645 |
| `explicit.stat_1037193709@T1` | -1.68386 |
| `crafted.stat_3035140377` | 0.97140 |
| `explicit.stat_3336890334@T1` | -0.87433 |
| `explicit.stat_1037193709@T2` | -0.83651 |
| `explicit.stat_387439868@T2` | -0.74937 |
| `explicit.stat_210067635@T1` | 0.67856 |
| `explicit.stat_1509134228@T1` | 0.67762 |
| `explicit.stat_691932474@T1` | -0.61580 |
| `explicit.stat_9187492@T1` | -0.60286 |
| `explicit.stat_518292764@T2` | -0.55509 |

## Coverage (listings per base)

- … **Sapphire** — 26606 listings (26560 priced) [0.3–885594757.8 ex]
- … **Emerald** — 26103 listings (26071 priced) [0.3–885594757.8 ex]
- … **Ruby** — 19970 listings (19950 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10282 listings (10267 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8759 listings (8743 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8496 listings (8477 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8385 listings (8378 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 7983 listings (7969 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 7823 listings (7805 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 7780 listings (7771 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6529 listings (6521 priced) [0.2–307202867.9 ex]
- … **Dueling Wand** — 6277 listings (6259 priced) [0.3–4297682211.9 ex]
- … **Topaz Ring** — 6252 listings (6246 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6213 listings (6207 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5548 listings (5525 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5521 listings (5516 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 5389 listings (5375 priced) [0.2–24532814.5 ex]
- … **Amber Amulet** — 5384 listings (5378 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 5383 listings (5373 priced) [0.3–4547453.5 ex]
- … **Ancestral Tiara** — 5358 listings (5339 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5197 listings (5189 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5097 listings (5090 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 4936 listings (4934 priced) [0.3–123132003.2 ex]
- … **Heavy Belt** — 4925 listings (4917 priced) [0.3–398912568423.8 ex]
- … **Lunar Amulet** — 4885 listings (4874 priced) [0.3–91750808.2 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-14T07:32:42+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **458482** (457560 priced in exalted)
- Distinct bases: 978 · distinct mods: 3036 · mod rows: 2177762
- Sold signals: **26998** sold · 252437 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-14T07:23:59+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×23.60** (median |log error| 3.1613)
- Within ±30% of asking price: **21%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.09** · typical error ×84.30 · ±30% 5% · n=65785
- Premium segment (60ex+): skill **+0.09** · typical error ×394.73 · ±30% 0% · n=43316

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 9013 | ×51.34 | 21% | +0.04 | +0.05 |
| accessory.amulet | 8396 | ×44.79 | 21% | +0.02 | +0.02 |
| jewel | 8279 | ×8.61 | 6% | +0.02 | +0.05 |
| accessory.belt | 6532 | ×46.98 | 22% | +0.05 | +0.07 |
| armour.chest | 6355 | ×11.99 | 27% | +0.04 | +0.07 |
| armour.helmet | 6250 | ×26.51 | 22% | +0.04 | +0.08 |
| armour.boots | 5822 | ×19.04 | 25% | +0.04 | +0.06 |
| armour.gloves | 5682 | ×29.48 | 24% | +0.03 | +0.04 |
| other | 5063 | ×2.44 | 42% | +0.09 | +0.16 |
| weapon.wand | 3703 | ×32.26 | 21% | +0.06 | +0.07 |
| weapon.bow | 2952 | ×28.89 | 19% | +0.08 | +0.08 |
| weapon.crossbow | 2817 | ×23.06 | 22% | +0.09 | +0.11 |
| weapon.warstaff | 1636 | ×42.19 | 19% | +0.09 | +0.10 |
| weapon.sceptre | 1498 | ×49.07 | 10% | +0.09 | +0.09 |
| weapon.staff | 1496 | ×52.82 | 18% | +0.06 | +0.07 |
| weapon.spear | 1245 | ×40.06 | 20% | +0.08 | +0.06 |
| armour.focus | 1035 | ×44.65 | 11% | +0.13 | +0.13 |
| armour.quiver | 985 | ×27.29 | 14% | +0.06 | +0.10 |
| armour.shield | 778 | ×19.89 | 19% | +0.03 | +0.04 |
| flask.charm | 746 | ×29.65 | 34% | +0.02 | +0.02 |
| weapon.twomace | 733 | ×26.50 | 15% | +0.06 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=44731, R²=-0.6108

intercept: `1.6041`  ·  log_price: True  ·  ilvl: `0.00007`  ·  n_mods: `0.01781`  ·  n_top_tier: `0.33309`  ·  corrupted: `0.33622`  ·  n_sockets: `-0.00009`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.50860 |
| `explicit.stat_2974417149@T1` | 0.48270 |
| `explicit.stat_789117908@T1` | -0.33610 |
| `explicit.stat_2891184298@T1` | 0.31795 |
| `explicit.stat_1050105434@T1` | -0.26017 |
| `explicit.stat_3299347043@T1` | -0.24296 |
| `implicit.stat_4041853756` | 0.22847 |
| `implicit.stat_3879011313` | 0.22847 |
| `explicit.stat_3917489142@T1` | 0.18683 |
| `implicit.stat_1379411836` | -0.13385 |
| `explicit.stat_2482852589@T1` | -0.09759 |
| `implicit.stat_2923486259` | -0.07278 |

### jewel — n=44674, R²=-0.7761

intercept: `-1.4886`  ·  log_price: True  ·  ilvl: `0.03174`  ·  n_mods: `0.49176`  ·  n_top_tier: `-0.17870`  ·  corrupted: `0.13804`  ·  quality: `0.23332`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.78310 |
| `explicit.stat_2301718443@T1` | 3.27940 |
| `explicit.stat_1697447343@T1` | -3.12438 |
| `explicit.stat_3780644166@T1` | -2.61494 |
| `explicit.stat_627767961@T1` | -2.25849 |
| `explicit.stat_1315743832@T1` | 2.06599 |
| `explicit.stat_3473929743@T1` | -2.00535 |
| `explicit.stat_795138349@T1` | -1.89576 |
| `explicit.stat_3485067555@T1` | 1.85635 |
| `explicit.stat_3166958180@T1` | -1.83113 |
| `explicit.stat_1805182458@T1` | -1.82738 |
| `explicit.stat_21071013@T1` | 1.63200 |

### accessory.ring — n=41256, R²=-1.9841

intercept: `3.3997`  ·  log_price: True  ·  ilvl: `-0.04191`  ·  n_mods: `-0.00104`  ·  n_top_tier: `0.56550`  ·  corrupted: `0.04650`  ·  n_sockets: `0.58388`  ·  quality: `0.07307`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -0.61079 |
| `explicit.stat_3325883026@T1` | -0.60510 |
| `explicit.stat_1263695895@T1` | -0.60164 |
| `explicit.stat_2557965901@T1` | -0.59898 |
| `explicit.stat_1573130764@T1` | -0.59661 |
| `explicit.stat_2557965901@T2` | -0.59126 |
| `explicit.stat_3962278098@T2` | -0.59102 |
| `explicit.stat_3032590688@T2` | -0.58945 |
| `explicit.stat_3291658075@T1` | -0.58834 |
| `explicit.stat_2231156303@T2` | -0.58450 |
| `explicit.stat_1368271171@T2` | -0.58440 |
| `explicit.stat_3917489142@T2` | -0.58376 |

### accessory.amulet — n=38332, R²=-2.1322

intercept: `3.9536`  ·  log_price: True  ·  ilvl: `-0.04794`  ·  n_mods: `-0.02706`  ·  n_top_tier: `0.78679`  ·  corrupted: `0.02943`  ·  n_sockets: `-0.03980`  ·  quality: `0.00129`

| stat_id | coef |
|---|---|
| `explicit.stat_2748665614@T1` | -0.90965 |
| `explicit.stat_2748665614@T2` | -0.88751 |
| `explicit.stat_124131830@T2` | -0.86747 |
| `explicit.stat_2901986750@T1` | -0.86443 |
| `explicit.stat_3299347043@T1` | -0.85551 |
| `explicit.stat_3299347043@T2` | -0.85130 |
| `explicit.stat_3917489142@T2` | -0.84205 |
| `explicit.stat_472520716@T1` | -0.84111 |
| `explicit.stat_472520716@T2` | -0.83738 |
| `explicit.stat_1050105434@T2` | -0.83625 |
| `explicit.stat_2974417149@T1` | -0.83537 |
| `explicit.stat_3917489142@T1` | -0.83149 |

### accessory.belt — n=29918, R²=-1.6136

intercept: `3.1605`  ·  log_price: True  ·  ilvl: `-0.03764`  ·  n_mods: `-0.02406`  ·  n_top_tier: `1.04354`  ·  corrupted: `1.33031`  ·  n_sockets: `1.50153`

| stat_id | coef |
|---|---|
| `explicit.stat_2881298780@T1` | -1.07360 |
| `explicit.stat_51994685@T1` | -1.07331 |
| `explicit.stat_809229260@T2` | -1.07327 |
| `explicit.stat_1389754388@T1` | -1.06925 |
| `explicit.stat_3325883026@T1` | -1.06254 |
| `explicit.stat_4220027924@T2` | -1.05474 |
| `explicit.stat_2881298780@T2` | -1.04619 |
| `explicit.stat_1671376347@T2` | -1.04597 |
| `explicit.stat_3299347043@T1` | -1.04153 |
| `explicit.stat_809229260@T1` | -1.04023 |
| `explicit.stat_51994685@T2` | -1.04013 |
| `explicit.stat_1570770415@T2` | -1.03926 |

### armour.chest — n=29565, R²=-1.7765

intercept: `3.1679`  ·  log_price: True  ·  ilvl: `-0.03912`  ·  n_mods: `-0.00844`  ·  n_top_tier: `0.17282`  ·  corrupted: `0.17653`  ·  n_sockets: `0.00782`  ·  quality: `0.02024`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.09103 |
| `explicit.stat_3981240776@T1` | 1.13071 |
| `explicit.stat_4080418644@T2` | -0.20953 |
| `explicit.stat_4080418644@T1` | -0.20070 |
| `explicit.stat_915769802@T1` | -0.19262 |
| `explicit.stat_986397080@T2` | -0.18630 |
| `explicit.stat_124859000@T2` | -0.18383 |
| `explicit.stat_2451402625@T2` | -0.18239 |
| `explicit.stat_3484657501@T1` | -0.18229 |
| `explicit.stat_915769802@T2` | -0.18215 |
| `explicit.stat_4015621042@T1` | -0.18133 |
| `explicit.stat_3261801346@T2` | -0.18106 |

### armour.helmet — n=28887, R²=-1.7896

intercept: `3.5593`  ·  log_price: True  ·  ilvl: `-0.04450`  ·  n_mods: `-0.01392`  ·  n_top_tier: `0.32989`  ·  corrupted: `0.43911`  ·  n_sockets: `0.00559`  ·  quality: `0.06433`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.55778 |
| `explicit.stat_2339757871@T1` | -1.11109 |
| `explicit.stat_1263695895@T1` | -0.50978 |
| `explicit.stat_1263695895@T2` | -0.44791 |
| `explicit.stat_53045048@T1` | -0.40460 |
| `explicit.stat_3917489142@T2` | -0.39825 |
| `explicit.stat_2162097452@T2` | -0.38397 |
| `explicit.stat_1999113824@T1` | -0.37359 |
| `explicit.stat_3261801346@T1` | -0.36373 |
| `explicit.stat_53045048@T2` | -0.36198 |
| `explicit.stat_3261801346@T2` | -0.36178 |
| `explicit.stat_328541901@T2` | -0.35970 |

### armour.boots — n=27090, R²=-1.7948

intercept: `3.2010`  ·  log_price: True  ·  ilvl: `-0.03951`  ·  n_mods: `-0.00564`  ·  n_top_tier: `0.59762`  ·  corrupted: `0.04528`  ·  n_sockets: `0.00441`  ·  quality: `0.02028`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.06863 |
| `desecrated.stat_2250533757@T2` | -0.70534 |
| `explicit.stat_3917489142@T2` | -0.68581 |
| `explicit.stat_3917489142@T1` | -0.66078 |
| `explicit.stat_3362812763@T1` | -0.62782 |
| `explicit.stat_1062208444@T2` | -0.62200 |
| `explicit.stat_2923486259@T2` | -0.61404 |
| `explicit.stat_99927264@T1` | -0.61303 |
| `explicit.stat_2160282525@T1` | -0.61265 |
| `explicit.stat_4080418644@T1` | -0.61245 |
| `explicit.stat_3299347043@T1` | -0.61117 |
| `explicit.stat_3362812763@T2` | -0.61117 |

### armour.gloves — n=26442, R²=-1.9856

intercept: `3.5422`  ·  log_price: True  ·  ilvl: `-0.04436`  ·  n_mods: `-0.00586`  ·  n_top_tier: `0.39555`  ·  corrupted: `-0.00620`  ·  n_sockets: `0.01590`  ·  quality: `0.03014`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T1` | 0.83684 |
| `explicit.stat_1671376347@T1` | 0.72965 |
| `explicit.stat_9187492@T2` | -0.72332 |
| `rune.stat_201332984` | 0.70192 |
| `explicit.stat_3484657501@T2` | -0.50590 |
| `explicit.stat_3917489142@T2` | -0.47304 |
| `explicit.stat_803737631@T2` | -0.45905 |
| `explicit.stat_2923486259@T2` | -0.44504 |
| `explicit.stat_3484657501@T1` | -0.43788 |
| `explicit.stat_3917489142@T1` | -0.43591 |
| `explicit.stat_328541901@T2` | -0.42614 |
| `explicit.stat_3321629045@T2` | -0.42539 |

### weapon.wand — n=17252, R²=-2.3061

intercept: `3.5866`  ·  log_price: True  ·  ilvl: `-0.04463`  ·  n_mods: `-0.01038`  ·  n_top_tier: `0.05525`  ·  corrupted: `-0.04850`  ·  n_sockets: `0.02846`  ·  quality: `0.00060`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.12137 |
| `rune.stat_124131830` | -2.73980 |
| `explicit.stat_2254480358@T1` | 2.57331 |
| `explicit.stat_591105508@T1` | 2.31841 |
| `explicit.stat_124131830@T1` | 2.25464 |
| `explicit.stat_4226189338@T1` | 2.24787 |
| `explicit.stat_2768835289@T2` | 1.45635 |
| `crafted.stat_124131830` | 1.23622 |
| `explicit.stat_2254480358@T2` | 0.88790 |
| `explicit.stat_736967255@T2` | 0.73207 |
| `explicit.stat_737908626@T1` | -0.13292 |
| `explicit.stat_2968503605@T1` | -0.12787 |

### weapon.bow — n=13993, R²=-2.0654

intercept: `3.3188`  ·  log_price: True  ·  ilvl: `-0.04045`  ·  n_mods: `-0.02208`  ·  n_top_tier: `0.75907`  ·  corrupted: `-0.06411`  ·  n_sockets: `-0.00477`  ·  quality: `0.03102`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.00376 |
| `explicit.stat_1202301673@T1` | 1.48857 |
| `crafted.stat_3035140377` | 1.30059 |
| `explicit.stat_1263695895@T1` | -0.87336 |
| `explicit.stat_1509134228@T1` | -0.81661 |
| `explicit.stat_1263695895@T2` | -0.81021 |
| `explicit.stat_669069897@T1` | -0.80838 |
| `explicit.stat_55876295@T1` | -0.79762 |
| `explicit.stat_3336890334@T2` | -0.79531 |
| `explicit.stat_3695891184@T1` | -0.79510 |
| `explicit.stat_821021828@T2` | -0.79434 |
| `explicit.stat_1368271171@T2` | -0.79076 |

### weapon.crossbow — n=13243, R²=-2.0026

intercept: `3.5583`  ·  log_price: True  ·  ilvl: `-0.04387`  ·  n_mods: `-0.01035`  ·  n_top_tier: `0.66570`  ·  corrupted: `-0.00933`  ·  n_sockets: `0.01627`  ·  quality: `0.00870`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.93126 |
| `explicit.stat_2250681686@T2` | -1.75316 |
| `explicit.stat_709508406@T1` | 1.54810 |
| `explicit.stat_1202301673@T1` | 1.37917 |
| `explicit.stat_1980802737` | 1.20977 |
| `explicit.stat_2250681686` | 1.14088 |
| `crafted.stat_3035140377` | 0.94324 |
| `explicit.stat_1263695895@T2` | -0.82578 |
| `explicit.stat_1202301673@T2` | -0.81009 |
| `explicit.stat_1263695895@T1` | -0.80096 |
| `explicit.stat_669069897@T1` | -0.73532 |
| `explicit.stat_1037193709@T2` | -0.71185 |

### flask.charm — n=11262, R²=-0.5073

intercept: `0.0004`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `1.56237`  ·  corrupted: `1.95845`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.44712 |
| `explicit.stat_1056492907` | 3.36752 |
| `explicit.stat_828533480@T2` | -1.56238 |
| `explicit.stat_1120862500@T2` | -1.56237 |
| `explicit.stat_3196823591@T2` | -1.56237 |
| `explicit.stat_1873752457@T2` | -1.56237 |
| `explicit.stat_2676834156@T2` | -1.56237 |
| `explicit.stat_1366840608@T2` | -1.56237 |
| `explicit.stat_1873752457@T1` | -1.56237 |
| `explicit.stat_2541588185@T2` | -1.56236 |
| `explicit.stat_388617051@T2` | -1.56236 |
| `explicit.stat_828533480@T1` | -1.56235 |

### weapon.warstaff — n=7758, R²=-0.528

intercept: `-3.6927`  ·  log_price: True  ·  ilvl: `0.05230`  ·  n_mods: `-0.13770`  ·  n_top_tier: `0.79330`  ·  corrupted: `0.24821`  ·  n_sockets: `0.07869`  ·  quality: `0.05418`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.32026 |
| `explicit.stat_328541901@T2` | -1.08672 |
| `explicit.stat_328541901@T1` | -1.07790 |
| `explicit.stat_1037193709@T1` | 1.00730 |
| `explicit.stat_55876295@T2` | -0.93478 |
| `explicit.stat_1037193709@T2` | -0.92756 |
| `explicit.stat_691932474@T2` | -0.91012 |
| `explicit.stat_55876295@T1` | -0.89160 |
| `explicit.stat_3336890334@T2` | -0.87883 |
| `explicit.stat_210067635@T1` | -0.87765 |
| `explicit.stat_1940865751@T1` | -0.83576 |
| `explicit.stat_791928121@T2` | -0.81907 |

### weapon.sceptre — n=7148, R²=-0.4778

intercept: `-10.9740`  ·  log_price: True  ·  ilvl: `0.13819`  ·  n_mods: `-0.05155`  ·  n_top_tier: `0.54941`  ·  corrupted: `0.30908`  ·  n_sockets: `0.25121`  ·  quality: `0.09140`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.03134 |
| `explicit.stat_2162097452@T2` | 1.36164 |
| `explicit.stat_4080418644@T1` | -1.21106 |
| `explicit.stat_1263695895@T1` | -1.06368 |
| `explicit.stat_1574590649@T2` | -1.04091 |
| `explicit.stat_1263695895@T2` | -0.97849 |
| `explicit.stat_4080418644@T2` | -0.93995 |
| `explicit.stat_289128254@T2` | -0.75595 |
| `explicit.stat_2347036682@T2` | -0.73136 |
| `explicit.stat_1050105434@T2` | -0.69283 |
| `explicit.stat_3639275092@T2` | -0.61766 |
| `explicit.stat_2854751904@T2` | -0.59384 |

### weapon.staff — n=7135, R²=-0.5675

intercept: `-6.4218`  ·  log_price: True  ·  ilvl: `0.08140`  ·  n_mods: `-0.04502`  ·  n_top_tier: `0.35717`  ·  corrupted: `0.05398`  ·  n_sockets: `0.17293`  ·  quality: `0.05645`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.01031 |
| `explicit.stat_124131830@T1` | 1.89168 |
| `explicit.stat_1545858329@T1` | 1.53599 |
| `explicit.stat_2768835289@T2` | 1.35306 |
| `explicit.stat_2254480358@T1` | 1.16514 |
| `explicit.stat_3291658075@T2` | 0.94400 |
| `explicit.stat_4226189338@T2` | 0.89690 |
| `rune.stat_124131830` | 0.66888 |
| `explicit.stat_1600707273@T1` | 0.64773 |
| `explicit.stat_2974417149@T1` | -0.62713 |
| `explicit.stat_2254480358@T2` | 0.61365 |
| `explicit.stat_293638271@T2` | -0.47175 |

### weapon.spear — n=5995, R²=-0.6556

intercept: `-3.4497`  ·  log_price: True  ·  ilvl: `0.04539`  ·  n_mods: `-0.01215`  ·  n_top_tier: `0.54606`  ·  corrupted: `-0.07259`  ·  n_sockets: `0.08423`  ·  quality: `0.08897`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.20070 |
| `explicit.stat_1202301673@T1` | 2.46057 |
| `explicit.stat_9187492@T1` | 2.31656 |
| `crafted.stat_3035140377` | 1.27788 |
| `explicit.stat_210067635@T1` | 0.87383 |
| `explicit.stat_1263695895@T2` | -0.73781 |
| `crafted.stat_518292764` | 0.72324 |
| `explicit.stat_55876295@T1` | -0.65052 |
| `explicit.stat_55876295@T2` | -0.59980 |
| `explicit.stat_1509134228@T1` | 0.58248 |
| `explicit.stat_1509134228@T2` | -0.57169 |
| `explicit.stat_1940865751@T2` | -0.53711 |

### armour.focus — n=4896, R²=-0.4673

intercept: `-9.3040`  ·  log_price: True  ·  ilvl: `0.11602`  ·  n_mods: `-0.06038`  ·  n_top_tier: `0.82184`  ·  corrupted: `0.80784`  ·  n_sockets: `0.45203`  ·  quality: `0.07009`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 6.12675 |
| `explicit.stat_4220027924@T2` | -1.28349 |
| `crafted.stat_2974417149@T1` | -1.25674 |
| `crafted.stat_737908626@T2` | -1.19530 |
| `explicit.stat_4220027924@T1` | -1.08636 |
| `explicit.stat_736967255@T2` | -1.05569 |
| `explicit.stat_2923486259@T1` | -0.96465 |
| `explicit.stat_328541901@T2` | -0.92965 |
| `explicit.stat_737908626@T2` | -0.88069 |
| `explicit.stat_3291658075@T1` | -0.87976 |
| `explicit.stat_3962278098@T2` | -0.85318 |
| `explicit.stat_3962278098@T1` | -0.82660 |

### armour.quiver — n=4573, R²=-0.4419

intercept: `-9.2481`  ·  log_price: True  ·  ilvl: `0.11409`  ·  n_mods: `-0.04389`  ·  n_top_tier: `0.72484`  ·  corrupted: `0.80271`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 7.24570 |
| `explicit.stat_2463230181@T1` | 1.99407 |
| `explicit.stat_2321178454@T2` | -1.15933 |
| `explicit.stat_681332047@T2` | -1.00365 |
| `explicit.stat_1573130764@T1` | -0.99429 |
| `explicit.stat_2194114101@T2` | -0.94010 |
| `explicit.stat_1573130764@T2` | -0.88269 |
| `explicit.stat_2463230181@T2` | 0.86452 |
| `explicit.stat_3261801346@T1` | -0.86331 |
| `explicit.stat_1368271171@T2` | -0.82069 |
| `explicit.stat_4067062424@T1` | -0.79561 |
| `explicit.stat_2321178454@T1` | -0.75962 |

### armour.shield — n=4006, R²=-0.5671

intercept: `-8.4293`  ·  log_price: True  ·  ilvl: `0.10910`  ·  n_mods: `-0.05303`  ·  n_top_tier: `0.61721`  ·  corrupted: `0.29208`  ·  n_sockets: `0.05328`  ·  quality: `0.05400`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.96376 |
| `explicit.stat_1011760251@T1` | -1.39564 |
| `explicit.stat_2339757871@T1` | -1.19615 |
| `explicit.stat_1011760251@T2` | -1.13803 |
| `explicit.stat_328541901@T1` | -0.91184 |
| `explicit.stat_2881298780@T1` | -0.88592 |
| `explicit.stat_2481353198@T1` | -0.87933 |
| `explicit.stat_2481353198@T2` | -0.86730 |
| `explicit.stat_328541901@T2` | -0.82953 |
| `explicit.stat_2923486259@T2` | -0.81654 |
| `explicit.stat_4095671657@T1` | -0.80657 |
| `explicit.stat_2881298780@T2` | -0.80586 |

### weapon.twomace — n=3666, R²=-0.4845

intercept: `-10.2478`  ·  log_price: True  ·  ilvl: `0.13452`  ·  n_mods: `-0.12474`  ·  n_top_tier: `0.31440`  ·  corrupted: `0.69835`  ·  n_sockets: `0.15324`  ·  quality: `0.04090`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.57339 |
| `desecrated.stat_1509134228@T1` | 2.43939 |
| `explicit.stat_1037193709@T1` | -1.40893 |
| `crafted.stat_3035140377` | 1.10081 |
| `explicit.stat_3336890334@T1` | -0.89680 |
| `explicit.stat_387439868@T2` | -0.87883 |
| `explicit.stat_210067635@T1` | 0.86475 |
| `explicit.stat_821021828@T2` | -0.75550 |
| `explicit.stat_1263695895@T1` | -0.70474 |
| `explicit.stat_2694482655@T1` | -0.62068 |
| `explicit.stat_3695891184@T1` | -0.60929 |
| `explicit.stat_3695891184@T2` | -0.58097 |

## Coverage (listings per base)

- … **Sapphire** — 20889 listings (20859 priced) [0.3–7553463.8 ex]
- … **Emerald** — 20650 listings (20622 priced) [0.3–7553463.8 ex]
- … **Ruby** — 15787 listings (15773 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 8794 listings (8785 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 7075 listings (7065 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 6923 listings (6910 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 6798 listings (6792 priced) [0.2–19945827.9 ex]
- … **Stellar Amulet** — 6518 listings (6514 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 6477 listings (6467 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 6324 listings (6313 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5478 listings (5463 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5300 listings (5294 priced) [0.2–307202867.9 ex]
- … **Ruby Ring** — 5095 listings (5093 priced) [0.2–37474957.5 ex]
- … **Topaz Ring** — 5089 listings (5085 priced) [0.3–307202867.9 ex]
- … **Plate Belt** — 4636 listings (4622 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4587 listings (4583 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4473 listings (4466 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4420 listings (4418 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4409 listings (4404 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4383 listings (4378 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4267 listings (4263 priced) [0.3–4275054.0 ex]
- … **Obliterator Bow** — 4202 listings (4190 priced) [0.3–42622633798.0 ex]
- … **Heavy Belt** — 4146 listings (4144 priced) [0.3–2608914286.6 ex]
- … **Pearl Ring** — 4098 listings (4094 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 4017 listings (4017 priced) [0.3–123132003.2 ex]

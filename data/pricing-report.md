# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-13T07:50:56+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **413690** (412929 priced in exalted)
- Distinct bases: 970 · distinct mods: 2967 · mod rows: 1965830
- Sold signals: **27876** sold · 222860 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-13T07:42:57+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×23.65** (median |log error| 3.1633)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.09** · typical error ×77.01 · ±30% 5% · n=59933
- Premium segment (60ex+): skill **+0.09** · typical error ×386.06 · ±30% 0% · n=38694

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 8109 | ×52.05 | 21% | +0.03 | +0.05 |
| accessory.amulet | 7509 | ×33.64 | 20% | +0.02 | +0.02 |
| jewel | 7285 | ×8.22 | 7% | +0.02 | +0.04 |
| accessory.belt | 5916 | ×30.60 | 15% | +0.08 | +0.11 |
| armour.chest | 5796 | ×16.51 | 25% | +0.04 | +0.06 |
| armour.helmet | 5693 | ×26.41 | 20% | +0.05 | +0.08 |
| armour.boots | 5238 | ×19.29 | 24% | +0.04 | +0.07 |
| armour.gloves | 5188 | ×40.54 | 23% | +0.03 | +0.06 |
| other | 4796 | ×2.63 | 41% | +0.09 | +0.16 |
| weapon.wand | 3403 | ×43.40 | 22% | +0.06 | +0.06 |
| weapon.bow | 2728 | ×30.62 | 18% | +0.08 | +0.09 |
| weapon.crossbow | 2605 | ×21.02 | 21% | +0.10 | +0.11 |
| weapon.warstaff | 1444 | ×77.81 | 17% | +0.08 | +0.08 |
| weapon.staff | 1327 | ×59.99 | 17% | +0.07 | +0.06 |
| weapon.sceptre | 1305 | ×79.77 | 13% | +0.07 | +0.09 |
| weapon.spear | 1149 | ×45.00 | 19% | +0.07 | +0.07 |
| armour.focus | 926 | ×33.28 | 14% | +0.13 | +0.15 |
| armour.quiver | 863 | ×34.81 | 16% | +0.05 | +0.10 |
| armour.shield | 730 | ×21.10 | 16% | +0.04 | +0.07 |
| weapon.twomace | 681 | ×24.93 | 13% | +0.06 | +0.08 |
| flask.charm | 618 | ×5.00 | 39% | +0.01 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=40970, R²=-0.6254

intercept: `1.6078`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `0.00732`  ·  n_top_tier: `0.33973`  ·  corrupted: `0.38308`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.56202 |
| `explicit.stat_2974417149@T1` | 0.50323 |
| `explicit.stat_2891184298@T1` | 0.34419 |
| `explicit.stat_2106365538@T1` | 0.33657 |
| `explicit.stat_789117908@T1` | -0.33102 |
| `explicit.stat_1050105434@T1` | -0.28449 |
| `explicit.stat_3917489142@T1` | 0.28246 |
| `explicit.stat_3299347043@T1` | -0.24520 |
| `implicit.stat_4041853756` | 0.22953 |
| `implicit.stat_3879011313` | 0.22952 |
| `implicit.stat_1379411836` | -0.17870 |
| `explicit.stat_1589917703@T1` | -0.17387 |

### jewel — n=39204, R²=-0.7093

intercept: `-1.3215`  ·  log_price: True  ·  ilvl: `0.03520`  ·  n_mods: `0.33284`  ·  n_top_tier: `-0.13082`  ·  corrupted: `0.14182`  ·  quality: `0.23109`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.58254 |
| `explicit.stat_3780644166@T1` | -3.42991 |
| `explicit.stat_3741323227@T1` | -2.71475 |
| `explicit.stat_234296660@T1` | -2.33965 |
| `explicit.stat_3485067555@T1` | 2.26242 |
| `explicit.stat_3714003708@T1` | -2.25100 |
| `explicit.stat_1569101201@T1` | 2.18821 |
| `explicit.stat_1315743832@T1` | 2.06844 |
| `explicit.stat_627767961@T1` | -2.03114 |
| `explicit.stat_153777645@T1` | -2.02278 |
| `explicit.stat_2527686725@T1` | 1.94449 |
| `explicit.stat_795138349@T1` | -1.92222 |

### accessory.ring — n=36911, R²=-1.9349

intercept: `3.9929`  ·  log_price: True  ·  ilvl: `-0.04903`  ·  n_mods: `0.00407`  ·  n_top_tier: `0.34224`  ·  corrupted: `0.44282`  ·  n_sockets: `-0.14695`  ·  quality: `0.01426`

| stat_id | coef |
|---|---|
| `explicit.stat_1671376347@T1` | 0.85578 |
| `explicit.stat_1263695895@T1` | -0.40698 |
| `explicit.stat_1368271171@T1` | -0.39610 |
| `explicit.stat_3291658075@T2` | -0.39140 |
| `explicit.stat_3325883026@T1` | -0.38890 |
| `explicit.stat_1368271171@T2` | -0.38432 |
| `explicit.stat_2231156303@T1` | -0.37953 |
| `explicit.stat_1050105434@T2` | -0.36928 |
| `explicit.stat_4220027924@T2` | -0.36606 |
| `explicit.stat_1263695895@T2` | -0.36513 |
| `explicit.stat_1573130764@T1` | -0.36495 |
| `explicit.stat_3917489142@T2` | -0.36450 |

### accessory.amulet — n=34470, R²=-2.0977

intercept: `4.0640`  ·  log_price: True  ·  ilvl: `-0.04893`  ·  n_mods: `-0.02819`  ·  n_top_tier: `0.71061`  ·  corrupted: `0.07266`  ·  n_sockets: `-0.14711`  ·  quality: `-0.00004`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.42178 |
| `explicit.stat_983749596@T2` | -1.19517 |
| `explicit.stat_124131830` | 0.89250 |
| `explicit.stat_3556824919@T1` | 0.83079 |
| `explicit.stat_3981240776@T2` | 0.82187 |
| `explicit.stat_2748665614@T2` | -0.81575 |
| `explicit.stat_124131830@T2` | -0.80420 |
| `explicit.stat_2748665614@T1` | -0.80246 |
| `explicit.stat_472520716@T1` | -0.79973 |
| `explicit.stat_3917489142@T2` | -0.77212 |
| `explicit.stat_3917489142@T1` | -0.77025 |
| `explicit.stat_2901986750@T1` | -0.76765 |

### accessory.belt — n=27162, R²=-1.3237

intercept: `4.7862`  ·  log_price: True  ·  ilvl: `-0.05445`  ·  n_mods: `-0.07961`  ·  n_top_tier: `0.69791`  ·  corrupted: `1.30107`  ·  n_sockets: `0.61724`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -0.87753 |
| `explicit.stat_51994685@T1` | -0.82768 |
| `explicit.stat_1389754388@T1` | -0.81085 |
| `explicit.stat_3299347043@T2` | -0.79680 |
| `explicit.stat_809229260@T2` | -0.78934 |
| `explicit.stat_2881298780@T1` | -0.77249 |
| `explicit.stat_3325883026@T1` | -0.75898 |
| `explicit.stat_1671376347@T2` | -0.74083 |
| `explicit.stat_4220027924@T2` | -0.72564 |
| `explicit.stat_1389754388@T2` | -0.71081 |
| `explicit.stat_1050105434@T1` | -0.69827 |
| `explicit.stat_3585532255@T2` | -0.69806 |

### armour.chest — n=26866, R²=-1.7117

intercept: `3.3493`  ·  log_price: True  ·  ilvl: `-0.04135`  ·  n_mods: `-0.01178`  ·  n_top_tier: `0.17980`  ·  corrupted: `0.05095`  ·  n_sockets: `0.01041`  ·  quality: `0.02195`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.30125 |
| `explicit.stat_3981240776@T1` | 1.37574 |
| `explicit.stat_4080418644@T2` | -0.22066 |
| `explicit.stat_4080418644@T1` | -0.21569 |
| `explicit.stat_915769802@T1` | -0.21413 |
| `explicit.stat_4015621042@T1` | -0.21376 |
| `explicit.stat_3325883026@T2` | -0.19614 |
| `explicit.stat_915769802@T2` | -0.19566 |
| `explicit.stat_4015621042@T2` | -0.19355 |
| `explicit.stat_986397080@T2` | -0.19210 |
| `explicit.stat_3261801346@T2` | -0.19071 |
| `explicit.stat_2451402625@T2` | -0.18855 |

### armour.helmet — n=26225, R²=-1.6373

intercept: `3.9071`  ·  log_price: True  ·  ilvl: `-0.04887`  ·  n_mods: `-0.01789`  ·  n_top_tier: `0.48355`  ·  corrupted: `0.52905`  ·  n_sockets: `0.01790`  ·  quality: `0.05365`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 4.80088 |
| `explicit.stat_2339757871@T1` | -2.28929 |
| `explicit.stat_1263695895@T1` | -0.70206 |
| `explicit.stat_53045048@T1` | -0.61958 |
| `explicit.stat_1263695895@T2` | -0.57912 |
| `explicit.stat_2162097452@T2` | -0.57734 |
| `explicit.stat_53045048@T2` | -0.54481 |
| `explicit.stat_587431675@T2` | -0.54178 |
| `explicit.stat_3917489142@T2` | -0.53451 |
| `explicit.stat_587431675@T1` | -0.52689 |
| `explicit.stat_1999113824@T1` | -0.52671 |
| `explicit.stat_803737631@T2` | -0.52423 |

### armour.boots — n=24633, R²=-1.7024

intercept: `3.4354`  ·  log_price: True  ·  ilvl: `-0.04235`  ·  n_mods: `-0.00845`  ·  n_top_tier: `0.58631`  ·  corrupted: `-0.01255`  ·  n_sockets: `0.00081`  ·  quality: `0.01758`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.34327 |
| `desecrated.stat_2250533757@T2` | -0.77283 |
| `crafted.stat_3917489142@T1` | -0.66323 |
| `explicit.stat_3917489142@T2` | -0.66227 |
| `explicit.stat_3362812763@T1` | -0.63042 |
| `explicit.stat_1062208444@T2` | -0.62129 |
| `explicit.stat_3917489142@T1` | -0.62013 |
| `explicit.stat_3362812763@T2` | -0.61216 |
| `explicit.stat_2923486259@T2` | -0.61197 |
| `explicit.stat_2160282525@T1` | -0.61182 |
| `explicit.stat_2160282525@T2` | -0.60693 |
| `explicit.stat_53045048@T1` | -0.60675 |

### armour.gloves — n=23987, R²=-1.9163

intercept: `3.7902`  ·  log_price: True  ·  ilvl: `-0.04755`  ·  n_mods: `-0.01152`  ·  n_top_tier: `0.41801`  ·  corrupted: `-0.01247`  ·  n_sockets: `0.02475`  ·  quality: `0.02456`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T1` | 0.77718 |
| `rune.stat_201332984` | 0.74380 |
| `explicit.stat_9187492@T2` | -0.71862 |
| `explicit.stat_3484657501@T2` | -0.55136 |
| `explicit.stat_3917489142@T2` | -0.50221 |
| `explicit.stat_803737631@T2` | -0.49807 |
| `explicit.stat_3484657501@T1` | -0.47550 |
| `explicit.stat_681332047@T1` | -0.47319 |
| `explicit.stat_1671376347@T1` | 0.47009 |
| `explicit.stat_2923486259@T2` | -0.45786 |
| `explicit.stat_681332047@T2` | -0.45562 |
| `explicit.stat_3917489142@T1` | -0.45114 |

### weapon.wand — n=15840, R²=-2.2644

intercept: `3.8879`  ·  log_price: True  ·  ilvl: `-0.04831`  ·  n_mods: `-0.00976`  ·  n_top_tier: `0.22256`  ·  corrupted: `-0.05447`  ·  n_sockets: `0.03910`  ·  quality: `0.00413`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 3.32579 |
| `rune.stat_124131830` | -3.21604 |
| `explicit.stat_1545858329@T1` | 2.46737 |
| `explicit.stat_591105508@T1` | 2.14745 |
| `explicit.stat_4226189338@T1` | 2.08480 |
| `explicit.stat_1600707273@T1` | 1.88460 |
| `explicit.stat_736967255@T2` | 1.61408 |
| `explicit.stat_124131830@T1` | 1.35857 |
| `crafted.stat_124131830` | 1.13877 |
| `explicit.stat_737908626@T1` | -0.27157 |
| `explicit.stat_3962278098@T2` | -0.25574 |
| `explicit.stat_473429811@T2` | -0.24943 |

### weapon.bow — n=12932, R²=-1.9854

intercept: `3.5173`  ·  log_price: True  ·  ilvl: `-0.04300`  ·  n_mods: `-0.02350`  ·  n_top_tier: `0.69964`  ·  corrupted: `-0.06380`  ·  n_sockets: `-0.00745`  ·  quality: `0.03183`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.97957 |
| `desecrated.stat_666077204@T1` | 1.84579 |
| `explicit.stat_1202301673@T1` | 1.45857 |
| `crafted.stat_3035140377` | 1.37679 |
| `explicit.stat_2463230181@T1` | 0.84927 |
| `explicit.stat_1263695895@T1` | -0.78251 |
| `explicit.stat_669069897@T1` | -0.75660 |
| `explicit.stat_55876295@T1` | -0.75619 |
| `explicit.stat_1037193709@T2` | -0.75309 |
| `explicit.stat_1037193709@T1` | -0.74724 |
| `explicit.stat_3695891184@T1` | -0.74124 |
| `explicit.stat_3336890334@T2` | -0.73948 |

### weapon.crossbow — n=12235, R²=-1.9602

intercept: `3.6323`  ·  log_price: True  ·  ilvl: `-0.04485`  ·  n_mods: `-0.00734`  ·  n_top_tier: `0.70528`  ·  corrupted: `-0.03363`  ·  n_sockets: `0.01742`  ·  quality: `0.00121`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -2.00838 |
| `explicit.stat_1980802737@T2` | -1.94922 |
| `explicit.stat_709508406@T1` | 1.51188 |
| `explicit.stat_1202301673@T1` | 1.50804 |
| `explicit.stat_2250681686` | 1.34614 |
| `explicit.stat_1980802737` | 1.19206 |
| `crafted.stat_3035140377` | 0.86344 |
| `explicit.stat_1263695895@T2` | -0.85736 |
| `explicit.stat_1263695895@T1` | -0.82938 |
| `explicit.stat_1202301673@T2` | -0.78588 |
| `rune.stat_669069897` | -0.77729 |
| `explicit.stat_1509134228@T2` | -0.74002 |

### flask.charm — n=9861, R²=-0.4527

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00044`  ·  corrupted: `1.15548`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.70661 |
| `explicit.stat_1056492907` | 3.40119 |
| `explicit.stat_2676834156@T1` | 1.60897 |
| `explicit.stat_2541588185@T1` | 0.46335 |
| `explicit.stat_2678930256` | 0.03212 |
| `explicit.stat_3138344128` | 0.02038 |
| `explicit.stat_39209842` | 0.00052 |
| `explicit.stat_828533480@T2` | -0.00045 |
| `explicit.stat_1366840608@T2` | -0.00044 |
| `explicit.stat_1873752457@T2` | -0.00044 |
| `explicit.stat_1873752457@T1` | -0.00044 |
| `explicit.stat_2676834156@T2` | -0.00044 |

### weapon.warstaff — n=6842, R²=-0.6136

intercept: `-0.6408`  ·  log_price: True  ·  ilvl: `0.00877`  ·  n_mods: `-0.02506`  ·  n_top_tier: `0.27170`  ·  corrupted: `0.05922`  ·  n_sockets: `0.01664`  ·  quality: `0.06243`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.45559 |
| `explicit.stat_9187492@T1` | 1.06275 |
| `rune.stat_731403740` | 0.76094 |
| `explicit.stat_1509134228@T2` | 0.54661 |
| `crafted.stat_3035140377` | 0.51759 |
| `desecrated.stat_9187492` | 0.51475 |
| `rune.stat_1712188793` | -0.33410 |
| `explicit.stat_1037193709@T1` | 0.33266 |
| `explicit.stat_328541901@T2` | -0.32491 |
| `explicit.stat_328541901@T1` | -0.32036 |
| `explicit.stat_3336890334@T2` | -0.29834 |
| `explicit.stat_1368271171@T1` | -0.28894 |

### weapon.sceptre — n=6348, R²=-0.5535

intercept: `-7.7319`  ·  log_price: True  ·  ilvl: `0.09666`  ·  n_mods: `-0.00370`  ·  n_top_tier: `0.39300`  ·  corrupted: `0.32149`  ·  n_sockets: `0.19660`  ·  quality: `0.09292`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.55195 |
| `explicit.stat_2162097452@T2` | 1.26004 |
| `explicit.stat_4080418644@T1` | -0.75523 |
| `explicit.stat_4080418644@T2` | -0.60880 |
| `explicit.stat_1263695895@T1` | -0.60125 |
| `explicit.stat_1263695895@T2` | -0.59326 |
| `explicit.stat_2347036682@T2` | -0.52200 |
| `explicit.stat_1574590649@T2` | -0.50250 |
| `explicit.stat_2854751904@T1` | -0.48535 |
| `explicit.stat_3639275092@T2` | -0.42860 |
| `explicit.stat_1574590649@T1` | -0.41172 |
| `explicit.stat_1050105434@T2` | -0.40866 |

### weapon.staff — n=6317, R²=-0.6745

intercept: `-0.7156`  ·  log_price: True  ·  ilvl: `0.00895`  ·  n_mods: `-0.00310`  ·  n_top_tier: `0.45171`  ·  corrupted: `0.06449`  ·  n_sockets: `0.04270`  ·  quality: `0.06211`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 2.62409 |
| `explicit.stat_4226189338@T1` | 1.84558 |
| `explicit.stat_1600707273@T1` | 1.74036 |
| `explicit.stat_1545858329@T1` | 1.69398 |
| `explicit.stat_2254480358@T1` | 1.57731 |
| `explicit.stat_2768835289@T2` | 1.09899 |
| `explicit.stat_124131830@T1` | 1.07997 |
| `explicit.stat_2254480358@T2` | 0.98550 |
| `crafted.stat_124131830` | 0.50665 |
| `explicit.stat_2974417149@T1` | -0.47869 |
| `explicit.stat_591105508@T1` | -0.47035 |
| `explicit.stat_293638271@T2` | -0.46646 |

### weapon.spear — n=5403, R²=-0.6825

intercept: `-0.2645`  ·  log_price: True  ·  ilvl: `0.00350`  ·  n_mods: `-0.00208`  ·  n_top_tier: `0.13013`  ·  corrupted: `-0.00971`  ·  n_sockets: `0.00667`  ·  quality: `0.10556`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.56679 |
| `explicit.stat_9187492@T1` | 2.54174 |
| `crafted.stat_210067635@T2` | -1.72074 |
| `crafted.stat_3035140377` | 1.41691 |
| `crafted.stat_518292764` | 0.69002 |
| `explicit.stat_1509134228@T1` | 0.65696 |
| `explicit.stat_210067635@T1` | 0.56251 |
| `explicit.stat_1037193709@T1` | 0.53388 |
| `rune.stat_3336890334` | 0.33746 |
| `explicit.stat_210067635@T2` | 0.31962 |
| `explicit.stat_709508406@T1` | 0.27985 |
| `crafted.stat_210067635` | 0.24024 |

### armour.focus — n=4414, R²=-0.5317

intercept: `-6.1212`  ·  log_price: True  ·  ilvl: `0.07557`  ·  n_mods: `-0.00501`  ·  n_top_tier: `0.90259`  ·  corrupted: `0.71386`  ·  n_sockets: `0.28063`  ·  quality: `0.07081`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 6.26157 |
| `crafted.stat_2974417149@T1` | 1.21175 |
| `explicit.stat_4220027924@T1` | -1.16300 |
| `explicit.stat_4220027924@T2` | -1.12638 |
| `explicit.stat_736967255@T2` | -1.04927 |
| `explicit.stat_2923486259@T1` | -1.03410 |
| `explicit.stat_2891184298@T1` | -0.99367 |
| `explicit.stat_2891184298@T2` | -0.96133 |
| `explicit.stat_3962278098@T2` | -0.94924 |
| `explicit.stat_1671376347@T1` | 0.92963 |
| `explicit.stat_124131830@T2` | -0.92340 |
| `explicit.stat_3291658075@T1` | -0.91387 |

### armour.quiver — n=4128, R²=-0.5346

intercept: `-5.9967`  ·  log_price: True  ·  ilvl: `0.07087`  ·  n_mods: `-0.00742`  ·  n_top_tier: `0.95380`  ·  corrupted: `0.18992`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 8.74287 |
| `explicit.stat_681332047@T2` | -1.20862 |
| `explicit.stat_2194114101@T2` | -1.16306 |
| `explicit.stat_1573130764@T1` | -1.14192 |
| `explicit.stat_2321178454@T2` | -1.13968 |
| `explicit.stat_1368271171@T2` | -1.08280 |
| `explicit.stat_1573130764@T2` | -1.03951 |
| `explicit.stat_3261801346@T1` | -0.99751 |
| `explicit.stat_2321178454@T1` | -0.98340 |
| `explicit.stat_3714003708@T2` | -0.95224 |
| `explicit.stat_4067062424@T1` | -0.94591 |
| `explicit.stat_4067062424@T2` | -0.93628 |

### armour.shield — n=3625, R²=-0.599

intercept: `-4.7386`  ·  log_price: True  ·  ilvl: `0.05925`  ·  n_mods: `-0.00291`  ·  n_top_tier: `0.54069`  ·  corrupted: `0.22938`  ·  n_sockets: `-0.00020`  ·  quality: `0.05295`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.15457 |
| `explicit.stat_328541901@T1` | -1.05637 |
| `explicit.stat_1011760251@T1` | -0.97022 |
| `explicit.stat_1011760251@T2` | -0.87615 |
| `explicit.stat_2481353198@T1` | -0.85854 |
| `explicit.stat_328541901@T2` | -0.85753 |
| `explicit.stat_2481353198@T2` | -0.83994 |
| `explicit.stat_1978899297@T1` | 0.81570 |
| `explicit.stat_1978899297@T2` | -0.74833 |
| `explicit.stat_3362812763@T1` | -0.74548 |
| `explicit.stat_2901986750@T1` | -0.71675 |
| `explicit.stat_53045048@T2` | -0.67458 |

### weapon.twomace — n=3280, R²=-0.5072

intercept: `-6.9198`  ·  log_price: True  ·  ilvl: `0.08930`  ·  n_mods: `-0.06503`  ·  n_top_tier: `0.40530`  ·  corrupted: `0.90441`  ·  n_sockets: `0.13453`  ·  quality: `0.03927`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.29359 |
| `desecrated.stat_1509134228@T1` | 1.86146 |
| `explicit.stat_1037193709@T1` | -1.06966 |
| `crafted.stat_3035140377` | 1.03799 |
| `explicit.stat_210067635@T1` | 0.98383 |
| `explicit.stat_3336890334@T1` | -0.74147 |
| `explicit.stat_1037193709@T2` | -0.72120 |
| `explicit.stat_387439868@T2` | -0.67905 |
| `explicit.stat_821021828@T2` | -0.61173 |
| `explicit.stat_1263695895@T2` | -0.58856 |
| `explicit.stat_3695891184@T1` | -0.57898 |
| `explicit.stat_691932474@T1` | -0.57516 |

## Coverage (listings per base)

- … **Sapphire** — 18438 listings (18413 priced) [0.3–7553463.8 ex]
- … **Emerald** — 18191 listings (18171 priced) [0.3–7553463.8 ex]
- … **Ruby** — 14024 listings (14012 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 8010 listings (8001 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 6367 listings (6360 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 6196 listings (6184 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 6126 listings (6122 priced) [0.2–19945827.9 ex]
- … **Stellar Amulet** — 5911 listings (5908 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 5854 listings (5844 priced) [0.3–27924159.0 ex]
- … **Gold Ring** — 5713 listings (5707 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 5009 listings (4997 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4752 listings (4747 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 4613 listings (4610 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 4603 listings (4601 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 4195 listings (4189 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4125 listings (4121 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4069 listings (4062 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4007 listings (4005 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3997 listings (3993 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 3931 listings (3929 priced) [0.2–24532814.5 ex]
- … **Obliterator Bow** — 3868 listings (3857 priced) [0.3–42622633798.0 ex]
- … **Bloodstone Amulet** — 3835 listings (3831 priced) [0.3–4275054.0 ex]
- … **Heavy Belt** — 3798 listings (3796 priced) [0.3–2608914286.6 ex]
- … **Pearl Ring** — 3700 listings (3697 priced) [0.2–275252424.7 ex]
- … **Lunar Amulet** — 3637 listings (3633 priced) [0.3–4877938.3 ex]

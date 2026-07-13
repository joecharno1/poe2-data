# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-13T13:50:43+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **425572** (424750 priced in exalted)
- Distinct bases: 971 · distinct mods: 2989 · mod rows: 2022949
- Sold signals: **27592** sold · 230852 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-13T13:40:21+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×23.79** (median |log error| 3.1693)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.07** · typical error ×57.11 · ±30% 5% · n=61738
- Premium segment (60ex+): skill **+0.08** · typical error ×216.48 · ±30% 0% · n=40306

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 8281 | ×53.42 | 21% | +0.03 | +0.04 |
| accessory.amulet | 7761 | ×52.00 | 20% | +0.03 | +0.03 |
| jewel | 7595 | ×8.41 | 7% | +0.02 | +0.05 |
| accessory.belt | 6100 | ×18.21 | 3% | +0.01 | +0.03 |
| armour.chest | 5935 | ×18.12 | 7% | +0.08 | +0.11 |
| armour.helmet | 5851 | ×18.66 | 5% | +0.01 | +0.05 |
| armour.boots | 5464 | ×24.03 | 8% | +0.09 | +0.12 |
| armour.gloves | 5287 | ×20.56 | 5% | +0.04 | +0.06 |
| other | 4802 | ×6.57 | 40% | +0.08 | +0.15 |
| weapon.wand | 3450 | ×38.83 | 19% | +0.06 | +0.07 |
| weapon.bow | 2823 | ×27.85 | 17% | +0.09 | +0.10 |
| weapon.crossbow | 2658 | ×21.45 | 20% | +0.10 | +0.13 |
| weapon.warstaff | 1507 | ×76.26 | 17% | +0.07 | +0.08 |
| weapon.sceptre | 1400 | ×74.98 | 15% | +0.08 | +0.09 |
| weapon.staff | 1332 | ×50.87 | 18% | +0.06 | +0.07 |
| weapon.spear | 1180 | ×49.99 | 17% | +0.07 | +0.08 |
| armour.focus | 974 | ×33.31 | 15% | +0.13 | +0.15 |
| armour.quiver | 913 | ×30.27 | 15% | +0.05 | +0.11 |
| armour.shield | 779 | ×11.77 | 16% | +0.04 | +0.07 |
| weapon.twomace | 700 | ×29.45 | 14% | +0.06 | +0.08 |
| flask.charm | 645 | ×10.00 | 35% | +0.01 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=42013, R²=-0.6161

intercept: `1.6052`  ·  log_price: True  ·  ilvl: `0.00005`  ·  n_mods: `0.01144`  ·  n_top_tier: `0.35528`  ·  corrupted: `0.40805`  ·  n_sockets: `-0.00007`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.64414 |
| `explicit.stat_2974417149@T1` | 0.49149 |
| `explicit.stat_789117908@T1` | -0.36116 |
| `explicit.stat_2891184298@T1` | 0.32651 |
| `explicit.stat_2106365538@T1` | 0.30345 |
| `explicit.stat_3917489142@T1` | 0.30100 |
| `explicit.stat_1050105434@T1` | -0.29724 |
| `explicit.stat_101878827@T1` | 0.27230 |
| `explicit.stat_3299347043@T1` | -0.25269 |
| `implicit.stat_4041853756` | 0.22911 |
| `implicit.stat_3879011313` | 0.22911 |
| `explicit.stat_3141070085@T1` | -0.21352 |

### jewel — n=40619, R²=-0.7444

intercept: `-1.3196`  ·  log_price: True  ·  ilvl: `0.03278`  ·  n_mods: `0.39683`  ·  n_top_tier: `-0.14687`  ·  corrupted: `0.17173`  ·  quality: `0.23635`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.91619 |
| `explicit.stat_3780644166@T1` | -3.29754 |
| `explicit.stat_3741323227@T1` | -2.80407 |
| `explicit.stat_3714003708@T1` | -2.27459 |
| `explicit.stat_153777645@T1` | -2.18446 |
| `explicit.stat_21071013@T1` | 2.17615 |
| `explicit.stat_1569101201@T1` | 2.11722 |
| `explicit.stat_795138349@T1` | -2.10305 |
| `explicit.stat_234296660@T1` | -2.00863 |
| `explicit.stat_1423639565@T1` | -2.00011 |
| `explicit.stat_3174700878@T1` | 1.98175 |
| `explicit.stat_627767961@T1` | -1.92060 |

### accessory.ring — n=38066, R²=-1.9383

intercept: `3.8833`  ·  log_price: True  ·  ilvl: `-0.04758`  ·  n_mods: `0.00358`  ·  n_top_tier: `0.40424`  ·  corrupted: `0.22558`  ·  n_sockets: `-0.14194`  ·  quality: `0.01143`

| stat_id | coef |
|---|---|
| `explicit.stat_1671376347@T1` | 0.59748 |
| `explicit.stat_2231156303@T1` | -0.44843 |
| `explicit.stat_3291658075@T2` | -0.44555 |
| `explicit.stat_1368271171@T1` | -0.43864 |
| `explicit.stat_1368271171@T2` | -0.43800 |
| `explicit.stat_3917489142@T2` | -0.43431 |
| `explicit.stat_1263695895@T1` | -0.43290 |
| `explicit.stat_3032590688@T2` | -0.43283 |
| `explicit.stat_3325883026@T1` | -0.43203 |
| `explicit.stat_4220027924@T2` | -0.43069 |
| `explicit.stat_3962278098@T2` | -0.42686 |
| `explicit.stat_1263695895@T2` | -0.42616 |

### accessory.amulet — n=35545, R²=-2.1054

intercept: `3.8976`  ·  log_price: True  ·  ilvl: `-0.04701`  ·  n_mods: `-0.02126`  ·  n_top_tier: `0.87077`  ·  corrupted: `0.06497`  ·  n_sockets: `-0.15462`  ·  quality: `0.00112`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.50678 |
| `explicit.stat_983749596@T2` | -1.29245 |
| `explicit.stat_124131830@T2` | -1.22200 |
| `explicit.stat_2748665614@T1` | -0.97718 |
| `explicit.stat_2748665614@T2` | -0.97173 |
| `explicit.stat_124131830` | 0.96739 |
| `explicit.stat_3299347043@T2` | -0.95836 |
| `explicit.stat_1050105434@T2` | -0.91924 |
| `explicit.stat_3917489142@T2` | -0.91886 |
| `explicit.stat_2901986750@T1` | -0.91380 |
| `explicit.stat_1671376347@T2` | -0.91320 |
| `explicit.stat_4220027924@T2` | -0.91200 |

### accessory.belt — n=27929, R²=-0.5828

intercept: `6.7463`  ·  log_price: True  ·  ilvl: `-0.05100`  ·  n_mods: `-0.48318`  ·  n_top_tier: `0.87376`  ·  corrupted: `1.10667`  ·  n_sockets: `0.27138`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.55866 |
| `explicit.stat_2881298780@T1` | -1.25531 |
| `explicit.stat_1389754388@T2` | -1.19839 |
| `explicit.stat_51994685@T1` | -1.19452 |
| `explicit.stat_809229260@T2` | -1.18352 |
| `explicit.stat_3585532255@T2` | -1.12050 |
| `explicit.stat_3299347043@T1` | -1.11696 |
| `explicit.stat_3299347043@T2` | -1.10568 |
| `explicit.stat_1671376347@T2` | -1.06943 |
| `explicit.stat_3325883026@T1` | -1.04461 |
| `explicit.stat_1050105434@T1` | -1.00116 |
| `explicit.stat_644456512@T1` | -0.98110 |

### armour.chest — n=27635, R²=-1.0706

intercept: `4.3545`  ·  log_price: True  ·  ilvl: `-0.05172`  ·  n_mods: `-0.09345`  ·  n_top_tier: `0.42606`  ·  corrupted: `0.35921`  ·  n_sockets: `0.09642`  ·  quality: `0.02649`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.15224 |
| `explicit.stat_3981240776@T1` | 0.90360 |
| `explicit.stat_4080418644@T1` | -0.68959 |
| `explicit.stat_124859000@T2` | -0.63882 |
| `explicit.stat_4080418644@T2` | -0.60237 |
| `explicit.stat_915769802@T1` | -0.59417 |
| `explicit.stat_915769802@T2` | -0.58793 |
| `explicit.stat_3321629045@T1` | -0.56047 |
| `explicit.stat_3484657501@T1` | -0.52665 |
| `explicit.stat_2881298780@T2` | -0.52306 |
| `explicit.stat_986397080@T2` | -0.52084 |
| `explicit.stat_3261801346@T2` | -0.50927 |

### armour.helmet — n=26971, R²=-0.7576

intercept: `3.9926`  ·  log_price: True  ·  ilvl: `-0.04892`  ·  n_mods: `-0.10397`  ·  n_top_tier: `0.48061`  ·  corrupted: `0.72915`  ·  n_sockets: `0.11995`  ·  quality: `0.03351`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.38460 |
| `explicit.stat_2339757871@T1` | -1.04301 |
| `explicit.stat_1263695895@T1` | -0.99324 |
| `explicit.stat_53045048@T2` | -0.95804 |
| `explicit.stat_1263695895@T2` | -0.87828 |
| `explicit.stat_53045048@T1` | -0.83201 |
| `explicit.stat_1999113824@T1` | -0.80194 |
| `explicit.stat_3261801346@T1` | -0.71072 |
| `explicit.stat_3917489142@T2` | -0.69524 |
| `explicit.stat_2162097452@T2` | -0.64574 |
| `explicit.stat_328541901@T2` | -0.64260 |
| `explicit.stat_4080418644@T2` | -0.58874 |

### armour.boots — n=25272, R²=-1.1398

intercept: `4.5275`  ·  log_price: True  ·  ilvl: `-0.05328`  ·  n_mods: `-0.09121`  ·  n_top_tier: `0.67852`  ·  corrupted: `0.21980`  ·  n_sockets: `0.03178`  ·  quality: `0.02056`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -1.89889 |
| `explicit.stat_2250533757@T1` | 1.37446 |
| `explicit.stat_3917489142@T2` | -1.09329 |
| `explicit.stat_2923486259@T2` | -1.01879 |
| `explicit.stat_3917489142@T1` | -0.93102 |
| `explicit.stat_1062208444@T2` | -0.92416 |
| `explicit.stat_53045048@T1` | -0.89910 |
| `explicit.stat_1999113824@T2` | -0.87668 |
| `explicit.stat_3362812763@T1` | -0.85670 |
| `explicit.stat_2160282525@T1` | -0.85032 |
| `desecrated.stat_2250533757@T2` | -0.84343 |
| `explicit.stat_1999113824@T1` | -0.83057 |

### armour.gloves — n=24627, R²=-0.8881

intercept: `3.8038`  ·  log_price: True  ·  ilvl: `-0.04862`  ·  n_mods: `-0.11706`  ·  n_top_tier: `0.42304`  ·  corrupted: `0.27848`  ·  n_sockets: `0.29337`  ·  quality: `0.02434`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.94440 |
| `explicit.stat_3484657501@T2` | -1.41898 |
| `explicit.stat_803737631@T2` | -1.07525 |
| `explicit.stat_3484657501@T1` | -0.93686 |
| `explicit.stat_3917489142@T2` | -0.88823 |
| `explicit.stat_1573130764@T1` | -0.74039 |
| `explicit.stat_3321629045@T2` | -0.72297 |
| `explicit.stat_3321629045@T1` | -0.72197 |
| `rune.stat_201332984` | 0.71660 |
| `explicit.stat_681332047@T2` | -0.71226 |
| `explicit.stat_2451402625@T2` | -0.71161 |
| `explicit.stat_3917489142@T1` | -0.70473 |

### weapon.wand — n=16181, R²=-2.2172

intercept: `3.9341`  ·  log_price: True  ·  ilvl: `-0.04881`  ·  n_mods: `-0.01849`  ·  n_top_tier: `0.33543`  ·  corrupted: `-0.04364`  ·  n_sockets: `0.04005`  ·  quality: `0.00191`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 3.15941 |
| `rune.stat_124131830` | -3.05665 |
| `explicit.stat_1545858329@T1` | 2.84218 |
| `explicit.stat_591105508@T1` | 2.04988 |
| `explicit.stat_4226189338@T1` | 1.99239 |
| `explicit.stat_124131830@T1` | 1.49642 |
| `crafted.stat_124131830` | 1.25802 |
| `explicit.stat_736967255@T2` | 1.18213 |
| `explicit.stat_2768835289@T2` | 0.87433 |
| `explicit.stat_737908626@T1` | -0.39114 |
| `explicit.stat_3278136794@T2` | -0.38841 |
| `explicit.stat_2231156303@T2` | -0.37672 |

### weapon.bow — n=13210, R²=-1.9819

intercept: `3.4909`  ·  log_price: True  ·  ilvl: `-0.04260`  ·  n_mods: `-0.02696`  ·  n_top_tier: `0.57049`  ·  corrupted: `-0.04599`  ·  n_sockets: `-0.00645`  ·  quality: `0.03561`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.94142 |
| `explicit.stat_1202301673@T1` | 1.59344 |
| `crafted.stat_3035140377` | 1.38876 |
| `explicit.stat_2463230181@T1` | 1.13180 |
| `explicit.stat_1263695895@T1` | -0.65853 |
| `explicit.stat_55876295@T1` | -0.63248 |
| `explicit.stat_669069897@T1` | -0.62582 |
| `explicit.stat_3336890334@T2` | -0.62141 |
| `explicit.stat_821021828@T2` | -0.61576 |
| `explicit.stat_2694482655@T2` | -0.61385 |
| `explicit.stat_1368271171@T2` | -0.60875 |
| `explicit.stat_3695891184@T1` | -0.60747 |

### weapon.crossbow — n=12461, R²=-1.8968

intercept: `3.5979`  ·  log_price: True  ·  ilvl: `-0.04430`  ·  n_mods: `-0.01779`  ·  n_top_tier: `0.71798`  ·  corrupted: `-0.02381`  ·  n_sockets: `0.04019`  ·  quality: `0.00527`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.92172 |
| `explicit.stat_2250681686@T2` | -1.47764 |
| `explicit.stat_709508406@T1` | 1.39795 |
| `explicit.stat_1202301673@T1` | 1.23770 |
| `explicit.stat_1980802737` | 1.14818 |
| `explicit.stat_1202301673@T2` | -0.96452 |
| `crafted.stat_3035140377` | 0.90485 |
| `explicit.stat_1263695895@T2` | -0.89566 |
| `explicit.stat_1509134228@T1` | 0.86992 |
| `explicit.stat_2250681686` | 0.81587 |
| `explicit.stat_1263695895@T1` | -0.80074 |
| `explicit.stat_1509134228@T2` | -0.78841 |

### flask.charm — n=10246, R²=-0.4654

intercept: `0.0001`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.69673`  ·  corrupted: `1.72862`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60517 |
| `explicit.stat_1056492907` | 3.27082 |
| `explicit.stat_2676834156@T1` | 0.91636 |
| `explicit.stat_828533480@T2` | -0.69674 |
| `explicit.stat_1873752457@T1` | -0.69672 |
| `explicit.stat_1120862500@T2` | -0.69672 |
| `explicit.stat_3196823591@T2` | -0.69672 |
| `explicit.stat_1873752457@T2` | -0.69672 |
| `explicit.stat_1366840608@T2` | -0.69672 |
| `explicit.stat_2676834156@T2` | -0.69672 |
| `explicit.stat_828533480@T1` | -0.69671 |
| `explicit.stat_388617051@T2` | -0.69671 |

### weapon.warstaff — n=7031, R²=-0.5961

intercept: `-1.2425`  ·  log_price: True  ·  ilvl: `0.01685`  ·  n_mods: `-0.04514`  ·  n_top_tier: `0.39584`  ·  corrupted: `0.16702`  ·  n_sockets: `0.03105`  ·  quality: `0.05615`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.39435 |
| `explicit.stat_9187492@T1` | 0.92551 |
| `rune.stat_731403740` | 0.81147 |
| `crafted.stat_3035140377` | 0.49913 |
| `explicit.stat_328541901@T1` | -0.47765 |
| `explicit.stat_328541901@T2` | -0.46643 |
| `explicit.stat_3336890334@T2` | -0.44169 |
| `desecrated.stat_9187492` | 0.43169 |
| `explicit.stat_821021828@T1` | -0.42671 |
| `explicit.stat_1940865751@T1` | -0.42628 |
| `explicit.stat_1263695895@T1` | -0.42602 |
| `explicit.stat_1368271171@T1` | -0.42202 |

### weapon.sceptre — n=6549, R²=-0.5184

intercept: `-9.7097`  ·  log_price: True  ·  ilvl: `0.12137`  ·  n_mods: `-0.01060`  ·  n_top_tier: `0.22958`  ·  corrupted: `0.36232`  ·  n_sockets: `0.12989`  ·  quality: `0.08640`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.61579 |
| `explicit.stat_2162097452@T2` | 1.52317 |
| `explicit.stat_1798257884@T2` | 0.80118 |
| `explicit.stat_4080418644@T1` | -0.60554 |
| `explicit.stat_1263695895@T2` | -0.56798 |
| `explicit.stat_3057012405@T1` | 0.51552 |
| `explicit.stat_1263695895@T1` | -0.50734 |
| `explicit.stat_4080418644@T2` | -0.45219 |
| `explicit.stat_2347036682@T2` | -0.39640 |
| `explicit.stat_1574590649@T2` | -0.34749 |
| `explicit.stat_3984865854@T2` | 0.33363 |
| `explicit.stat_328541901@T2` | 0.32304 |

### weapon.staff — n=6507, R²=-0.6422

intercept: `-2.0427`  ·  log_price: True  ·  ilvl: `0.02554`  ·  n_mods: `-0.00937`  ·  n_top_tier: `0.26839`  ·  corrupted: `0.07276`  ·  n_sockets: `0.06783`  ·  quality: `0.08905`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 1.91308 |
| `explicit.stat_4226189338@T1` | 1.86573 |
| `explicit.stat_1545858329@T1` | 1.72611 |
| `explicit.stat_2254480358@T1` | 1.60658 |
| `explicit.stat_124131830@T1` | 1.53809 |
| `explicit.stat_1600707273@T1` | 1.38334 |
| `explicit.stat_2768835289@T2` | 1.20237 |
| `explicit.stat_2254480358@T2` | 1.06956 |
| `explicit.stat_3291658075@T2` | 0.85722 |
| `explicit.stat_2231156303@T2` | 0.69812 |
| `explicit.stat_4226189338@T2` | 0.53665 |
| `explicit.stat_3962278098@T2` | 0.47021 |

### weapon.spear — n=5559, R²=-0.6771

intercept: `-1.0193`  ·  log_price: True  ·  ilvl: `0.01340`  ·  n_mods: `-0.00994`  ·  n_top_tier: `0.24516`  ·  corrupted: `-0.04145`  ·  n_sockets: `0.02519`  ·  quality: `0.10150`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.45274 |
| `explicit.stat_9187492@T1` | 2.29121 |
| `crafted.stat_210067635@T2` | -1.47269 |
| `crafted.stat_3035140377` | 1.31518 |
| `explicit.stat_1509134228@T1` | 0.67225 |
| `explicit.stat_210067635@T1` | 0.63478 |
| `crafted.stat_518292764` | 0.62066 |
| `explicit.stat_55876295@T1` | -0.29285 |
| `rune.stat_3336890334` | 0.28852 |
| `explicit.stat_55876295@T2` | -0.26715 |
| `explicit.stat_1037193709@T1` | -0.26715 |
| `explicit.stat_1263695895@T2` | -0.26457 |

### armour.focus — n=4545, R²=-0.5214

intercept: `-6.6847`  ·  log_price: True  ·  ilvl: `0.08254`  ·  n_mods: `-0.01275`  ·  n_top_tier: `0.93105`  ·  corrupted: `0.74046`  ·  n_sockets: `0.31551`  ·  quality: `0.07342`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 6.24478 |
| `crafted.stat_737908626@T2` | -2.69255 |
| `explicit.stat_4220027924@T1` | -1.21905 |
| `explicit.stat_4220027924@T2` | -1.16802 |
| `explicit.stat_2923486259@T1` | -1.09475 |
| `explicit.stat_2891184298@T2` | -1.07033 |
| `explicit.stat_2891184298@T1` | -1.04888 |
| `explicit.stat_736967255@T2` | -1.01960 |
| `explicit.stat_3962278098@T2` | -0.98612 |
| `explicit.stat_737908626@T2` | -0.90970 |
| `explicit.stat_3962278098@T1` | -0.90449 |
| `explicit.stat_2974417149@T2` | -0.90375 |

### armour.quiver — n=4247, R²=-0.5093

intercept: `-5.9964`  ·  log_price: True  ·  ilvl: `0.07072`  ·  n_mods: `0.01184`  ·  n_top_tier: `0.85689`  ·  corrupted: `0.61040`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.96084 |
| `explicit.stat_2463230181@T1` | 1.39095 |
| `explicit.stat_2321178454@T2` | -1.09850 |
| `explicit.stat_681332047@T2` | -1.08987 |
| `explicit.stat_2194114101@T2` | -1.08435 |
| `explicit.stat_1573130764@T1` | -1.07371 |
| `explicit.stat_1368271171@T2` | -1.00488 |
| `explicit.stat_3261801346@T1` | -0.91319 |
| `explicit.stat_1573130764@T2` | -0.90817 |
| `explicit.stat_4067062424@T1` | -0.90382 |
| `explicit.stat_2463230181@T2` | 0.87602 |
| `explicit.stat_3261801346@T2` | -0.78338 |

### armour.shield — n=3715, R²=-0.594

intercept: `-5.2099`  ·  log_price: True  ·  ilvl: `0.06524`  ·  n_mods: `0.00402`  ·  n_top_tier: `0.42160`  ·  corrupted: `0.25377`  ·  n_sockets: `0.01501`  ·  quality: `0.05155`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.13910 |
| `explicit.stat_1978899297@T1` | 0.87529 |
| `explicit.stat_328541901@T1` | -0.86813 |
| `explicit.stat_2339757871@T1` | -0.81760 |
| `explicit.stat_1011760251@T1` | -0.79005 |
| `explicit.stat_1011760251@T2` | -0.74720 |
| `explicit.stat_2481353198@T2` | -0.73690 |
| `explicit.stat_2481353198@T1` | -0.69462 |
| `explicit.stat_1978899297@T2` | -0.68841 |
| `explicit.stat_328541901@T2` | -0.65308 |
| `explicit.stat_3676141501@T1` | 0.60014 |
| `explicit.stat_3362812763@T1` | -0.58706 |

### weapon.twomace — n=3368, R²=-0.5018

intercept: `-7.7554`  ·  log_price: True  ·  ilvl: `0.10016`  ·  n_mods: `-0.07968`  ·  n_top_tier: `0.39784`  ·  corrupted: `0.77967`  ·  n_sockets: `0.11748`  ·  quality: `0.04716`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.54673 |
| `desecrated.stat_1509134228@T1` | 2.12333 |
| `explicit.stat_1509134228@T1` | 1.25702 |
| `explicit.stat_1037193709@T1` | -1.15130 |
| `crafted.stat_3035140377` | 1.04986 |
| `explicit.stat_3336890334@T1` | -0.90521 |
| `explicit.stat_1263695895@T1` | -0.85709 |
| `explicit.stat_1263695895@T2` | -0.76826 |
| `explicit.stat_210067635@T1` | 0.75224 |
| `explicit.stat_709508406@T1` | -0.70615 |
| `explicit.stat_821021828@T2` | -0.68213 |
| `explicit.stat_387439868@T2` | -0.68190 |

## Coverage (listings per base)

- … **Sapphire** — 19082 listings (19057 priced) [0.3–7553463.8 ex]
- … **Emerald** — 18828 listings (18806 priced) [0.3–7553463.8 ex]
- … **Ruby** — 14497 listings (14485 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 8267 listings (8258 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 6567 listings (6558 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 6398 listings (6386 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 6313 listings (6308 priced) [0.2–19945827.9 ex]
- … **Stellar Amulet** — 6077 listings (6074 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 6045 listings (6035 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 5883 listings (5876 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5129 listings (5116 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4874 listings (4869 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 4743 listings (4740 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 4736 listings (4734 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 4309 listings (4303 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4250 listings (4246 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4183 listings (4176 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4122 listings (4120 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4112 listings (4108 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4038 listings (4036 priced) [0.2–24532814.5 ex]
- … **Obliterator Bow** — 3955 listings (3944 priced) [0.3–42622633798.0 ex]
- … **Bloodstone Amulet** — 3952 listings (3948 priced) [0.3–4275054.0 ex]
- … **Heavy Belt** — 3898 listings (3896 priced) [0.3–2608914286.6 ex]
- … **Pearl Ring** — 3798 listings (3795 priced) [0.2–275252424.7 ex]
- … **Lunar Amulet** — 3722 listings (3718 priced) [0.3–4877938.3 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-15T13:36:03+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **510573** (509473 priced in exalted)
- Distinct bases: 982 · distinct mods: 3116 · mod rows: 2423156
- Sold signals: **26192** sold · 285030 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-15T13:27:50+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×27.28** (median |log error| 3.306)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×69.56 · ±30% 5% · n=73622
- Premium segment (60ex+): skill **+0.12** · typical error ×289.69 · ±30% 0% · n=49217

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 10215 | ×51.25 | 21% | +0.06 | +0.08 |
| jewel | 9502 | ×9.76 | 5% | +0.02 | +0.05 |
| accessory.amulet | 9394 | ×52.64 | 20% | +0.03 | +0.03 |
| accessory.belt | 7174 | ×19.60 | 5% | +0.06 | +0.09 |
| armour.chest | 7038 | ×31.53 | 19% | +0.07 | +0.09 |
| armour.helmet | 6895 | ×25.55 | 8% | +0.11 | +0.13 |
| armour.boots | 6416 | ×38.46 | 20% | +0.07 | +0.09 |
| armour.gloves | 6267 | ×37.70 | 11% | +0.09 | +0.11 |
| other | 5541 | ×3.96 | 41% | +0.10 | +0.16 |
| weapon.wand | 3934 | ×36.51 | 18% | +0.07 | +0.09 |
| weapon.bow | 3123 | ×27.95 | 19% | +0.09 | +0.10 |
| weapon.crossbow | 2966 | ×26.08 | 18% | +0.09 | +0.14 |
| weapon.warstaff | 1821 | ×35.93 | 16% | +0.11 | +0.10 |
| weapon.staff | 1676 | ×61.26 | 13% | +0.09 | +0.10 |
| weapon.sceptre | 1671 | ×42.47 | 6% | +0.14 | +0.13 |
| weapon.spear | 1361 | ×77.34 | 16% | +0.08 | +0.09 |
| armour.focus | 1149 | ×45.47 | 8% | +0.14 | +0.17 |
| armour.quiver | 1087 | ×28.99 | 9% | +0.10 | +0.12 |
| flask.charm | 903 | ×49.99 | 35% | +0.02 | +0.05 |
| armour.shield | 898 | ×17.08 | 16% | +0.03 | +0.03 |
| weapon.twomace | 790 | ×14.79 | 13% | +0.07 | +0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=51391, R²=-0.925

intercept: `-1.6990`  ·  log_price: True  ·  ilvl: `0.02676`  ·  n_mods: `0.66030`  ·  n_top_tier: `-0.19512`  ·  corrupted: `0.30313`  ·  quality: `0.22930`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.15341 |
| `explicit.stat_2301718443@T1` | 3.03724 |
| `explicit.stat_627767961@T1` | -2.45023 |
| `explicit.stat_3780644166@T1` | -2.35195 |
| `explicit.stat_3485067555@T1` | 2.24875 |
| `explicit.stat_1805182458@T1` | -2.12378 |
| `explicit.stat_239367161@T1` | -1.89929 |
| `explicit.stat_1062710370@T1` | -1.86367 |
| `explicit.stat_3091578504@T1` | -1.85089 |
| `explicit.stat_1697951953@T1` | -1.83911 |
| `explicit.stat_153777645@T1` | -1.80156 |
| `explicit.stat_234296660@T1` | -1.67053 |

### other — n=49371, R²=-0.6168

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.35923`  ·  corrupted: `0.34870`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.55838 |
| `explicit.stat_2974417149@T1` | 0.49126 |
| `explicit.stat_3299347043@T1` | -0.38107 |
| `explicit.stat_2482852589@T1` | -0.32744 |
| `explicit.stat_789117908@T1` | -0.30668 |
| `explicit.stat_2968503605@T1` | 0.28258 |
| `explicit.stat_3917489142@T1` | 0.23788 |
| `implicit.stat_3879011313` | 0.23468 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23026 |
| `explicit.stat_3141070085@T1` | -0.22303 |
| `explicit.stat_2106365538@T1` | -0.18958 |

### accessory.ring — n=46717, R²=-1.9913

intercept: `3.4035`  ·  log_price: True  ·  ilvl: `-0.04211`  ·  n_mods: `0.00109`  ·  n_top_tier: `0.95655`  ·  corrupted: `0.02589`  ·  n_sockets: `0.03074`  ·  quality: `0.05830`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -0.99594 |
| `explicit.stat_1573130764@T1` | -0.99580 |
| `explicit.stat_1368271171@T2` | -0.98680 |
| `explicit.stat_803737631@T1` | -0.98336 |
| `explicit.stat_2144192055@T1` | -0.98207 |
| `explicit.stat_3325883026@T1` | -0.98179 |
| `explicit.stat_3291658075@T2` | -0.97758 |
| `explicit.stat_3962278098@T2` | -0.97695 |
| `explicit.stat_4220027924@T2` | -0.97539 |
| `explicit.stat_3291658075@T1` | -0.97237 |
| `explicit.stat_3032590688@T2` | -0.97234 |
| `explicit.stat_1368271171@T1` | -0.97179 |

### accessory.amulet — n=43102, R²=-2.1407

intercept: `3.8034`  ·  log_price: True  ·  ilvl: `-0.04659`  ·  n_mods: `-0.02072`  ·  n_top_tier: `0.97026`  ·  corrupted: `0.05249`  ·  n_sockets: `-0.10997`  ·  quality: `-0.00013`

| stat_id | coef |
|---|---|
| `explicit.stat_472520716@T2` | -1.05199 |
| `explicit.stat_472520716@T1` | -1.04778 |
| `explicit.stat_803737631@T1` | -1.03581 |
| `explicit.stat_2901986750@T1` | -1.03163 |
| `explicit.stat_1050105434@T2` | -1.02149 |
| `explicit.stat_803737631@T2` | -1.01319 |
| `explicit.stat_2974417149@T1` | -1.00234 |
| `explicit.stat_2891184298@T1` | -1.00194 |
| `explicit.stat_2866361420@T2` | -1.00059 |
| `explicit.stat_3917489142@T2` | -1.00044 |
| `explicit.stat_2974417149@T2` | -0.99898 |
| `explicit.stat_1444556985@T1` | -0.99807 |

### accessory.belt — n=33110, R²=-0.8965

intercept: `6.3937`  ·  log_price: True  ·  ilvl: `-0.06378`  ·  n_mods: `-0.27027`  ·  n_top_tier: `1.20854`  ·  corrupted: `0.88648`  ·  n_sockets: `0.18054`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.96650 |
| `explicit.stat_1389754388@T1` | -1.73794 |
| `explicit.stat_2881298780@T1` | -1.68574 |
| `explicit.stat_809229260@T2` | -1.47057 |
| `explicit.stat_3299347043@T2` | -1.44726 |
| `explicit.stat_644456512@T1` | -1.43357 |
| `explicit.stat_4220027924@T2` | -1.38737 |
| `explicit.stat_809229260@T1` | -1.37884 |
| `explicit.stat_51994685@T1` | -1.37873 |
| `explicit.stat_1671376347@T2` | -1.32297 |
| `explicit.stat_4080418644@T2` | -1.29124 |
| `explicit.stat_1389754388@T2` | -1.24393 |

### armour.chest — n=32761, R²=-1.6035

intercept: `3.8130`  ·  log_price: True  ·  ilvl: `-0.04691`  ·  n_mods: `-0.02825`  ·  n_top_tier: `0.56765`  ·  corrupted: `0.24347`  ·  n_sockets: `0.03471`  ·  quality: `0.04474`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.94045 |
| `explicit.stat_3981240776@T1` | 0.91010 |
| `explicit.stat_3484657501@T1` | -0.66994 |
| `explicit.stat_986397080@T2` | -0.65305 |
| `explicit.stat_1999113824@T1` | -0.63194 |
| `explicit.stat_4080418644@T2` | -0.62925 |
| `explicit.stat_986397080@T1` | -0.62391 |
| `explicit.stat_4080418644@T1` | -0.62221 |
| `explicit.stat_915769802@T2` | -0.62143 |
| `explicit.stat_1692879867@T1` | -0.61605 |
| `explicit.stat_2451402625@T1` | -0.61166 |
| `explicit.stat_4015621042@T2` | -0.60864 |

### armour.helmet — n=31905, R²=-1.1812

intercept: `4.1192`  ·  log_price: True  ·  ilvl: `-0.05174`  ·  n_mods: `-0.09181`  ·  n_top_tier: `0.43229`  ·  corrupted: `0.67490`  ·  n_sockets: `0.14715`  ·  quality: `0.04710`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.78499 |
| `explicit.stat_1263695895@T1` | -1.01620 |
| `explicit.stat_3917489142@T2` | -0.94278 |
| `crafted.stat_3917489142@T1` | 0.79232 |
| `explicit.stat_1999113824@T1` | -0.73204 |
| `explicit.stat_53045048@T2` | -0.71524 |
| `explicit.stat_1263695895@T2` | -0.70050 |
| `explicit.stat_3261801346@T1` | -0.63863 |
| `explicit.stat_3321629045@T2` | -0.61851 |
| `explicit.stat_587431675@T2` | -0.61250 |
| `explicit.stat_3261801346@T2` | -0.58449 |
| `explicit.stat_3917489142@T1` | -0.57184 |

### armour.boots — n=29878, R²=-1.6572

intercept: `3.7904`  ·  log_price: True  ·  ilvl: `-0.04649`  ·  n_mods: `-0.02474`  ·  n_top_tier: `0.75642`  ·  corrupted: `0.03581`  ·  n_sockets: `0.01825`  ·  quality: `0.03199`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.43886 |
| `explicit.stat_2339757871@T1` | -0.92931 |
| `desecrated.stat_2250533757@T2` | -0.90639 |
| `explicit.stat_3917489142@T2` | -0.89680 |
| `explicit.stat_3299347043@T1` | -0.88826 |
| `crafted.stat_3917489142@T1` | 0.88002 |
| `explicit.stat_2160282525@T1` | -0.82542 |
| `explicit.stat_2923486259@T2` | -0.82186 |
| `explicit.stat_3917489142@T1` | -0.81312 |
| `explicit.stat_53045048@T1` | -0.80505 |
| `explicit.stat_1671376347@T2` | -0.80080 |
| `explicit.stat_3362812763@T1` | -0.79812 |

### armour.gloves — n=29118, R²=-1.4685

intercept: `4.0121`  ·  log_price: True  ·  ilvl: `-0.05224`  ·  n_mods: `-0.01750`  ·  n_top_tier: `0.56594`  ·  corrupted: `0.05140`  ·  n_sockets: `0.11498`  ·  quality: `0.04545`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | -6.69696 |
| `explicit.stat_2339757871@T1` | 3.50361 |
| `explicit.stat_3484657501@T2` | -0.98590 |
| `rune.stat_836936635` | 0.91033 |
| `explicit.stat_3484657501@T1` | -0.89688 |
| `explicit.stat_1671376347@T1` | 0.88183 |
| `explicit.stat_9187492@T1` | 0.86460 |
| `explicit.stat_2923486259@T1` | -0.86071 |
| `explicit.stat_4052037485@T1` | -0.81625 |
| `explicit.stat_803737631@T2` | -0.77872 |
| `explicit.stat_803737631@T1` | -0.76860 |
| `explicit.stat_3321629045@T2` | -0.76832 |

### weapon.wand — n=18609, R²=-2.2403

intercept: `3.8025`  ·  log_price: True  ·  ilvl: `-0.04694`  ·  n_mods: `-0.01843`  ·  n_top_tier: `0.56985`  ·  corrupted: `0.02581`  ·  n_sockets: `0.04015`  ·  quality: `0.00116`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -3.04357 |
| `explicit.stat_1545858329@T1` | 2.87321 |
| `explicit.stat_2254480358@T1` | 2.63958 |
| `explicit.stat_4226189338@T1` | 1.79975 |
| `explicit.stat_591105508@T1` | 1.78457 |
| `explicit.stat_124131830@T1` | 1.76814 |
| `explicit.stat_736967255@T2` | 1.64232 |
| `crafted.stat_124131830` | 1.15298 |
| `explicit.stat_1263695895@T2` | -0.69228 |
| `explicit.stat_2768835289@T2` | 0.67542 |
| `explicit.stat_2254480358@T2` | 0.67134 |
| `explicit.stat_1263695895@T1` | -0.65451 |

### weapon.bow — n=14970, R²=-2.0319

intercept: `3.4666`  ·  log_price: True  ·  ilvl: `-0.04192`  ·  n_mods: `-0.03194`  ·  n_top_tier: `0.59604`  ·  corrupted: `-0.09496`  ·  n_sockets: `0.01100`  ·  quality: `0.03138`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.06327 |
| `explicit.stat_1202301673@T1` | 1.64229 |
| `crafted.stat_3035140377` | 1.43270 |
| `explicit.stat_1263695895@T1` | -0.78445 |
| `explicit.stat_1263695895@T2` | -0.76765 |
| `explicit.stat_3695891184@T2` | -0.67046 |
| `explicit.stat_2463230181@T2` | -0.66742 |
| `explicit.stat_3695891184@T1` | -0.65445 |
| `explicit.stat_1509134228@T1` | -0.64612 |
| `explicit.stat_669069897@T1` | -0.63949 |
| `explicit.stat_2694482655@T2` | -0.63931 |
| `explicit.stat_1368271171@T2` | -0.63640 |

### weapon.crossbow — n=14104, R²=-1.9071

intercept: `3.8403`  ·  log_price: True  ·  ilvl: `-0.04681`  ·  n_mods: `-0.02231`  ·  n_top_tier: `0.70410`  ·  corrupted: `0.06215`  ·  n_sockets: `0.03060`  ·  quality: `0.01478`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.96622 |
| `explicit.stat_2250681686@T2` | -1.50626 |
| `explicit.stat_709508406@T1` | 1.50359 |
| `explicit.stat_1202301673@T1` | 1.38254 |
| `explicit.stat_1980802737` | 1.20415 |
| `explicit.stat_2250681686` | 0.91249 |
| `crafted.stat_3035140377` | 0.87693 |
| `explicit.stat_1263695895@T2` | -0.80246 |
| `explicit.stat_1509134228@T2` | -0.79181 |
| `explicit.stat_1544773869@T2` | -0.78841 |
| `explicit.stat_2694482655@T1` | -0.77772 |
| `explicit.stat_3695891184@T1` | -0.77454 |

### flask.charm — n=13144, R²=-0.5429

intercept: `0.0065`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.66318`  ·  corrupted: `2.19706`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.27247 |
| `explicit.stat_1056492907` | 3.36572 |
| `explicit.stat_828533480@T2` | -2.66319 |
| `explicit.stat_828533480@T1` | -2.66318 |
| `explicit.stat_2541588185@T2` | -2.66318 |
| `explicit.stat_2676834156@T2` | -2.66317 |
| `explicit.stat_1120862500@T2` | -2.66317 |
| `explicit.stat_1873752457@T2` | -2.66317 |
| `explicit.stat_3196823591@T2` | -2.66316 |
| `explicit.stat_388617051@T2` | -2.66316 |
| `explicit.stat_1366840608@T2` | -2.66315 |
| `explicit.stat_2365392475@T2` | -2.66315 |

### weapon.warstaff — n=8659, R²=-0.4589

intercept: `-7.0988`  ·  log_price: True  ·  ilvl: `0.09668`  ·  n_mods: `-0.17290`  ·  n_top_tier: `0.62158`  ·  corrupted: `0.24321`  ·  n_sockets: `0.10635`  ·  quality: `0.05751`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.36429 |
| `explicit.stat_1037193709@T1` | 1.26190 |
| `explicit.stat_328541901@T1` | -1.15657 |
| `explicit.stat_328541901@T2` | -1.14835 |
| `explicit.stat_1037193709@T2` | -0.82681 |
| `explicit.stat_55876295@T2` | -0.79208 |
| `desecrated.stat_9187492` | 0.72702 |
| `explicit.stat_210067635@T1` | -0.65618 |
| `explicit.stat_55876295@T1` | -0.64795 |
| `explicit.stat_1940865751@T1` | -0.62933 |
| `explicit.stat_791928121@T2` | -0.62285 |
| `explicit.stat_3695891184@T2` | -0.61940 |

### weapon.staff — n=8092, R²=-0.4416

intercept: `-11.2592`  ·  log_price: True  ·  ilvl: `0.14505`  ·  n_mods: `-0.10874`  ·  n_top_tier: `0.48374`  ·  corrupted: `0.06659`  ·  n_sockets: `0.22604`  ·  quality: `0.04581`

| stat_id | coef |
|---|---|
| `explicit.stat_1600707273@T1` | 1.29386 |
| `explicit.stat_4226189338@T1` | 1.29165 |
| `explicit.stat_1545858329@T1` | 1.21724 |
| `explicit.stat_4226189338@T2` | 1.19778 |
| `explicit.stat_124131830@T1` | 1.17574 |
| `explicit.stat_124131830@T2` | 1.15145 |
| `explicit.stat_2768835289@T2` | 1.00885 |
| `explicit.stat_293638271@T2` | -0.90283 |
| `explicit.stat_2254480358@T1` | 0.87287 |
| `explicit.stat_591105508@T1` | 0.78190 |
| `explicit.stat_3962278098@T2` | 0.73170 |
| `explicit.stat_2974417149@T1` | -0.66900 |

### weapon.sceptre — n=8020, R²=-0.4015

intercept: `-16.4634`  ·  log_price: True  ·  ilvl: `0.20807`  ·  n_mods: `-0.02750`  ·  n_top_tier: `0.54308`  ·  corrupted: `0.57993`  ·  n_sockets: `0.23399`  ·  quality: `0.05658`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.22051 |
| `explicit.stat_2162097452@T2` | 1.25932 |
| `explicit.stat_1263695895@T2` | -0.93059 |
| `explicit.stat_2347036682@T2` | -0.92099 |
| `explicit.stat_1263695895@T1` | -0.83265 |
| `explicit.stat_1574590649@T2` | -0.78604 |
| `explicit.stat_2854751904@T2` | -0.74288 |
| `explicit.stat_1250712710@T2` | 0.72930 |
| `explicit.stat_289128254@T2` | -0.72783 |
| `explicit.stat_4080418644@T1` | -0.68110 |
| `explicit.stat_1050105434@T2` | -0.66781 |
| `explicit.stat_789117908@T2` | -0.62441 |

### weapon.spear — n=6619, R²=-0.5238

intercept: `-8.6051`  ·  log_price: True  ·  ilvl: `0.11548`  ·  n_mods: `-0.03769`  ·  n_top_tier: `0.76939`  ·  corrupted: `-0.12355`  ·  n_sockets: `0.20361`  ·  quality: `0.10044`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -2.92642 |
| `explicit.stat_1202301673@T1` | 1.92730 |
| `explicit.stat_9187492@T1` | 1.77290 |
| `desecrated.stat_210067635@T1` | -1.14810 |
| `explicit.stat_1263695895@T2` | -1.12516 |
| `explicit.stat_55876295@T1` | -1.05897 |
| `crafted.stat_3035140377` | 0.96868 |
| `explicit.stat_1509134228@T1` | 0.92929 |
| `explicit.stat_1037193709@T1` | -0.86672 |
| `explicit.stat_55876295@T2` | -0.85885 |
| `explicit.stat_210067635@T1` | 0.83813 |
| `explicit.stat_1940865751@T2` | -0.80316 |

### armour.focus — n=5449, R²=-0.4193

intercept: `-11.8424`  ·  log_price: True  ·  ilvl: `0.15146`  ·  n_mods: `-0.15318`  ·  n_top_tier: `0.86100`  ·  corrupted: `0.78550`  ·  n_sockets: `0.48512`  ·  quality: `0.06558`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 4.25365 |
| `explicit.stat_4220027924@T2` | -1.28772 |
| `explicit.stat_3962278098@T1` | -1.18935 |
| `explicit.stat_736967255@T2` | -1.17599 |
| `explicit.stat_2231156303@T1` | -1.08239 |
| `explicit.stat_2923486259@T1` | -1.05828 |
| `explicit.stat_3962278098@T2` | -1.03597 |
| `explicit.stat_2231156303@T2` | -0.99011 |
| `explicit.stat_4015621042@T1` | -0.97484 |
| `explicit.stat_2974417149@T2` | -0.95945 |
| `explicit.stat_737908626@T2` | -0.91592 |
| `explicit.stat_3291658075@T1` | -0.90821 |

### armour.quiver — n=5075, R²=-0.3821

intercept: `-11.9234`  ·  log_price: True  ·  ilvl: `0.14450`  ·  n_mods: `-0.04993`  ·  n_top_tier: `0.81616`  ·  corrupted: `0.34433`

| stat_id | coef |
|---|---|
| `explicit.stat_2463230181@T1` | 1.46191 |
| `explicit.stat_681332047@T2` | -1.22331 |
| `explicit.stat_4067062424@T1` | -1.18288 |
| `explicit.stat_2321178454@T2` | -1.16755 |
| `desecrated.stat_3932115504@T1` | 1.10298 |
| `explicit.stat_1573130764@T1` | -1.04575 |
| `explicit.stat_803737631@T2` | -1.02953 |
| `explicit.stat_1573130764@T2` | -1.02640 |
| `explicit.stat_4067062424@T2` | -0.86949 |
| `explicit.stat_2321178454@T1` | -0.83588 |
| `explicit.stat_3261801346@T1` | -0.82001 |
| `explicit.stat_1368271171@T2` | -0.75467 |

### armour.shield — n=4397, R²=-0.5491

intercept: `-8.7506`  ·  log_price: True  ·  ilvl: `0.11357`  ·  n_mods: `-0.07198`  ·  n_top_tier: `0.50401`  ·  corrupted: `-0.11323`  ·  n_sockets: `0.10674`  ·  quality: `0.06561`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.22374 |
| `explicit.stat_4095671657@T1` | -0.99885 |
| `explicit.stat_1011760251@T2` | -0.97676 |
| `explicit.stat_2481353198@T2` | -0.88680 |
| `explicit.stat_3033371881@T2` | -0.85804 |
| `explicit.stat_2481353198@T1` | -0.83079 |
| `explicit.stat_2923486259@T2` | -0.80201 |
| `explicit.stat_3855016469@T1` | -0.78681 |
| `explicit.stat_3321629045@T2` | -0.78410 |
| `explicit.stat_2339757871@T1` | -0.77267 |
| `explicit.stat_3484657501@T1` | -0.76222 |
| `explicit.stat_3484657501@T2` | -0.74551 |

### weapon.twomace — n=4058, R²=-0.5084

intercept: `-10.4331`  ·  log_price: True  ·  ilvl: `0.13663`  ·  n_mods: `-0.13954`  ·  n_top_tier: `0.53529`  ·  corrupted: `0.35846`  ·  n_sockets: `0.18660`  ·  quality: `0.05490`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.96113 |
| `desecrated.stat_1509134228@T1` | 1.94022 |
| `explicit.stat_1037193709@T1` | -1.83901 |
| `explicit.stat_3336890334@T1` | -1.20320 |
| `explicit.stat_387439868@T2` | -0.96742 |
| `crafted.stat_3035140377` | 0.96063 |
| `explicit.stat_518292764@T2` | -0.94653 |
| `explicit.stat_1037193709@T2` | -0.85303 |
| `explicit.stat_3639275092@T1` | -0.75614 |
| `explicit.stat_2694482655@T1` | -0.65981 |
| `explicit.stat_3639275092@T2` | -0.62881 |
| `explicit.stat_2694482655@T2` | -0.62553 |

## Coverage (listings per base)

- … **Sapphire** — 23910 listings (23873 priced) [0.3–7553463.8 ex]
- … **Emerald** — 23564 listings (23534 priced) [0.3–7553463.8 ex]
- … **Ruby** — 18051 listings (18035 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 9657 listings (9648 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8006 listings (7996 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 7765 listings (7749 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 7658 listings (7651 priced) [0.2–19945827.9 ex]
- … **Gold Amulet** — 7306 listings (7296 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 7211 listings (7207 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 7160 listings (7146 priced) [0.2–91750808.2 ex]
- … **Sapphire Ring** — 5974 listings (5968 priced) [0.2–307202867.9 ex]
- … **Dueling Wand** — 5926 listings (5910 priced) [0.3–4297682211.9 ex]
- … **Topaz Ring** — 5708 listings (5703 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5695 listings (5692 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5131 listings (5114 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5095 listings (5090 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4982 listings (4969 priced) [0.6–398912568423.8 ex]
- … **Amber Amulet** — 4953 listings (4949 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 4946 listings (4939 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4901 listings (4894 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4792 listings (4786 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 4607 listings (4601 priced) [0.2–275252424.7 ex]
- … **Heavy Belt** — 4596 listings (4592 priced) [0.3–398912568423.8 ex]
- … **Azure Amulet** — 4528 listings (4528 priced) [0.3–123132003.2 ex]
- … **Obliterator Bow** — 4490 listings (4476 priced) [0.3–42622633798.0 ex]

# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-20T17:23:36+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **687754** (685628 priced in exalted)
- Distinct bases: 999 · distinct mods: 3310 · mod rows: 3255514
- Sold signals: **24351** sold · 391233 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-20T17:10:04+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×21.37** (median |log error| 3.0621)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.16** · typical error ×58.03 · ±30% 5% · n=100095
- Premium segment (60ex+): skill **+0.15** · typical error ×286.80 · ±30% 0% · n=67100

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 14649 | ×52.59 | 21% | +0.03 | +0.06 |
| jewel | 13880 | ×9.94 | 5% | +0.11 | +0.13 |
| accessory.amulet | 13213 | ×35.57 | 18% | +0.04 | +0.05 |
| accessory.belt | 9489 | ×24.19 | 16% | +0.06 | +0.08 |
| armour.chest | 9137 | ×17.36 | 20% | +0.09 | +0.10 |
| armour.helmet | 8938 | ×22.91 | 12% | +0.11 | +0.12 |
| armour.boots | 8297 | ×27.78 | 20% | +0.10 | +0.12 |
| armour.gloves | 8112 | ×35.87 | 14% | +0.08 | +0.11 |
| other | 8010 | ×3.16 | 41% | +0.10 | +0.15 |
| weapon.wand | 4842 | ×42.44 | 15% | +0.10 | +0.11 |
| weapon.bow | 3800 | ×29.01 | 13% | +0.15 | +0.15 |
| weapon.crossbow | 3582 | ×26.78 | 14% | +0.12 | +0.15 |
| weapon.warstaff | 2439 | ×14.23 | 7% | +0.22 | +0.22 |
| weapon.staff | 2344 | ×18.65 | 6% | +0.18 | +0.17 |
| weapon.sceptre | 2292 | ×21.59 | 4% | +0.09 | +0.09 |
| weapon.spear | 1842 | ×15.25 | 7% | +0.14 | +0.14 |
| armour.focus | 1541 | ×14.18 | 7% | +0.11 | +0.13 |
| armour.quiver | 1440 | ×18.53 | 6% | +0.13 | +0.14 |
| armour.shield | 1181 | ×10.45 | 8% | +0.10 | +0.12 |
| flask.charm | 1172 | ×10.07 | 28% | -0.01 | +0.00 |
| weapon.twomace | 1099 | ×8.09 | 9% | +0.11 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=76262, R²=-0.984

intercept: `-1.9304`  ·  log_price: True  ·  ilvl: `0.02421`  ·  n_mods: `0.83652`  ·  n_top_tier: `-0.26256`  ·  corrupted: `0.46865`  ·  quality: `0.00098`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.15683 |
| `explicit.stat_3485067555@T1` | 2.31420 |
| `explicit.stat_1594812856@T1` | 1.97185 |
| `explicit.stat_1869147066@T1` | -1.72871 |
| `explicit.stat_1569101201@T1` | -1.59704 |
| `explicit.stat_3780644166@T1` | -1.50020 |
| `explicit.stat_3174700878@T1` | 1.32452 |
| `explicit.stat_4147897060@T1` | -1.28555 |
| `explicit.stat_234296660@T1` | -1.27239 |
| `explicit.stat_3668351662@T1` | -1.17970 |
| `explicit.stat_3374165039@T1` | -1.17300 |
| `explicit.stat_2720982137@T1` | -1.12010 |

### accessory.ring — n=66781, R²=-2.0264

intercept: `3.5107`  ·  log_price: True  ·  ilvl: `-0.04377`  ·  n_mods: `0.00094`  ·  n_top_tier: `0.93506`  ·  corrupted: `0.00640`  ·  n_sockets: `1.88524`  ·  quality: `0.02254`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -0.96765 |
| `explicit.stat_803737631@T1` | -0.96073 |
| `explicit.stat_1573130764@T2` | -0.95511 |
| `explicit.stat_2231156303@T1` | -0.95503 |
| `explicit.stat_4080418644@T1` | -0.95382 |
| `explicit.stat_4220027924@T2` | -0.95075 |
| `explicit.stat_3325883026@T1` | -0.94961 |
| `explicit.stat_2891184298@T2` | -0.94693 |
| `explicit.stat_2144192055@T1` | -0.94429 |
| `explicit.stat_3261801346@T1` | -0.94355 |
| `explicit.stat_2923486259@T2` | -0.94335 |
| `explicit.stat_2891184298@T1` | -0.94279 |

### other — n=65516, R²=-0.6591

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.08590`  ·  n_top_tier: `0.26068`  ·  corrupted: `0.03735`  ·  n_sockets: `-0.00005`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.34664 |
| `explicit.stat_3299347043@T1` | -0.26239 |
| `implicit.stat_718638445` | 0.25773 |
| `implicit.stat_3182714256` | 0.25772 |
| `implicit.stat_2219129443` | 0.22166 |
| `explicit.stat_3917489142@T1` | -0.15586 |
| `explicit.stat_2974417149@T1` | 0.14937 |
| `implicit.stat_958696139` | -0.08588 |
| `explicit.stat_789117908@T1` | -0.06397 |
| `implicit.stat_3879011313` | 0.06072 |
| `implicit.stat_1416292992` | -0.05515 |
| `implicit.stat_1379411836` | -0.04911 |

### accessory.amulet — n=60142, R²=-2.1387

intercept: `3.4324`  ·  log_price: True  ·  ilvl: `-0.04301`  ·  n_mods: `-0.02196`  ·  n_top_tier: `1.31404`  ·  corrupted: `0.10329`  ·  n_sockets: `-0.13339`  ·  quality: `0.05105`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.94092 |
| `explicit.stat_3299347043@T2` | -1.81420 |
| `explicit.stat_587431675@T2` | -1.45897 |
| `explicit.stat_803737631@T1` | -1.45174 |
| `explicit.stat_2974417149@T1` | -1.41664 |
| `explicit.stat_2866361420@T2` | -1.41429 |
| `explicit.stat_2866361420@T1` | -1.39415 |
| `explicit.stat_803737631@T2` | -1.38586 |
| `explicit.stat_1050105434@T2` | -1.38052 |
| `explicit.stat_2974417149@T2` | -1.36415 |
| `explicit.stat_4080418644@T1` | -1.35770 |
| `explicit.stat_2901986750@T1` | -1.34779 |

### accessory.belt — n=43366, R²=-1.5804

intercept: `4.7024`  ·  log_price: True  ·  ilvl: `-0.05571`  ·  n_mods: `-0.03776`  ·  n_top_tier: `0.33318`  ·  corrupted: `1.32304`  ·  n_sockets: `1.18243`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.35107 |
| `explicit.stat_2923486259@T2` | 0.67817 |
| `explicit.stat_4220027924@T1` | 0.65360 |
| `explicit.stat_3372524247@T1` | 0.54250 |
| `explicit.stat_3299347043@T1` | -0.53345 |
| `explicit.stat_3299347043@T2` | -0.41600 |
| `explicit.stat_2881298780@T1` | -0.37912 |
| `explicit.stat_51994685@T1` | -0.35776 |
| `explicit.stat_4220027924@T2` | -0.35391 |
| `explicit.stat_1570770415@T2` | -0.35061 |
| `explicit.stat_809229260@T2` | -0.34952 |
| `explicit.stat_3325883026@T1` | -0.34760 |

### armour.chest — n=42933, R²=-1.6831

intercept: `3.5777`  ·  log_price: True  ·  ilvl: `-0.04416`  ·  n_mods: `-0.02135`  ·  n_top_tier: `0.36450`  ·  corrupted: `0.27422`  ·  n_sockets: `0.03176`  ·  quality: `0.07291`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.71541 |
| `explicit.stat_3981240776@T1` | 1.03653 |
| `explicit.stat_986397080@T2` | -0.52659 |
| `explicit.stat_986397080@T1` | -0.51155 |
| `explicit.stat_3484657501@T1` | -0.43536 |
| `explicit.stat_2339757871@T2` | -0.43218 |
| `explicit.stat_1692879867@T2` | -0.42032 |
| `explicit.stat_915769802@T2` | -0.41060 |
| `explicit.stat_4080418644@T2` | -0.40470 |
| `explicit.stat_4080418644@T1` | -0.40366 |
| `explicit.stat_2451402625@T1` | -0.39681 |
| `explicit.stat_3301100256@T2` | -0.39383 |

### armour.helmet — n=41740, R²=-1.446

intercept: `3.6984`  ·  log_price: True  ·  ilvl: `-0.04684`  ·  n_mods: `-0.04652`  ·  n_top_tier: `0.58944`  ·  corrupted: `0.59407`  ·  n_sockets: `0.14226`  ·  quality: `0.06114`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.86424 |
| `explicit.stat_3917489142@T2` | -1.13118 |
| `explicit.stat_3917489142@T1` | -0.96978 |
| `explicit.stat_1263695895@T1` | -0.92489 |
| `explicit.stat_1999113824@T1` | -0.75283 |
| `explicit.stat_2162097452@T2` | -0.74423 |
| `explicit.stat_3321629045@T2` | -0.74126 |
| `explicit.stat_803737631@T1` | -0.72322 |
| `explicit.stat_1263695895@T2` | -0.69389 |
| `explicit.stat_4052037485@T2` | -0.67807 |
| `explicit.stat_803737631@T2` | -0.67496 |
| `explicit.stat_1999113824@T2` | -0.65961 |

### armour.boots — n=38752, R²=-1.7319

intercept: `3.4498`  ·  log_price: True  ·  ilvl: `-0.04259`  ·  n_mods: `-0.01654`  ·  n_top_tier: `0.47042`  ·  corrupted: `0.08662`  ·  n_sockets: `0.04344`  ·  quality: `0.06775`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.77155 |
| `crafted.stat_3917489142@T1` | 1.53156 |
| `explicit.stat_2339757871@T1` | -1.24609 |
| `explicit.stat_3917489142@T2` | -0.58166 |
| `explicit.stat_3299347043@T1` | -0.54420 |
| `explicit.stat_2923486259@T2` | -0.52845 |
| `explicit.stat_1874553720@T1` | -0.51772 |
| `explicit.stat_328541901@T2` | -0.51234 |
| `explicit.stat_2923486259@T1` | 0.51104 |
| `explicit.stat_3321629045@T2` | -0.51098 |
| `explicit.stat_1671376347@T2` | -0.50877 |
| `explicit.stat_2160282525@T1` | -0.49809 |

### armour.gloves — n=37693, R²=-1.6731

intercept: `3.7875`  ·  log_price: True  ·  ilvl: `-0.04983`  ·  n_mods: `-0.00071`  ·  n_top_tier: `0.75018`  ·  corrupted: `-0.01867`  ·  n_sockets: `0.18561`  ·  quality: `0.06177`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.11614 |
| `explicit.stat_2923486259@T1` | -1.17668 |
| `explicit.stat_3321629045@T2` | -1.03107 |
| `explicit.stat_3484657501@T2` | -0.97902 |
| `explicit.stat_9187492@T2` | -0.97120 |
| `rune.stat_201332984` | 0.97074 |
| `explicit.stat_4015621042@T2` | -0.96395 |
| `explicit.stat_4052037485@T1` | -0.96382 |
| `explicit.stat_2923486259@T2` | -0.87463 |
| `explicit.stat_3484657501@T1` | -0.86871 |
| `explicit.stat_124859000@T1` | -0.86639 |
| `explicit.stat_803737631@T2` | -0.86501 |

### weapon.wand — n=22517, R²=-2.0022

intercept: `3.9177`  ·  log_price: True  ·  ilvl: `-0.04839`  ·  n_mods: `-0.05402`  ·  n_top_tier: `0.34388`  ·  corrupted: `0.00657`  ·  n_sockets: `0.04087`  ·  quality: `0.03692`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -3.75814 |
| `explicit.stat_1545858329@T1` | 2.85006 |
| `explicit.stat_2254480358@T1` | 2.59915 |
| `explicit.stat_124131830@T1` | 2.21366 |
| `explicit.stat_591105508@T1` | 2.02304 |
| `explicit.stat_4226189338@T1` | 1.88092 |
| `explicit.stat_736967255@T2` | 1.81250 |
| `crafted.stat_124131830` | 1.23812 |
| `explicit.stat_2254480358@T2` | 1.19343 |
| `explicit.stat_4226189338@T2` | 1.07874 |
| `explicit.stat_1263695895@T2` | -0.73192 |
| `explicit.stat_1545858329@T2` | 0.68230 |

### flask.charm — n=19184, R²=-0.6514

intercept: `0.1060`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.70432`  ·  corrupted: `1.44664`  ·  quality: `0.00642`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.77830 |
| `explicit.stat_1056492907` | 2.63883 |
| `explicit.stat_1120862500@T2` | -1.70435 |
| `explicit.stat_828533480@T2` | -1.70435 |
| `explicit.stat_1873752457@T2` | -1.70432 |
| `explicit.stat_3196823591@T2` | -1.70427 |
| `explicit.stat_2365392475@T2` | -1.70426 |
| `explicit.stat_2676834156@T2` | -1.70424 |
| `explicit.stat_388617051@T2` | -1.69974 |
| `explicit.stat_828533480@T1` | -1.69752 |
| `explicit.stat_2541588185@T2` | -1.69591 |
| `explicit.stat_1873752457@T1` | -1.68046 |

### weapon.bow — n=17973, R²=-1.8539

intercept: `3.9289`  ·  log_price: True  ·  ilvl: `-0.04757`  ·  n_mods: `-0.06729`  ·  n_top_tier: `0.83086`  ·  corrupted: `0.67076`  ·  n_sockets: `0.03460`  ·  quality: `0.03079`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.96885 |
| `crafted.stat_3035140377` | 1.30720 |
| `explicit.stat_1263695895@T1` | -1.23553 |
| `explicit.stat_3336890334@T1` | 1.21953 |
| `explicit.stat_1263695895@T2` | -1.13729 |
| `explicit.stat_2463230181@T2` | -0.99568 |
| `explicit.stat_1509134228@T1` | -0.95578 |
| `explicit.stat_3695891184@T2` | -0.95176 |
| `explicit.stat_1368271171@T2` | -0.93640 |
| `explicit.stat_210067635@T2` | -0.91826 |
| `explicit.stat_3695891184@T1` | -0.90805 |
| `explicit.stat_709508406@T1` | 0.87698 |

### weapon.crossbow — n=16855, R²=-1.6889

intercept: `4.0538`  ·  log_price: True  ·  ilvl: `-0.04902`  ·  n_mods: `-0.08820`  ·  n_top_tier: `0.38709`  ·  corrupted: `0.08305`  ·  n_sockets: `0.07703`  ·  quality: `0.02990`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.59091 |
| `explicit.stat_1202301673@T1` | 1.39239 |
| `explicit.stat_1980802737` | 1.37794 |
| `explicit.stat_2250681686@T2` | -1.30755 |
| `explicit.stat_2250681686` | 0.96877 |
| `explicit.stat_1509134228@T1` | 0.92323 |
| `crafted.stat_3035140377` | 0.85057 |
| `explicit.stat_709508406@T1` | 0.69748 |
| `explicit.stat_3695891184@T1` | -0.68659 |
| `explicit.stat_3336890334@T2` | -0.66009 |
| `explicit.stat_3695891184@T2` | -0.62472 |
| `explicit.stat_1037193709@T2` | -0.52628 |

### weapon.warstaff — n=11671, R²=-0.3459

intercept: `-10.4378`  ·  log_price: True  ·  ilvl: `0.14012`  ·  n_mods: `-0.20241`  ·  n_top_tier: `0.39222`  ·  corrupted: `0.17392`  ·  n_sockets: `0.12754`  ·  quality: `0.05667`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.15161 |
| `desecrated.stat_2527686725@T1` | 1.03205 |
| `desecrated.stat_2231156303@T1` | 1.03205 |
| `explicit.stat_328541901@T2` | -1.01046 |
| `explicit.stat_328541901@T1` | -0.92624 |
| `rune.stat_243313994` | 0.92554 |
| `desecrated.stat_9187492` | 0.78803 |
| `explicit.stat_1037193709@T1` | 0.64880 |
| `explicit.stat_691932474@T2` | -0.63216 |
| `explicit.stat_1368271171@T1` | -0.61168 |
| `explicit.stat_821021828@T2` | -0.54001 |
| `explicit.stat_2694482655@T1` | 0.51559 |

### weapon.staff — n=11058, R²=-0.3542

intercept: `-16.1173`  ·  log_price: True  ·  ilvl: `0.20663`  ·  n_mods: `-0.08115`  ·  n_top_tier: `0.41778`  ·  corrupted: `0.83858`  ·  n_sockets: `0.20240`  ·  quality: `0.03218`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.04935 |
| `explicit.stat_591105508@T1` | 2.02286 |
| `explicit.stat_1545858329@T1` | 1.86617 |
| `explicit.stat_124131830@T1` | 1.75104 |
| `explicit.stat_2254480358@T1` | 1.64569 |
| `explicit.stat_1600707273@T1` | 1.34289 |
| `explicit.stat_293638271@T2` | -1.01269 |
| `explicit.stat_3962278098@T2` | 0.82219 |
| `explicit.stat_2254480358@T2` | 0.75892 |
| `explicit.stat_1263695895@T2` | -0.74161 |
| `explicit.stat_4226189338@T2` | 0.65059 |
| `explicit.stat_473429811@T2` | -0.61705 |

### weapon.sceptre — n=10859, R²=-0.3355

intercept: `-21.8618`  ·  log_price: True  ·  ilvl: `0.27685`  ·  n_mods: `0.04391`  ·  n_top_tier: `0.10109`  ·  corrupted: `0.12739`  ·  n_sockets: `0.22082`  ·  quality: `0.03121`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.61336 |
| `explicit.stat_3057012405@T1` | 1.52118 |
| `explicit.stat_2162097452@T2` | 1.31338 |
| `explicit.stat_101878827@T2` | 0.97776 |
| `explicit.stat_1263695895@T2` | -0.94385 |
| `explicit.stat_101878827@T1` | 0.93709 |
| `explicit.stat_1798257884@T2` | 0.87128 |
| `explicit.stat_849987426@T1` | 0.80321 |
| `explicit.stat_1263695895@T1` | -0.79673 |
| `explicit.stat_2854751904@T2` | -0.78483 |
| `explicit.stat_1998951374@T1` | 0.64804 |
| `explicit.stat_2347036682@T1` | 0.46089 |

### weapon.spear — n=8799, R²=-0.3743

intercept: `-13.6896`  ·  log_price: True  ·  ilvl: `0.18725`  ·  n_mods: `-0.13080`  ·  n_top_tier: `0.57012`  ·  corrupted: `-0.62626`  ·  n_sockets: `0.23157`  ·  quality: `0.07458`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -4.68870 |
| `crafted.stat_210067635@T2` | -3.03186 |
| `explicit.stat_1202301673@T1` | 1.47152 |
| `explicit.stat_9187492@T1` | 1.37099 |
| `explicit.stat_1940865751@T2` | -1.01124 |
| `desecrated.stat_210067635@T1` | -1.00095 |
| `crafted.stat_3035140377` | 0.90569 |
| `explicit.stat_691932474@T2` | -0.86253 |
| `explicit.stat_4080418644@T2` | -0.85395 |
| `explicit.stat_1509134228@T1` | 0.85206 |
| `explicit.stat_748522257@T2` | -0.74284 |
| `explicit.stat_691932474@T1` | -0.69968 |

### armour.focus — n=7198, R²=-0.3327

intercept: `-16.0947`  ·  log_price: True  ·  ilvl: `0.20382`  ·  n_mods: `-0.11408`  ·  n_top_tier: `0.93688`  ·  corrupted: `0.15216`  ·  n_sockets: `0.31725`  ·  quality: `0.02510`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.56908 |
| `explicit.stat_4220027924@T1` | -1.52973 |
| `explicit.stat_2923486259@T2` | -1.25058 |
| `explicit.stat_4220027924@T2` | -1.19268 |
| `explicit.stat_2768835289@T1` | -1.08922 |
| `explicit.stat_2231156303@T2` | -1.08557 |
| `explicit.stat_2339757871@T2` | -1.03732 |
| `explicit.stat_4015621042@T1` | -1.02897 |
| `explicit.stat_1050105434@T2` | -1.00102 |
| `explicit.stat_737908626@T2` | -0.97610 |
| `explicit.stat_3291658075@T1` | -0.96536 |
| `explicit.stat_2231156303@T1` | -0.96277 |

### armour.quiver — n=6707, R²=-0.2994

intercept: `-16.5141`  ·  log_price: True  ·  ilvl: `0.19727`  ·  n_mods: `-0.06339`  ·  n_top_tier: `0.75114`  ·  corrupted: `0.95400`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.06254 |
| `explicit.stat_681332047@T2` | -1.50453 |
| `explicit.stat_681332047@T1` | -1.18936 |
| `explicit.stat_1573130764@T2` | -1.05153 |
| `explicit.stat_2463230181@T1` | 1.00891 |
| `explicit.stat_1573130764@T1` | -0.92504 |
| `explicit.stat_803737631@T1` | -0.74908 |
| `explicit.stat_4067062424@T1` | -0.73948 |
| `explicit.stat_4067062424@T2` | -0.70547 |
| `explicit.stat_803737631@T2` | -0.67938 |
| `explicit.stat_2321178454@T2` | -0.67771 |
| `explicit.stat_2194114101@T2` | -0.66681 |

### armour.shield — n=5785, R²=-0.4207

intercept: `-14.0345`  ·  log_price: True  ·  ilvl: `0.18426`  ·  n_mods: `-0.09161`  ·  n_top_tier: `0.49895`  ·  corrupted: `-0.37694`  ·  n_sockets: `0.43462`  ·  quality: `0.05137`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.12936 |
| `explicit.stat_2339757871@T1` | -1.06458 |
| `explicit.stat_3676141501@T1` | 1.05453 |
| `explicit.stat_3321629045@T2` | -1.02994 |
| `explicit.stat_1301765461@T2` | -1.00482 |
| `explicit.stat_4095671657@T2` | -0.97419 |
| `explicit.stat_1011760251@T1` | -0.94071 |
| `explicit.stat_2481353198@T1` | -0.88787 |
| `explicit.stat_2923486259@T1` | -0.82807 |
| `explicit.stat_4220027924@T1` | -0.82759 |
| `explicit.stat_4095671657@T1` | -0.81979 |
| `explicit.stat_2481353198@T2` | -0.75393 |

### weapon.twomace — n=5293, R²=-0.4544

intercept: `-11.2809`  ·  log_price: True  ·  ilvl: `0.14983`  ·  n_mods: `-0.18496`  ·  n_top_tier: `0.39368`  ·  corrupted: `0.53433`  ·  n_sockets: `0.14454`  ·  quality: `0.06695`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.95388 |
| `explicit.stat_1037193709@T1` | -1.46418 |
| `explicit.stat_3336890334@T1` | -1.31467 |
| `explicit.stat_1263695895@T2` | -1.15719 |
| `explicit.stat_9187492@T1` | -0.98598 |
| `explicit.stat_2694482655@T1` | 0.90042 |
| `explicit.stat_3695891184@T1` | -0.77293 |
| `explicit.stat_691932474@T1` | -0.73399 |
| `explicit.stat_518292764@T1` | 0.70323 |
| `explicit.stat_3695891184@T2` | -0.70190 |
| `explicit.stat_1263695895@T1` | -0.67445 |
| `explicit.stat_387439868@T2` | -0.60411 |

## Coverage (listings per base)

- … **Sapphire** — 35132 listings (35076 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 34252 listings (34210 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 26198 listings (26167 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 12394 listings (12376 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11264 listings (11240 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10884 listings (10859 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 10781 listings (10770 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10146 listings (10124 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10081 listings (10059 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 9609 listings (9596 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8368 listings (8353 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8038 listings (8029 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 7955 listings (7946 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7251 listings (7229 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6918 listings (6911 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 6910 listings (6891 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6856 listings (6842 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6809 listings (6802 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6765 listings (6737 priced) [0.3–398912568423.8 ex]
- … **Ancestral Tiara** — 6683 listings (6654 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6635 listings (6626 priced) [0.2–275252424.7 ex]
- … **Bloodstone Amulet** — 6593 listings (6583 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6277 listings (6274 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6161 listings (6147 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6002 listings (5992 priced) [0.3–398912568423.8 ex]

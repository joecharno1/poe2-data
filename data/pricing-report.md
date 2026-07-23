# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-23T21:28:38+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **755147** (752721 priced in exalted)
- Distinct bases: 1004 · distinct mods: 3357 · mod rows: 3567265
- Sold signals: **23967** sold · 430039 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-23T04:08:28+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.52** (median |log error| 3.1146)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 80% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×65.96 · ±30% 4% · n=110005
- Premium segment (60ex+): skill **+0.12** · typical error ×343.13 · ±30% 0% · n=72967

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 16355 | ×40.56 | 21% | +0.04 | +0.06 |
| jewel | 15900 | ×48.89 | 20% | +0.02 | +0.04 |
| accessory.amulet | 14678 | ×25.21 | 16% | +0.04 | +0.04 |
| accessory.belt | 10274 | ×24.95 | 21% | +0.04 | +0.06 |
| armour.chest | 9980 | ×18.07 | 21% | +0.08 | +0.11 |
| armour.helmet | 9733 | ×26.25 | 18% | +0.08 | +0.11 |
| armour.boots | 8968 | ×23.78 | 18% | +0.11 | +0.13 |
| armour.gloves | 8826 | ×33.67 | 13% | +0.09 | +0.11 |
| other | 8770 | ×1.84 | 42% | +0.18 | +0.25 |
| weapon.wand | 5136 | ×35.96 | 13% | +0.13 | +0.13 |
| weapon.bow | 4042 | ×24.39 | 11% | +0.17 | +0.20 |
| weapon.crossbow | 3798 | ×23.56 | 10% | +0.14 | +0.19 |
| weapon.warstaff | 2646 | ×13.27 | 7% | +0.15 | +0.15 |
| weapon.staff | 2549 | ×16.09 | 6% | +0.13 | +0.14 |
| weapon.sceptre | 2524 | ×16.95 | 5% | +0.07 | +0.07 |
| weapon.spear | 2014 | ×12.96 | 6% | +0.12 | +0.16 |
| armour.focus | 1674 | ×13.49 | 6% | +0.10 | +0.11 |
| armour.quiver | 1568 | ×17.43 | 7% | +0.12 | +0.12 |
| armour.shield | 1290 | ×7.73 | 7% | +0.11 | +0.11 |
| flask.charm | 1279 | ×10.00 | 27% | +0.03 | +0.03 |
| weapon.twomace | 1181 | ×8.91 | 7% | +0.09 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=87455, R²=-1.8843

intercept: `-0.1073`  ·  log_price: True  ·  ilvl: `0.00132`  ·  n_mods: `0.84877`  ·  n_top_tier: `-0.73871`  ·  corrupted: `0.93861`  ·  quality: `-0.06422`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 2.51967 |
| `explicit.stat_1604736568@T1` | -1.75860 |
| `explicit.stat_274716455@T1` | -1.67538 |
| `explicit.stat_1604736568` | 1.67007 |
| `explicit.stat_3556824919@T1` | 1.22066 |
| `explicit.stat_2194114101@T1` | -0.84004 |
| `explicit.stat_587431675@T1` | -0.78133 |
| `explicit.stat_681332047@T1` | -0.68329 |
| `explicit.stat_3714003708@T1` | 0.56053 |
| `explicit.stat_2023107756@T1` | -0.47753 |
| `explicit.stat_2023107756` | 0.36963 |
| `explicit.stat_3174700878@T1` | 0.34143 |

### accessory.ring — n=74621, R²=-2.0197

intercept: `3.1703`  ·  log_price: True  ·  ilvl: `-0.03995`  ·  n_mods: `0.00148`  ·  n_top_tier: `0.90050`  ·  corrupted: `0.00024`  ·  n_sockets: `2.23217`  ·  quality: `0.00357`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -0.96173 |
| `explicit.stat_1263695895@T2` | -0.94244 |
| `explicit.stat_1573130764@T2` | -0.94155 |
| `explicit.stat_4080418644@T1` | -0.92466 |
| `explicit.stat_1263695895@T1` | -0.92350 |
| `explicit.stat_3917489142@T2` | -0.92327 |
| `explicit.stat_2901986750@T2` | -0.92314 |
| `explicit.stat_2891184298@T1` | -0.91897 |
| `explicit.stat_3032590688@T1` | -0.91829 |
| `explicit.stat_1754445556@T1` | -0.91716 |
| `explicit.stat_2891184298@T2` | -0.91701 |
| `explicit.stat_3695891184@T1` | -0.91696 |

### other — n=71932, R²=-0.6764

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.12055`  ·  n_top_tier: `0.22602`  ·  corrupted: `-0.00002`  ·  n_sockets: `-0.00005`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_718638445` | 0.36169 |
| `implicit.stat_3182714256` | 0.36168 |
| `explicit.stat_1050105434@T1` | -0.35064 |
| `explicit.stat_3299347043@T1` | -0.23406 |
| `implicit.stat_2219129443` | 0.21819 |
| `explicit.stat_2974417149@T1` | 0.16409 |
| `explicit.stat_3917489142@T1` | -0.15640 |
| `implicit.stat_958696139` | -0.12054 |
| `implicit.stat_1416292992` | -0.08037 |
| `implicit.stat_3879011313` | 0.05421 |
| `explicit.stat_789117908@T1` | -0.05302 |
| `implicit.stat_3032590688` | -0.04821 |

### accessory.amulet — n=66800, R²=-2.067

intercept: `2.9784`  ·  log_price: True  ·  ilvl: `-0.03982`  ·  n_mods: `0.00077`  ·  n_top_tier: `0.94496`  ·  corrupted: `0.09996`  ·  n_sockets: `-0.08065`  ·  quality: `0.07034`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T2` | -1.57857 |
| `explicit.stat_3299347043@T1` | -1.54489 |
| `explicit.stat_2866361420@T1` | -1.09648 |
| `explicit.stat_2974417149@T1` | -1.09226 |
| `explicit.stat_2974417149@T2` | -1.07799 |
| `explicit.stat_4080418644@T1` | -1.07344 |
| `explicit.stat_2901986750@T1` | -1.06242 |
| `explicit.stat_2866361420@T2` | -1.05959 |
| `explicit.stat_1050105434@T1` | -1.04205 |
| `explicit.stat_803737631@T1` | -1.03059 |
| `explicit.stat_1050105434@T2` | -1.02388 |
| `explicit.stat_1202301673@T2` | -1.02199 |

### accessory.belt — n=47001, R²=-1.8548

intercept: `3.1304`  ·  log_price: True  ·  ilvl: `-0.03802`  ·  n_mods: `-0.01513`  ·  n_top_tier: `0.83262`  ·  corrupted: `1.11693`  ·  n_sockets: `1.52864`

| stat_id | coef |
|---|---|
| `explicit.stat_915769802@T1` | -0.85875 |
| `explicit.stat_3299347043@T2` | -0.85350 |
| `explicit.stat_2881298780@T1` | -0.85206 |
| `explicit.stat_809229260@T2` | -0.84772 |
| `explicit.stat_51994685@T1` | -0.84739 |
| `explicit.stat_1570770415@T2` | -0.84622 |
| `explicit.stat_3372524247@T2` | -0.84350 |
| `explicit.stat_3325883026@T1` | -0.83886 |
| `explicit.stat_915769802@T2` | -0.83784 |
| `explicit.stat_2881298780@T2` | -0.83641 |
| `explicit.stat_3299347043@T1` | -0.83573 |
| `explicit.stat_1570770415@T1` | -0.83301 |

### armour.chest — n=46647, R²=-1.7792

intercept: `3.3694`  ·  log_price: True  ·  ilvl: `-0.04129`  ·  n_mods: `-0.01746`  ·  n_top_tier: `0.38693`  ·  corrupted: `0.28189`  ·  n_sockets: `0.03125`  ·  quality: `0.07588`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.06974 |
| `explicit.stat_986397080@T2` | -0.43776 |
| `explicit.stat_4080418644@T2` | -0.42863 |
| `explicit.stat_1692879867@T2` | -0.41949 |
| `explicit.stat_986397080@T1` | -0.41830 |
| `explicit.stat_3484657501@T1` | -0.41793 |
| `explicit.stat_4080418644@T1` | -0.41577 |
| `explicit.stat_915769802@T2` | -0.41568 |
| `explicit.stat_915769802@T1` | -0.41369 |
| `explicit.stat_1999113824@T1` | -0.41310 |
| `explicit.stat_2451402625@T2` | -0.41165 |
| `explicit.stat_1062208444@T2` | -0.41009 |

### armour.helmet — n=45343, R²=-1.7451

intercept: `3.3370`  ·  log_price: True  ·  ilvl: `-0.04180`  ·  n_mods: `-0.02429`  ·  n_top_tier: `0.52967`  ·  corrupted: `0.64776`  ·  n_sockets: `0.07171`  ·  quality: `0.07127`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.84669 |
| `explicit.stat_1263695895@T1` | -0.81909 |
| `explicit.stat_3917489142@T2` | -0.73267 |
| `explicit.stat_3917489142@T1` | -0.67943 |
| `explicit.stat_2162097452@T2` | -0.67722 |
| `explicit.stat_4052037485@T2` | -0.62468 |
| `explicit.stat_4015621042@T2` | -0.61784 |
| `explicit.stat_1263695895@T2` | -0.60402 |
| `explicit.stat_4052037485@T1` | -0.58704 |
| `explicit.stat_803737631@T1` | -0.57857 |
| `explicit.stat_3321629045@T2` | -0.57803 |
| `explicit.stat_1999113824@T1` | -0.57383 |

### armour.boots — n=41817, R²=-1.6974

intercept: `3.7267`  ·  log_price: True  ·  ilvl: `-0.04581`  ·  n_mods: `-0.03153`  ·  n_top_tier: `0.43122`  ·  corrupted: `0.05065`  ·  n_sockets: `0.05859`  ·  quality: `0.07473`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.43201 |
| `explicit.stat_2250533757@T1` | 1.75133 |
| `crafted.stat_3917489142@T1` | 1.40428 |
| `explicit.stat_3299347043@T1` | -0.59231 |
| `explicit.stat_2923486259@T1` | 0.52397 |
| `explicit.stat_2923486259@T2` | -0.51445 |
| `explicit.stat_3917489142@T2` | -0.50357 |
| `explicit.stat_1874553720@T1` | -0.48837 |
| `explicit.stat_328541901@T2` | -0.48027 |
| `explicit.stat_2160282525@T1` | -0.47954 |
| `explicit.stat_1671376347@T2` | -0.47951 |
| `explicit.stat_1062208444@T2` | -0.47764 |

### armour.gloves — n=40814, R²=-1.6825

intercept: `3.9819`  ·  log_price: True  ·  ilvl: `-0.05179`  ·  n_mods: `-0.01068`  ·  n_top_tier: `0.71992`  ·  corrupted: `-0.04639`  ·  n_sockets: `0.18176`  ·  quality: `0.05981`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 1.45993 |
| `rune.stat_201332984` | 1.33185 |
| `explicit.stat_4052037485@T1` | -1.06682 |
| `explicit.stat_4052037485@T2` | -0.98759 |
| `explicit.stat_2923486259@T1` | -0.98085 |
| `explicit.stat_4015621042@T2` | -0.92542 |
| `explicit.stat_3484657501@T2` | -0.89349 |
| `explicit.stat_3321629045@T2` | -0.88670 |
| `explicit.stat_9187492@T2` | -0.87861 |
| `explicit.stat_3917489142@T2` | -0.86670 |
| `explicit.stat_3484657501@T1` | -0.86562 |
| `explicit.stat_803737631@T1` | -0.86308 |

### weapon.wand — n=23846, R²=-1.8269

intercept: `4.1345`  ·  log_price: True  ·  ilvl: `-0.05105`  ·  n_mods: `-0.07381`  ·  n_top_tier: `0.69214`  ·  corrupted: `0.24286`  ·  n_sockets: `0.02867`  ·  quality: `0.03099`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.19689 |
| `explicit.stat_2254480358@T1` | 2.64027 |
| `explicit.stat_1545858329@T1` | 2.59478 |
| `explicit.stat_591105508@T1` | 2.03473 |
| `explicit.stat_4226189338@T1` | 1.95278 |
| `explicit.stat_124131830@T1` | 1.89180 |
| `explicit.stat_2254480358@T2` | 1.23059 |
| `crafted.stat_124131830` | 1.21712 |
| `explicit.stat_1263695895@T2` | -1.09905 |
| `explicit.stat_473429811@T1` | -0.99426 |
| `explicit.stat_1600707273@T1` | 0.97803 |
| `explicit.stat_473429811@T2` | -0.95206 |

### flask.charm — n=21206, R²=-0.6722

intercept: `0.1081`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.69296`  ·  corrupted: `1.55006`  ·  quality: `0.01463`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.59545 |
| `explicit.stat_1056492907` | 2.53879 |
| `explicit.stat_3246948616` | 2.30233 |
| `explicit.stat_2541588185@T1` | 1.59522 |
| `explicit.stat_2365392475@T1` | 0.91659 |
| `explicit.stat_2676834156@T1` | 0.91553 |
| `explicit.stat_1120862500@T1` | 0.91541 |
| `explicit.stat_828533480@T2` | -0.69299 |
| `explicit.stat_1873752457@T2` | -0.69297 |
| `explicit.stat_1120862500@T2` | -0.69296 |
| `explicit.stat_388617051@T2` | -0.69294 |
| `explicit.stat_2365392475@T2` | -0.69289 |

### weapon.bow — n=19036, R²=-1.7357

intercept: `3.9874`  ·  log_price: True  ·  ilvl: `-0.04709`  ·  n_mods: `-0.09887`  ·  n_top_tier: `0.74201`  ·  corrupted: `0.56126`  ·  n_sockets: `0.04384`  ·  quality: `0.03466`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 6.45946 |
| `desecrated.stat_210067635@T1` | -1.70655 |
| `explicit.stat_1263695895@T1` | -1.40587 |
| `crafted.stat_210067635@T2` | -1.34148 |
| `explicit.stat_1263695895@T2` | -1.21359 |
| `crafted.stat_3035140377` | 1.19530 |
| `explicit.stat_2463230181@T2` | -1.17852 |
| `explicit.stat_210067635@T2` | -0.96449 |
| `explicit.stat_1509134228@T1` | -0.93768 |
| `explicit.stat_3695891184@T1` | -0.90823 |
| `explicit.stat_709508406@T2` | -0.88848 |
| `explicit.stat_1368271171@T1` | -0.87672 |

### weapon.crossbow — n=17828, R²=-1.5221

intercept: `4.0991`  ·  log_price: True  ·  ilvl: `-0.04711`  ·  n_mods: `-0.13792`  ·  n_top_tier: `0.31444`  ·  corrupted: `-0.00994`  ·  n_sockets: `0.11932`  ·  quality: `0.02133`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.73243 |
| `explicit.stat_1980802737` | 1.48349 |
| `explicit.stat_1202301673@T1` | 1.30600 |
| `explicit.stat_2250681686@T2` | -1.13939 |
| `explicit.stat_2250681686` | 1.04017 |
| `explicit.stat_1509134228@T1` | 0.96066 |
| `explicit.stat_709508406@T1` | 0.92865 |
| `crafted.stat_3035140377` | 0.82623 |
| `explicit.stat_210067635@T2` | -0.67704 |
| `explicit.stat_3695891184@T1` | -0.65195 |
| `explicit.stat_3695891184@T2` | -0.64897 |
| `explicit.stat_3336890334@T2` | -0.64195 |

### weapon.warstaff — n=12691, R²=-0.3356

intercept: `-9.9757`  ·  log_price: True  ·  ilvl: `0.13630`  ·  n_mods: `-0.24252`  ·  n_top_tier: `0.50603`  ·  corrupted: `0.33252`  ·  n_sockets: `0.14090`  ·  quality: `0.05501`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.02538 |
| `explicit.stat_328541901@T2` | -0.83164 |
| `explicit.stat_210067635@T1` | -0.81180 |
| `desecrated.stat_9187492` | 0.79620 |
| `explicit.stat_328541901@T1` | -0.78132 |
| `explicit.stat_1037193709@T2` | -0.76341 |
| `explicit.stat_1940865751@T1` | -0.76076 |
| `rune.stat_243313994` | 0.70062 |
| `explicit.stat_821021828@T2` | -0.61884 |
| `explicit.stat_1940865751@T2` | -0.58297 |
| `crafted.stat_3035140377` | 0.56951 |
| `desecrated.stat_3291658075@T1` | -0.54081 |

### weapon.staff — n=12092, R²=-0.3486

intercept: `-16.6765`  ·  log_price: True  ·  ilvl: `0.21522`  ·  n_mods: `-0.12345`  ·  n_top_tier: `0.52228`  ·  corrupted: `0.80646`  ·  n_sockets: `0.18720`  ·  quality: `0.03579`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 1.92123 |
| `explicit.stat_124131830@T1` | 1.67769 |
| `explicit.stat_4226189338@T1` | 1.64711 |
| `explicit.stat_1600707273@T1` | 1.52503 |
| `rune.stat_124131830` | 1.08820 |
| `explicit.stat_1545858329@T1` | 1.02499 |
| `explicit.stat_3962278098@T2` | 0.78890 |
| `explicit.stat_473429811@T2` | -0.78888 |
| `explicit.stat_591105508@T2` | 0.76281 |
| `explicit.stat_2768835289@T2` | -0.71986 |
| `explicit.stat_293638271@T2` | -0.71003 |
| `explicit.stat_2254480358@T2` | -0.67367 |

### weapon.sceptre — n=11739, R²=-0.3327

intercept: `-21.9054`  ·  log_price: True  ·  ilvl: `0.27917`  ·  n_mods: `-0.03105`  ·  n_top_tier: `0.17712`  ·  corrupted: `0.18473`  ·  n_sockets: `0.23527`  ·  quality: `0.03254`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.47937 |
| `explicit.stat_2162097452@T2` | 1.01686 |
| `explicit.stat_4080418644@T2` | -0.94735 |
| `explicit.stat_3057012405@T1` | 0.91597 |
| `explicit.stat_1798257884@T2` | 0.85237 |
| `explicit.stat_101878827@T1` | 0.66262 |
| `explicit.stat_4080418644@T1` | -0.51218 |
| `explicit.stat_2854751904@T2` | -0.50528 |
| `explicit.stat_101878827@T2` | 0.48960 |
| `explicit.stat_849987426@T1` | 0.45854 |
| `explicit.stat_1050105434@T1` | 0.39269 |
| `explicit.stat_1250712710@T2` | 0.38570 |

### weapon.spear — n=9546, R²=-0.374

intercept: `-14.4954`  ·  log_price: True  ·  ilvl: `0.19631`  ·  n_mods: `-0.16168`  ·  n_top_tier: `0.55254`  ·  corrupted: `-0.49988`  ·  n_sockets: `0.20751`  ·  quality: `0.07004`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.40508 |
| `desecrated.stat_666077204@T1` | -1.75880 |
| `explicit.stat_1037193709@T1` | -1.36743 |
| `crafted.stat_3035140377` | 1.14424 |
| `desecrated.stat_210067635@T1` | -1.04852 |
| `explicit.stat_9187492@T2` | -1.02972 |
| `explicit.stat_4080418644@T2` | -0.98576 |
| `explicit.stat_4080418644@T1` | -0.97554 |
| `explicit.stat_1202301673@T1` | 0.92566 |
| `explicit.stat_748522257@T2` | -0.90755 |
| `explicit.stat_1940865751@T2` | -0.88077 |
| `explicit.stat_3336890334@T2` | -0.88069 |

### armour.focus — n=7812, R²=-0.3311

intercept: `-16.4268`  ·  log_price: True  ·  ilvl: `0.20920`  ·  n_mods: `-0.18096`  ·  n_top_tier: `0.97779`  ·  corrupted: `0.01832`  ·  n_sockets: `0.44244`  ·  quality: `0.02412`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.72343 |
| `explicit.stat_4220027924@T1` | -1.44886 |
| `explicit.stat_3962278098@T2` | -1.36418 |
| `explicit.stat_2923486259@T2` | -1.26920 |
| `explicit.stat_2231156303@T1` | -1.23232 |
| `explicit.stat_2768835289@T1` | -1.22891 |
| `explicit.stat_2339757871@T2` | -1.22273 |
| `explicit.stat_4220027924@T2` | -1.14667 |
| `crafted.stat_2974417149@T1` | 1.11382 |
| `explicit.stat_2231156303@T2` | -1.10564 |
| `explicit.stat_3291658075@T2` | -1.07267 |
| `explicit.stat_4015621042@T1` | -1.06952 |

### armour.quiver — n=7275, R²=-0.2698

intercept: `-18.2369`  ·  log_price: True  ·  ilvl: `0.22024`  ·  n_mods: `-0.03864`  ·  n_top_tier: `0.67206`  ·  corrupted: `1.05942`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 4.91561 |
| `explicit.stat_681332047@T2` | -1.32041 |
| `explicit.stat_681332047@T1` | -1.13481 |
| `explicit.stat_1573130764@T2` | -0.98913 |
| `explicit.stat_2194114101@T2` | -0.81079 |
| `explicit.stat_1573130764@T1` | -0.75895 |
| `explicit.stat_2321178454@T2` | -0.65143 |
| `explicit.stat_3261801346@T1` | -0.59652 |
| `explicit.stat_803737631@T1` | -0.59231 |
| `explicit.stat_4067062424@T1` | -0.58176 |
| `explicit.stat_4067062424@T2` | -0.57992 |
| `explicit.stat_3714003708@T2` | -0.57019 |

### armour.shield — n=6256, R²=-0.3957

intercept: `-13.0928`  ·  log_price: True  ·  ilvl: `0.17739`  ·  n_mods: `-0.17656`  ·  n_top_tier: `0.62011`  ·  corrupted: `-0.66382`  ·  n_sockets: `0.32408`  ·  quality: `0.04479`

| stat_id | coef |
|---|---|
| `explicit.stat_4095671657@T1` | -1.73291 |
| `explicit.stat_3855016469@T1` | -1.60090 |
| `explicit.stat_4095671657@T2` | -1.37477 |
| `explicit.stat_1011760251@T1` | -1.31202 |
| `explicit.stat_328541901@T1` | -1.22641 |
| `explicit.stat_3033371881@T2` | -1.19599 |
| `explicit.stat_2901986750@T1` | -1.12760 |
| `explicit.stat_2923486259@T1` | -1.09320 |
| `explicit.stat_328541901@T2` | -1.04824 |
| `explicit.stat_4052037485@T1` | -1.02572 |
| `explicit.stat_3321629045@T2` | -0.89114 |
| `explicit.stat_2901986750@T2` | -0.85980 |

### weapon.twomace — n=5710, R²=-0.4372

intercept: `-11.0632`  ·  log_price: True  ·  ilvl: `0.15140`  ·  n_mods: `-0.21692`  ·  n_top_tier: `0.45917`  ·  corrupted: `0.95423`  ·  n_sockets: `0.18709`  ·  quality: `0.05501`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -6.02144 |
| `desecrated.stat_1509134228@T1` | 3.19399 |
| `explicit.stat_1037193709@T1` | -1.28554 |
| `explicit.stat_9187492@T1` | -1.16511 |
| `explicit.stat_3336890334@T1` | -1.15366 |
| `explicit.stat_1263695895@T2` | -1.03180 |
| `explicit.stat_2694482655@T1` | 0.86072 |
| `explicit.stat_518292764@T2` | -0.69294 |
| `explicit.stat_3695891184@T2` | -0.66381 |
| `explicit.stat_3695891184@T1` | -0.60280 |
| `explicit.stat_387439868@T2` | -0.58720 |
| `explicit.stat_210067635@T1` | -0.58129 |

## Coverage (listings per base)

- … **Sapphire** — 40148 listings (40081 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 39029 listings (38976 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 29908 listings (29876 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 13426 listings (13406 priced) [0.2–398916549611043.2 ex]
- … **Prismatic Ring** — 12479 listings (12452 priced) [0.2–398916549611043.2 ex]
- … **Solar Amulet** — 12121 listings (12095 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 11979 listings (11964 priced) [0.2–398916545621877.7 ex]
- … **Gold Amulet** — 11281 listings (11254 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 11219 listings (11196 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 10595 listings (10582 priced) [0.3–398916549611043.2 ex]
- … **Sapphire Ring** — 9268 listings (9253 priced) [0.2–398916549611043.2 ex]
- … **Topaz Ring** — 8957 listings (8946 priced) [0.3–398916549611043.2 ex]
- … **Ruby Ring** — 8861 listings (8851 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7724 listings (7700 priced) [0.3–398916553600208.8 ex]
- … **Unset Ring** — 7682 listings (7660 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7626 listings (7618 priced) [0.3–398916549611043.2 ex]
- … **Jade Amulet** — 7589 listings (7573 priced) [0.3–398916545621877.7 ex]
- … **Amber Amulet** — 7524 listings (7515 priced) [0.3–3985176410.3 ex]
- … **Pearl Ring** — 7419 listings (7410 priced) [0.2–398916549611043.2 ex]
- … **Plate Belt** — 7360 listings (7328 priced) [0.3–398916553600208.8 ex]
- … **Ancestral Tiara** — 7301 listings (7268 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 7268 listings (7256 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6939 listings (6935 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6871 listings (6856 priced) [0.3–398916549611043.2 ex]
- … **Heavy Belt** — 6472 listings (6456 priced) [0.3–398916553600208.8 ex]

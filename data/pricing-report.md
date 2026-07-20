# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-20T11:11:57+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **679942** (677828 priced in exalted)
- Distinct bases: 998 · distinct mods: 3302 · mod rows: 3218775
- Sold signals: **24402** sold · 386604 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-20T10:58:14+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×20.10** (median |log error| 3.0007)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.15** · typical error ×62.15 · ±30% 5% · n=99080
- Premium segment (60ex+): skill **+0.14** · typical error ×317.98 · ±30% 0% · n=66605

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 14446 | ×52.66 | 21% | +0.03 | +0.06 |
| jewel | 13711 | ×10.04 | 5% | +0.11 | +0.13 |
| accessory.amulet | 12993 | ×30.30 | 17% | +0.04 | +0.04 |
| accessory.belt | 9395 | ×19.99 | 26% | +0.01 | +0.03 |
| armour.chest | 8986 | ×16.53 | 22% | +0.08 | +0.09 |
| armour.helmet | 8873 | ×26.90 | 19% | +0.07 | +0.10 |
| armour.boots | 8201 | ×28.61 | 20% | +0.10 | +0.12 |
| armour.gloves | 8019 | ×36.53 | 16% | +0.08 | +0.10 |
| other | 7983 | ×1.60 | 44% | +0.12 | +0.19 |
| weapon.wand | 4786 | ×43.14 | 14% | +0.10 | +0.12 |
| weapon.bow | 3758 | ×25.13 | 12% | +0.16 | +0.17 |
| weapon.crossbow | 3524 | ×28.08 | 15% | +0.11 | +0.15 |
| weapon.warstaff | 2440 | ×15.43 | 7% | +0.21 | +0.21 |
| weapon.staff | 2304 | ×18.80 | 6% | +0.18 | +0.17 |
| weapon.sceptre | 2251 | ×21.54 | 5% | +0.09 | +0.10 |
| weapon.spear | 1824 | ×15.70 | 7% | +0.13 | +0.14 |
| armour.focus | 1516 | ×15.19 | 7% | +0.10 | +0.12 |
| armour.quiver | 1425 | ×19.65 | 7% | +0.17 | +0.18 |
| flask.charm | 1211 | ×13.02 | 27% | -0.00 | +0.01 |
| armour.shield | 1151 | ×11.02 | 7% | +0.10 | +0.12 |
| weapon.twomace | 1086 | ×8.71 | 8% | +0.11 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=75054, R²=-0.977

intercept: `-1.9462`  ·  log_price: True  ·  ilvl: `0.02443`  ·  n_mods: `0.85789`  ·  n_top_tier: `-0.28431`  ·  corrupted: `0.39959`  ·  quality: `-0.00106`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.58641 |
| `explicit.stat_3485067555@T1` | 2.38829 |
| `explicit.stat_1594812856@T1` | 2.11889 |
| `explicit.stat_1569101201@T1` | -1.73592 |
| `explicit.stat_3780644166@T1` | -1.73511 |
| `explicit.stat_2523933828@T1` | -1.54673 |
| `explicit.stat_4147897060@T1` | -1.39635 |
| `explicit.stat_3174700878@T1` | 1.37440 |
| `explicit.stat_1869147066@T1` | -1.36010 |
| `explicit.stat_3374165039@T1` | -1.30804 |
| `explicit.stat_3714003708@T1` | 1.16179 |
| `explicit.stat_3759663284@T1` | -1.11397 |

### accessory.ring — n=65839, R²=-2.0417

intercept: `3.4469`  ·  log_price: True  ·  ilvl: `-0.04296`  ·  n_mods: `0.00209`  ·  n_top_tier: `1.06861`  ·  corrupted: `0.00921`  ·  n_sockets: `2.04494`  ·  quality: `0.02386`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.09925 |
| `explicit.stat_2231156303@T1` | -1.09343 |
| `explicit.stat_1573130764@T2` | -1.09328 |
| `explicit.stat_4080418644@T1` | -1.08892 |
| `explicit.stat_4220027924@T2` | -1.08713 |
| `explicit.stat_2923486259@T2` | -1.08443 |
| `explicit.stat_2891184298@T2` | -1.08324 |
| `explicit.stat_803737631@T1` | -1.08095 |
| `explicit.stat_736967255@T2` | -1.08052 |
| `explicit.stat_3291658075@T2` | -1.07986 |
| `explicit.stat_2144192055@T1` | -1.07958 |
| `explicit.stat_3325883026@T1` | -1.07876 |

### other — n=64786, R²=-0.6193

intercept: `1.6093`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.14279`  ·  n_top_tier: `0.20377`  ·  corrupted: `0.00736`  ·  n_sockets: `-0.00005`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_718638445` | 0.42844 |
| `implicit.stat_3182714256` | 0.42843 |
| `explicit.stat_1050105434@T1` | -0.26216 |
| `explicit.stat_3299347043@T1` | -0.22962 |
| `implicit.stat_2219129443` | 0.21597 |
| `implicit.stat_3879011313` | 0.18840 |
| `explicit.stat_2974417149@T1` | 0.18539 |
| `implicit.stat_4041853756` | 0.14307 |
| `implicit.stat_958696139` | -0.14278 |
| `explicit.stat_3917489142@T1` | -0.08746 |
| `implicit.stat_1416292992` | -0.06590 |
| `implicit.stat_3032590688` | -0.05710 |

### accessory.amulet — n=59364, R²=-2.1237

intercept: `3.3931`  ·  log_price: True  ·  ilvl: `-0.04267`  ·  n_mods: `-0.01682`  ·  n_top_tier: `1.29713`  ·  corrupted: `0.10003`  ·  n_sockets: `-0.14154`  ·  quality: `0.03355`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.87598 |
| `explicit.stat_3299347043@T2` | -1.74073 |
| `explicit.stat_587431675@T2` | -1.46990 |
| `explicit.stat_803737631@T1` | -1.42805 |
| `explicit.stat_2974417149@T1` | -1.40094 |
| `explicit.stat_2866361420@T2` | -1.39302 |
| `explicit.stat_1050105434@T2` | -1.37393 |
| `explicit.stat_2866361420@T1` | -1.36745 |
| `explicit.stat_803737631@T2` | -1.36171 |
| `explicit.stat_1050105434@T1` | -1.33843 |
| `explicit.stat_2901986750@T1` | -1.33526 |
| `explicit.stat_2974417149@T2` | -1.33411 |

### accessory.belt — n=42916, R²=-2.1538

intercept: `0.1015`  ·  log_price: True  ·  ilvl: `-0.00122`  ·  n_mods: `-0.00052`  ·  n_top_tier: `0.68905`  ·  corrupted: `0.52904`  ·  n_sockets: `1.60624`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -0.68982 |
| `explicit.stat_915769802@T1` | -0.68969 |
| `explicit.stat_3299347043@T2` | -0.68962 |
| `explicit.stat_2881298780@T1` | -0.68956 |
| `explicit.stat_4220027924@T2` | -0.68950 |
| `explicit.stat_3325883026@T1` | -0.68949 |
| `explicit.stat_51994685@T1` | -0.68941 |
| `explicit.stat_809229260@T2` | -0.68938 |
| `explicit.stat_1389754388@T1` | -0.68931 |
| `explicit.stat_3372524247@T2` | -0.68927 |
| `explicit.stat_915769802@T2` | -0.68916 |
| `explicit.stat_1570770415@T2` | -0.68911 |

### armour.chest — n=42482, R²=-1.7699

intercept: `3.3287`  ·  log_price: True  ·  ilvl: `-0.04110`  ·  n_mods: `-0.01490`  ·  n_top_tier: `0.33466`  ·  corrupted: `0.12710`  ·  n_sockets: `0.01887`  ·  quality: `0.07125`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.68619 |
| `explicit.stat_3981240776@T1` | 1.00099 |
| `explicit.stat_986397080@T2` | -0.43144 |
| `explicit.stat_986397080@T1` | -0.42669 |
| `explicit.stat_1692879867@T2` | -0.37329 |
| `explicit.stat_3484657501@T1` | -0.36925 |
| `explicit.stat_915769802@T2` | -0.36175 |
| `explicit.stat_4080418644@T1` | -0.36012 |
| `explicit.stat_4080418644@T2` | -0.35909 |
| `explicit.stat_2339757871@T2` | -0.35894 |
| `explicit.stat_2451402625@T1` | -0.35365 |
| `explicit.stat_1062208444@T2` | -0.34718 |

### armour.helmet — n=41364, R²=-1.7807

intercept: `3.2038`  ·  log_price: True  ·  ilvl: `-0.04050`  ·  n_mods: `-0.01500`  ·  n_top_tier: `0.49436`  ·  corrupted: `0.66720`  ·  n_sockets: `0.03748`  ·  quality: `0.06942`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.83410 |
| `explicit.stat_1263695895@T1` | -0.70144 |
| `explicit.stat_3917489142@T2` | -0.69816 |
| `explicit.stat_2162097452@T2` | -0.65555 |
| `explicit.stat_3917489142@T1` | -0.61486 |
| `explicit.stat_1263695895@T2` | -0.57033 |
| `explicit.stat_803737631@T1` | -0.53890 |
| `explicit.stat_1999113824@T1` | -0.52794 |
| `explicit.stat_803737631@T2` | -0.52769 |
| `explicit.stat_4052037485@T2` | -0.52220 |
| `explicit.stat_3321629045@T2` | -0.52108 |
| `explicit.stat_53045048@T1` | -0.51980 |

### armour.boots — n=38395, R²=-1.7134

intercept: `3.5877`  ·  log_price: True  ·  ilvl: `-0.04429`  ·  n_mods: `-0.02049`  ·  n_top_tier: `0.49102`  ·  corrupted: `0.08422`  ·  n_sockets: `0.04488`  ·  quality: `0.06777`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.77344 |
| `explicit.stat_2339757871@T1` | -1.48323 |
| `crafted.stat_3917489142@T1` | 1.41327 |
| `explicit.stat_2923486259@T1` | 0.74068 |
| `explicit.stat_3917489142@T2` | -0.60970 |
| `explicit.stat_3299347043@T1` | -0.60936 |
| `explicit.stat_1874553720@T1` | -0.55791 |
| `explicit.stat_2923486259@T2` | -0.54491 |
| `explicit.stat_1671376347@T2` | -0.53005 |
| `explicit.stat_124859000@T1` | -0.52984 |
| `explicit.stat_3321629045@T2` | -0.52638 |
| `explicit.stat_1999113824@T2` | -0.52296 |

### armour.gloves — n=37341, R²=-1.7133

intercept: `3.8825`  ·  log_price: True  ·  ilvl: `-0.05058`  ·  n_mods: `-0.01029`  ·  n_top_tier: `0.75369`  ·  corrupted: `-0.02116`  ·  n_sockets: `0.13599`  ·  quality: `0.05951`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.82031 |
| `rune.stat_201332984` | 1.21116 |
| `explicit.stat_4052037485@T1` | -1.00869 |
| `explicit.stat_2923486259@T1` | -1.00102 |
| `explicit.stat_3321629045@T2` | -0.97232 |
| `explicit.stat_4052037485@T2` | -0.95708 |
| `explicit.stat_3484657501@T2` | -0.95698 |
| `explicit.stat_9187492@T2` | -0.93292 |
| `explicit.stat_4015621042@T2` | -0.91857 |
| `explicit.stat_803737631@T1` | -0.88374 |
| `explicit.stat_803737631@T2` | -0.88247 |
| `explicit.stat_3484657501@T1` | -0.84973 |

### weapon.wand — n=22366, R²=-1.9096

intercept: `4.2084`  ·  log_price: True  ·  ilvl: `-0.05203`  ·  n_mods: `-0.06346`  ·  n_top_tier: `0.26658`  ·  corrupted: `-0.05251`  ·  n_sockets: `0.04769`  ·  quality: `0.03940`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -3.35083 |
| `explicit.stat_1545858329@T1` | 2.96698 |
| `explicit.stat_2254480358@T1` | 2.72206 |
| `explicit.stat_124131830@T1` | 2.51459 |
| `explicit.stat_591105508@T1` | 2.12238 |
| `explicit.stat_4226189338@T1` | 2.01206 |
| `explicit.stat_736967255@T2` | 1.94163 |
| `explicit.stat_1600707273@T1` | 1.65761 |
| `explicit.stat_2254480358@T2` | 1.31700 |
| `crafted.stat_124131830` | 1.29096 |
| `explicit.stat_4226189338@T2` | 1.18723 |
| `explicit.stat_1263695895@T2` | -0.78042 |

### flask.charm — n=18899, R²=-0.65

intercept: `0.1072`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.60941`  ·  corrupted: `1.46227`  ·  quality: `0.00796`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60511 |
| `explicit.stat_1056492907` | 2.67711 |
| `explicit.stat_828533480@T2` | -1.60943 |
| `explicit.stat_1120862500@T2` | -1.60943 |
| `explicit.stat_1873752457@T2` | -1.60940 |
| `explicit.stat_3196823591@T2` | -1.60936 |
| `explicit.stat_2365392475@T2` | -1.60935 |
| `explicit.stat_2676834156@T2` | -1.60779 |
| `explicit.stat_1873752457@T1` | -1.60500 |
| `explicit.stat_388617051@T2` | -1.60050 |
| `explicit.stat_828533480@T1` | -1.59817 |
| `explicit.stat_2541588185@T2` | -1.59040 |

### weapon.bow — n=17859, R²=-1.7318

intercept: `3.9325`  ·  log_price: True  ·  ilvl: `-0.04642`  ·  n_mods: `-0.10080`  ·  n_top_tier: `0.74773`  ·  corrupted: `0.66505`  ·  n_sockets: `0.09502`  ·  quality: `0.02487`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.76919 |
| `explicit.stat_1263695895@T1` | -1.32147 |
| `crafted.stat_3035140377` | 1.26946 |
| `explicit.stat_3336890334@T1` | 1.19401 |
| `explicit.stat_1263695895@T2` | -1.16221 |
| `explicit.stat_1509134228@T1` | -0.99377 |
| `explicit.stat_3695891184@T2` | -0.88887 |
| `explicit.stat_2463230181@T2` | -0.87845 |
| `explicit.stat_1368271171@T2` | -0.85760 |
| `explicit.stat_3695891184@T1` | -0.84463 |
| `explicit.stat_3639275092@T1` | -0.83694 |
| `explicit.stat_210067635@T2` | -0.83043 |

### weapon.crossbow — n=16745, R²=-1.7512

intercept: `4.0988`  ·  log_price: True  ·  ilvl: `-0.05026`  ·  n_mods: `-0.06032`  ·  n_top_tier: `0.39585`  ·  corrupted: `0.09915`  ·  n_sockets: `0.07261`  ·  quality: `0.03639`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.66463 |
| `explicit.stat_1202301673@T1` | 1.54280 |
| `explicit.stat_2250681686@T2` | -1.49721 |
| `explicit.stat_1980802737` | 1.32521 |
| `explicit.stat_2250681686` | 1.15505 |
| `crafted.stat_3035140377` | 0.79491 |
| `explicit.stat_1509134228@T1` | 0.76157 |
| `explicit.stat_709508406@T1` | 0.73726 |
| `explicit.stat_3336890334@T2` | -0.60501 |
| `explicit.stat_1263695895@T2` | -0.58953 |
| `explicit.stat_3695891184@T1` | -0.57786 |
| `explicit.stat_1037193709@T1` | -0.55542 |

### weapon.warstaff — n=11541, R²=-0.3501

intercept: `-10.4299`  ·  log_price: True  ·  ilvl: `0.14023`  ·  n_mods: `-0.20403`  ·  n_top_tier: `0.38223`  ·  corrupted: `0.36960`  ·  n_sockets: `0.13463`  ·  quality: `0.05655`

| stat_id | coef |
|---|---|
| `desecrated.stat_473429811@T1` | -2.53031 |
| `desecrated.stat_3291658075@T1` | -2.53031 |
| `desecrated.stat_2527686725@T1` | 1.69289 |
| `desecrated.stat_2231156303@T1` | 1.69289 |
| `crafted.stat_210067635@T2` | 1.25264 |
| `explicit.stat_328541901@T2` | -0.92059 |
| `explicit.stat_328541901@T1` | -0.88751 |
| `explicit.stat_1368271171@T1` | -0.79998 |
| `desecrated.stat_9187492` | 0.79103 |
| `rune.stat_243313994` | 0.71061 |
| `explicit.stat_1509134228@T1` | 0.67463 |
| `explicit.stat_691932474@T2` | -0.65046 |

### weapon.staff — n=10933, R²=-0.3607

intercept: `-15.9028`  ·  log_price: True  ·  ilvl: `0.20443`  ·  n_mods: `-0.06584`  ·  n_top_tier: `0.37762`  ·  corrupted: `0.77580`  ·  n_sockets: `0.20049`  ·  quality: `0.03531`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.24447 |
| `explicit.stat_591105508@T1` | 2.16873 |
| `explicit.stat_1545858329@T1` | 1.95504 |
| `explicit.stat_124131830@T1` | 1.75905 |
| `explicit.stat_1600707273@T1` | 1.47530 |
| `explicit.stat_2254480358@T1` | 1.37470 |
| `explicit.stat_293638271@T2` | -1.07540 |
| `explicit.stat_2254480358@T2` | 0.91221 |
| `explicit.stat_3962278098@T2` | 0.82366 |
| `explicit.stat_1600707273@T2` | 0.70855 |
| `explicit.stat_4226189338@T2` | 0.69918 |
| `explicit.stat_591105508@T2` | 0.64117 |

### weapon.sceptre — n=10750, R²=-0.3339

intercept: `-21.2351`  ·  log_price: True  ·  ilvl: `0.26964`  ·  n_mods: `0.02512`  ·  n_top_tier: `0.09063`  ·  corrupted: `0.14433`  ·  n_sockets: `0.22435`  ·  quality: `0.03308`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.41838 |
| `explicit.stat_3057012405@T1` | 1.37211 |
| `explicit.stat_1263695895@T2` | -1.31554 |
| `explicit.stat_2162097452@T2` | 1.25817 |
| `explicit.stat_1263695895@T1` | -1.03960 |
| `explicit.stat_1798257884@T2` | 0.93959 |
| `explicit.stat_101878827@T2` | 0.92555 |
| `explicit.stat_849987426@T1` | 0.92279 |
| `explicit.stat_101878827@T1` | 0.91595 |
| `explicit.stat_2854751904@T2` | -0.76135 |
| `explicit.stat_1998951374@T1` | 0.71586 |
| `explicit.stat_289128254@T1` | 0.63437 |

### weapon.spear — n=8710, R²=-0.3693

intercept: `-13.8796`  ·  log_price: True  ·  ilvl: `0.18861`  ·  n_mods: `-0.12089`  ·  n_top_tier: `0.62199`  ·  corrupted: `-0.54373`  ·  n_sockets: `0.24749`  ·  quality: `0.07807`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.45298 |
| `desecrated.stat_666077204@T1` | -3.60519 |
| `explicit.stat_1202301673@T1` | 1.23193 |
| `explicit.stat_9187492@T1` | 1.21715 |
| `explicit.stat_4080418644@T2` | -1.14533 |
| `explicit.stat_1940865751@T2` | -1.13049 |
| `explicit.stat_1509134228@T1` | 1.12359 |
| `desecrated.stat_210067635@T1` | -1.05310 |
| `explicit.stat_691932474@T1` | -0.93465 |
| `explicit.stat_691932474@T2` | -0.87196 |
| `explicit.stat_748522257@T2` | -0.86067 |
| `crafted.stat_3035140377` | 0.81109 |

### armour.focus — n=7114, R²=-0.3485

intercept: `-16.0900`  ·  log_price: True  ·  ilvl: `0.20367`  ·  n_mods: `-0.11254`  ·  n_top_tier: `1.02764`  ·  corrupted: `0.09282`  ·  n_sockets: `0.35120`  ·  quality: `0.02668`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 6.25032 |
| `explicit.stat_4220027924@T1` | -1.76987 |
| `explicit.stat_2923486259@T1` | -1.75192 |
| `explicit.stat_274716455@T1` | -1.35959 |
| `explicit.stat_2923486259@T2` | -1.31226 |
| `explicit.stat_4220027924@T2` | -1.30464 |
| `explicit.stat_2231156303@T2` | -1.22530 |
| `explicit.stat_2231156303@T1` | -1.18021 |
| `explicit.stat_4015621042@T1` | -1.14696 |
| `explicit.stat_2339757871@T2` | -1.10242 |
| `explicit.stat_1050105434@T2` | -1.06473 |
| `explicit.stat_274716455@T2` | -1.06382 |

### armour.quiver — n=6631, R²=-0.29

intercept: `-16.9767`  ·  log_price: True  ·  ilvl: `0.20584`  ·  n_mods: `-0.12011`  ·  n_top_tier: `0.67922`  ·  corrupted: `0.88922`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.08826 |
| `explicit.stat_2463230181@T1` | 2.07254 |
| `explicit.stat_681332047@T2` | -1.39716 |
| `explicit.stat_1573130764@T1` | -1.25730 |
| `explicit.stat_2463230181@T2` | 1.14104 |
| `explicit.stat_681332047@T1` | -1.11747 |
| `explicit.stat_1573130764@T2` | -1.07005 |
| `explicit.stat_4067062424@T1` | -0.93669 |
| `explicit.stat_803737631@T1` | -0.84440 |
| `explicit.stat_4067062424@T2` | -0.82551 |
| `explicit.stat_2321178454@T2` | -0.75818 |
| `explicit.stat_803737631@T2` | -0.66044 |

### armour.shield — n=5728, R²=-0.4112

intercept: `-13.9237`  ·  log_price: True  ·  ilvl: `0.18480`  ·  n_mods: `-0.11893`  ·  n_top_tier: `0.44418`  ·  corrupted: `-0.40872`  ·  n_sockets: `0.46700`  ·  quality: `0.05690`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.25312 |
| `explicit.stat_2339757871@T1` | -1.04112 |
| `explicit.stat_3321629045@T2` | -0.95574 |
| `explicit.stat_4095671657@T2` | -0.86881 |
| `explicit.stat_1011760251@T1` | -0.86418 |
| `explicit.stat_2481353198@T1` | -0.77598 |
| `explicit.stat_2901986750@T1` | -0.76079 |
| `explicit.stat_3484657501@T1` | -0.75021 |
| `explicit.stat_3033371881@T2` | -0.72959 |
| `explicit.stat_2923486259@T1` | -0.72124 |
| `explicit.stat_3676141501@T1` | 0.71591 |
| `explicit.stat_2451402625@T1` | -0.69186 |

### weapon.twomace — n=5243, R²=-0.4419

intercept: `-10.9332`  ·  log_price: True  ·  ilvl: `0.14692`  ·  n_mods: `-0.20096`  ·  n_top_tier: `0.28919`  ·  corrupted: `0.58501`  ·  n_sockets: `0.15131`  ·  quality: `0.06591`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.35922 |
| `explicit.stat_1037193709@T1` | -1.39200 |
| `explicit.stat_1263695895@T2` | -1.19195 |
| `explicit.stat_2694482655@T1` | 1.16803 |
| `explicit.stat_3336890334@T1` | -1.02431 |
| `explicit.stat_518292764@T1` | 0.90665 |
| `explicit.stat_9187492@T1` | -0.81721 |
| `explicit.stat_1509134228@T1` | 0.76473 |
| `explicit.stat_691932474@T1` | -0.75526 |
| `explicit.stat_3695891184@T1` | -0.71412 |
| `explicit.stat_387439868@T1` | -0.68825 |
| `explicit.stat_387439868@T2` | -0.66757 |

## Coverage (listings per base)

- … **Sapphire** — 34601 listings (34545 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 33676 listings (33634 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 25811 listings (25780 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 12284 listings (12266 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11133 listings (11109 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10735 listings (10710 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 10652 listings (10641 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10012 listings (9990 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9922 listings (9900 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 9504 listings (9491 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8246 listings (8231 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7938 listings (7929 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 7834 listings (7825 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7194 listings (7172 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6849 listings (6842 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 6796 listings (6777 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6766 listings (6752 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6727 listings (6720 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6690 listings (6662 priced) [0.3–398912568423.8 ex]
- … **Ancestral Tiara** — 6616 listings (6587 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6540 listings (6531 priced) [0.2–275252424.7 ex]
- … **Bloodstone Amulet** — 6520 listings (6510 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6212 listings (6209 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6087 listings (6073 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5939 listings (5929 priced) [0.3–398912568423.8 ex]

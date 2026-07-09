# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-09T15:34:23+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **379282** (378647 priced in exalted)
- Distinct bases: 963 · distinct mods: 2928 · mod rows: 1801124
- Sold signals: **28670** sold · 202558 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-09T15:15:35+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×18.81** (median |log error| 2.9342)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 77% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.07** · typical error ×42.52 · ±30% 13% · n=55831
- Premium segment (60ex+): skill **+0.08** · typical error ×146.31 · ±30% 0% · n=35497

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 7339 | ×13.41 | 4% | +0.05 | +0.07 |
| accessory.amulet | 6941 | ×50.77 | 20% | +0.02 | +0.02 |
| jewel | 6601 | ×8.10 | 8% | +0.01 | +0.04 |
| accessory.belt | 5432 | ×10.00 | 20% | +0.02 | +0.02 |
| armour.chest | 5291 | ×10.00 | 23% | +0.01 | +0.01 |
| armour.helmet | 5202 | ×14.99 | 20% | +0.01 | +0.02 |
| armour.boots | 4912 | ×11.88 | 19% | +0.01 | +0.04 |
| armour.gloves | 4790 | ×25.80 | 18% | +0.00 | +0.01 |
| other | 4516 | ×10.00 | 35% | +0.08 | +0.20 |
| weapon.wand | 3162 | ×45.95 | 18% | +0.06 | +0.05 |
| weapon.bow | 2528 | ×27.58 | 17% | +0.09 | +0.12 |
| weapon.crossbow | 2382 | ×21.98 | 18% | +0.10 | +0.14 |
| weapon.warstaff | 1302 | ×92.98 | 14% | +0.07 | +0.08 |
| weapon.staff | 1214 | ×57.67 | 13% | +0.07 | +0.08 |
| weapon.sceptre | 1188 | ×61.91 | 10% | +0.08 | +0.09 |
| weapon.spear | 1001 | ×60.00 | 16% | +0.05 | +0.06 |
| armour.focus | 827 | ×74.54 | 13% | +0.07 | +0.14 |
| armour.quiver | 780 | ×69.14 | 13% | +0.03 | +0.09 |
| armour.shield | 629 | ×30.00 | 15% | +0.04 | +0.05 |
| flask.charm | 625 | ×20.00 | 34% | +0.01 | +0.01 |
| weapon.twomace | 586 | ×20.00 | 13% | +0.06 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=38006, R²=-0.4641

intercept: `1.6075`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `0.00625`  ·  n_top_tier: `0.68288`  ·  corrupted: `1.16999`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 3.65606 |
| `explicit.stat_2106365538@T1` | 3.36740 |
| `explicit.stat_2482852589@T1` | 3.30935 |
| `explicit.stat_1589917703@T1` | 2.69697 |
| `explicit.stat_101878827@T1` | 2.56153 |
| `explicit.stat_1050105434@T1` | -1.22169 |
| `explicit.stat_3917489142@T1` | 1.13422 |
| `explicit.stat_3141070085@T1` | -1.10374 |
| `explicit.stat_789117908@T1` | -0.95452 |
| `explicit.stat_2974417149@T1` | 0.91812 |
| `explicit.stat_2891184298@T1` | 0.44469 |
| `implicit.stat_1379411836` | -0.25613 |

### jewel — n=35658, R²=-0.6772

intercept: `-1.2468`  ·  log_price: True  ·  ilvl: `0.03531`  ·  n_mods: `0.22830`  ·  n_top_tier: `-0.04708`  ·  corrupted: `0.32328`  ·  quality: `0.22309`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -5.02000 |
| `explicit.stat_3780644166@T1` | -3.34747 |
| `explicit.stat_1569101201@T1` | 3.21068 |
| `explicit.stat_3741323227@T1` | -3.00588 |
| `explicit.stat_3485067555@T1` | 2.65801 |
| `explicit.stat_1316278494@T1` | -2.52368 |
| `explicit.stat_1315743832@T1` | 2.07651 |
| `explicit.stat_3714003708@T1` | -2.07041 |
| `explicit.stat_234296660@T1` | -2.04091 |
| `explicit.stat_2527686725@T1` | 1.81759 |
| `explicit.stat_795138349@T1` | -1.79811 |
| `explicit.stat_3374165039@T1` | -1.64798 |

### accessory.ring — n=33669, R²=-1.2042

intercept: `3.8345`  ·  log_price: True  ·  ilvl: `-0.04087`  ·  n_mods: `-0.02678`  ·  n_top_tier: `-0.00992`  ·  corrupted: `0.97543`  ·  n_sockets: `0.96473`  ·  quality: `0.01189`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 3.13375 |
| `explicit.stat_707457662@T2` | 3.08127 |
| `explicit.stat_1379411836@T1` | -0.97816 |
| `explicit.stat_1573130764@T1` | -0.95454 |
| `explicit.stat_2557965901@T1` | 0.89553 |
| `explicit.stat_2557965901@T2` | 0.79961 |
| `explicit.stat_2923486259@T1` | 0.72768 |
| `explicit.stat_2923486259@T2` | 0.72691 |
| `explicit.stat_1263695895@T1` | -0.71037 |
| `explicit.stat_1368271171@T1` | -0.70030 |
| `explicit.stat_1379411836@T2` | -0.62768 |
| `explicit.stat_1368271171@T2` | -0.59309 |

### accessory.amulet — n=31594, R²=-2.0866

intercept: `4.1778`  ·  log_price: True  ·  ilvl: `-0.05040`  ·  n_mods: `-0.02865`  ·  n_top_tier: `1.04564`  ·  corrupted: `0.15303`  ·  n_sockets: `0.88738`  ·  quality: `-0.00274`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.26882 |
| `explicit.stat_983749596@T2` | -1.22687 |
| `explicit.stat_472520716@T1` | -1.16912 |
| `explicit.stat_3299347043@T1` | -1.15786 |
| `explicit.stat_472520716@T2` | -1.14470 |
| `explicit.stat_2748665614@T2` | -1.14300 |
| `explicit.stat_3917489142@T2` | -1.13640 |
| `explicit.stat_3299347043@T2` | -1.12824 |
| `explicit.stat_2748665614@T1` | -1.12680 |
| `explicit.stat_3917489142@T1` | -1.12410 |
| `explicit.stat_587431675@T1` | -1.11912 |
| `explicit.stat_2106365538@T1` | -1.09666 |

### accessory.belt — n=25031, R²=-0.1622

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.00127`  ·  corrupted: `0.00005`  ·  n_sockets: `-0.69311`

| stat_id | coef |
|---|---|
| `explicit.stat_2639966148` | 0.13738 |
| `pseudo.total_ele_res>=80` | 0.06391 |
| `explicit.stat_174664100` | 0.05466 |
| `explicit.stat_3811191316` | 0.04985 |
| `explicit.stat_770672621` | 0.03353 |
| `pseudo.total_chaos_res` | 0.02377 |
| `explicit.stat_2923486259` | -0.02377 |
| `explicit.stat_3742865955` | 0.02291 |
| `explicit.stat_2957407601` | 0.01920 |
| `explicit.stat_1485480327` | 0.01500 |
| `explicit.stat_1389754388@T1` | -0.00129 |
| `explicit.stat_51994685@T1` | -0.00129 |

### armour.chest — n=24753, R²=-0.28

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.02728`  ·  corrupted: `0.00009`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 0.09197 |
| `desecrated.stat_4220027924` | -0.04130 |
| `implicit.stat_3372524247` | -0.03719 |
| `implicit.stat_1671376347` | -0.03719 |
| `pseudo.total_ele_res` | 0.03719 |
| `implicit.stat_4220027924` | -0.03719 |
| `explicit.stat_1671376347` | -0.03719 |
| `explicit.stat_3372524247` | -0.03719 |
| `explicit.stat_4220027924` | -0.03719 |
| `rune.stat_4220027924` | -0.03719 |
| `rune.stat_1671376347` | -0.03719 |
| `desecrated.stat_3372524247` | -0.03719 |

### armour.helmet — n=24220, R²=-0.3035

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.23849`  ·  corrupted: `1.60931`  ·  n_sockets: `0.00001`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.81937 |
| `explicit.stat_3362812763@T2` | -0.23853 |
| `explicit.stat_1263695895@T1` | -0.23852 |
| `explicit.stat_2451402625@T1` | -0.23852 |
| `explicit.stat_53045048@T2` | -0.23852 |
| `explicit.stat_803737631@T2` | -0.23851 |
| `explicit.stat_4080418644@T2` | -0.23851 |
| `explicit.stat_4080418644@T1` | -0.23850 |
| `explicit.stat_53045048@T1` | -0.23850 |
| `explicit.stat_1263695895@T2` | -0.23850 |
| `explicit.stat_3917489142@T2` | -0.23849 |
| `explicit.stat_3362812763@T1` | -0.23849 |

### armour.boots — n=22742, R²=-0.3353

intercept: `2.7108`  ·  log_price: True  ·  ilvl: `-0.00783`  ·  n_mods: `-0.05475`  ·  n_top_tier: `0.28678`  ·  corrupted: `0.16697`  ·  n_sockets: `0.01172`  ·  quality: `0.00282`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.71442 |
| `explicit.stat_1062208444@T2` | -0.67247 |
| `desecrated.stat_2250533757@T2` | -0.41040 |
| `explicit.stat_2451402625@T2` | -0.37412 |
| `explicit.stat_3261801346@T2` | -0.35301 |
| `explicit.stat_1999113824@T1` | -0.34810 |
| `explicit.stat_1999113824@T2` | -0.33743 |
| `explicit.stat_2923486259@T2` | -0.33330 |
| `explicit.stat_1671376347@T2` | -0.33025 |
| `explicit.stat_2923486259@T1` | -0.32869 |
| `explicit.stat_3917489142@T2` | -0.32404 |
| `explicit.stat_1062208444@T1` | -0.32310 |

### armour.gloves — n=22130, R²=-0.3942

intercept: `2.5971`  ·  log_price: True  ·  ilvl: `-0.00821`  ·  n_mods: `-0.05232`  ·  n_top_tier: `0.16287`  ·  corrupted: `0.14080`  ·  n_sockets: `0.04690`  ·  quality: `0.00881`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T2` | -0.31205 |
| `explicit.stat_803737631@T2` | -0.29882 |
| `explicit.stat_2339757871@T1` | 0.26222 |
| `explicit.stat_681332047@T2` | -0.24720 |
| `explicit.stat_2451402625@T2` | -0.22944 |
| `explicit.stat_2797971005@T2` | -0.21904 |
| `explicit.stat_3695891184@T1` | -0.21695 |
| `explicit.stat_1573130764@T1` | -0.21371 |
| `explicit.stat_328541901@T2` | -0.20918 |
| `explicit.stat_328541901@T1` | -0.20632 |
| `explicit.stat_3695891184@T2` | -0.20628 |
| `explicit.stat_3033371881@T1` | -0.19181 |

### weapon.wand — n=14770, R²=-2.1017

intercept: `3.7969`  ·  log_price: True  ·  ilvl: `-0.04723`  ·  n_mods: `-0.00981`  ·  n_top_tier: `0.45623`  ·  corrupted: `-0.03056`  ·  n_sockets: `0.02887`  ·  quality: `0.00832`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 3.11432 |
| `explicit.stat_4226189338@T1` | 2.41870 |
| `explicit.stat_1545858329@T1` | 1.97136 |
| `explicit.stat_591105508@T1` | 1.90040 |
| `explicit.stat_1600707273@T1` | 1.76750 |
| `explicit.stat_124131830@T1` | 1.34721 |
| `explicit.stat_736967255@T2` | 1.01160 |
| `crafted.stat_124131830` | 0.93561 |
| `explicit.stat_4226189338@T2` | 0.53830 |
| `explicit.stat_3015669065@T1` | -0.52854 |
| `explicit.stat_2231156303@T2` | -0.51397 |
| `explicit.stat_3015669065@T2` | -0.49391 |

### weapon.bow — n=12055, R²=-1.9142

intercept: `3.4448`  ·  log_price: True  ·  ilvl: `-0.04238`  ·  n_mods: `-0.02280`  ·  n_top_tier: `0.66949`  ·  corrupted: `0.32656`  ·  n_sockets: `0.00559`  ·  quality: `0.01150`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 2.66161 |
| `desecrated.stat_210067635@T1` | -2.21001 |
| `rune.stat_3885405204` | -1.90959 |
| `explicit.stat_2463230181@T1` | 1.46401 |
| `crafted.stat_3035140377` | 1.41010 |
| `explicit.stat_1202301673@T1` | 1.29815 |
| `explicit.stat_55876295@T1` | -0.80024 |
| `explicit.stat_1037193709@T1` | -0.76866 |
| `explicit.stat_1037193709@T2` | -0.73866 |
| `explicit.stat_55876295@T2` | -0.72737 |
| `explicit.stat_3336890334@T2` | -0.72100 |
| `explicit.stat_2694482655@T1` | -0.71217 |

### weapon.crossbow — n=11322, R²=-1.8279

intercept: `3.5596`  ·  log_price: True  ·  ilvl: `-0.04395`  ·  n_mods: `-0.01734`  ·  n_top_tier: `0.70392`  ·  corrupted: `-0.01290`  ·  n_sockets: `0.02777`  ·  quality: `0.00220`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.84796 |
| `explicit.stat_2250681686@T2` | -1.43419 |
| `explicit.stat_709508406@T1` | 1.35324 |
| `explicit.stat_1202301673@T1` | 1.12505 |
| `explicit.stat_1980802737` | 1.10480 |
| `explicit.stat_1202301673@T2` | -1.01011 |
| `explicit.stat_1263695895@T2` | -0.90682 |
| `explicit.stat_1509134228@T2` | -0.89949 |
| `crafted.stat_3035140377` | 0.88709 |
| `explicit.stat_669069897@T1` | -0.76783 |
| `explicit.stat_1037193709@T2` | -0.76548 |
| `explicit.stat_2250681686` | 0.76093 |

### flask.charm — n=8820, R²=-0.4384

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.07405`  ·  corrupted: `0.69264`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.98821 |
| `explicit.stat_1056492907` | 3.40116 |
| `explicit.stat_2676834156@T1` | 1.53538 |
| `explicit.stat_2541588185@T1` | 0.40541 |
| `explicit.stat_2676834156@T2` | -0.07406 |
| `explicit.stat_388617051@T2` | -0.07406 |
| `explicit.stat_828533480@T2` | -0.07406 |
| `explicit.stat_1120862500@T2` | -0.07406 |
| `explicit.stat_1873752457@T2` | -0.07405 |
| `explicit.stat_828533480@T1` | -0.07405 |
| `explicit.stat_3196823591@T2` | -0.07405 |
| `explicit.stat_1873752457@T1` | -0.07405 |

### weapon.warstaff — n=6211, R²=-0.6012

intercept: `-0.0640`  ·  log_price: True  ·  ilvl: `0.00086`  ·  n_mods: `-0.00193`  ·  n_top_tier: `0.29458`  ·  corrupted: `0.18015`  ·  n_sockets: `0.00168`  ·  quality: `0.07002`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.23923 |
| `explicit.stat_9187492@T1` | 1.23250 |
| `rune.stat_731403740` | 1.04510 |
| `crafted.stat_210067635@T2` | -0.62815 |
| `desecrated.stat_9187492` | 0.55387 |
| `rune.stat_1712188793` | -0.41600 |
| `crafted.stat_3035140377` | 0.40548 |
| `explicit.stat_1509134228@T2` | 0.39047 |
| `explicit.stat_328541901@T1` | -0.30027 |
| `explicit.stat_1509134228@T1` | -0.29972 |
| `explicit.stat_328541901@T2` | -0.29903 |
| `explicit.stat_1940865751@T1` | -0.29666 |

### weapon.sceptre — n=5734, R²=-0.5754

intercept: `-5.2906`  ·  log_price: True  ·  ilvl: `0.06659`  ·  n_mods: `-0.04330`  ·  n_top_tier: `0.46019`  ·  corrupted: `1.16097`  ·  n_sockets: `0.13120`  ·  quality: `0.09492`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.98119 |
| `explicit.stat_4080418644@T1` | -0.74957 |
| `explicit.stat_4080418644@T2` | -0.68918 |
| `explicit.stat_1263695895@T2` | -0.62082 |
| `explicit.stat_1574590649@T2` | -0.60834 |
| `explicit.stat_1263695895@T1` | -0.60515 |
| `explicit.stat_2854751904@T1` | -0.58169 |
| `explicit.stat_2347036682@T2` | -0.56401 |
| `explicit.stat_328541901@T1` | -0.51530 |
| `explicit.stat_3639275092@T2` | -0.49360 |
| `explicit.stat_1998951374@T1` | -0.45922 |
| `explicit.stat_1050105434@T2` | -0.45785 |

### weapon.staff — n=5722, R²=-0.628

intercept: `-0.4607`  ·  log_price: True  ·  ilvl: `0.00571`  ·  n_mods: `-0.00026`  ·  n_top_tier: `0.12747`  ·  corrupted: `0.22009`  ·  n_sockets: `0.01772`  ·  quality: `0.01093`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 4.36204 |
| `rune.stat_124131830` | 4.24174 |
| `explicit.stat_2254480358@T1` | 1.88711 |
| `explicit.stat_1600707273@T1` | 1.78306 |
| `explicit.stat_2254480358@T2` | 1.54544 |
| `explicit.stat_1545858329@T1` | 1.46169 |
| `explicit.stat_124131830@T1` | 1.25576 |
| `explicit.stat_4226189338@T2` | 1.24187 |
| `explicit.stat_2768835289@T2` | 1.04259 |
| `explicit.stat_3291658075@T2` | 0.85758 |
| `explicit.stat_2231156303@T2` | 0.78737 |
| `explicit.stat_473429811@T1` | 0.57698 |

### weapon.spear — n=4820, R²=-0.6685

intercept: `-0.0596`  ·  log_price: True  ·  ilvl: `0.00078`  ·  n_mods: `-0.00021`  ·  n_top_tier: `0.32176`  ·  corrupted: `0.00107`  ·  n_sockets: `0.00179`  ·  quality: `0.07004`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.36907 |
| `explicit.stat_9187492@T1` | 1.29397 |
| `crafted.stat_3035140377` | 1.01237 |
| `explicit.stat_210067635@T1` | 0.77416 |
| `explicit.stat_3336890334@T1` | 0.71872 |
| `crafted.stat_518292764` | 0.64833 |
| `explicit.stat_1509134228@T1` | 0.58107 |
| `explicit.stat_709508406@T1` | 0.34297 |
| `explicit.stat_1263695895@T2` | -0.32315 |
| `explicit.stat_55876295@T1` | -0.32312 |
| `explicit.stat_4080418644@T2` | -0.32281 |
| `explicit.stat_691932474@T1` | -0.32269 |

### armour.focus — n=3864, R²=-0.5875

intercept: `-3.2469`  ·  log_price: True  ·  ilvl: `0.04003`  ·  n_mods: `-0.01205`  ·  n_top_tier: `0.81579`  ·  corrupted: `0.03233`  ·  n_sockets: `0.12592`  ·  quality: `0.08851`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 10.07881 |
| `crafted.stat_737908626@T2` | -7.67324 |
| `crafted.stat_2974417149@T1` | -3.21931 |
| `desecrated.stat_3393628375@T1` | 2.86628 |
| `explicit.stat_124131830@T2` | -0.93537 |
| `explicit.stat_4220027924@T2` | -0.91657 |
| `explicit.stat_3962278098@T2` | -0.88779 |
| `explicit.stat_2231156303@T2` | -0.88583 |
| `explicit.stat_2891184298@T2` | -0.88111 |
| `explicit.stat_789117908@T2` | -0.86879 |
| `explicit.stat_3291658075@T1` | -0.86785 |
| `explicit.stat_4052037485@T2` | -0.86293 |

### armour.quiver — n=3660, R²=-0.5928

intercept: `-2.3485`  ·  log_price: True  ·  ilvl: `0.02700`  ·  n_mods: `0.01875`  ·  n_top_tier: `0.77818`  ·  corrupted: `0.34491`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 11.07260 |
| `explicit.stat_2463230181@T2` | -1.16246 |
| `explicit.stat_681332047@T2` | -0.91175 |
| `explicit.stat_1573130764@T1` | -0.87747 |
| `explicit.stat_2194114101@T2` | -0.85602 |
| `explicit.stat_1573130764@T2` | -0.85277 |
| `explicit.stat_681332047@T1` | -0.83397 |
| `explicit.stat_1368271171@T2` | -0.83212 |
| `desecrated.stat_3932115504` | -0.81197 |
| `explicit.stat_2321178454@T2` | -0.80924 |
| `explicit.stat_1368271171@T1` | -0.79676 |
| `explicit.stat_3261801346@T1` | -0.79575 |

### armour.shield — n=3151, R²=-0.6196

intercept: `-0.4673`  ·  log_price: True  ·  ilvl: `0.00584`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.38653`  ·  corrupted: `0.16816`  ·  n_sockets: `0.00228`  ·  quality: `0.07308`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.87244 |
| `explicit.stat_1978899297@T2` | -0.55244 |
| `explicit.stat_328541901@T1` | -0.42095 |
| `explicit.stat_328541901@T2` | -0.41813 |
| `explicit.stat_2481353198@T2` | -0.41221 |
| `explicit.stat_2481353198@T1` | -0.41147 |
| `explicit.stat_2339757871@T1` | -0.40933 |
| `explicit.stat_1011760251@T2` | -0.40430 |
| `explicit.stat_4220027924@T1` | 0.40207 |
| `explicit.stat_3484657501@T1` | -0.39925 |
| `explicit.stat_3372524247@T2` | -0.39815 |
| `explicit.stat_1671376347@T1` | -0.39662 |

### weapon.twomace — n=2869, R²=-0.5697

intercept: `-1.4475`  ·  log_price: True  ·  ilvl: `0.01847`  ·  n_mods: `-0.00798`  ·  n_top_tier: `0.85048`  ·  corrupted: `0.70600`  ·  n_sockets: `0.03032`  ·  quality: `0.02070`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.97305 |
| `crafted.stat_3035140377` | 1.02963 |
| `explicit.stat_1037193709@T1` | -0.97926 |
| `explicit.stat_3336890334@T1` | -0.93823 |
| `explicit.stat_387439868@T2` | -0.92641 |
| `explicit.stat_1037193709@T2` | -0.92044 |
| `explicit.stat_3695891184@T1` | -0.89235 |
| `explicit.stat_709508406@T1` | -0.88616 |
| `explicit.stat_3639275092@T1` | -0.88287 |
| `explicit.stat_709508406@T2` | -0.87812 |
| `explicit.stat_3695891184@T2` | -0.87799 |
| `explicit.stat_821021828@T2` | -0.87195 |

## Coverage (listings per base)

- … **Sapphire** — 16869 listings (16844 priced) [0.4–7553463.8 ex]
- … **Emerald** — 16637 listings (16621 priced) [0.4–7553463.8 ex]
- … **Ruby** — 12791 listings (12779 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 7279 listings (7273 priced) [0.2–5288620.9 ex]
- … **Prismatic Ring** — 5844 listings (5838 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 5689 listings (5679 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 5570 listings (5567 priced) [0.2–4323655.9 ex]
- … **Stellar Amulet** — 5497 listings (5494 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 5367 listings (5358 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 5199 listings (5195 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 4674 listings (4664 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4365 listings (4360 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 4256 listings (4253 priced) [1.0–307202867.9 ex]
- … **Ruby Ring** — 4224 listings (4222 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 3843 listings (3838 priced) [0.2–5286174.1 ex]
- … **Lapis Amulet** — 3801 listings (3799 priced) [0.2–5286174.1 ex]
- … **Ancestral Tiara** — 3752 listings (3746 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3704 listings (3703 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3699 listings (3697 priced) [0.2–4547453.5 ex]
- … **Unset Ring** — 3586 listings (3585 priced) [0.2–24532814.5 ex]
- … **Obliterator Bow** — 3584 listings (3575 priced) [0.4–42622633798.0 ex]
- … **Heavy Belt** — 3554 listings (3553 priced) [0.2–4877938.3 ex]
- … **Bloodstone Amulet** — 3477 listings (3475 priced) [0.2–4275054.0 ex]
- … **Pearl Ring** — 3381 listings (3379 priced) [0.2–24532814.5 ex]
- … **Lunar Amulet** — 3320 listings (3318 priced) [0.4–4877938.3 ex]

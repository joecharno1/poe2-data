# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-16T19:13:30+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **557004** (555501 priced in exalted)
- Distinct bases: 986 · distinct mods: 3182 · mod rows: 2639295
- Sold signals: **25604** sold · 314157 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-16T19:02:25+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×25.89** (median |log error| 3.2539)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×61.11 · ±30% 5% · n=80581
- Premium segment (60ex+): skill **+0.14** · typical error ×243.11 · ±30% 0% · n=54416

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 11352 | ×54.30 | 22% | +0.04 | +0.06 |
| jewel | 10480 | ×10.50 | 4% | +0.07 | +0.10 |
| accessory.amulet | 10362 | ×50.83 | 20% | +0.03 | +0.04 |
| accessory.belt | 7797 | ×16.73 | 4% | +0.04 | +0.06 |
| armour.chest | 7576 | ×24.23 | 10% | +0.10 | +0.12 |
| armour.helmet | 7379 | ×21.87 | 7% | +0.12 | +0.14 |
| armour.boots | 6820 | ×38.05 | 16% | +0.10 | +0.13 |
| armour.gloves | 6720 | ×30.78 | 7% | +0.12 | +0.13 |
| other | 6308 | ×6.08 | 40% | +0.09 | +0.15 |
| weapon.wand | 4204 | ×42.16 | 17% | +0.08 | +0.09 |
| weapon.bow | 3322 | ×20.31 | 5% | +0.03 | +0.02 |
| weapon.crossbow | 3138 | ×27.22 | 16% | +0.09 | +0.14 |
| weapon.warstaff | 1991 | ×32.44 | 10% | +0.14 | +0.13 |
| weapon.staff | 1873 | ×51.91 | 9% | +0.11 | +0.11 |
| weapon.sceptre | 1848 | ×40.64 | 5% | +0.17 | +0.16 |
| weapon.spear | 1444 | ×46.53 | 15% | +0.08 | +0.09 |
| armour.focus | 1217 | ×30.98 | 6% | +0.14 | +0.17 |
| armour.quiver | 1165 | ×29.69 | 7% | +0.12 | +0.14 |
| flask.charm | 1010 | ×30.00 | 32% | +0.04 | +0.06 |
| armour.shield | 948 | ×23.19 | 9% | +0.04 | +0.06 |
| weapon.twomace | 892 | ×11.99 | 10% | +0.07 | +0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=57584, R²=-0.9269

intercept: `-1.7647`  ·  log_price: True  ·  ilvl: `0.02657`  ·  n_mods: `0.72257`  ·  n_top_tier: `-0.23871`  ·  corrupted: `0.24330`  ·  quality: `0.22370`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.84100 |
| `explicit.stat_2301718443@T1` | 3.10704 |
| `explicit.stat_1805182458@T1` | -1.91564 |
| `explicit.stat_3780644166@T1` | -1.90499 |
| `explicit.stat_3485067555@T1` | 1.85005 |
| `explicit.stat_627767961@T1` | -1.80850 |
| `explicit.stat_1697951953@T1` | -1.68538 |
| `explicit.stat_3668351662@T1` | -1.59497 |
| `explicit.stat_3166958180@T1` | -1.53293 |
| `explicit.stat_1062710370@T1` | -1.45412 |
| `explicit.stat_239367161@T1` | -1.38671 |
| `explicit.stat_2523933828@T1` | -1.38033 |

### other — n=53570, R²=-0.5702

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.47965`  ·  corrupted: `0.21349`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.52014 |
| `explicit.stat_789117908@T1` | -0.43612 |
| `explicit.stat_2974417149@T1` | 0.40604 |
| `explicit.stat_2106365538@T1` | -0.37419 |
| `explicit.stat_3299347043@T1` | -0.35986 |
| `explicit.stat_1050105434@T1` | -0.23281 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_736967255@T1` | -0.22513 |
| `explicit.stat_3917489142@T1` | 0.20516 |
| `explicit.stat_2482852589@T1` | -0.18265 |

### accessory.ring — n=51875, R²=-2.0239

intercept: `3.4810`  ·  log_price: True  ·  ilvl: `-0.04308`  ·  n_mods: `0.00063`  ·  n_top_tier: `0.98584`  ·  corrupted: `0.02090`  ·  n_sockets: `2.18520`  ·  quality: `0.07102`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | -1.03119 |
| `explicit.stat_1263695895@T2` | -1.01931 |
| `explicit.stat_2231156303@T1` | -1.01902 |
| `explicit.stat_1573130764@T1` | -1.01447 |
| `explicit.stat_1368271171@T2` | -1.01354 |
| `explicit.stat_803737631@T1` | -1.01039 |
| `explicit.stat_4220027924@T2` | -1.00604 |
| `explicit.stat_3291658075@T2` | -1.00574 |
| `explicit.stat_2144192055@T1` | -1.00561 |
| `explicit.stat_3291658075@T1` | -1.00358 |
| `explicit.stat_2231156303@T2` | -1.00307 |
| `explicit.stat_1368271171@T1` | -1.00101 |

### accessory.amulet — n=47562, R²=-2.146

intercept: `3.6989`  ·  log_price: True  ·  ilvl: `-0.04525`  ·  n_mods: `-0.02397`  ·  n_top_tier: `1.13822`  ·  corrupted: `0.09217`  ·  n_sockets: `-0.10376`  ·  quality: `-0.00293`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.27264 |
| `explicit.stat_587431675@T2` | -1.20605 |
| `explicit.stat_472520716@T2` | -1.20135 |
| `explicit.stat_803737631@T1` | -1.19445 |
| `explicit.stat_2974417149@T2` | -1.18823 |
| `explicit.stat_2974417149@T1` | -1.18732 |
| `explicit.stat_1050105434@T2` | -1.18679 |
| `explicit.stat_803737631@T2` | -1.18536 |
| `explicit.stat_2866361420@T2` | -1.18274 |
| `explicit.stat_472520716@T1` | -1.17217 |
| `explicit.stat_3917489142@T2` | -1.17156 |
| `explicit.stat_2866361420@T1` | -1.17034 |

### accessory.belt — n=35839, R²=-0.8585

intercept: `6.7183`  ·  log_price: True  ·  ilvl: `-0.06433`  ·  n_mods: `-0.35278`  ·  n_top_tier: `1.05130`  ·  corrupted: `1.07855`  ·  n_sockets: `-0.31075`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.50888 |
| `explicit.stat_2881298780@T1` | -1.45322 |
| `explicit.stat_3299347043@T1` | -1.44387 |
| `explicit.stat_3299347043@T2` | -1.40389 |
| `explicit.stat_4220027924@T2` | -1.37610 |
| `explicit.stat_644456512@T1` | -1.34242 |
| `explicit.stat_809229260@T2` | -1.26850 |
| `explicit.stat_51994685@T1` | -1.23621 |
| `explicit.stat_809229260@T1` | -1.12072 |
| `explicit.stat_1671376347@T2` | -1.11862 |
| `explicit.stat_4080418644@T2` | -1.10113 |
| `explicit.stat_3585532255@T2` | -1.05340 |

### armour.chest — n=35607, R²=-1.3171

intercept: `4.2228`  ·  log_price: True  ·  ilvl: `-0.04979`  ·  n_mods: `-0.08078`  ·  n_top_tier: `0.55779`  ·  corrupted: `0.17036`  ·  n_sockets: `0.16958`  ·  quality: `0.05301`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.89082 |
| `explicit.stat_986397080@T2` | -0.90105 |
| `explicit.stat_3981240776@T1` | 0.90015 |
| `explicit.stat_986397080@T1` | -0.82687 |
| `explicit.stat_3033371881@T1` | 0.77896 |
| `explicit.stat_3484657501@T1` | -0.77235 |
| `explicit.stat_1692879867@T2` | -0.68628 |
| `explicit.stat_915769802@T2` | -0.66625 |
| `explicit.stat_1999113824@T1` | -0.65784 |
| `explicit.stat_2339757871@T2` | -0.64798 |
| `explicit.stat_4015621042@T1` | -0.64132 |
| `explicit.stat_1692879867@T1` | -0.64119 |

### armour.helmet — n=34532, R²=-1.1293

intercept: `3.9291`  ·  log_price: True  ·  ilvl: `-0.04879`  ·  n_mods: `-0.09060`  ·  n_top_tier: `0.43726`  ·  corrupted: `0.71908`  ·  n_sockets: `0.19079`  ·  quality: `0.03880`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.00204 |
| `explicit.stat_3917489142@T2` | -0.93636 |
| `explicit.stat_1999113824@T1` | -0.78733 |
| `explicit.stat_3321629045@T2` | -0.70426 |
| `explicit.stat_1999113824@T2` | -0.68247 |
| `explicit.stat_2162097452@T2` | -0.62511 |
| `explicit.stat_53045048@T2` | -0.62342 |
| `explicit.stat_803737631@T1` | -0.60933 |
| `explicit.stat_1263695895@T2` | -0.60186 |
| `explicit.stat_587431675@T2` | -0.57767 |
| `explicit.stat_3917489142@T1` | -0.57536 |
| `explicit.stat_4052037485@T2` | -0.55436 |

### armour.boots — n=32269, R²=-1.4644

intercept: `4.0999`  ·  log_price: True  ·  ilvl: `-0.04961`  ·  n_mods: `-0.04950`  ·  n_top_tier: `0.61389`  ·  corrupted: `0.04913`  ·  n_sockets: `0.06295`  ·  quality: `0.04720`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.46273 |
| `explicit.stat_2250533757@T1` | 1.48721 |
| `explicit.stat_3299347043@T1` | -1.03408 |
| `explicit.stat_3917489142@T2` | -0.91868 |
| `explicit.stat_2923486259@T2` | -0.81856 |
| `explicit.stat_2339757871@T1` | -0.77962 |
| `explicit.stat_3917489142@T1` | -0.74056 |
| `explicit.stat_1999113824@T2` | -0.73857 |
| `explicit.stat_2160282525@T1` | -0.73433 |
| `explicit.stat_1062208444@T2` | -0.70552 |
| `explicit.stat_4052037485@T2` | -0.69484 |
| `explicit.stat_3484657501@T2` | -0.68584 |

### armour.gloves — n=31395, R²=-1.2795

intercept: `3.8712`  ·  log_price: True  ·  ilvl: `-0.04950`  ·  n_mods: `-0.05967`  ·  n_top_tier: `0.54361`  ·  corrupted: `0.03357`  ·  n_sockets: `0.18628`  ·  quality: `0.03538`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 4.37373 |
| `rune.stat_201332984` | -1.29884 |
| `explicit.stat_2923486259@T1` | -1.13648 |
| `explicit.stat_3484657501@T2` | -0.91569 |
| `explicit.stat_3321629045@T2` | -0.89626 |
| `explicit.stat_9187492@T1` | 0.84083 |
| `explicit.stat_803737631@T2` | -0.83882 |
| `explicit.stat_3484657501@T1` | -0.77868 |
| `rune.stat_836936635` | 0.76178 |
| `explicit.stat_803737631@T1` | -0.71478 |
| `explicit.stat_1671376347@T1` | 0.70904 |
| `explicit.stat_4052037485@T1` | -0.69204 |

### weapon.wand — n=19726, R²=-2.1762

intercept: `3.6396`  ·  log_price: True  ·  ilvl: `-0.04493`  ·  n_mods: `-0.02964`  ·  n_top_tier: `0.42847`  ·  corrupted: `0.00881`  ·  n_sockets: `0.05583`  ·  quality: `0.01207`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.48912 |
| `explicit.stat_2254480358@T1` | 2.38479 |
| `explicit.stat_1545858329@T1` | 2.30712 |
| `explicit.stat_4226189338@T1` | 2.05087 |
| `explicit.stat_591105508@T1` | 1.92198 |
| `explicit.stat_124131830@T1` | 1.85057 |
| `explicit.stat_736967255@T2` | 1.75645 |
| `explicit.stat_1600707273@T1` | 1.27283 |
| `crafted.stat_124131830` | 1.24767 |
| `explicit.stat_2254480358@T2` | 1.02293 |
| `explicit.stat_4226189338@T2` | 0.79772 |
| `explicit.stat_1263695895@T2` | -0.57837 |

### weapon.bow — n=15763, R²=-0.9139

intercept: `3.9673`  ·  log_price: True  ·  ilvl: `-0.03322`  ·  n_mods: `-0.23817`  ·  n_top_tier: `0.46971`  ·  corrupted: `0.42376`  ·  n_sockets: `0.09570`  ·  quality: `0.01266`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.03730 |
| `explicit.stat_1263695895@T1` | -1.57423 |
| `crafted.stat_3035140377` | 1.16722 |
| `explicit.stat_1263695895@T2` | -1.07611 |
| `explicit.stat_518292764@T2` | -1.01818 |
| `explicit.stat_1368271171@T2` | -1.01194 |
| `explicit.stat_3695891184@T1` | -0.99578 |
| `explicit.stat_3695891184@T2` | -0.93963 |
| `desecrated.stat_210067635@T1` | -0.85308 |
| `explicit.stat_3336890334@T1` | 0.84919 |
| `explicit.stat_1202301673@T1` | 0.79372 |
| `explicit.stat_3261801346@T2` | -0.77330 |

### weapon.crossbow — n=14849, R²=-1.8516

intercept: `3.6418`  ·  log_price: True  ·  ilvl: `-0.04422`  ·  n_mods: `-0.05413`  ·  n_top_tier: `0.77938`  ·  corrupted: `0.06352`  ·  n_sockets: `0.05294`  ·  quality: `0.01681`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.91792 |
| `explicit.stat_2250681686@T2` | -1.38803 |
| `explicit.stat_1980802737` | 1.15533 |
| `explicit.stat_1202301673@T1` | 1.14446 |
| `explicit.stat_1263695895@T2` | -0.98569 |
| `explicit.stat_1263695895@T1` | -0.97617 |
| `explicit.stat_1509134228@T2` | -0.95501 |
| `explicit.stat_2694482655@T1` | -0.92781 |
| `explicit.stat_709508406@T1` | 0.92756 |
| `crafted.stat_3035140377` | 0.92148 |
| `explicit.stat_709508406@T2` | -0.86962 |
| `explicit.stat_1037193709@T1` | -0.86307 |

### flask.charm — n=14646, R²=-0.5566

intercept: `0.0409`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `2.47605`  ·  corrupted: `1.76237`  ·  quality: `0.00031`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.70445 |
| `explicit.stat_1056492907` | 3.18777 |
| `explicit.stat_828533480@T2` | -2.47607 |
| `explicit.stat_828533480@T1` | -2.47604 |
| `explicit.stat_1120862500@T2` | -2.47604 |
| `explicit.stat_388617051@T2` | -2.47604 |
| `explicit.stat_1873752457@T2` | -2.47603 |
| `explicit.stat_3196823591@T2` | -2.47603 |
| `explicit.stat_2541588185@T2` | -2.47603 |
| `explicit.stat_2676834156@T2` | -2.47602 |
| `explicit.stat_2365392475@T2` | -2.47602 |
| `explicit.stat_1873752457@T1` | -2.47601 |

### weapon.warstaff — n=9451, R²=-0.392

intercept: `-9.0951`  ·  log_price: True  ·  ilvl: `0.12365`  ·  n_mods: `-0.18839`  ·  n_top_tier: `0.35492`  ·  corrupted: `0.24320`  ·  n_sockets: `0.16519`  ·  quality: `0.06377`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.11607 |
| `rune.stat_243313994` | 0.95146 |
| `explicit.stat_328541901@T1` | -0.79252 |
| `explicit.stat_328541901@T2` | -0.78002 |
| `desecrated.stat_9187492` | 0.72230 |
| `explicit.stat_1037193709@T1` | 0.71756 |
| `explicit.stat_9187492@T1` | 0.70362 |
| `explicit.stat_518292764@T1` | -0.52232 |
| `explicit.stat_748522257@T2` | 0.50913 |
| `explicit.stat_1940865751@T1` | -0.46833 |
| `explicit.stat_2694482655@T2` | 0.45884 |
| `explicit.stat_1368271171@T1` | -0.43417 |

### weapon.staff — n=8838, R²=-0.4215

intercept: `-13.3926`  ·  log_price: True  ·  ilvl: `0.17325`  ·  n_mods: `-0.13126`  ·  n_top_tier: `0.47639`  ·  corrupted: `0.39918`  ·  n_sockets: `0.23111`  ·  quality: `0.04188`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.95836 |
| `explicit.stat_591105508@T1` | 1.57823 |
| `explicit.stat_4226189338@T1` | 1.57822 |
| `explicit.stat_293638271@T2` | -1.04996 |
| `rune.stat_124131830` | 0.98581 |
| `explicit.stat_3962278098@T2` | 0.96181 |
| `explicit.stat_124131830@T2` | 0.93034 |
| `explicit.stat_2254480358@T2` | 0.85029 |
| `explicit.stat_124131830@T1` | 0.74429 |
| `explicit.stat_591105508@T2` | 0.66683 |
| `explicit.stat_2505884597@T2` | -0.63944 |
| `explicit.stat_2974417149@T1` | -0.61127 |

### weapon.sceptre — n=8759, R²=-0.3563

intercept: `-17.7728`  ·  log_price: True  ·  ilvl: `0.22722`  ·  n_mods: `-0.06557`  ·  n_top_tier: `0.35802`  ·  corrupted: `0.41314`  ·  n_sockets: `0.30754`  ·  quality: `0.04373`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.92450 |
| `explicit.stat_2162097452@T2` | 1.68362 |
| `explicit.stat_1250712710@T2` | 1.20205 |
| `explicit.stat_1263695895@T1` | -0.93978 |
| `explicit.stat_3057012405@T1` | 0.88645 |
| `explicit.stat_1263695895@T2` | -0.85095 |
| `explicit.stat_1574590649@T1` | -0.79157 |
| `explicit.stat_2347036682@T2` | -0.74350 |
| `explicit.stat_2347036682@T1` | 0.67128 |
| `explicit.stat_289128254@T2` | -0.63401 |
| `explicit.stat_849987426@T1` | 0.54006 |
| `explicit.stat_2854751904@T2` | -0.53274 |

### weapon.spear — n=7143, R²=-0.4651

intercept: `-10.7503`  ·  log_price: True  ·  ilvl: `0.14666`  ·  n_mods: `-0.08702`  ·  n_top_tier: `0.79759`  ·  corrupted: `-0.12517`  ·  n_sockets: `0.28827`  ·  quality: `0.06074`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.17651 |
| `explicit.stat_1202301673@T1` | 1.73758 |
| `explicit.stat_1509134228@T1` | 1.51410 |
| `crafted.stat_3035140377` | 1.10353 |
| `explicit.stat_1037193709@T1` | -0.94959 |
| `explicit.stat_1263695895@T2` | -0.92907 |
| `explicit.stat_55876295@T1` | -0.91164 |
| `explicit.stat_1940865751@T2` | -0.89463 |
| `explicit.stat_4080418644@T2` | -0.88379 |
| `explicit.stat_691932474@T1` | -0.85753 |
| `explicit.stat_3261801346@T1` | -0.84087 |
| `explicit.stat_748522257@T2` | -0.81518 |

### armour.focus — n=5863, R²=-0.3822

intercept: `-13.0028`  ·  log_price: True  ·  ilvl: `0.16991`  ·  n_mods: `-0.20495`  ·  n_top_tier: `0.79020`  ·  corrupted: `0.48703`  ·  n_sockets: `0.45948`  ·  quality: `0.07161`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 6.71345 |
| `explicit.stat_4220027924@T2` | -1.34923 |
| `explicit.stat_3291658075@T1` | -1.30772 |
| `explicit.stat_3962278098@T1` | -1.29508 |
| `explicit.stat_2231156303@T1` | -1.10994 |
| `explicit.stat_2231156303@T2` | -1.08813 |
| `explicit.stat_2339757871@T2` | -0.93594 |
| `explicit.stat_2339757871@T1` | -0.91464 |
| `explicit.stat_4220027924@T1` | -0.88995 |
| `explicit.stat_736967255@T2` | -0.86107 |
| `explicit.stat_2974417149@T2` | -0.79564 |
| `explicit.stat_2891184298@T2` | -0.77141 |

### armour.quiver — n=5507, R²=-0.3442

intercept: `-13.6756`  ·  log_price: True  ·  ilvl: `0.16799`  ·  n_mods: `-0.14807`  ·  n_top_tier: `0.78002`  ·  corrupted: `0.81936`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.67779 |
| `explicit.stat_2463230181@T1` | 2.07613 |
| `explicit.stat_1573130764@T1` | -1.27401 |
| `explicit.stat_681332047@T2` | -1.22607 |
| `explicit.stat_4067062424@T1` | -1.10048 |
| `explicit.stat_803737631@T2` | -1.09152 |
| `explicit.stat_2321178454@T2` | -1.07899 |
| `explicit.stat_3261801346@T1` | -0.93237 |
| `explicit.stat_2321178454@T1` | -0.92602 |
| `explicit.stat_803737631@T1` | -0.90591 |
| `explicit.stat_2463230181@T2` | 0.88406 |
| `explicit.stat_2194114101@T2` | -0.86900 |

### armour.shield — n=4789, R²=-0.5041

intercept: `-10.5055`  ·  log_price: True  ·  ilvl: `0.14006`  ·  n_mods: `-0.10364`  ·  n_top_tier: `0.69923`  ·  corrupted: `-0.25583`  ·  n_sockets: `0.30074`  ·  quality: `0.06084`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.37599 |
| `explicit.stat_2481353198@T2` | -1.26714 |
| `explicit.stat_3484657501@T2` | -1.22899 |
| `explicit.stat_2339757871@T1` | -1.16689 |
| `explicit.stat_328541901@T1` | -1.12612 |
| `explicit.stat_3321629045@T2` | -1.05664 |
| `explicit.stat_2481353198@T1` | -1.01879 |
| `explicit.stat_2923486259@T2` | -0.98197 |
| `explicit.stat_3033371881@T2` | -0.94941 |
| `explicit.stat_2901986750@T1` | -0.93974 |
| `explicit.stat_2923486259@T1` | -0.89011 |
| `explicit.stat_3855016469@T1` | -0.87270 |

### weapon.twomace — n=4404, R²=-0.4989

intercept: `-9.2019`  ·  log_price: True  ·  ilvl: `0.12395`  ·  n_mods: `-0.16218`  ·  n_top_tier: `0.36277`  ·  corrupted: `-0.06781`  ·  n_sockets: `0.17957`  ·  quality: `0.05715`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.47406 |
| `desecrated.stat_1509134228@T1` | 2.86129 |
| `explicit.stat_1037193709@T1` | -1.62035 |
| `crafted.stat_3035140377` | 0.95934 |
| `explicit.stat_1037193709@T2` | -0.85540 |
| `explicit.stat_3336890334@T1` | -0.85489 |
| `explicit.stat_387439868@T2` | -0.81614 |
| `explicit.stat_210067635@T1` | 0.68398 |
| `explicit.stat_1509134228@T1` | 0.67647 |
| `explicit.stat_9187492@T1` | -0.66087 |
| `explicit.stat_691932474@T1` | -0.63901 |
| `explicit.stat_1263695895@T2` | -0.59222 |

## Coverage (listings per base)

- … **Sapphire** — 26781 listings (26735 priced) [0.3–885594757.8 ex]
- … **Emerald** — 26261 listings (26227 priced) [0.3–885594757.8 ex]
- … **Ruby** — 20112 listings (20091 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10345 listings (10330 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8846 listings (8830 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8571 listings (8552 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8463 listings (8455 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8053 listings (8039 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 7892 listings (7874 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 7855 listings (7846 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6585 listings (6577 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6323 listings (6317 priced) [0.3–307202867.9 ex]
- … **Dueling Wand** — 6309 listings (6290 priced) [0.3–4297682211.9 ex]
- … **Ruby Ring** — 6277 listings (6271 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5595 listings (5572 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5573 listings (5568 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 5442 listings (5427 priced) [0.2–24532814.5 ex]
- … **Jade Amulet** — 5439 listings (5429 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 5429 listings (5423 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5401 listings (5382 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5255 listings (5247 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5149 listings (5142 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 4974 listings (4972 priced) [0.3–3985176410.3 ex]
- … **Heavy Belt** — 4962 listings (4954 priced) [0.3–398912568423.8 ex]
- … **Lunar Amulet** — 4940 listings (4929 priced) [0.3–91750808.2 ex]

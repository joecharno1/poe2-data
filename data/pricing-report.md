# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-16T21:06:49+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **558055** (556551 priced in exalted)
- Distinct bases: 987 · distinct mods: 3186 · mod rows: 2643455
- Sold signals: **25583** sold · 314753 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-16T20:58:39+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.43** (median |log error| 3.1959)
- Within ±30% of asking price: **15%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 80% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×61.73 · ±30% 5% · n=80799
- Premium segment (60ex+): skill **+0.13** · typical error ×277.11 · ±30% 0% · n=54626

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 11352 | ×54.30 | 22% | +0.04 | +0.06 |
| jewel | 10541 | ×10.66 | 4% | +0.07 | +0.10 |
| accessory.amulet | 10362 | ×50.83 | 20% | +0.03 | +0.04 |
| accessory.belt | 7797 | ×16.73 | 4% | +0.04 | +0.06 |
| armour.chest | 7576 | ×24.23 | 10% | +0.10 | +0.12 |
| armour.helmet | 7393 | ×14.93 | 15% | +0.07 | +0.09 |
| armour.boots | 6928 | ×47.48 | 22% | +0.08 | +0.10 |
| armour.gloves | 6709 | ×45.61 | 16% | +0.08 | +0.10 |
| other | 6309 | ×1.62 | 42% | +0.12 | +0.21 |
| weapon.wand | 4227 | ×42.07 | 15% | +0.09 | +0.10 |
| weapon.bow | 3325 | ×27.61 | 10% | +0.15 | +0.16 |
| weapon.crossbow | 3149 | ×30.70 | 10% | +0.11 | +0.15 |
| weapon.warstaff | 1972 | ×29.62 | 9% | +0.14 | +0.12 |
| weapon.staff | 1859 | ×51.07 | 8% | +0.11 | +0.11 |
| weapon.sceptre | 1856 | ×42.95 | 5% | +0.17 | +0.16 |
| weapon.spear | 1468 | ×45.17 | 15% | +0.08 | +0.09 |
| armour.focus | 1237 | ×31.78 | 6% | +0.14 | +0.17 |
| armour.quiver | 1175 | ×29.92 | 7% | +0.12 | +0.13 |
| flask.charm | 1029 | ×29.99 | 33% | +0.04 | +0.06 |
| armour.shield | 959 | ×22.54 | 9% | +0.04 | +0.06 |
| weapon.twomace | 874 | ×10.25 | 11% | +0.07 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=57916, R²=-0.9378

intercept: `-1.8083`  ·  log_price: True  ·  ilvl: `0.02638`  ·  n_mods: `0.77778`  ·  n_top_tier: `-0.30297`  ·  corrupted: `0.23164`  ·  quality: `0.22285`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.52574 |
| `explicit.stat_2301718443@T1` | 3.06357 |
| `explicit.stat_1805182458@T1` | -2.03567 |
| `explicit.stat_627767961@T1` | -1.98171 |
| `explicit.stat_3780644166@T1` | -1.93499 |
| `explicit.stat_1697951953@T1` | -1.85180 |
| `explicit.stat_3485067555@T1` | 1.76679 |
| `explicit.stat_3668351662@T1` | -1.70393 |
| `explicit.stat_21071013@T1` | 1.57062 |
| `explicit.stat_3166958180@T1` | -1.42942 |
| `explicit.stat_2523933828@T1` | -1.40649 |
| `explicit.stat_3174700878@T1` | 1.34441 |

### other — n=53603, R²=-0.6331

intercept: `1.5680`  ·  log_price: True  ·  ilvl: `0.00264`  ·  n_mods: `-0.01037`  ·  n_top_tier: `0.27473`  ·  corrupted: `0.15918`  ·  n_sockets: `-0.05756`  ·  quality: `-0.00761`

| stat_id | coef |
|---|---|
| `implicit.stat_2219129443` | 0.41670 |
| `implicit.stat_3879011313` | 0.41647 |
| `explicit.stat_3299347043@T1` | -0.24728 |
| `explicit.stat_2974417149@T1` | 0.22145 |
| `implicit.stat_4041853756` | 0.21462 |
| `explicit.stat_2482852589@T1` | -0.21310 |
| `explicit.stat_1050105434@T1` | -0.18706 |
| `implicit.stat_3182714256` | 0.13838 |
| `implicit.stat_718638445` | 0.13835 |
| `explicit.stat_2106365538@T1` | -0.13715 |
| `implicit.stat_1379411836` | -0.13317 |
| `implicit.stat_958696139` | -0.12385 |

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

### armour.helmet — n=34578, R²=-1.5281

intercept: `3.4056`  ·  log_price: True  ·  ilvl: `-0.04310`  ·  n_mods: `-0.03844`  ·  n_top_tier: `0.37918`  ·  corrupted: `0.61594`  ·  n_sockets: `0.10402`  ·  quality: `0.04296`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -6.08659 |
| `crafted.stat_3917489142@T1` | 1.92609 |
| `explicit.stat_1263695895@T1` | -0.66841 |
| `explicit.stat_3917489142@T2` | -0.61595 |
| `explicit.stat_1263695895@T2` | -0.54671 |
| `explicit.stat_2162097452@T2` | -0.54541 |
| `explicit.stat_1999113824@T1` | -0.54460 |
| `explicit.stat_3321629045@T2` | -0.49984 |
| `explicit.stat_1999113824@T2` | -0.47653 |
| `explicit.stat_4052037485@T2` | -0.47652 |
| `explicit.stat_587431675@T2` | -0.47345 |
| `explicit.stat_3917489142@T1` | -0.46475 |

### armour.boots — n=32401, R²=-1.7281

intercept: `3.6228`  ·  log_price: True  ·  ilvl: `-0.04435`  ·  n_mods: `-0.02015`  ·  n_top_tier: `0.67592`  ·  corrupted: `0.00396`  ·  n_sockets: `0.02344`  ·  quality: `0.05118`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.72571 |
| `explicit.stat_2250533757@T1` | 1.48798 |
| `explicit.stat_3299347043@T1` | -0.83012 |
| `explicit.stat_3917489142@T2` | -0.82265 |
| `explicit.stat_2339757871@T1` | -0.81044 |
| `explicit.stat_2160282525@T1` | -0.72693 |
| `explicit.stat_3917489142@T1` | -0.72377 |
| `explicit.stat_2923486259@T2` | -0.72090 |
| `explicit.stat_1671376347@T2` | -0.70710 |
| `explicit.stat_3484657501@T2` | -0.69818 |
| `explicit.stat_3299347043@T2` | -0.69724 |
| `explicit.stat_53045048@T1` | -0.69696 |

### armour.gloves — n=31492, R²=-1.705

intercept: `4.0157`  ·  log_price: True  ·  ilvl: `-0.05072`  ·  n_mods: `-0.01533`  ·  n_top_tier: `0.51866`  ·  corrupted: `0.00899`  ·  n_sockets: `0.06054`  ·  quality: `0.04443`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 3.87036 |
| `rune.stat_201332984` | -1.32738 |
| `explicit.stat_1671376347@T1` | 1.09405 |
| `explicit.stat_9187492@T1` | 0.93545 |
| `explicit.stat_9187492@T2` | -0.81502 |
| `explicit.stat_1999113824@T1` | 0.77830 |
| `explicit.stat_2923486259@T1` | -0.73922 |
| `explicit.stat_3321629045@T2` | -0.68203 |
| `explicit.stat_4052037485@T1` | -0.66975 |
| `explicit.stat_3484657501@T2` | -0.64483 |
| `explicit.stat_3917489142@T2` | -0.62493 |
| `explicit.stat_124859000@T2` | -0.59725 |

### weapon.wand — n=19746, R²=-1.9835

intercept: `3.9272`  ·  log_price: True  ·  ilvl: `-0.04848`  ·  n_mods: `-0.04389`  ·  n_top_tier: `0.55370`  ·  corrupted: `0.02329`  ·  n_sockets: `0.10390`  ·  quality: `0.01759`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.55815 |
| `explicit.stat_4226189338@T1` | 2.53849 |
| `rune.stat_124131830` | -2.43763 |
| `explicit.stat_2254480358@T1` | 2.38941 |
| `explicit.stat_591105508@T1` | 1.90454 |
| `explicit.stat_124131830@T1` | 1.83131 |
| `explicit.stat_736967255@T2` | 1.67184 |
| `explicit.stat_1600707273@T1` | 1.22606 |
| `crafted.stat_124131830` | 1.19013 |
| `explicit.stat_2254480358@T2` | 0.90926 |
| `explicit.stat_4226189338@T2` | 0.83813 |
| `explicit.stat_1263695895@T1` | -0.78959 |

### weapon.bow — n=15804, R²=-1.6188

intercept: `3.6457`  ·  log_price: True  ·  ilvl: `-0.04172`  ·  n_mods: `-0.11500`  ·  n_top_tier: `0.54020`  ·  corrupted: `0.29151`  ·  n_sockets: `0.05549`  ·  quality: `0.02790`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.34132 |
| `desecrated.stat_210067635@T1` | -1.20590 |
| `desecrated.stat_666077204@T1` | -1.17471 |
| `explicit.stat_518292764@T2` | -1.16166 |
| `explicit.stat_3336890334@T1` | 1.09334 |
| `explicit.stat_1202301673@T1` | 1.07460 |
| `explicit.stat_1263695895@T1` | -1.02892 |
| `explicit.stat_2463230181@T1` | -1.01853 |
| `explicit.stat_1263695895@T2` | -0.98869 |
| `explicit.stat_2463230181@T2` | -0.97003 |
| `explicit.stat_3695891184@T2` | -0.85943 |
| `explicit.stat_3695891184@T1` | -0.82424 |

### weapon.crossbow — n=14871, R²=-1.5338

intercept: `3.7802`  ·  log_price: True  ·  ilvl: `-0.04486`  ·  n_mods: `-0.09724`  ·  n_top_tier: `0.79949`  ·  corrupted: `0.08557`  ·  n_sockets: `0.12980`  ·  quality: `0.01887`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.92717 |
| `explicit.stat_2250681686@T2` | -1.29066 |
| `explicit.stat_1980802737` | 1.17494 |
| `explicit.stat_2694482655@T1` | -1.05283 |
| `explicit.stat_210067635@T2` | -1.02329 |
| `explicit.stat_1037193709@T1` | -0.99442 |
| `explicit.stat_1940865751@T2` | -0.99089 |
| `explicit.stat_3695891184@T2` | -0.98791 |
| `explicit.stat_1263695895@T2` | -0.97218 |
| `explicit.stat_1544773869@T2` | -0.96686 |
| `explicit.stat_3695891184@T1` | -0.90320 |
| `explicit.stat_669069897@T1` | -0.90015 |

### flask.charm — n=14727, R²=-0.5534

intercept: `0.0458`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.45427`  ·  corrupted: `1.68077`  ·  quality: `0.00042`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.78505 |
| `explicit.stat_1056492907` | 3.20784 |
| `explicit.stat_828533480@T2` | -2.45429 |
| `explicit.stat_828533480@T1` | -2.45427 |
| `explicit.stat_1120862500@T2` | -2.45426 |
| `explicit.stat_1873752457@T2` | -2.45426 |
| `explicit.stat_388617051@T2` | -2.45425 |
| `explicit.stat_3196823591@T2` | -2.45425 |
| `explicit.stat_2676834156@T2` | -2.45424 |
| `explicit.stat_2365392475@T2` | -2.45424 |
| `explicit.stat_2541588185@T2` | -2.45424 |
| `explicit.stat_1873752457@T1` | -2.45423 |

### weapon.warstaff — n=9478, R²=-0.3895

intercept: `-9.1172`  ·  log_price: True  ·  ilvl: `0.12424`  ·  n_mods: `-0.19089`  ·  n_top_tier: `0.35658`  ·  corrupted: `0.23337`  ·  n_sockets: `0.16554`  ·  quality: `0.06442`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 1.15225 |
| `crafted.stat_210067635@T2` | 1.10294 |
| `rune.stat_243313994` | 0.93310 |
| `explicit.stat_328541901@T1` | -0.83564 |
| `explicit.stat_328541901@T2` | -0.79501 |
| `desecrated.stat_9187492` | 0.73735 |
| `explicit.stat_9187492@T1` | 0.64498 |
| `explicit.stat_748522257@T2` | 0.50808 |
| `explicit.stat_518292764@T1` | -0.49187 |
| `explicit.stat_2694482655@T2` | 0.44651 |
| `explicit.stat_1940865751@T1` | -0.43943 |
| `explicit.stat_1368271171@T1` | -0.42451 |

### weapon.staff — n=8857, R²=-0.4191

intercept: `-13.4916`  ·  log_price: True  ·  ilvl: `0.17428`  ·  n_mods: `-0.12485`  ·  n_top_tier: `0.44823`  ·  corrupted: `0.39440`  ·  n_sockets: `0.23017`  ·  quality: `0.04288`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.08372 |
| `explicit.stat_4226189338@T1` | 1.66767 |
| `explicit.stat_591105508@T1` | 1.47886 |
| `explicit.stat_293638271@T2` | -1.02180 |
| `explicit.stat_124131830@T2` | 1.02073 |
| `explicit.stat_3962278098@T2` | 0.93558 |
| `explicit.stat_2254480358@T2` | 0.92594 |
| `rune.stat_124131830` | 0.92086 |
| `explicit.stat_124131830@T1` | 0.86587 |
| `explicit.stat_2254480358@T1` | 0.62235 |
| `explicit.stat_2974417149@T1` | -0.61971 |
| `explicit.stat_2231156303@T2` | 0.61206 |

### weapon.sceptre — n=8774, R²=-0.357

intercept: `-17.8665`  ·  log_price: True  ·  ilvl: `0.22865`  ·  n_mods: `-0.06691`  ·  n_top_tier: `0.36433`  ·  corrupted: `0.38562`  ·  n_sockets: `0.30447`  ·  quality: `0.04522`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.93801 |
| `explicit.stat_2162097452@T2` | 1.68494 |
| `explicit.stat_1250712710@T2` | 1.20834 |
| `explicit.stat_1263695895@T1` | -0.91820 |
| `explicit.stat_3057012405@T1` | 0.88767 |
| `explicit.stat_1263695895@T2` | -0.83497 |
| `explicit.stat_1574590649@T1` | -0.79419 |
| `explicit.stat_2347036682@T2` | -0.73755 |
| `explicit.stat_2347036682@T1` | 0.63852 |
| `explicit.stat_289128254@T2` | -0.63812 |
| `explicit.stat_849987426@T1` | 0.59837 |
| `explicit.stat_2854751904@T2` | -0.54664 |

### weapon.spear — n=7171, R²=-0.4593

intercept: `-10.2580`  ·  log_price: True  ·  ilvl: `0.14333`  ·  n_mods: `-0.11419`  ·  n_top_tier: `0.78324`  ·  corrupted: `-0.20201`  ·  n_sockets: `0.23361`  ·  quality: `0.06798`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.44544 |
| `explicit.stat_1202301673@T1` | 1.57496 |
| `explicit.stat_1509134228@T1` | 1.54481 |
| `explicit.stat_9187492@T1` | 1.14933 |
| `crafted.stat_3035140377` | 1.11041 |
| `explicit.stat_1037193709@T1` | -1.07106 |
| `explicit.stat_1263695895@T2` | -0.89394 |
| `explicit.stat_1940865751@T2` | -0.86550 |
| `explicit.stat_4080418644@T2` | -0.85204 |
| `explicit.stat_55876295@T1` | -0.85197 |
| `explicit.stat_691932474@T1` | -0.82697 |
| `explicit.stat_3261801346@T1` | -0.82003 |

### armour.focus — n=5885, R²=-0.3906

intercept: `-12.9857`  ·  log_price: True  ·  ilvl: `0.16964`  ·  n_mods: `-0.19539`  ·  n_top_tier: `0.80367`  ·  corrupted: `0.45138`  ·  n_sockets: `0.41443`  ·  quality: `0.07437`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 9.05458 |
| `explicit.stat_4220027924@T2` | -1.38400 |
| `explicit.stat_3962278098@T1` | -1.34564 |
| `crafted.stat_737908626@T2` | 1.22865 |
| `explicit.stat_3291658075@T1` | -1.16817 |
| `explicit.stat_2231156303@T2` | -1.02675 |
| `explicit.stat_2231156303@T1` | -0.95949 |
| `explicit.stat_4220027924@T1` | -0.92809 |
| `explicit.stat_2339757871@T1` | -0.86920 |
| `explicit.stat_2339757871@T2` | -0.85250 |
| `explicit.stat_736967255@T2` | -0.83095 |
| `explicit.stat_2891184298@T2` | -0.82450 |

### armour.quiver — n=5515, R²=-0.3405

intercept: `-13.9521`  ·  log_price: True  ·  ilvl: `0.17067`  ·  n_mods: `-0.13626`  ·  n_top_tier: `0.84192`  ·  corrupted: `0.76275`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.68962 |
| `explicit.stat_2463230181@T1` | 2.07123 |
| `explicit.stat_681332047@T2` | -1.32257 |
| `explicit.stat_1573130764@T1` | -1.27188 |
| `explicit.stat_803737631@T2` | -1.16269 |
| `explicit.stat_4067062424@T1` | -1.10031 |
| `explicit.stat_2321178454@T2` | -1.06979 |
| `explicit.stat_3261801346@T1` | -0.95466 |
| `explicit.stat_2194114101@T2` | -0.94321 |
| `explicit.stat_803737631@T1` | -0.92075 |
| `explicit.stat_2321178454@T1` | -0.89957 |
| `explicit.stat_1573130764@T2` | -0.88962 |

### armour.shield — n=4800, R²=-0.5051

intercept: `-10.3596`  ·  log_price: True  ·  ilvl: `0.13769`  ·  n_mods: `-0.09708`  ·  n_top_tier: `0.69073`  ·  corrupted: `-0.23908`  ·  n_sockets: `0.29415`  ·  quality: `0.06179`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.33814 |
| `explicit.stat_2481353198@T2` | -1.26055 |
| `explicit.stat_328541901@T1` | -1.18795 |
| `explicit.stat_3484657501@T2` | -1.17875 |
| `explicit.stat_2339757871@T1` | -1.11173 |
| `explicit.stat_3321629045@T2` | -1.04617 |
| `explicit.stat_2481353198@T1` | -1.01078 |
| `explicit.stat_328541901@T2` | -0.94869 |
| `explicit.stat_3033371881@T2` | -0.93495 |
| `explicit.stat_2923486259@T2` | -0.93248 |
| `explicit.stat_4095671657@T1` | -0.88625 |
| `explicit.stat_2901986750@T1` | -0.87608 |

### weapon.twomace — n=4412, R²=-0.5031

intercept: `-9.3024`  ·  log_price: True  ·  ilvl: `0.12459`  ·  n_mods: `-0.15300`  ·  n_top_tier: `0.34646`  ·  corrupted: `-0.10244`  ·  n_sockets: `0.19558`  ·  quality: `0.06000`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.88991 |
| `desecrated.stat_1509134228@T1` | 2.94726 |
| `explicit.stat_1037193709@T1` | -1.55802 |
| `crafted.stat_3035140377` | 0.93922 |
| `explicit.stat_3336890334@T1` | -0.79429 |
| `explicit.stat_1037193709@T2` | -0.77717 |
| `explicit.stat_387439868@T2` | -0.75215 |
| `explicit.stat_210067635@T1` | 0.70499 |
| `explicit.stat_1509134228@T1` | 0.64040 |
| `explicit.stat_9187492@T1` | -0.62814 |
| `explicit.stat_691932474@T1` | -0.58300 |
| `explicit.stat_691932474@T2` | -0.52608 |

## Coverage (listings per base)

- … **Sapphire** — 26899 listings (26853 priced) [0.3–885594757.8 ex]
- … **Emerald** — 26396 listings (26362 priced) [0.3–885594757.8 ex]
- … **Ruby** — 20190 listings (20168 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10345 listings (10330 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8846 listings (8830 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8573 listings (8554 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8464 listings (8456 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8053 listings (8039 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 7892 listings (7874 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 7855 listings (7846 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6588 listings (6580 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6323 listings (6317 priced) [0.3–307202867.9 ex]
- … **Dueling Wand** — 6316 listings (6297 priced) [0.3–4297682211.9 ex]
- … **Ruby Ring** — 6278 listings (6272 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5595 listings (5572 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5574 listings (5569 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 5442 listings (5427 priced) [0.2–24532814.5 ex]
- … **Jade Amulet** — 5440 listings (5430 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 5429 listings (5423 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5409 listings (5390 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5256 listings (5248 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5149 listings (5142 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 4974 listings (4972 priced) [0.3–3985176410.3 ex]
- … **Heavy Belt** — 4964 listings (4956 priced) [0.3–398912568423.8 ex]
- … **Lunar Amulet** — 4940 listings (4929 priced) [0.3–91750808.2 ex]

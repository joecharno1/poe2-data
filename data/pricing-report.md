# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-04T02:28:37+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **80110** (80110 priced in exalted)
- Distinct bases: 838 · distinct mods: 1900 · mod rows: 392400
- Sold signals: **11201** sold · 13012 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-04T02:23:33+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×8.17** (median |log error| 2.1002)
- Within ±30% of asking price: **33%**
- Skill vs constant-price guess: **+0.01** (> 0 = the mods carry signal)
- Calibration: 66% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.08** · typical error ×23.41 · ±30% 18% · n=11421
- Premium segment (60ex+): skill **+0.08** · typical error ×110.45 · ±30% 1% · n=6543
- Sold listings (clearing prices): skill **-0.01** · typical error ×15.33 · ±30% 28% · n=4996

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| armour.chest | 1297 | ×10.00 | 39% | -0.01 | -0.16 |
| accessory.amulet | 1292 | ×19.54 | 6% | -0.12 | -0.12 |
| accessory.belt | 1286 | ×9.00 | 25% | +0.02 | +0.06 |
| accessory.ring | 1272 | ×9.61 | 5% | -0.26 | -0.20 |
| armour.helmet | 1221 | ×10.00 | 38% | +0.01 | -0.07 |
| armour.boots | 1157 | ×10.00 | 31% | -0.01 | -0.09 |
| armour.gloves | 1122 | ×10.00 | 33% | -0.00 | -0.08 |
| other | 1007 | ×9.99 | 36% | +0.43 | +0.41 |
| weapon.wand | 882 | ×9.10 | 37% | -0.01 | +0.07 |
| weapon.bow | 807 | ×8.97 | 33% | -0.02 | +0.08 |
| weapon.crossbow | 772 | ×8.54 | 30% | +0.02 | +0.11 |
| jewel | 713 | ×7.43 | 7% | -0.06 | +0.21 |
| weapon.sceptre | 220 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.spear | 191 | ×1.00 | 100% | +0.00 | +0.00 |
| armour.focus | 183 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.warstaff | 168 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.staff | 166 | ×1.00 | 98% | +0.00 | +0.00 |
| armour.shield | 150 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 116 | ×1.00 | 97% | +0.00 | +0.00 |
| weapon.twomace | 99 | ×1.00 | 99% | +0.00 | +0.00 |
| flask.charm | 30 | ×1.28 | 60% | +0.00 | -0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=9323, R²=-0.1388

intercept: `1.5046`  ·  log_price: True  ·  ilvl: `0.00501`  ·  n_mods: `0.05038`  ·  n_top_tier: `0.14579`  ·  corrupted: `0.41899`  ·  n_sockets: `-0.11372`  ·  quality: `-0.01254`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830` | -0.48931 |
| `implicit.stat_718638445` | 0.44693 |
| `implicit.stat_3182714256` | 0.44202 |
| `explicit.stat_2974417149@T1` | 0.30512 |
| `implicit.stat_1379411836` | -0.29291 |
| `explicit.stat_3299347043@T2` | -0.23741 |
| `explicit.stat_4052037485@T1` | -0.23703 |
| `explicit.stat_3299347043@T1` | -0.21288 |
| `explicit.stat_1050105434@T1` | -0.20156 |
| `implicit.stat_4041853756` | 0.19614 |
| `implicit.stat_3879011313` | 0.19566 |
| `explicit.stat_789117908@T1` | 0.19114 |

### accessory.belt — n=6200, R²=-1.2512

intercept: `4.5106`  ·  log_price: True  ·  ilvl: `-0.05456`  ·  n_mods: `-0.02059`  ·  n_top_tier: `0.04110`  ·  corrupted: `0.06513`  ·  n_sockets: `-0.17773`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T2` | 1.27914 |
| `crafted.stat_3249412463` | 1.01061 |
| `explicit.stat_1836676211@T1` | 0.74823 |
| `implicit.stat_731781020` | -0.22554 |
| `explicit.stat_3299347043@T1` | -0.21421 |
| `explicit.stat_3372524247@T1` | 0.20114 |
| `explicit.stat_3299347043@T2` | -0.18069 |
| `explicit.stat_2639966148` | 0.13410 |
| `explicit.stat_4220027924@T1` | 0.10671 |
| `explicit.stat_809229260@T2` | -0.10467 |
| `explicit.stat_2923486259@T1` | -0.09898 |
| `explicit.stat_1389754388@T1` | -0.09518 |

### armour.helmet — n=5966, R²=-0.207

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.56372`  ·  corrupted: `0.00006`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.22787 |
| `explicit.stat_803737631@T2` | -0.56376 |
| `explicit.stat_3321629045@T1` | -0.56375 |
| `explicit.stat_803737631@T1` | -0.56375 |
| `explicit.stat_3362812763@T2` | -0.56374 |
| `explicit.stat_328541901@T1` | -0.56374 |
| `explicit.stat_3362812763@T1` | -0.56373 |
| `explicit.stat_1062208444@T2` | -0.56373 |
| `explicit.stat_1263695895@T1` | -0.56373 |
| `explicit.stat_3325883026@T2` | -0.56373 |
| `explicit.stat_3261801346@T2` | -0.56373 |
| `explicit.stat_3484657501@T1` | -0.56373 |

### armour.chest — n=5961, R²=-0.2803

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.01422`  ·  corrupted: `0.00007`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.77745 |
| `crafted.stat_4220027924` | 0.03686 |
| `desecrated.stat_4015621042` | 0.03180 |
| `desecrated.stat_4220027924` | -0.02529 |
| `explicit.stat_3523867985` | 0.02347 |
| `crafted.stat_1671376347` | -0.01903 |
| `desecrated.stat_3372524247` | -0.01900 |
| `desecrated.stat_1671376347` | -0.01898 |
| `implicit.stat_4220027924` | -0.01863 |
| `explicit.stat_1671376347` | -0.01863 |
| `pseudo.total_ele_res` | 0.01863 |
| `explicit.stat_3372524247` | -0.01863 |

### accessory.amulet — n=5946, R²=-2.4068

intercept: `5.8895`  ·  log_price: True  ·  ilvl: `-0.06173`  ·  n_mods: `-0.25412`  ·  n_top_tier: `0.21980`  ·  corrupted: `-0.35039`  ·  n_sockets: `-0.89814`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | 3.12844 |
| `explicit.stat_983749596@T1` | -3.04613 |
| `explicit.stat_2923486259@T1` | -2.77683 |
| `explicit.stat_2923486259@T2` | -2.04007 |
| `explicit.stat_9187492@T2` | -1.98432 |
| `explicit.stat_1444556985@T1` | 1.66112 |
| `explicit.stat_983749596@T2` | -1.60676 |
| `explicit.stat_3299347043@T1` | -1.49312 |
| `explicit.stat_587431675@T2` | -1.39439 |
| `explicit.stat_803737631@T1` | -1.34142 |
| `explicit.stat_2162097452@T2` | -1.33163 |
| `explicit.stat_9187492` | 1.29458 |

### accessory.ring — n=5866, R²=-2.0551

intercept: `4.6643`  ·  log_price: True  ·  ilvl: `-0.03580`  ·  n_mods: `-0.23007`  ·  n_top_tier: `0.61273`  ·  corrupted: `0.19527`  ·  n_sockets: `3.20735`  ·  quality: `0.03250`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -2.48516 |
| `explicit.stat_1263695895@T2` | -1.84347 |
| `explicit.stat_2557965901@T1` | -1.74761 |
| `explicit.stat_1573130764@T1` | -1.62177 |
| `explicit.stat_1368271171@T1` | -1.61574 |
| `explicit.stat_1671376347@T1` | -1.54237 |
| `explicit.stat_1573130764@T2` | -1.52990 |
| `explicit.stat_1050105434@T2` | -1.28416 |
| `explicit.stat_2557965901@T2` | -1.15346 |
| `explicit.stat_1379411836@T1` | -1.14495 |
| `explicit.stat_3299347043@T2` | -1.13460 |
| `explicit.stat_1050105434@T1` | -1.13354 |

### armour.gloves — n=5378, R²=-0.2458

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00008`  ·  corrupted: `0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.20510 |
| `explicit.stat_2923486259` | -0.11327 |
| `pseudo.total_chaos_res` | 0.11327 |
| `explicit.stat_4067062424@T1` | 0.03310 |
| `explicit.stat_2339757871@T1` | -0.00082 |
| `desecrated.stat_3299347043` | 0.00041 |
| `explicit.stat_3556824919@T1` | 0.00016 |
| `explicit.stat_4052037485@T1` | -0.00013 |
| `explicit.stat_2451402625@T2` | -0.00013 |
| `explicit.stat_4015621042@T1` | -0.00013 |
| `explicit.stat_2557965901@T1` | -0.00012 |
| `explicit.stat_2797971005@T2` | -0.00011 |

### armour.boots — n=5344, R²=-0.1861

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.34246`  ·  corrupted: `0.00003`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1062208444@T2` | -0.41779 |
| `explicit.stat_1062208444@T1` | -0.36694 |
| `explicit.stat_2339757871@T1` | -0.34269 |
| `explicit.stat_3484657501@T2` | -0.34253 |
| `explicit.stat_3261801346@T2` | -0.34253 |
| `explicit.stat_3639275092@T1` | -0.34252 |
| `explicit.stat_3362812763@T1` | -0.34252 |
| `explicit.stat_3321629045@T2` | -0.34252 |
| `explicit.stat_3362812763@T2` | -0.34251 |
| `explicit.stat_3484657501@T1` | -0.34250 |
| `explicit.stat_3261801346@T1` | -0.34248 |
| `explicit.stat_328541901@T1` | -0.34248 |

### weapon.wand — n=4355, R²=-1.5324

intercept: `3.3624`  ·  log_price: True  ·  ilvl: `-0.04203`  ·  n_mods: `-0.01041`  ·  n_top_tier: `0.06982`  ·  corrupted: `0.03406`  ·  n_sockets: `-0.00292`  ·  quality: `0.01419`

| stat_id | coef |
|---|---|
| `explicit.stat_1600707273@T1` | 2.31415 |
| `explicit.stat_591105508@T1` | 2.30896 |
| `explicit.stat_1545858329@T1` | 2.22356 |
| `explicit.stat_736967255@T2` | 2.15836 |
| `explicit.stat_2974417149@T1` | 2.05098 |
| `explicit.stat_124131830@T1` | 1.90120 |
| `explicit.stat_2254480358@T1` | 1.84680 |
| `explicit.stat_1600707273@T2` | 1.70350 |
| `crafted.stat_124131830` | 1.08129 |
| `explicit.stat_4226189338@T1` | 1.07063 |
| `rune.stat_3990135792` | -0.25502 |
| `rune.stat_3278136794` | 0.22610 |

### weapon.bow — n=3784, R²=-1.4755

intercept: `3.2214`  ·  log_price: True  ·  ilvl: `-0.03978`  ·  n_mods: `-0.02265`  ·  n_top_tier: `0.46435`  ·  corrupted: `0.01328`  ·  n_sockets: `0.00778`  ·  quality: `-0.00575`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -7.35482 |
| `desecrated.stat_210067635@T1` | -3.11564 |
| `explicit.stat_2463230181@T1` | 1.80736 |
| `explicit.stat_1509134228@T1` | 1.79934 |
| `crafted.stat_3035140377` | 1.11968 |
| `rune.stat_3885405204` | -0.79467 |
| `explicit.stat_1202301673@T1` | 0.76095 |
| `desecrated.stat_666077204` | 0.59533 |
| `explicit.stat_821021828@T1` | -0.56812 |
| `explicit.stat_1263695895@T1` | -0.54490 |
| `explicit.stat_821021828@T2` | -0.53491 |
| `explicit.stat_691932474@T2` | -0.53300 |

### weapon.crossbow — n=3559, R²=-1.4419

intercept: `3.2697`  ·  log_price: True  ·  ilvl: `-0.04106`  ·  n_mods: `0.00403`  ·  n_top_tier: `0.41844`  ·  corrupted: `0.03480`  ·  n_sockets: `0.02142`  ·  quality: `-0.02289`

| stat_id | coef |
|---|---|
| `desecrated.stat_3131442032@T1` | -2.68215 |
| `desecrated.stat_1365232741@T1` | -2.68215 |
| `explicit.stat_3336890334@T1` | 1.89442 |
| `explicit.stat_709508406@T1` | 1.83382 |
| `explicit.stat_691932474@T1` | -1.72249 |
| `explicit.stat_1037193709@T1` | 1.42357 |
| `explicit.stat_1263695895@T1` | 1.07918 |
| `explicit.stat_1509134228@T1` | 0.91779 |
| `crafted.stat_3035140377` | 0.66354 |
| `explicit.stat_1202301673@T2` | -0.48553 |
| `explicit.stat_1509134228@T2` | -0.47719 |
| `explicit.stat_1940865751@T2` | -0.46189 |

### jewel — n=3541, R²=-0.9131

intercept: `-1.4261`  ·  log_price: True  ·  ilvl: `0.03393`  ·  n_mods: `0.23778`  ·  n_top_tier: `-0.50381`  ·  corrupted: `0.55705`

| stat_id | coef |
|---|---|
| `explicit.stat_1569101201@T1` | 7.12802 |
| `explicit.stat_2301718443@T1` | -6.49640 |
| `explicit.stat_3787460122@T1` | 4.96290 |
| `explicit.stat_293638271@T1` | -4.68855 |
| `explicit.stat_1459321413@T1` | 4.58883 |
| `explicit.stat_3851254963@T1` | 4.47686 |
| `explicit.stat_3824372849@T1` | -4.17755 |
| `explicit.stat_2011656677@T1` | 3.98154 |
| `explicit.stat_1569159338@T1` | 3.76951 |
| `explicit.stat_3714003708@T1` | -3.75153 |
| `explicit.stat_429143663@T1` | 3.67191 |
| `explicit.stat_2527686725@T1` | 3.51890 |

### weapon.sceptre — n=1076, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1798257884` | 0.00000 |
| `desecrated.stat_1050105434` | 0.00000 |
| `desecrated.stat_1250712710` | 0.00000 |
| `desecrated.stat_1798257884` | 0.00000 |
| `desecrated.stat_3984865854` | 0.00000 |
| `explicit.stat_101878827` | 0.00000 |
| `explicit.stat_101878827@T1` | 0.00000 |
| `explicit.stat_101878827@T2` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_1250712710` | 0.00000 |

### weapon.spear — n=972, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1202301673@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |

### armour.focus — n=860, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1671376347` | 0.00000 |
| `desecrated.stat_2891184298` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T1` | -0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |
| `explicit.stat_2231156303` | 0.00000 |

### weapon.warstaff — n=789, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_210067635` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |

### weapon.staff — n=767, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_124131830` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T1` | 0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |

### armour.shield — n=734, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1568848828` | 0.00000 |
| `explicit.stat_1011760251` | 0.00000 |
| `explicit.stat_1011760251@T1` | -0.00000 |
| `explicit.stat_1011760251@T2` | 0.00000 |
| `explicit.stat_1062208444` | 0.00000 |
| `explicit.stat_1062208444@T1` | 0.00000 |
| `explicit.stat_1062208444@T2` | 0.00000 |
| `explicit.stat_1301765461` | 0.00000 |
| `explicit.stat_1301765461@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |

### armour.quiver — n=684, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1241625305` | 0.00000 |
| `explicit.stat_1241625305@T1` | 0.00000 |
| `explicit.stat_1241625305@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | -0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1573130764` | 0.00000 |
| `explicit.stat_1573130764@T1` | 0.00000 |
| `explicit.stat_1573130764@T2` | 0.00000 |
| `explicit.stat_1754445556` | 0.00000 |

### flask.charm — n=527, R²=-0.6625

intercept: `0.0002`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `-0.00002`  ·  corrupted: `0.19461`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457@T1` | -0.20709 |
| `explicit.stat_828533480@T2` | -0.06102 |
| `explicit.stat_1873752457` | 0.05040 |
| `explicit.stat_2541588185@T2` | -0.02091 |
| `explicit.stat_1873752457@T2` | -0.01003 |
| `explicit.stat_3849649145` | -0.01001 |
| `implicit.stat_1412682799` | 0.00104 |
| `implicit.stat_4010341289` | -0.00015 |
| `implicit.stat_3699444296` | -0.00014 |
| `implicit.stat_3310778564` | -0.00013 |
| `implicit.stat_1810482573` | -0.00011 |
| `implicit.stat_1691862754` | -0.00011 |

### weapon.twomace — n=492, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |
| `explicit.stat_1940865751` | 0.00000 |
| `explicit.stat_1940865751@T1` | 0.00000 |

## Coverage (listings per base)

- … **Emerald** — 2020 listings (2020 priced) [0.4–802.8 ex]
- … **Utility Belt** — 1931 listings (1931 priced) [0.3–11357.0 ex]
- … **Sapphire** — 1918 listings (1918 priced) [0.4–802.8 ex]
- … **Ruby** — 1578 listings (1578 priced) [0.3–802.8 ex]
- … **Stellar Amulet** — 1445 listings (1445 priced) [0.3–37188.0 ex]
- … **Dueling Wand** — 1369 listings (1369 priced) [0.8–802.8 ex]
- … **Solar Amulet** — 1108 listings (1108 priced) [1.0–802.8 ex]
- … **Obliterator Bow** — 1092 listings (1092 priced) [0.4–802.8 ex]
- … **Gold Amulet** — 1085 listings (1085 priced) [0.3–802.8 ex]
- … **Prismatic Ring** — 1032 listings (1032 priced) [0.3–802.8 ex]
- … **Amethyst Ring** — 1013 listings (1013 priced) [0.8–802.8 ex]
- … **Gold Ring** — 954 listings (954 priced) [0.7–802.8 ex]
- … **Plate Belt** — 941 listings (941 priced) [1.0–802.8 ex]
- … **Ancestral Tiara** — 875 listings (875 priced) [1.0–802.8 ex]
- … **Heavy Belt** — 874 listings (874 priced) [0.5–802.8 ex]
- … **Topaz Ring** — 823 listings (823 priced) [1.0–802.8 ex]
- … **Sapphire Ring** — 819 listings (819 priced) [0.5–802.8 ex]
- … **Galvanic Wand** — 795 listings (795 priced) [0.8–802.8 ex]
- … **Ruby Ring** — 794 listings (794 priced) [0.4–802.8 ex]
- … **Warmonger Bow** — 783 listings (783 priced) [0.9–802.8 ex]
- … **Siphoning Wand** — 771 listings (771 priced) [1.0–802.8 ex]
- … **Lapis Amulet** — 748 listings (748 priced) [0.6–802.8 ex]
- … **Jade Amulet** — 731 listings (731 priced) [0.3–802.8 ex]
- … **Attuned Wand** — 723 listings (723 priced) [0.3–802.8 ex]
- … **Amber Amulet** — 722 listings (722 priced) [0.3–802.8 ex]

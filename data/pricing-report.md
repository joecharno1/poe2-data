# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-05T15:17:16+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **170313** (170313 priced in exalted)
- Distinct bases: 908 · distinct mods: 2398 · mod rows: 807491
- Sold signals: **39006** sold · 88674 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-05T15:11:30+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.17** (median |log error| 1.9702)
- Within ±30% of asking price: **26%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 67% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×29.20 · ±30% 6% · n=22097
- Premium segment (60ex+): skill **+0.12** · typical error ×156.74 · ±30% 0% · n=12695
- Sold listings (clearing prices): skill **+0.02** · typical error ×33.97 · ±30% 28% · n=6280

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 3156 | ×7.76 | 4% | +0.02 | +0.03 |
| accessory.amulet | 3077 | ×7.88 | 5% | +0.02 | +0.03 |
| accessory.belt | 2678 | ×10.01 | 27% | +0.01 | +0.05 |
| jewel | 2623 | ×7.69 | 6% | +0.00 | +0.05 |
| armour.helmet | 2594 | ×8.86 | 21% | +0.03 | +0.09 |
| armour.chest | 2579 | ×8.85 | 25% | +0.03 | +0.08 |
| armour.gloves | 2400 | ×8.92 | 24% | +0.02 | +0.04 |
| armour.boots | 2380 | ×9.13 | 25% | +0.03 | +0.09 |
| other | 2354 | ×6.41 | 35% | +0.17 | +0.26 |
| weapon.wand | 1690 | ×9.20 | 30% | +0.05 | +0.11 |
| weapon.bow | 1411 | ×8.95 | 33% | +0.05 | +0.05 |
| weapon.crossbow | 1355 | ×8.76 | 27% | +0.08 | +0.11 |
| weapon.warstaff | 338 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.sceptre | 330 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.staff | 316 | ×1.00 | 100% | n/a | - |
| weapon.spear | 304 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.focus | 238 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 232 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.shield | 207 | ×1.00 | 99% | +0.00 | +0.00 |
| flask.charm | 175 | ×1.00 | 99% | -0.00 | +0.00 |
| weapon.twomace | 166 | ×1.00 | 96% | +0.00 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=20598, R²=-0.4386

intercept: `1.5587`  ·  log_price: True  ·  ilvl: `0.00281`  ·  n_mods: `0.04635`  ·  n_top_tier: `0.21308`  ·  corrupted: `0.36391`  ·  n_sockets: `-0.06474`  ·  quality: `-0.00709`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.40018 |
| `explicit.stat_2974417149@T1` | 0.31962 |
| `implicit.stat_3182714256` | 0.31057 |
| `implicit.stat_718638445` | 0.31049 |
| `implicit.stat_1379411836` | -0.30160 |
| `explicit.stat_1050105434@T1` | -0.30120 |
| `explicit.stat_2106365538@T1` | 0.24315 |
| `explicit.stat_2891184298@T1` | 0.22594 |
| `implicit.stat_958696139` | -0.21455 |
| `implicit.stat_4041853756` | 0.20848 |
| `implicit.stat_3879011313` | 0.20820 |
| `explicit.stat_124131830` | -0.20329 |

### accessory.ring — n=14373, R²=-1.5545

intercept: `4.6965`  ·  log_price: True  ·  ilvl: `-0.04341`  ·  n_mods: `-0.25949`  ·  n_top_tier: `-0.12770`  ·  corrupted: `1.08387`  ·  n_sockets: `3.28109`  ·  quality: `0.04693`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 3.00696 |
| `explicit.stat_1379411836@T1` | -2.28479 |
| `explicit.stat_3299347043@T1` | -2.08306 |
| `explicit.stat_707457662@T2` | 2.00231 |
| `explicit.stat_1379411836@T2` | -1.47708 |
| `explicit.stat_1573130764@T1` | -1.39825 |
| `explicit.stat_1754445556@T1` | 1.18510 |
| `explicit.stat_3032590688@T2` | 1.07355 |
| `explicit.stat_4067062424@T2` | 1.00010 |
| `explicit.stat_3299347043@T2` | -0.95458 |
| `explicit.stat_2901986750@T1` | 0.84621 |
| `explicit.stat_1263695895@T1` | 0.78312 |

### accessory.amulet — n=13944, R²=-1.345

intercept: `4.1515`  ·  log_price: True  ·  ilvl: `-0.03948`  ·  n_mods: `-0.18907`  ·  n_top_tier: `0.52190`  ·  corrupted: `0.59389`  ·  n_sockets: `-0.23236`  ·  quality: `-0.17114`

| stat_id | coef |
|---|---|
| `explicit.stat_2748665614@T1` | -2.91970 |
| `explicit.stat_983749596@T1` | -2.24910 |
| `explicit.stat_2748665614@T2` | -1.89734 |
| `explicit.stat_983749596@T2` | -1.84014 |
| `explicit.stat_1671376347@T2` | -1.31414 |
| `explicit.stat_3299347043@T1` | -1.23536 |
| `explicit.stat_3261801346@T1` | -1.22393 |
| `explicit.stat_3556824919@T2` | -1.20330 |
| `explicit.stat_4080418644@T2` | -1.19765 |
| `explicit.stat_4080418644@T1` | -1.14508 |
| `explicit.stat_1444556985@T1` | -1.13116 |
| `explicit.stat_1671376347@T1` | -1.11713 |

### jewel — n=13357, R²=-0.8147

intercept: `-1.2352`  ·  log_price: True  ·  ilvl: `0.03479`  ·  n_mods: `0.18000`  ·  n_top_tier: `-0.41629`  ·  corrupted: `0.40079`  ·  quality: `0.22312`

| stat_id | coef |
|---|---|
| `explicit.stat_1869147066@T1` | 4.21426 |
| `explicit.stat_1405298142@T1` | 3.49076 |
| `explicit.stat_3192728503@T1` | 3.26817 |
| `explicit.stat_3780644166@T1` | 3.04512 |
| `explicit.stat_3851254963@T1` | 2.89800 |
| `explicit.stat_3714003708@T1` | -2.78393 |
| `explicit.stat_872504239@T1` | -2.68239 |
| `explicit.stat_1316278494@T1` | -2.54288 |
| `explicit.stat_2106365538@T1` | -2.44129 |
| `explicit.stat_1569101201@T1` | 2.36881 |
| `explicit.stat_416040624@T1` | -2.26895 |
| `explicit.stat_101878827@T1` | 2.21895 |

### accessory.belt — n=12282, R²=-1.262

intercept: `3.7550`  ·  log_price: True  ·  ilvl: `-0.04519`  ·  n_mods: `-0.02880`  ·  n_top_tier: `0.11170`  ·  corrupted: `0.26210`  ·  n_sockets: `-0.12446`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.57742 |
| `explicit.stat_2923486259@T1` | 1.49774 |
| `explicit.stat_3299347043@T1` | -0.48857 |
| `explicit.stat_2923486259@T2` | 0.47806 |
| `explicit.stat_3299347043@T2` | -0.33125 |
| `explicit.stat_3372524247@T1` | 0.16544 |
| `explicit.stat_809229260@T2` | -0.14912 |
| `explicit.stat_1389754388@T1` | -0.14815 |
| `explicit.stat_3325883026@T1` | -0.14064 |
| `pseudo.total_ele_res>=80` | 0.13833 |
| `explicit.stat_1836676211@T2` | -0.13619 |
| `explicit.stat_915769802@T1` | -0.13595 |

### armour.chest — n=12029, R²=-1.3269

intercept: `4.0034`  ·  log_price: True  ·  ilvl: `-0.04943`  ·  n_mods: `-0.01799`  ·  n_top_tier: `0.30038`  ·  corrupted: `0.18049`  ·  n_sockets: `0.00003`  ·  quality: `0.00926`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.28974 |
| `explicit.stat_3981240776@T1` | 1.77163 |
| `explicit.stat_3981240776@T2` | 1.13283 |
| `explicit.stat_4015621042@T1` | -0.44860 |
| `explicit.stat_328541901@T1` | -0.41120 |
| `explicit.stat_2339757871@T1` | -0.37769 |
| `explicit.stat_4080418644@T2` | -0.37632 |
| `explicit.stat_4080418644@T1` | -0.37383 |
| `explicit.stat_1999113824@T1` | -0.36557 |
| `explicit.stat_4015621042@T2` | -0.36531 |
| `explicit.stat_328541901@T2` | -0.35329 |
| `explicit.stat_3325883026@T2` | -0.34992 |

### armour.helmet — n=11854, R²=-1.3607

intercept: `4.6431`  ·  log_price: True  ·  ilvl: `-0.05804`  ·  n_mods: `-0.02247`  ·  n_top_tier: `0.63135`  ·  corrupted: `0.64297`  ·  n_sockets: `-0.01032`  ·  quality: `0.03082`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.58938 |
| `explicit.stat_2339757871@T1` | -2.23306 |
| `explicit.stat_3033371881@T1` | -0.71860 |
| `explicit.stat_803737631@T2` | -0.71435 |
| `explicit.stat_3033371881@T2` | -0.70884 |
| `explicit.stat_4052037485@T2` | -0.70413 |
| `explicit.stat_53045048@T1` | -0.69517 |
| `explicit.stat_2162097452@T2` | -0.68628 |
| `explicit.stat_4015621042@T2` | -0.68109 |
| `explicit.stat_4015621042@T1` | -0.67976 |
| `explicit.stat_328541901@T2` | -0.67253 |
| `explicit.stat_3321629045@T1` | -0.66612 |

### armour.boots — n=11079, R²=-1.1481

intercept: `4.0322`  ·  log_price: True  ·  ilvl: `-0.04978`  ·  n_mods: `-0.02803`  ·  n_top_tier: `0.20952`  ·  corrupted: `0.11482`  ·  n_sockets: `0.01606`  ·  quality: `0.03278`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 2.04308 |
| `explicit.stat_4220027924@T1` | 0.73388 |
| `explicit.stat_2339757871@T1` | -0.70298 |
| `desecrated.stat_2250533757@T2` | -0.46037 |
| `rune.stat_836936635` | -0.32934 |
| `explicit.stat_3917489142@T2` | -0.30068 |
| `explicit.stat_3362812763@T1` | -0.29437 |
| `explicit.stat_99927264@T1` | -0.28988 |
| `explicit.stat_1062208444@T2` | -0.27778 |
| `explicit.stat_1671376347@T2` | -0.27373 |
| `explicit.stat_2923486259@T2` | -0.27303 |
| `explicit.stat_2160282525@T1` | -0.26409 |

### armour.gloves — n=10968, R²=-1.406

intercept: `4.2372`  ·  log_price: True  ·  ilvl: `-0.05393`  ·  n_mods: `0.00455`  ·  n_top_tier: `1.03672`  ·  corrupted: `-0.08905`  ·  n_sockets: `-0.00329`  ·  quality: `0.01188`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.18943 |
| `explicit.stat_2797971005@T1` | -1.24002 |
| `explicit.stat_9187492@T2` | -1.21259 |
| `explicit.stat_681332047@T2` | -1.19103 |
| `explicit.stat_2797971005@T2` | -1.18485 |
| `explicit.stat_124859000@T1` | -1.15352 |
| `explicit.stat_3032590688@T1` | -1.15073 |
| `explicit.stat_1573130764@T1` | -1.14149 |
| `explicit.stat_681332047@T1` | -1.13878 |
| `explicit.stat_803737631@T1` | -1.13134 |
| `explicit.stat_803737631@T2` | -1.12171 |
| `explicit.stat_4015621042@T1` | -1.11500 |

### weapon.wand — n=7900, R²=-1.6473

intercept: `3.5728`  ·  log_price: True  ·  ilvl: `-0.04462`  ·  n_mods: `-0.01401`  ·  n_top_tier: `0.41445`  ·  corrupted: `0.01628`  ·  n_sockets: `-0.00294`  ·  quality: `0.02187`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 3.34790 |
| `explicit.stat_591105508@T1` | 1.95113 |
| `explicit.stat_4226189338@T1` | 1.94946 |
| `explicit.stat_1545858329@T1` | 1.86367 |
| `explicit.stat_2254480358@T1` | 1.84945 |
| `explicit.stat_1600707273@T1` | 1.55220 |
| `explicit.stat_736967255@T2` | 1.43599 |
| `explicit.stat_1600707273@T2` | 1.22415 |
| `crafted.stat_124131830` | 0.89438 |
| `explicit.stat_2768835289@T2` | -0.53847 |
| `explicit.stat_737908626@T1` | -0.50175 |
| `explicit.stat_293638271@T2` | -0.49598 |

### weapon.bow — n=6609, R²=-1.6152

intercept: `3.5088`  ·  log_price: True  ·  ilvl: `-0.04362`  ·  n_mods: `-0.01748`  ·  n_top_tier: `0.34053`  ·  corrupted: `-0.06771`  ·  n_sockets: `0.00256`  ·  quality: `0.00076`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.93355 |
| `desecrated.stat_666077204@T1` | -2.25892 |
| `explicit.stat_2463230181@T1` | 1.97090 |
| `explicit.stat_1202301673@T1` | 1.87076 |
| `explicit.stat_1509134228@T1` | 1.82365 |
| `explicit.stat_518292764@T1` | 1.62347 |
| `crafted.stat_3035140377` | 1.59888 |
| `rune.stat_3885405204` | -0.83597 |
| `explicit.stat_55876295@T1` | -0.41951 |
| `explicit.stat_3261801346@T1` | -0.41251 |
| `explicit.stat_2694482655@T1` | -0.40067 |
| `explicit.stat_1037193709@T1` | -0.39498 |

### weapon.crossbow — n=6246, R²=-1.4599

intercept: `3.5012`  ·  log_price: True  ·  ilvl: `-0.04437`  ·  n_mods: `-0.00356`  ·  n_top_tier: `0.48673`  ·  corrupted: `0.01871`  ·  n_sockets: `0.00572`  ·  quality: `-0.00310`

| stat_id | coef |
|---|---|
| `explicit.stat_1509134228@T1` | 2.09611 |
| `explicit.stat_709508406@T1` | 1.71197 |
| `explicit.stat_1037193709@T1` | 1.69485 |
| `explicit.stat_1202301673@T1` | 1.57425 |
| `explicit.stat_2250681686@T2` | -1.48597 |
| `crafted.stat_3035140377` | 1.12464 |
| `explicit.stat_2250681686` | 1.01154 |
| `explicit.stat_691932474@T1` | -0.93334 |
| `rune.stat_2246411426` | -0.70791 |
| `rune.stat_55876295` | 0.69925 |
| `explicit.stat_1202301673@T2` | -0.62912 |
| `explicit.stat_669069897@T1` | -0.58068 |

### flask.charm — n=2014, R²=-0.1703

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `-0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457` | 0.00003 |
| `explicit.stat_2541588185@T2` | 0.00001 |
| `explicit.stat_2365392475@T2` | 0.00001 |
| `explicit.stat_2566921799` | 0.00001 |
| `explicit.stat_3196823591@T2` | 0.00001 |
| `explicit.stat_1366840608@T2` | 0.00001 |
| `explicit.stat_828533480@T2` | 0.00000 |
| `explicit.stat_3849649145` | -0.00000 |
| `explicit.stat_828533480@T1` | 0.00000 |
| `explicit.stat_1120862500@T2` | -0.00000 |
| `implicit.stat_4010341289` | -0.00000 |
| `explicit.stat_388617051@T2` | 0.00000 |

### weapon.warstaff — n=1594, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_1037193709` | 0.00000 |
| `desecrated.stat_1368271171` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_1940865751` | 0.00000 |
| `desecrated.stat_210067635` | 0.00000 |
| `desecrated.stat_2694482655` | 0.00000 |
| `desecrated.stat_3261801346` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |

### weapon.sceptre — n=1559, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1798257884` | 0.00000 |
| `desecrated.stat_1050105434` | 0.00000 |
| `desecrated.stat_3984865854` | 0.00000 |
| `explicit.stat_101878827` | 0.00000 |
| `explicit.stat_101878827@T1` | 0.00000 |
| `explicit.stat_101878827@T2` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_1250712710` | 0.00000 |
| `explicit.stat_1250712710@T1` | 0.00000 |
| `explicit.stat_1250712710@T2` | 0.00000 |

### weapon.staff — n=1508, R²=0.0

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

### weapon.spear — n=1404, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1202301673@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |

### armour.focus — n=1123, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1671376347` | 0.00000 |
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
| `explicit.stat_2231156303@T1` | 0.00000 |

### armour.quiver — n=1099, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1241625305` | 0.00000 |
| `desecrated.stat_3032590688` | 0.00000 |
| `desecrated.stat_3714003708` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1241625305` | 0.00000 |
| `explicit.stat_1241625305@T1` | 0.00000 |
| `explicit.stat_1241625305@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | -0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1573130764` | 0.00000 |

### armour.shield — n=972, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

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

### weapon.twomace — n=791, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |
| `explicit.stat_1940865751` | 0.00000 |

## Coverage (listings per base)

- … **Emerald** — 6692 listings (6692 priced) [0.7–856.7 ex]
- … **Sapphire** — 6648 listings (6648 priced) [0.6–856.7 ex]
- … **Ruby** — 5241 listings (5241 priced) [0.3–856.7 ex]
- … **Utility Belt** — 3793 listings (3793 priced) [0.3–4555741.7 ex]
- … **Stellar Amulet** — 2881 listings (2881 priced) [0.3–71255.5 ex]
- … **Prismatic Ring** — 2572 listings (2572 priced) [0.3–856.7 ex]
- … **Gold Amulet** — 2529 listings (2529 priced) [0.7–856.7 ex]
- … **Solar Amulet** — 2528 listings (2528 priced) [1.0–856.7 ex]
- … **Amethyst Ring** — 2446 listings (2446 priced) [0.8–856.7 ex]
- … **Dueling Wand** — 2434 listings (2434 priced) [1.0–856.7 ex]
- … **Gold Ring** — 2360 listings (2360 priced) [0.5–856.7 ex]
- … **Topaz Ring** — 1953 listings (1953 priced) [1.0–856.7 ex]
- … **Sapphire Ring** — 1929 listings (1929 priced) [0.9–856.7 ex]
- … **Ruby Ring** — 1882 listings (1882 priced) [0.6–856.7 ex]
- … **Obliterator Bow** — 1880 listings (1880 priced) [0.6–856.7 ex]
- … **Plate Belt** — 1880 listings (1880 priced) [1.0–856.7 ex]
- … **Heavy Belt** — 1784 listings (1784 priced) [0.5–856.7 ex]
- … **Lapis Amulet** — 1733 listings (1733 priced) [0.6–856.7 ex]
- … **Amber Amulet** — 1687 listings (1687 priced) [0.7–856.7 ex]
- … **Jade Amulet** — 1686 listings (1686 priced) [0.7–856.7 ex]
- … **Ancestral Tiara** — 1662 listings (1662 priced) [1.0–856.7 ex]
- … **Unset Ring** — 1538 listings (1538 priced) [1.0–856.7 ex]
- … **Bloodstone Amulet** — 1512 listings (1512 priced) [1.0–856.7 ex]
- … **Pearl Ring** — 1484 listings (1484 priced) [0.8–856.7 ex]
- … **Lunar Amulet** — 1477 listings (1477 priced) [0.8–856.7 ex]
